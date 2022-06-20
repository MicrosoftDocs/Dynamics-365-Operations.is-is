---
title: Setja upp lánardrottna, viðskiptavina og vörur fyrir samstæðuviðskipti
description: Þessi grein útskýrir hvernig á að setja upp lánardrottna, viðskiptavini og vörur fyrir viðskipti milli fyrirtækja
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
ms.translationtype: MT
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
1. Þegar þú ert búinn að setja upp færibreytur milli fyrirtækja skaltu loka **Millifyrirtæki** síðu til að fara aftur í valdar upplýsingar um viðskiptavini.
1. Stækkaðu **Ýmis smáatriði** Flýtiflipa og stilla **Búa til millifyrirtækjapantanir** til *Já*. Ef þú vilt líka að pantanir séu afhentar beint til viðskiptavina skaltu stilla **Bein afhending** til *Já*.

    > [!NOTE]
    > Ef það eru einhverjar vörur sem fyrirtækið hefur á lager og afhendir viðskiptavinum ætti kannski ekki að stofna samstæðupantanir sjálfvirkt, jafnvel þótt varan sé til á lager. Til að óvirkja sjálfvirka myndun pantana fyrir vörur sem þú gætir stundum átt á lager skaltu stilla **Búa til millifyrirtækjapantanir** til *Nei*.

1. Ef þú vilt leyfa aukalínur að vera búnar til óbeint á sölupöntun, stilltu **Búðu til óbeinar pöntunarlínur** til *Já*. Notandi getur þá bætt línum við upprunalegu sölupöntunina úr samstæðusölupöntuninni.

> [!WARNING]
> Ef óbein stofnun sölulína er leyfð eru allar viðbætur við upprunalega sölupöntun úr samstæðusölupöntuninni leyfðar. Hver viðbót er þá keyrð í gegn til viðskiptavinarins og bætt við pöntunina og reikninginn. Auk þess eru öll skjöl sem tengjast sölunni prentuð og bókuð sjálfkrafa. Notendur eru ekki látnir vita af viðbótinni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
