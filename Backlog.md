# Requisitos

A elicitação e priorização dos requisitos foram conduzidas utilizando duas metodologias ágeis complementares: o **User Story Mapping (USM)** e o método **MoSCoW**.

## User Story Mapping

O **User Story Mapping (USM)** foi empregado para visualizar a jornada completa do usuário na plataforma. Ele permitiu desdobrar o sistema em quatro **Temas** principais implementados (as grandes áreas de valor), mapear as **Atividades** do usuário dentro de cada Tema (os Épicos) e, finalmente, detalhar as **Histórias de Usuário (US)** implementadas. Essa estrutura hierárquica (Tema $\rightarrow$ Épico $\rightarrow$ US) é a base para o modelo de microserviços atual.a representa um potencial limite de serviço independente.

<!-- <div style="text-align: center;">
<iframe width="768" height="496" src="https://miro.com/app/live-embed/uXjVJCLJwuA=/?focusWidget=3458764642080634350&embedMode=view_only_without_ui&embedId=512092104204" frameborder="0" scrolling="no" allow="fullscreen; clipboard-read; clipboard-write" allowfullscreen></iframe>
</div> -->

### Temas Implementados
| N° | Tema                        | Descrição                          | Status |
|----|-----------------------------|------------------------------------|--------|
| 1  | Gerir Conta                 | Auth-Service + User-Service        | **Implementado** |
| 2  | Explorar Catálogo           | Media-Service                      | **Implementado** |
| 3  | Avaliar Mídia               | Rating-Review-Service              | **Implementado** |
| 4  | Interagir com a Comunidade  | User-Service + Rating-Review-Service | 🔄 **Parcialmente Implementado** |

### Temas Não Implementados
| N° | Tema                        | Descrição                          | Status |
|----|-----------------------------|------------------------------------|--------|
| 3  | Reproduzir Mídia            | Player Service                     | ⏸️ **Não Implementado** |
| 4  | Organizar Mídia             | Playlist Service                   | ⏸️ **Não Implementado** |

### Épicos Implementados

<table style="width:100%; border-collapse: collapse; color: #f0f0f0; background-color: #1e1e1e;">
  <thead>
    <tr>
      <th style="border: 1px solid #444; padding: 12px; text-align: center; width: 5%; background-color: #2c2c2c;">N°</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 35%; background-color: #2c2c2c;">Tema</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 35%; background-color: #2c2c2c;">Épico</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: center; width: 25%; background-color: #2c2c2c;">Status de Implementação</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px; text-align: center;">1</td>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Gerir Conta</td>
      <td style="border: 1px solid #444; padding: 12px;">Registrar-se e autenticar-se</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar conta</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Editar conta</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Excluir conta</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px; text-align: center;">2</td>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Explorar Catálogo</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar mídia</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Aplicar filtro / ordenação</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Detalhes da Mídia</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Explorar artista</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td rowspan="1" style="border: 1px solid #444; padding: 12px; text-align: center;">3</td>
      <td rowspan="1" style="border: 1px solid #444; padding: 12px;">Organizar Mídia</td>
      <td style="border: 1px solid #444; padding: 12px;">Marcar como Favorito</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px; text-align: center;">4</td>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Avaliar Mídia</td>
      <td style="border: 1px solid #444; padding: 12px;">Avaliar mídia (Songs)</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Avaliar álbum</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Ver estatísticas dos reviews</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px; text-align: center;">5</td>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Interagir com a Comunidade</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar usuário</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Perfil do Usuário</td>
      <td style="border: 1px solid #444; padding: 12px; text-align: center;">Completo</td>
    </tr>
  </tbody>
</table>


### MVP

