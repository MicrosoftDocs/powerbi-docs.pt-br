---
title: Inserir um novo Power App em um relatório do Power BI
description: Inserir um aplicativo que usa a mesma fonte de dados e que pode ser filtrado como outros itens de relatório
author: mihart
manager: kvivek
ms.reviewer: tapan maniar
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 06/01/2020
ms.author: rien
LocalizationGroup: Visualizations
ms.openlocfilehash: 78d9d59455a86c5499bc8b01deeacb331bbe7a8b
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90858912"
---
# <a name="tutorial-embed-a-power-apps-visual-in-a-power-bi-report"></a>Tutorial: Inserir um visual do Power Apps em um relatório do Power BI

Neste tutorial, você vai usar o visual do Power Apps para criar um novo aplicativo que é inserido em um relatório de exemplo do Power BI. Este aplicativo interage com outros visuais no relatório.

Caso você não tenha uma assinatura do Power Apps, [crie uma conta gratuita](https://web.powerapps.com/signup?redirect=marketing&email=) antes de começar.

Neste tutorial, você aprenderá a:
> [!div class="checklist"]
> * Adicionar um visual do Power Apps a um relatório do Power BI
> * Trabalhar no Power Apps para criar um novo aplicativo que usa dados do relatório do Power BI
> * Exibir e interagir com o visual do Power Apps no relatório

## <a name="prerequisites"></a>Pré-requisitos

* Navegador [Google Chrome](https://www.google.com/chrome/browser/) ou [Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge)
* Uma [assinatura do Power BI](../fundamentals/service-self-service-signup-for-power-bi.md), com a [Amostra de Análise de Oportunidade](../create-reports/sample-opportunity-analysis.md#get-the-content-pack-for-this-sample) instalada
* Noções básicas de como [criar aplicativos no Power Apps](/powerapps/maker/canvas-apps/data-platform-create-app-scratch) e como [editar relatórios do Power BI](../create-reports/service-the-report-editor-take-a-tour.md)



## <a name="create-a-new-app"></a>Criar um novo aplicativo
Ao adicionar o visual do Power Apps a seu relatório, ele iniciará o Power Apps Studio com uma conexão de dados dinâmicos entre o Power Apps e o Power BI.

1. Abra o relatório de amostra de Análise de Oportunidade e selecione a página *Oportunidades Futuras*. 


2. Mova e redimensione alguns dos blocos do relatório para liberar espaço para o novo visual.

    ![Mover e redimensionar os blocos do relatório](media/power-bi-visualization-powerapp/power-bi-report-page.jpg)

2. No painel Visualizações, selecione o ícone do Power Apps e redimensione o visual para se ajustar ao espaço que você criou.

    ![Painel Visualização com o ícone do Power Apps selecionado](media/power-bi-visualization-powerapp/power-bi-powerapps-icon.jpg)

3. No painel **Campos**, selecione **Nome**, **Código do Produto** e **Estágio da Venda**. 

    ![selecionar campos](media/power-bi-visualization-powerapp/power-bi-fields.png)

4. No visual do Power Apps, selecione o ambiente do Power Apps no qual deseja criar o aplicativo e selecione **Criar novo**.

    ![Criar novo aplicativo](media/power-bi-visualization-powerapp/power-bi-create-new-powerapp.png)

    No Power Apps Studio, você verá que um aplicativo básico foi criado, com uma *galeria* que mostra um dos campos selecionados no Power BI.

    ![O Power Apps é aberto](media/power-bi-visualization-powerapp/power-bi-power-app.png)

5.  Redimensione a galeria para que ela ocupe somente metade da tela. 

6. No painel esquerdo, selecione **Tela1** e defina a propriedade **Preencher** da tela como "LightBlue" (de modo que ela tenha uma melhor exibição no relatório).

    ![paleta de cores](media/power-bi-visualization-powerapp/power-bi-powerapps-fill.png)

6. Libere espaço para um controle de rótulo. 

    ![alterar dimensões da galeria](media/power-bi-visualization-powerapp/power-bi-powerapps-gallery.png)


8. Em **galeria**, insira um controle de rótulo de texto.

   ![controle de rótulo](media/power-bi-visualization-powerapp/power-bi-label.png)

7. Arraste o rótulo para a parte inferior do visual. Defina a propriedade de **Texto** como `"Opportunity Count: " & CountRows(Gallery1.AllItems)`. Agora, ele mostra o número total de oportunidades no conjunto de dados.

    ![Aplicativo com a galeria redimensionada](media/power-bi-visualization-powerapp/power-bi-power-app-label.png)

    ![Aplicativo com o rótulo atualizado](media/power-bi-visualization-powerapp/power-bi-label-live.png)

7. Salve o aplicativo com o nome "aplicativo Oportunidades". 

    ![salve o aplicativo](media/power-bi-visualization-powerapp/power-bi-save-powerapp.png)


## <a name="view-the-app-in-the-report"></a>Exibir o aplicativo no relatório
O aplicativo agora está disponível no relatório do Power BI e interage com outros visuais, pois compartilha a mesma fonte de dados.

![Aplicativo no relatório do Power BI](media/power-bi-visualization-powerapp/power-bi-powerapps-visual.png)

No relatório do Power BI, selecione **Jan** na segmentação, que filtra o relatório inteiro, incluindo os dados do aplicativo.

![relatório filtrado](media/power-bi-visualization-powerapp/power-bi-last.png)

Observe que a contagem de oportunidades no aplicativo corresponde à contagem no canto superior esquerdo do relatório. Selecione outros itens no relatório e os dados no aplicativo serão atualizados.


## <a name="clean-up-resources"></a>Limpar os recursos
Caso não deseje mais usar a Amostra de Análise de Oportunidade, exclua o dashboard, o relatório e o conjunto de dados.

## <a name="limitations-and-considerations"></a>Limitações e considerações
Para obter informações sobre solução de problemas, consulte [Visual do Power Apps para Power BI](/powerapps/maker/canvas-apps/powerapps-custom-visual#limitations-of-the-power-apps-visual)

## <a name="next-steps"></a>Próximas etapas
[Visual de P e R](power-bi-visualization-types-for-reports-and-q-and-a.md)    
[Tutorial: Inserir um visual do Power Apps em um relatório do Power BI](/powerapps/maker/canvas-apps/powerapps-custom-visual)