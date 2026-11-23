# Elas Connect — logística descomplicada para mulheres MEI

Site do TCC do Curso Técnico em Logística. Oferece informação prática e ferramentas simples para mulheres MEI (microempreendedoras individuais) que trabalham com logística tomarem decisões melhores sobre estoque, custos e operação.

## Páginas

| Arquivo | O que é |
| --- | --- |
| `index.html` | Início: apresentação do projeto e atalhos para as ferramentas |
| `duvidas.html` | Dúvidas frequentes de logística, com exemplos e links para a calculadora |
| `calculadora.html` | Calculadora de estoque de segurança e ponto de pedido |
| `simulador.html` | MEI PREDICT: simulador de cenários otimista, provável e pessimista |
| `sobre.html` | Quem somos, por que escolhemos o tema e contato |
| `comunidade.html` | Apresentação da futura comunidade (aviso de “em breve”) |
| `404.html` | Página mostrada quando um endereço não existe |

## Outros arquivos

- `css/estilo.css`: todas as cores, fontes e o layout do site. As cores ficam no topo do arquivo.
- `js/site.js`: menu do celular, ano do rodapé e leitura de números no formato brasileiro (ex.: `1.200,50`).
- `js/calculadora.js`: contas da calculadora de estoque.
- `js/simulador.js`: regras e contas do simulador MEI PREDICT.
- `favicon.svg`: ícone que aparece na aba do navegador.
- `netlify.toml`: configuração de publicação na Netlify (site estático, sem build).

## Tecnologias

HTML, CSS e JavaScript puro. Não há frameworks, instalação, banco de dados, login nem chaves de API. As fontes (Bricolage Grotesque e Atkinson Hyperlegible) são carregadas do Google Fonts; sem internet, o site usa as fontes do próprio aparelho.

## Como ver no computador

Abra o arquivo `index.html` com dois cliques no navegador. Tudo funciona sem servidor.

## O que editar antes de apresentar

- `sobre.html`: nomes, iniciais e descrições das três integrantes (procure por “EDITE AQUI”).
- `sobre.html`: o e-mail de contato `contato@elasconnect.com.br` é um exemplo; troque pelo e-mail real do grupo.

## Próximas etapas

1. **Comunidade**: cadastro das participantes, publicação de perguntas e dicas, e moderação. Exige login e banco de dados, por isso ficou para a segunda entrega.
2. Mais perguntas na página de dúvidas (por exemplo: curva ABC, custo de frete, estoque parado).
