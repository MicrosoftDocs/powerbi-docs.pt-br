---
title: 'Pacotes de conteúdo organizacional: Gerenciar e atualizar'
description: Leia sobre gerenciamento, atualização e exclusão de pacotes de conteúdo organizacional no Power BI.
author: maggiesMSFT
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 08/02/2018
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: d741a489c5655e5a08f49f7197389a67c5d016ed
ms.sourcegitcommit: 181679a50c9d7f7faebcca3a3fc55461f594d9e7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2020
ms.locfileid: "86034395"
---
# <a name="manage-update-and-delete-organizational-content-packs"></a>Gerenciar, atualizar e excluir pacotes de conteúdo organizacional
> [!NOTE]
> Não é possível criar pacotes de conteúdo organizacional nem os instalar nas novas experiências do workspace. Agora é um bom momento para atualizar seu pacote de conteúdo para aplicativos, caso você ainda não tenha começado. Saiba [mais sobre a nova experiência de workspace](service-create-the-new-workspaces.md).
> 

Você pode empacotar e compartilhar seus painéis, relatórios, pastas de trabalho do Excel e conjuntos de dados com seus colegas em [pacotes de conteúdo organizacional](service-organizational-content-pack-introduction.md). Seus colegas podem usá-los como estiverem ou podem criar suas próprias cópias.

Criar pacotes de conteúdo é diferente de compartilhar dashboards ou colaborar neles em um grupo. Leia [Como devo colaborar e compartilhar relatórios e dashboards?](service-how-to-collaborate-distribute-dashboards-reports.md) para decidir sobre a melhor opção para sua situação.

Você só poderá realizar algumas tarefas do pacote de conteúdo organizacional se for o criador do pacote de conteúdo:

* Republicar.
* Restringir ou expandir o acesso ao pacote de conteúdo.
* Definir e alterar a atualização agendada.
* Excluir o pacote de conteúdo.

## <a name="modify-and-re-publish-an-organizational-content-pack"></a>Modificar e republicar um pacote de conteúdo organizacional
Se você fizer alterações no painel original do pacote de conteúdo, relatório ou pasta de trabalho do Excel, o Power BI solicitará que você publique novamente. Além disso, como criador do conteúdo do pacote, você pode atualizar qualquer uma das opções selecionadas na janela de criação de pacote de conteúdo, ao criar o pacote de conteúdo original. 

## <a name="republish-with-new-content"></a>Republicar com novo conteúdo
Ao fazer ou salvar uma alteração no painel que você incluiu em um pacote de conteúdo, o Power BI lembrará você de atualizá-lo para que outros possam ver as alterações. Por exemplo, se você fixa um novo bloco ou simplesmente altera o nome do painel.

1. Selecione **Exibir Pacotes de Conteúdo** na mensagem.
   
   ![Captura de tela de uma caixa de diálogo de mensagem para selecionar Exibir Pacotes de Conteúdo.](media/service-organizational-content-pack-manage-update-delete/pbi_contpkchangesmessage.png)
2. Ou selecione o ícone de engrenagem no canto superior direito ![Captura de tela do ícone engrenagem.](media/service-organizational-content-pack-manage-update-delete/cog.png) e selecione **Exibir Pacote de Conteúdo**.
   
   ![Captura de tela do ícone de engrenagem no canto superior direito.](media/service-organizational-content-pack-manage-update-delete/pbi_contpkview.png)
   
   Observe o ícone de aviso ![Captura de tela do ícone de aviso.](media/service-organizational-content-pack-manage-update-delete/pbi_contpkwarningicon.png).  Assim, você sabe que modificou o pacote de conteúdo de alguma forma e ele não coincide mais com o que foi publicado.
3. Selecione **Editar**.  
4. Faça as alterações necessárias na janela **Pacote de atualização de conteúdo** e selecione **Atualização**. Será exibida uma mensagem de **êxito** .
   
   * Para membros do grupo que não personalizaram o pacote de conteúdo, a atualização é aplicada automaticamente.
   * Os membros do grupo que personalizaram o pacote de conteúdo receberão uma notificação de que há uma nova versão.  Eles podem acessar o AppSource e obter o pacote de conteúdo atualizado sem perder sua versão personalizada.  Agora eles terão as duas versões: a versão personalizada e o pacote de conteúdo atualizado.  Na versão personalizada, todas as peças do pacote de conteúdo original serão eliminadas.  Mas os blocos fixados de outros relatórios ainda serão renderizados. No entanto, se o proprietário do pacote de conteúdo excluir o conjunto de dados em que o pacote se baseia, todo o relatório desaparecerá.  

