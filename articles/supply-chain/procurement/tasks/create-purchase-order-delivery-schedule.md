--- 
title: "Stofna innkaupapöntun með afhendingaráætlun"
description: "Þetta ferli sýnir hvernig á að stofna afhendingaráætlun fyrir innkaupapöntun."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Stofna innkaupapöntun með afhendingaráætlun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að stofna afhendingaráætlun fyrir innkaupapöntun. Afhendingaráætlun er notaður þegar magn í pöntun eða færslubók er beðið um að sé afhent í margar sendingar. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Þetta ferli myndi yfirleitt gert af innkaupaaðila.


## <a name="create-a-delivery-schedule"></a>Stofna afhendingaráætlun
1. Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Í svæðinu Lánardrottnalykill skal slá inn 'US-101'.
4. Smellið á „Í lagi“.
5. Í svæðið vörunúmer sláið inn M0001.
6. Fært er inn 10 í reitinn Magn.
7. Smellt er á Innkaup Innkaupapöntunarlína
8. Smellið á „Afhendingaráætlun“.
    * Síðan Afhendingaráætlun leyfir þér að tilgreina fjölda sendinga þar sem heildarmagn pöntunarlínu verða afhentar frá lánardrottinn.  
    * Að sjálfgefnu afritar kerfið heildarmagn og aðrar upplýsingar um afhendingu á upprunalegri innkaupalínu í fyrstu afhendingaráætlunarlínu. Í þessu dæmi stofnum við áætlun fyrir tvær sendingar og sendingardagsetning seinni sendingar er stillt viku eftir fyrstu sendinguna.  
9. Magninu er breytt í 4 í reitnum Magn.
10. Smellið á „Nýtt“.
11. Í reitnum Magn skal slá inn 6 sem eftirstandandi magn.
    * Í svæðinu dagsetning afhendingar, veljið dagsetningu sem er ein vika eftir dagsetningu fyrstu afhendingarlínu.  
    * Þú getur fylgst með heildarmagn sem úthlutað er til í línur afhendingaráætlunar með því að líta á svæðin Samtölu og Eftirstandandi. Þegar eftirstöðvar magns eru núll, allt magnið í upphaflegu línunni hefur verið úthlutað á áætlun.  
12. Útvíkka hlutann umreikningur gjalda.
    * Valkostir hér gera þér kleift að stjórna því hvernig á að dreifa gjöldum yfir í línur afhendingaráætlunar. Ef valið er Afrita brúttóupphæðir, er gjaldupphæð á upprunaleg pöntunarlína afritað í hverja pöntunarlínu. Valkosturinn úthluta á afhendingarlínur deilir upprunalegum línugjöldum samkvæmt magninu á hverri afhendingarlínu.  
13. Fella saman hluta umreikningur gjalda.
14. Smellið á „Í lagi“.
    * Afhendingaráætlunin hefur nú verið notuð í pöntunina.  
    * Upprunalegri pöntunarlínunni, nú nefnt viðskiptalína, hefur verið breytt í pöntunarlínu með margar afhendingar. Þetta er merkt með sérstöku tákni og virkar sem haus fyrir afhendingarlínurnar.  
15. Veljið aðra pöntunarlínuna sem er sú fyrri af tveimur afhendingarlínum.
    * Tvær nýjar línur sem vísað er til sem afhendingarlínur, mynda í sameiningu eina afhendingaráætlun. pöntunina verður unnin gegn þessum línum og ekki gagnvart upphaflegu línunni. Ef skjöl eins og staðfestingar, færslubók innhreyfingarskjals, eða reikninga eru prentaðar, eru eingöngu afhendingarlínur sýndar.  

## <a name="change-the-delivery-schedule"></a>Breyta Afhendingaráætlun
    * Hægt er að breyta magni í afhendingarlínum. Ef þetta er gert er viðskiptalínan uppfærð sjálfkrafa í heildarmagn í afhendingarlínunum.  
1. Í svæðinu magn í fyrstu afhendingarlínu, skal breyta magninu úr 4 í 5.
2. Veljið fyrsta pöntunarlínu (viðskiptalínuna).
    * Magn á viðskiptalínunni hefur verið breytt í 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Vinna úr innhreyfingarskjal afurða með afhendingaráætlanir
    * Þarf að staðfesta innkaupapöntun áður en hægt er að vinna úr innhreyfingarskjali afurða. Í þessu tilfelli er móttakan yfirleitt skráðar beint á Innkaupapöntunina. Kvittun gæti einnig hafa verið skráð þegar vörurnar komu í vöruhúsinu.  
1. Smellið á „Innkaup“ á aðgerðarúðunni.
2. Smellið á „Staðfesta“.
3. Smellið á „Móttaka“ á aðgerðarúðunni.
4. Smellið á „Innhreyfingarskjal“.
5. Í reitinn móttaka afurða skal slá inn hvaða gildi sem er.
    * Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.  
    * Í svæðinu magn skal velja "pantað magn" Þessi valkostur þýðir að móttaka verður unnið fyrir magnið sem pöntunarlínur voru stofnaðar með.  
    * Gangið úr skugga um að Prenta innhreyfingarskjal afurða svæðið er stillt á nei. Prentun er ekki þörf í þessu dæmi.  
6. Stækka línuhlutann.
    * Athugið hvernig innhreyfingarskjal afurða er stofnað fyrir tvær afhendingarlínur en ekki upprunalegu pöntunarlínunni. Hafi móttaka verið skráð í vöruhúsi, myndi það einnig hafa verið skráð á línur afhendingaráætlunar.  
7. Fella saman hlutann línur.
8. Smellt er á í lagi til að bóka móttöku.


