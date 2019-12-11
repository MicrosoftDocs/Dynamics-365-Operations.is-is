---
title: Yfirlit yfir upplýsingasíður afurða
description: Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697866"
---
# <a name="overview-of-product-details-pages"></a>Yfirlit yfir upplýsingasíður afurða

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

PDP veitir nákvæmar upplýsingar um afurð og gerir viðskiptavinum kleift að velja afurðakosti eins og stærð, stíl og lit. PDP ætti að sýna allar vöruupplýsingar sem viðskiptavinur þarfnast til að taka ákvörðun um kaup.

Eftirfarandi skýringarmynd sýnir dæmi um PDP.

![Dæmi um upplýsingasíðu afurðar](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Einingar síðuhauss og síðufótar

Efst á PDP er haus sem sýnir alla vöruflokka og aðrar síður sem smásalinn vill að viðskiptavinir skoði. Neðst á síðunni er síðufótur sem inniheldur fljótlega tengla á ýmis efni sem kaupendur gætu haft áhuga á.

## <a name="buy-box-module"></a>Kaupgluggaeining

Mikilvægasta einingin á PDP er einingin fyrir kaupglugga. Þess vegna er það fyrsta atriðið í aðalhlutanum á síðunni. Kaupgluggaeining er gámaeining og hýsir nokkrar einingar sem innihalda mikilvægustu upplýsingar um vöruna. Þessar upplýsingar innihalda afurðaheiti, afurðamyndir, lýsingu, verð og afurðaeinkunn.

Kaupgluggaeiningin gerir viðskiptavininum kleift að velja vöruvalkosti (til dæmis stærð, stíl og lit) og bæta vörunni í körfuna. Hún gerir viðskiptavininum einnig kleift að kaupa vöruna á netinu og sækja hana í verslun. Kaupið á netinu og sótt í verslunareininguna notar samþættingu við forritunarviðmót Bing Maps forrita (API) til að finna nálægar verslanir eða verslanir á öðrum stað sem viðskiptavinurinn tilgreinir.

Kaupgluggaeining þarf afurðakenni. Þetta auðkenni er dregið af samhengi síðunnar. Ef kaupgluggaeiningu er bætt við síðu þar sem samhengi síðunnar er ekki með afurðakenni, mun hún ekki birta upplýsingarnar rétt.

## <a name="product-specifications-module"></a>Afurðaskilgreiningaeining

Hægt er að nota afurðaskilgreiningareininguna til að sýna frekari upplýsingar um vöruna. Þessar upplýsingar eru fengnar frá afurðareigindum í Dynamics 365 Retail. Vörulýsingareiningin sýnir alla eiginleika þar sem eiginleikinn **sýnilegt** er stilltur á **satt**. Það þarf afurðakenni til að sækja afurðareigindir.

## <a name="recommendations-module"></a>Tillagnaeining

Tillagnaeiningin er mikilvæg einingin á PDP. Meðan viðskiptavinir leita að vörum ætti að kynna þeim fleiri vöruvalkosti svo þeir geti fundið réttu vöruna og gert kaup. Tilmæli hjálpa viðskiptavinum að uppgötva tengt efni og halda áfram að versla.

Mismunandi gerðir tillagna eru tiltækar:

- Listinn **Fólki líkar einnig** er byggður á vélanámi. Hann notar viðskiptasögu annarra viðskiptavina til að veita ráðleggingar. Þessi listi er búinn til með ráðleggingaþjónustunni og líkist listunum „Viðskiptavinir sem keyptu þetta keyptu líka ...“. Afurðakennis er krafist til að búa til þennan lista.
- Listann **Tengt** er hægt að stilla lista fyrir vöru í Retail. Til dæmis, fyrir brúna handtösku úr leðri, er hægt að stilla fleiri handtöskur úr leðri eða hannaðar til að nota í ferðalögum fyrir viðkomandi lista. Aðrar gerðir tengdra lista, svo sem **Aukahlutir** og **Meira eins og þetta** er einnig er hægt að stilla í Retail. Afurðakennis er krafist til að búa til þennan lista. Þess vegna, ef því er bætt við heimasíðuna, þar sem samhengi síðunnar inniheldur ekki afurðakenni, verður listinn tómur.
- Algrímmyndaðir myndaðir tillagnalistar, eins og **Vinsælt**, **Mest selt** og **Nýtt** má nota á PDP. Þó að þessir listar séu kannski ekki í beinum tengslum við vöruna á PDP, eru þeir önnur leið til að hjálpa viðskiptavinum að finna vörur sem gætu haft áhuga á þeim. Þessar gerðir lista þurfa ekki afurðakenni. Þetta eru almennir listar sem eru búnir til út frá innkaupamynstrum á vefnum.
- Ritstjórnarlistar eru handvirkir listar. Til dæmis gæti smásali ákveðið að setja handvirkt saman lista yfir vörur sem hann vill sýna.

## <a name="ratings-and-reviews-module"></a>Einkunna- og umsagnaeining

Einingin fyrir einkunnir og umsagnir sýnir einkunnir og umsagnir sem aðrir viðskiptavinir hafa gefið. Hún gerir viðskiptavinum einnig kleift að skrifa sína eigin umsögn um afurðina. Að auki inniheldur hún súlurit sem sýnir einkunnagjöf fyrir vöruna. Frekari upplýsingar eru í [Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Markaðssetningareiningar

Ef markaðsefni er einstakt fyrir ákveðna afurð er hægt að bæta hvaða markaðsseiningu sem er við PDP. Þú getur bætt markaðsseiningum við PDP með því að „auðga“ síðuna. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir heimasíðuna](quick-tour-home-page.md)

[Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu](category-search-page-overview.md)

[Yfirlit yfir á körfu- og greiðsluferlissíður](quick-tour-cart-checkout.md)

[Yfirlit yfir síður reikningastjórnunar](quick-tour-account-management.md)
