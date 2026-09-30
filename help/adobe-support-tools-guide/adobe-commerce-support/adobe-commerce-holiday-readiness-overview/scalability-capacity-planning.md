---
title: Planejamento de escalabilidade e capacidade
description: Recomendações de escalabilidade e planejamento de capacidade para ajudar os comerciantes da Adobe Commerce a preparar seus ambientes para eventos de alto tráfego, como a temporada de festas.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# Planejamento de escalabilidade e capacidade

Esta seção fornece recomendações técnicas para dimensionar ambientes do Adobe Commerce para se preparar para eventos de alto tráfego, como a temporada de festas.

>[!NOTE]
>
>As etapas marcadas **(Somente na nuvem)** se aplicam ao Commerce na infraestrutura em nuvem. A maioria das outras recomendações também se aplica a implantações locais.

## Planejar upsize do cluster antecipadamente (somente na Nuvem) {#plan-cluster-upsize-early}

Para clientes da infraestrutura em nuvem do Commerce, um upsize temporário de cluster aloca mais recursos de computação para lidar com picos de tráfego na temporada de pico. Eleve um tíquete de suporte com antecedência, com o intervalo de datas e o tamanho de cluster necessário, e fale com seu Gerente de conta dedicado sobre o consumo e os requisitos atuais de recursos. Envie a solicitação pelo menos 48 horas úteis antes que a capacidade seja necessária — especificamente para a temporada de festas, envie o mais cedo possível, já que a capacidade durante a Black Friday e a Cyber Monday é limitada. Consulte [Como solicitar um upsize temporário](https://experienceleague.adobe.com/pt-br/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize).

Por exemplo, um cliente de Pro-architecture com uma linha de base diária de 24 núcleos (24 vCPUs, 96 GB RAM) com upsizing para 96 núcleos por 7 dias usaria aproximadamente 4 vezes os recursos (96 vCPUs, 384 GB RAM) - um consumo incremental de cerca de 504 vCPU-dias (96×7 - 24×7).

## Blindagem de origem Fastly {#fastly-origin-shielding}

O objetivo da blindagem de origem do Adobe Commerce [!DNL Fastly] é reduzir o tráfego diretamente para a origem do Adobe Commerce. Quando uma solicitação é recebida, um local de borda [!DNL Fastly] (Ponto de Presença) verifica o conteúdo em cache e o entrega. Se não for armazenado em cache, ele continuará no POP de escudo para verificar se está armazenado em cache lá; se o conteúdo tiver sido solicitado anteriormente, mesmo de outro POP global, ele será armazenado em cache. Por fim, se não estiver armazenado em cache no POP de escudo, ele só continuará no servidor de origem.

A blindagem de origem [!DNL Fastly] pode ser habilitada no Administrador do Adobe Commerce, nas configurações de back-end do [!DNL Fastly]. Escolha um local de blindagem mais próximo ao data center de origem da Adobe Commerce para obter o melhor desempenho. Para obter detalhes, consulte [Configurar back-ends e blindagem de origem](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding).

Por padrão, a blindagem de origem [!DNL Fastly] não está habilitada.

## Realizar testes de carga e failover {#conduct-load-and-failover-tests}

Realize testes de carga e recuperação antes de campanhas importantes para validar configurações de dimensionamento e planos de reversão.