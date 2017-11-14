--- 
title: "Stofna afbrigðalíkan afurðar"
description: "Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 866a4f29723e10eb0a1e1be86d6d4f6da8a69b1c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-configuration-model"></a>Stofna afbrigðalíkan afurðar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-product-model"></a>Stofna framleiðslulíkan
1. Smellið á Skilgreining afurðarafbrigðislíkans
2. Smella á Afbrigðalíkan afurðar
3. Smellt er á Nýtt.
4. Í reitinn Heiti skal slá inn gildi.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Í reitnum Stefna leysis skal velja valkost.
    * Leysisstefnu ákvarðar hvernig skorður í afbrigðalíkani afurðar sem byggir á skorðum eru unnar. Þetta val getur haft áhrif á afköst afbrigðalíkan afurðar.  
7. Í reitinn Heiti skal slá inn gildi.
    * Rótaríhlutur stendur fyrir afbrigðalíkan afurðar, en einnig er hægt að nota það í öðrum vörulíkan.  
8. Smellið á „Í lagi“.
9. Veljið valkost í svæðinu skilgreiningar Endurnýtingu .
    * Ef færibreytan endurnýtingu skilgreiningar er stillt á Já, mun kerfið leita að eins skilgreiningar eftir hverja stillingarlotu og nota aftur ef nákvæm samsvörun finnst.  

## <a name="add-attributes"></a>Bæta við eigindum
1. Útvíkka hlutann eigindir.
2. Smelltu á Bæta við.
3. Í listanum skal merkja valda línu.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitinn Heiti leysis skal slá inn gildi.
    * Heiti Leysara er notaður af skorðu leysara afurðaafbrigðastillis. Hún má ekki innihalda bil eða sérstafir nema _ (undirstriki).  
6. Sláið inn gildi í reitnum „Lýsing“.
    * Texti lýsingar birtist notandanum skilgreiningu og þar af leiðandi getur þjónað sem hjálp í að velja rétt gildi eigindar.  
7. Færa inn eða veljið gildi í svæðinu gerð eigindar.
    * Gerð eigindar ákvarðar hvaða gildi eru tiltæk fyrir eigindina.  
8. Velja skal gátreit Taka í endurnýtingu .
    * Þessi valkostur er aðeins tiltækur þegar valkosturinn Endurnýtingu skilgreininga er valin. Að hafa eigind með í gátreit Endurnýta þýðir að þessi eigind verður athuguð þegar kerfið leitar að nákvæm samsvörun.  

## <a name="add-subcomponents"></a>Bæta við undiríhlutir
1. Stækkaðu hlutann undiríhlutir.
2. Smelltu á Bæta við.
3. Í listanum skal merkja valda línu.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitinn Heiti leysis skal slá inn gildi.
6. Sláið inn gildi í reitnum „Lýsing“.
7. Færa inn eða veljið gildi í svæðinu íhlutur.
    * Hver undirþáttagerð verður að vísa í íhlutarskilgreiningu. Þessi hönnun styður endurnýtanlegu íhluti og tryggir að þegar íhlutur hefur verið skilgreint er hægt að nota í mörg framleiðslulíkön.  
8. Smellið á „Vista“.
9. Smellt er á uppskriftarlínuupplýsingar.
    * Upplýsingar um uppskriftalínuskjámyndina gera notandanum kleift að velja viðeigandi eiginleika fyrir undiríhlutina. Hægt er að gefa hverjum eiginleika fast gildi eða varpa honum á eigind. Að varpa á eigind leiðir til að Uppskrift línueiginleika fær mismunandi gildi eftir því hvað var valið í skilgreiningarhlutanum.  
10. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Hver undirþáttagerð táknar skilgreinanleg afurðarsniðmát með skorðuskilgreiningartækni. Tilvísun er gerð með vörunúmeri.  
11. Veljið gátreitinn stilla.
12. Velja skal Já í Útreiknings reitnum.
    * Stilla valkost útreiknings tryggir að afurðin verða teknar með við útreikning kostnaðar fyrir afurðina.  
13. Smellið á flipann „Setja upp“.
14. Veljið gátreitinn stilla.
15. Færið inn númer í reitnum „Magn“.
    * Magn svæðið ákvarðar hversu mikið þessarar afurðar verður að nota í skilgreindu vörunni.  
16. Veljið gátreitinn stilla.
17. Í reitinn Á röð skal slá inn númer.
18. Smellið á „Í lagi“.


