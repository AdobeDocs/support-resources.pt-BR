---
title: Não foi possível adicionar o usuário ao projeto na nuvem do Adobe Commerce
description: Este artigo fornece uma solução para quando não é possível adicionar um usuário a um projeto na nuvem do Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Não foi possível adicionar o usuário ao projeto na nuvem do Adobe Commerce

Este artigo fornece uma solução para quando você está tentando adicionar um usuário a um projeto na nuvem, mas falha com um erro: *O usuário XXX não existe*.

## Produtos e versões afetados

* Adobe Commerce na infraestrutura em nuvem, [todas as versões com suporte](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problema

Este artigo fornece uma solução para quando não é possível adicionar um usuário a um projeto na nuvem do Adobe Commerce.

## Causa

A conta do usuário deve ser criada em [https://accounts.magento.cloud](https://accounts.magento.cloud) e vinculada ao SSO do Adobe antes de ser adicionada como usuário ao projeto. Se o usuário tiver uma conta do Adobe, mas não uma conta do Commerce (magento.com), primeiro deve criar uma.

## Solução

1. Peça ao usuário para entrar em [https://accounts.magento.cloud](https://accounts.magento.cloud). O usuário já deve estar registrado no Adobe usando o mesmo endereço de email.
   >[!NOTE]
   >Criar ou ter uma conta em [https://account.adobe.com](https://account.adobe.com) não significa automaticamente que o usuário tem uma conta em [https://accounts.magento.cloud](https://accounts.magento.cloud). O usuário deve primeiro [criar sua conta do Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Se o usuário já tiver uma conta da Adobe, mas não conseguir entrar, peça para ele enviar uma [solicitação de suporte](https://experienceleague.adobe.com/home?lang=pt-BR#support) com [!UICONTROL Motivo do Problema] definido como *Gerenciamento de Usuários*.

1. Depois que o usuário entrar com êxito no [https://accounts.magento.cloud](https://accounts.magento.cloud), você poderá adicionar o usuário ao projeto. Para obter etapas detalhadas, consulte [Adicionar usuários e gerenciar o acesso](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) no Guia de Infraestrutura do Commerce na Nuvem.

## Leitura relacionada:

* [Gerenciar o acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=pt-BR) em nosso Guia do Commerce na Infraestrutura em Nuvem.
* [Não é possível fazer logon no suporte da Adobe Commerce ou na conta de nuvem](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=pt-BR)
