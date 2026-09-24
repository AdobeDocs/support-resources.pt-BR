---
title: Guia de disponibilidade de feriados unificados das soluções do Adobe CX
description: Disponibilidade do Adobe CX para férias no AEP, AJO, CJA, Commerce, AEM, Marketo, Workfront, Campaign, Analytics e Target para ajudá-lo a planejar, dimensionar, proteger e otimizar.
hold: true
feature-set: Experience Cloud
feature: Support
solution: Experience Cloud, Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
index: true
exl-id: 7a36a281-98d0-4b1f-afc5-dbcde10fddaf
product_v2:
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
  - id: e98b7246-966c-4318-9e95-cad2f7a17dc7
    internal-label: Customer Journey Analytics
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ec060fad85a22f6d55c4de3dc2d7fbf8a1ecb8c7
workflow-type: tm+mt
source-wordcount: '4677'
ht-degree: 3%
---
# Guia de disponibilidade de feriados unificados das soluções do Adobe CX

Este Guia de disponibilidade de feriado unificado das soluções Adobe CX foi atualizado com as últimas recomendações para a temporada de festas de 2026. Ele ajuda você a se preparar concentrando-se no planejamento pró-ativo em vez da solução reativa de problemas. Ele fornece etapas práticas para garantir que suas instâncias estejam prontas, minimizando possíveis problemas antes que eles surjam. A equipe da Adobe oferece experiência técnica, uma ampla variedade de recursos e métodos comprovados para fornecer o nível certo de suporte e orientação — tanto técnico quanto estratégico — para que sua empresa esteja bem preparada.

Para garantir que suas soluções de experiência do cliente da Adobe sejam resilientes, seguras e estejam prontas para picos de tráfego de feriados, siga estas práticas recomendadas:

* Planeje o aumento do tráfego.
* Evite grandes alterações durante as janelas de pico; agende atualizações antes ou depois da temporada de festas.
* Use painéis e alertas para monitorar o desempenho e detectar gargalos antecipadamente.
* Verifique se os seus contatos de suporte autorizados estão atualizados.
* [Contate o suporte da Adobe](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket){target="_blank"} com antecedência sempre que possível.

Para obter as recomendações da Adobe sobre disponibilidade para feriados específicas da solução, consulte as seções a seguir.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>Clique em cada seção para expandi-la.


## Guia de disponibilidade de feriados do Adobe Experience Platform (AEP) {#aep}

+++**Clique para ver as recomendações de disponibilidade para feriados do Adobe Experience Platform (AEP).**

O Adobe Experience Platform (AEP) desempenha um papel essencial para potencializar as experiências do cliente em tempo real. Conforme a temporada de festas se aproxima, é essencial garantir que a implementação do AEP seja otimizada para aumentar o tráfego, o manuseio seguro de dados e a assimilação escalável.

### Prever demanda sazonal

