---
title: Solicitações de capacidade de aumento temporário do Adobe Commerce em nossa infraestrutura em nuvem
description: Durante a temporada de pico de vendas de feriados (aproximadamente de meados de novembro a meados de janeiro), a Adobe recomenda que todos os comerciantes da Adobe Commerce hospedados em nossa infraestrutura em nuvem se preparem para aumentar o tráfego.
feature: Support
feature-set: Commerce
role: Admin
exl-id: 560fae4d-77f0-4618-a3a5-f549daa74402
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%
---
# Solicitações de capacidade de aumento temporário do Adobe Commerce em nossa infraestrutura em nuvem

Durante a temporada de pico de vendas de feriados (aproximadamente de meados de novembro a meados de janeiro), a Adobe recomenda que todos os comerciantes da Adobe Commerce hospedados em nossa infraestrutura em nuvem se preparem para aumentar o tráfego.

Para obter uma lista de verificação abrangente entre soluções e práticas recomendadas para preparar seus sistemas e equipes para a temporada de pico, consulte o [Guia do Adobe DX Unified Holiday Readiness](https://experienceleague.adobe.com/en/docs/support-resources/data-sheets/unified-holiday-readiness).

**Planejando e estimando o tráfego**

Recomendamos que todos os comerciantes da Adobe Commerce em nossa infraestrutura em nuvem [utilizem esse conjunto de recomendações sobre como estimar o tráfego da temporada de pico](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic) para a temporada de pico de vendas das festas a cada ano.

Depois de concluir a estimativa recomendada, se sua equipe tiver identificado datas em que você acha que precisará de capacidade adicional, continue para a próxima etapa para obter informações sobre como solicitar capacidade de sobretensão.

**Exibir o histórico de seus uploads**

Você pode exibir o histórico de redimensionamentos solicitados solicitando as informações do seu **CSM (Customer Success Manager)**.
As seguintes informações estão disponíveis para cada solicitação de redimensionamento:

* **Data de Início do Tamanho**: data da solicitação de upsize.
* **Data de Término do Tamanho**: data em que o cluster retornou ao tamanho anterior.
* **Tamanho do vCPU**: o tamanho do cluster após o upsize.
* **Dias de Uso**: por quantos dias o cluster ficou com upsizing.
* **Period vCPU**: tamanho de vCPU alterado pelo número de dias em que foi usado. (por exemplo, o tamanho do vCPU 192 por 25 dias é igual a 4.800).

**Solicitando Capacidade de Sobretensão**

Os comerciantes da Adobe Commerce em nossa infraestrutura em nuvem que antecipam a necessidade de capacidade adicional durante a temporada de festas devem [enviar um Tíquete de Suporte para Capacidade Excedida](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-request-temporary-magento-upsize.html) por meio de nossa Central de Ajuda, indicando as datas e as necessidades esperadas de capacidade dentro do tíquete. Observe que o aumento da capacidade exigirá o uso da capacidade excedente licenciada.

**Recomendamos o envio desses tíquetes com pelo menos 48 horas úteis de antecedência em relação à necessidade da capacidade. Além disso, recomendamos que as solicitações referentes ao período Black Friday/Cyber Monday sejam feitas com a maior antecedência possível, já que a capacidade durante esse período é limitada.**


**Mais Ajuda?**

Precisa de mais orientação sobre como se preparar para o tráfego de pico de temporada? Os comerciantes da Adobe Commerce em nossa infraestrutura em nuvem podem entrar em contato com a equipe de conta da Adobe para obter ajuda, estratégia e dicas de planejamento para se preparar para uma temporada de pico bem-sucedida. Também recomendamos consultar o [Blog do Adobe for Business](https://magento.com/blog) para obter dicas de estratégia o ano todo.

## Recursos para analisar sua capacidade

Em nossa base de conhecimento de suporte:

* [Cálculo de alocação de CPU para Adobe Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-cpu-allocation-calculation.html)
* [Verifique se o upsize das instâncias do host é necessário para o Adobe Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-if-upsize-for-hosts-instances-is-needed.html)
* [Verificar a configuração do CPU do host para o Adobe Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-hosts-cpu-configuration.html)
* [Identificar e medir paralisações do Adobe Commerce na nuvem](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-identify-outages.html)
