1. Estratégias para Contornar Direitos Autorais (Foco em Ambiente Acadêmico)
Para um projeto universitário onde o objetivo é a arquitetura e o desenvolvimento, e não o lançamento comercial, você tem algumas abordagens para evitar problemas legais:

A. Foco em Conteúdo Não Protegido
Músicas e Letras de Domínio Público: Concentre-se em músicas cujos direitos autorais expiraram (geralmente 70 anos após a morte do autor, dependendo do país). Isso é comum para músicas clássicas, folclóricas antigas ou religiosas.

Artistas Independentes (Licença Aberta): Use músicas de artistas que distribuem seu trabalho sob licenças abertas (como Creative Commons). Isso é perfeito para simular o "mundo real" sem custo de licenciamento.

Conteúdo Autoral: Você e seus colegas podem escrever as próprias músicas e letras. Isso garante 100% dos direitos e é uma ótima forma de preencher o banco de dados.

B. Mantenha os Dados Abstratos
Não Use Arquivos Reais: No seu projeto, você pode simular a reprodução de áudio. Por exemplo, a classe Musica armazena apenas metadados (nome, artista, letra), e você não precisa incluir o arquivo MP3/MP4 real.

Foque na Sincronização: O desafio técnico está em mostrar a letra no momento correto. Foque em desenvolver a lógica de sincronização de letras (timestamping) usando arquivos de metadados simples (como um arquivo LRC, que mapeia frases a segundos), e não o áudio em si.



Sim, há uma diferença crucial entre Playlist e Álbum, tanto conceitualmente quanto na forma como você deve modelar seu sistema.

A principal distinção reside na autoria e permanência do conteúdo.

1. Diferença Conceitual
Característica	Playlist	Álbum
Autoria	Criada e organizada por um Usuário ou um Curador (ou uma entidade de serviço, como o Spotify).	Criado e definido por um Artista ou uma Gravadora.
Conteúdo	É uma coleção pessoal ou temática. Pode misturar músicas de vários artistas e álbuns.	É uma coleção oficial e fixa de mídias de um ou poucos Artistas.
Permanência	É volátil e mutável. O usuário pode adicionar, remover e reordenar itens a qualquer momento.	É estável e imutável (após o lançamento). A ordem e o conteúdo são definitivos.
Propósito	Organização, humor, curadoria, compartilhamento social.	Lançamento oficial, conceito artístico, registro histórico do trabalho do Artista.

Exportar para as Planilhas
No seu sistema, a Playlist é uma entidade de curadoria do usuário. O Álbum é uma entidade de catálogo e metadados, ligada à entidade Artista.

2. Documentação nos Requisitos (User Stories)
Como você está focando no valor do usuário, documente as diferenças no uso:

Requisitos para o Álbum (Explorar Catálogo)
O foco é a descoberta e os metadados.

US: Como um usuário, eu quero buscar mídias agrupadas por Álbum, para que eu possa encontrar todos os sons de um lançamento específico.

US: Como um usuário, eu quero visualizar a capa e o ano de lançamento de um Álbum, para que eu tenha o contexto histórico e visual daquele conjunto de mídias.

US: Como um curador, eu quero ver a nota média de todas as mídias de um Álbum, para que eu possa avaliar a obra completa do artista.

Requisitos para a Playlist (Organizar Mídia)
O foco é a criação e o controle.

US: Como um usuário, eu quero adicionar mídias de diferentes Álbuns e Artistas à minha Playlist, para que eu possa criar coleções temáticas e pessoais.

US: Como um usuário, eu quero reordenar as mídias dentro da minha Playlist, para que eu possa definir a sequência exata de reprodução.

US: Como um usuário, eu quero tornar minha Playlist pública ou privada, para que eu possa controlar quem acessa minha curadoria.

3. Modelagem UML e Banco de Dados
Você deve adicionar uma nova classe (Album) ao seu Diagrama UML e mapear as relações de forma clara.

Atualização do Diagrama UML (Modelagem de Domínio)
Você precisará da nova classe Album e ajustar a classe Musica:

Classe Album:

nome: String

anoLancamento: int

artistaPrincipal: Artista (associação 1:1, ou 1:* se for colaborativo)

Relação Musica e Album:

Uma Música pertence a exatamente um Álbum (ou 0 se for um single ou faixa avulsa).

Um Álbum contém uma ou mais Músicas.

Snippet de código

classDiagram
    class Artista{
        - nome : String
    }
    class Musica{
        - nome : String
    }
    class Album{
        - nome : String
        - anoLancamento : int
    }
    class Playlist{
        - nome : String
    }
    
    Artista "1" -- "0..*" Album : possui
    Album "1" -- "1..*" Musica : contém
    
    Playlist "1" -- "0..*" Musica : contém (pode ser repetida)
Modelagem de Banco de Dados (Esquema Básico)
Seu microserviço de Catálogo (onde Álbum e Música residem) usaria a seguinte estrutura de tabelas:

Tabela Artista:

id_artista (PK)

nome

Tabela Album:

id_album (PK)

nome

ano_lancamento

id_artista (FK para Artista.id_artista)

Tabela Midia (ou Musica):

id_midia (PK)

titulo

duracao

id_album (FK para Album.id_album) (Permite NULL para singles)

Tabela Playlist (Microserviço de Playlist):

id_playlist (PK)

nome

id_usuario (FK para o Usuario)

privacidade (pública/privada)

Tabela Playlist_Midia (Associação N:N):

id_playlist (PK, FK)

id_midia (PK, FK)

ordem (Int) <-- Essencial para manter a ordem definida pelo usuário!