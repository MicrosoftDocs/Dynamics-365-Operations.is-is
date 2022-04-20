---
title: Gera skiltákn bókhaldslykils einkvæmt
description: Þetta efni útskýrir hvernig ekki er hægt að hafa sama skiltákn fyrir bókhaldslykil og víddargildi. Þú verður að breyta gildum skiltákns eftir uppfærslu.
author: panolte
ms.date: 04/13/2022
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
ms.openlocfilehash: 6081a62077f1fc6b6920991ed6faae667c25a47c
ms.sourcegitcommit: e8a2a1e34fa48a42afac9724828f4ec72b6d7085
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2022
ms.locfileid: "8573619"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Gera skiltákn bókhaldslykils einkvæmt

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics AX 2012 er hægt að nota sama skiltáknið fyrir bókhaldslykil og víddargildi. Í núverandi útgáfum af Finance and Operations er ekki hægt að hafa sömu afmörkun fyrir bókhaldsyfirlit og víddarheiti eða gildi. Ef tvítekið skiltákn er til staðar er hægt að breyta því eftir uppfærslu. 

## <a name="update-delimiter"></a>Uppfæra skiltákn
Ef það er ósamræmi milli bókhaldslykils, skiltákni bókhaldslykils og kenni verks/undirverks er hægt að breyta sniði. Ekki er hægt að breyta öðrum víddarskiltáknum. 
- Hægt er að breyta skiltákni bókhaldslykils eftir uppfærslu í **Færibreytur fjárhags** > **Bókhaldslyklar og víddir** > **Breyta skiltákni**. 
- Ef eina ósamræmið er sniðið fyrir kenni verks/undirverks er hægt að breyta því gildi í **Verkefnastjórnun og bókhaldfæribreytur** > **Almennt** > **Breyta sniði undirverks**. 

### <a name="other-considerations"></a>Annað sem skal hafa í huga
Líkt og auðkenni verks/undirverks, ættu allar aðrar aðalgagnafærslur sem notaðar eru sem fjárhagsvíddir, svo sem lánardrottnar eða viðskiptavinir, ekki að hafa reikningsauðkennisgildi sem nota sama staf og afmörkun bókhaldsyfirlits. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Hvernig á að ákvarða hvort umhverfið þitt krefst uppfærðra skiltákna 
Ef skiltákn í uppfærða umhverfinu þínu stangast á gætir þú fundið fyrir óstöðugleika þegar þú slærð inn gildi í sundurliðaðri innfærslustýringu eða víddarstýrðri innfærslu. Sem þýðir að alltaf þarf að nota uppflettingar eða hliðargluggavalmynd þegar slegnar eru inn lykla- og víddarsamsetningar.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
