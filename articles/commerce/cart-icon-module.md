---
title: Körfutáknseining
description: Þessi grein fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
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
ms.openlocfilehash: a5b86b0c843a680dd0c46295a69e12d6e3542619
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859114"
---
# <a name="cart-icon-module"></a>Körfutáknseining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um körfutáknseininguna og lýsir því hvernig á að bæta henni við vefsíður í Microsoft Dynamics 365 Commerce.

Körfutákneiningin táknar körfuna í hauseiningu síðunnar og sýnir fjölda af vörum í körfunni. Körfutáknseiningin birtir einnig yfirlit yfir körfu (einnig þekkt sem smákarfa) þegar músin sveimar yfir körfutákninu. Smákarfan veitir notanda yfirlit yfir hluti í körfunni án þess að þurfa að fara á körfusíðuna. Að auki gerir það notandanum einnig kleift að fara beint á greiðslusíðu ef viðkomandi er ánægður með yfirlitið. Þetta dregur úr fjölda síðnaferða og gerir afgreiðsluna hraðari. 

Eftirfarandi mynd sýnir dæmi um einingu körfutákns sem sýnir smákörfu í Fabrikam-fyrirsögninni.

![Dæmi um körfutáknseiningu.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

- **Sýna smákörfu** – Þegar þessi eiginleiki er stilltur á **Satt** er yfirlit yfir körfu (smákörfu) sýnt þegar notendur fara með bendilinn yfir körfuna. Þessi virkni er aðeins studd fyrir skjáborðsgáttir.
- **Leyfa nafnlausa kaup** – Þegar þessi eiginleiki er stilltur á **Satt** gerir smákarfan notendum sem ekki hafa skráð sig inn kleift að ganga frá kaupum sem gestir. Þessi eiginleiki er urfáanleg í Commerce útgáfu 10.0.21, sem hluti af einingasafnspakkanum.
- **Röð hluta** – Þessi eiginleiki stýrir röðinni sem hlutir eru sýndir í smákörfunni. Þegar valkosturinn **Nýjum hlutum bætt efst á listann** er valinn birtast nýir hlutir sem bætt er við efst á listanum í smákörfu fyrir vörur. Þegar sjálfgefni valkosturinn **Nýjum hlutum bætt neðst á listann** er valinn birtast nýir hlutir sem bætt er við neðst á listanum í smákörfu fyrir vörur. Þessi eiginleiki er urfáanleg frá Commerce útgáfu 10.0.21, sem hluti af einingasafnspakkanum.

> [!IMPORTANT]
> Eiginleikarnir **Leyfa nafnlaus kaup** og **Röðun hluta** eru í boði frá og með Commerce-útgáfu 10.0.21. Nauðsynlegt er að Commerce einingasafnspakki 9.31 útgáfa sé settur upp.

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Eiginleikar einingar og hólfa í þema Adventure Works

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
