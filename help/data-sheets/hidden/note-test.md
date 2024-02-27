---
description: Conectar à Data Warehouse do Widget - Documentação do produto
title: Conectar à Data Warehouse do Widget
hide: true
hidefromtoc: true
source-git-commit: fcf5fb8f9728dd27a81de21241a71ce49dd015f8
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Conectar à Data Warehouse do Widget {#connecting-to-the-widget-data-warehouse}

## Novo teste

<ol><li>Use o `{{name}}".</li></ol>

<ol><li>Usar o &amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace;.</li></ol>

## Teste aninhado

**Primeiro**

>[!NOTE]
>
>Não é possível excluir o seguinte:
>
>* Os status incorporados Planejamento, Atual e Concluído. É possível atualizar os nomes, editar as cores e bloqueá-las ou desbloqueá-las, mas elas não podem ser excluídas.
>* Status que estão em um estado pendente de aprovação para pelo menos um objeto no sistema.

**Second**

>[!NOTE]
>
>Não é possível excluir o seguinte:
>
>* Os status incorporados Planejamento, Atual e Concluído. É possível atualizar os nomes, editar as cores e bloqueá-las ou desbloqueá-las, mas elas não podem ser excluídas.
>
>  Isto é entre
>
>* Status que estão em um estado pendente de aprovação para pelo menos um objeto no sistema.

## Link de acesso do widget {#widget-access-link}

Para acessar o data warehouse do Widget, será necessário navegar até o URL específico da conta do Widget.  Você pode encontrar esse link de acesso fazendo logon no Marketo Measure e seguindo as etapas abaixo para navegar até a página de informações da Data Warehouse.

1. No Marketo Measure, na parte superior da página, clique em **Minha conta** > **Configurações**.

   ![](assets/adobe-logo-old.png)

1. No menu do lado esquerdo, em Segurança, clique em **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. Nesta página, você encontrará o link para seu data warehouse do Widget e seu nome de usuário.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Essa é uma conta somente leitura disponível para sua organização, não apenas para um usuário individual. Qualquer usuário em sua organização que tenha acesso ao Marketo Measure pode usar essa conta para fazer logon na conta do leitor de Data Warehouse do Widget.

1. Clique no link fornecido no URL do Widget, isso direcionará você à página de logon do Widget, onde você digitará seu nome de usuário e senha. _Se você não tiver sua senha, consulte as etapas abaixo para redefini-la_.

   ![](assets/adobe-logo-old.png)

1. Depois de fazer logon, clique em **Planilhas** na parte superior da página.

   ![](assets/adobe-logo-old.png)

1. Os objetos do banco de dados BIZIBLE_ROI_V3 estão no lado esquerdo da tela.  Informe o Depósito, o Banco de Dados e o Esquema nas opções suspensas na parte superior da janela de consulta.  Deve haver apenas uma opção para cada um.  Agora você está pronto para executar consultas dentro do Editor de consultas do Widget.

   ![](assets/adobe-logo-old.png)

## Redefinir sua senha {#reset-your-password}

O Marketo Measure não tem acesso à sua senha de login do Widget.  Se precisar redefinir a senha, clique no botão Redefinir senha na página de informações de Data Warehouse e siga as instruções. Uma senha temporária será exibida imediatamente na interface do usuário. Você será solicitado a criar sua própria senha no próximo login do data warehouse.

>[!NOTE]
>
>* Redefinir a senha a redefine para todos os usuários da Marketo Measure em sua organização, não apenas para o usuário conectado no momento.
>* Somente mostramos a senha temporária na interface do usuário. Um email não será enviado.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Conexão com o Widget por meio de ferramentas de terceiros {#connecting-to-widget-via-third-party-tools}

Você precisará inserir algumas informações para conectar seu Data warehouse de widget a uma ferramenta de terceiros.

>[!NOTE]
>
>Cada ferramenta tem requisitos de conexão diferentes. Recomenda-se consultar a documentação da ferramenta específica que você está tentando conectar.

* **URI** (sempre obrigatório)
   * Esse é o nome de domínio da conta do Widget.  Ele está contido em uma parte do link de login do Widget.
* **Nome de usuário** (sempre obrigatório)
   * O nome de usuário está listado na página Informações da Data Warehouse no Marketo Measure.
* **Senha** (sempre obrigatório)
   * Esta é a senha que você definiu na primeira vez que fez logon na sua conta do Widget.  Para redefinir a senha, consulte as etapas descritas acima.
* **Nome do banco de dados** (nem sempre é obrigatório)
   * O banco de dados é o que armazena os dados no Widget. É o recurso de armazenamento. O nome do banco de dados está listado na página Informações da Data Warehouse no Marketo Measure.
* **Nome do Depósito** (nem sempre é obrigatório)
   * O warehouse é o que executa consultas no Widget. É o recurso de computação.  O nome do warehouse está listado na página de informações de Data Warehouse no Marketo Measure.

  ![](assets/adobe-logo-old.png)

## Compartilhamento direto da Data Warehouse do widget {#widget-data-warehouse-direct-share}

**Requisitos**

Para que o Marketo Measure configure um compartilhamento direto no data warehouse, é necessário atender aos seguintes requisitos.

* Você tem sua própria instância do Widget.
* Sua instância do Widget está localizada na região do Widget do Azure East US 2.
* Você fornece à Marketo Measure a ID da conta do Widget.

**Limitações**

Para que a Marketo Measure configure um compartilhamento direto, a conta que solicita acesso deve estar localizada no Azure East US 2. Estamos cientes de que o Widget oferece uma solução de replicação de dados entre regiões, no entanto, não oferecemos suporte a isso de nossa parte, pois hospedamos apenas dados na região do Azure East US 2. Você pode aproveitar esse recurso configurando sua própria instância no Azure East US 2 e [replicação de dados entre regiões](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} à sua instância existente. No entanto, o recurso de replicação de dados do Widget só está disponível em tabelas, portanto, para usar esse recurso, primeiro será necessário copiar os dados de nossas exibições para suas próprias tabelas.

**Acesso ao compartilhamento**

Depois que o compartilhamento for criado para a ID de conta fornecida, você deverá concluir a [etapas de configuração](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} na instância do Widget para acessar os dados.

>[!NOTE]
>
>Você pode escolher qualquer nome de banco de dados desejado. Você pode atribuir os privilégios a qualquer regra escolhida, desde que ela exista na sua instância do Widget.

* Usar a função de administrador da conta

```
USE ROLE ACCOUNTADMIN
```

* Exibir compartilhamentos disponíveis (mostrará o nome do compartilhamento concedido)

```
SHOW SHARES
```

* Criar um banco de dados para o compartilhamento

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Conceder privilégios no banco de dados compartilhado

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Para obter instruções mais detalhadas e as etapas para realizar essas etapas na interface do usuário do Widget, consulte [Documentação do widget diretamente](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
