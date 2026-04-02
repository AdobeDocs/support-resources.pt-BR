---
title: Atualizar políticas da organização na Global Admin Console
description: Saiba como um administrador global pode definir e modificar políticas para uma organização e seus filhos na Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
source-git-commit: 90807a4e803de702c9e0975df551efefc254030a
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 0%

---

# Atualizar políticas da organização na Global Admin Console

**Aplica-se a:** Empresa

Saiba como um administrador global pode definir e modificar políticas para uma organização e seus filhos na Global Admin Console.

>[!NOTE]
>
>Na [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html), selecione uma organização na hierarquia e navegue até a guia **Políticas** para permitir, proibir ou bloquear as políticas.
>
> [Entrar na Global Admin Console](https://global-admin-console.adobe.com/)

As políticas são associadas a uma organização e restringem as operações que podem ser executadas nessa organização. Quando um valor de política é definido, ele restringe ou habilita ações a partir desse ponto.
Por exemplo, se a política **Domínios de Declaração** estiver definida como *não permitido*, nenhum domínio adicional poderá ser reivindicado, mas os domínios reivindicados antes da definição do valor da política não serão afetados.

## Configurar Políticas

Para modificar as políticas de uma organização, faça o seguinte:

1. Na Global Admin Console, [selecione uma organização](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) para editar e navegue até a guia **[!UICONTROL Políticas]**.
1. Selecione o botão de alternância da política relevante para permitir ou impedir sua permissão. Você também pode bloquear uma política para que ninguém, exceto um administrador global da [organização selecionada](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) ou sua organização principal, possa alterá-la ou desbloqueá-la.
1. Para bloquear uma política, selecione o ícone **[!UICONTROL Bloquear]** ![Bloquear](./assets/lock.png). Passar o mouse sobre o bloqueio exibe o nome da organização selecionada. Saiba mais sobre [bloqueios de política](#policy-locks).
1. Selecione **[!UICONTROL Revisar alterações pendentes]** depois de concluir a edição das organizações. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Bloqueios de Política {#policy-locks}

Quando uma política é bloqueada, seu valor não pode ser alterado até que a política seja desbloqueada. A Global Admin Console lembra a [organização selecionada](https://helpx.adobe.com/enterprise/global-admin-console/overview.html) no seletor de organização como sendo a organização da qual a política foi bloqueada. Qualquer administrador global dessa organização selecionada ou de qualquer organização localizada na parte superior da árvore tem permissão para desbloquear a política. Os administradores globais cujo escopo é inferior a essa organização não têm permissão para desbloquear e alterar valores de política.

Para criar um ambiente bloqueado, defina os valores de política desejados em suas organizações secundárias e bloqueie-os. Os administradores globais dessas organizações secundárias não poderão editar os valores da política.

### Exemplo: ambiente bloqueado

Se Elissa, administrador global da *Acme Division*, criar organizações secundárias para *Marketing* e *Engenharia*, então adicionará Robert como administrador global da *Marketing* e Sarah como administrador global da *Engenharia*. Em seguida, ela define várias políticas como *Não permitido* e *bloqueia*. Posteriormente, Elissa pode desbloquear e alterar os valores de políticas ao escolher *Acme Division* como a organização selecionada, mas Robert e Sarah não podem desbloquear as políticas nas organizações das quais são administradores globais, pois as políticas estão bloqueadas pela organização *Acme Division*.

## Detalhes da política

### Gerenciamento de Organização

| Nome da política | Descrição |
| --- | --- |
| **Criar organizações secundárias** | Permite que administradores globais criem organizações secundárias. Se *desativado*, nenhuma organização secundária poderá ser criada. |
| **Renomear Organização** | Se permitido, um administrador global ou do sistema pode renomear a organização. Também controla a alteração do país/região da organização. O nome do caminho de uma organização também pode ser alterado independentemente dessa configuração de política se uma organização principal for renomeada, ou se a organização ou um ancestral da organização for um pai ou mãe. |
| **Excluir organizações** | Permite que administradores globais excluam organizações secundárias. Isso se torna mais importante quando as organizações com armazenamento corporativo são habilitadas devido ao risco de excluir ativos do usuário. |

### Gerenciamento de administradores

| Nome da política | Descrição |
| --- | --- |
| **Adicionar ou Excluir Administradores** | Permite que administradores globais adicionem novos administradores a uma organização. Se *off*, não é possível adicionar novos administradores. |
| **Herdar Administradores do Sistema do Pai quando a Organização Filho for Criada** | Quando administradores globais criam novas organizações secundárias, os administradores de sistema da organização principal se tornam administradores de sistema da nova organização automaticamente. Esta política é *off* por padrão. |
| **Gerenciar administradores** | Permite que administradores globais alterem ou removam/editem permissões de administrador. |

### User Management

| Nome da política | Descrição |
| --- | --- |
| **Herdar Usuários dos Diretórios Gerenciados pela Organização Pai** | Esta política deve ser alternada *em* e ativa antes da criação da nova organização secundária. Quando uma organização secundária é criada, os usuários na organização principal são disponibilizados como usuários na organização secundária. Em outras palavras, essa política define automaticamente uma relação de confiança entre o pai e o filho quando o novo filho é criado dentro do GAC. Para organizações existentes, quaisquer relações de confiança antes de serem adicionadas ao GAC permanecerão assim que forem trazidas ao GAC. Se não houver relações de confiança em vigor, o processo normal de solicitação de confiança deverá ser seguido. Para que essa política seja bem-sucedida, o administrador global que cria a nova organização também deve ser um administrador do sistema da organização principal com o domínio reivindicado. Caso contrário, a relação de confiança do domínio não será herdada para a organização recém-criada. |
| **Adicionar usuários do Adobe ID** | Se definida, a organização não poderá adicionar usuários do tipo Adobe ID por meio da Admin Console, da API de gerenciamento de usuários (UMAPI) nem do mecanismo de sincronização. |
| **Gerenciar grupos de usuários** | Se permitido, os administradores Globais, de Sistema e de grupo de usuários poderão criar, editar e excluir Grupos de Usuários. |

### Imposição de Diretório e Domínio

| Nome da política | Descrição |
| --- | --- |
| **Domínios de Declaração** | Se definido, os administradores do sistema poderão reivindicar domínios na Admin Console. |
| **Alterar configuração de identidade** | Se definido, os administradores do sistema podem alterar a configuração da identidade do usuário no Admin Console. |

### Alocação de produto

| Nome da política | Descrição |
| --- | --- |
| **Gerenciar Produtos** | Permite que administradores globais adicionem ou removam produtos e alterem as concessões de recursos do produto. |

### Compartilhamento de ativos

| Nome da política | Descrição |
| --- | --- |
| **O administrador do sistema ou do armazenamento pode alterar as configurações de compartilhamento do ativo** | Se permitido, os administradores de armazenamento e de sistema podem alterar as configurações de compartilhamento de ativos, incluindo contatos de segurança, política de senhas e política de armazenamento. |
| **Herdar a política de compartilhamento de um pai quando uma organização é criada** | Se permitido, as configurações de compartilhamento do ativo são herdadas do pai quando uma organização secundária é criada. As configurações de compartilhamento de ativos incluem contatos de segurança, política de senha e política de armazenamento. Isso se aplica somente às organizações recém-criadas no momento da criação. Ela é definida em um pai e afeta a criação de organizações filho sob esse pai. |
