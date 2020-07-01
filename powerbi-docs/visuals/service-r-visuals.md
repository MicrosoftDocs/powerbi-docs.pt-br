---
title: Criar visualizações e análises avançadas usando scripts do R
description: Usar scripts do R no Power BI Desktop para criar visualizações e análise avançadas
author: mihart
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 11/14/2019
ms.author: rien
LocalizationGroup: Visualizations
ms.openlocfilehash: 91ca05a144166abbc903d42ba30a5c70b839987d
ms.sourcegitcommit: e8b12d97076c1387088841c3404eb7478be9155c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "85782818"
---
# <a name="create-and-use-r-visuals-in-power-bi"></a>Criar e usar visuais do R no Power BI

[!INCLUDE[consumer-appliesto-nnyn](../includes/consumer-appliesto-nnyn.md)]

Atualmente, os visuais do R só podem ser criados no **Power BI Desktop** e, em seguida, publicados no serviço do Power BI. Para obter mais informações sobre como criar visuais do R, confira [Criar visuais do Power BI usando o R](../create-reports/desktop-r-visuals.md).

## <a name="viewing-r-visuals-in-the-power-bi-service"></a>Exibição de visuais do R no serviço do Power BI
O serviço do Power BI dá suporte à exibição e interação com visuais criados com scripts do R. Os visuais criados com scripts do R, normalmente chamados de *visuais do R*, podem apresentar formatação e análise de dados avançadas, como previsão, usando o poder da análise e da visualização avançadas do R.

