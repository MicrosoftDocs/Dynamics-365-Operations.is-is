---
title: Upplýsingaeining pöntunar
description: Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026018"
---
# <a name="order-details-module"></a>Upplýsingaeining pöntunar


[!include [banner](includes/banner.md)]

Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Eftir að pöntun hefur verið gerð er hægt að nota staðfestingarhlutann til að sýna staðfestingarupplýsingar. Hún sýnir auðkenni pöntunarstaðfestingar, upplýsingar um pöntunarupplýsingar og aðrar pöntunarupplýsingar, svo sem hlutina sem voru keyptir, greiðsluupplýsingar og sendingaraðferð.

## <a name="order-confirmation-module-properties"></a>Eiginleikar staðfestingareiningar pöntunar

| Nafn eiginleika  | Gildi | Lýsing |
|----------------|--------|-------------|
| Fyrirsögn        | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Pöntunarstaðfestingareiningin getur haft fyrirsögn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Númer tengiliðar | Text | Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Einingar sem hægt er að nota á pöntunarupplýsingasíðu

Þegar þú býrð til síðu fyrir pöntunarupplýsingar geturðu bætt við öðrum viðeigandi einingum til viðbótar pöntunarupplýsingareiningunni. Hér eru nokkur dæmi:

- **Tillögueining** - Hægt er að bæta tillögueiningunni við á upplýsingasíðu pöntunar til að benda viðskiptavinum á aðrar vörur.
- **Markaðseiningar** - Hægt er að bæta hvaða markaðsseining sem er við pöntunarsíðuna til að sýna markaðsefni.

## <a name="create-an-order-details-page-module"></a>Búa til einingu pöntunarupplýsingasíðu

1. Búðu til síðusniðmát sem heitir **Sniðmát pöntunarstaðfestingar**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við pöntunarupplýsingaeiningu.
1. Bættu við tillögueiningu í pöntunarupplýsingaeiningunni.
1. Vistaðu og forskoðaðu sniðmátið. Pöntunarupplýsingaeiningin verður ekki látin af hendi sem hún þarf samhengi við pöntunarstaðfestingarnúmerið.
1. Ljúktu við að breyta sniðmátinu, vistaðu það og birtu.
1. Notaðu pöntunarupplýsingasniðmátið sem þú bjóst til til að búa til síðu sem heitir **pöntunarupplýsingasíða**.
1. Bættu sjálfgefnu síðunni við útlínur síðunnar.
1. Í hólfið **Fyrirsögn** bætirðu við fyrirsagnarbroti.
1. Í hólfið **Síðufótur** bætirðu við síðufótarbroti.
1. Í hólfinu **Aðal** bætirðu við pöntunarupplýsingaeiningu.
1. Í eiginleikaglugganum í einingu pöntunarupplýsinga bætirðu við fyrirsögninni **Pöntunarupplýsingar**.
1. Fyrir neðan pöntunarupplýsingaeininguna skaltu bæta við tillögueiningunni og stilla hana þannig að hún noti stillingarnar **Nýtt** og **Mest selt**.
1. Vistaðu og forskoðaðu síðuna.
1. Ljúktu við að breyta síðunni, vistaðu hana og birtu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining síðuhauss](author-header-module.md)

[Eining síðufótar](author-footer-module.md)
