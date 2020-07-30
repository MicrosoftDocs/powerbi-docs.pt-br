---
title: Usar temas de relatório no Power BI Desktop
description: Saiba como usar uma paleta de cores personalizada e aplicá-la a um relatório inteiro no Power BI Desktop.
author: davidiseminger
ms.reviewer: ''
ms.custom: contperfq4
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 07/28/2020
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: fdd08c32277dfaa9a619b024a7fb0ece0517f1cb
ms.sourcegitcommit: a254f6e2453656f6783690669be8e881934e15ac
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/28/2020
ms.locfileid: "87364090"
---
# <a name="use-report-themes-in-power-bi-desktop"></a>Usar temas de relatório no Power BI Desktop

Com os *temas de relatório* do Power BI Desktop, você pode aplicar alterações no design de seu relatório inteiro para, por exemplo, usar cores corporativas, alterar conjuntos de ícones ou aplicar uma nova formatação visual padrão. Quando você aplica um tema de relatório, todos os visuais do relatório passam a usar as cores e a formatação do tema selecionado com seus padrões. Algumas exceções se aplicam e são descritas neste artigo.

Os temas de relatório podem ser selecionados navegando até a faixa de opções **Exibição** e, em seguida, selecionando o botão de seta suspenso na seção **Temas** da faixa de opções e, em seguida, selecionando o tema desejado. Os temas disponíveis são semelhantes aos temas vistos em outros produtos da Microsoft, como o Microsoft PowerPoint.

![Temas de relatórios](media/desktop-report-themes/report-themes-01.png)

Há dois tipos de temas de relatório: os temas de relatório internos e os arquivos de tema de relatório personalizado.

- Os temas de relatório **internos** fornecem diferentes tipos de esquemas de cores predefinidos que são instalados com o Power BI Desktop. Selecione temas de relatório internos diretamente no menu do Power BI Desktop.

- Os temas de relatório **personalizados** são criados ajustando um tema atual e, em seguida, salvando-o como um tema personalizado ou criando o seu próprio tema de personalizado usando um arquivo JSON. O arquivo JSON fornece controle granular sobre vários aspectos de um tema de relatório, conforme descrito posteriormente neste artigo. 

Vamos discutir como os temas de relatório funcionam e, em seguida, mostraremos como criar temas de relatório personalizados.


## <a name="how-report-themes-work"></a>Como os temas de relatório funcionam

Para aplicar um tema de relatório a um relatório do Power BI Desktop, você pode selecionar uma das seguintes opções:

