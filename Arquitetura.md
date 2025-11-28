# Arquitetura do Sistema

## Visão Geral da Arquitetura

O **LyricBox** é implementado utilizando uma **Arquitetura de Microserviços**, onde cada serviço tem responsabilidades específicas e se comunica através de APIs REST. O sistema foi projetado seguindo os princípios de **Domain-Driven Design (DDD)** e **Separation of Concerns**.

### PRINCIPAIS CARACTERÍSTICAS ARQUITETURAIS

- **Arquitetura de Microserviços**: Serviços independentes e especializados
- **Comunicação Síncrona**: APIs REST com protocolo HTTP/HTTPS
- **Autenticação/Autorização**: JWT (JSON Web Tokens) distribuído
- **Banco de Dados**: Padrão Database-per-Service com MySQL
- **Containerização**: Docker para todos os serviços
- **Frontend**: Single Page Application (SPA) em React/TypeScript

## Identificação dos Microserviços

### **AUTH-SERVICE** (Porta 8080)
**Responsabilidade:** Autenticação e autorização de usuários
- **Contexto de Domínio:** Security & Authentication
- **Base Path:** `/api/auth`
- **Banco de Dados:** Stateless (utiliza User-Service via HTTP)

### **USER-SERVICE** (Porta 8083)  
**Responsabilidade:** Gerenciamento de usuários e perfis
- **Contexto de Domínio:** User Management
- **Base Path:** `/users`
- **Banco de Dados:** `lyricbox_user_db`

### **MEDIA-SERVICE** (Porta 8081)
**Responsabilidade:** Gerenciamento do catálogo musical (artistas, álbuns, músicas)
- **Contexto de Domínio:** Media Catalog & Content Management
- **Base Path:** `/api/media`
- **Banco de Dados:** `lyricbox_media_db`

### **RATING-REVIEW-SERVICE** (Porta 8082)
**Responsabilidade:** Sistema de avaliações e reviews
- **Contexto de Domínio:** User Engagement & Feedback
- **Base Path:** `/api/rating`
- **Banco de Dados:** `lyricbox_rating_db`

<!-- ### **FRONTEND** (Porta 3000)
**Responsabilidade:** Interface de usuário e experiência do cliente
- **Tecnologia:** React + TypeScript + Tailwind CSS
- **Arquitetura:** Single Page Application (SPA) -->

## Interações Entre Microserviços

### **FLUXO DE AUTENTICAÇÃO**

```
1. Frontend → Auth-Service: POST /api/auth/register
2. Auth-Service → User-Service: POST /users/register
3. User-Service → Auth-Service: UserResponseDto
4. Auth-Service → Frontend: UserResponseDto (201 Created)

5. Frontend → Auth-Service: POST /api/auth/login  
6. Auth-Service → User-Service: GET /users/auth/login-data?identifier={username/email}
7. User-Service → Auth-Service: UserLoginDto (id, username, email, password, role)
8. Auth-Service → Frontend: JwtResponseDto (token, user info)
```

### **FLUXO DE BUSCA E CONSUMO DE MÍDIA**

```
1. Frontend → Media-Service: GET /api/media/songs/search?q={query}
2. Media-Service → Frontend: Page<SongResponseDto>

3. Frontend → Media-Service: GET /api/media/songs/{id}
4. Media-Service → Frontend: SongResponseDto

5. Frontend → Rating-Review-Service: GET /api/rating/song/{songId}/average
6. Rating-Review-Service → Frontend: AverageRatingDto
```

### **FLUXO DE AVALIAÇÃO E REVIEW**

```
1. Frontend → Rating-Review-Service: POST /api/rating/ratings (JWT Required)
2. Rating-Review-Service → Frontend: RatingResponseDto

3. Frontend → Rating-Review-Service: POST /api/rating/reviews (JWT Required) 
4. Rating-Review-Service → Frontend: ReviewResponseDto
```

### **FLUXO DE FAVORITOS**

```
1. Frontend → Media-Service: POST /api/media/songs/{id}/favorite (JWT Required)
2. Media-Service → Frontend: 200 OK

3. Frontend → Media-Service: GET /api/media/songs/favorites (JWT Required)
4. Media-Service → Frontend: List<SongResponseDto>
```

## Padrões Arquiteturais Implementados

### **1. API GATEWAY PATTERN (Implícito)**
Cada microserviço expõe suas próprias APIs REST com contextos específicos:
- `/api/auth/*` → Auth-Service
- `/users/*` → User-Service  
- `/api/media/*` → Media-Service
- `/api/rating/*` → Rating-Review-Service

