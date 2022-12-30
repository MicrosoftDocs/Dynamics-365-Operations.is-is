---
title: Setja upp lánardrottna, viðskiptavina og vörur fyrir samstæðuviðskipti
description: Þessi grein útskýrir hvernig lánardrottnar, viðskiptavinir og vörur eru sett upp fyrir samstæðuviðskipti
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945756"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Setja upp lánardrottna, viðskiptavina og vörur fyrir samstæðuviðskipti

[!include [banner](../../includes/banner.md)]

Til að undirbúa fyrirtækið undir samstæðuviðskipti þarf fyrst að skilgreina lánardrottna og viðskiptavini sem verður átt í viðskiptum við innan samstæðu. Því næst þarf að tengja þessa lánardrottna og viðskiptavini við vörurnar sem verða keyptar og seldar.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**.
1. Veldu lánardrottin sem á að skilgreina sem samstæðulánardrottin.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Tilgreindu uppsetningarfæribreytur innan samstæðu fyrir lánardrottnalykilinn. Þessar færibreytur fela í sér lögaðila og lykil viðskiptavinar, sölupöntunarreglur, innkaupapöntunarreglur, gildisvörpun og reglur innkaupasamnings og sölusamnings. Þú tilgreinir einnig hvort nota eigi gildi grunngagna úr lánardrottnalyklinum eða úr viðskiptavinalyklinum í hinum lögaðilanum.
1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Á listasíðunni **Útgefnar afurðir** skal velja vörurnar sem úthluta á lánardrottni þannig að vörurnar séu aðgengilegar í samstæðuviðskiptum. Fyrir hverja vöru skal opna síðuna **Upplýsingar um útgefna afurð**. Í flipann **Innkaup**, í reitinn **Lánardrottinn**, skal slá inn lánardrottnanúmerið.
1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veldu viðskiptavin sem á að skilgreina sem samstæðuviðskiptavin.
1. Í aðgerðasvæðinu, á flipanum **Almennt**, skal velja **Innan samstæðu**.
1. Tilgreindu uppsetningarfæribreytur innan samstæðu fyrir viðskiptavinalykilinn. Þessar færibreytur fela í sér lögaðila og lykil lánardrottins, sölupöntunarreglur, innkaupapöntunarreglur, gildisvörpun og reglur innkaupasamnings og sölusamnings. Þú tilgreinir einnig hvort nota eigi gildi grunngagna úr viðskiptavinalyklinum eða úr lánardrottnalyklinum í hinum lögaðilanum.
1. Þegar búið er að setja upp færibreytur innan samstæðu skal loka síðunni **Innan samstæðu** til að fara aftur á upplýsingar um valdan viðskiptavin.
1. Stækkaðu flýtiflipann **Ýmsar upplýsingar** og stilltu **Stofna samstæðupantanir** á *Já*. Ef þú vilt einnig að pantanir séu afhentar beint til viðskiptavina skal stilla **Bein afhending** á *Já*.

    > [!NOTE]
    > Ef það eru einhverjar vörur sem fyrirtækið hefur á lager og afhendir viðskiptavinum ætti kannski ekki að stofna samstæðupantanir sjálfvirkt, jafnvel þótt varan sé til á lager. Til að gera sjálfvirka myndun pantana á vörum sem stundum eru til á lager óvirka skal stilla **Stofna samstæðupantanir** á *Nei*.

1. Ef þú vilt leyfa að aukalínur séu stofnaðar með óbeinum hætti í sölupöntun skaltu stilla **Búa til óbeinar pöntunarlínur** á *Já*. Notandi getur þá bætt línum við upprunalegu sölupöntunina úr samstæðusölupöntuninni.

> [!WARNING]
> Ef óbein stofnun sölulína er leyfð eru allar viðbætur við upprunalega sölupöntun úr samstæðusölupöntuninni leyfðar. Hver viðbót er þá keyrð í gegn til viðskiptavinarins og bætt við pöntunina og reikninginn. Auk þess eru öll skjöl sem tengjast sölunni prentuð og bókuð sjálfkrafa. Notendur eru ekki látnir vita af viðbótinni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
