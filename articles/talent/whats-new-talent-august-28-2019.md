---
title: Nýjungar eða breytingar í Dynamics 365 for Talent (27. ágúst 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529805"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Nýjungar eða breytingar í Dynamics 365 for Talent (27. ágúst 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2447. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forskoðunareiginleikar eru aðeins virkjaðir í tilvikum sandkassans

Þegar þú setur fram nýtt tilvik í Talent getur þú tiltekið hvort gerð tilviks er Framleiðsla eða Sandkassi. Tilvik af gerðinni Sandkassi gerir kleift að prófa nýja eiginleika snemma. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina Framleiðsla. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina Sandkassi skal hafa samband við notendaþjónustu til að hefja breytingarbeiðni.

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Skoðaðu framlengdar upplýsingar um afköst í sjálfsafgreiðslu stjórnanda

Ný valkostur mun gera stjórnendum kleift að skoða árangur af bæði beinum skýrslum sínum og framlengdum skýrslum sínum. Eins og er, geta línustjórnendur úthlutað og uppfært árangursmörk og gefið út nýjar umsagnir. Að auki geta beinar stjórnendur og starfsmenn þeirra viðhaldið og uppfært afkastabækur til að tryggja að ferli afkastarýni gangi vandræðalaust. Þegar þessi breyting er framkvæmd verða stjórnendur að geta skoðað og viðhaldið árangursskyldum upplýsingum um útbreiddar skýrslur auk þeirra beinna skýrslna.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Ekki er leyfilegt að eyða lögaðilum ef starfsmenn eru til innan fyrirtækisins (339849)

Með þessari breytingu geturðu ekki fjarlægt eða eytt fyrirtækjum ef starfsmenn og önnur skyld gögn eru til fyrir lögaðilinn.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Greining á viðskiptagreind launastjórnunar samræmist ekki á vinnusvæði bóta (322493)

Í þessari útgáfu hefur greiningum á bótum verið breytt til að endurspegla nákvæmlega áætlanir sem starfsmönnum er úthlutað.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Verkflæðisstaðgengillinn % fyrirtæki% birtir DAT við ráðningar á starfsmönnum í gegnum verkflæði (343905)

Með þessari útgáfu sýnir fyrirtækjastaðgengillinn lögaðilann sem er tengdur ráðningu nýja starfsmannsins.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>Einingin CDSJobPosition birtir villu þegar gildir til dags. er stillt (349387)

Í þessari útgáfu leyfa gagnaveiturnar **Upplýsingar um stöðu** og **Tímalengd stöðu** í einingunni **CDSJobPosition** breytingar úr Common Data Service í reitina **Dagsetningarháð**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Fyrir starfslok starfsmanna er síðasti dagurinn sem unnið var fylltur út á lokadagsetningu verkefnis (332496)

Þessi breyting stillir núna stöðuna **Lokadagsetning verkefnis** sjálfvirkt á **Dagsetning starfsloka**. Þú getur breytt þessum sjálfgildum þegar þú slærð inn gögn.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Lögaðilar takmarkast ekki við leigu (338871)
 
Þessi breyting takmarkar ráðningarferlið til að sýna aðeins þá lögaðila sem notandinn hefur aðgang að.  

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="streamlined-employee-entry-and-navigation"></a>Einfaldaður innsláttur og skoðun starfsmanns

Þessi aðgerð er nú fáanleg í sandkassa- og prófunarumhverfi. Til að kveikja á þessum eiginleika skaltu fara á **Kerfisstjórnun > Tenglar > Uppsetning > Kerfisfæribreytur > Forskoðunaraðgerðir**. Veldu **Bætt skjámynd starfskrafta og yfirlit**. Þetta virkjar þessar breytingar fyrir alla notendur. Þú getur slökkt á þessum möguleika hvenær sem er.

Sjá frekari upplýsingar í [Einfaldaður innsláttur og skoðun starfsmanns](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Væntanlegt

### <a name="platform-update-29"></a>Update 29 fyrir verkvang

Frekari upplýsingar um verkvangsuppfærslu 29 er að finna í [Forskoðun á eiginleikum í Dynamics 365 for Finance and Operations verkvangsuppfærslu 29 (október 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
