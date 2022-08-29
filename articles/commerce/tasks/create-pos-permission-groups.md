---
title: Stofna heimildaflokka sölustaða
description: Þessi grein útskýrir hvernig á að búa til POS heimildahóp.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277961"
---
# <a name="create-pos-permission-groups"></a>Stofna heimildaflokka sölustaða

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að búa til POS heimildahóp. Sýnigögn fyrirtækisins til að stofna verkið er USRT. Þetta verk er ætluð fyrir hlutverk stjórnanda Commerce aðgerðir.

1. Í skoðunarrúðunni ferðu í **Einingar > Retail og Commerce > Starfsmenn > Leyfishópar**.
2. Veljið **Nýtt**.
3. Færðu inn gildi í reitnum **Kenni heimildaflokks sölustaðar**.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Velja skal **Já** í reitnum **Skoða færslur stimpilklukku**. Nú er hægt að virkja eða óvirkja mismunandi heimildir fyrir heimildaflokk Sölustaðar. Í sumum heimild hægt að stilla gildi sem verður notað til að meta ef notanda sölustaður getur framkvæmt aðgerðina. Þessi leiðarvísi fyrir verk virkjar nokkrar heimild sem hugsanlega má veita gjaldkera.  
6. Velja skal **Já** í reitnum **Leyfa stofnun pöntunar**.
7. Velja skal **Já** í reitnum **Leyfa breytingu á pöntun**.
8. Velja skal **Já** í reitnum **Leyfa að pöntun sé sótt**.
9. Velja skal **Já** í reitnum **Leyfa breytingu á aðgangsorði**.
10. Velja skal **Já** í reitnum **Leyfa blinda lokun**.
11. Veljið **Vista**. Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á Commerce-rása. 
12. Í skoðunarglugganum ferðu í **Kerfiseiningar > Mannauður > Störf > Störf**.
13. Næsta verður að úthluta heimildaflokk Sölustaðar til Vinnslu. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Veljið **Breyta**.
15. Útvíkkaðu hlutann **Flokkun starfs**.
16. Í reitinn Heimildaflokkur sölustaðar skal slá inn eða velja gildi. Allir starfsmenn í stöðum fyrir þessa vinnslu munu nota stillingar þessa heimildaflokks sölustaðar nema heimildum sölustaðar starfsmanna hafi verið hnekkt á stöðustigi þeirra.  
17. Veljið **Vista**. Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á rása.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
