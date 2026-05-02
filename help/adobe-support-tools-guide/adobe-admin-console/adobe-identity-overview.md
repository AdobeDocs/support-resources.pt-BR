---
title: Visão geral da identidade
description: Entenda e escolha tipos de identidade (Federated ID, Enterprise ID, Adobe ID e Personal Adobe ID) para sua organização e gerencie o acesso de usuários na Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e53ded7c-1ba3-4d98-bc20-792a252618ac
source-git-commit: f20f8cfe6f9f31af953c089b9c5f4e76d0573f84
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 5%

---

# Visão geral da identidade

Aplica-se a empresas e equipes.

O sistema de gerenciamento de identidades da Adobe ajuda os administradores a criar e gerenciar o acesso do usuário a aplicativos e serviços. A Adobe oferece esses tipos de identidade ou contas para autenticar e autorizar os usuários.

## Tipos de identidade no Adobe Admin Console

Os tipos de identidade permitem que a organização tenha diferentes níveis de controle sobre as contas e os dados dos usuários. Sua escolha de modelo de identidade tem um impacto considerável em como sua organização armazena e compartilha ativos. Embora os modelos do Federated ID e do Enterprise ID sejam criados e gerenciados pela organização, as Adobe IDs são criadas e gerenciadas pelo indivíduo.

A tabela a seguir orienta você a escolher qual modelo de identidade se adapta melhor à sua organização.

