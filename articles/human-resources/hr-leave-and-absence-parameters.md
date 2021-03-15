---
title: Grunnstilla færibreytur leyfis og fjarvista
description: Skilgreindu færibreytur Human Resources fyrir leyfi og fjarvistir í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997102"
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

>[!IMPORTANT]
>Skoðun leyfis og fjarvista milli fyrirtækja er gert í forskoðun eins og er. Þú þarft að virkja þetta í **sandkassaumhverfinu** til að birta valkostinn fyrir leyfi og fjarvistir. Frekari upplýsingar um virkjun forútgáfueiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Skoða og breyta samnýttum færibreytum fyrir mannauð

1. Á síðunni **Starfsmannastjórnun** skal velja flipann **Tenglar**.

2. Undir **Uppsetning**, veldu **Samnýttar færibreytur fyrir mannauð**.

3. Á flipanum **Ítarlegur aðgangur** skal velja **Já** til að **Virkja yfirlit á milli fyrirtækja** til að heimila skoðun leyfis í öllu fyrirtækinu.

4. Veljið **Vista**.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]