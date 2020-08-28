---
title: Eining sendingaraðseturs
description: Þetta efnisatriði fjallar um einingu sendingaraðseturs og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 380d268ec0ba64367f090c31408eac1c54d0ff17
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661442"
---
# <a name="shipping-address-module"></a>Eining sendingaraðseturs

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir einingu sendingaraðseturs og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Einingin fyrir sendingaraðsetur gerir viðskiptavinum kleift að bæta við eða velja sendingaraðsetur fyrir pöntun meðan á greiðsluferlinu stendur. Ef viðskiptavinur er skráður inn eru öll aðsetur sem áður voru vistuð fyrir þennan viðskiptavin sýnd og viðskiptavinurinn getur valið á milli þeirra. Viðskiptavinurinn getur einnig bætt við nýju heimilisfangi. Einingin fyrir sendingaraðsetur er notuð fyrir allar vörur í pöntun sem krefjast sendingar.

Hægt er að skilgreina snið sendingaraðseturs í Commerce Headquarters fyrir hvert land eða svæði og eining sendingaraðseturs framfylgir þá reglum fyrir tiltekið land/svæði.

Þegar viðskiptavinir færa inn sendingaraðsetur í greiðsluferlinu, hafa þeir val um að vista aðsetrið sem aðalaðsetur. Þessi valkostur er aðeins sýndur ef viðskiptavinur er skráður inn.

Þótt einingin fyrir sendingaraðsetur veiti ekki staðfestingu á aðsetri, er hægt að innleiða þessa virkni í gegnum sérstillingu.

Eftirfarandi mynd sýnir dæmi um nýja einingu sendingaraðseturs á greiðsluferlissíðu.

![Dæmi um einingu sendingaraðseturs á greiðsluferlissíðu](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Fyrirsögn | Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Valfrjáls fyrirsögn fyrir einingu sendingaraðseturs. |
| Sýna aðsetursgerð | **Satt** eða **Ósatt** | Ef þessi valfrjálsi eiginleiki er stilltur á **Satt**, verður gerð aðseturs, t.d. **Heimili** eða **Fyrirtæki** sýnt. Ef engin aðsetursgerð er tilgreind verður aðsetrið sjálfkrafa vistað sem **Gerð**=**Annað**. |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Bæta einingu sendingaraðseturs við greiðsluferlissíðu og stilla nauðsynlega eiginleika

Aðeins er hægt að bæta einingu sendingaraðseturs við greiðsluferliseiningu. Frekari upplýsingar um hvernig skilgreina á einingu sendingaraðseturs og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Eining afhendingarvalkosta](delivery-options-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)
