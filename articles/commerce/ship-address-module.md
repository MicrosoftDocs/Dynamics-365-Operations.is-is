---
title: Sendingaraðseturseining
description: Þessi grein fjallar um sendingarheimiliseininguna og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 48e6909b4dac9722830a83ec3a63a58876768d7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275006"
---
# <a name="shipping-address-module"></a>Sendingaraðseturseining

[!include [banner](includes/banner.md)]

Þessi grein lýsir nær yfir sendingarheimiliseininguna og útskýrir hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.

Einingin fyrir sendingaraðsetur gerir viðskiptavinum kleift að bæta við eða velja sendingaraðsetur fyrir pöntun meðan á greiðsluferlinu stendur. Ef viðskiptavinur er skráður inn eru öll aðsetur sem áður voru vistuð fyrir þennan viðskiptavin sýnd og viðskiptavinurinn getur valið á milli þeirra. Viðskiptavinurinn getur einnig bætt við nýju heimilisfangi. Einingin fyrir sendingaraðsetur er notuð fyrir allar vörur í pöntun sem krefjast sendingar.

Hægt er að skilgreina snið sendingaraðseturs í Commerce Headquarters fyrir hvert land eða svæði og eining sendingaraðseturs framfylgir þá reglum fyrir tiltekið land/svæði.

Þegar viðskiptavinir færa inn sendingaraðsetur í greiðsluferlinu, hafa þeir val um að vista aðsetrið sem aðalaðsetur. Þessi valkostur er aðeins sýndur ef viðskiptavinur er skráður inn.

Þótt einingin fyrir sendingaraðsetur veiti ekki staðfestingu á aðsetri, er hægt að innleiða þessa virkni í gegnum sérstillingu.

Eftirfarandi mynd sýnir dæmi um nýja einingu sendingaraðseturs á greiðsluferlissíðu.

![Dæmi um einingu sendingaraðseturs á greiðsluferlissíðu.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Haus | Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Valfrjáls fyrirsögn fyrir einingu sendingaraðseturs. |
| Sýna aðsetursgerð | **Satt** eða **Ósatt** | Ef þessi valfrjálsi eiginleiki er stilltur á **Satt**, verður gerð aðseturs, t.d. **Heimili** eða **Fyrirtæki** sýnt. Ef engin aðsetursgerð er tilgreind verður aðsetrið sjálfkrafa vistað sem **Gerð**=**Annað**. |
| Kveikja á sjálfvirkum tillögum| **Satt** eða **Ósatt** | Ef þessi valfrjálsa eiginleiki er stilltur á **Satt** verða tillögur að sjálfvirkum aðsetrum veittar. Þessar tillögur eru knúnar af Bing-kortum. Frekari upplýsingar um hvernig setja á upp samþættingu Bing-korta á svæðinu er að finna í [Verslunarvalseining](store-selector.md). Þessi eiginleiki er í boði frá og með Commerce útgáfu 10.0.15.|
|Valkostir fyrir sjálfvirkar tillögur| Númer| Ef sjálfvirkar aðseturstillögur eru virkar er hægt að tilgreina frekari valmöguleika, svo sem hámarksfjölda tillagna sem ætti að gefa upp.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Bæta einingu sendingaraðseturs við greiðsluferlissíðu og stilla nauðsynlega eiginleika

Aðeins er hægt að bæta einingu sendingaraðseturs við greiðsluferliseiningu. Frekari upplýsingar um hvernig skilgreina á einingu sendingaraðseturs og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Afhendingarkostaeining](delivery-options-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)

[Eining til að velja verslun](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
