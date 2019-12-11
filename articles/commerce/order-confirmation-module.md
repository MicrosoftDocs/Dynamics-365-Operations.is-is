---
title: Eining pöntunarstaðfestingar
description: Þetta efni fjallar um staðfestingareiningar panntana og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698327"
---
# <a name="order-confirmation-module"></a>Eining pöntunarstaðfestingar

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um staðfestingareiningar panntana og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Pöntunarstaðfestingareining er notuð til að sýna staðfestingarskilaboð á staðfestingarsíðu þegar pöntun hefur verið gerð. Pöntunarstaðfestingareiningin sýnir pöntunarstaðfestingarnúmerið og netfang viðskiptavinarins sem gefið var upp í greiðsluferlinu.

Þegar pöntun er gerð í greiðsluferli er pöntunarstaðfestingarnúmerið og netfang viðskiptavina sent á staðfestingarsíðu sem fyrirspurnstrengur í vefslóð síðunnar. Pöntunarstaðfestingareiningin fær þessar upplýsingar og birtir pöntunarstöðu á pöntunarstaðfestingarsíðunni. Pöntunarstaðfestingin þarf þetta síðusamhengi til að gefa upp stöðu pöntunarinnar.

## <a name="order-confirmation-module-properties"></a>Eiginleikar staðfestingareiningar pöntunar

| Nafn eiginleika | Gildi | Lýsing |
|---------------|--------|-------------|
| Fyrirsögn       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Pöntunarstaðfestingareiningin getur haft fyrirsögn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Einingar sem hægt er að nota í einingu pöntunarstaðfestingarsíðu 

- **Tillögur** - Hægt er að setja tillögueininguna á staðfestingarsíðu pöntunar til að benda viðskiptavinum á aðrar vörur.
- **Markaðssetning** - Markaðseiningin getur bætt markaðsinnihaldi við staðfestingarsíðu.

## <a name="create-an-order-confirmation-page-module"></a>Búa til einingu pöntunarstaðfestingarsíðu

1. Búðu til síðusniðmát sem heitir **sniðmát pöntunarstaðfestingar**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við pöntunarstaðfestingareiningu.
1. Bættu við tillagnaeiningu í pöntunarstaðfestingareiningunni.
1. Vistaðu og forskoðaðu sniðmátið. Ekki ætti að láta pöntunarstaðfestinguna af hendi þar sem hún þarf samhengi við pöntunarstaðfestingarnúmerið.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu pöntunarstaðfestingarsniðmátið sem þú bjóst til til að búa til síðu sem heitir **pöntunarstaðfestingarsíða**.
1. Bættu sjálfgefnu síðunni við útlínur síðunnar.
1. Í hólfið **Fyrirsögn** bætirðu við fyrirsagnarbroti.
1. Í hólfið **Síðufótur** bætirðu við síðufótarbroti.
1. Í hólfinu **Aðal** bætirðu við pöntunarstaðfestingareiningu.
1. Í eiginleikaglugganum í einingu pöntunarstaðfestingar bætirðu við fyrirsögninni **Pöntunarstaðfesting**.
1. Fyrir neðan pöntunarstaðfestingareininguna skaltu bæta við tillögueiningunni og stilla hana þannig að hún noti stillingarnar **Nýtt** og **Mest selt**.
1. Vistaðu og forskoðaðu síðuna, skráðu hana inn og gefðu út.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining síðuhauss](author-header-module.md)

[Eining síðufótar](author-footer-module.md)
