---
title: Tiltækt fjármagn úr fjárhagsáætlun
description: Í þessari grein er kynntur eiginleiki fjárhagsáætlunarstýringar og veittar upplýsingar sem hjálpa til við að stilla fjárhagsáætlunarstýringu til að ná sem mest út úr stjórnun á fjárhagslegum tilföngum fyrirtækisins.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898241"
---
# <a name="budget-funds-available"></a>Tiltækt fjármagn úr fjárhagsáætlun

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessari grein er kynntur eiginleiki fjárhagsáætlunarstýringar og veittar upplýsingar sem hjálpa til við að stilla fjárhagsáætlunarstýringu til að ná sem mest út úr stjórnun á fjárhagslegum tilföngum fyrirtækisins.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Ítarlegur útreikningseiginleiki fyrir tiltækt fjármagn fjárhagsáætlunar

Eiginleikinn **Aðeins rekja upphæðir með í útreikningi á tiltæku fjármagni fjárhagsáætlunar** gerir þér kleift að fylgjast með undirliggjandi fjárhagsáætlunarstýringartöflum fyrir skjalategundir og stöður, byggt á stillingum á síðunni **Skilgreina færibreytur fjárhagsáætlunarstýringar**.

Sumir stillingarvalkostir fyrir stjórn fjárhagsáætlunar verða að vera með sérstakar stillingar til að eiginleikinn virki rétt. Þessir valkostir eru valdir eða hreinsaðir á flipanum **Tiltækt fjármagn úr fjárhagsáætlun** flipanum úr **Skilgreina færibreytur fjárhagsáætlunarstýringar** síðunni. Eftirfarandi tafla sýnir stillingarnar sem eru nauðsynlegar fyrir tiltæka eiginleikann fyrir fjármagn fjárhagsáætlunar.

| Þessi möguleiki er valinn | Þessi valkostur verður einnig að vera valinn |
| ------------------------- | -------------------------------- |
| Frátektir fjárhagsáætlunar fyrir áætlaðar fjárúthlutanir | Frátektir fjárhagsáætlunar fyrir fjárúthlutanir *og* raunútgjöld. |
| Frátektir fjárhagsáætlunar fyrir fjárúthlutanir | Raunútgjöld |
| Frátektir fjárhagsáætlunar fyrir fjárúthlutanir með skjölum af innkaupabeiðnigerð | Frátektir fjárhagsáætlunar fyrir áætlaðar fjárúthlutanir |

Þessi eiginleiki hefur aðeins áhrif á ný skjöl. Fjárhæðir fyrirliggjandi skjala verða áfram raktar og sýndar í fyrirspurn um fjárhagsáætlunarstjórnun þar til fjárhagsáætlunarstillingu er breytt og nýja fjárhagsáætlunarstýringarstillingin er virkjuð. Á þeim tímapunkti verða fylgigögn fjárhagsáætlunar fjarlægð fyrir skjöl sem voru fjarlægð úr tiltækum útreikningi fjárhagsáætlunar.

Mælt er með því að valkosturinn **Óbókuð raunútgjöld** sé fjarlægður. Ef það er valið verður farið í tímafreka útreikninga á fjárhagsstjórn á óbirtum skjölum, t.d. reikningum seljenda sem bíða.
