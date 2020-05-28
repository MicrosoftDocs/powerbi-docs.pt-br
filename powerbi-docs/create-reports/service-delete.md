---
title: Excluir um painel, um relatório, uma pasta de trabalho, um conjunto de dados ou um workspace
description: Saiba como excluir quase tudo do Power BI
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 09/11/2018
ms.author: maggies
LocalizationGroup: Common tasks
ms.openlocfilehash: a48d83223ab02d2f9f043dde2facebd6ad73c27a
ms.sourcegitcommit: a72567f26c1653c25f7730fab6210cd011343707
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83565662"
---
# <a name="delete-almost-anything-in-power-bi-service"></a>Excluir quase tudo no serviço do Power BI
Este artigo ensina como excluir um dashboard, um relatório, uma pasta de trabalho, um conjunto de dados, um aplicativo, uma visualização e um workspace no serviço do Power BI.

## <a name="delete-a-dashboard"></a>Excluir um painel
Os painéis podem ser removidos. Remover o painel não exclui o conjunto de dados subjacente ou os relatórios associados a esse painel.

* Se você for o proprietário do painel, poderá removê-lo. Se você compartilhou o painel com colegas, remover o painel de seu workspace do Power BI removerá o painel do workspace do Power BI de seus colegas.
* Se um painel de controle for compartilhado com você e você não deseja vê-lo, é possível removê-lo.  Remover um painel não o remove do workspace do Power BI de outra pessoa.
* Se um dashboard fizer parte de um [pacote de conteúdo organizacional](../collaborate-share/service-organizational-content-pack-disconnect.md), a única maneira de removê-lo é remover o conjunto de dados associado.

### <a name="to-delete-a-dashboard"></a>Excluir um painel
1. Em seu workspace, selecione a guia **Dashboards**.
2. Localize o dashboard a ser excluído e selecione o ícone Excluir ![ícone excluir](media/service-delete/power-bi-delete-icon.png).

    ![vídeo](media/service-delete/power-bi-delete-dash.gif)

## <a name="delete-a-report"></a>Excluir um relatório
Não se preocupe, excluir um relatório não exclui o conjunto de dados que o relatório está baseado.  E quaisquer visualizações que você tenha fixado por meio do relatório também estão seguras - permanecem no painel até você excluí-las individualmente.

### <a name="to-delete-a-report"></a>Para excluir um relatório
1. Em seu workspace, selecione a guia **Relatórios**.
2. Localize o relatório a ser excluído e selecione o ícone Excluir   ![ícone excluir](media/service-delete/power-bi-delete-icon.png).   

    ![guia relatórios do workspace](media/service-delete/power-bi-delete-reportnew.png)
3. Confirme a exclusão.

   ![Caixa de diálogo Excluir relatório](media/service-delete/power-bi-delete-report.png)

   > [!NOTE]
   > Se o relatório fizer parte de um [pacote de conteúdo](../collaborate-share/service-organizational-content-pack-introduction.md), você não poderá excluí-la usando esse método.  Consulte [Remover a conexão com um pacote de conteúdo organizacional](../collaborate-share/service-organizational-content-pack-disconnect.md).
   >
   >

## <a name="delete-a-workbook"></a>Excluir uma pasta de trabalho
As pastas de trabalho podem ser removidas. No entanto, a remoção de uma pasta de trabalho também remove todos os relatórios e blocos de dashboard que contêm dados desta pasta de trabalho.

Se a pasta de trabalho está armazenada no OneDrive for Business, excluí-la do Power BI não a exclui do OneDrive.

### <a name="to-delete-a-workbook"></a>Para excluir uma pasta de trabalho
1. Em seu workspace, selecione a guia **Pastas de trabalho**.
2. Localize a pasta de trabalho a ser excluída e selecione o ícone ![ícone excluir](media/service-delete/power-bi-delete-report2.png) .

    ![Guia Pastas de trabalho](media/service-delete/power-bi-delete-workbooknew.png)
3. Confirme a exclusão.

   ![Caixa de diálogo Remover pasta de trabalho](media/service-delete/power-bi-delete-confirm.png)

## <a name="delete-a-dataset"></a>Excluir um conjunto de dados
Os conjuntos de dados podem ser excluídos. No entanto, excluir um conjunto de dados também exclui todos os relatórios e blocos de painel que contêm dados desse conjunto de dados.

Se um conjunto de dados fizer parte de um ou mais [pacotes de conteúdo organizacional](../collaborate-share/service-organizational-content-pack-disconnect.md), a única maneira de exclui-lo é removê-lo dos pacotes de conteúdo em que ele está sendo usado, aguardar para que isso seja processado e tentar excluí-lo novamente.

