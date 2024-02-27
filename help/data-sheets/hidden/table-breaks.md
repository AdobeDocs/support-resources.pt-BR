---
title: Quebras de tabela
description: Teste de diferentes quebras de tabela
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# Quebras de tabela

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