### **2. DATABASE PER SERVICE**
Cada microserviço possui seu próprio banco de dados MySQL:
- **User-Service:** `lyricbox_user_db` 
- **Media-Service:** `lyricbox_media_db`
- **Rating-Review-Service:** `lyricbox_rating_db`
- **Auth-Service:** Stateless (não possui banco próprio)

### **3. CIRCUIT BREAKER PATTERN**
Implementado através de clients HTTP com tratamento de exceções:
- `UserServiceClient` no Auth-Service
- Tratamento de `WebClientResponseException`

### **4. DISTRIBUTED AUTHENTICATION**
JWT é validado de forma independente em cada microserviço:
- Chave secreta compartilhada: `JWT_SECRET`
- Filtros de autenticação: `JwtAuthenticationFilter`
- Validação local: `JwtUtil`

## Segurança e Autorização

### **NÍVEIS DE ACESSO**

#### **🌐 ENDPOINTS PÚBLICOS**
- Busca de músicas, artistas, álbuns
- Visualização de estatísticas de rating
- Busca de usuários por nome
- Registro de usuário via Auth-Service

#### **🔒 ENDPOINTS AUTENTICADOS (JWT Required)**
- Gerenciamento de perfil pessoal
- Sistema de favoritos
- Criação/edição de ratings e reviews
- Visualização de dados pessoais

#### **👑 ENDPOINTS DE ADMINISTRADOR (ADMIN Role)**
- Criação/edição/remoção de conteúdo musical
- Gerenciamento de usuários (CRUD completo)
- Acesso a dados administrativos

### **FLUXO DE AUTORIZAÇÃO JWT**

```
1. Client → Auth-Service: POST /api/auth/login
2. Auth-Service: Valida credenciais + Gera JWT
3. Client: Armazena JWT no localStorage/sessionStorage

4. Client → Any-Service: Request + "Authorization: Bearer {JWT}"
5. Any-Service: Valida JWT + Extrai userId/role
6. Any-Service: Executa business logic + Response
```

## Tecnologias e Ferramentas

### **BACKEND (MICROSERVIÇOS)**
- **Framework:** Spring Boot 3.x
- **Linguagem:** Java 17+
- **Banco de Dados:** MySQL 8.0
- **ORM:** Spring Data JPA + Hibernate
- **Segurança:** Spring Security + JWT
- **Documentação:** OpenAPI 3 (Swagger)
- **Build:** Maven
- **Containerização:** Docker + Docker Compose

### **FRONTEND**
- **Framework:** React 18+ com TypeScript
- **Build Tool:** Vite
- **Estilização:** Tailwind CSS
- **Componentes:** Shadcn/ui
- **Gerenciamento de Estado:** Context API
- **HTTP Client:** Axios/Fetch API

### **INFRAESTRUTURA**
- **Containerização:** Docker
- **Orquestração:** Docker Compose
- **Banco de Dados:** MySQL (containers separados por serviço)
- **Reverse Proxy:** Nginx (no frontend)

## Escalabilidade e Manutenibilidade

### **VANTAGENS DA ARQUITETURA**

#### **Escalabilidade Horizontal**
- Cada microserviço pode ser escalado independentemente
- Load balancing pode ser aplicado por serviço conforme demanda
- Banco de dados separado permite otimização específica por domínio

#### **Manutenibilidade**
- **Separation of Concerns:** Cada serviço tem responsabilidade bem definida
- **Independent Deployment:** Deploy independente por microserviço
- **Technology Diversity:** Possibilidade de usar diferentes stacks por serviço

#### **Resiliência**
- **Fault Isolation:** Falha em um serviço não afeta outros diretamente
- **Circuit Breaker:** Proteção contra cascade failures
- **Stateless Design:** Auth-Service não possui estado próprio

### **CONSIDERAÇÕES DE DEPLOYMENT**

#### **Ambiente de Desenvolvimento**
```bash
# Cada serviço pode ser executado independentemente
./start_auth_service.sh
./start_user_service.sh  
# etc...
```

#### **Ambiente de Produção**
- Utilização de **Docker Compose** para orquestração
- **Health Checks** configurados via Spring Actuator
- **Environment Variables** para configuração externa
- **Reverse Proxy** (Nginx) para roteamento de requests

### **COMUNICAÇÃO ENTRE SERVIÇOS**

| Origem | Destino | Tipo | Propósito |
|--------|---------|------|-----------|
| Auth-Service | User-Service | HTTP/REST | Criação de usuário e validação de login |
| Frontend | Auth-Service | HTTP/REST | Autenticação e autorização |
| Frontend | User-Service | HTTP/REST | Gestão de perfil |
| Frontend | Media-Service | HTTP/REST | Catálogo musical e favoritos |
| Frontend | Rating-Review-Service | HTTP/REST | Avaliações e reviews |
