---
title: Entender os níveis de privacidade do Power BI Desktop
description: Níveis de privacidade do Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: reference
ms.date: 09/09/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 19189529637fe5511ebd6f736c17b8a10a1d2ef9
ms.sourcegitcommit: 181679a50c9d7f7faebcca3a3fc55461f594d9e7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033774"
---
# <a name="power-bi-desktop-privacy-levels"></a>Níveis de privacidade do Power BI Desktop
No **Power BI Desktop**, os níveis de privacidade especificam um nível de isolamento que define o grau que uma fonte de dados será isolada de outras fontes de dados. Apesar de o nível de isolamento restrito bloquear a troca de informações entre as fontes de dados, ele poderá reduzir a funcionalidade e causar um impacto no desempenho.

A configuração **Níveis de Privacidade**, encontrada em **Arquivo > Opções e configurações > Opções** e, em seguida, em **Arquivo atual > Privacidade** determina se o Power BI Desktop usa suas configurações de Nível de Privacidade ao combinar dados. Essa caixa de diálogo inclui um link para a documentação do Power BI Desktop sobre Níveis de Privacidade (este artigo).

![Captura de tela da caixa de diálogo Opções.](media/desktop-privacy-levels/desktop_privacylevels1.png)

## <a name="configure-a-privacy-level"></a>Configurar um nível de privacidade
Com as configurações de nível de privacidade, você pode especificar um nível de isolamento que define o grau que uma fonte de dados deve ser isolada de outras fontes de dados.

| Configuração | Descrição | Exemplo de fontes de dados |
| --- | --- | --- |
| **Fonte de dados particular** |Uma fonte e dados **Particular** contém informações confidenciais e a visibilidade da fonte de dados pode ser restrita a usuários autorizados. Uma fonte de dados particular é completamente isolada de outras fontes de dados. |Os dados do Facebook, um arquivo de texto com prêmios de ações ou uma pasta de trabalho com informações de avaliação de funcionários. |
| **Fonte de dados Organizacional** |Uma fonte de dados **Organizacional** limita a visibilidade de uma fonte de dados para um grupo de pessoas confiáveis. Uma fonte de dados **Organizacional** é isolada de todas as fontes de dados **Públicas** , mas é visível para outras fontes de dados **Organizacionais** . |Um documento do **Microsoft Word** em um site do SharePoint com permissões habilitadas para um grupo de pessoas confiáveis. |
| **Fonte de dados pública** |Uma fonte de dados **Pública** fornece a todos visibilidade dos dados contidos na fonte de dados. Somente arquivos, fontes de dados da internet ou dados de pasta de trabalho podem ser marcados **Públicos**. |Os dados gratuitos do Microsoft Azure Marketplace, os dados de uma página do Wikipedia ou um arquivo local com os dados copiados de uma página da Web pública. |

## <a name="configure-privacy-level-settings"></a>Definir configurações de nível de privacidade
O diálogo de configurações de **Privacidade** para cada fonte de dados pode ser encontrado em **Arquivo > Opções e configurações > Configurações da fonte de dados**.

Para configurar um nível de privacidade da fonte de dados, selecione a fonte de dados e selecione **Editar**. O diálogo **Configurações de fonte de dados** é exibida e nele você pode selecionar o nível de privacidade adequado no menu suspenso na parte inferior da caixa de diálogo, como mostrado na imagem a seguir.

![Captura de tela da caixa de diálogo Configurações da Fonte de Dados.](media/desktop-privacy-levels/desktop_privacylevels2.png)

> [!CAUTION]
> Configure uma fonte de dados que contenha dados altamente confidenciais como **Privada**.
> 

## <a name="configure-privacy-levels"></a>Configurar Níveis de Privacidade
A configuração padrão dos **Níveis de Privacidade** é **Combine dados de acordo com sua configuração de Nível de Privacidade para cada fonte** por padrão, o que significa que os **Níveis de Privacidade** são impostos.

| Configuração | Descrição |
| --- | --- |
| **Combinar os dados de acordo com as definições de Nível de privacidade de cada origem** (ativada e a configuração padrão) |As configurações de nível de privacidade são usadas para determinar o nível de isolamento entre fontes de dados ao combinar dados. |
| **Ignorar os níveis de Privacidade e melhorar potencialmente o desempenho** (desativada) |No entanto, os níveis de privacidade não são considerados ao combinar dados; podem aumentar o desempenho e a funcionalidade dos dados. |

> **Observação de segurança:** Selecionar **Ignore os Níveis de Privacidade e melhore potencialmente o desempenho** na caixa de diálogo **Níveis de Privacidade** pode expor dados confidenciais para uma pessoa não autorizada. Não *desative* essa configuração, a menos que você tenha certeza de que a fonte de dados não contém dados confidenciais.
> 
> 

> [!CAUTION]
> O **Ignore os Níveis de Privacidade e melhore potencialmente o desempenho** não funciona no serviço do Power BI. Dessa forma, os relatórios do Power BI Desktop com essa configuração habilitada que, em seguida, são publicados no serviço do Power BI, *não* refletem esse comportamento quando usado no serviço.
> 

**Configurar Níveis de Privacidade**

No Power BI Desktop ou no Editor de Consultas, selecione **Arquivo > Opções e configurações > Opções** e **Arquivo atual > Privacidade**.

a. Quando **Combinar dados de acordo com as configurações de Nível de privacidade para cada fonte** estiver selecionado, os dados serão combinados de acordo com a sua configuração dos Níveis de privacidade. Mesclar dados entre zonas de isolamento de Privacidade resultará em buffer de dados.

b. Quando **Ignorar os Níveis de privacidade e potencialmente melhorar o desempenho** estiver selecionado, os dados serão combinados, ignorando os Níveis de Privacidade que poderiam revelar dados confidenciais para um usuário não autorizado. A configuração pode melhorar o desempenho e a funcionalidade

> **Observação de segurança:** selecionar **Ignore os Níveis de Privacidade e melhore potencialmente o desempenho** pode melhorar o desempenho; no entanto, o Power BI Desktop não pode garantir a privacidade dos dados mesclados para o arquivo do Power BI Desktop.
> 
> 

