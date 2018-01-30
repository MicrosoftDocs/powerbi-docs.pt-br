---
title: Conectar-se ao Mandrill com o Power BI
description: Mandrill para o Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 92b069bded7fc6a22480d8190c1b8d0f53f959e4
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-mandrill-with-power-bi"></a>Conectar-se ao Mandrill com o Power BI
O pacote de conteúdo do Power BI extrai dados de sua conta do Mandrill e gera um painel, um conjunto de relatórios e um conjunto de dados para permitir que você explore seus dados. Use a análise do Mandrill para obter informações rapidamente sobre sua campanha de boletim informativo e de marketing. Os dados são configurados para serem atualizados diariamente, garantindo que os dados que você está monitorando são atuais.

Conecte-se ao [pacote de conteúdo do Mandrill para o Power BI.](http://app.powerbi.com/getdata/services/mandrill)

## <a name="how-to-connect"></a>Como se conectar
1. Selecione **Obter Dados** na parte inferior do painel de navegação esquerdo.
   
    ![](media/service-connect-to-mandrill/getdata.png)
2. Na caixa **Serviços** , selecione **Obter**.
   
    ![](media/service-connect-to-mandrill/services.png)
3. Selecione **Mandrill** > **Obter**.
   
    ![](media/service-connect-to-mandrill/mandrill.png)
4. Como o **Método de Autenticação**, selecione **Chave** e forneça sua chave de API. Você pode encontrar a chave na guia **Configurações** no painel do Mandrill. Selecione **Entrar** para iniciar o processo de importação, que pode levar alguns minutos dependendo do volume de dados em sua conta.
   
    ![](media/service-connect-to-mandrill/auth.png)
5. Após o Power BI importar os dados, você verá novos elementos (painel, relatório e conjunto de dados) no painel de navegação esquerdo. Esse é o painel padrão criado pelo Power BI para exibir seus dados.
   
    ![](media/service-connect-to-mandrill/mandrill-dashboard1.jpg)

**E agora?**

* Tente [fazer uma pergunta na caixa de P e R](power-bi-q-and-a.md) na parte superior do dashboard
* [Altere os blocos](service-dashboard-edit-tile.md) no dashboard.
* [Selecione um bloco](service-dashboard-tiles.md) para abrir o relatório subjacente.
* Enquanto seu conjunto de dados será agendado para ser atualizado diariamente, você pode alterar o agendamento de atualização ou tentar atualizá-lo sob demanda usando **Atualizar Agora**

## <a name="next-steps"></a>Próximas etapas
[Introdução ao Power BI](service-get-started.md)

[Power BI – conceitos básicos](service-basic-concepts.md)
