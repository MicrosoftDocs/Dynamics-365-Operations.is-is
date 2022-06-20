---
title: Sléttun upphæða fyrir afskriftaútreikninga.
description: Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93842f7cca483df89188695c945edf77e118cef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870105"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Sléttun upphæða fyrir afskriftaútreikninga.

[!include [banner](../includes/banner.md)]

Þessi grein fjallar um **Heildarafskriftir** reit sem er að finna á **Uppsetning bóka** síður.

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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
