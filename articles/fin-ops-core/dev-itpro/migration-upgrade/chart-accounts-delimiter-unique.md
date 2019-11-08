---
title: Gera skiltákn bókhaldslykils einkvæmt
description: Þetta efni útskýrir hvernig ekki er hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Þú verður að breyta gildum skiltákns eftir uppfærslu.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 5861bcaa42f7bc5ec20916fe1a44418bdd9c2ffe
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550909"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gera skiltákn bókhaldslykils einkvæmt

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics AX 2012 er hægt að nota sama skiltáknið fyrir bókhaldslykil og víddargildi. Í núverandi útgáfum af Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Ef tvítekið skiltákn er til staðar er hægt að breyta því eftir uppfærslu. 

Þessi eiginleiki er ekki í boði eftirfarandi útgáfum:
- Finance and Operations, útgáfu 8.0
- Finance and Operations, útgáfu 7.1, KB 4094701 Ekki er hægt að slá inn fjárhagsvíddir þegar víddargildin innihalda skiltákn bókhaldslykils
- Finance and Operations, útgáfu 7.2, KB 4092967 Ekki er hægt að velja undirverk sem vídd þegar snið undirverks inniheldur víddarskiltákn

## <a name="update-delimiter"></a>Uppfæra skiltákn
Ef það er ósamræmi milli bókhaldslykils, skiltákni bókhaldslykils og kenni verks/undirverks er hægt að breyta sniði. Ekki er hægt að breyta öðrum víddarskiltáknum. 
- Hægt er að breyta skiltákni bókhaldslykils eftir uppfærslu í **Færibreytur fjárhags** > **Bókhaldslyklar og víddir** > **Breyta skiltákni**. 
- Ef eina ósamræmið er sniðið fyrir kenni verks/undirverks er hægt að breyta því gildi í **Verkefnastjórnun og bókhaldfæribreytur** > **Almennt** > **Breyta sniði undirverks**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Hvernig á að ákvarða hvort umhverfið þitt krefst uppfærðra skiltákna 
Ef skiltákn í uppfærða umhverfinu þínu stangast á gætir þú fundið fyrir óstöðugleika þegar þú slærð inn gildi í sundurliðaðri innfærslustýringu eða víddarstýrðri innfærslu. Sem þýðir að alltaf þarf að nota uppflettingar eða hliðargluggavalmynd þegar slegnar eru inn lykla- og víddarsamsetningar.
