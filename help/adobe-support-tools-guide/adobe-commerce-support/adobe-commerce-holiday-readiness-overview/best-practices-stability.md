---
title: Práticas recomendadas e estabilidade
description: Práticas recomendadas e recomendações de estabilidade para ajudar os comerciantes do Adobe Commerce a preparar seus ambientes para eventos de alto tráfego, como a temporada de festas.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-wordcount: '861'
ht-degree: 4%
---

# Práticas recomendadas e estabilidade

Esta seção fornece recomendações técnicas para preparar ambientes do Adobe Commerce, tanto Commerce na infraestrutura em nuvem quanto no local, para eventos de alto tráfego, como a temporada de festas.

>[!NOTE]
>
>As etapas marcadas **(Somente na nuvem)** se aplicam ao Commerce na infraestrutura em nuvem. A maioria das outras recomendações também se aplica a implantações locais.

## Atualizar para a versão mais recente do Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

Verifique se o site não está em uma versão não compatível do Adobe Commerce, o que pode afetar o desempenho do site e aumentar a vulnerabilidade a problemas de segurança. Atualize para a versão mais recente do Adobe Commerce para estar seguro e pronto para a temporada de festas.

A [última versão](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/release/notes/overview) do Adobe Commerce inclui várias [correções críticas de segurança](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/release/notes/security-patches/overview), incluindo aprimoramentos e problemas atenuados, que beneficiarão seu projeto ao atualizar de uma versão anterior.

Para obter mais informações sobre versões não compatíveis do Adobe Commerce, reveja a [Política de Ciclo de Vida do Adobe Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/release/planning/lifecycle-policy).

## Instale as ferramentas ECE-Tools e Quality Patch Tool (QPT) mais recentes {#install-latest-ece-tools-and-quality-patch-tool-qpt}

Verifique se o módulo `ece-tools` mais recente e seus módulos dependentes estão instalados, usando o switch `--with-dependencies`, para que todos os patches de nuvem necessários estejam instalados corretamente para sua versão do Adobe Commerce. Para obter as etapas, consulte [Atualizar o pacote ECE-Tools](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package).

Revise a lista de patches disponível na Ferramenta de patches de qualidade e certifique-se de que os patches de desempenho compatíveis com sua versão do Adobe Commerce foram aplicados. Consulte [Ferramenta de Patches de Qualidade: Pesquisar por patches](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview).

>[!NOTE]
>
>O QPT está disponível para o Adobe Commerce na infraestrutura em nuvem e instalações locais. Os comandos de instalação e uso diferem entre os dois - para a nuvem, o QPT está incluído no pacote ECE-Tools.

## Revisar e limpar arquivos de log {#review-and-clean-log-files}

Revise os arquivos de log no ambiente de nuvem (por exemplo, arquivos de log de aplicativo em `~/var/log`) e identifique todos os registros frequentemente registrados que estão sendo gravados nos arquivos de log padrão ou personalizados. Para obter detalhes, consulte [Exibir e gerenciar logs](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

* Revise os seguintes arquivos de log padrão e corrija erros recorrentes: `~/var/log`, `~/var/log/exception.log`, `~/var/log/support_report.log`, `~/var/log/system.log`, `~/var/report`.
* Remova os logs de depuração que foram adicionados anteriormente para solucionar problemas anteriores.

Esses logs também estão disponíveis em [!DNL New Relic], consulte [gerenciamento de logs do New Relic](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Monitorar o crescimento do tamanho do disco {#monitor-disk-size-growth}

Sua infraestrutura do Adobe Commerce na nuvem tem dois volumes de disco principais. Monitore esses volumes para garantir que eles tenham espaço livre suficiente quando houver tráfego intenso. O Adobe Commerce fornece um aviso quando qualquer um dos volumes atinge mais de 70% de uso.

* `/mnt/shared` (arquivos compartilhados, incluindo logs e arquivos de mídia)
* `/data/mysql` (volume do banco de dados)

Para obter detalhes, consulte [Gerenciar espaço em disco](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space).

## Revisar as solicitações mais lentas do banco de dados {#review-slowest-database-requests}

É importante monitorar e revisar regularmente as transações de banco de dados mais demoradas em [!DNL New Relic]. Investigar consultas e componentes significativamente lentos.

* **Verifique as transações que consomem mais tempo:** Vá para **[!UICONTROL New Relic]** > **[!UICONTROL APM e Serviços]** > selecione o ambiente > **[!UICONTROL Bancos de Dados]** e classifique pelas transações que consomem mais tempo.

* **Verifique o log de consultas lentas do MySQL:** Consulte `mysql-slow.log` para ver se há consultas lentas registradas pelo sistema. Estes logs também estão disponíveis em [!DNL New Relic]: vá para **[!UICONTROL New Relic]** > **[!UICONTROL Logs]** e filtre por `filePath:"/var/log/mysql/mysql-slow.log"`.

Revise os [!DNL MySQL] logs de consulta lenta regularmente para confirmar se as consultas lentas não estão sendo executadas com frequência. Para obter as etapas para resolver consultas que você identificou como problemáticas, consulte [Resolver problemas de desempenho do banco de dados](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues).

## Configurar trabalhos cron {#configure-cron-jobs}

Todas as operações assíncronas no Commerce são executadas usando o comando cron do Linux.

O Commerce depende da configuração adequada do trabalho cron para funções importantes do sistema, incluindo indexação e operações de consumidor de fila. Se não for configurado corretamente, o Commerce não funcionará conforme esperado.

É crítico que o cron do Commerce esteja configurado corretamente, usando o usuário Unix apropriado no arquivo crontab Unix. Cada usuário Unix tem seu próprio arquivo crontab, que é a configuração usada para executar tarefas cron para esse usuário. Para etapas, consulte [Configurar e executar trabalhos cron](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs).

O script `dev/tools/cron.sh` não pode mais ser executado porque foi removido.

## Otimizar configurações do lado do cliente {#optimize-client-side-settings}

Para melhorar a capacidade de resposta da vitrine eletrônica da sua instância do Commerce, defina as seguintes configurações em **[!UICONTROL Lojas]** > **[!UICONTROL Configuração]** > **[!UICONTROL Avançado]** > **[!UICONTROL Desenvolvedor]**, que estão disponíveis apenas no Modo de desenvolvedor:

* **[!UICONTROL Configurações de Grade]** > **[!UICONTROL Indexação assíncrona]**: *[!UICONTROL Habilitar]*
* **[!UICONTROL Configurações de CSS]** — **[!UICONTROL Minificar Arquivos CSS]**: *[!UICONTROL Sim]*
* **[!UICONTROL Configurações do JavaScript]** — **[!UICONTROL Minificar Arquivos do JavaScript]**: *[!UICONTROL Sim]*
* **[!UICONTROL Configurações do JavaScript]** — **[!UICONTROL Habilitar o JavaScript Bundling]**: *[!UICONTROL Sim]* (não habilitado por padrão)
* **[!UICONTROL Configurações de Modelo]** — **[!UICONTROL Minificar HTML]**: *[!UICONTROL Sim]*

Como o Adobe Commerce na nuvem sempre é executado no modo de Produção, defina cada opção na linha de comando, por exemplo, `bin/magento config:set --lock-config dev/css/minify_files 1`, e confirme a alteração `app/etc/config.php` resultante e reimplante. Para obter a lista completa de caminhos CLI, consulte [Otimizar arquivos de recursos](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files).