## <a name="update-the-audience-expand-or-restrict-access"></a>Atualizar o público: expandir ou restringir o acesso
Outra modificação para criadores de pacote de conteúdo está expandindo e restringindo o acesso ao pacote de conteúdo.  Talvez você tenha publicado um pacote de conteúdo para um público amplo e decidiu restringir o acesso a um grupo menor.  

1. Selecione o ícone de engrenagem ![Captura de tela do ícone de engrenagem.](media/service-organizational-content-pack-manage-update-delete/cog.png) e escolha **Exibir Pacotes de Conteúdo**.
2. Selecione **Editar**. 
3. Faça as alterações necessárias na janela **Pacote de atualização de conteúdo** e selecione **Atualização**. Por exemplo, exclua o grupo de distribuição original no campo **Grupos Específicos** e substitua-o por um grupo de distribuição diferente (que tem menos membros).
   
   Será exibida uma mensagem de êxito.
   
   Para qualquer colaborador que não faz parte do novo alias:
   
   * Para os membros do grupo que não personalizaram o pacote de conteúdo, o dashboard e os relatórios associados a esse pacote de conteúdo não estarão mais disponíveis e o pacote de conteúdo não será exibido no painel de navegação.
   * Para os membros do grupo que personalizaram o pacote de conteúdo, na próxima vez que eles abrirem o painel personalizado, todos os blocos do pacote de conteúdo original desaparecerão.  Mas os blocos fixados de outros relatórios ainda serão renderizados. Os relatórios e o conjunto de dados do pacote de conteúdo original não estarão mais disponíveis, e o pacote de conteúdo não aparecerá no painel de navegação.   

## <a name="refresh-an-organizational-content-pack"></a>Atualizar um pacote de conteúdo organizacional
Como o criador do pacote de conteúdo, você pode [agendar a atualização dos conjuntos de dados](../connect-data/refresh-data.md).  Quando você cria e carregar o pacote de conteúdo, essa agenda de atualização é carregada com os conjuntos de dados. Se você alterar o agendamento de atualização, você precisará publicar novamente o pacote de conteúdo (veja acima).

## <a name="delete-an-organizational-content-pack-from-appsource"></a>Excluir um pacote de conteúdo organizacional do AppSource
Você só poderá excluir um pacote de conteúdo do AppSource se o tiver criado. Se você criar um pacote de conteúdo organizacional em um workspace e, depois, decidir excluir esse workspace, lembre-se de excluir o pacote de conteúdo primeiro. Se você excluir o workspace sem excluir o pacote de conteúdo primeiro, você perderá todo o acesso a esses pacotes de conteúdo e terá que entrar em contato com o Suporte da Microsoft para obter ajuda. 

> [!TIP]
> É possível [excluir a conexão com um pacote de conteúdo](service-organizational-content-pack-disconnect.md) que você não criou. Isso não exclui o pacote de conteúdo do AppSource.
> 
> 

1. Para excluir um pacote de conteúdo do AppSource, acesse o workspace em que você criou o pacote de conteúdo, selecione o ícone de engrenagem ![Captura de tela do ícone de engrenagem.](media/service-organizational-content-pack-manage-update-delete/cog.png) e escolha **Exibir Pacotes de Conteúdo**.
2. Selecione **Excluir \> Excluir**. 
   
   * Para os membros do grupo que não personalizaram o pacote de conteúdo, o painel e os relatórios associados a esse pacote de conteúdo serão removidos automaticamente. Eles não estarão disponíveis, e o pacote de conteúdo não aparecerá no painel de navegação.
   * Para os membros do grupo que personalizaram o pacote de conteúdo, na próxima vez que eles abrirem o painel personalizado, todos os blocos do pacote de conteúdo original desaparecerão.  Mas os blocos fixados de outros relatórios ainda serão renderizados. Os relatórios e o conjunto de dados do pacote de conteúdo original não estarão mais disponíveis, e o pacote de conteúdo não aparecerá no painel de navegação.   

## <a name="next-steps"></a>Próximas etapas
* [Introdução aos pacotes de conteúdo organizacional](service-organizational-content-pack-introduction.md)
* [Criar e distribuir um aplicativo no Power BI](service-create-distribute-apps.md) 
* Mais perguntas? [Experimente a Comunidade do Power BI](https://community.powerbi.com/)

