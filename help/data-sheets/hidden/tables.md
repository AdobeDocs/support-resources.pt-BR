---
title: Tabela
description: Trabalhar com tabelas de markdown e tabelas de HTML.
hide: true
hidefromtoc: true
exl-id: 5ce746fc-6835-4bee-85c5-5ad5176baca0
source-git-commit: 6893d1e41c3899c3ab6a9b02b305161eb3f7e049
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 3%

---

# Tabela

Matt estava aqui várias vezes...

EDS

O Markdown padrão é compatível somente com tabelas básicas. Para o AdobeDocs Markdown, você tem as seguintes opções:

* Tabelas básicas do Markdown
* tabelas de HTML
* Tabelas do Markdown com sintaxe de HTML limitada para quebras de parágrafo (`<p>`), quebras de linha (`<br>`) e listas básicas (`<ul>`, `<ol>`).

## Conversão de tabelas de HTML para tabelas do Markdown

Em alguns casos, convém converter uma tabela de HTML em uma tabela do Markdown ou em um texto do Markdown. Talvez seja necessário melhorar a aparência, resolver um erro de validação ou facilitar a edição a partir de agora.

Infelizmente, não foi possível encontrar uma única ferramenta que converte bem as tabelas de HTML. Geralmente usamos uma combinação de ferramentas para reunir uma mesa do Markdown decente.

