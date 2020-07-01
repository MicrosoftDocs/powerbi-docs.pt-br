---
title: Conectar-se a dados usando interfaces genéricas no Power BI Desktop
description: Saiba como se conectar a fontes de dados diferentes com interfaces genéricas no Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 6a0170d40413cd2833f7e31bb3bc7c5704a1f5cc
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85224044"
---
# <a name="connect-to-data-by-using-power-bi-desktop-generic-interfaces"></a>Conectar-se a dados usando as interfaces genéricas do Power BI Desktop 

Conecte-se a uma variedade de fontes de dados diferentes no **Power BI Desktop**, usando conectores de dados internos que vão desde **bancos de dados do Access** até recursos do **Zendesk**, como mostra a janela **Obter Dados**. Conecte-se também a todos os *outros* tipos de fontes de dados para expandir ainda mais as opções de conectividade, com o uso das interfaces genéricas (como **ODBC** ou **APIs REST**) internas do **Power BI Desktop**.

![](media/desktop-connect-using-generic-interfaces/generic-data-interfaces_1.png)

## <a name="power-bi-desktop-data-interfaces"></a>Interfaces de dados do Power BI Desktop
O **Power BI Desktop** inclui uma coleção cada vez maior de conectores de dados desenvolvidos para se conectarem a uma fonte de dados específica. Por exemplo, o conector de dados para a **Lista do SharePoint** fornece campos específicos e informações de suporte durante a sequência de conexão projetados para as **Listas do SharePoint**, que é o caso com outras fontes de dados encontradas na janela exibida ao selecionar **Obter Dados > Mais...** (mostrado na imagem anterior).

Além disso, o **Power BI Desktop** permite que você se conecte a fontes de dados que não são identificadas nas listas de **Obter Dados**, usando uma das seguintes interfaces de dados genéricas:

* **ODBC**
* **OLE DB**
* **OData**
* **APIs REST**
* **Scripts do R**

Ao fornecer os parâmetros apropriados nas janelas de conexão fornecidas por essas interfaces genéricas, a infinidade de fontes de dados que você pode acessar e usar no **Power BI Desktop** aumenta consideravelmente.

Nas seções a seguir, encontre várias listas de fontes de dados que podem ser acessadas por essas interfaces genéricas.

