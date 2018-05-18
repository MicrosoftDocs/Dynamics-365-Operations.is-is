---
title: "Skilgreina birgðatalningarferli"
description: "Þetta ferli fer í gegnum skilgreiningu á grunni birgðatalningabókar ferli með því að stofna talningarflokk og talningarbók."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c14c846c55a3d821945160835817cd4f467deda9
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="define-inventory-counting-processes"></a>Skilgreina birgðatalningarferli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum skilgreiningu á grunni birgðatalningabókar ferli með því að stofna talningarflokk og talningarbók. Hún líka sýnir hvernig á að virkja talningareglur á stigi vöruhúss og vöru. Þessum verkefnum myndi venjulega að framkvæma með yfirmaður vöruhús. Er skilyrði til að hafa einhverja fyrirliggjandi losaðar afurðir og vöruhús. Ef verið er að nota sýnigögn fyrirtæki er hægt að keyra þetta ferli í USMF fyrirtæki með einhverri vörur í birgðum.


## <a name="create-a-counting-group"></a>Stonfa talningarflokk
1. Fara í birgðastjórnun > Uppsetning > Birgðir > Talningaflokka.
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu Talningarflokkur.
4. Í reitinn Heiti skal slá inn gildi.
5. Veljið valkost í svæðinu kóði lykils.
    *  – handvirkt – Tekur með línur í hvert sinn sem vinnsla er keyrð. Með öðrum orðum ákvarðar notandi talningarbil fyrir talningarflokk.  Tímabil - Tekur með línur fyrir tímabil í talningarbók þegar tímabil hefur runnið út.   Núll á lager - Ef lagerbirgðir verða núll (0) eru línur myndaðar í talningarbók þegar vinnslan er keyrð. Ef lagerbirgðir verða 0 eftir talningu verða línur myndaðar í næsta sinn sem talning hefst.   Lágmarkið – Setur inn línur í talningarbók ef lagerbirgðir eru jafnar og eða minni en lágmarkið sem er tilgreint.  
    * Valkostur: Hafirðu tilgreint Tímabil í Teljarakóða svæði, verður þú að færa inn tímabil fyrir tímabil í svæðinu talningartímabil. Einingin fyrir bil er dagar.  
    * Þegar þú keyra vinnsluna til að stofna nýjar línur talningarbókar, nýjar línur eru stofnaðar á bilinu sem er tilgreint í þessu svæði, óháð því hversu oft sama vinnslan er keyrð. Til dæmis, ef tímabil Talning er stillt á 7 og færslubókarlínur voru síðast búin til fyrir talningu 1. Janúar, ef annað vinnslan hefst þann 5. Janúar, sjö dagar hafa liðið ekki og því engar línur myndaðar í færslubók fyrir tímabilið. Ef þú ræsir vinnsla aftur á janúar 8, línur eru myndað fyrir tímabil í counting færslubók, því 7 dagar hafa liðið.  
6. Smellið á „Vista“.

## <a name="create-a-counting-journal-name"></a>Stofna heiti talningabókar
1. Fara í birgðastjórnun > Uppsetning > færslubókarheiti > Birgðir.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum færslubókargerð skal velja „Talning“.
    * Valfrjálst: hægt er að velja annað Kenni fylgiskjalarunu ef tiltekin númeraröð fyrir Kenni fylgiskjals er myndað þegar stofnaðar eru talningarbækur. Fylgiskjalaruna eru stofnaðar í Númeraröð síða.  
6. Í reitnum nákvæmnisstig skal velja valkost.
    * Þetta er stig sundurliðunar sem er notað þegar færslubók er bókuð.  
    * Valfrjálst: Hægt er að skoða eða breyta gildinu í svæðinu frátekning. Þetta er aðferðin sem notuð er til að taka vörur frá meðan á talningu stendur.   
    * Handvirk – vörurnar eru fráteknar handvirkt í skjámyndinni Frátektir.   Sjálfvirkt – pöntunarmagn er frátekið úr tiltækt lagerbirgðir fyrir vara.   Niðurbrot - frátekning er hluti af aðaláætlanagerð færslunnar.  
7. Smellið á „Vista“.

## <a name="set-standard-counting-journal-name"></a>Setja færslubókarheiti staðlaða talningar
1. Fara í Birgðastjórnun > Uppsetning > Birgðir og færibreytur vöruhúsakerfis.
2. Smellið á flipann Færslubækur.
3. Í reitnum Talning skal smella á fellilistahnappinn til að opna leitina.
4. Veljið færslubókina sem búinn var til áður.
    * Þessi færslubók verður þá sjálfgefið færslubókarheiti fyrir birgðabækur af gerðinni Talning.  
5. Smellið á flipann „Almennt“.
    * Valkostur: skal velja þennan valkostur í til að læsa vara á meðan á talningaferli stendur til að koma í veg fyrir uppfærslur fyrir fylgiseðill, tiltektarlisti, eða skráningar tiltektarlista.  

## <a name="set-the-counting-policy-for-an-item"></a>Setja talningarreglu fyrir vöru
1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Smelltu á tengil fyrir vörunúmerið afurðar sem á að setja reglur talningu fyrir á listanum.
    * Athugasemd sem þarf að velja vöru sem er rakin í birgðum. Ekki er hægt að telja afurð sem er ekki á lager. Ef verið er að nota sýnigögn USMF er hægt að velja vöru A0001.  
3. Smellið á „Breyta“.
4. Víxla útvíkkun á liðnum Stjórna birgðum.
5. Í reitnum TALNINGARFLOKKUR skal smella á fellilistahnappinn til að opna leitina.
6. Á listanum, smella á talningarflokk áður stofnaðar.
    * Þessi afurð núna verða teknar með þegar birgðalínur talningabókar eru stofnaðar með því að nota þetta talningarflokkur.  
7. Smellið á „Vista“.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Setja talningarreglu fyrir vöru í ákveðnu vöruhúsi
1. Á Aðgerðasvæðinu skal smella á Stjórna birgðum.
2. Smellt er á vörur í Vöruhúsi.
3. Smellt er á Nýtt.
4. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
5. Veljið vöruhúsið sem óskað er að setja upp tiltekna talningu reglur fyrir af listanum.
6. Í reitnum TALNINGARFLOKKUR skal smella á fellilistahnappinn til að opna leitina.
7. Á listanum, veljið talningarflokk
    * Hér er hægt að velja ákveðna talningarflokk sem nota á fyrir vöruna í tiltekið vöruhús sem var valið. Þegar talning fer fram í vöruhúsinu mun þessi talningarregla hnekkja almennri talningarreglu fyrir vöru.  
8. Smellið á „Vista“.

