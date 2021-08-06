---
title: Körfutáknseining
description: Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9e3850d98e716d1bbea2017f6e8c9d75f19adc9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638002"
---
# <a name="cart-icon-module"></a>Körfutáknseining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.

Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni. Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu. Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna. Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið. Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari. 

Eftirfarandi mynd sýnir dæmi um einingu körfutákns sem sýnir smákörfu í Fabrikam-fyrirsögninni.

![Dæmi um körfutáknseiningu.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

- **Sýna smákörfu** - Þegar satt gerir þessi eiginleiki kleift að birta yfirlit yfir körfu (smákörfu) þegar músin sveimar yfir körfutákninu. Þessi virkni er aðeins studd fyrir skjáborðsgáttir.

## <a name="module-properties-in-the-adventure-works-theme"></a>Eiginleikar einingar í þema Adventure Works

Í þema Adventure Works inniheldur körfutáknseiningin tvö aukaleg hólf fyrir smákörfuna. Þessi hólf eru tekin með í viðbót einingaskilgreiningar.

- **Kynningartilboð í tómri körfu** – Þetta hólf notar einingu efnisbálks. Þegar karfan er tóm er tilgreind eining efnisbálks sýnd. Hægt er að nota einingu efnisbálksins fyrir kynningartilboð, markaðsefni og tengla á flokkasíður til að aðstoða viðskiptavini með áframhaldandi verslunarferli.
- **Kynningarefni** – Hægt er að nota þetta hólf til að sýna kynningartilboð, svo sem „Ókeypis sending á pöntunum yfir $100.“ Hægt er að nota einingar efnisbálks, textabálks og myndalista í hólfi kynningarefnis.

Eftirfarandi mynd sýnir dæmi um einingu körfutákns í þema Adventure Works sem sýnir kynningarefni í smákörfunni.

![Dæmi um körfutáknseiningu í þema Adventure Works](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Hólf í þema Adventure Works eru í boði frá og með Dynamics 365 Commerce útgáfu 10.0.20.

## <a name="add-a-cart-icon-module-to-a-page"></a>Bæta körfutáknseiningu við síðu

Til að bæta við einingunni fyrir körfutákn, sjá [Hauseiningu](author-header-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Sendingaraðseturseining](ship-address-module.md)

[Afhendingarkostaeining](delivery-options-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
