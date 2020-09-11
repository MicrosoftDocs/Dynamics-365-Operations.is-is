---
title: Grunnstilla færibreytur leyfis og fjarvista
description: Skilgreindu færibreytur Human Resources fyrir leyfi og fjarvistir í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712377"
---
# <a name="configure-leave-and-absence-parameters"></a>Grunnstilla færibreytur leyfis og fjarvista

Áður en þú setur upp áætlanir um leyfi og fjarvistir í Dynamics 365 Human Resources, það er góð hugmynd að staðfesta stillingar fyrir allar skyldar færibreytur Human Resources, þar á meðal:

- Númeraröð fyrir leyfisbeiðnir
- Stillingar á Family and Medical Leave Act (lög um leyfi vegna fjölskyldu eða veikinda)
- Stillingar fyrir sjálfsafgreiðslu starfsmanna vegna orlofs- og fjarverubeiðna
- Færibreytur leyfis og fjarvista

## <a name="view-and-change-human-resources-parameters"></a>Skoða og breyta færibreytum Human Resources

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Skipulag**, veldu **Færirbreytur Human Resources**.

3. Á **Númeraraðir** flipann, staðfestu **Númeraröð kóða** fyrir **Skildu eftir skilríki** og breyta eftir þörfum. Þessi stilling ákvarðar röðina sem notuð er til að úthluta sjálfkrafa skilríkjum til að skilja eftir beiðnir.

4. Á **FMLA** flipanum, staðfestu FMLA stillingarnar og breyttu eftir þörfum.

5. Á **Sjálfsafgreiðsla starfsmanna** flipann, tilgreinir hvort stjórnendur geti slegið inn leyfi og fjarvistarbeiðnir fyrir hönd starfsmanna sinna.

7. Veljið **Vista**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Skoða og breyta færibreytum leyfis og fjarvista

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Uppsetning** velurðu **Færibreytur leyfis og fjarvista**.

3. Á flipanum **Almennt** skal stilla eftirfarandi færibreytur:
 
    - Stilltu **Eining fyrir leyfi og fjarvistir** á annaðhvort klukkutíma eða daga. Ef dagar, getur þú valið **Virkja skilgreining á hálfum degi** til að gera starfsmönnum kleift að velja annaðhvort fyrri eða seinni hluta dags í beiðnum sínum um frí. 

    - Veldu **Mánuðir gildistíma þjónustu** til að stilla hvenær uppsöfnunarhlutfallið tekur gildi vegna leyfisáætlana sem nota mánaðalega þjónustu.

    - Veljið **Útreikningur á stöðu** til að birta stöður frá og með deginum í dag eða á uppsöfnunartímabilinu. Ef þú velur **Staðan frá deginum í dag** sýnir staðan samtölu allra uppsafnana, leiðréttinga og beiðna frá og með deginum í dag. Ef þú velur **Staða frá og með uppsöfnunartímabili** sýnir staðan samtölu allra uppsafnana, leiðréttinga og beiðna frá og með uppsöfnunartímabilinu sem skilgreint er af tíðni í leyfisáætluninni. 

    - Stillið upphafstímann á runuvinnslu gildistíma yfirfærslu.  
    
    - Veljið **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga** og **Leyfa starfsmönnum að selja leyfisdaga**. Ef valið er **Já** fyrir þessa valmöguleika er hægt að búa til reglur um kaup og sölu á leyfisdögum og gera starfsmönnum kleift að senda inn beiðnir um kaup og sölu á leyfisdögum.

## <a name="configure-calendar-parameters"></a>Skilgreina færibreytur dagatals

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Uppsetning** velurðu **Færibreytur leyfis og fjarvista**.

3. Á **Dagatal** flipanum, skal breyta stillingu dagatals eftir þörfum.

4. Veljið **Vista**.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
