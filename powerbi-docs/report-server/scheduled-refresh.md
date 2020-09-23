---
title: Atualização agendada de relatório do Power BI no Servidor de Relatórios do Power BI
description: Os relatórios do Power BI podem conectar-se a fontes de dados diferentes. Dependendo de como os dados são usados, fontes de dados diferentes estão disponíveis.
author: maggiesMSFT
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 01/09/2020
ms.author: maggies
ms.openlocfilehash: 89adff51d70be24e4f42c379a729fd1123ca10a5
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90861764"
---
# <a name="power-bi-report-scheduled-refresh-in-power-bi-report-server"></a>Atualização agendada de relatório do Power BI no Servidor de Relatórios do Power BI
A atualização agendada dos relatórios do Power BI permite que os dados de um relatório permaneçam atualizados.

![Atualização agendada no Servidor de Relatórios do Power BI](media/scheduled-refresh/scheduled-refresh-success.png)

A atualização agendada é específica aos relatórios do Power BI com um modelo inserido. Isso significa que você importa dados para o relatório em vez de usar uma conexão dinâmica ou o DirectQuery. Ao importar os dados, eles são desconectados da fonte de dados original e precisam ser atualizados para permanecerem em sua versão mais recente. A atualização agendada é uma forma de manter os dados atualizados.

A atualização agendada é configurada na seção de gerenciamento de um relatório. Para obter mais informações sobre como configurar a atualização agendada, consulte [Como configurar a atualização agendada de relatório do Power BI](configure-scheduled-refresh.md).

## <a name="how-this-works"></a>Como isso funciona
Vários componentes são envolvidos ao usar a atualização agendada dos relatórios do Power BI.

* O SQL Server Agent atua como um timer para a geração dos eventos agendados.
* Os trabalhos agendados são adicionados a uma fila de eventos e de notificações no banco de dados do servidor de relatório. Em uma implantação escalável, a fila é compartilhada entre todos os servidores de relatórios na implantação.
* Todo o processamento de relatório que ocorre como resultado de um evento de agendamento é executado como um processo em segundo plano.
* O modelo de dados é carregado em uma instância do Analysis Services.
* Para algumas fontes de dados, o mecanismo de mashup do Power Query é usado para os processos de conexão a fontes de dados e de transformação dos dados. Outras fontes de dados podem ser conectadas diretamente de um serviço do Analysis Services usado para hospedar os modelos de dados do Servidor de Relatórios do Power BI.
* Os novos dados são carregados no modelo de dados do Analysis Services.
* Em uma configuração de expansão, o modelo de dados pode ser replicado entre os nós.
* O Analysis Services processa os dados e executa os cálculos necessários.

O Servidor de Relatórios do Power BI mantém uma fila de eventos para todas as operações agendadas. Ele pesquisa a fila em intervalos regulares para verificar novos eventos. Por padrão, a fila é verificada em intervalos de 10 segundos. Você pode alterar o intervalo modificando as definições de configuração de **PollingInterval**, de **IsNotificationService** e de **IsEventService** no arquivo RSReportServer.config. **IsDataModelRefreshService** também pode ser usado para definir se um processo do servidor de relatório agendou eventos.

### <a name="analysis-services"></a>Analysis Services
A renderização de um relatório do Power BI, bem como a execução de uma atualização agendada, exige o carregamento do modelo de dados do relatório do Power BI no Analysis Services. Um processo do Analysis Services será executado com o Servidor de Relatórios do Power BI.

## <a name="considerations-and-limitations"></a>Considerações e limitações
### <a name="when-scheduled-refresh-cant-be-used"></a>Quando não é possível usar a atualização agendada
Nem todos os relatórios do Power BI permitem a criação de um plano de atualização agendada. Veja a seguir uma lista dos relatórios do Power BI que não permitem a criação de um plano de atualização agendada.

* O relatório contém uma ou mais fontes de dados do Analysis Services que usam uma conexão dinâmica.
* O relatório contém uma ou mais fontes de dados que usam o DirectQuery.
* O relatório não contém nenhuma fonte de dados. Por exemplo, os dados são inseridos manualmente por meio da opção *Inserir Dados* ou um relatório contém apenas conteúdo estático, como imagens, texto, etc.

Além da lista acima, há cenários específicos com fontes de dados no modo *Importar* para os quais não é possível criar planos de atualização.

* Se uma fonte de dados de *Arquivo* ou de *Pasta* for usada e o caminho do arquivo for um caminho local (por exemplo, C:\Users\user\Documents), não será possível criar um plano de atualização. O caminho deverá ser um caminho ao qual o servidor de relatório possa se conectar, como um compartilhamento de rede. Por exemplo, *\\myshare\Documents*.
* Se for possível conectar a fonte de dados usando apenas o OAuth (por exemplo, Facebook, Google Analytics, Salesforce, etc.), o plano de atualização de cache não poderá ser criado. No momento, o Servidor de Relatórios não é compatível com a autenticação OAuth para nenhum tipo de fonte de dados, independentemente dos relatórios serem paginados, móveis ou do Power BI.

### <a name="memory-limits"></a>Limites de memória
A carga de trabalho tradicional de um servidor de relatório é semelhante à de um aplicativo Web. A capacidade de carregamento de relatórios usando dados importados ou o DirectQuery, bem como a capacidade de execução da atualização agendada, depende de uma instância do Analysis Services ser hospedada juntamente com o servidor de relatório. Como resultado, isso pode provocar uma demanda de memória inesperada no servidor. Planeje a implantação do servidor adequadamente sabendo que o Analysis Services pode consumir memória juntamente com o servidor de relatório.

Para obter informações sobre como monitorar uma instância do Analysis Services, consulte [Monitorar uma instância do Analysis Services](/sql/analysis-services/instances/monitor-an-analysis-services-instance).

Para obter informações sobre as configurações de memória no Analysis Services, consulte [Propriedades de memória](/sql/analysis-services/server-properties/memory-properties).

### <a name="data-model-size-limit"></a>Limite de tamanho do modelo de dados
O modelo de dados carregado no mecanismo interno do Analysis Services durante uma atualização agendada tem um tamanho máximo de 2.000 MB (2 GB). Esse tamanho máximo não pode ser configurado. Se o modelo de dados exceder 2 GB, você receberá o erro de atualização "O tamanho do resultado excede o limite de tamanho (2 GB) do tipo de destino grande". Nesse caso, recomendamos hospedar o modelo em uma instância do Analysis Services e usar uma conexão dinâmica com o modelo no relatório.

## <a name="next-steps"></a>Próximas etapas
Configurar a [atualização agendada](configure-scheduled-refresh.md) em um relatório do Power BI.

Mais perguntas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)