---
title: 'Vísir: Búa til grunnlínuspá'
description: Skipuleggjandi framleiðslu getur stofna grunnlínuspá með því að nota annað hvort spálíkön tímaraðar eða með því að afrita söguleg eftirspurn.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 843e0b3827851e1251a2c77269859bb7903f69ec
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578321"
---
# <a name="guide-create-a-baseline-forecast"></a>Vísir: Búa til grunnlínuspá

[!include [banner](../../includes/banner.md)]

Skipuleggjandi framleiðslu getur stofna grunnlínuspá með því að nota annað hvort spálíkön tímaraðar eða með því að afrita söguleg eftirspurn. Þessi verklýsing sýnir hvernig á að stofna grunnlínuspá fyrir allar afurðir með því að nota eitt úthlutunarlykill vöru með því að afrita söguleg eftirspurn.

## <a name="set-up-an-item-allocation-key"></a>Uppsetning vöruúthlutunarlykils

1. Fara í **Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu**.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið *Heiti* með virði *10*.
    * Eftirspurnarspá keyrir milli lögaðila. Þess vegna þarf að setja upp öll fyrirtæki sem á að mynda spár fyrir í eina áætlunarhóp innan samstæðu.  
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Smellt er á **Úthlutunarlyklar vöru**.
    * Velja allar á úthlutunarlykla vöru sem á að stofna spá fyrir.  
5. Í listanum skal merkja valda línu.
    * Veljið D_Aloc úthlutunarlykil vöru.  
6. Velja skal **>**.
7. Lokið síðunni.
8. Lokið síðunni.

## <a name="set-up-the-demand-forecasting-parameters"></a>Setja upp færibreytur eftirspurnarspár

1. Fara í **Aðaláætlanagerð > Uppsetning > Eftirspurnarspá > Færibreytur eftirspurnarspár**.
2. Útvíkka hlutann **Færibreytur reiknirita fyrir spá**.
3. Í **stjórnunarstefnu Spármyndunar** svæðinu, veljið **Afrita yfir sögulega eftirspurn**.
4. Veldu **Vista**.

## <a name="create-a-baseline-forecast"></a>Búa til grunnlínuspá

1. Fara í **Aðaláætlanagerð > Spá > Eftirspurnarspá > Mynda tölfræðilega grunnlínuspá**.
2. Í reitnum **Frá dags.** færirði inn dagsetningu.
    * Ef þú ert með sölupantanir sem byrja frá 1. Janúar, 2015, færðu inn þessa dagsetningu. Ef ekki, skal færa inn fyrstu dagsetningu sölupantanirnar.  
3. Í reitnum **Til dags.** færirðu inn dagsetningu.
    * Færið inn síðustu dagsetningu sölupantana þinna, til dæmis *2015-03-31*.  
4. Í reitnum **Frá dags.** færirði inn dagsetningu.
    * Færðu inn *2015-04-01*. Þessi dagsetning verður reiknaður sjálfvirkt sem upphafsdagsetning fyrir næsta tímaramma eftirspurnarspár.  
5. Útvíkka **Færslur til að taka með** hlutann.
6. Velja **Síu**.
7. Í listanum skal merkja valda línu.
    * Merkið línuna þar sem **Svæði** = *Áætlunarhópur innan samstæðu*.  
8. Í reitnum **Skilyrði** skal slá inn gildi.
    * Færðu inn áætlunarhó innan samstæðu, t.d. *10*, sem notað er í fyrsta verkefninu.  
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið línuna þar sem **Svæði** = *Úthlutunarlykill vöru*.  
10. Í reitnum **Skilyrði** skal slá inn gildi.
11. Veljið **Í lagi**.
12. Útvíkka hlutann **Ítarlegar færibreytur**.
13. Í **Spárammi** reitnum veljið *Mánuður*.
14. Í **Spátími** reitinn, færið inn *3*.
15. Í svæði **Frysta tímamörk**, færið inn *1*.
16. Veljið **Í lagi**.

## <a name="visualize-the-demand-forecast"></a>Myndgera eftirspurnarspá

1. Fara í **Aðaláætlanagerð > Spá > Eftirspurnarspá > Leiðrétt eftirspurnarspá**.
2. Í töflunni samanlagt yfirlit skal velja hólfið í línu 1 og dálki 2. Þetta er annar mánuðinum sem búið er að stofna spá fyrir.
3. Stilla **QtyCell** á *400*.
    * Í reitnum, færa inn annað númer en það sem var spáð, til dæmis 400.  
4. handvirkar leiðréttingar voru gerðar á Spá. Athugið myndræna tilkynning í næsta þrepi.
5. Smellt er á **Upplýsingar spárlínu**.
    * Á þessari síðu er hægt að sjá nákvæmnisgildi, söguleg eftirspurn og spár. Hægt er að gera breytingar á spá einnig.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]