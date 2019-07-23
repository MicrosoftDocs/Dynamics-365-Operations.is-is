---
title: Hvað er nýtt eða breytt í Dynamics 365 for Talent (23. apríl 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5ec10820761cb22cbff6229babe8a250848214b7
ms.sourcegitcommit: 15154b0aa86110ce5fad6f63e6763103a676a1d2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624582"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-23-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 for Talent (23. apríl 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 for Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard
Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 for Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR
Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2253. Tölur í sviga vísa til stuðningsnúmera í Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Stuðningur Common Data Service-einingar fyrir sérstillt svæði
Með útgáfunni í þessari viku styðja eftirfarandi einingar sérstillt svæði: launastig, fríðindavalkost, hæfnisgerð og launasvæði.

### <a name="additional-odata-entities-302992"></a>Aðrar OData-einingar (302992)
Eftirfarandi einingar eru nú studdar innan OData: starfsreynsla starfskrafts og menntun starfskrafts.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Viðhengi fyrir frammistöðubók fyrir yfirmenn og starfsmenn (308248)
Með þessari útgáfu eru viðhengi nú í boði fyrir bæði yfirmenn og starfsmenn þegar færslur frammistöðubókar eru búnar til og uppfærðar.

### <a name="employee-rehire-flag-always-available-310047"></a>Endurráðningarflagg starfsmanns er alltaf í boði (310047)
Endurráðningarvalkostur starfsmanns er nú í boði fyrir uppfærslu utan uppsagnarferlisins. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Ekki er hægt að breyta heiti á **Greiðslumáti notanda** (308815)
Sérstilling hefur verið virkjuð til að gera kleift að breyta **Greiðslumáti notanda** í sjálfsafgreiðslu starfsmanns.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Ekki er hægt að eyða fjárhagsvíddum gagnvart stöðu (293908)
Núna er hægt að fjarlægja fjárhagsvíddir þegar óskað er eftir breytingu fyrir fyrirliggjandi stöðu og mörk fjárhagsvídda yfir fyrirtækið. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Viðskiptavinur er ófær um að birta aftur gögn í Talent þegar hann opnar gögnin úr Excel (302955)
Þessi breyting leiðréttir vandamál við útgáfu þegar tengdar töflur eru notaðar.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leyfa að tilgreina ástæðukóða fyrir leyfisgerðir
Fyrirtæki gætu þurft frekari upplýsingar um frítímabeiðnir. Nú er hægt að tilgreina ástæðukóða fyrir leyfisgerðir og gert starfsmönnum kleift að velja ástæðukóða fyrir frítímabeiðnir.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Fara fram á ástæðukóða fyrir ákveðnar leyfisgerðir á frítímabeiðnum
Fyrirtæki gætu krafist ástæðukóða fyrir ákveðna leyfisgerðir þegar starfsfólk sendir inn frítíma. Þetta gæti verið vegna stefnu fyrirtækis eða út af reglugerðum. Nú er hægt að tilgreina hvers konar leyfisgerðir þurfa ástæðukóða og nú er hægt að krefja starfsfólk um að gefa upp ástæðukóða fyrir leyfisgerðina út af frítímabeiðni þeirra.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Bjóða upp á færslulista leyfa og fjarvista fyrir mannauðsstjóra
Að fylgjast með frítíma starfsmanns og skilja hvernig frítími er reiknaður hjálpar ekki aðeins mannauðsstjóra við að svara spurningum starfsmanns en tryggir einnig nákvæma frítímainneign starfsmanna. Mannauðsstjóri er nú með nýja sýn á færslunum (styrkir, uppsafnanir, leiðréttingar og beiðnir) til að sjá ástæðurnar á bak við stöðurnar.

## <a name="coming-soon"></a>Væntanlegt

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Umbætur á notendaviðmótinu fyrir tvítekningu á athugun starfsmanns
Með þessari breytingu er borið kennsl á tvítekningar á meðan þú færir inn heiti á reitum og staða sýnir hversu margar tvítekningar fundust. Þú getur valið tengilinn sem gefinn er upp til að opna nýja síðu til að meta hvort nota skuli samsvörun sem borin var kennsl á. Til að forðast að trufla gagnafærslu, opnast tvítekin skjámynd ekki sjálfkrafa.
## <a name="known-issues"></a>Þekkt vandamál

### <a name="email-support-for-alerts"></a>Tölvupóstur út af viðvörunum
Í verkvangsuppfærslu 26 geta notendur stofnað viðvörunarreglur sem senda sjálkrafa tilkynningar í tölvupósti á tengiliði þegar þær ræsast út af tilviki.
