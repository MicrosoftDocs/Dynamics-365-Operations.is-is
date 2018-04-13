--- 
title: "Stofna innkaupapöntun"
description: "Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun handvirkt."
author: FrankDahl
manager: AnnBe
ms.date: 06/07/2016
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
ms.openlocfilehash: 27ed15e6d9a376c4203e5446d056f221bd3eb730
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun handvirkt. Dæmigerðara er fyrir innkaupapantanir að stofnast sjálfkrafa sem afleiðing af aðaláætlanagerð, bein afhending og önnur ferli. Innkaupapöntun eru yfirleitt stofnaðar af innkaupastjórar. Dæmi sýnd hér er hægt að nota í USMF sýnigögn fyrirtækis með gildum sem eru lögð til í athugasemdir fyrir mismunandi skref.


## <a name="create-the-purchase-order-header"></a>Stofna haus innkaupapöntunar
1. Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Veljið lánardrottinslykil US-101.
    * Þegar þú velur lánardrottinn, upplýsingar úr færslu um lánardrottinn eins og aðsetur, reikningslykil, afhendingarskilmála og afhendingarmáta verður afrituð sem sjálfgefin gildi í pöntunarhaus. Hægt er að breyta þessum gildum hvenær sem er.  
4. Víkkið út almenna hlutann.
    * Reiturinn svæði ásamt reitnum vöruhús ákvarða hvar innkeyptar vörur eða þjónusta skulu afhent. Sjálfgefið afhendingaraðsetur er svæðið. Bæði svæðin má fylla með gildi sem sett er upp fyrir valinn lánardrottinn, eða hægt að tilgreina þær handvirkt.  
    * Dagsetning Afhendingar svæðið er notað til að tilgreina þegar keypt vara og þjónustu þarf að afhenda. Hægt er að tilgreina eina afhendingardagsetningu fyrir pöntun eða fyrir einstakar pöntunarlínum má úthluta einkvæmt afhendingardagsetningar. Ef afhendingardagsetningu sem er tilgreint hér ekki er hægt að uppfylla fyrir tilteknar vörur eða þjónustu þar sem þeir hafa lengri afhendingartíma, þá verða þessar línur stofnuð með fjarlægari afhendingardag til að hliðra til fyrir þessu.  
5. Fella saman almenna hlutann.
6. Stækka eða fella saman stjórnunarhlutann.
    * Hægt er að nota svæðið Pöntunaraðili til að tilgreina hver er að panta. Það getur verið hentugt að deila þessu með lánardrottins ef þau þurfa að hafa samband við þann einstakling. Svæðinu má úthlutað gildi sjálfkrafa ef gildandi notandareikningurinn tengist heiti á síðunni Notendur.  
7. Fella saman  stjórnunarhlutann.
8. Smellið á „Í lagi“.
    * Pöntunarhaus hefur nú verið stofnaður. Þegar unnið er með innkaupapöntunarlínur birtist aðeins útdráttur úr upplýsingar úr haus. Smella á Haus ef nauðsynlegt er að skoða aðrar upplýsingar.  

## <a name="add-a-purchase-order-line"></a>Bæta við innkaupapöntunarlína
1. Smellt er á Innkaup Innkaupapöntunarlína
2. Smellt er á Víddir.
    * Afurðir mega vera vöruvíddasamsetningar flokkuð eftir víddir, eins og lit, stærð eða stíl. Einnig er hægt að setja afurðir upp til að nota geymsluvíddir eins og svæði og vöruhús. Það eru einnig valfrjálsar rakningarvíddir, eins og runu og raðnúmer. Hægt er að skilvirkni skráning pantana, er hægt að bæta við víddarsvæði sem þú notar oft beint í hnitanet.  
3. Velja gátreitinn litur.
    * Valfrjálst: Sé notað svæðið vista uppsetningu, munu víddirnar sem þú valdir einnig birtast á hnitaneti pöntunarlínu næst þégar þú opnar síðuna innkaupapöntun.  
