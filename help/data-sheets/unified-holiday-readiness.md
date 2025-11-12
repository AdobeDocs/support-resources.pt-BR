---
title: Guia de prontidão para férias unificado das soluções Adobe DX
description: Este artigo fornece um guia de preparação para férias das soluções DX.
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
source-git-commit: b4b75c2c32f6265ce3fbac9f3bed888e08956982
workflow-type: tm+mt
source-wordcount: '3815'
ht-degree: 1%

---

# Guia de prontidão para férias unificado das soluções Adobe DX


O Guia de disponibilidade de feriado unificado das soluções Adobe DX ajuda você a se preparar para a temporada de festas, concentrando-se no planejamento pró-ativo em vez da solução reativa de problemas. Ele fornece etapas práticas para garantir que suas instâncias estejam prontas, minimizando possíveis problemas antes que eles surjam. A equipe da Adobe oferece experiência técnica, uma ampla variedade de recursos e métodos comprovados para fornecer o nível certo de suporte e orientação — tanto técnico quanto estratégico — para que sua empresa esteja bem preparada.

Siga estas práticas recomendadas para garantir que suas soluções da Adobe Digital Experience sejam resilientes, seguras e estejam prontas para o pico de tráfego de feriados:

* Planeje o aumento do tráfego.
* Evite grandes alterações durante as janelas de pico; agende atualizações antes ou depois da temporada de festas.
* Use painéis e alertas para monitorar o desempenho e detectar gargalos antecipadamente.
* Verifique se os seus contatos de suporte autorizados estão atualizados.
* [Contate o suporte da Adobe](https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/faq/how-to-submit-support-ticket) com antecedência sempre que possível.

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


## Guia de disponibilidade de feriados do Adobe Experience Platform (AEP)

+++**Clique para ver as recomendações de disponibilidade para feriados do Adobe Experience Platform (AEP).**

O Adobe Experience Platform (AEP) desempenha um papel essencial para potencializar as experiências do cliente em tempo real. Conforme a temporada de festas se aproxima, é essencial garantir que a implementação do AEP seja otimizada para aumentar o tráfego, o manuseio seguro de dados e a assimilação escalável.

## Prever demanda sazonal

