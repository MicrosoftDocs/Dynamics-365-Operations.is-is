---
title: Skilgreina birgðatalningarferli
description: Þetta efni lýsir skilgreiningu á grunni birgðatalningabókar ferli með því að stofna talningarflokk og talningarbók.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e54dfae274b201949d943b3e3e06b0c5b2c61ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244502"
---
# <a name="define-inventory-counting-processes"></a>Skilgreina birgðatalningarferli

[!include [banner](../../includes/banner.md)]

Þetta efni lýsir skilgreiningu á grunni birgðatalningabókar ferli með því að stofna talningarflokk og talningarbók. Hún líka sýnir hvernig á að virkja talningareglur á stigi vöruhúss og vöru. Þessum verkefnum myndi venjulega að framkvæma með yfirmaður vöruhús. Er skilyrði til að hafa einhverja fyrirliggjandi losaðar afurðir og vöruhús. Ef verið er að nota sýnigögn fyrirtæki er hægt að keyra þetta ferli í USMF fyrirtæki með einhverri vörur í birgðum.


## <a name="create-a-counting-group"></a>Stonfa talningarflokk
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Birgðir > Talningaflokkar**.
2. Veljið **Nýtt**.
3. Í reitinn **Talningaflokkur** í nýju línunni færirðu inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitinn **Talningarkóði** velurðu valkost.

    - **Handvirkt** – Tekur með línur í hvert sinn sem vinnsla er keyrð. Með öðrum orðum ákvarðar notandi talningarbil fyrir talningarflokk.  
    - **Tímabil** - Tekur með línur fyrir tímabil í talningarbók þegar tímabil hefur runnið út.  
    - **Núll á lager** - Ef lagerbirgðir verða núll (0) eru línur myndaðar í talningarbók þegar vinnslan er keyrð. Ef lagerbirgðir verða 0 eftir talningu verða línur myndaðar í næsta sinn sem talning hefst.  
    - **Lágmarkið** – Setur inn línur í talningarbók ef lagerbirgðir eru jafnar og eða minni en lágmarkið sem er tilgreint.  
    - Valkostur: Hafirðu tilgreint **Tímabil** í reitnum **Teljarakóða** verður þú að færa inn tímabil fyrir tímabil í reitnum **Talningartímabil**. Einingin fyrir bil er dagar.  
    - Þegar þú keyra vinnsluna til að stofna nýjar línur talningarbókar, nýjar línur eru stofnaðar á bilinu sem er tilgreint í þessu svæði, óháð því hversu oft sama vinnslan er keyrð. Til dæmis, ef **Talningartímabil** er stillt á 7 og færslubókarlínur voru síðast myndaðar fyrir talningu þann 1. janúar, ef önnur vinnsla er hafin þann 5. janúar hafa sjö dagar ekki liðið og því eru engar línur myndaðar í færslubók fyrir tímabilið. Ef þú ræsir vinnsla aftur á janúar 8, línur eru myndað fyrir tímabil í counting færslubók, því 7 dagar hafa liðið.  

6. Veljið **Vista**.

## <a name="create-a-counting-journal-name"></a>Stofna heiti talningabókar
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Færslubókaheiti > Birgðir**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Færslubókargerð** skal velja **Talning**. Valfrjálst: hægt er að velja annað Kenni fylgiskjalarunu ef tiltekin númeraröð fyrir Kenni fylgiskjals er myndað þegar stofnaðar eru talningarbækur. Fylgiskjalaruna eru stofnaðar á síðunni **Númeraröð**.  
6. Í reitnum **Lýsing á stigi** skal velja valkost.  

    - Þetta er stig sundurliðunar sem er notað þegar færslubók er bókuð.  
    - Valfrjálst: Hægt er að skoða eða breyta gildinu í svæðinu frátekning. Þetta er aðferðin sem notuð er til að taka vörur frá meðan á talningu stendur.   
    - **Handvirkt** – vörurnar eru fráteknar handvirkt í skjámyndinni Frátektir.  
    - **Sjálfvirkt** – pöntunarmagn er frátekið úr tiltækt lagerbirgðir fyrir vara.   
    - **Niðurbrot** - frátekning er hluti af aðaláætlanagerð færslunnar.  

7. Veljið **Vista**.

## <a name="set-standard-counting-journal-name"></a>Setja færslubókarheiti staðlaða talningar
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Birgðir og færibreytur vöruhúsakerfis**.
2. Velja flipann **Færslubækur**.
3. Í fellivalmyndinni í reitnum **Talning** skal velja færslubókina sem þú bjóst til áður. Þessi færslubók verður þá sjálfgefið færslubókarheiti fyrir birgðabækur af gerðinni **Talning**.  
4. Veldu flipann **Almennt**. Valfrjálst: Veljið þennan valkost til að læsa vöru í talningarferlinu til að hindra uppfærslu á fylgiseðli, tiltektarlista eða tiltektarlistaskráningu.  

## <a name="set-the-counting-policy-for-an-item"></a>Setja talningarreglu fyrir vöru
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.
2. Af listanum velurðu tengil fyrir vörunúmer afurðarinnar sem á að setja talningarreglur upp á. Þú verður að velja vöru sem er rakin í birgðum. Ekki er hægt að telja afurð sem er ekki á lager. Ef verið er að nota sýnigögn USMF er hægt að velja vöru A0001.  
3. Veljið **Breyta**.
4. Víxla útvíkkun á liðnum **Stjórna birgðum**.
5. Í fellivalmyndinni í reitnum **Talningaflokkur** skal velja talningaflokkinn sem þú bjóst til áður. Þessi afurð núna verða teknar með þegar birgðalínur talningabókar eru stofnaðar með því að nota þetta talningarflokkur.  
6. Veljið **Vista**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Setja talningarreglu fyrir vöru í ákveðnu vöruhúsi
1. Á Aðgerðasvæðinu skal velja **Stjórna birgðum.**
2. Veldu **Vörur í vöruhúsi**.
3. Veljið **Nýtt**.
4. Í fellivalmyndinni í reitnum **Vöruhús** velurðu vöruhúsið sem þú vilt setja upp sérstakar talningarstefnur fyrir.
5. Í fellivalmyndinni í reitnum **Talningarflokkur** skal velja talningarflokk. Hægt er að velja ákveðinn talningarflokk sem nota á fyrir vöruna í tiltekið vöruhús sem var valið. Þegar talning fer fram í vöruhúsinu mun þessi talningarregla hnekkja almennri talningarreglu fyrir vöru.  
6. Veljið **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]