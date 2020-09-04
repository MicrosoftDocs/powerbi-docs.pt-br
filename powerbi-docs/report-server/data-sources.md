---
title: Fontes de dados de relatórios do Power BI no Servidor de Relatórios do Power BI
description: Os relatórios do Power BI podem se conectar a diversas fontes de dados. Dependendo de como os dados são usados, fontes de dados diferentes estão disponíveis.
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 08/04/2020
ms.author: maggies
ms.openlocfilehash: 08294e1320e603131beb0ca332b0f85ee51ea8bb
ms.sourcegitcommit: 13c4bec679313f2951f1833033316cb8176da8a1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2020
ms.locfileid: "88937552"
---
# <a name="power-bi-report-data-sources-in-power-bi-report-server"></a>Fontes de dados de relatórios do Power BI no Servidor de Relatórios do Power BI
Os relatórios do Power BI podem se conectar a diversas fontes de dados. Dependendo de como os dados são usados, fontes de dados diferentes estão disponíveis. Os dados podem ser importados ou consultados diretamente usando o DirectQuery ou uma conexão dinâmica ao SQL Server Analysis Services. Algumas fontes de dados estão disponíveis no Power BI Desktop otimizado para o Servidor de Relatórios do Power BI, mas não têm suporte quando publicadas no Servidor de Relatórios do Power BI.

