---
title: Flytja inn eiginleika frá alþjóðlegu geymslunni
description: Þetta efnisatriði útskýrir hvernig á að flytja inn hnattvæðingareiginleika úr alþjóðlegu geymslunni.
author: dkalyuzh
ms.date: 02/11/2022
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
ms.openlocfilehash: ff3019986d089a286f7aef94346398b3d328ad54
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371927"
---
# <a name="import-features-from-the-global-repository"></a>Flytja inn eiginleika frá alþjóðlegu geymslunni

[!include [banner](../includes/banner.md)]

Alþjóðlega geymslan inniheldur rafræna reikningseiginleika sem er deilt með stillingaveitunni þinni. Öllum eiginleikum rafrænna reikninga sem Microsoft býður upp á er deilt með öllum fyrirtækjum. Þú hefur sjálfkrafa aðgang að öllum eiginleikum rafrænna reikninga sem Microsoft gefur út og birtir á alþjóðlegu geymslunni.

Til að byrja að vinna með eiginleika rafrænna reikninga sem er deilt með stillingaveitunni þinni skaltu flytja þá inn í tilvikið þitt af Regulatory Configuration Service (RCS) frá alþjóðlegu geymslunni. Skoðaðu síðan eiginleikaupplýsingarnar, svo sem rafræna skýrslugerð (ER) stillingar og vinnsluleiðslur.

## <a name="import-a-feature-from-the-global-repository"></a>Flytja inn eiginleika úr alþjóðlegu geymslunni

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Veldu **Flytja inn** að opna **Flytja inn eiginleiki frá alþjóðlegri geymslu** horfðu upp.
4. Til að skoða rafræna reikningseiginleika í alþjóðlegu geymslunni sem eru tiltækar fyrir tiltekna stillingaveitu skaltu samstilla RCS tilvik fyrirtækisins með því að velja **Samstilla**. Eftir að samstillingu er lokið er listi yfir tiltæka eiginleika rafrænna reikninga uppfærður úr alþjóðlegu geymslunni. Þessi uppfærsla gæti tekið nokkrar mínútur.
5. Veldu eiginleikann sem á að flytja inn og veldu síðan **Flytja inn**.

Til að skoða innfluttan rafrænan reikningseiginleika, vertu viss um að rétt stillingarveita sé valin. Sjálfgefið er að eiginleikar sem voru búnir til af virku stillingarveitunni eru sjálfkrafa síaðir út. Þú getur stillt síuna til að skoða eiginleika sem voru búnir til af öðrum veitum, eins og Microsoft stillingarveitunni.

Þú getur nú unnið með innflutta eiginleikann. Þú getur skoðað upplýsingar þess og búið til nýjan eiginleika með því að nota innflutta eiginleikann sem sniðmát.

> [!NOTE]
> Þú getur aðeins breytt eiginleikum ef hann var búinn til af stillingaveitunni sem er virkur. Þú getur búið til nýjan eiginleika með því að nota upprunalega eiginleikann sem grunn. Þú getur síðan gert nauðsynlegar breytingar eða sett upp færibreytur.

Þegar Microsoft eða annað fyrirtæki sem deilir hnattvæðingareiginleikum með fyrirtækinu þínu uppfærir eiginleika sem þú hefur flutt inn geturðu leitað að uppfærðum útgáfum með því að velja **Athugaðu hvort eiginleikauppfærslur séu til staðar** í **Tengdar stillingar** kafla í **Hnattvæðingareiginleikar** vinnurými.

Ef þú sérð að það eru uppfærslur fyrir eiginleika sem þú notar sem sniðmát geturðu flutt inn nýja útgáfu eftir að þú hefur samstillt listann yfir birta eiginleika í alþjóðlegu geymslunni.
