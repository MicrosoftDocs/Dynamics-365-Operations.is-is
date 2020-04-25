---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261422"
---
# <a name="cart-module"></a>Körfueining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Körfueining sýnir hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa. Einingin sýnir einnig samantekt á pöntun og gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.

Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur. Hún styður einnig tengilinn **Til baka í verslun**. Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.

Í körfueiningunni eru gögn byggð á körfuauðkenninu, sem er vafrakaka sem hægt er að nálgast á vefsvæðinu.

## <a name="cart-module-properties-and-slots"></a>Eiginleikar og hólf körfueininga

Körfueiningin er með eiginleikann **Fyrirsögn** sem hægt er að stilla á gildi eins og **Innkaupapoki** og **Vörur í körfunni þinni**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Einingar sem hægt er að nota í körfueiningu

- **Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni. Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS). Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“
- **Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu. Fyrir frekari upplýsingar um þessa einingu, sjá [Verslunarvalseiningu](store-selector.md).


## <a name="module-properties"></a>Eiginleikar einingar

Körfueiningar hafa eftirfarandi stillingar sem hægt er að stilla á **Svæðisstillingar \> Viðbætur**:

- **Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager. Þessi úttekt á birgðum er gerð fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina. Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð. Nánari upplýsingar um hvernig á að stilla birgðastillingar í bakvinnslu er að finna í [Reikna birgðaframboð fyrir smásölurásir](calculated-inventory-retail-channels.md).
- **Birgðabiðminni** - Þessi eiginleiki er notaður til að tilgreina biðminnisnúmer fyrir birgðir. Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu. Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager. Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir og birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.
- **Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**. Hægt er að stilla leiðina á vettvangsstigi, sem gerir smásöluaðilum kleift að fara með viðskiptavininn aftur á heimasíðuna eða aðra síðu á síðunni.

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce. Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Bæta körfueiningu við síðu

Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til brot sem er nefnt **Körfubrot** og bættu körfueiningunni við nýja brotið.
1. Bæta fyrirsögn við körfueininguna.
1. Bættu verslunarvalseiningu við körfueininguna.
1. Vistaðu brotið, ljúktu við að breyta því og birtu síðan brotið.
1. Búðu til sniðmát sem heitir **Körfusniðmát** og bættu við körfubrotinu sem þú bjóst til.
1. Vistaðu sniðmátið, ljúktu við að breyta því og birtu síðan sniðmátið.
1. Búðu til síðu sem notar nýja sniðmátið.
1. Vistaðu og forskoðaðu síðuna.
1. Ljúktu við að breyta síðunni og birtu hana síðan.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Vista valeiningu](store-selector.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining pöntunarstaðfestingar](order-confirmation-module.md)

[Eining síðuhauss](author-header-module.md)

[Eining síðufótar](author-footer-module.md)

[Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md)
