---
title: Parâmetros de URL em relatórios paginados – Construtor de Relatórios do Power BI
description: Este tópico descreve os usos comuns de parâmetros de relatório do Power BI Report Builder, as propriedades que podem ser definidas, entre outros.
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
author: maggiesMSFT
ms.author: maggies
ms.reviewer: cfinlan
ms.custom: ''
ms.date: 05/01/2020
ms.openlocfilehash: fd92e64ac04a31446214bd6f1661d9ba5c1358d9
ms.sourcegitcommit: 10c5b6cd5e7070f96de8a9f1d9b95f3d242ac7f2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "86557087"
---
# <a name="url-parameters-in-paginated-reports-in-power-bi"></a>Parâmetros de URL em relatórios paginados no Power BI

Você pode enviar comandos para relatórios paginados no Power BI adicionando um parâmetro em uma URL. Por exemplo, você pode ter exibido o relatório usando um conjunto específico de valores de parâmetro de relatório. Você encapsula essas informações na URL usando parâmetros de acesso à URL predefinidos. Você pode personalizar ainda mais a forma como o Power BI processa o relatório inserindo parâmetros para formatos de renderização ou para determinar a aparência e o estilo da barra de ferramentas de relatório. Em seguida, você pode colar essa URL diretamente em um email ou uma página da Web para que outras pessoas experimentem o relatório da mesma maneira em um navegador. 

Aqui estão as ações que você pode executar por meio de parâmetros de acesso à URL: 

- Enviar parâmetros de relatório a um relatório. 
- Iniciar a exportação do conteúdo do relatório em um formato de arquivo compatível. 
- Ocultar ou exibir o painel de parâmetros. 
- Especificar a configuração DeviceInfo. 

