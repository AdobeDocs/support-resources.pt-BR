---
title: Alocar produtos a organizações secundárias usando o Global Admin Console
description: Saiba como os administradores globais podem distribuir recursos para organizações secundárias, permitindo um gerenciamento eficiente de recursos e a atribuição de usuários em cada organização.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: f14254a77ce3620208389b36222f89be8f9d15b6
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Alocar produtos a organizações secundárias usando o Global Admin Console

Aplicável à empresa.

Saiba como os administradores globais podem distribuir recursos para organizações secundárias, permitindo um gerenciamento eficiente de recursos e a atribuição de usuários em cada organização.

No [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration), vá para a guia **[!UICONTROL Alocação de Produto]** e selecione um produto para alocar às organizações secundárias.

Entrar na [Global Admin Console](https://global-admin-console.adobe.com).

>[!NOTE]
>
>A **[!UICONTROL Alocação de Produto]** está disponível somente para contratos Enterprise Term License Agreement (ETLA).

Parte da distribuição e administração dos produtos da Adobe nas organizações é o particionamento de recursos adquiridos em alocações de recursos nas organizações a serem gerenciadas. É possível distribuir a administração dos recursos do produto para outras organizações fornecendo todo o recurso ou parte dele. Nem todos os recursos de todos os produtos podem ser alocados; alguns produtos não são distribuíveis para outras organizações. Esses produtos aparecem na guia **[!UICONTROL Alocação de Produto]**, mas não têm controles para adicioná-los a outras organizações.

>[!WARNING]
>
>Não é possível alocar produtos a uma organização secundária a partir de um contrato que expirou **1&rbrace; ou se a organização está em um estado** inativo **.** Saiba mais sobre a [expiração do contrato](https://helpx.adobe.com/enterprise/using/contract-expiry.html) ou entre em contato com o administrador da empresa para obter assistência para evitar que os usuários na organização secundária percam o acesso aos aplicativos e serviços da Adobe.

## Armazenamento em pool

Isso se aplica aos clientes que têm uma guia Armazenamento em sua Admin Console. Se você não vir uma guia Storage (Armazenamento), sua Admin Console ainda não foi atualizada para o Enterprise Storage Model (Modelo de armazenamento corporativo). Depois que sua organização for migrada, você verá as seguintes alterações:

- Os administradores globais obtêm acesso à cota e ao uso de armazenamento na hierarquia e podem alocar armazenamento para organizações usando a guia **[!UICONTROL Alocação de Produto]** na [Global Admin Console](https://adminconsole.adobe.com/).
- Os administradores de sistemas e de armazenamento têm controle total e visibilidade do armazenamento em toda a empresa. Eles podem rastrear e gerenciar o armazenamento usando a guia **[!UICONTROL Armazenamento]** no [Adobe Admin Console](https://adminconsole.adobe.com/).

Com as atualizações do armazenamento Adobe Creative Cloud, as cotas de armazenamento são flexíveis para usuários finais, até o volume de armazenamento adquirido pela organização. [Saiba mais](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html).

## Alocar produtos

A guia **[!UICONTROL Alocação de Produto]** no Global Admin Console mostra unidades de alocação para produtos comprados na hierarquia da organização. Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), você pode alocar esses recursos de produto para outra organização na árvore da organização e especificar a quantidade de alocação. Como um [visualizador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), você pode exibir e exportar os dados, mas não pode fazer nenhuma atualização.

Para alocar produtos a uma organização, siga estas etapas:

1. Entre no [Global Admin Console](https://global-admin-console.adobe.com) e vá para **[!UICONTROL Alocação de Produto]**.
1. Selecione um produto na lista suspensa para ver como ele é alocado para diferentes organizações.\
   Se uma organização não tiver o produto no momento, o ícone **[!UICONTROL Adicionar +]** será exibido.

   >[ !NNota]
   >
   >Se a organização secundária já tiver um contrato de compra, a alocação de produtos do pai para essa organização secundária poderá ser limitada. [Saiba mais](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. Para alocar o produto, selecione o ícone **[!UICONTROL Adicionar +]** para a organização relevante.\
   Alguns produtos incluem mais de um recurso alocável; nesse caso, vários recursos são listados na caixa de diálogo e você deve fornecer valores para cada um. Por exemplo, o Adobe Stock pode incluir créditos de imagem do Adobe Stock e créditos premium.
   ![Imagens do Adobe Stock](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. Na caixa de diálogo exibida, especifique a quantidade do produto.
1. Selecione **[!UICONTROL Salvar]**.
1. Para permitir ou não a superalocação de um recurso, selecione a opção relevante.
   ![Superalocação](/help/adobe-support-tools-guide/assets/overallocation.png)
1. Selecione **[!UICONTROL Revisar alterações pendentes]** depois de concluir a alocação de recursos. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Alocar e distribuir licenças ou transações de usuário do Adobe Acrobat Sign

O Global Admin Console permite alocar e distribuir licenças ou transações de usuário do Acrobat Sign na hierarquia organizacional. Cada organização na hierarquia que tem licenças ou transações do Acrobat Sign alocadas para ela cria sua própria conta separada do Acrobat Sign.

- Cada conta do Acrobat Sign criada é independente e em silos, em termos de administração e conteúdo.
- Cada conta da Acrobat Sign não tem conhecimento de outras contas da Acrobat Sign (por exemplo, em organizações principais ou irmãs).

Saiba mais sobre o [gerenciamento de Adobe Acrobat Sign na Admin Console](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html).

Para gerenciar complementos de autenticação, como KBA (Knowledge-Based Authentication, autenticação com base em conhecimento) e PA (Phone Authentication, autenticação por telefone), entre em contato com o representante da Adobe ou com o Gerente de sucesso do cliente.


## Limitações na alocação de produtos

A alocação de uma organização principal para uma organização secundária é limitada nestes casos:

- Se ambas as organizações tiverem contratos diferentes e o produto que você está tentando alocar existir em ambas, não será permitido misturar a mesma oferta entre contratos.
- Se ambas as organizações tiverem o mesmo contrato, você poderá solicitar permissão para alocar o produto entrando em contato com o representante da Adobe ou [enviando um caso de suporte](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html) especificando que a **[!UICONTROL Alocação de Produto]** no Global Admin Console está bloqueada.

## Superalocação

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), você pode permitir a superalocação de recursos.

Uma [política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies) de alocação associada ao produto e à organização indica se a superalocação é permitida.

A superalocação permite conceder a uma organização secundária mais recursos de produto do que os disponíveis na organização principal. É útil quando as alocações são aproximadas e o administrador não deseja ser sobrecarregado com a manutenção das alocações de recursos adicionando.
Se a superalocação for desativada para um recurso de produto em uma organização, a soma das concessões secundárias não poderá exceder a concessão principal. As solicitações para superalocar um recurso marcado com superalocação desabilitada não são executadas.
Quando a alternância de superalocação é alterada de ativado para desativado, os valores de concessão devem ser ajustados para eliminar a superalocação antes que as atualizações de concessão possam ser executadas, se uma situação de superalocação estiver presente nas quantidades de concessão de um recurso.

![Superalocação](/help/adobe-support-tools-guide/assets/overallocation.png)

## Contratos expirados na hierarquia

Não é possível alocar produtos a uma organização secundária a partir de um contrato do ETLA que expirou. Banners e notificações no aplicativo, como os mostrados a seguir, nas páginas **[!UICONTROL Visão geral]** e **[!UICONTROL Alocação de produtos]** indicam claramente quando o contrato em uma ou mais organizações derivadas irá expirar, expirou ou está inativo.

![Alocação de produto](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !IImportante]
>
>Quando um contrato do ETLA que faz parte da hierarquia estiver inativo, os produtos serão removidos das páginas **[!UICONTROL Visão geral]** e **[!UICONTROL Alocação de produto]**.

[Saiba mais sobre a expiração do contrato](https://helpx.adobe.com/enterprise/using/contract-expiry.html) ou entre em contato com o administrador da empresa para obter assistência para evitar que os usuários na organização secundária percam o acesso aos aplicativos e serviços da Adobe.
