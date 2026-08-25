---
title: Como aplicar um patch isolado fornecido pelo Adobe
description: Este artigo instrui como aplicar um patch isolado para Adobe Commerce no local, infraestrutura do Adobe Commerce na nuvem e Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
source-git-commit: 45b00b9b0d2ceb422747c0a4a34f060f33ab127b
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Como aplicar um patch isolado fornecido pelo Adobe

Este artigo instrui como aplicar um patch isolado para Adobe Commerce no local, infraestrutura do Adobe Commerce na nuvem e Magento Open Source.

>[!WARNING]
>
>É altamente recomendável aplicar e testar o patch no ambiente de Preparo/Integração antes de aplicá-lo à Produção. Também recomendamos que você tenha um backup recente antes de qualquer manipulação.

## Como aplicar um patch isolado para a infraestrutura do Adobe Commerce na nuvem {#cloud}

1. Se você não tiver um diretório chamado `m2-hotfixes` na raiz do projeto, crie um.
1. Copie o(s) arquivo(s) `%patch_name%.patch` para o diretório `m2-hotfixes`.
1. Adicionar, confirmar e enviar por push suas alterações de código:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

Para obter informações adicionais sobre como aplicar patches a projetos na nuvem, consulte [Aplicar patches](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches).

## Como aplicar um patch Isolado para o Adobe Commerce no local e o Magento Open Source {#commerce}

1. Faça upload do patch para o seu diretório raiz do Adobe Commerce no local ou Magento Open Source.
1. Execute o seguinte comando SSH:

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   (Se o comando acima não funcionar, tente usar `-p2` em vez de `-p1`)

1. Para que as alterações sejam refletidas, atualize o cache no [!UICONTROL Administrador] em **[!UICONTROL Sistema]** > **[!UICONTROL Gerenciamento de Cache]**.
