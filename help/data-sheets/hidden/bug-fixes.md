---
title: Correções de erros (ocultas)
description: Página de teste para fins de teste interno
hide: true
hidefromtoc: true
source-git-commit: 0279a8985376d587b470bf81fbe8958a5679afb5
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 4%

---

# Correções de erros

## UGP-10560 - Emblemas em seções recolhíveis

+++ Versões anteriores

### Versão V1.16

_13 de fevereiro de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Os vídeos de produtos agora são compatíveis com a API de serviço de catálogo.
![Correção](assets/package.png) Agora há suporte para pacotes de produtos com preços fixos.
![Correção](assets/package.png) As opções indisponíveis agora são mostradas no widget PDP.

#### Limitações conhecidas

Estes recursos ainda não são compatíveis:

* O tamanho máximo para a carga de atributos dinâmicos é de 9 MB.
* Preço de produto de grupo. Pode ser calculada com preços simples de produtos.
* Em uma matriz de imagens, somente a primeira imagem contém funções.

As seguintes limitações podem ser resolvidas usando a API Mesh e a Core GraphQL API:

* Preço Mínimo Anunciado
* [Nível de preços](https://www.adobe.com)

### Versão V1.13

_sexta-feira, 12 de outubro de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) O Serviço de catálogo oferece suporte ao `inStock` sinalizador para grades de produtos.
![Novo](assets/package.png) `urlKey` e `externalId` foram adicionados ao esquema do GraphQL.
![Novo](assets/package.png) Produtos e cartões-presente baixáveis agora são compatíveis.

### Versão V1.12

_quarta-feira, 19 de setembro de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](https://www.adobe.com).
![Correção](assets/package.png) Esta versão contém correções de erros e melhorias no lado do serviço.

### Versão V1.11

_quarta-feira, 18 de julho de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) O Serviço de catálogo agora é compatível com o [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) Consulta do GraphQL para Recommendations do produto.

### Versão V1.10

_quarta-feira, 27 de junho de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) A API do Serviço de catálogo agora é compatível com &quot;produtos relacionados&quot;.

### Versão V1.7

_quinta-feira, 12 de abril de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) O Serviço de catálogo agora limpa as variantes de produtos excluídas.
![Correção](assets/package.png) Aprimoramentos de desempenho e escalabilidade da infraestrutura.

### Versão V1.6

_quarta-feira, 28 de março de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Adição de amostras à [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) consulta.
![Novo](https://www.adobe.com).

### Versão V1.5

_terça-feira, 6 de março de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Adicionado [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) funcionalidade do GraphQL.
![Correção](assets/package.png) Melhor desempenho e escalabilidade da API.

### Versão V1.4

_quarta-feira, 7 de fevereiro de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Metappackage do serviço de catálogo publicado para simplificar as etapas de instalação.
![Correção](assets/package.png) Melhorias na escalabilidade e no desempenho da API.

### Versão V1.3

_quarta-feira, 17 de janeiro de 2023_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Simplificação e melhoria da experiência de integração.
![Novo](assets/package.png) Novos pontos de extremidade de sandbox do cliente estão disponíveis para testes de pré-produção.
![Novo](assets/package.png) Suporte adicionado para produtos virtuais.
![Correção](assets/package.png) Melhorias na escalabilidade e no desempenho da API.

### Versão V1.1

_sábado, 18 de novembro de 2022_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) O Serviço de catálogo agora é compatível com o Adobe [API Mesh](https://developer.adobe.com/graphql-mesh-gateway/).
![Correção](assets/package.png) Melhor escalabilidade da API e desempenho geral.

### Versão V1.0

_quarta-feira, 4 de outubro de 2022_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Agora oferecem suporte a produtos agrupados.
![Novo](assets/package.png) Adição de substituições de visibilidade B2B. Agora os produtos podem ser pesquisados e adicionados ao carrinho para grupos específicos de clientes.
![Correção](assets/package.png) O serviço agora está mais estável e melhorou o desempenho.

### Versão 0.3 - Beta+

_terça-feira, 12 de setembro de 2022_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) Suporte a imagens para variantes: as imagens do produto são retornadas com base nas opções selecionadas
![Novo](assets/package.png) Funções para suporte a preços: permite que somente membros de grupos de clientes específicos vejam o preço dos produtos
![Correção](assets/package.png) Melhor estabilidade e desempenho do serviço
![Novo](assets/package.png) As atualizações são recebidas quando os produtos são excluídos do catálogo

