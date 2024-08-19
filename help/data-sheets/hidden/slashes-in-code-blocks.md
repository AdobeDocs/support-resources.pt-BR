---
title: Barras em blocos de código UGP-11189
description: Barras no teste UGP-11189 de blocos de código
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# Barra em blocos de código

1. Execute o comando:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Próxima etapa

Não está no bloco de código

fornecedor/bin/magento-patches -n status |grep &quot;27015\|Status&quot;

Barra invertida com escape:

fornecedor/bin/magento-patches -n status |grep &quot;27015&amp;bsol;|Status&quot;
