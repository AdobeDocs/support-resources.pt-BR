---
title: Gerenciar perfis de produto no Global Admin Console
description: Saiba como administradores globais podem adicionar, editar e excluir Perfis de produto no Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: 580
ht-degree: 1%

---

# Gerenciar perfis de produto no Global Admin Console

**Aplica-se a:** Empresa


## Visão geral

Os administradores globais podem adicionar, editar e excluir Perfis de produto no [Global Admin Console](https://global-admin-console.adobe.com/).

>[!NOTE]
>
>Na [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access), selecione uma organização e navegue até **[!UICONTROL Produtos]**. É possível ativar todos os serviços ou os serviços selecionados de um produto usando Perfis de produto.

Como no Admin Console padrão, os Perfis de produto permitem ajustar o uso dos produtos em uma organização. Você também pode atribuir administradores, chamados de **[!UICONTROL Administradores de perfil de produto]**, aos Perfis de produto. Esses administradores podem adicionar usuários finais aos Perfis de produto que eles gerenciam.

Para gerenciar Perfis de produto, selecione um produto. Os controles para adicionar, editar e excluir Perfis de produto serão exibidos.

>[!NOTE]
>
>Para alguns produtos, não é possível criar ou editar Perfis de produto no Global Admin Console. Nesses casos, use a [Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html).

## Adicionar um perfil de produto

1. Na [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização para editar e navegue até a guia **[!UICONTROL Produtos]**.
1. Selecione um produto ao qual adicionar um Perfil de produto.
1. Selecione **[!UICONTROL Adicionar Perfil]**.
1. Na caixa de diálogo **[!UICONTROL Adicionar Perfil]**, insira os seguintes detalhes:

   | Campo | Descrição |
   |---|---|
   | **[!UICONTROL Nome]** | Um nome exclusivo para o Perfil de produto na organização, diferente de outros Perfis de produto e grupos de usuários. |
   | **[!UICONTROL Cota]** | O número de destino de licenças alocadas para este perfil. |
   | **[!UICONTROL Grupos de usuários]** | Selecione na lista suspensa ou digite um nome de grupo de usuários. Se o grupo de usuários ainda não existir, crie-o primeiro por meio da guia [**[!UICONTROL Grupos de Usuários ]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html). |
   | **[!UICONTROL Administradores]** | Selecione na lista suspensa ou insira um endereço de email de administrador. Se o administrador ainda não existir, crie-o primeiro por meio da guia [**[!UICONTROL Administradores ]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html). |

   Os [!UICONTROL Grupos de Usuários] especificados são atribuídos ao Perfil do Produto. Os administradores especificados se tornam os **[!UICONTROL Administradores do Perfil de Produto]**, que podem gerenciar o perfil por meio da Adobe Admin Console para a organização relevante.

   ![Adicionar perfil](./assets/manage-product-profiles_add-profile.png)

1. Use a opção **[!UICONTROL Notificações]** para habilitar ou desabilitar notificações por email. Quando ativados, os usuários são notificados por email quando são adicionados ou removidos do perfil.
1. Use os botões **[!UICONTROL Serviços]** individuais para habilitar ou desabilitar serviços específicos para o Perfil do Produto. Para obter mais informações, consulte [Habilitar/Desabilitar Serviços para um Perfil de Produto](https://helpx.adobe.com/enterprise/using/enable-disable-services.html).
1. Selecione **[!UICONTROL Salvar]**.
1. Selecione **[!UICONTROL Revisar alterações pendentes]** após concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Editar um perfil de produto

1. Selecione uma organização para editar, navegue até a guia **[!UICONTROL Produtos]** e selecione um produto.
1. Selecione o ícone **[!UICONTROL Mais Opções]** ![Mais Opções](./assets/manage-product-profiles_more-options.png) para o Perfil de Produto relevante e selecione **[!UICONTROL Editar Perfil]**.
1. Atualize os detalhes do Perfil do Produto conforme necessário e selecione **[!UICONTROL Salvar]**.
1. Selecione **[!UICONTROL Revisar alterações pendentes]** após concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Excluir um perfil de produto

>[!WARNING]
>
> A exclusão de um Perfil de produto remove o acesso ao produto para todos os usuários que eram membros desse perfil ou que pertenciam a grupos de usuários anexados a esse perfil.

1. Selecione uma organização para editar, navegue até a guia **[!UICONTROL Produtos]** e selecione um produto.
1. Selecione o ícone **[!UICONTROL Mais Opções]** ![Mais Opções](./assets/manage-product-profiles_more-options.png) para o Perfil de Produto relevante e selecione **[!UICONTROL Excluir Perfil]**.
1. Selecione **[!UICONTROL OK]** na caixa de diálogo de confirmação.
1. Selecione **[!UICONTROL Revisar alterações pendentes]** após concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).


## Leitura relacionada

- [Adotar Administração Global](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)
- [Gerenciar Administradores](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)
- [Gerenciar grupos de usuários](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html)
- [Alocar Produtos a Organizações Secundárias](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)
- [Executar Trabalhos Pendentes](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [Habilitar/Desabilitar Serviços](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Visão geral do Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html)