| Ferramenta | O que faz |
|--- |--- |
| [Gerador de tabelas do Markdown](https://www.tablesgenerator.com/markdown_tables) | Bom para criar tabelas do Markdown do zero. |
| [Conversor de tabela avançado](https://tableconvert.com/html-to-markdown) | Converta tabelas de qualquer formato em qualquer formato. <p>**Nota:** Links e imagens são nivelados quando convertidos. |
| [HTML de tabela básica > conversor de markdown](https://jmalarcon.github.io/markdowntables/) | Conversor de HTML simples <p>**Nota:** Links e imagens são nivelados quando convertidos. |
| [HTML não tabela > Conversor de Markdown](https://codebeautify.org/html-to-markdown) | Converte tabelas de HTML em sintaxe de Markdown que não seja de tabela. Use em combinação com as ferramentas acima para copiar links, imagens e qualquer outro item nivelado. |

## Tabelas básicas do Markdown

* Adicione pelo menos três hifens na segunda linha que determina as propriedades da tabela. Exemplo: `|--- |--- |--- |` para uma tabela de 3 colunas.
* As tabelas do Markdown devem ter pelo menos uma linha de cabeçalho e uma linha de corpo. Não é possível criar uma tabela de markdown de uma linha ou de uma célula (use HTML).
* Certifique-se de que cada linha tenha o mesmo número de caracteres de barra vertical ( &amp;vert; ). Se você precisar incluir um caractere de barra vertical em uma célula de tabela, escape ao precedê-lo com uma barra invertida (`\|`) ou usando o código de entidade HTML (`&vert;`).
* Tenha cuidado ao usar blocos de código em tabelas. Blocos de código em linha podem causar larguras de coluna desproporcionais.
* Você pode alterar como a tabela é renderizada especificando Automático ou Fixo. Consulte [Alteração no modo como as tabelas são renderizadas](#table-rendering).

## Criação de tabelas do Markdown com HTML de bônus

Para facilitar a migração, estendemos as tabelas do Markdown para oferecer suporte a quebras de parágrafo de HTML (`<p>`), quebras de linha (`<br>`) e listas de HTML básicas (`<ul>` e `<ol>`) nas tabelas do Markdown.

**Tabela do Markdown com quebras de linha e listas**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**Exemplo**

| Cabeçalho 1 | Cabeçalho 2 | Cabeçalho 3 |
|--- |--- |--- |
| Linha normal | row 1 column 2 | row 1 column 3 |
| Quebra de linha | primeira linha na célula<br>segunda linha na célula | row 1 column 3 |
| Lista de marcadores | Lista de marcadores:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Lista de marcadores com quebra de linha | Lista de marcadores:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>Esta é uma nova linha depois da lista de marcadores | row 2 column 3 |

>[!IMPORTANT]
>
>Se decidir usar o HTML em tabelas nativas, certifique-se de usar a sintaxe de HTML adequada. Erros na sintaxe de HTML resultam em erros de validação que são difíceis de entender. Verifique seu trabalho.

## Trabalhar com tabelas de HTML

A ferramenta de migração tentou preservar o máximo de formatação possível da tabela original. A maior parte dessa sintaxe de HTML é ignorada, enquanto parte dela resulta em erros de validação.

**Exemplo de tabela de HTML migrada**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**Renderizado**

<table> 
 <tbody>
  <tr>
   <th>Propriedade</th> 
   <th>Tipo</th> 
   <th>Valor Descrição</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Obrigatório)</i> Uma cadeia de caracteres de vários valores de imagens de selo até o número de badgingLevels. Os caminhos da imagem do selo devem ser solicitados para que o primeiro seja concedido ao especialista mais alto. Se houver menos selos do que o indicado por badgingLevels, o último selo na matriz preencherá o restante da matriz. Exemplo de entrada:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Longo</td> 
   <td><p><i>(Opcional)</i> Especifica os níveis de experiência a serem atribuídos. Por exemplo, se houver uma variável <code>expert </code>e uma <code>almost expert</code> (duas medalhas), então o valor deve ser definido como 2. O badgingLevel deve corresponder ao número de imagens de selo relacionadas a especialistas listadas para a propriedade badgingPath. O padrão é 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Obrigatório)</i> Identifica o mecanismo de pontuação como "básico" ou "avançado". Defina como "avançado", caso contrário, o padrão será "básico".</p></td> 
  </tr>
 </tbody>
</table>

**Quando usar tabelas de HTML**

* Para balancear colunas.
* Para omitir cabeçalhos de tabela (as tabelas do Markdown devem ter uma linha de cabeçalho).
* Para remover a borda de uma tabela de uma linha (`<tr style="border: 0;">`).
* Para adicionar extensões de coluna ou linha.
* Para alinhar o texto em uma célula da tabela.

**Notas para trabalhar com tabelas de HTML**

* Não use a sintaxe do Markdown em tabelas de HTML. Por exemplo, se você adicionar `[!NOTE]` para uma tabela HTML, ela será renderizada como está (`[!NOTE]`). Em vez disso, use a sintaxe de HTML para coisas como notas e imagens.

  As tags loc são uma exceção a essa regra, pois as tags UICONTROL e DNL são removidas antes que as páginas sejam renderizadas.

* Nem toda sintaxe de HTML é suportada em tabelas. Largura, altura, cor e outros elementos da sintaxe de HTML são ignorados quando renderizados em EXL. Você pode deixar esses valores no, a menos que resultem em erros de validação.
* Para alinhar texto, use `align: "left|center|right"` em HTML. Por exemplo, para centralizar o conteúdo de uma célula de tabela, use `<td align="center">`.
* As tabelas de HTML não podem incluir tabelas aninhadas.

>[!TIP]
>
>Se quiser desativar uma borda para uma tabela de HTML de uma linha, use esta sintaxe:
>
>```
><table>
><tr style="border: 0;">
>```

## Especificação de como as tabelas são renderizadas {#table-rendering}

Podemos renderizar tabelas de duas maneiras:

* **Fixo** (atualmente o padrão) - Inclui regras personalizadas para renderizar tabelas, incluindo tabelas de HTML com imagens. As tabelas são renderizadas como largura total sem rolagem, o que às vezes causa a sobreposição de texto.
* **Automático** - Semelhante ao Git-flavored Markdown (GFM). As tabelas podem rolar, de modo que o texto não se sobrepõe.

Na maioria dos casos, as tabelas são renderizadas com a mesma aparência. No entanto, se a tabela incluir texto sobreposto, será necessário aplicar o `auto` tag. Ou, se a tabela de HTML com cartões de imagem não estiver sendo renderizada corretamente, talvez você queira aplicar a variável `fixed` tag.

Estamos considerando alterar o padrão de `fixed` para `auto`.

## Edição de tabelas do Markdown

Se quiser especificar como uma tabela de markdown nativa é renderizada, adicione uma destas linhas de sintaxe DEPOIS da tabela, com linhas em branco antes e depois de:

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![renderização de tabela](assets/table-render.png)

### Edição de tabelas de HTML

Se quiser especificar como uma tabela de HTML é renderizada, use uma destas linhas de sintaxe na primeira linha da tabela:

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### Quando usar Automático ou Fixo

**Sobreposição de texto**

Uso `auto` para tabelas com blocos de código longos ou texto que causa sobreposição de texto quando `fixed` (padrão) está selecionado.

*Fixo (Padrão)*

| Métrica de insights | Descrição | Parâmetro de consulta de ID |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Número total de mensagens inválidas do tipo para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.range.count** | Número total de mensagens de &quot;intervalo&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.format.count** | Número total de mensagens de &quot;formato&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.pattern.count** | Número total de mensagens &quot;padrão&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.present.count** | Número total de mensagens de &quot;presença&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.enum.count** | Número total de mensagens &quot;enum&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |

{style="table-layout:fixed"}

*Automático*

| Métrica de insights | Descrição | Parâmetro de consulta de ID |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Número total de mensagens inválidas do tipo para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.range.count** | Número total de mensagens de &quot;intervalo&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.format.count** | Número total de mensagens de &quot;formato&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.pattern.count** | Número total de mensagens &quot;padrão&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.present.count** | Número total de mensagens de &quot;presença&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |
| **timeseries.data.collection.validation.category.enum.count** | Número total de mensagens &quot;enum&quot; inválidas para um conjunto de dados ou para todos os conjuntos de dados. | ID do conjunto de dados |

{style="table-layout:auto"}

**tabelas de HTML com imagens balanceadas**

Uso `fixed` para tabelas de HTML que requerem imagens balanceadas que se tornam desbalanceadas quando `auto` está selecionada. Neste exemplo, as imagens têm tamanhos idênticos, mas há mais texto na coluna do meio.

*Automático*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Fluxo de trabalho para clientes em potencial do Adobe</strong></a>
    </div>
    <em>Fluxo de trabalho de edição principal para escritores principais.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Pouco frequente" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Fluxo de trabalho para usuários pouco frequentes</strong></a>
    </div>
    <em>Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validação" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validação</strong></a>
    </div>
    <em>Saiba como resolver erros de validação.</em>
    <br>
  </td>
</tr>
</table>

*Fixo (de mais de um modo)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="note-test.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="note-test.md"><strong>Fluxo de trabalho para clientes em potencial do Adobe</strong></a>
    </div>
    <em>Fluxo de trabalho de edição principal para escritores principais.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Pouco frequente" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Fluxo de trabalho para usuários pouco frequentes</strong></a>
    </div>
    <em>Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições. Não é um escritor principal? Saiba mais sobre as maneiras mais fáceis de fazer contribuições.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Validação" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Validação</strong></a>
    </div>
    <em>Saiba como resolver erros de validação.</em>
    <br>
  </td>
</tr>
</table>
