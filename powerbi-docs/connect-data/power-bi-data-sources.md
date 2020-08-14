---
title: Fontes de dados do Power BI
description: Este artigo lista as fontes de dados compatíveis com o Power BI, incluindo informações sobre o DirectQuery e o gateway de dados local.
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 08/05/2020
ms.author: davidi
ms.openlocfilehash: 6afc5dd36127390dd359d76fc8970d5ef6f7b590
ms.sourcegitcommit: 65822b51810a5239fea9d3d0af1fc286436c6cad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2020
ms.locfileid: "87837556"
---
# <a name="power-bi-data-sources"></a>Fontes de dados do Power BI

A tabela a seguir mostra as fontes de dados para as quais o Power BI dá suporte relacionado a conjuntos de dados, incluindo informações sobre o DirectQuery e o gateway de dados local. Confira informações sobre fluxos de dados em [Conectar-se a fontes de dados para fluxos de dados do Power BI](../transform-model/service-dataflows-data-sources.md).

> [!NOTE]
> Há muitos conectores de dados para o Power BI Desktop que exigem o Internet Explorer 10 (ou mais recente) para autenticação. 


| Fonte de dados | Conectar da Área de Trabalho | Conectar e atualizar do serviço | DirectQuery/conexão dinâmica | Gateway (com suporte) | Gateway (necessário) |
|---|---|---|---|---|---|---|---|
| Banco de dados do Access | Sim | Sim | Não | Sim <sup>1</sup> | Sim |
| ActiveDirectory | Sim | Sim | Não | Sim | Sim |
| Adobe Analytics | Sim | Sim | Não | Não | Não |
| Amazon Redshift | Sim | Sim | Sim | Sim | Não |
| appFigures | Sim | Sim | Não | Não | Não |
| Cubos do AtScale | Sim | Sim | Sim | Sim | Não |
| Azure Analysis Services | Sim | Sim | Sim | Não | Não |
| Armazenamento de Blobs do Azure | Sim | Sim | Não | Sim | Não |
| Azure Cosmos DB | Sim | Sim | Não | Não | Não |
| Gerenciamento de Custos do Azure | Sim | Sim | Não | Não | Não |
| Azure Data Explorer (kusto) | Sim | Sim | Sim | Não | Não |
| Azure Data Lake Storage Gen1 | Sim | Sim | Não | Não | Não |
| Azure Data Lake Storage Gen2 | Sim | Sim | Não | Sim | Não |
| Azure DevOps | Sim | Sim | Não | Não | Não |
| Azure DevOps Server | Sim | Sim | Não | Sim | Sim |
| Azure HDInsight (HDFS) | Sim | Sim | Não | Não | Não |
| Azure HDInsight Spark | Sim | Sim | Sim | Não | Não |
| Banco de Dados SQL do Azure | Sim | Sim | Sim | Sim <sup>2</sup> | Não |
| SQL Data Warehouse do Azure | Sim | Sim | Sim | Sim <sup>2</sup> | Não |
| Armazenamento de Tabelas do Azure | Sim | Sim | Não | Sim | Não |
| Conector do BI | Sim | Sim | Sim | Sim | Sim |
| BI360 – Relatórios financeiros e de orçamento | Sim | Sim | Não | Não | Não |
| Common Data Service | Sim | Sim | Não | Não | Não |
| Data.World – Obter Conjunto de Dados | Sim | Sim | Não | Não | Não |
| Denodo | Sim | Sim | Sim | Sim | Sim |
| Dremio | Sim | Sim | Sim | Sim | Sim |
| Dynamics 365 (online) | Sim | Sim | Não | Não | Não |
| Dynamics 365 Business Central | Sim | Sim | Não | Não | Não |
| Central do Microsoft Dynamics 365 Business (local) | Sim | Sim | Não | Não | Não |
| Customer Insights do Dynamics 365 | Sim | Sim | Não | Não | Não |
| Dynamics NAV | Sim | Sim | Não | Não | Não |
| Fonte de dados do Emigo | Sim | Sim | Não | Não | Não |
| Entersoft Business Suite | Sim | Sim | Não | Não | Não |
| Essbase | Sim | Sim | Sim | Sim | Sim |
| Exasol | Sim | Sim | Sim | Sim | Sim |
| Excel | Sim <sup>3</sup> | Sim <sup>3</sup> | Não | Sim <sup>3</sup> | Não <sup>4</sup> |
| Facebook | Sim | Sim | Não | Não | Não |
| Arquivo | Sim | Sim | Não | Sim | Sim |
| Pasta | Sim | Sim | Não | Sim | Sim |
| GitHub | Sim | Sim | Não | Não | Não |
| Google Analytics | Sim | Sim | Não | Não | Não |
| Google BigQuery | Sim | Sim | Sim | Não | Não |
| HDFS (Arquivo do Hadoop) | Sim | Não | Não | Não | Não |
| Consulta Interativa do HDInsight | Sim | Sim | Sim | Não | Não |
| IBM DB2 | Sim | Sim | Sim | Sim | Não |
| Banco de Dados do IBM Informix | Sim | Sim | Não | Sim | Não |
| IBM Netezza | Sim | Sim | Sim | Sim | Sim |
| Impala | Sim | Sim | Sim | Sim | Sim |
| Indexima | Sim | Sim | Sim | Sim | Sim |
| Industrial App Store | Sim | Sim | Não | Não | Não |
| Grade de Informações | Sim | Sim | Não | Não | Não |
| Intersystems IRIS | Sim | Sim | Sim | Sim | Sim |
| Intune Data Warehouse | Sim | Sim | Não | Não | Não |
| Jethro ODBC | Sim | Sim | Sim | Sim | Sim |
| JSON | Sim | Sim | Não | Sim** | Não <sup>4</sup> |
| Kyligence Enterprise | Sim | Sim | Sim | Sim | Sim |
| MailChimp | Sim | Sim | Não | Não | Não |
| Marketo | Sim | Sim | Não | Não | Não |
| MarkLogic ODBC | Sim | Sim | Sim | Sim | Sim |
| Microsoft Azure Consumption Insights | Sim | Sim | Não | Não | Não |
| Microsoft Exchange | Sim | Sim | Não | Sim | Não |
| Microsoft Exchange Online | Sim | Sim | Não | Não | Não |
| Segurança do Microsoft Graph | Sim | Sim | Não | Sim | Não |
| Mixpanel | Sim | Sim | Não | Não | Não |
| MySQL | Sim | Sim | Não | Sim | Sim |
| OData | Sim | Sim <sup>7</sup> | Não | Sim | Não |
| ODBC | Sim | Sim | Não | Sim | Sim |
| OleDb | Sim | Sim | Não | Sim | Sim |
| Oracle | Sim | Sim | Sim | Sim | Sim |
| Paxata <sup>8</sup> | Sim | Sim | Não | Sim | Não |
| PDF | Sim | Sim | Não | Sim | Não <sup>4</sup> |
| Planview Enterprise One – CTM | Sim | Sim | Não | Não | Não |
| Planview Enterprise One – PRM | Sim | Sim | Não | Não | Não |
| Planview Projectplace | Sim | Sim | Não | Não | Não |
| PostgreSQL | Sim | Sim | Sim | Sim | Não |
| Fluxos de dados do Power BI | Sim | Sim | Não | Não | Não |
| Conjuntos de dados do Power BI | Sim | Sim | Sim | Não | Não |
| Fluxos de dados do Power Platform | Sim | Sim | Não | Não | Não |
| Script do Python | Sim | Sim <sup>5</sup> | Não | Sim <sup>5</sup> | Sim |
| QubolePresto | Sim | Sim | Sim | Sim | Sim |
| Quick Base | Sim | Sim | Não | Sim | Sim |
| QuickBooks Online | Sim | Sim | Não | Não | Não |
| Script R | Sim | Sim <sup>5</sup> | Não | Sim <sup>5</sup> | Não |
| Roamler | Sim | Sim | Não | Sim | Não |
| Objetos do Salesforce | Sim | Sim | Não | Não | Não |
| Relatórios do Salesforce | Sim | Sim | Não | Não | Não |
| Servidor de Mensagens SAP Business Warehouse | Sim | Sim | Sim | Sim | Sim |
| Servidor do SAP Business Warehouse | Sim | Sim | Sim | Sim | Sim |
| SAP HANA | Sim | Sim | Sim | Sim | Sim |
| Pasta do SharePoint | Sim | Sim | Não | Sim | Não <sup>4</sup> |
| Lista do SharePoint | Sim | Sim | Não | Sim | Não <sup>4</sup> |
| Lista do SharePoint Online | Sim | Sim | Não | Sim <sup>2</sup> | Não |
| Smartsheet | Sim | Sim | Não | Não | Não |
| Snowflake | Sim | Sim | Sim | Sim | Não |
| Spark | Sim | Sim | Sim | Sim | Não |
| SparkPost | Sim | Sim | Não | Não | Não |
| SQL Server | Sim | Sim | Sim | Sim | Sim |
| SQL Server Analysis Services | Sim | Sim | Sim | Sim | Sim |
| Stripe | Sim | Sim | Não | Não | Não |
| SurveyMonkey | Sim | Sim | Não | Sim | Não |
| SweetIQ | Sim | Sim | Não | Não | Não |
| Sybase | Sim | Sim | Não | Sim | Sim |
| TeamDesk | Sim | Sim | Não | Sim | Não |
| Tenforce | Sim | Sim | Não | Não | Não |
| Teradata | Sim | Sim | Sim | Sim | Sim |
| Texto/CSV | Sim | Sim | Não | Sim | Não <sup>4</sup> |
| Twilio | Sim | Sim | Não | Não | Não |
| tyGraph | Sim | Sim | Não | Não | Não |
| Vertica | Sim | Sim | Sim | Sim | Sim |
| Web | Sim | Sim | Não | Sim | Sim <sup>6</sup> |
| Webtrends | Sim | Sim | Não | Não | Não |
| Workforce Dimensions | Sim | Sim | Não | Sim | Não |
| XML | Sim | Sim | Não | Sim | Não <sup>4</sup> |
| Zendesk | Sim | Sim | Não | Não | Não |
| | | | | | | | |