Não conseguiu encontrar a fonte de dados que você deseja usar com o **Power BI Desktop**? Envie sua ideia para a [lista de solicitações e ideias](https://ideas.powerbi.com/) da equipe do Power BI.

## <a name="data-sources-accessible-through-odbc"></a>Fontes de dados acessíveis por meio do ODBC
O conector para **ODBC** do **Power BI Desktop** permite que você importe dados de qualquer driver ODBC de terceiros apenas especificando um **DSN (Nome da Fonte de Dados)** ou uma *cadeia de conexão*. Como opção, especifique também uma instrução SQL para ser executada no driver ODBC.

![](media/desktop-connect-using-generic-interfaces/generic-data-interfaces_2.png)

A lista a seguir fornece detalhes sobre alguns exemplos de fontes de dados às quais o **Power BI Desktop** pode se conectar usando a interface genérica do **ODBC**.

| Conector genérico do Power BI Desktop | Fonte de dados externa | Link para mais informações |
| --- | --- | --- |
| ODBC |Cassandra |[Driver ODBC do Cassandra](https://www.simba.com/drivers/cassandra-odbc-jdbc/) |
| ODBC |Couchbase DB |[Couchbase e Power BI](https://powerbi.microsoft.com/blog/visualizing-data-from-couchbase-server-v4-using-power-bi/) |
| ODBC |DynamoDB |[Driver ODBC do DynamoDB](https://www.simba.com/drivers/dynamodb-odbc-jdbc/) |
| ODBC |Google BigQuery |[Driver ODBC do BigQuery](https://www.simba.com/drivers/bigquery-odbc-jdbc/) |
| ODBC |HBase |[Driver ODBC do HBase](https://www.simba.com/drivers/hbase-odbc-jdbc/) |
| ODBC |Hive |[Driver ODBC do Hive](https://www.simba.com/drivers/hive-odbc-jdbc/) |
| ODBC |IBM Netezza |[Informações sobre o IBM Netezza](https://www.ibm.com/support/knowledgecenter/SSULQD_7.2.1/com.ibm.nz.datacon.doc/c_datacon_plg_overview.html) |
| ODBC |Presto |[Driver ODBC do Presto](https://www.simba.com/drivers/presto-odbc-jdbc/) |
| ODBC |Project Online |[Artigo de projeto online](desktop-project-online-connect-to-data.md) |
| ODBC |Progress OpenEdge |[Postagem do blog de driver ODBC do Progress OpenEdge](https://www.progress.com/blogs/connect-microsoft-power-bi-to-openedge-via-odbc-driver) |

## <a name="data-sources-accessible-through-ole-db"></a>Fontes de dados acessíveis por meio do OLE DB
O conector para **OLE DB** do **Power BI Desktop** permite que você importe dados de qualquer driver OLE DB de terceiros apenas especificando uma *cadeia de conexão*. Como opção, especifique também uma instrução SQL para ser executada no driver OLE DB.

![](media/desktop-connect-using-generic-interfaces/generic-data-interfaces_3.png)

A lista a seguir fornece detalhes sobre alguns exemplos de fontes de dados às quais o **Power BI Desktop** pode se conectar usando a interface genérica do **OLE DB**.

| Conector genérico do Power BI Desktop | Fonte de dados externa | Link para mais informações |
| --- | --- | --- |
| OLE DB |OLE DB para SAS |[Provedor SAS para OLE DB](https://support.sas.com/downloads/package.htm?pid=648) |
| OLE DB |OLE DB para Sybase |[Provedor Sybase para OLE DB](http://infocenter.sybase.com/help/index.jsp?topic=/com.sybase.infocenter.dc35888.1550/doc/html/jon1256941734395.html) |

## <a name="data-sources-accessible-through-odata"></a>Fontes de dados acessíveis por meio do OData
O conector para **OData** no **Power BI Desktop** permite que você importe dados de qualquer URL do **OData** apenas digitando ou colando a URL do **OData**. Adicione várias partes da URL digitando ou colando esses links nas caixas de texto fornecidas na janela **Feed OData**.

![](media/desktop-connect-using-generic-interfaces/generic-data-interfaces_4.png)

A lista a seguir fornece detalhes sobre alguns exemplos de fontes de dados às quais o **Power BI Desktop** pode se conectar usando a interface genérica do **OData**.

| Conector genérico do Power BI Desktop | Fonte de dados externa | Link para mais informações |
| --- | --- | --- |
| OData |Em breve |Verifique novamente em breve para ver as fontes de dados OData |

## <a name="data-sources-accessible-through-rest-apis"></a>Fontes de dados acessíveis por meio das APIs REST
Conecte-se a fontes de dados usando as **APIs REST** e, portanto, use dados de todos os tipos de fontes de dados que dão suporte ao **REST**.

![](media/desktop-connect-using-generic-interfaces/generic-data-interfaces_5.png)

A lista a seguir fornece detalhes sobre alguns exemplos de fontes de dados às quais o **Power BI Desktop** pode se conectar usando a interface genérica das **APIs REST**.

| Conector genérico do Power BI Desktop | Fonte de dados externa | Link para mais informações |
| --- | --- | --- |
| APIs REST |Couchbase DB |[Informações sobre a API REST do Couchbase](https://powerbi.microsoft.com/blog/visualizing-data-from-couchbase-server-v4-using-power-bi/) |

## <a name="data-sources-accessible-through-r-script"></a>Fontes de dados acessíveis por meio do Script do R
Use **scripts do R** para acessar fontes de dados e use esses dados no **Power BI Desktop**.

![](media/desktop-connect-using-generic-interfaces/r-scripts-2.png)

A lista a seguir fornece detalhes sobre alguns exemplos de fontes de dados às quais o **Power BI Desktop** pode se conectar usando a interface genérica dos **scripts do R**.

| Conector genérico do Power BI Desktop | Fonte de dados externa | Link para mais informações |
| --- | --- | --- |
| Script do R |Arquivos SAS |[Diretrizes do CRAN sobre o script do R](https://cran.r-project.org/doc/manuals/R-data.html) |
| Script do R |Arquivos SPSS |[Diretrizes do CRAN sobre o script do R](https://cran.r-project.org/doc/manuals/R-data.html) |
| Script do R |Arquivos estatísticos do R |[Diretrizes do CRAN sobre o script do R](https://cran.r-project.org/doc/manuals/R-data.html) |

## <a name="next-steps"></a>Próximas etapas
Há diversos tipos de fontes de dados aos quais você pode se conectar usando o **Power BI Desktop**. Para obter mais informações sobre fontes de dados, confira os seguintes recursos:

* [O que é o Power BI Desktop?](../fundamentals/desktop-what-is-desktop.md)
* [Fontes de dados no Power BI Desktop](desktop-data-sources.md)
* [Formatar e combinar dados com o Power BI Desktop](desktop-shape-and-combine-data.md)
* [Conectar-se a pastas de trabalho do Excel no Power BI Desktop](desktop-connect-excel.md)   
* [Inserir dados diretamente no Power BI Desktop](desktop-enter-data-directly-into-desktop.md)   
