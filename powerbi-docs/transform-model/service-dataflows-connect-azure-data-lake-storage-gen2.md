---
title: Saiba como conectar o Azure Data Lake Storage Gen 2 ao Power BI para o armazenamento de fluxo de dados
description: Traga seus próprios dados para fluxos de dados usando o Azure Data Lake Storage Gen2
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: how-to
ms.date: 01/22/2020
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: d6301b4eea49ab4ae5714446e051290cb254c324
ms.sourcegitcommit: caf60154a092f88617eb177bc34fb784f2365962
ms.contentlocale: pt-BR
ms.lasthandoff: 06/25/2020
ms.locfileid: "85354744"
---
# <a name="connect-azure-data-lake-storage-gen2-for-dataflow-storage"></a>Conectar-se ao Azure Data Lake Storage Gen2 para armazenamento de fluxo de dados

Você pode configurar os workspaces do Power BI para armazenar fluxos de dados na conta do Azure Data Lake Storage Gen2 da sua organização. Este artigo descreve as etapas gerais necessárias para fazer isso e fornece diretrizes e práticas recomendadas ao longo do caminho. Há algumas vantagens em configurar workspaces para armazenar definições de fluxo de dados e arquivos de dados no data lake, incluindo as seguintes:

* O Azure Data Lake Storage Gen2 fornece um local de armazenamento extremamente escalonável para os dados
* Os arquivos de definição e de dados de fluxo de dados podem ser usados pelos desenvolvedores de seu departamento de TI para aproveitar os serviços de IA (inteligência artificial) e dados do Azure, conforme demonstrado nas [amostras do GitHub dos Serviços de Dados do Azure](https://aka.ms/cdmadstutorial)
* Permite que os desenvolvedores na sua organização integrem dados de fluxo de dados a aplicativos internos e soluções de linha de negócios, usando recursos de desenvolvedor para fluxos de dados e Azure

Para usar o Azure Data Lake Storage Gen2 para fluxo de dados, é necessário o seguinte:

* **Locatário do Power BI:** pelo menos uma conta no seu locatário do AAD (Azure Active Directory) precisa estar inscrita no Power BI
* **Uma conta de administrador global:** essa conta é necessária para conectar e configurar o Power BI para armazenar a definição e os dados de fluxo de dados na sua conta do Azure Data Lake Storage Gen2
* **Uma assinatura do Azure:** você precisa de uma assinatura do Azure para usar o Azure Data Lake Storage Gen2
* **Grupo de recursos:** use um grupo de recursos que você já tem ou crie um novo
* **Uma conta de Armazenamento do Azure com o recurso Data Lake Storage Gen2 habilitado** 

> [!TIP]
> Se você não tiver uma assinatura do Azure, crie uma [conta gratuita](https://azure.microsoft.com/free/) antes de começar.

> [!WARNING]
> Depois que um local de armazenamento de fluxo de dados for configurado, ele não poderá ser alterado. Confira a seção [Considerações e limitações](#considerations-and-limitations) ao fim deste artigo para saber quais outros elementos importantes devem ser considerados.

## <a name="prepare-your-azure-data-lake-storage-gen2-for-power-bi"></a>Preparar seu Azure Data Lake Storage Gen2 para o Power BI

Antes de configurar o Power BI com uma conta do Azure Data Lake Storage Gen2, você deve criar e configurar uma conta de armazenamento. Vamos examinar os requisitos para o Power BI:

1. É necessário ser o proprietário da conta de armazenamento do ADLS. Isso precisa ser atribuído no nível de recurso, e não herdado do nível de assinatura.
2. A conta de armazenamento deve ser criada no mesmo locatário do AAD que seu locatário do Power BI.
3. A conta de armazenamento deve ser criada na mesma região do AAD que seu locatário do Power BI. Para determinar onde seu locatário do Power BI está localizado, confira o artigo [Onde meu locatário do Power BI está localizado](../admin/service-admin-where-is-my-tenant-located.md).
4. A conta de armazenamento deve ter o recurso *Namespace hierárquico* habilitado.

As seções a seguir percorrem as etapas necessárias para configurar sua conta do Azure Data Lake Storage Gen2 detalhadamente.

### <a name="create-the-storage-account"></a>Criar a conta de armazenamento

Siga as etapas do artigo [Criar uma conta de armazenamento do Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-quickstart-create-account).

1. Certifique-se de selecionar o mesmo local que o do locatário do Power BI e defina seu armazenamento como **StorageV2 (uso geral v2)**
2. Não deixe de habilitar o recurso de namespace hierárquico
3. É recomendável definir a configuração de replicação como **armazenamento com redundância geográfica com acesso de leitura (RA-GRS)**

### <a name="grant-permissions-to-power-bi-services"></a>Conceder permissões para serviços do Power BI

Em seguida, você precisa conceder ao serviço do Power BI as funções de leitor e acesso a dados na conta de armazenamento criada. Eles são funções internas, portanto, as etapas são simples. 

Siga as etapas em [Atribuir uma função RBAC interna](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac#assign-a-built-in-rbac-role).

Na janela **Adicionar atribuição de função** selecione a função **Leitor e Acesso a Dados**. Em seguida, use a opção pesquisar para localizar o aplicativo **Serviço do Power BI**.
Repita as mesmas etapas para a função **Proprietário de Dados do Blob de Armazenamento** e atribua a função aos aplicativos **Serviço do Power BI** e **Power BI Premium**.

> [!NOTE]
> Aguarde pelo menos 30 minutos para que a permissão seja propagada para o Power BI no Portal. Sempre que você alterar as permissões no portal, aguarde 30 minutos para que elas sejam refletidas no Power BI. 

## <a name="connect-your-azure-data-lake-storage-gen2-to-power-bi"></a>Conectar seu Azure Data Lake Storage Gen2 ao Power BI

Depois de configurar sua conta do Azure Data Lake Storage Gen2 no portal do Azure, conecte-a ao Power BI no **portal de administração do Power BI**. Também é possível gerenciar o armazenamento de fluxo de dados do Power BI na seção de configurações do **Armazenamento de fluxo de dados** do portal de administração do Power BI. Para ver orientações detalhadas sobre inicialização e uso básico, consulte [Como chegar ao Portal de administração](../admin/service-admin-portal.md).

Conecte-se à sua conta do **Azure Data Lake Storage Gen2** com as seguintes etapas:

1. Navegue até a guia **Configurações de fluxo de dados** no **portal de administração do Power BI**

    ![Portal de administração do Power BI](media/service-dataflows-connect-azure-data-lake-storage-gen2/dataflows-connect-08b.png) 

2. Selecione o botão **Conectar-se ao Azure Data Lake Storage Gen2**. A janela a seguir é exibida.

    ![Azure Data Lake Storage Gen2](media/service-dataflows-connect-azure-data-lake-storage-gen2/dataflows-connect-adlsg2_09.jpg) 

3. Forneça a **ID da assinatura** da conta de armazenamento.
4. Forneça o **nome do grupo de recursos** em que a conta de armazenamento foi criada.
5. Fornecer o **nome da conta de armazenamento**.
6. Selecione **Conectar**.

Depois que essas etapas forem concluídas com êxito, sua conta do Azure Data Lake Storage Gen2 estará conectada ao Power BI. 

> [!NOTE]
> Você precisa ter permissões de Administrador Global para configurar uma conexão do Azure Data Lake Storage Gen2 no portal de administração do Power BI. No entanto, os Administradores Globais não podem conectar o armazenamento externo no portal de administração.  

Em seguida, você precisa permitir que as pessoas da sua organização configurem os workspaces, o que possibilita que elas utilizem essa conta de armazenamento para definição de fluxo de dados e armazenamento de dados. Vamos fazer isso na próxima seção. 


## <a name="allow-admins-to-assign-workspaces"></a>Permitir que os administradores atribuam workspaces

Por padrão, os arquivos de dados e a definição de fluxo de dados são armazenados no armazenamento fornecido pelo Power BI. Para acessar arquivos de fluxo de dados em sua própria conta de armazenamento, os administradores do workspace devem primeiro configurar o workspace para permitir atribuição e armazenamento de fluxos de dados na nova conta de armazenamento. Antes que um administrador do workspace possa definir configurações de armazenamento de fluxo de dados, ele precisa receber permissões de atribuição de armazenamento no **Portal de administração do Power BI**.

Para conceder permissões de atribuição de armazenamento, vá para a guia **Configurações de fluxo de dados** no **portal de administração do Power BI**. Há um botão de opção para *Permitir que os administradores do workspace atribuam workspaces para esta conta de armazenamento*, que deve ser definido como **permitir**. Depois de habilitar esse controle deslizante, selecione o botão **Aplicar** para que a alteração tenha efeito. 

![Permitir que os administradores atribuam workspaces](media/service-dataflows-connect-azure-data-lake-storage-gen2/dataflows-connect-adlsg2_10.jpg) 

Isso é tudo. Os administradores do workspace do Power BI agora podem atribuir os fluxos de trabalho ao sistema de arquivos criado.


## <a name="considerations-and-limitations"></a>Considerações e limitações

Esta é uma versão prévia do recurso, e o comportamento dela pode mudar conforme o lançamento se aproxima. Há algumas considerações e limitações para ter em mente ao trabalhar com o armazenamento de fluxo de dados:

* Depois que um local de armazenamento de fluxo de dados for configurado, ele não poderá ser alterado.
* Somente os proprietários de um fluxo de dados armazenado no Azure Data Lake Storage Gen2 pode acessar seus dados por padrão. Para autorizar outras pessoas a acessarem os fluxos de dados armazenados no Azure, adicione-as à pasta do CDM do fluxo de dados 
* A criação de fluxos de dados com entidades vinculadas só é possível quando elas são armazenados na mesma conta de armazenamento
* Não há suporte para fontes de dados local, em capacidades compartilhadas do Power BI, em fluxos de dados armazenados no data lake da sua organização
* Os instantâneos não são excluídos automaticamente no ADLS Gen 2. Se você quiser liberar espaço, poderá criar uma função do Azure para limpar periodicamente os instantâneos antigos.

Também há alguns problemas conhecidos, conforme descrito nesta seção.

Os clientes do Power BI Desktop não podem acessar os fluxos de dados armazenados em uma **conta do Azure Data Lake Storage**, a menos que sejam os proprietários do fluxo de dados ou tenham sido autorizados a acessar a pasta do CDM no lake. O cenário é descrito a seguir:

1. Brenda criou um workspace e o configurou para armazenar fluxos de dados no data lake da organização. 
2. Davi, que também é membro do workspace criado por Brenda, deseja usar o Power BI Desktop e o conector de fluxo de dados para obter dados do fluxo de dados criado por Brenda.
3. Davi recebe um erro semelhante, porque não foi autorizado a acessar a pasta do CDM do fluxo de dados no lake.

Perguntas e respostas comuns incluem as seguintes:

**Pergunta:** E se eu tivesse criado anteriormente fluxos de dados em um workspace e quisesse alterar o local de armazenamento?

**Resposta:** Não é possível alterar o local de armazenamento de um fluxo de dados depois que ele foi criado. 

**Pergunta:** Quando posso alterar o local de armazenamento do fluxo de dados de um workspace?

**Resposta:** A alteração do local de armazenamento do fluxo de dados de um workspace só será permitida se o workspace não contiver nenhum fluxo de dados.


## <a name="next-steps"></a>Próximas etapas

Este artigo fornece orientações sobre como se conectar a um Azure Data Lake Gen2 para armazenamento de fluxo de dados. Para saber mais, confira os seguintes artigos:

Para saber mais sobre fluxos de dados, CDM e o Azure Data Lake Storage Gen2, confira os seguintes artigos:

* [Integração entre fluxos de dados e o Azure Data Lake (versão prévia)](service-dataflows-azure-data-lake-integration.md)
* [Definir configurações de fluxo de dados de workspace (versão prévia)](service-dataflows-configure-workspace-storage-settings.md)
* [Adicionar uma pasta do CDM ao Power BI como um fluxo de dados (versão prévia)](service-dataflows-add-cdm-folder.md)

Para saber mais sobre fluxos de dados em geral, confira estes artigos:

* [Criação e uso de fluxos de dados no Power BI](service-dataflows-create-use.md)
* [Como usar entidades computadas no Power BI Premium](service-dataflows-computed-entities-premium.md)
* [Como usar fluxos de dados com fontes de dados locais](service-dataflows-on-premises-gateways.md)
* [Recursos de desenvolvedor para fluxos de dados do Power BI](service-dataflows-developer-resources.md)

Para saber mais sobre o armazenamento do Azure, você pode ler estes artigos:
* [Guia de segurança do Armazenamento do Microsoft Azure](https://docs.microsoft.com/azure/storage/common/storage-security-guide)

Leia este artigo de visão geral para saber mais sobre o Common Data Service:
* [Common Data Service - visão geral ](https://docs.microsoft.com/powerapps/common-data-model/overview)
* [Pastas do CDM](https://go.microsoft.com/fwlink/?linkid=2045304)
* [Definição de arquivo de modelo do CDM](https://go.microsoft.com/fwlink/?linkid=2045521)

E você pode sempre tentar [fazer perguntas à Comunidade do Power BI](https://community.powerbi.com/).
