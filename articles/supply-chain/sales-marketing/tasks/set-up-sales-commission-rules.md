---
title: Setja upp reglur söluþóknunar
description: Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu.
author: omulvad
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d575e609ac5289f9acb219322c9df93972e5dfc
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995214"
---
# <a name="set-up-sales-commission-rules"></a>Setja upp reglur söluþóknunar

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu. Ferlið sýnir hvernig á að stofna bæði sölulaunaflokka viðskiptavina og vöru og svo hvernig á að tengja við valinn viðskiptavin og afurð viðkomandi flokka. Þessir flokkar eru síðan notaðir í uppsetningu á útreikningi þóknunar til að stofna samsetningu viðskiptavinar, vöru og sölufulltrúa sem jafna verður við sölupöntun til að heimila sölufulltrúum að fá þóknun. Valfrjálst er að stofna sölulaunaflokk viðskiptavinar og vöru, þar sem einnig er hægt að reikna þóknun fyrir stakan viðskiptavin og/eða vöru. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="set-up-commission-groups-and-commission-rates"></a>Setja upp þóknunarflokka og umboðslaunataxta
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala- og markaðssetning > Þóknanir > Viðskiptavinaflokkar þóknunar**.
2. Veljið **Nýtt**.
3. Í reitinn **Hópur** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Veljið **Vista**.
6. Lokið síðunni.
7. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala- og markaðssetning > Þóknanir > Vöruflokkar**.
8. Veljið **Nýtt**.
9. Í reitinn **Hópur** skal slá inn gildi.
10. Í reitinn **Heiti** skal slá inn gildi.
11. Veljið **Vista**.
12. Lokið síðunni.
13. Farðu í **Sala og markaðssetning > Þóknanir > Söluflokkar**.
    - Söluflokkur Þóknunar tilgreinir starfsmenn í hlutverki sölufulltrúa sem eru hæfir til að fá þóknun þegar viðskiptavinur tengdur viðeigandi söluflokk kaupir tilteknar vörur.  
    - Í sýnifyrirtækinu USMF er söluflokkur sem heitir „Sölufulltrúar US“.  
14. Í **aðgerðasvæðinu** velurðu **Almennt**.
15. Smelltu á **Sölufulltrúa**. Síðan Sölufulltrúi sýnir lista yfir sölufulltrúa fyrirtækisins sem tengjast ákveðnum þóknunarflokki. Hægt er að úthluta mörgum sölufulltrúum á sama flokk og skilgreina viðkomandi hluta þeirra í heildarþóknun sem prósentugildi. Heildarþóknunarhluti yfir alla starfsmenn má ekki fara yfir 100. 
16. Í listanum skal merkja valda línu.
17. Veljið **Breyta**.
18. Stilla **þóknunarhlut** á '50'.
19. Smellt er á **Nýtt**.
20. Í reitnum **Heiti** skal smella á fellilistahnappinn til að opna leitina.
21. Nota **Flýtiafmörkun** til að finna skrár. Til dæmis, sía svæðið Heiti með gildinu 'Susan Burk'.
22. Smellið á **Velja**.
23. Stilla **þóknunarhlut** á '50'.
24. Smellt er á **Vista**.
25. Farðu í **Sala og markaðssetning > Þóknanir > Útreikningur þóknunar**. Á síðunni **Útreikningur á þóknun** skilgreinirðu umboðslaunataxta sem starfsmaðurinn á að fá sölufærslu fyrir þegar hún inniheldur fyrirframstillta samsetningu viðskiptavinar og vöru. Sem hluti af uppsetningu umboðslaunataxta verður að tilgreina grundvöll fyrir útreikning þóknunar og hvort hún eigi að taka með eða útiloka afslætti. Hægt er að færa inn gildistímabil þegar umboðslaunataxti er virkur.  
26. Smellt er á **Nýtt**.
27. Í reitnum **vörukóði** er valið 'flokkur'.
28. Í reitnum **Vöruvensl** skal smella á fellilistahnappinn til að opna uppflettinguna.
29. Í listanum finnurðu og velur flokk sem þú stofnaðir áður.
30. Í reitnum **Viðskiptavinakóði** er valið flokkur.
31. Í reitnum **Tengsl viðskiptavina** skal smella á fellilistahnappinn til að opna leitina.
32. Á listanum velurðu flokkinn sem áður var settur upp.
33. Í reitnum **Vensl sölumanns** skal smella á fellilistahnappinn til að opna leitina.
34. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    - Halda valkosturinn „Fyrir línuafslátt".  
    - Halda valkosturinn "Tekjur" sem grunni fyrir útreikning á þóknana gildi.    
35. Færið inn tölu í reitinn þóknunarprósenta.
36. Smellt er á **Vista**.

## <a name="setting-up-commission-posting"></a>Uppsetning á þóknunarbókun
1. Farðu í **Skoðunarrúðu > Sala- og markaðssetning > Þóknanir > Bókun þóknunar**. Þóknun er greiðsla til starfsmanna og hana verður því að setja upp til að tryggja rétta fjárhagsbókun á viðeigandi lykla í **Fjárhag**. Þetta er gert á síðunni **Bókun þóknunar**. Endurskoða uppsetningu sem er tiltæk fyrir gildandi fyrirtæki. Yfirleitt eru upphæðir þóknunar bókaðar á sérstakan kostnaðarlykil og jafnaðar við sérstakan reikning lánardrottna. Ef ekki er búið að setja upp bókunarreglur þóknunar mun kerfinu ekki takast að ljúka reikningsfærslu sölupöntunarinnar sem er með hæfar þóknanir.  
2. Lokið síðunni.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Úthluta þóknunarflokki á viðskiptavin og afurð
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala- og markaðssetning > Viðskiptavinir > Allir viðskiptavinir**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smellið á **Breyta**.
5. Útvíkkaðu hlutann **Sjálfgildi sölupöntunar**.
6. Í reitnum **Þóknunarflokkur** skal smella á fellilistahnappinn til að opna leitina.
7. Á listanum velurðu flokkinn sem þú stofnaðir áður.
8. Í reitnum **Söluflokkur** skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellt er á **Vista**.
11. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.
12. Nota **Síu** til að finna skrár. Til dæmis, sía svæðið Vara með gildinu 'T0020'.
13. Í listanum skal smella á tengilinn í valinni línu.
14. Smellið á **Breyta**.
15. Útvíkkaðu hlutann **Selja**.
16. Í reitnum **Þóknunarflokkur** skal smella á fellilistahnappinn til að opna leitina.
17. Á listanum velurðu þóknunarflokk sem þú stofnaðir áður.
18. Veljið **Vista**.

