---
title: Nýjungar eða breytingar í Dynamics 365 Talent (29. október 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529685"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (29. október 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2586. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Eyða aðilum án hlutverka ætti að vera sjálfgefið (371233)

Þegar þú útvegar nýtt umhverfi í Talent er sjálfgefið kveikt á **Eyða aðilum ef engin hlutverk eru til**. Þegar þú eyðir starfsmanni er aðilinn sem tengist starfsmanninum ekki fjarlægður nema að þessi stilling sé virk. Þessi breyting takmarkar afritaðar færslur í altækri aðsetursbók þegar þú þarft að flytja inn, breyta eða flytja starfsmenn aftur inn.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Heimilt skal vera að eyða drögum og niðurfelldum orlofsbeiðnum í Common Data Service (376999)

Með þessari breytingu geturðu nú eytt leyfisbeiðnum með stöðuna **Drög** eða **Hætt við** í Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Viðbótarlisti gilda í sérsniðnum reitum endurspeglast ekki í Common Data Service þegar smellt hefur verið á Sækja um í eyðublaðsreitnum Sérsnið (379599)

Þegar þú bætir nýjum listagildum við núverandi sérsniðinn reit sem þegar hefur verið samstilltur við Common Data Service eru þeir núna fáanlegir í Common Data Serivce eftir að þú hefur notað breytingarnar á gluggann **Sérsniðnir reitir**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Notaðu nýliðagátlista um borð í lögaðila þegar fleiri en eitt starf er fyrir hendi (371270)

Í útgáfu vikunnar geturðu sótt gátlista yfir starfsmenn sem eru með fleiri en eitt starf í **Skjámyndin Starfskraftur > Gátlistar**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Forskoðunareiginleikinn Opin innskráning bóta hefur verið fjarlægður

Í tengslum við tilkynningu okkar í bloggfærslunni [Strategískar fjárfestingar í kjarnastarfsemi HR keyra gæðarekstur](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) hefur Microsoft fjarlægt eiginleikann opin innskráning bóta úr forsýningu almennings. Ný virkni gefinn út í framtíðinni. Ekki er hægt að styðja framleiðslunotkun á eiginleikanum opin innskráning bóta.

## <a name="coming-soon"></a>Væntanlegt

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Sjá [Prenta árangursumsagnir](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) í Dynamics 365: 2019 útgáfu bylgjuáætlun 2.

### <a name="feature-management-workspace"></a>Vinnusvæði eiginleikastjórnunar

Eiginleikum er bætt við og þeir uppfærðir í hverri útgáfu. Upplifun eiginleikastjórnunar veitir vinnusvæði þar sem hægt er að skoða lista yfir eiginleika sem hafa verið gefnir út í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið til að kveikja á þeim og skoða fylgiskjölin fyrir þá.

Til að læra meira um breytingarnar sem fylgja eiginleikastjórnun, sjá [Eiginleikastjórnunaryfirlit](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
