---
title: Usar gráficos de faixa de opções no Power BI
description: Criar e consumir gráficos de faixa de opções no Power BI Desktop
author: mihart
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 05/05/2019
ms.author: rien
LocalizationGroup: Visualizations
ms.openlocfilehash: e7f36ada69f1ee98c7392d05eb169947c600774e
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85221635"
---
# <a name="create-ribbon-charts-in-power-bi"></a>Criar gráficos de faixa de opções no Power BI

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

É possível criar gráficos de faixa de opções para visualizar dados e descobrir rapidamente qual categoria de dados tem a classificação mais alta (maior valor). Gráficos de faixa de opções são eficazes para mostrar alterações na classificação, com o maior intervalo (valor) sempre exibido na parte superior de cada período. 

![gráfico de faixa de opções](media/desktop-ribbon-charts/ribbon-charts-01.png)

> [!NOTE]
> Compartilhar seu relatório com um colega do Power BI exige que você tenha licenças de Power BI Pro individuais ou que o relatório seja salvo na capacidade Premium. Confira [compartilhamento de relatórios](../collaborate-share/service-share-reports.md).

## <a name="prerequisites"></a>Pré-requisitos

Este tutorial usa o [arquivo PBIX de exemplo de Análise de Varejo](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).

1. Na seção superior esquerda da barra de menus, selecione **Arquivo** > **Abrir**
   
2. Encontre sua cópia do **arquivo PBIX de exemplo de Análise de Varejo**

1. Abra o **arquivo PBIX de exemplo de Análise de Varejo** na exibição de relatório ![Captura de tela do ícone de exibição de relatório](media/power-bi-visualization-kpi/power-bi-report-view.png).

1. Selecionar ![Captura de tela da guia amarela.](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) para adicionar uma nova página.

## <a name="create-a-ribbon-chart"></a>Criar um gráfico de faixa de opções

1. Para criar um gráfico de faixa de opções, selecione **Gráfico de faixa de opções** no painel **Visualizações**.

    ![modelos de visualização](media/desktop-ribbon-charts/power-bi-template.png)

    Os gráficos de faixa de opções conectam uma categoria de dados no continuum de tempo visualizado usando faixas de opções, permitindo que você veja como determinada categoria é classificada em todo o intervalo do eixo x do gráfico (geralmente, a linha do tempo).

2. Selecione campos para **Eixo**, **Legenda** e **Valor**.  Neste exemplo, selecionamos: **Store** > **OpenDate**, **Item** > **Category** e **Sales** > **Vendas deste ano** > **Valor**.  

    ![campos selecionados](media/desktop-ribbon-charts/power-bi-ribbon-values.png)

    Como o conjunto de dados contém dados para apenas um ano, removemos os campos **Ano** e **Trimestre** da lista **Eixo**.

3. O gráfico de faixa de opções mostra a classificação para cada mês. Observe como a classificação é alterada ao longo do tempo. Por exemplo, a categoria Página Inicial passa de segunda a quinta, de fevereiro a março.

    ![gráfico de faixa de opções](media/desktop-ribbon-charts/power-bi-ribbon.png)

## <a name="format-a-ribbon-chart"></a>Formatar um gráfico de faixa de opções
Quando você cria um gráfico de faixa de opções, você tem opções de formatação disponíveis na seção **Formato** do painel **Visualizações**. As opções de formatação para gráficos de faixa de opções são semelhantes às de um gráfico de colunas empilhadas, com opções de formatação adicionais específicas às faixas de opções.

![modelo de faixa de opções no painel de Visualização](media/desktop-ribbon-charts/power-bi-format-ribbon.png)

Estas opções de formatação para gráficos de faixa de opções permitem que você faça ajustes.

* A opção **Espaçamento** permite ajustar a quantidade de espaço exibida entre as faixas de opções. O número é o percentual da altura máxima da coluna.
* A opção **Corresponder cor da série** permite fazer a correspondência da cor das faixas de opções com a cor da série. Quando definidas como **desligado**, as faixas de opções ficam cinza.
* A opção **Transparência** especifica o grau de transparência das faixas de opções, com o padrão definido como 30.
* A opção **Borda** permite colocar uma borda escura na parte superior e inferior das faixas de opções. Por padrão, as bordas estão desativadas.

Já que o gráfico de faixa de opções não tem rótulos do eixo y, você talvez queira adicionar rótulos de dados. No painel de Formatação, selecione **Rótulos de dados**. 

![opções de formatação para rótulos de dados](media/desktop-ribbon-charts/power-bi-labels.png)

Defina as opções de formatação para seus rótulos de dados. Neste exemplo, definimos a cor do texto como branca e as unidades de exibição como milhares.

![modelo de faixa de opções no painel de Visualização](media/desktop-ribbon-charts/power-bi-data-labels.png)

## <a name="next-steps"></a>Próximas etapas

[Gráficos de dispersão e gráficos de bolhas no Power BI](power-bi-visualization-scatter.md)

[Tipos de visualização no Power BI](power-bi-visualization-types-for-reports-and-q-and-a.md)
