---
title: Vinna með skilgreiningar
description: Í þessari grein er að finna yfirlit yfir helstu aðstæður til að vinna með skilgreiningar rafrænnar skýrslugerðar af vinnusvæði altækra eiginleika.
author: gionoder
ms.date: 01/26/2022
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
ms.openlocfilehash: d87559405d2490c314eb2c8b88268af0dc0dfaca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283056"
---
# <a name="work-with-configurations"></a>Vinna með skilgreiningar

[!include [banner](../includes/banner.md)]

Skilgreiningar rafrænnar skýrslugerðar eru einn helsti þátturinn í eiginleikum rafrænnar reikningsfærslu. Skilgreining rafrænnar skýrslugerðar inniheldur uppsetninguna á skráarskipulagi og safn af umbreytingarreglum fyrir umbreytingu gagna á tvennan hátt:

- **Flytja út skilgreiningu rafræns skýrslugerðarsniðs** – Þessi skilgreining umbreytir gögnum úr sameinuðu innra skipulagi (líkan rafrænnar skýrslugerðar) í rafrænt skráarsnið.
- **Flytja inn skilgreiningu rafræns skýrslugerðarsniðs** – Þessi skilgreining umbreytir gögnum úr rafrænu skýrslugerðarsniðið í sameinað innra skipulag (líkan rafrænnar skýrslugerðar).

Auk þess að búa til rafrænar skrár á útleið í fyrirfram skilgreindu sniði eru skilgreiningar rafrænnar skýrslugerðar notaðar víða til að þátta skeyti á innleið úr ytri vefþjónustum sem svör. Þessi virkni hjálpar til við að byggja upp stillanleg rök til að fá niðurstöður samskipta með ytri rásum, umbreyta þessum niðurstöðum (kóðum, skeytum og klöddum) í skipulag sem er læsilegt notendum og síðan flytja þessar upplýsingar yfir í biðlaraforritið.

Til að byrja að nota skilgreiningar rafrænnar skýrslugerðar í eiginleika rafrænnar reikningsfærslu þarf að tengja þær við eiginleikann og gera þær aðgengilegar í flipanum **Skilgreiningar** fyrir núverandi eiginleikaútgáfu. Hægt er að vinna með tengda skilgreiningu rafrænnar skýrslugerðar með því að velja **Bæta við**, **Eyða**, **Breyta** eða **Skoða**.

Áður en hægt er að bæta tengli við skilgreiningu rafrænnar skýrslugerðar þarf skilgreiningin að vera til í gagnageymslu Regulatory Configuration Service (RCS). Fylgdu eftirfarandi skrefum til að fara yfir ER stillingarnar sem eru tiltækar í RCS-geymslunni þinni.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Í vinnusvæðinu **Rafræn skýrslugerð**, í kaflanum **Skilgreiningar** velurðu reitinn **Skilgreiningar skýrslugerðar**.

Upplýsingar um hvernig á að búa til nýja skilgreiningu rafrænnar skýrslugerðar eða flytja inn núverandi skilgreiningu rafrænnar skýrslugerðar úr gagnageymslunni er að finna í [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Til að breyta tengdri skilgreiningu rafrænnar skýrslugerðar skal velja **Breyta** í flipanum **Skilgreiningar** fyrir núverandi eiginleika rafrænnar reikningsfærslu. Kerfið býr sjálfkrafa til útgáfu af skilgreiningu rafrænnar skýrslugerðar. Ef núverandi útgáfa var ekki búin til af virkri skilgreiningarveitu býr kerfið til afleidda útgáfu sem notar skilgreiningarveituna þína. Ef núverandi útgáfa var búin til af virkri skilgreiningarveitu býr kerfið til nýja útgáfu. Í báðum tilvikum er hægt að breyta útgáfunni sem er búin til og síðan gera sjálfkrafa allar nauðsynlegar uppfærslur.
