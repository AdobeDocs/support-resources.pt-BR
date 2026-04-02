---
title: Selecione uma organização na Global Admin Console
description: Saiba como escolher uma organização para edição na Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 1%

---

# Selecione uma organização na Global Admin Console

Saiba como escolher uma organização para edição na Global Admin Console.

>[!NOTE]
>
>Depois de ter acesso ao [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), você pode começar selecionando uma organização para exibir e gerenciar o nome da organização, grupos de usuários, perfis de produtos, administradores e políticas da organização. Para entrar na Global Admin Console, [clique aqui](https://global-admin-console.adobe.com/).

A Global Admin Console atua como um hub de gerenciamento central de uma organização para os recursos da Adobe. Os administradores globais podem:

- Criar organizações filhas em sua organização
- Atribuir administradores de sistema para gerenciá-los
- Distribuir recursos a organizações-filho para gerenciamento e atribuição a usuários nessas organizações

>[!NOTE]
>
> Os usuários e administradores em uma organização não têm visibilidade sobre usuários, armazenamento ou outros recursos fora da organização.

## Selecione sua organização

As organizações listadas na lista suspensa **[!UICONTROL seletor de organização]** são aquelas das quais você é explicitamente um administrador global, ou seja, você foi adicionado à lista de administradores dessa organização com uma função de administrador global ou visualizador global. Você é implicitamente um administrador global (ou visualizador global) de todas as organizações abaixo desse ponto na hierarquia, mas essas organizações não estão listadas no [!UICONTROL seletor de organizações].

![Seletor de organização](/help/adobe-support-tools-guide/assets/org-picker.png)

Se quiser que eles sejam listados, adicione a si mesmo como administrador global às organizações que deseja listar. Ao selecionar uma organização no [!UICONTROL seletor de organização], suas permissões administrativas baseiam-se em ser um administrador global da organização selecionada. Você também pode estar listado como administrador global de uma organização principal no topo da árvore, o que pode lhe dar mais permissões. Você deve selecionar essa organização de nível superior para obter as permissões adicionais.

Na Global Admin Console, depois de selecionar uma organização na [!UICONTROL árvore hierárquica], você pode começar a editar informações de uma organização específica.

**As edições podem afetar:**

- Nome da organização
- Grupos de usuários
- Perfis de produto
- Administradores
- Políticas da organização

**As edições não podem afetar:**

- Usuários (exceto para exclusão de grupos ou perfis de produtos)
- Adicionar usuários (exceto para administradores)

Quando uma organização é selecionada na árvore hierárquica, as seguintes informações são exibidas:

- Nome da organização
- Região
- Número de usuários
- Lista de produtos
- Perfis de produto
- Grupos de usuários
- Administradores
- Domínios reivindicados
- Valores de política da organização

Para exibir ou editar produtos, grupos de usuários, administradores, domínios, políticas ou modelos de políticas, selecione a guia apropriada. Você pode usar o campo [!UICONTROL pesquisa] na maioria dos casos para localizar um item específico dentro da guia.

![Editar uma organização](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

Todos os administradores adicionados ou removidos de uma organização receberão uma notificação por email. Certas alterações de política em uma organização resultam em uma notificação na [!DNL Admin Console] dessa organização.

## Saiba mais sobre as restrições e condições necessárias

- A profundidade máxima para organizações de aninhamento é cinco. Portanto, a/b/c/d/e é permitido, mas a/b/c/d/e/f é um erro. Por exemplo, Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London é permitido, mas Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair é um erro.

- O comprimento máximo do nome de caminho (incluindo todas as organizações) é de 255 caracteres (incluindo &quot;/&quot;). O tamanho máximo de um único nome de organização é entre 4 e 100 caracteres.

- O nome do caminho da organização é exclusivo, mas o nome simples é exclusivo apenas entre seus irmãos. Pode haver organizações com o mesmo nome simples em outro lugar na hierarquia da organização.

- Você só pode exibir a lista de domínios vinculados à organização selecionada usando o Global Admin Console. Se você for um administrador do sistema da organização selecionada, selecione a **[!UICONTROL Abrir no Admin Console]** para [gerenciar domínios](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html). Para entender as informações exibidas na guia Domínios, consulte [exportar e importar esquemas](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas).

- O IE 11 não é compatível com o acesso de administração global. Use um navegador diferente ou uma versão mais recente do navegador IE.