Essas fontes de dados são específicas aos relatórios do Power BI usados no Servidor de Relatórios do Power BI. Para obter informações sobre fontes de dados compatíveis com relatórios paginados (.rdl), veja [Fontes de dados com suporte no Reporting Services](https://docs.microsoft.com/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs).

> [!IMPORTANT]
> Todas as fontes de dados em um relatório do Power BI Desktop devem ser compatíveis com a configuração da atualização agendada.
>  

## <a name="list-of-supported-data-sources"></a>Lista das fontes de dados com suporte

| **Fonte de dados** | **Dados armazenados em cache** | **Atualização agendada** | **Live/DirectQuery** |
| --- | --- | --- | --- |
| Banco de dados do SQL Server |Sim |Sim |Sim |
| SQL Server Analysis Services |Sim |Sim |Sim |
| Banco de Dados SQL do Azure |Sim |Sim |Sim |
| SQL Data Warehouse do Azure |Sim |Sim |Sim |
| Excel |Sim |Sim |Não |
| Banco de dados do Access |Sim |Sim |Não |
| Active Directory |Sim |Sim |Não |
| Amazon Redshift |Sim |Não |Não |
| Armazenamento de Blobs do Azure |Sim |Sim |Não |
| Repositório Azure Data Lake |Sim |Não |Não |
| Azure HDInsight (HDFS) |Sim |Não |Não |
| Azure HDInsight (Spark) |Sim |Não |Não |
| Armazenamento de Tabelas do Azure |Sim |Sim |Não |
| Dynamics 365 (online) |Sim |Não |Não |
| Facebook |Sim |Não |Não |
| Pasta |Sim |Sim |Não |
| Google Analytics |Sim |Não |Não |
| HDFS (Arquivo do Hadoop) |Sim |Não |Não |
| Banco de dados IBM DB2 |Sim |Sim |Não |
| Impala |Sim |Não |Não |
| JSON |Sim |Sim |Não |
| Microsoft Exchange |Sim |Não |Não |
| Microsoft Exchange Online |Sim |Não |Não |
| Banco de dados MySQL |Sim |Sim |Não |
| Feed OData |Sim |Sim |Não |
| ODBC |Sim |Sim |Não |
| OLE DB |Sim |Sim |Não |
| Banco de dados Oracle |Sim |Sim |Sim |
| Banco de dados PostgreSQL |Sim |Sim |Não |
| Serviço do Power BI |Não |Não |Não |
| Script do R |Sim |Não |Não |
| Objetos do Salesforce |Sim |Não |Não |
| Relatórios do Salesforce |Sim |Não |Não |
| Servidor do SAP Business Warehouse |Sim |Sim |Sim |
| Banco de dados do SAP HANA |Sim |Sim |Sim |
| Pasta do SharePoint (local) |Sim |Sim |Não |
| Lista do SharePoint (local) |Sim |Sim |Não |
| Lista do SharePoint Online |Sim |Não |Não |
| Snowflake |Sim |Não |Não |
| Banco de dados Sybase |Sim |Sim |Não |
| Teradata |Sim |Sim |Sim |
| Texto/CSV |Sim |Sim |Não |
| Web |Sim |Sim |Não |
| XML |Sim |Sim |Não |
| appFigures (Beta) |Sim |Não |Não |
| Banco de Dados do Azure Analysis Services |Sim |Não |Sim |
| Azure Cosmos DB (Beta) |Sim |Não |Não |
| Azure HDInsight Spark (Beta) |Sim |Não |Não |
| Common Data Service (Beta) |Sim |Não |Não |
| comScore Digital Analytix (Beta) |Sim |Não |Não |
| Dynamics 365 for Customer Insights (Beta) |Sim |Não |Não |
| Dynamics 365 for Financials (Beta) |Sim |Não |Não |
| GitHub (Beta) |Sim |Não |Não |
| Google BigQuery (Beta) |Sim |Não |Não |
| Banco de dados IBM Informix (Beta) |Sim |Não |Não |
| IBM Netezza (Beta) |Sim |Não |Não |
| Kusto (Beta) |Sim |Não |Não |
| MailChimp (Beta) |Sim |Não |Não |
| Microsoft Azure Consumption Insights (Beta) |Sim |Não |Não |
| Mixpanel (Beta) |Sim |Não |Não |
| Planview Enterprise (Beta) |Sim |Não |Não |
| Projectplace (Beta) |Sim |Não |Não |
| QuickBooks Online (Beta) |Sim |Não |Não |
| Smartsheet |Sim |Não |Não |
| Spark (Beta) |Sim |Não |Não |
| SparkPost (Beta) |Sim |Não |Não |
| SQL Sentry (Beta) |Sim |Não |Não |
| Stripe (Beta) |Sim |Não |Não |
| SweetIQ (Beta) |Sim |Não |Não |
| Troux (Beta) |Sim |Não |Não |
| Twilio (Beta) |Sim |Não |Não |
| tyGraph (Beta) |Sim |Não |Não |
| Vertica (Beta) |Sim |Não |Não |
| Visual Studio Team Services (Beta) |Sim |Não |Não |
| Webtrends (Beta) |Sim |Não |Não |
| ZenDesk (Beta) |Sim |Não |Não |

> [!IMPORTANT]
> A segurança de nível de linha configurada na fonte de dados deve funcionar para determinadas conexões dinâmicas e do DirectQuery (SQL Server, Banco de Dados SQL do Azure, Oracle e Teradata) considerando que o Kerberos esteja configurado adequadamente no ambiente.
> 
> 

## <a name="list-of-supported-authentication-methods-for-model-refresh"></a>Lista de métodos de autenticação compatíveis para atualização do modelo

O Servidor de Relatórios do Power BI não é compatível com a autenticação com base em OAuth para a atualização do modelo. Algumas fontes de dados, como bancos de dados do Excel ou do Access, usam uma etapa separada como Arquivo ou Web para se conectarem a dados.

| **Fonte de dados** | **Autenticação Anônima** | **Autenticação de chave** | **Nome de usuário e senha** | **Autenticação do Windows** |
| --- | --- | --- | --- | --- |
| Banco de dados do SQL Server |Não |Não |Sim |Sim |
| SQL Server Analysis Services |Não |Não |Sim |Sim |
| Web |Sim |Não |Sim |Sim |
| Banco de Dados SQL do Azure |Não |Não |Sim |Não |
| SQL Data Warehouse do Azure |Não |Não |Sim |Não |
| Active Directory |Não |Não |Sim |Sim |
| Amazon Redshift |Não |Não |Não |Não |
| Armazenamento de Blobs do Azure |Sim |Sim |Não |Não |
| Repositório Azure Data Lake |Não |Não |Não |Não |
| Azure HDInsight (HDFS) |Não |Não |Não |Não |
| Azure HDInsight (Spark) |Não |Não |Não |Não |
| Armazenamento de Tabelas do Azure |Não |Sim |Não |Não |
| Dynamics 365 (online) |Não |Não |Não |Não |
| Facebook |Não |Não |Não |Não |
| Pasta |Não |Não |Não |Sim |
| Google Analytics |Não |Não |Não |Não |
| HDFS (Arquivo do Hadoop) |Não |Não |Não |Não |
| Banco de dados IBM DB2 |Não |Não |Sim |Sim |
| Impala |Não |Não |Não |Não |
| Microsoft Exchange |Não |Não |Não |Não |
| Microsoft Exchange Online |Não |Não |Não |Não |
| Banco de dados MySQL |Não |Não |Sim |Sim |
| Feed OData |Sim |Sim |Sim |Sim |
| ODBC |Sim |Não |Sim |Sim |
| OLE DB |Sim |Não |Sim |Sim |
| Banco de dados Oracle |Não |Não |Sim |Sim |
| Banco de dados PostgreSQL |Não |Não |Sim |Não |
| Serviço do Power BI |Não |Não |Não |Não |
| Script do R |Não |Não |Não |Não |
| Objetos do Salesforce |Não |Não |Não |Não |
| Relatórios do Salesforce |Não |Não |Não |Não |
| Servidor do SAP Business Warehouse |Não |Não |Sim |Não |
| Banco de dados do SAP HANA |Não |Não |Sim |Sim |
| Pasta do SharePoint (local) |Sim |Não |Não |Sim |
| Lista do SharePoint (local) |Sim |Não |Não |Sim |
| Lista do SharePoint Online |Não |Não |Não |Não |
| Snowflake |Não |Não |Não |Não |
| Banco de dados Sybase |Não |Não |Sim |Sim |
| Teradata |Não |Não |Sim |Sim** |
| appFigures (Beta) |Não |Não |Não |Não |
| Banco de dados do Analysis Services do Azure (Beta) |Não |Não |Não |Não |
| Azure Cosmos DB (Beta) |Não |Não |Não |Não |
| Azure HDInsight Spark (Beta) |Não |Não |Não |Não |
| Common Data Service (Beta) |Não |Não |Não |Não |
| comScore Digital Analytix (Beta) |Não |Não |Não |Não |
| Dynamics 365 for Customer Insights (Beta) |Não |Não |Não |Não |
| Dynamics 365 for Financials (Beta) |Não |Não |Não |Não |
| GitHub (Beta) |Não |Não |Não |Não |
| Google BigQuery (Beta) |Não |Não |Não |Não |
| Banco de dados IBM Informix (Beta) |Não |Não |Não |Não |
| IBM Netezza (Beta) |Não |Não |Não |Não |
| Kusto (Beta) |Não |Não |Não |Não |
| MailChimp (Beta) |Não |Não |Não |Não |
| Microsoft Azure Consumption Insights (Beta) |Não |Não |Não |Não |
| Mixpanel (Beta) |Não |Não |Não |Não |
| Planview Enterprise (Beta) |Não |Não |Não |Não |
| Projectplace (Beta) |Não |Não |Não |Não |
| QuickBooks Online (Beta) |Não |Não |Não |Não |
| Smartsheet |Não |Não |Não |Não |
| Spark (Beta) |Não |Não |Não |Não |
| SparkPost (Beta) |Não |Não |Não |Não |
| SQL Sentry (Beta) |Não |Não |Não |Não |
| Stripe (Beta) |Não |Não |Não |Não |
| SweetIQ (Beta) |Não |Não |Não |Não |
| Troux (Beta) |Não |Não |Não |Não |
| Twilio (Beta) |Não |Não |Não |Não |
| tyGraph (Beta) |Não |Não |Não |Não |
| Vertica (Beta) |Não |Não |Não |Não |
| Visual Studio Team Services (Beta) |Não |Não |Não |Não |
| Webtrends (Beta) |Não |Não |Não |Não |
| ZenDesk (Beta) |Não |Não |Não |Não |

**Não há suporte para o uso da autenticação LDAP com o Teradata (habilitado no Power BI Desktop com o comando do prompt de comando 'setx PBI_EnableTeradataLdap true') na atualização de modelo.

## <a name="list-of-supported-authentication-methods-for-directquery"></a>Lista de métodos de autenticação compatíveis para DirectQuery

O Servidor de Relatórios do Power BI não é compatível com a autenticação com base em OAuth para DirectQuery.

| **Fonte de dados** | **Autenticação Anônima** | **Autenticação de chave** | **Nome de usuário e senha** | **Autenticação do Windows** | **Autenticação Integrada do Windows** |
| --- | --- | --- | --- | --- | --- |
| Banco de dados do SQL Server |Não |Não |Sim |Sim |Sim |
| SQL Server Analysis Services |Não |Não |Sim |Sim |Sim |
| Banco de Dados SQL do Azure |Não |Não |Sim |Não |Não |
| SQL Data Warehouse do Azure |Não |Não |Sim |Não |Não |
| Banco de dados Oracle |Não |Não |Sim |Sim |Sim |
| Servidor do SAP Business Warehouse |Não |Não |Sim |Não |Não |
| Banco de dados do SAP HANA |Não |Não |Sim |Sim |Sim** |
| Teradata |Não |Não |Sim |Sim |Sim |

**O SAP HANA é compatível com o DirectQuery com Autenticação Integrada do Windows somente ao usá-lo como um banco de dados relacional no arquivo do Power BI Desktop publicado (.pbix).

## <a name="next-steps"></a>Próximas etapas

[Fontes de dados para relatórios do Power BI](../connect-data/power-bi-data-sources.md) no serviço do Power BI

Agora que você se conectou à sua fonte de dados, [crie um relatório do Power BI](quickstart-create-powerbi-report.md) usando os dados da fonte de dados.

Mais perguntas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)
