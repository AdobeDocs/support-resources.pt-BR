---
title: Como incluir um membro da equipe nas notificações de suporte
description: Este artigo fornece uma explicação de como incluir um membro da equipe nas notificações de suporte.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

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
1. Verifique se o membro da equipe foi adicionado ao projeto e se é um [!DNL Project Admin].

Se não tiverem sido adicionados ao projeto, será necessário adicioná-los como um [!DNL Project Admin] e conceder [!DNL Shared Access]:

* [Gerenciar acesso do usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=pt-BR) em nosso guia do usuário.
* [Não é possível adicionar usuário ao projeto de nuvem do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=pt-BR) na Base de Dados de Conhecimento Commerce.
* [Guia do Usuário da Central de Ajuda do Adobe Commerce: Acesso Compartilhado](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=pt-BR#shared-access) na Base de Dados de Conhecimento Commerce.

Se eles foram adicionados ao [!DNL cloud project], mas não têm o [!DNL Project Admin role], atualize seus [!DNL role] apropriadamente em [Gerenciar acesso de usuário](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=pt-BR).

Se você quiser permitir que um membro da equipe seja um inspetor em todas as ocorrências abertas na sua organização, envie um [Tíquete de suporte](https://experienceleague.adobe.com/home?lang=pt-BR&support-tab=home#support).

## Leitura relacionada

[Ex-membros da equipe recebem emails de notificação na nuvem do Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html?lang=pt-BR)
