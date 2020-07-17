---
title: Baixar um relatório do serviço do Power BI para o Power BI Desktop (versão prévia)
description: Baixar um relatório do serviço do Power BI para um arquivo do Power BI Desktop
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 07/14/2020
ms.author: maggies
LocalizationGroup: Reports
ms.openlocfilehash: 5cd0dd3b91109e63e5481e2f5e5516fd9ecd245c
ms.sourcegitcommit: d8acf2fb0318708a3e8e1e259cb3747b0312b312
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "86385965"
---
# <a name="download-a-report-from-the-power-bi-service-to-power-bi-desktop-preview"></a>Baixar um relatório do serviço do Power BI para o Power BI Desktop (versão prévia)
      
No Power BI Desktop, você pode publicar um relatório (um arquivo *.pbix*) do seu computador local no serviço do Power BI. Os relatórios do Power BI também podem ir para a outra direção: Você pode baixar um relatório do serviço do Power BI para o Power BI Desktop. A extensão de um relatório do Power BI, em ambos os casos, é. pbix.

Há algumas limitações a serem consideradas, que são abordadas na seção na seção [Considerações e solução de problemas ](#considerations-and-troubleshooting) deste artigo.

![Lista suspensa de arquivos](media/service-export-to-pbix/power-bi-file-export.png)

## <a name="download-the-report-as-a-pbix-file"></a>Baixar o relatório como um arquivo .pbix

Você só pode baixar relatórios [criados com o Power BI Desktop](/learn/modules/publish-share-power-bi/2-publish-reports) após 23 de novembro de 2016 e atualizados desde então. Se ele foi criado antes disso, a opção de menu **Baixar relatório** no serviço do Power BI service ficará esmaecida.

Para baixar o arquivo .pbix, siga estas etapas:

1. No serviço do Power BI, abra o relatório que você deseja baixar no [Modo de exibição de edição](https://docs.microsoft.com/power-bi/service-interact-with-a-report-in-editing-view).

2. No painel de navegação superior, selecione **Arquivo > Baixar relatório**.
   
3. Enquanto o relatório está baixando, uma faixa de status exibe o progresso. Quando o arquivo estiver pronto, você será perguntado onde deseja salvar o arquivo .pbix. O nome padrão do arquivo corresponde ao título do relatório.
   
4. [Instale o Power BI Desktop](../fundamentals/desktop-get-the-desktop.md), caso ainda não tenha feito isso e abra o arquivo .pbix no Power BI Desktop.
   
    Ao abrir o relatório no Pober BI Desktop, uma mensagem de aviso pode ser exibida informando que alguns recursos disponíveis no relatório do serviço do Power BI não estão disponíveis no Power BI Desktop.
   
    ![Caixa de diálogo de aviso](media/service-export-to-pbix/power-bi-export-to-pbix_2.png)

5. O editor de relatório do no Power BI Desktop é semelhante ao editor de relatório no serviço do Power BI.  
   
    ![Editor de relatórios do Power BI Desktop](media/service-export-to-pbix/power-bi-desktop.png)

## <a name="considerations-and-troubleshooting"></a>Considerações e solução de problemas

Há algumas considerações e limitações importantes associadas ao download de um arquivo .pbix no serviço do Power BI.

* Para baixar o arquivo, você deve ter acesso de edição ao relatório.
* O relatório deve ter sido criado usando o Power BI Desktop e ter sido *publicado* no serviço do Power BI ou o .pbix deve ter sido *carregado* nele.
* Os relatórios devem ser publicados ou atualizados após 23 de novembro de 2016. Os relatórios publicados anteriormente não podem ser baixados.
* Esse recurso não funcionará com relatórios e pacotes de conteúdo criados originalmente no serviço do Power BI.
* Use sempre a última versão do Power BI Desktop ao abrir os arquivos baixados. Talvez não seja possível abrir os arquivos .pbix baixados em versões não atuais do Power BI Desktop.
* Se o administrador tiver desativado a capacidade de baixar dados, esse recurso não estará visível no serviço do Power BI.
* Conjuntos de dados com a atualização incremental não podem ser baixados para um arquivo .pbix.
* Os conjuntos de dados habilitados para [modelos grandes](../admin/service-premium-large-models.md) não podem ser baixados em um arquivo .pbix.
* Os conjuntos de dados modificados por meio do [ponto de extremidade XMLA](../admin/service-premium-connect-tools.md) não podem ser baixados em um arquivo .pbix.
* Se você criar um relatório do Power BI com base em um conjunto de dados em um workspace e publicá-lo em outro workspace, você e os usuários não poderão baixá-lo. No momento, o recurso de download não tem suporte neste cenário.

## <a name="next-steps"></a>Próximas etapas

Assista ao vídeo de um minuto **Guy in a Cube** sobre esse recurso:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ymWqU5jiUl0" frameborder="0" allowfullscreen></iframe>

Veja alguns outros artigos que podem ajudá-lo a aprender a usar o serviço do Power BI:

* [Relatórios no Power BI](../consumer/end-user-reports.md)
* [Conceitos básicos para designers no serviço do Power BI](../fundamentals/service-basic-concepts.md)

Depois que você instalar o Power BI Desktop, confira o artigo a seguir para ajudá-lo a colocá-lo em funcionamento rapidamente:

* [Introdução ao Power BI Desktop](../fundamentals/desktop-getting-started.md)

Mais perguntas? [Experimente a Comunidade do Power BI](https://community.powerbi.com/).
