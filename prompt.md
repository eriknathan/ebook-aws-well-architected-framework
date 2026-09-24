# Converter material de estudo (.md) em ebook HTML

## Objetivo

Transforme o conteúdo Markdown que vou enviar em um **ebook de estudo** publicado como artifact HTML (não como arquivo para download). O leitor é um estudante revisando o material: o ebook precisa ser agradável de ler do início ao fim e fácil de consultar depois.

## Regras de conteúdo (prioridade máxima)

1. **Fidelidade total:** preserve todo o conteúdo do original. Não resuma, não corte trechos e não acrescente fatos que não estejam no material. O trabalho é de diagramação, não de reescrita.
2. **Ajustes permitidos:** corrigir erros evidentes de digitação e dividir parágrafos muito longos. Se encontrar algo que pareça um erro técnico, mantenha o texto e me avise na resposta, sem alterar no ebook.
3. **Idioma:** português do Brasil, mantendo termos técnicos em inglês quando o original os usa (ex: "Well-Architected", "pillar").
4. **Metadados ausentes:** se curso, módulo ou autor não estiverem no material, omita o campo em vez de inventar.

## Estrutura do ebook

Na ordem:

1. **Capa:** tag/kicker de categoria, título grande, subtítulo e uma linha de metadados (curso · módulo · autor).
2. **Sumário:** logo após a capa, em caixa destacada, listando todas as seções numeradas **como links âncora** para cada seção.
3. **Seções:** espelhe a numeração do original (1.1, 1.2...), cada uma com um rótulo pequeno em fonte monoespaçada mostrando o número. Se o original não tiver numeração, numere na ordem dos títulos.
4. **Perguntas de fixação:** use as perguntas do material, se houver. Se não houver, crie de 3 a 5 perguntas baseadas **apenas** no conteúdo do ebook. Cada pergunta fica em uma caixa com alternativas (A, B, C, D) e a resposta dentro de `<details>` (clicável), com a alternativa correta e uma frase curta explicando o porquê.
5. **Resumo final:** bloco de destaque com fundo de cor sólida/escura fechando o ebook, com os pontos-chave do material.

## Qual componente usar para cada tipo de conteúdo

Escolha o componente pelo formato do conteúdo, e não para variar o visual. Texto corrido continua como parágrafo.

| Conteúdo no original | Componente |
| --- | --- |
| Definição-chave ou citação oficial | Blockquote em destaque |
| Aviso, dica, "importante", "atenção" | Callout (caixa com ícone ou rótulo) |
| Lista de itens paralelos com descrição (pilares, componentes, serviços) | Cards em grid |
| Eventos com data ou sequência cronológica | Linha do tempo vertical |
| Dados com colunas / comparações | Tabela estilizada |
| Lista curta de termos soltos (tags, siglas, nomes) | Chips/badges |
| Passo a passo | Lista numerada com marcadores destacados |

## Visual

- **Tema:** claro, com fundo branco ou off-white.
- **Paleta:** derivada da marca do assunto. Para AWS: laranja `#FF9900` como destaque e azul-escuro `#232F3E` para títulos e para o bloco de resumo. Use o laranja com moderação (rótulos, bordas, detalhes) e nunca como cor de texto corrido sobre branco, porque o contraste não é suficiente.
- **Tipografia:** serifada com personalidade para títulos (ex: Fraunces), sans-serif legível para o corpo (ex: Inter ou Source Sans 3) e monoespaçada para rótulos, números e tags (ex: JetBrains Mono). Carregue as fontes pelo Google Fonts.
- **Hierarquia:** bordas sutis e cantos arredondados, com sombra e raio variando conforme a importância do elemento (ex: capa e resumo mais marcados, cards leves, tabelas quase planas).
- **Leitura:** largura de texto confortável (cerca de 65–75 caracteres por linha), bom espaçamento entre seções e contraste AA.
- **Responsivo:** funcionar bem na largura de um celular (cards viram coluna única, tabelas ganham rolagem horizontal própria sem estourar a página).
- **Impressão:** incluir `@media print` básico (`<details>` aberto, sem quebra de página no meio de cards).

## Entrega

- HTML único e autocontido (CSS inline no `<head>`; sem JavaScript, a menos que seja indispensável).
- HTML semântico: `<article>`, `<section id="...">`, `<h1>`–`<h3>` em ordem hierárquica.
- Publique como artifact com um título curto e específico do assunto (ex: "AWS Well-Architected Framework").
- Antes de publicar, confira: todas as seções do original estão presentes, os links do sumário funcionam e nenhuma informação foi inventada.
- Na resposta, envie o link e, se houver, uma lista curta de pontos do original que pareceram errados ou ambíguos.

---

<conteudo>
[COLE O MARKDOWN AQUI]
</conteudo>
