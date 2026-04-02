---
title: Gerenciar modelos de política no Global Admin Console
description: Saiba como os administradores globais podem aplicar modelos de política a qualquer organização secundária, direta ou indiretamente, a partir da organização em que estão armazenados na Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cf30f2a656ccb28b678ea6fcd8e4d56d7c8a8fb4
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# Gerenciar modelos de política no Global Admin Console

**Aplica-se a:** Empresa

Saiba como os administradores globais podem aplicar modelos de política a qualquer organização secundária, direta ou indiretamente, a partir da organização em que estão armazenados na Global Admin Console.

>[!NOTE]
>
>Na [Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html), selecione uma organização para editar e navegue até a guia **Modelos de Política** para simplificar a configuração e facilitar o gerenciamento consistente de políticas entre organizações.
>
> [Entrar na Global Admin Console](https://global-admin-console.adobe.com/)

## Como os modelos de política funcionam

Os Modelos de política são armazenados com uma organização e ficam visíveis para todos os administradores globais dessa organização. Depois de aplicadas, as entradas do modelo de política são definidas individualmente em cada organização. Quando um modelo de política é aplicado a uma organização, cada uma das entradas no modelo de política é aplicada às políticas da organização, substituindo os valores de política existentes.

### Comportamento de política bloqueado

As atualizações de políticas bloqueadas só serão executadas se o usuário que estiver aplicando a atualização for um administrador global da organização, indicado pelo ícone **[!UICONTROL Bloqueado por]** da política que está sendo atualizada.

Se o usuário que aplicar o modelo tiver permissão para desbloquear a política, os bloqueios de política assumirão os valores do modelo aplicado (bloqueado ou desbloqueado). Se o modelo indicar que o bloqueio deve ser deixado como está, o valor do bloqueio na política permanecerá o mesmo de antes.

### Observação importante sobre como salvar

>[!NOTE]
>
>Ao contrário de outras alterações feitas na Global Admin Console, as edições nos modelos de política têm efeito imediatamente, sem a necessidade de passar pelo processo **[!UICONTROL Revisar alterações pendentes - Enviar]**. No entanto, para implementar alterações pendentes em organizações onde o modelo de política é aplicado, é necessário [enviar](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Criar um modelo de política

1. Na [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização para editar e navegue até a guia **[!UICONTROL Modelos de política]**.
1. Selecione **[!UICONTROL Criar Modelo]**.<br>
   ![Pic1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. Na caixa de diálogo **[!UICONTROL Criar Modelo de Política]**, digite o **nome** e a **descrição** para o modelo de política.<br>O nome do modelo de política pode ter no máximo 100 caracteres.
1. Selecione as políticas a serem incluídas no modelo.
1. Defina valores para as políticas selecionadas (consulte [Definindo Valores de Política](#setting-policy-values) abaixo).
1. Selecione **Salvar**.

### Definição de valores de política {#setting-policy-values}

Para cada política incluída no modelo, defina duas configurações:

* **Permitido/Não permitido:** Defina o controle deslizante para o valor desejado. Saiba mais sobre [detalhes da política](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#policy-details).
* **Valor de bloqueio:** Modifique o estado de bloqueio da política usando uma das seguintes opções:
   * **Bloquear** — A política será bloqueada após a aplicação do modelo.
   * **Desbloquear** — A política será desbloqueada após a aplicação do modelo.
   * **Manter como está** — O estado de bloqueio da política será o mesmo de antes da aplicação do modelo.<br>
     ![Pic2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## Aplicar um modelo a organizações

1. Na [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização para editar e navegue até a guia **[!UICONTROL Modelos de política]**.
1. Selecione o ícone **[!UICONTROL Mais Opções]** ![Mais Opções](./assets/manage-product-profiles_more-options.png) para o modelo de política relevante e selecione **[!UICONTROL Aplicar modelo à organização]**.<br>
   ![Pic3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. Selecione as organizações às quais deseja aplicar o modelo. Você pode selecionar várias organizações.<br>
   ![Pic4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. Selecione **[!UICONTROL Aplicar modelo]**.
1. Para implementar alterações pendentes em organizações às quais o modelo de política é aplicado, selecione **[!UICONTROL Revisar Alterações Pendentes]**. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Se todos os valores de política nas organizações selecionadas já corresponderem aos valores no modelo, será exibida uma mensagem notificando que nenhuma alteração foi feita. Além disso, **[!UICONTROL Revisar alterações pendentes]** não será habilitado se não houver outras edições pendentes.

## Editar um modelo

1. Na [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização para editar e navegue até a guia **[!UICONTROL Modelos de política]**.
1. Selecione o ícone **[!UICONTROL Mais Opções]** ![Mais Opções](./assets/manage-product-profiles_more-options.png) para o modelo relevante e selecione **[!UICONTROL Editar modelo]**.<br>
   ![Imagem5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. Atualize o modelo de política e selecione **[!UICONTROL Atualizar Agora]**.
1. Para implementar alterações pendentes em organizações às quais o modelo de política é aplicado, selecione **[!UICONTROL Revisar Alterações Pendentes]**. Depois de revisar, selecione **[!UICONTROL Enviar alterações]** para [executá-las](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Excluir um modelo

1. Na [Global Admin Console](https://global-admin-console.adobe.com/), selecione uma organização para editar e navegue até a guia **[!UICONTROL Modelos de política]**.
1. Selecione o ícone **[!UICONTROL Mais Opções]** ![Mais Opções](./assets/manage-product-profiles_more-options.png) para o modelo relevante e selecione **[!UICONTROL Excluir Modelo]**.<br>
   ![Imagem6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. Selecione *Sim* na caixa de diálogo exibida.
