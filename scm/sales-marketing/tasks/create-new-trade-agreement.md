--- 
title: "Stofna nýja verðsamning"
description: "Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1178c7a5db129801f83afa8b4caf9357ccf76b71
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-new-trade-agreement"></a>Stofna nýja verðsamning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Ef verið er að nota eigin gögn, þarftu að ganga úr skugga um áður en byrjað er að þessari handbók að á heiti færslubókar fyrir Verðsamningur er til staðar þar sem Sjálfgefinn tengsl er stillt á "Verð (sala)".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Stofna og bóka nýja færslubók verðsamnings
1. Fara í Sölu og markaðssetningu > Verð og afslætti > Færslubækur viðskiptasamninga.
2. Smellið á „Nýtt“.
3. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á „Línur“.
7. Í reitnum kóði lykils er valið 'tafla'.
    * Í þessu dæmi er verið að uppfæra verð fyrir tiltekinn viðskiptavin, sem þýðir að þarf að velja Töflu. Ef verið var að uppfæra listaverð afurðar, myndirðu velja Allt, þannig að ný verði gildir fyrir alla viðskiptavini. Ef þú værir að sundurgreina verð milli ólíkra hluta viðskiptavinar þá myndiðu velja Flokk. Til að velja Flokk, verður að hafa að sett upp verðflokka viðskiptavinar.  
8. Í reitnum Val á lykli skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í reitnum vörukóði er valið ‚Tafla‘.
    * Þegar þú færir inn viðskiptasamningur af gerðinni 'Verð (sala) verður einungis að velja Tafla í vörukóðasvæðinu. Þetta er vegna þess að verð með raungildi og má ekki vera það sama fyrir allar afurðir eða flokka afurða.  
11. Í reitnum Vöruvensl skal smella á fellilistahnappinn til að opna leitina.
12. Á listanum, veljið afurð sem á að taka með í samningnum.
    * Skrifaðu athugasemd um hvaða vöru sem var valin.  
13. Í listanum skal smella á tengilinn í valinni línu.
14. Í reitinn Frá skal slá inn lágmarksmagn.
    * Ef viðskiptavinur þarf að panta lágmarksmagn áður en þeir verða gjaldgengir fyrir nýtt verð, þá þarf að tilgreina það magn hér.  
    * Færið inn gildi í svæðinu Til, til að tilgreina hámarksmagn og ef farið er umfram það mun verðið á samningnum ekki vera gilt. Ef þú ert að bjóða verð og afslætti sem byggir á mörgum hléum í magni, þá skaltu tilgreina hvern magnsvina sem par af lágmarks- og hámarksmagni í 'Frá' og '‘Til svæði, í þessari röð.  
15. Færa inn verð í svæðinu Upphæð í gjaldmiðli
16. Í dagsetningarsvæði Frá, færið inn dagsetningu sem þessi samningur gildir uppfrá.
17. Smellið á „Vista“.
18. Smella á Villuleita.
19. Smella á Villuleita valdar línur.
20. Smellið á „Í lagi“.
21. Smellið á „Bóka“.
22. Smellið á „Í lagi“.

## <a name="view-trade-agreements-for-a-product"></a>Skoða viðskiptasamninga fyrir afurð
1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Finna og velja vöru sem verð hefur nýlega verið uppfært verð, á listanum.
3. Í aðgerðasvæðinu er smellt á selja.
4. Smellt er á Skoða viðskiptasamninga.
    * Fara yfir nákvæmar upplýsingar um verð viðskiptasamnings sem var nýverið stofnaður.    
5. Lokið síðunni.


