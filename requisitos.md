# Requisitos

A elicitação e priorização dos requisitos foram conduzidas utilizando duas metodologias ágeis complementares: o **User Story Mapping (USM)** e o método **MoSCoW**.

## User Story Mapping

O **User Story Mapping (USM)** foi empregado para visualizar a jornada completa do usuário na plataforma. Ele permitiu desdobrar o sistema em seis **Temas** principais (as grandes áreas de valor), mapear as **Atividades** do usuário dentro de cada Tema (os Épicos) e, finalmente, detalhar as **Histórias de Usuário (US)**, que se tornaram os requisitos funcionais concretos. Essa estrutura hierárquica (Tema $\rightarrow$ Épico $\rightarrow$ US) é a base para o modelo de microserviços, onde cada Tema representa um potencial limite de serviço independente.

<!-- <div style="text-align: center;">
<iframe width="768" height="496" src="https://miro.com/app/live-embed/uXjVJCLJwuA=/?focusWidget=3458764642080634350&embedMode=view_only_without_ui&embedId=512092104204" frameborder="0" scrolling="no" allow="fullscreen; clipboard-read; clipboard-write" allowfullscreen></iframe>
</div> -->

### Temas
| N° | Tema                        | Descrição                          |
|----|-----------------------------|------------------------------------|
| 1  | Gerir Conta                 | Microserviço de Usuário            |
| 2  | Explorar Catálogo           | Microserviço de Catálogo/Busca     |
| 3  | Reproduzir Mídia            | Microserviço de Player             |
| 4  | Organizar Mídia             | Microserviço de Playlist           |
| 5  | Avaliar Mídia               | Microserviço de Avaliação          |
| 6  | Interagir com a Comunidade  | Microserviço Social                |

### Épicos

<table style="width:100%; border-collapse: collapse; color: #f0f0f0; background-color: #1e1e1e;">
  <thead>
    <tr>
      <th style="border: 1px solid #444; padding: 12px; text-align: center; width: 5%; background-color: #2c2c2c;">N°</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 45%; background-color: #2c2c2c;">Tema</th>
      <th style="border: 1px solid #444; padding: 12px; text-align: left; width: 50%; background-color: #2c2c2c;">Épico</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px; text-align: center;">1</td>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Gerir Conta</td>
      <td style="border: 1px solid #444; padding: 12px;">Registrar-se e autenticar-se</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar conta</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Editar conta</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Excluir conta</td>
    </tr>
    <tr>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px; text-align: center;">2</td>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px;">Explorar Catálogo</td>
      <td style="border: 1px solid #444; padding: 12px;">Ver Recomendações</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Buscar mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Aplicar filtro / ordenação</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Detalhes da Mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Explorar artista</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px; text-align: center;">3</td>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Reproduzir Mídia</td>
      <td style="border: 1px solid #444; padding: 12px;">Iniciar e pausar mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Controlar volume / tempo</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Exibir letra</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Gerenciar fila de reprodução</td>
    </tr>
    <tr>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px; text-align: center;">4</td>
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Organizar Mídia</td>
      <td style="border: 1px solid #444; padding: 12px;">Criar playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Gerenciar mídia em playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Definir privacidade</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Marcar como Favorito</td>
    </tr>
    <tr>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px; text-align: center;">5</td>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px;">Avaliar Mídia</td>
      <td style="border: 1px solid #444; padding: 12px;">Avaliar mídia</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Avaliar álbum</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Avaliar playlist</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Avaliar artista</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Ver estatísticas dos reviews</td>
    </tr>
    <tr>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px; text-align: center;">6</td>
      <td rowspan="5" style="border: 1px solid #444; padding: 12px;">Interagir com a Comunidade</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Feed</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Interagir com reviews</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Buscar usuário</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Seguir / Deixar de Seguir</td>
    </tr>
    <tr>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar Perfil do Usuário</td>
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
      <td rowspan="14" style="border: 1px solid #444; padding: 12px;">Explorar Catálogo</td>
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
      <td rowspan="4" style="border: 1px solid #444; padding: 12px;">Explorar artista</td>
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
      <td style="border: 1px solid #444; padding: 8px; text-align: center;">US 19</td>
      <td style="border: 1px solid #444; padding: 12px;">Visualizar reviews de artista escritos por outros usuários</td>
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
      <td rowspan="3" style="border: 1px solid #444; padding: 12px;">Explorar Catálogo</td>
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

