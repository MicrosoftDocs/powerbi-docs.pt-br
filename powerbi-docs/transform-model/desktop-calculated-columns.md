---
title: Usando colunas calculadas no Power BI Desktop
description: Colunas calculadas no Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 05/07/2019
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: 0d8510e1ef76ba07623e135f51eb0ce21ceac4c4
ms.sourcegitcommit: c83146ad008ce13bf3289de9b76c507be2c330aa
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2020
ms.locfileid: "86214401"
---
# <a name="create-calculated-columns-in-power-bi-desktop"></a>Criar colunas calculadas no Power BI Desktop
Com as colunas calculadas, você pode adicionar novos dados a uma tabela já presente em seu modelo. Mas em vez de consultar e carregar valores na sua nova coluna por meio de uma fonte de dados, você cria uma fórmula DAX (Data Analysis Expressions) que define os valores da coluna. No Power BI Desktop, colunas calculadas são criadas usando o recurso nova coluna na exibição **Relatório**.

Ao contrário das colunas personalizadas criadas como parte de uma consulta por meio de **Adicionar Coluna Personalizada** no Editor de Consultas, as colunas calculadas criadas na exibição de **Relatório** ou de **Dados** são baseadas em dados que você já carregou no modelo. Por exemplo, você poderá concatenar os valores de duas colunas diferentes em duas tabelas diferentes, mas relacionadas, realizar adição ou extrair subcadeias de caracteres.

As colunas calculadas criadas são exibidas na lista **Campos** assim como qualquer outro campo, mas elas terão um ícone especial que mostrará que os valores são resultado de uma fórmula. Você pode nomear suas colunas como desejar e adicioná-las a uma visualização de relatório, assim como com outros campos.

![Captura de tela do Power BI Desktop mostrando colunas calculadas na exibição Campos.](media/desktop-calculated-columns/calccolinpbid_fields.png)
 
Colunas calculadas calculam os resultados usando a DAX, uma linguagem de fórmula destinada a trabalhar com os dados relacionais, como no Power BI Desktop. O DAX inclui uma biblioteca de mais de 200 funções, operadores e constructos. Ela fornece uma enorme flexibilidade na criação de fórmulas para calcular os resultados de praticamente qualquer análise de dados exigida. Para saber mais sobre o DAX, consulte [Noções básicas do DAX no Power BI Desktop](desktop-quickstart-learn-dax-basics.md).

As fórmulas DAX são semelhantes às fórmulas do Excel. Na verdade, o DAX tem muitas das mesmas funções usadas no Excel. Funções DAX, no entanto, devem trabalhar com dados fracionados interativamente ou filtrados em um relatório, como no Power BI Desktop. No Excel, você pode ter uma fórmula diferente para cada linha em uma tabela. No Power BI, quando você criar uma fórmula DAX para uma nova coluna, ela calculará um resultado para cada linha na tabela. Valores de coluna são recalculados conforme necessário, como quando os dados subjacentes são atualizados e os valores mudaram.

## <a name="lets-look-at-an-example"></a>Vamos examinar um exemplo
Jeff é gerente de entregas na Contoso e quer criar um relatório que mostre o número de remessas para diferentes cidades. Jeff tem uma tabela **Geography** com campos separados para cidade e estado. No entanto, ele quer que os relatórios mostrem os valores de cidade e estado como um valor na mesma linha. No momento, a tabela **Geography** de Matheus não tem o campo desejado.

![Captura de tela do Power BI Desktop mostrando o filtro Geography na exibição Campos.](media/desktop-calculated-columns/calccolinpbid_cityandstatefields.png)

Porém, com uma coluna calculada, Jeff pode juntar as cidades na coluna **City** com os estados da coluna **State**.

Jeff clica com o botão direito do mouse na tabela **Geography** e, em seguida, seleciona **Nova Coluna**. Em seguida, ele insere a fórmula DAX a seguir na barra de fórmulas:

![Captura de tela do Power BI Desktop mostrando a entrada da fórmula DAX.](media/desktop-calculated-columns/calccolinpbid_formula.png)

Essa fórmula simplesmente cria uma coluna chamada **CityState**. Para cada linha na tabela **Geography**, ela usa os valores da coluna **City**, adiciona uma vírgula e um espaço e, em seguida, concatena os valores da coluna **State**.

Agora Jeff tem o campo desejado.

![Captura de tela do Power BI Desktop mostrando a opção CityState marcada no filtro Geography da exibição Campos.](media/desktop-calculated-columns/calccolinpbid_citystatefield.png)

Ele poderá adicionar esse campo à tela de relatório juntamente com o número de remessas. Com o mínimo de esforço, agora Jeff tem um campo **CityState**, que pode ser adicionado a qualquer tipo de visualização. Quando Jeff cria um mapa, o Power BI Desktop já sabe como ler os valores de cidade e estado na nova coluna.

![Captura de tela do Power BI Desktop mostrando dados representados em um visual de Mapa.](media/desktop-calculated-columns/calccolinpbid_citystatemap.png)

## <a name="next-steps"></a>Próximas etapas
Fornecemos aqui apenas uma rápida introdução às colunas calculadas. Confira mais informações nos recursos a seguir:

* Para baixar um arquivo de exemplo e obter lições passo a passo sobre como criar mais colunas, confira [Tutorial: Criar colunas calculadas no Power BI Desktop](desktop-tutorial-create-calculated-columns.md)

* Para saber mais sobre o DAX, consulte [Noções básicas do DAX no Power BI Desktop](desktop-quickstart-learn-dax-basics.md).

* Para saber mais sobre as colunas que você cria como parte de uma consulta, confira a seção **Criar colunas personalizadas** em [Tarefas comuns de consulta no Power BI Desktop.](desktop-common-query-tasks.md)  

