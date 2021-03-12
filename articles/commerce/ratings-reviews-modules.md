---
title: Einkunna- og umsagnaeiningar
description: Þetta efni fjallar um mat og yfirferð einingar sem notaðar eru á upplýsingasíðum afurða í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: b17e986c2e30134c334cd547a85a1dd682172a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979804"
---
# <a name="ratings-and-reviews-modules"></a>Einkunna- og umsagnaeiningar

[!include [banner](includes/banner.md)]

Þetta efni fjallar um mat og yfirferð einingar sem notaðar eru á upplýsingasíðum afurða í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun og eru einnig búnaður til að safna endurgjöf viðskiptavina um afurðir. 

Einkunnir eru sýndar á vörulistasíðum, flokkalistasíðum, leitarniðurstöðusíðum og öðrum vefsíðum. 

Stuðlarit einkunna og afurðaumsagnir eru sýndar á upplýsingasíðum afurða. Hnappurinn **Skrifa umsögn** gerir viðskiptavinum kleift að senda inn einkunnir og umsagnir um afurð. Þessum eiginleikum upplýsingasíða afurða er stjórnað af mats- og umsagnareiningum.

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
![Skrifaðu umsagnarglugga](media/rnr-eCommerce-write-review-module.png) Eftirfarandi tafla sýnir eiginleikann fyrir eininguna skrifa umsögn sem þarf að stilla í höfundatólinu.
| Nafn eiginleika | Virði        | Lýsing á eiginleika                 |
|---------------|--------------|--------------------------------------|
| Nafn          | Skrifa umsögn | Heiti einingarinnar skrifa umsögn. |

### <a name="ratings-histogram-module"></a>Stuðlaritseining einkunna

Stuðlaritseining einkunna sýnir stuðlarit með einkunnum. Þessi eining birtist venjulega á milli eininga skrifa umsagna og afurðaumsagnalistaeiningarinnar á PDP.
Stuðlaritseining einkunna þarf enga skilgreiningu. Þú þarft bara að bæta einingunni við í PDP sniðmátinu. Eftirfarandi myndir sýna hvernig PDP sniðmát lítur út í Dynamics 365 Commerce þegar einkunnir og umsagnaeiningar eru stilltar til birtingar á PDP.
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

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining pöntunarstaðfestingar](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
