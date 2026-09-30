---
title: Visão geral da preparação para feriados do Adobe Commerce
description: Orientação de nível executivo para preparar o Adobe Commerce em ambientes de infraestrutura em nuvem para eventos de alto tráfego, como a temporada de festas.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Visão geral da preparação para feriados do Adobe Commerce

Este manual fornece orientação para preparar ambientes do Adobe Commerce para eventos de alto tráfego, como a temporada de festas. Ele consolida recomendações técnicas em cinco áreas de foco estratégico:

- Otimização do desempenho
- Práticas recomendadas e estabilidade
- Monitorização e observabilidade
- Planejamento de escalabilidade e capacidade
- Disponibilidade operacional

Essas áreas de foco ajudam a garantir que sua plataforma permaneça estável, segura e com desempenho máximo.

## Otimização do desempenho

Veja a seguir uma visão geral das etapas recomendadas para garantir um desempenho otimizado. Para obter detalhes, consulte [Disponibilidade festiva do Adobe Commerce > Otimização de desempenho](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md).

* Otimizar o cache de solicitações do Fastly: Normalize seus parâmetros de rastreamento promocional, confirme se as páginas de aterrissagem podem ser armazenadas em cache e use o GraphQL GET para PWA ou as lojas headless para aumentar sua taxa de acessos ao cache do Fastly.
* Ativar Fastly IO: Ative o Fastly Image Otimization e o Deep IO para que as transformações de imagem sejam executadas na borda da CDN, substituindo a origem, recortando o tempo de renderização da página em vitrines com muitas imagens.
* Ativar cache L2: armazena dados de cache localmente em cada nó da Web para reduzir a latência e as chamadas de rede para Redis/Valkey, dependendo da versão do Adobe Commerce. O cache Redis não é suportado para Adobe Commerce 2.4.9 ou versões de patch posteriores a 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 e 2.4.8-p4.
* Habilitar conexões subordinadas: encaminhe consultas com leitura pesada para nós de réplica com `MYSQL_USE_SLAVE_CONNECTION` e `REDIS_USE_SLAVE_CONNECTION` ou `VALKEY_USE_SLAVE_CONNECTION`, de modo que os bancos de dados mestres não sejam o afunilamento sob carga.
* Ativar processamento assíncrono de pedidos e email: o posicionamento da ordem de fila, as atualizações de grade de dados de pedido e os emails de check-out são executados em segundo plano em três configurações separadas, para que o check-out permaneça rápido em um volume de pedidos alto.
* Alternar indexadores para o modo Atualizar na Programação: Mova indexadores de Atualizar ao Salvar para o modo Atualizar na Programação orientado por cron para evitar o bloqueio durante atualizações frequentes de catálogo, exceto para o indexador customer_grid.
* Considere a arquitetura dimensionada (dividida): se o ajuste e as correções no nível de código ainda deixarem o CPU no limite de carga, vá para uma configuração de camada dividida em seis nós que dimensiona os nós da Web e do banco de dados independentemente.

## Práticas recomendadas e estabilidade

Veja a seguir uma visão geral das práticas recomendadas que garantem a estabilidade da sua instância. Para obter etapas detalhadas para cada uma dessas, consulte [Disponibilidade para feriados do Adobe Commerce > Práticas recomendadas e estabilidade](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md).

* Atualização para a versão mais recente do Adobe Commerce: mantenha-se em uma versão compatível para manter as correções de segurança e as melhorias de desempenho fornecidas pelo Adobe em cada versão.
* Instale as ferramentas ECE-Tools e Quality Patch Tool (QPT) mais recentes: atualize as ferramentas ECE com suas dependências e confirme se as correções da Ferramenta de correção de qualidade aplicáveis são aplicadas, tanto para instalações na nuvem quanto locais.
* Revisar e limpar arquivos de log: remova logs de depuração e monitore erros recorrentes para evitar o uso excessivo do disco e melhorar a visibilidade do log.
* Monitorar o crescimento do tamanho do disco: mantenha os volumes de arquivos compartilhados e de bancos de dados abaixo de 70% de uso, para que o crescimento do armazenamento não acione uma paralisação.
* Revisar consultas lentas ao banco de dados: Use a ferramenta APM e o log de consultas lentas do MySQL para localizar e corrigir consultas caras antes que elas sejam compostas em tráfego de pico.
* Configurar os trabalhos do cron corretamente: confirme se o cron é executado a cada minuto sob o usuário correto, já que cada operação assíncrona no Commerce depende dela.
* Otimizar configurações do lado do cliente: ative a minificação e o agrupamento de CSS, JavaScript e HTML para acelerar o tempo de carregamento da loja.

## Monitorização e observabilidade

A seguir estão as maneiras recomendadas de monitorar a instância do Adobe Commerce durante a temporada de pico. Para obter etapas detalhadas para cada uma dessas recomendações de monitoramento e observabilidade, consulte [Disponibilidade festiva do Adobe Commerce > Monitoramento e observação](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md).

* Monitorar o tráfego com o New Relic: use os logs do Fastly no New Relic para detectar anomalias de tráfego, IPs abusivos, solicitações mal-intencionadas direcionando endpoints como pagamento e tendências de dispositivos/navegadores.
* Personalizar alertas do New Relic: configure seus próprios alertas baseados em NRQL para tráfego incomum, consultas lentas do GraphQL ou taxas de erro crescentes, além dos alertas gerenciados do Adobe.
* Rastrear pontuação do Apdex: observe a pontuação do Apdex (target ≥ 0,85) para manter os tempos de resposta de back-end e front-end em um intervalo que os usuários consideram satisfatório.
* Revisar insights de suporte (Relatório SWAT): execute um relatório SWAT antes e depois dos eventos de pico para identificar riscos no nível do sistema e áreas de melhoria.

## Planejamento de escalabilidade e capacidade

Para obter etapas detalhadas para cada uma dessas recomendações de escalabilidade e planejamento de capacidade, consulte [Prontidão para feriados do Adobe Commerce > Planejamento de Escalabilidade e Capacidade](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md).

* Planejar o upsize do cluster antecipadamente: solicite um upsize de computação temporário ao Suporte da Adobe pelo menos 10 dias úteis antes de uma grande promoção.
* Ativar o Fastly origin shield: encaminhe solicitações não armazenadas em cache por meio de um POP de escudo próximo à sua origem para que menos solicitações atinjam o servidor de origem diretamente.
* Realizar testes de carga e failover: teste a carga e os cenários de recuperação antes das principais campanhas para confirmar que seus planos de reversão e dimensionamento realmente resistem.

## Disponibilidade operacional

* Aplicar todos os patches de segurança e desempenho: Conclua todos os patches antes do congelamento do código para que as implantações não sejam interrompidas posteriormente.
* Execute verificações de integridade antes do feriado: teste backups, integridade do cron e scripts de aquecimento de cache para que as operações sejam executadas sem problemas quando carregadas.
* Estabelecer manuais de monitoramento: limites de alerta de documentos, caminhos de escalonamento e contatos 24 horas por dia, 7 dias por semana, para que a equipe possa responder rapidamente durante o pico.
* Planos de reversão de documentos: mantenha prontas as estratégias de reversão com versão para que você possa se recuperar rapidamente de uma implantação inválida.