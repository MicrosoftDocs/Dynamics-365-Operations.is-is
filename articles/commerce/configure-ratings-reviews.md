---
title: Skilgreina einkunnir og umsagnir
description: Þetta efni lýsir því hvernig á að stilla netverslunarsíðuna þína til að sýna viðskiptavini mat og umsagnir í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071567"
---
# <a name="configure-ratings-and-reviews"></a>Skilgreina einkunnir og umsagnir

[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að stilla netverslunarsíðuna þína til að sýna viðskiptavini mat og umsagnir í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun með því að sýna þeim hvað öðrum viðskiptavinum finnst um þessar vörur. Fyrir vefsíður í netverslun eru einkunnir og umsagnir einnig búnaður til að safna endurgjöf viðskiptavina um vörur. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Skilgreina svæði til að sýna einkunnir og umsagnir

Stillingargildi fyrir einkunnir og umsagnir, svo sem auðkenni leigjanda, lengd textatexta og lengd endurskoðunar titils, eru stillt á vefsvæðisstig. 

Fylgdu þessum skrefum til að stilla vefsíðu til að sýna einkunnir og umsagnir. 

1. Fara til **Heim \> Svæði**.
1. Veldu heiti vefsvæðisins. 
1. Fara til **Vefstillingar \> Viðbætur**. 
1. Í reitinn **Hámarkstextalengd umsagnar** slærðu inn hámarksfjölda stafa sem umsagnartexti getur haft (t.d. **1000**). 
1. Í reitinn **Hámarkstitillengd umsagnar** slærðu inn hámarksfjölda stafa sem umsagnartitill getur haft (t.d. **55**). 
1. Veldur **Vista og birta**. 

Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.

![Skilgreining svæðis til að sýna einkunnir og umsagnir](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Tengja vörueinkunn við umsagnarhlutann í PDP

Afurðaeinkunn er sýnd fyrir neðan afurðaheitið efst á PDP. Hægt er að stilla afurðaeinkunnina þannig að hún sé tengd við hlutann **Umsagnir** í sama PDP. 

Til að tengja vörueinkunn við hlutann **Umsagnir** í PDP fylgirðu þessum skrefum.

1. Opnaðu PDP-sniðmátið. 
1. Farðu í **Einingastillingar kaupkassagáma**.
1. Undir **Kaupkassi** velurðu **Afurðaeinkunn** og velur síðan gátreitinn **Tengja smellinn við fulla umsagnaeiningu**.

Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.

![Tenging afurðaeinkunnar við umsagnarhlutann í PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Stilltu hlekkinn fyrir persónuverndar- og stefnusíðuna

Til að stilla hlekkinn fyrir persónuverndar- og stefnusíðuna skaltu fylgja þessum skrefum.

1. Fara til **Heim \> Svæði**.
1. Veldu heiti vefsvæðisins. 
1. Fara til **Vefstillingar \> Viðbætur**.
1. Á flipanum **Leiðir**, undir **Persónuvernd og stefna RNR**, velurðu **Bæta við tengli**. Ef tengill hefur þegar verið sleginn inn og þú vilt skipta um hann skaltu velja hann. 
1. Í valmyndinni **Bæta við tengli** velurðu tengilinn fyrir persónuverndar- og stefnusíðuna og velur síðan **Í lagi**. 
1. Veldur **Vista og birta**. 

Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.

![Stilling tengils fyrir persónuverndar- og stefnusíðuna](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Stilla einkunnir og endurskoða einingar á upplýsingasíðum

Sjá upplýsingar um stillingar á einkunna- og umsagnaeiningum á upplýsingasíðum afurða [Einkunna- og umsagnaeiningar](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Stilla einkunnir og endurskoða einingar á upplýsingasíðum](ratings-reviews-modules.md)

[Samstilla afurðaeinkunnir í Dynamics 365 Retail](sync-product-ratings.md)
