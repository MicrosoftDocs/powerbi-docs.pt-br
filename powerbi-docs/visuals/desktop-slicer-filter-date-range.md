---
title: Usar uma segmentação ou um filtro de data relativa no Power BI
description: Saiba como usar uma segmentação ou um filtro para restringir intervalos de datas relativas no Power BI.
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 09/09/2020
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: 26e638e106f7bd11544d1d80dae543f06783bda7
ms.sourcegitcommit: 92b033ee7a6e36808371b247b7b41536cee6c2f6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "90008786"
---
# <a name="creating-a-relative-date-slicer-and-filter-in-power-bi"></a>Como criar uma segmentação e um filtro de data relativa no Power BI

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

Com a **segmentação de datas relativas** ou o **filtro de datas relativas**, aplique filtros baseados em tempo a qualquer coluna de data do modelo de dados. Por exemplo, você pode usar a **segmentação de datas relativas** para mostrar apenas os dados de vendas ocorridos nos últimos 30 dias (ou mês, meses do calendário e assim por diante). Quando você atualizar os dados, o período relativo aplicará automaticamente a restrição de datas relativas apropriada.

![Captura de tela de um relatório com uma seta apontando para uma segmentação de data relativa.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-01.png)

Compartilhar seu relatório com um colega do Power BI exige que você tenha licenças de Power BI Pro individuais ou que o relatório seja salvo na capacidade Premium.

## <a name="create-the-relative-date-range-slicer"></a>Criar a segmentação de intervalo de data relativa

Use a segmentação de datas relativas como qualquer outra segmentação. Crie um visual de **segmentação** para o relatório e, em seguida, selecione um valor de data no valor **Campo**. Na imagem a seguir, selecionamos o campo *OrderDate*.

![Captura de tela do painel de visualizações com setas apontando para o ícone do visual de segmentação e a área Campo.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-02.png)

Selecione a segmentação em sua tela e, em seguida, o acento circunflexo no canto superior direito do visual da segmentação. Se o visual tiver dados de data, o menu exibirá a opção para **Relativo**.

![Captura de tela do visual da segmentação com um destaque em torno do acento circunflexo e uma seta apontando para Relativo.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-03.png)

Na segmentação de datas relativas, selecione *Relativo*.

Em seguida, selecione as configurações.

Na primeira configuração da *segmentação de datas relativas*, você tem as seguintes opções:

![Captura de tela das opções de configuração relativa com a primeira configuração destacada.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-04.png)

* Último
* Próximo
* Esse

A segunda configuração (no meio) da *segmentação de datas relativas* permite inserir um número para definir o intervalo de datas relativas.

![Captura de tela das opções de configuração relativa com a segunda configuração destacada.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-04a.png)

A terceira configuração permite escolher a medida de data. Você tem as seguintes opções:

![Captura de tela das opções de configuração relativa com a terceira configuração destacada.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-05.png)

* Days (dias)
* Weeks
* Semanas (calendário)
* Months
* Meses (calendário)
* Years
* Anos (Calendário)

Se você selecionar **Meses** nessa lista e inserir *2* na configuração do meio, veja o que acontecerá:

* se hoje for 20 de julho:

    - os dados incluídos nos visuais restringidos pela segmentação mostrarão os dados dos dois meses anteriores,
    - começando em 21 de maio até 20 de julho (a data de hoje).

Em comparação, se você selecionou *Meses (calendário)* , os visuais restringidos mostrarão dados de 1º de maio a 30 de junho (os dois últimos meses do calendário completos).

## <a name="create-the-relative-date-range-filter"></a>Criar o filtro de intervalo de data relativa

Você também pode criar um filtro de intervalo de datas relativas para a página de relatório ou para o relatório inteiro. Para fazer isso, arraste um campo de data para as áreas **Filtros no nível de página** ou **Filtros no nível de relatório** do painel **Campo**:

![Captura de tela do campo OrderDate, que está sendo arrastado para a área dos filtros de nível de página.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-06.png)

Uma vez lá, você pode alterar o intervalo de datas relativas. Isso é semelhante a como você pode personalizar a **segmentação de datas relativas**. Selecione **Filtragem de datas relativas** na lista suspensa **Tipo de Filtro**.

![Captura de tela mostrando a lista suspensa Tipo de Filtro e o ponteiro do mouse sobre a filtragem de Data Relativa.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-07.png)

Depois que selecionar **Filtragem de datas relativas**, você verá três seções a serem modificadas, incluindo uma caixa numérica intermediária, como a segmentação.

![Captura de tela dos filtros de nível de relatório com setas apontando para a opção Mostrar itens quando o valor.](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-08.png)

## <a name="limitations-and-considerations"></a>Limitações e considerações

No momento, as limitações e considerações a seguir aplicam-se ao filtro e à **segmentação de intervalo de datas relativas**.

* O tipo de dados do campo na segmentação precisa ser uma data e não o padrão de texto. Caso contrário, as opções relativas não são exibidas na segmentação.
* Os modelos de dados do **Power BI** não incluem informações de fuso horário. Os modelos podem armazenar horários, mas não há nenhuma indicação do fuso horário em que estão localizados.
* A segmentação e o filtro sempre se baseiam no horário em UTC. Se você definir um filtro em um relatório e enviá-lo para um colega em um fuso horário diferente, ambos verão os mesmos dados. A menos que você esteja no fuso horário UTC, você e seu colega precisarão considerar a diferença de horário.
* É possível converter dado capturados em um fuso horário local em UTC usando o **Editor de Consultas**.

## <a name="next-steps"></a>Próximas etapas

- [Usar uma segmentação e um filtro de tempo relativo no Power BI](../create-reports/slicer-filter-relative-time.md)
- [Segmentações no Power BI](power-bi-visualization-slicers.md)
