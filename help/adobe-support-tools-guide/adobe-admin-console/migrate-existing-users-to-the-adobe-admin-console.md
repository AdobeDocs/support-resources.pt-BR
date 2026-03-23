---
title: Migrar usuários existentes para o Adobe Admin Console
description: Orientação para organizações que usam licenças de assinatura do Adobe e precisam migrar usuários existentes no Admin Console para um programa de compra ou tipo de licença diferente.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 42ab19551ba5c70712245236ffc7daf687486fb2
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# Migrar usuários existentes para o Adobe Admin Console

Aplica-se a empresas e equipes.

Este documento é para organizações com licenças existentes do Creative Cloud, Document Cloud e Acrobat por meio de uma assinatura do Enterprise Term License Agreement (ETLA) ou do Value Incentive Plan (VIP) que estão migrando para um programa de compra ou tipo de licença diferente.

>[!NOTE]
>
>Se você estiver na América do Norte e precisar de ajuda com a renovação anual do contrato do Adobe VIP com seu Gerente de conta, envie um email para **renewalhelp@adobe.com** e entraremos em contato com você em breve.

Para ajudar a evitar uma falha no acesso do usuário final ao produto, atribua licenças no Adobe Admin Console antes do término do período de assinatura existente do VIP.

* Para clientes do ETLA, aguarde pelo menos 30 dias de sobreposição do produto. Conclua a migração antes da data de aniversário para que os usuários mantenham acesso aos aplicativos e serviços da Adobe. Para obter detalhes sobre a expiração do contrato do ETLA, consulte [Estágios de expiração automatizados para contratos do ETLA](https://helpx.adobe.com/br/enterprise/using/contract-expiry.html).
* Para clientes do VIP, compre licenças antes da data de aniversário e atribua licenças antes que a janela de renovação se feche no seu termo atual do VIP.
* Os clientes do CLP ou TLP podem migrar do Acrobat ou Creative Suite serializado para licenças de usuário nomeado usando as instruções de migração no [Licenciamento](https://helpx.adobe.com/br/enterprise/using/licensing.html).

>[!NOTE]
>
>Se o tipo de licença de sua organização for alterado, os usuários finais deverão sair de qualquer produto ou serviço da Adobe e entrar novamente com as mesmas credenciais.
>
>Para produtos para desktop, como Photoshop, Acrobat e Illustrator, use as opções Sair e Fazer logon no menu Ajuda. Em Adobe.com, use o ícone no canto superior direito para sair e entrar novamente.

## Atribuição rápida de licença (VIP para VIP)

Os membros atuais da VIP que compraram o Creative Cloud para corporações ou o Acrobat (para corporações) por meio da VIP podem ser capazes de atribuir licenças rapidamente durante a janela de renovação usando a Atribuição rápida de licença. Os clientes qualificados atendem a critérios como os descritos a seguir.

* Os produtos são os mesmos

   1. A janela de renovação está aberta (30 dias antes ou depois da data de aniversário do contrato VIP).
   2. Os produtos empresariais no pedido são novos SKUs equivalentes às versões de equipe no termo atual.
   3. A quantidade da ordem de licença corporativa é maior ou igual à quantidade existente de licença de equipe.

* Os produtos têm maior valor

   1. A janela de renovação está aberta.
   2. Os produtos empresariais do pedido são novos SKUs que são produtos de maior valor do que os produtos da equipe no termo atual.
   3. A quantidade da ordem de licença corporativa é maior ou igual à quantidade existente de licença de equipe.

* A Atribuição rápida de licença não está disponível quando

   * A quantidade de licenças empresariais no pedido é inferior ao número de licenças para equipes existentes.
   * O pedido é para produtos corporativos de valor mais alto, mas a quantidade solicitada da licença corporativa é inferior à quantidade existente da licença da equipe.
   * O pedido combina produtos de equipes e corporativas, independentemente da quantidade.
   * O cliente já comprou produtos de equipe e corporativos antes do período de renovação.
   * As SKUs de renovação de empresa são usadas para o novo pedido de empresa.
   * O pedido de produtos empresariais é para um número de contrato VIP diferente.
   * Os produtos da equipe atual incluem itens que não têm versões corporativas.

Depois que a Adobe processar seu pedido de compra da empresa, você receberá um email de confirmação com instruções, incluindo o dia em que deverá transferir os usuários das licenças de equipe para as licenças da empresa na Admin Console antes que eles percam o acesso.

No Admin Console, você é solicitado a atribuir licenças usando a Atribuição rápida de licença:

1. Confirme o número de licenças para atribuição.

   ![Transferir licenças](assets/migrate-transfer-licenses.png)

2. Confirme se as licenças de produto de equipe que estão sendo desatribuídas correspondem às licenças corporativas que estão sendo atribuídas.

3. Você recebe um email quando o processo é concluído.

   ![Confirmação de atribuição de licença](assets/migrate-license-assignment.png)

Baixe o [relatório de resultados](https://helpx.adobe.com/br/enterprise/using/users.html#main-pars_header_1346350355) na Admin Console para confirmar se todas as licenças foram atribuídas. Se você terminar antes da data no email de confirmação, os usuários finais não devem enfrentar uma falha no serviço.

Agende uma chamada de integração do :1 com um especialista em integração da Adobe (se ainda não tiver) para saber mais sobre a Admin Console, incluindo as [Funções administrativas](https://helpx.adobe.com/br/enterprise/using/admin-roles.html) e a [Identidade](https://helpx.adobe.com/br/enterprise/using/identity.html).

>[!NOTE]
>
>A Atribuição rápida de licença não migra usuários com convites pendentes no Team Admin Console.

## Atribuição de licença em massa (VIP para VIP)

Atribua licenças com uma operação em massa usando um modelo CSV do [!DNL Admin Console]. Use esta abordagem quando:

* Você é um cliente do VIP que não atende aos requisitos da Atribuição rápida de licenças ou
* Você precisa atribuir licenças fora da janela de renovação.

1. Após ter acesso ao [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) e adicionar suas licenças, vá para **[!UICONTROL Usuários]** > **[!UICONTROL Usuários]**.
2. Clique no ![menu de opções de Mais](assets/migrate-more-options.png) no canto superior direito da página **[!UICONTROL Usuários]** e escolha **[!UICONTROL Editar Detalhes do Usuário por CSV]**.
3. Na caixa de diálogo **[!UICONTROL Editar Usuários por CSV]**, clique em **[!UICONTROL Baixar modelo de CSV]** e escolha **[!UICONTROL Lista de usuários atuais]**.

   ![Editar usuários por CSV](assets/migrate-edit-users-by-csv.png)

   Para obter descrições dos campos no arquivo baixado, consulte [formato de arquivo CSV](https://helpx.adobe.com/br/enterprise/using/users.html#main-pars_header).
4. Adicione atribuições de licença ao CSV, arraste o arquivo atualizado para a caixa de diálogo **[!UICONTROL Editar Usuários por CSV]** e clique em **[!UICONTROL Carregar]**. Você recebe um email quando a operação é concluída.

   ![Edição de usuário concluída](assets/migrate-user-edit-complete.png)

Baixe o [relatório de resultados](https://helpx.adobe.com/br/enterprise/using/users.html#main-pars_header_1346350355) para validar atribuições. Em seguida, agende a integração com um especialista em integração da Adobe para saber mais sobre [funções administrativas](https://helpx.adobe.com/br/enterprise/using/admin-roles.html) e [identidade](https://helpx.adobe.com/br/enterprise/using/identity.html).

## Atribuição de licença em massa (VIP para ETLA)

Se você tiver uma assinatura do VIP e estiver movendo usuários para o ETLA, use este fluxo em massa:

1. Faça logon no [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) e abra a organização que contém seus usuários do VIP.
2. Vá para **[!UICONTROL Usuários]** > **[!UICONTROL Usuários]**.
3. Clique no ![menu de opções](assets/migrate-more-options.png) no canto superior direito e escolha **[!UICONTROL Exportar lista de usuários para CSV]**.
4. Abra a organização da ETLA onde deseja esses usuários.
5. Vá para **[!UICONTROL Usuários]** > **[!UICONTROL Usuários]**.
6. Clique em **[!UICONTROL Adicionar usuários por CSV]**.
7. Clique em **[!UICONTROL Baixar modelo CSV]** e adicione os usuários do VIP do CSV exportado na etapa 3.
8. Carregue o CSV atualizado.

Você recebe um email quando os usuários são adicionados à organização da ETLA.

![Usuários adicionados após a migração do VIP para o ETLA](assets/migrate-users-added-vip-etla.png)

Baixe o [relatório de resultados](https://helpx.adobe.com/br/enterprise/using/users.html#main-pars_header_1346350355) para validar atribuições. Agende a integração com um especialista em integração da Adobe para [funções administrativas](https://helpx.adobe.com/br/enterprise/using/admin-roles.html) e [identidade](https://helpx.adobe.com/br/enterprise/using/identity.html).

Para problemas de carregamento em massa, consulte [Solucionar problemas de carregamento de usuário em massa](https://helpx.adobe.com/br/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).

## Atribuição de licença em massa (ETLA para VIP)

Se você tiver uma assinatura do ETLA e estiver movendo usuários para o VIP:

1. Faça logon no [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) e abra a organização que contém seus usuários do ETLA.
2. Vá para **[!UICONTROL Usuários]** > **[!UICONTROL Usuários]**.
3. Clique no ![menu de opções](assets/migrate-more-options.png) no canto superior direito e escolha **[!UICONTROL Exportar lista de usuários para CSV]**.

   ![Exportar menu da lista de usuários](assets/migrate-export-user-list.png)

4. Abra a organização da VIP onde deseja esses usuários.
5. Vá para **[!UICONTROL Usuários]** > **[!UICONTROL Usuários]**.
6. Clique em **[!UICONTROL Adicionar usuários por CSV]**.
7. Clique em **[!UICONTROL Baixar modelo CSV]** e adicione os usuários do ETLA do CSV exportado na etapa 3.
8. Carregue o CSV atualizado.

Você recebe um email quando os usuários são adicionados à organização da VIP.

![Usuários adicionados após a migração do ETLA para o VIP](assets/migrate-users-added-etla-vip.png)

Baixe o [relatório de resultados](https://helpx.adobe.com/br/enterprise/using/users.html#main-pars_header_1346350355) para validar atribuições. Agende a integração com um especialista em integração da Adobe para [funções administrativas](https://helpx.adobe.com/br/enterprise/using/admin-roles.html) e [identidade](https://helpx.adobe.com/br/enterprise/using/identity.html).

Para problemas de carregamento em massa, consulte [Solucionar problemas de carregamento de usuário em massa](https://helpx.adobe.com/br/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).


