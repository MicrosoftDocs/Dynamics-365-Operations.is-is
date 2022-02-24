---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (13. maí 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 11c9f03f4b3915d81b624115a1d97a0c7bc31709
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529733"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (13. maí 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="coming-soon-in-attract"></a>Væntanlegt í Attract

### <a name="job-approvals-on-home-page"></a>Samþykktir starfs á heimasíðunni

Samþykktir birtast í hlutanum **Samþykktir** í yfirlitinu. Samþykktaraðilar geta yfirfarið samþykktir sínar undir **Úthlutað á þig**, sem sýnir auðkenni starfs, titil, aðra samþykktaraðila og dagsetningu úthlutunar. Notendur sem senda inn starf til samþykktar geta yfirfarið störfin sín undir **Beiðni frá þér**, sem sýnir samþykktaraðilana sem verða enn að samþykkja innsent starf.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2297. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Tilgreina gerð tilviks við úthlutun Talent

Við úthlutun á nýju tilviki af Talent er hægt að gefa upp hvort gerð tilviks er **Framleiðsla** eða **Sandkassi**, sem opnar fyrir snemmbærar prófanir á nýjum eiginleikum. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina **Framleiðsla**. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina **Sandkassi** skal hafa samband við [notendaþjónustu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) til að koma breytingarbeiðninni áfram.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Stuðningur Common Data Service-einingar fyrir sérstillt svæði

Í útgáfu þessarar viku styðja eftirfarandi Common Data Service-einingar nú sérstillt svæði: Ráðning, tíðni á útreikningi fríðinda, útreikningur á hlutfalli fríðinda, frídagar vinnudagatals og gerð auðkennis.

### <a name="common-data-service-integration-page"></a>Samþættingarsíða Common Data Service

Þessi útgáfa veitir nýjan valkost í **Kerfisstjórnun > Tenglar > Samþættingar > Common Data Service skilgreining**. Valkosturinn **Common Data Service skilgreining** veitir stjórnanda eða yfirmanni gagnastjórnunar smá sveigjanleika og innsýn með Common Data Service. Með þessum valkosti er hægt að kveikja eða slökkva á Common Data Service-samþættingunni með Talent-tilviki og skoða upplýsingar um samstillingu milli Talent-tilviks og Common Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Flytja inn frammistöðugögn með lokamati starfsmanns (316710)

Í þessari útgáfu er hægt að flytja inn eldri gögn starfsmannamats. Reiturinn **FinalEmployeeRatingId** er nú með skrifaðgang.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Get ekki búið til aðsetur starfskrafts í Common Data Service og samstillt það við Talent (317555)

Þessi breyting gerir gögnum aðseturs sem búin eru til í Common Data Service að samstillast við Talent.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ný síða til að villuleita gögn staðsetningarstigveldis

Mannauðsstjórar og stjórnendur geta nú villuleitað stjórnunarstigveldið fyrir allar hringtilvísanir sem kunna að hafa verið óvart fluttar inn. Hægt er að komast á þessa síðu frá **Stjórnun fyrirtækis > Tenglar > Staðsetningar > Villuleita stigveldi staðsetningar**.

### <a name="specify-reason-codes-on-leave-types"></a>Tilgreina ástæðukóða fyrir leyfisgerðir

Fyrirtæki gætu gert kröfu um frekari upplýsingar um frítímabeiðnir. Nú er hægt að tilgreina ástæðukóða fyrir leyfisgerðir og leyfa starfsmönnum að velja ástæðukóða fyrir frítímabeiðnir.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Fara fram á ástæðukóða fyrir tilteknar leyfisgerðir á frítímabeiðnum

Fyrirtæki gætu krafist ástæðukóða fyrir ákveðna leyfisgerðir þegar starfsfólk sendir inn frítímabeiðnir. Þessi krafa gæti verið til vegna stefnu fyrirtækis eða reglugerða. Hægt er að tilgreina hvers konar leyfisgerðir þurfa ástæðukóða og nú er hægt að krefja starfsfólk um að gefa upp ástæðukóða fyrir leyfisgerðina út af frítímabeiðni þeirra.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Bjóða upp á færslulista leyfa og fjarvista fyrir mannauðsstjóra

Möguleikinn til að fylgjast með frítíma starfsmanns og skilja hvernig frítími er reiknaður hjálpar ekki aðeins mannauðsstjóra við að svara spurningum starfsmanns heldur tryggir einnig nákvæma frítímainneign starfsmanna. Mannauðsstjóri er nú með nýja sýn á færslunum (styrkir, uppsafnanir, leiðréttingar og beiðnir), svo að starfsmenn mannauðs geta skoðað ástæðurnar á bak við frítímastöðu.
