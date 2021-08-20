---
title: Magn fer yfir umframafhendingarprósentu við myndun fylgiseðils
description: Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu ofafhendingar.
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
ms.openlocfilehash: 00e3da7767b80e16f9351f59b109765bffc0128fe149cefafc1edda3a6cbcb96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781346"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Magn fer yfir umframafhendingarprósentu við myndun fylgiseðils

Villukóði SYS24920

## <a name="symptoms"></a>Einkenni

Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu ofafhendingar.

Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:

> Ofafhending línu er %1 prósent, en leyfileg ofafhending er aðeins %2 prósent.

Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.

## <a name="cause"></a>Orsök

Tiltektarmagn fyrir hleðsluna eða sendinguna er meira en pantað magn og er ekki innan marka fyrir prósentu ofafhendingar.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Stillið magn hleðslulínunnar.
- Stilla prósentu ofafhendingar.
- Bakfærið og gerið leiðréttingar.

### <a name="adjust-the-load-line-quantity"></a>Stilla magn hleðslulínunnar

Notið eftirfarandi ferli til að stilla magn farmlínu.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.
1. Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.
1. Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu ofafhendingar.
1. Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.
1. Í flipanum  **Línuupplýsingar** skal velja **Pöntun**.
1. Stillið reitinn **Magn** á tiltektarmagnið (þ.e. gildið í reitnum **Magn stofnaðs verks**) svo hægt sé að halda áfram með myndun fylgiseðils.

### <a name="adjust-the-over-delivery-percentage"></a>Stilla prósentu ofafhendingar

Notið eftirfarandi aðgerð til að stilla prósentu ofafhendingar.

1. Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.
1. Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.
1. Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna fyrir vöruna sem fer umfram prósentu ofafhendingar.
1. Í flipanum  **Línuupplýsingar** skal velja **Afhending**.
1. Stillið gildið í reitnum **Ofafhending** á hærri prósentu sem nær utan um magnið sem var tínt gagnvart hleðslumagninu, þannig að myndun fylgiseðils geti átt sér stað.

### <a name="reverse-and-make-adjustments"></a>Bakfæra og gera leiðréttingar

Bakfærið allt sem hefur verið bókað fyrir hleðsluna (til dæmis fylgiseðilinn, staðfestingu sendingar og vinnu), gerið leiðréttingar á sölupöntun, losið pöntunina aftur í vöruhúsið og ljúkið sendingarferlinu.

Notið eftirfarandi ferli til að hætta við fylgiseðil.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Hætta við fylgiseðla**.

Notið eftirfarandi ferli til að afturkalla staðfestingu sendingar.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.

Notið eftirfarandi ferli til að bakfæra vinnu.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Á aðgerðasvæðinu, í flipanum  **Hleðslur**, í flokknum  **Vinna**, skal velja  **Bakfæra vinnu**.
