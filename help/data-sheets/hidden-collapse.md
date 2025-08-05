---
title: Recolher bug de seções
description: Seções recolhíveis UGP-13446 não renderizáveis, talvez devido a guias de página incorporadas
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# Seções flexíveis

<http://jira.corp.adobe.com/browse/UGP-13446> Seções recolhíveis UGP-13446 não renderizáveis, talvez devido a guias de página incorporadas

## Exemplos

Primeiro com guias de página; segundo sem

### Opção 2: com guias de página

+++ Instalação manual de Hotfix do 6.5.18.0 - 6.5.22.0

**Etapa 1: baixar e extrair o pacote de Hotfix**

- Baixe o [hotfix de 6.5.18.0 - 6.5.22](https://www.adobe.com) do Portal de Distribuição de Software da Adobe
- Extrair localmente

**Etapa 2: Navegar até a Pasta de Versão Correta**

- Com base na versão do Service Pack instalada em seu ambiente, vá para a pasta correspondente.

  Exemplo para o Service Pack 20: a pasta é:

  ```
  <extracted-hotfix>/SP20/
  ```

**Etapa 3: Localizar o Diretório de Implantação**

- No AEM Forms no servidor JEE, acesse:

  ```
  [AEM installation directory]/deploy
  ```

  Exemplo: `adobe/adobe-experience-manager-forms/deploy`



**Etapa 4: atualizar e substituir os arquivos EAR**

>[!BEGINTABS]

>[!TAB JBoss]

1. Abrir `adobe-core-jboss.ear` e substituir `adminui.war` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. Dentro do `adobe-core-jboss.ear`, vá para a pasta `lib/` e substitua `adobe-uisupport.jar` por:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salve o EAR. Verifique se as alterações foram salvas corretamente.


1. Substituir `adobe-edcserver-jboss.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. Substituir `adobe-forms-jboss.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. Abrir `adobe-core-weblogic.ear` e substituir `adminui.war` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. Dentro do `adobe-core-weblogic.ear`, substitua `adobe-uisupport.jar` por:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salve o EAR. Verifique se as alterações foram salvas corretamente.


1. Substituir `adobe-edcserver-weblogic.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. Substituir `adobe-forms-weblogic.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. Abrir `adobe-core-websphere.ear` e substituir `adminui.war` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. Dentro do `adobe-core-websphere.ear`, substitua `adobe-uisupport.jar` por:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salve o EAR. Verifique se as alterações foram salvas corretamente.


1. Substituir `adobe-edcserver-websphere.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. Substituir `adobe-forms-websphere.ear` por

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   Por exemplo, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**Etapa 5: atualizar `adobe-rightsmanagement-<appserver>-dsc.jar`arquivo com**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Por exemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Etapa 6: Configuração Adicional para Segurança de Documentos no WebSphere e no WebLogic**:

Se você estiver usando a Segurança de documentos (antigo Rights Management), defina a seguinte propriedade do sistema Java (argumento JVM) antes de iniciar o servidor do AEM Forms:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Etapa 7: executar novamente o Gerenciador de Configurações**

- Inicie o Configuration Manager para reimplantar o EAR atualizado e aplicar o hotfix

+++

### Opção 2: sem guias de página

+++ Instalação manual de Hotfix do 6.5.18.0 - 6.5.22.0

**Etapa 1: baixar e extrair o pacote de Hotfix**

- Baixe o [hotfix de 6.5.18.0 - 6.5.22](https://www.adobe.com) do Portal de Distribuição de Software da Adobe
- Extrair localmente

**Etapa 2: Navegar até a Pasta de Versão Correta**

- Com base na versão do Service Pack instalada em seu ambiente, vá para a pasta correspondente.

  Exemplo para o Service Pack 20: a pasta é:

  ```
  <extracted-hotfix>/SP20/
  ```

**Etapa 3: Localizar o Diretório de Implantação**

- No AEM Forms no servidor JEE, acesse:

  ```
  [AEM installation directory]/deploy
  ```

  Exemplo: `adobe/adobe-experience-manager-forms/deploy`



**Etapa 4: atualizar e substituir os arquivos EAR**

Guias de página excluídas

**Etapa 5: atualizar `adobe-rightsmanagement-<appserver>-dsc.jar`arquivo com**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Por exemplo, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Etapa 6: Configuração Adicional para Segurança de Documentos no WebSphere e no WebLogic**:

Se você estiver usando a Segurança de documentos (antigo Rights Management), defina a seguinte propriedade do sistema Java (argumento JVM) antes de iniciar o servidor do AEM Forms:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Etapa 7: executar novamente o Gerenciador de Configurações**

- Inicie o Configuration Manager para reimplantar o EAR atualizado e aplicar o hotfix

+++

Localizar
