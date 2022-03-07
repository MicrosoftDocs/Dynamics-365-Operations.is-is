---
title: Gera skiltákn bókhaldslykils einkvæmt
description: Þetta efni útskýrir hvernig ekki er hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Þú verður að breyta gildum skiltákns eftir uppfærslu.
author: panolte
ms.date: 09/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: a19dc8926df0efeac242e2e42ac37fdad91df9f8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500504"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gera skiltákn bókhaldslykils einkvæmt

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics AX 2012 er hægt að nota sama skiltáknið fyrir bókhaldslykil og víddargildi. Í núverandi útgáfu af Finance and Operations er ekki hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Ef tvítekið skiltákn er til staðar er hægt að breyta því eftir uppfærslu. 

## <a name="update-delimiter"></a>Uppfæra skiltákn
Ef það er ósamræmi milli bókhaldslykils, skiltákni bókhaldslykils og kenni verks/undirverks er hægt að breyta sniði. Ekki er hægt að breyta öðrum víddarskiltáknum. 
- Hægt er að breyta skiltákni bókhaldslykils eftir uppfærslu í **Færibreytur fjárhags** > **Bókhaldslyklar og víddir** > **Breyta skiltákni**. 
- Ef eina ósamræmið er sniðið fyrir kenni verks/undirverks er hægt að breyta því gildi í **Verkefnastjórnun og bókhaldfæribreytur** > **Almennt** > **Breyta sniði undirverks**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Hvernig á að ákvarða hvort umhverfið þitt krefst uppfærðra skiltákna 
Ef skiltákn í uppfærða umhverfinu þínu stangast á gætir þú fundið fyrir óstöðugleika þegar þú slærð inn gildi í sundurliðaðri innfærslustýringu eða víddarstýrðri innfærslu. Sem þýðir að alltaf þarf að nota uppflettingar eða hliðargluggavalmynd þegar slegnar eru inn lykla- og víddarsamsetningar.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
