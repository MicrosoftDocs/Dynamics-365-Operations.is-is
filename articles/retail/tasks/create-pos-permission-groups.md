---
title: Stofna heimildaflokka sölustaða
description: Þetta efnisatriði útskýrir hvernig á að stofna heimildaflokk sölustaðar.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914805"
---
# <a name="create-pos-permission-groups"></a>Stofna heimildaflokka sölustaða

[!include[task guide banner](../includes/task-guide-banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna heimildaflokk sölustaðar. Sýnigögn fyrirtækisins til að stofna verkið er USRT. Þetta verk er ætluð fyrir hlutverk stjórnanda Smásölu aðgerðir.

1. Í skoðunarrúðunni ferðu í **Einingar > Smásala > Starfsmenn > Leyfishópar**.
2. Veljið **Nýtt**.
3. Færðu inn gildi í reitnum **Kenni heimildaflokks sölustaðar**.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Velja skal **Já** í reitnum **Skoða færslur stimpilklukku**. Nú er hægt að virkja eða óvirkja mismunandi heimildir fyrir heimildaflokk Sölustaðar. Í sumum heimild hægt að stilla gildi sem verður notað til að meta ef notanda sölustaður getur framkvæmt aðgerðina. Þessi leiðarvísi fyrir verk virkjar nokkrar heimild sem hugsanlega má veita gjaldkera.  
6. Velja skal **Já** í reitnum **Leyfa stofnun pöntunar**.
7. Velja skal **Já** í reitnum **Leyfa breytingu á pöntun**.
8. Velja skal **Já** í reitnum **Leyfa að pöntun sé sótt**.
9. Velja skal **Já** í reitnum **Leyfa breytingu á aðgangsorði**.
10. Velja skal **Já** í reitnum **Leyfa blinda lokun**.
11. Veljið **Vista**. Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á smásölurása. 
12. Í skoðunarglugganum ferðu í **Kerfiseiningar > Mannauður > Störf > Störf**.
13. Næsta verður að úthluta heimildaflokk Sölustaðar til Vinnslu. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Veljið **Breyta**.
15. Útvíkkaðu hlutann **Flokkun starfs**.
16. Í reitinn Heimildaflokkur sölustaðar skal slá inn eða velja gildi. Allir starfsmenn í stöðum fyrir þessa vinnslu Munu nota stillingar þessa heimildaflokk Sölustaðar nema heimildir Sölustaðar starfsmanna hafi verið hnekkt á stigi Stöðu þeirra.  
17. Veljið **Vista**. Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á smásölurása.  

