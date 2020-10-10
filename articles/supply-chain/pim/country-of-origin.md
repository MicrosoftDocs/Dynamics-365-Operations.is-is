---
title: Upprunaland
description: Mörg fyrirtæki gefa út vottorð til lánardrottna sinna til að tryggja að afurðir uppfylli tiltekna vottunarstaðla. Þessi vottorð eru oft háð upprunalandi. Í þessu efnisatriði er að finna upplýsingar um eiginleika upprunalands, sem gerir þér kleift að tengja afurð við upprunaland hennar og fylgjast með afurðarvottorðum þess.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895549"
---
# <a name="country-of-origin"></a>Upprunaland

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mörg fyrirtæki gefa út vottorð til lánardrottna sinna til að tryggja að afurðir uppfylli tiltekna vottunarstaðla. Þessi vottorð eru oft háð upprunalandi. Eiginleiki upprunalands gerir þér kleift að tengja afurð við upprunaland hennar og fylgjast með afurðarvottorðum þess.

## <a name="turn-on-the-country-of-origin-feature"></a>Kveikja á eiginleika upprunalands

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Afurðaupplýsingastjórnun*
- **Heiti eiginleika:** *Stjórnunareiginleiki fyrir upprunaland*

## <a name="configure-source-and-destination-countries"></a>Skilgreina uppruna- og viðtökuland

Áður en hægt er að gefa út vottorð fyrir afurð verður að tengja afurðina við viðtökuland og upprunaland hennar.

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðasamræmi \> Upprunaland \> Reglur upprunalands**.
2. Veldu fyrirliggjandi uppsetningu lands til að breyta henni, eða **Ný** á aðgerðasvæðinu til að búa til nýja uppsetning lands.
3. Stilltu eftirfarandi gildi fyrir valda landið eða nýtt land.

    | Svæði | lýsing |
    |---|---|
    | Vörunúmer | Veldu vörunúmer Afurðarinnar. |
    | Áfangaland | Veldu landið sem þú ert að senda afurðina til. |
    | Upprunaland | Veljið landið sem á að afhenda afurðina frá. |

Tilgangur þessarar uppsetningar er að auðvelda skýrslumyndun uppskriftar þar sem hægt er að hafa með upprunaland fyrir hvern hluta sem uppruna- og viðtökuland eru tilgreind fyrir. Þessi skýrsla veitir heildstæðari mynd af því hvaðan hlutirnir koma og hvert þeir eru að fara.

## <a name="keep-track-of-vendor-certificates"></a>Fylgstu með vottorðum lánardrottna

Hægt er að nota síðuna **Vottorð lánardrottins um upprunaland** til að fylgjast með vottorðum sem gefin er út til lánardrottna.

Þú verður að ákveða hvaða vottorðsskjöl þú ert að gefa út og hvernig þú munt skrá þau til viðskiptavina. Þessi eiginleiki hjálpar til við að fylgjast með vottorðum. Hann gerir þér einnig kleift að velja hvort viðeigandi vottorðanúmer komi fram á reikningum, fylgiseðlum og/eða pöntunarstaðfestingum.

Til að setja upp upplýsingar um vottorð skal fylgja þessum skrefum.

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðasamræmi \> Upprunaland \> Vottorð lánardrottins um upprunaland**.
2. Veljið fyrirliggjandi uppsetningu vottorðs til að breyta henni, eða veljið **Nýtt** á aðgerðasvæðinu til að búa til nýja uppsetningu vottorðs.
3. Stilltu eftirfarandi stillingar fyrir valda vottorðið eða nýtt vottorð.

    | Svæði | lýsing |
    |---|---|
    | Lykill lánardrottins | Veljið lánardrottininn sem vottorð var gefið út fyrir. |
    | Vörunúmer | Veljið vöruna sem vottorðið var gefið út fyrir. |
    | Land/svæði | Viðtökuland eða svæði þar sem þú verður að nota þetta vottorð. |
    | Númer vottorðs | Sláðu inn auðkennisnúmer vottorðsins sem var gefið út. |
    | Virkt | Veljið fyrstu dagsetningu þegar núgildandi vottorð er gilt.|
    | Lok gildistíma | Veljið síðustu dagsetningu þegar núgildandi vottorð er gilt. |
    | Prenta á reikning | Veljið þennan gátreit til að prenta númer vottorðs á reikningunum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils. |
    | Prenta á fylgiseðil | Veljið þennan gátreit til að prenta númer vottorðs á fylgiseðlum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils. |
    | Prenta á sölupöntun | Veljið þennan gátreit til að prenta númer vottorðs á sölupöntunum sem eru stílaðar á tiltekið land innan tiltekins dagsetningabils. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Láta upprunaland fylgja með í skýrslum uppskrifta

Þegar skýrsla uppskriftar er búin til er hægt að láta upprunaland fylgja með fyrir hvern hlut sem uppruna- og viðtökuland eru tilgreind fyrir á síðunni **Reglur upprunalands**.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið eða stofnið afurð til að opna síðuna **Upplýsingar um losaðar afurðir**.
1. Á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Uppskrift**, skal velja **Hönnuður**.
1. Á síðunni sem birtist, á Aðgerðasvæðinu skal smellt á **Uppskrift \> Prenta**.
1. Í svarglugganum **Uppskriftalínur** skal stilla reitinn **Viðtökuland** á viðtökulandið sem á að koma fram í skýrslunni.
1. Veljið **Í lagi**.

Skýrsla sem sýnir upplýsingar um upprunaland hvers hluta er búin til og sýnd. Hér er dæmi um skýrsluna.

![Skýrsla upprunalands](media/country-of-origin-report.png "Skýrsla upprunalands")