### <a name="to-delete-a-dataset"></a>Para excluir um conjunto de dados
1. Em seu workspace, selecione a guia **Conjuntos de dados**.
2. Localize o conjunto de dados para excluir e selecione **Mais opções** (...).  

    ![Guia Conjuntos de dados](media/service-delete/power-bi-delete-datasetnew.png)
3. No menu suspenso, selecione **Excluir**.

   ![menu de reticências](media/service-delete/power-bi-delete-datasetnew2.png)
4. Confirme a exclusão.

   ![Caixa de diálogo Excluir dashboard](media/service-delete/power-bi-delete-dataset-confirm.png)

## <a name="delete-a-workspace"></a>Excluir um workspace
> [!WARNING]
> Quando você cria um workspace, você cria um grupo do Microsoft 365. E quando você exclui um workspace, você exclui esse grupo do Microsoft 365. Isso significa que o grupo também será excluído de outros produtos do Microsoft 365 como o SharePoint e o Microsoft Teams.
>
>

Como autor do workspace, você poderá excluí-lo. Ao excluí-lo, o aplicativo associado também é excluído de todos os membros do grupo e removido do seu AppSource, caso você tenha publicado o aplicativo para toda a sua organização. Excluir um workspace é diferente de sair dele.

### <a name="to-delete-a-workspace---if-you-are-an-admin"></a>Para excluir um workspace – caso você seja um administrador
1. No painel de navegação, selecione **Workspaces**

2. Selecione **Mais opções** (...) à direita do workspace a ser excluído e escolha **Editar workspace**.

    ![Workspaces](media/service-delete/power-bi-delete-workspace.png)

3. Na janela **Editar workspace**, selecione **Excluir workspace** > **Excluir**.

    ![excluir workspace](media/service-delete/power-bi-delete-workspace2.png)

### <a name="to-remove-a-workspace-from-your-list"></a>Para remover um workspace da sua lista
Se não desejar mais ser membro de um workspace, você poderá ***sair*** dele e ele será removido da sua lista. Sair de um workspace deixa-o no lugar para todos os outros membros do workspace.  

> [!IMPORTANT]
> Se você for o único administrador do workspace, o Power BI não permitirá que você saia.
>
>

1. Inicie no workspace que você deseja remover.

2. No canto superior direito, selecione **Mais opções** (...) e escolha **Sair do workspace** > **Sair**.

      ![sair do workspace](media/service-delete/power-bi-leave-workspace.png)

   > [!NOTE]
   > As opções exibidas na lista suspensa dependem se você é um Administrador ou um Membro desse workspace.
   >
   >

## <a name="delete-or-remove-an-app"></a>Excluir ou remover um aplicativo
Os aplicativos podem ser removidos facilmente da sua página de lista de aplicativos. Mas somente um Administrador de aplicativo pode excluir permanentemente um aplicativo.

### <a name="remove-an-app-from-your-app-list-page"></a>Remover um aplicativo de sua página de lista de aplicativos
A exclusão de um aplicativo de sua página de lista de aplicativos não exclui o aplicativo para outros membros.

1. No painel de navegação, selecione **Aplicativos** para abrir a página de lista de aplicativos.
2. Passe o mouse sobre o aplicativo a ser excluído e selecione o ícone Excluir ![](media/service-delete/power-bi-delete-report2.png).

   ![selecionar Aplicativos](media/service-delete/power-bi-delete-app.png)

   Se você remover um aplicativo acidentalmente, você terá várias opções para obtê-lo novamente.  Você pode solicitar ao criador do aplicativo para enviá-lo novamente, pode encontrar o email original com o link para o aplicativo, pode verificar seu [Centro de Notificações](../consumer/end-user-notification-center.md) para ver se a notificação desse aplicativo ainda está listada ou pode verificar o [AppSource da sua organização](../consumer/end-user-apps.md).

## <a name="considerations-and-troubleshooting"></a>Considerações e solução de problemas
Este artigo abordou como excluir os principais elementos básicos do serviço do Power BI. Mas há mais coisas que você pode excluir no Power BI.  

* [Remover seu Dashboard em destaque](../consumer/end-user-featured.md)
* [Remover (dos favoritos) um dashboard](../consumer/end-user-favorite.md)
* [Excluir uma página de relatório](service-delete.md)
* [Excluir um bloco de dashboard](service-dashboard-edit-tile.md)
* [Excluir uma visualização de relatório](service-delete.md)

Mais perguntas? [Experimente a Comunidade do Power BI](https://community.powerbi.com/)
