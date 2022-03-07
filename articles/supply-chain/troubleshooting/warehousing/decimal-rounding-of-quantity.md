---
title: Sléttun aukastafa á uppfærslu efnislegs magns er röng
description: Þegar fylgiseðill er búinn til inniheldur hleðslan á útleið magn sem passar ekki við nákvæmni aukastafa sem er skilgreind í einingunni.
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
ms.openlocfilehash: ddfac7106eb0e8b934516ca10e3950891d10910a2ccdef1868faf25812243159
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726562"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Sléttun aukastafa á uppfærslu efnislegs magns er röng

Villukóði SYS19589

## <a name="symptoms"></a>Einkenni

Þegar fylgiseðill er búinn til inniheldur hleðslan á útleið magn sem passar ekki við nákvæmni aukastafa sem er skilgreind í einingunni.

Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:

> Sléttun aukastafa á efnislegu uppfærslumagni í einingu %1 er röng.

Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.

## <a name="cause"></a>Orsök

Kerfið metur hvort sléttun aukastafa á magni sendingar samsvari nákvæmni aukastafa sem er skilgreind fyrir sendingareininguna. Þegar kerfið sléttar magn sendingar í tiltekinn fjölda aukastafa, ef það finnur út að sléttað magn sendingar passar ekki við raunverulegt magn sendingar, er ekki hægt að búa til fylgiseðil. Þetta vandamál gæti til dæmis komið upp ef sölumagnið er 1,75 kíló (kg) en nákvæmni aukastafa er stillt á *1*.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið án aukastafa og annarra sléttunarvandamála.
- Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið án aukastafa og annarra sléttunarvandamála

Notið eftirfarandi leið til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að hægt sé að umreikna magnið án aukastafa og annarra sléttunarvandamála.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.
1. Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.
1. Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.
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
