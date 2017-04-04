---
title: "Sléttun upphæða fyrir afskriftaútreikninga."
description: "Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 0cb514dfb8c37b8c027ab895cb970af1b0135bf0
ms.lasthandoff: 03/31/2017


---

# <a name="round-off-amount-for-depreciation-calculations"></a>Sléttun upphæða fyrir afskriftaútreikninga.

Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.

Slétta afskriftarupphæðir eru sett fyrir hvert. Slétta afskriftarupphæðir eru notaðar í afskriftaregla eigna sem sýnir afskriftina í framtíðinni og gildi fyrir eignina og einnig í afskriftartillögur. Færið inn lægstu leyfilegu upphæðina til afskriftar fyrir þetta bók. 

Óháð því hvaða sléttun er sett upp verður afskriftarupphæðin í síðasta afskriftartímabilinu ekki sléttuð. Við lok síðasta afskriftartímabilsins, verður virði eignar að vera 0 (núll) eða á rýrnunarvirði ef rýrnunarvirði er notað.

### <a name="example"></a>Dæmi

Afskrift án sléttunar er reiknuð sem 2.444,44. Mismunandi upphæðir eru lagðar til eftir því hvaða sléttun er sett upp, eins og sýnt er í töflunni.

| Sléttunaraðferð | Afskriftarupphæð |
|-----------------|---------------------|
| Sléttun 0,1    | 2.444,40            |
| Sléttun 1,00   | 2.444,00            |
| Sléttun 10,00  | 2.440,00            |
| Sléttun 100,00 | 2.400,00            |