Para se preparar para picos de tráfego sazonais, a Adobe recomenda o planejamento da capacidade e o monitoramento da assimilação do perfil de transmissão. Isso inclui prever volumes de dados e garantir que seu sistema possa lidar com o aumento da taxa de transferência. Consulte [Plano de capacidade e tráfego sazonal](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile#plan-for-capacity-and-seasonal-traffic){target="_blank"} para referência.

### Preparar-se para a escala

O Adobe fornece várias estratégias para garantir que seu ambiente esteja pronto para o tráfego de feriados:

* Aumentar a capacidade alocada para sandboxes.
* Identifique fluxos de dados de alta taxa de transferência no [painel de monitoramento](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile){target="_blank"} e aplique limitação ou filtragem onde necessário.
* Use a assimilação em lote para casos de uso de latência mais baixa a fim de otimizar o desempenho, conforme descrito em [Uso e capacidades da licença: Práticas recomendadas de taxa de transferência de streaming](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#plan-and-schedule-streaming-and-edge-capacity){target="_blank"}.

Essas práticas ajudam a manter a confiabilidade da assimilação e reduzem a latência durante períodos de pico.

### Práticas recomendadas e medidas de proteção

Para ficar dentro dos limites operacionais e evitar interrupções do serviço, a Adobe recomenda as seguintes medidas de proteção de assimilação e perfil:

* [Práticas recomendadas de taxa de transferência de transmissão](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity){target="_blank"}
* [Medidas de proteção para a assimilação de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/guardrails){target="_blank"}
* [Medidas de proteção padrão para dados e segmentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"}
* [Blueprints da AEP: Medidas de Proteção](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-overview/guardrails){target="_blank"}

### Segurança e governança

A Adobe enfatiza as fortes práticas de segurança e governança, especialmente durante temporadas de alto tráfego, quando a sensibilidade dos dados é aumentada.

Consulte [Governança, privacidade e segurança no Adobe Experience Platform: Segurança](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/overview#security){target="_blank"} para obter recomendações sobre como proteger os dados do cliente, aplicar controles de privacidade e manter a conformidade na implementação do AEP.

Seguindo essas diretrizes e aproveitando a documentação pública da Adobe, as organizações podem garantir que seus Adobe Experience Platform sejam resilientes, seguros e prontos para fornecer experiências excepcionais ao cliente durante toda a temporada de festas.

+++

## Guia de disponibilidade de feriados do Adobe Journey Optimizer (AJO) {#ajo}

+++**Clique para ver as recomendações de disponibilidade para feriados do Adobe Journey Optimizer (AJO).**


Para preparar o Adobe Journey Optimizer para a temporada de festas, as organizações devem antecipar picos de eventos e complexidade entre canais, configurar regras de jornada e frequência e garantir a higiene de dados e a lógica de decisão. Eles também devem validar o desempenho em escala, aplicar medidas de proteção de segurança e API e aplicar insights pós-pico para refinar campanhas futuras.

### Prever demanda

* Com base nas compressões da temporada de festas e no maior volume de campanha, espere:
  * Um pico em eventos em tempo real e jornadas acionadas (abandono de carrinho, ofertas de última hora)
  * Riscos de saturação de mensagens (opções de não participação mais altas, fadiga)
  * Maior complexidade entre canais (email + push + SMS + no aplicativo)
* Use as métricas do ano passado (taxas de abertura/clique/recusa, volumes de entrada de jornada) para modelar as cargas esperadas e definir limites para seus sistemas de mensagens.
* Identifique &quot;janelas tranquilas&quot; prováveis ou períodos de baixo desempenho (por exemplo: fins de semana, feriados) e planeje os volumes de envio de acordo.

### Preparar-se para a escala

* Verifique se todas as configurações de canal no AJO estão definidas corretamente: email, push, SMS, Web e no aplicativo. Consulte [Configurar canais](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces){target="_blank"}.
* Configure regras de limite e limite de frequência para controlar volumes de mensagens. Consulte o artigo [Limite de frequência](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules){target="_blank"}.
* Configurar conjuntos de regras de canal/jornada: Consulte [Trabalhar com conjuntos de regras](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets){target="_blank"}.
* Prepare sua higiene de dados / fluxos de eventos em tempo real e estruturas de segmentação.
* Verifique se você definiu públicos-alvo para campanhas de fim de ano, como:
  * clientes de alto valor
  * segmentos fiéis
  * abandonadores de carrinho
  * compradores pela primeira vez
* Pré-carregar ou preparar modelos para jornadas de feriados, aproveitar a lógica de decisão (ofertas/restrições) para que você possa se adaptar dinamicamente com base no inventário, nas ofertas sensíveis ao tempo e na preferência de canal. Consulte o exemplo no artigo [Adicionar restrições a uma oferta](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints){target="_blank"}.
* Disponibilidade técnica: confirme a capacidade de carregamento da API/endpoint, as regras de limitação/limitação para ações personalizadas e integrações externas. Consulte [Medidas de proteção e limitações](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/guardrails){target="_blank"}.

### Teste e validação

* Use sua estrutura de experimentação para testar as principais alterações de variáveis:
  * hora de envio
  * tipo de oferta
  * mix de canais
    Consulte as [práticas recomendadas da AJO Experimentation Accelerator](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices){target="_blank"}.
* Realizar validação completa da jornada:
  * disparadores de eventos
  * entrada de segmentação
  * Fluxos de caminho de jornada
  * lógica de personalização
  * restrições de oferta
  * critérios de saída
* Verifique as regras de limite e conflito. Consulte o artigo [Limite de Jornada e arbitragem](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/journey-capping){target="_blank"}.
* Volumes dimensionados para testes de estresse para envios ou picos de pico: simule volumes de acionador altos para validar o comportamento do sistema sob carga.
* Validar a capacidade de entrega: aquecer domínios/remetentes de email, confirmar configurações de push móveis e verificar canais de fallback para SMS/no aplicativo.

### Práticas recomendadas

* Use a orquestração omnicanal. Consulte o artigo do blog [jornadas essenciais de clientes omnicanal para engajamento e crescimento](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement){target="_blank"} que mostra um exemplo de temporada de festas com a AJO.
* Priorize acionadores em tempo real quando apropriado. Por exemplo: abandono de carrinho, abandono de navegação e alertas de estoque, já que os compradores de feriados são mais reativos.
* Aproveite a segmentação e personalização: segmente segmentos de alta intenção, adapte ofertas com base no comportamento de compras anteriores e preferências.
* Fadiga mínima das mensagens: aplique limites e horas de silêncio para evitar solicitações excessivas. Consulte a publicação do blog [Aumentar a experiência do cliente com limite diário de frequência no AJO](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510){target="_blank"}.
* Importância do tempo: o plano envia anteriormente na janela do feriado (dada a estação compactada) e alinha os canais aos fusos horários e ao comportamento do público local.
* Ofereça ofertas dinâmicas/por tempo limitado para criar urgência, mas coordene entre canais para evitar duplicação e conflito.
* Usar lógica de supressão: suprima públicos que acabaram de comprar ou aplique jornadas pós-compra para evitar mensagens redundantes.

### Segurança e governança

* Verifique se o controle de acesso e as permissões estão configurados para que somente os usuários necessários possam implantar jornadas ou modificar regras de negócios.
* Monitorar e impor o limite de chamada/conexão de API: Por exemplo, consulte a [API de Limite Artigo sobre Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/connect-systems/external-systems/capping){target="_blank"}.
* Use dados primários limpos e garanta a identificação adequada da identidade para que as mensagens sejam centradas no cliente e não duplicadas/desalinhadas.
* Verifique se os domínios de deliverability estão aquecidos e se as medidas antisspam estão em vigor, especialmente para envios de feriados de alto volume.
* Revise logs de auditoria e alterações de jornada com frequência durante a temporada de pico para detectar jornadas mal executadas ou errantes antecipadamente.

### Aprendizados pós-pico

* Após os picos de carga, faça uma análise das contagens de entrada de jornada, das contagens de supressão, das taxas de recusa, das métricas de capacidade de entrega e do desempenho do canal.
* Limpe os segmentos suprimidos e pause ou desative as jornadas criadas para a janela do feriado a fim de evitar a fadiga de transporte.
* Use insights de desempenho em tempo real para refinar o planejamento do próximo ano (por exemplo: ajustes de hora de envio, combinação de canais e volume de mensagens).

Prevendo de forma proativa a demanda sazonal, configurando canais e regras, validando o desempenho da jornada e reforçando a segurança e o controle, as organizações podem garantir que a Adobe Journey Optimizer ofereça experiências do cliente perfeitas, personalizadas e resilientes durante esse período de festas e muito além.

+++

## Guia de disponibilidade de feriados do Customer Journey Analytics (CJA) {#cja}

+++**Clique para ver as recomendações de disponibilidade para feriados do Customer Journey Analytics (CJA).**

A Customer Journey Analytics usa os 5 PCs para atingir a prontidão para feriados/épocas de pico.

### Preparar-se para a escala

* Analise as conexões e visualizações de dados do CJA; estabeleça quais conexões e visualizações de dados exigem monitoramento e provisionamento aprimorados.
* Confirme se o provisionamento é suficiente para a escala de feriados; faça upscaling das Conexões críticas e das Visualizações de dados conforme necessário. Consulte [Gerenciar conexões](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/manage-connections){target="_blank"} para obter mais informações.

### Monitorar o desempenho

* Aproveite a RAM ([[!UICONTROL Visão geral do Gerenciador de Atividades de Relatórios]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) para monitorar solicitações de relatórios ativas e enfileiradas em tempo real, identificar conexões com capacidade total e identificar gargalos.
* Fique atento a maior latência durante o pico de carga usando os artigos [Guia de Solução de Erros](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages){target="_blank"} e [Limitações Conhecidas](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations){target="_blank"}.
* Permita que os administradores suspendam ou cancelem solicitações de longa duração/bloqueadas preventivamente via RAM. Consulte o artigo [Cancelar solicitações de relatórios no CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests){target="_blank"}.

### Práticas recomendadas

* Agendar exportações/relatórios durante períodos de tráfego baixo para suavizar a carga e minimizar a latência. Consulte o artigo [Relatórios agendados](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/scheduled-projects-manager){target="_blank"}.
* Distribuir solicitações: programe relatórios em diferentes intervalos ao longo do dia.
* Reduza painéis, simplifique segmentos, reduza intervalos de datas e evite o excesso de trabalhos simultâneos. Consulte o artigo [Otimização do desempenho do CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance){target="_blank"} para obter detalhes.

### Solução de problemas

* Ao solucionar erros de espaço de trabalho, consulte as mensagens de erro para a causa e as ações recomendadas; use a RAM ([!UICONTROL Gerenciador de Atividades de Relatórios]) para eliminar gargalos e gerenciar a simultaneidade de maneira eficiente. Consulte [Tratamento de erros do CJA Workspace](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages){target="_blank"} para obter mais detalhes.
* Use a RAM ([[!UICONTROL Gerenciador de Atividades de Relatórios] no CJA](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) para apontar usuários, consultas ou projetos problemáticos; priorize e encerre/cancele conforme necessário.

### Aprendizados pós-pico

* Após o feriado/período de pico, analise os registros de desempenho e incidentes para avaliar o impacto das práticas recomendadas fornecidas.
* Revise consultas lentas e tarefas do usuário para identificar padrões/tendências que podem ser otimizados para a próxima temporada.
* Colete feedback dos usuários e das partes interessadas — atualize seus próprios runbooks e planos de disponibilidade usando insights recém-obtidos.
* Forneça feedback às equipes da Adobe por meio da equipe de conta.

+++

## Guia de preparação para feriados do Adobe Commerce {#commerce}

+++**Clique para ver as recomendações de preparação para feriados do Adobe Commerce.**

Para garantir uma temporada de pico bem-sucedida para sua organização, é essencial preparar sua loja digital Adobe Commerce para tráfego alto.

### Prever demanda

* Durante o período de pico de vendas de feriados (de meados de novembro a meados de janeiro), a Adobe recomenda que todos os comerciantes do Adobe Commerce hospedados em nossa infraestrutura em nuvem planejem proativamente um aumento nos visitantes enviando solicitações de aumento de capacidade de feriados. Consulte [Solicitações de capacidade de aumento temporário de férias do Adobe Commerce em nossa infraestrutura em nuvem](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud){target="_blank"} para obter detalhes.

### Preparar-se para a escala

Siga as recomendações no [Planejamento e tabela dinâmica: uma abordagem estratégica para a temporada de pico de 2025](https://experienceleague.adobe.com/en/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025){target="_blank"} guia, que fornece estratégias acionáveis usando o Adobe Commerce (e ferramentas opcionais da Adobe Experience Cloud) para ajudar você a planejar, girar e fornecer experiências excepcionais para o cliente durante o período mais movimentado do ano.

### Práticas recomendadas

* Siga o guia da Adobe [Como preparar sua infraestrutura para tráfego alto — os 5 pontos de desempenho da temporada de pico](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic){target="_blank"}.
* Confira as [Dicas técnicas para a preparação para feriados da Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness){target="_blank"} para obter dicas sobre como preparar sua infraestrutura para tráfego intenso, evitar tempo de inatividade e otimizar o desempenho no período de feriados.

+++

## Guia de disponibilidade de feriados do Adobe Experience Manager (AEM) {#aem}

+++**Clique para ver as recomendações de disponibilidade para feriados do Adobe Experience Manager (AEM).**

A temporada de festas está se aproximando rapidamente e, para muitos clientes da Adobe, isso significa o início dos períodos de pico de vendas. Em nosso compromisso com seu sucesso, queremos garantir que você esteja totalmente preparado para o aumento futuro do tráfego.

### Serviços em nuvem do Adobe Experience Manager (AEM)

Se a sua organização passar pelos momentos mais movimentados durante a temporada de festas, talvez você esteja pensando em como otimizar o site do Adobe Experience Manager para acomodar o pico de tráfego. Felizmente, os Serviços em nuvem da Adobe Experience Manager equipam seu site para dimensionamento automático, garantindo uma experiência contínua para seus visitantes, apesar das alterações repentinas no tráfego.

#### Preparar-se para a escala

* Para obter insights e orientações detalhadas sobre como se preparar para alto tráfego com os Serviços em nuvem da Adobe Experience Manager, consulte os seguintes links:

  * [CDN no AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn){target="_blank"}
  * [Cache do AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/caching/overview){target="_blank"}

* Se você for cliente do Ultimate Success e tiver compartilhado recentemente as informações de previsão de volume com a sua equipe de conta da Adobe, não se preocupe em enviá-las novamente, pois já temos uma visualização.

Estamos aqui para apoiá-lo em todas as etapas da sua jornada. Caso tenha dúvidas ou dúvidas, sinta-se à vontade para [enviar um tíquete de suporte](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket){target="_blank"}.

Para se preparar para uma campanha de marketing na temporada de festas, consulte o [Guia do usuário do AEMaaCS: Introdução - Documentação dos parâmetros da campanha de marketing](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters){target="_blank"}.

#### Segurança e governança

Para obter informações sobre a segurança/proteção do tráfego do site da AEM, consulte o artigo [Visão geral - Protegendo sites da AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview){target="_blank"} nos Tutoriais da AEM as a Cloud Service.

#### Planejamento de manutenção de feriados

A Adobe programou períodos de exclusão de manutenção para garantir serviço ininterrupto durante períodos de feriado críticos:

* **Nenhuma manutenção automática do AEMaaCS** ocorre durante os seguintes períodos de tempo, começando e terminando à meia-noite (00:00) CET:
  * de segunda-feira, 23 de novembro de 2026 até terça-feira, 1 de dezembro de 2026.
  * Segunda-feira, 14 de dezembro de 2026 até domingo, 3 de janeiro de 2027.

Isso garante a estabilidade durante períodos de alto tráfego. Para obter cronogramas de lançamento completos e janelas de manutenção, consulte o [roteiro de versões do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap){target="_blank"}.


### Adobe Experience Manager (AEM) com Adobe Managed Services (AMS)

Os clientes da AEM que usam o Adobe Managed Services podem trabalhar proativamente com seus CSEs para planejar as necessidades de cobertura dos feriados.

+++

## Guia de disponibilidade de feriados do Adobe Marketo {#marketo}

+++**Clique para ver as recomendações de preparação para feriados do Adobe Marketo.**

Para garantir campanhas de fim de ano bem-sucedidas com o Adobe Marketo, as equipes devem verificar as configurações de autenticação de email, limpar e proteger o banco de dados, otimizar a lógica e o agendamento da campanha, testar detalhadamente a renderização e o delivery de email e simplificar a preparação do suporte para o máximo de desempenho e engajamento.

### Preparar-se para a escala

* Verifique as configurações de SPF/DKIM e certifique-se de que tudo ainda esteja configurado e funcionando corretamente. Consulte o artigo [Configurar SPF e DKIM para a capacidade de entrega de emails](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability){target="_blank"} para obter detalhes.
* Faça auditoria e limpe o banco de dados do Marketo limpando registros inativos/inválidos. Isso aumenta a probabilidade de o enviar terras nas caixas de entrada dos leads mais prontos para vendas. Consulte o artigo [Verificação de integridade do banco de dados do Marketo e como mantê-lo limpo](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563){target="_blank"} para obter detalhes.
* Confirme se os membros da equipe têm as permissões certas para executar tarefas e impedir acesso não intencional ou alterações nos emails. Esteja você fazendo alterações por meio do **[!UICONTROL Administrador]** ou do **[!UICONTROL Admin Console]**, nós o protegemos. Consulte o artigo [Gerenciando Permissões e Funções de Usuário](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"}.
* Revise suas integrações do Launchpad para garantir a autenticação correta e resolver possíveis erros antes de serem usadas. Consulte o artigo [Guia do desenvolvedor do Marketo: Autenticação](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication){target="_blank"}.

### Práticas recomendadas

A eficiência começa com a compreensão exata de como o Marketo prioriza e processa campanhas. Dê às suas campanhas o dom da velocidade com essas dicas de otimização.

* Entender como o Marketo prioriza o processamento das etapas do fluxo de campanha é fundamental para evitar o atraso inadvertido de qualquer email urgente ou de alta prioridade. Consulte o artigo [Como funciona o processamento da campanha](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Considere a lógica da lista inteligente e ajude a garantir que suas campanhas sejam executadas rapidamente e com desempenho máximo. Consulte o artigo [Práticas recomendadas para Smart Lists](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists){target="_blank"}.
* O **[!UICONTROL Head Start]** ou o **[!UICONTROL Fuso horário do destinatário]** pode começar a criar emails antes do envio, reduzindo atrasos e fornecendo tempo de preparação adicional para qualificar clientes potenciais com lógica de alto recurso. Para obter detalhes, consulte os artigos [Head Start para Programas de Email](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs){target="_blank"} e [Agendar Programas de Email com Fuso Horário do Destinatário](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone){target="_blank"}.
* Sua campanha está ativa, e os leads estão fluindo, e você percebe um erro com a etapa de fluxo. É tentador corrigir com um ajuste rápido, mas estar ciente do que acontece quando você altera uma etapa de espera ao vivo ou reordena seus fluxos pode ajudá-lo a evitar muitas dores de cabeça e limpar mais tarde. Consulte o artigo [Editando o Fluxo da Campanha com Membros em Etapas de Espera](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

### Teste e validação

Antes de clicar em **[!UICONTROL Enviar]**, verifique se os seus emails têm a aparência e o desempenho esperados.

* O Marketo oferece várias maneiras de testar a aparência de um email. Use-os para garantir que fique exatamente com a aparência que você imaginou.
  * Use a função **[!UICONTROL Visualizar]** para garantir que o conteúdo dinâmico e os tokens sejam renderizados corretamente ao visualizar por segmentação ou leads individuais. Consulte o artigo [Visualizar um email com conteúdo dinâmico](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content){target="_blank"}.
  * Envie um email direto para seus registros de teste de forma rápida e fácil para ver como seu email aparece em diferentes clientes/dispositivos. Consulte o artigo [Executar uma única etapa de fluxo de uma lista inteligente](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list){target="_blank"}.
  * Para [!DNL Litmus] usuários, agora está mais fácil do que nunca integrar sua conta e iniciar testes de renderização diretamente do editor de email. Consulte o artigo [Testar renderização de email [!DNL Litmus]](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering).
* Confira o recurso Relatório de spam por email, que se integra ao [!DNL SpamAssassin] para revisar o conteúdo do seu email e atribuir uma pontuação sobre a probabilidade de ele chegar à caixa de entrada ou ser marcado como *spam*. Consulte o artigo [Relatório de spam por email](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report){target="_blank"}.
* Fique de olho na [!UICONTROL Fila de campanha] para verificar se suas campanhas estão processando e priorizando itens de alta urgência corretamente. Consulte [Minha campanha está em execução?](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662){target="_blank"} artigo.

### Simplifique sua experiência de suporte

Quando algo dá errado, a velocidade é importante e o Suporte da Marketo está aqui para ajudar. Inclua esses detalhes em seu caso de suporte para evitar problemas e ajudar nossa equipe a trabalhar para uma resolução mais rápida. Consulte o artigo [Práticas recomendadas para trabalhar com o suporte da Marketo](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491).

Com este guia, você pode ficar um pouco mais tranquilo sabendo que está começando de uma posição forte para impulsionar engajamento e conversões durante essa janela crítica. O que está em jogo é alto, mas o seu estresse não precisa ser. Comece seus preparativos hoje e faça desta temporada de festas a sua mais bem sucedida ainda.

+++

## Guia de preparação para feriados do Adobe Workfront {#workfront}

+++**Clique para ver as recomendações de preparação para feriados do Adobe Workfront.**

Para preparar o Adobe Workfront para a temporada de festas, atualize os contatos de suporte, alinhe as programações internas com o Adobe, evite grandes alterações durante os horários de pico e monitore de forma proativa as automações e integrações para garantir operações tranquilas.

### Preparar-se para a escala

Para ajudar a garantir uma experiência de suporte tranquila durante os feriados:

* Revise e atualize seus contatos de suporte autorizados com antecedência.
* Confirmar se os principais interessados estão disponíveis para colaborar com o suporte se surgirem problemas críticos.
* Se o produto ou workflow do planejamento for alterado durante a janela do feriado, considere programá-los antes de meados de novembro ou depois do início de janeiro para obter melhores tempos de resposta.
* Comunique as programações de feriados internas aos contatos do Adobe para garantir o alinhamento.

### Teste e validação

Mantenha-se informado sobre os lançamentos do Workfront e teste novos recursos em ambientes de sandbox:

* [Preparação para uma versão do Adobe Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-readiness){target="_blank"}
* [Arquivo de notas de versão do Workfront](https://experienceleague.adobe.com/pt-br/docs/workfront/using/product-announcements/product-releases/product-releases){target="_blank"}

### Práticas recomendadas

* Planejamento Pró-ativo: Identifique quaisquer dependências do sistema ou automações programadas que possam ser afetadas por programações de folga internas.
* Comunicação contínua: mantenha suas equipes internas e o suporte da Adobe informados sobre manutenção planejada ou eventos importantes.
* Use painéis: monitore as principais integrações e automatizações para capturar sinais antecipados de problemas de desempenho.
* Escalonar com antecedência: se você antecipar ou observar a degradação do serviço, abra um tíquete de suporte imediatamente — não espere até que ele se torne crítico.

Ao planejar com antecedência, manter uma comunicação clara e encaminhar os problemas antecipadamente, as organizações podem minimizar as interrupções e garantir que a Workfront continue a oferecer suporte a fluxos de trabalho críticos durante todo o período do feriado.

+++

## Guia de preparação para feriados do Adobe Campaign {#campaign}

+++**Clique para ver as recomendações de preparação para feriados do Adobe Campaign.**


Para preparar o Adobe Campaign para as férias, valide proativamente as configurações de capacidade de entrega, otimize a segmentação de público e a frequência de mensagens, garanta a escalabilidade da infraestrutura e teste a orquestração de campanhas entre canais para lidar com picos sazonais de volume e engajamento de maneira eficaz.

Consulte a documentação a seguir para obter mais detalhes.

**Para o Adobe Campaign v8 e o Adobe Campaign Classic v7:**

* [Aprimorando a capacidade de entrega](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/send/deliverability-management/about-deliverability){target="_blank"}
* [Práticas recomendadas de fluxo de trabalho](https://experienceleague.adobe.com/en/docs/campaign/automation/workflows/introduction/workflow-best-practices){target="_blank"}

**Para Adobe Campaign Standard:**

* [Aprimoramento da capacidade de entrega](https://experienceleague.adobe.com/en/docs/campaign-standard/using/testing-and-sending/managing-deliverability/about-deliverability){target="_blank"}
* [Práticas recomendadas de fluxo de trabalho](https://experienceleague.adobe.com/en/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows){target="_blank"}

**Práticas recomendadas gerais de entrega:**

* [Manual de práticas recomendadas para a entrega](https://experienceleague.adobe.com/pt-br/docs/deliverability-learn/deliverability-best-practice-guide/introduction){target="_blank"}

+++

## Guia de preparação para feriados do Adobe Analytics {#analytics}

+++**Clique para ver as recomendações de preparação para feriados do Adobe Analytics.**

À medida que a temporada de festas se aproxima, as organizações que usam o Adobe Analytics devem tomar medidas proativas para garantir a precisão dos dados, o desempenho da plataforma e a confiabilidade dos relatórios durante os períodos de pico de tráfego. A Adobe fornece vários recursos e práticas recomendadas para ajudar as equipes a se prepararem de maneira eficaz.

### Prever tráfego

Para garantir alocação adequada de hardware e capacidade de resposta do sistema, a Adobe recomenda enviar com antecedência os **volumes de ocorrências/chamadas diárias e por hora do servidor**.

* Verifique [O planejamento de pico de tráfego e os prazos de entrega para alocação de hardware](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times){target="_blank"}, já que entender a rapidez com que os dados são disponibilizados é essencial para a tomada de decisões em tempo real durante períodos de alto volume.

* Saiba o que afeta a disponibilidade e a latência de dados no Adobe Analytics em [visão geral da latência de dados do Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/technotes/latency){target="_blank"}, incluindo picos inesperados de tráfego e problemas de hardware, e descubra estratégias recomendadas para reduzir atrasos de dados.

### Práticas recomendadas

Para as equipes que usam feeds de dados para exportar dados brutos de análise, o Adobe fornece orientação sobre como otimizar as configurações do feed e evitar armadilhas comuns.

* [Práticas recomendadas para feeds de dados do Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feeds-best-practices){target="_blank"}

Para manter relatórios rápidos e confiáveis durante os feriados, a Adobe recomenda:

* [Otimização do desempenho do Analysis Workspace](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance){target="_blank"}
* [Resolução de problemas e práticas recomendadas do Report Builder: recomendações para solicitações de otimização](https://experienceleague.adobe.com/en/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F){target="_blank"}
* [Guia de componentes do Analytics: fila de relatórios agendados](https://experienceleague.adobe.com/en/docs/analytics/components/scheduled-reports-admin){target="_blank"}

### Planejamento de manutenção de feriados

A Adobe normalmente impõe **janelas de exclusão de manutenção** durante períodos de pico de feriados para garantir serviço ininterrupto. Monitore os cronogramas de lançamento e manutenção da Adobe por meio da Experience League e coordene com as equipes de conta da Adobe para planejar o suporte.

Seguindo essas diretrizes e aproveitando a documentação pública da Adobe, as organizações podem garantir que sua implementação do Adobe Analytics seja robusta, responsiva e esteja pronta para as demandas da temporada de festas.

+++

## Guia de preparação para feriados do Adobe Target {#target}

+++**Clique para ver as recomendações de preparação para feriados do Adobe Target.**

A temporada de festas traz excelentes oportunidades de envolvimento, mas também apresenta desafios como picos de tráfego e maior demanda de sistemas de personalização. Para ajudá-lo a fornecer experiências perfeitas durante esse período crítico, compilamos as principais recomendações para garantir que sua implementação do Adobe Target esteja pronta.

### Prever demanda

Comece antecipando picos de tráfego de 20 a 50% ou mais e validando se sua infraestrutura pode lidar com a carga. Preveja a atividade e os volumes de dados no Adobe Target, Analytics e AEP para evitar surpresas.

Também é importante identificar jornadas essenciais, como check-out, recomendações de produtos e ofertas promocionais, para que os esforços de personalização se concentrem onde são mais importantes.

Consulte [Práticas recomendadas para otimização com o Adobe Target](https://experienceleague.adobe.com/en/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization){target="_blank"}.

### Preparar-se para a escala

* Planeje o aumento do tráfego no site e nos dispositivos móveis e informe a equipe de suporte do Target para aumentar a capacidade do servidor e evitar chamadas bloqueadas.
* Para qualquer teste de carga/caneta, a equipe de suporte do Target deve ser informada com antecedência.
* Atualize para as versões mais recentes da API de entrega/`at.js`.
* Congelar alterações não críticas; preparar para experiências de fallback.
* Alinhe os processos de suporte e escalonamento e ative os alertas proativos.

### Teste e validação

Valide a entrega de conteúdo usando os [links de controle de qualidade](https://experienceleague.adobe.com/en/docs/target/using/activities/activity-qa/activity-qa){target="_blank"} para confirmar se tudo funciona conforme o esperado. Use as **[!UICONTROL Regras de correspondência de público-alvo para ver as experiências]** para garantir que o público-alvo correto se qualifique para a atividade que você está testando. Verifique se a sua configuração de **[!UICONTROL Métrica de meta]** está alinhada ao **[!UICONTROL Objetivo]** da atividade. E sempre tenha um plano de backup pronto — por via das dúvidas.

### Práticas recomendadas

Mantenha sua implementação dentro dos [limites do Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/troubleshoot/target-limits){target="_blank"} e verifique antecipadamente a [conformidade com o GDPR e a CCPA](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation){target="_blank"} antes de iniciá-la. Mantenha menos de 100 atividades ativas e arquive as mais antigas para simplificar as coisas. Aproveite a **[!UICONTROL Alocação automática]**/**[!UICONTROL Direcionamento automático]** para otimização orientada por IA. Estabeleça planos de reversão e painéis de monitoramento em tempo real.

### Segurança e governança

Antes de personalizar as experiências, confirme a conformidade com o consentimento de acordo com o GDPR e a CCPA. Evite armazenar informações de identificação pessoal (PII) em parâmetros de perfil e valide a segurança da API para proteger os dados do cliente.

+++
