---
title: Gerenciar sua fonte de dados –SQL
description: Como gerenciar o gateway de dados local e as fontes de dados que pertencem ao gateway.
author: arthiriyer
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 07/15/2019
ms.author: arthii
LocalizationGroup: Gateways
ms.openlocfilehash: 851b7645a9e0b5aa09ba9fff4f71abeb79b67dfc
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85237002"
---
# <a name="manage-your-data-source---sql-server"></a>Gerenciar sua fonte de dados – SQL Server

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

Depois de [instalar o gateway de dados local](/data-integration/gateway/service-gateway-install), você pode [adicionar fontes de dados](service-gateway-data-sources.md#add-a-data-source) que possam ser usadas com o gateway. Este artigo aborda como trabalhar com gateways e fontes de dados SQL Server que são usadas para a atualização agendada ou para o DirectQuery.

## <a name="add-a-data-source"></a>Adicionar uma fonte de dados

Para obter mais informações sobre como adicionar uma fonte de dados, consulte [Adicionar uma fonte de dados](service-gateway-data-sources.md#add-a-data-source). Em **Tipo de Fonte de Dados**, selecione **SQL Server**.

![Selecionar a fonte de dados do SQL Server](media/service-gateway-enterprise-manage-sql/datasourcesettings2.png)

> [!NOTE]
> Quando você usa o DirectQuery, o gateway dá suporte apenas ao **SQL Server 2012 SP1** e a versões posteriores.

Em seguida, preencha as informações sobre a fonte de dados, que incluem o **Servidor** e o **Banco de Dados**. 

Em **Método de Autenticação**, escolha **Windows** ou **Básico**. Escolha **Básico** se você planeja usar a autenticação do SQL em vez da autenticação do Windows. Em seguida, insira as credenciais que serão usadas para esta fonte de dados.

> [!NOTE]
> Todas as consultas à fonte de dados serão executadas com essas credenciais, a menos que o SSO (logon único) do Kerberos esteja configurado e habilitado para a fonte de dados. Com SSO, conjuntos de dados de importação usam as credenciais armazenadas, mas conjuntos de dados de DirectQuery usam o usuário atual do Power BI para executar consultas usando o SSO. Para saber mais sobre como as credenciais são armazenadas, confira [Armazenar credenciais criptografadas na nuvem](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud). Ou confira o artigo que descreve como [Usar o Kerberos para logon único (SSO) do Power BI para fontes de dados locais](service-gateway-sso-kerberos.md).

![Preencher as configurações de fonte de dados](media/service-gateway-enterprise-manage-sql/datasourcesettings3.png)

Depois de preencher tudo, selecione **Adicionar**. Agora você pode usar esta fonte de dados para atualização agendada ou para o DirectQuery em um SQL Server local. Você verá *Conexão Bem-sucedida* se tiver êxito.

![Exibindo o status da conexão](media/service-gateway-enterprise-manage-sql/datasourcesettings4.png)

### <a name="advanced-settings"></a>Configurações avançadas

Opcionalmente, você pode configurar o nível de privacidade para sua fonte de dados. Essa configuração controla como os dados podem ser combinados. Ela é usada somente para a atualização agendada. A configuração de nível de privacidade não se aplica ao DirectQuery. Para saber mais sobre os níveis de privacidade para sua fonte de dados, confira [Níveis de privacidade (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540).

![Definir o nível de privacidade](media/service-gateway-enterprise-manage-sql/datasourcesettings9.png)

## <a name="use-the-data-source"></a>Usar a fonte de dados

Depois de criar a fonte de dados, ela está disponível para uso com as conexões do DirectQuery ou por meio da atualização agendada.

> [!NOTE]
> Os nomes do servidor e do banco de dados devem corresponder entre o Power BI Desktop e a fonte de dados no gateway de dados local.

O vínculo entre o conjunto de dados e a fonte de dados no gateway baseia-se nos nomes do servidor e do banco de dados. Esses nomes devem corresponder. Por exemplo, se você fornecer um endereço IP como nome do servidor no Power BI Desktop, precisará usar o endereço IP como fonte de dados na configuração do gateway. Se usar *SERVER\INSTANCE* no Power BI Desktop, você também precisará usar o mesmo na fonte de dados configurada para o gateway.

Esse requisito existe para o DirectQuery e para a atualização agendada.

### <a name="use-the-data-source-with-directquery-connections"></a>Usar a fonte de dados com conexões do DirectQuery

Verifique se os nomes do servidor e do banco de dados correspondem entre o Power BI Desktop e a fonte de dados configurada para o gateway. Para que seja possível publicar os conjuntos de dados do DirectQuery, você também precisa verificar se o usuário está listado na guia **Usuários** da fonte de dados. A seleção para o DirectQuery ocorre no Power BI Desktop quando você importa dados pela primeira vez. Para obter mais informações sobre como usar o DirectQuery, consulte [Usar o DirectQuery no Power BI Desktop](desktop-use-directquery.md).

Após a publicação, por meio do Power BI Desktop ou do recurso **Obter Dados**, seus relatórios deverão começar a funcionar. Pode levar vários minutos após a criação da fonte de dados no gateway para que a conexão seja utilizável.

### <a name="use-the-data-source-with-scheduled-refresh"></a>Usar a fonte de dados com a atualização agendada

Se estiver listado na guia **Usuários** da fonte de dados configurada no gateway e houver a correspondência entre os nomes do servidor e do banco de dados, você verá o gateway como uma opção a ser usada com a atualização agendada.

![Exibir os usuários](media/service-gateway-enterprise-manage-sql/powerbi-gateway-enterprise-schedule-refresh.png)

## <a name="next-steps"></a>Próximas etapas

* [Conectar-se a dados locais no SQL Server](service-gateway-sql-tutorial.md)
* [Solução de problemas do gateway de dados local](/data-integration/gateway/service-gateway-tshoot)
* [Solucionar problemas de gateways – Power BI](service-gateway-onprem-tshoot.md)
* [Usar o Kerberos para logon único (SSO) do Power BI para fontes de dados locais](service-gateway-sso-kerberos.md)

Mais perguntas? Experimente perguntar à [Comunidade do Power BI](https://community.powerbi.com/).