<sup>1</sup> Compatível com o [provedor do ACE OLEDB](https://www.microsoft.com/download/details.aspx?id=54920), instalado no mesmo computador que o gateway.

<sup>2</sup> Compatível com a mesma função M da versão local, restringindo as opções de autenticação (o gateway não tem suporte para OAuth).

<sup>3</sup> Os arquivos do Excel 1997-2003 (.xls) exigem o [provedor ACE OLEDB](https://www.microsoft.com/download/details.aspx?id=54920).

<sup>4</sup> Necessário para a versão local da tecnologia.

<sup>5</sup> Compatível apenas com o [gateway pessoal](service-gateway-personal-mode.md).

<sup>6</sup> Obrigatório para .html, .xls e Bancos de Dados do Access

<sup>7</sup> O serviço do Power BI não dá suporte a feeds OData que exigem autenticação.

<sup>8</sup> O Paxata tem suporte na versão do Power BI Desktop otimizada para o Servidor de Relatórios do Power BI. Ele não tem suporte nos relatórios do Power BI publicados no Servidor de Relatórios. Confira [Fontes de dados de relatórios do Power BI no Servidor de Relatórios do Power BI](../report-server/data-sources.md) para obter a lista de fontes de dados com suporte.

## <a name="single-sign-on-sso-for-directquery-sources"></a>SSO (logon único) para fontes do DirectQuery

Quando a opção de SSO está habilitada e os usuários acessam os relatórios baseados na fonte de dados, o Power BI envia suas credenciais autenticadas do Azure AD nas consultas à fonte de dados subjacente. Isso permite que o Power BI respeite as configurações de segurança que são configuradas no nível da fonte de dados.
A opção de SSO entra em vigor em todos os conjuntos de dados que usam essa fonte de dados. Isso não afeta o método de autenticação usado para cenários de importação. As seguintes fontes de dados dão suporte ao SSO para conexões por meio do DirectQuery:

- Banco de Dados SQL do Azure
- SQL Data Warehouse do Azure
- Impala
- SAP HANA
- SAP BW
- Servidor de Mensagens SAP BW
- Snowflake
- Spark
- SQL Server
- Teradata

> [!Note]
> Não há suporte para Autenticação Multifator do Microsoft Azure (MFA). Os usuários que desejam usar o SSO com o DirectQuery precisam ser isentos de MFA.

## <a name="next-steps"></a>Próximas etapas

[Conectar-se a dados no Power BI Desktop](desktop-quickstart-connect-to-data.md)  
[Usar o DirectQuery no Power BI](desktop-directquery-about.md)  
[Dados dinâmicos do SQL Server Analysis Services no Power BI](sql-server-analysis-services-tabular-data.md)  
[O que é um gateway de dados local?](service-gateway-onprem.md)  
[Fontes de dados de relatórios do Power BI no Servidor de Relatórios do Power BI](../report-server/data-sources.md)
