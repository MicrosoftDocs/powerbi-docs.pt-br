---
title: 'Como fixar uma página inteira do relatório em um painel do Power BI '
description: Documentação sobre como fixar uma página dinâmica inteira do relatório em um dashboard do Power BI por meio de um relatório.
author: maggiesMSFT
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 03/02/2018
ms.author: maggies
LocalizationGroup: Dashboards
ms.openlocfilehash: 157fc47050d7210e1424bb922782c8a3af6e61fb
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85219242"
---
# <a name="pin-an-entire-report-page-as-a-live-tile-to-a-power-bi-dashboard"></a>Fixar uma página inteira do relatório, como um bloco dinâmico, em um painel do Power BI
Outra maneira de adicionar um novo [bloco do dashboard](../consumer/end-user-tiles.md) é fixar uma página inteira do relatório. Essa é uma maneira fácil de fixar mais de uma visualização por vez.  Além disso, quando você fixa uma página inteira, os blocos são *dinâmicos*, sendo possível interagir com eles diretamente no painel. E as alterações feitas a qualquer uma das visualizações no editor de relatórios, como adicionar um filtro ou alterar os campos usados no gráfico, também são refletidas no bloco do painel.  

Fixar blocos dinâmicos de relatórios nos painéis só está disponível no serviço Power BI (app.powerbi.com).

> [!NOTE]
> Não é possível fixar blocos de relatórios que são compartilhados com você.
> 
> 

## <a name="pin-a-report-page"></a>Fixar uma página do relatório
Veja Amanda fixar uma página dinâmica do relatório em um dashboard e siga as instruções passo a passo abaixo do vídeo para testá-lo por conta própria.

<iframe width="560" height="315" src="https://www.youtube.com/embed/EzhfBpPboPA" frameborder="0" allowfullscreen></iframe>


1. Abra um relatório no [Modo de Exibição de Edição](service-interact-with-a-report-in-editing-view.md).
2. Sem nenhuma visualização selecionada, na barra de menus, selecione **Fixar esta Página em Tempo Real**.
   
   ![Ícone Fixar página em tempo real](media/service-dashboard-pin-live-tile-from-report/pbi-pin-live-page.png) 
3. Fixe o bloco em um painel existente ou em um novo painel. Observe o texto realçado: *Fixar esta página em tempo real permite que as alterações nos relatórios sejam exibidas no bloco do painel quando a página é atualizada.*
   
   * Painel existente: selecione o nome do painel no menu suspenso. Painéis que foram compartilhados com você não aparecerão na lista suspensa.
   * Novo painel: digite o nome do novo painel.
     
     ![Caixa de diálogo Fixar no dashboard](media/service-dashboard-pin-live-tile-from-report/pbi-pin-live-page-dialog.png)
4. Selecione **Fixar em tempo real**. Uma mensagem de Êxito (próximo ao canto superior direito) informa que a página foi adicionada, como um bloco, ao painel.

## <a name="open-the-dashboard-to-see-the-pinned-live-tile"></a>Abrir o dashboard para ver o bloco dinâmico fixado
1. No painel de navegação, selecione o dashboard com o novo bloco dinâmico. Nele, você pode executar ações como [renomear, redimensionar, vincular e mover](service-dashboard-edit-tile.md) a página de relatório fixada.  
2. Interagir com os blocos dinâmicos.  Na captura de tela abaixo, selecionando uma barra no gráfico de colunas há um filtro cruzado e realçado entre outras visualizações do bloco.
   
    ![dashboards com um bloco dinâmico](media/service-dashboard-pin-live-tile-from-report/pbi-live-tile.png)

## <a name="next-steps"></a>Próximas etapas
[Dashboards no Power BI](../consumer/end-user-dashboards.md)

Mais perguntas? [Experimente a Comunidade do Power BI](https://community.powerbi.com/)
