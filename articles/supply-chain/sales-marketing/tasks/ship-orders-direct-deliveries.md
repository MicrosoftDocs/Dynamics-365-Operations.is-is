---
title: Senda pantanir sem beinar afhendingar
description: Þetta efni sýnir hvernig á að búa til beina afhendingu fyrir sölupöntun.
author: omulvad
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart, PurchEditLines, PurchTable, PurchTableReferences, MCRDropShipWorkbench, SalesShippingLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31cb26479ccb74dfb58fd5590cd60d7b7c64c292
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430748"
---
# <a name="ship-orders-as-direct-deliveries"></a>Senda pantanir sem beinar afhendingar

[!include [banner](../../includes/banner.md)]

Þetta efni sýnir hvernig á að búa til beina afhendingu fyrir sölupöntun. Nota beina afhendingu þegar á að senda vörurnar viðskiptavininum beint frá lánardrottni í staðinn fyrir sendingu þær í eigin vöruhúsi fyrirtækisins fyrst. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Til að ljúka seinni undirverki "Stofna beinar afhendingar úr vinnusvæði", ganga úr skugga um vöru sem er valin á sölupöntun hefur sjálfgefið Lánardrottins tilgreindan á Flýtiflipanum Innkaupa fyrir Útgefnar afurðarsniðmát.

## <a name="set-an-individual-order-for-direct-delivery"></a>Stilla á einstaka pöntun fyrir beina afhendingu
1. Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Færa inn eða veljið gildi í svæðinu **Reikningur viðskiptavinar** og veldu síðan **Í lagi**.
4. Sláðu inn eða veldu gildi í **Vörunúmer** og **Vefsvæði** reitir, veldu síðan **Vista**.
5. Á Aðgerðarúða velurðu **sölupöntun** og síðan **bein afhending** Stofna afhendingu síðu sýnir allar opnar sölupöntunarlínurnar sem afritað er úr sölupöntuninni. Hægt er að skoða upplýsingar um pöntun, og ef þörf krefur, er hægt að breyta upplýsingum um slíkar innkaupamagn og verðskilmálar áður en hægt er að stofna beina afhendingu.  
6. Velja skal **Já** í reitnum **Taka með öll**.
    - Ef mynda á beina afhendingu fyrir aðeins hlutmengi sölupöntunarlínur, veljið þær sérstaklega.  
    - Svæðið **Lánardrottnalykill** getur eða ekki þegar vera með númer lánardrottins. Ef sjálfgefinn lánardrottinn er sett upp fyrir afurðina (á tengda vöruþekju) verður þessi lánardrottinn afritaður í línuna. Annars þarf að færa lánardrottinn handvirkt. Í þessu dæmi veljum við nýjan lánardrottinn í næsta skrefi jafnvel þótt þegar sé fyllt út.   
7. Færa inn eða veljið gildi í svæðinu **Lánardrottnalykill** og veldu síðan **Í lagi**. Skilaboðin tilkynnir að innkaupapöntunin hefur nú verið stofnuð.   
8. Útvíkkaðu hlutann **upplýsingar Línu**.
9. Veldu **Afhending** flipann og sannreyndu að **Bein afhending** reiturinn er stilltur á **Já**.
10. Í aðgerðasvæðinu velurðu **Almennt**.
11. Velja **Tengdar pantanir**.
12. Veldu tengilinn í retinum **Innkaupapöntun**.
13. Stækkaðu **Línulýsing** kafla og veldu **Heimilisfang** flipann.
    - Afhendingaraðsetur fyrir þessa innkaupapöntunarlínu er aðsetur viðskiptavinar og ekki aðsetur fyrirtækisins.  
    - Ef breytt er afhendingaraðsetrið á innkaupapöntunarlínunni eða upphaflegri sölupöntunarlínu er aðsetur í samsvarandi pöntunarlínu verða uppfærð sjálfkrafa.  
