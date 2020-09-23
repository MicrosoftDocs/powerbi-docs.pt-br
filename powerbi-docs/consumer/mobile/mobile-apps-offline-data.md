---
title: Exibir os dados offline em aplicativos móveis do Power BI
description: 'Leia sobre uma das vantagens de exibir o Power BI em um aplicativo móvel em vez de em um navegador móvel: você pode ver seus dados mesmo quando não estiver conectado a uma rede.'
author: paulinbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 12/09/2019
ms.author: painbar
ms.openlocfilehash: 3b7f578040a49438ccca89fd9112a3ca5079a20a
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90856014"
---
# <a name="view-your-data-offline-in-the-power-bi-mobile-apps"></a>Exibir os dados offline em aplicativos móveis do Power BI
Aplica-se a:

| ![iPhone](./media/mobile-apps-offline-data/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-offline-data/ipad-logo-50-px.png) | ![Telefone Android](./media/mobile-apps-offline-data/android-phone-logo-50-px.png) | ![Tablet Android](./media/mobile-apps-offline-data/android-tablet-logo-50-px.png) | ![Windows 10](./media/mobile-apps-offline-data/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhones |iPads |Telefones Android |Tablets Android |Dispositivos Windows 10 |

>[!NOTE]
>O suporte de aplicativo móvel Power BI para **telefones que usam o Windows 10 Mobile** será descontinuado em 16 de março de 2021. [Saiba mais](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

Uma vantagem da visualização do Power BI em um aplicativo móvel em vez de em um navegador móvel é que você pode ver os dados mesmo quando não estiver conectado a uma rede. 

![Sem mensagem de rede](./media/mobile-apps-offline-data/power-bi-iphone-no-network.png)

Por padrão, o Power BI atualiza os dados com frequência para que você obtenha respostas atualizadas para suas questões de negócios a qualquer momento, mesmo durante o transporte ou viagens.

## <a name="data-access-while-youre-offline"></a>Acesso a dados enquanto estiver offline
Enquanto estiver offline, você poderá acessar e interagir com os painéis que tenha acessado anteriormente por meio do aplicativo móvel.

Você também tem acesso somente leitura a todos os relatórios do Power BI que tiver acessado anteriormente do aplicativo móvel. Você pode ver o relatório completo, mas não filtrar, aplicar filtro cruzado, classificar ou usar segmentações de dados nele.

>[!NOTE]
> Os relatórios baseados no DirectQuery não são armazenados em cache e não estão disponíveis offline.

## <a name="background-data-refresh"></a>Atualização de dados em segundo plano
A atualização em segundo plano atualiza seus dashboard favoritos, assim como os dashboards e relatórios que você exibiu nas últimas duas semanas, com os dados no serviço do Power BI (não a fonte de dados). Se você estiver conectado ao Wi-Fi, a atualização em segundo plano atualizará a cada duas horas. Caso contrário, se você estiver em uma rede 3G, o Power BI atualizará o conteúdo a cada 24 horas.

É possível desligar a atualização em segundo plano, por exemplo, para evitar o uso da rede. Verifique as configurações do seu dispositivo.

> [!NOTE]
> Se você usar o aplicativo móvel do Power BI em seu dispositivo iOS e sua organização tiver configurado o Microsoft Intune MAM, a atualização de dados em segundo plano será desabilitada. Na próxima vez que você entrar no aplicativo, o Power BI atualiza os dados do serviço do Power BI na Web.
> 
> Leia mais sobre [Configurar aplicativos móveis do Power BI com o Microsoft Intune](../../admin/service-admin-mobile-intune.md). 
> 
> 

## <a name="offline-indicators"></a>Indicadores offline
O Power BI fornece indicadores claros quando você entrar e sair do modo offline, bem como indicadores de painés, relatórios e blocos ausentes que não estão disponíveis offline.

## <a name="limitations"></a>Limitações
Quando estiver offline com o Power BI em seu dispositivo móvel, talvez você tenha estas limitações:

* O Power BI pode armazenar em cache até 250 MB de dados offline.
* Alguns tipos de peças precisam de uma conexão de servidor ativa e, portanto, não estão disponíveis offline. Por exemplo, peças de mapa do Bing e algumas peças personalizadas.
* Pastas de trabalho do Excel inteiras no Power BI não estão disponíveis offline.
* Você poderá ver os relatórios móveis e KPIs do Reporting Services offline se eles foram exibidos quando você estava conectado. Eles não são atualizadas em segundo plano. Elas são atualizadas sempre que você as abri-las.
* Nos aplicativos móveis do Power BI, não é possível ver os arquivos do Power BI Desktop (.pbix) salvos no Servidor de Relatórios do Power BI. 
* Relatórios paginados (RDL) não ficam disponíveis enquanto a rede está offline.

## <a name="next-steps"></a>Próximas etapas
Seus comentários nos ajudam a decidir o que implementar no futuro, portanto, não deixe de votar em outros recursos que você gostaria de ver em aplicativos móveis do Power BI. 

* [Aplicativos do Power BI para dispositivos móveis](mobile-apps-for-mobile-devices.md)
* Siga @MSPowerBI no Twitter
* Participe da conversa na [Comunidade do Power BI](https://community.powerbi.com/)
* [O que é o Power BI?](../../fundamentals/power-bi-overview.md)