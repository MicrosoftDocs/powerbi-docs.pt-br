---
title: Gerenciar o armazenamento de dados em workspaces
description: Saiba como gerenciar seu armazenamento de dados em seu workspace individual ou workspace comum para garantir que possa continuar publicando relatórios e conjuntos de dados.
author: maggiesMSFT
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 02/25/2020
ms.author: maggies
LocalizationGroup: Administration
ms.openlocfilehash: 50d3adef65791c3fecd1a2125f67318fb8ab0298
ms.sourcegitcommit: c83146ad008ce13bf3289de9b76c507be2c330aa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2020
ms.locfileid: "86214252"
---
# <a name="manage-data-storage-in-power-bi-workspaces"></a>Gerenciar o armazenamento de dados em workspaces do Power BI

Saiba como gerenciar seu armazenamento de dados em seu workspace individual para que você possa continuar publicando relatórios e conjuntos de dados.

## <a name="capacity-limits"></a>Limites de capacidade

Os limites de armazenamento do workspace, sejam para meu workspace ou um workspace de aplicativo, dependem de se o workspace está em [capacidade compartilhada ou Premium](../fundamentals/service-basic-concepts.md#capacities).

### <a name="shared-capacity-limits"></a>Limites de capacidade compartilhada
Para workspaces em capacidade compartilhada: 

- Há um limite de armazenamento de 100 GB por workspace.
- Para workspaces de aplicativos, o uso total não pode exceder o limite de armazenamento do locatário de 10 GB, multiplicado pelo número de licenças Pro no locatário.

### <a name="premium-capacity-limits"></a>Limites de capacidade Premium
Para workspaces na capacidade Premium:
- Há um limite de 100 TB por capacidade Premium.
- Não há limite de armazenamento por usuário.

Leia sobre outros recursos do [modelo de preços do Power BI](https://powerbi.microsoft.com/pricing).

## <a name="whats-included-in-storage"></a>O que está incluído no armazenamento

No armazenamento de dados estão incluídos seus próprios conjuntos de dados e relatórios do Excel e os itens que alguém compartilhou com você. Os conjuntos de dados são as fontes de dados que você carregou ou às quais se conectou. Essas fontes de dados incluem os arquivos do Power BI Desktop e as pastas de trabalho do Excel que você está usando. O exemplo a seguir também está incluído em sua capacidade de dados.

* Intervalos do Excel fixados em um dashboard.
* Visualizações locais do Reporting Services fixadas em um painel do Power BI.
* Imagens carregadas.

O tamanho de um dashboard que você compartilha varia dependendo do que é fixado a ele. Por exemplo, se você fixar itens de dois relatórios que façam parte de dois conjuntos de dados diferentes, o tamanho incluirá os dois conjuntos de dados.

## <a name="manage-items-you-own"></a>Gerenciar os itens que você tem

Veja a quantidade de armazenamento de dados que você está usando em sua conta do Power BI e gerencie sua conta.

1. Para gerenciar seu armazenamento, acesse **Meu Workspace** no painel de navegação.
   
    ![Captura de tela do painel de navegação com Meu Workspace em destaque.](media/service-admin-manage-your-data-storage-in-power-bi/pbi_myworkspace.png)

2. Selecione o ícone de engrenagem ![ícone de Engrenagem](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) no canto superior direito **Gerenciar armazenamento pessoal**.
   
    A barra superior mostra o limite de armazenamento que você usou.
   
    ![Captura de tela de Gerenciar limite de armazenamento mostrando quanto armazenamento foi usado.](media/service-admin-manage-your-data-storage-in-power-bi/pbi_persnlstorage.png)
   
    Os conjuntos de dados e os relatórios são separados em duas guias:
   
    **Pertencente a mim:** Você carregou esses relatórios e conjuntos de dados em sua conta do Power BI, incluindo os conjuntos de dados de serviço, como o Salesforce e o Dynamics CRM.  

    **Pertencente a outros:** Outras pessoas compartilharam esses relatórios e conjuntos de dados com você.
1. Para excluir um conjunto de dados ou um relatório, selecione o ícone de lixeira ![Ícone de lixeira](media/service-admin-manage-your-data-storage-in-power-bi/pbi_deleteicon.png).

Tenha em mente que você ou outra pessoa pode ter relatórios e painéis com base em um conjunto de dados. Se você excluir o conjunto de dados, os relatórios e painéis de controle não funcionarão mais.

## <a name="manage-your-workspace"></a>Gerenciar seu workspace
1. Selecione a seta ao lado de **Workspaces** e escolha o nome do workspace.
   
    ![Captura de tela da seleção de Workspace mostrando o workspace do Grupo de Vendas.](media/service-admin-manage-your-data-storage-in-power-bi/pbi_groupworkspaces.png)
2. Selecione o ícone de engrenagem ![ícone de Engrenagem](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) no canto superior direito **Gerenciar armazenamento de grupo**.
   
    A barra superior mostra o limite de armazenamento de grupo que você usou.
   
    ![Captura de tela de Gerenciar armazenamento mostrando quanto do limite de armazenamento do Grupo de Vendas foi usado.](media/service-admin-manage-your-data-storage-in-power-bi/pbi_groupstorage.png)
   
    Os conjuntos de dados e os relatórios são separados em duas guias:
   
    **Pertencente a nós:** Você ou outra pessoa carregou esses relatórios e conjuntos de dados para a conta do Power BI do grupo, incluindo os conjuntos de dados de serviço, como o Salesforce e o Dynamics CRM.

    **Pertencente a outros:** Outras pessoas compartilharam esses relatórios e conjuntos de dados com seu grupo.

3. Para excluir um conjunto de dados ou um relatório, selecione o ícone de lixeira ![Ícone de lixeira](media/service-admin-manage-your-data-storage-in-power-bi/pbi_deleteicon.png).
   
   > [!NOTE]
   > Tenha em mente que você ou outra pessoa do grupo pode ter relatórios e painéis com base em um conjunto de dados. Se você excluir o conjunto de dados, os relatórios e painéis de controle não funcionarão mais.
   
   Qualquer membro em um workspace com a função de administrador, membro ou colaborador tem permissões para excluir conjuntos de e relatórios do workspace.

## <a name="dataset-limits"></a>Limites de conjunto de dados
Há um limite de 1 GB por conjunto de dados que é importado para o Power BI. Se você optou por manter a experiência do Excel em vez de importar os dados, o limite será de 250 MB para o conjunto de dados.

## <a name="what-happens-when-you-reach-a-limit"></a>O que acontece quando você atinge um limite
Ao atingir o limite da capacidade de dados daquilo que você pode fazer, serão exibidos avisos dentro do serviço. 

Ao selecionar o ícone de engrenagem ![Ícone de engrenagem](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png), será exibida uma barra vermelha indicando que você está acima do limite da capacidade de dados.

![Captura de tela da capacidade de armazenamento mostrando que o limite foi atingido.](media/service-admin-manage-your-data-storage-in-power-bi/manage-storage-limit.png)

Esse limite também é indicado em **Gerenciar armazenamento pessoal**.

 ![Captura de tela da capacidade de armazenamento pessoal mostrando que o limite de Beatriz foi atingido.](media/service-admin-manage-your-data-storage-in-power-bi/manage-storage-limit2.png)

 Quando você tentar executar uma ação que atingirá um dos limites, será exibida uma mensagem informando que você está acima do limite. Você pode [gerenciar seu armazenamento](#manage-items-you-own) para reduzir a quantidade de armazenamento e ultrapassar o limite.

 ![Captura de tela da caixa de diálogo Acima do seu limite de armazenamento mostrando que os limites foram atingidos.](media/service-admin-manage-your-data-storage-in-power-bi/powerbi-pro-over-limit.png)

 ## <a name="next-steps"></a>Próximas etapas

 Mais perguntas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)