### Versão Beta

_9 de agosto de 2022_

[!BADGE Compatível]{type=Informative tooltip="Suportado"}

![Novo](assets/package.png) A variável `products` e `refineProduct` queries retornam os seguintes dados:

* Atributos de produto predefinidos (sistema).
* Atributos dinâmicos do produto e filtrá-los por função (página de exibição do produto/página da lista de produtos).
* Opções de produto.
* Imagens de produto e filtrá-las por função (PDP/PLP).
* Um preço específico para produtos simples e faixas de preço para produtos configuráveis.
* Preços de grupo e faixas de preços do cliente. Eles retornam um preço padrão de fallback para os compradores sem um grupo de clientes.
* Tipos de produto que usam preços específicos do cliente B2B.

+++

## UGP-10565 - Destaque de texto

Texto anterior `<div class="preview">`

<div class="preview">

### Adicionar campos nativos do Workfront

Você pode adicionar campos nativos Workfront aos seus formulários personalizados. Quando o formulário personalizado é anexado a um objeto, o campo é preenchido a partir dos dados do objeto. Por exemplo, o campo Descrição em um formulário personalizado anexado a um projeto extrairá a descrição do projeto. (O campo pode mostrar &quot;N/D&quot; se nenhum dado estiver disponível.)

1. No lado esquerdo da tela, localize **Campo nativo** e arraste-a para uma seção na tela.
1. No lado direito da tela, configure as opções do campo personalizado:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Rótulo</td> 
      <td> <p>(Obrigatório) Digite um rótulo descritivo para exibir acima do campo. Você pode alterar o rótulo a qualquer momento.</p> <p><b>IMPORTANTE</b>: Evite usar caracteres especiais neste rótulo. Eles não são exibidos corretamente nos relatórios.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nome</td> 
      <td> <p>(Obrigatório) Esse nome é a forma como o sistema identifica o campo.</p><p> Ao configurar o campo pela primeira vez e digitar o rótulo, o campo Nome é preenchido automaticamente para corresponder a ele. Mas os campos Label e Name não são sincronizados — isso dá a você a liberdade de alterar o rótulo que seus usuários veem sem precisar alterar o nome que o sistema vê.</p>
      <p><b>IMPORTANTE</b>:
      <ul> 
      <li>Embora seja possível fazer isso, recomendamos que você não altere esse nome depois que você ou outros usuários começarem a usar o formulário personalizado no Workfront. Se você fizer isso, o sistema não reconhecerá mais o campo onde ele pode agora ser referenciado em outras áreas do Workfront.</p> </li>
      <li> <p>Cada nome de campo deve ser exclusivo na instância do Workfront da organização. Dessa forma, é possível reutilizar um que já foi criado para outro formulário personalizado.</p> </li>
      <li><p>Recomendamos que você não use o caractere ponto no nome do campo personalizado para evitar erros ao usar o campo em diferentes áreas do Workfront.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Instruções</td> 
      <td> <p>Digite quaisquer informações adicionais sobre o campo. Quando os usuários preencherem o formulário personalizado, poderão passar o mouse sobre o ícone de ponto de interrogação para exibir uma dica de ferramenta contendo as informações digitadas aqui.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Campo de referência</td> 
      <td><p>(Obrigatório) Selecione um campo nativo do Workfront.<p><p>Somente campos nativos para os objetos do formulário estão disponíveis. Por exemplo, se a lista Tipos de objeto na parte superior do designer do formulário mostrar Projeto, você poderá selecionar campos nativos para projetos, mas não campos específicos para tarefas.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Tamanho</td> 
      <td>(Opcional) Altere o tamanho de exibição do campo, conforme necessário.</td> 
     </tr> 
    </tbody> 
   </table>

