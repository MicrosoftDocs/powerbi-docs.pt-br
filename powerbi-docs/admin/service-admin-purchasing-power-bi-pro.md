---
title: Comprar e atribuir licenças do Power BI Pro
description: Saiba como comprar e atribuir licenças de usuário do Power BI Pro para que os usuários possam acessar o conteúdo e colaborar com outras pessoas no serviço do Power BI.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 04/08/2020
ms.author: kfollis
ms.custom: licensing support
LocalizationGroup: Administration
ms.openlocfilehash: 72e2744fc325f5e5b36f3abcf4a6d3d71767fbd4
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85227646"
---
# <a name="purchase-and-assign-power-bi-pro-user-licenses"></a>Comprar e atribuir licenças de usuário do Power BI Pro

>[!IMPORTANT]
>Este artigo é para administradores. Você é um usuário que está pronto para fazer upgrade para uma licença do Power BI Pro? Acesse diretamente a [Introdução ao Power BI Pro](https://go.microsoft.com/fwlink/?LinkId=2106428&clcid=0x409&cmpid=pbidocs-purchasing-power-bi-pro) para configurar sua conta.

O Power BI Pro é uma licença individual de usuário que permite que eles leiam e interajam com relatórios e painéis publicados por outras pessoas no serviço do Power BI. Os usuários com esse tipo de licença podem compartilhar conteúdo e colaborar com outros usuários do Power BI Pro. Somente os usuários do Power BI Pro podem publicar ou compartilhar conteúdo com outros usuários ou consumir conteúdo criado por outros usuários, a menos que uma capacidade do Power BI Premium hospede esse conteúdo. Para obter mais informações sobre os tipos de licenças e assinaturas disponíveis, confira [Licenciamento do Power BI em sua organização](service-admin-licensing-organization.md).

## <a name="purchase-power-bi-pro-user-licenses"></a>Comprar licenças de usuário do Power BI Pro

Este artigo explica como comprar licenças de usuário do Power BI Pro no Centro de administração do Microsoft 365. Após comprar licenças, é possível atribuí-las a usuários no Centro de administração do Microsoft 365 ou no Portal do Azure.

> [!NOTE]
> Desde 14 de janeiro de 2020, as funcionalidades de compra por autoatendimento, assinatura e gerenciamento de licenças para os produtos da Power Platform (Power BI, Power Apps e Power Automate) estão disponíveis para clientes da nuvem comercial. Para obter mais informações, confira [Perguntas frequentes sobre compras por autoatendimento](https://docs.microsoft.com/microsoft-365/commerce/subscriptions/self-service-purchase-faq). Para habilitar ou desabilitar as funcionalidades de compra por autoatendimento, confira [Habilitar ou desabilitar a inscrição e a compra por autoatendimento](/service-admin-disable-self-service.md).

### <a name="prerequisites"></a>Pré-requisitos

Para comprar e atribuir licenças no centro de administração do Microsoft 365, você deve ser membro da função de [administrador global ou administrador de cobrança](https://support.office.com/article/about-office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d) no Microsoft 365.

Para atribuir licenças no portal do Azure, você precisa ser um proprietário da assinatura do Azure que o Power BI usa para realizar pesquisas no Azure Active Directory.

### <a name="purchase-licenses-in-microsoft-365"></a>Comprar licenças no Microsoft 365

> [!NOTE]
> Se você geralmente compra licenças por meio de um contrato de licenciamento por volume, como um Enterprise Agreement, e deseja receber uma fatura em vez de comprar com um cartão de crédito ou uma conta bancária, você precisa enviar o pedido de um modo diferente. Fale com o seu Revendedor da Microsoft ou acesse o Centro de Serviços de Licenciamento por Volume para adicionar ou remover licenças. Para obter mais informações, consulte [Gerenciar as licenças de assinatura](https://docs.microsoft.com/microsoft-365/commerce/licenses/buy-licenses?view=o365-worldwide).

Siga estas etapas para comprar licenças do Power BI Pro no centro de administração do Microsoft 365:

1. Entre no [centro de administração do Microsoft 365](https://admin.microsoft.com).

2. No menu de navegação, selecione **Cobrança** > **Serviços de compra**.

3. Pesquise ou role a tela para encontrar a assinatura que deseja comprar. Você verá **Power BI** em **Outras categorias que podem lhe interessar** próximo à parte inferior da página. Selecione o link para exibir as assinaturas do Power BI disponíveis para sua organização.

4. Selecione **Power BI Pro**.

5. Na página **Serviços de compra**, selecione **Comprar**.

6. Escolha **Pagar mensalmente** ou **Pagar por um ano inteiro**, de acordo com sua preferência de pagamento.

7. Em **Quantos usuários você deseja?** , insira a quantidade de licenças a comprar e selecione **Pagar agora** para concluir a transação.

8. Verifique sua compra acessando **Cobrança** > **Produtos e serviços** e procure **Power BI Pro**.

9. Para adicionar mais licenças posteriormente, localize **Power BI Pro** na página **Produtos e serviços** e selecione **Adicionar/remover licenças**.


## <a name="assign-licenses-in-the-microsoft-365-admin-center"></a>Atribuir licenças no centro de administração do Microsoft 365

Para obter informações sobre como atribuir licenças no Centro de administração do Microsoft 365, confira [Atribuir licenças a usuários](/office365/admin/manage/assign-licenses-to-users).

Para usuários convidados, confira [Atribuir licenças a usuários na página Licenças](/office365/admin/manage/assign-licenses-to-users#assign-licenses-to-users-on-the-licenses-page). Antes de atribuir licenças Pro a usuários convidados, entre em contato com seu representante da conta Microsoft para garantir que você esteja em conformidade com os termos do seu contrato com a Microsoft.

## <a name="assign-licenses-in-the-azure-portal"></a>Atribuir licenças no portal do Azure

Siga estas etapas para atribuir licenças do Power BI Pro a contas de usuário individuais:

1. Entre no [portal do Azure](https://portal.azure.com/).

2. Pesquise **Azure Active Directory** e selecione-o.

3. Em **Gerenciar** no menu de recursos do **Azure Active Directory**, selecione **Licenças**.

4. Selecione **Todos os produtos** no menu de recursos **Licenças – Visão geral** e selecione **Power BI Pro** para ver a lista de usuários licenciados.

5. Na barra de comandos, selecione **+ Atribuir**. Na página **Atribuir licença**, primeiro escolha um usuário e depois selecione **Opções de atribuição** para ativar uma licença do Power BI Pro para a conta de usuário selecionada.

## <a name="next-steps"></a>Próximas etapas

- [Licenciamento do Power BI na sua organização](service-admin-licensing-organization.md)

 - [Encontrar usuários do Power BI que entraram](service-admin-access-usage.md)

 - [Inscrever-se no Power BI (gratuito) como um indivíduo](../fundamentals/service-self-service-signup-for-power-bi.md)

Mais perguntas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)
