---
title: Setja upp og nota „greiðist-þegar-greitt“ greiðslur lánardrottins
description: Þetta efnisatriði útskýrir hvernig á að búa til skilmála „greiðist-þegar-greitt“ (PWP) svo að þú getir losað að hluta um greiðslur lánardrottins, miðað við greiðslur viðskiptavinar.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284114"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Setja upp og nota „greiðist-þegar-greitt“ greiðslur lánardrottins

[!include [banner](../includes/banner.md)]

Þegar lánardrottinn er samþykktur sem undirverktaki er hægt að viðhalda greiðslu til lánardrottins þar til viðskiptamaður hefur greitt fyrir verkið. Til að styðja þess atburðarás geturðu sett upp „greiðist-þegar-greitt“ (PWP) skilmála þegar sett er upp innkaupapöntun með lánardrottni.

Til dæmis þegar viðskiptavinur greiðir upphæð á verkreikning, er hægt að losa um upphæð reiknings lánadrottins að hluta til eða að öllu leyti. Settu einfaldlega upp PWP skilmála sem tilgreina að lánardrottinn fái greitt eftir að þú hefur fengið prósentuhlutfall af tengdri greiðslu frá viðskiptavininum. Þegar hlutagreiðsla berst frá viðskiptavini er hægt handvirkt að losa suma tengda reikninga lánardrottins til greiðslu.

Eftirfarandi dæmi lýsir ferlinu þegar PWP skilmálar eru notaðir.

## <a name="example"></a>Dæmi

Fyrirtækið þitt samþykkir að útvega viðskiptavini 100 tölvur sem eru með uppsettan hugbúnað, að upphæðr 150,00 bandaríkjadali (USD) á hverja tölvu. Þú ræður síðan lánardrottinn til að útvega þér tölvurnar sem hafa hugbúnað uppsettan. Samkvæmt samningnum verður viðskiptavinurinn að samþykkja gæði tölvanna áður en hann borgar fyrirtækinu þínu. Regla fyrirtækisins þíns er að halda eftir greiðslu til lánardrottna þar til viðskiptavinurinn hefur greitt þér. Því setur þú verkið upp þannig að PWP prósenta þess er 100 prósent.

Lánardrottinn sendir þér 100 tölvur sem hafa hugbúnað uppsettan ásamt reikningi fyrir 10.000,00 USD. Þar sem PWP skilmálar eru settir upp fyrir verkið þitt greiðir þú ekki lánardrottninum við móttöku tölvanna. Þess í stað sendir þú tölvurnar til viðskiptavinarins ásamt reikningi fyrir 15.000,00. Viðskiptavinurinn skoðar tölvurnar og staðfestir heildarupphæð verkreikningsins.

Eftir að full greiðsla berst frá viðskiptavininum greiðir fyrirtækið lánardrottni 10.000,00, eða heildarupphæð reiknings lánardrottins.

## <a name="set-up-pwp-terms-for-a-project"></a>Setja upp PWP skilmála fyrir verk

Þegar þú setur upp PWP skilmála fyrir verk verður þú að tilgreina sem prósentu lágmarksupphæð sem viðskiptavinur verður að greiða þér fyrir verkið áður en þú greiðir lánardrottinum. Viðmiðunarupphæðin er sjálfkrafa reiknuð út á reikningum viðskiptavinar fyrir verkið. Fylgið eftirfarandi skrefum til að setja upp viðmiðunarhlutfall fyrir PWP skilmála.

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Öll verk**.
2. Finndu og opnaðu verkið sem þú vilt setja upp PWP skilmála fyrir.
3. Á flýtiflipanum **Samningar lánardrottins** velurðu **Bæta við línu**.
3. Veljið einn eftirfarandi valkosta í svæðinu **Lykilkóði**:

    - **Tafla** – PWP skilmálar eiga við um einn lánardrottinn.
    - **Hópur** – PWP skilmálar eiga við um alla lánardrottna í lánardrottnaflokki.
    - **Allt** – PWP skilmálar eiga við um alla lánardrottna.