* Selecione entre os [temas de relatório internos disponíveis](#built-in-report-themes) que são integrados ao Power BI Desktop
* Personalize um tema, usando a caixa de diálogo **Personalizar tema**
* [Importe um arquivo JSON de tema personalizado](#import-custom-report-theme-files).

Vamos dar uma olhada em cada uma dessas opções de cada vez.

> [!NOTE]
> Os temas podem ser aplicados somente ao usar o Power BI Desktop. Não é possível aplicar temas a relatórios existentes no serviço do Power BI. 

### <a name="built-in-report-themes"></a>Temas de relatório internos

Para selecionar entre os temas de relatório internos disponíveis:

1. Selecione o botão de seta suspenso **Temas** **Alternar Tema** na faixa de opções **Exibição**.

   ![Selecionar um tema de relatório](media/desktop-report-themes/report-themes-02.png)

2. Selecione um dos temas incluídos no menu suspenso que é exibido.

   ![Selecionar um tema de relatório](media/desktop-report-themes/report-themes-03.png)

   Agora, o tema é aplicado ao relatório.

    A tabela a seguir mostra os temas de relatório internos disponíveis.
    
    | Tema de relatório interno | Sequência de cores padrão |
    |------ |---------- |
    | Padrão | ![Padrão](media/desktop-report-themes/report-themes-color-scheme-default.png)|
    | Highrise | ![Highrise](media/desktop-report-themes/report-themes-color-scheme-highrise.png)|
    | Executivo | ![Executivo](media/desktop-report-themes/report-themes-color-scheme-executive.png)|
    | Fronteira| ![Fronteira](media/desktop-report-themes/report-themes-color-scheme-frontier.png)|
    | Inovar | ![Inovar](media/desktop-report-themes/report-themes-color-scheme-innovative.png)|
    | Bloom | ![Bloom](media/desktop-report-themes/report-themes-color-scheme-bloom.png)|
    | Tidal| ![Tidal](media/desktop-report-themes/report-themes-color-scheme-tidal.png)|
    | Temperatura | ![Temperatura](media/desktop-report-themes/report-themes-color-scheme-temperature.png)|
    | Solar| ![Solar](media/desktop-report-themes/report-themes-color-scheme-solar.png)|
    | Divergente | ![Divergente](media/desktop-report-themes/report-themes-color-scheme-divergent.png)|
    | Storm | ![Storm](media/desktop-report-themes/report-themes-color-scheme-storm.png)|
    | Clássico | ![Clássico](media/desktop-report-themes/report-themes-color-scheme-classic.png)|
    | Parque urbano | ![Parque urbano](media/desktop-report-themes/report-themes-color-scheme-city-park.png)|
    | Sala de aula | ![Sala de aula](media/desktop-report-themes/report-themes-color-scheme-classroom.png)|
    | Adequado para daltônicos | ![Adequado para daltônicos](media/desktop-report-themes/report-themes-color-scheme-colorblind-safe.png)|
    | Elétrico | ![Elétrico](media/desktop-report-themes/report-themes-color-scheme-electric.png)|
    | Alto contraste | ![Alto contraste](media/desktop-report-themes/report-themes-color-scheme-high-contrast.png)|
    | Pôr do sol | ![Pôr do sol](media/desktop-report-themes/report-themes-color-scheme-sunset.png)|
    | Crepúsculo | ![Crepúsculo](media/desktop-report-themes/report-themes-color-scheme-twilight.png)|
    
3. Você também pode procurar a coleção de temas criados por membros da Comunidade do Power BI, selecionando **Galeria de temas** na lista suspensa Temas.

   ![Galeria de temas](media/desktop-report-themes/report-themes-04.png)

    Na galeria, você pode selecionar um tema que goste e baixar o arquivo JSON associado a ele. 

    Para instalar o arquivo baixado, selecione **Procurar temas** na lista suspensa **Temas**, navegue até a localização em que você baixou o arquivo JSON e selecione-o para importar o tema para o Power BI Desktop como um novo tema.

    Quando for bem-sucedida, o Power BI mostrará uma caixa de diálogo de que a importação foi bem-sucedida.

   ![Importação de tema bem-sucedida](media/desktop-report-themes/report-themes-05.png)

## <a name="customize-report-themes"></a>Personalizar temas do relatório

Você pode personalizar e padronizar praticamente todos os elementos relacionados na seção **Formatar** do painel **Visualizações**, seja por meio de personalizações feitas diretamente no Power BI Desktop ou por meio do arquivo JSON de tema de relatório. A meta é fornecer a você o controle completo sobre a aparência padrão do seu relatório, alcançando um nível granular.

As duas maneiras de personalizar temas de relatório são as seguintes:

- [Criar e personalizar um tema no Power BI Desktop](#create-and-customize-a-theme-in-power-bi-desktop)
- [Criar e personalizar um arquivo JSON de tema de relatório personalizado](#introduction-to-report-theme-json-files)

Vamos dar uma olhada em cada uma dessas abordagens, uma de cada vez, nas seções a seguir.

### <a name="create-and-customize-a-theme-in-power-bi-desktop"></a>Criar e personalizar um tema no Power BI Desktop

Para personalizar um tema diretamente no Power BI Desktop, você pode selecionar um tema próximo ao que deseja e fazer alguns ajustes. Primeiro, selecione o tema que está próximo (ou apenas comece com qualquer tema e personalize-o) e execute as seguintes etapas:

1. Na faixa de opções **Exibição**, selecione o botão suspenso **Temas** e selecione **Personalizar o tema atual**.

   ![Personalizar o tema](media/desktop-report-themes/report-themes-06.png)

2. Uma caixa de diálogo é exibida, na qual você pode fazer todos os tipos de alterações no tema atual e, em seguida, pode salvar as suas configurações como um novo tema.

   ![Personalizar o tema atual](media/desktop-report-themes/report-themes-07.png)

As configurações de tema que podem ser personalizadas encontram-se nas seguintes categorias, refletidas na janela **Personalizar o tema**:

- **Nome e cores**: As configurações de nome e cor do tema incluem as [cores do tema](#how-report-theme-colors-stick-with-your-reports), as cores do sentimento, as cores divergentes e as [cores estruturais (Avançado)](#setting-structural-colors).
- **Texto**: As configurações de texto incluem a família, o tamanho e a cor da fonte, que define [os padrões de classe de texto primária](#setting-formatted-text-defaults) para rótulos, títulos, cartões e KPIs e cabeçalhos de guias.
- **Visuais**: As configurações de visuais incluem a tela de fundo, a borda, o cabeçalho e as dicas de ferramentas.
- **Página**: as configurações de elementos de página incluem papel de parede e plano de fundo.
- **Painel de filtros**: as configurações do painel de filtros incluem cor da tela de fundo, transparência, fonte e cor do ícone, tamanho, cartões de filtro.

Depois de fazer as alterações, selecione **Aplicar e salvar** para salvar seu tema. Agora é possível usar o seu tema no relatório atual e exportá-lo.

Personalizar o tema atual dessa maneira agiliza e facilita a personalização dos temas. No entanto, você pode fazer ajustes mais precisos em temas, o que exige a modificação do [arquivo JSON](#report-theme-json-file-format) do tema.

> [!TIP]
> Você pode personalizar as opções de tema do relatório mais comuns usando os controles na caixa de diálogo **Personalizar tema**. Para ter ainda mais controle, você pode opcionalmente exportar o arquivo JSON de um tema e fazer ajustes, modificando manualmente as configurações desse arquivo. Você pode renomear esse arquivo JSON ajustado para depois importá-lo.

### <a name="import-custom-report-theme-files"></a>Importar arquivos de tema de relatório personalizado

Você também pode importar um arquivo de tema de relatório personalizado, executando as seguintes etapas:

1. Selecione a faixa de opções **Exibição** e, em seguida, no botão suspenso **Temas**, selecione **Procurar temas**.

   ![Importar tema](media/desktop-report-themes/report-themes-08.png)

   Será exibida uma janela permitindo navegar até o local do arquivo de tema JSON.

2. Na imagem a seguir, alguns arquivos de tema de feriado estão disponíveis. Vamos escolher um tema de feriado em março, *St Patricks Day.json*.

   ![Tema de feriado](media/desktop-report-themes/report-themes_4.png)

   Quando o arquivo de tema é carregado com êxito, o Power BI Desktop mostra uma mensagem de êxito.

   ![Importação de tema bem-sucedida](media/desktop-report-themes/report-themes-05.png)

## <a name="introduction-to-report-theme-json-files"></a>Introdução aos arquivos JSON de tema de relatório

 Ao abrir o arquivo JSON básico mencionado na seção anterior (St Patricks Day.json), ele é exibido da seguinte maneira:

 ```json
    {
        "name": "St Patrick's Day",
        "dataColors": ["#568410", "#3A6108", "#70A322", "#915203", "#D79A12", "#bb7711", "#114400", "#aacc66"],
        "background":"#FFFFFF",
        "foreground": "#3A6108",
        "tableAccent": "#568410"
    }
```

Este arquivo JSON de tema de relatório tem as seguintes linhas:

- **name**: o nome do tema do relatório. Este é o único campo obrigatório.
- **dataColors**: a lista de códigos hexadecimais de cores a ser usada nos dados dos visuais do Power BI Desktop. Essa lista pode ter quantas cores você desejar.
- **background**, **firstLevelElements** e **tableAccent** (etc.): são classes de cores. As classes de cores permitem definir muitas cores estruturais no relatório de uma só vez.

Você pode usar esse arquivo JSON como base para criar seu próprio arquivo de tema de relatório personalizado a ser importado. Se quiser ajustar apenas as cores básicas do relatório, altere o nome e os códigos hexadecimais no arquivo.

Em um arquivo JSON de tema de relatório, você define apenas a formatação que deseja alterar. Tudo o que você não especificar no arquivo JSON será revertido para as configurações padrão do Power BI Desktop.

As vantagens de criar um arquivo JSON são muitas. Por exemplo, você pode especificar que todos os gráficos usem o tamanho de fonte 12, que alguns visuais usem uma família de fontes específica ou que os rótulos de dados fiquem desativados em determinados tipos de gráfico. Ao usar um arquivo JSON, você pode criar um arquivo de tema de relatório que padroniza os gráficos e relatórios, facilitando a consistência entre os relatórios de sua organização.

Para obter mais informações sobre o formato do arquivo JSON, confira [Formato de arquivo JSON de tema de relatório](#report-theme-json-file-format).

> [!NOTE]
> A modificação de um tema de relatório JSON personalizado com a [caixa de diálogo **Personalizar tema**](#create-and-customize-a-theme-in-power-bi-desktop) é segura.  A caixa de diálogo não modificará as configurações de tema que ele não pode controlar e atualizará as alterações feitas no tema do relatório in-loco.

## <a name="how-report-theme-colors-stick-with-your-reports"></a>Como as cores de tema de relatório permanecem nos relatórios

Ao publicar o relatório no serviço do Power BI, as cores do tema de relatório continuam nele. A seção **Cores dos dados** do painel **Formatar** reflete o tema do relatório.

Para exibir as cores disponíveis em um tema de relatório:

1. Selecione um visual.

2. Na seção **Formatar** do painel de **Visualização**, selecione **Cores dos dados**.

3. Selecione a lista suspensa de um item para exibir as informações das **Cores do tema** do relatório.

   ![Cores do tema](media/desktop-report-themes/report-themes-09.png)

Em nosso exemplo, após você aplicar diversos tons de verde e marrom do tema de relatório Dia de São Patrício, exiba as cores do tema. Viu todo esse verde? Isso ocorre porque essas cores faziam parte do tema de relatório importado e aplicado.

As cores da paleta também têm relação com o tema atual. Por exemplo, suponha que você selecione a terceira cor da linha superior para um ponto de dados. Posteriormente, se você alterar para um tema diferente, a cor desse ponto de dados será atualizada automaticamente para a terceira cor da linha superior no novo tema, assim como você veria ao alterar os temas no Microsoft Office.

Configurar o tema de um relatório altera as cores padrão usadas nos visuais em todo o relatório. O Power BI mantém uma lista com centenas de cores a fim de garantir que os visuais tenham diversas cores exclusivas para exibição nos relatórios. Quando o Power BI atribui cores à série de um visual, essas cores são selecionadas por ordem de chegada conforme as cores da série são atribuídas. Quando você importa um tema, o mapeamento de cores da série de dados é redefinido. 

O Power BI acompanha a cor de uma série dinâmica e usa a mesma cor para o valor em outros visuais. Em uma *série dinâmica*, o número de séries apresentadas nos visuais pode mudar com base nas medidas, nos valores ou em outros aspectos. Por exemplo, se mostrar o *Lucro por região* em um relatório, você poderá ter cinco ou poderá ter nove regiões de vendas. O número de regiões é dinâmico e, portanto, é considerado uma série dinâmica. 

Por outro lado, em uma *série estática*, o número de séries é conhecido. Por exemplo, *Lucro* e *Receita* são séries estáticas. Em séries estáticas, o Power BI atribui as cores de acordo com o índice dentro das paletas do tema. Você pode substituir a atribuição de cor padrão selecionando uma cor no painel de formatação em **Cores de dados**. Talvez você precise alterar suas seleções de segmentação para ver todos os valores potenciais da série e definir as cores deles também. Se você definir explicitamente a cor de um só visual usando o painel **Propriedades**, o tema importado não se aplicará a nenhuma dessas cores definidas explicitamente. 

Para que o tema se aplique às cores selecionadas explicitamente, use **Reverter para o padrão** na seção **Cores de dados** do visual cuja cor foi definida explicitamente, a fim de desfazer a aplicação de cor explícita e permitir que o tema seja aplicado.


### <a name="situations-when-report-theme-colors-wont-stick-to-your-reports"></a>Situações em que as cores do tema de relatório não permanecem nos relatórios

Vamos supor que você aplique um conjunto de cores personalizado (ou uma cor individual) a determinado ponto de dados em um visual usando a opção **Cor personalizada** no seletor de cores. Quando você aplica um tema de relatório, ele *não* substitui a cor do ponto de dados personalizado.

Suponha que você também precise definir manualmente a cor de um ponto de dados usando a seção **Cores do tema**. Quando você aplicar um novo tema de relatório, essas cores *não* serão atualizadas. Para retornar às cores padrão de modo que elas sejam atualizadas quando você aplicar um novo tema de relatório, selecione **Reverter para padrão** ou selecione uma cor na paleta **Cores do tema** no seletor de cores.

![Reverter para o padrão](media/desktop-report-themes/report-themes-10.png)

Muitos visuais do Power BI não se aplicam aos temas de relatório.

## <a name="custom-report-theme-files-you-can-use-right-now"></a>Arquivos de tema de relatório personalizado que você pode usar agora

Deseja começar a usar temas de relatório? Confira os temas de relatório personalizados na [galeria de temas](https://community.powerbi.com/t5/Themes-Gallery/bd-p/ThemesGallery) o experimente os arquivos JSON de tela de relatório personalizado já prontos que você pode baixar e importar para o seu relatório do Power BI Desktop:

- [Tema de forma de onda](https://community.powerbi.com/t5/Themes-Gallery/Waveform/m-p/140536). Esse tema de relatório foi introduzido na [postagem no blog](https://powerbi.microsoft.com/blog/power-bi-desktop-march-feature-summary/) que anunciou a primeira versão dos temas de relatório. [Baixar Waveform.json](https://go.microsoft.com/fwlink/?linkid=843924).

  ![Tema waveform.json](media/desktop-report-themes/report-themes_10.png)

- [Tema amigável para daltônicos](https://community.powerbi.com/t5/Themes-Gallery/Color-Blind-Friendly/m-p/140597).
Esse tema de relatório facilita a leitura de portadores de deficiências visuais. [Baixe o ColorblindSafe-Longer.json](https://go.microsoft.com/fwlink/?linkid=843923).

  ![Tema ColorblindSafe-Longer.json](media/desktop-report-themes/report-themes_11.png).

- Temas do Power View, apresentando o Apothecary.json. [Baixe os temas do Power View em um arquivo zip](https://go.microsoft.com/fwlink/?linkid=843925).

  ![Tema Apothecary.json](media/desktop-report-themes/report-themes_12.png)

- Tema Dia dos Namorados.

  ![Tema Dia dos Namorados](media/desktop-report-themes/report-themes_13.png)

  Aqui está o código do arquivo JSON do Dia dos Namorados:

   ```json
       {
           "name": "Valentine's Day",
           "dataColors": ["#990011", "#cc1144", "#ee7799", "#eebbcc", "#cc4477", "#cc5555", "#882222", "#A30E33"],
           "background":"#FFFFFF",
           "foreground": "#ee7799",
           "tableAccent": "#990011"
       }
   ```

Aqui estão alguns mais temas de relatório, que você pode usar como pontos de partida:

- [Girassol-crepúsculo](https://community.powerbi.com/t5/Themes-Gallery/Sunflower-Twilight/m-p/140749)
- [Ameixa](https://community.powerbi.com/t5/Themes-Gallery/Plum/m-p/140711)
- [Outono](https://community.powerbi.com/t5/Themes-Gallery/Autumn/m-p/140746)
- [Alto contraste](https://community.powerbi.com/t5/Themes-Gallery/Color-Blind-Friendly/m-p/140597)

Os temas de relatório permitem que seus relatórios do Power BI Desktop reflitam as suas cores ou as cores da organização, da estação ou do feriado atual.

## <a name="export-report-themes"></a>Exportar temas de relatório

Você pode exportar o tema de relatório atualmente aplicado diretamente do Power BI Desktop para um arquivo JSON. Depois de exportar um tema de relatório, você poderá reutilizá-lo em outros próprios. Essa opção permite exportar o arquivo JSON da maioria dos temas internos. As únicas exceções são os temas básicos, Clássico e Padrão, com base nos quais os outros temas são criados quando importados.

Para exportar o tema atualmente aplicado do Power BI Desktop:

1. Selecione **Arquivo** > **Opções e configurações** > **Opções**.

2. Na seção **Versão prévia dos recursos**, selecione **Personalizar o tema atual** e **OK**.

   Talvez você precise reiniciar o Power BI Desktop para que a versão prévia do recurso seja habilitada. Depois de reiniciar, você pode começar a exportar o tema aplicado no momento.

3. Na faixa de opções **Início**, selecione **Alternar tema** > **Exportar tema atual**.

4. Na caixa de diálogo **Salvar Como**, navegue até o diretório que contém o aquivo JSON e selecione **Salvar**.

## <a name="report-theme-json-file-format"></a>Formato de arquivo JSON de tema do relatório

Em seu nível mais básico, o arquivo JSON de tema tem apenas uma linha obrigatória: **name**.

```json
{
    "name": "Custom Theme"
}
```

Exceto por **name**, todo o restante é opcional, ou seja, você pode adicionar as propriedades específicas que deseja formatar ao arquivo do tema e continuar usando os padrões do Power BI para o restante.

### <a name="setting-theme-colors"></a>Definir as cores do tema

Em **name**, você pode adicionar algumas propriedades básicas relacionadas à cor dos dados:

- **dataColors**: A lista de códigos hexadecimais de cores a ser usada para colorir formas que representam os dados dos visuais do Power BI Desktop. Essa lista pode ter quantas cores você desejar. Quando todas as cores dessa lista tiverem sido usadas, se o visual ainda precisar de mais cores, ele passará a usar a paleta de cores padrão do Power BI.
- **good**, **neutral**, **bad**: Essas propriedades definem as cores de status usadas pelo gráfico de cascata e pelo visual de KPI.
- **maximum**, **center**, **minimum**, **null**: Definem as diversas cores gradientes na caixa de diálogo de formatação condicional.

Veja abaixo como seria um tema básico que define essas cores:

```json
{
    "name": "Custom Theme",
    "dataColors": [
        "#118DFF",
        "#12239E",
        "#E66C37",
        "#6B007B",
        "#E044A7",
        "#744EC2",
        "#D9B300",
        "#D64550",
        "#197278",
        "#1AAB40"
    ],
    "good": "#1AAB40",
    "neutral": "#D9B300",
    "bad": "#D64554",
    "maximum": "#118DFF",
    "center": "#D9B300",
    "minimum": "#DEEFFF",
    "null": "#FF7F48"
}
```

### <a name="setting-structural-colors"></a>Definir cores estruturais

Em seguida, você pode adicionar várias classes de cores, como **background** e **firstLevelElements**. Essas classes de cor definem as cores estruturais dos elementos no relatório, como linhas de grade do eixo, cores de realce e cores da tela de fundo para elementos visuais.

A tabela a seguir mostra as seis classes de cores que você pode formatar.  Os nomes de **Classe de cor** correspondem aos nomes na subseção "Avançado" da seção "Nome e cores" na [caixa de diálogo **Personalizar tema**](#create-and-customize-a-theme-in-power-bi-desktop).

|Classe de cor  |O que ela formata  |
|---------|---------|
| **firstLevelElements** <br> **foreground** (preterido) | Cor do plano de fundo dos rótulos (quando estiverem fora dos pontos de dados) <br> Cor da linha de tendência <br>  Cor padrão da caixa de texto <br> Valores de tabela e matriz e cores de fonte de valores totais, cor do eixo de barras de dados <br> Rótulos de dados de cartão <br> Cor do valor de balão do medidor <br> Cor da meta de KPI <br>  Cor do texto de KPI <br> Cor do item da segmentação (quando estiver no modo de foco)  <br> Cor da fonte do item de menu suspenso da segmentação de dados <br> Cor da fonte de entrada numérica da segmentação de dados <br> Cor da fonte do cabeçalho da segmentação de dados <br> Cor da linha de proporção do gráfico de dispersão <br> Cor da linha de previsão do gráfico de linhas <br> Cor da linha tracejada do mapa <br> Cor do painel do filtro e texto do cartão|
| **secondLevelElements** <br> **foregroundNeutralSecondary** (preterido) | [classes de texto secundário](#setting-formatted-text-defaults) “claras” <br> Cores do rótulo  <br> Cor do rótulo de legenda <br> Cor do rótulo de eixo <br> Cor da fonte do cabeçalho da tabela e da matriz <br> Cor da linha tracejada de destino e do destino do medidor <br>  Cor do eixo de tendência do KPI <br> Cor do controle deslizante da segmentação de dados <br> Cor da fonte do item da segmentação de dados <br> Cor do contorno da segmentação de dados <br> Cor da focalização do gráfico de linhas <br> Cor do título do cartão de múltiplas linhas <br> Cor do traçado do gráfico de faixas <br> Cor da borda do mapa da forma <br> Cor da fonte do texto do botão <br> Cor da linha do ícone do botão <br> Cor do contorno do botão |
| **thirdLevelElements** <br >**backgroundLight** (preterido) | Cor da linha de grade do eixo <br> Cor da grade de tabela e da matriz <br> Cor do plano de fundo do cabeçalho da segmentação (no modo de foco)  <br> Cor do contorno do cartão com várias linhas  <br> Cor de preenchimento da forma <br> Cor da tela de fundo do arco do medidor <br> Cor do plano de fundo do cartão de filtro aplicado <br> Quando a tela de fundo = FFFFFF: <br> Cor do preenchimento do botão desabilitada <br> Cor do contorno do botão desabilitada <br> |
| **fourthLevelElements** <br> **foregroundNeutralTertiary** (preterido) | Cor esmaecida da legenda <br> Cor do rótulo da categoria do cartão <br> Cor dos rótulos da categoria de cartão com várias linhas <br> Cor da barra do cartão com várias linhas <br> Cor do traçado da taxa de conversão do gráfico de funil <br> Cor da fonte do texto do botão desabilitada <br> Cor da linha do ícone do botão desabilitada <br> |
| **segundo plano** | Cor do plano de fundo dos rótulos (quando estiver dentro dos pontos de dados) <br> Cor do plano de fundo de itens de menu suspenso da segmentação de dados  <br> Cor do traçado do gráfico de rosca <br> Cor do traçado do mapa de árvore <br> Cor do plano de fundo do gráfico de combinação <br> Cor de preenchimento do botão <br> Cor do plano de fundo do painel de filtro e do cartão de filtro disponível |
| **secondaryBackground** <br> **backgroundNeutral** (preterido) | Cor de contorno da grade da tabela e da matriz <br> Cor padrão do mapa de formas <br> Cor de preenchimento da faixa de opções do gráfico de faixas (quando a opção de série de correspondência estiver desativada) <br> Quando a tela de fundo != FFFFFF: <br> Cor do preenchimento do botão desabilitada <br> Cor do contorno do botão desabilitada <br> |
| **tableAccent** | Substitui a cor de contorno da tabela e da grade de matriz, quando estiver presente |

Veja um exemplo de tema que define as classes de cor:

```json
{
    "name": "Custom Theme",
    "firstLevelElements": "#252423",
    "secondLevelElements": "#605E5C",
    "thirdLevelElements": "#F3F2F1",
    "fourthLevelElements": "#B3B0AD",
    "background": "#FFFFFF",
    "secondaryBackground": "#C8C6C4",
    "tableAccent": "#118DFF"
}
```

> [!TIP]
> Se você estiver criando um "tema escuro" ou outro tema colorido que seja diferente do **firstLevelElements** “preto” no estilo da **tela de fundo** “branca”, defina também os valores para outras cores estruturais e as [cores da classe de texto primária](#setting-formatted-text-defaults).  Isso verificará se (por exemplo) os rótulos de dados nos gráficos com uma tela de fundo de rótulo corresponderão ao estilo previsto e serão legíveis, assim como se as linhas de grade do eixo estão visíveis.

### <a name="setting-formatted-text-defaults"></a>Definir padrões de texto formatado

Em seguida, você pode adicionar classes de texto ao seu arquivo JSON. Classes de texto são semelhantes às classes de cores, mas foram desenvolvidas para permitir que você atualize o tamanho, a cor e a família da fonte para grupos de texto em seu relatório.

Há 12 classes de texto, mas você precisa definir somente quatro classes, chamadas de *classes primárias*, para alterar toda a formatação de texto em seu relatório.  Essas quatro classes primárias podem ser definidas na [caixa de diálogo **Personalizar tema**](#create-and-customize-a-theme-in-power-bi-desktop) na seção "Texto": "Geral" corresponde a **label**, "Título" a **title**, "Cartões e KPIs" a **callout** e "Cabeçalhos de guias" a **header**.

Outras classes de texto, consideradas *classes secundárias*, derivam automaticamente suas propriedades de suas classes primárias associadas. Frequentemente, uma classe secundária seleciona um tom mais claro de cor de texto ou um percentual de tamanho de texto maior ou menor em comparação com a classe primária.

Veja a classe **label**, por exemplo. A formatação padrão para a classe **label** é Segoe UI, #252423 (uma cor cinza escuro) e 12 pontos. Essa classe é usada para formatar os valores na tabela e na matriz. Normalmente, os valores totais em uma tabela ou matriz têm uma formatação semelhante, mas ficam em negrito com a classe **bold label** para que se destaquem. No entanto, você não precisa especificar essa classe no tema JSON, pois o Power BI faz isso automaticamente. Se você decidir posteriormente especificar rótulos que tenham uma fonte de 14 pontos em seu tema, não será necessário atualizar também a classe **bold label**, porque ela herda a formatação de texto da classe **label**.

A tabela a seguir mostra estas informações:

- Cada uma das quatro classes de texto primárias, o que elas formatam e suas configurações padrão
- Cada classe secundária, o que elas formatam e sua configuração padrão, que é exclusiva em comparação com a classe primária

|Classe primária  |Classes secundárias  |Nome da classe do JSON  | Configurações padrão  |Objetos visuais associados  |
|---------|---------|---------|---------|---------|
| Callout | N/D | callout | DIN <br> #252423 <br> 45pt |Rótulos de dados de cartão <br> Indicadores de KPI|
|Cabeçalho|N/D|header|Segoe UI Semibold <br> #252423 <br> 12pt |Cabeçalhos dos principais influenciadores |
| Título || title |DIN <br> #252423 <br> 12pt |Título do eixo de categoria <br> Título do eixo dos valores <br> Título do cartão de múltiplas linhas * <br> Cabeçalho de segmentação de dados|
|-| Large title | largeTitle |14pt |Título visual |
|Label ||label |Interface do Usuário Segoe<br>#252423<br>10pt |Cabeçalhos de coluna de tabela e matriz <br> Cabeçalhos de linha de matriz<br>Grade de tabela e matriz<br>Valores de tabela e matriz |
|-|Semibold |semiboldLabel| Segoe UI Semibold | Texto do perfil de principais influenciadores
|-|Grande |largeLabel |12pt | Rótulos de dados de cartão com múltiplas linhas |
|-|Pequeno |smallLabel |9pt |Rótulos da linha de referência * <br>Rótulos de intervalo de datas da segmentação de dados<br> Estilo de texto de entrada numérica da segmentação de dados<br>Caixa de pesquisa da segmentação de dados<br>Texto influenciador de principais influenciadores|
|-|Claro |lightLabel |#605E5C |Texto da legenda<br>Texto do botão<br>Rótulos de eixo de categoria<br>Rótulos de dados do gráfico de funil<br>Rótulos de taxa de conversão de gráfico de funil<br>Destino do medidor<br>Rótulo de categoria do gráfico de dispersão<br>Itens de segmentação de dados|
|-|Bold |boldLabel |Segoe UI Bold |Subtotais da matriz<br>Totais gerais da matriz<br>Totais da tabela |
|-|Large and Light |largeLightLabel |#605E5C<br>12pt |Rótulos da categoria do cartão<br>Rótulo do medidor<br>Rótulos de categoria de cartão com várias linhas |
|-|Small and Light |smallLightLabel |#605E5C<br>9pt |Rótulos de dados<br>Rótulos de eixo de valor|

*\* Os itens com estrela também são coloridos com base na primeira cor de dados do tema do relatório.*

> [!TIP]
> As variações *claras* das classes de texto extraem as cores claras delas das [cores estruturais](#setting-structural-colors) definidas acima.  Se você estiver criando um "tema escuro", defina também as cores "firstLevelElements" (que correspondem à cor do texto primário), "secondLevelElements" (que corresponde à cor de "clara" prevista para o texto) e "background" (com contraste suficiente para as cores de elementos de primeiro e segundo níveis).

Veja um exemplo de tema que define apenas as classes de texto primárias:

```json
{
    "name": "Custom Theme",
    "textClasses": {
        "callout": {
            "fontSize": 45,
            "fontFace": "DIN",
            "color": "#252423"
        },
        "title": {
            "fontSize": 12,
            "fontFace": "DIN",
            "color": "#252423"
        },
        "header": {
            "fontSize": 12,
            "fontFace": "Segoe UI Semibold",
            "color": "#252423"
        },
        "label": {
            "fontSize": 10,
            "fontFace": "Segoe UI",
            "color": "#252423"
        }
    }
}
```

Como as classes secundárias herdam as configurações das classes primárias, você não precisa defini-las em seu arquivo de tema. Entretanto, se não gostar das regras de herança (por exemplo, se não quiser que os totais sejam uma versão em negrito dos valores em uma tabela), você poderá formatar explicitamente as classes secundárias no arquivo de tema, assim como pode ser feito com as classes primárias.

### <a name="setting-visual-property-defaults-visualstyles"></a>Definir padrões de propriedade visual (`visualStyles`)

Por fim, para criar um arquivo JSON em um formato estendido, com um controle granular e mais detalhado sobre toda a formatação de visual em um relatório, adicione uma seção **visualStyles** ao arquivo JSON para aninhar as formatações específicas. Veja um exemplo modelado da seção **visualStyles**:

```json
    "visualStyles": {
        "<visualName>": {
            "<styleName>": {
                "<cardName>": [{
                    "<propertyName>": <propertyValue>
                }]
            }
        }
    }
```

Para as seções **visualName** e **cardName**, use um visual e nome de cartão específicos. No momento, **styleName** é sempre um asterisco (*), porém, em uma versão futura, você poderá criar diferentes estilos para seus visuais e dar nomes a eles (semelhante ao recurso de estilo de tabela e matriz). **propertyName** é o nome da opção de formatação específica e **PropertyValue** é o valor dessa opção de formatação.

Para **visualName** e **cardName**, use um asterisco entre aspas se quiser que essa configuração seja aplicada a todos os visuais ou cartões que tiverem uma propriedade. Se você usar o asterisco para o visual e para o nome do cartão, estará aplicando uma configuração global em seu relatório, como um tamanho de fonte ou uma família de fontes específica para todo o texto em todos os visuais.

Veja um exemplo que define algumas propriedades por meio dos estilos visuais:

```json
{
   "name":"Custom Theme",
   "visualStyles":{
      "*": {
         "*": {
            "*": [{
                "wordWrap": true
            }],
            "categoryAxis": [{
                "gridlineStyle": "dotted"
            }],
            "filterCard": [
              {
                "$id": "Applied",
                "foregroundColor": {"solid": {"color": "#252423" } }
              },
              {
                "$id":"Available",
                "border": true
              }
            ]
         }
      },
      "scatterChart": {
         "*": {
            "bubbles": [{
                  "bubbleSize": -10
            }]
         }
      }
   }
}
```

Esse exemplo define as seguintes configurações:

- Ativa a quebra automática de linha em todos os lugares
- Define o estilo da linha de grade como pontilhado para todos os visuais com um eixo de categoria
- Define algumas formatações para os cartões de filtro disponíveis e aplicados (observe o formato usando "$id" para definir as diferentes versões dos cartões de filtro)
- Define o tamanho da bolha para gráficos de dispersão como -10.

> [!NOTE]
> Você só precisa especificar os elementos de formatação que quer ajustar. Os elementos de formatação não incluídos no arquivo JSON são revertidos para as configurações e os valores padrão.

### <a name="visualstyles-definition-list"></a>Lista de definições `visualStyles`

As tabelas nesta seção definem os nomes de visual (**visualName**), os nomes de cartão (**cardName**), os nomes de propriedade (**propertyName**) e as enumerações necessárias para a criação do seu arquivo JSON.

| valores de visualName |
| --- |
| areaChart |
| barChart |
| basicShape |
| cartão |
| clusteredBarChart |
| clusteredColumnChart |
| columnChart |
| comboChart |
| donutChart |
| filledMap |
| funil |
| medidor |
| hundredPercentStackedBarChart |
| hundredPercentStackedColumnChart |
| imagem |
| kpi |
| lineChart |
| lineClusteredColumnComboChart |
| lineStackedColumnComboChart |
| mapa |
| multiRowCard |
| pieChart |
| pivotTable |
| ribbonChart |
| scatterChart |
| shapeMap |
| segmentação de dados |
| stackedAreaChart |
| tableEx |
| mapa de árvore |
| waterfallChart |

A tabela a seguir define os valores de **cardName**. O primeiro valor em cada célula é o termo do arquivo JSON. O segundo valor é o nome do cartão como visto na interface do usuário do Power BI Desktop.

| valores de cardName |
| --- |
| axis: Eixo do medidor |
| breakdown: Divisão |
| bubbles: Bolhas |
| calloutValue: Valor do Balão |
| card: Cartão |
| cardTitle: Título do cartão |
| categoryAxis: Eixo X |
| categoryLabels: Rótulos da categoria |
| columnFormatting: Formatação de campo |
| columnHeaders: Cabeçalhos da coluna |
| dataLabels: Rótulos de dados |
| fill: Preencher |
| fillPoint: Ponto de preenchimento |
| forecast: Previsão |
| general: Geral |
| goals: Metas |
| grid: Grade |
| header: Cabeçalho |
| imageScaling: Dimensionando |
| indicator: Indicador |
| items: Itens |
| labels: Rótulos de dados |
| legend: Legenda |
| lineStyles: Formas |
| mapControls: Controles de mapa |
| mapStyles: Estilos de mapa |
| numericInputStyle: Entradas numéricas |
| percentBarLabel: Etiqueta de taxa de conversão |
| plotArea: Área de Plotagem |
| plotAreaShading: Sombreamento de simetria |
| ratioLine: Linha de proporção |
| referenceLine: Linha Constante |
| ribbonChart: Faixas de opções |
| rotation: Rotação |
| rowHeaders: Cabeçalhos da linha |
| selection: Controles de Seleção |
| sentimentColors: Cores de sentimentos |
| shape: Forma |
| slider: Controle deslizante |
| status: Codificação de cores |
| subTotals: Subtotais |
| target: Destino |
| total: Total geral |
| trend: Linha de Tendência |
| trendline: Eixo da tendência |
| valueAxis: Eixo Y |
| values: Valores |
| wordWrap: Quebra automática de linha |
| xAxisReferenceLine: Linha constante do eixo X |
| y1AxisReferenceLine: Linha Constante |
| zoom: Zoom |

### <a name="properties-within-each-card"></a>Propriedades dentro de cada cartão

A seção a seguir define as propriedades em cada cartão. O nome do cartão é seguido pelo nome de cada propriedade. Para cada propriedade: o nome que você verá se o painel de formatação for exibido, uma descrição do que a opção de formatação faz e o tipo da opção de formatação. Essa abordagem permite que você saiba que tipo de valores pode usar em seu arquivo de tema.

Ao usar **dateTime**, a data deve ser uma data ISO entre aspas simples, com o datetime no início. Consulte o seguinte exemplo:

  "datetime'2011-10-05T14:48:00.000Z'"

Os boolianos são true ou false. As cadeias de caracteres devem estar entre aspas duplas, como em “esta é uma cadeia de caracteres”. Os números são apenas o próprio valor, sem aspas.

As cores usam o seguinte formato, em que o código hexadecimal personalizado substitui "FFFFFF" neste exemplo:

    { "solid": { "color": "#FFFFFF" } }

Uma enumeração, normalmente usada para opções de formatação de menu suspenso, indica que ela pode ser definida para qualquer uma das opções vistas no painel, por exemplo, "RightCenter" para posição da legenda ou "Valor dos dados, percentual do total" para rótulo de dados de pizza. As opções de enumeração são mostradas abaixo da lista de propriedades.

```json
{
      "general":{
        "responsive": {
          "type": [
            "bool"
          ],
          "displayName": [
            "(Preview) Responsive"
          ],
          "description": [
            "The visual will adapt to size changes"
          ]
        },
        "legend": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "position": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Select the location for the legend"
          ]
        },
        "showTitle": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Title"
          ],
          "description": [
            "Display a title for legend symbols"
          ]
        },
        "labelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        }
      },
      "categoryAxis": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "axisScale": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Scale type"
          ]
        },
        "start": {
          "type": [
            "numeric",
            "dateTime"
          ],
          "displayName": [
            "Start"
          ],
          "description": [
            "Enter a starting value (optional)"
          ]
        },
        "end": {
          "type": [
            "numeric",
            "dateTime"
          ],
          "displayName": [
            "End"
          ],
          "description": [
            "Enter an ending value (optional)"
          ]
        },
        "axisType": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Type"
          ]
        },
        "showAxisTitle": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Title"
          ],
          "description": [
            "Title for the X-axis",
            "Title for the Y-axis"
          ]
        },
        "axisStyle": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Style"
          ]
        },
        "labelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "labelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "labelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        },
        "concatenateLabels": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Concatenate labels"
          ],
          "description": [
            "Always concatenate levels of the hierarchy instead of drawing the hierarchy."
          ]
        },
        "preferredCategoryWidth": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Minimum category width"
          ]
        },
        "titleColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Title color"
          ]
        },
        "titleFontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "titleFontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Title text size"
          ]
        },
        "position": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Select left or right"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "duration": {
          "type": [
            "numeric"
          ]
        }
      },
      "valueAxis": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "position": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Select left or right"
          ]
        },
        "axisScale": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Scale type"
          ]
        },
        "start": {
          "type": [
            "numeric",
            "dateTime"
          ],
          "displayName": [
            "Start"
          ],
          "description": [
            "Enter a starting value (optional)"
          ]
        },
        "end": {
          "type": [
            "numeric",
            "dateTime"
          ],
          "displayName": [
            "End"
          ],
          "description": [
            "Enter an ending value (optional)"
          ]
        },
        "showAxisTitle": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Title"
          ],
          "description": [
            "Title for the Y-axis",
            "Title for the X-axis"
          ]
        },
        "axisStyle": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Style"
          ]
        },
        "labelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "labelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "labelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        },
        "titleColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Title color"
          ]
        },
        "titleFontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "titleFontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Title text size"
          ]
        },
        "axisLabel": {
          "type": [
            "none"
          ],
          "displayName": [
            "Y-Axis (Column)"
          ]
        },
        "secShow": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show secondary"
          ]
        },
        "alignZeros": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Align zeros"
          ],
          "description": [
            "Align the zero tick marks for both value axes"
          ]
        },
        "secAxisLabel": {
          "type": [
            "none"
          ],
          "displayName": [
            "Y-Axis (Line)"
          ]
        },
        "secPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Select left or right"
          ]
        },
        "secAxisScale": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Scale type"
          ]
        },
        "secStart": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Start"
          ],
          "description": [
            "Enter a starting value (optional)"
          ]
        },
        "secEnd": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "End"
          ],
          "description": [
            "Enter an ending value (optional)"
          ]
        },
        "secShowAxisTitle": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Title"
          ],
          "description": [
            "Title for the Y-axis"
          ]
        },
        "secAxisStyle": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Style"
          ]
        },
        "secLabelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ]
        },
        "secFontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "secFontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "secLabelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "secLabelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        },
        "secTitleColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Title color"
          ]
        },
        "secTitleFontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "secTitleFontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Title text size"
          ]
        }
      },
      "dataPoint": {
        "defaultColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Default color",
            "Default Column Color"
          ]
        },
        "fill": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Fill"
          ]
        },
        "defaultCategoryColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Default color",
            "Default Column Color"
          ]
        },
        "showAllDataPoints": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show all"
          ]
        }
      },
      "labels": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "showSeries": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "labelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "labelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        },
        "showAll": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Customize series"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "labelDensity": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Label density"
          ]
        },
        "labelOrientation": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Orientation"
          ]
        },
        "labelPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ]
        },
        "percentageLabelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "% decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the percentages"
          ]
        },
        "labelStyle": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Label style"
          ]
        }
      },
      "lineStyles": {
        "strokeWidth": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Stroke width"
          ]
        },
        "strokeLineJoin": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Join type"
          ]
        },
        "lineStyle": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Line style"
          ]
        },
        "showMarker": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show marker"
          ]
        },
        "markerShape": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Marker shape"
          ]
        },
        "markerSize": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Marker size"
          ]
        },
        "markerColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Marker color"
          ]
        },
        "showSeries": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Customize series",
            "Show"
          ]
        },
        "shadeArea": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Shade area"
          ]
        }
      },
      "plotArea": {
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for background color"
          ]
        }
      },
      "trend": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "displayName": {
          "type": [
            "text"
          ],
          "displayName": [
            "Name"
          ],
          "description": [
            "Set trend line name"
          ]
        },
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set trend line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for trend line color"
          ]
        },
        "style": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Style"
          ],
          "description": [
            "Set trend line style"
          ]
        },
        "combineSeries": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Combine Series"
          ],
          "description": [
            "Show one trend line per series or combine"
          ]
        }
      },
      "y1AxisReferenceLine": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "value": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value"
          ],
          "description": [
            "Set reference line numeric value"
          ]
        },
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set reference line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for reference line color"
          ]
        },
        "style": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Line style"
          ]
        },
        "position": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Arrange relative to chart data points"
          ]
        },
        "dataLabelShow": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Data label"
          ],
          "description": [
            "Display a data label for the reference line"
          ]
        },
        "dataLabelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set the reference line data label color"
          ]
        },
        "dataLabelDecimalPoints": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Decimal Places"
          ]
        },
        "dataLabelHorizontalPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Horizontal Position"
          ],
          "description": [
            "Set the horizontal position for the reference line data label"
          ]
        },
        "dataLabelVerticalPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Vertical Position"
          ],
          "description": [
            "Set the vertical position for the reference line data label"
          ]
        },
        "dataLabelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        }
      },
      "referenceLine": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "displayName": {
          "type": [
            "text"
          ],
          "displayName": [
            "Name"
          ],
          "description": [
            "Set reference line name"
          ]
        },
        "value": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value"
          ],
          "description": [
            "Set reference line numeric value"
          ]
        },
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set reference line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for reference line color"
          ]
        },
        "style": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Line style"
          ]
        },
        "position": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Arrange relative to chart data points"
          ]
        },
        "dataLabelShow": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Data label"
          ],
          "description": [
            "Display a data label for the reference line"
          ]
        },
        "dataLabelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set the reference line data label color"
          ]
        },
        "dataLabelDecimalPoints": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Decimal Places"
          ]
        },
        "dataLabelHorizontalPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Horizontal Position"
          ],
          "description": [
            "Set the horizontal position for the reference line data label"
          ]
        },
        "dataLabelVerticalPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Vertical Position"
          ],
          "description": [
            "Set the vertical position for the reference line data label"
          ]
        },
        "dataLabelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        }
      },
      "line": {
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for background color"
          ]
        },
        "weight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Weight"
          ]
        },
        "roundEdge": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Round edges"
          ]
        }
      },
      "fill": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "fillColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Fill color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for background color"
          ]
        }
      },
      "rotation": {
        "angle": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Rotation"
          ]
        }
      },
      "categoryLabels": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "wordWrap": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        }
      },
      "dataLabels": {
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "cardTitle": {
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "card": {
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "outlineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Outline color"
          ],
          "description": [
            "Color of the outline"
          ]
        },
        "outlineWeight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Outline weight"
          ],
          "description": [
            "Thickness of the outline in pixels"
          ]
        },
        "barShow": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show bar"
          ],
          "description": [
            "Display a bar to the left side of the card as an accent"
          ]
        },
        "barColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Bar color"
          ]
        },
        "barWeight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Bar thickness"
          ],
          "description": [
            "Thickness of the bar in pixels"
          ]
        },
        "cardPadding": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Padding"
          ],
          "description": [
            "Background"
          ]
        },
        "cardBackground": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background"
          ]
        }
      },
      "percentBarLabel": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "axis": {
        "min": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Min"
          ]
        },
        "max": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Max"
          ]
        },
        "target": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Target"
          ]
        }
      },
      "target": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "labelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "labelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "calloutValue": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Select color for data labels"
          ]
        },
        "labelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "labelPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        }
      },
      "forecast": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "displayName": {
          "type": [
            "text"
          ],
          "displayName": [
            "Name"
          ],
          "description": [
            "Set forecast name"
          ]
        },
        "confidenceBandStyle": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Confidence band style"
          ],
          "description": [
            "Set forecast confidence band style"
          ]
        },
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set forecast line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for background color"
          ]
        },
        "style": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Line style"
          ]
        },
        "transform": {
          "type": [
            "queryTransform"
          ]
        }
      },
      "bubbles": {
        "bubbleSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Size"
          ]
        }
      },
      "mapControls": {
        "autoZoom": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Auto zoom"
          ]
        },
        "zoomLevel": {
          "type": [
            "numeric"
          ]
        },
        "centerLatitude": {
          "type": [
            "numeric"
          ]
        },
        "centerLongitude": {
          "type": [
            "numeric"
          ]
        }
      },
      "mapStyles": {
        "mapTheme": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Theme"
          ]
        }
      },
      "shape": {
        "map": {
          "type": [
            "geoJson"
          ]
        },
        "projectionEnum": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Projection"
          ],
          "description": [
            "Projection"
          ]
        }
      },
      "zoom": {
        "autoZoom": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Auto zoom"
          ],
          "description": [
            "Zoom in on shapes with available data"
          ]
        },
        "selectionZoom": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Selection zoom"
          ],
          "description": [
            "Zoom in on selected shapes"
          ]
        },
        "manualZoom": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Manual zoom"
          ],
          "description": [
            "Allow user to zoom and pan"
          ]
        }
      },
      "xAxisReferenceLine": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "value": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value"
          ],
          "description": [
            "Set reference line numeric value"
          ]
        },
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set reference line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for reference line color"
          ]
        },
        "style": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Line style"
          ]
        },
        "position": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Position"
          ],
          "description": [
            "Arrange relative to chart data points"
          ]
        },
        "dataLabelShow": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Data label"
          ],
          "description": [
            "Display a data label for the reference line"
          ]
        },
        "dataLabelColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set the reference line data label color"
          ]
        },
        "dataLabelDecimalPoints": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Decimal Places"
          ]
        },
        "dataLabelHorizontalPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Horizontal Position"
          ],
          "description": [
            "Set the horizontal position for the reference line data label"
          ]
        },
        "dataLabelVerticalPosition": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Vertical Position"
          ],
          "description": [
            "Set the vertical position for the reference line data label"
          ]
        },
        "dataLabelDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        }
      },
      "fillPoint": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        }
      },
      "colorByCategory": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        }
      },
      "plotAreaShading": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "upperShadingColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Upper shading"
          ],
          "description": [
            "Shading color of the upper region"
          ]
        },
        "lowerShadingColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Lower shading"
          ],
          "description": [
            "Shading color of the lower region"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for background color"
          ]
        }
      },
      "ratioLine": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "lineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ],
          "description": [
            "Set reference line color"
          ]
        },
        "transparency": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Transparency"
          ],
          "description": [
            "Set transparency for line color"
          ]
        },
        "style": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Line style"
          ]
        }
      },
      "grid": {
        "outlineColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Outline color"
          ],
          "description": [
            "Color of the outline"
          ]
        },
        "outlineWeight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Outline weight"
          ],
          "description": [
            "Thickness of the outline in pixels"
          ]
        },
        "gridVertical": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Vert grid"
          ],
          "description": [
            "Show/Hide the vertical gridlines"
          ]
        },
        "gridVerticalColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Vert grid color"
          ],
          "description": [
            "Color for the vertical gridlines"
          ]
        },
        "gridVerticalWeight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Vert grid thickness"
          ],
          "description": [
            "Thickness of the vertical gridlines in pixels"
          ]
        },
        "gridHorizontal": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Horiz grid"
          ],
          "description": [
            "Show/Hide the horizontal gridlines"
          ]
        },
        "gridHorizontalColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Horiz grid color"
          ],
          "description": [
            "Color for the horizontal gridlines"
          ]
        },
        "gridHorizontalWeight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Horiz grid thickness"
          ],
          "description": [
            "Thickness of the horizontal gridlines in pixels"
          ]
        },
        "rowPadding": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Row padding"
          ],
          "description": [
            "Padding in pixels applied to top and bottom of every row"
          ]
        },
        "imageHeight": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Image height"
          ],
          "description": [
            "The height of images in pixels"
          ]
        },
        "textSize": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Text Size"
          ]
        }
      },
      "columnHeaders": {
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "backColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background color"
          ],
          "description": [
            "Background color of the cells"
          ]
        },
        "wordWrap": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Word wrap"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "autoSizeColumnWidth": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Auto-size column width"
          ]
        },
        "urlIcon": {
          "type": [
            "bool"
          ],
          "displayName": [
            "URL icon"
          ],
          "description": [
            "Show an icon instead of the full URL"
          ]
        }
      },
      "values": {
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "backColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color scales"
          ]
        },
        "fontColorPrimary": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the odd rows"
          ]
        },
        "backColorPrimary": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background color"
          ],
          "description": [
            "Background color of the odd rows"
          ]
        },
        "fontColorSecondary": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Alternate font color"
          ],
          "description": [
            "Font color of the even rows"
          ]
        },
        "backColorSecondary": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Alternate background color"
          ],
          "description": [
            "Background color of the even rows"
          ]
        },
        "urlIcon": {
          "type": [
            "bool"
          ],
          "displayName": [
            "URL icon"
          ],
          "description": [
            "Show an icon instead of the full URL"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "wordWrap": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Word wrap"
          ]
        },
        "bandedRowHeaders": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Banded row style"
          ],
          "description": [
            "Apply banded row style to the last level of the row group headers, using the colors of the values."
          ]
        },
        "valuesOnRow": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show on rows"
          ],
          "description": [
            "Show values in row groups rather than columns"
          ]
        }
      },
      "total": {
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "backColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background color"
          ],
          "description": [
            "Background color of the cells"
          ]
        },
        "applyToHeaders": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Apply to labels"
          ]
        },
        "totals": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Totals"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        }
      },
      "columnFormatting": {
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "backColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background color"
          ],
          "description": [
            "Background color of the cells"
          ]
        },
        "styleHeader": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Color header"
          ]
        },
        "styleValues": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Color values"
          ]
        },
        "styleTotal": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Color total"
          ]
        },
        "styleSubtotals": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Color subtotals"
          ]
        }
      },
      "rowHeaders": {
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "backColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background color"
          ],
          "description": [
            "Background color of the cells"
          ]
        },
        "wordWrap": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Word wrap"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "stepped": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Stepped layout"
          ],
          "description": [
            "Render row headers with stepped layout"
          ]
        },
        "steppedLayoutIndentation": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Stepped layout indentation"
          ],
          "description": [
            "Set the indentation, in pixels, applied to row headers"
          ]
        },
        "urlIcon": {
          "type": [
            "bool"
          ],
          "displayName": [
            "URL icon"
          ],
          "description": [
            "Show an icon instead of the full URL"
          ]
        }
      },
      "subTotals": {
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "backColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background color"
          ],
          "description": [
            "Background color of the cells"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "fontSize": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "rowSubtotals": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Total row"
          ]
        },
        "columnSubtotals": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Total column"
          ]
        },
        "applyToHeaders": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Apply to labels"
          ]
        }
      },
      "selection": {
        "selectAllCheckboxEnabled": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Select All"
          ]
        },
        "singleSelect": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Single Select"
          ]
        }
      },
      "header": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "background": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background"
          ]
        },
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "textSize": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "items": {
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "background": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background"
          ]
        },
        "outline": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Outline"
          ]
        },
        "textSize": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        }
      },
      "numericInputStyle": {
        "fontColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Font color"
          ],
          "description": [
            "Font color of the cells"
          ]
        },
        "textSize": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Text Size"
          ]
        },
        "fontFamily": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Font family"
          ]
        },
        "background": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Background"
          ]
        }
      },
      "slider": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        },
        "color": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Color"
          ]
        }
      },
      "dateRange": {
        "includeToday": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Include today"
          ]
        }
      },
      "sentimentColors": {
        "increaseFill": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Increase"
          ]
        },
        "decreaseFill": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Decrease"
          ]
        },
        "totalFill": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Total"
          ]
        },
        "otherFill": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Other"
          ]
        }
      },
      "breakdown": {
        "maxBreakdowns": {
          "type": [
            "integer"
          ],
          "displayName": [
            "Max breakdowns"
          ],
          "description": [
            "The number of individual breakdowns to show (rest grouped into Other)"
          ]
        }
      },
      "indicator": {
        "indicatorDisplayUnits": {
          "type": [
            "formatting"
          ],
          "displayName": [
            "Display units"
          ],
          "description": [
            "Select the units (millions, billions, etc.)"
          ]
        },
        "indicatorPrecision": {
          "type": [
            "numeric"
          ],
          "displayName": [
            "Value decimal places"
          ],
          "description": [
            "Select the number of decimal places to display for the values"
          ]
        },
        "kpiFormat": {
          "type": [
            "text"
          ],
          "displayName": [
            "Format"
          ]
        }
      },
      "trendline": {
        "show": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Show"
          ]
        }
      },
      "goals": {
        "showGoal": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Goal"
          ]
        },
        "showDistance": {
          "type": [
            "bool"
          ],
          "displayName": [
            "Distance"
          ]
        }
      },
      "status": {
        "direction": {
          "type": [
            "enumeration"
          ],
          "displayName": [
            "Direction"
          ]
        },
        "goodColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Good Color"
          ]
        },
        "neutralColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Neutral Color"
          ]
        },
        "badColor": {
          "type": [
            "fill"
          ],
          "displayName": [
            "Bad Color"
          ]
        }
      }
```



### <a name="enumerations-in-the-json-file"></a>Enumerações no arquivo JSON
A seção a seguir define as enumerações que podem ser usadas no arquivo JSON.

```json
    {
        "legend": {
            "position": [
                {
                    "value": "Top",
                    "displayName": "Top"
                },
                {
                    "value": "Bottom",
                    "displayName": "Bottom"
                },
                {
                    "value": "Left",
                    "displayName": "Left"
                },
                {
                    "value": "Right",
                    "displayName": "Right"
                },
                {
                    "value": "TopCenter",
                    "displayName": "Top Center"
                },
                {
                    "value": "BottomCenter",
                    "displayName": "Bottom Center"
                },
                {
                    "value": "LeftCenter",
                    "displayName": "Left Center"
                },
                {
                    "value": "RightCenter",
                    "displayName": "Right center"
                }
            ],
            "legendMarkerRendering": [
                {
                    "value": "markerOnly",
                    "displayName": "Markers only"
                },
                {
                    "value": "lineAndMarker",
                    "displayName": "Line and markers"
                },
                {
                    "value": "lineOnly",
                    "displayName": "Line only"
                }
            ]
        },
        "categoryAxis": {
            "axisScale": [
                {
                    "value": "linear",
                    "displayName": "Linear"
                },
                {
                    "value": "log",
                    "displayName": "Log"
                }
            ],
            "axisType": [
                {
                    "value": "Scalar",
                    "displayName": "Continuous"
                },
                {
                    "value": "Categorical",
                    "displayName": "Categorical"
                }
            ],
            "axisStyle": [
                {
                    "value": "showTitleOnly",
                    "displayName": "Show title only"
                },
                {
                    "value": "showUnitOnly",
                    "displayName": "Show unit only"
                },
                {
                    "value": "showBoth",
                    "displayName": "Show both"
                }
            ],
            "gridlineStyle": [
                {
                    "value": "dashed",
                    "displayName": "Dashed"
                },
                {
                    "value": "solid",
                    "displayName": "Solid"
                },
                {
                    "value": "dotted",
                    "displayName": "Dotted"
                }
            ],
            "position": [
                {
                    "value": "Left",
                    "displayName": "Left"
                },
                {
                    "value": "Right",
                    "displayName": "Right"
                }
            ]
        },
        "valueAxis": {
            "position": [
                {
                    "value": "Left",
                    "displayName": "Left"
                },
                {
                    "value": "Right",
                    "displayName": "Right"
                }
            ],
            "axisScale": [
                {
                    "value": "linear",
                    "displayName": "Linear"
                },
                {
                    "value": "log",
                    "displayName": "Log"
                }
            ],
            "axisStyle": [
                {
                    "value": "showTitleOnly",
                    "displayName": "Show title only"
                },
                {
                    "value": "showUnitOnly",
                    "displayName": "Show unit only"
                },
                {
                    "value": "showBoth",
                    "displayName": "Show both"
                }
            ],
            "gridlineStyle": [
                {
                    "value": "dashed",
                    "displayName": "Dashed"
                },
                {
                    "value": "solid",
                    "displayName": "Solid"
                },
                {
                    "value": "dotted",
                    "displayName": "Dotted"
                }
            ],
            "secPosition": [
                {
                    "value": "Left",
                    "displayName": "Left"
                },
                {
                    "value": "Right",
                    "displayName": "Right"
                }
            ],
            "secAxisScale": [
                {
                    "value": "linear",
                    "displayName": "Linear"
                },
                {
                    "value": "log",
                    "displayName": "Log"
                }
            ],
            "secAxisStyle": [
                {
                    "value": "showTitleOnly",
                    "displayName": "Show title only"
                },
                {
                    "value": "showUnitOnly",
                    "displayName": "Show unit only"
                },
                {
                    "value": "showBoth",
                    "displayName": "Show both"
                }
            ]
        },
        "lineStyles": {
            "strokeLineJoin": [
                {
                    "value": "miter",
                    "displayName": "Miter"
                },
                {
                    "value": "round",
                    "displayName": "Round"
                },
                {
                    "value": "bevel",
                    "displayName": "Bevel"
                }
            ],
            "lineStyle": [
                {
                    "value": "dashed",
                    "displayName": "Dashed"
                },
                {
                    "value": "solid",
                    "displayName": "Solid"
                },
                {
                    "value": "dotted",
                    "displayName": "Dotted"
                }
            ],
            "markerShape": [
                {
                    "value": "circle",
                    "displayName": "●"
                },
                {
                    "value": "square",
                    "displayName": "■"
                },
                {
                    "value": "diamond",
                    "displayName": "◆"
                },
                {
                    "value": "triangle",
                    "displayName": "▲"
                },
                {
                    "value": "x",
                    "displayName": "☓"
                },
                {
                    "value": "shortDash",
                    "displayName": " -"
                },
                {
                    "value": "longDash",
                    "displayName": "—"
                },
                {
                    "value": "plus",
                    "displayName": "+"
                }
            ]
        },
        "trend": {
            "style": [
                {
                    "value": "dashed",
                    "displayName": "Dashed"
                },
                {
                    "value": "solid",
                    "displayName": "Solid"
                },
                {
                    "value": "dotted",
                    "displayName": "Dotted"
            }
        ]
    },
    "y1AxisReferenceLine": {
        "style": [
            {
                "value": "dashed",
                "displayName": "Dashed"
            },
            {
                "value": "solid",
                "displayName": "Solid"
            },
            {
                "value": "dotted",
                "displayName": "Dotted"
            }
        ],
        "position": [
            {
                "value": "back",
                "displayName": "Behind"
            },
            {
                "value": "front",
                "displayName": "In Front"
            }
        ],
        "dataLabelText": [
            {
                "value": "Value",
                "displayName": "Value"
            },
            {
                "value": "Name",
                "displayName": "Name"
            },
            {
                "value": "ValueAndName",
                "displayName": "Name and Value"
            }
        ],
        "dataLabelHorizontalPosition": [
            {
                "value": "left",
                "displayName": "Left"
            },
            {
                "value": "right",
                "displayName": "Right"
            }
        ],
        "dataLabelVerticalPosition": [
            {
                "value": "above",
                "displayName": "Above"
            },
            {
                "value": "under",
                "displayName": "Under"
            }
        ]
    },
    "referenceLine": {
        "style": [
            {
                "value": "dashed",
                "displayName": "Dashed"
            },
            {
                "value": "solid",
                "displayName": "Solid"
            },
            {
                "value": "dotted",
                "displayName": "Dotted"
            }
        ],
        "position": [
            {
                "value": "back",
                "displayName": "Behind"
            },
            {
                "value": "front",
                "displayName": "In Front"
            }
        ],
        "dataLabelText": [
      {
        "value": "Value",
        "displayName": "Value"
      },
      {
        "value": "Name",
        "displayName": "Name"
      },
      {
        "value": "ValueAndName",
        "displayName": "Name and Value"
      }
    ],
    "dataLabelHorizontalPosition": [
      {
        "value": "left",
        "displayName": "Left"
      },
      {
        "value": "right",
        "displayName": "Right"
      }
    ],
    "dataLabelVerticalPosition": [
      {
        "value": "above",
        "displayName": "Above"
      },
      {
        "value": "under",
        "displayName": "Under"
      }
    ]
    },
    "labels": {
    "labelOrientation": [
      {
        "value": "vertical",
        "displayName": "Vertical"
      },
      {
        "value": "horizontal",
        "displayName": "Horizontal"
      }
    ],
    "labelPosition": [
      {
        "value": "Auto",
        "displayName": "Auto"
      },
      {
        "value": "InsideEnd",
        "displayName": "Inside End"
      },
      {
        "value": "OutsideEnd",
        "displayName": "Outside End"
      },
      {
        "value": "InsideCenter",
        "displayName": "Inside Center"
      },
      {
        "value": "InsideBase",
        "displayName": "Inside Base"
      }
    ],
    "labelStyle": [
      {
        "value": "Category",
        "displayName": "Category"
      },
      {
        "value": "Data",
        "displayName": "Data value"
      },
      {
        "value": "Percent of total",
        "displayName": "Percent of total"
      },
      {
        "value": "Both",
        "displayName": "Category, data value"
      },
      {
        "value": "Category, percent of total",
        "displayName": "Category, percent of total"
      },
      {
        "value": "Data value, percent of total",
        "displayName": "Data value, percent of total"
      },
      {
        "value": "Category, data value, percent of total",
        "displayName": "All detail labels"
      }
     ]
    },
    "card": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
         ]
    },
    "imageScaling": {
        "imageScalingType": [
          {
            "value": "Normal",
            "displayName": "Normal"
          },
          {
            "value": "Fit",
            "displayName": "Fit"
          },
          {
            "value": "Fill",
            "displayName": "Fill"
          }
        ]
    },
    "forecast": {
        "confidenceBandStyle": [
          {
            "value": "fill",
            "displayName": "Fill"
          },
          {
            "value": "line",
            "displayName": "Line"
          },
          {
            "value": "none",
            "displayName": "None"
          }
        ],
        "style": [
          {
            "value": "dashed",
            "displayName": "Dashed"
          },
          {
            "value": "solid",
            "displayName": "Solid"
          },
          {
            "value": "dotted",
            "displayName": "Dotted"
          }
        ]
        },
        "mapStyles": {
        "mapTheme": [
          {
            "value": "aerial",
            "displayName": "Aerial"
          },
          {
            "value": "canvasDark",
            "displayName": "Dark"
          },
          {
            "value": "canvasLight",
            "displayName": "Light"
          },
          {
            "value": "grayscale",
            "displayName": "Grayscale"
          },
          {
            "value": "road",
            "displayName": "Road"
          }
        ]
    },
    "shape": {
        "projectionEnum": [
          {
            "value": "albersUsa",
            "displayName": "Albers USA"
          },
          {
            "value": "equirectangular",
            "displayName": "Equirectangular"
          },
          {
            "value": "mercator",
            "displayName": "Mercator"
          },
          {
            "value": "orthographic",
            "displayName": "Orthographic"
          }
        ]
        },
        "xAxisReferenceLine": {
        "style": [
          {
            "value": "dashed",
            "displayName": "Dashed"
          },
          {
            "value": "solid",
            "displayName": "Solid"
          },
          {
            "value": "dotted",
            "displayName": "Dotted"
          }
        ],
        "position": [
          {
            "value": "back",
            "displayName": "Behind"
          },
          {
            "value": "front",
            "displayName": "In Front"
          }
        ],
        "dataLabelText": [
          {
            "value": "Value",
            "displayName": "Value"
          },
          {
            "value": "Name",
            "displayName": "Name"
          },
          {
            "value": "ValueAndName",
            "displayName": "Name and Value"
          }
        ],
        "dataLabelHorizontalPosition": [
          {
            "value": "left",
            "displayName": "Left"
          },
          {
            "value": "right",
            "displayName": "Right"
          }
        ],
        "dataLabelVerticalPosition": [
          {
            "value": "above",
            "displayName": "Above"
          },
          {
            "value": "under",
            "displayName": "Under"
          }
        ]
        },
        "ratioLine": {
        "style": [
          {
            "value": "dashed",
            "displayName": "Dashed"
          },
          {
            "value": "solid",
            "displayName": "Solid"
          },
          {
            "value": "dotted",
            "displayName": "Dotted"
          }
        ]
        },
        "columnHeaders": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ]
        },
        "values": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ]
        },
        "total": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ]
        },
        "rowHeaders": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ]
        },
        "subTotals": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ],
        "rowSubtotalsPosition": [
          {
            "value": "Top",
            "displayName": "Top"
          },
          {
            "value": "Bottom",
            "displayName": "Bottom"
          }
        ]
        },
        "general": {
        "orientation": [
          {
            "value": "vertical",
            "displayName": "Vertical"
          },
          {
            "value": "horizontal",
            "displayName": "Horizontal"
          }
        ]
        },
        "data": {
        "relativeRange": [
          {
            "value": "Last",
            "displayName": "Last"
          },
          {
            "value": "Next",
            "displayName": "Next"
          },
          {
            "value": "This",
            "displayName": "This"
          }
        ],
        "relativePeriod": [
          {
            "value": "None",
            "displayName": "Select"
          },
          {
            "value": "Days",
            "displayName": "Days"
          },
          {
            "value": "Weeks",
            "displayName": "Weeks"
          },
          {
            "value": "Calendar Weeks",
            "displayName": "Weeks (Calendar)"
          },
          {
            "value": "Months",
            "displayName": "Months"
          },
          {
            "value": "Calendar Months",
            "displayName": "Months (Calendar)"
          },
          {
            "value": "Years",
            "displayName": "Years"
          },
          {
            "value": "Calendar Years",
            "displayName": "Years (Calendar)"
          }
        ],
        "mode": [
          {
            "value": "Between",
            "displayName": "Between"
          },
          {
            "value": "Before",
            "displayName": "Before"
          },
          {
            "value": "After",
            "displayName": "After"
          },
          {
            "value": "Basic",
            "displayName": "List"
          },
          {
            "value": "Dropdown",
            "displayName": "Dropdown"
          },
          {
            "value": "Relative",
            "displayName": "Relative"
          },
          {
            "value": "Single",
            "displayName": "Single Value"
          }
        ]
        },
        "header": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ]
        },
        "items": {
        "outline": [
          {
            "value": "None",
            "displayName": "None"
          },
          {
            "value": "BottomOnly",
            "displayName": "Bottom only"
          },
          {
            "value": "TopOnly",
            "displayName": "Top only"
          },
          {
            "value": "LeftOnly",
            "displayName": "Left only"
          },
          {
            "value": "RightOnly",
            "displayName": "Right only"
          },
          {
            "value": "TopBottom",
            "displayName": "Top + bottom"
          },
          {
            "value": "LeftRight",
            "displayName": "Left + right"
          },
          {
            "value": "Frame",
            "displayName": "Frame"
          }
        ]
        },
        "status": {
        "direction": [
          {
            "value": "Positive",
            "displayName": "High is good"
          },
          {
            "value": "Negative",
            "displayName": "Low is good"
          }
         ]
       }
    }
  }
}
```

## <a name="limitations-and-considerations"></a>Limitações e considerações

Se você estiver usando um de nossos temas originais, o tema "Clássico" ou um tema personalizado que você importou sobre um deles, a seção texto da caixa de diálogo do tema não estará disponível para configuração.

Os temas internos afetados por essa limitação incluem os seguintes temas:
* Clássico
* Parque urbano
* Sala de aula
* Adequado para daltônicos
* Elétrico
* Alto contraste
* Pôr do sol
* Crepúsculo

Se você estiver usando um dos temas afetados e não precisar modificar as configurações de texto, poderá usar com segurança as outras guias da caixa de diálogo sem problemas. No entanto, se desejar usar as classes de texto com um dos temas afetados, terá algumas opções:

- A maneira mais rápida e fácil de habilitar as classes de texto é selecionar as opções de tema Padrão.
- Se quiser manter seu tema personalizado atual, para habilitar a guia de texto:
  1. Exporte seu tema atual.
  1. Selecione o tema padrão.
  1. Importe o tema personalizado que você exportou na primeira etapa.

O texto em seu relatório terá uma aparência diferente, mas você poderá acessar a guia de texto na caixa de diálogo do tema.


