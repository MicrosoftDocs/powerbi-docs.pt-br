---
title: Obter dados de arquivos CSV (Valores Separados por Vírgula)
description: Saiba como obter dados de arquivos CSV no Power BI
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: 4827049ee8eff86b2ce71ee9befd3d01760c0840
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85230476"
---
# <a name="get-data-from-comma-separated-value-csv-files"></a>Obter dados de arquivos CSV (Valores Separados por Vírgula)
![](media/service-comma-separated-value-files/csv_icon.png)

Arquivos de valores separados por vírgula, geralmente conhecidos como .CSV, são arquivos de texto simples com linhas de dados em que cada valor é separado por uma vírgula. Esses tipos de arquivos podem conter grandes quantidades de dados em um tamanho do arquivo relativamente pequeno, tornando-os uma fonte de dados ideal para o Power BI. É possível baixar um arquivo .CSV de exemplo [aqui](https://go.microsoft.com/fwlink/?LinkID=619356).

Caso você tenha um .CSV, é hora de inseri-lo em seu site do Power BI como um conjunto de dados, no qual será possível começar a explorar seus dados, criar alguns dashboards e compartilhar suas ideias com outras pessoas.

>[!TIP]
>Muitas organizações produzem um .CSV em que dados atualizados diariamente. Para garantir que o conjunto de dados no Power BI permanece em sincronia com o arquivo atualizado, certifique-se de que o arquivo é salvo no OneDrive com o mesmo nome.

## <a name="where-your-file-is-saved-makes-a-difference"></a>O local em que o arquivo é salvo faz a diferença
**Local** - Caso o arquivo .CSV seja salvo em uma unidade local no computador ou em outro local em sua organização, por meio do Power BI, é possível *importar* o arquivo para o Power BI. Na verdade, o arquivo permanecerá na unidade local; portanto, o arquivo completo não é, de fato, importado para o Power BI. O que realmente ocorre é que um novo conjunto de dados é criado no Power BI e os dados do arquivo .CSV são carregados nesse conjunto de dados.

**OneDrive - Business** – Caso você tenha o OneDrive for Business e entre com a mesma conta usada para o logon no Power BI, essa será, sem dúvida, a maneira mais efetiva de manter o arquivo .CSV, bem como seu conjunto de dados, seus relatórios e dashboards no Power BI em sincronia. Visto que tanto o Power BI quanto o OneDrive ficam na nuvem, o Power BI se *conecta* ao seu arquivo no OneDrive em intervalos aproximados de sessenta minutos. Caso sejam encontradas alterações, o conjunto de dados, os relatórios e os dashboards serão atualizados automaticamente no Power BI.

**OneDrive - Personal** – Caso os arquivos sejam salvos em sua própria conta do OneDrive, você aproveitará vários dos mesmos benefícios que teria com o OneDrive for Business. A maior diferença é que, na primeira conexão ao arquivo (usando Obter Dados > Arquivos > OneDrive – Personal), será necessário entrar no OneDrive com sua conta da Microsoft, que, normalmente, é diferente daquela usada para fazer logon no Power BI. Ao entrar no OneDrive com sua conta da Microsoft, certifique-se de selecionar a opção Mantenha-me conectado. Dessa forma, o Power BI poderá se conectar ao seu arquivo em intervalos aproximados de sessenta minutos e garantir que o conjunto de dados no Power BI está em sincronia.

**SharePoint – Sites de Equipe** – Salvar seus arquivos do Power BI Desktop no SharePoint – Sites de Equipe é muito semelhante a salvá-los no OneDrive for Business. A maior diferença nesse caso é como você se conecta ao arquivo do Power BI. É possível especificar uma URL ou conectar-se à pasta raiz.

## <a name="import-or-connect-to-a-csv-file"></a>Importar ou conectar-se a um arquivo .CSV
>[!IMPORTANT]
>O tamanho máximo do arquivo que pode ser importado no Power BI é de 1 gigabyte.

1. No Power BI, no painel do navegador, clique em **Obter Dados**.
   
   ![](media/service-comma-separated-value-files/csv_get_data_button.png)
2. Em **Arquivos**, clique em **Obter**.
   
   ![](media/service-comma-separated-value-files/csv_files_get.png)
3. Encontre o arquivo.
   
   ![](media/service-comma-separated-value-files/csv_find_your_file.png)

## <a name="next-steps"></a>Próximas etapas
**Explore os dados** – Depois de obter dados de seu arquivo no Power BI, é hora de explorá-los. Basta clicar com o botão direito do mouse no novo conjunto de dados e clicar em **Explorar**.

**Agendar atualização** – Caso o arquivo seja salvo em uma unidade local, é possível configurar a atualização agendada para que o conjunto de dados e os relatórios no Power BI permaneçam atualizados. Para saber mais, veja [Atualização de dados no Power BI](refresh-data.md). Se o arquivo for salvo no OneDrive, o Power BI será sincronizado de forma automática com ele a cada hora, aproximadamente.

