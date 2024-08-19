---
title: Barras em blocos de código UGP-11189
description: Barras no teste UGP-11189 de blocos de código
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Barra em blocos de código

1. Execute o comando:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Execute o comando (escaped):

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

Não está no bloco de código

fornecedor/bin/magento-patches -n status |grep &quot;27015\|Status&quot;

Escapado:

fornecedor/bin/magento-patches -n status |grep &quot;27015&amp;bsol;|Status&quot;

