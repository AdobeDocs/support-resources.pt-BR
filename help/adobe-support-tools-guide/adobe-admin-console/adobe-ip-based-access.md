---
title: Limitar o acesso ao produto por endereços IP
description: Use o acesso baseado em IP para controlar o acesso do usuário aos produtos da Adobe e restringir o uso a intervalos de IP públicos aprovados.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---


# Limitar o acesso ao produto por endereços IP

Aplicável à empresa.

Use o acesso baseado em IP para controlar o acesso dos usuários aos produtos da Adobe e impedir o uso não autorizado de endereços IP públicos não listados.

Acesse o [Admin Console](https://adminconsole.adobe.com/settings/identity) para adicionar endereços IP públicos confiáveis ao incluo na lista de permissões **acesso baseado em IP** para uso seguro de aplicativos e serviços Adobe.

## Benefícios do acesso baseado em IP

O controle de acesso baseado em IP usa um incluo na lista de permissões de endereço IP para limitar o uso de produtos Adobe de endereços IP públicos aleatórios. O acesso baseado em IP se aplica a todos os diretórios e aos produtos associados na Adobe Admin Console.

Você pode adicionar IPs públicos confiáveis à lista **Endereços IP permitidos** para impedir que os usuários:

- Acessar produtos de IPs públicos que estejam fora dos intervalos de IP permitidos
- Entrando no Adobe [perfis de usuário](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html) de IPs públicos fora dos intervalos de IP permitidos
- Alternar perfis de usuário em aplicativos Web fora dos intervalos IP permitidos

  ![Exportar estrutura da organização](./assets/ip-based-access.avif)

## Habilitar acesso baseado em IP

### Considerações importantes

>[!Iconsiderações importantes]
>
>- Os administradores devem começar adicionando seu próprio endereço IP público e depois adicionar outros intervalos IP. Caso contrário, você poderá enfrentar um erro.
>- O acesso baseado em IP não se aplica a endereços IP privados.

Você pode adicionar até 150 intervalos de IP públicos diferentes somente no formato CIDR.

Siga estas etapas para habilitar o acesso baseado em IP no seu Adobe Admin Console:

1. Vá para a seção **[!UICONTROL Configurações do Adobe Admin Console](https://adminconsole.adobe.com/settings/identity)**.
2. Selecione e expanda **[!UICONTROL Privacidade e segurança]** no menu de seleção e selecione **[!UICONTROL Configurações de autenticação]**.
3. Na seção **[!UICONTROL Acesso baseado em IP]**, selecione o botão **[!UICONTROL Adicionar endereço IP]**.
4. Na janela **[!UICONTROL Adicionar endereço IP]**:
   - Insira os endereços IP públicos ou o bloco CIDR a ser adicionado ao incluo na lista de permissões.
   - Use uma vírgula para separar vários endereços IP.
   - Selecione **[!UICONTROL Salvar]**.

   Atualmente, só há suporte para o formato IPv4. Veja alguns exemplos:
   - Endereço IP v4: 1.3.4.6
   - Endereço de sub-rede IP v4: 1.2.0.0/24

Seus endereços IP serão adicionados em alguns minutos. Os usuários associados verão a restrição na próxima vez que tentarem entrar ou alternar perfis fora dos endereços IP públicos permitidos. Recomendamos que você informe seus usuários antes dessa alteração.

É possível editar ou remover qualquer endereço IP listado selecionando as opções de edição ou exclusão ao lado de cada entrada.

>[!NOTE]
>
>- Quando o acesso baseado em IP está habilitado, **não ocorre logout forçado**. Os usuários só são afetados quando tentam selecionar o perfil restrito ao entrar ou alternar o perfil na Web.
>- Se você estiver usando um gateway da Web seguro, certifique-se de que todo o tráfego seja roteado através dele. Exiba a [lista de domínios a serem permitidos](https://helpx.adobe.com/enterprise/kb/network-endpoints.html) para que os aplicativos e serviços da Adobe funcionem corretamente.
>- Se você estiver bloqueado na Admin Console porque inseriu um endereço IP inválido, entre em contato com o [Atendimento ao cliente da Adobe](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html).

## Participe da conversa

Para colaborar, fazer perguntas e conversar com outros administradores, visite nossa [Comunidade de Empresas e Equipes](https://www.adobe.com/go/entcom).
