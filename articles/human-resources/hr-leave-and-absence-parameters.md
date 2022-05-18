---
title: Grunnstilla færibreytur leyfis og fjarvista
description: Þetta efnisatriði lýsir því hvernig á að skilgreina mannauðsfæribreytur fyrir orlof og fjarveru í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79052c550783dee1ba4091ad10bde4d79d7b905e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690695"
---
# <a name="configure-leave-and-absence-parameters"></a>Grunnstilla færibreytur leyfis og fjarvista

>[!Important]
>Virknin sem vísað er til í þessu efnisatriði er nú í boði fyrir viðskiptavini sem nota stakt Dynamics 365 Human Resources. Sum eða öll virknin verður í boði sem hluti af síðari útgáfu í tölvukerfi Finance eftir útgáfu 10.0.26 af Finance.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Áður en þú setur upp orlofs- og fjarvistaáætlanir inn Dynamics 365 Human Resources, það er góð hugmynd að staðfesta stillingar fyrir allar tengdar **Stærðir mannauðs**, þar á meðal:

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

    - Stilltu **Byrjunartími** fyrir **Flytja gildistíma** lotuvinna.  
    
    - Veljið **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga** og **Leyfa starfsmönnum að selja leyfisdaga**. Ef valið er **Já** fyrir þessa valmöguleika er hægt að búa til reglur um kaup og sölu á leyfisdögum og gera starfsmönnum kleift að senda inn beiðnir um kaup og sölu á leyfisdögum.

## <a name="configure-calendar-parameters"></a>Skilgreina færibreytur dagatals

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Uppsetning** velurðu **Færibreytur leyfis og fjarvista**.

3. Á **Dagatal** flipanum, skal breyta stillingu dagatals eftir þörfum.

4. Veljið **Vista**.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
