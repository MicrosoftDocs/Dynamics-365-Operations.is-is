---
title: Stofna innkaupapöntun úr sölupöntun
description: Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun sem byggist á sölupöntun.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7991476b86ace92cda513ae8906c62ba7fbbe915
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547423"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Stofna innkaupapöntun úr sölupöntun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun sem byggist á sölupöntun. Magn afurðarinnar á innkaupapöntuninni eru síðan hannaðir til að uppfylla eftirspurn upphaflegrar sölupöntunar. Uppfylling þannig að sölueftirspurn er annar valkostur við yfirgripsmeiri og bestuð aðferð við Dreifingu Kröfum Áætlanagerðar. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Stofna innkaupapöntun úr sölupöntun
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Smellt er á Í lagi.
6. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota USMF, var hægt að velja D0001.  
8. Færið inn númer í reitnum „Magn“.
9. Smellið á „Bæta við línu“.
10. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota USMF, var hægt að velja T0020.  
12. Í listanum skal smella á tengilinn í valinni línu.
13. Færið inn númer í reitnum „Magn“.
14. Smelltu á Vista.
15. Smellið á „Sölupöntun“ á aðgerðarúðunni.
16. Smellt er á Innkaupapöntunarlína.
    * Stofna innkaupapöntunarsíðu sýnir allar opnar sölupöntunarlínurnar sem afritað er úr sölupöntuninni. Hægt er að skoða upplýsingar um pöntun, og ef þörf krefur, er hægt að breyta völdum upplýsingum um slíkar innkaupamagn og verðskilmálar áður en hægt er að stofna innkaup .  
17. Veljið valkostinn er Taka allar með
    * Ef mynda á innkaupapöntun fyrir aðeins hlutmengi sölupöntunarlínur, veljið þær sérstaklega.  
    * Svæðið fyrir reikninga Lánardrottins getur eða ekki þegar vera með númer lánardrottins. Ef sjálfgefinn lánardrottinn er sett upp fyrir afurðina (á tengda vöruþekju) þessi lánardrottinn verða afritaðar í línuna. Annars þarf að færa lánardrottinn handvirkt.  Í þessari handbók, óháð því hvort svæðið Lánardrottins þegar inniheldur gildi eða ekki, eftirfarandi skref sýna hvernig á að velja nýja lánardrottins sem eru mismunandi fyrir hverja línu.  
18. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
19. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
20. Í listanum skal smella á tengilinn í valinni línu.
21. Veljið pöntunarlínu númer tvö.
22. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
23. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
24. Í listanum skal smella á tengilinn í valinni línu.
25. Smella á Villuleita.
26. Smellið á „Í lagi“.
    * Skilaboðin tilkynnir þér að ein eða fleiri innkaupapantanir hafa verið stofnaðar. Kerfið myndar til aðskilda innkaupapöntun fyrir hvern lánardrottin sem tilgreindur er í sölupöntunarlínum. Þetta þýðir að ef margar sölupöntunarlínur eiga að vera frá sama lánardrottni, eina innkaupapöntun fyrir með margar línur eru mynduð.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Yfirfara innkaupapantanir stofnaðar úr sölupantana
1. Smellið á „Almennt“ á aðgerðarúðunni.
2. Smellt er á Tengdar pantanir.
    * Tengdar pantanir síða inniheldur lista yfir allar pantanir sem voru stofnaðar úr sölupöntun. Í þessu dæmi eru tvær innkaupapantanir búnar til fyrir tveimur mismunandi lánardrottnum í þessari röð.  
3. Smellið til að velja tengilinn í reitnum Innkaupapöntun.
    * Hvert innkaupapöntunarlína er tengd sölupöntunarlína sem leiddi til innkaupanna. Vensl á sölupöntun er tilgreint á afurðaflipanum í flýtiflipi línuupplýsingar, í svæðunum tilvísunargerð, tilvísunarnúmer og tilvísunarlota.  
4. Útvíkka eða draga saman hluta upplýsingar Línu.
5. Smellið á flipann Afurðar.
    * Tilvísunarlota tryggir að kostnaður úr núgildandi Innkaup eru gjaldfærð á viðhengda sölupöntun.  
    * Hægt er að fara á upprunalegri sölupöntun með því að opna tengil í svæðinu Tilvísunarnúmer.  

