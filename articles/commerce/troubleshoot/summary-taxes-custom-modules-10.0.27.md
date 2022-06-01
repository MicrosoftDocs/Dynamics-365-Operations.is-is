---
title: Samtala pöntunarsamantektar inniheldur ekki skatta á gjöld þegar sérsniðnar pöntunarsamantektareiningar eru notaðar
description: Þetta efnisatriði veitir leiðbeiningar um úrræðaleit sem geta hjálpað þér þegar þú notar sérsniðnar pöntunarsamantektareiningar og undirsamtala pöntunaryfirlits inniheldur ekki skatta af gjöldum í atburðarásinni „verð inniheldur söluskatt“.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767929"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Samtala pöntunarsamantektar inniheldur ekki skatta á gjöld þegar sérsniðnar pöntunarsamantektareiningar eru notaðar

Þetta efnisatriði veitir leiðbeiningar um úrræðaleit sem geta hjálpað þér þegar þú notar sérsniðnar pöntunarsamantektareiningar og undirsamtala pöntunaryfirlits inniheldur ekki skatta af gjöldum í atburðarásinni „verð inniheldur söluskatt“.

## <a name="description"></a>Lýsing

Frá og með Microsoft Dynamics 365 Commerce útgáfu 10.0.27, hafa eftirfarandi breytingar verið gerðar á atburðarásinni „verð inniheldur söluskatt“ til að veita samræmda upplifun á samantektareiningum á e-verslunarsíðum.

- Tveimur nýjum sviðum hefur verið bætt við: **TaxOnShippingCharge** og **TaxOnNonShippingCharges**.
- The **GetSalesOrderBySalesId** og **GetSalesOrderByTransactionId** forritunarviðmót (API) hafa nákvæm gildi fyrir eftirfarandi reiti í atburðarásinni „verð inniheldur söluskatt“:

    - Subtotal SalesAmount
    - SubtotalAmountUnTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Hins vegar, ef þú ert að nota sérsniðnar pöntunarsamantektareiningar, gætu þessar breytingar haft áhrif á undirsamtölur pöntunarsamantektar með því að skattar af gjöldum eru ekki teknir með.

## <a name="resolution"></a>Upplausn

Ef þú ert að nota sérsniðnar pöntunarsamantektareiningar og vilt ekki erfa breytingarnar sem hafa verið gerðar á atburðarásinni "verð inniheldur söluskatt" í Commerce útgáfu 10.0.27 og síðar, fylgdu leiðbeiningunum í þessum hluta.

Með því að fara aftur í fyrri (áður útgáfu 10.0.27) pöntunarsamantektarhegðun **söluTransaction.SubtotalAmount** og **söluTransaction.SubtotalAmountWithoutTax** reitum, endurheimtir þú innifalið heildarskattupphæð gjalds (**TaxOnShippingCharge** og **TaxOnNonShippingCharges**) í undirheildarupphæðum (**SubtotalAmount** og **SubtotalAmountUnTax**).

Til að fara aftur í fyrri pöntunarsamantektarhegðun skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum Commerce, opnaðu síðuna Commerce færibreytur (**Verslun og verslun \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptabreytur**).
1. Í vinstri yfirlitsrúðunni, veldu **Stillingarfæribreytur**.
1. Bættu við eftirfarandi stillingarbreytum og stilltu gildi hvers og eins á **satt**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Ef þú hefur áður notað **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** stillingarbreytu og vilja halda sömu hegðun fyrir **order.NetAmountWithoutTax** eign, þú ættir líka að bæta við **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** stillingarbreytu og stilltu gildi hennar á **satt**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Fela upplýsingar um skattskil í samantektum pantana](../hide-taxes-breakup.md)