14. Velja flipann **Afhending**.
    - Eins og sölupöntunarlínu, tengt innkaupapöntunarlína er einnig stillt á Beina afhendingu.  
    - Dagsetning Afhendingar á innkaupapöntunarlínu vörunnar og Staðfest dagsetning afhendingar eru stillt á Umbeðinni móttökudagsetningu og Staðfest móttökudagsetning á upphaflegu sölupöntunarlínunni í þessari röð.   
    - Ef einhver dagsetningum á innkaupalína eða sölulínu verða dagsetningar á samsvarandi pöntun uppfærð sjálfkrafa.     
    - Innkaupapöntun sem er stillt á að afhenda vörur beint í viðskiptavin er tengd við upprunalegu sölupöntunina með sérstökum tengingu. Þessi tenging setur þá reglan að uppfærsla fylgiseðils fyrir sölupöntunar er ekki hægt að gera úr sölupöntun sjálf og verður að gera með því að nota innkaupapöntun. Hins vegar reikningsfærsla viðskiptavinar verður að vinna úr sölupöntun.  
15. Í aðgerðasvæðinu velurðu **Innkaup**.
16. Veldu **Staðfesting**.
17. Veljið **Í lagi**.
18. Í aðgerðasvæðinu velurðu **Móttaka**.
19. Velja **Innhreyfingarskjal afurða**.
20. Í reitinn **Innhreyfingarskjal afurða** skal slá inn gildi.
21. Veljið **Í lagi**.
22. Í aðgerðasvæðinu velurðu **Almennt**.
23. Veldu **Skyldar pantanir** og auðkenndu viðeigandi skrá.
    - Þegar innkaupapöntun hefur verið uppfærð sem móttekin eða með öðrum orðum, eftir að lánardrottinn hefur sent til aðsetur viðskiptavinarins, er staða upphaflegrar sölupöntunar sjálfkrafa uppfærist í Afhent.  
    - Nú er hægt að reikningsfæra sölupöntunina.    
24. Veljið **Í lagi**.
25. Lokið síðunni.
26. Veljið **Í lagi**. Lokið síðunum og farið aftur á heimasíðuna.

## <a name="create-direct-deliveries-from-the-workbench"></a>Stofna beinar afhendingar úr á vinnusvæði
1. Farðu í **Yfirlit > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Færa inn eða veljið gildi í svæðinu **Reikningur viðskiptavinar** og veldu síðan **Í lagi**.
4. Færðu eða veldu gildi í reitunum **Vörunúmer** og **Svæði**.
5. Stækkaðu hlutann **Línuupplýsingar**, veldu síðan flipann **Afhending**. Í stað þess að stofna beina afhendingu sem hluta af vinnslu sölupöntunar eins og í fyrra ferli er hægt að velja að afhenda þessu verki til innkaupasérfræðings. Til að taka með sölupöntunarlínu í ferli beinnar afhendingar, verður að merkja línuna til beinnar afhendingar.  
6. Velja skal **Já** í svæðinu **Bein afhending**.
    - Ef varan hefur þegar verið sett upp fyrir beina afhendingu sjálfgefið, svæðið verður sjálfkrafa stillt á Já við færslu pöntunarlína. Hægt er að setja upp vöru fyrir beina afhendingu á sniðmát útgefinnar afurðar með valkostinn Bein afhending er stillt á Já og velja sjálfgefið vöruhús Beinnar afhendingar.  
    - Vegna þess að innkaupapöntunin hefur ekki enn verið stofnuð er Bein afhending staðan er stillt til að Afhenda beint.   
7. Veljið **Vista**.
8. Lokið síðunum þar til komið er aftur á heimasíðuna.
9. Færa skal `Direct delivery` inn í leitarstikuna.
    - Síða Beinnar afhendingar þjónar sem vinnusvæðis sem veitir innkaupaaðila yfirlit yfir allar sölupöntunarlínur sem eiga að vera afhentar beint og gerir þær mögulegt að stofna samsvarandi innkaupapantanir. Þar að auki þeir geti skoðað opna beinar afhendingarpantanir og staðfestar pantanir á flipunum Staðfestingu og Afhending.  
    - Þegar búið er að stofna pöntun fyrir beina afhendingu er það sjálfkrafa flutt í flipann Staðfestingu. Hægt er að velja að staðfesta pöntunina beint úr þessari síðu. Þegar innkaupin er að staðfesta það sjálfkrafa færist í flipanum Afhendingar, þar sem hægt er að skrá móttöku hans.  

