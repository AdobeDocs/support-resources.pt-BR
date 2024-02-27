---
title: Quebras de tabela
description: Teste de diferentes quebras de tabela
hide: true
hidefromtoc: true
source-git-commit: 9ad23090cb13f36d6d015b23122736048fe2230c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 11%

---

# Quebras de tabela

Não há muito a ver aqui.

## Tabela de marcação padrão com `<br>`

**FIXO`Green<br>Red<br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br>Vermelho<br>Azul |
| Maria | 23 | Amarelo<br>Marrom |

{style="table-layout:fixed"}

**AUTOMÁTICO`Green<br>Red<br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br>Vermelho<br>Azul |
| Maria | 23 | Amarelo<br>Marrom |

{style="table-layout:auto"}

## Tabela do Markdown com duplo `<br>`s

**FIXO`Green<br><br>Red<br><br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br><br>Vermelho<br><br>Azul |
| Maria | 23 | Amarelo<br><br>Marrom |

{style="table-layout:fixed"}

**AUTOMÁTICO`Green<br><br>Red<br><br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br><br>Vermelho<br><br>Azul |
| Maria | 23 | Amarelo<br><br>Marrom |

{style="table-layout:auto"}

## Tabela do Markdown com `<p>`

**FIXO`Green<p>Red<p>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<p>Vermelho<p>Azul |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:fixed"}

**AUTOMÁTICO`Green<p>Red<p>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<p>Vermelho<p>Azul |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:auto"}

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Esta é a cor **verde** e se destina a envolver em uma linha diferente como um assunto e ou meio de testar as quebras de parágrafo acima. <p>Esta é a cor **vermelho** e se destina a envolver em uma linha diferente como um assunto e ou meio de testar as quebras de parágrafo acima. <p>Esta é a cor **azul** e se destina a envolver em uma linha diferente como um assunto e ou meio de testar as quebras de parágrafo acima. |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:fixed"}

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Esta é a cor **verde** e se destina a envolver em uma linha diferente como um assunto e ou meio de testar as quebras de parágrafo acima. <p>Esta é a cor **vermelho** e se destina a envolver em uma linha diferente como um assunto e ou meio de testar as quebras de parágrafo acima. <p>Esta é a cor **azul** e se destina a envolver em uma linha diferente como um assunto e ou meio de testar as quebras de parágrafo acima. |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:auto"}
