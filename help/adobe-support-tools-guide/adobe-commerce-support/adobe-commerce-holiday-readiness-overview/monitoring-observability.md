---
title: Monitorização e observabilidade
description: Recomendações de monitoramento e observabilidade para ajudar os comerciantes do Adobe Commerce a preparar seus ambientes para eventos de alto tráfego, como a temporada de festas.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# Monitorização e observabilidade

Esta seção fornece recomendações técnicas para monitorar ambientes do Adobe Commerce a fim de se preparar para eventos de alto tráfego, como a temporada de festas.

>[!NOTE]
>
>As etapas marcadas **(Somente na nuvem)** se aplicam ao Commerce na infraestrutura em nuvem. A maioria das outras recomendações também se aplica a implantações locais.

## Monitorar o tráfego com o New Relic (somente Cloud) {#monitor-traffic-with-new-relic}

A infraestrutura do Adobe Commerce na nuvem inclui uma assinatura da plataforma de observabilidade [!DNL New Relic], que incorpora perfeitamente a transmissão de logs do [!DNL Fastly] para o [!DNL New Relic] em tempo quase real. Essa integração permite monitorar os padrões de tráfego e as tendências em tempo real para que você possa tomar medidas corretivas.

Use esses logs para:

* Identifique os países dos quais suas solicitações da Web são originadas.
* Encontre endereços IP abusivos ou agentes de usuário que rastream do site.
* Identifique tráfego mal-intencionado direcionado a endpoints específicos, como pagamento.
* Crie relatórios sobre o dispositivo e os tipos de navegador que seus clientes usam.

Por exemplo, monitore o país de origem do seu tráfego para confirmar se ele reflete as localizações geográficas de suas promoções e clientes:

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

Modifique essa consulta para atender às suas necessidades, segmente-a ainda mais ou transforme-a em um painel para rastreamento centralizado. Para obter detalhes, consulte [gerenciamento de logs do New Relic](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Personalizar alertas do New Relic (somente na nuvem) {#customize-new-relic-alerts}

Além dos Alertas gerenciados definidos pela Adobe Commerce na infraestrutura em nuvem, você pode definir uma grande variedade de alertas e notificações para sua plataforma durante o pico da temporada de vendas — por exemplo, notificando você sobre o tráfego de bot ou um maior tempo de resposta em uma consulta do GraphQL. Consulte [Alertas gerenciados para Adobe Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce) para obter a lista completa de alertas internos.

[!DNL New Relic] Alertas e IA dão suporte a estruturas de consulta baseadas em NRQL. Configure alertas personalizados no painel do [!DNL New Relic] em **[!UICONTROL Alertas e IA]**.

## Revisar pontuação do Apdex (somente na nuvem) {#review-apdex-score}

A pontuação do Apdex mede a satisfação do usuário com o tempo de resposta de seus aplicativos e serviços da Web. Você pode analisar a pontuação Apdex do seu Adobe Commerce na infraestrutura em nuvem usando o [!DNL New Relic].

Uma pontuação do Apdex varia de 0 a 1. Uma pontuação de 0 é a pior pontuação possível, o que significa que 100% dos tempos de resposta foram **frustrados**. Uma pontuação de 1 é a melhor pontuação possível, o que significa que 100% dos tempos de resposta foram **satisfeitos**. [!DNL New Relic] relata uma pontuação do Servidor de Aplicativos, que reflete o desempenho do back-end, e uma pontuação do Usuário Final, que reflete o desempenho do cliente.

Uma pontuação Apdex de 0,5 ou inferior justifica investigação. Uma pontuação abaixo de 0,4 é considerada uma interrupção.

Juntamente com o Apdex, o [!DNL New Relic] fornece uma variedade de estatísticas para analisar problemas de desempenho no Adobe Commerce na infraestrutura em nuvem. Para ver as etapas, consulte [Solucionar problemas de desempenho usando o New Relic no Adobe Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce).

## Revisar insights de suporte (relatório SWAT) {#review-support-insights-swat-report}

Para obter um relatório mais detalhado sobre o seu ambiente, gere um relatório da Ferramenta de análise do site (SWAT). Para obter mais informações sobre a ferramenta SWAT, consulte [Ferramenta de Análise do Site](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/tools/site-wide-analysis-tool/intro).