---
title: Stofna innkaupapöntun úr sölupöntun
description: Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun sem byggist á sölupöntun.
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ca91f17c13e210a4df6c22e0ed12370179bb866
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572473"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Stofna innkaupapöntun úr sölupöntun

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun sem byggist á sölupöntun. Magn afurðarinnar á innkaupapöntuninni eru síðan hannaðir til að uppfylla eftirspurn upphaflegrar sölupöntunar. Uppfylling þannig að sölueftirspurn er annar valkostur við yfirgripsmeiri og bestuð aðferð við Dreifingu Kröfum Áætlanagerðar. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Stofna innkaupapöntun úr sölupöntun
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Smellt er á **OK**.
6. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Ef verið er að nota USMF, var hægt að velja D0001.  
8. Í reitnum **Magn** slærðu inn tölu.
9. Smella á **Bæta við línu**.
10. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Ef verið er að nota USMF, var hægt að velja T0020.  
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í reitnum **Magn** slærðu inn tölu.
14. Smellt er á **Vista**.
15. Á **Aðgerðasvæðinu** skal smellt á **Sölupöntun**.
16. Smelltu á **Innkaupapöntun**. Síðan **Stofna innkaupapöntun** sýnir allar opnar sölupöntunarlínurnar sem afritað er úr sölupöntuninni. Hægt er að skoða upplýsingar um pöntun, og ef þörf krefur, er hægt að breyta völdum upplýsingum um slíkar innkaupamagn og verðskilmálar áður en hægt er að stofna innkaup . 
17. Veldu **Taka alla valkosti með**.
    - Ef mynda á innkaupapöntun fyrir aðeins hlutmengi sölupöntunarlínur, veljið þær sérstaklega.  
    - Svæðið **Lánardrottnalykill** getur eða ekki þegar vera með númer lánardrottins. Ef sjálfgefinn lánardrottinn er sett upp fyrir afurðina (á tengda vöruþekju) þessi lánardrottinn verða afritaðar í línuna. Annars þarf að færa lánardrottinn handvirkt.  Í þessari handbók, óháð því hvort reiturinn **Lánardrottnalykill** inniheldur þegar gildi eða ekki, sýna eftirfarandi skref hvernig á að velja nýja lánardrottins sem eru mismunandi fyrir hverja línu.  
18. Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina.
19. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
20. Í listanum skal smella á tengilinn í valinni línu.
21. Veljið pöntunarlínu númer tvö.
22. Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina.
23. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
24. Í listanum skal smella á tengilinn í valinni línu.
25. Smelltu á **Villuleita**.
26. Smellt er á **OK**. Skilaboðin tilkynnir þér að ein eða fleiri innkaupapantanir hafa verið stofnaðar. Kerfið myndar til aðskilda innkaupapöntun fyrir hvern lánardrottin sem tilgreindur er í sölupöntunarlínum. Þetta þýðir að ef margar sölupöntunarlínur eiga að vera frá sama lánardrottni, eina innkaupapöntun fyrir með margar línur eru mynduð.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Yfirfara innkaupapantanir stofnaðar úr sölupantana
1. Á **aðgerðasvæðinu** er smellt á **Almennt**.
2. Smelltu á **Tengdar pantanir**. Síðan **Tengdar pantanir** inniheldur lista yfir allar pantanir sem voru stofnaðar úr sölupöntun. Í þessu dæmi eru tvær innkaupapantanir búnar til fyrir tveimur mismunandi lánardrottnum í þessari röð. 
3. Smelltu til að fylgja tenglinum í reitnum **Innkaupapöntun**. Hvert innkaupapöntunarlína er tengd sölupöntunarlína sem leiddi til innkaupanna. Vensl við sölupöntun eru tilgreind á flipanum **Afurð** á flýtiflipanum **Línuupplýsingar**, í reitunum **Tilvísunargerð**, **Tilvísunarnúmer** og **Tilvísunarlota**.  
4. Útvíkkaðu eða dragðu saman hlutann **Línuupplýsingar**.
5. Smelltu á flipann **Afurð**.
    - **Tilvísunarlota** tryggir að kostnaður úr núgildandi Innkaup eru gjaldfærð á viðhengda sölupöntun.  
    - Hægt er að fara á upprunalegri sölupöntun með því að opna tengil í svæðinu **Tilvísunarnúmer**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]