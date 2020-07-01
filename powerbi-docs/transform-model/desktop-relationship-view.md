---
title: Exibição de modelo no Power BI Desktop
description: Exibição de modelo no Power BI Desktop
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: how-to
ms.date: 01/17/2020
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: 1c580d403ef33f1c61d5fcd0707d78b4b331da5d
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85239870"
---
# <a name="work-with-model-view-in-power-bi-desktop"></a>Trabalhar com a exibição de modelo no Power BI Desktop

A *exibição de modelo* mostra todas as tabelas, colunas e relações em seu modelo. Essa exibição pode ser especialmente útil quando seu modelo tem relações complexas entre muitas tabelas.

Selecione o ícone de **Modelo** próximo à lateral da janela para ver uma exibição do modelo existente. Passe o cursor sobre uma linha de relação para mostrar as colunas usadas.

![Exibição de modelo, Power BI Desktop](media/desktop-relationship-view/model-view-full-screen.png)

Na figura, a tabela *Stores* tem uma coluna *StoreKey* relacionada à tabela *Sales*, que também tem uma coluna *StoreKey*. As duas tabelas têm uma relação *Muitos para Um* (\*: 1). Uma seta no meio da linha mostra a direção do fluxo do contexto de filtro. As setas duplas significam que a direção do filtro cruzado está definida como *Ambas*.

Clique duas vezes em uma relação para abri-la na caixa de diálogo **Editar Relação**. Para saber mais sobre as relações, consulte [Criar e gerenciar relações no Power BI Desktop](desktop-create-and-manage-relationships.md).
