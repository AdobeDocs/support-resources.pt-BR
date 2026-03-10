---
title: Aviso de fim de suporte do MySQL e orientação de compatibilidade de banco de dados para o Adobe Commerce
description: Este artigo fornece informações sobre as linhas do tempo de fim de suporte do MySQL e orientação de compatibilidade do banco de dados para versões compatíveis do Adobe Commerce.
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Aviso de fim de suporte do MySQL e orientação de compatibilidade de banco de dados para o Adobe Commerce

Este artigo fornece informações importantes sobre o fim do suporte do MySQL (EOS) e a compatibilidade do banco de dados para versões do Adobe Commerce compatíveis.
A Adobe recomenda que os comerciantes analisem este anúncio e tomem medidas para manter a estabilidade da plataforma e permaneçam em conformidade com os requisitos de suporte.
Saiba mais nos [Pré-requisitos de atualização para MariaDB](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) e [Requisitos do sistema](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).

## Fim de Suporte do MySQL 8.0 (EOS)

O MySQL 8.0 atingirá o fim do suporte (EOS) em 30 de abril de 2026.
Após essa data, as seguintes versões do Adobe Commerce não serão compatíveis ou manterão a compatibilidade com versões do MySQL lançadas após o MySQL 8.0:

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

A Adobe não validará ou fornecerá suporte para versões principais mais recentes do MySQL nessas versões do Adobe Commerce.

## Ação necessária para clientes locais

As instalações locais do Adobe Commerce que executam as seguintes versões são altamente recomendáveis para migrar seus servidores de banco de dados para uma versão compatível com o MariaDB:

* 2.4.5
* 2.4.6
* 2.4.7

O MariaDB é totalmente compatível com essas versões e é a plataforma de banco de dados recomendada para avançar.

* 2.4.5
* 2.4.6
* 2.4.7

A recomenda que você migre seus servidores de banco de dados para uma versão compatível do MariaDB.
O MariaDB é totalmente compatível com essas versões do Adobe Commerce e é a plataforma de banco de dados recomendada.

## Suporte a MySQL no Adobe Commerce 2.4.8 e 2.4.9

Adobe Commerce 2.4.8 e 2.4.9 são as últimas versões do Adobe Commerce compatíveis com MySQL.

Para estas versões:
* MySQL 8.4 é a versão final do MySQL suportada pela Adobe Commerce.
* Nenhuma versão do MySQL lançada após a 8.4 será certificada ou compatível com o Adobe Commerce.

## Direção futura: MariaDB como plataforma de banco de dados padrão

A partir de agora, o Adobe Commerce continuará a oferecer suporte ao MariaDB como a plataforma de banco de dados padrão e recomendada.

A Adobe recomenda que os seguintes clientes comecem a planejar sua migração para o MariaDB a fim de manter a compatibilidade a longo prazo e o alinhamento de suporte:
* Todos os clientes locais do Adobe Commerce 2.4.8 e 2.4.9
* Clientes que executam versões anteriores do Adobe Commerce compatíveis
