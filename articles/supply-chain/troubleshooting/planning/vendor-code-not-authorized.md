---
title: Kóði lánardrottins er ekki heimilaður fyrir tiltekna afurð og dagsetningu
description: Þegar reynt er að staðfesta áætlaða pöntun eða bæta línu við innkaupapöntun berast villuboð þar sem kemur fram að kóði lánardrottins sé ekki heimilaður fyrir afurð og dagsetningu.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294104"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Kóði lánardrottins er ekki heimilaður fyrir tiltekna afurð og dagsetningu

Villukóði SYP4881415

## <a name="symptoms"></a>Einkenni

Þegar reynt er að fastsetja áætlaða pöntun eða bæta línu við innkaupapöntun koma upp eftirfarandi villuboð:

> Kóði lánardrottins %1 er ekki heimilaður fyrir %2 á %3.

## <a name="cause"></a>Orsök

Villa kemur upp vegna þess að reiturinn **Samþykkt prófunaraðferð lánadrottins** er stilltur á *Aðeins viðvörun* eða *Ekki leyfð* fyrir tilgreinda afurð og lánardrottinn hefur ekki leyfi til að útvega þessa afurð sem stendur.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál skal annaðhvort slökkva á athugun lánardrottins fyrir viðeigandi afurð eða samþykkja lánardrottin.

Til að slökkva á athugun lánardrottins fyrir afurð skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Viðeigandi vara er opnuð.
1. Í flýtiflipanum **Innkaup** skal stilla reitinn **Samþykkt prófunaraðferð lánadrottins** á annað gildi en *Aðeins viðvörun* eða *Ekki leyfð*.

Til að samþykkja lánardrottinn fyrir vöru skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opnið viðeigandi vöru.
1. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Samþykktur lánardrottinn**, skal velja **Uppsetning**.
1. Á listasíðunni **Samþykktur lánardrottinn** skal bæta línu við hnitanetið og stilla eftirfarandi gildi fyrir hana:

    - **Lánardrottinn** – Veljið lánardrottin til að samþykkja fyrir núverandi afurð.
    - **Gildisdagsetning** – Veljið fyrstu dagsetninguna sem lánardrottinn er samþykktur fyrir.
    - **Lokadagsetning** – Veljið síðustu dagsetninguna sem lánardrottinn er samþykktur fyrir.

Frekari upplýsingar er að finna í [Samþykkja lánardrottna fyrir tilteknar afurðir](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
