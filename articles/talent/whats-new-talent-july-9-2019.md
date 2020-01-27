---
title: Nýjungar eða breytingar í Dynamics 365 Talent (9. júlí 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 99a7e6130d45229011a185087d4872fe34b8224a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897627"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (9. júlí 2019)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Væntanlegt í Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>Vinnslusamþykktir birtast á heimasíðunni

Samþykktir birtast í hlutanum **Samþykktir** í yfirlitinu. Samþykktaraðilar geta yfirfarið samþykktir sínar undir **Úthlutað á þig**, sem sýnir auðkenni vinnslu, titil vinnslu, aðra samþykktaraðila og dagsetningu þegar vinnslunni var úthlutað. Notendur sem senda inn vinnslu til samþykktar geta yfirfarið vinnslur sínar undir **Beiðni frá þér**, sem sýnir samþykktaraðilana sem eiga enn eftir að samþykkja innsenda vinnslu.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Verkvangsuppfærsla 28 fyrir Finance and Operations

Frekari upplýsingar um verkvangsuppfærslu 28 fyrir Finance and Operations er að finna í [Forskoðun á eiginleikum í Dynamics 365 Finance and Operations verkvangsuppfærslu 28 í (júlí 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Stuðningur við einingar fyrir sérsniðna reiti í Common Data Service 

Eftirfarandi einingar styðja núna sérsniðna reiti: 

- **Fyrirkomulag fastra launa**
- **Uppsetning á tilvísunarpunkti launa**
- **Setja upp línu tilvísunarpunkts launa**
- **Tekjukóði launa**
- **Launatímabil**
- **Fast launatilvik**
- **Launanet**

Til að skoða allar uppfærðar einingar í Talent:

1. Veldu **Kerfisstjórnun**, veldu **Tenglar** og veldu síðan **Skilgreining á Common Data Service**.
2. Veldu fellivalmyndina **Heiti CDS einingar**. Allar skráðar einingar eru í nýjustu útgáfunni. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Fullu nafni bætt við einiguna Starfskraftur í Common Data Service

Reitnum **Fullt nafn** hefur verið bætt við eininguna **Starfskraftur**.

### <a name="full-time-equivalent-higher-than-10"></a>Jafngildi fulls starfs hærri en 1,0

Viðvörun birtist nú ef gildi hærra en 1,0 er slegið inn fyrir starfsmann í fullu starfi í stöðu. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Viðvörun birtist ekki lengur á síðunni Starfskraftur þegar það er engin framtíðardagsett atvinna

Þú munt ekki lengur fá skilaboð sem segja til um að framtíðarstörf séu til þegar þú ferð á síðuna **Starfskraftur** úr listanum **Starfsmenn sem hætta** á vinnusvæðinu **Starfsmannastjórnun**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Ekki tókst að eyða viðskiptaferli í Talent

Núna er hægt að eyða viðskiptaferlum í vinnusvæðinu **Viðskiptaferli**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Leyfisstaða sýnir ekki lengur núll fyrir áætlanir án uppsafnana þegar Staða er notuð á uppsöfnunartímabilinu

Áætlanir sem eru settar upp án uppsafnana geta nú sýnt stöðu.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forskoðunareiginleikar eru aðeins virkjaðir í tilvikum sandkassans

Þegar þú setur fram nýtt tilvik í Talent getur þú tiltekið hvort gerð tilviks er **Framleiðsla** eða **Sandkassi**. Tilvik af gerðinni **Sandkassi** gerir kleift að prófa nýja eiginleika snemma. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina **Framleiðsla**. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina **Sandkassi** skal hafa samband við [notendaþjónustu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) til að hefja breytingarbeiðni.

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Takmarka leyfisgerðir í frítímabeiðnum

Fyrirtæki geta boðið starfsmönnum upp á margar mismunandi leyfisgerðir. Hins vegar gæti það verið óviðeigandi fyrir starfsmenn að leggja fram beiðni um frest fyrir sumar gerðir leyfis. Þessum leyfisgerðum kann að vera stjórnað af mannauði (HR) í staðinn. Í þessari útgáfu er hægt að skilgreina hvaða leyfisgerðir starfsmenn geta sent inn fyrir frítímabeiðnir. 

## <a name="coming-soon-in-core-hr"></a>Kemur fljótlega í Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Skoðaðu framlengdar upplýsingar um afköst í sjálfsafgreiðslu stjórnanda

Ný valkostur mun gera stjórnendum kleift að skoða árangur af bæði beinum skýrslum sínum og framlengdum skýrslum sínum. Eins og er, geta línustjórnendur úthlutað og uppfært árangursmörk og gefið út nýjar umsagnir, sem starfsmenn þeirra stýra einnig. Að auki geta beinar stjórnendur og starfsmenn þeirra viðhaldið og uppfært afkastabækur til að tryggja að ferli afkastarýni gangi vandræðalaust. Þegar þessi breyting er framkvæmd verða stjórnendur að geta skoðað og viðhaldið árangursskyldum upplýsingum um útbreiddar skýrslur auk þeirra beinna skýrslna. 

### <a name="entities-supporting-custom-fields"></a>Einingar sem styðja sérsniðna reiti

Eftirfarandi einingar verða virkjaðar fyrir sérsniðna reiti í Common Data Service: 

- **Gerð leyfis**
- **Bankareikningur starfskrafts**
- **Vinnudagatal**
