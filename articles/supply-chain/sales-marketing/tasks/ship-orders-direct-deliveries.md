--- 
title: Senda pantanir sem beinar afhendingar
description: "Þetta ferli sýnir hvernig á að búa til beina afhendingu fyrir sölupöntun."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Senda pantanir sem beinar afhendingar

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að búa til beina afhendingu fyrir sölupöntun. Nota beina afhendingu þegar á að senda vörurnar viðskiptavininum beint frá lánardrottni í staðinn fyrir sendingu þær í eigin vöruhúsi fyrirtækisins fyrst. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Til að ljúka seinni undirverki "Stofna beinar afhendingar úr vinnusvæði", ganga úr skugga um vöru sem er valin á sölupöntun hefur sjálfgefið Lánardrottins tilgreindan á Flýtiflipanum Innkaupa fyrir Útgefnar afurðarsniðmát.


## <a name="set-an-individual-order-for-direct-delivery"></a>Stilla á einstaka pöntun fyrir beina afhendingu
1. Fara í Allar sölupantanir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
    * Ef verið er að nota USMF er hægt að velja lykil U.S.-001.  
4. Smellið á „Í lagi“.
5. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Ef verið er að nota USMF er hægt að velja vöru T0020.  
6. Smellið á „Vista“.
7. Smellið á „Sölupöntun“ á aðgerðarúðunni.
8. Smellið á „Bein afhending“.
    * Stofna afhendingu síðu sýnir allar opnar sölupöntunarlínurnar sem afritað er úr sölupöntuninni. Hægt er að skoða upplýsingar um pöntun, og ef þörf krefur, er hægt að breyta upplýsingum um slíkar innkaupamagn og verðskilmálar áður en hægt er að stofna beina afhendingu.  
9. Veljið „Já“ á svæðinu „Taka allt með“.
    * Ef mynda á beina afhendingu fyrir aðeins hlutmengi sölupöntunarlínur, veljið þær sérstaklega.  
    * Svæðið fyrir reikninga Lánardrottins getur eða ekki þegar vera með númer lánardrottins. Ef sjálfgefinn lánardrottinn er sett upp fyrir afurðina (á tengda vöruþekju) verður þessi lánardrottinn afritaður í línuna. Annars þarf að færa lánardrottinn handvirkt. Í þessu dæmi veljum við nýja lánardrottins í næsta skref jafnvel þótt þegar sé fyllt út.   
10. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
    * Ef verið er að nota USMF er hægt að velja lykil 1001.  
11. Smellið á „Í lagi“.
    * Skilaboðin tilkynnir að innkaupapöntunin hefur nú verið stofnuð.   
12. Víkkið út hlutann „Upplýsingar um línu“.
13. Smellið á flipann „Afhending“.
    * Svæðið Bein afhending er nú stillt á Já.  
    * Staða Beinnar afhendingar sýnir innkaupapöntun stofnuð.   
14. Smellið á „Almennt“ á aðgerðarúðunni.
15. Smellt er á Tengdar pantanir.
16. Smellið til að velja tengilinn í reitnum Innkaupapöntun.
17. Víkkið út hlutann „Upplýsingar um línu“.
18. Smellt er á flipann Aðsetur.
    * Athugið að afhendingaraðsetur fyrir þessa innkaupapöntunarlínu er aðsetur viðskiptavinar og ekki aðsetur fyrirtækisins.  
    * Ef breytt er afhendingaraðsetrið á innkaupapöntunarlínunni eða upphaflegri sölupöntunarlínu er aðsetur í samsvarandi pöntunarlínu verða uppfærð sjálfkrafa.  
