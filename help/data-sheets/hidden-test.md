---
title: Página de teste oculta
description: Esta página está oculta da pesquisa e do índice
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download premium"
badgeExam: label="Exame ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# Página de teste oculta

Ativar? Verifique o envio novamente por volta das 15:10. Será que ele entrará em funcionamento às 15:30?

## Botões

[Padrão do botão](https://www.adobe.com/)

**[Botão principal](https://www.adobe.com/)**

_[Botão Secundário](https://www.adobe.com/)_

**_[Botão Terciário](https://www.adobe.com/)_**

## Visualizar problema

O parágrafo a seguir não é renderizado corretamente na Visualização do VSC. Não sei por quê.

Se sua senha for gerenciada pela [!DNL Adobe], você pode [alterar a senha na sua conta da Adobe](https://helpx.adobe.com/br/manage-account/using/change-or-reset-password.html){target="_blank"}.

## Tipos de nota

Todos os tipos de notas compatíveis.

>[!NOTE]
>
>Esta é um bloco NOTA padrão.

>[!TIP]
>
>Esta é uma dica padrão.

>[!IMPORTANT]
>
>Essa é uma nota importante.

>[!WARNING]
>
>Isso é um aviso.

>[!CAUTION]
>
>Isso é um alerta.

>[!ADMIN]
>
>Esta é uma nota de administração que é renderizada como ADMINISTRAÇÃO. Somente EXL.

>[!AVAILABILITY]
>
>Esta é uma nota de disponibilidade. Somente EXL.

>[!PREREQUISITES]
>
>Esta é uma nota de pré-requisitos. Somente EXL.

>[!INFO]
>
>Esta é uma nota informativa. Somente EXL.

>[!ERROR]
>
>Esta é uma nota de erro. Somente EXL.

>[!SUCCESS]
>
>Esta é uma nota de sucesso. Somente EXL.

>[!MORELIKETHIS]
>
>* Página 1
>* Página 2

## Emblemas

Um emblema é um rótulo colorido usado como indicador de conteúdo. Por exemplo, é possível adicionar um emblema para marcar um artigo como _Beta_ ou uma seção como _Premium_. É possível alterar a cor de um emblema e associar um URL e uma dica de ferramenta.

[!BADGE Exemplo de emblema]

Há dois tipos of emblemas, cada um com sintaxe diferente:

* **Metadados**: exibe o emblema próximo à parte superior de uma página
* **Em linha**: exibe o emblema onde a sintaxe está localizada

### Emblemas de metadados

A adição da sintaxe do emblema nos metadados coloca um emblema acima do título da página (H1) no artigo.

É possível nomear emblemas, por exemplo, usando _emblema1_ ou _emblema2_. Ou você pode ser mais criativo (desde que o nome comece com _emblema_).

Exemplos de metadados:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium:** este exemplo exibe um emblema Premium com um URL e uma dica de ferramenta.

* **badgeExam:** este exemplo exibe um emblema escuro com um número de ID de exame.

#### Emblemas em linha

Especifique as informações do emblema em sua própria linha ou em um cabeçalho, tabela ou outro elemento de página.

Esta é a sintaxe de um emblema em linha com um rótulo beta, cor azul, URL e dica de ferramenta:

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### Cores de emblemas disponíveis

Os emblemas usam cores definidas no Adobe Spectrum:

| Tipo | Emblema |
|---|---|
| Informativo (padrão) | [!BADGE Beta]{type=Informative url="https://www.exemplo.com"} |
| Positivo | [!BADGE Novo recurso]{type=Positive url="https://www.example.com" tooltip="Ir para example.com"} |
| Negativo | [!BADGE Descontinuado]{type=denied tooltip="Este recurso agora é o fim da vida útil"} |
| Neutro | [!BADGE Talvez]{type=Neutral tooltip="Um cavaleiro caiu do cavalo..."} |
| Cuidado | [!BADGE Atenção]{type=Caution tooltip="Yellow status"} |

Exemplos de sintaxe

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### Requisitos para emblemas

* Somente dois emblemas são permitidos nos metadados. Essa regra é configurável, portanto, informe-nos se você precisa de uma exceção.
* Somente o rótulo do emblema é obrigatório. Os parâmetros `type`, `url` e `tooltip` são opcionais. O parâmetro `type` determina a cor. O parâmetro `url` permite que os usuários cliquem no emblema para abrir um artigo ou página. O parâmetro `tooltip` exibe o texto da dica de ferramenta ao passar o mouse.
* Adicionar um emblema ao arquivo `TOC.md` exibe o emblema em cada artigo no guia. Se você especificar um URL para o emblema pular para um artigo, use um link raiz (por exemplo, `/help/guide/article.md`) não um link relativo (por exemplo, `article.md`) para levar em conta os artigos em pastas diferentes.
* Adicionar um emblema ao `metadata-new.md` exibe o emblema em cada artigo em um repositório.
* Para emblemas de metadados, verifique se todos os valores estão entre aspas. Para emblemas em linha, verifique se `url` e `tooltip` estão entre aspas.
* Os valores de tipo válido incluem *Informativo* (padrão, azul), *Positivo* (verde), *Negativo* (vermelho), *Neutro* (cinzento escuro) e *Cuidado* (amarelo).
* Os rótulos de emblema são localizados.
* Se vários emblemas de metadados forem especificados, eles serão exibidos em ordem alfabética com base em seu nome, como `badge1:` ou `badgeWeb`.
* Se quiser que o URL seja aberto em uma nova guia, use esta sintaxe:

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  Renderizado:

  [!BADGE Abrir em nova guia]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Abrir adobe.com em nova guia"}

## Destaque de texto

A equipe do Workfront pediu para usar o realce amarelo para indicar a pré-visualização dos recursos futuros. Veja como funciona.

Exemplo 1:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Renderizado:

Todo este parágrafo NÃO deve ser destacado. <span class="preview"> Esta palavra está em **negrito** dentro de uma frase destacada.</span> E esta é apenas a última frase.

Exemplo 2:

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

Renderizado:

O realce deve começar após este parágrafo.

<div class="preview">

Início da DIV.

Este é um novo parágrafo, depois uma imagem

![imagem](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Último item realçado.

</div>

Não realçado

## Realce de sintaxe para blocos de código

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