1. Para salvar as alterações, clique em **Aplicar** e vá para outra seção para continuar criando seu formulário.

   ou

   Clique em **Salvar e fechar**.

</div>

Texto depois do realce

## UGP-10566 - O texto do link é menor do que o texto normal em tabelas de HTML

Consulte também UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>Entrada em</td>
<td>Descrição</td>
<td>Disponível para </td>
</tr>
<tr> 
    <td role="rowheader">Rótulo</td> 
    <td> <p>(Obrigatório) Digite um rótulo descritivo para exibir acima do campo personalizado. Você pode alterar o rótulo a qualquer momento. Para obter mais informações, consulte <a href="https://www.adobe.com" class="MCXref xref">Adicionar um campo personalizado a um formulário personalizado</a> neste artigo.</p> <p><b>IMPORTANTE</b>: Evite usar caracteres especiais neste rótulo. Eles não são exibidos corretamente nos relatórios.</p> </td> 
    <td>
    <ul>
    <li>Botões de opção. Para obter mais informações, consulte <a href="https://www.adobe.com">Adicionar um campo personalizado a um formulário personalizado</a> neste artigo. (Sem classe)</li>
    <li>Grupos de caixa de seleção</li>
    <li>Lista suspensa</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Erro antigo

A tag &quot;span&quot; não está funcionando muito bem em uma NOTA (e lista)

Para obter informações sobre quais recursos estão disponíveis na nova experiência de comentários e para quais objetos, consulte [Nova experiência de comentários](note-test.md).

1. Vá para o objeto ao qual deseja adicionar uma resposta.
1. Clique em **Atualizações** e, em seguida, clique na guia **Comentários** para o objeto e localize o comentário ou resposta à qual deseja responder

   Ou

   <span class="preview">Clique em **Todos** e clique em **Responder em Comentários** para abrir o comentário na guia Comentários e respondê-lo. Não é possível responder na guia All.</span>

1. (Opcional) Para incluir texto de uma atualização anterior em sua resposta, clique no link **Mais** no canto superior direito do comentário que deseja responder e clique em **Citar resposta**. O texto da atualização anterior é exibido na área de entrada, marcado com uma linha cinza vertical.
1. Clique em **Responder**.

   ![](assets/package.png)

   Você pode ver os usuários que estão ativamente envolvidos na conversa na parte inferior da **Adicionar resposta...** e você poderá adicionar ou remover as que não são mais relevantes. Esses usuários, juntamente com quaisquer usuários que se inscreveram no objeto, recebem uma notificação sempre que uma atualização ou resposta é feita no objeto. Você também pode adicionar tags a mais usuários para incluí-los em sua resposta.  Para marcar mais usuários, consulte [Marcar outros usuários em atualizações](note-test.md).

   >[!TIP]
   >
   >   Para adicionar respostas adicionais a uma resposta existente, comece digitando o **Adicionar resposta...** ou clique em **Responder** sobre o comentário original. Sua resposta é adicionada ao final da thread.

1. Comece a digitar sua resposta e use qualquer opção adicional da barra de ferramentas Rich Text. Para obter informações sobre como usar Rich Text ou outros recursos de atualização, consulte [Atualizar trabalho](note-test.md).

1. Clique em **Enviar** para salvar a resposta.

1. (Opcional) Clique no link **Mais** no canto superior direito do comentário ao qual deseja responder para obter mais opções para gerenciar a resposta. Para obter mais informações, consulte [Atualizar trabalho](note-test.md).