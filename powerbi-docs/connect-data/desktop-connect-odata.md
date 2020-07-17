---
title: Conectar-se a um feed OData no Power BI Desktop
description: Conecte-se facilmente e use um feed OData no Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 9e10d694940bda465e68f54370d87aab15b628ee
ms.sourcegitcommit: c83146ad008ce13bf3289de9b76c507be2c330aa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2020
ms.locfileid: "86216487"
---
# <a name="connect-to-odata-feeds-in-power-bi-desktop"></a>Conectar-se a feeds OData no Power BI Desktop
No Power BI Desktop, você pode se conectar a um **feed OData** e usar os dados subjacentes, assim como qualquer outra fonte de dados no Power BI Desktop.

Para se conectar a um feed OData, selecione **Obter Dados > Feed OData** na faixa de opções **Página Inicial** no Power BI Desktop.

![Captura de tela da faixa de opções Obter Dados no Power BI Desktop mostrando a seleção de Feed OData.](media/desktop-connect-odata/connect-to-odata_1.png)

Na janela **Feed OData** exibida, digite ou cole a URL do feed OData na caixa e selecione **OK**.

![Captura de tela da caixa de diálogo Feed OData mostrando o campo URL.](media/desktop-connect-odata/connect-to-odata_2.png)

O Power BI Desktop se conecta ao feed OData e exibe as tabelas disponíveis e outros elementos de dados na janela **Navegador**. Quando você seleciona um elemento, o painel direito da janela **Navegador** exibe uma visualização dos dados. Você pode selecionar quantas tabelas desejar importar. A janela **Navegador** mostra uma visualização da tabela selecionada no momento.

![Captura de tela da caixa de diálogo Navegador mostrando uma visualização dos dados da tabela selecionada.](media/desktop-connect-odata/connect-to-odata_3.png)

É possível escolher o botão **Editar**, que inicia o **Editor de Consultas**, no qual você pode formatar e transformar os dados do feed OData antes de importá-los para o Power BI Desktop. Se preferir, selecione o botão **Carregar** e importe todos os elementos de dados selecionados no painel esquerdo.

Quando selecionamos **Carregar**, o Power BI Desktop importa os itens selecionados e exibe uma janela **Carregar** do progresso da importação.

![Captura de tela da caixa de diálogo Carregar mostrando o progresso da importação.](media/desktop-connect-odata/connect-to-odata_4.png)

Após a conclusão, o Power BI Desktop disponibiliza as tabelas e outros elementos de dados selecionados no painel **Campos**, localizado no lado direito da exibição *Relatórios* no Power BI Desktop.

![Captura de tela do painel Campos mostrando a lista de tabelas selecionadas.](media/desktop-connect-odata/connect-to-odata_5.png)

É isso.

Agora você está pronto para usar os dados importados do feed OData no Power BI Desktop para criar visuais, relatórios, ou para interagir com quaisquer outros dados aos quais você queira se conectar e importar, por exemplo, outras pastas de trabalho do Excel, bancos de dados ou qualquer outra fonte de dados.

## <a name="next-steps"></a>Próximas etapas
Há todos os tipos de dados aos quais você pode se conectar usando o Power BI Desktop. Para obter mais informações sobre fontes de dados, confira os seguintes recursos:

* [O que é o Power BI Desktop?](../fundamentals/desktop-what-is-desktop.md)
* [Fontes de dados no Power BI Desktop](desktop-data-sources.md)
* [Formatar e combinar dados com o Power BI Desktop](desktop-shape-and-combine-data.md)
* [Conectar-se a pastas de trabalho do Excel no Power BI Desktop](desktop-connect-excel.md)   
* [Inserir dados diretamente no Power BI Desktop](desktop-enter-data-directly-into-desktop.md)   
