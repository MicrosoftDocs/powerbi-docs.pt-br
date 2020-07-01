---
title: Criar e gerenciar relações no Power BI Desktop
description: Criar e gerenciar relações no Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 05/28/2020
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: f241315eecdbb600a798630167913aa1be0079a3
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85239045"
---
# <a name="create-and-manage-relationships-in-power-bi-desktop"></a>Criar e gerenciar relações no Power BI Desktop
Quando você importa várias tabelas, é provável que você realize algumas análises usando dados de todas essas tabelas. Relações entre essas tabelas são necessárias para calcular os resultados com precisão e exibir as informações corretas em seus relatórios. O Power BI Desktop torna fácil a criação dessas relações. Na verdade, na maioria dos casos, você não precisará fazer nada, o recurso de detecção automática fará tudo por você. No entanto, às vezes você pode precisar criar relações por conta própria ou fazer alterações a uma relação. De qualquer modo, é importante compreender as relações no Power BI Desktop e compreender como criá-las e editá-las.

## <a name="autodetect-during-load"></a>Detectar automaticamente durante o carregamento
Se você consultar duas ou mais tabelas ao mesmo tempo, quando os dados forem carregados, o Power BI Desktop tentará localizar e criar relações para você. As opções de relação **Cardinalidade**, **Direção de filtro cruzado** e **Tornar essa relação ativa** são definidas automaticamente. O Power BI Desktop procura nomes de colunas nas tabelas que você está consultando para determinar se há alguma relação em potencial. Se houver, essas relações serão criadas automaticamente. Caso o Power BI Desktop não possa determinar com um alto nível de confiança que há uma correspondência, ele não criará a relação. Porém, você ainda pode usar a caixa de diálogo **Gerenciar relações** para criar ou editar relações manualmente.

## <a name="create-a-relationship-with-autodetect"></a>Criar um relacionamento com detecção automática
Na guia **Página Inicial**, selecione **Gerenciar Relações** \> **Detectar Automaticamente**.

![Criar um relacionamento com detecção automática](media/desktop-create-and-manage-relationships/automaticrelationship.gif)

## <a name="create-a-relationship-manually"></a>Criar uma relação manualmente
1. Na guia **Página Inicial**, selecione **Gerenciar Relações** \> **Nova**.

2. Na caixa de diálogo **Criar relação**, na primeira lista suspensa da tabela, selecione uma tabela. Selecione a coluna que você deseja usar na relação.

3. Na segunda lista suspensa tabela, selecione a outra tabela que você deseja ter na relação. Selecione a outra coluna que você deseja usar e, em seguida, escolha **OK**.

   ![Criar uma relação manual](media/desktop-create-and-manage-relationships/manualrelationship2.gif)

