---
title: "Skilgreina samskipti á smásölurásum (Commerce Data Exchange)"
description: "Þessi skrá veitir yfirlit yfir Commerce Data Exchange og þáttum þess. Það útskýrt hluti sem gegnir hvern þátt í flutning á gögnum milli Microsoft Dynamics 365 aðgerða og smásölurása."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Skilgreina samskipti á smásölurásum (Commerce Data Exchange)

Þessi skrá veitir yfirlit yfir Commerce Data Exchange og þáttum þess. Það útskýrt hluti sem gegnir hvern þátt í flutning á gögnum milli Microsoft Dynamics 365 aðgerða og smásölurása.

<a name="overview"></a>Yfirlit
--------

Commerce Data Exchange er kerfi sem flytur gögn milli Dynamics 365 aðgerða og smásölurása verslanir á netinu eða stað og mortar verslanir. Gagnagrunnur sem geymir gögn fyrir smásölurásar er aðskildar frá Dynamics 365 fyrir gagnagrunn Aðgerðir. Gagnagrunnur smásölurásar inniheldur aðeins gögnin sem krafist er fyrir smásölufærslur. Aðalgögn er skilgreindur í Dynamics 365 aðgerða og þeim dreift til rásir. Færslugögn er stofnuð á sölustað. kerfið eða á netinu geyma, og svo hlaðið upp Dynamics 365 fyrir Aðgerðir. Gagnadreifing er ósamstillt. Með öðrum orðum, það ferli að safna og pakka gögnum við upprunann á sér stað aðskilið frá ferlinu að taka við og beita gögnum á viðtökustaðnum. Í sumum aðstæðum, eins og verð- og birgðir uppflettingar, verður að sækja gögn í rauntíma. Til að styðja við þessar aðstæður, Commerce Data Exchange inniheldur einnig þjónustu sem gerir upp samskipti milli Dynamics 365 fyrir Aðgerðir og leið. 

[![uppfæra-retail-mynd](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Service
Microsoft SQL Server breytingarrakningu í Dynamics 365 fyrir gagnagrunn Aðgerða er notuð til að ákvarða gögn breytingarnar sem þarf að senda rásir. Samkvæmt dreifingaráætlun Dynamics 365 aðgerða packages gögnin og vistar central geymslu (Azure blob geymslu). Aðskilin runuvinnsla notar Commerce Data Exchange: Async Client safn til að setja þennan gagnapakka í gagnagrunn rásar. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Retail Verkraðari

Raðaravinnslur eru mekanismi til að dreifa gögnum til og frá staðsetningum. Vinnslur sem eru gerðar úr undirvinnslum sem tilgreina töflum og svæðum í töflu sem innihalda gögn sem á að dreifa. Dynamics 365 aðgerða felur í sér forskilgreindar verkraðara og undirvinnslum sem uppfyllir gagnaspeglun yfir flest fyrirtæki. Eftirfarandi gerðir af forskilgreindum vinnslur eru stofnaðar:

-   **Sækja vinnslur** – Niðurhal vinnslur senda gögn sem hefur breyst úr Dynamics 365 aðgerða gagnagrunnar rásar. Breytingar á færslum eru raktar gegnum breytingarakningu í SQL Server.
-   **Senda vinnslur (P-vinnslur)** – Upphleðslu vinnslur sækja sölufærslur úr leið í Dynamics 365 fyrir Aðgerðir í gagnagrunni. P-vinnslur senda gögn stigvaxandi. Þegar P-vinnslu er keyrt, athugar safn Async Client gagnaspeglunarteljara fyrir færslur sem hafa þegar verið mótteknar frá staðsetningu. Færsla er hlaðið upp eingöngu ef gagnaspeglunarteljari hennar er hærri en hæsta gildi sem finnst. P-vinnslur uppfæra ekki gögnin sem áður var hlaðið upp.

Dreifingaráætlun sem er notuð til að keyra flutning gagna, annað hvort handvirkt eða með röðun runuvinnslu í Dynamics 365 fyrir Aðgerðir. Dreifingaráætlun getur innihaldið einn eða fleiri gagnaflokka rásar, og ein eða fleiri vinnslur verkraðara.

## <a name="realtime-service"></a>Realtime-Þjónustuna
Commerce Data Exchange: Real-time Service er innbyggð þjónusta sem býður upp samskipti milli Dynamics 365 aðgerða og smásölurása. Real-time Service gerir einstaka tölvur POS og netverslanir til að sækja tilteknar gögn úr Dynamics 365 fyrir Aðgerðir í rauntíma. Þó að hægt er að framkvæma flestum helstu aðgerðir í gagnagrunni rásar staðbundna við eftirfarandi kringumstæður þurfa aðgang að gögnum sem geymd er í Dynamics 365 fyrir Aðgerðir:

-   Útgáfa og innleysing gjafakorta.
-   Innleysa vildarpunkta.
-   Útgáfa og innleysing kreditreikninga.
-   Stofnun og uppfærsla á færslu viðskiptavinar.
-   Stofna, uppfærslu og ljúka sölupöntunum.
-   Móttaka birgða gagnvart innkaupapöntun eða flutningspöntun.
-   Framkvæma birgðatalningu.
-   Sækja sölufærslur milli verslana og ljúka skilafærslum.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Forskilgreind Real-time Service forstilling er stofnuð.