## Requisitos Funcionais Priorizados

Para gerenciar o escopo e o prazo de dois meses, o método **MoSCoW** (Must Have, Should Have, Could Have) foi aplicado rigorosamente. Os 49 requisitos do MVP foram classificados para garantir que os esforços de desenvolvimento se concentrassem na entrega do valor essencial da plataforma:

* **Must Have (M):** Requisitos essenciais, como **Registro de Usuário** e as funcionalidades básicas de **Avaliação** e **Visualização de Mídia**. Sem eles, o produto não pode ser lançado.
* **Should Have (S):** Funcionalidades importantes, como **Busca Avançada**, **Criação de Playlists** e **Curtir Reviews**, que aprimoram a experiência de uso.
* **Could Have (C):** Funcionalidades desejáveis, como a **Avaliação de Álbuns/Playlists** e a **Tradução de Letras**, que serão executadas apenas se o prazo e os recursos permitirem.

Essa combinação garantiu que o foco fosse mantido no **Mínimo Produto Viável (MVP)**, que engloba a gestão de conta e o ciclo de avaliação social.

| N°        | História de Usuário | Critério de Aceitação | Prioridade |
| :---:     | :--- | :--- | :---: |
| **US 1**  | Criar conta | Deve registrar o usuário com e-mail e senha. | **M** |
| **US 2**  | Realizar login com usuário e senha | Deve autenticar e iniciar a sessão do usuário. | **M** |
| **US 49** | Visualizar perfil de usuário | Deve exibir o perfil básico de qualquer usuário e seus dados públicos. | **M** |
| **US 7**  | Buscar mídia por artista | Deve retornar Mídias cujo Artista corresponda ao termo de busca. | **M** |
| **US 13** | Visualizar dados básicos da mídia | Deve exibir título, artista, álbum, e descrição da Mídia. | **M** |
| **US 31** | Cadastrar nota de mídia | Deve registrar a nota (1 a 5 estrelas) no banco de dados, associada ao Usuário e à Mídia. | **M** |
| **US 34** | Publicar review de mídia | Deve permitir a submissão de texto (review) associado à Mídia e ao Usuário. | **M** |
| **US 14** | Visualizar nota da mídia | Deve exibir a nota média agregada da Mídia (depende de US 31). | **M** |
| **US 15** | Visualizar reviews de outros usuários em mídia | Deve exibir reviews e o nome/perfil do Usuário que as publicou. | **M** |
| **US 20** | Controlar reprodução da mídia | Deve ter botões funcionais de play/pause. | **M** |
| **US 23** | Visualizar letra da mídia | Deve exibir o texto da letra (estático) na tela de reprodução. | **M** |
| **US 4**  | Editar dados do perfil | Deve permitir a alteração de dados básicos (nome de exibição) após o login. | **S** |
| **US 46** | Curtir reviews | Deve registrar o "curtir" no banco, incrementando o contador da Review. | **S** |
| **US 5**  | Excluir conta do perfil | Deve deletar a conta e todos os dados associados (Reviews, Notas). | **S** |
| **US 3**  | Visualizar dados do perfil | Deve exibir os dados básicos do perfil logado. | **S** |
| **US 32** | Visualizar nota dada em mídia | Deve exibir a nota que o usuário logado deu àquela Mídia. | **S** |
| **US 35** | Visualizar review de mídia | Deve exibir a review que o usuário logado escreveu. | **S** |
| **US 6**  | Buscar mídia por nome | Deve retornar Mídias pelo título. | **S** |
| **US 8**  | Buscar álbum | Deve retornar Álbuns pelo nome. | **S** |
| **US 9**  | Filtrar pesquisa por gênero | Deve aplicar filtro para limitar resultados ao Gênero selecionado. | **S** |
| **US 10** | Filtrar pesquisa por nota | Deve aplicar filtro para limitar resultados pela Nota Média mínima. | **S** |
| **US 16** | Buscar artista | Deve buscar Artistas pelo nome. | **S** |
| **US 17** | Visualizar perfil do artista | Deve exibir informações do Artista. | **S** |
| **US 18** | Ver estatísticas do artista | Deve exibir a nota média agregada de todas as Mídias do Artista. | **S** |
| **US 19** | Visualizar reviews de artista escritos por outros usuários | Deve exibir reviews feitas sobre o Artista. | **S** |
| **US 21** | Ajustar volume da mídia | Deve permitir alterar o volume do áudio. | **S** |
| **US 22** | Ajustar linha do tempo da mídia | Deve permitir navegar na linha do tempo do áudio (arrastar). | **S** |
| **US 29** | Marcar/Desmarcar mídia como favorita | Deve registrar/remover o status de Favorita no banco de dados. | **S** |
| **US 30** | Visualizar suas mídias favoritas | Deve exibir a lista de Mídias favoritas. | **S** |
| **US 33** | Excluir nota de mídia | Deve remover a nota registrada no banco. | **S** |
| **US 36** | Excluir review de mídia | Deve remover a review registrada no banco. | **S** |
| **US 43** | Ver nota média de mídia específica | Deve calcular e exibir a nota média da Mídia. | **S** |
| **US 44** | Ver nota média do artista de acordo com suas mídias | Deve calcular e exibir a nota média agregada do Artista. | **S** |
| **US 45** | Ver nota média de álbums de um artista | Deve calcular e exibir a nota média agregada do Álbum. | **S** |
| **US 37** | Cadastrar nota de álbum | Deve registrar a nota para o Álbum. | **S** |
| **US 38** | Visualizar nota dada em álbum | Deve exibir a nota do usuário para o Álbum. | **S** |
| **US 39** | Excluir nota de álbum | Deve remover a nota do Álbum. | **S** |
| **US 40** | Publicar review de álbum | Deve registrar a review para o Álbum. | **S** |
| **US 41** | Visualizar review de álbum | Deve exibir a review do usuário para o Álbum. | **S** |
| **US 42** | Excluir review de álbum | Deve remover a review do Álbum. | **S** |
| **US 11** | Ordenar pesquisa por nome | Deve ordenar os resultados da busca pelo nome. | **S** |
| **US 12** | Ordenar pesquisa por nota | Deve ordenar os resultados da busca pela nota média. | **S** |
| **US 24** | Visualizar tradução da letra da mídia | Deve exibir o texto traduzido da letra. | **S** |
| **US 25** | Ver fila de reprodução | Deve exibir a lista de Mídias na fila. | **S** |
| **US 26** | Adicionar mídia à fila de reprodução | Deve permitir adicionar Mídia à lista de reprodução. | **S** |
| **US 27** | Remover mídia de fila de reprodução | Deve permitir remover Mídia da lista de reprodução. | **S** |
| **US 28** | Alterar ordem de mídia na fila de reprodução | Deve permitir reordenar as Mídias na fila. | **S** |
| **US 47** | Buscar usuário por nome de usuário | Deve retornar Usuários pelo nome de usuário. | **S** |
| **US 48** | Buscar usuário por nome | Deve retornar Usuários pelo nome completo (se disponível). | **S** |

## Requisitos Não Funcionais

| N°    | Requisito                                                                                                                 |
| :---: | :------------------------------------------------------------------------------------------------------------------------ |
| RNF 1 | O sistema deve ser **responsivo**, adaptando-se a telas mobile (largura de 375px) e desktop, sem perda de funcionalidade. |
| RNF 2 | O player deve ter latência de resposta menor que **150ms** ao receber comandos (play/pause).                              |
| RNF 3 | A busca deve retornar resultados em menos de **2 segundos** (tempo de resposta) para até 10.000 registros no catálogo.    |
| RNF 4 | A senha do usuário deve ser armazenada com **hashing** e não deve ser recuperável em texto simples.                       |
