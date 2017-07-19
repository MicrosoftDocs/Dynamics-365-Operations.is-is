---
title: "Setja upp fjárhagsáætlunargerðar stöðu"
description: "Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina stöðu fjárhagsáætlunargerðar. Það svarar algengum spurningum um hvernig á að búa til kostnaðarþætti fjárhagsáætlunar, launaflokka og launahintanet."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3fe1e1842b1cd808d35105ec7ec494107127690
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="position-budgeting-troubleshooting"></a>Setja upp fjárhagsáætlunargerðar stöðu

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina stöðu fjárhagsáætlunargerðar. Það svarar algengum spurningum um hvernig á að búa til kostnaðarþætti fjárhagsáætlunar, launaflokka og launahintanet. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Af hverju finnst ekki spástöðu síðan í mannauði?
---------------------------------------------------------------

Spástöður hafa verið fluttar í Fjárhagsáætlun.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Af hverju get ég ekki eytt kostnaðareiningum fjárhagsáætlunar?
Ekki er hægt að eyða kostnaðareiningum fjárhagsáætlunar sem er úthlutað á spástöðuna. Áður en hægt er að eyða kostnaðareiningu fjárhagsáætlunar þarf að fjarlægja hana úr öllum spástöðum. **Ábending:** Til að finna allar stöður sem kostnaðareiningu fjárhagsáætlunar er úthlutað til , veljið kostnaðareininguna á síðunni **Kostnaðareiningar Fjárhagsáætlunar** og smellið síðan á **Uppfæra stöður**. Stöður sem nota á kostnaðareiningum eru talin upp í efra hnitanetinu.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Er einhver leið til að fjarlægja kostnaðarþátt úr mörgum spárstöðum án þess að opna hvern og einn?
Ekki er hægt að fjarlægja kostnaðareiningu. Ef upphafs- og lokadagsetningum er breytt þannig að þær falli utan dagsetningar ferlis fjárhagsáætlunargerðar verður kostnaðareiningum ekki lengur úthlutað á spástöður í því ferli fjárhagsáætlunargerðar. Til að gera þessa breytingu skal opna kostnaðareiningu fjárhagsáætlunar, og síðan, á flýtiflipanum **Kostnaðarútreikningur** skal smellt á **Breyta dagsetningum**, og breyta upphafsdagsetningu eða lokadegi. Smellið á **Í lagi** til að uppfæra sjálfkrafa allar spástöður sem kostnaðareiningu er úthlutað. **Vísbending:** Ef þessi aðferð er notuð, skal hafa í huga að hún fjarlægir kostnaðareiningu fjárhagsáætlunar úr **öllum** spástöðum þar sem upphafs- og lokadagsetningarnar eru ekki lengur innan viðeigandi tímabils. Ef þetta er ekki það sem til stóð þarf að opna hverja spástöðu sem á að fjarlægja kostnaðareiningu fjárhagsáætlunar úr og gera breytingar handvirkt.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Af hverju get ég ekki slegið inn árlega upphæð í flýtiflipanum Útreikningur kostnaðar fyrir kostnaðareiningu fjárhagsáætlunar?
Ekki er hægt að slá inn árlega upphæð ef það eru kostnaðareiningar fjárhagsáætlunar á flýtiflipanum **Grundvöllur útreikninga** því kerfið krefst prósentuhlutfalls til að reikna út gildi. Til að breyta þessu gildi skal fjarlægja allar kostnaðareiningar fjárhagsáætlunar úr flýtiflipanum **Grundvöllur útreikninga**.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Af hverju get ég ekki breytt kostnaðargerð fjárhagsáætlunar úr tekjum í aðra kostnaðargerð fjárhagsáætlunar?
Sumar kostnaðargerðir fjárhagsáætlunar nota kostnaðarþáttinn tekjur sem reiknigrundvöll. Til að breyta svæðinu **Kostnaðargerð fjárhagsáætlunar** skal fjarlægja kostnaðareiningu tekna úr flýtiflipanum **Grundvöllur útreikninga** í öllum einingum fjárhagsáætlunar.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Af hverju get ég ekki breytt dagsetningu einingar kostnaðarlínu fjárhagsáætlunar fyrir kostnaðareiningu fjárhagsáætlunar?
Ekki er hægt að breyta dagsetningunni á línu kostnaðareiningar fjárhagsáætlunar þegar kostnaðareining fjárhagsáætlunar er notuð með spástöðu. Þessar takmarkanir eru til að tryggja að spástöður séu alltaf innan viðmiðunarreglna kostnaðareininga fjárhagsáætlunar. Til að breyta dagsetningunni, skal á flýtiflipanum **Kostnaðarútreikningur** smella á **Breyta dagsetningum**, og færið inn nýja dagsetningu. Smellið síðan á **Í lagi** til að uppfæra allar stöður sem kostnaðareiningunni er úthlutað sjálfkrafa.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Af hverju get ég ekki breytt kostnaði fyrir kostnaðareiningu fjárhagsáætlunar í skjámyndinni Launaflokkur?
Aðeins er hægt að stofna og breyta kostnaðareiningum fjárhagsáætlunar á síðunni **Kostnaðareiningar Fjárhagsáætlunar**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Af hverju koma villuboð þegar ég breyti dagsetningum kostnaðareiningar á spástöðu?
Dagsetningar á línu spástöðu kostnaðareiningarinnar verða að vera innan eftirfarandi afmarkana:

-   Virkjun og starfslok dagsetningarnar stöðunnar.
-   Virkjun og gildistíma dagsetningar kostnaðareining fjárhagsáætlunar.
-   Upphafs- og lokadagsetningu ferlis fjárhagsáætlunar sem er tengt fjárhagsáætlunargerð fyrir spástöðuna.





