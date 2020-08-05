---
title: Executar e exibir insights em blocos do painel
description: Como usuário final do Power BI, saiba como obter insights sobre seus blocos de painel.
author: mihart
ms.reviewer: mihart
featuredvideoid: et_MLSL2sA8
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 06/22/2020
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: 5fa66f2ff3650e4b4578207c2c70b70041c2c3d5
ms.sourcegitcommit: 2131f7b075390c12659c76df94a8108226db084c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/03/2020
ms.locfileid: "87537724"
---
# <a name="view-data-insights-on-dashboard-tiles-with-power-bi"></a>Exibir insights de dados em blocos do painel com o Power BI

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

Cada bloco de [visual](end-user-tiles.md) em seu dashboard é uma porta de entrada para exploração de dados. Quando você seleciona um bloco, ele abre um relatório ou [abre a seção de P e R](end-user-q-and-a.md), em que você pode filtrar, classificar e examinar o conjunto de dados do relatório. E quando você executa insights, o Power BI faz a exploração de dados para você.

![modo de menu de reticências](./media/end-user-insights/power-bi-insight.png)

Execute insights para gerar visuais interativos e interessantes com base em seus dados. Insights podem ser executados em um bloco de dashboard específico, e você pode até mesmo executar insights em um insight.

O recurso Insights tem como base um crescente [conjunto de algoritmos analíticos avançados](end-user-insight-types.md), desenvolvido em conjunto com o Microsoft Azure for Research, os quais continuaremos a usar para permitir que mais pessoas encontrem informações em seus próprios dados de maneiras novas e intuitivas.

## <a name="run-insights-on-a-dashboard-tile"></a>Executar insights em um bloco do painel
Quando você executar insights em um bloco do dashboard, o Power BI pesquisa apenas os dados usados para criar esse bloco de dashboard único. 

1. [Abra um dashboard](end-user-dashboards.md).
2. Passe o mouse sobre um bloco. Selecione **Mais opções** (...) e **Exibir insights**. 

    ![modo de menu de reticências](./media/end-user-insights/power-bi-hovers.png)


3. O bloco é aberto no [modo de foco](end-user-focus.md) com os cartões de insights exibidos à direita.    
   
    ![Modo de foco](./media/end-user-insights/power-bi-insights-tile.png)    
4. Algum insight desperta seu interesse? Selecione esse cartão de insights para se aprofundar ainda mais. O insight selecionado aparece à esquerda e novos insights, com base apenas nos dados daquele único insight, são exibidos à direita.    

 ## <a name="interact-with-the-insight-cards"></a>Interagir com os cartões de insights
Depois que você tiver um insight aberto, continue a explorar.

   * Filtre esse visual na tela.  Para exibir os filtros, no canto superior direito, selecione a seta para expandir o painel Filtros.

      ![análise de um menu Filtros expandido](./media/end-user-insights/power-bi-filters.png)
   
   * Execute insights no cartão de insight em si. Isso é conhecido como **insights relacionados**. Selecione um cartão de insight para ativá-lo. Ele será exibido na tela de relatório.
   
      ![análise de um menu Filtros expandido](./media/end-user-insights/power-bi-insight-card.png)
   
   * No canto superior direito, selecione o ícone de lâmpada ![ícone Obter insights](./media/end-user-insights/power-bi-bulb-icon.png) ou **Obter insights**. O insight é exibido à esquerda e novos cartões, com base apenas nos dados daquele único insight, são exibidos à direita.
     
     ![barra de menus mostrando o ícone Obter Insights](./media/end-user-insights/power-bi-related.png)
     
Para retornar ao relatório, no canto superior esquerdo, selecione **Sair do modo de foco**.

## <a name="considerations-and-troubleshooting"></a>Considerações e solução de problemas
- **Exibir insights** não funciona com todos os tipos de bloco do dashboard. Por exemplo, ele não está disponível para visuais personalizados do Power BI.<!--[Power BI visuals](end-user-custom-visuals.md)-->


## <a name="next-steps"></a>Próximas etapas

Executar insights sobre visuais de relatórios [usando o recurso Analisar](end-user-analyze-visuals.md)    
Saiba mais sobre os [tipos de Insights Rápidos disponíveis](end-user-insight-types.md)

