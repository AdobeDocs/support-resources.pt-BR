---
title: Baixar logs de auditoria e exportar relatórios
description: Saiba como os administradores globais visualizam, filtram e exportam logs e relatórios de auditoria na Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 7211d382c6cfba6070c8c3203956a1193f64ffbe
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%

---

# Baixar logs de auditoria e exportar relatórios

Aplicável à empresa.

Saiba como os administradores globais visualizam, filtram e exportam logs e relatórios de auditoria usando o Global Admin Console.

Para começar, entre na [Global Admin Console](https://global-admin-console.adobe.com/). Em seguida, vá para a guia **[!UICONTROL Insights]** e selecione **[!UICONTROL Logs de auditoria]** para acompanhar todas as alterações feitas entre organizações.

## Exibir e baixar logs de auditoria

Como administrador global, você tem total visibilidade das alterações feitas na Global Admin Console. Você pode pesquisar logs de auditoria em todas as organizações para ações tomadas nos últimos 90 dias, incluindo quando ocorreram e quem as executou.
- Os logs de auditoria ajudam a garantir a conformidade contínua, protegendo contra acesso inadequado ao sistema e auditando comportamentos suspeitos em sua organização.
- Os logs disponíveis no Global Admin Console incluem somente eventos que um administrador global pode acessar. Eles não incluem atribuições de usuário ou eventos de usuário. [Saiba mais](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) sobre os diferentes recursos que cada console oferece.
- Os logs abrangem eventos para todas as organizações na hierarquia, permitindo pesquisar logs de auditoria em todas as organizações de uma só vez.

>[!NOTE]
>
> Como administrador do sistema em uma organização do [Adobe Admin Console](https://adminconsole.adobe.com), você pode usar o [Log de Auditoria](https://helpx.adobe.com/enterprise/using/audit-logs.html) para examinar as atribuições de usuários e os eventos de usuários. As ações executadas pelos administradores do sistema em organizações secundárias da organização selecionada também são incluídas nos logs de auditoria. Saiba mais sobre como os administradores do sistema podem [rastrear alterações](https://helpx.adobe.com/enterprise/using/audit-logs.html) feitas na Admin Console.

Para exibir ou baixar logs de auditoria para sua organização:

1. Como administrador global, entre na [Global Admin Console](https://global-admin-console.adobe.com/insights).
1. Selecione **[!UICONTROL Insights]** > **[!UICONTROL Logs de auditoria]**.

Os logs de auditoria exibem as seguintes informações para eventos filtrados:

| Campo | Descrição |
|------ |-------------|
| Data | Data e hora do evento, mostradas no fuso horário local. |
| Nome do evento | Descrição da ação executada. |
| Detalhes do evento | Detalhes adicionais do evento, se disponíveis. |
| Nome do objeto | Nome do produto, perfil do produto ou grupo de usuários envolvidos no evento, conforme aplicável. |
| Usuário afetado | Endereço de email do usuário afetado, se aplicável. |
| Administrador | Endereço de email do administrador que executou a ação. *Sistema* será exibido se a ação tiver sido executada por um sistema de back-end do Adobe. |
| Endereço IP | Endereço IP da máquina em que a ação foi executada. Isso geralmente reflete o local físico, mas pode ser um servidor proxy ou endereço VPN. |
| Organização | Nome da organização afetada pelo evento. |

1. Você pode filtrar logs de auditoria usando as seguintes opções:

   - Pesquisar por usuário ou administrador afetado.
   - Selecione uma ou mais organizações.
   - Defina um intervalo de datas.
   - Filtrar por nome de evento.
   - Combine filtros para restringir resultados, como a exibição de eventos dos últimos sete dias para uma organização específica.

   ![logs de auditoria](assets/audit-logs.png)

   *Filtre os logs de auditoria com base no nome do evento, na organização afetada ou no intervalo de datas.*

   ![selecionar-organização](assets/select-organizations.png)

   *Selecione organizações para filtrar os logs de auditoria.*

1. Para exportar logs de auditoria, selecione **[!UICONTROL Exportar CSV]** para exportar resultados filtrados. Os resultados são baixados no formato CSV.

Para obter detalhes sobre os campos incluídos na exportação, consulte [Esquema de Log](#log-schema).

>[!NOTE]
>
>Os relatórios de log de auditoria exportados são retidos por 90 dias após serem gerados.


## Entender o relatório de log de auditoria {#log-schema}

O relatório de log de auditoria exportado inclui os seguintes campos para cada organização:

| Campo | Descrição |
|------|------------|
| id | ID de evento |
| eventTime | Data e hora do evento (fuso horário local) |
| eventType | Nome do evento |
| eventSubType | Detalhes adicionais do evento, se disponíveis |
| atorEmail | Endereço de email do administrador que executou o evento. *System* será exibido se o evento tiver sido executado por um sistema back-end do Adobe. |
| targetUserEmail | Email do usuário afetado, se aplicável |
| targetGroupName | Grupo de usuários afetado, se aplicável |
| targetProductName | Produto afetado, se aplicável |
| targetProfileName | Perfil de produto afetado, se aplicável |
| ipAddress | Endereço IP da máquina em que a ação foi executada. Normalmente reflete o local físico, mas pode ser um servidor proxy ou endereço VPN. |
| organizationName | Nome da organização afetada |

## Baixar relatórios de exportação

Quando qualquer administrador global exporta dados da organização do [Global Admin Console](https://global-admin-console.adobe.com/insights), o relatório é processado e disponibilizado na guia **[!UICONTROL Insights]** em **[!UICONTROL Exportar Relatórios]**.

Todos os relatórios gerados por qualquer administrador global estão disponíveis em um único local. O recurso de relatórios de exportação é útil nos seguintes cenários:

- Se você tiver uma hierarquia grande com muitas organizações, não precisará mais aguardar o arquivo de exportação ser processado. Você pode usar os relatórios gerados por seus colegas administradores.
- Não é mais necessário manter ou salvar esses relatórios para comparação posterior. Os relatórios são retidos por 90 dias e você pode baixá-los a qualquer momento para comparar relatórios.


Para baixar um relatório de exportação:

1. Faça logon no [Global Admin Console](https://global-admin-console.adobe.com/insights) e navegue até **[!UICONTROL Insights]** > **[!UICONTROL Exportar Relatórios]**.

   Os relatórios gerados nos últimos 90 dias são exibidos. Após 90 dias, você pode gerar o relatório novamente. Saiba como gerar relatórios para [Estrutura de organização](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-the-organization-structure).


   | Campo | Descrição |
   |------|------------|
   | Relatório | Data e hora em que o relatório foi gerado (fuso horário local) |
   | Formato | Formato de arquivo (CSV, JSON, XLSX) |
   | Tamanho | Tamanho do arquivo |
   | Criado por | Endereço de email do administrador que gerou o relatório |
   | Ação | Link para baixar o relatório |

1. Para baixar um relatório, selecione **[!UICONTROL Baixar]**.

   Se o relatório que você acabou de gerar não aparecer na lista, selecione **[!UICONTROL Atualizar]**.

   ![exportar-relatórios](assets/export-reports.png)

*Baixe qualquer relatório gerado nos últimos 90 dias.*
