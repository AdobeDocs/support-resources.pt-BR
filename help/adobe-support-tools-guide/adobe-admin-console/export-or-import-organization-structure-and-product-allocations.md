---
title: Exportar ou importar estrutura da organização e alocações de produtos
description: Saiba como os administradores globais exportam e importam dados de hierarquia de organização e alocação de produto na Global Admin Console usando JSON, CSV ou XLSX. Aplicável a Enterprise.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 3220086a-4603-465f-a3e3-194193ca10ba
source-git-commit: ee2da1708a19eb7871ffb03f2840c0b7d82bd159
workflow-type: tm+mt
source-wordcount: '4423'
ht-degree: 3%

---

# Exportar ou importar estrutura da organização e alocações de produtos

**Aplica-se a:** Empresa

Saiba como os administradores globais podem simplificar o gerenciamento de organização e de produtos com recursos de exportação e importação na Global Admin Console.

Acesse a guia **[!UICONTROL Organizações]** no [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) para exportar ou importar a estrutura da organização. Acesse a guia **[!UICONTROL Alocação de Produto]** para obter dados de alocação. Use o ícone **[!UICONTROL Mais Opções]** **&#x200B;**&#x200B;para selecionar exportar ou importar. [Entre na Global Admin Console](https://global-admin-console.adobe.com).

## Exportar a estrutura da organização

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), você pode exportar a hierarquia da organização. É possível baixar uma representação JSON, CSV ou XLSX de toda a hierarquia da organização ou um subconjunto dela. É possível então usar esses dados para análise ou modificação.

O formato de exportação escolhido afeta a estrutura dos dados exportados:

- Formato CSV — Permite exportar apenas um tipo de dados por vez. Ao exportar perfis de produto no formato CSV, os perfis e os recursos são combinados em uma tabela. Há várias entradas para o perfil de produto, uma para cada recurso.
- Formato XLSX — os resultados em cada detalhe da organização são exibidos em uma planilha separada. Os registros são conectados entre os diferentes tipos de objeto por uma ID de referência. Em alguns casos, pode haver várias linhas para um objeto específico (por exemplo, objetos de Recurso quando há um conjunto de valores associados a um determinado recurso).
- Formato JSON — O mais flexível. Ele pode aproveitar as relações estruturais entre objetos exportados (por exemplo, os produtos em uma organização aparecem diretamente no elemento de organização). Os mesmos campos são exportados em todos os três formatos, mas alguns valores são redundantes no formato JSON.

### Etapas para exportar

