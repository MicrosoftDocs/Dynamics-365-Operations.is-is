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
ms.openlocfilehash: 7cdc22eeabda6cf9f08484d698e5096f66af4a12
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920699"
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
1. Á **Sölupöntunarlínur** flipanum, veldu sölupöntunarlínuna fyrir vöruna sem fer yfir vanskilahlutfallið.
1. Á **Upplýsingar um línu** flipa, veldu **Afhending**.
1. Stillið gildið í reitnum **Vanafhending** á hærri prósentu sem nær utan um magnið sem var tínt gagnvart hleðslumagninu, þannig að myndun fylgiseðils geti átt sér stað.

### <a name="reverse-and-make-adjustments"></a>Bakfæra og gera leiðréttingar

Bakfærið allt sem hefur verið bókað fyrir hleðsluna (til dæmis fylgiseðilinn, staðfestingu sendingar og vinnu), gerið leiðréttingar á sölupöntun, losið pöntunina aftur í vöruhúsið og ljúkið sendingarferlinu.

Notið eftirfarandi ferli til að hætta við fylgiseðil.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Á aðgerðarrúðunni, á **Senda og taka á móti** flipa, í **Öfugt** hópur, veldu **Hætta við fylgiseðla**.

Notið eftirfarandi ferli til að afturkalla staðfestingu sendingar.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Á aðgerðarrúðunni, á **Senda og taka á móti** flipa, í **Öfugt** hópur, veldu **Staðfesting á öfugri sendingu**.

Notið eftirfarandi ferli til að bakfæra vinnu.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Á aðgerðarrúðunni, á **Álag** flipa, í **Vinna** hópur, veldu **Öfugt verk**.
