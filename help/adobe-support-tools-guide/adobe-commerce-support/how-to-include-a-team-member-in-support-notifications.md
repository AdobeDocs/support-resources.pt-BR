---
title: Como incluir um membro da equipe nas notificações de suporte
description: Este artigo fornece uma explicação de como incluir um membro da equipe nas notificações de suporte.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
source-git-commit: 3d2865871a355ff70d146bb83780f7b92fd8f677
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 10%

---

# Como incluir um membro da equipe nas notificações de suporte

Este artigo fornece uma explicação sobre como incluir um membro da equipe para receber atualizações de suporte automaticamente por meio de notificações de email.

## Produtos e versões afetados

* Adobe Commerce na infraestrutura em nuvem, todas as [versões com suporte](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Causa

* O membro da equipe não foi adicionado ao [!DNL cloud project] com os privilégios necessários.
* O membro da equipe não tem uma conta de Suporte.

## Solução

1. Vá para **[!DNL Cloud Project URL]** (Exemplo: `https://us-3.magento.cloud/projects/xxxxxx/edit`).
1. Verifique se o membro da equipe foi adicionado ao projeto e se é um [!DNL Super User].

Se não tiverem sido adicionados ao projeto, será necessário adicioná-los como um [!DNL Super User] e conceder [!DNL Shared Access]:

* [Gerenciar acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) em nosso guia do usuário.
* [Não é possível adicionar usuário ao projeto de nuvem do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=pt-BR) na Base de Dados de Conhecimento Commerce.
* [Guia do Usuário da Central de Ajuda do Adobe Commerce: Acesso Compartilhado](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#shared-access) na Base de Dados de Conhecimento Commerce.

Se eles foram adicionados ao [!DNL cloud project], mas não têm o [!DNL Super User role], atualize seus [!DNL role] apropriadamente em [Gerenciar acesso de usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html).

Se você quiser permitir que um membro da equipe seja um inspetor em todas as ocorrências abertas na sua organização, envie um [Tíquete de suporte](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support).

## Leitura relacionada

[Ex-membros da equipe recebem emails de notificação do Adobe Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)