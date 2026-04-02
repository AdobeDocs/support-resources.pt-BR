---
title: Gerenciar hierarquia da organização
description: Saiba como os administradores globais podem gerenciar a hierarquia da organização na Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# Gerenciar hierarquia da organização

Aplicável à empresa.

Saiba como os administradores globais podem gerenciar a hierarquia da organização na Global Admin Console.

Depois de obter [acesso a [!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), você poderá criar novas organizações, adicionar organizações existentes à hierarquia, excluir organizações e alterar uma organização principal. Acesse aqui para [entrar na Global Admin Console](https://global-admin-console.adobe.com/)

Uma organização é uma estrutura usada para gerenciar produtos e usuários da Adobe. O [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) permite que os administradores gerenciem a implantação e a configuração de produtos e usuários em sua organização. O [[!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration) permite que administradores globais criem, gerenciem e excluam várias organizações.

## Criar uma organização secundária

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), você pode criar organizações secundárias de qualquer organização na hierarquia e definir o nome, país, grupos de usuários, produtos, perfis de produtos, administradores e políticas.

Quando uma nova organização secundária é criada, os itens a seguir são herdados automaticamente do pai imediato:

- Configurações de [política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) da organização (incluindo bloqueios, se presentes).
- A lista de administradores do sistema (controlada por **[!UICONTROL Herdar Administradores do Sistema na criação]** [política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).
Os itens a seguir podem impedir que administradores do sistema sejam herdados:
   - Falta de [confiança de domínio](https://helpx.adobe.com/enterprise/using/directory-trust.html).
   - Restrições de tipo de usuário (adicionar políticas de usuários do Adobe ID / Enterprise ID / Federated ID). Saiba mais sobre os [detalhes da política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Acesso a [[!DNL Federated ID]] ou [[!DNL Enterprise ID]] usuários a partir de domínios aos quais a organização principal tem acesso. Isso disponibiliza os usuários do domínio no pai na organização secundária. A herança de acesso do usuário é controlada por **Herdar usuários de diretórios gerenciados pela organização principal** [política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Política de compartilhamento, política de senha e contatos de segurança (controlado por **Herdar configurações de compartilhamento de ativos quando uma organização secundária é criada** [política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. Entrar na [Global Admin Console](https://global-admin-console.adobe.com/). Na guia **[!UICONTROL Organizações]**, selecione a organização à qual deseja adicionar uma organização secundária.
2. Selecione o ícone **[!UICONTROL Adicionar+]**.
   ![Adicionar Organização](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Especifique um **nome** e o **país** da organização.\
   O nome simples da organização deve ter entre 4 e 100 caracteres; o comprimento máximo do nome do caminho é de 255 caracteres.
   ![Adicionar Organização filha](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. Selecione **[!UICONTROL Salvar]**.
5. Selecione **[!UICONTROL Revisar alterações pendentes]** depois de concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Excluir uma organização secundária

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), você pode excluir organizações secundárias. A operação de exclusão não pode ser desfeita e a organização raiz não pode ser excluída. Os recursos alocados para a organização excluída são retornados à organização principal. Antes de uma organização ser excluída, seu pai se torna automaticamente o pai de qualquer uma de suas organizações-filho.

Uma organização só poderá ser excluída se os seguintes critérios forem atendidos:

- Não há contas do Sign, compras da Adobe Stock ou repositórios de armazenamento na organização.
- Não há domínios reivindicados na organização.
- Não há produtos instanciados na organização.
- Não há produtos da Experience Cloud que possam incluir instanciações na organização.

>[!WARNING]
>
>A exclusão de uma organização afeta seus usuários. Verifique se não há acesso ou informações que serão perdidas quando uma organização for excluída.

1. Entre no [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/). Vá para a guia **[!UICONTROL Organizações]** e selecione a organização que deseja excluir.
1. Selecione o ícone **[!UICONTROL Excluir]**.
   ![Excluir organização](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. Na caixa de diálogo **[!UICONTROL Excluir Organização]**, selecione **[!UICONTROL OK]**.
1. Selecione **[!UICONTROL Revisar alterações pendentes]** depois de concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Renomear uma organização

O nome da organização é o nome oficial da sua empresa ou instituição, definido durante a compra. Os usuários veem esse nome ao selecionar um perfil durante o logon, especialmente se tiverem acesso a produtos da Adobe de várias organizações ou precisarem escolher entre um perfil comercial e pessoal.

Como [administrador global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), você pode editar o nome de qualquer organização pai ou filho para ajudar os usuários a identificarem o perfil correto ao entrarem nos [[!DNL Creative Cloud]] produtos e serviços.

1. Entrar na [Global Admin Console](https://global-admin-console.adobe.com/). Na guia **[!UICONTROL Organizações]**, selecione a organização que deseja renomear.
1. Selecione o ícone **[!UICONTROL Editar]**.
   ![Renomear organização](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Atualize o nome da sua organização e selecione **[!UICONTROL Salvar]**.

>[!TIP]
>
>Use um nome de organização claro e reconhecível de até 255 caracteres para ajudar os usuários a selecionar o perfil correto. Evite usar caracteres especiais e considere incluir região, departamento ou direito. Além disso, evite acrônimos incomuns e nomes vagos ou semelhantes em toda a hierarquia da organização.

As alterações são registradas no log de auditoria, todos os usuários são notificados por email e o nome não pode ser atualizado novamente por 24 horas. [Saiba como exibir e baixar logs de auditoria](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports).

## Alterar o pai de uma organização

Como um [[!DNL Global Administrator]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), você pode atribuir um pai a uma organização na hierarquia da organização usando o botão **[!UICONTROL Alterar hierarquia]**.

Alterar o pai de uma organização tem o seguinte impacto:

- O reparo de uma organização move a subárvore inteira com raiz na organização com pai. Os nomes de caminho da organização com pai e seus filhos são atualizados para refletir sua nova localização.
- As [políticas](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) da organização de organizações movidas são atualizadas para que qualquer bloqueio nas políticas seja mantido por uma organização na nova hierarquia.
- Alterar a posição de uma organização na hierarquia pode alterar os administradores globais dessa organização. As funções de administração globais são herdadas na hierarquia para que qualquer administrador global da nova organização pai se torne automaticamente administrador global da organização movida. Da mesma forma, os administradores globais podem perder sua função na organização movida se tiverem essa função em virtude de serem administradores globais do pai antigo. As funções de administração global herdadas não estão listadas no painel Administradores da organização.
- O reparo também afeta os produtos disponíveis nas organizações movidas. Quando possível, [as alocações de produtos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) são atualizadas para que sejam fornecidas por meio da nova localização principal.
- Se as alocações de produtos não puderem ser atualizadas para vir do novo pai, os produtos serão removidos junto com os perfis de produto desses produtos. Os usuários podem perder acesso como resultado dessa operação. Para que o produto esteja disponível no novo local, o ancestral comum mais próximo dos locais antigo e novo deve ter o produto disponível.

>[!WARNING]
>
>Se os produtos forem removidos como resultado da criação de novos pais, os usuários perderão o acesso a esses produtos.

1. Entrar na [Global Admin Console](https://global-admin-console.adobe.com/). Na guia **[!UICONTROL Organizações]**, selecione **[!UICONTROL Alterar hierarquia]** para habilitar a criação de pai das organizações.
2. Selecione **[!UICONTROL OK]** na tela pop-up exibida.
3. Para criar um pai, arraste a organização filho para cima da organização desejada.
4. Selecione **[!UICONTROL Salvar]** quando terminar de criar os pais das suas organizações.
5. Selecione **[!UICONTROL Revisar alterações pendentes]** depois de concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Quando o trabalho for concluído, você poderá navegar até a Alocação de Produtos e [alterar os valores de concessão](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) para refletir a alteração na alocação de recursos de produtos.

## Adicionar organizações existentes usando o Mapeador de organizações

Como [Administrador Global](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), você pode adicionar organizações existentes que atualmente não fazem parte de sua hierarquia da Global Admin Console à hierarquia da organização.

Você também pode adicionar organizações da equipe à hierarquia da organização. As organizações da equipe não participam da alocação de produtos ou do acúmulo de uso de produtos, e o gerenciamento de organizações da equipe na Global Admin Console é limitado. Você pode adicioná-los à hierarquia da organização para rastreá-los e ter visibilidade dos produtos que compram. As organizações de equipe não podem ter organizações secundárias e não têm muitos dos recursos das organizações corporativas.

Saiba mais sobre as [limitações na alocação de produtos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Você só pode adicionar organizações secundárias às organizações raiz que são baseadas no mesmo modelo de armazenamento. Assim, as organizações secundárias baseadas no modelo de armazenamento de usuários só podem ser adicionadas às organizações básicas com base no modelo de armazenamento de usuários. E as organizações secundárias baseadas no modelo de armazenamento corporativo só podem ser adicionadas às organizações básicas baseadas no modelo de armazenamento corporativo.

A guia **[!UICONTROL Mapeador da Organização]** mostra o seguinte:

1. Uma lista suspensa com uma lista de possíveis organizações principais nas quais você pode adicionar uma organização secundária. Essas são organizações para as quais você é um administrador global.
1. Uma lista de organizações-filho que podem ser adicionadas sob a organização-pai selecionada na etapa 1. Essas são organizações para as quais você é um administrador do sistema e que ainda não são filhas de outra organização.

Quando uma organização é adicionada à administração global, os produtos nas organizações que são adicionadas usando o Mapeador da organização permanecem como compras; os números de [Alocação de produtos](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) interrompem o acúmulo nessas organizações.

1. Entre no [Global Admin Console](https://global-admin-console.adobe.com/) e navegue até o **[!UICONTROL Mapeador da Organização]**.
2. Selecione uma organização principal na lista suspensa.\
   Essas são as organizações para as quais você é adicionado diretamente como administrador global. Na lista suspensa, se você não vir uma organização que deseja usar como principal, selecione uma mais alta na hierarquia. Quando a operação do Mapeador da organização for concluída, você poderá usar [Alterar hierarquia](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization) para mover a nova organização para baixo na árvore para ter o pai que deseja usar.
3. Selecione as organizações a serem adicionadas como filhas da organização selecionada na etapa anterior.
4. Selecione **[!UICONTROL Revisar alterações pendentes]**. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).
5. Depois de executar as alterações, repita as etapas acima para adicionar outras organizações-filho à hierarquia da organização.

Depois que uma organização estiver na hierarquia, você poderá ajustar as políticas da organização, os administradores ou outras configurações navegando até a guia **[!UICONTROL Organizações]**.
