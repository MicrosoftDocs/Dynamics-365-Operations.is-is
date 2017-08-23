--- 
title: "Setja upp reglur söluþóknunar"
description: "Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a>Setja upp reglur söluþóknunar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu. Ferlið sýnir hvernig á að stofna bæði sölulaunaflokka viðskiptavina og vöru og svo hvernig á að tengja við valinn viðskiptavin og afurð viðkomandi flokka. Þessir flokkar eru síðan notaðir í uppsetningu á útreikningi þóknunar til að stofna samsetningu viðskiptavinar, vöru og sölufulltrúa sem jafna verður við sölupöntun til að heimila sölufulltrúum að fá þóknun. Valfrjálst er að stofna sölulaunaflokk viðskiptavinar og vöru, þar sem einnig er hægt að reikna þóknun fyrir stakan viðskiptavin og/eða vöru. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="set-up-commission-groups-and-commission-rates"></a>Setja upp þóknunarflokka og umboðslaunataxta
1. Fara í Sölu og markaðssetningu > Þóknanir > Viðskiptavinaflokkar þóknunar.
2. Smellið á „Nýtt“.
3. Í reitinn Hópur skal slá inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Smellið á „Vista“.
6. Lokið síðunni.
7. Fara í Sölu og markaðssetningu > Þóknanir > Vöruflokkar.
8. Smellið á „Nýtt“.
9. Í reitinn Hópur skal slá inn gildi.
10. Í reitinn Heiti skal slá inn gildi.
11. Lokið síðunni.
12. Fara í Sölu og markaðssetningu > Þóknanir > Söluflokkar.
    * Söluflokkur Þóknunar tilgreinir starfsmenn í hlutverki sölufulltrúa sem eru hæfir til að fá þóknun þegar viðskiptavinur tengdur viðeigandi söluflokk kaupir tilteknar vörur.  
    * Í sýnifyrirtækinu USMF er söluflokkur sem heitir „Sölufulltrúar US“.  
13. Smellið á „Almennt“ á aðgerðarúðunni.
14. Smellt er á Sölufulltrúa...
    * Sölufulltrúinn síðan birtir lista yfir sölumenn fyrirtækisins sem eru tengdar við tiltekinn þóknunarflokk. Hægt er að úthluta mörgum sölufulltrúum á sama flokk og skilgreina viðkomandi hluta þeirra í heildarþóknun sem prósentugildi. Heildarþóknunarhluti yfir alla starfsmenn má ekki fara yfir 100.  
15. Í listanum skal merkja valda línu.
16. Smellið á „Breyta“.
17. Stilla þóknunarhluti á '50'.
18. Smellið á „Nýtt“.
19. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
20. Nota Síu á Flýtiræsistikunni til að leita að færslum. Til dæmis, sía svæðið Heiti með gildinu 'Susan Burk'.
21. Smellið á Velja.
22. Stilla þóknunarhluti á '50'.
23. Smellið á „Vista“.
24. Fara í Sölu og markaðssetningu > Þóknanir > Útreikningur þóknunar.
    * Á síðunni Útreikningur á þóknun skilgreinirðu umboðslaunataxta sem starfsmaðurinn á að fá sölufærslu fyrir þegar hún inniheldur fyrirframstillta samsetningu viðskiptavinar og vöru. Sem hluti af uppsetningu umboðslaunataxta verður að tilgreina grundvöll fyrir útreikning þóknunar og hvort hún eigi að taka með eða útiloka afslætti. Hægt er að færa inn gildistímabil þegar umboðslaunataxti er virkur.  
25. Smellið á „Nýtt“.
26. Í reitnum vörukóði er valið 'flokkur'.
27. Í reitnum Vöruvensl skal smella á fellilistahnappinn til að opna leitina.
28. Í listanum finnurðu og velur flokk sem þú stofnaðir áður.
29. Í listanum skal smella á tengilinn í valinni línu.
30. Í reitnum Viðskiptavinakóði er valið „Flokkur“.
31. Í reitnum Tengsl viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
32. Á listanum velurðu flokkinn sem áður var settur upp.
33. Í Sölufulltrúa í reitnum Tengsl skal smella á fellilistahnappinn til að opna leitina.
34. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Halda valkosturinn „Fyrir línuafslátt".  
    * Halda valkosturinn "Tekjur" sem grunni fyrir útreikning á þóknana gildi.    
35. Færið inn tölu í reitinn þóknunarprósenta.
36. Smellið á „Vista“.

## <a name="setting-up-commission-posting"></a>Uppsetning á þóknunarbókun
1. Fara í Sölu og markaðssetningu > Þóknanir > Bókun þóknunar.
    * Þóknun er greiðsla til starfsmanna og hana verður því að setja upp til að tryggja rétta fjárhagsbókun á viðeigandi lykla í fjárhag. Þetta er gert á bókunarsíðu Þóknunar. Endurskoða uppsetningu sem er tiltæk fyrir gildandi fyrirtæki. Yfirleitt eru upphæðir þóknunar bókaðar á sérstakan kostnaðarlykil og jafnaðar við sérstakan reikning lánardrottna. Ef ekki er búið að setja upp bókunarreglur þóknunar mun kerfinu ekki takast að ljúka reikningsfærslu sölupöntunarinnar sem er með hæfar þóknanir.  
2. Lokið síðunni.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Úthluta þóknunarflokki á viðskiptavin og afurð
1. Fara í Sölu og markaðssetningu > Viðskiptavinir > Allir viðskiptavinir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smella á Breyta.
5. Útvíkka hlutann Sjálfgildi sölupöntunar.
6. Í reitnum Sölulaunaflokkur skal smella á fellilistahnappinn til að opna leitina.
7. Á listanum velurðu flokkinn sem þú stofnaðir áður.
8. Í reitnum Söluflokkur skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellið á „Vista“.
11. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
12. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Vara með gildinu 'T0020'.
13. Í listanum skal smella á tengilinn í valinni línu.
14. Smella á Breyta.
15. Útvíkka hlutann Selja.
16. Í reitnum Sölulaunaflokkur skal smella á fellilistahnappinn til að opna leitina.
17. Á listanum velurðu þóknunarflokk sem þú stofnaðir áður.


