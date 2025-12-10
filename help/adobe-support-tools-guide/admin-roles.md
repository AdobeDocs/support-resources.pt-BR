---
title: Funções administrativas
description: Usando a Adobe Admin Console, as organizações podem definir uma hierarquia administrativa flexível que permita o gerenciamento refinado do acesso e uso dos produtos da Adobe.
exl-id: bfee66b5-d7bb-4ecb-8d22-efb68611ecc8
source-git-commit: 21f2b42e3131fe0339e5de15824f48166409c7c1
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Funções administrativas

Usando a Adobe Admin Console, as organizações podem definir uma hierarquia administrativa flexível que permita o gerenciamento refinado do acesso e uso dos produtos da Adobe. Um ou mais administradores de sistema, provisionados durante o processo de integração corporativa, estão no topo da hierarquia. Esses administradores do sistema podem delegar responsabilidades a outros administradores e, ao mesmo tempo, manter o controle geral.

As Funções Administrativas oferecem os seguintes benefícios-chave para as empresas:

* Descentralização controlada das responsabilidades administrativas
* Exibição rápida das atribuições de produtos — por usuário e por produto
* Funcionalidade para atribuir cotas a administradores de produtos

## Hierarquia administrativa

Aplicável a: clientes corporativos do Adobe.

A hierarquia administrativa pode ser usada para atender aos requisitos exclusivos de sua empresa. Por exemplo, uma empresa pode indicar diferentes administradores para gerenciar direitos a ofertas da Adobe Creative Cloud e da Adobe Marketing Cloud. Como alternativa, uma empresa pode ter diferentes administradores para gerenciar direitos de usuários pertencentes a diferentes unidades de negócios.

>[!NOTE]
>
>A hierarquia administrativa não se aplica aos clientes das equipes. Os clientes das equipes têm uma única função de **Administrador do sistema**. O proprietário do contrato (_anteriormente conhecido como **Administrador principal**_) é o administrador do sistema com acesso aos detalhes do contrato e ao histórico de cobrança. Se você for o proprietário do contrato atual, poderá indicar um administrador do sistema existente (_ anteriormente mencionado como **administrador secundário**_) como o proprietário do contrato.

![imagem do administrador](assets/storage_admin.png)

_Hierarquia de funções de administrador_

| Função | Descrição |
|--- |--- |
| **Administrador do sistema** | Superusuário da organização; autorizado a executar todas as tarefas administrativas na Admin Console.<br>Além disso, o tem permissões para delegar a seguinte funcionalidade administrativa a outros usuários: administrador de produto, administrador de Perfil de produto, administrador de Grupo de usuários, administrador de implantação e administrador de suporte. |
| **Administrador de produto** | Administra os produtos atribuídos a esse administrador e todas as funções administrativas associadas, que incluem:<ul><li>Criar perfis de produto</li><li>Adicionar usuários e grupos de usuários à organização, mas não remover esses</li><li>Adicionar ou remover usuários e grupos de usuários dos perfis de produtos</li><li>Adicionar ou remover administradores de Perfil de produto de perfis de produto</li><li>Adicionar ou remover outros administradores de produto do produto</li><li>Adicionar ou remover administradores de grupo de grupos</li></ul> |
| **Administrador do Perfil de Produto** | Administra as descrições do Perfil do produto atribuídas a esse administrador e todas as funções administrativas associadas, que incluem:<ul><li>Adicionar usuários e grupos de usuários à organização, mas não remover esses</li><li>Adicionar ou remover usuários e grupos de usuários dos perfis de produtos</li><li>Atribuir ou revogar permissões de produto a usuários e grupos de usuários a partir de perfis de produtos</li><li>Gerenciar funções de produto de usuários e grupos de usuários para perfis de produtos |
| **Administrador do Grupo de Usuários** | Administra as descrições do grupo de usuários atribuídas a esse administrador e todas as funções administrativas associadas, que incluem:<ul><li>Adicionar ou remover usuários de grupos</li><li>Adicionar ou remover administradores de grupo de usuários de grupos |
| **Administrador da implantação** | Cria, gerencia e implanta pacotes de software e atualizações para usuários finais. |
| **Administrador de Suporte** | Função não administrativa que tem acesso a informações relacionadas ao suporte, como relatórios de problemas relatados pelo cliente. |
| **Administrador de Armazenamento** | Gerencia a administração de armazenamento da organização. O administrador pode visualizar o consumo de armazenamento de usuários ativos e inativos e transferir conteúdo para outros recipients. |

