---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (10. september 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304894"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (10. september 2018)

[!include [banner](includes/banner.md)]

**Smíði 8.1.138.0**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Leyfa beiðni um frí (hálfir dagar) á ákveðnum tíma dags

Ef leyfi og fjarvera er sett upp þannig að frítími sé sendur inn í dögum, geturðu nú einnig virkjað skilgreiningu á hálfum dag. Þá, þegar notendur leggja inn beiðni um frítíma, geta þeir tilgreint hvort þeir biðja um frí fyrri eða seinni hluta dags.

Sjálfgefið er að slökkt sé á þessum valkosti. Til að starfsmenn geti óskað eftir fríi fyrri eða seinni hluta dags verður þú að kveikja á þessum valkosti á **Leyfi og fjarvera** svæði fyrir færibreytur mannauðs.

Öryggisréttindi fyrir þennan eiginleika er Vinna með færibreytur fyrir mannauð.

## <a name="validation-of-leave-and-absence-entries"></a>Villuleit á færslum leyfis og fjarvista

Það fer eftir því hvernig leyfi er stillt, starfsmenn sem reyna að leggja fram beiðni um frítíma sem er lengri en vinnudagur þeirra fá viðvörunarboð. Með öðrum orðum, þeir eru varaðir við ef þeir reyna að taka meira en heilan dag í frí fyrir sérhvern dag.

Það er alltaf kveikt á þessari villuleit. Hvenær sem starfsmenn fara yfir dagsmörkin sem eru skilgreind, fá þeir viðvörun þegar þeir leggja fram beiðni um frí.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Viðbótarsvæði fyrir skilyrtar yfirlýsingar í verkflæði

Viðbótarsvæðum hefur verið bætt við skilyrtar yfirlýsingar og staðgengla fyrir nokkur verkflæði í Core HR.

Eftirfarandi svæðum hefur verið bætt við verkflæði launa, starfsloka og flutninga:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Staða
- Félag
- Deild
- PositionType
- CompLocation
- Starfsheiti
- Starf
- JobType
- JobFamily
- JobFunction

Eftirfarandi svæðum hefur verið bætt við verkflæðisstöðuna:

- Staða
- Félag
- Deild
- PositionType
- CompLocation
- Starfsheiti
- Starf
- JobType
- JobFamily
- JobFunction

Svæði í skilyrtum yfirlýsingum og staðgenglum eru tiltæk öllum notendum sem hafa aðgang til að stilla áðurnefnd verkflæði.

## <a name="navigation-to-attract-from-personnel-management"></a>Farið í Attract frá starfsmannastjórnun

Í starfsmannastjórnun, ef Attract hefur ekki verið sett upp, þá beinir kaflinn **Umsækjendur til að ráða** notendum að því að byrja með Attract í stað þess að sýna skilaboðin: „Við fundum ekkert til að sýna hér.“

## <a name="other-changes"></a>Aðrar breytingar

Þessi útgáfa inniheldur nokkrar villuleiðréttingar í viðbót:

- Þegar verktaki er ráðinn ætti flipinn **Laun** ekki að vera tiltækur á beiðni/aðgerðasíðunni.
- Á meðan uppsagnarbeiðni er í ferli er ekki hægt að halda áfram fyrr en allir áskildir reitir innihalda gögn.
- Tekið hefur verið á vandamálum vegna birtingar á röðun og dagsetningu í greiningu starfsmannastjórnunar.
