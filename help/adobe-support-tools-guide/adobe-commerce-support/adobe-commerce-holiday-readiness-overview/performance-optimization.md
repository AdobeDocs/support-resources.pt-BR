---
title: Otimização do desempenho
description: Recomendações de otimização de desempenho para ajudar os comerciantes do Adobe Commerce a preparar seus ambientes para eventos de alto tráfego, como a temporada de festas.
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
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# Otimização do desempenho

Esta seção fornece recomendações técnicas para preparar ambientes do Adobe Commerce, tanto Commerce na infraestrutura em nuvem quanto no local, para eventos de alto tráfego, como a temporada de festas.

>[!NOTE]
>
>As etapas marcadas **(Somente na nuvem)** se aplicam ao Commerce na infraestrutura em nuvem. A maioria das outras recomendações também se aplica a implantações locais.

## Otimizar o cache de solicitações do Fastly (somente na nuvem) {#optimize-fastly-request-caching}

[!DNL Fastly] armazena em cache as respostas na borda para reduzir a carga no servidor de origem. Durante a temporada de pico, algumas verificações de configuração ajudam a aproveitar ao máximo esse cache, especialmente ao executar promoções com parâmetros de rastreamento ou uma loja headless. Para obter a referência de configuração completa, consulte [Personalizar configuração do cache](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration).

* Normalizar parâmetros de rastreamento: durante a temporada de festas, é provável que você execute campanhas sociais e pagas, como Google Ads, Facebook e X, que anexam sequências de rastreamento exclusivas a cada URL. Cada string exclusiva cria uma entrada de cache separada para a mesma página, o que diminui a taxa de ocorrência do cache. Adicione esses parâmetros à lista **[!UICONTROL Parâmetros de URL Ignorados]** na configuração [!DNL Fastly] no Administrador do Adobe Commerce para que [!DNL Fastly] os trate como equivalentes.
* Confirme se as páginas de aterrissagem podem ser armazenadas em cache: verifique o cabeçalho de resposta `x-cache` em cada página de aterrissagem de promoção. Uma página armazenável em cache retorna `HIT` ou um par `HIT`/`MISS` em cargas subsequentes. Se o cabeçalho retornar `MISS, MISS`, a página não está sendo armazenada em cache e requer investigação.
* Usar solicitações GET para consultas GraphQL: se você executar uma loja PWA ou headless, envie consultas GraphQL como `GET` solicitações com a consulta incluída na URL, em vez de como `POST` solicitações. [!DNL Fastly] armazena em cache somente `GET` solicitações em que a consulta é parte da URL. Uma solicitação `GET` com a consulta enviada no corpo não é armazenada em cache.

