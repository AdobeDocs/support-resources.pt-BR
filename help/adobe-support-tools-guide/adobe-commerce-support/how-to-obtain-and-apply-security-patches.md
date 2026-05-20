---
title: Como obter e aplicar o [!UICONTROL patch de segurança]
description: Este artigo fornece instruções sobre como obter e aplicar um [!UICONTROL patch de segurança] que foi lançado, mas as instruções não estão disponíveis.
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 9a4d96e06b949e4c229fdf0f084810b27bf8b346
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Como obter e aplicar um [!UICONTROL patch de segurança]

>[!NOTE]
>Se você tiver uma instalação no local e não estiver usando sistemas de controle de versão como o [!DNL CVS] ou o GitHub para gerenciar seu código, talvez o host da Web possa ajudá-lo a aplicar o patch. Entre em contato com eles para obter apoio.

Este artigo fornece instruções sobre como obter e aplicar um [!UICONTROL patch de segurança] que foi lançado, mas as instruções não estão disponíveis.

## Produtos e versões afetados

Infraestrutura em nuvem e no local do Adobe Commerce - todas as versões compatíveis


## Causa

Para os boletins de segurança do Adobe Commerce, o Adobe fornece apenas um arquivo de patch isolado ou hotfix separado quando esse artefato é lançado explicitamente como parte do boletim. Se nenhum patch ou hotfix isolado for publicado ou referenciado nos materiais de informativo, a Adobe não criará um patch independente depois.

Isso ocorre porque as correções de segurança são projetadas, validadas e lançadas juntas como parte da versão de segurança compatível para a linha de versão aplicável.

Portanto, o caminho de remediação compatível é aplicar a atualização de segurança oficial para a linha de versão afetada ou atualizar para uma versão que já contém a correção.

## Solução


### Caso I:

* Se um arquivo/hotfix de patch isolado for mencionado nas [Notas de Versão](https://experienceleague.adobe.com/pt-br/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite), baixe o arquivo da seção de download de [https://account.magento.com](https://account.magento.com/downloads/view/). Os usuários com acesso compartilhado devem primeiro receber privilégios de download do proprietário da conta/titular da licença.

**Avisos:**

* O Adobe Commerce 2.4.6 continua sendo compatível com o suporte estendido até 30 de agosto de 2027.

* O Adobe Commerce 2.4.5 permanece no Suporte estendido até 11 de agosto de 2026. Após essa data, a Adobe fornecerá correções de segurança somente até 31 de maio de 2027.

* O Adobe Commerce 2.4.4 não está mais sob Suporte estendido. O Adobe fornece correções de segurança somente até 31 de maio de 2027.

* Para o Adobe Commerce 2.4.4 e 2.4.5, o Adobe fornece apenas arquivos de patch de segurança. Essas atualizações não incluem:

   * Suporte ou assistência de engenharia da Adobe Commerce
   * Patches de qualidade
   * Atualizações de dependência de plataforma ou sistema operacional

Versões não compatíveis (2.3.x e 2.4.0-2.4.3) não estão qualificadas para suporte. Você pode atualizar para uma versão compatível para receber as correções de segurança mais recentes.

### Caso II:

Os patches isolados são fornecidos apenas em casos excepcionais e não são o método preferido para implementar correções de segurança.

Se um arquivo de patch ou hotfix isolado não for mencionado nas Notas de versão, siga estas diretrizes:

>[!IMPORTANT]
>
>Se um arquivo de patch ou hotfix isolado não for lançado explicitamente por um problema de segurança, atualize o aplicativo Adobe Commerce completo para a versão de patch aplicável mais recente para a linha de lançamento afetada.

**Nuvem:**

1. Alguns [!UICONTROL patches de segurança] podem ser incluídos/lançados na versão mais recente do Conjunto de Ferramentas da Nuvem (Ferramentas ECE) em Patches da Nuvem para o Commerce - verifique as [Notas de versão](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) e, se uma correção de segurança for mencionada na versão, atualize o pacote para essa versão.
1. Se as Notas de versão não mencionarem uma correção de segurança, continue lendo.

**Infraestrutura em nuvem ou no local:**

* Se um arquivo/hotfix de patch isolado não estiver disponível, [atualize a versão do Adobe Commerce na infraestrutura de nuvem](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X para a versão de patch mais recente 2.4.X-pY.
* Se um arquivo/hotfix de patch isolado não estiver disponível, [atualize a versão do Adobe Commerce no local](https://experienceleague.adobe.com/pt-br/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X para a versão de patch mais recente 2.4.X-pY.

## Leitura relacionada

* Consulte as [Notas de versão do Conjunto de ferramentas do Commerce Cloud](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) no *Guia de Infraestrutura do Adobe Commerce na Nuvem*.
* Consulte [Atualizar a versão do Adobe Commerce](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) no *Guia de Infraestrutura do Adobe Commerce on Cloud*.
