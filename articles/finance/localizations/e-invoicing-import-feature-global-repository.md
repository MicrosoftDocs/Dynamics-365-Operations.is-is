---
title: Flytja inn eiginleika úr altækri geymslu
description: Í þessari grein er útskýrt hvernig á að flytja inn altæka eiginleika úr altækri geymslu.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5a72673e17c5653d43b60d3348d5518e09c40a15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278312"
---
# <a name="import-features-from-the-global-repository"></a>Flytja inn eiginleika úr altækri geymslu

[!include [banner](../includes/banner.md)]

Altæka geymslan inniheldur eiginleika rafrænnar reikningsfærslu sem deilt er með skilgreiningarveitunni þinni. Allir eiginleikar rafrænnar reikningsfærslu sem Microsoft býður upp á er deilt með öllum fyrirtækjum Þú færð sjálfkrafa aðgang að öllum rafrænum reikningseiginleikum sem Microsoft gefur út og birtir í gagnasafni á heimsvísu.

Til að byrja að vinna með eiginleika rafrænnar reikningsfærslu sem deilt er með skilgreiningarveitunni þinni skaltu flytja þá inn í tilvikið þitt af Regulatory Configuration Service (RCS) úr altæku geymslunni. Farðu svo yfir upplýsingar um eiginleikann, t.d. skilgreiningar rafrænnar skýrslugerðar og vinnslukeðjur.

## <a name="import-a-feature-from-the-global-repository"></a>Flytja inn eiginleika úr altækri geymslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Veldu **Flytja inn** til að opna uppflettinguna **Flytja inn eiginleika úr altækri geymslu**.
4. Til að fletta í gegnum eiginleika rafrænnar reikningsfærslu sem eru í boði fyrir tiltekna skilgreiningarveitu skal samstilla RCS-tilvik fyrirtækisins með því að velja **Samstilla**. Að samstillingu lokinni verður listi yfir tiltæka eiginleika rafrænnar reikningsfærslu uppfærður úr altæku geymslunni. Þessi uppfærsla gæti tekið nokkrar mínútur.
5. Veldu eiginleikann sem á að flytja inn og veldu síðan **Flytja inn**.

Til að skoða innflutta rafræna reikningagerð skal ganga úr skugga um að rétt stillingaþjónusta sé valin. Sjálfgefið er að eiginleikar sem voru búnir til af virkri skilgreiningarveitu séu sjálfkrafa síaðir út. Þú getur breytt síunni til að skoða eiginleika sem aðrar veitur hafa búið til, t.d. skilgreiningarveita Microsoft.

Nú getur þú unnið með innfluttningseiginleikann. Þú getur farið yfir upplýsingar um það og búið til nýjan eiginleika með því að nota innflutta eiginleikann sem sniðmát.

> [!NOTE]
> Þú getur aðeins breytt eiginleikanum ef hann var búinn til af skilgreiningarveitunni sem er virk eins og er. Þú getur búið til nýjan eiginleika með því að nota upprunalega eiginleikann sem grunn. Síðan getur þú gert nauðsynlegar breytingar eða sett upp færibreyturnar.

Þegar Microsoft eða annað fyrirtæki sem deilir altækum eiginleikum með fyrirtækinu þínu uppfærir eiginleika sem þú hefur flutt inn, er hægt að athuga með uppfærðar útgáfur með því að velja **Athuga eiginleikauppfærslur** í hlutanum **Tengdar stillingar** á vinnusvæðinu **Altækir eiginleikar**.

Ef þú sérð að það eru uppfærslur fyrir eiginleika sem þú notar sem sniðmát geturðu flutt inn nýja útgáfu eftir að þú samstillir lista yfir útgefna eiginleika í altæku geymslunni.
