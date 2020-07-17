---
title: Como fixar um bloco em um dashboard de P e R
description: Documentação sobre como fixar um bloco em um dashboard do Power BI por meio da caixa de P e R
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 03/02/2018
ms.author: maggies
LocalizationGroup: Dashboards
ms.openlocfilehash: 76c76cf5ae41c369e3810f3a52ee43816184d8e1
ms.sourcegitcommit: e8ed3d120699911b0f2e508dc20bd6a9b5f00580
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "86263056"
---
# <a name="pin-a-tile-to-a-dashboard-from-qa"></a>Fixar um bloco em um dashboard de P e R
## <a name="how-to-pin-a-tile-from-qa"></a>Como fixar um bloco de P e R
P e R é a ferramenta de geração de relatórios ad hoc do Power BI. Precisa encontrar uma visão particular? Faça uma pergunta sobre os dados e receba uma resposta na forma de uma visualização.

Nestas instruções, usaremos o serviço do Power BI (app.powerbi.com) para abrir um dashboard, fazer uma pergunta usando idioma natural para criar uma visualização e fixar essa visualização em um dashboard. Dashboards não estão disponíveis no Power BI Desktop. Para obter informações sobre como usar P e R com outras ferramentas e conteúdo do Power BI, consulte a [Visão geral de P e R do Power BI](../consumer/end-user-q-and-a.md). 

Para acompanhar, abra o [painel de exemplo da Análise de Varejo](sample-retail-analysis.md).


1. Abra um [dashboard](../consumer/end-user-dashboards.md) que tenha pelo menos um bloco fixado de um relatório. Quando você faz uma pergunta, o Power BI procura a resposta em qualquer conjunto de dados que tenha um bloco fixado a esse dashboard.  Para saber mais, veja [obter dados](../connect-data/service-get-data.md).
2. Na caixa de pergunta, na parte superior do painel, comece a digitar o que você deseja saber sobre os dados.  
   ![caixa de perguntas de P e R](media/service-dashboard-pin-tile-from-q-and-a/power-bi-question-box.png)
3. Por exemplo, ao digitar “vendas do ano passado por mês e território”...  
   ![digitar uma pergunta](media/service-dashboard-pin-tile-from-q-and-a/power-bi-type-q-and-a.png)

   a caixa de perguntas oferece sugestões.
4. Para adicionar o gráfico ao dashboard como um bloco, selecione o marcador ![Ícone de fixação](media/service-dashboard-pin-tile-from-q-and-a/pbi_pintile.png) no lado superior direito da tela. Se o dashboard tiver sido compartilhado com você, você não poderá fixar nenhuma visualização.

5. Fixe o bloco em um painel existente ou em um novo painel.

   ![Caixa de diálogo Fixar no dashboard](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin-to-dashboard.png)

   * Painel existente: selecione o nome do painel no menu suspenso. Suas opções serão limitadas apenas aos painéis no workspace atual.
   * Novo dashboard: digite o nome do novo dashboard e ele será adicionado ao seu workspace atual.

6. Selecione **Fixar**.

   Uma mensagem de êxito (perto do canto superior direito) informa que a visualização foi adicionada, como um bloco, ao dashboard.  

   ![Fixado ao dashboard](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin.png)
7. Selecione **Ir para o dashboard** para ver o novo bloco. Lá, é possível [renomear, redimensionar, adicionar um hiperlink, reposicionar o bloco e muito mais](service-dashboard-edit-tile.md) no dashboard.

   ![painel com blocos](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a>Considerações e solução de problemas
* Quando você começa a digitar uma pergunta, o P e R imediatamente começa a procurar a melhor resposta de todos os conjuntos de dados associados com o painel atual.  O "dashboard atual" é o dashboard listado no painel de navegação superior. Por exemplo, essa pergunta está sendo feita no dashboard de **exemplo Análise de Varejo**, que faz parte do workspace **mihart**.

  ![trilhas](media/service-dashboard-pin-tile-from-q-and-a/power-bi-navbar.png)
* **Como a P e R sabe quais conjuntos de dados deverão ser usados**?  A P e R tem acesso a todos os conjuntos de dados que têm pelo menos uma visualização fixada nesse dashboard.

* **Você não vê a caixa de perguntas**? Verifique com seu administrador do Power BI. O administrador tem a capacidade de desabilitar a P e R.


## <a name="next-steps"></a>Próximas etapas
[Renomear, redimensionar, adicionar um hiperlink, reposicionar o bloco e muito mais](service-dashboard-edit-tile.md)    
[Exibir seu bloco do dashboard no Modo de foco](../consumer/end-user-focus.md)     
[Voltar a P e R no Power BI](../consumer/end-user-q-and-a.md)  
Mais perguntas? [Experimente a Comunidade do Power BI](https://community.powerbi.com/)
