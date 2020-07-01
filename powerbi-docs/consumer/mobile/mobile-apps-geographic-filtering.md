---
title: Filtrar relatório por localização geográfica em um aplicativo móvel do Power BI
description: Saiba como você pode filtrar um relatório por localização geográfica nos aplicativos móveis do Power BI da Microsoft se o proprietário do relatório definir marcações geográficas.
author: paulinbar
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.author: painbar
ms.openlocfilehash: 4cf94628b1d423d5b382e718d850fc403d516083
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85234318"
---
# <a name="filter-a-report-by-geographic-location-in-the-power-bi-mobile-apps"></a>Filtrar um relatório por localização geográfica nos aplicativos móveis do Power BI
Aplica-se a:

| ![iPhone](./media/mobile-apps-geographic-filtering/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-geographic-filtering/ipad-logo-50-px.png) | ![Telefone Android](./media/mobile-apps-geographic-filtering/android-phone-logo-50-px.png) | ![Tablet Android](./media/mobile-apps-view-dashboard/android-tablet-logo-50-px.png) | ![Windows Phone](./media/mobile-apps-geographic-filtering/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhones |iPads |Telefones Android |Tablets Android |Telefones Windows 10 |

Ao examinar um relatório do Power BI em seu dispositivo móvel, você vê um pequeno ícone de tachinha no canto superior direito? Nesse caso, você pode filtrar o relatório com base em sua localização geográfica.

> [!NOTE]
> Só será possível filtrar por localização se os nomes geográficos no relatório estiverem em inglês; por exemplo, “New York City” ou “Germany”. Tablets e PCs com Windows 10 não oferecem suporte a filtragem geográfica, mas celulares com Windows 10 fazem.

>[!NOTE]
>O suporte de aplicativo móvel Power BI para **telefones que usam o Windows 10 Mobile** será descontinuado em 16 de março de 2021. [Saiba mais](https://go.microsoft.com/fwlink/?linkid=2121400)

## <a name="filter-your-report-by-your-geographic-location"></a>Filtrar o relatório por localização geográfica
1. Abra um relatório no aplicativo móvel do Power BI em seu dispositivo móvel.
2. Se o relatório tiver dados geográficos, você verá uma mensagem pedindo para permitir que o Power BI acesse sua localização. Clique em **Permitir** e, em seguida, toque em **Permitir** novamente.
3. Toque na tachinha ![Ícone de tachinha](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-icon.png). Você pode filtrar por cidade, por estado/província ou por país/região, dependendo dos dados no relatório. O filtro lista apenas as opções que correspondem à sua localização atual.
   
    ![Filtro de tachinha](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-map-set-filter.png)

## <a name="why-dont-i-see-location-tags-on-a-report"></a>Por que não vejo marcações de localização em um relatório?
Todas as três condições abaixo precisam ser verdadeiras para que seja possível ver as marcações de localização. 

* A pessoa que criou o relatório no Power BI Desktop precisa ter [categorizado os dados geográficos](../../transform-model/desktop-mobile-geofiltering.md) em pelo menos uma coluna, como cidade, estado ou país/região.
* Você está em um dos locais que contém dados nessa coluna.
* Você está usando um desses dispositivos móveis:
  * iOS (iPad, iPhone, iPod).
  * Android (celular, tablet).
  * Celular com Windows 10 (outros dispositivos com Windows 10, como PCs e tablets que não dão suporte para filtragem geográfica).

Leia mais sobre a [configuração da filtragem geográfica](../../transform-model/desktop-mobile-geofiltering.md) no Power BI Desktop.

### <a name="next-steps"></a>Próximas etapas
* [Conectar-se a dados do Power BI do mundo real](mobile-apps-data-in-real-world-context.md) com os aplicativos móveis
* [Categorização de dados no Power BI Desktop](../../transform-model/desktop-data-categorization.md) 
* Perguntas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)
