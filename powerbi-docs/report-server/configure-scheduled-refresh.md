---
title: Como configurar a atualização agendada de relatório do Power BI
description: Para atualizar dados em um relatório do Power BI, um plano de atualização agendado deverá ser criado.
author: davidiseminger
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 06/10/2020
ms.author: davidi
ms.openlocfilehash: 3814c0532d94af3265bd608fc7837df982f9b6c4
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85236078"
---
# <a name="how-to-configure-power-bi-report-scheduled-refresh"></a>Como configurar a atualização agendada de relatório do Power BI
Para atualizar dados em um relatório do Power BI no Servidor de Relatórios do Power BI, você deve criar um plano de atualização agendada. Crie esse plano na área *Gerenciar* de um relatório do Power BI no servidor de relatório.

![Atualização agendada bem-sucedida de um relatório do Power BI](media/configure-scheduled-refresh/scheduled-refresh-success.png)

## <a name="configure-data-source-credentials"></a>Configurar credenciais da fonte de dados
Você precisa das permissões necessárias para criar um plano de atualização agendada. As permissões são configuradas nas definições de função do servidor de relatório. Confira [Definições de função – funções predefinidas](https://docs.microsoft.com/sql/reporting-services/security/role-definitions-predefined-roles) na documentação do SQL Server Reporting Services para obter detalhes.

Antes de criar um plano de atualização de dados de agendamento, você precisará definir as credenciais para **cada fonte de dados** usada no relatório do Power BI.

1. No portal da Web, clique com o botão direito do mouse no relatório do Power BI e selecione **Gerenciar**.
   
    ![Selecione Gerenciar no menu de contexto do relatório do Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. No menu à esquerda, selecione a guia **Fontes de dados**.
3. Para cada fonte de dados que aparecer, escolha o tipo de autenticação a ser usado ao conectar-se à fonte de dados. Insira as credenciais apropriadas.
   
    ![Credenciais da fonte de dados na tela Gerenciar relatório](media/configure-scheduled-refresh/data-source-credentials.png)

## <a name="creating-a-schedule-refresh-plan"></a>Criando um plano de agendamento de atualização
Siga estas etapas para criar um plano de atualização agendada.

1. No portal da Web, clique com o botão direito do mouse no relatório do Power BI e selecione **Gerenciar**.
   
    ![Selecione Gerenciar no menu de contexto do relatório do Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. No menu à esquerda, selecione a guia **Atualização agendada**.
3. Na página **Atualização agendada**, selecione **Novo plano de atualização agendada**.
   
    ![Novo plano de atualização agendada](media/configure-scheduled-refresh/new-scheduled-refresh-plan.png)
4. Na página **Novo Plano de Atualização Agendada**, insira uma descrição e agende a atualização do modelo de dados desejado.
5. Selecione **Criar plano de atualização agendada** ao terminar.
   
    ![Criar plano de atualização agendada](media/configure-scheduled-refresh/create-scheduled-refresh-plan.png)

## <a name="modifying-a-schedule-refresh-plan"></a>Modificando um plano de agendamento de atualização
Modificar um plano de atualização agendada é semelhante à criação de um.

1. No portal da Web, clique com o botão direito do mouse no relatório do Power BI e selecione **Gerenciar**.
   
    ![Selecione Gerenciar no menu de contexto do relatório do Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. No menu à esquerda, selecione a guia **Atualização agendada**.
3. Na página **Atualização agendada**, selecione **Editar** ao lado do plano de atualização que você deseja gerenciar.
   
    ![Selecione Editar ao lado do plano que você deseja editar](media/configure-scheduled-refresh/edit-scheduled-refresh-plan.png)
4. Na página **Editar Plano de Atualização Agendada**, insira uma descrição e agende a atualização do modelo de dados desejado.
5. Selecione **Aplicar** quando terminar.
   
    ![A página Editar plano de atualização agendada é semelhante à tela Criar](media/configure-scheduled-refresh/edit-scheduled-refresh-plan-page.png)

## <a name="viewing-the-status-of-schedule-refresh-plan"></a>Exibindo o status do plano de agendamento de atualização
Exiba o status de um plano de agendamento de atualização no portal da Web.

1. No portal da Web, clique com o botão direito do mouse no relatório do Power BI e selecione **Gerenciar**.
   
    ![Selecione Gerenciar no menu de contexto do relatório do Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. No menu à esquerda, selecione a guia **Atualização agendada**.
3. Na página **Atualização agendada**, a coluna da extrema direita exibe o status de um plano.
   
   | **Status** | **Descrição** |
   | --- | --- |
   | Novo Plano de Atualização Agendada |O plano foi criado, mas não executado. |
   | Atualizando |O processo de atualização foi iniciado. |
   | Transmitindo o modelo ao Analysis Server |Copiando o modelo do banco de dados do catálogo de servidores de relatórios para a instância hospedada do Analysis Services. |
   | Atualizando dados |Atualizando os dados no modelo. |
   | Removendo credenciais do modelo |Remoção das credenciais usadas para conectar-se à fonte de dados do modelo. |
   | Salvando modelo no catálogo |A atualização de dados está concluída e o modelo atualizado é salvo no banco de dados de catálogo de servidor de relatório. |
   | Concluído: Atualização de Dados |A atualização está concluída feita. |
   | Erro: |Ocorreu um erro durante a atualização e ele é exibido. |

Para ver o status atual, a página da Web deverá ser atualizada. O status não será alterado automaticamente.

## <a name="next-steps"></a>Próximas etapas
Para obter mais informações sobre como criar e modificar agendas, consulte [Criar, modificar e excluir agendas](https://docs.microsoft.com/sql/reporting-services/subscriptions/create-modify-and-delete-schedules).

Para obter informações sobre como solucionar problemas de atualização agendada, consulte [Solucionar problemas de atualização agendada no Servidor de Relatórios do Power BI](scheduled-refresh-troubleshoot.md).

Mais perguntas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)

