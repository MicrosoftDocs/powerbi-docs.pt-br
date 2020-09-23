---
title: Distribuir conteúdos para usuários convidados externos com o Azure AD B2B
description: O Power BI permite o compartilhamento de conteúdo com usuários convidados externos por meio do Azure AD B2B (Azure Active Directory Business-to-business).
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 07/02/2020
ms.author: kfollis
LocalizationGroup: Administration
ms.openlocfilehash: 4a38ca35e6955bc92f52492e657a9e00bad05ea3
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90857601"
---
# <a name="distribute-power-bi-content-to-external-guest-users-with-azure-ad-b2b"></a>Distribuir o conteúdo do Power BI para usuários convidados externo com o Azure AD B2B

O Power BI permite o compartilhamento de conteúdo com usuários convidados externos por meio do Azure AD B2B (Azure Active Directory Business-to-business). Usando o Azure AD B2B, sua organização habilita e rege o compartilhamento com usuários externos em um local central. Por padrão, os convidados externos têm uma experiência apenas de consumo. Além disso, você pode permitir que usuários convidados fora da sua organização editem e gerenciem o conteúdo dentro de sua organização.

Este artigo fornece uma introdução básica ao Azure AD B2B no Power BI. Para obter mais informações, confira [Distribuir o conteúdo do Power BI para usuários convidados externos usando o Azure Active Directory B2B](../guidance/whitepaper-azure-b2b-power-bi.md).

## <a name="enable-access"></a>Habilitar acesso

