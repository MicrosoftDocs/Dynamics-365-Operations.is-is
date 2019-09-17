---
title: Nýjungar eða breytingar í Dynamics 365 for Talent (25. júní 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3c7a13373193a6af4033b4609f0c338c2c6128c6
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856354"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-25-2019"></a>Nýjungar eða breytingar í Dynamics 365 for Talent (25. júní 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Væntanlegt í Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Vinnslusamþykktir birtast á heimasíðunni

Samþykktir birtast í hlutanum **Samþykktir** í yfirlitinu. Samþykktaraðilar geta yfirfarið samþykktir sínar undir **Úthlutað á þig**, sem sýnir auðkenni vinnslu, titil vinnslu, aðra samþykktaraðila og dagsetningu þegar vinnslunni var úthlutað. Notendur sem senda inn vinnslu til samþykktar geta yfirfarið vinnslur sínar undir **Beiðni frá þér**, sem sýnir samþykktaraðilana sem eiga enn eftir að samþykkja innsenda vinnslu.

## <a name="changes-in-onboard"></a>Breytingar í Onboard
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Rangt gildi birtist fyrir aðalstillingu (314266)

Þessar breytingar munu stöðugt sýna stillinguna **Aðalstaða** á öllum síðum.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Ekki hægt að breyta eftir að kallað er aftur á verkflæði í Umsögnum (318180)

Umsögnum sem hafa verið sendar í gegnum verkflæði má nú breyta.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Reiturinn Lokaathugasemdir í Umsögnum er ekki þýddur (325921)

Merkið **Lokaathugasemdir** verður þýtt í Talent.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Forskoðun aðgerða verður aðeins virkjuð í umhverfi sandkassa

Þegar þú setur fram nýtt tilvik í Talent getur þú bent á hvort gerð tilviks er **Framleiðsla** eða **Sandkassi**. Tilvikagerðin **Sandkassi** gerir kleift að prófa nýja eiginleika snemma. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina **Framleiðsla**. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina **Sandkassi** skal hafa samband við [notendaþjónustu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) til að hefja breytingarbeiðni.

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Takmarka leyfisgerðir í frítímabeiðnum

Fyrirtæki geta boðið starfsmönnum upp á margar leyfisgerðir. Hins vegar gæti það verið óviðeigandi fyrir starfsmenn að leggja fram beiðni um frest fyrir sumar gerðir leyfis. Þessum leyfisgerðum kann að vera stjórnað af mannauði (HR) í staðinn. Í þessari útgáfu er hægt að skilgreina hvaða leyfisgerðir starfsmenn geta sent inn fyrir frítímabeiðnir. 

## <a name="coming-soon-in-core-hr"></a>Kemur fljótlega í Core HR

### <a name="feature-management-area-in-talent"></a>Svæði eiginleikastjórnunar í Talent

**Eiginleikastjórnun** verður fjarlægð úr **Kerfisstjórnun** vegna vandamála með eiginleikanum. Við munum kynna aftur **Eiginleikastjórnun** í framtíðarútgáfu. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Stuðningur Common Data Service-einingar fyrir sérstillt svæði

Eftirfarandi einindi munu styðja sérsniðna reiti: **Tekjukóðar launa**, **Fast launatilvik**, **Launanet**, **Greiðslutímabil** og **Tilvísunarpunktur launa**. 

### <a name="new-common-data-service-entities"></a>Ný Common Data Service eining

Einindinu **Ástæðukóðar** verður bætt við Common Data Service.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Skoðaðu afkastaupplýsingar fyrir beinar og útbreiddum skýrslum í sjálfsafgreiðslu stjórnanda

Ný valkostur mun gera stjórnendum kleift að skoða árangur af bæði beinum skýrslum sínum og framlengdum skýrslum sínum. Eins og er, geta línustjórnendur úthlutað og uppfært árangursmörk og gefið út nýjar umsagnir. Að auki geta beinar stjórnendur og starfsmenn þeirra viðhaldið og uppfært afkastabækur til að tryggja að ferli afkastarýni gangi vandræðalaust. Þegar þessi breyting er framkvæmd verða stjórnendur að geta skoðað og viðhaldið árangursskyldum upplýsingum um útbreiddar skýrslur auk þeirra beinna skýrslna.

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Starfsmenn, stjórnendur og HR munu geta prentað út afkastarýni starfsmanns.