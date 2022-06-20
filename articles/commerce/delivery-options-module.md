---
title: Afhendingarkostaeining
description: Þessi grein fjallar um einingar fyrir afhendingarvalkosti og útskýrir hvernig á að stilla þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 554a17cf1c90f7fdaa20de74c3f6726910ab815d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894559"
---
# <a name="delivery-options-module"></a>Afhendingarkostaeining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um einingar fyrir afhendingarvalkosti og útskýrir hvernig á að stilla þær í Microsoft Dynamics 365 Commerce.

Einingar afhendingarvalkosta leyfir viðskiptavinum að velja afhendingarmáta á borð við senda eða sækja fyrir pöntun á netinu. Heimilisfang viðtakanda er nauðsynlegt til að ákvarða afhendingarmáta. Ef heimilisfang viðtakanda breytist, þarf að sækja afhendingarvalkostina aftur. Ef pöntun inniheldur aðeins vörur sem verða sóttar í verslun, verður þessi eining sjálfkrafa falin.

Frekari upplýsingar um hvernig skilgreina á afhendingarmáta er að finna í [Uppsetning netrásar](channel-setup-online.md) og [Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Hver afhendingarmáti getur verið með gjald tengt við. Frekari upplýsingar um hvernig á að skilgreina gjöld fyrir netverslun er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md).

Í Commerce-útgáfu 10.0.13 hefur eining afhendingarvalkosta verið uppfærð til að styðja eiginleikana **Gjöld í haus án skiptingar** og **Senda sem línugjald**. Ef slökkt er á skiptingu má búast við því að verkflæði rafrænna viðskipta leyfi ekki blandaðan afhendingarmáta fyrir vörurnar í körfunni (þ.e. sumar vörur eru valdar fyrir sendingu, en aðrar eru valdar til að sækja). Eiginleikinn **Gjöld í haus án skiptingar** krefst þess að kveikt sé á flagginu **Virkja samræmda meðhöndlun afhendingar í rás** í Commerce Headquarters. Þegar kveikt er á eiginleikaflagginu verða sendingargjöld sett á annaðhvort á hausstigi eða línustigi, fer eftir skilgreiningunni í Commerce Headquarters.

Fabrikam-þemað styður við blandaða afhendingarmáta, þar sem sumar vörur eru valdar fyrir sendingu en aðrar eru valdar til að vera sóttar. Í þessari stillingu verður sendingargjöldum skipt niður fyrir allar vörur sem eru valdar fyrir afhendingarmáta sendingar. Til að blandaður afhendingarmáti virki þarf fyrst að skilgreina eiginleikann **Gjöld í haus með skiptingu** í Commerce Headquarters. Frekari upplýsingar um þessa skilgreiningu er að finna í [Skipta gjöldum í haus til að stemma við sölulínur](pro-rate-charges-matching-lines.md).

Ef sendingargjöld eiga við um línuatriði er hægt að sýna þau í körfulínunni fyrir hverja vöru. Þessi virkni krefst þess að kveikt sé á eiginleikanum **Sýna sendingargjöld í línuatriði** fyrir bæði körfueininguna og greiðsluferliseininguna. Frekari upplýsingar er að finna í [Körfueining](add-cart-module.md) og [Greiðsluferliseining](add-checkout-module.md).

Eftirfarandi mynd sýnir dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu.

![Dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Eiginleikar einingar afhendingarvalkosta

| Eiginleiki | Gildi | lýsing |
|----------|--------|-------------|
| Fyrirsögn | Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Valfrjáls fyrirsögn fyrir einingu afhendingarvalkosta. |
| Sérsniðið CSS heiti klasa | Texti | Sérsniðið klasaheiti stallaðs stílblaðs (CSS) sem verður notað til að sýna þessa einingu, ef það á við. |
| Sía fyrir sendingarstillingu | **Ekki sía** eða **Afhendingarmátar án sendingar** | Gildi sem tilgreinir hvort eining afhendingarvalkosta eigi að sía út alla afhendingarmáta án sendingar. |
| Velja afhendingarvalkost sjálfkrafa | **Ekki sía**, **Velja afhendingarvalkost sjálfkrafa og sýna samantekt** eða **Velja afhendingarvalkost sjálfkrafa og ekki sýna samantekt** | Þessi eiginleiki notar sjálfkrafa fyrsta tiltæka afhendingarvalkostinn til að ljúka kaupum án þess að notandinn þurfi að velja hann. Aðeins ætti að nota hann ef einn afhendingarvalkostur er fyrir hendi. Þessi eiginleiki er studdur frá og með Commerce-útgáfu 10.0.19. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Bæta einingu afhendingarvalkosta við greiðsluferlissíðu og stilla nauðsynlega eiginleika

Aðeins er hægt að bæta einingu afhendingarvalkosta við greiðsluferliseiningu. Frekari upplýsingar um hvernig skilgreina á einingu afhendingarvalkosta og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).

> [!NOTE]
> Þú gætir fundið fyrir ósamkvæmri afgreiðslu meðhöndlunar, eða þú gætir ekki séð óhlutfallsbundnar hausagjöld á rafrænu viðskiptarásinni þinni. Fyrir leiðbeiningar um hvernig eigi að laga þessi vandamál, sjá [Virkjaðu samræmda afhendingarham meðhöndlun í rafrænum viðskiptarásum](consistent-delivery-mode-handling.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Sendingaraðseturseining](ship-address-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)

[Uppsetning netrásar](channel-setup-online.md)

[Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md)

[Skipta gjöldum í haus til að stemma við sölulínur](pro-rate-charges-matching-lines.md)

[Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