Habilite o recurso [Compartilhar conteúdo com usuários externos](service-admin-portal.md#export-and-sharing-settings) no portal de administração do Power BI antes de convidar usuários. Mesmo quando essa opção está habilitada, o usuário deve receber a função Emissor de convites independente no Azure Active Directory para convidar usuários.

A opção de [Permitir que os usuários externos convidados editem e gerenciem o conteúdo da organização](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization) permite que você ofereça aos usuários convidados a capacidade de ver e criar conteúdo em workspaces, incluindo a navegação pelo Power BI da sua organização.

> [!NOTE]
> A configuração [Compartilhar conteúdo com usuários externos](service-admin-portal.md#export-and-sharing-settings) controla se o Power BI permite convidar usuários externos para sua organização. Após um usuário externo aceitar o convite, ele se tornará um usuário convidado do Azure AD B2B em sua organização. Ele aparecerá nos seletores de pessoas durante a experiência do Power BI. Se a configuração for desabilitada, os usuários convidados existentes na sua organização continuarão a ter acesso a todos os itens aos quais já tinham acesso e permanecerão listados nas experiências do seletor de pessoas. Além disso, se os convidados forem adicionados por meio da abordagem de [convite planejado](#planned-invites), eles também aparecerão nos seletores de pessoas. Você pode usar uma política de acesso condicional do Azure AD para impedir que usuários convidados acessem o Power BI.

## <a name="who-can-you-invite"></a>Que você pode convidar?

Há suporte para a maioria dos endereços de email nos convites de usuário, incluindo contas pessoais do Gmail, Outlook ou Hotmail. O Azure AD B2B chama esses endereços de *identidades sociais*.

Você não pode convidar usuários associados a uma nuvem governamental, como o [Power BI for US Government](service-govus-overview.md).

## <a name="invite-guest-users"></a>Convidar usuários convidados

Os usuários convidados só precisam de convites na primeira vez que você os convida para sua organização. Para convidar usuários, use convites planejados ou ad hoc.

Para usar convites ad hoc, use os recursos a seguir:

* Compartilhamento de relatórios e painéis
* Lista de acesso a aplicativos

Não há suporte para convites ad hoc na lista de acesso do workspace. Use a [abordagem de convites planejados](#planned-invites) para adicionar esses usuários à sua organização. Depois que o usuário externo se tornar um convidado em sua organização, adicione-o à lista de acesso do workspace.

### <a name="planned-invites"></a>Convites planejados

Use um convite planejado se souber quais usuários vai convidar. O portal do Azure ou o PowerShell permite que você envie os convites. Você deve receber a função de administrador de usuários para convidar pessoas.

Execute estas etapas para enviar um convite no Portal do Azure.

1. No [portal do Azure](https://portal.azure.com), selecione **Azure Active Directory**.

1. Em **Gerenciar**, selecione **Usuários** > **Todos os usuários** > **Novo usuário convidado**.

    ![Captura de tela do portal do Azure com a opção Novo Usuário Convidado ativada.](media/service-admin-azure-ad-b2b/azure-ad-portal-new-guest-user.png)

1. Insira um **endereço de email** e **mensagem pessoal**.

    ![Captura de tela da caixa de diálogo Novo Usuário Convidado com os campos de email e mensagem em destaque.](media/service-admin-azure-ad-b2b/azure-ad-portal-invite-message.png)

1. Selecione **Convidar**.

Para convidar mais de um usuário, use o PowerShell ou crie um convite em massa no Azure AD. Para usar o PowerShell no convite em massa, siga as etapas do [Tutorial: usar o PowerShell para convidar usuários de colaboração do Azure AD B2B em massa](/azure/active-directory/b2b/bulk-invite-powershell/). Para usar o portal do Azure no convite em massa, siga as etapas do [Tutorial: convidar usuários de colaboração B2B do Azure AD em massa](/azure/active-directory/b2b/tutorial-bulk-invite/).

O usuário convidado precisa selecionar **Introdução** no convite que recebeu por email. O usuário convidado é adicionado à organização.

![Captura de tela do convite por email do usuário convidado com o botão Começar Agora em destaque.](media/service-admin-azure-ad-b2b/guest-user-invite-email.png)

### <a name="ad-hoc-invites"></a>Convites ad hoc

Para convidar um usuário externo a qualquer momento, adicione-o ao seu dashboard ou relatório por meio do recurso de compartilhamento ou ao seu aplicativo por meio da página de acesso. Aqui está um exemplo de como convidar um usuário externo para usar um aplicativo.

![Captura de tela do usuário externo adicionado à lista de Acesso do aplicativo no Power BI.](media/service-admin-azure-ad-b2b/power-bi-app-access.png)

O usuário convidado receberá um email indicando que você compartilhou o aplicativo com ele.

![Captura de tela do email que o usuário convidado recebe quando o aplicativo é compartilhado.](media/service-admin-azure-ad-b2b/guest-user-invite-email-2.png)

O usuário convidado deverá entrar com o endereço de email da organização. Ele receberá uma solicitação para aceitar o convite depois de entrar. Depois de entrar, o aplicativo é aberto para o usuário convidado. Para retornar ao aplicativo, é necessário marcar o link ou salvar o email.

## <a name="licensing"></a>Licenciamento

O usuário convidado precisa ter a licença correta em vigor para ver o conteúdo compartilhado. Há três maneiras de garantir uma licença adequada para o usuário: usar o Power BI Premium, atribuir uma licença do Power BI Pro ao convidado ou usar a licença do Power BI Pro do convidado.

[Os usuários convidados que podem editar e gerenciar conteúdo na organização](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization) precisam de uma licença do Power BI Pro para contribuir com conteúdo em workspaces ou para compartilhar conteúdo com outras pessoas.

### <a name="use-power-bi-premium"></a>Usar o Power BI Premium

A atribuição do workspace à [capacidade do Power BI Premium](service-premium-what-is.md) permite que o usuário convidado use o aplicativo sem precisar de uma licença do Power BI Pro. O Power BI Premium também permite que aplicativos aproveitem outros recursos, como taxas mais altas de atualização, capacidade dedicada e tamanhos grandes de modelos.

![Diagrama da experiência do usuário convidado com o Power BI Premium.](media/service-admin-azure-ad-b2b/license-approach-1.png)

### <a name="assign-a-power-bi-pro-license-to-guest-user"></a>Atribuir uma licença do Power BI Pro ao usuário convidado

A atribuição de uma licença do Power BI Pro da sua organização para um usuário convidado permite que o usuário convidado veja o conteúdo compartilhado com ele. Para obter mais informações sobre como atribuir licenças, confira [Atribuir licenças a usuários na página Licenças](/office365/admin/manage/assign-licenses-to-users#assign-licenses-to-users-on-the-licenses-page). Antes de atribuir licenças Pro a usuários convidados, consulte o [site Termos do Produto](https://www.microsoft.com/licensing/terms) para garantir que você esteja em conformidade com os termos do seu contrato de licenciamento com a Microsoft.

![Diagrama da experiência do usuário convidado com Atribuir licença Pro do locatário.](media/service-admin-azure-ad-b2b/license-approach-2.png)

### <a name="guest-user-brings-their-own-power-bi-pro-license"></a>O usuário convidado traz a própria licença do Power BI Pro

O usuário convidado pode já ter uma licença do Power BI Pro atribuída pela organização dele.

![Diagrama da experiência do usuário convidado quando ele traz a própria licença.](media/service-admin-azure-ad-b2b/license-approach-3.png)

## <a name="guest-users-who-can-edit-and-manage-content"></a>Usuários convidados que podem editar e gerenciar conteúdo

Ao usar o recurso [Permitir que os usuários externos convidados editem e gerenciem o conteúdo da organização](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization), os usuários convidados especificados obtêm acesso adicional ao Power BI da sua organização. Os usuários permitidos podem ver qualquer conteúdo ao qual tenham permissão, acessar a página inicial, navegar por workspaces, instalar aplicativos, ver onde estão na lista de acesso e contribuir com conteúdo para os workspaces. Eles podem ser administradores de workspaces que usam a nova experiência de workspace e até mesmo criar tais workspaces. Algumas limitações se aplicam. A seção Considerações e limitações lista essas restrições.

Para ajudar os convidados autorizados a entrar no Power BI, forneça a eles a URL do locatário. Para localizar a URL do locatário, siga estas etapas.

1. No serviço do Power BI, no cabeçalho superior, selecione a ajuda ( **?** ) e **Sobre o Power BI**.

2. Procure o valor ao lado de **URL do locatário**. Compartilhe a URL do locatário com os usuários convidados permitidos.

    ![Captura de tela da caixa de diálogo Sobre o Power BI com a URL do Locatário do Usuário Convidado em destaque.](media/service-admin-azure-ad-b2b/power-bi-about-dialog.png)

## <a name="considerations-and-limitations"></a>Considerações e limitações

* Por padrão, o Azure AD B2B externo limita os convidados ao consumo apenas de conteúdo. Os convidados de Azure AD B2B externos podem exibir aplicativos, painéis, relatórios, além de exportar dados e criar assinaturas de email para painéis e relatórios. Eles não podem acessar os workspaces ou publicar seu próprio conteúdo. Para remover essas restrições, você pode usar o recurso [Permitir que os usuários externos convidados editem e gerenciem o conteúdo da organização](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization).

* Para convidar usuários, uma licença do Power BI Pro é necessária. Os usuários da avaliação do Pro não podem convidar usuários convidados no Power BI.

* Algumas experiências não estão disponíveis para [usuários convidados que podem editar e gerenciar conteúdo na organização](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization). Para atualizar ou publicar relatórios, os usuários convidados precisarão usar o serviço do Power BI, incluindo Obter Dados, para carregar arquivos do Power BI Desktop.  Não há suporte para as seguintes experiências:
  * Publicação direta do Power BI Desktop para o serviço do Power BI
  * Os usuários convidados não podem usar o Power BI Desktop para se conectar a conjuntos de dados de serviço no serviço do Power BI
  * Workspaces clássicos associados a Grupos do Microsoft 365
    * Os usuários convidados não podem criar nem ser administradores desses workspaces
    * Os usuários convidados podem ser membros
  * O envio de convites ad hoc para listas de acesso do workspace não é uma ação compatível
  * O Power BI Publisher para Excel não é compatível com usuários convidados
  * Os usuários convidados não podem instalar um Power BI Gateway e conectá-lo à sua organização
  * Os usuários convidados não podem instalar aplicativos e publicá-los para toda a organização
  * Os usuários convidados não podem usar, criar, atualizar ou instalar pacotes de conteúdo organizacional
  * Os usuários convidados não podem usar o Analisar no Excel
  * Os usuários convidados não podem ser @mentioned em comentários
  * Os usuários convidados não podem usar assinaturas
  * Usuários convidados que usam essa funcionalidade devem ter uma conta corporativa ou de estudante

* Usuários convidados que usam identidades sociais terão mais limitações devido a restrições de entrada.
  * Eles podem usar experiências de consumo no serviço do Power BI por meio de um navegador da Web
  * Eles não podem usar os aplicativos Power BI Mobile
  * Eles não poderão entrar quando uma conta corporativa ou de estudante for necessária

* No momento, este recurso não está disponível com a web part de relatório do Power BI para o SharePoint Online.

* Há configurações do Azure Active Directory que podem limitar o que os usuários convidados externos podem fazer dentro de sua organização em geral. Essas configurações também se aplicam ao seu ambiente do Power BI. A documentação a seguir descreve as configurações:
  * [Gerenciar configurações de colaboração externa](/azure/active-directory/b2b/delegate-invitations#configure-b2b-external-collaboration-settings)
  * [Permitir ou bloquear convites para usuários B2B de organizações específicas](/azure/active-directory/b2b/allow-deny-list)
  * [Usar o acesso condicional para permitir ou bloquear o acesso](/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps)

* Você pode compartilhar conteúdo de uma nuvem governamental, como GCC, para um usuário externo de nuvem comercial. No entanto, o usuário convidado não pode usar sua própria licença. O conteúdo deve ter a capacidade atribuída a Premium para habilitar o acesso. Ou você pode atribuir uma licença do Power BI Pro à conta de convidado.

* O compartilhamento fora de sua organização não tem suporte em nuvens nacionais, como as instâncias de nuvem da Alemanha ou China. Alternativamente, crie contas de usuário em sua organização que usuários externos possam usar para acessar o conteúdo.

* Se você compartilhar conteúdo diretamente com um usuário convidado, o Power BI enviará a ele um email com o link. Para evitar o envio de um email, adicione o usuário convidado a um grupo de segurança e compartilhe com o grupo de segurança.  

## <a name="next-steps"></a>Próximas etapas

Para obter mais informações, inclusive sobre o funcionamento da segurança de linha, confira o white paper: [Distribuir o conteúdo do Power BI para usuários convidados externo com o Azure AD B2B](../guidance/whitepaper-azure-b2b-power-bi.md).

Para saber mais sobre o Azure AD B2B, confira [O que é o acesso de usuários convidados na colaboração B2B do Azure Active Directory?](/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b/).