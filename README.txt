TAVERNA DE DADOS – Clube de Jogos de Tabuleiro e RPG
Desenvolvimento Web I – Escola Técnica Municipal de Sete Lagoas

Dupla: Iury e Joseph

EXERCÍCIOS
1. exercicio1/ – Página institucional do clube
2. exercicio2/ – Formulário de cadastro de jogadores (Ficha do Aventureiro)
3. exercicio3/ – Tabela do acervo de jogos
4. exercicio4/ – Galeria com as capas dos jogos
5. exercicio5/ – Página do evento Maratona da Taverna 2026

IDENTIDADE VISUAL
- Cores: verde feltro (#1f4d3a), marrom madeira (#4a2e1d),
  pergaminho (#f3ead6) e dourado (#c9962b).
- Fontes (Google Fonts): Alegreya SC para títulos e Alegreya Sans para textos.

PRINCIPAIS DECISÕES DE HTML E CSS

Gerais
- Usamos as tags semânticas header, nav, main, section e footer para
  organizar as partes de cada página.
- Cada exercício tem seu próprio CSS externo (css/estilo.css), separando a
  estrutura (HTML) da aparência (CSS).
- As cores ficam em variáveis no :root (--feltro, --madeira, --pergaminho,
  --ouro e --tinta), assim basta mudar em um lugar para trocar a cor da
  página toda.
- Todas as páginas têm o mesmo cabeçalho, com o mesmo menu ligando os cinco
  exercícios, e o mesmo rodapé. Isso mantém a identidade visual do clube.
- Usamos a meta viewport para a página se ajustar à largura do celular.
- Colocamos comentários curtos no HTML para identificar cada seção.

Exercício 1 – Página institucional
- A apresentação usa display: flex para deixar o texto ao lado da imagem.
  No celular, o @media muda para flex-direction: column e a imagem vai para
  baixo do texto.
- Os serviços usam display: grid com 3 colunas, que viram 1 coluna no celular.
- O link "Voltar ao topo" aponta para o id #topo, e o scroll-behavior: smooth
  deixa a rolagem suave.
- Usamos seletores de elemento (body, h2), de classe (.servico, .menu) e de
  id (#topo, #contato).

Exercício 2 – Formulário
- Cada label tem o atributo for igual ao id do campo, então clicar no texto
  seleciona o campo.
- Usamos type="email" e type="tel" para o navegador entender o tipo de dado,
  e required nos campos obrigatórios.
- Os radios de experiência têm o mesmo name, por isso só uma opção pode ser
  marcada. Os checkboxes permitem marcar várias.
- O fieldset com legend agrupa as opções relacionadas.

Exercício 3 – Tabela
- Usamos caption (título), thead (cabeçalho) e tbody (dados), com os títulos
  das colunas em th.
- O border-collapse: collapse junta as bordas das células.
- A tabela fica dentro de uma div com overflow-x: auto, então no celular ela
  rola para o lado sem quebrar a página.
- Na legenda, cada categoria tem um símbolo e um nome (♜ Estratégia, ⚔ RPG),
  para não depender só da cor.
- O tbody tr:hover muda a cor da linha ao passar o mouse.

Exercício 4 – Galeria
- Cada imagem fica em um figure com figcaption para a legenda, e todas têm
  alt descrevendo a pintura.
- A grade usa grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)),
  que muda o número de colunas sozinho conforme a largura da tela.
- O aspect-ratio: 4 / 3 com object-fit: cover deixa todas as imagens do
  mesmo tamanho sem deformar.
- O figure:hover img com transform: scale(1.05) dá um zoom leve. O
  overflow: hidden no figure impede que a imagem passe da borda, e a legenda
  fica fora da imagem, então continua legível.
- As capas de RPG têm link para o cadastro (exercício 2).

Exercício 5 – Evento
- O nome do evento fica no h1 dentro do cabeçalho.
- Logo no início do main, um nav com links (#sobre, #programacao,
  #informacoes, #inscricao) faz a navegação interna até as seções da página,
  com rolagem suave pelo scroll-behavior: smooth.
- A programação usa um article para cada atividade, com horário e
  responsável, e as atividades ficam em 2 colunas com grid.
- As informações importantes estão em ul (a ordem não importa) e os passos
  da inscrição estão em ol (a ordem importa).
- Cada section tem uma borda tracejada separando as partes da página.
- No celular, o @media (max-width: 700px) deixa as atividades em 1 coluna.

DIVISÃO DE TAREFAS
- Iury: Fez toda a estrutura HTML.
- Joseph: Fez toda a estrutura CSS.

FONTES E FERRAMENTAS
- Imagens: https://unsplash.com | https://commons.wikimedia.org/wiki/Main_Page
- Fontes: Google Fonts
- Editor: VsCode
- Uso de IA: Utilizado com bastante vigor no CSS, para algumas finalidades criativas e técnicas, para procura de banco de dados de imagens e explicação 

Todos os nomes, jogos, endereços e contatos são fictícios.