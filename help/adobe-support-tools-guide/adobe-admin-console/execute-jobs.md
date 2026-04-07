---
title: Executar trabalhos pendentes
description: Saiba como executar tarefas pendentes na Adobe Admin Console para garantir que todas as alterações sejam aplicadas à organização.
exl-id: 18549d19-7985-4a45-8894-e69836ddb23c
source-git-commit: 9085108231aaa46d8417d346686c211ea48f6b81
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Executar trabalhos pendentes

Este recurso se aplica às organizações corporativas que usam o [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/).

- As alterações no [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) foram concluídas em duas fases:

   1. **Editar fase**: fazer alterações nas organizações ou alocar produtos.
   2. **Fase de execução**: revise e execute as alterações pendentes para que elas entrem em vigor.

- Para garantir que todas as alterações feitas em [[!DNL Global Admin Console]](https://helpx.adobe.com/br/enterprise/global-admin-console/adopt-global-administration.html) sejam implementadas e tenham efeito, selecione a guia **[!UICONTROL Execução do Trabalho]** e continue com a execução das alterações pendentes.

  Entre no [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/).

## Persistência e visibilidade das alterações

### Alterar persistência

- Você pode sair e retornar mais tarde sem perder as alterações pendentes.
- Alterações não executadas:
   - São descartadas após 30 dias.
   - São limpas quando a sessão termina, como quando a guia ou a janela do navegador é fechada.

&#x200B;> [!NOTE]
>
> Execute rapidamente alterações importantes para garantir que elas sejam aplicadas com êxito.

### Vários administradores e conflitos

- Dois administradores que trabalham na mesma organização:
   - Não ver as alterações não executadas umas das outras.
   - Consulte as alterações somente após:
      - Execução e
      - Atualizando a exibição ou fazendo logon novamente.
- As alterações não executadas podem entrar em conflito com as alterações já executadas.

### Tratamento de conflitos

Os conflitos são relatados:
- No momento da execução ou
- Quando os dados são atualizados (por exemplo, depois de sair e entrar novamente).

## Executando alterações pendentes

Como administrador global, você pode revisar e executar alterações pendentes na guia **[!UICONTROL Execução do trabalho]**.

### Etapas para executar as alterações

1. Entre no [!DNL Global Admin Console].
2. Selecione a guia **[!UICONTROL Execução do trabalho]** no painel de navegação esquerdo.
3. Revise as alterações pendentes.
4. Selecione **[!UICONTROL Enviar alterações]** para executá-las.

Depois de submeter o job:

- O job entra na fila de execução.
- O status é **[!UICONTROL Pendente]** enquanto o trabalho é executado.
- A Adobe recomenda executar apenas uma tarefa de cada vez para proporcionar previsibilidade e facilitar a solução de problemas.

&#x200B;> [!IMPORTANT]
>
> Se ocorrer um erro durante a execução, as alterações que não foram aplicadas com êxito deverão ser inseridas novamente e reenviadas.

### Alocações de longa duração

Se uma alocação de produto levar mais de 12 horas:
- O trabalho está marcado como **[!UICONTROL Com Falha]**.
- As tarefas pendentes subsequentes nesse trabalho não são executadas.

![trabalhos pendentes](assets/pending-jobs.png)

## Cancelar um trabalho em execução

Você pode cancelar um trabalho em execução na guia **[!UICONTROL Execução do Trabalho]**.

### Etapas para cancelar um trabalho em execução

1. Entre no [!DNL Global Admin Console].
2. Selecione **[!UICONTROL Execução do Trabalho]**.
3. Selecione **[!UICONTROL Cancelar Trabalho Em Execução]**.

### Comportamento de cancelamento

1. O trabalho é interrompido no final da etapa atual.
2. A tarefa não para no meio de uma etapa.
3. Algumas etapas podem levar minutos ou horas para serem concluídas.
4. Durante este tempo, o trabalho pode permanecer em um estado **[!UICONTROL Cancelando]**.

&#x200B;> [!NOTE]
>
> Planeje cancelamentos com o entendimento de que a conclusão da etapa atual pode atrasar significativamente quando a tarefa for interrompida.

## Exibir histórico de tarefas

- Para exibir ordens de produção executadas nos últimos 30 dias:

   1. Entre no [!DNL Global Admin Console].
   2. Selecione **[!UICONTROL Execução do Trabalho]**.
   3. Role até a parte inferior da página.
   4. Selecione **[!UICONTROL Trabalhos Recentes]**.

- Os trabalhos recentes são exibidos:
   - **comandos de trabalho** enviados.
   - **Erros** e **avisos** associados à execução.

&#x200B;> [!NOTE]
>
> Renomeações ou exclusões subsequentes de objetos relacionados **não afetam** como os comandos são exibidos no histórico de trabalhos. O histórico reflete o estado no momento do envio.
