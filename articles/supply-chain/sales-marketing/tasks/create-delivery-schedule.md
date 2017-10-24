--- 
title: "Stofna afhendingaráætlun"
description: "Þetta ferli sýnir hvernig á að stofna afhendingaráætlun fyrir sölupöntun."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
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
ms.openlocfilehash: 956edeac33f8531ecebef64301f2318333000429
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-delivery-schedule"></a>Stofna afhendingaráætlun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að stofna afhendingaráætlun fyrir sölupöntun. Afhendingaráætlun er notaður þegar magn í pöntun beðið er um að afhenda í margar sendingar. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="create-delivery-schedule"></a>Stofna afhendingaráætlun
1. Fara í Allar sölupantanir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
4. Smellt er á Í lagi.
5. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
6. Í reitinn magn skal slá inn númer sem er stærra en 1
7. Smellið á „Sölupöntunarlína“.
8. Smellið á „Afhendingaráætlun“.
    * Síðan Afhendingaráætlun er staðurinn þar sem hægt er að tilgreina fjölda sendinga þar sem heildarmagn pöntunarlínu verða afhentar viðskiptavininum.    
    * Að sjálfgefnu kerfið afritar heildarmagn og aðrar upplýsingar um afhendingu á upprunalegri sölulínu í fyrstu afhendingaráætlunarlínu. Í þessu dæmi stofnum við áætlun fyrir tvær sendingar og sendingardagsetningin er stillt viku eftir þá fyrstu.  
9. Í reitinn magn skal slá inn númer sem er hluti af heildarmagni
10. Smellt er á Nýtt.
11. Í reitnum Magn skal slá inn eftirstandandi magn.
12. Í reitnum Umbeðinni sendingardagsetningu skal færa inn dagsetningu sem er eina viku á undan dagsetningu fyrstu afhendingarlínu.
    * Tveir valmöguleikar á flýtiflipanum Gjöld fyrir umreikning stýrir hvernig á að dreifa á milli afhendingar á að raða línum þegar þeim hefur verið búið að úthluta upprunalegu pöntunarlínunni. Ef valið er Afrita brúttóupphæðir, er sömu upphæð gjalda afritað í hverja línu. Valkosturinn Úthlutun á afhendingarlínur skiptir gjöld jafnt yfir í afhendingarlínur.  
    * Aðeins föst gjöld hægt er að skipta niður, en enn verða afritaðar breytileg gjöld í línur.  
13. Færðu Bendillinn frá önnur afhendingarlína til að uppfæra síðu.
    * Þú getur fylgst með heildarmagn sem úthlutað er til í línur afhendingaráætlunar með því að líta á svæðin Samtölu og Eftirstandandi. Þegar eftirstöðvar magns eru núll, allt magnið í upphaflegu línunni hefur verið úthlutað á áætlun.   
14. Smellið á „Í lagi“.
    * Afhendingaráætlunin hefur nú verið afrituð í pöntunarlínurnar.   
    * Upprunalegri pöntunarlínunni, nefnt Heildarsöluverðmæti línu, hefur verið breytt í pöntunarlínu með margar afhendingar. Hún er merkt með áberandi tákni og þjónar sem haus fyrir afhendingarlínur.  
    * Hinar tvær nýju línurnar, sem nefndar eru afhendingarlínur, mynda í sameiningu eina afhendingaráætlun. pöntunina verður unnin gegn þessum línum og ekki gagnvart upphaflegu línunni. Ef skjöl eins og staðfestingarseðlar, tiltektarlista, fylgiseðla eða reikninga eru prentaðar, eru eingöngu afhendingarlínur sýndar.   
    * Afhendingarlínur getur haft mismunandi afhendingardagsetningar, magn, afhendingarmáti og geymsluvíddir, eins og svæði og vöruhús. Hins vegar afurðarvíddum alltaf verður að samsvara þeim sem eru á viðskiptalínu og ekki er hægt að breyta.  
15. Í reitinn magn skal slá inn númer sem er stærra en núverandi tala.
16. Veljið viðskiptalínu til að sjá áhrifin endurútreiknings magns.
17. Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.
18. Smellt er á Bóka fylgiseðil.
19. Víkkið út færibreytuhlutann.
20. Veljið „Allt“ á svæðinu „Magn“.
    * Athugið að fylgiseðill verður stofnuð fyrir tvær línur afhendingaráætlunar og ekki upprunalegu pöntunarlínunni.  
21. Velja skal Já í svæðinu Prenta fylgiseðill.
22. Smellið á „Í lagi“.
23. Smella á Já.
24. Lokið síðunni.


