---
title: Definir alertas de dados nos aplicativos móveis do Power BI
description: Saiba como definir alertas nos aplicativos móveis do Power BI para receber notificações quando os dados em um painel são alterados além dos limites definidos.
author: paulinbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/11/2019
ms.author: painbar
ms.openlocfilehash: 6cddfd820da45de6141b698b8cb6e3c2bfc68069
ms.sourcegitcommit: e8ed3d120699911b0f2e508dc20bd6a9b5f00580
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "86264895"
---
# <a name="set-data-alerts-in-the-power-bi-mobile-apps"></a>Definir alertas de dados nos aplicativos móveis do Power BI
Aplica-se a:

| ![iPhone](./media/mobile-set-data-alerts-in-the-mobile-apps/iphone-logo-50-px.png) | ![iPad](./media/mobile-set-data-alerts-in-the-mobile-apps/ipad-logo-50-px.png) | ![Telefone Android](./media/mobile-set-data-alerts-in-the-mobile-apps/android-phone-logo-50-px.png) | ![Tablet Android](./media/mobile-set-data-alerts-in-the-mobile-apps/android-tablet-logo-50-px.png) | ![Tablet Android](./media/mobile-set-data-alerts-in-the-mobile-apps/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhones |iPads |Telefones Android |Tablets Android |Dispositivos com Windows 10 |

Você pode definir alertas em painéis nos aplicativos móveis do Power BI e no serviço do Power BI. Os alertas notificam quando dados em um bloco são alterados além dos limites definidos. Os alertas funcionam em blocos que contêm um único número, como cartões e medidores, mas não em dados de streaming. É possível definir alertas de dados no seu dispositivo móvel e vê-los no serviço do Power BI e vice-versa. Só você pode ver os alertas de dados que você definir, mesmo que você compartilhe um painel ou um instantâneo de um bloco.

Você pode definir alertas em blocos se tiver uma licença do Power BI Pro ou se o dashboard compartilhado estiver com capacidade de Premium. 

> [!WARNING]
> Notificações de alerta controladas por dados fornecem informações sobre seus dados. Se o dispositivo for roubado, recomendamos que você vá para o serviço do Power BI para desligar todas as regras de alerta controladas por dados. 
> 
> Saiba mais sobre o [gerenciamento de alertas de dados no serviço do Power BI](../../create-reports/service-set-data-alerts.md).
> 
> 

## <a name="data-alerts-on-an-iphone-or-ipad"></a>Alertas de dados em um iPhone ou iPad
### <a name="set-an-alert-on-an-iphone-or-ipad"></a>Definir um alerta em um iPhone ou iPad
1. Toque em um número ou bloco em um dashboard para abri-lo em modo de foco.  
   
   ![Captura de tela de um dashboard mostrando o bloco do medidor no modo de foco.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-card-visual.png)
2. Toque no ícone de sino ![Ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-alert-icon.png) para adicionar um alerta.  
3. Toque em **Adicionar regra de alerta**.
   
   ![Captura de tela da regra de alerta mostrando que nenhum alerta foi definido.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-add-alert-rule.png)
4. Opte por receber alertas acima ou abaixo de um valor e defina o valor.
   
   ![Captura de tela das configurações de alerta mostrando o título e o valor do alerta a ser definido](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-set-alert-threshold.png)
5. Decida se deseja receber por hora ou alertas diários e se também deseja receber um email quando um alerta for enviado.
   
   > [!NOTE]
   > Você não recebe alertas a cada hora ou diariamente, a menos que os dados estejam realmente atualizados no momento.
   > 
   > 
6. Também é possível alterar o título do alerta.
7. Toque em **Salvar**.
8. Um único bloco pode ter alertas para valores acima e abaixo dos limites. Em **Gerenciar alertas**, toque em **Adicionar regra de alerta**.
   
   ![Captura de tela de Gerenciar alerta mostrando um ponteiro para adicionar uma regra de alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-add-another-alert-rule.png)

### <a name="manage-alerts-on-your-iphone-or-ipad"></a>Gerenciar alertas no seu iPhone ou iPad
Você pode gerenciar os alertas individuais no seu dispositivo móvel ou [gerenciar todos os alertas no serviço do Power BI](../../create-reports/service-set-data-alerts.md).

1. Em um dashboard, toque em um bloco de números ou medidores que tenha um alerta.  
   
   ![Captura de tela do dashboard mostrando o bloco de número que tem um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-card-visual_has_alert.png)

2. Toque no ícone de sino ![Ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-has-alert-icon.png).  
3. Toque no nome do alerta para editá-lo, toque no controle deslizante para desligar os alertas de email ou toque na lata de lixo para excluir o alerta.
   
    ![Captura de tela de um alerta, apontando para o nome do alerta, a lixeira para exclui-lo e o controle deslizante para desativá-lo.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-edit-delete-alert.png)

## <a name="data-alerts-on-an-android-device"></a>Alertas de dados em um dispositivo Android
### <a name="set-an-alert-on-an-android-device"></a>Definir um alerta em um dispositivo Android
1. No dashboard do Power BI, toque em um bloco de número ou medidor para abri-lo.  
2. Toque no ícone de sino ![Ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-alert-icon.png) para adicionar um alerta.  
   
   ![Captura de tela do dashboard mostrando o bloco de número que tem um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-tap-alert.png)
3. Toque no ícone de mais (+).
   
   ![Captura de tela de Gerenciar alertas mostrando um ponteiro para o ícone de adição.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-plus-alert.png)
4. Opte por receber alertas acima ou abaixo de um valor e digite o valor.
   
   ![Captura de tela da configuração de alerta mostrando ponteiros para Salvar e Concluído.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-tablet-set-alert-condition.png)
5. Toque em **Concluído**.
6. Decida se deseja receber por hora ou alertas diários e se também deseja receber um email quando um alerta for enviado.
   
   > [!NOTE]
   > Você não recebe alertas a cada hora ou diariamente, a menos que os dados estejam realmente atualizados no momento.
   > 
   > 
7. Também é possível alterar o título do alerta.
8. Toque em **Salvar**.

### <a name="manage-alerts-on-an-android-device"></a>Gerenciar alertas em um dispositivo Android
Você pode gerenciar os alertas individuais no aplicativo móvel do Power BI ou [gerenciar todos os alertas no serviço do Power BI](../../create-reports/service-set-data-alerts.md).

1. Em um dashboard, toque em um bloco de cartões ou medidores que tenha um alerta.  
2. Toque no ícone de sino sólido ![Ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-filled-alert-bell.png).  
3. Toque no alerta para alterar um valor ou desativá-lo.
   
    ![Captura de tela do bloco Gerenciar alerta mostrando o ícone de adição para adicionar um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-manage-alerts.png)
4. Toque no ícone de adição (+) para adicionar outro alerta no mesmo bloco.
5. Para excluir o alerta por completo, toque no ícone de lixeira ![Ícone de lixeira](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-delete-alert-icon.png).

## <a name="data-alerts-on-a-windows-device"></a>Alertas de dados em um dispositivo Windows

>[!NOTE]
>O suporte de aplicativo móvel Power BI para **telefones que usam o Windows 10 Mobile** será descontinuado em 16 de março de 2021. [Saiba mais](https://go.microsoft.com/fwlink/?linkid=2121400)

### <a name="set-data-alerts-on-a-windows-device"></a>Definir alertas de dados em um dispositivo Windows
1. Toque em um bloco de números ou medidores em um dashboard para abri-lo.  
2. Toque no ícone de sino ![Ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-alert-bell-off.png) para adicionar um alerta.  
   
   ![Captura de tela do dashboard mostrando o bloco de número que tem um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-tap-alert.png)
3. Toque no ícone de mais (+).
   
   ![Captura de tela de Gerenciar alertas mostrando que nenhum alerta foi definido.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-no-alerts-yet.png)
4. Opte por receber alertas acima ou abaixo de um valor e digite o valor.
   
   ![Captura de tela das configurações de alerta mostrando as entradas usadas para editar o alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-set-alert.png)
5. Decida se deseja receber por hora ou alertas diários e se também deseja receber um email quando um alerta for enviado.
   
   > [!NOTE]
   > Você não recebe alertas a cada hora ou diariamente, a menos que os dados estejam realmente atualizados no momento.
   > 
   > 
6. Também é possível alterar o título do alerta.
7. Toque na marca de seleção.
8. Um único bloco pode ter alertas para valores acima e abaixo dos limites. Em **Gerenciar alertas**, toque no sinal de mais (+).
   
   ![Captura de tela de Gerenciar alertas mostrando o sinal de adição usado para adicionar um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-add-another-alert.png)

### <a name="manage-alerts-on-a-windows-device"></a>Gerenciar alertas em um dispositivo Windows
Você pode gerenciar os alertas individuais no aplicativo móvel do Power BI ou [gerenciar todos os alertas no serviço do Power BI](../../create-reports/service-set-data-alerts.md).

1. Em um dashboard, toque em um bloco de cartões ou medidores que tenha um alerta.  
2. Toque no ícone de sino ![Ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-alert-bell-on.png).  
   
   ![Captura de tela do dashboard mostrando o bloco de número que tem um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-has-alerts.png)
3. Toque no alerta para alterar um valor ou desativá-lo.
   
    ![Captura de tela de Gerenciar alertas mostrando o sinal de adição usado para adicionar um alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-add-another-alert.png)
4. Para excluir completamente o alerta, clique com o botão direito do mouse ou toque e segure > **Excluir**.

## <a name="receiving-alerts"></a>Recebendo alertas
Você recebe alertas na [Central de Notificações](mobile-apps-notification-center.md) do Power BI no seu dispositivo móvel ou no serviço do Power BI, juntamente com as notificações sobre novos dashboards que alguém compartilhou com você.

As fontes de dados geralmente são configuradas para atualização diária, embora algumas sejam atualizadas com mais frequência. Quando os dados no dashboard forem atualizados, se os dados que estão sendo controlados atingirem um dos limites que você definiu, várias coisas acontecerão.

1. O Power BI verifica se passou mais de uma hora ou mais de 24 horas (dependendo da opção selecionada) desde o envio do último alerta.
   
   Enquanto os dados estiverem acima do limite, você receberá um alerta a cada uma hora ou a cada 24 horas.
2. Se tiver definido que o alerta deve lhe enviar um email, você verá algo parecido com isto na Caixa de Entrada.
   
   ![Captura de tela de uma notificação por email mostrando o alerta.](media/mobile-set-data-alerts-in-the-mobile-apps/powerbi-alerts-email.png)
3. O Power BI adiciona uma mensagem ao seu [Centro de notificações](mobile-apps-notification-center.md) e adiciona um ponto amarelo ao ícone de sino ![ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/powerbi-alert-tile-notification-icon.png) na barra de título (iOS e Android) ou ao botão de navegação global ![botão de navegação global](./media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-alert-global-nav-button.png) (dispositivos Windows 10).


4. Toque no ícone de sino ![ícone de sino](media/mobile-set-data-alerts-in-the-mobile-apps/powerbi-alert-tile-notification-icon.png) ou no botão de navegação global ![botão de navegação global](./media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-alert-global-nav-button.png) para [abrir seu **Centro de notificações**](mobile-apps-notification-center.md) e ver os detalhes do alerta.
   
     

> [!NOTE]
> Os alertas funcionam somente em dados que estão atualizados. Depois que os dados são atualizados, o Power BI verifica se foi definido um alerta para esses dados. Se os dados atingirem um limite de alerta, um alerta será disparado.
> 
> 

## <a name="tips-and-troubleshooting"></a>Dicas e solução de problemas
* Não há suporte atualmente para alertas para blocos do Bing ou blocos de cartões com medidas de data/hora.
* Os alertas funcionam apenas com dados numéricos.
* Os alertas funcionam somente em dados que estão atualizados. Eles não funcionam em dados estáticos.
* Os alertas não funcionam com blocos que contêm dados de streaming.

## <a name="next-steps"></a>Próximas etapas
* [Gerenciar seus alertas no serviço do Power BI](../../create-reports/service-set-data-alerts.md)
* [Central de Notificações do Power BI Mobile](mobile-apps-notification-center.md)
* Perguntas? [Experimente perguntar para a Comunidade do Power BI](https://community.powerbi.com/)
