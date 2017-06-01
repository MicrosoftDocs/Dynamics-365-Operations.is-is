---
title: "Skilgreina samskipti á smásölurásum (Commerce Data Exchange)"
description: "Þessi skrá veitir yfirlit yfir Commerce Data Exchange og þáttum þess. Það útskýrir þann þátt sem hver þáttur spilar í flutningum gagna milli Microsoft Dynamics 365 for Operations og smásölurása."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ba1bb54a29250a2bb59622ee4391b64ac455af33
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Skilgreina samskipti á smásölurásum (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


Þessi skrá veitir yfirlit yfir Commerce Data Exchange og þáttum þess. Það útskýrir þann þátt sem hver þáttur spilar í flutningum gagna milli Microsoft Dynamics 365 for Operations og smásölurása.

<a name="overview"></a>Yfirlit
--------

Commerce Data Exchange er kerfi sem flytur gögn milli 365 fyrir Operations og smásölurása, eins og netverslanir eða hefðbundnar verslanir. Gagnagrunnur sem geymir gögn fyrir smásölurásar er aðskildar úr Dynamics 365 for Operations gagnagrunninum. Gagnagrunnur smásölurásar inniheldur aðeins gögnin sem krafist er fyrir smásölufærslur. Aðalgögn er skilgreindur í Microsoft Dynamics 365 for Operations og dreift á rásir. Færslugögn er stofnuð í sölustaðarkerfi (POS) eða í netverslun, og svo hlaðið upp í Dynamics 365 for Operations. Gagnadreifing er ósamstillt. Með öðrum orðum, það ferli að safna og pakka gögnum við upprunann á sér stað aðskilið frá ferlinu að taka við og beita gögnum á viðtökustaðnum. Í sumum aðstæðum, eins og verð- og birgðir uppflettingar, verður að sækja gögn í rauntíma. Til að styðja við þessar aðstæður, Commerce Data Exchange inniheldur einnig þjónustu sem virkjar rauntíma samskipti á milli Dynamics 365 fyrir Operations og rásar. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Service
Microsoft SQL Server breytingarrakning í gagnagrunni Dynamics 365 for Operations er notað til að ákvarða breytingar á gögnum sem þarf að senda í rásir. Byggt á dreifingaráætlun, Dynamics 365 for Operations pakkar saman gögnunum og vistar þau í miðlæga geymslu (Azure blob-geymslu). Aðskilin runuvinnsla notar Commerce Data Exchange: Async Client safn til að setja þennan gagnapakka í gagnagrunn rásar. 

[![Ósamstillt þjónusta](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Retail Verkraðari

Raðaravinnslur eru mekanismi til að dreifa gögnum til og frá staðsetningum. Vinnslur sem eru gerðar úr undirvinnslum sem tilgreina töflum og svæðum í töflu sem innihalda gögn sem á að dreifa. Dynamics 365 for Operations felur í sér forskilgreinda röðunarvinnslur og undirvinnslum sem uppfyllir gagnaspeglun fyrir flest fyrirtæki. Eftirfarandi gerðir af forskilgreindum vinnslur eru stofnaðar:

-   **Niðurhalsvinnslur** – Niðurhalsvinnslur senda gögn sem hafa breyst úr Dynamics 365 for Operations til gagnagrunnar rásar. Breytingar á færslum eru raktar gegnum breytingarakningu í SQL Server.
-   **Upphalsvinnslur (P-vinnslur)** – Upphalsvinnslur sækja sölufærslur úr rás og inní gagnagrunn Dynamics 365 for Operations. P-vinnslur senda gögn stigvaxandi. Þegar P-vinnslu er keyrt, athugar safn Async Client gagnaspeglunarteljara fyrir færslur sem hafa þegar verið mótteknar frá staðsetningu. Færsla er hlaðið upp eingöngu ef gagnaspeglunarteljari hennar er hærri en hæsta gildi sem finnst. P-vinnslur uppfæra ekki gögnin sem áður var hlaðið upp.

Dreifingaráætlun er notuð til að keyra gagnaflutning, annaðhvort handvirkt eða með röðun runuvinnslu í Dynamics 365 for Operations. Dreifingaráætlun getur innihaldið einn eða fleiri gagnaflokka rásar, og ein eða fleiri vinnslur verkraðara.

## <a name="realtime-service"></a>Rauntímaþjónusta
Commerce Data Exchange: Real-time Service er innbyggð þjónusta sem býður upp á samskipti í rauntíma á milli Dynamics 365 for Operations og smásölurása. Real-time Service virkjar einstaka tölvur POS og netverslanir til að geta sótt tilteknar gögn úr Dynamics 365 for Operations í rauntíma. Þótt flestum mikilvægustu aðgerðir megi framkvæma í staðbundnum gagnagrunnum rásarinnar, krefjast eftirfarandi aðstæður beins aðgangs að gögnum sem geymd er í Dynamics 365 for Operations:

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




