---
title: Setja upp samfelldniáætlanir fyrir símaver
description: Þessi grein lýsir hvernig setja á upp samfelldniáætlanirnar fyrir símaver.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 39c3e6d740bff2af27a2fba2ac4c406c01b43a87218fdc1dcfe094c147cd3de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716151"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Setja upp samfelldniáætlanir fyrir símaver

[!include [banner](includes/banner.md)]

Þessi grein lýsir hvernig setja á upp samfelldniáætlanirnar fyrir símaver.

Í samfelldniáætlun, sem er einnig þekkt sem forrit fyrir endurtekna pöntun, viðskiptavinir fá reglulegar vörusendingar samkvæmt fyrirfram ákveðinni áætlun. Hver sending getur innihaldið aðra afurð og mál yfir bók-á-í-mánuður klúbbkort, eða hægt er að senda á sömu afurð margsinnis. Til að skilgreina samfelldniáætlun þarf að ljúka eftirfarandi verkefnum:

1. Setja upp færibreytur samfelldni á síðunni **Færibreytur símavers**.
2. Stofnaðu samfelluforrit sem skilgreinir upplýsingar, svo sem greiðsluáætlun, tímasetningu sendingar, og hvort greitt er upp að framan. Einnig verður að bæta við lista yfir afurðir sem eru innifaldar í samfelldniáætlanirnar. Hver afurð fær kennisnúmer tilviks sem er úthlutað í röð og byrjar á 1. Kenni tilviks ákvarðar röðina sem afurðir eru sendar í.

    - Þegar viðskiptavinir fá mismunandi afurð í hverri sendingu eru afurðirnar sendar raðbundið, samkvæmt tilvikskennum þeirra og ni tilviks frá og hefjast á núgildandi tilviki.
    - Ef viðskiptavinir fá sömu afurð í hverri sendingu inniheldur listinn einungis eina afurð sem hefur eitt tilvikskenni. Sama atvikið kemur endurtekið upp. Hægt er að tilgreina hversu oft á að endurtaka öll tilvik.

3. Stofnaðu yfirafurð sem endurspeglar samfelluforritið sem þú bjóst til í verki 2. Ef þessar afurð er bætt við sölupöntun opnast síðan **Samfelldni**. Síðan er hægt að nota þá síðu til að stofna samfelldnipöntunina sjálfa. Yfirstig afurða tilgreinir ekki stakar afurðir sem viðskiptavinur fær í hverri sendingu.

Eftir að þú hefur sett upp samfelluforrit eins og lýst er hér að ofan, getur þú stofnað samfellupöntun fyrir viðskiptavin. Einnig gæti þurft að framkvæma eftirfarandi verk viðbótar viðhalds:

- **Uppfæra núverandi tilvikstímabil samfelldni** – Setja upp runuvinnslu sem segir kerfinu hvert núverandi tilvikstímabilið er.
- **Stofna samfelldniundirpantanir** - Stofna undirpantanir úr yfirstigi samfelldnipöntunar.
- **Vinna samfelldnigreiðslur** – Vinna reikningsfærslu og tilkynningar fyrir greiðslur sem eru tengdar samfelldnisölupöntunum.
- **Útvíkka samfelldnilínur (Ef þarf)** - Lengja fjölda skipta sem hægt er að endurtaka samfelldnitilvik. Endurtekning sendinga er síðan hægt að útvíkka umfram mörk sem voru sett í reitinn **Viðmiðunarmörk á endurtekinni samfelldni** í færibreytum símavers.
- **Framkvæma samfelldniuppfærslu** (ef þarf) - Samstilltu breytingar milli samfelldniáætlunarinnar og samfelldni yfirsölupöntunar.
- **Loka samfelldnisyfirlínum og -pöntunum** - Loka pöntunum.


[!INCLUDE[footer-include](../includes/footer-banner.md)]