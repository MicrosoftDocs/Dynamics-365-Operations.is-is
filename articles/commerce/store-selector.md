---
title: Vista valeiningu
description: Þetta efni fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157341"
---
# <a name="store-selector-module"></a>Vista valeiningu

[!include [banner](includes/banner.md)]

Þetta efni fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Verslunarvalseining er notuð fyrir „kaup á netinu, sækja í verslun“ (BOPIS) viðskiptavinar atburðarás. Það birtir lista yfir verslanir þar sem vara er fáanleg, svo og verslunartími og vörubirgðir fyrir hverja verslun.

Verslunarvalseiningin krefst samhengis vöru og leitarstað til að finna verslanir. Ef ekki er leitað, skiptir það staðinn að vafra staðsetningu viðskiptavinarins að því tilskildu að viðskiptavinurinn veiti samþykki. Einingin er með inntakskassa sem gerir viðskiptavininum kleift að slá inn staðsetningu (póstnúmer, eða borg og ríki) til að finna verslanir sem eru í nágrenninu.

Verslunarvalseiningin er samþætt við Bing Maps Geocoding forritunarviðmót (API) landskóðunar til að umbreyta staðsetningunni í breiddar- og lengdargráðu. Bing Maps API lykils er krafist og bæta verður honum við Commerce sameiginlegar færibreytusíðuna í Dynamics 365 Commerce.

Hægt er að bæta verslunareiningareiningunni við innkaupakassaeiningu á upplýsingasíðu vöru (PDP) til að birta verslanir þar sem vara er fáanleg. Það er einnig hægt að bæta við körfu mát. Þegar versluninni er bætt við körfueininguna birtir valkosti verslunarinnar söfnunarkosti fyrir hverja vöruhluta í körfunni. Að auki, með sérsniðnum kóðun er hægt að bæta þessari einingu við aðrar síður eða einingar í gegnum viðbætur og sérstillingar.

Til að BOPIS atburðarásinn virki, ættu vörur að vera stilltar með afhendingarstillingu „viðskiptavinur sækir“. Annars verður einingin ekki sýnd á viðkomandi síðum. Nánari upplýsingar um hvernig á að stilla afhendingarstillingu, sjá [Settu upp afhendingaraðferðir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Eftirfarandi mynd sýnir dæmi um verslunarvalseiningu sem er notuð á PDP.

![Dæmi um verslunarvalseiningu](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Notkun verslunarvalseiningar í e-Commerce

- Hægt er að nota verslunareiningareiningu á upplýsingasíðu vöru (PDP) til að finna nálægar verslanir þar sem vara er fáanleg.
- Hægt er að nota verslunarvalseiningu á körfusíðu til að finna nálægar verslanir þar sem vara í körfunni er fáanleg.

## <a name="store-selector-module-properties"></a>Eiginleikar verslunarvalseiningar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Leitarradíus | Númer | Skilgreinir leitarradíus fyrir verslanir, í mílum. Ef ekkert gildi er tilgreint er sjálfgefinn leitarradíus upp á 50 mílur notaður.|
|Þjónustuskilmálar | URL    |  Skilmálar þjónustuslóðarinnar sem er krafist fyrir þjónustuna Bing Maps. |

## <a name="add-a-store-selector-module-to-a-page"></a>Bæta við verslunarvalseiningu á síðu

Verslunarvalseining þarf samhengi vöru, þannig að það er aðeins hægt að nota það innan kaupabox og körfueiningar. Verslunarvalseiningar virka ekki utan þessara eininga.

- Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við innkaupakassaeiningar, sjá [Kaupkassaeiningu](add-buy-box.md). 
- Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við körfueiningar, sjá [Körfueiningu](add-cart-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Stutt kynning um PDP](quick-tour-pdp.md)

[Stutt kynning á Körfu og greiðsluferli](quick-tour-cart-checkout.md)

[Setja upp afhendingarmáta](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
