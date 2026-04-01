---
title: Criar relatórios de atribuição de licença para várias organizações e produtos
description: Gerar, exibir e baixar relatórios de atribuição de licença em várias organizações e produtos da Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e3380a89-8529-473f-bd17-efb05466eab9
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Criar relatórios de atribuição de licença para várias organizações e produtos

Saiba como os administradores globais podem gerar e baixar relatórios de licença detalhados para várias organizações e produtos para intervalos de datas específicos a fim de facilitar o rastreamento preciso do provisionamento de licenças.

>[!NOTE]
>
>Para criar, exibir e exportar um relatório de atribuição de licença, entre no [Global Admin Console](https://global-admin-console.adobe.com/) e vá para **[!UICONTROL Insights]** > **[!UICONTROL Relatórios]** > **[!UICONTROL Atribuição de licença]**.

## Criar um relatório

Os relatórios de atribuição de licença ajudam você a monitorar proativamente o provisionamento de licenças e reduzir o rastreamento manual. Os administradores globais podem criar um relatório de atribuição de licença para produtos selecionados para qualquer número de organizações secundárias para monitorar os dados de provisionamento de licença de software em todos os departamentos.

1. Vá para a guia **[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)** na Global Admin Console.
1. Na página **[!UICONTROL Atribuição de licença]**, selecione **[!UICONTROL Criar relatório]**.
1. Selecione as organizações e selecione **[!UICONTROL Próximo]**. Você pode escolher individualmente cada organização ou selecionar todas as organizações secundárias dentro de um pai usando o botão **[!UICONTROL Selecionar tudo]**.

   >[!NOTE]
   >
   >**Saiba por que você não pode selecionar determinadas organizações**:
   >Se uma organização secundária não tiver um contrato ou tiver um contrato empresarial separado com o mesmo produto da organização principal, ela será desativada para criar um relatório de atribuição de licença. Por exemplo, se o contrato da organização principal tiver Adobe Acrobat e a organização secundária tiver o mesmo como parte de outro contrato, o produto será limitado para alocação. Como resultado, também é limitado para a criação de relatórios no Global Admin Console. [Saiba como rastrear o provisionamento dessas organizações usando a respectiva Admin Console](https://helpx.adobe.com/br/enterprise/using/assignment-reports.html).

   >[!NOTE]
   >
   >Você pode criar relatórios de atribuição somente para organizações com um contrato ativo.

1. Selecione os produtos a serem incluídos no relatório e selecione **[!UICONTROL Próximo]**.

   >[!NOTE]
   >
   >**Saiba por que não é possível selecionar determinados produtos**:
   >Os produtos que não podem ser alocados na Global Admin Console não são incluídos na criação do relatório. Atualmente, isso inclui alguns produtos da Digital Experience, como o [!DNL Workfront], o [!DNL Adobe Experience Manager] e o [!DNL Adobe Experience Platform], e também produtos como o [!DNL Adobe Firefly Services], o [!DNL Acrobat Sign] e o [!DNL Adobe Stock]. [Use o Adobe Admin Console para localizar os dados de provisionamento de licença desses produtos](https://helpx.adobe.com/br/enterprise/using/assignment-reports.html).

1. Selecione se deseja agregar o relatório por mês ou ano.
1. Selecione um intervalo de datas personalizado ou escolha entre opções predefinidas. Você pode escolher qualquer data de início de 18 de junho de 2020 até o dia anterior, desde que não seja anterior à data de início do contrato.
1. Selecione **[!UICONTROL Baixar]** para exportar o relatório como um arquivo CSV.

O relatório inicia o processamento e aparece na página **[!UICONTROL Atribuição de licença]** com detalhes como nome, criador, hora de criação, intervalo de datas e status. Quando estiver pronto, você receberá uma notificação por email e o relatório será baixado automaticamente.

Qualquer administrador global pode baixar o relatório a qualquer momento depois que ele estiver pronto, usando o ícone **[!UICONTROL Baixar]** ao lado do nome do relatório.

>[!NOTE]
>
>- Para garantir que os dados mais recentes sejam refletidos, gere relatórios 48 horas após qualquer alocação.
>- Os relatórios são retidos por 90 dias após serem gerados.

## Visualizar e baixar relatórios gerados anteriormente

Os administradores globais podem exibir e baixar os relatórios de atribuição de licença gerados por qualquer outro administrador global em sua organização. No entanto, visualizadores globais só podem exibir a lista de relatórios de atribuição de licença.

1. Vá para a guia **[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)** na Global Admin Console.
1. Na página **[!UICONTROL Atribuição de licença]**, todos os relatórios são listados com os seguintes detalhes:

   | Campo | Descrição |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | Nome | Gerado automaticamente e não pode ser editado. |
   | Criador | O administrador global que gerou o relatório. |
   | Hora de criação | A hora do sistema em que o relatório foi criado. |
   | Intervalo de data | O intervalo de datas selecionado para o relatório. |
   | Status | **Êxito** se o relatório estiver pronto para download ou **Processamento** se ele ainda estiver sendo gerado. |

1. Para exportar o relatório como um arquivo CSV, selecione o ícone **[!UICONTROL Baixar]** ao lado do relatório.

## Conhecer seu relatório de atribuição de licença

O relatório que você baixou contém as seguintes informações para cada evento:

| Campo | Descrição |
| -------------------------------- | -------------------------------------------------------- |
| ID da organização | ID exclusiva vinculada à organização principal |
| Nome da organização | Nome da organização principal |
| ID da organização secundária | Identificador exclusivo da organização secundária selecionada |
| Nome da organização secundária | Nome da organização secundária |
| ID da licença | Identificador exclusivo para a licença do produto |
| Nome do produto | Nome do produto selecionado |
| Data | Seleção de data |
| Quantidade total de licenças | Número total de licenças no nível da organização principal |
| Licenças secundárias | Contagem de licenças alocada à organização secundária |
| Quantidade máxima atribuída mensal/anual | Valor agregado do provisionamento de licenças (mensal/anual) |
