---
title: Eftirstöðvar efnislegs magns í einingunni má ekki vera núll
description: Þegar fylgiseðill er myndaður hafa gögnin sem fylgja honum birgðamagn sem er ekki núll heldur sölumagn sem er núll.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 187363db3030ee0741f0c7e7746295b88320162c156120112332bb78593bb673
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744655"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Eftirstöðvar efnislegs magns í einingunni má ekki vera núll

Villukóði SYS19591

## <a name="symptoms"></a>Einkenni

Þegar fylgiseðill er myndaður hafa gögnin sem fylgja honum birgðamagn sem er ekki núll heldur sölumagn sem er núll.

Þegar reynt er að búa til fylgiseðilinn sýnir kerfið eftirfarandi villuboð:

> Efnislegar eftirstöðvar í einingunni %1 verða að vera annað en núll.

Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.

## <a name="cause"></a>Orsök

Kerfið metur eftirstandandi efnislegt magn í birgðaeiningunni og eftirstandandi efnislegt magn í sendingareiningunni. Ef kerfið kemst að því að eftirstandandi magn í sendingareiningunni er 0 (núll), en eftirstandandi efnislegt magn í birgðaeiningunni er ekki 0, getur þú ekki búið til fylgiseðilinn. Þetta vandamál gæti til dæmis komið upp ef sölueining og birgðaeining fyrir vöruna eru frábrugðnar og umreikningur milli eininga er ekki nákvæmur.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.
- Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið á hreinlegan hátt án vandamála með sléttun.
- Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.
- Gangið úr skugga um að mælieining birgða sé minni en mælieining sölu.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi

Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.
1. Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.
1. Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið á hreinlegan hátt án vandamála með sléttun

Notið eftirfarandi aðferð til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að hægt sé að umreikna magnið á hreinlegan hátt án vandamála með sléttun

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.
1. Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.
1. Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram ofafhendingu.
1. Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.
1. Í flipanum  **Línuupplýsingar** skal velja **Pöntun**.
1. Stillið reitinn **Magn** á tiltektarmagnið (þ.e. gildið í reitnum **Magn stofnaðs verks**) svo hægt sé að halda áfram með myndun fylgiseðils.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni

Notið eftirfarandi aðferðir til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp. Gera skal athugasemd um gildið í reitunum **Magn** og **Eining**.
1. Farið í **Fyrirtækisstjórnun \> Einingar \> Einingar**.
1. Veljið eininguna sem ekki er hægt að búa til fylgiseðil fyrir.
1. Stillið gildið í reitnum **Nákvæmni aukastafa** eftir þörfum.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Gangið úr skugga um að mælieining birgða sé minni en mælieining sölu

Gangið úr skugga um að mælieining birgða sé minni en mælieining sölu. Íhugið að endurstilla mælieininguna fyrir vöruna eins og þarf.
