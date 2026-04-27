---
title: Insights do sistema
description: Os System Insights identificam proativamente possíveis problemas em ambientes Adobe Commerce. A análise de insights durante a criação de casos reduz o tempo de resolução, ajuda a evitar paralisações e oferece suporte a uma implantação estável e segura.
source-git-commit: 4172c364c9bfffaae13759da882d03daa15d0754
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---

# Insights do sistema

Os Insights do sistema fornecem descobertas proativas que ajudam a identificar possíveis problemas de desempenho, segurança e funcionalidade em uma configuração de produto do Adobe. Esses insights apresentam riscos como degradação de desempenho, vulnerabilidades de segurança ou configurações incorretas com base em dados de telemetria coletados de ferramentas de observabilidade, incluindo APIs, New Relic e [!DNL Splunk].

Os insights do sistema aparecem durante o processo de criação de casos e ajudam a acelerar o diagnóstico e a resolução.

## Como os Insights do Sistema são criados

As equipes da Adobe analisam continuamente problemas comuns de suporte e tendências emergentes. Com base nessas descobertas, a Adobe adiciona verificações automatizadas ao sistema.

Essas verificações examinam a configuração do produto para detectar problemas, como configurações incorretas, tarefas paralisadas ou condições que possam resultar em problemas funcionais ou paralisações do sistema.

Quando uma verificação identifica um valor ou estado fora do intervalo de segurança definido pelas equipes de produto e suporte da Adobe, o sistema o exibe como um Insight do sistema.

## Por que os insights do sistema são importantes

A revisão regular dos Insights do sistema ajuda a identificar problemas antecipadamente, antes que afetem a estabilidade do sistema ou a experiência do cliente. Essa abordagem proativa:

- Aumenta a confiabilidade da plataforma
- Reduz o tempo de inatividade
- Ajuda a manter as práticas recomendadas pela Adobe

## Disponibilidade e escopo

Os Insights do sistema estão disponíveis somente para o Adobe Commerce. Esses insights aparecem durante o processo de criação de casos no Suporte da Experience League e também estão disponíveis por meio da [Ferramenta de Análise do Site (SWAT)](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/site-wide-analysis-tool/intro).

> [ !NObservação]
>
>Os Insights do sistema exibem dados somente de ambientes de produção.

## Acesso ao System Insights

Os Insights do sistema são exibidos em todo o fluxo de trabalho de criação de casos. À medida que os detalhes do problema são inseridos, o painel **[!UICONTROL Insights do Sistema]** é exibido no lado direito da tela, abaixo da seção de recomendações habilitadas por IA. Para saber mais sobre as recomendações habilitadas por IA, consulte [Preencher o tíquete de suporte](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket) no artigo Experiência de suporte ao cliente da Adobe.

O painel exibe uma lista rolável de insights com escopo para a instância do projeto específica. O escopo é baseado nas informações inseridas no campo **[!UICONTROL URL do projeto]**. Insira a **[!UICONTROL URL do projeto]** com precisão para garantir que os insights reflitam o ambiente correto.

Depois que o painel é carregado, ele exibe uma lista rolável de cartões insight sinalizados para o seu ambiente. Cada cartão insight inclui:

- Um título que resume o problema
- Uma breve descrição do insight

![Acessar Recursos de Suporte](/help/adobe-support-tools-guide/assets/access-support-resources.png)

Para visualizar todos os detalhes do insight, selecione um cartão insight na lista. A view detalhada fornece as seguintes informações:

- Nome do insight
- Produto do Adobe no qual a insight está sinalizada
- Tipo de insight, categorizado como:
   - [!UICONTROL Funcionalidade]
   - [!UICONTROL Desempenho]
   - [!UICONTROL Segurança]
- [!UICONTROL Nível de risco] indicando a gravidade
- [!UICONTROL Última Execução de Verificação] indica quando a descoberta foi detectada.
- [!UICONTROL Insight Source], fornecido pela Ferramenta de Análise do Site (SWAT)
- Uma explicação detalhada do problema e seu impacto potencial, juntamente com etapas acionáveis para investigar e resolver o problema. A exibição detalhada também explica as causas típicas desse tipo de problema e inclui links para a documentação relevante do Adobe para referência adicional.

![Clique no Cartão de Ocorrência](/help/adobe-support-tools-guide/assets/click-case-card.png)

Revise todos os insights no painel antes de continuar, pois um insight pode abordar diretamente o problema que está sendo experimentado.

## Realizar ações em uma insight

Depois de revisar uma insight, escolha uma das seguintes ações.

### Continuar criação de caso

Se o problema persistir ou exigir assistência adicional, selecione **[!UICONTROL Continuar criação de caso]**. O sistema retém todas as informações de caso inseridas anteriormente.

### Marcar problema como resolvido

Se a insight resolver o problema e um caso de suporte não for mais necessário, selecione **[!UICONTROL Problema resolvido]**.

Quando esta opção é selecionada:

- Uma caixa de diálogo de confirmação é exibida.
- A caixa de diálogo indica que todos os dados de caso inseridos serão apagados permanentemente.

![Ação em um insight](/help/adobe-support-tools-guide/assets/issue-resolved.png)

Selecione **[!UICONTROL Concluído]** para confirmar e retornar à página **[!UICONTROL Meus Casos]**. Selecione **[!UICONTROL Cancelar]** para retornar à exibição detalhada do insight.

![Limpar Formulário de Maiúsculas e Minúsculas](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## Fornecer feedback sobre uma insight

Na parte inferior de cada exibição detalhada do insight, é possível fornecer feedback sobre a utilidade da insight. Este feedback ajuda a Adobe a melhorar continuamente a relevância e a precisão dos insights do sistema.

![Fornecer feedback](/help/adobe-support-tools-guide/assets/submit-feedback.png)

Para fornecer feedback:

1. Abra uma visualização detalhada do insight.
2. Role até a parte inferior do painel.
3. Localizar o prompt **[!UICONTROL Isso foi útil? Enviar comentários.]**
4. Selecione uma das seguintes opções:
   - Ícone de **Aumentar** se a insight foi útil
   - Ícone de **Polegar para baixo** se a insight não foi útil
5. (Opcional) Informe comentários adicionais.
6. Selecione **[!UICONTROL Enviar]** para enviar comentários ou **[!UICONTROL Ignorar]** para fechar a seção de comentários sem enviar.