> [!NOTE]
> A [linguagem de programação R](https://www.r-project.org/) está entre as linguagens de programação mais amplamente usadas por estatísticos, cientistas de dados e analistas de negócios. A linguagem R conta com uma comunidade de software livre que oferece mais de 7.000 pacotes de complementos, além de Grupos de Usuários do R amplamente utilizados. A versão do R implantada no serviço do Power BI é o *Microsoft R 3.4.4.*
> 
> 

A imagem a seguir mostra um dashboard do Power BI com uma coleção de visuais do R usados para análise avançada.

![Captura da tela do relatório de serviço do Power BI](media/service-r-visuals/power-bi-r-visuals.png)

Os visuais do R são criados em um [relatório do Power BI Desktop](../fundamentals/desktop-get-the-desktop.md), como o relatório mostrado na imagem a seguir.

![Relatório de desktop com dois visuais](media/service-r-visuals/power-bi-r-visual-desktop.png)

Depois que o relatório for criado no **Power BI Desktop**, será possível publicar o relatório contendo um ou mais visuais do R no serviço do Power BI. 

 No serviço, não há suporte para todos os pacotes do R. Confira os pacotes com suporte ao final deste artigo para obter a lista dos pacotes atualmente com suporte no serviço do Power BI.

Você pode baixar este [arquivo de exemplo do Power BI Desktop](https://download.microsoft.com/download/D/9/A/D9A65269-D1FC-49F8-8EC3-1217E3A4390F/RVisual_correlation_plot_sample%20SL.pbix) (arquivo .pbix) que contém alguns visuais do R para ver como isso funciona e testá-lo.

Na maioria dos casos, os visuais do R criados no **Power BI Desktop** e publicados no serviço do Power BI, se comportam como qualquer outro visual do serviço do Power BI: é possível interagir, filtrar, segmentá-los e fixá-los em um dashboard ou compartilhá-los com outras pessoas. Para obter mais informações sobre como compartilhar dashboards e visuais, veja [compartilhar um dashboard com seus colegas e com outras pessoas](../collaborate-share/service-share-dashboards.md). Uma diferença entre os visuais do R e outros visuais é que aqueles não podem mostrar dicas de ferramenta e não podem ser usados para filtrar outros visuais.

Como você pode ver na imagem a seguir, os visuais do R no serviço do Power BI, estejam eles em dashboards ou relatórios, na maioria dos casos, aparecem e se comportam como qualquer outro visual, e os usuários não precisam conhecer o script do R subjacente que criou o visual.

![captura de tela da página de relatório no serviço do Power BI](media/service-r-visuals/power-bi-r-visual.png)

## <a name="r-scripts-security"></a>Segurança de scripts do R
Os visuais do R são criados com base nos scripts do R que, potencialmente, podem conter código com riscos de segurança ou privacidade.

Esses riscos existem, principalmente, na fase de criação, quando o autor do script executa o script no próprio computador.

O serviço do Power BI aplica uma tecnologia de *área restrita* para proteger os usuários e o serviço contra riscos de segurança.

Essa abordagem de *área restrita* impõe algumas restrições sobre os scripts do R em execução no serviço do Power BI, como o acesso à Internet ou o acesso a outros recursos que não são necessários para criar o visual do R.

## <a name="r-scripts-error-experience"></a>Experiência de erro com scripts do R
Quando há um erro em um script do R, o visual do R não é plotado e uma mensagem de erro é exibida. Para obter detalhes sobre o erro, selecione **Ver detalhes** no erro do visual do R na tela, conforme mostrado na imagem a seguir.

![mensagem de erro](media/service-r-visuals/r-visuals-service-4.png)

Como outro exemplo, a imagem a seguir mostra a mensagem de erro que aparece quando um script do R não é executado corretamente devido à ausência de um pacote do R no Azure.

![Captura de tela mostrando um erro de runtime](media/service-r-visuals/r-visuals-service-5.png)

## <a name="licensing"></a>Licenciamento
Os visuais do R exigem uma licença [Power BI Pro](../fundamentals/service-self-service-signup-for-power-bi.md) para serem renderizados em relatórios, na atualização, no filtro e no filtro cruzado. Para obter mais informações sobre licenças do Power BI Pro e como elas diferem das licenças gratuitas, veja [Conteúdo do Power BI Pro – o que é isto?](../admin/service-admin-purchasing-power-bi-pro.md)

Os usuários da versão gratuita do Power BI só poderão consumir blocos compartilhados com eles nos workspaces Premium. Veja [Comprando o Power BI Pro](../admin/service-admin-purchasing-power-bi-pro.md) para obter mais informações.

A tabela a seguir descreve as funcionalidades dos visuais do R com base em licenciamento.


|  |Criar visuais do R no Power BI Desktop  | Criar relatórios de serviço PBI com visuais R |Exibir visuais R em relatórios  | Exibir blocos R em dashboards |
|---------|---------|---------|---------|--------|
|**Convidado** (Power BI Embedded)     |  Com suporte|  Sem suporte      | Compatível apenas na capacidade Premium/Azure  | Compatível apenas na capacidade Premium/Azure |
|**Locatário não gerenciado** (domínio não verificado) | Com suporte | Sem suporte |  Sem suporte |Compatível (cenário B2B) |
|**Locatário gerenciado** com licença gratuita    |  Com suporte       |  Sem suporte       |    Compatível apenas na capacidade Premium    | Com suporte |
**Locatário gerenciado** com licença Pro     |   Com suporte      | Com suporte      | Com suporte    |Com suporte|



## <a name="known-limitations"></a>Limitações Conhecidas
Os visuais do R no serviço do Power BI têm algumas limitações:

* O suporte a visuais do R é limitado aos pacotes identificados [em Saiba quais pacotes do R têm suporte](../connect-data/service-r-packages-support.md). Atualmente, não há suporte para pacotes personalizados.
* Limitações de tamanho de dados – os dados usados pelo visual R para plotar são limitados a 150.000 linhas. Se mais de 150.000 linhas forem selecionadas, somente as primeiras 150.000 linhas serão usadas e uma mensagem será exibida na imagem. Além disso, os dados de entrada têm um limite de 250 MB.
* Resolução: todos os visuais do R são exibidos com 72 dpi.
* Dispositivo de plotagem: somente a plotagem para o dispositivo padrão é compatível. 
* Limite de tempo de cálculo – se um cálculo do visual do R exceder 60 SEGUNDOS, o script atingirá o tempo limite, resultando em erro.
* Visuais R são atualizados após atualizações de dados, filtragem e realce. No entanto, a própria imagem não é interativa e não dá suporte a dicas de ferramenta.
* Visuais R respondem ao realce de outros elementos visuais, mas você não pode clicar em elementos no visual R para fazer filtragem cruzada de outros elementos.
* Atualmente, não há suporte nos visuais do R para o tipo de dados *Hora*. Em vez disso, use Data/Hora.
* Os visuais do R não são exibidos ao usar o recurso **Publicar na Web**.
* Os visuais do R não dão suporte à renomeação de colunas de entrada. As colunas serão referenciadas pelo nome original durante a execução do script.
* Atualmente, os visuais do R não são impressos com a impressão de dashboards e relatórios
* Atualmente, não há suporte para os visuais do R no modo DirectQuery do Analysis Services
* Os visuais do R podem converter rótulos de texto em elementos gráficos. Fazer isso na serviço do Power BI requer a seguinte etapa adicional:
  
  * Adicione a seguinte linha ao início do script de R:
    
```powerbi_rEnableShowText =  1```

* As fontes de chinês, japonês e coreano exigem todas as etapas adicionais a seguir para funcionar corretamente no serviço do Power BI:
  
  * Primeiro, instale o pacote de R *showtext* e todas as suas dependências. Você pode fazer isso executando o seguinte script:
    
```install.packages("showtext")```

  * Em seguida, adicione a seguinte linha no início do script de R:
    
```R script
powerbi_rEnableShowTextForCJKLanguages =  1
```

## <a name="overview-of-r-packages"></a>Visão geral de pacotes de R
Pacotes de R são coleções de funções de R, dados e código compilado combinados em um formato bem definido. Quando o R é instalado, ele vem com um conjunto padrão de pacotes e outros pacotes estão disponíveis para download e para instalação. Depois de instalado, um pacote do R deve ser carregado na sessão a ser usada. A principal origem de pacotes de R gratuitos é o CRAN, a [Rede Completa de Arquivos do R](https://cran.r-project.org/web/packages/available_packages_by_name.html).

O **Power BI Desktop** pode usar qualquer tipo de pacotes de R sem limitação. É possível instalar pacotes de R para uso no **Power BI Desktop** por conta própria (usando o [IDE RStudio](https://www.rstudio.com/), por exemplo).

Os pacotes encontrados na seção **Pacotes com suporte** encontrada **neste artigo** dão suporte aos visuais do R no [serviço do Power BI](../connect-data/service-r-packages-support.md). Se você não encontrar um pacote do seu interesse na lista de pacotes com suporte, será possível solicitar o suporte do pacote. Consulte [Pacotes do R no serviço do Power BI](../connect-data/service-r-packages-support.md) para obter informações sobre como solicitar suporte.

### <a name="requirements-and-limitations-of-r-packages"></a>Requisitos e limitações de pacotes de R
Há alguns requisitos e limitações dos pacotes de R:

* O serviço do Power BI, na sua maioria, dá suporte a pacotes de R com licenças de software gratuitas e de software livre como GPL-2, GPL-3, MIT+ e assim por diante.
* O serviço do Power BI dá suporte a pacotes publicados no CRAN. O serviço não dá suporte a pacotes de R personalizados ou privados. Recomendamos que os usuários disponibilizem seus pacotes privados no CRAN antes de solicitar que o pacote esteja disponível no serviço do Power BI.
* O **Power BI Desktop** tem duas variações para pacotes de R:
  
  * Para visuais do R, é possível instalar qualquer pacote, incluindo pacotes de R personalizados
  * Para visuais personalizados do R, há suporte somente para pacotes CRAN públicos para instalação automática dos pacotes
* Por motivos de privacidade e segurança, atualmente não damos suporte a pacotes de R que forneçam consultas de cliente-servidor por meio da World Wide Web (como RgoogleMaps) no serviço. A rede está bloqueada para essas tentativas. Consulte [Pacotes do R no serviço do Power BI](../connect-data/service-r-packages-support.md) para obter uma lista de pacotes do R com e sem suporte.
* O processo de aprovação para a inclusão de um novo pacote de R tem uma árvore de dependências; algumas delas que precisam ser instaladas no serviço não têm suporte.

### <a name="supported-packages"></a>Pacotes com suporte:
Para obter uma lista longa de pacotes do R com suporte (e a lista curta de pacotes sem suporte), consulte o seguinte artigo:

* [Pacotes do R no serviço do Power BI](../connect-data/service-r-packages-support.md)
