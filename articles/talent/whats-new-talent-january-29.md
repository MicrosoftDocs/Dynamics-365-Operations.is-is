---
title: Nýjungar eða breytingar í Dynamics 365 Talent (31. janúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899106"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Nýjungar eða breytingar í Dynamics 365 Talent (31. janúar 2019)

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.

**Smíði 8.1.2128**

## <a name="core-hr-changes"></a>Breytingar á Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Frítími sem tekin er af leyfi tengiliðaspjalds tekur ekki tillit til dagsetninga leyfisáætlunar
Fyrir þá sem hafa leyfisáætlanir sem ekki keyra ekki á almanaksári birtir **Tekið** spjaldið núna frítíma sem hefur verið tekinn á áætlanamiðuðu leyfisári. Til dæmis, ef leyfisár fyrirtækis er frá 1. júní til og með 30. maí og starfsmaður hefur tekið 3 daga í frí í desember, birtast 3 dagar þann 15. janúar á spjaldinu **Tekið**. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Uppsafnaðar upphæðir passa ekki við lag dagsetningagrunns
Nýjum möguleikum hefur verið bætt við leyfi og fjarvistir (færibreyturnar **Mannauður**) til að gera viðskiptavinum kleift að ákvarða hvenær dagsetning fyrir starfsaldur starfsmanns í mánuðum tekur gildi. Fyrir sum fyrirtæki er dagsetningin í lok mánaðar, en fyrir önnur kann dagsetningin að vera við upphaf næsta mánaðar. Til dæmis getur eitt fyrirtæki veitt frítíma 31. desember á meðan annað fyrirtæki kann að veita frítíma 1. janúar. Þessi valkostur leyfir þér að velja hvenær umbunin á að eiga sér stað. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Aðgerðir starfsmannaráðningar eru fastar í stöðunni „Verkflæði lokið“.
Breytingar hafa verið gerðar til að leiðrétta vandamál þar sem lítill fjöldi verkflæða kláraðist með stöðuna „Verkflæði lokið“. Ný verkflæði ætti nú að færa yfir í stöðuna „Lokið“ þegar verkflæðið klárast. Öll verkflæði með stöðuna lokið verða færð yfir í villustöðu til að leyfa uppfærslu og fjarlægingu ef þörf krefur. 