1. Entrar na [Global Admin Console](https://global-admin-console.adobe.com/). Na guia **[!UICONTROL Organizações]**, use o seletor de organização para selecionar a hierarquia da organização para a qual deseja exportar. Os dados de todas as organizações na hierarquia são exportados.
2. Selecione o ícone **[!UICONTROL Mais Opções]** e escolha **[!UICONTROL Exportar]**.

   ![Exportar estrutura da organização](./assets/export-org-structure.png)

3. Na caixa de diálogo **[!UICONTROL Exportar]**, selecione o que deseja exportar e um formato no qual os dados serão exportados.

   ![Caixa de diálogo de exportação do Admin Console](./assets/export-12.png)

4. Selecione **[!UICONTROL Exportar]**. O arquivo de exportação pode levar vários minutos para ser gerado. Após a conclusão, para baixar o relatório, navegue até **[!UICONTROL Global Admin Console]** > **[!UICONTROL Insights]** > **[!UICONTROL Exportar Relatórios]**.

>[!NOTE]
>
>Os arquivos JSON são exportados em um formato zip. Você pode abri-los usando um utilitário zip ou os recursos zip do sistema operacional.

Após baixar o arquivo, você pode manipular os dados e importá-los de volta. As atualizações importadas aparecem no Global Admin Console como se você tivesse editado manualmente os dados.

## Importar a estrutura da organização

Como [administrador global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), você pode importar dados potencialmente modificados. Quando carregados, os novos dados são comparados com os dados atuais e quaisquer alterações são aplicadas à hierarquia da organização. Todas as operações de importação são executadas na cópia atualizada da hierarquia da organização. Se você tiver alterações pendentes, as alterações de importação serão adicionadas sobre as alterações pendentes na hierarquia.

### Etapas para importar

1. Entrar na [Global Admin Console](https://global-admin-console.adobe.com). Na guia **[!UICONTROL Organizações]**, use o seletor de organização para selecionar a hierarquia da organização na qual você deseja realizar a importação.
2. Selecione o ícone **[!UICONTROL Mais Opções]** **&#x200B;**&#x200B;e selecione **[!UICONTROL Importar]**. Dependendo do tamanho e da complexidade do arquivo de importação, o processamento pode levar de alguns segundos a vários minutos.
3. Selecione **[!UICONTROL Selecione um arquivo]** e escolha um arquivo JSON, CSV ou XLSX para ser carregado. Para CSV, somente um detalhe da organização pode ser importado de cada vez e ele não oferece suporte à importação de produtos. As alterações importadas aparecem como se você tivesse editado manualmente os dados.
4. Selecione **[!UICONTROL Fechar]**.
5. Selecione **[!UICONTROL Revisar alterações pendentes]**. Em seguida, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html). Antes de executar as alterações, as ações pendentes são exibidas da mesma maneira que quando as edições são feitas manualmente no Global Admin Console.

## Exportar e importar esquemas

Ao importar dados usando um arquivo CSV, os campos podem aparecer em qualquer ordem, mas sempre devem corresponder à linha de cabeçalho.

Ao importar dados, você deve especificar uma operação para cada elemento. A operação pode ser qualquer uma das seguintes:

- Update: indica uma edição.
- Criar: indica a criação de um novo objeto (por exemplo, organização, grupo de usuários ou administrador).
- Deletar: indica a deleção de um objeto (por exemplo, organização, grupo de usuários ou administrador).

Os registros de entrada sem campo de operação ou com campo de operação em branco são ignorados.

### Organizações

<table>
  <tr>
    <th>Nome do campo</th>
    <th>Descrição</th>
    <th>Notas</th>
  </tr>

<tr>
    <td>id</td>
    <td>
      ID da organização.<br><br>
      Ao adicionar uma nova organização, isso pode ficar vazio ou ser definido como um identificador de espaço reservado, por exemplo,
      new_org_1 O identificador de espaço reservado é usado em casos em que outras entradas importadas precisam se referir a
      para esta organização. Após a criação, uma ID de organização real será atribuída e substituirá todas
      usos da id da organização de espaço reservado.
    </td>
    <td>Pode ser definido como um valor temporário quando operation=create</td>
  </tr>

<tr>
    <td>name</td>
    <td>
      Nome simples da organização. Comprimento mínimo 4, máximo 100.
      Os nomes podem conter caracteres UTF-8 de até 3 bytes,
      Caracteres de 4 bytes não são suportados.
    </td>
    <td>
      Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>Código do país ou região</td>
    <td>
      Deve ser definido quando operation=create, pode ser atualizado quando operation=update
    </td>
  </tr>

<tr>
    <td>tipo</td>
    <td>Tipo de organização</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      ID da organização principal. Em branco para a organização raiz.
      Ao atualizar, restrições significativas se aplicam, incluindo que o novo pai esteja na mesma hierarquia e
      ter os produtos presentes na organização.
    </td>
    <td>
      Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>adminCount</td>
    <td>Número de administradores</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>domainCount</td>
    <td>Número de domínios</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Número de usuários</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>userGroupCount</td>
    <td>Número de grupos de usuários</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>administradores</td>
    <td>Conjunto de objetos de administrador que representam administradores para esta organização</td>
    <td rowspan="6">
      Pode estar ausente se não for selecionada para exportação. Ele é exibido em uma guia separada em arquivos XLSX.
    </td>
  </tr>

<tr>
    <td>domínios</td>
    <td>Conjunto de objetos de domínio que representam domínios nesta organização</td>
  </tr>

<tr>
    <td>products</td>
    <td>Conjunto de objetos de produto que representam produtos nesta organização</td>
  </tr>

<tr>
    <td>productProfiles</td>
    <td>Conjunto de objetos de perfil de produto que representam perfis de produto nesta organização</td>
  </tr>

<tr>
    <td>userGroups</td>
    <td>Conjunto de objetos de grupo de usuários que representam grupos de usuários nesta organização</td>
  </tr>

<tr>
    <td>orgPolicies</td>
    <td>Estrutura que representa as políticas e seus valores</td>
  </tr>

<tr>
    <td>operação</td>
    <td>
      Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados.
    </td>
    <td>Sempre deixar em branco ao exportar.</td>
  </tr>
</table>


**Requisitos de importação:**

- Para atualizar ou excluir, orgId deve se referir a uma organização existente na hierarquia.
- Se estiver criando uma nova organização, você pode deixar o campo orgId em branco ou defini-lo como uma ID exclusiva que pode ser criada (como new-1 ou new-2). Isso fornece uma ID que pode ser usada para fazer referência à organização que será criada.
- O código do país deve ser válido.
- A orgId das operações *Update* e *Delete* já deve estar presente na hierarquia da organização.
- A orgId marcada como *Excluir* não deve ser selecionada como parentOrgId para organizações com a operação *Atualizar* ou *Criar*.
- Organizações secundárias no mesmo nível e do mesmo pai não devem ter os mesmos orgNames.
- Para criar uma organização ou atualizar o nome de uma organização, o nome da organização não deve corresponder ao nome de um filho existente do mesmo pai.

### Administradores

<table>
  <tr>
    <th>Nome do campo</th>
    <th>Descrição</th>
    <th>Usar</th>
  </tr>

<tr>
    <td>orgId</td>
    <td>Referência à organização na qual o administrador reside.</td>
    <td>Usado como uma referência para localizar objetos contendo ou associados.</td>
  </tr>

<tr>
    <td>firstName</td>
    <td>
     Nome do usuário administrador.
O nome e sobrenome dos usuários do Adobe ID podem ser substituídos por um valor fornecido pelo usuário quando ele aceitar o convite.
    </td>
    <td rowspan="4">
      Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>lastName</td>
    <td>Sobrenome do usuário administrador</td>
  </tr>

<tr>
    <td>email</td>
    <td>Endereço de email do usuário administrador. Essa é uma chave primária para o usuário e deve ser exclusiva.</td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>
Código do país ou região onde o usuário opera. Aplica-se somente a tipos Federated Id e Enterprise Id.
    </td>
  </tr>

<tr>
    <td>userType</td>
    <td>Um de "Adobe ID", "Enterprise ID" ou "Federated ID".</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>Um entre "GLOBAL ADMIN", "GLOBAL VIEWER", "SYSTEM ADMIN", "USER GROUP ADMIN", "PRODUCT ADMIN", "PRODUCT PROFILE ADMIN", "DEPLOYMENT ADMIN" e "STORAGE_ADMIN".</td>
    <td rowspan="4">Pode ser definido quando operation=Create</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>ID do grupo do qual este usuário é administrador. Relevante somente para administradores de grupos de usuários e perfis de produtos.</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>ID da licença do produto do qual este usuário é administrador. Relevante somente para administradores de produtos.</td>

</tr>

<tr>
    <td>domínio</td>
    <td>Nome de domínio do usuário, se não estiver usando o domínio de email</td>

</tr>

<tr>
    <td>userName</td>
    <td>Nome de usuário, se não estiver usando o endereço de email</td>
    <td></td>
  </tr>

<tr>
    <td>operação</td>
    <td>Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados.</td>
    <td></td>
  </tr>
</table>


**Requisitos de importação:**

- orgId, email, adminType e userType devem conter valores válidos.
- countryCode deve ser válido.
- Se o usuário já existir e estiver sendo atualizado, userType deverá corresponder ao usuário.
- Verifique se há endereços de email duplicados na organização.

### Perfis de produto

As exportações e importações de perfis de produtos consistem em duas partes: os detalhes do perfil do produto e um conjunto de recursos associados ao perfil do produto. Esses recursos identificam serviços que podem ser configurados, geralmente apenas para ativá-los ou desativá-los.

- Os objetos de recurso são aninhados no perfil do produto no formato JSON.
- Ao usar CSV ou XLSX com perfis de produto, os perfis e os recursos são combinados em uma tabela. Haverá várias entradas para o perfil de produto, uma para cada recurso.
- O campo &quot;selecionado&quot; no recurso controla se o serviço está ativado.
- Ao importar perfis de produtos, deve haver uma operação Criar ou Atualizar no próprio perfil do produto e em qualquer objeto de recurso que deva ser atualizado ou criado.


<table>
  <tr>
    <th>Nome do campo</th>
    <th>Descrição</th>
    <th>Usar</th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      Identificador do perfil de produto
O valor do espaço reservado pode ser usado na criação para que outros objetos possam fazer referência ao novo perfil.
    </td>
    <td>Pode ser definido como valor temporário quando operation=create</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     Nome do perfil do produto. Não pode ser uma duplicata de outros perfis de produto ou grupos de usuários na mesma organização.
    </td>
    <td rowspan="2">
   Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>Descrição de texto do perfil de produto</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>Referência da ID da licença para o produto</td>
    <td rowspan="2"> Usado como uma referência para localizar o objeto contêiner ou associado
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
Organização que contém o grupo de usuários
    </td>
  </tr>

<tr>
    <td>notificações</td>
    <td>Verdadeiro ou falso para indicar se a notificação por email deve ser enviada aos usuários quando eles forem adicionados ou removidos do perfil de produto</td>
    <td>Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente</td>
  </tr>

<tr>
    <td>recursos</td>
    <td> Matriz de recursos associados a este perfil de produto.
O campo de recursos só está presente para o formato JSON. Para os formatos CSV e XLSX, os recursos são representados com os seguintes campos adicionais: resourceName, resourceId, resourceDescription, icon, seleted, quota, resourceType. Para obter detalhes sobre esses campos, consulte [Products and resources](#products-and-resources).
Se o perfil de produto tiver mais de um recurso, haverá várias linhas presentes, uma para cada recurso. Os outros campos terão os mesmos valores para cada recurso. </td>
    <td></td>
  </tr>

<tr>
    <td>operação</td>
    <td>Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados.</td>  
    <td></td>
  </tr>
</table>



**Requisitos de importação:**

- productProfileId, licenseId e orgId devem ter valores válidos.
- Ao criar um perfil de produto, productProfileName deve ser um nome válido e não deve duplicar outro nome de perfil de produto ou nome de grupo de usuários na mesma organização.
- O campo de cota deve ter um valor válido para o tipo de unidade. É numérico ou &quot;ilimitado&quot; quando resourceType=QUOTA ou em branco caso contrário.
- O campo de notificação deve ser verdadeiro ou falso.
- Para importações CSV e XLSX, valide productProfileId; todas as entradas devem ter a mesma orgId, licenseId e productProfileName.
- Valide productProfileName duplicado no arquivo de entrada e na organização.
- Os perfis a serem atualizados e excluídos devem estar presentes na organização.
- Os recursos a serem atualizados e excluídos (desativados) devem estar presentes no perfil.
- Para que os perfis sejam criados, verifique o seguinte:
   - A orgId deve ser uma nova organização ou uma organização existente.
   - A licenseId deve ser um produto novo ou um produto existente.
   - Valide os recursos do perfil.

### Recursos em perfis de produtos

<table>
  <tr>
    <th>Nome do campo</th>
    <th>Descrição</th>
    <th>Usar</th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>Nome do recurso</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>Identificador do recurso</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>Descrição de texto do recurso</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>ícone</td>
    <td>URL para imagem do recurso</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>selecionado</td>
    <td>
      Para uma entrada de configuração, se o recurso está habilitado.
      Esse campo está presente somente em JSON.
    </td>
    <td rowspan="2">
      Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente.
    </td>
  </tr>

<tr>
    <td>cota</td>
    <td>
      Quantidade de recursos principais que podem ser fornecidos aos usuários por meio deste perfil de produto.
      Esse campo está presente somente em JSON.
    </td>
  </tr>


<tr>
    <td>resourceType</td>
    <td>
      Se presente, o valor é SERVICE. Indica que esse recurso representa um serviço que pode ser
      ativado ou desativado com base no valor do campo selecionado.
      Esse campo está presente somente em JSON.
    </td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>operação</td>
    <td>
      Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados.
    </td>
    <td></td>
  </tr>
</table>


**Requisitos de importação:**

- O campo de operação nos recursos será ignorado quando o perfil de produto ao qual ele pertence tiver operações definidas como *Excluir* ou *Criar*.
- Nenhum recurso deve ser marcado para exclusão; é uma operação inválida.
- Para que perfis de produtos sejam criados, o número de recursos deve corresponder ao número de recursos do perfil de produto de origem.
- Para recursos com a operação *Atualizar*, o recurso deve estar presente no perfil do produto.

### Grupos de usuários

<table>
  <tr>
    <th>Nome do campo</th>
    <th>Descrição</th>
    <th>Usar</th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
      Identificador do grupo de usuários. O valor do espaço reservado pode ser usado na criação para que
      outros objetos podem fazer referência ao novo grupo de usuários.
    </td>
    <td>Pode ser definido como valor temporário quando operation=create</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td>Nome do grupo de usuários</td>
    <td rowspan="2">
      Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente.
    </td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>Descrição de texto do grupo de usuários</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Número de usuários no grupo</td>
    <td>Somente leitura</td>
  </tr>

<tr>
    <td>perfis</td>
    <td>
      Matriz de IDs de perfil de produto à qual o grupo de usuários está associado.
      XLSX tem uma linha por valor com os mesmos valores para outros campos.
    </td>
    <td>
      Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente.
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>Organização que contém o grupo de usuários</td>
    <td>Usado como uma referência para localizar o objeto contêiner ou associado</td>
  </tr>

<tr>
    <td>operação</td>
    <td>
      Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados.
    </td>
    <td></td>
  </tr>
</table>

**Requisitos de importação:**

- orgId deve se referir a uma organização existente ou a uma organização que está sendo criada na mesma importação.
- userGroupId deve se referir a um grupo existente para atualização ou exclusão, e pode ser uma id definida por você para novos grupos de usuários.
- Para atualizar ou criar, userGroupName não deve estar em branco e não deve duplicar outro grupo de usuários ou nome de perfil de produto na mesma organização.
- Verifique se userGroupName não está duplicado no arquivo de entrada e na organização.
- Os grupos de usuários a serem atualizados e excluídos devem estar presentes na organização.
- O perfil a ser removido do grupo de usuários deve estar presente no grupo de usuários. Não é possível executar operações de atualização no perfil de um grupo de usuários.
- Para criar grupos de usuários, verifique o seguinte:
   - A orgId deve ser uma nova organização ou uma organização existente.
   - A licenseId, se aplicável, deve ser um produto novo ou um produto existente.
   - O productProfileId deve ser um perfil de produto novo ou um perfil de produto existente.

### Domínios

As informações de domínio fornecem informações somente leitura sobre domínios disponíveis em cada organização. Estes dados não podem ser editados.


| Nome do campo | Descrição | Usar |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | Referência à organização na qual este domínio está listado | Usado como uma referência para localizar objetos contendo ou associados. |
| domainName | Nome do domínio (por exemplo, adobe.com). | Somente leitura |
| diretoryName | Nome do diretório no qual o domínio está listado | Somente leitura |
| diretoryType | Um Federated ID ou Enterprise ID. | Somente leitura |
| domainStatus | Um dos seguintes: &quot;ATIVO&quot;, &quot;RESERVADO&quot;, &quot;NÃO RECLAMADO&quot;, &quot;RECLAMADO&quot;, &quot;VALIDADO&quot;, &quot;RETIRADO&quot;, &quot;EXPIRADO&quot;. | Somente leitura |


### Produtos e recursos {#products-and-resources}

Nos arquivos XLSX, há duas folhas — uma para produtos e outra para os recursos. Em JSON, os objetos de recurso são aninhados no objeto de produto.

**Produtos**


| Nome do campo | Descrição | Usar |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | ID que identifica o produto. Cada produto tem uma ID de licença exclusiva na organização em que está listado. Ao adicionar um novo produto, pode estar vazio ou usar um identificador de espaço reservado (por exemplo, new_product_1). Após a criação, é atribuída uma ID de licença real que substitui todos os usos da ID de licença de espaço reservado. | Pode ser definido como valor temporário quando operation=create |
| productName | Nome do produto | Somente leitura |
| productDescription | Descrição de texto do produto | Somente leitura |
| allowOverallocation | Booleano que indica se a superalocação desta instância do produto é permitida. Superalocação refere-se à capacidade de conceder mais quantidades a uma organização-filho do que você recebeu. | Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente |
| ícone | URL do ícone do produto | Somente leitura |
| sourceLicenseId | ID da licença da instância do produto na organização da qual este produto foi alocado. O valor é nulo se essa instância não for um produto alocado, em vez de ser um produto comprado. | Pode ser definido quando operation=Create |
| productId | Identificador do produto. | Somente leitura |
| orgId | Identificador da organização que contém esta instância do produto | Usado como uma referência para localizar o objeto contêiner ou associado |
| redistribuível | Booleano que indica se este produto tem recursos que podem ser concedidos a organizações-filho. | Somente leitura |
| recursos | Objeto que contém um conjunto de objetos de recurso que representam os recursos e as configurações deste produto |                                                                               |
| operação | Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados. |                                                                               |


**Requisitos de importação:**

- Para criar, a licenseId deve ser uma ID exclusiva, criada por você.
- Para a atualização, a licenseId deve ser a id de um produto existente na organização especificada.
- orgId deve se referir a uma organização existente ou que está sendo criada na mesma operação de importação.
- Para criar, sourceLicenseId deve se referir a um produto existente ou à ID definida para um produto que está sendo criado na mesma operação de importação.
- licenseId e sourceLicenseId não devem ser iguais para produtos com a operação *Criar*.
- Validar organizações de produtos; a organização deve ser uma nova ou já deve estar presente na hierarquia da organização.
- Para as operações de *Atualização* e *Exclusão*, o produto já deve estar presente na hierarquia da organização.
- A licenseId marcada como *Excluir* não deve ser usada como sourceLicenseId de produtos com a operação *Criar* e *Atualizar*.
- Para produtos com a operação *Criar*, valide se sourceLicenseId deve estar presente na organização principal.

**Recursos para produtos**

Os objetos de recurso podem aparecer em produtos e em perfis de produto.


| Nome do campo | Descrição | Usar |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | Nome do recurso | Somente leitura |
| resourceId | Identificador do recurso | Somente leitura |
| resourceDescription | Descrição de texto do recurso | Somente leitura |
| ícone | URL para imagem do recurso | Somente leitura |
| productName | Nome do produto do qual este recurso faz parte. | Somente leitura |
| licenseId | ID da licença (instância do produto) do produto do qual este recurso faz parte. | Usado como uma referência para localizar o objeto contêiner ou associado |
| grantedQuantity | Quantidade concedida deste recurso: quantidade de recursos que esta organização tem disponíveis para uso local ou alocar para organizações filhas. | Pode ser definido ou atualizado quando operation=create ou operation=update, respectivamente |
| unidade | Nome da unidade de quantidade concedida. | Somente leitura |
| currentQuantity | Quantidade utilizável atual nesta organização. É a grantedQuantity menos os recursos alocados às organizações-filho. Este é o valor exibido no Admin Console para este produto/recurso. | Somente leitura |
| provisionedQuantity | Quantidade realmente provisionada: pode ser menor que concessão ou atual e pode ser menor que currentQuantity se alguma limitação estiver em vigor. | Somente leitura |
| operação | Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados. |                                                                               |


**Requisitos de importação:**

O campo de operação nos recursos será ignorado quando o produto ao qual ele pertence tiver operações definidas como *Excluir* ou *Criar*.
- Nenhum recurso deve ser marcado para exclusão; é uma operação inválida.
- Para que os produtos sejam criados, o número de recursos deve corresponder ao número de recursos do produto de origem.
- Para recursos com a operação *Atualizar*, o recurso deve estar presente no produto.

## Importar e exportar dados de alocação de produtos

Como [Administrador Global](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), você pode exportar os dados de alocação do produto como um arquivo JSON ou CSV. Em seguida, você pode manipular esses dados e carregá-los de volta para importar as alterações. Quando os dados potencialmente modificados são carregados, os novos dados são comparados com os dados atuais e todas as alterações são aplicadas aos dados de alocação do produto. É possível revisar e enviar as alterações pendentes para que elas entrem em vigor.

## Exportar o modelo de alocação de produtos

Para exportar o modelo de alocação de produtos, faça o seguinte:

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/) e navegue até a guia **[!UICONTROL Alocação de Produto]**.
2. Selecione o ícone **[!UICONTROL Mais Opções]** e selecione **[!UICONTROL Exportar CSV]** ou **[!UICONTROL Exportar JSON]**. Seu arquivo foi baixado. [Saiba mais](#export-and-import-formats-for-product-allocation) sobre os formatos de exportação.

## Importar o modelo de alocação de produtos

É possível exportar dados, modificá-los e importar o arquivo modificado. Para importar o modelo de alocação de produtos, faça o seguinte:

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/) e navegue até a guia **[!UICONTROL Alocação de Produto]**.
2. Selecione o ícone **[!UICONTROL Mais Opções]** e selecione **[!UICONTROL Importar]**.
3. Selecione um arquivo JSON ou CSV para fazer upload.
4. Selecione **[!UICONTROL Revisar alterações pendentes]**. Depois de revisar as alterações, selecione **[!UICONTROL Enviar Alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Exportar e importar formatos para alocação de produtos

Os formatos de exportação e importação são os mesmos. Ao importar no formato CSV, os campos podem aparecer em qualquer ordem, mas devem corresponder à linha de cabeçalho. Ao importar no formato JSON, os campos podem aparecer em qualquer ordem.

Você deve especificar a operação ao importar dados de alocação de produtos. A operação pode ser uma das seguintes:

- Atualizar: indica uma edição (alteração para valores grantedQuantity, allowOverAllocation).
- Criar: indica a adição de um recurso de produto à organização especificada.
- Excluir: indica a exclusão do produto.

Se nenhuma operação for fornecida, nenhuma alteração ocorrerá quando os dados forem importados para essa linha no CSV ou objeto no JSON.

No arquivo exportado, há uma linha ou registro para cada recurso de produto. Alguns produtos têm mais de um recurso.

Se um produto tiver mais de um recurso, as operações Atualizar poderão ser aplicadas a recursos independentes, uma operação Excluir excluirá o produto, incluindo todos os recursos de uma organização, e uma operação Criar precisará de um registro para cada um dos recursos no arquivo de importação para que a quantidade adequada de cada um deles possa ser especificada. O campo allowOverAllocation abrange todo o produto e não importa em qual recurso uma atualização para esse campo está.

### Descrição dos cabeçalhos


| Nome do campo | Descrição | Usar |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| productName | Nome do produto. | Somente leitura |
| licenseId | ID de um produto (exclusivo de um produto em uma organização). Ao adicionar um novo produto, isso pode ficar vazio ou ser definido como um identificador de espaço reservado (por exemplo, new_product_1). O identificador de espaço reservado é usado nos casos em que outras entradas importadas precisam se referir a este produto. Após a criação, uma ID de licença real será atribuída e substituirá todos os usos da ID de licença de espaço reservado. | Pode ser definido quando operation=Create |
| sourceLicenseId | ID do produto principal. Está vazio ou nulo se representa uma compra em vez de uma alocação. | Pode ser definido quando operation=Create |
| productId | ID que identifica esta classe de produto. Essa ID é compartilhada entre produtos do mesmo tipo e difere da licenseId que identifica uma instância desse produto. | Somente leitura |
| resourceName | Nome deste recurso de produto. Por exemplo, Licenças de usuário. | Somente leitura |
| resourceId | ID que identifica este recurso do produto. | Pode ser definido quando operation=Create |
| orgPathName | Nome do caminho da organização na qual este recurso de produto está. Segmentos separados por &quot;/&quot;. | Somente leitura |
| orgName | Nome simples da organização que contém este recurso de produto. Este é o segmento final do orgPathName. | Somente leitura |
| orgId | ID da organização que contém este recurso de produto. | Pode ser definido quando operation=Create |
| grantedQuantity | Número de unidades de quantidade de recurso concedidas a esta organização por seu pai ou a quantidade comprada se esta entrada de recurso do produto representar uma compra. Este campo é atualizável, exceto para produtos comprados ou alocações raiz que o administrador global não tem permissão para alterar. | Pode ser atualizado quando operation=Update ou operation=Create |
| unidade | Nome da unidade de recurso. Por exemplo, Usuários. | Somente leitura |
| totalAllocations | Soma das concessões para organizações derivadas desta organização para este recurso de produto. Esse valor inclui as concessões diretas aos filhos imediatos mais as superalocações dessas organizações. Por exemplo, se essa organização concedesse a uma criança 10 e ela alocasse seu filho 25, o totalAllocations seria 25: o 10 concedido à criança mais um excedente de 15 nessa criança. | Somente leitura |
| grantOverage | Valor pelo qual totalAllocations excede a grantedQuantity. Se totalAllocations não exceder grantedQuantity, esse valor será nulo ou igual a zero. | Somente leitura |
| localLicensedQuantity | Quantidade deste recurso concedida a esta organização deixada para uso após a dedução da quantidade alocada aos filhos. Essa é a quantidade mostrada como disponível no Admin Console. Esse valor pode ser zero, mas nunca é negativo mesmo se essa organização tiver recursos superalocados para seus filhos. | Somente leitura |
| localUsage | Número de unidades do recurso usado nesta organização. Por exemplo, delegar uma licença de usuário a um usuário contaria como 1 unidade de uso. | Somente leitura |
| totalUsage | Número de unidades do recurso usado por esta organização e todos os filhos. Isso mostra o uso desse recurso na parte da hierarquia da organização enraizada por essa organização. | Somente leitura |
| useOverage | Valor do uso total na concessão da organização (a organização e os filhos usaram mais recursos do que o disponível). Isso mostra um valor diferente de zero quando totalUsage excede localLicensedQuantity. | Somente leitura |
| allowOverAllocation | Indica se o usuário tem permissão para conceder mais recursos aos filhos, mesmo que não haja mais concessão (permissão para conceder apesar do excedente de concessão). Esse valor se aplica a todos os recursos desse produto. Se for feita uma tentativa de atualizar allowOverallocation para mais de um recurso do mesmo produto para valores diferentes, o resultado é aleatório. | Pode ser atualizado quando operation=Update |
| isPurchasedProduct | true se o produto for um produto de compra (não alocado pelo pai). É equivalente a sourceLicenseId com um valor vazio. | Somente leitura |
| redistribuível | true se o produto puder ser alocado para filhos, false significa que o produto só estará disponível na organização em que é exibido e os recursos não poderão ser alocados para outra organização. | Somente leitura |
| operação | Um de em branco, Criar, Atualizar ou Excluir. Ação a ser tomada quando os dados forem importados. |                                                          |


**Requisitos de importação**

**Validação de dados**

- O campo de operação deve ter uma operação válida.
- Os dados de importação do produto devem ter propriedades e valores para os campos obrigatórios.
- As propriedades de dados de importação do produto devem ser do tipo correto.
- O campo de política de produto (overAllocation) não deve ser fornecido para recursos diferentes.
- O campo grantedQuantity:
   - Não pode ser alterado para *ilimitado* se ainda não for *ilimitado*.
   - Deve ser um inteiro não negativo ou o valor da cadeia de caracteres *ilimitado.*

**Validação de permissão/acessível**

- A organização associada aos dados de importação deve existir. Se estiver atualizando, verifique se o produto e o recurso associados aos dados de importação realmente existem.

**Adicionar validação de produto**

- SourceLicenseId deve existir.
- A organização associada ao novo produto deve existir.
- O produto que está sendo criado não deve existir (produto com a mesma licenseId).
- Os recursos associados a um produto que está sendo criado devem ter uma productId correspondente que corresponda a esse produto.
