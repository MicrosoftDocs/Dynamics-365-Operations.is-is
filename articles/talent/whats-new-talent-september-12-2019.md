---
title: Nýjungar eða breytingar í Dynamics 365 for Talent (10. september 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
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
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006242"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Nýjungar eða breytingar í Dynamics 365 for Talent (10. september 2019)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="candidate-e-mail-login"></a>Innskráning umsækjanda með tölvupósti

Umsækjendur geta nú notað hvaða tölvupóstfang sem er til að stofna reikning og skrá sig inn á starfsferilsíðu Talent til að sækja um störf og leita að stöðu umsóknar þeirra. Þetta er auk þess að þegar er hægt að skrá sig inn á Talent ferilsíðuna með því að nota félagslega reikninga sína eða persónuskilríki.

### <a name="job-activation-and-posting"></a>Virkjun og birtingu starfa

Við höfum gert nokkrar breytingar á virkjun og birtingu starfa. Þú verður að virkja störf áður en þú birtir þau á Talent ferilsíðunni eða á neinar utanaðkomandi atvinnustjórnir, þar með talið LinkedIn eða Broadbean.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2482. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Þú getur gert forskoðunareiginleika virkar í Sandbox og prufuumhverfi

Þegar þú setur fram nýtt tilvik í Talent getur þú tiltekið hvort gerð tilviks er Framleiðsla eða Sandkassi. Tilvik af gerðinni Sandkassi gerir kleift að prófa nýja eiginleika snemma. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina Sandkassi skal hafa samband við notendaþjónustu til að hefja breytingarbeiðni.

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](./provisioning-talent.md).

### <a name="platform-update-29"></a>Update 29 fyrir verkvang

Frekari upplýsingar um verkvangsuppfærslu 29 er að finna í [Forskoðun á eiginleikum í Dynamics 365 for Finance and Operations verkvangsuppfærslu 29 (október 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Nýr atvinnugreinareining í boði innan gagnaumsýslu (347202)

Með þessari útgáfu er ný Base Job eining tiltæk til að flytja inn / flytja út gögn. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Háþróaður öryggisstefna verkamanns sýnir rangt stöðu í stigveldi (354868)

Með þessari útgáfu birtast staðsetningar ekki lengur opnar hjá „auðum“ starfsmanni þegar notendur hafa takmarkaðan aðgang.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Loka reitinn á atvinnuformi lokar ekki formi við ákveðnar aðstæður (342467)

Þessi útgáfa felur í sér breytingu sem gerir Job formi kleift að loka í öllum atburðarásum.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Nýtt mál á starfsmannaskrá er læst vegna starfsmannastjórahlutverks (337111)

Með þessari breytingu er málstjórnunareyðublað ekki lengur læst þegar aðgangur er að því frá starfsmannaforminu.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Lokadagsetning atvinnu er alltaf vanskil 23:59:59 (351492)

Með þessari breytingu geturðu breytt ráðningardegi í annan tíma en 23:59:59 þegar þú slítur ráðningu handvirkt.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Ekki tókst að setja upp lokadagsetningu á launakóða með gagnastjórnun (336604)

Í þessari útgáfu geturðu sett upp launakóða sem renna út í gegnum eininguna **PayrollWorkerPositionEarningCodeEntity**.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Greiningarskýrsla starfsmannaþróunar sýnir ekki gögn (348737)

Í útgáfu vikunnar hefur verið greint frá færni starfsmanna til að veita nákvæma skýrslugerð.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Starfsskilmálar dagsetning/tími vantar ekki upphaf dagsins (349101)

Með þessari breytingu er upphafsdagsetning / tími nú sjálfgefinn byrjun dags og lokadagsetning / tími sjálfgefið til loka dags.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Breyting á lokadegi ráðningar á aðgerðarformi starfsmanns sýnir villu (354092) 

Þessi breyting leiðréttir mál þegar breyting á lokadegi ráðningar er hluti af aðgerðum starfsmanna.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Notkun gátlista um borð í fyrirtækjum (338433)

Þessi útgáfa veitir nú möguleika á að beita gátlistum fyrir starfsmenn sem eru starfandi hjá öðrum lögaðilum en undirritaður lögaðili.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="streamlined-employee-entry-and-navigation"></a>Einfaldaður innsláttur og skoðun starfsmanns

Þessi aðgerð er nú fáanleg í sandkassaumhverfi. Til að kveikja á þessum eiginleika skaltu fara á **Kerfisstjórnun > Tenglar > Uppsetning > Kerfisfæribreytur > Forskoðunaraðgerðir**. Veldu **Bætt skjámynd starfskrafta og yfirlit**. Þetta mun virkja þessar breytingar fyrir alla notendur. Þú getur slökkt á þessum möguleika hvenær sem er.

Sjá frekari upplýsingar í [Einfaldaður innsláttur og skoðun starfsmanns](./streamlined-employee-entry.md).
