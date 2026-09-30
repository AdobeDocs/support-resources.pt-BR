---
title: Disponibilidade operacional
description: Recomendações de disponibilidade operacional para ajudar os comerciantes da Adobe Commerce a preparar seus ambientes para eventos de alto tráfego, como a temporada de festas.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bcd8874c-7b93-5596-bdaa-22660e84df14
    internal-label: Deploy
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 938d2364-5176-55ec-80f1-9415253e5e51
    internal-label: Site Management
  - id: b48dbafb-4193-5648-b9d9-bf96e9c9a411
    internal-label: Backend Development
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: c89c0345d0e483463ab44195c2d5c0cb18d1d4c5
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%
---

# Disponibilidade operacional

Esta seção fornece recomendações técnicas para preparar ambientes do Adobe Commerce, tanto Commerce na infraestrutura em nuvem quanto no local, para eventos de alto tráfego, como a temporada de festas.

## Aplicar todos os patches de segurança e desempenho {#apply-all-security-and-performance-patches}

Conclua todas as atualizações antes do congelamento do código para evitar interrupções na implantação.

## Executar verificações de integridade antes do feriado {#run-pre-holiday-health-checks}

Teste backups, integridade do cron e scripts de aquecimento de cache para garantir operações tranquilas sob carga.

## Estabelecer manuais de monitoramento {#establish-monitoring-playbooks}

Documente os limites de alerta, as etapas de escalonamento e os pontos de contato para obter uma resposta 24x7 durante o pico.

## Planos de reversão de documento {#document-rollback-plans}

Mantenha estratégias de reversão com versão para se recuperar rapidamente de anomalias na implantação.

