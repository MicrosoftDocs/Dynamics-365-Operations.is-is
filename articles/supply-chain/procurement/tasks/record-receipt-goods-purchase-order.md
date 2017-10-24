--- 
title: "Skrá vörumóttöku í innkaupapöntun"
description: "Þessi verklýsing sýnir hvernig á að skrá móttöku á vörum beint á innkaupapöntun."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Skrá vörumóttöku í innkaupapöntun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að skrá móttöku á vörum beint á innkaupapöntun. Einnig er hægt að skrá innhreyfingu afurða í vöruhúsinu og síðan síðar skrá hana í innkaupapöntun. Þetta verk er yfirleitt gert af innkaupaaðila eða af samræmingaraðila viðskiptaskulda. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Dæmin inniheldur skref til að stofna einfalda innkaupapöntun, þannig að hægt er að spila ferlið sem leiðarvísi fyrir verk. Ef þú værir að nota ferlið á þín eigin gögn, myndirðu byrgja á undirverkinu Færsla innhreyfingar á vörum.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Undirbúa nýja innkaupapöntun vegna móttöku afurða.
1. Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Í svæðinu Lánardrottnalykill skal slá inn 'US-101'.
4. Smellið á „Í lagi“.
5. Í svæðið vörunúmer sláið inn M0001.
6. Í reitinn magn skal slá inn 5.
7. Smellið á „Innkaup“ á aðgerðarúðunni.
8. Smellið á „Staðfesta“.

## <a name="record-receipt-of-goods"></a>Skrásetja viðtöku varnings
1. Smellið á „Móttaka“ á aðgerðarúðunni.
2. Smellið á „Innhreyfingarskjal“.
    * Magnsvæðið leyfir þér að velja mismunandi valkosti fyrir það magn sem á að taka á móti. Til dæmis, ef áður hefur verið skráð magn í vöruhúsi, er hægt að velja Skráð magn .  Í þessu dæmis, notaðu gildið Pantað magn.   
3. Í reitinn móttaka afurða skal slá inn hvaða gildi sem er.
    * Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.  
4. Stækka línuhlutann.
5. Stillið magn á „4“.
    * Hér er hægt að tilgreina handvirkt magn sem fæst fyrir hverja línu í pöntun.  
6. Fella saman hlutann línur.
7. Smellið á „Í lagi“.
    * Vörurnar hafa nú verið skráð sem móttekið á innkaupapöntuninni og búið er að stofna færslubók fyrir innhreyfingarskjal afurða sem endurspegla þetta. Hægt er að nota aðgerðina innhreyfing afurðar til að fara yfir færslubækur sem stofnaðar eru með innkaupapöntuninni og sjá hvað var móttekið og hvenær.  


