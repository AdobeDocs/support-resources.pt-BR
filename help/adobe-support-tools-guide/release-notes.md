---
title: Notas de versão de suporte do Experience League
description: As informações mais recentes da versão sobre o suporte da Experience League.
feature: Release Notes
exl-id: 875ad82e-56b5-4d58-9237-bb7aa0d9ffaf
source-git-commit: 26a20998811059cf66d8609c0ae7ac2816df3337
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 1%

---

# Notas de versão de suporte do Experience League

Essas notas de versão contêm atualizações para o suporte da Experience League e incluem:

![Novos](../adobe-support-tools-guide/assets/new.svg) Novos recursos
![Correção](../adobe-support-tools-guide/assets/fix.svg) Correções e melhorias
![Bug](../adobe-support-tools-guide/assets/bug.svg) Problemas conhecidos


## 27 de abril de 2026 - Gerenciamento de escalonamento e aprimoramentos do System Insights para o Adobe Commerce

### Gestão de encaminhamento

1. O gerenciamento de atendimento de segundo nível do suporte da Experience League oferece um novo conjunto de recursos de autoatendimento para oferecer maior visibilidade dos casos de suporte com um fluxo de trabalho simplificado e orientado pelo sistema, criado de acordo com as suas necessidades.

1. Obtenha um instantâneo instantâneo do seu caso de suporte, alimentado por IA, incluindo o status atual, as próximas etapas, as principais atualizações e um resumo completo do caso sem precisar ler todo o histórico do caso.

1. A nova opção **[!UICONTROL Obter ajuda]** oferece uma experiência centralizada para que os clientes colaborem perfeitamente com as equipes de suporte — abrangendo solução de problemas, solicitações de retorno de chamada, atualizações de urgência de problemas de autoatendimento e solicitações de atenção gerencial.

1. **[!UICONTROL Solicite Chamada Imediata]** - Para casos P1-Críticos, solicite um retorno de chamada imediato de um Engenheiro de Suporte Técnico diretamente da sua lista de casos. Basta fornecer seu número de telefone e uma breve descrição do problema. Um engenheiro de suporte entrará em contato assim que estiverem disponíveis.

1. **[!UICONTROL Solicitar uma Chamada Agendada]** - Para casos P2-Urgentes e P3-Importantes, agende uma reunião da Web com um Engenheiro de Suporte Técnico em uma data e hora adequadas para você. Uma sessão de compartilhamento de tela do Microsoft Teams será confirmada com todos os detalhes da reunião após a reserva.

1. **[!UICONTROL Alteração na Urgência do Problema]** - Para casos P3-Importantes e P4-Menores, o autoatendimento encaminha a prioridade do seu caso de P4-Menor para P2-Urgente, fornecendo uma breve justificativa. Uma solicitação de alteração de prioridade pode ocorrer sem o ticket, resultando em reatribuição.

1. **[!UICONTROL Tenho um Problema Não Listado]** - Para todas as prioridades, gere um escalonamento para qualquer cenário não coberto pelas opções acima, como **[!UICONTROL Tempo de Resolução]**, **[!UICONTROL A Resolução não atendeu às expectativas]**, **[!UICONTROL Habilidades de Comunicação com o Agente]** ou **[!UICONTROL Conhecimento Técnico do Agente]**.

### Insights do sistema no formulário de criação de caso para o Adobe Commerce

1. O System Insights exibe automaticamente os problemas detectados em seu ambiente. Inclui reduções de desempenho, riscos de segurança e erros de configuração usando dados de telemetria de APIs, New Relic e [!DNL Splunk]. Isso o ajuda a identificar e resolver problemas com mais rapidez.

1. Atualmente, os Insights do sistema estão disponíveis exclusivamente para o suporte da Adobe Commerce no Experience League durante o processo de criação do caso.

1. Os insights têm como escopo sua instância de projeto específica, garantindo que as informações exibidas sejam relevantes para o seu ambiente.

1. Os insights incluem uma descrição detalhada, etapas para resolver, análise da causa principal e links para a documentação relevante do Adobe.

1. Os usuários podem enviar feedback sobre insights individuais para ajudar a Adobe a melhorar continuamente a precisão e a relevância dos insights do sistema.

## 23 de abril de 2026 - Expansão da solicitação para o recurso de retorno de chamada

O recurso Solicitação de retorno de chamada agora está disponível para usuários de produtos do Analytics, Admin Console, Audience Manager e Target.

