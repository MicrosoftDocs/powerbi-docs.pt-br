---
title: O que é administração do Power BI?
description: Saiba mais sobre a configuração das políticas de governança do Power BI, monitoramento de uso, provisionamento de licenças, capacidades e recursos organizacionais.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: overview
ms.date: 09/09/2019
ms.author: kfollis
LocalizationGroup: Administration
ms.openlocfilehash: afa8513267be4ec2de18a9adda7995c88f4f2aa8
ms.sourcegitcommit: 6ba7cc9afaf91229f717374bc0c12f0b8201d15e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2020
ms.locfileid: "83438029"
---
# <a name="what-is-power-bi-administration"></a>O que é administração do Power BI?

A administração do Power BI é o gerenciamento de um locatário do Power BI, incluindo a configuração de políticas de governança, monitoramento de uso, provisionamento de licenças, capacidades e recursos organizacionais. Este artigo fornece uma visão geral de funções de administração, tarefas e ferramentas, além de links para artigos que oferecem mais detalhes.

![Portal de administração do Power BI](media/service-admin-administering-power-bi-in-your-organization/admin-portal.png)

O Power BI foi projetado para business intelligence de autoatendimento e o administrador é o responsável pelos dados, pelos processos e pelas políticas no locatário do Power BI. Um administrador do Power BI é um membro essencial de uma equipe que inclui os desenvolvedores de BI, analistas e outras funções. O administrador pode ajudar a dar suporte a uma organização para garantir que objetivos críticos sejam atendidos:

- Entender os KPIs e as métricas de que os usuários _realmente_ precisam.
- Diminuir o tempo de entrega para relatórios corporativo orientados por TI.
- Aumentar a adoção e o retorno sobre o investimento de uma implantação do Power BI.

O trabalho é tornar os usuários empresariais produtivos e garantir a segurança e a conformidade com as leis e os regulamentos. As responsabilidades podem incluir a ajuda e o suporte e, em muitos casos, ajudar os usuários corporativos a fazerem a coisa certa.

## <a name="administrator-roles-related-to-power-bi"></a>Funções de administrador relacionadas ao Power BI

Há várias funções relacionadas à administração do Power BI, que são abordadas na tabela a seguir.

| **Tipo de administrador** | **Escopo administrativo** | **Escopo do Power BI** |
| --- | --- | --- |
| Administrador global | Microsoft 365 | Pode gerenciar todos os aspectos de um locatário do Power BI e outros serviços. |
| Administrador de cobrança | Microsoft 365 | Pode adquirir licenças do Power BI por meio de assinaturas do Office 365. |
| Administrador de serviços do Power BI | Locatário do Power BI | Tem controle total sobre um locatário do Power BI e seus recursos administrativos (com exceção de licenciamento). |
| Administrador de capacidade do Power BI Premium | Uma única capacidade Premium | Tem controle total sobre a capacidade de premium e seus recursos administrativos. |
| Administrador de capacidade do Power BI Embedded | Uma única capacidade Embedded | Tem controle total sobre a capacidade Embedded e seus recursos administrativos. |

Os administradores globais no Microsoft 365 ou no Azure Active Directory têm direitos de administrador no Power BI. Um administrador global pode atribuir outros usuários à função de Administrador de serviços do Power BI, que concede direitos administrativos apenas sobre os recursos do Power BI.

Os administradores de serviços do Power BI têm acesso ao portal de administração do Power BI, que inclui várias configurações de locatário em relação a funcionalidade, segurança e monitoramento. Os administradores de serviços têm acesso completo a todos os recursos de um locatário do Power BI. Na maioria dos casos, os administradores de serviço identificam problemas e, em seguida, acompanham os proprietários de recursos para executar ações corretivas.

A função de Administrador de serviços do Power BI não concede a capacidade de atribuir licenças a usuários ou exibir logs de auditoria no Microsoft 365. Portanto, a tarefa de administrar o Power BI atualmente não pode ser executada por usuários que são somente membros da função de administrador de serviços do Power BI.

## <a name="administrative-tasks"></a>Tarefas administrativas

Os administradores realizam várias tarefas para dar suporte ao Power BI para sua organização, que são abordadas na tabela a seguir.

