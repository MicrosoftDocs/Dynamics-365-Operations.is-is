---
title: Magn fer yfir undirafhendingarprósentu við myndun fylgiseðils
description: Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu undirafhendingar.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249116"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Magn fer yfir undirafhendingarprósentu við myndun fylgiseðils

Villukóði SYS24921

## <a name="symptoms"></a>Einkenni

Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu undirafhendingar.

Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:

> Vanafhending línu er %1 prósent, en leyfileg vanafhending er aðeins %2 prósent.

Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.

## <a name="cause"></a>Orsök

Tiltektarmagn fyrir hleðsluna eða sendinguna er minna en pantað magn og er ekki innan marka fyrir prósentu vanafhendingar.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Stillið prósentu vanafhendingar.
- Bakfærið og gerið leiðréttingar.

### <a name="adjust-the-under-delivery-percentage"></a>Stilla prósentu vanafhendingar

Notaðu eftirfarandi ferli til að stilla prósentu vanafhendingar.

1. Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.
1. Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.
1. Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna fyrir vöruna sem fer umfram prósentu vanafhendingar.
1. Í flipanum  **Línuupplýsingar** skal velja **Afhending**.
1. Stillið gildið í reitnum **Vanafhending** á hærri prósentu sem nær utan um magnið sem var tínt gagnvart hleðslumagninu, þannig að myndun fylgiseðils geti átt sér stað.

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
