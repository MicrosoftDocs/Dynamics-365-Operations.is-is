---
title: Úthlutun tíma á vinnslur í vinnslubúnti
description: Í Framkvæmd framleiðslu er hægt að sameina vinnslur. Þá er hægt að hefja margar vinnslur á sama tíma á listasíðunni Vinnslur.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fbc81de8ba59f0782bd9af5b50bfcf45d5621a
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193046"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Úthlutun tíma á vinnslur í vinnslubúnti

[!include [banner](../includes/banner.md)]

Í Framkvæmd framleiðslu er hægt að sameina vinnslur. Þá er hægt að hefja margar vinnslur á sama tíma á listasíðunni Vinnslur.

Ef vinnslur eru sameinaðar verður að skilgreina hvernig skráðum heildartíma fyrir allar vinnslur skal úthlutað á hverja vinnslu. Úthlutunin er skilgreind með því að velja einn af eftirfarandi valkostum í reitnum **Gerð búnts** á síðunni **Úthlutunarlyklar**:

-   **Mat** – Tíma er skipt á milli vinnsla samkvæmt áætluðum tíma vinnslunnar.
-   **Vinnslur** – Tíma er skipt samkvæmt samtölu vinnsla sem eru í búnti og hversu miklum tíma var eytt í að ljúka öllum vinnslunum.
-   **Nettótími** – Tíma er skipt jafnt á milli vinnslanna sem eru í búnti á hverjum tíma.
-   **Rauntíma** – Raunvinnslutíma er úthlutað. Hægt er að reikna kostnað á grundvelli raunverulegs launakostnaðar. **Ábending:** Úthlutunarlykillinn **Rauntími** er aðeins tiltækur ef fyrirtækið notar launaeiginleika í Tíma og viðveru.

Eftirfarandi dæmi sýna niðurstöður mismunandi úthlutunarlykla.

## <a name="example-scenario"></a>Dæmi
Ljúka þarf þremur vinnslum í vinnsluröðinni. Fyrsta vinnslan er hafin og á meðan hún er í gangi eru vinnslur tvö og þrjú ræstar svo að þrjár vinnslur verða sameinaðar. Þannig eru þrjár vinnslur sameinaðar í búnt. Eftirfarandi tafla sýnir áætlaðan framleiðslutíma fyrir hverja vinnslu.

| Vinnsla   | Tími framleiðslu |
|-------|-----------------|
| Vinnsla 1 | 1 klukkustund          |
| Vinnsla 2 | 3 stundir         |
| Vinnsla 3 | 4 stundir         |
| Samtals | 8 stundir         |

Eftirfarandi tafla sýnir raunverulegar vinnustundir sem er eytt í hverja vinnslu.

| Vinnsla    | Upphafstími | Lokatími | Sameinaður tími |
|--------|------------|----------|-------------|
| Vinnsla 1  | 09:00      | 11:00:00    | 2 stundir     |
| Vinnsla 2  | 10:00      | 13:00:00    | 3 stundir     |
| Vinnsla 3  | 10:00      | 15:00    | 5 klukkustundir     |
| Búnt | 09:00      | 15:00    | 6 stundir     |

Eftirfarandi kaflar lýsa niðurstöðum fyrir reiknaðan tíma fyrir hvern úthlutunarlykil.

## <a name="estimation-allocation-key"></a>Úthlutunarlykillinn Mat
Eftirfarandi tafla sýnir formúluna til að reikna út úthlutaðan tíma. Hér er formúlan: Tími á hverja vinnslu = Búnt-tími samtals x (Áætlaður vinnslutími ÷ Áætlaður heildartími)

| Vinnsla   | Formúla           | Úthlutaður tími |
|-------|-------------------|----------------|
| Vinnsla 1 | 6 × (1 ÷ 8) klst. | 0,75 klukkustundir      |
| Vinnsla 2 | 6 × (3 ÷ 8) klst. | 2,25 klukkustundir     |
| Vinnsla 3 | 6 × (4 ÷ 8) klst. | 3,00 klukkustundir     |

## <a name="jobs-allocation-key"></a>Úthlutunarlykillinn Vinnslur
Eftirfarandi tafla sýnir formúluna til að reikna út úthlutaðan tíma. Hér er formúlan: Tími á hverja vinnslu = Búnt-tími samtals ÷ Fjöldi vinnsla

