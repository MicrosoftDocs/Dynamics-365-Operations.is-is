---
title: Vinna með stillingar
description: Þetta efnisatriði veitir yfirlit yfir helstu atburðarás fyrir vinnu með rafrænum skýrslum (ER) stillingum frá Hnattvæðingareiginleikum vinnusvæðinu.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371964"
---
# <a name="work-with-configurations"></a>Vinna með stillingar

[!include [banner](../includes/banner.md)]

Stillingar rafrænna skýrslugerðar (ER) eru ein helsta sett af íhlutum rafrænna reikningseiginleika. ER uppsetning inniheldur uppsetningu skráarskipulagsins og sett af umbreytingarreglum til að umbreyta gögnum á tvo vegu:

- **Flytja út ER snið stillingar** – Þessi uppsetning umbreytir gögnum úr sameinuðu innri skipulagi (ER líkan) yfir í rafrænt skráarsnið.
- **Flytja inn ER snið stillingar** – Þessi uppsetning umbreytir gögnum úr rafrænu skráarsniði yfir í sameinaða innri uppbyggingu (ER líkan).

Auk þess að búa til rafrænar skrár á útleið á fyrirfram skilgreindu sniði, eru ER stillingar mikið notaðar til að flokka innkomin skilaboð frá ytri vefþjónustu sem svör. Þessi virkni hjálpar til við að byggja upp stillanlega rökfræði til að fá niðurstöður samskipta við ytri rásir, umbreyta þessum niðurstöðum (kóðum, skilaboðum og annálum) í notendalesanlega uppbyggingu og senda þær upplýsingar til biðlaraforritsins.

Til að byrja að nota ER stillingar í rafræna reikningseiginleika þínum verður þú að tengja þær við eiginleikann og gera þær aðgengilegar á **Stillingar** flipa fyrir núverandi eiginleikaútgáfu. Þú getur unnið með tengda ER uppsetningu með því að velja **Bæta við**, **·**, **·**, eða **Útsýni**.

Áður en þú getur bætt við tengli við ER uppsetningu verður stillingin að vera til í Regulatory Configuration Service (RCS) geymslunni þinni. Til að fara yfir ER stillingar sem eru tiltækar í RCS geymslunni þinni skaltu fylgja þessum skrefum.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Í vinnusvæðinu **Rafræn skýrslugerð**, í kaflanum **Skilgreiningar** velurðu reitinn **Skilgreiningar skýrslugerðar**.

Fyrir upplýsingar um hvernig á að búa til nýja ER-stillingu eða flytja inn núverandi ER-stillingu úr alþjóðlegu geymslunni, sjá [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Til að stilla tengda ER uppsetningu skaltu velja **Breyta** á **Stillingar** flipa fyrir núverandi eiginleika rafrænna reikninga. Kerfið býr sjálfkrafa til útgáfu af ER uppsetningunni. Ef núverandi útgáfa var ekki búin til af virku stillingaveitunni, býr kerfið til afleidda útgáfu sem notar stillingarveituna þína. Ef núverandi útgáfa var búin til af virku stillingarveitunni, býr kerfið til nýja útgáfu. Í báðum tilfellum er hægt að breyta útgáfunni sem er búin til og síðan gera allar nauðsynlegar uppfærslur sjálfkrafa.
