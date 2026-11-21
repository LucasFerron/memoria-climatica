# Memória Climática

**Mapeamento comunitário de eventos climáticos**

Projeto da disciplina de Ciência da Computação — Universidade Federal da Fronteira Sul (UFFS), Campus Chapecó.

## Sobre o projeto

A Memória Climática é uma plataforma web colaborativa em que moradores de áreas urbanas e rurais registram eventos climáticos que viveram (enchentes, granizo, secas, vendavais e outros). Os relatos aparecem em um mapa e em uma linha do tempo, permitindo que qualquer pessoa veja com que frequência esses eventos atingem a sua região e como municípios e estados responderam a eles.

A proposta é aproximar os impactos das mudanças climáticas da realidade de cada comunidade, em vez de deixá-los restritos a relatórios técnicos e projeções futuras.

## Alinhamento com a ODS

- **ODS 13 — Ação contra a mudança global do clima**
- **Meta 13.3:** melhorar a educação, aumentar a conscientização e a capacidade humana e institucional sobre mitigação, adaptação, redução de impacto e alerta precoce da mudança do clima.

## Identidade Visual e Paleta de Cores

A interface adota uma paleta em **tons pastéis e suaves**, escolhida para evitar o cansaço visual em leituras prolongadas, transmitir acolhimento aos relatos comunitários e manter contraste adequado entre texto e fundo (legibilidade e acessibilidade).

| Papel | Cor | Hexadecimal | Aplicação e justificativa |
|-------|-----|-------------|---------------------------|
| **Primária (Atmosfera / Água)** | Azul Céu / Azul Pastel | `#0284c7` / `#e0f2fe` | Botões principais, datas da linha do tempo e eventos ligados a enchentes e alagamentos; remete aos recursos hídricos e à clareza informativa. |
| **Secundária (Sustentabilidade / ODS 13)** | Verde Sálvia | `#047857` / `#d1fae5` | Cabeçalho da tela de registro, etiquetas de tempestades/granizo e elementos alinhados à preservação ambiental e à ODS 13. |
| **Neutra (Fundo e Leitura)** | Off-white / Cinza Claro / Ardósia | `#f8fafc` / `#f1f5f9` / `#1e293b` | Fundos de página, seções alternadas e tipografia escura de alto contraste para leitura confortável. |
| **Detalhe (Solo / Terra)** | Marrom Argila / Terracota Suave | `#9a3412` / `#ffedd5` | Etiquetas de estiagem/seca e blocos de orientação; representa o solo e o caráter comunitário dos relatos. |

## Páginas

| Página | Descrição |
|--------|-----------|
| **Home** (`index.html`) | Apresentação do projeto e mapa geral, com filtros por país, estado e cidade. |
| **Registrar acontecimento** (`registrar.html`) | Formulário para relatar um evento, com data, descrição e localização.  (ilustrativo) |
| **Linha do Tempo** (`linha-do-tempo.html`) | Histórico cronológico e estático de ocorrências climáticas extremas (enchentes, granizo e seca), com filtros ilustrativos por tipo e período e cards diferenciados por categoria. |
| **Sobre o ODS 13** (`sobre-ods13.html`) | Explicação do ODS 13 e de como o site contribui para ele. |

## Escopo desta fase

Neste primeiro momento o site é **estático**, feito somente com HTML e CSS (Tailwind), sem JavaScript próprio e sem back-end.

**Funcionalidades mínimas (esta fase)**

- As quatro páginas construídas, com navegação entre elas
- Layout responsivo para desktop e celular, seguindo os wireframes
- Home com apresentação, indicadores, barra de filtros (país, estado, cidade), mapa ilustrativo e relatos de exemplo
- Formulário de registro com validação nativa do navegador
- Linha do Tempo com relatos de exemplo
- Página explicativa sobre o ODS 13
- Site publicado (por exemplo, no GitHub Pages)

**Funcionalidades desejáveis (fases seguintes)**

- Mapa interativo com marcadores reais e agrupamento por região
- Filtros funcionando, inclusive por tipo de evento e período
- Salvar e listar relatos de verdade (JavaScript e back-end)
- Estados e cidades carregados da API de localidades do IBGE
- Registro das soluções adotadas por municípios e estados
- Marcação do local exato no mapa e envio de fotos

## Tecnologias

| Camada | Tecnologia |
|--------|-----------|
| Estrutura | HTML5 |
| Estilo | [Tailwind CSS](https://tailwindcss.com/) (por CDN no início) e `css/style.css` para ajustes próprios |
| Mapa (nesta fase) | Imagem ilustrativa ou incorporação do [OpenStreetMap](https://www.openstreetmap.org/) |
| Design | Figma |
| Publicação | GitHub Pages |

## Protótipo

Wireframes de baixa fidelidade da Home e do formulário: [Figma](https://www.figma.com/design/6FbzoltwNisM9sRQ91oUPN)

## Estrutura de pastas

```
memoria-climatica/
├── index.html
├── registrar.html
├── linha-do-tempo.html
├── sobre-ods13.html
├── css/          # Estilos próprios
├── components/   # Trechos de HTML reaproveitados (navbar, rodapé, card)
├── assets/       # Imagens, ícones e fontes
├── docs/         # Relatório, wireframes e planejamento das sprints
└── .github/      # Modelos de issue
```

A estrutura completa, com a função de cada arquivo, está em [`docs/estrutura-de-pastas.md`](docs/estrutura-de-pastas.md).

## Como executar

Como o arquivo `css/output.css` já está compilado no repositório, basta abrir os arquivos `.html` no navegador (ou via extensão *Live Server* no VS Code).

Caso precise editar estilos em `css/`:

```bash
# 1. Clonar o repositório e instalar dependências
git clone [https://github.com/LucasFerron/memoria-climatica.git]
cd memoria-climatica
npm install

# 2. Recompilar o CSS do Tailwind v4
npx @tailwindcss/cli -i ./css/input.css -o ./css/output.css --watch
```

Abra o arquivo `index.html` no navegador ou, de preferência, use a extensão *Live Server* do VS Code, que recarrega a página a cada alteração. Como o Tailwind é carregado por CDN, é necessário estar com internet.

## Cronograma

| Sprint | Foco | Entregas previstas |
|--------|------|--------------------|
| **Sprint 1** | Planejamento | Projeto escrito, objetivos, ODS, público-alvo e wireframes. |
| **Sprint 2** | Páginas principais | Estrutura do repositório e configuração do Tailwind; trechos reaproveitáveis (navbar, rodapé, card); página **Home** com apresentação, filtros, mapa ilustrativo e relatos de exemplo; página **Registrar acontecimento** com validação nativa. |
| **Sprint 3** | Conclusão e publicação | Páginas **Linha do Tempo** e **Sobre o ODS 13**; ajustes de responsividade e acessibilidade (contraste, rótulos, texto alternativo); revisão de conteúdo e links; publicação no GitHub Pages; versão final do relatório. |

O detalhamento de cada sprint fica em `docs/sprints/`.

## Equipe

- Lucas Ferron da Silva
- João Eduardo Dias Duarte

## Licença

Projeto acadêmico. Defina aqui a licença do código (por exemplo, MIT) e adicione o arquivo `LICENSE` na raiz.# memoria-climatica