| Vinnsla   | Formúla | Úthlutaður tími |
|-------|---------|----------------|
| Vinnsla 1 | 6 ÷ 3   | 2 stundir        |
| Vinnsla 2 | 6 ÷ 3   | 2 stundir        |
| Vinnsla 3 | 6 ÷ 3   | 2 stundir        |

## <a name="net-time-allocation-key"></a>Úthlutunarlykillinn Nettó-tími
Eftirfarandi tafla sýnir formúluna til að reikna út úthlutaðan tíma. Hér er formúlan: Tími á hverja skýrslu = Búnt-tími samtals ÷ Fjöldi vinnsla

| Dæmi                       | 09:00–10:00 (1 klst.) | 10:00–11:00 (1 klst.) | 11:00–13:00 (2 klst.) | 13:00–15:00 (2 klst.) | Úthlutaður tími |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Fjöldi vinnsla í búntinu. | 1                    | 3                    | 2                     | 1                     | Ekki tiltækt |
| Vinnsla 1                        | 1 ÷ 1 = 1 klst.       | 1 ÷ 3 = 0,33 klst.    | Ekki tiltækt        | Ekki tiltækt        | 1,33 klukkustundir     |
| Vinnsla 2                        | Ekki tiltækt       | 1 ÷ 3 = 0,33 klst.    | 2 ÷ 2 = 1 klst.        | Ekki tiltækt        | 1,33 klukkustundir     |
| Vinnsla 3                        | Ekki tiltækt       | 1 ÷ 3 = 0,33 klst.    | 2 ÷ 2 = 1 klst.        | 2 ÷ 1 = 2 klst.       | 3,33 klukkustundir     |

## <a name="real-time-allocation-key"></a>Úthlutunarlykill rauntíma
Ef óskað er eftir að reikna út framleiðslukostnað samkvæmt raunkostnaði, verður að hreinsa valkostinn **Kostnaðartegund** á síðunni **Sjálfgildi innkaupapöntunar framleiðslu**. Eftirfarandi tafla sýnir formúluna til að reikna út úthlutaðan tíma. Hér er formúlan: Rauntími á hverja vinnslu = Rauntími á búnt

| Vinnsla   | Raunverulegur tími |
|-------|-------------|
| Vinnsla 1 | 2 stundir     |
| Vinnsla 2 | 3 stundir     |
| Vinnsla 3 | 5 klukkustundir     |

Íhugið að vinnslurnar þrjár eru framkvæmdar af starfsmanni með tímakaupið 12,00 USD. Engin yfirvinna eða kaupauki fékkst fyrir tímann sem varið var í vinnslurnar. Starfsmaðurinn hefur unnið í samtals sex klukkustundir við þessar þrjár sameinuðu vinnslur. Þess vegna er launakostnaðurinn 6 × USD 12,00 = USD 72,00. Þegar úthlutunarlykill rauntíma er notaður er kostnaður á hverja klukkustund endurreiknaður með stuðlinum úr formúlunni Nettótími. Raunverulegur tími sem var varið í hverja vinnslu er síðan fluttur en með leiðrétt kostnaðarverð á klukkustund. Í dæminu er sex klukkustundum eytt þó svo að 10 klukkustundum sé úthlutað. Eftirfarandi tafla sýnir formúluna til að reikna út kostnað. Hér er formúlan: Kostnaður á klukkustund = (Búnt-tími samtals á hverja vinnslu (Nettótími)) x Staðlað kostnaðarverð á klukkustund

| Vinnsla   | Útreikningar á leiðréttum kostnaði á klukkustund | Leiðréttur kostnaður á klukkustund | Úthlutaður tími | Heildarkostnaður vinnslu |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Vinnsla 1 | (1,33 ÷ 2) × USD 12,00                 | USD 8,00                | 2 stundir        | USD 16,00         |
| Vinnsla 2 | (1,33 ÷ 3) × USD 12,00                 | USD 5,33                | 3 stundir        | USD 16,00         |
| Vinnsla 3 | (3,33 ÷ 5) × USD 12,00                 | USD 8,00                | 5 klukkustundir        | USD 40,00         |

Leiðréttur kostnaður á klukkustund og vinnslutíminn eru bókaðir í framleiðslubókina. **Ábending:** Ef valinn valkosturinn **Kostnaðartegund** á flipanum **Almennt** á síðunni **Sjálfgildi framleiðslupöntunar** er rauntími hverrar vinnslu fluttur í framleiðslubók, þar sem kostnaði er beitt á kostnaðartegund tilgreindrar vinnslu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]