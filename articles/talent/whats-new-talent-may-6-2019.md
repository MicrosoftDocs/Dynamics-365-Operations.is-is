---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (6. maí 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c04af27bcc446b516f14125e71fb707bfd1d7708
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529709"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (6. maí 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Velja valfrjáls skjöl við stofnun tilboðs

Þegar valið er sniðmát fyrir tilboðspakka, biður Attract nú um valin séu viðeigandi, valfrjáls skjöl úr þessum sniðmátspakka. Hægt er að bæta við öðrum valfrjálsum skjölum á meðan tilboðið er undirbúið.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2282. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>Uppfærsla 26 fyrir verkvang fyrir Finance and Operations

Frekari upplýsingar um verkvangsuppfærslu 26 fyrir Finance and Operations er að finna í [Forskoðun á eiginleikum í Dynamics 365 Finance and Operations verkvangsuppfærslu 26 (maí 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Stuðningur Common Data Service-einingar fyrir sérstillt svæði

Í útgáfu þessarar viku styðja eftirfarandi einingar nú sérstillt svæði: Tíðni á útreikningi fríðinda, útreikningur á réttindum fríðinda, gerð fríðinda, vinnudagatal, frídagar á vinnudagatali, greiðsluferli og auðkennisgerð starfskrafta.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Fjöldaskráning á leyfum, breyting á grunnlagi í „Starfsaldursdagsetning“ uppfærir ekki upprunalega uppsöfnun réttinda (318526)

Við fjöldaskráningu starfsmanna og breytingu á grunnlagi endurspeglar upphaflega uppsöfnunin nú grunnlagið sem var valið.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Verkflæði sem sýnir tvítekna staðgengla (313636)

Breytingar í þessari útgáfu koma í veg fyrir tvítekningu á staðgenglum þegar tilkynningar verkflæðis eru sendar.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Víddarreitir eru ekki uppfærðir þegar „Opna í Excel“ er notað (176261)

Í þessari útgáfu er nú hægt að uppfæra fjárhagsvídd með **Opna í Excel** frá síðunni **Starfskraftur**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Aðsetur starfskrafts sem er búið til í Common Data Service er ekki samstillt við Talent (317555)

Með þessari breytingu eru aðsetur sem eru búin til í Common Data Service uppfærð í Talent: Core HR.


## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="new-page-to-validate-position-hierarchy-data"></a>Ný síða til að villuleita gögn staðsetningarstigveldis

Mannauðsstjórar og stjórnendur geta nú villuleitað stjórnunarstigveldið fyrir allar hringtilvísanir sem kunna að hafa verið óvart fluttar inn. Hægt er að komast á þessa síðu frá **Stjórnun fyrirtækis > Tenglar > Staðsetningar > Villuleita stigveldi staðsetningar**.

### <a name="specify-reason-codes-on-leave-types"></a>Tilgreina ástæðukóða fyrir leyfisgerðir

Fyrirtæki gætu gert kröfu um frekari upplýsingar um frítímabeiðnir. Nú er hægt að tilgreina ástæðukóða fyrir leyfisgerðir og leyfa starfsmönnum að velja ástæðukóða fyrir frítímabeiðnir.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Fara fram á ástæðukóða fyrir tilteknar leyfisgerðir á frítímabeiðnum

Fyrirtæki gætu krafist ástæðukóða fyrir ákveðna leyfisgerðir þegar starfsfólk sendir inn frítímabeiðnir. Þessi krafa gæti verið til vegna stefnu fyrirtækis eða reglugerða. Nú er hægt að tilgreina hvers konar leyfisgerðir þurfa ástæðukóða og nú er hægt að krefja starfsfólk um að gefa upp ástæðukóða fyrir leyfisgerðina út af frítímabeiðni þeirra.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Bjóða upp á færslulista leyfa og fjarvista fyrir mannauðsstjóra

Möguleikinn til að fylgjast með frítíma starfsmanns og skilja hvernig frítími er reiknaður hjálpar ekki aðeins mannauðsstjóra við að svara spurningum starfsmanns heldur tryggir einnig nákvæma frítímainneign starfsmanna. Mannauðsstjóri er nú með nýja sýn á færslunum (styrkir, uppsafnanir, leiðréttingar og beiðnir) til, svo að starfsmenn mannauðs geta skoðað ástæðurnar á bak við stöðurnar.

## <a name="coming-soon"></a>Væntanlegt

### <a name="indicate-instance-type-when-provisioning-talent"></a>Tilgreina gerð tilviks við úthlutun Talent

Við úthlutun á nýju tilviki af Talent er hægt að gefa upp hvort gerð tilviks er **Framleiðsla** eða **Sandkassi**, sem opnar fyrir snemmbærar prófanir á nýjum eiginleikum. Öll núverandi tilvik Talent verða uppfærð í tilviksgerðina Framleiðsla. Ef uppfæra á eitt af núverandi tilvikum í tilviksgerðina Sandkassi skal hafa samband við notendaþjónustu til að koma breytingarbeiðninni áfram.


[!INCLUDE[footer-include](../includes/footer-banner.md)]