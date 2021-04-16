---
title: Tengja eignir við leigu
description: Efnið útskýrir hvernig á að tengja fyrirliggjandi eign við nýja leigu.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e2261755d98ee38564b4b864daf8e79551d1239
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814081"
---
# <a name="associate-fixed-assets-with-leases"></a>Tengja eignir við leigu

[!include [banner](../includes/banner.md)]

Efnið útskýrir hvernig á að tengja fyrirliggjandi eign við nýja leigu. Þegar eign er tengd við leigu verður eignarvirði afnotaréttar af eign (ROU) við fyrstu viðurkenningu kaupverð eignarinnar.

Áður en hægt er að tengja eign við leigusamning þarf að stofna færslu fyrir eignina í „Eignir“. Á síðunni **Samantekt leigu** þarf að stofna leigusamning og tengja eignina við viðkomandi leigusamning.

1. Bætið við leigu með því að fylgja eftirfarandi skrefum í [Bæta við eða afrita leigusamninga](add-lease.md). Á síðunni **Bæta við leigusamningi**, í reitnum **Númer eignar** , skal velja eignina sem hefur ekki enn verið keypt.
2. Veljið **Bækur** og staðfestið greiðsluáætlunina.
3. Veljið **Upphafleg skráning**.
4. Veljið **Færslubækur eignarleigu**.

    Upphafleg bókarfærsla fyrir leigusamning debetfærir eignina fyrir þá upphæð sem venjulega er debetfærð á reikning ROU-eignar.

    Nú er hægt að skoða færslugerðina og bókina fyrir eignina.

5. Veljið **Færslubókarupplýsingar**.
6. Veljið **Línur** til að skoða stakar línur fyrir bókarfærsluna.
7. Veljið færslubókarlínuna sem inniheldur eignina og veljið svo flipann **Eignir**.

    Flipinn **Eignir** sýnir færslugerðina og bókina. Sjálfgefið er að reiturinn **færslugerð** sé stilltur á **kaup** og reiturinn **bók** sé stilltur á núverandi bók fyrir eignina.

Þegar búið er að bóka upphaflegu bókarfærsluna birtist færslan sem kaupfærsla fyrir eignina. Til að skoða færslutöflu skal fara á **Eignir \> Eignir \> Eignir**, velja viðeigandi eign og velja síðan **Mat**. Þú ættir að sjá að upphaflega bókarfærslan hafi stofnað kaupfærslu fyrir tilgreinda eign.

Nú er hægt að afskrifa eignina með því að nota staðlaða afskriftarvirkni í eignum. Frekari upplýsingar um afskriftir eru í [Afskriftaaðferðir og hefðir](../fixed-assets/depreciation-methods-conventions.md).

> [!NOTE]
> Ef eign er tengd við leigusamning eru hnapparnir **Afskrift eigna** og **Virðisrýrnun leigusamnings** óvirkir í eignarleigu. Hægt er að skoða færslur fyrir afskriftir eigna og virðisrýrnun leigusamninga úr eignum. Hnappurinn **Eignarfærslur**, sem opnar fyrirspurnarskjámynd er einnig gerður óvirkur. Einnig er hægt að opna **Eignarfærslur** fyrirspurnarskjámyndina í Eignir.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]