<table style="width:100%; border-collapse: collapse; color: #f0f0f0; background-color: #1e1e1e;">
  <thead>
    <tr>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 15%; background-color: #2c2c2c;">Tema</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 25%; background-color: #2c2c2c;">Épico</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: center; width: 5%; background-color: #2c2c2c;">N°</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 55%; background-color: #2c2c2c;">Requisito</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px;">Gerir Conta</td>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Registrar-se e autenticar-se</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 1</td>
      <td style="border: 1px solid #444; padding: 12px;">Criar conta</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 2</td>
      <td style="border: 1px solid #444; padding: 12px;">Realizar login com usuário e senha</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar conta</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 3</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar dados do perfil</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Editar conta</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 4</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar dados do perfil</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Excluir conta</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 5</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir conta do perfil</td>
    </tr>
    <tr>
      <td rowspan="13" style="border: 1px solid #444; padding: 12px;">Explorar Catálogo</td>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Buscar mídia</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 6</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar mídia por nome</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 7</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar mídia por artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 8</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar álbum</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Aplicar filtro / ordenação</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 9</td>
      <td style="border: 1px solid #444; padding: 12px;">Filtrar pesquisa por gênero</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 10</td>
      <td style="border: 1px solid #444; padding: 12px;">Filtrar pesquisa por nota</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 11</td>
      <td style="border: 1px solid #444; padding: 12px;">Ordenar pesquisa por nome</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 12</td>
      <td style="border: 1px solid #444; padding: 12px;">Ordenar pesquisa por nota</td>
    </tr>
    <tr>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Visualizar Detalhes da Mídia</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 13</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar dados básicos da mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 14</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar nota da mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 15</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar reviews de outros usuários em mídia</td>
    </tr>
    <tr>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Explorar artista</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 16</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 17</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar perfil do artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 18</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver estatísticas do artista</td>
    </tr>
    <tr>
      <td rowspan="9" style="border: 1px solid #444; padding: 12px;">Reproduzir Mídia</td>
      <td style="border: 1px solid #444; padding: 12px;">Iniciar e pausar mídia</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 20</td>
      <td style="border: 1px solid #444; padding: 12px;">Controlar reprodução da mídia</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Controlar volume / tempo</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 21</td>
      <td style="border: 1px solid #444; padding: 12px;">Ajustar volume da mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 22</td>
      <td style="border: 1px solid #444; padding: 12px;">Ajustar linha do tempo da mídia</td>
    </tr>
        <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Exibir letra</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 23</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar letra da mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 24</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar tradução da letra da mídia</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Gerenciar fila de reprodução</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 25</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver fila de reprodução</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 26</td>
      <td style="border: 1px solid #444; padding: 12px;">Adicionar mídia à fila de reprodução</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 27</td>
      <td style="border: 1px solid #444; padding: 12px;">Remover mídia de fila de reprodução</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 28</td>
      <td style="border: 1px solid #444; padding: 12px;">Alterar ordem de mídia na fila de reprodução</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Organizar Mídia</td>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Marcar como Favorito</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 29</td>
      <td style="border: 1px solid #444; padding: 12px;">Marcar/Desmarcar mídia como favorita</td>
    </tr>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 30</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar suas mídias favoritas</td>
    </tr>
    <tr>
      <td rowspan="15" style="border: 1px solid #444; padding: 12px;">Avaliar Mídia</td>
      <td rowspan="6" style="border: 1px solid #444; padding: 12px;">Avaliar mídia</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 31</td>
      <td style="border: 1px solid #444; padding: 12px;">Cadastrar nota de mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 32</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar nota dada em mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 33</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir nota de mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 34</td>
      <td style="border: 1px solid #444; padding: 12px;">Publicar review de mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 35</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar review de mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 36</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir review de mídia</td>
    </tr>
    <tr>
      <td rowspan="6" style="border: 1px solid #444; padding: 12px;">Avaliar álbum</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 37</td>
      <td style="border: 1px solid #444; padding: 12px;">Cadastrar nota de álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 38</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar nota dada em álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 39</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir nota de álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 40</td>
      <td style="border: 1px solid #444; padding: 12px;">Publicar review de álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 41</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar review de álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 42</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir review de álbum</td>
    </tr>
    <tr>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Ver estatísticas dos reviews</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 43</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver nota média de mídia específica</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 44</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver nota média do artista de acordo com suas mídias</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 45</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver nota média de álbums de um artista</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Interagir com a Comunidade</td>
      <td style="border: 1px solid #444; padding: 12px;">Interagir com reviews</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 46</td>
      <td style="border: 1px solid #444; padding: 12px;">Curtir reviews</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Buscar usuário</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 47</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar usuário por nome de usuário</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 48</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar usuário por nome</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Perfil do Usuário</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 49</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar perfil de usuário</td>
    </tr>
  </tbody>
