---
title: Configuração de direitos de suporte ao cliente da Adobe
description: Como os clientes do Adobe podem configurar e gerenciar direitos de suporte no Admin Console para que os usuários possam acessar recursos de suporte, enviar problemas e gerenciar atividades de caso.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 7f7a394874014fb5333ed9fb39f84b7137562726
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Configuração de direitos de suporte ao cliente da Adobe

Para configurar os direitos de suporte para sua organização, primeiro adicione ou convide o usuário por meio da Admin Console.

## Adicionar funções de direito de suporte a uma organização

A função de **[!UICONTROL Administrador de suporte]** é uma função não administrativa que tem acesso a informações relacionadas a suporte. Um **[!UICONTROL Administrador de suporte]** pode exibir, criar e gerenciar relatórios de problemas.

Para adicionar ou convidar um administrador:

1. Na Admin Console, escolha **[!UICONTROL Usuários]** > **[!UICONTROL Administradores]**.
1. Clique em **[!UICONTROL Adicionar administrador]**.
1. Insira um nome ou endereço de email.

   Você pode pesquisar usuários existentes ou adicionar um novo usuário especificando um endereço de email válido e preenchendo as informações na tela.

   ![Adicionar administrador](assets/admin-console-add-admin.png)

1. Clique em **[!UICONTROL Avançar]**. Uma lista de funções administrativas é exibida.

Para atribuir uma função de **[!UICONTROL Administrador de suporte]** a um usuário (habilitar um usuário para contatar o suporte):

1. Selecione a opção **[!UICONTROL Administrador de suporte]**.

   ![Editar direitos administrativos](assets/edit-admin-rights.png)

1. Escolha uma das duas opções a seguir:

   * Opção 1: **[!UICONTROL Administrador de suporte básico]**. Selecione essa opção se desejar conceder ao usuário suporte acesso a todas as soluções (exceto Marketo Engage).
   * Opção 2: **[!UICONTROL Administrador de suporte do produto]**: selecione esta opção para obter suporte do Marketo Engage. Selecione quais instâncias do Marketo Engage devem receber acesso de suporte do usuário.

   ![Editar Marketo de direitos administrativos](assets/edit-admin-rights-advanced.png)

1. Depois de fazer as seleções, clique em **[!UICONTROL Salvar]**.

O usuário recebe um convite por email sobre os novos privilégios administrativos de `message@adobe.com`.

Os usuários devem clicar em **[!UICONTROL Introdução]** no email para ingressar na organização. Se os novos administradores não usarem o link **[!UICONTROL Introdução]** no convite por email, eles não poderão entrar na Admin Console.

Como parte do processo de logon, os usuários podem ser solicitados a configurar um perfil do Adobe se ainda não tiverem um. Se os usuários tiverem vários perfis associados ao seu endereço de email, eles deverão escolher **[!UICONTROL Ingressar na Equipe]** (se solicitado) e selecionar o perfil associado à nova organização.

![Confirmação de direitos do administrador](assets/admin-rights-confirmation.png)

Para obter mais detalhes, consulte as instruções de [Editar função de administrador de empresa](admin-roles.md#edit-enterprise-admin-role) na documentação de funções administrativas. Observe que somente um administrador do sistema de sua organização pode atribuir essa função. Para obter mais informações sobre hierarquia administrativa, consulte a documentação de [Funções administrativas](admin-roles.md).