Por padrão, o Power BI Desktop configura automaticamente as opções **Cardinalidade** (direção), **Direção de filtro cruzado** e **Tornar essa relação ativa** para sua nova relação. No entanto, você poderá alterar essas configurações se necessário. Para obter mais informações, confira [Noções básicas sobre opções adicionais](#understanding-additional-options).

Se nenhuma das tabelas selecionadas para a relação tiver valores exclusivos, você verá o seguinte erro: *Uma das colunas deve ter valores exclusivos*. Pelo menos uma tabela em uma relação *precisa* ter uma lista distinta e exclusiva de valores de chave, que é um requisito comum para todas as tecnologias de banco de dados relacional. 

Se você encontrar esse erro, haverá duas maneiras de corrigir o problema:

* Use **Remover Duplicatas** para criar uma coluna com valores exclusivos. A desvantagem dessa abordagem é que você poderá perder informações quando as linhas duplicadas forem removidas. Muitas vezes, uma chave (linha) é duplicada por um bom motivo.
* Adicione uma tabela intermediária composta pela lista de valores de chave distintos no modelo, que, em seguida, será vinculado às duas colunas originais na relação.

Para saber mais, consulte esta [postagem em blog](https://blogs.technet.microsoft.com/cansql/2016/12/19/relationships-in-power-bi-fixing-one-of-the-columns-must-have-unique-values-error-message/).


## <a name="edit-a-relationship"></a>Editar uma relação
1. Na guia **Página Inicial**, selecione **Gerenciar Relações**.

2. Na caixa de diálogo **Gerenciar relações**, selecione a relação e selecione **Editar**.

## <a name="configure-additional-options"></a>Configurar opções adicionais
Quando você cria ou edita uma relação, pode configurar opções adicionais. Por padrão, o Power BI Desktop configura automaticamente as opções adicionais com base em uma melhor estimativa, que pode ser diferente para cada relacionamento com base nos dados das colunas.

### <a name="cardinality"></a>Cardinalidade
A opção **Cardinalidade** pode ter uma das seguintes configurações:

**Muitos para um (\*:1)** : uma relação de muitos para um é o tipo padrão mais comum de relação. Isso significa que a coluna em determinada tabela pode ter mais de uma instância de um valor, enquanto a outra tabela relacionada, geralmente conhecida como a tabela de pesquisa, tem apenas uma instância de cada valor.

**Um para um (1:1)** : Em uma relação de um para um, a coluna em uma tabela tem apenas uma instância de um determinado valor e que o mesmo é válido para a outra tabela relacionada.

**Um para muitos (1:*)** : Em uma relação de um para muitos a coluna em uma tabela tem apenas uma instância de um determinado valor, enquanto a outra tabela relacionada pode ter mais de uma instância de um valor.

**Muitos para muitos (\*:\*)** : com os modelos de composição, você pode estabelecer uma relação de muitos para muitos entre tabelas, o que remove os requisitos para valores exclusivos em tabelas. Ela também remove as soluções alternativas anteriores, como introduzir novas tabelas somente para estabelecer relações. Para obter mais informações, confira [Relações com uma cardinalidade muitos para muitos](https://docs.microsoft.com/power-bi/desktop-many-to-many-relationships). 

Para obter mais informações sobre quando alterar a cardinalidade, confira [Noções básicas sobre opções adicionais](#understanding-additional-options).

### <a name="cross-filter-direction"></a>Direção do filtro cruzado
A opção **Direção do filtro cruzado** pode ter uma das seguintes configurações:

**Ambas**: para fins de filtragem, ambas as tabelas são tratadas como se fossem uma tabela. A configuração **Ambas** é ideal para uma tabela que tem uma série de tabelas de pesquisa em torno dela. Um exemplo é uma tabela de dados reais de vendas com uma tabela de pesquisa por departamento. Essa configuração costuma ser chamada de configuração de esquema em estrela (uma tabela central com várias Tabelas de pesquisa). No entanto, se você tiver duas ou mais tabelas que também têm tabelas de pesquisa (com algumas em comum), não será vantajoso usar a configuração **Ambas**. Para continuar o exemplo anterior, nesse caso, você também tem uma tabela de vendas de orçamento que registra o orçamento de destino para cada departamento. E a tabela de departamento é conectada tanto à tabela de vendas quanto à de alocação. Evite a configuração **Ambas** para esse tipo de configuração.

**Único**: a descrição padrão mais comum, o que significa que as opções de filtragem em tabelas conectadas funcionam na tabela na qual os valores estão sendo agregados. Se você importar uma tabela do Power Pivot no Excel 2013 ou um modelo de dados anterior, todas as relações terão uma única direção. 

Para obter mais informações sobre quando alterar a direção do filtro cruzado, confira [Noções básicas sobre opções adicionais](#understanding-additional-options).

### <a name="make-this-relationship-active"></a>Ativar esta relação
Quando marcada, a relação serve como a relação ativa padrão. Em casos nos quais há mais de uma relação entre duas tabelas, a relação ativa fornece uma maneira para o Power BI Desktop criar automaticamente visualizações que incluem ambas as tabelas.

Para obter mais informações sobre quando criar uma relação específica ativa, confira [Noções básicas sobre opções adicionais](#understanding-additional-options).

## <a name="understanding-relationships"></a>Noções básicas sobre relações
Depois que você tiver conectado duas tabelas unindo-as com uma relação, poderá trabalhar com os dados em ambas as tabelas como se fossem uma, não precisando mais se preocupar com detalhes da relação nem mesclar essas tabelas em uma tabela antes de importá-las. Em muitas situações, o Power BI Desktop pode criar relações automaticamente para você. No entanto, se o Power BI Desktop não puder determinar com alto grau de certeza que deve existir uma relação entre duas tabelas, ele não criará automaticamente a relação. Nesse caso, você deve fazer isso. 

Vamos conferir um pequeno tutorial, para mostrar melhor como funcionam as relações no Power BI Desktop.

>[!TIP]
>Você pode concluir esta lição por conta própria: 
>
> 1. Copie a tabela **ProjectHours** a seguir em uma planilha do Excel (excluindo o título), selecione todas as células e, em seguida, selecione **Inserir** \> **Tabela**. 
> 2. Na caixa de diálogo **Criar Tabela**, selecione **OK**. 
> 3. Selecione qualquer célula da tabela, selecione **Design de Tabela** \> **Nome da Tabela** e, em seguida, insira *ProjectHours*. 
> 4. Faça o mesmo para a tabela **CompanyProject**. 
> 5. Importe os dados por meio de **Obter Dados** no Power BI Desktop. Selecione as duas tabelas como uma fonte de dados e, em seguida, selecione **Carregar**.

A primeira tabela, **ProjectHours**, é um registro de tíquetes de trabalho que gravam o número de horas que uma pessoa já trabalhou em um projeto específico. 

**ProjectHours**

| **Ticket** | **SubmittedBy** | **Hours** | **Project** | **DateSubmit** |
| ---:|:--- | ---:|:--- | ---:|
| 1001 |Alan Brewer |22 |Azul |1/1/2013 |
| 1002 |Alan Brewer |26 |Vermelho |2/1/2013 |
| 1003 |Shu Ito |34 |Amarelo |1242012 |
| 1004 |Alan Brewer |13 |Laranja |1/2/2012 |
| 1005 |Eli Bowen |29 |Roxo |01/10/2013 |
| 1006 |Nuno Bento |35 |Verde |2/1/2013 |
| 1007 |David Hamilton |10 |Amarelo |01/10/2013 |
| 1008 |Mu Han |28 |Laranja |1/2/2012 |
| 1009 |Shu Ito |22 |Roxo |2/1/2013 |
| 1010 |Eli Bowen |28 |Verde |1012013 |
| 1011 |Eli Bowen |9 |Azul |10/15/2013 |

Essa segunda tabela, **CompanyProject**, é uma lista de projetos aos quais é atribuída uma prioridade: A, B ou C. 

**CompanyProject**

| **ProjName** | **Priority** |
| --- | --- |
| Azul |A |
| Vermelho |B |
| Verde |C |
| Amarelo |C |
| Roxo |B |
| Laranja |C |

Observe que cada tabela tem uma coluna de projeto. Cada uma é nomeada de modo ligeiramente diferente, mas os valores parecem ser os mesmos. Isso é importante, e retornaremos a esse assunto em breve.

Agora que temos nossas duas tabelas importadas para um modelo, vamos criar um relatório. A primeira coisa que queremos ter é o número de horas enviadas por prioridade do projeto, então vamos selecionar **Prioridade** e **Horas** no painel **Campos**.

![Selecionar Prioridade e Horas no painel Campos](media/desktop-create-and-manage-relationships/candmrel_reportfiltersnorel.png)

Se observarmos nossa tabela na tela Relatório, veremos que o número de horas é 256 para cada projeto, que é também o total. Claramente, esse número não está correto. Por que? É porque não podemos calcular uma soma total dos valores de uma tabela (**Hours** na tabela **Project**), dividida por valores em outra tabela (**Priority** na tabela **CompanyProject**) sem que exista uma relação entre essas duas tabelas.

Portanto, vamos criar uma relação entre essas duas tabelas.

Lembre-se das colunas que vimos em ambas as tabelas com um nome de projeto, mas com valores parecidos? Vamos usar essas duas colunas para criar uma relação entre nossas tabelas.

Por que essas colunas? Bem, se observarmos a coluna **Projeto** na tabela **ProjectHours**, veremos valores como Azul, Vermelho, Amarelo, Laranja e assim por diante. Na verdade, podemos ver várias linhas que têm o mesmo valor. Assim, temos muitos valores de cor para **Project**.

Se observarmos a coluna **ProjName** na tabela **CompanyProject**, veremos que há somente um de cada um dos valores de cor para o nome do projeto. Cada valor de cor nesta tabela é exclusivo e isso é importante, porque podemos criar uma relação entre essas duas tabelas. Nesse caso, uma relação de tipo muitos para um. Em uma relação muitos para um, pelo menos uma coluna em uma das tabelas deve conter valores exclusivos. Há algumas opções adicionais para algumas relações, que veremos posteriormente. Por enquanto, vamos criar uma relação entre as colunas do projeto em cada uma de nossas duas tabelas.

### <a name="to-create-the-new-relationship"></a>Para criar a nova relação
1. Selecione **Gerenciar Relações** na guia **Página Inicial**.
2. Em **Gerenciar relações**, clique em **Nova** para abrir a caixa de diálogo **Criar relação**, na qual podemos selecionar tabelas, colunas e outras configurações desejadas para nossa relação.
3. Na primeira lista suspensa, selecione **ProjectHours** como a primeira tabela e, em seguida, selecione a coluna **Projeto**. Este é o lado *muitos* de nossa relação.
4. Na segunda lista suspensa, **CompanyProject** é pré-selecionada como a segunda tabela. Selecione a coluna **ProjName**. Este é o lado *um* de nossa relação. 
5. Aceite os padrões para as opções de relação e, em seguida, selecione **OK**.

   ![Caixa de diálogo Criar relação](media/desktop-create-and-manage-relationships/candmrel_create_compproj.png)

6. Na caixa de diálogo **Gerenciar relações**, selecione **Fechar**.

Buscando uma divulgação completa, acabamos criando essa relação da maneira mais difícil. Você poderia ter simplesmente selecionado **Detecção automática** na caixa de diálogo **Gerenciar relações**. Na verdade, a detecção automática teria criado automaticamente a relação para você quando você carregou os dados se ambas as colunas tivessem o mesmo nome. Mas qual é o desafio nisso?

Agora, vamos examinar novamente a tabela em nossa tela de relatório.

![Relação criada com Prioridade e Horas](media/desktop-create-and-manage-relationships/candmrel_reportfilterswithrel.png)

Agora está muito melhor, não é?

Quando somamos as horas por **Prioridade**, o Power BI Desktop procura cada instância dos valores de cor exclusivos na tabela de pesquisa **CompanyProject**, procura todas as instâncias de cada um desses valores na tabela **ProjectHours** e, por fim, calcula uma soma total para cada valor exclusivo.

Foi fácil. Na verdade, com a detecção automática, talvez você nem precise fazer tudo isso.

## <a name="understanding-additional-options"></a>Noções básicas sobre opções adicionais
Quando uma relação é criada, seja com detecção automática ou manualmente por você, o Power BI Desktop configura opções adicionais automaticamente com base nos dados de suas tabelas. Essas opções de relação adicionais estão localizadas na parte inferior das caixas de diálogo **Criar relação** e **Editar relação**.

 ![Opções de relação](media/desktop-create-and-manage-relationships/candmrel_advancedoptions2.png)

O Power BI tipicamente define essas opções automaticamente e você não precisará ajustá-las. No entanto, há várias situações em que você talvez queira configurar essas opções por conta própria.

## <a name="automatic-relationship-updates"></a>Atualizações automáticas de relação

Você pode gerenciar como o Power BI trata e ajusta automaticamente as relações em seus relatórios e modelos. Para especificar como o Power BI trata as opções de relações, selecione **Arquivo** > **Opções e configurações** > **Opções** no Power BI Desktop, em seguida, selecione **Carregamento de Dados** no painel esquerdo. As opções para **Relações** aparecem.

   ![Opções de relacionamentos](media/desktop-create-and-manage-relationships/relationships-options-01.png)

Há três opções disponíveis para selecionar e habilitar: 

- **Importar relacionamentos de fontes de dados no primeiro carregamento**: Esta opção é selecionada por padrão. Quando selecionada, o Power BI verifica as relações definidas na fonte de dados, como relações de chave estrangeira/chave primária no data warehouse. Se essas relações existirem, elas serão espelhadas no modelo de dados do Power BI quando você carregar os dados inicialmente. Essa opção permite que você comece a trabalhar rapidamente com seu modelo, em vez de exigir que você encontre ou defina essas relações por conta própria.

- **Atualize ou exclua relacionamentos ao atualizar os dados**: esta opção está desmarcada por padrão. Se você selecioná-la, o Power BI verificará se há alterações nas relações de fonte de dados quando o conjunto de dados for atualizado. Quando essas relações são alteradas ou removidas, o Power BI espelha essas alterações no respectivo modelo de dados, atualizando-as ou excluindo-as para correspondência.

   > [!WARNING]
   > Se você está usando a segurança em nível de linha que se baseia nas relações definidas, não é recomendável selecionar essa opção. Se você remover um relacionamento do qual se baseiam as configurações da RLS, o modelo poderá se tornar menos seguro. 

- **Detectar automaticamente novas relações após os dados serem carregados**: essa opção é descrita em [Detecção automática durante o carregamento](#autodetect-during-load). 


## <a name="future-updates-to-the-data-require-a-different-cardinality"></a>Atualizações futuras dos dados exigem uma cardinalidade diferente
Normalmente, o Power BI Desktop pode determinar automaticamente a melhor cardinalidade para a relação. Se precisar substituir a configuração automática por saber que os dados serão alterados no futuro, você poderá alterá-la com o controle **Cardinalidade**. Vejamos um exemplo em que precisamos selecionar uma cardinalidade diferente.

A tabela **CompanyProjectPriority** é uma lista de todos os projetos da empresa e da prioridade de cada um. A tabela **ProjectBudget** é o conjunto de projetos para os quais um orçamento foi aprovado.

**CompanyProjectPriority**

| **ProjName** | **Priority** |
| --- | --- |
| Azul |A |
| Vermelho |B |
| Verde |C |
| Amarelo |C |
| Roxo |B |
| Laranja |C |

**ProjectBudget**

| **Approved Projects** | **BudgetAllocation** | **AllocationDate** |
|:--- | ---:| ---:|
| Azul |40.000 |1212012 |
| Vermelho |100.000 |1212012 |
| Verde |50.000 |1212012 |

Se criarmos uma relação entre a coluna **Approved Projects** na tabela **ProjectBudget** e a coluna **ProjectName** na tabela **CompanyProjectPriority**, o Power BI definirá automaticamente a **Cardinalidade** como **Um para um (1:1)** e a **Direção do filtro cruzado** como **Ambas**. 

 ![Criar relação entre as colunas da tabela](media/desktop-create-and-manage-relationships/candmrel_create_compproj_appproj2.png)

O motivo pelo qual o Power BI faz essas configurações é que, para o Power BI Desktop, a melhor combinação das duas tabelas é a seguinte:

| **ProjName** | **Priority** | **BudgetAllocation** | **AllocationDate** |
|:--- | --- | ---:| ---:|
| Azul |A |40.000 |1212012 |
| Vermelho |B |100.000 |1212012 |
| Verde |C |50.000 |1212012 |
| Amarelo |C |<br /> |<br /> |
| Roxo |B |<br /> |<br /> |
| Laranja |C |<br /> |<br /> |

Há uma relação um para um entre nossas duas tabelas porque não há repetição de valores na coluna **ProjName** da tabela combinada. A coluna **ProjName** é exclusiva, porque cada valor ocorre apenas uma vez, assim, as linhas das duas tabelas podem ser combinadas diretamente sem nenhuma duplicação.

Mas digamos que você saiba que os dados mudarão na próxima vez que você atualizá-los. Uma versão atualizada da tabela **ProjectBudget** agora tem linhas adicionais para os projetos Azul e Vermelho:

**ProjectBudget**

| **Approved Projects** | **BudgetAllocation** | **AllocationDate** |
| --- | ---:| ---:|
| Azul |40.000 |1212012 |
| Vermelho |100.000 |1212012 |
| Verde |50.000 |1212012 |
| Azul |80,000 |6/1/2013 |
| Vermelho |90,000 |6/1/2013 |

 Essas linhas adicionais significam que a melhor combinação das duas tabelas agora é assim: 

| **ProjName** | **Priority** | **BudgetAllocation** | **AllocationDate** |
| --- | --- | ---:| ---:|
| Azul |A |40.000 |1212012 |
| Vermelho |B |100.000 |1212012 |
| Verde |C |50.000 |1212012 |
| Amarelo |C |<br /> |<br /> |
| Roxo |B |<br /> |<br /> |
| Laranja |C |<br /> |<br /> |
| Azul |A |80000 |6/1/2013 |
| Vermelho |B |90000 |6/1/2013 |

Nessa nova tabela combinada, a coluna **ProjName** tem valores repetidos. As duas tabelas originais não terão uma relação de tipo um para um depois que a tabela for atualizada. Nesse caso, por sabermos que as atualizações futuras farão com que a coluna **ProjName** tenha duplicatas, queremos definir a **Cardinalidade** como **Muitos Para Um (\*:1)** , com *muitos* no lado de **ProjectBudget** e *um* no lado de **CompanyProjectPriority**.

## <a name="adjusting-cross-filter-direction-for-a-complex-set-of-tables-and-relationships"></a>Ajuste da direção de filtro cruzado para um conjunto complexo de tabelas e relações
Para a maioria das relações, a direção do filtro cruzado é definida como **Ambas**. No entanto, há algumas circunstâncias mais incomuns em que você talvez precise definir essa opção de modo diferente do padrão, como se você estivesse importando um modelo de uma versão anterior do PowerPivot, na qual cada relação é configurada para uma direção. 

A configuração **Ambas** habilita o Power BI Desktop a tratar todos os aspectos das tabelas conectadas como se elas fossem uma tabela. Há algumas situações, porém, em que o Power BI Desktop não pode definir a direção de filtro cruzado da relação como **Ambas** e, ao mesmo tempo, manter um conjunto inequívoco de padrões disponíveis para fins de relatório. Se a direção de filtro cruzado de uma relação não é definida como **Ambas**, isso geralmente ocorre porque tal configuração geraria ambiguidade. Se a configuração padrão de filtro cruzado não está funcionando para você, você pode defini-la em direção a uma tabela específica ou **Ambas**.

A filtragem cruzada em uma única direção funciona em muitas situações. Na verdade, se você importar um modelo do PowerPivot no Excel 2013 ou anterior, todas as relações estarão definidas para uma única direção. O uso de uma única direção significa que as opções de filtragem, em tabelas conectadas, funcionam na tabela na qual está ocorrendo trabalho de agregação de valores. Às vezes compreender a filtragem cruzada pode ser um pouco difícil, portanto, vamos examinar um exemplo.

Com filtragem cruzada de direção única, se você criar um relatório que resume as horas de projeto, poderá escolher resumir (ou filtrar) pela tabela **CompanyProject** e sua coluna **Priority** ou pela tabela **CompanyEmployee** e sua coluna **City**. Se, no entanto, você quiser contar o número de funcionários por projeto (uma pergunta menos comum), isso não funcionará. Você obterá uma coluna de valores todos iguais. No seguinte exemplo, a direção da filtragem cruzada de ambas as relações está definida como uma direção: em direção à tabela **ProjectHours**. Em **Valores**, o campo **Projeto** é definido como **Contagem**:

 ![Direção da filtragem cruzada](media/desktop-create-and-manage-relationships/candmrel_repcrossfiltersingle.png)

A especificação de filtro fluirá de **CompanyProject** para **ProjectHours** (conforme mostra a imagem a seguir), porém, não fluirá até **CompanyEmployee**. 

 ![Exemplo de filtragem cruzada](media/desktop-create-and-manage-relationships/candmrel_singledircrossfiltering.png)


No entanto, se você definir a direção de filtragem cruzada como **Ambas**, ela funcionará. A configuração **Ambas** permite que a especificação de filtro flua até **CompanyEmployee**.

 ![Fluxo de especificação de filtro](media/desktop-create-and-manage-relationships/candmrel_bidircrossfiltering.png)

Com a direção da filtragem cruzada definida como **Ambas**, nosso relatório agora parece correto:

 ![Direção da filtragem cruzada definida como Ambas](media/desktop-create-and-manage-relationships/candmrel_repcrossfilterbi.png)

A filtragem cruzada em ambos os trajetos funciona bem para um padrão de relações de tabela como o padrão acima. Esse esquema é mais comumente chamado de um esquema em estrela, como esse:

 ![Filtragem cruzada em ambas as direções no esquema em estrela](media/desktop-create-and-manage-relationships/candmrel_crossfilterstarschema.png)

A direção de filtragem cruzada não funciona bem com um padrão mais geral encontrado com frequência em bancos de dados, como nesse diagrama:

 ![Filtragem cruzada em ambas as direções no padrão de banco de dados](media/desktop-create-and-manage-relationships/candmrel_crossfilterwithloops.png)

Se você tiver um padrão de tabela como este, com loops, então a filtragem cruzada pode criar um conjunto ambíguo de relações. Por exemplo, se você realiza a soma de um campo da Tabela X e, em seguida, opta por filtrar por um campo na Tabela Y, não fica claro o percurso que o filtro deve fazer: pela tabela superior ou pela inferior. Um exemplo comum para esse tipo de padrão é que a TableX seja uma tabela Sales com os dados efetivos e que TableY seja de dados de orçamento. Em seguida, as tabelas no meio são tabelas de pesquisa usadas por ambas as tabelas, como divisão ou região. 

Como ocorre com relações ativas/inativas, o Power BI Desktop não permitirá que uma relação seja definida como **Ambas** se isso gerar ambiguidade em relatórios. Há várias maneiras de lidar com essa situação. Aqui estão as duas mais comuns:

* Excluir ou marcar relações como inativas para reduzir a ambiguidade. Em seguida, talvez você possa definir a filtragem cruzada de uma relação como **Ambas**.
* Inclua uma tabela duas vezes (com um nome diferente na segunda vez) para eliminar os loops. Fazer isso torna o padrão de relações similar a um esquema em estrela. Com um esquema em estrela, todas as relações podem ser definidas como **Ambas**.

## <a name="wrong-active-relationship"></a>Relação ativa errada
Quando o Power BI Desktop cria relações automaticamente, ele às vezes encontra mais de uma relação entre duas tabelas. Quando essa situação acontece, apenas uma das relações é definida como ativa. A relação ativa serve como a relação padrão para que, quando você escolher campos de duas tabelas diferentes, o Power BI Desktop possa criar automaticamente uma visualização para você. No entanto, em alguns casos, a relação selecionada automaticamente pode estar errada. Use a caixa de diálogo **Gerenciar relações** para definir uma relação como ativa ou inativa ou defina a relação ativa na caixa de diálogo **Editar relação**. 

Para garantir que exista uma relação padrão, o Power BI Desktop permite apenas uma relação ativa entre duas tabelas em um determinado momento. Portanto, você deve primeiro definir a relação atual como inativa e, em seguida, definir como ativa a relação desejada.

Vejamos um exemplo. A primeira tabela é **ProjectTickets**, a segunda tabela é **EmployeeRole**.

**ProjectTickets**

| **Ticket** | **OpenedBy** | **SubmittedBy** | **Hours** | **Project** | **DateSubmit** |
| ---:|:--- |:--- | ---:|:--- | ---:|
| 1001 |Tom Perham |Alan Brewer |22 |Azul |1/1/2013 |
| 1002 |Daniel Romano |Alan Brewer |26 |Vermelho |2/1/2013 |
| 1003 |Daniel Roth |Shu Ito |34 |Amarelo |1242012 |
| 1004 |Tom Perham |Alan Brewer |13 |Laranja |1/2/2012 |
| 1005 |Daniel Romano |Eli Bowen |29 |Roxo |01/10/2013 |
| 1006 |Daniel Roth |Nuno Bento |35 |Verde |2/1/2013 |
| 1007 |Daniel Roth |David Hamilton |10 |Amarelo |01/10/2013 |
| 1008 |Tom Perham |Mu Han |28 |Laranja |1/2/2012 |
| 1009 |Daniel Romano |Shu Ito |22 |Roxo |2/1/2013 |
| 1010 |Daniel Roth |Eli Bowen |28 |Verde |1012013 |
| 1011 |Tom Perham |Eli Bowen |9 |Azul |10/15/2013 |

**EmployeeRole**

| **Employee** | **Função** |
| --- | --- |
| Nuno Bento |Gerente de projeto |
| Eli Bowen |Líder de projeto |
| Alan Brewer |Gerente de projeto |
| David Hamilton |Líder de projeto |
| Mu Han |Líder de projeto |
| Shu Ito |Líder de projeto |
| Tom Perham |Patrocinador de projeto |
| Daniel Romano |Patrocinador de projeto |
| Daniel Roth |Patrocinador de projeto |

Na verdade, existem duas relações aqui:
- Entre **Employee** na tabela **EmployeeRole** e **SubmittedBy** na tabela **ProjectTickets**.
- Entre **OpenedBy** na tabela **ProjectTickets** e **Employee** na tabela **EmployeeRole**.

 ![Exemplo de duas relações](media/desktop-create-and-manage-relationships/candmrel_activerelview.png)

Se adicionarmos ambas as relações no modelo (**OpenedBy** primeiro), a caixa de diálogo **Gerenciar relações** mostrará que **OpenedBy** está ativo:

 ![OpenedBy ativo na caixa de diálogo Gerenciar relações](media/desktop-create-and-manage-relationships/candmrel_managerelactive.png)

Agora, se criarmos um relatório que usa os campos **Role** e **Employee** de **EmployeeRole** e o campo **Hours** de **ProjectTickets** em uma visualização de tabela na tela Relatório, veremos apenas patrocinadores de projeto, porque eles são os únicos a terem aberto um tíquete de projeto.

 ![Campos Employee, Role e Hours selecionados](media/desktop-create-and-manage-relationships/candmrel_repcrossfilteractive.png)

Podemos alterar a relação ativa e obter **SubmittedBy**, em vez de **OpenedBy**. Em **Gerenciar relações**, desmarcamos a relação entre **ProjectTickets(OpenedBy)** e **EmployeeRole(Employee)** e, em seguida, marcamos **EmployeeRole(Employee)** como a relação **Project Tickets(SubmittedBy)** .

![Alterar relação ativa na caixa de diálogo Gerenciar relação](media/desktop-create-and-manage-relationships/candmrel_managerelactivesubmittedby.png)

## <a name="see-all-of-your-relationships-in-relationship-view"></a>Ver todas as relações na exibição Relação
Às vezes, seu modelo tem várias tabelas e relações complexas entre elas. A exibição **Relação** no Power BI Desktop mostra todas as relações em seu modelo, sua direção e cardinalidade em um diagrama fácil de entender e personalizável. 

Para saber mais, confira [Trabalhar com a exibição Relação no Power BI Desktop](desktop-relationship-view.md).