19. Smellið á flipann „Afhending“.
    * Eins og sölupöntunarlínu, tengt innkaupapöntunarlína er einnig stillt á Beina afhendingu.  
    * Dagsetning Afhendingar á innkaupapöntunarlínu vörunnar og Staðfest dagsetning afhendingar eru stillt á Umbeðinni móttökudagsetningu og Staðfest móttökudagsetning á upphaflegu sölupöntunarlínunni í þessari röð.   
    * Ef einhver dagsetningum á innkaupalína eða sölulínu verða dagsetningar á samsvarandi pöntun uppfærð sjálfkrafa.     
    * Innkaupapöntun sem er stillt á að afhenda vörur beint í viðskiptavin er tengd við upprunalegu sölupöntunina með sérstökum tengingu. Þessi tenging setur þá reglan að uppfærsla fylgiseðils fyrir sölupöntunar er ekki hægt að gera úr sölupöntun sjálf og verður að gera með því að nota innkaupapöntun. Hins vegar reikningsfærsla viðskiptavinar verður að vinna úr sölupöntun.  
20. Smellið á „Innkaup“ á aðgerðarúðunni.
21. Smellt er á Staðfestingu.
22. Smellið á „Í lagi“.
23. Smellið á „Móttaka“ á aðgerðarúðunni.
24. Smellið á „Innhreyfingarskjal“.
25. Í reitinn innhreyfingarskjal afurða skal slá inn gildi.
26. Smellið á „Í lagi“.
27. Smellið á „Almennt“ á aðgerðarúðunni.
28. Smellt er á Tengdar pantanir.
29. Í listanum skal merkja valda línu.
    * Þegar innkaupapöntun hefur verið uppfærð sem móttekin eða með öðrum orðum, eftir að lánardrottinn hefur sent til aðsetur viðskiptavinarins, er staða upphaflegrar sölupöntunar sjálfkrafa uppfærist í Afhent.  
    * Nú er hægt að reikningsfæra sölupöntunina.    
30. Smellið á „Í lagi“.
31. Lokið síðunni.
32. Smellið á „Í lagi“.

## <a name="create-direct-deliveries-from-the-workbench"></a>Stofna beinar afhendingar úr á vinnusvæði
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara í Allar sölupantanir.
4. Smellið á „Nýtt“.
5. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
6. Smellt er á Í lagi.
7. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
8. Víkkið út hlutann „Upplýsingar um línu“.
9. Smellið á flipann „Afhending“.
    * Í stað þess að stofna beina afhendingu sem hluta af vinnslu sölupöntunar eins og í fyrra ferli er hægt að velja að afhenda þessu verki til innkaupasérfræðings. Til að taka með sölupöntunarlínu í ferli beinnar afhendingar, verður að merkja línuna til beinnar afhendingar.  
10. Velja skal Já í svæðinu Beina afhendingu.
    *   Ef varan hefur þegar verið sett upp fyrir beina afhendingu sjálfgefið, svæðið verður sjálfkrafa stillt á Já við færslu pöntunarlína. Hægt er að setja upp vöru fyrir beina afhendingu á sniðmát útgefinnar afurðar með valkostinn Bein afhending er stillt á Já og velja sjálfgefið vöruhús Beinnar afhendingar.  
    * Vegna þess að innkaupapöntunin hefur ekki enn verið stofnuð er Bein afhending staðan er stillt til að Afhenda beint.   
11. Lokið síðunni.
12. Lokið síðunni.
13. Fara á Beina afhendingu.
    * Síða Beinnar afhendingar þjónar sem vinnusvæðis sem veitir innkaupaaðila yfirlit yfir allar sölupöntunarlínur sem eiga að vera afhentar beint og gerir þær mögulegt að stofna samsvarandi innkaupapantanir. Þar að auki þeir geti skoðað opna beinar afhendingarpantanir og staðfestar pantanir á flipunum Staðfestingu og Afhending.   
14. Smellt er á Stofna beinar afhendingar
15. Smellið á staðfestarflipann
    * Þegar búið er að stofna pöntun fyrir beina afhendingu er það sjálfkrafa flutt í flipann Staðfestingu. Hægt er að velja að staðfesta pöntunina beint úr þessari síðu. Þegar innkaupin er að staðfesta það sjálfkrafa færist í flipanum Afhendingar, þar sem hægt er að skrá móttöku hans.  


