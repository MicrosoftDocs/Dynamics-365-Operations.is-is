--- 
title: "Stofna fjölda sölutilboða"
description: "Þetta ferli sýnir hvernig stofna á hagkvæman hátt tilboð og bjóða úrval af vörum eða þjónustu sem á að senda mörg viðskiptavinum."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fcb2c4d47f0c8e701be025e0554ed476693d732
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="mass-create-sales-quotations"></a>Stofna fjölda sölutilboða

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig stofna á hagkvæman hátt tilboð og bjóða úrval af vörum eða þjónustu sem á að senda mörg viðskiptavinum. Stofnun margra tilboða er byggt á tilboðssniðmát. Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.


## <a name="create-a-quotation-template"></a>Stofna a sniðmát tilboðs
1. Fara í Sölu og markaðssetningu > Uppsetning > Tilboð > Sniðmátsflokka.
2. Smellið á „Nýtt“.
3. Rita Kenni að eigin vali í svæðinu Flokkskenni.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellið á „Vista“.
6. Lokið síðunni.
7. Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.
8. Smellið á „Nýtt“.
9. Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.
10. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
11. Smellið á „Í lagi“.
    * Fyrir tilboð að verða sniðmát verður að framkvæma uppsetningu skref í tilboðshausnum. Það verður gert áður en línum er bætt við tilboðið.   
12. Í aðgerðasvæðinu er smellt á valkostir.
13. Smellið á skoða Breytingu.
14. Smellið á skoða Haus.
15. Víkka út hlutann Uppsetning.
16. Í reitinn kenni hóps skal slá inn eða velja gildi.
17. Í reitinn Heiti sniðmáts skal slá inn gildi.
18. Velja skal Já í Virka svæðinu.
    * Hægt er að nota aðeins virk sniðmát þegar sniðmátsuppskrift er beitt í nýja sölutilboðið.  
19. Í aðgerðasvæðinu er smellt á valkostir.
20. Smellið á skoða Breytingu.
21. Smellið á Línuyfirlit.
22. Í reitinn vara skal slá inn eða veldu gildi.
23. Í reitinn vara skal slá inn gildi.
24. Lokið síðunni.
25. Færið inn tölu í svæðinu afsláttarprósenta.
26. Smella á bæta Við línu.
27. Í reitinn vara skal slá inn eða veldu gildi.
28. Í reitinn vara skal slá inn gildi.
29. Lokið síðunni.
30. Færa inn nýtt verð eða breyta gildandi í svæðinu einingarverð.
31. Smella á bæta Við línu.
32. Í reitinn vara skal slá inn eða veldu gildi.
33. Í reitinn vara skal slá inn gildi.
34. Lokið síðunni.
35. Færið inn númer í reitnum „Magn“.
36. Í reitinn afsláttur skal slá inn númer.
37. Smellið á „Vista“.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Nota sniðmát til að stofna eitt tilboð
1. Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.
    * Athugið að tilboð sem þú varst að stofna er merkt sem sniðmát.  
2. Smellið á „Nýtt“.
3. Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.
4. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
5. Stækkaðu hlutann Sniðmát.
6. Í reitinn kenni hóps skal slá inn eða velja gildi.
7. Sláið inn eða veldu gildi í reitnum heiti sniðmáts.
8. Veljið í svæðinu útreikningsaðferð 'Byggt á sniðmátsgildum'.
9. Smellið á „Í lagi“.
    * Nýtt tilboð hefur nú verið stofnað, byggt á gögnum og skilmála sniðmátsins.  
10. Lokið síðunni.
11. Lokið síðunni.

## <a name="apply-the-template-to-mass-create-quotations"></a>Nota sniðmát til að stofna fjölda tilboða
1. Fara í Sölu og markaðssetningu > Sölutilboð > Uppfærsla tilboðs > Stofna fjölda tilboða.
2. Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.
3. Í reitinn kenni hóps skal slá inn eða velja gildi.
4. Sláið inn eða veldu gildi í reitnum heiti sniðmáts.
5. Veljið í svæðinu útreikningsaðferð 'Byggt á sniðmátsgildum'.
6. Útvíkka Færslur til að taka hluta.
7. Smellt er á Síu.
8. í svæðinu Skilyrði, Stilla síu til að ná yfir svið viðskiptavina sem á að taka með í þetta stofnun fjöldatilboðs. Notaðu eftirfarandi snið „Viðskiptavinur1... ViðskiptavinurN.
    * Til dæmis væri hægt að setja síu: US-001..US-004  
9. Smellið á „Í lagi“.
10. Smellið á „Í lagi“.
11. Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.
    * Staðfestið að tilboð hafa verið stofnaðar fyrir alla viðskiptavini sem eru tilgreind í fjöldauppfærslu, sem byggist á völdu sniðmáti.  


