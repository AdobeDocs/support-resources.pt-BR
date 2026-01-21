---
title: Notas de versão do novo formulário de caso EXL
description: As informações mais recentes da versão do formulário de caso do EXL.
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 7%

---


# Notas de versão do novo formulário de caso EXL

A nova experiência de criação de casos apresenta um formulário atualizado projetado para simplificar a resolução de problemas e inclui:

![Novidade](../adobe-support-tools-guide/assets/new.svg): novos recursos
![Correção](../adobe-support-tools-guide/assets/fix.svg): correções e melhorias
![Bug](../adobe-support-tools-guide/assets/bug.svg): problemas conhecidos

## Versão 1.0 - Formulário aprimorado de criação de casos

*sexta-feira, 15 de janeiro de 2026*

![Novo](../adobe-support-tools-guide/assets/new.svg) O formulário de caso é organizado em um fluxo guiado, ajudando os usuários a compreender quais informações são necessárias em cada estágio:

- [!UICONTROL Seleção de produto]
- [!UICONTROL Detalhes do problema]
- [!UICONTROL Informações do sistema]
- [!UICONTROL Impacto]
- [!UICONTROL Informações de contato]
- [!UICONTROL Revisar e enviar]

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionado **Novo(s) [!UICONTROL Etapas para Reproduzir] Campo** para capturar detalhes acionáveis e acelerar a solução de problemas.

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou **[!UICONTROL Contexto de Ambiente] Campos** adicionais para os produtos autorizados a capturar detalhes críticos:

- **Marketo**
   - ID do Munchkin
- **Adobe Target**
   - Nome da atividade
   - URL do site (Nome da propriedade das tags) / log HAR ou Assurance
- **Adobe Analytics**
   - RSID
   - URL do site (Nome da propriedade das tags) / Log de HAR ou Assurance / cURL / Log de depuração
   - Workspace shortlink
- **Adobe Journey Optimizer (AJO)**
   - ID de jornada ou URL de Jornada
   - Exemplo de perfil
- **Real-Time Customer Data Platform (RTCDP)**
   - ID do componente afetado (ID de destino, ID de perfil, ID de público-alvo, ID de conjunto de dados ou ID de fluxo de dados)
   - Arquivo HAR / logs do Assurance
- **Customer Journey Analytics (CJA)**
   - Projeto do Workspace
   - Nome da propriedade das tags


![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou um **Painel do Recommendations[!UICONTROL Orientado por IA]** para exibir orientações úteis sem interromper o fluxo de criação de casos.

![Novo](../adobe-support-tools-guide/assets/new.svg) Adicionou uma etapa do [!UICONTROL Resumo da Revisão] para fornecer uma exibição consolidada de todas as informações inseridas e permitir que os usuários:

- Revisar detalhes do caso em um local
- Voltar às etapas anteriores para fazer edições
- Retornar ao resumo sem perder o progresso

![Correção](../adobe-support-tools-guide/assets/fix.svg) Renomeou o Campo de Descrição de Ocorrência como *[!UICONTROL &quot;Descreva o problema&quot;]* para maior clareza.

![Correção](../adobe-support-tools-guide/assets/fix.svg) Adição de asterisco (*) como Indicadores de campo obrigatórios para garantir a integridade e reduzir erros de envio.