>[!NOTE]
>
>A blindagem de origem [!DNL Fastly] também afeta o desempenho do cache. Para obter detalhes sobre a configuração, consulte [Fastly origin shielding](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

## Habilitar Fastly IO (Somente na nuvem) {#enable-fastly-io}

A E/S [!DNL Fastly] descarrega o redimensionamento da imagem e a conversão de formato para a rede de borda [!DNL Fastly], em vez da origem Adobe Commerce. Isso reduz a carga do servidor e melhora a velocidade de renderização da página para vitrines com muitas imagens, um gargalo comum durante períodos de vendas de alto tráfego. Para obter opções de configuração, consulte [Fastly image otimization](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization).

Antes de começar, confirme se a blindagem de origem está configurada. [!DNL Fastly] A E/S exige a blindagem de origem como pré-requisito. Para obter detalhes sobre a configuração, consulte [Fastly origin shielding](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

Para habilitar E/S de [!DNL Fastly]:

1. No Administrador, vá para a página **[!UICONTROL Configuração do Fastly]** e selecione **[!UICONTROL Configurar]** ao lado de **[!UICONTROL Opções de configuração de E/S padrão]**.
1. Confirme se o trecho de E/S [!DNL Fastly] está habilitado.
1. Na configuração **[!UICONTROL Otimização de Imagem]**, defina **[!UICONTROL Habilitar otimização de imagem profunda]** como *[!UICONTROL Sim]*. Esta configuração desabilita o redimensionamento de imagem interno do Adobe Commerce e transfere a tarefa para [!DNL Fastly].
1. Confirme se a localização da blindagem está definida corretamente. Para obter detalhes sobre a configuração, consulte [Fastly origin shielding](#fastly-origin-shielding).

>[!NOTE]
>
>A otimização de imagem profunda redimensiona apenas imagens de produtos. As imagens do CMS, como banners e blocos de conteúdo, não são afetadas e continuam a usar o redimensionamento integrado do Adobe Commerce.

Para verificar se a E/S de [!DNL Fastly] está funcionando, verifique os cabeçalhos de resposta em uma solicitação de imagem do produto:

* O cabeçalho `x-cache` retorna `HIT`.
* Os cabeçalhos `fastly-io-info` e `fastly-stats` estão preenchidos.
* A URL da imagem não inclui um diretório `/cache/` no caminho.

## Implementação do cache Redis L2 {#implement-redis-l2-cache}

Implemente práticas eficazes de armazenamento em cache para que sua loja funcione de maneira confiável durante as estações de pico do tráfego. [!DNL Redis] O cache L2 reduz a largura de banda da rede para [!DNL Redis], armazenando os dados do cache localmente em cada nó da Web. Para obter informações sobre como funciona o cache L2, consulte [Cache de Nível dois](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/level-two-cache).

No Commerce na infraestrutura em nuvem, habilite isso definindo a variável de implantação `REDIS_BACKEND`. Para obter as etapas de configuração, consulte [REDIS_BACKEND](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend) no Guia de Infraestrutura do Commerce na Nuvem. No local, configure-o diretamente em `app/etc/env.php`.

>[!NOTE]
>
>Não há suporte para [!DNL Redis] como back-end do cache L2 no Adobe Commerce 2.4.9 ou posterior, ou em versões de patch posteriores a 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 ou 2.4.8-p4. Nessas versões, use `VALKEY_BACKEND`.

## Habilitar conexões subordinadas do MySQL e do Redis (somente Cloud) {#enable-mysql-and-redis-slave-connections}

As conexões subordinadas [!DNL Redis] e [!DNL MySQL] descarregam o tráfego de leitura nos nós de réplica, reduzindo a carga na conexão principal durante períodos de tráfego alto. Para obter as etapas de configuração, consulte [MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection) e [REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection) ou [VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection), dependendo da versão do Adobe Commerce.

### Conexões Redis slave

Uma conexão slave [!DNL Redis] é uma conexão somente leitura com uma instância [!DNL Redis], permitindo que o tráfego de leitura seja veiculado a partir de um nó não mestre. Sem ele habilitado, [!DNL MySQL] pode sofrer um afunilamento de carga alta. Verifique o gráfico Visão geral de APM de [!DNL New Relic] quanto ao aumento do tempo de resposta como um sinal antecipado, em seguida, confirme na guia **[!UICONTROL Banco de dados]** classificando pela transação mais demorada para identificar consultas lentas de [!DNL MySQL] `SELECT`. Habilite isso definindo a variável de implantação `REDIS_USE_SLAVE_CONNECTION` como `true`.

>[!NOTE]
>
>Há suporte para `REDIS_USE_SLAVE_CONNECTION` somente em ambientes de cluster de Preparo e Produção Pro. Não é compatível com projetos de arquitetura Starter ou Dimensionado (dividido). Habilitá-la na arquitetura Escalonada causa [!DNL Redis] erros de conexão. Use o cache L2 [!DNL Redis] nessa arquitetura. Consulte [Implementar o cache L2 Redis](#implement-redis-l2-cache-implement-redis-l2-cache) acima.

### Conexões subordinadas do MySQL

Habilite o sinalizador `MYSQL_USE_SLAVE_CONNECTION` em ambientes de cluster Pro para direcionar consultas específicas ao banco de dados somente leitura para uma conexão subordinada, descarregando a execução da consulta da conexão mestre.

>[!CAUTION]
>
>Faça um teste de carga antes de ativar qualquer uma das configurações na produção. Em ambientes com carga normal, as conexões escravas podem reduzir o desempenho em 10 a 15%. Em ambientes com carga pesada e sustentada, eles podem melhorar o desempenho por uma margem semelhante. Avalie o tráfego no pico da temporada esperado antes de habilitar.

## Habilitar ordem assíncrona e processamento de email {#enable-asynchronous-order-and-email-processing}

Use o processamento assíncrono para enfileirar e executar operações de alto volume relacionadas a ordens em segundo plano, reduzindo a latência de front-end durante picos de tráfego. Isso abrange três configurações relacionadas, mas distintas. Consulte [Práticas recomendadas de configuração](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration) para obter uma visão geral.

* Posicionamento assíncrono de pedido: o módulo de Pedido assíncrono marca um pedido como recebido, o coloca em uma fila e processa pedidos primeiro a entrar, primeiro a sair. Ela está desativada por padrão. Habilite-o na linha de comando:

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  Depois de habilitado, os detalhes do pedido não ficam disponíveis imediatamente, o pedido permanece na fila até que o consumidor `placeOrderProcess` o verifique no inventário (habilitado por padrão) e o atualize. Antes de desabilitar esse módulo, verifique se todos os pedidos assíncronos em andamento terminaram o processamento. Para obter detalhes, consulte [Práticas recomendadas de desempenho de check-out](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/high-throughput-order-processing).

* Processamento assíncrono de dados de pedidos: vendas intensivas de vitrine e processamento intensivo de pedidos podem entrar em conflito no nível do banco de dados. Ativar essa configuração distingue os dois padrões de tráfego, de modo que os pedidos são colocados no armazenamento temporário e movidos em massa para a grade do Order Management sem colisões. Essa programação atualiza, por cron, as grades Ordens, NFFs, Entregas e Avisos de Crédito, evitando bloqueios e reduzindo o tempo de processamento. Para obter melhores resultados, configure o cron para ser executado uma vez a cada minuto.

  >[!NOTE]
  > 
  >A maneira como você habilita isso depende do modo de implantação. Os ambientes de Preparo e Produção da infraestrutura em nuvem do Adobe Commerce são executados no modo de Produção por padrão, onde essa configuração não está disponível por meio do Administrador. No modo de Produção, execute `bin/magento config:set dev/grid/async_indexing 1`. No modo Padrão, vá para **[!UICONTROL Lojas]** > **[!UICONTROL Configuração]** > **[!UICONTROL Avançado]** > **[!UICONTROL Desenvolvedor]** > **[!UICONTROL Configurações de Grade]** e defina **[!UICONTROL Indexação Assíncrona]** como *[!UICONTROL Habilitar]*.

  Para obter detalhes, consulte [Operações de ordem agendadas](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations).

* Notificações por email assíncronas: essa configuração move notificações por email de check-out e processamento de pedido para o segundo plano. Habilite-o em **[!UICONTROL Lojas]** > **[!UICONTROL Configuração]** > **[!UICONTROL Vendas]** > **[!UICONTROL Emails de Vendas]** > **[!UICONTROL Configurações Gerais]** > **[!UICONTROL Envio Assíncrono]**.

## Configurar indexadores para atualização programada {#configure-indexers-for-update-on-schedule}

Defina indexadores para serem executados no modo agendado para evitar o bloqueio do banco de dados e melhorar a capacidade de resposta durante atualizações frequentes do catálogo. Para obter detalhes, consulte [Práticas recomendadas para configuração de indexador](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration).

Um indexador pode ser executado no modo **[!UICONTROL Atualizar ao Salvar]** ou **[!UICONTROL Atualizar na Agenda]**.

* **[!UICONTROL Atualizar ao Salvar]** indexa imediatamente sempre que o catálogo ou outros dados forem alterados. Ele assume baixa intensidade de atualização e navegação e pode causar atrasos significativos e indisponibilidade de dados em carga alta.
* **[!UICONTROL Atualizar na Agenda]** é recomendado para produção. Ele armazena informações sobre atualizações de dados e reindexações em segundo plano por meio de uma tarefa cron dedicada.

Defina o modo de atualização de cada indexador independentemente em **[!UICONTROL Sistema]** > **[!UICONTROL Ferramentas]** > **[!UICONTROL Gerenciamento de Índice]**.

>[!IMPORTANT]
>
>Os modos com suporte do indexador `customer_grid` dependem da versão do Adobe Commerce. Em versões anteriores à 2.4.8, a Grade de Clientes oferece suporte somente a **[!UICONTROL Atualização ao Salvar]**—não a defina como **[!UICONTROL Atualização agendada]**. No Adobe Commerce 2.4.8 e posterior, a Grade de Clientes oferece suporte a ambos os modos e agora o padrão é **[!UICONTROL Atualizar na Programação]**.

## Desabilitar e avaliar tabela simples de catálogo {#disable-and-evaluate-catalog-flat-table}

Não se recomenda a utilização de mesas planas para produtos e categorias. Esse recurso obsoleto pode causar degradação de desempenho e problemas de indexação. Para obter detalhes, consulte [Catálogos simples](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/catalog-flat).

Para desabilitar o catálogo simples, vá para **[!UICONTROL Lojas]** > **[!UICONTROL Configuração]** > **[!UICONTROL Catálogo]** > **[!UICONTROL Catálogo]** > **[!UICONTROL Vitrine]**, defina **[!UICONTROL Usar Categoria de Catálogo Simples]** como *[!UICONTROL Não]*, defina **[!UICONTROL Usar Produto de Catálogo Simples]** como *[!UICONTROL Não]* e clique em **[!UICONTROL Salvar Configuração]**.

Alguns módulos e personalizações de terceiros exigem tabelas simples para funcionar corretamente. Avalie o impacto e o risco de continuar usando essas extensões antes de desativar as tabelas simples.

## Considere a arquitetura dimensionada (dividida) (somente na nuvem) {#consider-scaled-split-architecture}

Se, após aplicar a configuração anterior e as otimizações em nível de código, o teste de carga ou o desempenho da infraestrutura em tempo real ainda mostrar o CPU e outros recursos no limite máximo, considere mudar para uma arquitetura dimensionada (dividida). Para obter detalhes, consulte [Arquitetura em escala](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture).

>[!NOTE]
>
>A arquitetura dimensionada está disponível somente para contas com um cluster Pro 48 ou superior.

A arquitetura de camada dividida usa no mínimo seis nós: três nós de serviço executando [!DNL OpenSearch] ou [!DNL Elasticsearch], [!DNL MariaDB] e [!DNL Redis] ou [!DNL Valkey], e três nós da Web executando `php-fpm` e `NGINX`.

* Os nós de serviço podem ser dimensionados apenas verticalmente, aumentando o tamanho do servidor (CPU e memória). Como o cluster de banco de dados é criado para alta disponibilidade, os nós de serviço não podem ser dimensionados horizontalmente de forma confiável.
* Os nós da Web podem ser dimensionados vertical e horizontalmente, adicionando servidores da Web para lidar com um maior volume de solicitações.

Isso permite expandir a infraestrutura sob demanda por períodos de alta carga, dimensionando cada nível independentemente. Para mudar para a arquitetura de nível dividido antes de um período de carga pesada esperado, entre em contato com a equipe de conta da Adobe.