Para obter uma lista detalhada de permissões e privilégios para cada função de administrador, consulte [Permissões](#enterprise-admins-permissions-matrix).

## Adicionar uma função de administrador corporativo {#add-enterprise-role}

Aplicável a: clientes corporativos do Adobe.

Como administrador, você pode atribuir uma função de administrador a outros usuários, dando a eles os mesmos privilégios que você tem, ou privilégios para uma função sob sua função de administrador na hierarquia, conforme descrito [acima](#administrative-hierarchy). Por exemplo, como administrador de produto, você pode conceder privilégios de administrador de produto ou privilégios de administrador de Perfil de produto a um usuário, mas não privilégios de administrador de implantação. Para obter as permissões no Admin Console, consulte a [Matriz de permissões](#enterprise-admins-permissions-matrix).

Para adicionar ou convidar um administrador:

1. No [Admin Console](https://adminconsole.adobe.com/), escolha **Usuários** > **Administradores**.

   Como alternativa, vá para o Produto, Perfil de Produto ou Grupo de Usuários relevante e navegue até a guia **Administradores**.

1. Clique em **Adicionar administrador**.
1. Insira um nome ou endereço de email. Você pode pesquisar usuários existentes ou adicionar um novo usuário especificando um endereço de email válido e preenchendo as informações na tela.
1. Clique em **Avançar**. Uma lista de funções administrativas é exibida.

>[!NOTE]
>
>* As opções nessa tela dependem da sua conta e da função do administrador. Você pode conceder os mesmos privilégios que possui ou privilégios para uma função sob a sua na hierarquia.
>* Como administrador do sistema de uma equipe, você pode atribuir apenas uma função de administrador: Administrador do sistema.

1. Selecione uma ou mais funções administrativas.
1. Em Tipos de administrador, como Administrador de produto, Administrador de perfil de produto e Administrador de grupo de usuários, selecione os produtos, perfis e grupos específicos, respectivamente.

>[!NOTE]
>
>Para um Administrador de perfil de produto, é possível incluir perfis para mais de um produto.

![adicionar administrador](assets/add-admin.png)

1. Revise as funções de administrador atribuídas ao usuário e clique em **Salvar**.

O usuário recebe um convite por email sobre os novos privilégios administrativos de `message@adobe.com`.

Os usuários devem clicar em **Introdução** no email para ingressar na organização. Se os novos administradores não usarem o link **Introdução** no convite por email, eles não poderão entrar na Admin Console.

Como parte do processo de logon, os usuários podem ser solicitados a configurar um perfil do Adobe se ainda não tiverem um. Se os usuários tiverem vários perfis associados ao seu endereço de email, eles deverão escolher &quot;Ingressar na equipe&quot; (se solicitado) e selecionar o perfil associado à nova organização.

![imagem de direitos de administrador](assets/admin-get-started-email.png)

## Adicionar um administrador de equipes {#add-admin-teams}

Aplicável a: clientes de equipes do Adobe.

Como administrador, você pode atribuir a função Administrador do sistema a outros usuários, dando a eles os mesmos privilégios que você tem.

Para adicionar ou convidar um administrador do sistema:

1. Na Admin Console, escolha **Usuários** > **Administradores**.

   Uma lista de administradores existentes é exibida.

1. Clique em **Adicionar administrador**.

   A tela **Adicionar um Administrador** é exibida.

1. Insira um nome ou endereço de email. Você pode pesquisar usuários existentes ou adicionar um novo usuário especificando um endereço de email válido e preenchendo as informações na tela.

   Por padrão, Administrador do sistema é selecionado.

1. Clique em **Salvar**.

![imagem do administrador das equipes](assets/teams-admin.png)

Como todos os usuários em uma organização de equipes são usuários de Business ID, eles recebem um convite por email sobre os novos privilégios administrativos de `message@adobe.com`.
Os usuários devem clicar em Introdução no email para ingressar na organização.

Como parte do processo de logon, os usuários podem ser solicitados a configurar um perfil do Adobe se ainda não tiverem um. Se os usuários tiverem vários perfis associados ao seu endereço de email, eles deverão escolher &quot;Ingressar na equipe&quot; (se solicitado) e selecionar o perfil associado à nova organização.

![imagem de direitos de administrador](assets/admin-get-started-email.png)

## Editar atribuição de administrador corporativo

Aplicável a: clientes corporativos do Adobe.

Como administrador, você pode editar a função de administrador para outro administrador que esteja abaixo de você na Hierarquia administrativa. Por exemplo, você pode remover os privilégios de administrador de outros administradores.

Para editar funções administrativas:

1. Na Admin Console, escolha **Usuários** > **Administradores**. A lista de administradores existentes é exibida.

   Como alternativa, vá para o Produto, Perfil de Produto ou Grupo de Usuários relevante e navegue até a guia **Administradores**.

1. Clique no nome do administrador para editar.
1. Nos **Detalhes do Usuário**, clique no ![ícone](assets/one-console-ellipses.png) da seção **Direitos Administrativos** e escolha **Editar direitos administrativos**.

   ![editar direitos administrativos](assets/admin-rights-section.png)

1. Edite os direitos administrativos e salve as alterações.

## Editar função de administrador de equipes

Aplicável a: clientes de equipes do Adobe.

Como um Administrador do sistema das equipes, você pode remover os privilégios de Administrador do sistema de outros administradores.

Para revogar privilégios de administrador do sistema:

1. Na Admin Console, escolha **Usuários** > **Administradores**.

   A lista de administradores existentes é exibida.

1. Nos Detalhes do Usuário, clique no ![ícone](assets/one-console-ellipses.png) à direita da seção **Direitos Administrativos** e escolha **Editar direitos administrativos**.

   ![editar direitos administrativos](assets/admin-rights-section.png)

1. Edite os direitos administrativos e salve as alterações.

## Remover um administrador

Aplicável a: equipes da Adobe para clientes corporativos.

1. Para revogar permissões de administrador, selecione um usuário e clique em **Remover Administrador**.

![remover imagem do administrador](assets/remove-admin.png)

>[!NOTE]
>
>Remover um administrador não exclui o usuário da Admin Console, mas remove apenas os privilégios associados à função de administrador.

## Matriz de permissões de administradores corporativos

Aplicável a: clientes corporativos do Adobe.

A tabela a seguir lista todas as permissões para os diferentes tipos de administradores, categorizadas pelas seguintes áreas de funcionalidade:

### Gerenciamento de identidade

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Adicionar domínio (solicitar/reivindicar um domínio) | ✔ | |
| Exibir listagem de domínio e domínio | ✔ | |
| Gerenciar chaves de criptografia de domínio | ✔ | |
| Gerenciar política padrão de senha da organização | ✔ | |
| Exibir política padrão de senha da organização | ✔ | |

### Gerenciamento de usuários

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Adicionar usuário à organização | ✔ | |
| Remover usuário da organização | ✔ | |
| Exibir detalhes e listagem do usuário | ✔ | |
| Editar perfil de usuário | ✔ | |
| Adicionar perfil de produto ao usuário ou grupo | ✔ | |
| Remover Perfil de Produto para usuário ou grupo | ✔ | |
| Adicionar perfil de produto a vários usuários | ✔ | |
| Exibir perfis de produto para um usuário | ✔ | |
| Exibir lista de usuários de produtos | ✔ | |
| Adicionar usuários em massa à organização | ✔ | |

### Gerenciamento de administradores

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Conceder Org Admin a um usuário | ✔ | |
| Revogar o Org Admin de um usuário | ✔ | |
| Conceder administrador de licença de produto a um usuário | ✔ | |
| Revogar administrador de licença de produto de um usuário | ✔ | |
| Conceder administrador de implantação a um usuário | ✔ | |
| Revogar administrador de implantação de um usuário | ✔ | |
| Conceder administrador de grupo de usuários a um usuário | ✔ | |
| Revogar administrador de grupo de usuários de um usuário | ✔ | |
| Conceder administrador de proprietário de produto a um usuário | ✔ | |
| Revogar administrador proprietário do produto de um usuário | ✔ | |

### Gerenciamento de configuração de licença de produto

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Conceder direito de produto à organização | | |
| Remover direito do produto da organização | | |
| Exibir o número total de licenças pertencentes à organização | ✔ | |
| Exibir produtos e famílias de produtos disponíveis | ✔ | |
| Editar descrições/dados de licença do produto | ✔ | |
| Provisionar licença de produto para um usuário | ✔ | |
| Desprovisionar licença de produto de um usuário | ✔ | |
| Adicionar nova configuração de licença de produto | ✔ | |
| Editar configuração do serviço de licença do produto | ✔ | |
| Excluir configuração do serviço de licença do produto | ✔ | |
| Remover o acesso ao produto de um usuário (remover de todas as configurações) | ✔ | |

### Gerenciamento de armazenamento

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Exibir pastas de usuários Ativas e Inativas | ✔ | |
| Excluir pastas de usuários inativos e transferir conteúdo | ✔ | |

### Implantação

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Guia Exibir/usar pacotes | ✔ | |

### Suporte

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Exibir guia Suporte | ✔ | |
| Gerenciar casos de suporte | ✔ | ✔ |

### Gerenciamento do grupo de usuários

| Permissão | Administrador do sistema | Administrador de suporte |
|--- |--- |--- |
| Criar grupo de usuários | ✔ | |
| Remover grupo de usuários | ✔ | |
| Adicionar usuário ao grupo de usuários | ✔ | |
| Remover usuário do grupo de usuários | ✔ | |
| Atribuir grupo de usuários à licença do produto | ✔ | |
| Remover grupo de usuários da licença do produto | ✔ | |
| Exibir membro do grupo de usuários | ✔ | ✔ |
| Exibir lista de grupos de usuários | ✔ | ✔ |