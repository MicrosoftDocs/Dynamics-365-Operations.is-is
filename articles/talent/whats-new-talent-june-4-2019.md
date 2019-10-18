---
title: Nýjungar eða breytingar í Dynamics 365 Talent (4. júní 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32b168eca210b1371db129c05f7035237eb35c38
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008985"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (4. júní 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Væntanlegt í Attract

### <a name="job-approvals-on-the-home-page"></a>Vinnslusamþykktir á heimasíðunni

Samþykktir birtast í hlutanum **Samþykktir** í yfirlitinu. Samþykktaraðilar geta skoðað samþykki sín undir **Úthlutað til þín**. Þessi hluti sýnir vinnslukenni, titil, aðra samþykktaraðila og daginn þegar vinnslunni var úthlutað. Notendur sem leggja fram starf til samþykktar geta skoðað störf sín undir **Umbeðið af notanda**. Þessi kafli sýnir samþykktaraðila sem eiga enn eftir að samþykkja innsenda vinnslu.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingunum sem er lýst í þessum hluta eiga við um smíðarnúmer 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ný síða til að villuleita gögn staðsetningarstigveldis

Mannauðsstjórar (HR) og stjórnendur geta nú staðfest stjórnunarstigveldið fyrir allar hringtilvísanir sem kunna að hafa verið óvart fluttar inn. Hægt er að komast á þessa nýju síðu á **Stjórnun fyrirtækis \> Tenglar \> Staðsetningar \> Villuleita stigveldi staðsetningar**.

### <a name="specify-reason-codes-on-leave-types"></a>Tilgreina ástæðukóða fyrir leyfisgerðir

Fyrirtæki gætu gert kröfu um frekari upplýsingar um frítímabeiðnir. Nú er hægt að tilgreina ástæðukóða fyrir leyfisgerðir og leyfa starfsmönnum að velja ástæðukóða fyrir frítímabeiðnir.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Fara fram á ástæðukóða fyrir tilteknar leyfisgerðir á frítímabeiðnum

Fyrirtæki gætu krafist ástæðukóða fyrir ákveðna leyfisgerðir þegar starfsfólk sendir inn frítímabeiðnir. Þessi krafa gæti verið til vegna stefnu fyrirtækis eða reglugerða. Hægt er að tilgreina hvers konar leyfisgerðir þurfa ástæðukóða og nú er hægt að krefja starfsfólk um að gefa upp ástæðukóða fyrir leyfisgerðina út af frítímabeiðni þeirra.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Bjóða upp á færslulista leyfa og fjarvista fyrir mannauðsstjóra

Möguleikinn til að fylgjast með frítíma starfsmanns og skilja hvernig frítími er reiknaður hjálpar ekki aðeins mannauðsstjóra við að svara spurningum starfsmanns heldur tryggir einnig nákvæma frítímainneign starfsmanna. Mannauðsstjóri er nú með nýja sýn á færslunum (styrkir, uppsafnanir, leiðréttingar og beiðnir), svo að starfsmenn mannauðs geta skoðað ástæðurnar á bak við frítímastöðu.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Ef þú eyðir skrá úr Talent fjarlægir það skrána ekki úr Common Data Service

Skrár sem eru fjarlægðar úr Talent: Core HR eru nú einnig fjarlægðar úr Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Ekki er verið að uppfylla áætlun um breytilega uppbót gildir frá/til dagsetninga

Í þessari útgáfu getur þú ekki skráð starfsmann í áætlun breytilegrar uppbótar ef upphafsdagurinn er á undan upphafsdegi áætlunarinnar eða lokadagsetning er eftir lokadagsetningu áætlunarinnar. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Athugasemdir um frammistöðurýni eru fjarlægðar þegar notendur velja Hætta við

Þessi útgáfa leiðréttir vandamál þar sem athugasemdir um rýni eru fjarlægðar ef notandi byrjar að breyta ummælum en velur síðan **Hætta við**. 

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forskoðunareiginleikar eru aðeins virkjaðir í tilvikum sandkassans

Þegar þú setur fram nýtt tilvik í Talent getur þú tiltekið hvort gerð tilviks er **Framleiðsla** eða **Sandkassi**. Tilvik af gerðinni **Sandkassi** gerir kleift að prófa nýja eiginleika snemma. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina **Framleiðsla**. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina **Sandkassi** skal hafa samband við [notendaþjónustu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) til að hefja breytingarbeiðni.

Nánari upplýsingar um hvernig breytingar eru gefnar út er að finna í [Úthluta Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Takmarka leyfisgerðir í frítímabeiðnum

Fyrirtæki geta boðið starfsmönnum upp á margar mismunandi leyfisgerðir. Hins vegar gæti það verið óviðeigandi fyrir starfsmenn að leggja fram beiðni um frest fyrir sumar gerðir leyfis. Þessum leyfisgerðum kann að vera stjórnað af mannauði (HR) í staðinn. Í þessari útgáfu er hægt að skilgreina hvaða leyfisgerðir starfsmenn geta sent inn fyrir frítímabeiðnir. 

## <a name="coming-soon-in-core-hr"></a>Kemur fljótlega í Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Skoðaðu framlengdar upplýsingar um afköst í sjálfsafgreiðslu stjórnanda

Ný valkostur mun gera stjórnendum kleift að skoða árangur af bæði beinum skýrslum sínum og framlengdum skýrslum sínum. Eins og er, geta línustjórnendur úthlutað og uppfært árangursmörk og gefið út nýjar umsagnir, sem starfsmenn þeirra stýra einnig. Að auki geta beinar stjórnendur og starfsmenn þeirra viðhaldið og uppfært afkastabækur til að tryggja að ferli afkastarýni gangi vandræðalaust. Þegar þessi breyting er framkvæmd verða stjórnendur að geta skoðað og viðhaldið árangursskyldum upplýsingum um útbreiddar skýrslur auk þeirra beinna skýrslna. 

### <a name="print-performance-reviews"></a>Prenta árangursumsagnir

Starfsmenn, stjórnendur og HR munu geta prentað út afkastarýni starfsmanns.