| **Área de tarefa** | **Tarefas comuns** |
| --- | --- |
| Gerenciar o locatário do Power BI |<ul><li>Habilitar e desabilitar os principais recursos do Power BI<br><li>Criar relatórios sobre uso e desempenho<br><li>Analisar e gerenciar a auditoria de eventos</ul>|
| Adquirir e atribuir licenças do Power BI |<ul><li>Gerenciar a inscrição do usuário<br><li>Comprar e atribuir licenças Pro<br><li>Impedir que os usuários acessem o Power BI</ul>|
| Gerenciar a capacidade Premium |<ul><li>Adquirir e trabalhar com a capacidade Premium<br><li>Garantir a qualidade do serviço|
| Gerenciar a capacidade Embedded |<ul><li>Adquirir a capacidade Embedded para simplificar como os ISVs e os desenvolvedores usam recursos do Power BI</ul>|
| Garantir a conformidade com políticas internas, leis e regulamentos | <ul><li>Gerenciar a classificação de dados de negócios<br><li>Ajudar a impor políticas de publicação e compartilhamento de conteúdo</ul>|
| Gerenciar recursos do Power BI |<ul><li>Gerenciar workspaces<br><li>Publicar visuais do Power BI<br><li>Verificar os códigos usados para inserir o Power BI em outros aplicativos|
| Fornecer ajuda e suporte para usuários de locatário |<ul><li>Solucionar problemas de acesso a dados e outros problemas</ul>|
| Outras tarefas |<ul><li>Implantar o Power BI Desktop, por exemplo, usando o Microsoft Endpoint Configuration Manager<br><li>Gerenciar a implantação de aplicativos móveis do Power BI com o Intune<br><li>Gerenciar a privacidade e a segurança dos dados, como segurança de dados de origem</ul>|

## <a name="administrative-tools"></a>Ferramentas administrativas

Há várias ferramentas relacionadas à administração do Power BI, que são abordadas na tabela a seguir. Normalmente, os administradores passam a maior parte do tempo no portal de administração do Power BI e usam outras ferramentas conforme o necessário.

| **Ferramenta** | **Tarefas comuns** |
| --- | --- |
| Portal de administração do Power BI |<ul><li>Adquirir e trabalhar com a capacidade Premium</li><li>Garantir a qualidade do serviço</li><li>Gerenciar a classificação de dados de negócios</li><li>Ajudar a impor políticas de publicação e compartilhamento de conteúdo</li><li>Gerenciar workspaces<br><li>Publicar visuais do Power BI</li><li>Verificar os códigos usados para inserir o Power BI em outros aplicativos</li><li>Solucionar problemas de acesso a dados e outros problemas</li></ul>|
| Centro de administração do Microsoft 365 |<ul><li>Gerenciar a inscrição do usuário</li><li>Comprar e atribuir licenças Pro</li><li>Impedir que os usuários acessem o Power BI</li></ul>|
| Central de Segurança e Conformidade do Office 365 |<ul><li>Analisar e gerenciar a auditoria de eventos</li></ul>|
| Azure Active Directory (AAD) no portal do Azure |<ul><li>Configurar o acesso condicional a recursos do Power BI por meio do AAD</li><li>Provisionar a capacidade do Power BI Embedded</li></ul>|
| Cmdlets do PowerShell |<ul><li>Gerenciar workspaces e outros aspectos do Power BI por meio de scripts</li></ul>|
| APIs administrativas e SDK |<ul><li>Criar ferramentas administrativas personalizadas para facilitar o trabalho de um administrador do Power BI. Por exemplo, o Power BI Desktop pode usar essas APIs para criar relatórios com base nos dados relacionados à administração</li></ul>|

## <a name="next-steps"></a>Próximas etapas

Esperamos que este artigo tenha dado a você algumas ideias práticas sobre o trabalho e as funções do administrador do Power BI, as tarefas e as ferramentas específicas que estão envolvidas. Para saber mais, recomendamos os artigos a seguir.

- [Usar o portal de administração do Power BI](service-admin-portal.md)
- [Diretrizes de configuração do administrador de locatários](../guidance/admin-tenant-settings.md)
- [Usar cmdlets do PowerShell](/powershell/power-bi/overview)
- [Perguntas frequentes de administração do Power BI](service-admin-faq.md)
- Dúvidas? [Experimente perguntar à Comunidade do Power BI](https://community.powerbi.com/)
- Sugestões? [Contribuir com ideias para aprimorar o Power BI](https://ideas.powerbi.com/)
