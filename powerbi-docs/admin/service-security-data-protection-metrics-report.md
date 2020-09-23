---
title: Relatório de métricas de proteção de dados
description: Saiba mais sobre o relatório de métricas de proteção de dados
author: paulinbar
manager: rkarlin
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 08/16/2020
ms.author: painbar
LocalizationGroup: Data from files
ms.openlocfilehash: ea4aa1772712fbfff67ab749a379638ba698f554
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90854496"
---
# <a name="data-protection-metrics-report"></a>Relatório de métricas de proteção de dados

## <a name="what-is-the-data-protection-metrics-report"></a>O que é o relatório de métricas de proteção de dados?
O relatório de métricas de proteção de dados é um relatório dedicado que os [administradores do Power BI](./service-admin-role.md) podem usar para monitorar e acompanhar o uso e a adoção de rótulos de confidencialidade em seus locatários.

![Relatório de métricas de proteção de dados](./media/service-security-data-protection-metrics-report/protection-metrics-seven-days-1.png)
 
Os recursos do relatório:
* Um gráfico 100% de colunas empilhadas que mostra o uso do rótulo de sensibilidade diária no locatário para os últimos 7, 30 ou 90 dias. Esse gráfico facilita o acompanhamento do uso com relação aos diferentes tipos de rótulo ao longo do tempo.
* Gráficos de rosca que mostram o estado atual do uso do rótulo de sensibilidade no locatário para dashboards, relatórios, conjuntos de tabelas e fluxos de dados.
* Um link para o portal do Cloud App Security em que alertas do Power BI, usuários em risco, logs de atividades e outras informações estão disponíveis. Para obter mais informações, confira [Como usar controles do Microsoft Cloud App Security no Power BI](./service-security-using-microsoft-cloud-app-security-controls.md).

O relatório é atualizado a cada 24 horas.

## <a name="viewing-the-data-protection-metrics-report"></a>Como visualizar o relatório de métricas de proteção de dados

Você deve ter uma [função de Administrador do Power BI](./service-admin-role.md) para abrir e exibir o relatório.
Para exibir o relatório, acesse **Configurações > Portal de administração** e escolha **Métricas de proteção**.

![portal de administração de métricas de proteção](./media/service-security-data-protection-metrics-report/protection-metrics-admin-portal.png)
 
 
Na primeira vez que você abrir o relatório de métricas de proteção de dados, o carregamento poderá levar alguns segundos. Um relatório e um conjunto de dados chamados de **Métricas de proteção de dados (geradas automaticamente)** serão criados em seu ambiente privado, em "Meu workspace". Não recomendamos exibi-lo aqui. Esse não é o relatório completo. Em vez disso, exiba o relatório no portal de administração, conforme descrito acima.

> [!CAUTION]
> Não altere o relatório nem o conjunto de dados de nenhuma maneira, já que novas versões do relatório são distribuídas periodicamente, e qualquer alteração feita ao relatório original é substituída quando você atualiza para a nova versão.

## <a name="report-updates"></a>Atualizações de relatório

Versões aprimoradas do relatório de métricas de proteção de dados são liberadas periodicamente. Quando você abrir o relatório, se uma nova versão estiver disponível, será consultado se deseja abrir a nova versão. Se você responder "Sim", a nova versão do relatório será carregada e substituirá a versão anterior. As alterações que você tiver ao relatório e/ou conjunto de dados antigo serão perdidas. Você poderá optar por não abrir a nova versão, mas nesse caso, não se beneficiará dos aprimoramentos nela incluídos. 
## <a name="notes-and-considerations"></a>Observações e considerações
* Para que o relatório de métricas de proteção de dados seja gerado com êxito, a [proteção de informações](./service-security-enable-data-sensitivity-labels.md) deve estar habilitada em seu locatário e [rótulos de sensibilidade devem ter sido aplicados](./service-security-apply-data-sensitivity-labels.md). 
* Para acessar informações do Cloud App Security, sua organização deve ter a [licença do Cloud App Security](./service-security-using-microsoft-cloud-app-security-controls.md#cloud-app-security-licensing) apropriada.
* Se você decidir compartilhar informações do relatório de métricas de proteção de dados com um usuário que não seja um Administrador do Power BI, lembre-se de que esse relatório contém informações confidenciais sobre sua organização.
* O relatório de métricas de proteção de dados é um tipo especial de relatório e não aparece em listas do tipo "Compartilhados comigo", "Recentes" e "Favoritos".
* O relatório de métricas de proteção de dados não está disponível para [usuários externos (usuários convidados do Azure Active Directory B2B)](./service-admin-azure-ad-b2b.md).
## <a name="next-steps"></a>Próximas etapas
* [Rótulos de confidencialidade no Power BI](./service-security-sensitivity-label-overview.md)
* [Como usar controles do Microsoft Cloud App Security no Power BI](service-security-using-microsoft-cloud-app-security-controls.md)
* [Noções básicas sobre a função de Administrador de serviços do Power BI](service-admin-role.md)
* [Habilitar rótulos de confidencialidade no Power BI](service-security-enable-data-sensitivity-labels.md)