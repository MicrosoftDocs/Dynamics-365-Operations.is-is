---
title: "Afhendingaráætlanir"
description: "Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: fbada697060c823b0afdb72d1c0cfd8703f4d527
ms.lasthandoff: 03/31/2017


---

# <a name="delivery-schedules"></a>Afhendingaráætlanir

Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun.

Nota afhendingaráætlun þegar verður að vera afhent heildarmagn á línu í pöntun eða tilboðslínu í margar sendingar. Einstökum sendingum er táknuð með afhendingarlínur. Tvær eða fleiri afhendingarlínur mynda eina afhendingaráætlun. Afhendingarlínur getur haft mismunandi afhendingardagsetningar, magn, afhendingarmáta og geymsluvíddir, eins og svæði og vöruhús.  

**Dæmi um afhendingaráætlun**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Heildarpöntun (upprunalegu pöntunarlína) | 600 stólar                               |
| Umbeðin afhendingaráætlun       | 100 stólar á mánuði                     |
| Umbeðinn tímarammi fyrir afhendingu | 6 mánuðir, á fyrsta degi hvers mánaðar |

Í þessu dæmi biður viðskiptavinur um afhendingu á 600 stólum í runum með 100 stólum yfir sex mánaða tímabil. Til að rekja afhendingarkröfur skal stofna afhendingaráætlun. Á síðunni Afhendingaráætlun skal stofna sex aðskildar afhendingarlínur. Hver afhendingarlína inniheldur 100 stóla og tekur fram afhendingardag fyrir þessa 100 stóla. Í þessu tilfelli er hver lína mótfærsla fyrsta mánaðar fyrir sex samfellda mánuði.  

Þegar þú stofnar afhendingaráætlun er gerð upprunalegrar pöntunarlínu sjálfkrafa breytt í **Sölupöntunarlínu með margar afhendingar**. Lína af þessari gerð kallast viðskiptalína og er merkt með tákni. Afhendingarlínan er merkt með öðru tákni. Ef magni í afhendingarlínu heildarsöluverðmæti línan er uppfærð heildarmagn afhendingaráætlunar. Ef viðskiptasamningur hefur skilgreint heildarafsláttar fyrir pöntunina, tryggir afhendingaráætlunar pöntunin er hæfur fyrir lokaafsláttur, jafnvel þegar pöntun er skipt í sérstök afhendingar.  

Pantanir sem hafa afhendingaráætlun eru unnar gegn afhendingarlínum. Vinnsla felur í sér bókun á fylgiseðlum, innhreyfingarskjölum afurða og reikningsfærslu.  

Skjalaútprentun pantana og tilboða sem hafa afhendingaráætlun sýna aðeins afhendingarlínurnar. Hún sýnir ekki upprunalegar línur (viðskiptalínur). **Ábending:** Þar að auki eru aðeins afhendingarlínur sýndar þegar þessar aðgerðir eru framkvæmdar:

-   Bóka
-   Afrita síður
-   Fletta listasíðum og skýrslum

Þegar sölutilboð er staðfest sýna myndaðar sölupantanir alla afhendingaráætlunina, jafnvel pöntunarlínur sem hafa margar afhendingar. Þar að auki er öll afhendingaráætlunin sýnd á öllum aðalsíðum, eins og sölupöntunum, sölutilboðum og innkaupapöntunum.


