---
title: Quebras de tabela
description: Teste de diferentes quebras de tabela
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# Quebras de tabela

Não há muito a ver aqui.

## Tabela de marcação padrão com `<br>`

**CORRIGIDO`Green<br>Red<br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br>Vermelho<br>Azul |
| Maria | 23 | Amarelo<br>Marrom |

{style="table-layout:fixed"}

**AUTO`Green<br>Red<br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br>Vermelho<br>Azul |
| Maria | 23 | Amarelo<br>Marrom |

{style="table-layout:auto"}

## Tabela do Markdown com `<br>`s duplo

**CORRIGIDO`Green<br><br>Red<br><br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br><br>Vermelho<br><br>Azul |
| Maria | 23 | Amarelo<br><br>Marrom |

{style="table-layout:fixed"}

**AUTO`Green<br><br>Red<br><br>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<br><br>Vermelho<br><br>Azul |
| Maria | 23 | Amarelo<br><br>Marrom |

{style="table-layout:auto"}

## Tabela do Markdown com `<p>`

**CORRIGIDO`Green<p>Red<p>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<p>Vermelho<p>Azul |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:fixed"}

**AUTO`Green<p>Red<p>Blue`**

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Verde<p>Vermelho<p>Azul |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:auto"}

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Esta é a cor **verde** e destina-se a envolver uma linha diferente como um assunto e/ou meio de testar as quebras de parágrafo mencionadas anteriormente. <p>Esta é a cor **vermelha** e destina-se a envolver uma linha diferente como um assunto e/ou meio de teste acima mencionado quebras de parágrafo. <p>Esta é a cor **azul** e destina-se a envolver uma linha diferente como um assunto e/ou meio de teste das quebras de parágrafo acima mencionadas. |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:fixed"}

|  | Número | Cores |
|---|---|---|
| Juanya | 17 | Esta é a cor **verde** e destina-se a envolver uma linha diferente como um assunto e/ou meio de testar as quebras de parágrafo mencionadas anteriormente. <p>Esta é a cor **vermelha** e destina-se a envolver uma linha diferente como um assunto e/ou meio de teste acima mencionado quebras de parágrafo. <p>Esta é a cor **azul** e destina-se a envolver uma linha diferente como um assunto e/ou meio de teste das quebras de parágrafo acima mencionadas. |
| Maria | 23 | Amarelo<p>Marrom |

{style="table-layout:auto"}