## 8 de abril de 2026 - Expansão da solicitação para o recurso de retorno de chamada

O recurso Solicitação de retorno de chamada agora está disponível para usuários de produtos do Marketo.

## 30 de março de 2026 - Formulário aprimorado de ocorrência

![Novo](../adobe-support-tools-guide/assets/new.svg) O formulário de ocorrência é organizado em um fluxo guiado que ajuda os usuários a compreender quais informações são necessárias em cada estágio:

- [!UICONTROL Seleção de produto]
- [!UICONTROL Descrição do problema]
- [!UICONTROL Informações do sistema]
- [!UICONTROL Prioridade e impacto nos negócios]
- [!UICONTROL Informações de contato e Lista de observadores]
- [!UICONTROL Revisar e enviar]

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionada a geração automática de título com base na **[!UICONTROL Descrição do Problema]**, permitindo que o título seja gerado automaticamente, enquanto ainda oferece aos usuários a opção de editá-lo antes de enviar a ocorrência.

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou um **[!UICONTROL &quot;O problema pode ser reproduzido?&quot;]** para ajudar a melhorar a solução de problemas. Se os usuários selecionarem **[!UICONTROL Sim]**, serão solicitados a fornecer as etapas executadas para reproduzir o problema. Se *Não* for selecionado, os usuários poderão continuar com o envio do caso.

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionada uma opção para indicar se alterações recentes foram feitas no ambiente ou na instância. Se **[!UICONTROL Sim]** for selecionado, os usuários serão solicitados a fornecer detalhes adicionais sobre as alterações.

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou **[!UICONTROL Contexto de Ambiente] Campos** adicionais para os produtos autorizados a capturar detalhes críticos:

- **Marketo**
   - ID do Munchkin
- **Adobe Target**
   - Nome da atividade
   - URL do site (Nome da propriedade das tags)
- **Adobe Analytics**
   - RSID
   - URL do site (Nome da propriedade das tags) / cURL
   - Workspace Shortlink
- **Adobe Journey Optimizer (AJO)**
   - ID de Jornada ou ID de URL/campanha ou ID de URL/canal ou ID de URL/Offer Decisioning ou URL
   - Exemplo de perfil
   - Nome da sandbox
- **Real-Time Customer Data Platform (RTCDP)**
   - ID do componente afetado (ID de destino/ID de público-alvo/ID de conjunto de dados/ID de fluxo de dados/ID de política de mesclagem/ID de esquema/ID do Source/ID do lote)
   - Exemplo de perfil
   - Nome da sandbox
- **Adobe Experience Platform (AEP)**
   - ID do componente afetado (ID de destino/ID de público-alvo/ID de conjunto de dados/ID de fluxo de dados/ID de política de mesclagem/ID de esquema/ID do Source/ID do lote)
   - Exemplo de perfil
   - Nome da sandbox
- **Customer Journey Analytics (CJA)**
   - URL do projeto Workspace
   - ID da conexão / Mensagem de erro / Código
   - ID da visualização de dados

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou um **Painel do Recommendations[!UICONTROL Orientado por IA]** para exibir orientações úteis sem interromper o fluxo de criação de casos.

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou uma etapa do **[!UICONTROL Resumo da Revisão]** para fornecer uma exibição consolidada de todas as informações inseridas e permitir que os usuários:

- Revisar detalhes do caso em um local
- Voltar às etapas anteriores para fazer edições
- Retornar ao resumo sem perder o progresso

![Correção](../adobe-support-tools-guide/assets/fix.svg) Renomeou o campo Descrição de Ocorrência como *[!UICONTROL &quot;Descreva o problema&quot;]* para maior clareza.

![Correção](../adobe-support-tools-guide/assets/fix.svg) Adição de asteriscos (*) como indicadores de campo obrigatórios para garantir a integridade e reduzir erros de envio.

## 18 de março de 2026 - Expansão da solicitação para o recurso de retorno de chamada

O Experience League agora oferece uma opção de Solicitação de retorno de chamada, permitindo o agendamento de reuniões na Web de autoatendimento com recursos de compartilhamento de tela para resolução mais rápida de problemas.

- Esse recurso está disponível para o Adobe Experience Manager, Campaign e Workfront.
- Os clientes podem agendar reuniões conforme sua conveniência e receber convites instantâneos.
- Para casos de Adobe Experience Manager P1, retornos de chamada imediatos garantem um engajamento mais rápido durante problemas críticos, ajudando a minimizar o tempo de inatividade e o impacto nos negócios.
