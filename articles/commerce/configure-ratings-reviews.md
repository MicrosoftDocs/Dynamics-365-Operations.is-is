---
title: Skilgreina einkunnir og umsagnir
description: Þetta efni lýsir því hvernig á að stilla netverslunarsíðuna þína til að sýna viðskiptavini mat og umsagnir í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770482"
---
# <a name="configure-ratings-and-reviews"></a>Skilgreina einkunnir og umsagnir

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að stilla netverslunarsíðuna þína til að sýna viðskiptavini mat og umsagnir í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun með því að sýna þeim hvað öðrum viðskiptavinum finnst um þessar vörur. Fyrir vefsíður í netverslun eru einkunnir og umsagnir einnig búnaður til að safna endurgjöf viðskiptavina um vörur. 

Einkunnir eru sýndar á vörulistasíðum, flokkalistasíðum, leitarniðurstöðusíðum og öðrum vefsíðum. Stuðlarit einkunna og afurðaumsagnir eru sýndar á upplýsingasíðum afurða (PDPs). Hnappurinn **Skrifa umsögn** gerir viðskiptavinum kleift að senda inn einkunnir og umsagnir um afurð.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Einkunna- og umsagnaeiningar á PDP 

Þrjár einingar sýna yfirlit yfir mat og yfirlit yfir PDP:

- Skrifa umsagnareiningu
- Eining umsagnalista afurðar
- Stuðlaritseining einkunna
 
Eftirfarandi mynd sýnir hvernig einkunnirnar og umsagnirnar líta út á PDP.

![Einkunna- og umsagnaeiningar á PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Fyrir upplýsingar um hvernig á að fínstilla PDP sniðmát og útlit svo að þú getir deilt stillingum fyrir einingar einkunna og umsagna meðal margra PDP á netverslunarvefsvæðinu, sjá [Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md).

Eftirfarandi mynd sýnir hvernig glugginn **Bæta við einingu** birtir einingar einkunna og umsagna í Dynamics 365 Commerce.

![Bættu við einingaglugga](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Skrifa umsagnareiningu

Í einingunni skrifa umsögn inniheldur hnappurinn **Skrifa umsögn** sem gerir notendum kleift að skrá sig inn, úthluta mati og skrifa umsögn um vöru. Þessi eining gerir notendum einnig kleift að breyta einkunn eða umsögn sem þeir sendu inn áður. Þessi eining birtist venjulega fyrir ofan einingarnar stuðlarit einkunna og lista yfir afurðaumsagnir á PDP.

Eftirfarandi mynd sýnir valmyndina **Skrifa umsögn** sem birtist þegar viðskiptavinur velur **Skrifa umsögn**. Viðskiptavinurinn getur notað þennan glugga til að leggja fram mat og umsögn.

![Skrifaðu umsagnarglugga](media/rnr-eCommerce-write-review-module.png)

Eftirfarandi tafla sýnir eiginleikann fyrir eininguna skrifa umsögn sem þarf að stilla í höfundatólinu.

| Nafn eiginleika | Virði        | Lýsing á eiginleika                 |
|---------------|--------------|--------------------------------------|
| Nafn          | Skrifa umsögn | Heiti einingarinnar skrifa umsögn. |

### <a name="ratings-histogram-module"></a>Stuðlaritseining einkunna

Stuðlaritseining einkunna sýnir stuðlarit með einkunnum. Þessi eining birtist venjulega á milli eininga skrifa umsagna og afurðaumsagnalistaeiningarinnar á PDP.

Stuðlaritseining einkunna þarf enga skilgreiningu. Þú þarft bara að bæta einingunni við í PDP sniðmátinu. 

Eftirfarandi myndir sýna hvernig PDP sniðmát lítur út í Dynamics 365 Commerce þegar einkunnir og umsagnaeiningar eru stilltar til birtingar á PDP.

![PDP sniðmát þegar einkunnir og umsagnir eru stilltar til birtingar á PDP](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Eining umsagnalista afurðar

Einingin yfir vöruúttektarlista sýnir lista yfir afurðaumsagnir ásamt flokkunar-, síunar- og síðuskiptingarvalkostum. Þessi eining birtist venjulega eftir stuðlaritseining einkunna á PDP.

Eftirfarandi tafla sýnir eiginleika fyrir einingu yfir umsagnalista afurða sem þarf að stilla í höfundatólinu.

| Nafn eiginleika              | Virði | Lýsing á eiginleika |
|----------------------------|-------| ---------------------|
| Umsagnir sýndar á síðu | 10    | Fjöldi umsagna sem ætti að birtast í einu á PDP. Hnapparnir **Næst** og **Fyrri** eru með, svo að notendur geti farið í gegnum umsagnasíðurnar. |

#### <a name="ratings-histogram--summary-view"></a>Stuðlarit einkunna - Samantektaryfirlit

Einingin yfir afurðaumsagnalista inniheldur hólf þar sem þú getur bætt við stuðlaritseiningu einkunna. Eftirfarandi mynd sýnir hvernig þú getur bætt við stuðlaritseiningu einkunna fyrir afurðaumsagnalista í Dynamics 365 Commerce.

![Bætir við stuðlaritseiningu einkunna í einingu afurðaumsagnalista](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Skilgreina svæði til að sýna einkunnir og umsagnir

Stillingargildi fyrir einkunnir og umsagnir, svo sem auðkenni leigjanda, lengd textatexta og lengd endurskoðunar titils, eru stillt á vefsvæðisstig. 

Fylgdu þessum skrefum til að stilla vefsíðu til að sýna einkunnir og umsagnir. 

1. Fara til **Heim \> Svæði**.
1. Veldu heiti vefsvæðisins. 
1. Farðu á **Svæðisstjórnun \> Stækkunarhæfni**. 
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
1. Farðu á **Svæðisstjórnun \> Stækkunarhæfni**
1. Á flipanum **Leiðir**, undir **Persónuvernd og stefna RNR**, velurðu **Bæta við tengli**. Ef tengill hefur þegar verið sleginn inn og þú vilt skipta um hann skaltu velja hann. 
1. Í valmyndinni **Bæta við tengli** velurðu tengilinn fyrir persónuverndar- og stefnusíðuna og velur síðan **Í lagi**. 
1. Veldur **Vista og birta**. 

Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.

![Stilling tengils fyrir persónuverndar- og stefnusíðuna](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Samstilla afurðaeinkunnir í Dynamics 365 Retail](sync-product-ratings.md)