4. Smellið á „Í lagi“.
5. Í svæðið vörunúmer veldu 'T0004'.
    * Pöntunarlínur eru stofnaðar fyrir vörur og þjónustu með því að tilgreina vörunúmer eða sem útgjöld með því að tilgreina innkaupaflokk.  
    * Svæðið Tegund Innkaupa er notað til að bæta línum við þar sem innkeyptar vörur eru gjaldfærðar beint, frekar en að fara inn í birgðir. Það merkir að ef gjaldfæra á innkaup er hægt að gera það með því að stofna innkaupapöntunarlínu sem tilgreinir innkaupategund frekar en að stofna línu með vörunúmeri. Vörur má einnig tengja innkaupaflokki og í því tilfelli er innkaupategund sýnd sem upplýsingar aðeins.  
6. Sláið inn eða veldu gildi í reitnum litur.
    * Reitirnir Svæði og Vöruhús eru yfirleitt útfylltar með gildum úr pöntunarhaus, en hægt er að hnekkja svæðin ef sumar línur er þörf á að afhenda á mismunandi stöðum.  
7. Færið inn númer í reitnum „Magn“.
    * Tilgreinið magnið sem á að kaupa. Magnsvæðið er sjálfkrafa fyllt út með minnsta pöntunarmagn afurðar ef þetta er sett upp, eða með gildinu 1.  
    * Í reitnum Einingu er gefið til kynna mælieiningu fyrir pantað magn. Venjulega er einingin er sjálfkrafa gefið úr innkaupaeiningu á afurðarsniðmáti, en hægt er að breyta þessu.  
    * Yfirleitt inniheldur í svæðið einingarverð gildi úr annað hvort innkaupasamning eða viðskiptasamningi. Mögulegt er að breyta einingarverðinu í einstaka pöntunarlínum, til dæmis ef einkvæmt verð er samið við lánardrottininn.  
    * Svæðið Afsláttur inniheldur afsláttarupphæð á einingu afurðar. Þessi afsláttur minnkar því einingarverð samkvæmt afsláttinn. Þennan afslátt er yfirleitt fengið sjálfkrafa frá innkaupasamningum eða viðskiptasamninga en mögulegt er að hnekkja honum í einstökum línum ef einkvæmt afsláttur hefur verið samið við lánardrottininn.  
    * Afsláttarprósenta er hægt að færa inn sem minnkar nettóupphæð línunnar, samkvæmt því. Þessi afsláttarprósenta er oft fengið sjálfkrafa frá innkaupasamningum eða viðskiptasamninga en mögulegt er að hnekkja honum í einstökum línum ef einkvæmt afsláttarprósenta hefur verið samið við lánardrottininn.  
    * Gildið í svæðinu Nettóupphæð er reiknaður úr öðrum svæðum í línunni, þar með talið magn, einingarverð, afslætti og afsláttarprósenta. Hægt er að breyta Nettó upphæð en þá verða svæðin Einingarverð Afsláttar, og afsláttarprósenta autt, og þegar því línan er bókuð verður bókuð upphæð í hlutfalli við nettó upphæð. Yfirleitt er svæðið Nettóupphæð einungis notað til að birta nettóupphæð línunnar.  
8. Víkkið út hlutann „Upplýsingar um línu“.
9. Smellið á flipann „Afhending“.
    * Einkvæmt afhendingardagsetningu er hægt að úthluta hverri pöntunarlínu. Dagsetningin kemur úr svæðinu á haus innkaupapöntunar, en hægt er að breyta þessu.  
10. draga saman hluta upplýsingar Línu.

## <a name="review-order-totals"></a>Fara yfir samtölu pöntunar
1. Smellið á „Samtölur“.
    * Ef þú sérð ekki aðgerðina samtölur, smellið á flipann Innkaupapöntun á aðgerðastiku.  
    * Svarglugginn sýnir samtölur fyrir alla pöntunina.  
    * Svæðið Val leyfir þér að breyta grundvellinum sem notaður er til að reikna samtölur. Til dæmis gætirðu valið magn innhreyfingarskjals afurða til að sýna samtölur sem tengjast upphæð afurðir sem hafa verið móttekin, eða Pantað magn til að sýna upphæð afurða sem var pantað.  
2. Smellið á „Í lagi“.


