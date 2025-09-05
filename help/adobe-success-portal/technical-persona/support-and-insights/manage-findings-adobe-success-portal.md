---
title: 'Gerenciar descobertas no portal  [!DNL Adobe Success] '
description: Este guia explica como acessar, interpretar e atuar nas descobertas no Portal  [!DNL Adobe Success]  para ajudar você a gerenciar proativamente o desempenho do produto, a segurança e os riscos de funcionalidade.
exl-id: c787ce29-993c-498c-9e39-8a04c2eeedda
source-git-commit: b05c238726c88ae0c51f40f077192dc136c0ae59
workflow-type: ht
source-wordcount: '765'
ht-degree: 100%

---

# Gerenciar descobertas no portal [!DNL Adobe Success]

Este guia explica como acessar, interpretar e atuar nas descobertas no portal [!DNL Adobe Success] para ajudar você a gerenciar proativamente o desempenho do produto, a segurança e os riscos de funcionalidade.

A página **[!UICONTROL Descobertas]** do portal [!DNL Adobe Success] exibe os problemas ou riscos detectados na instância do produto Adobe. As descobertas incluem problemas de desempenho, segurança e funcionalidade, bem como o respectivo status e nível de risco. O monitoramento dessa página ajuda a resolver problemas antecipadamente — antes que eles afetem os ambientes.

**O que são descobertas?**

As descobertas são alertas de Suporte e insights mostrados no portal [!DNL Adobe Success]. Eles destacam possíveis problemas na configuração do produto Adobe, como desempenho lento, riscos de segurança ou configurações incorretas. Esses alertas são baseados em dados de telemetria coletados de ferramentas como APIs, [!DNL New Relic] e [!DNL Splunk].

**Como as descobertas são criadas?**

As equipes Adobe estudam regularmente os problemas e as tendências mais comuns do suporte. Com base nos insights, elas adicionam novas verificações ao sistema. Uma vez por dia, o portal [!DNL Adobe Success] verifica os dados do produto para detectar problemas como configurações incorretas, tarefas paralisadas ou qualquer item que possa causar uma interrupção do sistema. Se uma verificação encontrar algo fora do intervalo seguro (conforme definido pelas equipes de produto e suporte da Adobe), isso será exibido como uma descoberta.

**Por que as descobertas são importantes**

A análise regular das descobertas ajuda a detectar problemas antecipadamente — antes que eles afetem o sistema ou os clientes. Essa abordagem proativa melhora a estabilidade do sistema, reduz o tempo de inatividade e apoia as práticas recomendadas.

**Como corrigir descobertas**

Cada descoberta inclui recomendações e instruções claras sobre como resolver o problema, além de links para a documentação relevante, se disponível. Compartilhe as descobertas com sua equipe de TI, de engenharia ou com um parceiro da Adobe e trabalhe em colaboração para resolvê-las. A correção antecipada desses itens ajuda a evitar problemas maiores e mantém a execução ininterrupta do sistema.


## Acessar descobertas

Para visualizar os insights de um produto:

1. Navegue até **[!UICONTROL Suporte e insights]**.
1. Selecione o cartão do produto relevante. Selecione a guia **[!UICONTROL Descobertas]**.

   ![asp-support-inisghts-findings](../../assets/asp-support-inisghts-findings.png)


1. Você verá uma lista de todas as descobertas do produto selecionado.

   ![adobe-success-portal-findings](../../assets/adobe-success-portal-findings.png)

1. Aqui, você pode:

   ![adobe-success-portal-download](../../assets/adobe-success-portal-download.png)

   * Pesquisar entradas específicas.
   * Exportar a lista de descobertas selecionando **[!UICONTROL Baixar descobertas]**. Para exportar um relatório de uma descoberta, marque a caixa de seleção ao lado da descoberta relevante na coluna **[!UICONTROL Nome da descoberta]**. Se você não selecionar uma descoberta, o PDF conterá por padrão uma lista de todas as descobertas.
   * Veja os detalhes de uma descoberta, incluindo uma resolução recomendada, selecionando-a em **[!UICONTROL Nome da descoberta]**. A página Detalhes da descoberta exibe a descoberta selecionada com um contexto adicional e uma recomendação. Para ver esse relatório, selecione a seta para baixar.


     ![findings-details](../../assets/findings-details.png)


## Descobertas de ação

Siga estas etapas para validar se cada descoberta ainda é aplicável ou pode ser rejeitada.

>[!NOTE]
>
>As verificações padrão são executadas nas instâncias. Se as verificações não detectarem que o problema está presente na instância, o status será **[!UICONTROL Não detectado]**.

1. Navegue até **[!UICONTROL Suporte e insights]**.
1. Selecione o cartão do produto relevante.
1. Abra a guia **[!UICONTROL Descobertas]**.  Você verá todos das descobertas do produto selecionado.
1. Selecione uma entrada em **[!UICONTROL Nome da descoberta]**. Na página Detalhes da descoberta, é possível:
   * Selecionar **[!UICONTROL Validar]** para verificar se o problema ainda está presente (o botão **[!UICONTROL Validar]** foi criado como uma confirmação de que o problema foi resolvido):

   ![adobe-success-portal-validate](../../assets/adobe-success-portal-validate.png)


   * Se o problema persistir, a seguinte mensagem será exibida: *[!UICONTROL Validação concluída.  Descoberta ainda detectada]*. Use as informações e recomendações da página Detalhes da descoberta para investigar e resolver.
   * Se o problema não estiver mais presente, a seguinte mensagem será exibida: *[!UICONTROL Validação concluída.  Descoberta não foi mais detectada]*. Quando a descoberta não é mais detectada, ela se torna cinza e o status muda para **[!UICONTROL Não detectado]**. Descobertas com o status **[!UICONTROL Não detectado]** estão localizadas na parte inferior da lista de descobertas.
   * Se o problema não for aplicável ou relevante para você, basta descartá-lo selecionando a opção **[!UICONTROL Descartar]**. Quando a descoberta é descartada, se torna cinza e o status muda para **[!UICONTROL Descartada]**.  Descobertas com o status **[!UICONTROL Descartado]** estão localizadas na parte inferior da lista.

## Noções básicas de descobertas

* **[!UICONTROL Nome da descoberta]** – Selecione para obter informações detalhadas e etapas de resolução recomendadas.
* **[!UICONTROL Tipo]** – Categorizado como *Funcionalidade*, *Desempenho* e *Segurança*.
* **[!UICONTROL Nível de risco]** – Indicador de severidade, com indicações visuais.
* **[!UICONTROL Status]** – O estado atual da descoberta (por exemplo, *Detectado*, *Não detectado*, *Descartado*).
* **[!UICONTROL Verificar última execução]** – Carimbo de data/hora da última verificação que atualizou a descoberta.


## Práticas recomendadas

A página **[!UICONTROL Descobertas]** lista recomendações com os seguintes níveis de risco: **[!UICONTROL Alto]**, **[!UICONTROL Elevado]** e **[!UICONTROL Médio]**. **[!UICONTROL Alto]** é crítico, **[!UICONTROL Elevado]** é urgente e **[!UICONTROL Médio]** é não crítico.  Para manter a integridade e o desempenho do site:

* Resolva prontamente as descobertas de **[!UICONTROL Alto risco]**, pois representam ameaças críticas.
* Resolva logo os problemas de risco **[!UICONTROL Elevado]** para evitar o escalonamento.
* Monitore regularmente as descobertas de risco **[!UICONTROL Médio]** e atue conforme necessário.
