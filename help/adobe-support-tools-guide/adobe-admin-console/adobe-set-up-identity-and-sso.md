---
title: Configurar identidade e logon único
description: Saiba como os administradores de sistema da organização podem configurar a identidade do usuário e o Logon único (SSO) na Adobe Admin Console usando o Adobe ID, o Enterprise ID ou o Federated ID.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# Configurar identidade e logon único

**Aplica-se a:** Empresa

Saiba como configurar a identidade na Adobe Admin Console. Compare o Adobe ID, o Enterprise ID e o Federated ID e configure o Logon único (SSO) para obter acesso seguro aos aplicativos do Adobe.

Configure a identidade e configure o Logon Único (SSO) para que os funcionários possam [fazer logon](https://adminconsole.adobe.com/settings/) com as credenciais organizacionais existentes.

Este é o tutorial em vídeo sobre como [Configurar identidade e SSO (YouTube)](https://youtu.be/V57lU4zaSBs).

## Termos e conceitos principais

### Diretório

Um diretório no Admin Console é uma entidade que armazena recursos como usuários e políticas como autenticação. Esses diretórios são semelhantes ao LDAP ou Diretórios ativos.

### Provedor de identidade (IdP)

Um provedor de identidade (IdP) é o provedor de identidade de sua organização, como:

- Ative Diretory
- Microsoft Azure
- Ping
- Okta
- EmComum
- Shibboleth

### Pessoas envolvidas

| Função | Responsabilidade |
|------|----------------|
| Administrador do sistema | Trabalha com gerentes de diretório IdP e gerentes DNS para configurar a identidade na Admin Console. |
| Gerenciador DNS | Atualiza tokens DNS para validar a propriedade do domínio. |
| Gerenciador de diretórios do Provedor de Identidade (IdP) | Manipula o portal IdP e os conectores associados. |

### Adobe ID

Criado, de propriedade e gerenciado pelo usuário final. O Adobe executa a autenticação e o usuário final gerencia a identidade. Dependendo do [modelo de armazenamento](https://helpx.adobe.com/br/enterprise/using/storage-for-business.html), os usuários ou empresas mantêm o controle sobre arquivos e dados.

Para organizações que foram atualizadas para o modelo de armazenamento corporativo, os ativos e os dados são controlados pela organização. Para organizações que não foram atualizadas, a pessoa é proprietária e controla os ativos da Adobe ID.

### Enterprise ID

Criado, pertencente e gerenciado por uma organização. O Adobe hospeda a Enterprise ID e executa a autenticação, mas a organização mantém a Enterprise ID. Os administradores criam uma Enterprise ID e a emitem para um usuário. Os administradores podem revogar o acesso a produtos e serviços assumindo a conta ou excluindo a Enterprise ID para bloquear permanentemente o acesso a dados associados. Para saber mais, clique [aqui](https://helpx.adobe.com/br/enterprise/using/setup-enterprise-id.html).

### Federated ID

Criado e de propriedade de uma organização, e vinculado ao diretório corporativo via federação. A organização gerencia credenciais e processa o Logon Único por meio de um Provedor de Identidade SAML2 (IdP).

Veja a seguir alguns requisitos e cenários em que as Federated IDs são recomendadas:

- Se desejar provisionar usuários com base no diretório enterprise da sua organização.
- Se quiser gerenciar a autenticação de usuários.
- Se você precisar ter controle rigoroso sobre aplicativos e serviços disponíveis para um usuário.

## Configurar identidade sem logon único

Você pode usar o Adobe ID ou o Enterprise ID se sua organização não estiver usando atualmente o SSO em outros aplicativos.

## Utilização do Adobe ID

A Adobe está atualizando todas as organizações para o [Modelo de armazenamento corporativo](https://helpx.adobe.com/br/enterprise/using/storage-for-business.html). Isso dá à sua organização maior controle sobre os ativos e dados dos usuários.

Introdução a [adicionar usuários](https://helpx.adobe.com/br/enterprise/using/users.html) à Admin Console.

## Configurar identidade com o Enterprise ID

Você pode configurar um diretório do Enterprise ID se quiser ter mais controle sobre os dados dos usuários sem usar o SSO. Somente os administradores criam uma Enterprise ID e a emitem para um usuário.

Consulte [Configurar organização com o Enterprise ID](https://helpx.adobe.com/br/enterprise/using/setup-enterprise-id.html) para obter os requisitos e as etapas para criar diretórios do Enterprise ID.

## Configurar identidade com logon único

Você deve configurar a identidade do usuário com contas do Federated ID para usar o SSO.

As Federated IDs são recomendadas quando:

- Você precisa ter controle rigoroso sobre os aplicativos e serviços disponíveis para um usuário.
- Você deseja gerenciar a autenticação de usuários.
- Você deseja provisionar usuários com base no diretório enterprise de sua organização.

## Configurar uma nova integração de SSO

Você pode usar provedores de identidade populares, como Microsoft Azure AD, Google, ou usar outro IdP baseado em SAML para configurar o SSO entre sua organização e os produtos da Adobe.

**Azure AD** (Recomendado) - [Configurar SSO e sincronização de usuário com o Conector do Azure AD](https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html)

**Outro IdP SAML** - [Configurar SSO com outros provedores SAML](https://helpx.adobe.com/br/enterprise/using/create-directory.html)

**Google** (Recomendado) - [Configurar SSO e sincronização de usuário usando o Google Connector](https://helpx.adobe.com/br/enterprise/using/setup-sso-google.html)

## Gerenciar configuração de SSO existente

Depois que o SSO for configurado entre sua organização e a Adobe, use o seguinte para gerenciar e alterar sua configuração.

Saiba como gerenciar domínios e diretórios:

- [Gerenciar usuários](https://helpx.adobe.com/br/enterprise/using/users.html) e [grupos](https://helpx.adobe.com/br/enterprise/using/user-groups..html)
- [Vincular domínios a diretórios](https://helpx.adobe.com/br/enterprise/using/add-domains-directories.html#link-domains-to-directoies) para controlar o acesso dos usuários a aplicativos, serviços e configurações
- [Gerencie a confiança do diretório](https://helpx.adobe.com/br/enterprise/using/directory-trust.html) para usar os domínios reivindicados por outra organização

Saiba como alterar o provedor de identidade:

- [Altere seu IdP](https://helpx.adobe.com/br/enterprise/using/migrate-authentication-provider.html) sem interromper o trabalho de seus usuários
- [Mover domínios entre diretórios](https://helpx.adobe.com/br/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [Remover usuários do diretório herdado](https://helpx.adobe.com/br/enterprise/using/manage-directory-users.html)
- [Excluir domínios antigos/não solicitados e diretórios vazios](https://helpx.adobe.com/br/enterprise/using/manage-domains-directories.html#delete)

## Erros e perguntas comuns

Soluções para dúvidas e erros comuns ao configurar e gerenciar o SSO:

### Azure AD - Perguntas frequentes e solução de problemas

#### Perguntas frequentes

- [Perguntas frequentes sobre o Azure AD Connector](https://helpx.adobe.com/br/enterprise/using/azure-ad-connector-faq.html)
- [Como excluir diretórios e domínios](https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### Solução de problemas

- [Usuários com acesso negado](https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html#sync-issues)
- [Problemas de sincronização](https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html#sync-issues)

### Outro IdP SAML - Perguntas frequentes e solução de problemas

#### Perguntas frequentes

[Perguntas frequentes sobre integração com o SAML](https://helpx.adobe.com/br/enterprise/using/sso-faq.html)

#### Solução de problemas

- [Solução de problemas gerais de SSO](https://helpx.adobe.com/br/enterprise/kb/tshoot-fed-id.html)
- [&#x200B; Erro &quot;Acesso negado&quot;](https://helpx.adobe.com/br/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [&#x200B; &quot;Outro usuário está conectado no momento&quot; erro](https://helpx.adobe.com/br/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [Executar um rastreamento SAML](https://helpx.adobe.com/br/enterprise/kb/perform-a-saml-trace.html)

### Google - Perguntas frequentes

- [Perguntas frequentes sobre o Google Connector](https://helpx.adobe.com/br/enterprise/using/google-federation-faq.html)
- [Como excluir diretórios e domínios](https://helpx.adobe.com/br/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## Participe da conversa

Para colaborar, fazer perguntas e conversar com outros administradores, use a [Comunidade de Empresas e Equipes](https://www.adobe.com/go/entcom_br).

## Assuntos legais e privacidade

- [Avisos legais](https://helpx.adobe.com/br/legal/legal-notices.html)
- [Política de Privacidade Online](https://www.adobe.com/br/privacy.html)
