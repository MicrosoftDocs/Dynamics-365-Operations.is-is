---
title: Stjórna mælieiningu
description: Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8d9b6f18fdc1c47d6a695ca6a2330f6f02fc1bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430189"
---
# <a name="manage-unit-of-measure"></a>Stjórna mælieiningu

[!include [banner](../../includes/banner.md)]

Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar. Hægt er að fara í gegnum þetta ferli með því að nota sýnigögn eða með því að nota eigin gögn.

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Viðhald útgefinna afurða**.
2. Smelltu á **Einingar**.

## <a name="create-a-unit-of-measure"></a>Stofna mælieiningu
1. Smellt er á **Nýtt**.
2. Í reitnum **Eining** skal slá inn gildi. Færið inn Kenni eða tákn sem nota á þegar vísað er í mælieiningu.  
3. Í reitinn **Lýsing** skal slá inn gildi. Færið inn lýsandi heiti fyrir mælieiningu á tungumáli kerfisins.  
4. Í reitnum **Einingaflokkur** skal velja valkost. Mælieiningaflokkurinn skilgreinir hvaða röklegu flokkun, eins og svæði, fjöldi eða magni, mælieiningin er hluti af.  
5. Í reitinn **Nákvæmni aukastafa** skal slá inn tölu. Tilgreina fjölda aukastafa sem verður að slétta umreiknaðar mælieiningu í þegar útreikningi er lokið fyrir mælieiningu.  
6. Smellt er á **Vista**.

## <a name="define-unit-translations"></a>Skilgreina þýðingar eininga
1. Á **Aðgerðasvæði** er smellt á **Einingatexti**.
2. Smellt er á **Nýtt**. Einingatexti skal nota til að stofna þýðing fyrir Kenni eða tákn sem standa fyrir mælieiningu sem nota á á ytri skjöl í tungumálum fyrir viðskiptavin eða lánardrottin.  
3. Í reitnum **Tungumál** skal færa inn eða velja gildi.
4. Í reitnum **Texti** skal slá inn gildi.
5. Smellt er á **Vista**.
6. Lokið síðunni.
7. Í **aðgerðasvæðinu** er smellt á **Þýddar lýsingar á einingum**.
8. Smellt er á **Nýtt**. Skilgreina lýsingar fyrir tiltekin tungumál fyrir mælieiningu.  
9. Í reitnum **Tungumál** skal færa inn eða velja gildi.
10. Í reitinn **Lýsing** skal slá inn gildi.
11. Smellt er á **Vista**.
12. Lokið síðunni.

## <a name="define-unit-conversion-rules"></a>Skilgreina umreikningsreglur eininga
1. Á **Aðgerðasvæðinu** er smellt á **Umreikningur eininga**. Skilgreina reglur til að umreikna mælieininguna í og frá öðrum mælieiningar í völdu einingaflokknum.  
2. Smelltu á **Nýtt** til að opna felligluggann.
3. Í reitnum **Stuðull** skal slá inn tölu. Umreiknistuðull milli Frá einingu og Til einingar. til dæmis er umreiknistuðullinn úr sentímetrum í metra 100 þar sem 100 sentímetrar eru í einum metra.  
4. Í reitnum **Til einingar** skal færa inn eða velja gildi.
5. Í reitnum **Sléttun** skal velja valkost. Skilgreina hvernig slétta skal umbreytt gildi.  
6. Smellt er á **OK**.
7. Lokið síðunni.

