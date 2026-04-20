---
title: Como obter e aplicar o [!UICONTROL patch de segurança]
description: Este artigo fornece instruções sobre como obter e aplicar um [!UICONTROL patch de segurança] que foi lançado, mas as instruções não estão disponíveis.
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: eee15976f3dd402e84774ec5b769d952259c8dff
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Como obter e aplicar um [!UICONTROL patch de segurança]

>[!NOTE]
>Se você tiver uma instalação no local e não estiver usando sistemas de controle de versão como o [!DNL CVS] ou o GitHub para gerenciar seu código, talvez o host da Web possa ajudá-lo a aplicar o patch. Entre em contato com eles para obter apoio.

Este artigo fornece instruções sobre como obter e aplicar um [!UICONTROL patch de segurança] que foi lançado, mas as instruções não estão disponíveis.

## Produtos e versões afetados

Infraestrutura em nuvem e no local do Adobe Commerce - todas as versões compatíveis


## Causa

A maioria dos [!UICONTROL patches de segurança] foram lançados sem nenhum patch ou hotfix isolado para serem aplicados e exigirão a atualização para a versão [!UICONTROL patch de segurança].

Para os boletins de segurança do Adobe Commerce, a Adobe fornece apenas um arquivo de patch/hotfix físico separado quando é explicitamente publicado/mencionado como parte do lançamento do boletim. Se o boletim não incluir (ou fazer referência) um pacote de patch/hotfix isolado, não poderemos gerar e fornecer um após o fato.

Isso ocorre porque as correções de segurança são desenvolvidas, testadas e enviadas juntas como parte da versão de segurança compatível (por exemplo, uma versão de patch) e não foram projetadas para serem claramente separadas/dissociadas em arquivos de patch CVE individuais sem correr o risco de cobertura incompleta ou regressões.

O caminho de remediação compatível permanece aplicando a atualização de segurança oficial para sua linha de versão (ou atualizando para uma versão que inclui as correções).

## Solução


### Caso I:

* Se um arquivo/hotfix de patch isolado for mencionado nas [Notas de Versão](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite), baixe o arquivo da seção de download de [https://account.magento.com](https://account.magento.com/downloads/view/). Os usuários com acesso compartilhado devem primeiro receber privilégios de download do proprietário da conta/titular da licença.

**Avisos:**

Se você estiver em uma versão mais antiga do Adobe Commerce (2.4.4), terá recebido automaticamente o Suporte estendido. Sua versão deve ser uma das seguintes versões não suportadas para poder aplicar os patches de segurança mais recentes disponíveis:

2.4.4 - 2.4.4-p11

Versões não compatíveis (2.3.x, 2.4.0 - 2.4.3) não são elegíveis para suporte e você deve primeiro atualizar para uma versão compatível para aproveitar as correções de segurança mais recentes.

Se você não tiver o suporte estendido, poderá solicitar suporte para compartilhar os patches com você, mas eles não poderão resolver nenhum problema/erro que você possa encontrar ao aplicá-los.

### Caso II:

Os patches isolados são fornecidos apenas em casos excepcionais, e não é a forma preferida de implementar correções de segurança.

Se um arquivo/hotfix de patch isolado não for mencionado nas Notas de versão:

* **Nuvem:**

1. Alguns [!UICONTROL patches de segurança] podem ser incluídos/lançados na versão mais recente do Conjunto de Ferramentas da Nuvem (Ferramentas ECE) em Patches da Nuvem para o Commerce - verifique as [Notas de versão](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) e, se uma correção de segurança for mencionada na versão, atualize o pacote para essa versão.
1. Se as Notas de versão não mencionarem uma correção de segurança, continue lendo.

* **Infraestrutura em nuvem ou no local:**

* Se um arquivo/hotfix de patch isolado não estiver disponível, [atualize a versão do Adobe Commerce na infraestrutura de nuvem](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X para a versão de patch mais recente 2.4.X-pY.
* Se um arquivo/hotfix de patch isolado não estiver disponível, [atualize a versão do Adobe Commerce no local](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X para a versão de patch mais recente 2.4.X-pY.

## Leitura relacionada

* Consulte as [Notas de versão do Conjunto de ferramentas do Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) no *Guia de Infraestrutura do Adobe Commerce na Nuvem*.
* Consulte [Atualizar a versão do Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) no *Guia de Infraestrutura do Adobe Commerce on Cloud*.
