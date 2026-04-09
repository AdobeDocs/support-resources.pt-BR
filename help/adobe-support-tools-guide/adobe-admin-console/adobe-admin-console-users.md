---
title: Usuários do Adobe Admin Console
description: Planeje sua estratégia para gerenciar usuários no Adobe Admin Console — adicione administradores e usuários finais, escolha um método de gerenciamento de usuários e atribua licenças.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 3%

---

# Usuários do Adobe Admin Console

Aplica-se a empresas e equipes.

Enfrentando um desses problemas? Selecione um problema para ver a resolução.

- [Gerenciar funções de Administrador](https://helpx.adobe.com/br/enterprise/using/admin-roles.html)
- [Problemas de download-instalação](https://helpx.adobe.com/br/download-install.html)
- [Redefinir senha de usuário do Enterprise ID](https://helpx.adobe.com/br/enterprise/kb/enterprise-id-faq.html#faq)
- [Resolver erros do Federated ID](https://helpx.adobe.com/br/enterprise/kb/tshoot-fed-id.html)
- [Excluir usuário ou restaurar usuário excluído](https://helpx.adobe.com/br/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - Usuários** — [Assista no YouTube](https://youtu.be/w8b36YX2TEM)

## Por que adicionar usuários ao Adobe Admin Console

>[!NOTE]
>
>Como administrador na Adobe Admin Console, depois de escolher seu [tipo de identidade](https://helpx.adobe.com/br/enterprise/using/identity.html) e [configurar a identidade](https://helpx.adobe.com/br/enterprise/using/set-up-identity.html), sua próxima tarefa será adicionar usuários à Admin Console.

O Adobe Enterprise e Equipes define amplamente dois tipos de usuários:

### Administradores (administradores)

Os administradores de empresas ou equipes executam tarefas administrativas na Admin Console. Você adiciona administradores para definir uma hierarquia administrativa flexível que permita o gerenciamento refinado do acesso, utilização e outras tarefas administrativas do produto Adobe.

Todos os administradores devem ser adicionados à Admin Console. Ao adicioná-los, os privilégios administrativos são baseados em suas [funções administrativas](https://helpx.adobe.com/br/enterprise/using/admin-roles.html).

### Usuários finais

Os usuários finais são os usuários em sua organização ou instituição que usam os produtos e serviços da Adobe que sua organização ou instituição obteve como parte do contrato com a Adobe.

## Decida sua estratégia de gerenciamento de usuários

Dependendo das suas necessidades, você pode adicionar, remover ou atualizar os usuários *individualmente* ou usar um dos *métodos de carregamento em massa* disponíveis. Use a matriz a seguir como guia para planejar o gerenciamento de usuários.

>[!NOTE]
>
>Se você for um novo cliente corporativo ou de equipes do Adobe, recomendamos consultar essa tabela antes de começar a gerenciar os usuários na Admin Console. Os clientes existentes podem usar isso, especialmente se estiverem planejando migrar de um tipo de identidade para outro (consulte [Editar tipo de identidade](https://helpx.adobe.com/br/enterprise/using/switch-user-identity.html)).

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>Individualmente (Admin Console)</strong></th>
<th scope="col"><strong>Upload em massa de CSV (Admin Console)</strong></th>
<th scope="col"><strong>Conectores Azure/Google</strong></th>
<th scope="col"><strong>Ferramenta de sincronização de usuários</strong></th>
<th scope="col"><strong>API REST de gerenciamento de usuários</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Aplicável a</strong></th>
<td colspan="2">Equipes da Adobe e clientes corporativos</td>
<td colspan="3">Clientes corporativos da Adobe</td>
</tr>
<tr>
<th scope="row"><strong>Descrição</strong></th>
<td>Gerenciar usuários individualmente na Admin Console.</td>
<td>Gerencie usuários com o upload de arquivo CSV na Admin Console.</td>
<td>Gerencie usuários (e grupos) com base em seu portal do Azure AD existente ou na federação do Google.</td>
<td colspan="2">Gerencie usuários (e grupos) com base no LDAP da sua organização.</td>
</tr>
<tr>
<th scope="row"><strong>Adicionar usuários</strong></th>
<td>Guia <strong>Usuários</strong> no <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html#add-users">Leia mais</a>.</td>
<td>Usar <strong>Adicionar usuários por CSV</strong> em <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html">Leia mais</a>. <em>(Usar modelo CSV padrão.)</em></td>
<td>Adicionar usuários no <a href="https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html">Azure</a> ou <a href="https://helpx.adobe.com/br/enterprise/using/setup-sso-google.html">Google</a>. Ou via <strong>Admin Console</strong>.</td>
<td colspan="2">Os usuários devem ser adicionados ao LDAP de sua organização.</td>
</tr>
<tr>
<th scope="row"><strong>Remover usuários</strong></th>
<td>Selecione e remova o usuário no <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html#remove-users">Leia mais</a>.</td>
<td>Escolha <strong>Remover usuários por CSV</strong> na guia <strong>Usuários</strong> do <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html#remove-users">Leia mais</a>. <em>(Usar modelo CSV padrão.)</em></td>
<td>Os usuários devem ser removidos no <a href="https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html">Azure</a> ou <a href="https://helpx.adobe.com/br/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Certifique-se de que as informações do usuário estejam sincronizadas. <strong>Cuidado:</strong> os usuários que não estão no LDAP de sua organização foram removidos do Admin Console.</td>
</tr>
<tr>
<th scope="row"><strong>Editar detalhes do usuário</strong></th>
<td>Selecione o usuário e depois <strong>Editar Detalhes do Usuário</strong> no Admin Console. <a href="https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html#edit-user-details">Leia mais</a>.</td>
<td>Escolha <strong>Editar detalhes do usuário por CSV</strong> na guia <strong>Usuários</strong> do <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html#edit-user-details">Leia mais</a>. <em>(Usar modelo CSV padrão.)</em></td>
<td>Todas as informações do usuário devem ser alteradas no <a href="https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html">Azure</a> ou <a href="https://helpx.adobe.com/br/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Certifique-se de que as informações do usuário estejam sincronizadas.</td>
</tr>
<tr>
<th scope="row"><strong>Tipos de identidade compatíveis</strong></th>
<td colspan="2">Todas</td>
<td>Federated ID</td>
<td colspan="2">FEDERATED ID e ENTERPRISE ID</td>
</tr>
<tr>
<th scope="row"><strong>Limite do atualizações por operação</strong></th>
<td>10</td>
<td>25.000 (<em>5.000 para desempenho ideal</em>)</td>
<td colspan="3">Ilimitado (mapeia para o LDAP da sua organização)</td>
</tr>
<tr>
<th scope="row"><strong>Exige</strong></th>
<td>Adobe Admin Console</td>
<td>Criar e atualizar formatos de arquivo .csv, de preferência usando o Microsoft Excel</td>
<td>Você deve configurar a federação do Azure AD ou do Google</td>

<td>
  <ul>
    <li>Terminal macOS ou Prompt de comando do Windows</li>
    <li>Noções básicas sobre LDAP</li>
  </ul>
</td>

<td>Conhecimento prático de uma linguagem de programação (como Python) para consumir APIs REST</td>
</tr>
<tr>
<th scope="row"><strong>Saiba mais</strong></th>
<td><a href="https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html">Gerenciar usuários individuais</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html">
        Gerenciar usuários | Carregamento em massa de CSV
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/br/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        Solucionar problemas de upload de CSV de usuário em massa
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/br/enterprise/using/sso-setup-azure.html">
        Azure AD Connector
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/br/enterprise/using/setup-sso-google.html">
        conector de federação do Google
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        Sobre a sincronização de usuários
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Repositório Git
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/br/enterprise/using/user-sync.html">
        Guia passo a passo
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">Sobre a UMAPI</a></td>
</tr>
</tbody>
</table>

## Próximas etapas

### Criar pacotes

Depois de adicionados, os usuários estarão prontos para receber os aplicativos e serviços designados.

Atribua licenças a usuários finais com base em seu método de licenciamento:

- **Licenciamento de Usuário Nomeado:** Adicione estes usuários a **produtos** ([para equipes](https://helpx.adobe.com/br/enterprise/using/assign-licenses-to-teams-users.html)) ou **perfis de produto** ([para empresas](https://helpx.adobe.com/br/enterprise/using/manage-product-profiles.html)) para conceder a eles direitos de produto e serviço da Adobe. Para obter mais detalhes, consulte como [criar pacotes de Licenciamento de Usuário Nomeados](https://helpx.adobe.com/br/enterprise/using/create-nul-packages.html) e [perfis de produto](https://helpx.adobe.com/br/enterprise/using/manage-product-profiles.html#create-product-profile).
- **Licenciamento de Dispositivo Compartilhado:** [Os usuários adicionados](https://helpx.adobe.com/br/enterprise/using/sdl-deployment-guide.html#add-users-admin-console) podem usar os dispositivos compartilhados configurados que são acessíveis somente por **usuários da organização**. Para obter mais detalhes, consulte [Criar pacotes SDL](https://helpx.adobe.com/br/enterprise/using/create-sdl-packages.html).

### Implantar pacotes

Depois de criar o pacote, implante-o nos computadores clientes usando um destes métodos:

- Vá para a máquina cliente e clique duas vezes no arquivo de pacote (Windows ou macOS).
- Use o prompt de comando do Windows ou o terminal macOS.
- Usar ferramentas de terceiros:
   - [Microsoft Intune](https://helpx.adobe.com/br/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Microsoft System Center Configuration Manager (SCCM)](https://helpx.adobe.com/br/enterprise/kb/deploy-packages-using-sccm.html)
   - [Área de Trabalho Remota (ARD) do Apple](https://helpx.adobe.com/br/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/br/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki](https://helpx.adobe.com/br/enterprise/kb/deploy-packages-using-munki.html)

## Leitura relacionada

- [Gerenciar usuários | Individualmente](https://helpx.adobe.com/br/enterprise/using/manage-users-individually.html)
- [Gerenciar usuários | Carregamento de CSV em massa](https://helpx.adobe.com/br/enterprise/using/bulk-upload-users.html)
- [Gerenciar usuários do Diretório](https://helpx.adobe.com/br/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/br/enterprise/using/admin-console.html)
- [Atribuir usuários a perfis de produtos (para empresas e instituições)](https://helpx.adobe.com/br/enterprise/using/manage-product-profiles.html#assign-users)
- [Atribuir licenças a usuários de equipes](https://helpx.adobe.com/br/enterprise/using/assign-licenses-to-teams-users.html)
- [Modelo de armazenamento empresarial](https://helpx.adobe.com/br/enterprise/kb/business-storage-model-introduction.html)