Para obter a lista completa de comandos e configurações disponíveis por meio do acesso à URL, confira  [Referência de parâmetro de acesso à URL](#url-access-parameter-reference) mais adiante neste artigo. 

## <a name="url-access-concepts"></a>Conceitos de acesso à URL 

As solicitações de URL para o Power BI contêm parâmetros que são processados pelo serviço. A maneira como o serviço gerencia as solicitações de URL depende dos parâmetros, dos prefixos de parâmetro e dos tipos de itens incluídos na URL. A funcionalidade de URL de relatório paginado é compatível com a maioria dos navegadores e aplicativos que são compatíveis com o endereçamento de URL padrão. 

## <a name="url-access-syntax"></a>Sintaxe do acesso à URL 

As solicitações de URL podem conter vários parâmetros, listados em qualquer ordem. Os parâmetros são separados por um E comercial (&). Os pares de nome e valor são separados por um sinal de igual (=). Por exemplo:

```
powerbiserviceurl?rp:parametervalueh&rdl:parameter=value  
```

## <a name="syntax-description"></a>Descrição da sintaxe 

### <a name="powerbiserviceurl"></a>powerbiserviceurl 

A URL do serviço Web do seu locatário do Power BI. Por exemplo: 

**&** Usado para separar pares de nome e valor dos parâmetros de acesso à URL.

**prefixo** Um prefixo para o parâmetro da URL (por exemplo, rp: ou rdl:) que especifique uma ação no Serviço do Power BI. 

> [!NOTE]
> Os parâmetros de relatório exigem um prefixo de parâmetro e diferenciam maiúsculas de minúsculas. 

**parâmetro** O nome do parâmetro. 

### <a name="value"></a>valor 

Texto da URL correspondente ao valor do parâmetro que está sendo usado. 

Para ver exemplos de como passar parâmetros de relatório na URL, confira  [Passar um parâmetro de relatório em uma URL](report-builder-url-pass-parameters.md).

## <a name="url-access-parameter-reference"></a>Referência de parâmetro de acesso à URL

Você pode usar os parâmetros a seguir como parte de uma URL para configurar a aparência e o estilo dos seus relatórios paginados no Power BI. Os parâmetros mais comuns são listados nesta seção. Os parâmetros não diferenciam maiúsculas de minúsculas e começam com o prefixo de parâmetro `rdl:` , se relacionado ao formato de saída.  

### <a name="report-commands-rdl"></a>Comandos de relatório (`rdl:`) 

**Formato de exportação** Especifica o formato no qual renderizar e exportar um relatório.

Exemplo: rdl:format=PDF

Os valores disponíveis são:
 
- PPTX (PowerPoint)
- MHTML 
- IMAGEM 
- EXCELOPENXML (EXCEL) 
- WORDOPENXML (WORD) 
- CSV 
- PDF 
- ACCESSIBLEPDF (PDF)
- XML 

**Visualização de Relatório** Especifica o tipo de visualização usado para exibir o relatório.

-   rdl:reportView

    - "interactive" (padrão): carrega o relatório no modo interativo.
    - "pageView": carrega o relatório no modo de exibição de página.

**Estado do painel de parâmetros** Especifica se o painel de parâmetros fica fechado ou aberto quando o relatório é carregado ou fica totalmente oculto.

-   rdl:parameterPanelState

    - 'recolhido': carregue o relatório com o painel de parâmetros fechado. O botão de parâmetro é habilitado para que os usuários possam clicar no botão para expandi-lo;
    - 'oculto': carregue o relatório com o painel de parâmetros fechado e o botão de parâmetro desabilitado;
    - 'expandido' (padrão): carregue o relatório com o painel de parâmetros aberto e o botão de parâmetro habilitado;

**Informações do Dispositivo** Você pode especificar parâmetros de saída adicionais para os formatos de exportação a seguir. 

PDF/ACCESSIBLEPDF:

- rdl:AccessiblePDF=true/false
- rdl:Columns=integer
- rdl:ColumnSpacing=decimal(in)
- rdl:DpiX=integer
- rdl:DpiY=integer
- rdl:EndPage=integer
- rdl:HumanReadablePDF=true/false
- rdl:MarginBottom=decimal(in)
- rdl:MarginLeft=decimal(in)
- rdl:MarginRight=decimal(in)
- rdl:MarginTop=decimal(in)
- rdl:PageHeight=decimal(in)
- rdl:PageWidth=decimal(in)
    - rdl:StartPage=integer
    
CSV:

- rdl:Encoding=string
- rdl:ExcelMode=true/false
- rdl:FieldDelimiter=string
- rdl:FileExtension=string
- rdl:NoHeader=true/false
- rdl:Qualifier=string
- rdl:RecordDelimiter=string
- rdl:SuppressLineBreaks=true/false
    - rdl:UseFormattedValues=true/false
    
WORDOPENXML (WORD):

- rdl:AutoFit=string -> True/False/Never/Default
- rdl:ExpandToggles=true/false
- rdl:FixedPageWidth=true/false
- rdl:OmitHyperlinks=true/false
- rdl:OmitDrillthroughs=true/false

EXCELOPENXML (EXCEL):

- rdl:OmitDocumentMap=true/false
- rdl:OmitFormulas=true/false
    - rdl:SimplePageHeaders=true/false
    
PPTX (PowerPoint):
 
- rdl:Columns=integer
- rdl:ColumnSpacing=decimal(in)
- rdl:DpiX=integer
- rdl:DpiY=integer
- rdl:EndPage=integer
- rdl:MarginBottom=decimal(in)
- rdl:MarginLeft=decimal(in)
- rdl:MarginRight=decimal(in)
- rdl:MarginTop=decimal(in)
- rdl:PageHeight=decimal(in)
- rdl:PageWidth=decimal(in)
- rdl:StartPage=integer
    - rdl:UseReportPageSize=true/false

XML:

- rdl:XSLT=string
- rdl:MIMEType=string
- rdl:UseFormattedValues=true/false
- rdl:Indented=true/false
- rdl:OmitNamespace=true/false
- rdl:OmitSchema=true/false
- rdl:Encoding=string
- rdl:FileExtension=string
- rdl:Schema=true/false

**Abra o hiperlink na mesma janela do navegador**. Você pode acrescentar 'rdl:targetSameWindow=true' à URL do hiperlink no seu relatório para que o Power BI abra esse hiperlink na mesma janela do navegador. Para obter informações sobre como adicionar hiperlinks a um relatório, consulte [Adicionar um hiperlink a uma URL](https://docs.microsoft.com/sql/reporting-services/report-design/add-a-hyperlink-to-a-url-report-builder-and-ssrs) na documentação do SQL Server Reporting Services.

## <a name="next-steps"></a>Próximas etapas

- [Passar um parâmetro de relatório em uma URL para um relatório paginado no Power BI](report-builder-url-pass-parameters.md)
- [O que são os relatórios paginados no Power BI Premium?](paginated-reports-report-builder-power-bi.md)
