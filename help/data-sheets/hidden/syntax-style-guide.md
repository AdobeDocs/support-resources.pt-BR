---
title: Guia de Sintaxe e Formatação de Documentação Colaborativa de Excelência de Autoatendimento
description: Uma introdução básica ao estilo do Markdown
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '4305'
ht-degree: 13%

---

# Guia de estilo da sintaxe do Markdown

Esta página ilustra a entrada do componente de Markdown para a criação de documentação técnica da experiência digital usando o formato markdown (.md). Esta página inclui detalhes para funcionários da Adobe.

EDS

Veja aqui: [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>Assista a este [vídeo sobre o AdobeDocs Markdown](https://video.tv.adobe.com/v/26165).

Na maioria das vezes, seguimos a sintaxe padrão Git-flavored markdown (GFM) para formatar texto. No entanto, alguma sintaxe (como linhas horizontais) não é compatível e estendemos o Markdown de várias maneiras para atender às nossas necessidades de documentação.

## Formatação básica de texto

Um parágrafo não requer sintaxe especial no Markdown. Adicione uma linha em branco entre cada parágrafo.

Para formatar o texto como **negrito**, coloque-o entre dois asteriscos:

```
This text is **bold**.
```

Para formatar o texto como *itálico*, coloque-o entre um único asterisco:

```
This text is *italic*.
```

Para formatar o texto como ***negrito e itálico***, coloque-o entre três asteriscos:

```
This is text is both ***bold and italic***.
```

Para ignorar os caracteres de formatação do Markdown, use `\` antes do caractere:

`This is not \*italicized\* type.`

Renderizado: não é um tipo \*em itálico\*.

## Emblemas

Em andamento. Aguardando Loc.

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## Citações Bloqueadas

Nosso sistema de criação usa a sintaxe de citações de bloqueio (`>` no início das linhas) para identificar extensões de Markdown personalizadas para dicas, anotações e vídeos. Você pode criar citações de bloqueio reais adicionando um caractere `>` na frente de um parágrafo.

>Esta é uma citação em bloco.

```
>This is a blockquote quotation.
```

## Bloco de código (em linha){#code-block}

**Quando usar**

Usado para renderizar uma parte do código em linha em uma frase. Ideal para chamar um nome de cookie, nome de arquivo, valor ou comando que não requer um bloco de código com zoneamento completo.

Conteúdo em blocos de código é renderizado como está e não está localizado. (A única exceção para esta regra é a sintaxe `!UICONTROL` e `!DNL`, que é removida durante o empacotamento para publicação.)

Também use blocos de código para exemplos de URLs que não devem ser validadas: `https://www.example.com`

**Sintaxe**

Um bloco de código usa acentos graves únicos para delimitar o elemento de código que você deseja destacar.

```
This is `inline code` within a paragraph of text.
```

**Exemplo**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>Você também pode quebrar o texto em acentos graves triplos (&grave;&grave;&grave;) para criar um bloco de código em linha. Isso é especialmente útil quando você precisa referenciar um caractere de marca de verificação inversa em um bloco de código em linha. Exemplo:
>
&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;

## Bloco de código (cercado)

**Quando usar**

Use um bloco de código para exibir a sintaxe do código. Um bloco de código cercado usa acentos graves triplos para delimitar o elemento de código que você deseja destacar. Adicione linhas em branco acima e abaixo do bloco de código cercado.

Observe que os blocos de código não estão localizados.

>[!TIP]
>
Especifique um idioma ao criar um bloco de código cercado. A especificação de um idioma permite o realce de sintaxe específico para esse idioma e exibe um botão **Copiar** para os usuários. Também é possível exibir números de linha se você especificar um idioma.

**Sintaxe**

Use três acentos graves ( &grave;&grave;&grave; ) antes e depois das linhas de código. Certifique-se de que os tiques abertos e fechados sejam recuados com o mesmo número de espaços. Para uma renderização ideal, especifique uma linguagem de código.

&grave;&grave;&grave;`javascript`

**Exemplo**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### Realce de sintaxe para blocos de código

A Experience League aceita realce de sintaxe para blocos de código. Especifique um idioma como `java` após o conjunto de acentos graves de abertura para ter certeza de que a sintaxe está realçada corretamente. Para obter uma lista de idiomas válidos, consulte [https://prismjs.com](https://prismjs.com/#supported-languages). Se algum idioma estiver ausente, registre um tíquete no jira.

### Numeração de linha em blocos de código

Adicione `{line-numbers="true"}` depois do idioma para habilitar a numeração de linha.

Exemplo com números de linha (&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Iniciar numeração na linha _**

Adicione `start-number="n"` após a sintaxe de número de linha para iniciar a numeração em um número diferente de 1.

Exemplo com a nova linha inicial (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Realce de linha em blocos de código

Adicionar `highlight="n"` após a sintaxe de número de linha para destacar linhas em um bloco de código. Especificar `11-13, 16` destacará as linhas 11 a 13 e 16.

Exemplo com realce de linha (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Formatação de variáveis em blocos de código

Sintaxe de variável, como `<i>italic</i>`, não tem suporte em blocos de código. Para indicar texto variável, uma opção é usar colchetes `< >`.

## Seções flexíveis

Você pode criar uma seção recolhível (às vezes chamada de **acordeão**) que fica oculta por padrão. O usuário pode clicar no título para expandir ou recolher a seção.

O texto flexível pode ser usado para simplificar conteúdo complexo, como simplificar uma página de perguntas frequentes ou desorganizar um procedimento complexo com listas aninhadas. Por exemplo, em vez de exibir um conjunto de subetapas, é possível recolher as subetapas em uma seção &quot;Exibir detalhes&quot;.

**Sintaxe**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**Exemplo**

+++Ver detalhes
Este é o texto dentro de uma seção que pode ser recolhida.

* Marcador um
* Marcador dois
* Marcador três

+++

**Notas**

* Não aninhe seções que podem ser recolhidas em seções que podem ser recolhidas. Seções recolhíveis aninhadas não são renderizadas corretamente. No entanto, eles não causam falha na validação, portanto, os usuários verão a sintaxe `+++` da seção aninhada.
* Certifique-se de adicionar linhas em branco acima e abaixo de itens como listas de marcadores e blocos de código dentro da seção recolhível, ou você receberá um erro de validação.
* Você pode adicionar cabeçalhos dentro de seções que podem ser recolhidas, mas isso não é recomendado.
* [Acordeões nem sempre são a resposta para conteúdo complexo em desktops](https://www.nngroup.com/articles/accordions-complex-content/)
* Uma desvantagem histórica de seções que podem ser recolhidas é que **Localizar na Página** (Ctrl/Cmd+F) ignora o texto recolhido. Embora isso ainda seja verdade no Safari, não é mais verdade no Chrome; Localizar na página detecta texto recolhido no Chrome.
* Exemplo de uma página de [atualizações de manutenção](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) usando seções recolhíveis.

## Comentários e observações

Os comentários não aparecem no sistema de ajuda renderizado. Use comentários para deixar anotações para você ou para outros escritores. Também é possível usar comentários em seções de rascunho de texto.

Para comentários, lembre-se de que, embora não sejam renderizados no sistema de ajuda, eles ficam visíveis para usuários que editam arquivos do Markdown em GitHub.com. Não inclua informações confidenciais em comentários.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

Você não poderá ver o texto abaixo dele (&quot;Você não pode me ver&quot;), a menos que esteja editando o documento.

<!--
You can't see me (unless you're editing in Git).
-->

**Lembrete:** comentários (observações) não aparecem nos artigos de ajuda voltados ao público. No entanto, os comentários aparecem nos arquivos do Markdown voltados ao público que os usuários podem visualizar e editar.

>[!IMPORTANT]
>
Evite adicionar comentários em componentes de bloco, como listas de marcadores, especialmente listas de marcadores aninhadas. O comentário pode alterar como a lista de marcadores é renderizada.
>
No arquivo TOC.md, não comente linhas no meio da lista TOC. Isso pode quebrar a lista de índice e causar erros de validação. Em vez disso, mova os comentários do sumário para o final do arquivo.

## CONTEXTUALHELP

Os autores podem trabalhar com equipes de produtos para adicionar popovers de ajuda na interface do usuário do produto Experience Cloud ou Experience Platform. Exemplo:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## Listas de definições

Para listas de definição, ainda não oferecemos suporte à sintaxe padrão do Markdown. Em vez disso, use a formatação manual como esta:

```
**Frog** - An amphibious green creature. Likes flies.
```

Renderizado:

**Sapo** - Uma criatura verde anfíbia. Gosta de moscas.

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## Baixar arquivos

Faça upload do arquivo .zip ou outro arquivo que possa ser baixado no diretório de ativos e vincule-o. Se for um arquivo .zip, clicar no link baixará o arquivo. Se for um tipo de arquivo, como PDF ou PNG, que pode ser aberto em um navegador, clicar no link abrirá uma nova guia. Para esses arquivos, considere compactá-los ou fornecer instruções para clicar com o botão direito do mouse no link e baixar.

`Download` &amp;lbrack;`download-test.zip`&amp;rbrack;`(assets/download-test.zip)`

Renderizado:

Baixar [zip de teste de download](assets/download-test.zip)

>[!NOTE]
>
O tamanho máximo para arquivos e imagens baixados é de 100 MB. Esse é o limite do github.com. O limite do git.corp.adobe.com é maior (250 MB), mas precisamos copiar arquivos para o espelho do github.com.

## Cabeçalhos {#headings}

No Markdown, use sinais de libra (`#`) para identificar níveis de cabeçalho. O primeiro nível (`#`) é o título do artigo, que também é especificado no cabeçalho de metadados. Mantenha-os iguais. O segundo nível (`##`) representa os cabeçalhos principais da página que será incluída no miniTOC. Se você está acostumado a escrever em AEM (chl-author), os cabeçalhos de nível 2 (`##`) são mapeados para o componente de &quot;Cabeçalho 1&quot; no AEM.

Contagem máxima de caracteres para cabeçalhos: 69 caracteres (inglês) / 120 caracteres (LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**Práticas recomendadas de cabeçalho**

* Certifique-se de que um cabeçalho de nível 1 (`#`) siga uma linha em branco após os metadados em cada artigo.
* Não pule níveis, como saltar do nível 2 (`##`) para o nível 4 (`####`).
* Inclua uma linha em branco *antes* e *depois* de cada cabeçalho.
* Se um cabeçalho incluir numerais, especifique uma ID de cabeçalho explícita que não comece com um número, como `## Release notes for 2016 {#release-notes-2016}`.
* Recomendamos apenas 3 níveis de cabeçalho. Os níveis 4 e posteriores não estão sendo renderizados corretamente no momento.
* Os títulos são exibidos na navegação à direita para que os usuários possam clicar em para ir para uma seção. Por padrão, dois níveis de cabeçalho aparecem na navegação à direita. Se quiser alterar o número de níveis, use `mini-toc-levels` metadados, como `mini-toc-levels: 3`.

**IDs de cabeçalho**

As IDs de cabeçalho (também chamadas de *IDs de âncora*) são usadas para criar deep links personalizados para seções dentro de artigos. Para especificar uma ID de cabeçalho, use este formato:

```
## Creating processing rules {#processing-rules}
```

As IDs de cabeçalho devem estar em minúsculas e hifenizadas.

Se você não especificar uma ID de cabeçalho para um cabeçalho, a ID de cabeçalho padrão será o cabeçalho &quot;slugified&quot; (minúsculas e hifenizadas). Por exemplo, o cabeçalho `## Creating widgets and Such` terá uma âncora `#creating-widgets-and-such`.

## Sintaxe de HTML {#html}

Por vários motivos, incluindo segurança e acessibilidade, limitamos a sintaxe de HTML que pode ser usada no Markdown. A lista a seguir mostra a sintaxe de HTML suportada. Qualquer sintaxe de HTML que não estiver nessa lista resultará em um erro de validação.

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

Se quiser que a sintaxe de HTML seja adicionada a essa lista, registre um tíquete ou entre em contato com a equipe do SSE.

## Imagens {#images}

Use a sintaxe `![]()` para imagens. Os colchetes `[ ]` incluem texto alternativo, e os parênteses `( )` incluem o local da imagem e o texto de focalização opcional (dica de ferramenta). O ponto de exclamação distingue uma imagem de um link.

```
![alt text](assets/logo.png "Hover text")
```

![alt text](assets/logo.png "Focalizar texto")

Para imagens compartilhadas, você pode colocar as imagens em uma pasta de ativos raiz e usar um link raiz que funcione de qualquer arquivo em um repositório:

```
/help/assets/imagename.png
```

### Redimensionamento e alinhamento de imagens

**Propriedades da imagem (com imagem alinhada à direita)** ![texto alternativo](assets/premium.png "Texto ao passar o mouse Premium"){align="right"}

Use a sintaxe como a seguir para alterar a largura ou o centro da imagem padrão ou alinhe a imagem à direita na exibição de página ou na célula da tabela.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

Renderizado:

Bob - Largura = 300 pixels abaixo

![Texto alternativo da imagem de mergulho](assets/maui-dive.jpg "Focalizar texto - A largura de mergulho de Maui é de 300 pixels e centralizada"){width="300" align="center"}

* Para imagens grandes, recomendamos que você crie imagens grandes o suficiente para serem dimensionadas para se ajustarem à largura da página (pelo menos 640 pixels de largura). A largura recomendada é de 1500 pixels. Não há necessidade de criar imagens com mais de 2500 pixels ou 500 kilobytes. O tamanho máximo de arquivo para imagens é 100 MB.
* Para imagens pequenas, crie imagens usando a largura desejada em pixels ou use o parâmetro de largura, como `{width="250"}` (pixels) ou `{width="50%"}` (porcentagem da área de exibição, não tamanho da imagem original). As imagens são dimensionadas proporcionalmente. Observe que as imagens podem ser aumentadas ou diminuídas, portanto, tenha cuidado com a pixelação.
* Em alguns casos, imagens da mesma interface parecerão fora de proporção na página, pois imagens mais largas (como uma barra de ferramentas) são dimensionadas para baixo, enquanto imagens estreitas (como um painel) não são dimensionadas para baixo. Nesses casos, considere diminuir o tamanho das imagens mais amplas para melhorar a consistência visual.
* É possível alterar o alinhamento de uma imagem na área de exibição. Use `{align="center"}` ou `{align="right"}`. O parâmetro `valign` não tem suporte.

>[!NOTE]
>
O tamanho máximo de arquivo para imagens é 100 MB. Esse é o limite do github.com. O limite do git.corp.adobe.com é maior (250 MB), mas precisamos copiar arquivos para o espelho do github.com.

### Links de imagem

Se você quiser permitir que os usuários cliquem em uma imagem para ir para uma página diferente, use este formato.

**Sintaxe**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**Exemplo**

Clique nesta imagem para ir para o site do Adobe.

[![imagem](assets/core-services_96.png)](https://www.adobe.com)

### Clique para ampliar imagens

Use o parâmetro `zoomable` para permitir que os usuários cliquem em uma imagem para exibir uma versão ampliada da imagem. Quando o usuário passa o mouse sobre uma imagem com zoom, o ponteiro se torna uma lupa. Quando clicada, a imagem se expande até a largura total do navegador. Ele pode ser descartado com um botão Fechar.

**Exemplo**

![Imagem de mergulho](/help/data-sheets/hidden/assets/maui-dive.jpg "Mergulhando em Maui"){width="100" zoomable="yes"}

**Sintaxe**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## Links e referências cruzadas {#links-and-cross-references}

Os links externos são diretos e podem ser renderizados como uma legenda vinculada ou um URL puro.

```
[Adobe](https://www.adobe.com)
```

Renderizado:

[Adobe](https://www.adobe.com)

Se você adicionar um URL diretamente ao texto, ele não será convertido em um link automaticamente. Para que uma URL apareça como um link, adicione a sintaxe `< >`. Exemplos:

```
https://www.adobe.com

<https://www.adobe.com>
```

Renderizado:

https://www.adobe.com

<https://www.adobe.com>

Os links para artigos (referências cruzadas) podem ser um pouco mais complexos.

**Opção 1: link relativo padrão**

Veja como um link relativo padrão se parece:

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

O nome do caminho precisa levar em conta o local do arquivo de origem e do arquivo de destino. Você pode usar todos os operandos de links relativos, como `./` (diretório atual), `../` (voltar um diretório) e `../../` (voltar dois diretórios).

**Opção 2: link relativo de raiz**

A vantagem desse tipo de link é que ele precisa levar em conta apenas o arquivo de destino. Funciona a partir de qualquer arquivo de origem no repositório, independentemente do local do arquivo de origem.

```
/help/using/docile-rules/introduction.md
```

**Deep linking**

Para vincular a um cabeçalho em um artigo, o cabeçalho de destino deve ter uma ID de cabeçalho explícita (também chamada de &quot;ID de âncora&quot;). Exemplo:

`## Creating audience segments {#creating-audience-segments}`

Para vincular a este cabeçalho na mesma página, use a ID do cabeçalho como o link:

`See [Creating audience segments](#creating-audience-segments)`

Para vincular a este cabeçalho a partir de um artigo diferente no repositório, adicione o sufixo de ID do cabeçalho ao final do link:

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**Abrir em nova guia**

Se quiser que um link abra uma nova guia, como quando você pular para um guia diferente, use a propriedade `{target="_blank"}` no link.

Exemplo:

`[See What's new](whats-new.md){target="_blank"}`

## Metadados

Adicione metadados à parte superior do arquivo de marcação. A próxima linha após a linha de metadados (e linha em branco) DEVE ser o título do artigo (nº do título).

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## Tags de localização: UICONTROL, DNL e DONOTLOCALIZE

Todo o conteúdo de ajuda do Markdown é localizado usando a tradução automática inicialmente. Se a ajuda nunca foi localizada, mantemos a tradução automática. No entanto, se o conteúdo da ajuda tiver sido localizado no passado, o conteúdo traduzido por máquina atuará como um espaço reservado, enquanto o conteúdo estiver passando por tradução humana.

## Mais artigos como este

Use o componente &quot;Mais artigos como este&quot; para exibir links relacionados no final de um artigo. Quando renderizado, o componente MORELIKETHIS é renderizado como &quot;Artigos Relacionados&quot; (e localizado em outros idiomas).

**Sintaxe**

![Mais artigos como esta sintaxe](assets/morelikethis.png)

**Exemplo**

>[!MORELIKETHIS]
>
* [Article 1](https://helpx.adobe.com/br/support/analytics.html)
* [Article 2](https://helpx.adobe.com/br/support/audience-manager.html)

## Observações / admoestações

Estendemos o Markdown para formatar vários tipos de notas: Nota, Dica, Importante e Aviso.

**Sintaxe**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**Exemplo**

>[!NOTE]
>
Esta é um bloco NOTA padrão.

**Sintaxe**

```
>[!TIP]
>
>This is a standard tip.
```

**Exemplo**

>[!TIP]
>
Esta é uma dica padrão.

**Sintaxe**

```
>[!WARNING]
>
>This is a standard warning block.
```

**Exemplo**

>[!WARNING]
>
Este é um bloco de aviso padrão.

**Sintaxe**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**Exemplo**

>[!IMPORTANT]
>
Este é um bloco padrão importante.

**Sintaxe**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**Exemplo**

>[!NOTE]
>
Esta é um bloco NOTA padrão.
>
Inclui vários parágrafos.

Novos tipos de observações compatíveis:

>[!ADMIN]
>
Esta é uma nota de administração. Somente EXL.

>[!AVAILABILITY]
>
Esta é uma nota de disponibilidade. Somente EXL.

>[!PREREQUISITES]
>
Esta é uma nota de pré-requisitos. Somente EXL.

>[!INFO]
>
Esta é uma nota informativa. Somente EXL.

>[!ERROR]
>
Esta é uma nota de erro. Somente EXL.

>[!SUCCESS]
>
Esta é uma nota de sucesso. Somente EXL.

## Listas numeradas e listas com marcadores {#lists}

Para criar listas numeradas, comece uma linha com `1.` ou `1)`, mas escolha um método e use-o consistentemente no artigo. Você não precisa especificar os números. O GitHub faz isso para você.

Use o número `1` para cada etapa da lista numerada.

Adicione linhas em branco antes e depois das listas.

**Sintaxe**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**Exemplo**

1. This is step 1.

   1. Subetapa

   1. Subetapa

1. This is the next step.

1. This is yet another step, the third.

Para criar listas de itens, comece uma linha com `*` ou `-` ou `+`, mas escolha um método e use-o consistentemente no artigo. (Se você misturar os formatos, como `*` e `+`, receberá um erro de validação do Markdown ao fazer check-in do arquivo.)

**Prática recomendada:** Use `*` para marcadores. O Visual Studio Code aplica o asterisco para marcadores, portanto, é mais fácil permanecer com asteriscos para automatizar a criação de uma lista não ordenada. (Talvez você tenha notado que o arquivo TOC.md usa os sinais de adição `+` para listas. Isso é um remanescente da migração. Qualquer marcador válido funcionaria desde que fosse consistente dentro do artigo.)

**Sintaxe**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**Exemplo**

* First item in an unordered list.
* Another item.
* Here we go again.

Também é possível incorporar listas em listas e adicionar conteúdo entre itens de lista. Recuar conteúdo entre itens de lista para evitar o início de uma nova lista. Os itens entre etapas devem ser recuados até o início do texto: 3 espaços para listas numeradas, 2 espaços para listas de marcadores.

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**Exemplo**

1. Set up your table and code blocks.
1. Perform this step.

   ![tela](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   This is note text.

1. Do another step.

   Esta é uma linha recuada.

OBSERVAÇÃO: se você recuar muito, como 6 espaços em vez de 3, o conteúdo nessa linha será tratado como um bloco de código.

## Sombrear Caixas

As caixas de sombra são úteis para desativar uma seção de conteúdo do restante da página. Por exemplo, a equipe do Workfront gosta de adicionar caixas de &quot;Exemplo&quot;, que contêm texto, imagens e exemplos de código para atingir uma finalidade específica. Uma caixa de sombra também pode ser útil para seções &quot;Por conta própria&quot; ou &quot;Caso de uso&quot;, ou para notas ou dicas estendidas.

Para criar uma caixa de sombra, adicione `>[!BEGINSHADEBOX]` no início da seção e `>[!ENDSHADEBOX]` no final. Todo o conteúdo entre essas tags de início e término terá um plano de fundo cinza. Adicionar um rótulo a `BEGINSHADEBOX` (como `>[!BEGINSHADEBOX "Use Case]`) é uma maneira opcional de criar um título de caixa de sombra em negrito. Você também pode simplesmente adicionar um texto em negrito ou um cabeçalho na linha seguinte.

Exemplo:

>[!BEGINSHADEBOX]

**Removendo a borda em uma tabela de HTML**

Em alguns casos, você usa uma tabela de HTML para criar um design balanceado, mas não quer que o conteúdo se pareça com uma tabela. Para desativar uma borda para uma tabela de HTML de uma linha, use esta sintaxe:

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
Não use demais. Para tabelas normais, queremos manter um design consistente em todo o conteúdo.

![dica de tabela](assets/table-no-border.png)

Em uma tabela de três colunas, você também pode adicionar `<td align="center">` e `<td align="right">` para distribuir o conteúdo da célula uniformemente pela área de exibição. Se não fosse assim, eu teria lhe dito.

Esta é a última linha da caixa de sombra.

>[!ENDSHADEBOX]

## Trechos e inclusões

Para compartilhar texto entre artigos em um repositório, crie uma pasta `_includes` na pasta `help`. Esta pasta `_includes` pode ter arquivos .md que podem ser referenciados (incluídos) de outros arquivos no repositório. Além disso, um arquivo `snippets.md` nesse repositório pode incluir âncoras Head2 que podem ser referenciadas a partir de qualquer arquivo no repositório.

Referência a H2 no arquivo snippets.md: `{{id-name}}`

Referência para incluir arquivo: `{{$include /help/_includes/filename.md}}`

## Tabela

As tabelas podem ser problemáticas no Markdown. Quando as tabelas são migradas do sistema de criação anterior, as tabelas simples (uma linha por célula) são formatadas como tabelas nativas do Markdown (preferencial). Tabelas mais avançadas são formatadas como HTML.

>[!TIP]
>
Assista ao [vídeo sobre Tabelas do Markdown](https://video.tv.adobe.com/v/26220)

Tabelas nativas frequentemente têm melhor aparência no Markdown. As colunas são dimensionadas de acordo com seu conteúdo. As tabelas de HTML são renderizadas com colunas de igual largura.

Por padrão, o Markdown não é compatível com várias linhas ou listas em células. No entanto, estendemos as tabelas do Markdown para permitir várias linhas em células (usando `<p>` ou `<br>`) ou listas básicas (usando `<ul><li>` etc.).

>[!IMPORTANT]
>
Tenha cuidado ao adicionar esses códigos de HTML às tabelas do Markdown. Se a sintaxe estiver incorreta, você receberá um erro de validação confuso que não descreve com precisão o problema. Verifique a sintaxe do HTML para garantir que ela esteja bem formada.

Não permitido em nenhuma tabela: iframes, extensões de células, tabelas incorporadas.

Não permitido na tabela nativa do Markdown: listas aninhadas ou complexas.

Ver [Tabelas](tables.md)

**Sintaxe**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**Exemplo**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Tabelas simples funcionam adequadamente no Markdown. No entanto, as tabelas que incluem vários parágrafos ou listas dentro de uma célula são difíceis de trabalhar. Para tal conteúdo, recomendamos usar um formato diferente, como cabeçalhos e texto.

**Tabela de Markdown com quebras de parágrafo e listas**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**Exemplo**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | primeiro parágrafo na célula<p>segundo parágrafo na célula(`<p>`)<br>quebra de linha (`br`) | row 1 column 3 |
| row 2 | lista de marcadores<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |

**Tabela de Markdown com quebras de linha e lista falsa**

Solução alternativa com marcadores manuais.

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**Exemplo**

| Cor | Coisas para fazer |
|--- |--- |
| Vermelho | * Ler <br> * Gravar <br> * Estudo |
| Azul | * Swim <br> * Run <br> * Lift <br> **Observação**: lembre-se de treinar inteligente. |


## Guias

Uma guia é uma área clicável na parte superior de uma seção que mostra conteúdo diferente. Quando uma guia é clicada, o conteúdo da guia é exibido e o conteúdo de outras guias fica oculto.

Para criar um conjunto de guias, adicione `>[!BEGINTABS]` no início do conjunto de guias e `>[!ENDTABS]` depois da última guia. Adicione `>[!TAB <tab title>]` tags para cada seção de guia e adicione o conteúdo de cada guia abaixo dela.

**Sintaxe de guia**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**Renderizado**

>[!BEGINTABS]

>[!TAB iOS]

Esse conteúdo aparece na guia iOS.

>[!TAB Android]

Esse conteúdo aparece na guia Android.

>[!TAB Janelas]

Esse conteúdo aparece na guia Windows.

>[!TAB MacOS]

Esse conteúdo aparece na guia MacOS.

>[!TAB Linux]

Esse conteúdo aparece na guia Linux.

>[!ENDTABS]

**Anotações da guia**

* Os usuários não podem usar a pesquisa na página (Ctrl+F/Cmd+F) para localizar conteúdo em guias que não são exibidas.
* Se os títulos das guias se estenderem além da largura da exibição de página no navegador do usuário, uma barra de rolagem horizontal será exibida.
* Não é possível formatar os títulos das guias. Qualquer sintaxe adicionada será passada como parte do título. Por exemplo, `>[!TAB **iOS**]` será exibido como `**iOS**`.
* É possível criar vários conjuntos de guias em uma página, mas não é possível aninhar um conjunto de guias em outro conjunto de guias.
* Um plano de fundo sombreado é aplicado ao conjunto de guias para que os usuários possam ver e distinguir o conteúdo da guia de outro conteúdo.

## Destaque de texto

A equipe do Workfront pediu para usar o realce amarelo para indicar a pré-visualização dos recursos futuros. Veja como funciona.

Exemplo:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Renderizado:

Todo este parágrafo NÃO deve ser destacado. <span class="preview"> Esta palavra está em **negrito** dentro de uma frase destacada.</span> E esta é apenas a última frase.

Como regra geral, use `<span class="preview">` para realçar um parágrafo ou texto dentro de um parágrafo, e use `<div class="preview">` para vários parágrafos e componentes.

>[!NOTE]
>
Ainda estamos trabalhando para melhorar a exibição de realce de determinados elementos da página, como notas e tabelas. Fique à vontade para registrar bugs de JIRA se visualizar uma renderização incorreta. Em andamento.
>
A visualização do VSC ainda não oferece suporte ao realce.

## Vídeo

Os vídeos não serão renderizados nativamente no Markdown. Para exibir um vídeo em linha, use o indicador de componente `[!VIDEO]` e depois a url.

**Sintaxe**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**Exemplo**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## Informações adicionais de sintaxe do Markdown

### Componentes estendidos do Markdown

Precisamos estender o Markdown para oferecer suporte a itens que não estão incluídos no Markdown comum.

Os componentes especiais são declarados em uma aspa de bloco contêiner usando colchetes e um ponto de exclamação mais a referência para o tipo de bloco que é. Por exemplo, veja como declarar uma nota:

```
>[!NOTE]
>
>This is a note.
```

* Notas (admoestações), incluindo Nota, Importante, Dica, Cuidado e Aviso
* Vídeo incorporado
* Mais artigos similares
* Várias tags de interface para localização
* Propriedades de componente para cabeçalhos, imagens e blocos de código
* Seções flexíveis
* Destaque de texto
* Guias de página

Use a aspa de bloco ( `>` ) do Markdown no início de cada linha para unir um componente baseado em parágrafo, como uma observação. Para melhorar a visualização, adicione uma linha imediatamente após o início da seção que tenha apenas um símbolo de citação de bloco (`>`). Para finalizar a seção, adicione uma linha em branco.

Se você precisar usar subcomponentes dentro de componentes, adicione um nível extra de aspas de bloco (`>  >`) para essa seção de subcomponente. Por exemplo, uma NOTA em uma seção DONOTLOCALIZE deve começar com `>  >`.

Em alguns casos, precisamos suportar configurações específicas para elementos do Markdown, como cabeçalhos. Se você precisar alterar as configurações padrão, adicione os parâmetros em chaves francesas `{# }` após o componente.

### Linhas em branco

Você pode adicionar algum espaço para respirar às suas paredes de texto com linhas em branco. Use `<br>&nbsp;` como solução alternativa para adicionar uma linha em branco.

Exemplo: esta é uma primeira frase do que pode ser um texto muito longo. Deixe-me inserir uma linha em branco entre este parágrafo e o próximo.

<br> 

Isso pode não parecer muito impressionante aqui, mas tente linhas em branco quando você achar que suas páginas estão muito cheias.

### Caracteres a serem &quot;escapados&quot; {#characters-to-escape}

Vários caracteres (`# { } [ ] < > * + - . !`) têm um significado especial no Markdown ou no HTML para a criação de cabeçalhos, imagens, listas e outros componentes. Ao usar esses caracteres, o mecanismo de renderização pensa que você está adicionando código. No entanto, em alguns casos, você deseja exibir esses caracteres no texto. Para fazer isso, você precisa &quot;escapar&quot; os caracteres. O método de escape mais fácil é preceder o caractere com uma barra invertida (`\`). Por exemplo, se você deseja iniciar uma linha com um caractere `#` para que ela não seja interpretada como um cabeçalho, você digitaria `\#`:

`\# This is not a heading`

**Renderizado:**

\# Isto não é um cabeçalho

A barra invertida funciona somente com estes caracteres: `# { } [ ] * + - . !`. Se você precisar escapar caracteres como colchetes angulares (como `<yourname>`), poderá colocar o texto entre acentos graves para aplicar um bloco de código em linha ou usar o código da entidade HTML em vez do caractere. Exemplos de códigos HTML comuns:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

Uma lista completa de entidades HTML está disponível no [site de formatação livre](https://www.freeformatter.com/html-entities.html). Isso permitirá que você procure todos os caracteres especiais.

>[!NOTE]
>
Para etapas de cadeia, como &quot;Escolher arquivo > Salvar como&quot;, você não precisa usar o caractere `>` como escape porque ele não está ao lado de outros caracteres. Para variáveis como `<filename>`, você desejará usar o escape entre colchetes usando o bloco de código `backticks` ou os códigos de caractere (`&lt;filename&gt;`).

Se você usar entidades HTML em blocos de código, o texto da entidade não será convertido no caractere especial. Por exemplo, `&gt;` aparece em um bloco de código como &quot; `&gt;` &quot; em vez de &quot; > &quot;.

Para escapar acentos graves ( &grave; ), use `&grave;` ou insira o acento grave dentro de acentos graves triplos que envolvem um bloco de código em linha.

### Itens incompatíveis

Existem alguns itens do Markdown com sabor de Git que não pretendemos suportar. A ferramenta de visualização que você usa pode ativar alguns desses recursos, mas não depende disso.

**Lista de tarefas**

Não suportado

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**Emoji**

Não suportado

```
:bowtie:
```

**Regra horizontal**

Não suportado

```
***
```

**Cotas de bloqueio**

Usamos aspas de bloco (`>` no início de uma linha) para indicar a sintaxe estendida do Markdown, como notas e vídeos, descrita a seguir. Mas você também pode usar a sintaxe `>` para criar uma seção de citação em bloco.

>[!NOTE]
>
Se você recuar muito, como seis espaços em vez de três, o conteúdo será renderizado como aspas de bloco. Use a quantidade adequada de recuo para evitar que o conteúdo seja renderizado incorretamente como uma aspa de bloco.