Para se preparar para picos de tráfego sazonais, a Adobe recomenda o planejamento da capacidade e o monitoramento da assimilação do perfil de transmissão. Isso inclui prever volumes de dados e garantir que seu sistema possa lidar com o aumento da taxa de transferência. Consulte [Plano de capacidade e tráfego sazonal](https://experienceleague.adobe.com/pt-br/docs/experience-platform/dataflows/ui/monitor-streaming-profile) para referência.

## Preparar-se para a escala

O Adobe fornece várias estratégias para garantir que seu ambiente esteja pronto para o tráfego de feriados:

* Aumentar a capacidade alocada para sandboxes.
* Identifique fluxos de dados de alta taxa de transferência no [painel de monitoramento](https://experienceleague.adobe.com/pt-br/docs/experience-platform/dataflows/ui/monitor-streaming-profile) e aplique limitação ou filtragem onde necessário.
* Use a assimilação em lote para casos de uso de latência mais baixa a fim de otimizar o desempenho, conforme descrito em [Uso e capacidades da licença: Práticas recomendadas de taxa de transferência de streaming](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/license/capacity#suggestions).

Essas práticas ajudam a manter a confiabilidade da assimilação e reduzem a latência durante períodos de pico.

## Práticas recomendadas e medidas de proteção

Para ficar dentro dos limites operacionais e evitar interrupções do serviço, a Adobe recomenda as seguintes medidas de proteção de assimilação e perfil:

* [Práticas recomendadas de taxa de transferência de streaming](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/license/capacity#suggestions)
* [Medidas de proteção para a assimilação de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/guardrails)
* [Medidas de proteção padrão para dados e segmentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails)
* [Blueprints do AEP: Medidas de Proteção](https://experienceleague.adobe.com/pt-br/docs/blueprints-learn/architecture/architecture-overview/guardrails)

## Segurança e governança

A Adobe enfatiza as fortes práticas de segurança e governança, especialmente durante temporadas de alto tráfego, quando a sensibilidade dos dados é aumentada.

Consulte [Governança, privacidade e segurança no Adobe Experience Platform: Segurança](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/governance-privacy-security/overview#security) para obter recomendações sobre como proteger os dados do cliente, aplicar controles de privacidade e manter a conformidade na implementação do AEP.

Seguindo essas diretrizes e aproveitando a documentação pública da Adobe, as organizações podem garantir que seus Adobe Experience Platform sejam resilientes, seguros e prontos para fornecer experiências excepcionais ao cliente durante toda a temporada de festas.

+++

## Guia de disponibilidade de feriados do Adobe Journey Optimizer (AJO)

+++**Clique para ver as recomendações de disponibilidade para feriados do Adobe Journey Optimizer (AJO).**


Para preparar o Adobe Journey Optimizer para a temporada de festas, as organizações devem antecipar picos de eventos e complexidade entre canais, configurar regras de jornada e frequência e garantir a higiene de dados e a lógica de decisão. Eles também devem validar o desempenho em escala, aplicar medidas de proteção de segurança e API e aplicar insights pós-pico para refinar campanhas futuras.

## Prever demanda

* Com base nas compressões da temporada de festas e no maior volume de campanha, espere:
   * Um pico em eventos em tempo real e jornadas acionadas (abandono de carrinho, ofertas de última hora)
   * Riscos de saturação de mensagens (opções de não participação mais altas, fadiga)
   * Maior complexidade entre canais (email + push + SMS + no aplicativo)
* Use as métricas do ano passado (taxas de abertura/clique/recusa, volumes de entrada de jornada) para modelar as cargas esperadas e definir limites para seus sistemas de mensagens.
* Identifique &quot;janelas tranquilas&quot; prováveis ou períodos de baixo desempenho (por exemplo: fins de semana, feriados) e planeje os volumes de envio de acordo.

## Preparar-se para a escala

* Verifique se todas as configurações de canal no AJO estão definidas corretamente: email, push, SMS, Web e no aplicativo. Consulte [Configurar canais](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/channel-surfaces).
* Configure regras de limite e limite de frequência para controlar volumes de mensagens. Consulte o artigo [Limite de frequência](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules).
* Configurar conjuntos de regras de canal/jornada: Consulte [Trabalhar com conjuntos de regras](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets).
* Prepare sua higiene de dados / fluxos de eventos em tempo real e estruturas de segmentação.
* Verifique se você definiu públicos-alvo para campanhas de fim de ano, como:
   * clientes de alto valor
   * segmentos fiéis
   * abandonadores de carrinho
   * compradores pela primeira vez
* Pré-carregar ou preparar modelos para jornadas de feriados, aproveitar a lógica de decisão (ofertas/restrições) para que você possa se adaptar dinamicamente com base no inventário, nas ofertas sensíveis ao tempo e na preferência de canal. Consulte o exemplo no artigo [Adicionar restrições a uma oferta](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints).
* Disponibilidade técnica: confirme a capacidade de carregamento da API/endpoint, as regras de limitação/limitação para ações personalizadas e integrações externas. Consulte [Medidas de proteção e limitações](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/get-started/guardrails).

## Teste e validação

* Use sua estrutura de experimentação para testar as principais alterações de variáveis:
   * hora de envio
   * tipo de oferta
   * mix de canais
Consulte as [práticas recomendadas da AJO Experimentation Accelerator](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices).
* Realizar validação completa da jornada:
   * disparadores de eventos
   * entrada de segmentação
   * Fluxos de caminho de jornada
   * lógica de personalização
   * restrições de oferta
   * critérios de saída
* Verifique as regras de limite e conflito. Consulte o artigo [Limite de Jornada e arbitragem](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/conflict-prioritization/journey-capping).
* Volumes dimensionados para testes de estresse para envios ou picos de pico: simule volumes de acionador altos para validar o comportamento do sistema sob carga.
* Validar a capacidade de entrega: aquecer domínios/remetentes de email, confirmar configurações de push móveis e verificar canais de fallback para SMS/no aplicativo.

## Práticas recomendadas

* Use a orquestração omnicanal. Consulte o artigo do blog [jornadas essenciais de clientes omnicanal para engajamento e crescimento](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) que mostra um exemplo de temporada de festas com a AJO.
* Priorize acionadores em tempo real quando apropriado. Por exemplo: abandono de carrinho, abandono de navegação e alertas de estoque, já que os compradores de feriados são mais reativos.
* Aproveite a segmentação e personalização: segmente segmentos de alta intenção, adapte ofertas com base no comportamento de compras anteriores e preferências.
* Fadiga mínima das mensagens: aplique limites e horas de silêncio para evitar solicitações excessivas. Consulte a publicação do blog [Aumentar a experiência do cliente com limite diário de frequência no AJO](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510?profile.language=pt).
* Importância do tempo: o plano envia anteriormente na janela do feriado (dada a estação compactada) e alinha os canais aos fusos horários e ao comportamento do público local.
* Ofereça ofertas dinâmicas/por tempo limitado para criar urgência, mas coordene entre canais para evitar duplicação e conflito.
* Usar lógica de supressão: suprima públicos que acabaram de comprar ou aplique jornadas pós-compra para evitar mensagens redundantes.

## Segurança e governança

* Verifique se o controle de acesso e as permissões estão configurados para que somente os usuários necessários possam implantar jornadas ou modificar regras de negócios.
* Monitorar e impor o limite de chamada/conexão de API: Por exemplo, consulte a [API de Limite | Artigo do Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/connect-systems/external-systems/capping).
* Use dados primários limpos e garanta a identificação adequada da identidade para que as mensagens sejam centradas no cliente e não duplicadas/desalinhadas.
* Verifique se os domínios de deliverability estão aquecidos e se as medidas antisspam estão em vigor, especialmente para envios de feriados de alto volume.
* Revise logs de auditoria e alterações de jornada com frequência durante a temporada de pico para detectar jornadas mal executadas ou errantes antecipadamente.

## Aprendizados pós-pico

* Após os picos de carga, faça uma análise das contagens de entrada de jornada, das contagens de supressão, das taxas de recusa, das métricas de capacidade de entrega e do desempenho do canal.
* Limpe os segmentos suprimidos e pause ou desative as jornadas criadas para a janela do feriado a fim de evitar a fadiga de transporte.
* Use insights de desempenho em tempo real para refinar o planejamento do próximo ano (por exemplo: ajustes de hora de envio, combinação de canais e volume de mensagens).

Prevendo de forma proativa a demanda sazonal, configurando canais e regras, validando o desempenho da jornada e reforçando a segurança e o controle, as organizações podem garantir que a Adobe Journey Optimizer ofereça experiências do cliente perfeitas, personalizadas e resilientes durante esse período de festas e muito além.

+++

## Guia de disponibilidade de feriados do Customer Journey Analytics (CJA)

+++**Clique para ver as recomendações de disponibilidade para feriados do Customer Journey Analytics (CJA).**

A Customer Journey Analytics usa os 5 PCs para atingir a prontidão para feriados/épocas de pico.

### Preparar-se para a escala

* Analise as conexões e visualizações de dados do CJA; estabeleça quais conexões e visualizações de dados exigem monitoramento e provisionamento aprimorados.
* Confirme se o provisionamento é suficiente para a escala de feriados; faça upscaling das Conexões críticas e das Visualizações de dados conforme necessário. Consulte [Gerenciar conexões](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-connections/manage-connections) para obter mais informações.

### Monitorar desempenho

* Aproveite a RAM ([[!UICONTROL Visão geral do Gerenciador de Atividades de Relatórios]](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) para monitorar solicitações de relatórios ativas e enfileiradas em tempo real, identificar conexões com capacidade total e identificar gargalos.
* Fique atento a maior latência durante o pico de carga usando os artigos [Guia de Solução de Erros](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) e [Limitações Conhecidas](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations).
* Permita que os administradores suspendam ou cancelem preventivamente solicitações de longa duração/bloqueadas por meio da RAM. Consulte o artigo [Cancelar solicitações de relatórios no CJA](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests).

### Práticas recomendadas

* Agendar exportações/relatórios durante períodos de tráfego baixo para suavizar a carga e minimizar a latência. Consulte o artigo [Relatórios agendados](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-components/scheduled-projects-manager).
* Distribuir solicitações: programe relatórios em diferentes intervalos ao longo do dia.
* Reduza painéis, simplifique segmentos, reduza intervalos de datas e evite o excesso de trabalhos simultâneos. Consulte o artigo [Otimização do desempenho do CJA Workspace](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance) para obter detalhes.

### Resolução de problemas

* Ao solucionar erros de espaço de trabalho, consulte as mensagens de erro para a causa e as ações recomendadas; use a RAM ([!UICONTROL Gerenciador de Atividades de Relatórios]) para eliminar gargalos e gerenciar a simultaneidade de maneira eficiente. Consulte [Tratamento de erros do CJA Workspace](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) para obter mais detalhes.
* Use a RAM ([[!UICONTROL Gerenciador de Atividades de Relatórios] no CJA](https://experienceleague.adobe.com/pt-br/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) para apontar usuários, consultas ou projetos problemáticos; priorize e encerre/cancele conforme necessário.

### Aprendizados pós-pico

* Após o feriado/período de pico, analise os registros de desempenho e incidentes para avaliar o impacto das práticas recomendadas fornecidas.
* Revise consultas lentas e tarefas do usuário para identificar padrões/tendências que podem ser otimizados para a próxima temporada.
* Colete feedback dos usuários e das partes interessadas — atualize seus próprios runbooks e planos de disponibilidade usando insights recém-obtidos.
* Forneça feedback às equipes da Adobe por meio da equipe de conta.

+++

## Guia de preparação para feriados do Adobe Commerce

+++**Clique para ver as recomendações de preparação para feriados do Adobe Commerce.**

Para garantir uma temporada de pico bem-sucedida para sua organização, é essencial preparar sua loja digital Adobe Commerce para tráfego alto.

## Prever demanda

* Durante o período de pico de vendas de feriados (de meados de novembro a meados de janeiro), a Adobe recomenda que todos os comerciantes do Adobe Commerce hospedados em nossa infraestrutura em nuvem planejem proativamente um aumento nos visitantes enviando solicitações de aumento de capacidade de feriados. Consulte [Solicitações de capacidade de aumento temporário de férias do Adobe Commerce em nossa infraestrutura em nuvem](https://experienceleague.adobe.com/pt-br/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud) para obter detalhes.

## Preparar-se para a escala

Siga as recomendações no [Planejamento e tabela dinâmica: uma abordagem estratégica para a temporada de pico de 2025](https://experienceleague.adobe.com/pt-br/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025) guia, que fornece estratégias acionáveis usando o Adobe Commerce (e ferramentas opcionais do Adobe Experience Cloud) para ajudá-lo a planejar, girar e fornecer experiências excepcionais para o cliente durante o período mais movimentado do ano.

## Práticas recomendadas

* Siga o guia da Adobe [Como preparar sua infraestrutura para tráfego alto — os 5 pontos de desempenho da temporada de pico](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic).
* Confira as [Dicas técnicas para a preparação para feriados da Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness) para obter dicas sobre como preparar sua infraestrutura para tráfego intenso, evitar tempo de inatividade e otimizar o desempenho no período de feriados.

+++

## Guia de disponibilidade do Adobe Experience Manager (AEM) Cloud Services

+++**Clique para ver as recomendações de preparação do Adobe Experience Manager (AEM) Cloud Services.**

A temporada de festas está se aproximando rapidamente e, para muitos clientes da Adobe, isso significa o início dos períodos de pico de vendas. Em nosso compromisso com seu sucesso, queremos garantir que você esteja totalmente preparado para o aumento futuro do tráfego.

## Serviços em nuvem do Adobe Experience Manager (AEM)

Se a sua organização passar pelos momentos mais movimentados durante a temporada de festas, talvez você esteja pensando em como otimizar o site do Adobe Experience Manager para acomodar o pico de tráfego. Felizmente, com o Adobe Experience Manager Cloud Services, seu site já está equipado com a capacidade de dimensionar automaticamente, garantindo uma experiência contínua para seus visitantes, independentemente de haver alterações súbitas no tráfego.

## Preparar-se para a escala

* Para obter insights e orientações detalhadas sobre como se preparar para alto tráfego com os Serviços em nuvem da Adobe Experience Manager, consulte os seguintes links:

   * [CDN no AEM as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [Cache do AEM as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/caching/overview)

* Se você for um cliente do Ultimate Success e tiver compartilhado recentemente as informações de previsão de volume com a sua equipe de conta da Adobe, não se preocupe em enviá-las para nós novamente, pois já temos uma visualização.

Estamos aqui para apoiá-lo em todas as etapas da sua jornada. Caso tenha dúvidas ou dúvidas, sinta-se à vontade para [enviar um tíquete de suporte](https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Para se preparar para uma campanha de marketing na temporada de festas, consulte o [Guia do usuário do AEMaaCS: Introdução - Documentação dos parâmetros da campanha de marketing](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters).

## Segurança e governança

Para obter informações sobre a segurança/proteção do tráfego do site da AEM, consulte o artigo [Visão geral - Protegendo sites da AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) nos Tutoriais da AEM as a Cloud Service.

## Planejamento de manutenção de feriados

A Adobe programou períodos de exclusão de manutenção para garantir serviço ininterrupto durante períodos de feriado críticos:

* **Nenhuma atualização automática** ocorrerá entre:
   * 24 de novembro de 2025 - 2 de dezembro de 2025
   * 15 de dezembro de 2025 - 2 de janeiro de 2026

Isso garante a estabilidade durante períodos de alto tráfego. Para obter cronogramas de lançamento completos e janelas de manutenção, consulte o [roteiro de versões do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap).


## Adobe Experience Manager (AEM) com Adobe Managed Services (AMS)

Os clientes da AEM que usam o Adobe Managed Services podem trabalhar proativamente com seus CSEs para planejar as necessidades de cobertura dos feriados.

++++

## Guia de disponibilidade de feriados do Adobe Marketo

+++**Clique para ver as recomendações de preparação para feriados do Adobe Marketo.**

Para garantir campanhas de fim de ano bem-sucedidas com o Adobe Marketo, as equipes devem verificar as configurações de autenticação de email, limpar e proteger o banco de dados, otimizar a lógica e o agendamento da campanha, testar detalhadamente a renderização e o delivery de email e simplificar a preparação do suporte para o máximo de desempenho e engajamento.

## Preparar-se para a escala

* Verifique as configurações de SPF/DKIM e certifique-se de que tudo ainda esteja configurado e funcionando corretamente. Consulte o artigo [Configurar SPF e DKIM para a capacidade de entrega de emails](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability) para obter detalhes.
* Faça auditoria e limpe o banco de dados do Marketo limpando registros inativos/inválidos. Isso aumentará a probabilidade de seu envio chegar às caixas de entrada de seus leads mais prontos para vendas. Consulte o artigo [Verificação de integridade do banco de dados do Marketo e como mantê-lo limpo](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563) para obter detalhes.
* Confirme se os membros da equipe têm as permissões certas para executar tarefas e impedir acesso não intencional ou alterações nos emails. Esteja você fazendo alterações por meio do **[!UICONTROL Administrador]** ou do **[!UICONTROL Admin Console]**, nós o protegemos. Consulte o artigo [Gerenciando Permissões e Funções de Usuário](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions).
* Revise suas integrações do Launchpad para garantir a autenticação correta e resolver possíveis erros antes de serem usadas. Consulte o artigo [Guia do desenvolvedor do Marketo: Autenticação](https://experienceleague.adobe.com/pt-br/docs/marketo-developer/marketo/rest/authentication).

## Práticas recomendadas

A eficiência começa com a compreensão exata de como o Marketo prioriza e processa campanhas. Dê às suas campanhas o dom da velocidade com essas dicas de otimização.

* Entender como o Marketo prioriza o processamento das etapas do fluxo de campanha é fundamental para evitar o atraso inadvertido de qualquer email urgente ou de alta prioridade. Consulte o artigo [Como funciona o processamento da campanha](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Considere a lógica da lista inteligente e ajude a garantir que suas campanhas sejam executadas rapidamente e com desempenho máximo. Consulte o artigo [Práticas recomendadas para Smart Lists](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists).
* O **[!UICONTROL Head Start]** ou o **[!UICONTROL Fuso horário do destinatário]** pode começar a criar emails antes do envio, reduzindo atrasos e fornecendo tempo de preparação adicional para qualificar clientes potenciais com lógica de alto recurso. Para obter detalhes, consulte os artigos [Head Start para Programas de Email](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs) e [Agendar Programas de Email com Fuso Horário do Destinatário](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone).
* Sua campanha está ativa, e os leads estão fluindo, e você percebe um erro com a etapa de fluxo. É tentador corrigir com um ajuste rápido, mas estar ciente do que acontece quando você altera uma etapa de espera ao vivo ou reordena seus fluxos pode ajudá-lo a evitar muitas dores de cabeça e limpar mais tarde. Consulte o artigo [Editando o Fluxo da Campanha com Membros em Etapas de Espera](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

## Teste e validação

Antes de clicar em **[!UICONTROL Enviar]**, verifique se os seus emails têm a aparência e o desempenho esperados.

* O Marketo oferece várias maneiras de testar a aparência de um email para garantir que ele tenha a aparência exata que você imaginou.
   * Use a função **[!UICONTROL Visualizar]** para garantir que o conteúdo dinâmico e os tokens sejam renderizados corretamente ao visualizar por segmentação ou leads individuais. Consulte o artigo [Visualizar um email com conteúdo dinâmico](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content).
   * Envie um email direto para seus registros de teste de forma rápida e fácil para ver como seu email aparece em diferentes clientes/dispositivos. Consulte o artigo [Executar uma única etapa de fluxo de uma lista inteligente](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list).
   * Para [!DNL Litmus] usuários, agora está mais fácil do que nunca integrar sua conta e iniciar testes de renderização diretamente do editor de email. Consulte o artigo [Testar renderização de email [!DNL Litmus]](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering).
* Confira o recurso Relatório de spam por email, que se integra ao [!DNL SpamAssassin] para revisar o conteúdo do seu email e atribuir uma pontuação sobre a probabilidade de ele chegar à caixa de entrada ou ser marcado como *spam*. Consulte o artigo [Relatório de spam por email](https://experienceleague.adobe.com/pt-br/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report).
* Fique de olho na [!UICONTROL Fila de campanha] para verificar se suas campanhas estão processando e priorizando itens de alta urgência corretamente. Consulte [Minha campanha está em execução?Artigo &#x200B;](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662).

## Simplifique sua experiência de suporte

Quando algo dá errado, a velocidade é importante e o Suporte da Marketo está aqui para ajudar. Inclua esses detalhes em seu caso de suporte para evitar problemas e ajudar nossa equipe a trabalhar para uma resolução mais rápida. Consulte o artigo [Práticas recomendadas para trabalhar com o suporte da Marketo](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491).

Com este guia, você pode ficar um pouco mais tranquilo sabendo que está partindo de uma posição forte para impulsionar o engajamento e as conversões durante essa janela crítica. O que está em jogo é alto, mas o seu estresse não precisa ser. Comece seus preparativos hoje e faça desta temporada de festas a sua mais bem sucedida ainda.

+++

## Guia de preparação para feriados do Adobe Workfront

+++**Clique para ver as recomendações de preparação para feriados do Adobe Workfront.**

Para preparar o Adobe Workfront para a temporada de festas, as equipes devem atualizar os contatos de suporte, alinhar as programações internas ao Adobe, evitar grandes alterações durante os horários de pico e monitorar proativamente as automações e integrações para garantir operações tranquilas.

## Preparar-se para a escala

Para ajudar a garantir uma experiência de suporte tranquila durante os feriados:

* Revise e atualize seus contatos de suporte autorizados com antecedência.
* Confirmar se os principais interessados estão disponíveis para colaborar com o suporte se surgirem problemas críticos.
* Se o produto ou workflow do planejamento for alterado durante a janela do feriado, considere programá-los antes de meados de novembro ou depois do início de janeiro para obter melhores tempos de resposta.
* Comunique as programações de feriados internas aos contatos do Adobe para garantir o alinhamento.

## Teste e validação

Mantenha-se informado sobre os lançamentos do Workfront e teste novos recursos em ambientes de sandbox:

* [Preparar para uma versão do Adobe Workfront](https://experienceleague.adobe.com/pt-br/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Arquivo Morto das Notas de Versão do Workfront](https://experienceleague.adobe.com/pt-br/docs/workfront/using/product-announcements/product-releases/product-releases)
* [Visão geral da versão do primeiro trimestre de 2025](https://experienceleague.adobe.com/pt-br/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Gravação do webinário da versão do Workfront](https://experienceleague.adobe.com/pt-br/docs/events/workfront-recordings/releases/25-1-release-webinar)

## Práticas recomendadas

* Planejamento Pró-ativo: Identifique quaisquer dependências do sistema ou automações programadas que possam ser afetadas por programações de folga internas.
* Comunicação contínua: mantenha suas equipes internas e o suporte da Adobe informados sobre manutenção planejada ou eventos importantes.
* Use painéis: monitore as principais integrações e automatizações para capturar sinais antecipados de problemas de desempenho.
* Escalonar com antecedência: se você antecipar ou observar a degradação do serviço, abra um tíquete de suporte imediatamente — não espere até que ele se torne crítico.

Ao planejar com antecedência, manter uma comunicação clara e encaminhar os problemas antecipadamente, as organizações podem minimizar as interrupções e garantir que a Workfront continue a oferecer suporte a fluxos de trabalho críticos durante todo o período do feriado.

+++

## Guia de preparação para feriados do Adobe Campaign

+++**Clique para ver as recomendações de preparação para feriados do Adobe Campaign.**


Para preparar o Adobe Campaign para as férias, as equipes devem validar proativamente as configurações de capacidade de entrega, otimizar a segmentação de público e a frequência de mensagem, garantir a escalabilidade da infraestrutura e testar a orquestração de campanhas entre canais para lidar com picos sazonais de volume e engajamento de maneira eficaz.

## Dicas de especialistas para fazer suas campanhas de fim de ano se destacarem

Assim como nunca é cedo demais para começar as compras para datas comemorativas, também nunca é cedo demais para começar a planejar uma campanha de marketing de grande sucesso para datas comemorativas. Com o Adobe Campaign, você pode projetar, planejar e executar campanhas que realizarão todos os desejos de fim de ano da sua organização. Mas você conhece todas as dicas para veicular campanhas que encerram o ano em alta? Confira este vídeo, [Dicas de especialistas para destacar suas campanhas de fim de ano](https://experienceleague.adobe.com/pt-br/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03), que aborda as práticas recomendadas de entrega e execução e mostrará como fazer tudo isso no Adobe Campaign.

## Considerações e preparativos para o período de férias

Este vídeo, [Adobe Campaign: Disponibilidade para feriados - Considerações e preparativos para o período de feriados](https://helpx.adobe.com/br/customer-care-office-hours/campaign/campaign-holiday-readiness.html), aborda:

* Envolver a comunidade do Campaign
* Capacidade de entrega - Considerações para feriados e muito mais!
* Recomendações técnicas para Adobe Campaign Classic (ACC) e Adobe Campaign Standard (ACS)

Para que a Adobe Campaign esteja pronta para a temporada de pico de feriados, as organizações devem finalizar as verificações de capacidade de delivery, validar as configurações de campanha e garantir que a infraestrutura escalável e a orquestração entre canais estejam em vigor para executar campanhas de alto volume e com detecção de tempo durante a temporada de festas com confiança.

+++

## Guia de preparação para feriados do Adobe Analytics

+++**Clique para ver as recomendações de preparação para feriados do Adobe Analytics.**

À medida que a temporada de festas se aproxima, as organizações que usam o Adobe Analytics devem tomar medidas proativas para garantir a precisão dos dados, o desempenho da plataforma e a confiabilidade dos relatórios durante os períodos de pico de tráfego. A Adobe fornece vários recursos e práticas recomendadas para ajudar as equipes a se prepararem de maneira eficaz.

## Prever tráfego

Para garantir alocação adequada de hardware e capacidade de resposta do sistema, a Adobe recomenda enviar com antecedência os **volumes de ocorrências/chamadas diárias e por hora do servidor**.

* Verifique [O planejamento de pico de tráfego e os prazos de entrega para alocação de hardware](https://experienceleague.adobe.com/pt-br/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times), já que entender a rapidez com que os dados são disponibilizados é essencial para a tomada de decisões em tempo real durante períodos de alto volume.

* Saiba o que afeta a disponibilidade e a latência de dados no Adobe Analytics em [visão geral da latência de dados do Adobe Analytics](https://experienceleague.adobe.com/pt-br/docs/analytics/technotes/latency), incluindo picos inesperados de tráfego e problemas de hardware, e descubra estratégias recomendadas para reduzir atrasos de dados.

## Práticas recomendadas

Para as equipes que usam feeds de dados para exportar dados brutos de análise, o Adobe fornece orientação sobre como otimizar as configurações do feed e evitar armadilhas comuns.

* [Práticas recomendadas para feeds de dados do Adobe Analytics](https://experienceleague.adobe.com/pt-br/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

Para manter relatórios rápidos e confiáveis durante os feriados, a Adobe recomenda:

* [Otimizando o desempenho do Analysis Workspace](https://experienceleague.adobe.com/pt-br/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Resolução de problemas e práticas recomendadas do Report Builder: recomendações para solicitações de otimização](https://experienceleague.adobe.com/pt-br/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Guia de componentes do Analytics: fila de relatórios agendados](https://experienceleague.adobe.com/pt-br/docs/analytics/components/scheduled-reports-admin)

## Planejamento de manutenção de feriados

A Adobe normalmente impõe **janelas de exclusão de manutenção** durante períodos de pico de feriados para garantir serviço ininterrupto. Os clientes devem monitorar os cronogramas de lançamento e manutenção da Adobe por meio da Experience League e coordenar com as equipes de conta da Adobe para o planejamento de suporte.

Seguindo essas diretrizes e aproveitando a documentação pública da Adobe, as organizações podem garantir que sua implementação do Adobe Analytics seja robusta, responsiva e esteja pronta para as demandas da temporada de festas.

+++

## Guia de preparação para feriados do Adobe Target

+++**Clique para ver as recomendações de preparação para feriados do Adobe Target.**

A temporada de festas traz excelentes oportunidades de envolvimento, mas também apresenta desafios como picos de tráfego e maior demanda de sistemas de personalização. Para ajudá-lo a fornecer experiências perfeitas durante esse período crítico, compilamos as principais recomendações para garantir que sua implementação do Adobe Target esteja pronta.

## Prever demanda

Comece antecipando picos de tráfego de 20 a 50% ou mais e validando se sua infraestrutura pode lidar com a carga. Preveja a atividade e os volumes de dados no Adobe Target, Analytics e AEP para evitar surpresas.

Também é importante identificar jornadas essenciais, como check-out, recomendações de produtos e ofertas promocionais, para que os esforços de personalização se concentrem onde são mais importantes.

Consulte [Práticas recomendadas para otimização com o Adobe Target](https://experienceleague.adobe.com/pt-br/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization).

## Preparar-se para a escala

* Planeje o aumento do tráfego no site e nos dispositivos móveis e informe a equipe de suporte do Target para aumentar a capacidade do servidor e evitar chamadas bloqueadas.
* Para qualquer teste de carga/caneta, a equipe de suporte do Target deve ser informada com antecedência.
* Atualize para as versões mais recentes da API de entrega/`at.js`.
* Congelar alterações não críticas; preparar para experiências de fallback.
* Alinhe os processos de suporte e escalonamento e ative os alertas proativos.

## Teste e validação

Valide a entrega de conteúdo usando os [links de controle de qualidade](https://experienceleague.adobe.com/pt-br/docs/target/using/activities/activity-qa/activity-qa) para confirmar se tudo funciona conforme o esperado. Use as **[!UICONTROL Regras de correspondência de público-alvo para ver as experiências]** para garantir que o público-alvo correto se qualifique para a atividade que você está testando. Verifique se a sua configuração de **[!UICONTROL Métrica de meta]** está alinhada ao **[!UICONTROL Objetivo]** da atividade. E sempre tenha um plano de backup pronto — por via das dúvidas.

## Práticas recomendadas

Mantenha sua implementação dentro dos [limites do Adobe Target](https://experienceleague.adobe.com/pt-br/docs/target/using/troubleshoot/target-limits) e verifique antecipadamente a [conformidade com o GDPR e a CCPA](https://experienceleague.adobe.com/pt-br/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation) antes de iniciá-la. Mantenha menos de 100 atividades ativas e arquive as mais antigas para simplificar as coisas. Aproveite a **[!UICONTROL Alocação automática]**/**[!UICONTROL Direcionamento automático]** para otimização orientada por IA. Estabeleça planos de reversão e painéis de monitoramento em tempo real.

## Segurança e governança

Antes de personalizar as experiências, confirme a conformidade com o consentimento de acordo com o GDPR e a CCPA. Evite armazenar informações de identificação pessoal (PII) em parâmetros de perfil e valide a segurança da API para proteger os dados do cliente.

+++
