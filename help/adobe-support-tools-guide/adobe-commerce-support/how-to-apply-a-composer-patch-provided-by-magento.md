---
title: Como aplicar um patch de compositor fornecido pelo Adobe
description: Este artigo instrui como aplicar um patch de compositor para Adobe Commerce no local, Adobe Commerce na infraestrutura em nuvem e Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
exl-id: 66d8df60-4c4a-49ef-8107-986e10d6e289
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
    internal-label: Compliance
  - id: 125c1f49-aefd-5f34-a252-288937f95f6b
    internal-label: Marketing Tools
subfeature_v2:
  - id: c4af0798-d497-5e6b-8380-19812c26d00a
    internal-label: Console
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '225'
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