</table>

### Product Backlog

<table style="width:100%; border-collapse: collapse; color: #f0f0f0; background-color: #1e1e1e;">
  <thead>
    <tr>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 15%; background-color: #2c2c2c;">Tema</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 25%; background-color: #2c2c2c;">Épico</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: center; width: 5%; background-color: #2c2c2c;">N°</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 55%; background-color: #2c2c2c;">Requisito</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Gerir Conta</td>
      <td style="border: 1px solid #444; padding: 12px;">Registrar-se e autenticar-se</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 50</td>
      <td style="border: 1px solid #444; padding: 12px;">Realizar login utilizando provedores externos</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar conta</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 51</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar foto de perfil</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Editar conta</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 52</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar foto de perfil</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 53</td>
      <td style="border: 1px solid #444; padding: 12px;">Remover foto do perfil</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Explorar Catálogo</td>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Ver Recomendações</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 54</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver playlist de músicas ouvidas recentemente como sugestão</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 55</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver mídias lançadas recentemente por artistas que sigo</td>
    </tr>
    <tr>
      <td rowspan="1" style="border: 1px solid #444; padding: 12px;">Buscar mídia</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 56</td>
      <td style="border: 1px solid #444; padding: 12px;">Buscar playlist</td>
    </tr>
    <tr>
      <td rowspan="1" style="border: 1px solid #444; padding: 12px;">Explorar Artista</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 19</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar reviews de artista escritos por outros usuários</td>
    </tr>
    <tr>
      <td rowspan="1" style="border: 1px solid #444; padding: 12px;">Reproduzir mídia</td>
      <td rowspan="1" style="border: 1px solid #444; padding: 12px;">Exibir letra</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 57</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar letra em tempo real (timestamp)</td>
    </tr>
    <tr>
      <td rowspan="10" style="border: 1px solid #444; padding: 12px;">Organizar Mídia</td>
        <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Criar playlist</td>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 58</td>
        <td style="border: 1px solid #444; padding: 12px;">Criar uma playlist</td>
    </tr>
    <tr>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 59</td>
        <td style="border: 1px solid #444; padding: 12px;">Renomear playlist</td>
    </tr>
    <tr>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 60</td>
        <td style="border: 1px solid #444; padding: 12px;">Excluir playlist</td>
    </tr>
    <tr>
        <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Gerenciar mídia em playlist</td>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 61</td>
        <td style="border: 1px solid #444; padding: 12px;">Adicionar mídia à playlist</td>
    </tr>
    <tr>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 62</td>
        <td style="border: 1px solid #444; padding: 12px;">Remover mídia de playlist</td>
    </tr>
    <tr>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 63</td>
        <td style="border: 1px solid #444; padding: 12px;">Alterar ordem de mídia em playlist</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Definir privacidade</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 64</td>
      <td style="border: 1px solid #444; padding: 12px;">Definir playlist como pública ou privada</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 65</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar suas playlists privadas</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Marcar como Favorito</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 66</td>
      <td style="border: 1px solid #444; padding: 12px;">Marcar/Desmarcar playlist como favorita</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 67</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar suas playlists favoritas</td>
    </tr>
    <tr>
      <td rowspan="21" style="border: 1px solid #444; padding: 12px;">Avaliar mídia</td>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Avaliar mídia</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 68</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar nota de mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 69</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar review de mídia</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Avaliar álbum</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 70</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar nota de álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 71</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar review de álbum</td>
    </tr>
    <tr>
        <td rowspan="8" style="border: 1px solid #444; padding: 12px;">Avaliar playlist</td>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 72</td>
        <td style="border: 1px solid #444; padding: 12px;">Cadastrar nota de playlist</td>
    </tr>
    <tr>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 73</td>
        <td style="border: 1px solid #444; padding: 12px;">Visualizar nota dada em playlist</td>
    </tr>
    <tr>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 74</td>
        <td style="border: 1px solid #444; padding: 12px;">Excluir nota de playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 75</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar nota de playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 76</td>
      <td style="border: 1px solid #444; padding: 12px;">Publicar review de playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 77</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar review de playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 78</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar review de playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 79</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir review de playlist</td>
    </tr>
    <tr>
      <td rowspan="8" style="border: 1px solid #444; padding: 12px;">Avaliar artista</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 80</td>
      <td style="border: 1px solid #444; padding: 12px;">Publicar review de artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 81</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar review de artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 82</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar review de artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 83</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir review de artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 84</td>
      <td style="border: 1px solid #444; padding: 12px;">Cadastrar nota de artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 85</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar nota dada para artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 86</td>
      <td style="border: 1px solid #444; padding: 12px;">Editar nota dada para artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 87</td>
      <td style="border: 1px solid #444; padding: 12px;">Excluir nota de artista</td>
    </tr>
    <tr>
        <td rowspan="1" style="border: 1px solid #444; padding: 12px;">Ver estatísticas dos reviews</td>
        <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 88</td>
        <td style="border: 1px solid #444; padding: 12px;">Ver nota média de playlist com base nas mídias que ela possui</td>
    </tr>
    <tr>
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Interagir com a Comunidade</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Feed</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 89</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver reviews de usuários seguidos</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Interagir com reviews</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 90</td>
      <td style="border: 1px solid #444; padding: 12px;">Comentar reviews</td>
    </tr>
    <tr>
      <td rowspan="2" style="border: 1px solid #444; padding: 12px;">Seguir / Deixar de Seguir</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 91</td>
      <td style="border: 1px solid #444; padding: 12px;">Seguir / deixar de seguir artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Seguir / Deixar de Seguir</td>
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 92</td>
      <td style="border: 1px solid #444; padding: 12px;">Seguir / deixar de seguir usuário</td>
    </tr>
  </tbody>
