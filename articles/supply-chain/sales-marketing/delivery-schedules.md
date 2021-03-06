---
title: Afhendingaráætlanir
description: Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193783"
---
# <a name="delivery-schedules"></a>Afhendingaráætlanir

[!include [banner](../includes/banner.md)]

Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun.

Notaðu afhendingaráætlun þegar verður heildarmagn í pöntun eða tilboðslínu verður að vera afhent í mörgum sendingum. Stakar sendingar eru táknaðar með afhendingarlínum. Tvær eða fleiri afhendingarlínur mynda eina afhendingaráætlun. Afhendingarlínur getur haft mismunandi afhendingardagsetningar, magn, afhendingarmáti og geymsluvíddir, eins og svæði og vöruhús.  

**Dæmi um afhendingaráætlun**

| vara                              | Virði                                    |
|-----------------------------------|------------------------------------------|
| Heildarpöntun (upprunalegu pöntunarlína) | 600 stólar                               |
| Umbeðin afhendingaráætlun       | 100 stólar á mánuði                     |
| Umbeðinn tímarammi fyrir afhendingu | 6 mánuðir, á fyrsta degi hvers mánaðar |

Í þessu dæmi biður viðskiptavinur um afhendingu á 600 stólum í runum með 100 stólum yfir sex mánaða tímabil. Til að rekja afhendingarkröfur skal stofna afhendingaráætlun. Á síðunni Afhendingaráætlun skal stofna sex aðskildar afhendingarlínur. Hver afhendingarlína inniheldur 100 stóla og tekur fram afhendingardag fyrir þessa 100 stóla. Í þessu tilfelli er hver lína mótfærsla fyrsta mánaðar fyrir sex samfellda mánuði.  

Þegar þú stofnar afhendingaráætlun er gerð upprunalegrar pöntunarlínu sjálfkrafa breytt í **Sölupöntunarlínu með margar afhendingar**. Lína af þessari gerð kallast viðskiptalína og er merkt með tákni. Afhendingarlínan er merkt með öðru tákni. Ef þetta magni er breytt í afhendingarlínu er sviðskiptalínan uppfærð í heildarmagn afhendingaráætlunar. Ef magni í afhendingarlínu er breytt er viðskiptalínan uppfærð í heildarmagn afhendingaráætlunar, jafnvel þegar pöntun er skipt upp í aðskildar afhendingar.  

Pantanir sem hafa afhendingaráætlun eru unnar gegn afhendingarlínum. Vinnsla felur í sér bókun á fylgiseðlum, innhreyfingarskjölum afurða og reikningsfærslu.  

Skjalaútprentun pantana og tilboða sem hafa afhendingaráætlun sýna aðeins afhendingarlínurnar. Hún sýnir ekki upprunalegar línur (viðskiptalínur). **Ábending:** Þar að auki eru aðeins afhendingarlínur sýndar þegar þessar aðgerðir eru framkvæmdar:

-   Bóka
-   Afrita síður
-   Fletta listasíðum og skýrslum

Þegar sölutilboð er staðfest sýna myndaðar sölupantanir alla afhendingaráætlunina, jafnvel pöntunarlínur sem hafa margar afhendingar. Þar að auki er öll afhendingaráætlunin sýnd á öllum aðalsíðum, eins og sölupöntunum, sölutilboðum og innkaupapöntunum.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]