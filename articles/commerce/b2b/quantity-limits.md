---
title: Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði
description: Þetta efnisatriði lýsir hvernig á að stilla takmörk afurðarmagns fyrir B2B-vefsvæði rafrænna viðskipta.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799782"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stilla takmörk afurðarmagns fyrir B2B-vefsvæði rafrænna viðskipta.

Flestar afurðir eru með mælieiningu sem skilgreinir flokkun þeirra. Flokkunin hefur áhrif á það hvernig hægt er að selja afurðirnar. Sumar afurðir gætu verið með viðbótarflokkun fyrir magn. Þessi flokkun ákvarðar hvort hægt er að selja afurðirnar sem stakar einingar eða margar og hvort það er lágmark eða hámark á pöntunarmagni sem þarf að fylgja eftir.

Eiginleikinn fyrir takmörkun á magni tryggir að lágmarks- eða hámarksmagn, margar afurðir eða staðlað magn sem er skilgreint í Microsoft Dynamics 365 Commerce (í sjálfgefnum pöntunarstillingum eða í svæðisstillingum Commerce-vefsmiðs) verði notað í pöntunum viðskiptavina sem eru gerðar á svæði fyrir rafræn viðskipti. Takmörk afurðarmagns eru ekki studd sem stendur fyrir sölustað og símaver.

Margir smásalar bjóða upp á valkost viðskiptavinapantana (einnig þekkt sem sérpantanir) til að mæta ýmsum þörfum afurða og uppfyllingar. Hér eru nokkrar dæmigerðar aðstæður.

- Viðskiptavinur vill að afurðir af tilteknum afbrigðum verði seldar nokkrar í einu.
- Viðskiptavinur vill taka til afurðir úr verslun eða staðsetningu sem er önnur en verslunin eða staðsetningin þar sem viðskiptamaðurinn keypti þær afurðir. Hins vegar eru pökkunarstaðlar fyrir verslanirnar ólíkir pökkunarstöðlum söludreifingar á netinu.
- Viðskiptavinur vill kaupa afurð í takmörkuðu upplagi sem er með hámarksmagn fyrir vörur sem má kaupa.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Kveikja á eiginleika sjálfgefinna pöntunarstillinga í Commerce Headquarters

Áður en hægt er að stilla takmarkanir á afurðarmagni þarf að kveikja á eiginleika sjálfgefinna pöntunarstillinga í Commerce Headquarters.

Til að kveikja á eiginleika sjálfgefinna pöntunarstillinga skal fylgja þessum skrefum.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Finnið og veljið eiginleikann **Styðja svæðisstillingar og sjálfgefnar pöntunarstillingar í pöntun viðskiptavinar**.
1. Neðst í glugganum hægra megin skal velja **Virkja núna**. 

## <a name="define-quantity-settings"></a>Skilgreina magnstillingar 

Hægt er að skilgreina magnstillingar á síðunni **Sjálfgefnar pöntunarstillingar**.

Til að skilgreina magnstillingar skal fylgja þessum skrefum. 

1. Farið í **Smásala og viðskipti \> Afurðir og tegundir \> Losaðar afurðir eftir flokki**.
1. Veljið útgefna afurð.
1. Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar**. 
1. Á síðunni **Sjálfgefnar pöntunarstillingar**, í flýtiflipanum **Sölupöntun**, í hlutanum **Sölumagn**, skal stilla sölumagn afurðar:

    - **Margfeldi** – Magnið sem hægt er að kaupa afurðina í margfeldi af.
    - **Lágmarksmagn pöntunar** – Lágmarksfjöldi afurða sem þarf að kaupa.
    - **Hámarksmagn pöntunar** – Hámarksfjöldi afurða sem hægt er að kaupa.
    - **Staðlað pöntunarmagn** – Sjálfgefið magn sem sjálfkrafa er fært inn þegar afurðin er valin.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Kveikja á eiginleika fyrir takmörk B2B-pöntunarmagns í Commerce-vefsmið

Til að kveikja á eiginleika fyrir takmörk B2B-pöntunarmagns í Commerce-vefsmið skal fylgja þessum skrefum.

1. Farið í **Svæðisstillingar \> Viðbætur**
1. Undir **Virkja takmörk pöntunarmagns** skal velja **Virkjað fyrir B2B-viðskiptavini** í fellivalmyndinni. 

> [!NOTE] 
> Uppfærðar stillingar vefsmiðs taka fyrst gildi eftir að skráin app.settings.json hefur verið uppfærð. Frekari upplýsingar er að finna í [Uppfærslur á SDK og einingasafni](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2B-svæði fyrir rafræn viðskipti](set-up-b2b-site.md)

[Stofna líkanastigveldi fyrir B2B-fyrirtæki](org-model.md)

[Stjórna notendum viðskiptafélaga á B2B svæði fyrir rafræn viðskipti](manage-b2b-users.md)

[Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]