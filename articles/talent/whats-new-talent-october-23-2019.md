---
title: Nýjungar eða breytingar í Dynamics 365 Talent (23. október 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 66419d9093cff68aa6109b22ab57bcb46ac6c718
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772897"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (23. október 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2569. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Verkvangsuppfærsla 30 fyrir forrit Finance and Operations

Sjá frekari upplýsingar [Hvað er nýtt eða breytt í uppfærslu pallsins 30 fyrir forrit Finance and Operations (nóvember 2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Fjarlægja ávinning opinn forskoðunareiginleika skráningar

Í tengslum við tilkynningu okkar í bloggfærslunni [Strategískar fjárfestingar í kjarnastarfsemi HR keyra gæðarekstur](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence), Microsoft er að fjarlægja ávinninginn fyrir opnun skráningar úr forsýningu almennings 18. október 2019. Í staðinn verður nýr virkni gefinn út í framtíðinni. Framleiðslunotkun kostanna opnar skráningaraðgerð sem nú er í forskoðun almennings verður ekki studd.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Villa við val á landi/svæði á verkamannaforminu í annað sinn (350294)

Með útgáfu vikunnar hefur málið verið leiðrétt við val á landi/svæði í skjámyndinni **starfskraftur**.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Gildi fjárhagsvíddar eru sjálfgefin í reitnum Samsetning þegar ekki leyfa handvirka færslu er stillt á satt (340097)

Þegar þessi breyting er sett upp, þegar fjárhagsvíddir eru settar upp og valmöguleikinn notaður til að leyfa ekki handvirka færslu, mun kerfið sjálfgilda víddargildið á réttan hátt inn í reitinn **Samsetningarskjár**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Bæta ætti við nýjum samskiptategundum við leit að samskiptum á formi persónulegra tengiliða (347691)

Þessi útgáfa inniheldur nýja möguleika til að bæta við nýjum samskiptategundum í töflunni **Venslategundir** og endurspegla þær breytingar á sambandi leit að persónulegum tengiliðum.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Viðbótarlista gildi í sérsniðnum reitum endurspeglast ekki í Common Data Service (379599)

Með útgáfu vikunnar bætist nýju listagildi við núverandi sérsniðinn reit sem þegar er samstilltur við Common Data Service, nýju gildi listans munu nú birtast eftir að breytingum hefur verið beitt á eininguna.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Á Starfsskilmálasíðunni birtast öll ráðningarkjör starfsmanna eftir að hafa valið Opna í Excel (348073)

Með þessari útgáfu opnast aðeins ráðningarkjör starfsmanna sem valin eru í Excel. Öllu öryggi fyrirtækisins er einnig haldið.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Það vantar tengsl milli frídagseiningar Vinnudagatals og Vinnudagatalseiningar í Common Data Service (324178)

Þessu sambandi hefur verið bætt við útgáfuna. Þessi breyting gerir vinnudegi starfsmanns kleift að birtast í PowerApps. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Villa við að nota sjálfsþjónustuverkflæði starfsmanna með stillanlegum stigveldum (370132)

Í þessari útgáfu er betri skilaboð fáanleg um hvernig á að stilla verkflæði með stillanlegum stigveldum. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Kerfið gerir kleift að búa til nýjar stöður þar sem dagsetningin sem er fáanleg fyrir framsal er fyrr en virkjunardagurinn (340103)

Þessi breyting mun sýna viðvörun þegar dagsetningin **Laus til verkefna** er fyrir dagsetningu **Virkjunar** á stöðunni.

## <a name="coming-soon"></a>Væntanlegt

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.

### <a name="feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu. Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá.

Til að læra meira um breytingarnar sem fylgja eiginleikastjórnun, sjá [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
