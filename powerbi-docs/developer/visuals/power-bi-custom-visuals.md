---
title: Visuais no Power BI
description: Este artigo descreve visuais personalizados do Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: overview
ms.date: 07/14/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: e56b03eeccc3140709fb458d4e42a9065a4da5d4
ms.sourcegitcommit: 2131f7b075390c12659c76df94a8108226db084c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/03/2020
ms.locfileid: "87538000"
---
# <a name="visuals-in-power-bi"></a>Visuais no Power BI

O Power BI vem com muitos visuais prontos para uso. Esses visuais estão disponíveis no painel de visualização do [Power BI Desktop](https://powerbi.microsoft.com/desktop/) e do [serviço do Power BI](https://app.powerbi.com) e podem ser usados para criar e editar o conteúdo do Power BI.

![Captura de tela do painel de visualização do Power BI como ele aparece no Power BI Desktop e no serviço do Power BI.](media/power-bi-custom-visuals/power-bi-visualizations.png)

Muitos outros visuais do Power BI estão disponíveis no Microsoft [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) ou por meio do Power BI. Esses visuais são criados pela Microsoft e por parceiros da Microsoft e são testados e validados pela equipe de validação do AppSource.

Você também pode desenvolver seu próprio visual do Power BI, a ser usado por você, sua organização ou pela comunidade inteira do Power BI.

## <a name="default-power-bi-visuals"></a>Visuais padrão do Power BI

Estes são os visuais prontos para uso do Power BI disponíveis no painel de visualização do *Power BI Desktop* e do *serviço do Power BI*.

Para desafixar um visual do Power BI do painel de visualização, clique com o botão direito do mouse nele e selecione **Desafixar**.

Para restaurar os visuais padrão do Power BI no painel de visualização, clique em **Importar um visual personalizado** e selecione **Restaurar visuais padrão**. 

## <a name="appsource-power-bi-visuals"></a>Visuais do Power BI no AppSource

A Microsoft e os membros da comunidade contribuem com visuais do Power BI para o benefício público e os publicam no [AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals). Baixe esses visuais e adicione-os aos seus relatórios do Power BI. A Microsoft testou e aprovou esses visuais do Power BI com relação à funcionalidade e à qualidade.

>[!NOTE]
>* Ao usar visuais do Power BI criados com o nosso SDK, talvez você esteja importando dados de/enviando dados para terceiros ou outros serviços localizados fora da região geográfica do seu locatário do Power BI, limite de conformidade ou instância de nuvem nacional.
>* Visuais certificados do Power BI são visuais no AppSource que foram adicionalmente testados para verificar que o visual não acessa serviços nem recursos externos.
>* Após os visuais do Power BI do AppSource serem importados, eles poderão ser atualizados automaticamente sem outros avisos.

### <a name="what-is-appsource"></a>O que é o AppSource?

O [AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals) é o lugar para encontrar aplicativos, suplementos e extensões para seu software Microsoft. O AppSource conecta milhões de usuários de produtos como Microsoft 365, Azure, Dynamics 365, Cortana e Power BI a soluções que os ajudam a realizar o trabalho com mais eficiência e insights do que antes.

### <a name="certified-power-bi-visuals"></a>Visuais do Power BI certificados

Os visuais certificados do Power BI são visuais do [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) testados e aprovados pela equipe do Microsoft Power BI que atendem a determinados requisitos de código especificados. Os testes foram criados para verificar se o visual não acessa serviços ou recursos externos.

Para ver a lista de visuais certificados do Power BI ou para enviar seus próprios, confira [Visuais certificados do Power BI](power-bi-custom-visuals-certified.md).

### <a name="samples-for-power-bi-visuals"></a>Amostras de visuais do Power BI

Cada visual do Power BI no AppSource tem uma amostra de dados que ilustra como ele funciona. Para baixar a amostra, no [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0), selecione um visual do Power BI e, na seção *Experimentar uma amostra*, clique no link **Relatório de exemplo**.

## <a name="organizational-store"></a>Repositório organizacional

Os administradores do Power BI aprovam e implantam visuais do Power BI em sua organização. Isso permite que os autores de relatórios descubram, atualizem e usem esses visuais do Power BI com facilidade. Os administradores podem gerenciar esses visuais com facilidade por meio de ações como atualizar versões, desabilitar e habilitar visuais do Power BI.

Para acessar o repositório organizacional, no painel *Visualização*, clique em **Importar um visual personalizado**, selecione **Importar do marketplace** e, na parte superior da janela *Visuais do Power BI*, selecione a guia **Minha organização**.

[Leia mais sobre visuais da organização](power-bi-custom-visuals-organization.md).

## <a name="visual-files"></a>Arquivos visuais

Os visuais do Power BI são pacotes que incluem o código para renderizar os dados fornecidos a eles. Qualquer pessoa pode criar um visual personalizado e empacotá-lo como um único arquivo `.pbiviz`, que pode ser importado em um relatório do Power BI.

Para importar um visual do Power BI, no painel *Visualização*, clique em **Importar um visual personalizado** e selecione **Importar do arquivo**.

Se você é desenvolvedor da Web e está interessado em criar seu próprio visual e adicioná-lo ao AppSource, saiba como [desenvolver um visual do Power BI](custom-visual-develop-tutorial.md) e [publicar um visual do Power BI no AppSource](office-store.md).

> [!WARNING]
> Um visual do Power BI pode conter código com riscos de segurança ou de privacidade. É importante confiar no autor e na fonte do visual do Power BI antes de importá-lo para o relatório.

## <a name="next-steps"></a>Próximas etapas

>[!div class="nextstepaction"]
>[Desenvolver um visual do Power BI](custom-visual-develop-tutorial.md)

>[!div class="nextstepaction"]
>[Estrutura de projeto de visuais do Power BI](visual-project-structure.md)

>[!div class="nextstepaction"]
>[Diretrizes para visuais do Power BI](guidelines-powerbi-visuals.md)

>[!div class="nextstepaction"]
>[Perguntas frequentes](power-bi-custom-visuals-faq.md)

>[!div class="nextstepaction"]
>[Comunidade do Power BI](https://community.powerbi.com/)