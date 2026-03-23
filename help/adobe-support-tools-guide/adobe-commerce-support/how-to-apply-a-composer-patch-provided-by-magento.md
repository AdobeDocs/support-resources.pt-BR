---
title: Como aplicar um patch de compositor fornecido pelo Adobe
description: Este artigo instrui como aplicar um patch de compositor para Adobe Commerce no local, Adobe Commerce na infraestrutura em nuvem e Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
source-git-commit: fa46bb7187c55a0c7d75930868c74bf8ba072c41
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Como aplicar um patch de compositor fornecido pelo Adobe

Este artigo instrui como aplicar um patch de compositor para Adobe Commerce no local, Adobe Commerce na infraestrutura em nuvem e Magento Open Source.

>[!WARNING]
>
>É altamente recomendável aplicar e testar o patch no ambiente de Preparo/Integração antes de aplicá-lo à Produção. Também recomendamos que você tenha um backup recente antes de qualquer manipulação.

## Como aplicar um patch compositor para Adobe Commerce na infraestrutura em nuvem {#cloud}

1. Se você não tiver um diretório chamado `m2-hotfixes` na raiz do projeto, crie um.
1. Copie o(s) arquivo(s) `%patch_name%.composer.patch` para o diretório `m2-hotfixes`.
1. Adicionar, confirmar e enviar por push suas alterações de código:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.composer.patch patch"
   ```

   ```git
   git push origin
   ```

Para obter informações adicionais sobre como aplicar patches a projetos na nuvem, consulte [Aplicar patches](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches) na documentação do desenvolvedor.

## Como aplicar um patch do compositor para Adobe Commerce no local e Magento Open Source {#commerce}

1. Faça upload do patch para o seu diretório raiz do Adobe Commerce no local ou Magento Open Source.
1. Execute o seguinte comando SSH:

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   (Se o comando acima não funcionar, tente usar `-p2` em vez de `-p1` )

1. Para que as alterações sejam refletidas, atualize o cache no Administrador em **[!UICONTROL Sistema]** > **[!UICONTROL Gerenciamento de Cache]**.