4. Ef þú valdir **Töflu** eða **Hóp** í fyrra skrefi, í svæðinu **Lánardrottinn eða lánardrottnaflokkur** veldu lánardrottinn eða lánardrottnaflokk sem PWP skilmálarnir eiga við um. Ef þú valdir **Allt** í fyrra skrefi er ekki hægt að breyta svæðinu **Lánardrottinn/lánardrottnaflokkur**.
5. Ef varðveisluskilmálar lánardrottins hafa einnig verið settir upp fyrir lánadrottinn verksins á svæðinu **Varðveisluskilmálar lánardrottins** skal velja reglukenni varðveisluskilmála.
6. Á svæðinu **Þröskuldsprósenta greiðist þegar greitt** er fært inn viðmiðunarhlutfall fyrir verkið. Hlutfallið sem fært er inn fyrir verkið ákvarðar lágmarksupphæð sem viðskiptavinurinn verður að greiða áður en þú greiðir lánardrottni.

## <a name="create-a-po-that-has-pwp-terms"></a>Stofna innkaupapöntun sem hefur PWP skilmála

Þegar þú bókar reikning lánardrottins birtast skilmálarnir í línum innkaupapöntunarinnar, ef PWP skilmálar eiga við um viðkomandi lánardrottinn. Fylgdu eftirfarandi skrefum til að stofna innkaupapöntun sem hefur PWP skilmála.

1. Opnaðu **Innkaup og aðföng** \> **Innkaupapantanir** \> **Allar innkaupapantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**. Sláðu síðan inn nauðsynlegar upplýsingar í svargluggann **Stofna innkaupapöntun** og veldu **Í lagi**.

    Að öðrum kosti skaltu opna núverandi innkaupapöntun á listasíðunni **Allar innkaupapantanir**.

4. Á síðunni **Innkaupapöntun** á flýtiflipanum **Innkaupapöntunarlínur** þarf að fara yfir upplýsingar innkaupapöntunarlínunnar fyrir viðkomandi lánardrottinn. Valkosturinn **Greiðist þegar greitt** er sjálfkrafa valinn og gildið á svæðinu **PWP viðmiðunarhlutfall** er sjálfkrafa afritað af svæðinu **PWP viðmiðunarhlutfall** á síðunni **Verk**.
6. Ef þú vilt ekki að PWP skilmálar gildi um lánardrottinn á innkaupapöntunarlínu skaltu hreinsa út valkostinn **Greiðist þegar greitt**. Í þessu tilfelli verður svæðið **PWP viðmiðunarhlutfall** fyrir innkaupapöntunarlínuna endurstillt á 0 (núll).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Uppfærðu greiðslu viðskiptavina og borgaðu lánardrottninum

Þegar lánardrottinn lýkur vinnu sinni við verk og sendir þér reikning, verður þú að fara yfir stöðu verksins og reikninga viðskiptavina til að ákvarða hvort PWP skilmálum hafi verið fullnægt fyrir verkið. Ef PWP skilmála fyrir lánardrottins voru uppfylltir er hægt að ákvarða hvaða línur á lánardrottnareikningi á að greiða á grundvelli greiðslu viðskiptamanns fyrir verkið. Ef þú ákveður að greiða viðkomandi lánardrottni þó að PWP skilmálum hafi ekki verið fullnægt geturðu hnekkt PWP skilmálum á síðunni **Reikningur lánardrottins sem er greiddur þegar greitt er**.

1. Opnaðu **Verkefnastjórnun og bókhald** \> **Fyrirspurnir og skýrslur** \> **Fyrirspurnir um varðveislu** \> **Reikningur lánardrottins sem er greiddur þegar greitt er**.
2. Á síðunni **Reikningar lánardrottins sem eru greiddir þegar greitt er** á leitarsvæðinu slærðu inn gildi til að finna reikning lánardrottins sem þú vilt fara yfir og síðan velurðu **Leita**.
3. Á flýtiflipanum **Reikningslínur lánardrottins** skal velja línurnar sem á að vinna úr.
4. Ef skilyrðin fyrir **Greiðist þegar greitt** eru uppfyllt fyrir reikningslínuna, veldu **Losa greiðslu lánardrottins**. Valkosturinn **Greiðist þegar greitt** er hreinsaður og gildi svæðisins **Tilbúið til greiðslu** er breytt í **Já**.
