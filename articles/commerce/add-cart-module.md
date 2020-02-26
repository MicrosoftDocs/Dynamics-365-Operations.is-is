---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025437"
---
# <a name="cart-module"></a>Körfueining


[!include [banner](includes/banner.md)]

Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Körfueining er notuð til að sýna hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa. Til dæmis felur hún í sér alla hluti sem hafa verið settir í körfuna og samantekt pöntunarinnar. Það gerir viðskiptavininum einnig kleift að beita eða fjarlægja kynningarkóða.

Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur. Hún styður einnig tengilinn **Til baka í verslun**. Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.

Í körfueiningunni eru gögn byggð á auðkenni körfunnar. Auðkenni körfunnar er vafrakaka sem er fáanleg á þessu svæði.

## <a name="cart-module-properties-and-slots"></a>Eiginleikar og hólf körfueininga

Körfueiningin er með eiginleikann **Fyrirsögn** sem hægt er að stilla á gildi eins og **Innkaupapoki** og **Vörur í körfunni þinni**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Einingar sem hægt er að nota í körfueiningu

- **Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni. Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS). Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“
- **Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu. Verslunarvalseiningin er samþætt við Bing Maps Geocoding forritunarviðmót (API) landskóðunar til að umbreyta staðsetningunni í breiddar- og lengdargráðu. Bing Maps API lykils er krafist og bæta verður honum við Retail sameiginlegar færibreytusíðuna í Dynamics 365 Retail. Þessi eining styður tvo eiginleika, **Leitarradíus** og **Tengil í þjónustuskilmála**. Eiginleikinn **Leitarradíus** skilgreinir leitarradíus fyrir verslanir, í mílum. Ef ekkert gildi er tilgreint er sjálfgefinn leitarradíus notaður, 50 mílur. Ef Bings kort eða utanaðkomandi þjónusta er notuð er hægt að nota eiginleikann **Tengill í þjónustuskilmála** til að veita tengil á þjónustuskilmálana. Þjónustuskilmálatengils er krafist fyrir þjónustuna Bing Maps. 

## <a name="cart-module-settings"></a>Stillingar körfueiningar

Körfueiningar hafa eftirfarandi stillingar sem hægt er að stilla á **Svæðisstillingar \> Viðbætur**:

- **Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager. Þessi úttekt á birgðum er gerð bæði fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina. Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð.
- **Birgðabiðminni** - Þessi eiginleiki er notaður til að tilgreina biðminnisnúmer fyrir birgðir. Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu. Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager. Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir og birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.
- **Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**. Hægt er að stilla þessa leið á vettvangsstigi. Þessar stillingar gera smásölum færa viðskiptavininn til baka á heimasíðuna eða aðra síðu á vefsvæðinu.

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce. Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Bæta körfueiningu við síðu

Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til brot sem er nefnt **Körfubrot** og bættu körfueiningunni við það.
1. Bæta fyrirsögn við körfueininguna.
1. Bættu verslunarvalseiningu við körfueininguna.
1. Vistaðu brotið, ljúktu við að breyta því og birtu það.
1. Búðu til sniðmát sem heitir **Körfusniðmát** og bættu körfubrotinu sem þú bjóst til við það.
1. Vistaðu sniðmátið, ljúktu við að breyta því og birtu það.
1. Búðu til síðu sem notar nýja sniðmátið.
1. Vistaðu og forskoðaðu síðuna.
1. Ljúktu við að breyta síðunni, vistaðu hana og birtu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupkassaeining](add-buy-box.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
