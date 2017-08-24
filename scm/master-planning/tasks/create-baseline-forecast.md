--- 
title: "Búa til grunnlínuspá"
description: "Skipuleggjandi framleiðslu getur stofna grunnlínuspá með því að nota annað hvort spálíkön tímaraðar eða með því að afrita söguleg eftirspurn."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c94a9766319531bd8285cca04003225709ce2113
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-baseline-forecast"></a>Búa til grunnlínuspá

[!include[task guide banner](../../includes/task-guide-banner.md)]

Skipuleggjandi framleiðslu getur stofna grunnlínuspá með því að nota annað hvort spálíkön tímaraðar eða með því að afrita söguleg eftirspurn. Þessi verklýsing sýnir hvernig á að stofna grunnlínuspá fyrir allar afurðir með því að nota eitt úthlutunarlykill vöru með því að afrita söguleg eftirspurn. 


## <a name="set-up-an-item-allocation-key"></a>Uppsetning vöruúthlutunarlykils
1. Fara í Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Heiti með virði '10'.
    * Eftirspurnarspá keyrir milli lögaðila. Þess vegna þarf að setja upp öll fyrirtæki sem á að mynda spár fyrir í eina áætlunarhóp innan samstæðu.  
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Smellt er á úthlutunarlykla vöru
    * Velja allar á úthlutunarlykla vöru sem á að stofna spá fyrir.  
5. Í listanum skal merkja valda línu.
    * Veljið D_Aloc úthlutunarlykil vöru.  
6. Smellt er á >.
7. Lokið síðunni.
8. Lokið síðunni.

## <a name="set-up-the-demand-forecasting-paramters"></a>Setja upp færibreytur eftirspurnarspár
1. Fara í Aðaláætlanagerð > Uppsetning > Eftirspurnarspá > Færibreytur eftirspurnarspár.
2. Útvíkka hlutann Færibreytur reiknirita fyrir spá.
3. Í stjórnunarstefnu Spármyndunar svæðinu, veljið 'Afrita yfir sögulega eftirspurn'.
4. Smellið á „Vista“.

## <a name="create-a-baseline-forecast"></a>Búa til grunnlínuspá
1. Fara í Aðaláætlanagerð > Spá > Eftirspurnarspá > Mynda tölfræðilega grunnlínuspá.
2. Dagsetning er rituð í reitinn Frá dags.
    * Ef þú ert með sölupantanir sem byrja frá 1. Janúar, 2015, færðu inn þessa dagsetningu. Ef ekki, skal færa inn fyrstu dagsetningu sölupantanirnar.  
3. Í reitinn Til dagsetningar skal slá inn dagsetningu.
    * Færið inn síðustu dagsetningu sölupantana þinna, til dæmis '2015-03-31'..  
4. Dagsetning er rituð í reitinn Frá dags.
    * Færðu inn '2015-04-01'. Þessi dagsetning verður reiknaður sjálfvirkt sem upphafsdagsetning fyrir næsta tímaramma eftirspurnarspár.  
5. Útvíkka Færslur til að taka hluta.
6. Smellt er á Síu.
7. Í listanum skal merkja valda línu.
    * Merkja línuna þar sem Svæðið = áætlunarhóp innan samstæðu.  
8. Í reitinn Skilyrði skal slá inn gildi.
    * Færðu inn áætlunarhó innan samstæðu, t.d. 10, sem notað er í fyrsta verkefninu.  
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið línuna þar sem Svæðið = úthlutunarlykil Vöru.  
10. Í reitinn Skilyrði skal slá inn gildi.
11. Smellið á „Í lagi“.
12. Útvíkka hlutann Ítarlegar færibreytur.
13. Veljið 'Mánuð' í svæði spárrammi.
14. Færa inn "3" í spátími svæði.
15. Í svæði Frysta tímamörk , færið inn '1'.
16. Smellið á „Í lagi“.

## <a name="visualize-the-demand-forecast"></a>Myndgera eftirspurnarspá
1. Fara í Aðaláætlanagerð > Spá > Eftirspurnarspá > Leiðrétt eftirspurnarspá.
2. Í töflunni samanlagt yfirlit skal velja hólfið í línu 1 og dálki 2. Þetta er annar mánuðinum sem búið er að stofna spá fyrir.
3. Stilla QtyCell á '400'.
    * Í reitnum, færa inn annað númer en það sem var spáð, til dæmis 400.  
4. handvirkar leiðréttingar voru gerðar á Spá. Athugið myndræna tilkynning í næsta þrepi.
5. Smellt er á Upplýsingar spárlínu
    * Á þessari síðu er hægt að sjá nákvæmnisgildi, söguleg eftirspurn og spár. Hægt er að gera breytingar á spá einnig.  


