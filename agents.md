# AGENTS.md — guia para agentes de IA

## Visão geral
Site estático em português do Brasil (pt-BR) para um TCC de técnico em logística, voltado a mulheres MEI. HTML, CSS e JavaScript puro, sem build, sem dependências, sem backend. Publicado na Netlify com `publish = "."` (ver `netlify.toml`).

## Estrutura
- Páginas na raiz: `index.html`, `duvidas.html`, `calculadora.html`, `simulador.html`, `sobre.html`, `comunidade.html`, `404.html`.
- `css/estilo.css`: folha única. Paleta e fontes em variáveis no `:root`. Componentes com nomes em português (`.etiqueta`, `.botao`, `.campo`, `.aviso`, `.cenario`...).
- `js/site.js`: carregado em todas as páginas; expõe `window.ElasConnect` (`lerNumero`, `formatarNumero`, `formatarDinheiro`). Deve vir antes dos scripts das ferramentas.
- `js/calculadora.js` e `js/simulador.js`: lógica das ferramentas, rodando só no navegador.

## Convenções e decisões
- **Menu e rodapé estão repetidos em cada página** (não há build nem includes). Ao mudar o menu, altere todas as páginas e mantenha `aria-current="page"` só no link da página atual.
- Links são relativos (`calculadora.html`) para o site funcionar abrindo o arquivo direto no computador. Exceção: `404.html` usa caminhos absolutos (`/css/...`) porque a Netlify a serve em qualquer endereço.
- Números são digitados em campos `type="text"` com `inputmode="decimal"` para aceitar vírgula; sempre use `ElasConnect.lerNumero`.
- Calculadora: ES = Z × σ × √L; PP = d × L + ES; Z = 1,28 / 1,65 / 2,33; σ estimado por faixa = (máx − mín) ÷ 4; resultados arredondados para cima. Aceita parâmetros de URL (`demanda`, `desvio`, `min`, `max`, `prazo`, `nivel`), usados pelos links de `duvidas.html`.
- Simulador: as constantes ficam no objeto `REGRAS` em `js/simulador.js` e **estão descritas por extenso na seção “Regras do simulador” de `simulador.html`**. Se mudar uma, mude a outra. Sempre manter o aviso de que é simulação, não previsão nem conselho financeiro.
- Requisitos do projeto: não coletar dados pessoais (sem formulários; contato é por `mailto:`), sem imagens externas (ilustrações em SVG inline e emojis), linguagem simples e acolhedora, acessibilidade (títulos em ordem, rótulos, foco visível, link “pular para o conteúdo”).
- Conteúdo a ser personalizado pelo grupo está marcado com “EDITE AQUI” em `sobre.html`.

## Próximos passos
A segunda entrega é a comunidade (`comunidade.html` hoje é só apresentação + “em breve”). Ela exigirá login e persistência; na Netlify, usar Netlify Identity e Netlify Database, o que implica introduzir funções/servidor.
