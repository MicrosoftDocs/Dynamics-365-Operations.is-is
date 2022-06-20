---
title: Tiltækt fjármagn úr fjárhagsáætlun
description: Þessi grein kynnir tiltæka eiginleika fjárhagsáætlunarsjóða og veitir upplýsingar sem geta hjálpað þér að stilla fjárhagsáætlunarstýringu til að hámarka stjórnun á fjárhag fyrirtækisins.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898241"
---
# <a name="budget-funds-available"></a>Tiltækt fjármagn úr fjárhagsáætlun

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein kynnir tiltæka eiginleika fjárhagsáætlunarsjóða og veitir upplýsingar sem geta hjálpað þér að stilla fjárhagsáætlunarstýringu til að hámarka stjórnun á fjárhag fyrirtækisins.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Aukinn útreikningseiginleiki fyrir fjárveitingar í boði

The **Fylgstu aðeins með upphæðum í tiltækum útreikningi fjárlaga** eiginleiki gerir þér kleift að fylgjast með undirliggjandi fjárhagsáætlunarstjórnunartöflum fyrir skjalagerðir og ástand, byggt á stillingum á **Skilgreindu færibreytur fjárhagsáætlunarstýringar** síðu.

Sumir stillingarvalkostir fjárhagsáætlunarstýringar verða að hafa sérstakar stillingar til að eiginleikinn virki rétt. Þessir valkostir eru valdir eða hreinsaðir á **Fjármagn til ráðstöfunar** flipi á **Skilgreindu færibreytur fjárhagsáætlunarstýringar** síðu. Eftirfarandi tafla sýnir stillingarnar sem eru nauðsynlegar fyrir tiltæka eiginleika fjárhagsáætlunarfjár.

| Ef þessi valkostur er valinn | Einnig verður að velja þennan valkost |
| ------------------------- | -------------------------------- |
| Frátektir fjárhagsáætlunar fyrir áætlaðar fjárúthlutanir | Fjárhagsfyrirvarar vegna kvaða *og* Raunveruleg útgjöld |
| Frátektir fjárhagsáætlunar fyrir fjárúthlutanir | Raunútgjöld |
| Fráteknir fjárhagsáætlunar fyrir kvaðir með skjölum af gerð innkaupabeiðni | Frátektir fjárhagsáætlunar fyrir áætlaðar fjárúthlutanir |

Þessi eiginleiki hefur aðeins áhrif á ný skjöl. Upphæðir fyrir núverandi skjöl verða áfram raktar og sýndar í fyrirspurn um tölfræði fjárhagsáætlunarstýringar þar til stillingu fjárhagsáætlunarfjár tiltækt er breytt og nýja stillingar fjárhagsáætlunarstýringar er virkjuð. Á þeim tímapunkti verða rakningargögn fjárhagsáætlunar fjarlægð fyrir skjöl sem voru fjarlægð úr tiltækum útreikningi fjárhagsáætlunarfjár.

Við mælum með að þú yfirgefur **Óbókuð raunútgjöld** valkostur hreinsaður. Ef það er valið verður tímafrekur útreikningur fjárhagsáætlunargerðar á óbókuðum skjölum, svo sem reikningum lánardrottins í bið.
