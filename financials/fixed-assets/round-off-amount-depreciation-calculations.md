---
title: "Sléttun upphæða fyrir afskriftaútreikninga."
description: "Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8d5a9d9267c14ee045388c3b3b42b26f2fff45ea
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a>Sléttun upphæða fyrir afskriftaútreikninga.

[!include[banner](../includes/banner.md)]


Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.

Slétta afskriftarupphæðir eru sett fyrir hverja bók. Sléttun afskriftarupphæða er notuð í afskriftareglu eigna sem sýnir afskriftina í framtíðinni og gildi fyrir eignina og einnig í afskriftartillögum. Færið inn lægstu leyfilegu upphæðina til afskriftar fyrir þetta bók. 

Óháð því hvaða sléttun er sett upp verður afskriftarupphæðin í síðasta afskriftartímabilinu ekki sléttuð. Við lok síðasta afskriftartímabilsins, verður virði eignar að vera 0 (núll) eða á rýrnunarvirði ef rýrnunarvirði er notað.

### <a name="example"></a>Dæmi

Afskrift án sléttunar er reiknuð sem 2.444,44. Mismunandi upphæðir eru lagðar til eftir því hvaða sléttun er sett upp, eins og sýnt er í töflunni.

| Sléttunaraðferð | Afskriftarupphæð |
|-----------------|---------------------|
| Sléttun 0,1    | 2.444,40            |
| Sléttun 1,00   | 2.444,00            |
| Sléttun 10,00  | 2.440,00            |
| Sléttun 100,00 | 2.400,00            |






