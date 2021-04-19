---
title: Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti
description: Þetta efnisatriði lýsir því hvernig á að skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði rafrænna viðskipta.
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
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799806"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði rafrænna viðskipta.

Smásalar geta tekið við ýmsum gerðum af greiðslum í staðinn fyrir afurðir og þjónustu sem þeir selja í rás rafrænna viðskipta. Hver greiðslugerð sem smásali samþykkir verður að vera skilgreind í Microsoft Dynamics 365 Commerce þegar kerfið er sett upp. Greiðslumáti viðskiptavinalykils (eða „á lykli“) verður að vera studdur á B2B-svæðum rafrænna viðskipta. 

## <a name="prerequisites"></a>Forkröfur

1. Bætið greiðslumáta viðskiptavinalykils við Commerce Headquarters.
2. Tengið greiðslumáta viðskiptavinalykils við rás rafrænna viðskipta.
3. Gangið úr skugga um að **Leyfa á lykli** sé virkjað fyrir viðskiptavininn í **Smásala og viðskipti \> Viðskiptavinir \> Allir viðskiptavinir \> Sjálfgildi greiðslu** í Commerce Headquarters. Gangið einnig úr skugga um að færibreytur **Lánamarks** séu rétt stilltar fyrir viðskiptavininn í **Smásala og viðskipti \> Viðskiptavinir \> Allir viðskiptavinir \> Skuldir og innheimta** í Commerce Headquarters. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Virkja greiðslumáta fyrir viðskiptavinalykil í Commerce Site Builder 

Til að virkja greiðslumáta fyrir viðskiptavinalykil í Commerce Site Builder skal fylgja þessum skrefum.

1. Farið í **Svæðisstillingar \> Viðbætur**.
1. Stillið eiginleikann **Virkja greiðslur viðskiptavinalykils** á **Virkjað fyrir B2B-viðskiptavini**. 
1. Veldur **Vista og birta**.

> [!NOTE]
> Nýjar svæðisstillingar taka gildi aðeins eftir að búið er að uppfæra skrána app.settings.json. Frekari upplýsingar er að finna í [Uppfærslur á SDK og einingasafni](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Virkja greiðslumáta fyrir viðskiptavinalykil á greiðslusíðu fyrir B2B-svæði rafrænna viðskipta

Til að virkja greiðslumáta viðskiptavinalykils á greiðslusíðunni fyrir B2B-svæði rafrænna viðskipta skal fylgja þessum skrefum.

1. Í Commerce Site Builder skal finna og breyta greiðslusíðunni eða brotinu sem inniheldur greiðslueininguna fyrir B2B-svæði rafrænna viðskipta.
1. Í raufinni **Hólf greiðsluferlishluta** skal velja **Bæta við einingu** og síðan bæta við einingu **Greiðsla með viðskiptavinalykli**.
1. Staðsetjið eininguna **Greiðsla með viðskiptavinalykli** með því að velja úrfellingarmerkið (**...**) og veljið síðan **Færa upp** eða **Færa niður** eftir þörfum.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Staðfesta að greiðslumáti viðskiptavinalykils hafi verið virkjaður og gefin út

Til að staðfesta að greiðslumáti viðskiptavinalykils hafi verið gerður virkur skal fylgja þessum skrefum.

1. Skráðu þig inn á svæði rafrænna viðskipta.
1. Bætið afurð við körfuna.
1. Farið á síðu greiðsluferlis. Þar ætti að sjást nýi greiðslumáti **Viðskiptavinalykils**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2B-svæði fyrir rafræn viðskipti](set-up-b2b-site.md)

[Stofna líkanastigveldi fyrir B2B-fyrirtæki](org-model.md)

[Stjórna notendum viðskiptafélaga á B2B-svæði fyrir rafræn viðskipti](manage-b2b-users.md)

[Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði](quantity-limits.md)

[Uppfærslur á SDK og kjarnasafni](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]