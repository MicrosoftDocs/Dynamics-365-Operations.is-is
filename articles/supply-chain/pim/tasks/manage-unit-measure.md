--- 
title: "Stjórna mælieiningu"
description: "Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar."
author: sorenva
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a>Stjórna mælieiningu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar. Hægt er að fara í gegnum þetta ferli með því að nota sýnigögn eða með því að nota eigin gögn.

1. Farðu í Viðhald útgefinnar afurðar.
2. Smellt er á Einingum.

## <a name="create-a-unit-of-measure"></a>Stofna mælieiningu
1. Smellið á „Nýtt“.
2. Í reitnum Eining skal slá inn gildi.
    * Færið inn Kenni eða tákn sem nota á þegar vísað er í mælieiningu.  
3. Sláið inn gildi í reitnum „Lýsing“.
    * Færið inn lýsandi heiti fyrir mælieiningu á tungumáli kerfisins.  
4. Í reitnum Einingaflokkur skal velja valkost.
    * Mælieiningaflokkurinn skilgreinir hvaða röklegu flokkun, eins og svæði, fjöldi eða magni, mælieiningin er hluti af.  
5. Í reitinn Nákvæmni aukastafa skal slá inn númer.
    * Tilgreina fjölda aukastafa sem verður að slétta umreiknaðar mælieiningu í þegar útreikningi er lokið fyrir mælieiningu.  
6. Smellið á „Vista“.

## <a name="define-unit-translations"></a>Skilgreina þýðingar eininga
1. Smellt er á einingatexti.
2. Smellið á „Nýtt“.
    * Einingatexti skal nota til að stofna þýðing fyrir Kenni eða tákn sem standa fyrir mælieiningu sem nota á á ytri skjöl í tungumálum fyrir viðskiptavin eða lánardrottin.  
3. Í reitnum Tungumál skal færa inn eða velja gildi.
4. Í reitinn Texti skal slá inn gildi.
5. Smellið á „Vista“.
6. Lokið síðunni.
7. Smellt er á Þýddar einingalýsingar.
8. Smellið á „Nýtt“.
    * Skilgreina lýsingar fyrir tiltekin tungumál fyrir mælieiningu.  
9. Í reitnum Tungumál skal færa inn eða velja gildi.
10. Sláið inn gildi í reitnum „Lýsing“.
11. Smellið á „Vista“.
12. Lokið síðunni.

## <a name="define-unit-conversion-rules"></a>Skilgreina umreikningsreglur eininga
1. Smellt er á Umreikningur eininga.
    * Skilgreina reglur til að umreikna mælieininguna í og frá öðrum mælieiningar í völdu einingaflokknum.  
2. Smellt er á Nýtt til að opna felligluggann.
3. Í reitnum Stuðull skal slá inn tölu.
    * Umreiknistuðull milli Frá einingu og Til einingar. til dæmis er umreiknistuðullinn úr sentímetrum í metra 100 þar sem 100 sentímetrar eru í einum metra.  
4. Í reitnum Til einingar skal færa inn eða velja gildi.
5. Í reitnum Sléttun skal velja valkost.
    * Skilgreina hvernig slétta skal umbreytt gildi.  
6. Smellið á „Í lagi“.
7. Lokið síðunni.


