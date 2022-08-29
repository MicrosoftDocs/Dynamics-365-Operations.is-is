---
title: Skilgreina einkunnir og umsagnir
description: Þessi grein lýsir því hvernig á að stilla e-Commerce síðuna þína til að sýna einkunnir viðskiptavina og umsagnir í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 27b1beddd474a2ca4db73f8e344b2d85934c43b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276866"
---
# <a name="configure-ratings-and-reviews"></a>Skilgreina einkunnir og umsagnir

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla e-Commerce síðuna þína til að sýna einkunnir viðskiptavina og umsagnir í Microsoft Dynamics 365 Commerce.

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

![Skilgreining svæðis til að sýna einkunnir og umsagnir.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Tengja vörueinkunn við umsagnarhlutann í PDP

Afurðaeinkunn er sýnd fyrir neðan afurðaheitið efst á PDP. Hægt er að stilla afurðaeinkunnina þannig að hún sé tengd við hlutann **Umsagnir** í sama PDP. 

Til að tengja vörueinkunn við hlutann **Umsagnir** í PDP fylgirðu þessum skrefum.

1. Opnaðu PDP-sniðmátið. 
1. Farðu í **Einingastillingar kaupkassagáma**.
1. Undir **Kaupkassi** velurðu **Afurðaeinkunn** og velur síðan gátreitinn **Tengja smellinn við fulla umsagnaeiningu**.

Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.

![Tenging afurðaeinkunnar við umsagnarhlutann í PDP.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Stilltu hlekkinn fyrir persónuverndar- og stefnusíðuna

Til að stilla hlekkinn fyrir persónuverndar- og stefnusíðuna skaltu fylgja þessum skrefum.

1. Fara til **Heim \> Svæði**.
1. Veldu heiti vefsvæðisins. 
1. Fara til **Vefstillingar \> Viðbætur**.
1. Á flipanum **Leiðir**, undir **Persónuvernd og stefna RNR**, velurðu **Bæta við tengli**. Ef tengill hefur þegar verið sleginn inn og þú vilt skipta um hann skaltu velja hann. 
1. Í valmyndinni **Bæta við tengli** velurðu tengilinn fyrir persónuverndar- og stefnusíðuna og velur síðan **Í lagi**. 
1. Veldur **Vista og birta**. 

Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.

![Stilling tengils fyrir persónuverndar- og stefnusíðuna.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Stilla einkunnir og endurskoða einingar á upplýsingasíðum

Sjá upplýsingar um stillingar á einkunna- og umsagnaeiningum á upplýsingasíðum afurða [Einkunna- og umsagnaeiningar](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Samstilla afurðaeinkunnir í Dynamics 365 Retail](sync-product-ratings.md)

[Virkja handvirka birtingu einkunna og umsagna hjá stjórnanda](manual-publish-rating-reviews.md)

[Flytja einkunnir og umsagnir inn og út](import-export-reviews.md)

[Stilla sannvottun milli þjónusta](service-to-service-auth.md)

[Algengar spurningar um einkunnir og umsagnir](ratings-reviews-faq.md)

[Einkunna- og umsagnaeiningar](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
