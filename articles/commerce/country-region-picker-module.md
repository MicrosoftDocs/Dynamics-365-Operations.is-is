---
title: Eining lands-/svæðisvals
description: Þetta efnisatriði fjallar um einingu lands-/svæðisvals og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 3134e10c096525ec2d82365a25eff16a3c5d5e11
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472627"
---
# <a name="countryregion-picker-module"></a>Eining lands-/svæðisvals

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um einingu lands-/svæðisvals og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.

Eining lands-/svæðisvals notar eiginleikann [landfræðileg greining og áframsending](geo-detection-redirection.md) í Dynamics 365 Commerce til að sýna viðskiptavinum ráðlagðar vefslóðir sem óska eftir vefslóð fyrir rafrænt viðskiptasvæði sem tengist ekki landinu eða svæðinu þeirra.

Viðskiptavinur í Kanada óskar til dæmis eftir vefslóð fyrir vefsvæði sem tengist ekki Kanada. Í þessu tilviki sýnir eining lands-/svæðisvals svarglugga sem ráðleggur vefslóðir vefsvæða sem tengjast Kanada. Eftirfarandi mynd sýnir dæmi um svarglugga lands-/svæðisvals.

![Dæmi um svarglugga lands-/svæðisvals á heimasíðu.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Eiginleikar einingar lands-/svæðisvals

| Nafn eiginleika              | Virði       | lýsing |
| -------------------------- | ----------- | ----------- |
| Haus                    | Texti        | Fyrirsögnin sem birtist efst í svarglugganum. |
| Undirfyrirsögn                 | Texti        | Undirfyrirsögnin sem birtist fyrir neðan fyrirsögnina. |
| Land: birtingarstrengur    | Texti        | Birtingarheiti fyrir valkost vefslóðar (til dæmis „Kanada“). |
| Land: undirstrengur birtingar | Texti        | Valkvæmur undirstrengur sem birtist fyrir valkost vefslóðar (til dæmis „enska“ eða „franska“). |
| Land: Landsmynd     | Eign geymslumiðils | Valfrjáls mynd sem tengist valkosti vefslóðar (til dæmis mynd af kanadíska fánanum). |
| Land: vefslóð lands       | Texti        | Vefslóðin sem samsvarar rásinni og landsstaðlinum sem er stillt fyrir landið eða svæðið á síðunni **Rásir** í vefsmið Commerce (**Stillingar vefsvæðis \> Rásir**). Þessi vefslóð verður að passa nákvæmlega við vefslóðina sem er stillt á síðunni **Rásir**. |
| Aðgerðartengill                | Aðgerðartengill | Valfrjáls tengill sem birtist neðst í svarglugganum. Þessi tengill getur til dæmis bent á innri síðu þar sem er að finna lista yfir öll lönd og svæði sem vefsvæðið styður. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Bæta einingu lands-/svæðisvals við síðu

Hægt er að bæta einingu lands-/svæðisvals við hausaeininguna annaðhvort beint eða í gegnum samnýtt síðubrot. Frekari upplýsingar um hausaeiningar er að finna í [Hausaeining](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Stilla einingu lands-/svæðisvals í vefsmið Commerce

> [!NOTE]
> Vefslóðir sem þú mælir með fyrir viðskiptavini þína verða að vera stilltar sem hlutar lands í einingu lands-/svæðisvals.

Fyrir hverja vefslóð sem þú vilt sýna og mæla með fyrir viðskiptavini skaltu fylgja þessum skrefum í vefsmið Commerce.

1. Veldu hólfaeiningu lands-/svæðisvals.
1. Á eiginleikasvæðinu undir **Landalisti** skal velja **Bæta við landi**.
1. Velja nýja **Land** reitinn.
1. Í reitinn **Birta streng** skal færa inn birtingarnafn (til dæmis **Kanada**).
1. Valfrjálst: Í reitinn **Birta undirstreng** skal færa inn undirstreng (til dæmis **franskur** eða **fr-ca**).
1. Valfrjálst: Veldu mynd úr miðlasafninu.
1. Í reitinn **Vefslóð lands** er slegin inn slóðin. Þessi vefslóð verður að passa nákvæmlega við vefslóðina sem birtist á síðunni **Rásir** og er varpað í rásina, þ.m.t. landsstaðalinn sem tengist landinu eða svæðinu.
1. Veldu **Í lagi**.
1. Endurtaktu skrefin fyrir allar vefslóðir annarra landa sem þú vilt að eining lands-/svæðisvals sýni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp landfræðilega greiningu og áframsendingu](geo-detection-redirection.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining síðuhauss](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
