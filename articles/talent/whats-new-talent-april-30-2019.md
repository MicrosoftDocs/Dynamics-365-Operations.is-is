---
title: Hvað er nýtt eða breytt í Dynamics 365 Talent (30. apríl 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38158948dbcf8966edf49bcce5b1e5da7eddb8dc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026039"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 Talent (30. apríl 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingunum sem er lýst í þessum hluta eiga við um smíðarnúmer 8.1.2270. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Senda ábendingar

Möguleikinn á því að veita endurgjöf er að finna í valmyndinni **Hjálp** (**?**) í Talent. Þessi valmynd veitir aðgang að eftirfarandi tilföngum:

- Ábendingar
- Hjálp
- Leiðsögn
- Stuðningur
- Hugmyndir
- Um

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Umbætur á notendaviðmótinu fyrir tvítekningu á athugun starfsmanns

Vegna þessarar breytingar er nú borin kennsl á tvítekningar þegar reiti fyrir heiti er stilltur, og stöðuvísir sýnir fjölda tvítekninga sem fundust. Tengill sem gefinn er upp opnar síðu þar sem hægt er að meta hvort nota eigi eina af tvítekningunum. Til að forðast að trufla gagnafærslu, opnast tvítekin síða ekki sjálfkrafa. Velja þarf tengilinn til að opna síðuna.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Stuðningur Common Data Service-einingar fyrir sérstillt svæði

Í útgáfu þessarar viku styðja eftirfarandi einingar sérstillt svæði: Ráðning, gerð fríðinda og greiðsluferli.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Villa kemur upp þegar gátlista starfsloka er úthlutað (299877)

Þessi breyting leiðréttir villuboð sem birtast þegar gátlista starfsloka er úthlutað til starfsmanns utan uppsagnarferlisins.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Tengill fyrir starfsmenn sem eru hættir opnar rangan starfsmann (309939)

Þessi breyting leiðréttir vandamál sem kemur upp þegar starfsmaður er endurráðinn frá öðrum lögaðila og reynt er að fara í starfsmann úr listanum yfir hætta starfsmenn.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Launaspjald fyrir sjálfsafgreiðslu starfsmann sýnir ekki samtekin gildi þegar kveikt er á ítarlegu öryggi (315231)

Þessi breyting leiðréttir vandamál sem á sér stað þegar notað er ítarlegt launaöryggi. Þegar kveikt er á ítarlegu öryggi sýnir sjálfsafgreiðsla starfsmanns samantekt launaupphæða fyrir bæði starfsmenn og yfirmenn. Á undan þessari breytingu birtust samantektargildi sem 0 (núll).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Ef staða án titils er búin til í Common Data Service er engin staða búin til í Talent (314562)

Breytingar þessarar viku leiðréttir vandamál sem kemur upp þegar búnar eru til stöður í Common Data Service en titill er ekki gefinn upp.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Villuboð í færslum frammistöðubókar í sjálfsafgreiðslu starfsmanns (314134)

Þessi breyting leiðréttir vandamál sem kemur upp þegar frammistöðumarkmið eru hengd við færslur frammistöðubókar í sjálfsafgreiðslu starfsmanns.

## <a name="in-preview"></a>Í kynningarútgáfu

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leyfa að tilgreina ástæðukóða fyrir leyfisgerðir

Fyrirtæki gætu gert kröfu um frekari upplýsingar um frítímabeiðnir. Nú er hægt að tilgreina ástæðukóða fyrir leyfisgerðir og leyfa starfsmönnum að velja ástæðukóða fyrir frítímabeiðnir.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Fara fram á ástæðukóða fyrir tilteknar leyfisgerðir á frítímabeiðnum

Fyrirtæki gætu krafist ástæðukóða fyrir ákveðna leyfisgerðir þegar starfsfólk sendir inn frítímabeiðnir. Þessi krafa gæti verið til vegna stefnu fyrirtækis eða reglugerða. Nú er hægt að tilgreina hvers konar leyfisgerðir þurfa ástæðukóða og nú er hægt að krefja starfsfólk um að gefa upp ástæðukóða fyrir leyfisgerðina út af frítímabeiðni þeirra.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Bjóða upp á færslulista leyfa og fjarvista fyrir mannauðsstjóra

Möguleikinn til að fylgjast með frítíma starfsmanns og skilja hvernig frítími er reiknaður hjálpar ekki aðeins mannauðsstjóra við að svara spurningum starfsmanns heldur tryggir einnig nákvæma frítímainneign starfsmanna. Mannauðsstjóri er nú með nýja sýn á færslunum (styrkir, uppsafnanir, leiðréttingar og beiðnir) til, svo að starfsmenn mannauðs geta skoðað ástæðurnar á bak við stöðurnar.

## <a name="coming-soon"></a>Væntanlegt

### <a name="email-support-for-alerts"></a>Tölvupóstur út af viðvörunum

Í verkvangsuppfærslu 26 fyrir Finance and Operations geta notendur stofnað viðvörunarreglur sem senda sjálfkrafa tilkynningar í tölvupósti á tengiliði þegar þær ræsast út af tilviki.