>[!NOTE]
>Se sua organização não tiver sido atualizada para o modelo de armazenamento corporativo da Adobe e você ainda estiver usando Adobe IDs para indivíduos, consulte a descrição na [tabela de tipos de identidade](https://helpx.adobe.com/enterprise/using/identity.html#using-personal-adobe-id) abaixo.

<table>
<thead>
<tr>
<th scope="col">Tipos de identidade</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Ícone do Federated ID"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Principais ofertas</strong></th>
<td>Criado, de propriedade e gerenciado pela organização. A organização gerencia credenciais de usuário e usa Logon Único (SSO) por meio de um provedor de identidade SAML2 (IdP).</td>
<td>Criado, de propriedade e gerenciado pela organização. A organização retém direitos exclusivos para criar contas de usuário em domínios verificados.</td>
<td>Criado, de propriedade e gerenciado pelo usuário final. O Adobe executa a autenticação e o usuário final gerencia a identidade. Dependendo do <a href="https://helpx.adobe.com/enterprise/using/storage-for-business.html">modelo de armazenamento</a>, os usuários ou empresas mantêm o controle sobre arquivos e dados. As contas do Adobe ID são criadas em domínios não verificados, públicos ou confiáveis. Consulte o ponto 2 da seção de notas abaixo.</td>
</tr>
<tr>
<th scope="row"><strong>Propriedade da conta e dos dados</strong></th>
<td colspan="2">Propriedade e controlada pela organização</td>
<td>Propriedade da organização para armazenamento corporativo e propriedade do usuário para armazenamento do usuário</td>
</tr>
<tr>
<th scope="row"><strong>Segurança e monitoramento</strong></th>
<td colspan="2">
  <ul>
    <li>Logs de auditoria</li>
    <li>Logs de conteúdo</li>
    <li>Restrições de compartilhamento</li>
    <li>Configurações de autenticação da organização</li>
  </ul>
</td>

<td>
  <ul>
    <li>Logs de conteúdo</li>
    <li>Restrições de compartilhamento</li>
    <li>Política de senha</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>Redefinir senha</strong></th>
<td colspan="2">Incompatível</td>
<td><a href="https://helpx.adobe.com/manage-account/using/change-or-reset-password.html">Redefinir a senha da sua conta</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud para corporações e Document Cloud para corporações</strong></th>
<td colspan="3">Suportado</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud para equipes e Document Cloud para equipes</strong></th>
<td colspan="2">Incompatível</td>
<td>Suportado</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">Suportado</td>
</tr>
<tr>
<th scope="row"><strong>Recomendado para</strong></th>
<td>
  <ul>
    <li>Organizações que já usam SSO ou SAML</li>
    <li>Serviços de diretório existentes (por exemplo, Google e Azure AD)</li>
    <li>Requer fácil integração com serviços que não são da Adobe</li>
    <li>Pode demonstrar a propriedade do domínio</li>
  </ul>
</td>
<td>
  <ul>
    <li>Pode demonstrar a propriedade do domínio</li>
    <li>Não exigir SSO</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud para equipes</li>
    <li>A organização prefere usar domínios que não são seus</li>
    <li>Domínios públicos (por exemplo, Hotmail, Gmail)</li>
    <li>Acessar aplicativos como o Adobe Experience Manager Mobile</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Introdução</strong></th>
<td><a href="https://helpx.adobe.com/br/enterprise/using/set-up-identity.html">Configurar identidade</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/add-domains-directories.html#claim-domains">Domínios de declaração</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">Adicionar usuário</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. A política de senha do Creative Cloud para equipes é a mesma do Creative Cloud para usuários individuais.
>1. Os usuários do Adobe ID se autenticam com suas credenciais do Adobe ID ou pelo modelo de autenticação da organização proprietária (SSO, 2FA etc.). Nesses cenários, os usuários são redirecionados para a página SSO da organização proprietária. Após a autenticação, os usuários podem precisar [escolher um perfil comercial](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#choose-profile).

## Utilização de IDs pessoais do Adobe

A Adobe está atualizando todas as equipes e clientes corporativos para usar o modelo de armazenamento corporativo da Adobe. Consulte a tabela a seguir caso sua organização tenha usuários que estejam usando Adobe IDs pessoais para acessar aplicativos e serviços da Adobe de sua empresa ou escola.

### Adobe ID pessoal

<table>
<thead>
<tr>
<th scope="col">Tipo de identidade</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  Adobe ID pessoal
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Principais ofertas</strong></th>
<td>Criado, de propriedade e gerenciado pelo usuário final. O Adobe executa a autenticação e o usuário final gerencia a identidade.</td>
</tr>
<tr>
<th scope="row"><strong>Propriedade da conta e dos dados</strong></th>
<td>Controlado pelo usuário</td>
</tr>
<tr>
<th scope="row"><strong>Segurança e monitoramento</strong></th>
<td>Política de senha. Consulte o ponto 1 na seção de notas abaixo.</td>
</tr>
<tr>
<th scope="row"><strong>Redefinir senha</strong></th>
<td><a href="https://helpx.adobe.com/manage-account/using/change-or-reset-password.html">Redefinir a senha da sua conta.</a>  Consulte o ponto 2 na seção de notas abaixo.</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud para corporações e Document Cloud para corporações</strong></th>
<td>Suportado</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>Suportado</td>
</tr>
<tr>
<th scope="row"><strong>Disponível somente para / Recomendado para</strong></th>
<td>
  <ul>
    <li>Integração de clientes corporativos e de equipes antes da migração</li>
    <li>Creative Cloud para equipes</li>
    <li>Deseja ter controle na mão do usuário</li>
    <li>Acessar aplicativos como o Digital Publishing Suite</li>
    <li>Os usuários possuem ativos após a separação da organização</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Introdução</strong></th>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">Adicionar usuário</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. A política de senha do Creative Cloud para equipes é a mesma do Creative Cloud para usuários individuais.
>1. Para clientes do Creative Cloud para corporações que usam o [armazenamento corporativo](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html), os administradores podem adicionar usuários do Adobe ID à Admin Console, mas não podem adicioná-los aos perfis de produtos. Os administradores devem migrar os usuários do Adobe ID para outro tipo de identidade.
>1. Há alguns produtos e serviços, como o **Site de Licenciamento da Adobe, que só oferece suporte** ao Adobe ID.

## Veja mais aqui

- [Configurar identidade](https://helpx.adobe.com/br/enterprise/using/set-up-identity.html)
- [Alternar identidade do usuário](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)
- [Visão geral do Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
- [Perguntas frequentes sobre educação](https://helpx.adobe.com/x-productkb/policy-pricing/education-faq.html)
- [Adicionar e gerenciar usuários](https://helpx.adobe.com/br/enterprise/using/users.html)
