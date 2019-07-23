---
title: Nýjungar eða breytingar í Dynamics 365 for Talent (11. júní 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634481"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a>Nýjungar eða breytingar í Dynamics 365 for Talent (11. júní 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="search-engine-optimization-for-job-posts"></a>Leitarvélabestun fyrir vinnslubókanir

Þegar þú hefur kveikt á **Leitarvélarbestun** í Dynamics 365 for Talent : Attract Admin center, segir Attract forritunarviðmótið Google Indexing application (API) að skríða á vefsíðuna í hvert skipti sem þú virkjar og bókar nýja vinnslu eða uppfærir núverandi vinnslu. Þannig mun vinnslan birtast í leitarniðurstöðum fyrir Google og aðrar leitarvélar.

Sömuleiðis, þegar þú sendir frá sér vinnslu upplýsir Attract lyklunina API um það, svo að óbókuð vinnsla muni ekki birtast í leitarniðurstöðum.

> [!NOTE]
> Vefskriðlarar hafa ekki skilgreindan tímaramma fyrir skrið á vefsíður eða uppfærslu leitarniðurstaðna.

## <a name="coming-soon-in-attract"></a>Væntanlegt í Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Vinnslusamþykktir birtast á heimasíðunni

Samþykktir birtast í hlutanum **Samþykktir** í yfirlitinu. Samþykktaraðilar geta yfirfarið samþykktir sínar undir **Úthlutað á þig**, sem sýnir auðkenni vinnslu, titil vinnslu, aðra samþykktaraðila og dagsetningu þegar vinnslunni var úthlutað. Notendur sem senda inn vinnslu til samþykktar geta yfirfarið vinnslur sínar undir **Beiðni frá þér**, sem sýnir samþykktaraðilana sem eiga enn eftir að samþykkja innsenda vinnslu.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 for Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingunum sem er lýst í þessum hluta eiga við um smíðarnúmer 8.1.2337.

### <a name="platform-update-27"></a>Update 27 fyrir verkvang

Frekari upplýsingar um verkvangsuppfærslu 27 er að finna í [Forskoðun á eiginleikum í Dynamics 365 for Finance and Operations verkvangsuppfærslu 27 (júní 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Vinnusvæði eiginleikastjórnunar í Talent

Vinnusvæðið **Stjórnun eiginleika** í **Kerfisstjórnun** gerir þér kleift að skoða, virkja, slökkva á og skipuleggja aðgerðir sem hafa verið afhentir í hverri útgáfu. Sjálfgefið er að slökkt sé á nýjum eiginleikum. Hægt er að nota vinnusvæðið **Stjórnun eiginleika** til að kveikja á þeim og skoða fylgiskjölin fyrir þá.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Stuðningur Common Data Service-einingar fyrir sérstillt svæði

Útgáfustofnunin styður nú sérsniðna reitir.

### <a name="new-common-data-service-entities"></a>Ný Common Data Service eining

Einingunni Verkflokki hefur verið bætt við.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Forskoðun aðgerða verður aðeins virkjuð í umhverfi sandkassa

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

Þegar þú setur fram nýtt tilvik í Talent getur þú bent á hvort gerð tilviks er Framleiðsla eða Sandkassi. Tilvikagerðin Sandkassi gerir kleift að prófa nýja eiginleika snemma. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina **Framleiðsla**. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina **Sandkassi** skal hafa samband við [notendaþjónustu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) til að hefja breytingarbeiðni.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Takmarka leyfisgerðir í frítímabeiðnum

Fyrirtæki geta boðið starfsmönnum upp á margar leyfisgerðir. Hins vegar gæti það verið óviðeigandi fyrir starfsmenn að leggja fram beiðni um frest fyrir sumar gerðir leyfis. Þessum leyfisgerðum kann að vera stjórnað af mannauði (HR) í staðinn. Í þessari útgáfu er hægt að skilgreina hvaða leyfisgerðir starfsmenn geta sent inn fyrir frítímabeiðnir. 

## <a name="coming-soon-in-core-hr"></a>Kemur fljótlega í Core HR

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Skoðaðu framlengdar upplýsingar um skýrsluafköst í sjálfstætt sjálfsafgreiðslu stjórnanda

Ný valkostur mun gera stjórnendum kleift að skoða árangur af bæði beinum skýrslum sínum og framlengdum skýrslum sínum. Eins og er, geta línustjórnendur úthlutað og uppfært árangursmörk og gefið út nýjar umsagnir. Að auki geta beinar stjórnendur og starfsmenn þeirra viðhaldið og uppfært afkastabækur til að tryggja að ferli afkastarýni gangi vandræðalaust. Þegar þessi breyting er framkvæmd verða stjórnendur að geta skoðað og viðhaldið árangursskyldum upplýsingum um útbreiddar skýrslur auk þeirra beinna skýrslna.

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Starfsmenn, stjórnendur og HR munu geta prentað út afkastarýni starfsmanns.
