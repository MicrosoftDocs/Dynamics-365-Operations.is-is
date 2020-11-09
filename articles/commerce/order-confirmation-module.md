---
title: Upplýsingaeining pöntunar
description: Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015181"
---
# <a name="order-details-module"></a>Upplýsingaeining pöntunar

[!include [banner](includes/banner.md)]

Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Eftir að pöntun hefur verið gerð er hægt að nota staðfestingarhlutann til að sýna staðfestingarupplýsingar. Hún sýnir auðkenni pöntunarstaðfestingar, upplýsingar um pöntunarupplýsingar og aðrar pöntunarupplýsingar, svo sem hlutina sem voru keyptir, greiðsluupplýsingar og sendingaraðferð.

## <a name="order-details-module-properties"></a>Eiginleikar upplýsingaeiningar pöntunar

| Nafn eiginleika  | Gildi | lýsing |
|----------------|--------|-------------|
| Yfirskrift        | Texti og merki fyrirsagnar ( **H1** , **H2** , **H3** , **H4** , **H5** eða **H6** ) | Upplýsingaeining pöntunar getur verið með haus. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Númer tengiliðar | Text | Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Einingar sem hægt er að nota á pöntunarupplýsingasíðu

Þegar þú býrð til síðu fyrir pöntunarupplýsingar geturðu bætt við öðrum viðeigandi einingum til viðbótar pöntunarupplýsingareiningunni. Hér eru nokkur dæmi:

- **Tillögueining** - Hægt er að bæta tillögueiningunni við á upplýsingasíðu pöntunar til að benda viðskiptavinum á aðrar vörur.
- **Markaðseiningar** - Hægt er að bæta hvaða markaðsseining sem er við pöntunarsíðuna til að sýna markaðsefni.

## <a name="add-an-order-details-module-to-a-page"></a>Bæta upplýsingaeiningu pöntunar við síðu

Til að bæta upplýsingaeiningu pöntunar við nýja síðu og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát** , undir **Heiti sniðmáts** , skal slá inn heitið **Sniðmát pöntunarupplýsinga** og velja síðan **Í lagi**.
1. Í hólfinu **Meginmál** , skal velja úrfellingarmerkið ( **...** ) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið ( **...** ) og síðan velja **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja eininguna **Upplýsingar um pöntun** og síðan velja **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða sniðmátið. Pöntunarupplýsingaeiningin verður ekki látin af hendi sem hún þarf samhengi við pöntunarstaðfestingarnúmerið.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja **Sniðmát pöntunarupplýsinga**. Undir **Síðuheiti** skal færa inn **Upplýsingasíða pöntunar** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið ( **...** ) og síðan velja **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja eininguna **Upplýsingar um pöntun** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu fyrir upplýsingaeiningu pöntunar skal velja **Fyrirsögn** við hliðina á blýantstákninu.
1. Í reitinn **Fyrirsagnartexti** í svarglugganum **Fyrirsögn** skal slá inn fyrirsagnartextanum **Upplýsingar pöntunar** og velja síðan **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Eining sendingaraðseturs](ship-address-module.md)

[Eining afhendingarvalkosta](delivery-options-module.md)

[Gjafakortseining](add-giftcard.md)
