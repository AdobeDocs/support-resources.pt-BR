---
title: Gerenciar grupos de usuários na Global Admin Console
description: Saiba como criar, compartilhar, editar e excluir grupos de usuários na Global Admin Console para simplificar o gerenciamento de usuários em todas as organizações.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: f81a20fd6d9d64443f4708b3fc17de7240d1bc61
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---


# Gerenciar grupos de usuários na Global Admin Console

Crie, gerencie e compartilhe grupos de usuários no Global Admin Console para simplificar o gerenciamento de usuários, agrupando usuários com as mesmas permissões, economizando tempo e garantindo consistência.

No [Global Admin Console](https://helpx.adobe.com/br/enterprise/global-admin-console/adopt-global-administration.html), selecione uma organização e navegue até **[!UICONTROL Grupos de Usuários]**. Compartilhe grupos em várias organizações usando uma única fonte de gerenciamento de usuários para sincronizar usuários e grupos.

[Entrar na Global Admin Console](https://global-admin-console.adobe.com)



## Criar grupos de usuários

Você pode [criar grupos de usuários](https://helpx.adobe.com/br/enterprise/using/user-groups.html) individualmente, em massa ou [sincronizá-los diretamente de um Azure AD](https://helpx.adobe.com/br/enterprise/using/add-azure-sync.html) estabelecido para um diretório federado no Adobe Admin Console. No Global Admin Console, é possível definir grupos de usuários com perfis de produto relevantes atribuídos, aos quais os administradores de grupo de usuários podem adicionar usuários posteriormente usando o Admin Console.

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização para editar e navegue até a guia **[!UICONTROL Grupos de Usuários]**.

2. Selecione **[!UICONTROL Adicionar Grupo De Usuários]**.

   ![Guia Organizações na Global Admin Console com a guia Grupos do usuário selecionada.](assets/add-user-group.png "Adicionar grupo de usuários")

   _Adicione grupos de usuários a uma organização para simplificar o gerenciamento de usuários._

3. Digite o seguinte na caixa de diálogo **[!UICONTROL Adicionar Grupo de Usuários]** que é exibida:
   - **[!UICONTROL Nome]**: especifique um nome para o grupo de usuários.
   - **[!UICONTROL Perfis de Produtos]**: se você deseja conceder acesso ao produto para os membros atuais ou futuros do grupo de usuários, clique na seta suspensa para selecionar um Perfil de Produto na lista ou digite o nome do Perfil de Produto e selecione-o na lista suspensa exibida. Para adicionar um perfil de produto que ainda não foi criado, faça isso primeiro usando a guia [Perfis de produto](https://helpx.adobe.com/br/enterprise/using/global-admin-edit-organizations.html#profiles).
   - **[!UICONTROL Administradores]**: clique na seta suspensa para selecionar um administrador na lista ou digite o endereço de email do administrador e selecione-o na lista suspensa exibida. Se quiser adicionar um novo administrador que ainda não foi criado, você deve primeiro criar esse administrador usando a guia [Administradores](#share-user-groups).

   Os perfis de produto especificados são atribuídos ao Grupo de usuários, e os administradores especificados se tornam os administradores do grupo de usuários. Os administradores de grupo de usuários podem usar o Adobe Admin Console para que a organização relevante gerencie o grupo.

4. Selecione **[!UICONTROL Salvar]**.

5. Selecione **[!UICONTROL Revisar alterações pendentes]** para revisar as atualizações. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Administradores globais podem [atribuir perfis de produtos e administradores de grupos de usuários](#review-user-groups) aos grupos de usuários usando a Global Admin Console. Usando a Adobe Admin Console, administradores do sistema e administradores de grupos de usuários podem [adicionar usuários e atribuir administradores e perfis de produtos](https://helpx.adobe.com/br/enterprise/using/user-groups.html) ao grupo de usuários.



## Compartilhar grupos de usuários

A projeção de grupo permite sincronizar grupos de usuários e seus usuários associados de uma única fonte de gerenciamento para vários Admin Consoles. Os administradores globais podem compartilhar grupos de usuários com descendentes hierárquicos da organização de origem, trabalhando para baixo, não para cima ou de um lado para o outro.

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização e navegue até a guia **[!UICONTROL Grupos de Usuários]**.

2. Marque as caixas de seleção dos grupos de usuários que deseja compartilhar.

   Os grupos podem ser desativados para compartilhamento nos seguintes casos:
   - O grupo de usuários é compartilhado de outra organização. Para compartilhar ou editar o grupo, selecione na hierarquia da organização a organização à qual ele pertence.
   - A organização não está usando o [armazenamento Adobe para empresa](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html), que está sendo implantado globalmente em fases.
   - A política da organização está desabilitada. Acesse a guia **[!UICONTROL Políticas]** para ativar a política **[!UICONTROL Gerenciar grupos de usuários compartilhados]**.
   - A organização não tem nenhuma organização filha com a qual compartilhar grupos de usuários.

3. Selecione **[!UICONTROL Compartilhar grupo de usuários]**.

4. <a id="review-user-groups"></a>Revise os grupos de usuários para compartilhar com outras organizações. Se você também for um administrador do sistema na organização selecionada, selecione a **[!UICONTROL Abrir no Admin Console]** Ícone <img src="assets/icon-open-in-admin-console.png" alt="Ícone Abrir no Admin Console" width="14" height="14"> para revisar a lista de membros do grupo de usuários na Adobe Admin Console.

   >[!NOTE]
   >
   >Para evitar conflitos, verifique se as organizações com as quais você planeja compartilhar grupos de usuários ainda não têm grupos com o mesmo nome.

5. Selecione **[!UICONTROL Próximo]**.

6. Selecione as organizações com as quais compartilhar grupos de usuários e selecione **[!UICONTROL Avançar]**.

7. Se não houver conflitos, selecione **[!UICONTROL Compartilhar Grupos de Usuários]**.

   Se houver conflitos (em que existam grupos de usuários com o mesmo nome na organização de destino), escolha uma das seguintes opções e selecione **[!UICONTROL Compartilhar Grupos de Usuários]**:
   - **[!UICONTROL Ignorar (padrão)]**: ignorar os grupos nas organizações de destino com o mesmo nome.
   - **[!UICONTROL Adicionar somente]**: mescla os grupos de usuários adicionando novos usuários aos grupos de usuários existentes sem remover nenhum usuário.
   - **[!UICONTROL Grupo de espelhamento]**: ajuste os grupos da organização de destino para corresponder ao grupo compartilhado adicionando ou removendo usuários.

8. Selecione **[!UICONTROL Revisar alterações pendentes]** para revisar as atualizações. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   Os eventos de projeção de grupo são registrados para sua referência. Saiba como [exibir e baixar logs de auditoria](https://helpx.adobe.com/br/enterprise/global-admin-console/insights.html).


Quando você compartilha um grupo de usuários, o grupo e seus usuários são adicionados à organização de destino. No entanto, o *grupo de usuários de origem* controla os grupos de usuários compartilhados e seus usuários. As atribuições de perfil de administrador e de produto *não* estão sincronizadas entre as organizações.

As alterações no nome do grupo de usuários projetado ou nos usuários associados no grupo de usuários de origem são atualizadas automaticamente na organização de destino. Embora o grupo de usuários compartilhado não possa ser gerenciado diretamente, um administrador na organização de destino pode atribuir perfis de produto a um grupo compartilhado, dando acesso de licença aos usuários do grupo.



## Revogar acesso a grupos compartilhados

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização e navegue até a guia **[!UICONTROL Grupos de Usuários]**.

2. Selecione **[!UICONTROL Gerenciar acesso compartilhado]** para o grupo de usuários relevante.

3. Selecione as organizações das quais deseja revogar o acesso.

4. Selecione **[!UICONTROL Revogar acesso]**.

5. Ao revogar o acesso, você pode optar por deletar o grupo de usuários e os usuários ou deixar uma cópia nas organizações de destino:
   - Ao excluir, o grupo de usuários é removido das organizações de destino. Os usuários que não são membros de outros grupos compartilhados são removidos das organizações de destino e perdem o acesso a todos os produtos, serviços e ativos.
   - Ao sair de uma cópia, o grupo de usuários e os usuários permanecem nas organizações de destino, mantendo todas as atribuições intactas. No entanto, o grupo de usuários não será mais sincronizado e poderá ser gerenciado pelos administradores das organizações de destino.

6. Selecione **[!UICONTROL Revogar acesso]**.

7. Selecione **[!UICONTROL Revisar alterações pendentes]** para revisar as atualizações. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).



## Editar grupos de usuários

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização e navegue até a guia **[!UICONTROL Grupos de Usuários]**.

2. Selecione as **[!UICONTROL Mais Opções]** Ícone <img src="assets/icon-more-options.png" alt="Ícone Mais opções" width="14" height="14" style="vertical-align:middle"> para o grupo de usuários relevante e selecione **[!UICONTROL Editar Grupo de Usuários]**.

   >[!NOTE]
   >
   >Você não pode editar grupos de usuários que não sejam de propriedade da organização selecionada.

   ![Uma organização selecionada com a opção editar grupo de usuários realçada na guia grupos de usuários.](assets/edit-user-group.png "Editar grupo de usuários")

   _Edite os grupos de usuários para atualizar o nome do grupo de usuários, os perfis de produtos ou os administradores._

3. Atualize o nome do grupo de usuários, os perfis de produtos ou os administradores. Em seguida, selecione **[!UICONTROL Salvar]**.

   >[!NOTE]
   >
   >No assistente **[!UICONTROL Editar Grupo de Usuários]**, você pode atribuir funções de administrador apenas a usuários que já tenham uma função de administrador atribuída nesta organização. Saiba como [adicionar novos administradores](https://helpx.adobe.com/enterprise/global-admin-console/manage-admins.html).

4. Selecione **[!UICONTROL Revisar alterações pendentes]** para revisar as atualizações. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Se você alterar o nome de um grupo de usuários compartilhado, as alterações serão atualizadas automaticamente na organização de destino.



## Excluir grupos de usuários

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização e navegue até a guia **[!UICONTROL Grupos de Usuários]**.

2. Selecione as **[!UICONTROL Mais Opções]** Ícone <img src="assets/icon-more-options.png" alt="Ícone Mais opções" width="14" height="14" style="vertical-align:middle"> para o grupo de usuários relevante e selecione **[!UICONTROL Excluir Grupo de Usuários]**.

   >[!NOTE]
   >
   >Você não pode excluir grupos de usuários que não sejam de propriedade da organização selecionada.

3. Selecione **[!UICONTROL Ok]** na caixa de diálogo exibida.

   >[!CAUTION]
   >
   >A exclusão de um grupo de usuários pode afetar seus usuários. Verifique se não há acesso ou informações que serão perdidas quando o grupo de usuários for excluído.

4. Depois de editar as organizações, selecione **[!UICONTROL Revisar alterações pendentes]** para analisá-las. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).
