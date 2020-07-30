---
title: Onde está localizado meu locatário do Power BI?
description: Saiba onde está localizado seu locatário do Power BI e como essa localização é selecionada. É importante compreender isso, já que é algo que pode afetar suas interações com o serviço.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/09/2019
ms.author: kfollis
LocalizationGroup: Administration
ms.openlocfilehash: ee123bed8940b52a66f3b0f860671a87210c261f
ms.sourcegitcommit: e9cd61eaa66eda01cc159251d7936a455c55bd84
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2020
ms.locfileid: "86952675"
---
# <a name="where-is-my-power-bi-tenant-located"></a>Onde está localizado meu locatário do Power BI?

<iframe width="560" height="315" src="https://www.youtube.com/embed/0fOxaHJPvdM?showinfo=0" frameborder="0" allowfullscreen></iframe>

Saiba onde está localizado seu locatário do Power BI e como essa localização é selecionada. É importante compreender o local, pois isso pode afetar suas interações com o serviço.

## <a name="how-to-determine-where-your-power-bi-tenant-is-located"></a>Como determinar onde se encontra o seu locatário do Power BI

Para localizar em qual região seu locatário está, execute estas etapas.

1. No serviço do Power BI, no menu superior, selecione a Ajuda ( **?** ), em seguida, **Sobre o Power BI**.

1. Procure o valor ao lado de **Seus dados são armazenados em**. Essa é a região na qual seu locatário está localizado. O valor é também a região na qual os dados estão armazenados, a menos que você esteja usando capacidades dedicadas em regiões diferentes para seus workspaces.

    ![Região de dados](media/service-admin-where-is-my-tenant-located/power-bi-data-region.png)

## <a name="how-the-data-region-is-selected"></a>Como a região de dados é selecionada

A região de dados está localizada na região/no país que você seleciona quando cria o locatário. A seleção se aplica à inscrição do Microsoft 365 e do Power BI, pois essas informações são compartilhadas. Se esse for um novo locatário, selecione a região/o país apropriado na lista quando você se inscrever.

![Seleção de país](media/service-admin-where-is-my-tenant-located/sign-up-country-selection.png)

O Power BI seleciona uma região de dados mais próxima de sua seleção, o que determina onde os dados são armazenados para seu locatário.

> [!IMPORTANT]
> Não é possível alterar a seleção após a criação do locatário.

Mais perguntas? [Experimente a Comunidade do Power BI](https://community.powerbi.com/)
