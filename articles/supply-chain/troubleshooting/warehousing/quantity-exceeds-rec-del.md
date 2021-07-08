---
title: Magnið sem reynt er að uppfæra er meira en móttekið/afhent magn.
description: Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram vinnumagnið sem var tínt og tekið frá fyrir sölupöntunina.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249121"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Magnið sem reynt er að uppfæra er meira en móttekið/afhent magn

Villukóði SYS7676

## <a name="symptoms"></a>Einkenni

Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram vinnumagnið sem var tínt og tekið frá fyrir sölupöntunina.

Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:

> Magnið sem reynt var að uppfæra er meira en móttekið/afhent magn.

Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.

## <a name="cause"></a>Orsök

Tiltekið vinnumagn passar ekki við vinnumagn sem var búið til á farmlínunni. Þetta vandamál gæti til dæmis komið upp ef magn hleðslulínu, magn vinnu sem er búin til eða tiltektarmagn er ekki nákvæmt.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.
- Stillið magn hleðslulínunnar.
- Bakfærið allar tiltektarskráningar og endurtakið tiltekt.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi

Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að mynda sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.
1. Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.
1. Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.

### <a name="adjust-the-load-line-quantity"></a>Stilla magn hleðslulínunnar

Notið eftirfarandi ferli til að stilla magn farmlínu.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.
1. Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.
1. Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.
1. Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.
1. Stillið reitinn **Minnka hleðslulínu** til að endurspegla leiðréttingar á hleðslulínunni.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Bakfæra allar tiltektarskráningar og endurtaka tiltekt

Ef einhver notaði tiltektarskráningu til að loka hleðslulínu án vinnu getur misræmi komið upp milli magns hleðslulínunnar og tiltektarmagnsins. Í þessu tilviki þarf að bakfæra handvirka skráningu tiltektar og síðan þarf að ljúka tiltekt með farsímaforriti Warehouse Management.

Notið eftirfarandi ferli til að bakfæra skráningu tiltektar.

1. Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.
1. Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.
1. Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna sem skráning tiltektar var gerð fyrir.
1. Veljið **Uppfæra línu \> Tiltekt** til að afturkalla tiltekt á vörunum.
