---
title: Gera skiltákn bókhaldslykils einkvæmt
description: Í Dynamics 365 for Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Þú verður að breyta gildum skiltákns eftir uppfærslu.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559529"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gera skiltákn bókhaldslykils einkvæmt

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics AX 2012 er hægt að nota sama skiltáknið fyrir bókhaldslykil og víddargildi. Í Dynamics 365 for Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Ef tvítekið skiltákn er til staðar er hægt að breyta því eftir uppfærslu. 

Þessi eiginleiki er fáanlegur í:
- Dynamics 365 for Finance and Operations útgáfa 8.0
- Dynamics 365 for Finance and Operations útgáfa 7.1, KB 4094701 Ekki er hægt að slá inn fjárhagsvíddir þegar víddargildin innihalda skiltákn bókhaldslykils
- Dynamics 365 for Finance and Operations útgáfa 7.2, KB 4092967 Ekki er hægt að velja undirverk sem vídd þegar snið undirverks inniheldur víddarskiltákn

## <a name="update-delimiter"></a>Uppfæra skiltákn
Ef það er ósamræmi milli bókhaldslykils, skiltákni bókhaldslykils og kenni verks/undirverks er hægt að breyta sniði. Ekki er hægt að breyta öðrum víddarskiltáknum. 
- Hægt er að breyta skiltákni bókhaldslykils eftir uppfærslu á Finance and Operations í **Færibreytur fjárhags** > **Bókhaldslyklar og víddir** > **Breyta skiltákni**. 
- Ef eina ósamræmið er sniðið fyrir kenni verks/undirverks er hægt að breyta því gildi í **Verkefnastjórnun og bókhaldfæribreytur** > **Almennt** > **Breyta sniði undirverks**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Hvernig á að ákvarða hvort umhverfið þitt krefst uppfærðra skiltákna 
Ef skiltákn í uppfærða umhverfinu þínu stangast á gætir þú fundið fyrir óstöðugleika þegar þú slærð inn gildi í sundurliðaðri innfærslustýringu eða víddarstýrðri innfærslu. Sem þýðir að alltaf þarf að nota uppflettingar eða hliðargluggavalmynd þegar slegnar eru inn lykla- og víddarsamsetningar.