</table>

## Status de Implementação das Funcionalidades

O desenvolvimento foi focado nos requisitos essenciais para criar um **MVP funcional** com as principais funcionalidades do LyricBox. A tabela abaixo mostra o **status atual de implementação** das User Stories planejadas:

**Legenda de Status:**
* **IMPLEMENTADO:** Funcionalidade totalmente desenvolvida e testada
* 🔄 **PARCIALMENTE IMPLEMENTADO:** Funcionalidade básica implementada, mas com limitações
* ⏸️ **NÃO IMPLEMENTADO:** Funcionalidade não desenvolvida (fora do escopo atual)
* ⚠️ **DEPENDÊNCIA:** Funcionalidade dependente de outras não implementadas

O foco atual contempla: **Gestão de Usuários**, **Catálogo Musical**, **Sistema de Avaliações** e **Funcionalidades Sociais Básicas**.

| N°        | História de Usuário | Status | Implementação |
| :---:     | :--- | :---: | :--- |
| **US 1**  | Criar conta | | Auth-Service + User-Service |
| **US 2**  | Realizar login com usuário e senha | | Auth-Service com JWT |
| **US 3**  | Visualizar dados do perfil | | User-Service `/users/me` |
| **US 4**  | Editar dados do perfil | | User-Service `PUT /users/me` |
| **US 5**  | Excluir conta do perfil | | User-Service `DELETE /users/me` |
| **US 6**  | Buscar mídia por nome | | Media-Service `/songs/search` |
| **US 7**  | Buscar mídia por artista | | Media-Service `/songs/by-artist` |
| **US 8**  | Buscar álbum | | Media-Service `/albums/search` |
| **US 11** | Ordenar pesquisa por nome | 🔄 | Via query params `sort=name,asc/desc` |
| **US 12** | Ordenar pesquisa por nota | 🔄 | Rating-Service `/ratings/songs/order-by-rating` |
| **US 13** | Visualizar dados básicos da mídia | | Media-Service `/songs/{id}` |
| **US 14** | Visualizar nota da mídia | | Rating-Service `/ratings/song/{id}/average` |
| **US 15** | Visualizar reviews de outros usuários em mídia | | Rating-Service `/reviews/song/{id}` |
| **US 16** | Buscar artista | | Media-Service `/artists/search` |
| **US 17** | Visualizar perfil do artista | | Media-Service `/artists/{id}` |
| **US 18** | Ver estatísticas do artista | | Media-Service `/artists/{id}/stats` + Rating-Service |
| **US 29** | Marcar/Desmarcar mídia como favorita | | Media-Service `POST /songs/{id}/favorite` |
| **US 30** | Visualizar suas mídias favoritas | | Media-Service `/songs/favorites` |
| **US 31** | Cadastrar nota de mídia | | Rating-Service `POST /ratings` |
| **US 32** | Visualizar nota dada em mídia | | Rating-Service `/ratings/my-rating/{songId}` |
| **US 33** | Excluir nota de mídia | | Rating-Service `DELETE /ratings/{songId}` |
| **US 34** | Publicar review de mídia | | Rating-Service `POST /reviews` |
| **US 35** | Visualizar review de mídia | | Rating-Service `/reviews/my-review/{songId}` |
| **US 36** | Excluir review de mídia | | Rating-Service `DELETE /reviews/{songId}` |
| **US 43** | Ver nota média de mídia específica | | Rating-Service `/ratings/song/{id}/average` |
| **US 44** | Ver nota média do artista de acordo com suas mídias | | Rating-Service `/ratings/artist/{id}/average` |
| **US 45** | Ver nota média de álbums de um artista | | Rating-Service `/ratings/album/{id}/average` |
| **US 47** | Buscar usuário por nome de usuário | | User-Service `/users/search` |
| **US 48** | Buscar usuário por nome | | User-Service `/users/search` |
| **US 49** | Visualizar perfil de usuário | | User-Service `/users/{id}` (admin) |
| **US 9**  | Filtrar pesquisa por gênero | ⚠️ | Requer implementação de gêneros no Media-Service |
| **US 10** | Filtrar pesquisa por nota | 🔄 | Rating-Service `/ratings/songs/filter-by-rating` |
| **US 37** | Cadastrar nota de álbum | ⚠️ | Depende de avaliação direta de álbuns |
| **US 38** | Visualizar nota dada em álbum | ⚠️ | Depende de avaliação direta de álbuns |
| **US 39** | Excluir nota de álbum | ⚠️ | Depende de avaliação direta de álbuns |
| **US 40** | Publicar review de álbum | ⚠️ | Depende de review direto de álbuns |
| **US 41** | Visualizar review de álbum | ⚠️ | Depende de review direto de álbuns |
| **US 42** | Excluir review de álbum | ⚠️ | Depende de review direto de álbuns |
| **US 20** | Controlar reprodução da mídia | ⏸️ | Player não implementado |
| **US 21** | Ajustar volume da mídia | ⏸️ | Player não implementado |
| **US 22** | Ajustar linha do tempo da mídia | ⏸️ | Player não implementado |
| **US 23** | Visualizar letra da mídia | ⏸️ | Campo lyrics não implementado |
| **US 24** | Visualizar tradução da letra da mídia | ⏸️ | Feature de tradução não implementada |
| **US 25** | Ver fila de reprodução | ⏸️ | Player não implementado |
| **US 26** | Adicionar mídia à fila de reprodução | ⏸️ | Player não implementado |
| **US 27** | Remover mídia de fila de reprodução | ⏸️ | Player não implementado |
| **US 28** | Alterar ordem de mídia na fila de reprodução | ⏸️ | Player não implementado |
| **US 46** | Curtir reviews | ⏸️ | Sistema de likes não implementado |

## Requisitos Não Funcionais

| N°    | Requisito                                                                                                                 |
| :---: | :------------------------------------------------------------------------------------------------------------------------ |
| RNF 1 | O sistema deve ser **responsivo**, adaptando-se a telas mobile (largura de 375px) e desktop, sem perda de funcionalidade. |
| RNF 2 | O player deve ter latência de resposta menor que **150ms** ao receber comandos (play/pause).                              |
| RNF 3 | A busca deve retornar resultados em menos de **2 segundos** (tempo de resposta) para até 10.000 registros no catálogo.    |
| RNF 4 | A senha do usuário deve ser armazenada com **hashing** e não deve ser recuperável em texto simples.                       |
