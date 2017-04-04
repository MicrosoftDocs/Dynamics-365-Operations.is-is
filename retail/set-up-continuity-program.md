---
title: "Setja upp samfelldniáætlanirnar fyrir símaver"
description: "Þessi grein lýsir hvernig setja á upp samfelldniáætlanirnar fyrir símaver."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e32961f2a0e0e41715d98075cbc5777d256eb187
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Setja upp samfelldniáætlanirnar fyrir símaver

Þessi grein lýsir hvernig setja á upp samfelldniáætlanirnar fyrir símaver.

Í samfelldniáætlun, sem er einnig þekkt sem forrit fyrir endurtekna pöntun, viðskiptavinir fá reglulegar vörusendingar samkvæmt fyrirfram ákveðinni áætlun. Hver sending getur innihaldið aðra afurð og mál yfir bók-á-í-mánuður klúbbkort, eða hægt er að senda á sömu afurð margsinnis. Til að skilgreina samfelldniáætlun þarf að ljúka eftirfarandi verkefnum:

1.  Setja upp færibreytur samfelldni á síðunni **Færibreytur símavers**.
2.  Stofnaðu samfelluforrit sem skilgreinir upplýsingar, svo sem greiðsluáætlun, tímasetningu sendingar, og hvort greitt er upp að framan. Einnig verður að bæta við lista yfir afurðir sem eru innifaldar í samfelldniáætlanirnar. Hverja vöru fær tilviki kennisnúmer sem er úthlutað röð, byrja 1. Tilvikið Kennum ákvarða pöntun sem vörur eru sendar.
    -   Þegar viðskiptavinir fá mismunandi afurð í hverri sendingu eru afurðirnar sendar raðbundið, samkvæmt tilvikskennum þeirra og ni tilviks frá og hefjast á núgildandi tilviki.
    -   Ef viðskiptavinir fá sömu afurð í hverri sendingu inniheldur listinn einungis eina afurð sem hefur eitt tilvikskenni. Sama atvikið kemur endurtekið upp. Hægt er að tilgreina hversu oft á að endurtaka öll tilvik.

3.  Stofna yfirstig afurð sem stendur fyrir samfelldniáætlanirnar sem stofnaðir voru í verkið 2. Ef þessi afurð er bætt við sölupöntun, í **Samfelldni** opnast. Síðan er hægt að nota þá síðu til að stofna samfelldnipöntunina sjálfa. Yfirstig afurða tilgreinir ekki stakar afurðir sem viðskiptavinur fær í hverri sendingu.

Eftir að þú hefur sett upp samfelluforrit eins og lýst er hér að ofan, getur þú stofnað samfellupöntun fyrir viðskiptavin. Einnig gæti þurft að framkvæma eftirfarandi verk viðbótar viðhalds:

-   **Uppfæra núverandi tilvikstímabil samfelldni** – Setja upp runuvinnslu sem segir kerfinu hvert núverandi tilvikstímabilið er.
-   **Stofna samfelldniundirpantanir** - Stofna undirpantanir úr yfirstigi samfelldnipöntunar.
-   **Vinna samfelldnigreiðslur** – Vinna reikningsfærslu og tilkynningar fyrir greiðslur sem eru tengdar samfelldnisölupöntunum.
-   **Útvíkka samfelldnilínur (Ef þarf)** - Lengja fjölda skipta sem hægt er að endurtaka samfelldnitilvik. Endurtekning sendinga er síðan hægt að útvíkka umfram mörk sem voru sett í reitinn **Viðmiðunarmörk á endurtekinni samfelldni** í færibreytum símavers.
-   **Framkvæma samfelldniuppfærslu** (ef þarf) - Samstilltu breytingar milli samfelldniáætlunarinnar og samfelldni yfirsölupöntunar.
-   **Loka samfelldnisyfirlínum og -pöntunum** - Loka pöntunum.



