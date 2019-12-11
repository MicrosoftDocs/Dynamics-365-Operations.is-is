---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696762"
---
# <a name="cart-module"></a>Körfueining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Körfueining er gámur sem er notaður til að hýsa alla einingar sem þarf til að sýna hluti sem eru í körfunni. Til dæmis felur hún í sér alla hluti sem hafa verið settir í körfuna, samantekt pöntunarinnar og kynningarkóða.

Í körfueiningunni eru gögn byggð á auðkenni körfunnar. Auðkenni körfunnar er vafrakaka sem er fáanleg á þessu svæði.

## <a name="cart-module-properties-and-slots"></a>Eiginleikar og hólf körfueininga

Sem gámur stjórnar körfueining sumum grunneiginleikum, svo sem fyrirsögn og breidd. Yfirskriftin er venjulega texti eins og **Innkaupapoki**, **Karfan þín** eða **Vörur í körfunni þinni**. Breiddarstillingin ákvarðar hvort einingarnar í gámnum verða að passa innan í þann gám eða hvort þær geta fyllt skjáinn.

Körfusíðunni er skipt í mörg svæði: línuatriði körfu, samantekt pöntunar og kassa og virknina „finna í verslun“. Hverju svæði er varpað í hólf í körfueiningunni og sérhvert hólf samþykkir fyrirfram skilgreindar einingar.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Einingar sem hægt er að nota í körfueiningu

- **Línuatriði körfu** - Þessi eining sýnir yfirlit yfir hvert atriði sem hefur verið bætt í körfuna. Upplýsingarnar innihalda afurðarheiti, valdar víddir, verð, magn og afslætti. Þessi eining styður einnig aðgerðir eins og „fjarlægja úr körfu“ og „bæta við óskalista.“ Fyrir hvert línuatriði er möguleiki að senda vöruna eða sækja hana úr versluninni. Þennan valkost verður að stilla sérstaklega í einingunni Sækja í verslun.
- **Samantekt pöntunar** - Þessi eining sýnir pöntunarsamantekt. Upplýsingarnar innihalda millisamtölu, sendingu, skatta og sparnað. Hægt er að stilla fyrirsögn fyrir þessa einingu.
- **Kynningarkóði** - Þessi eining gerir viðskiptavininum kleift að innleysa kynningarkóða. Hægt er að nota eða fjarlægja kynningarkóða.
- **Greiðsluferli** - Þessi eining byrjar á greiðsluferlisaðgerðinni og vísar notandanum á greiðslusíðuna. Þrjá tengla verður að stilla fyrir þessa einingu:

    - **Greiðsluferli** - Þessi tengill neyðir viðskiptavini til að skrá sig inn ef þeir eru ekki þegar innskráðir.
    - **Greiðsla sem gestur** - Þessi tengill gerir kleift að nafnlausir viðskiptavinir setji inn pantanir. Hann er aðeins sýndur þegar viðskiptavinir eru ekki innskráðir.
    - **Til baka í verslun** - Þessi tengill gerir viðskiptavinum kleift að fara á heimasíðuna eða aðra síðu, svo að þeir geti haldið áfram að versla.

- **Eining með fjölbreyttu efni** - Þessi eining styður sérsniðin skilaboð í körfueiningunni. Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS). Hægt er að bæta við hvaða skilaboðum sem er, svo sem „Fyrir vandamál með pöntunina, hafið samband við 1-800-Fabrikam.“
- **Sækja í verslun** - Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Sjálfgefið er að þessi eining sýnir verslanir sem eru innan 50 mílna radíuss frá staðsetningu viðskiptavinarins. Hins vegar er hægt að aðlaga leitaradíusinn í einingunni. Fyrir hverja verslun er úttekt á birgðum gerð, ef kveikt er á virkni birgðaeftirlitsins og viðeigandi skilaboð eru sýnd um að vara sé á lager eða ekki á lager.
- **Leita að verslunum með Bing Maps** – Hægt er að nota þessa einingu í einingunni Sækja í verslun. Hún gerir viðskiptavinum kleift að leita að verslunum með því að slá inn staðsetningu. Bing Maps forritunarviðmót (API) landskóðunar er notað til að umbreyta þá staðsetningu sem viðskiptavinurinn sló inn í breiddar- og lengdargráðu. Ef þessi eining er ekki notuð eru aðeins verslanir sem eru nálægt núverandi staðsetningu viðskiptavinarins sýndar og viðskiptavinurinn getur ekki leitað að öðrum stað.

## <a name="cart-module-settings"></a>Stillingar körfueiningar

Körfueiningar hafa þrjár stillingar sem hægt er að stilla:

- **Hámarksmagn** - Hámarksfjöldi hvers hlutar sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager. Þessi úttekt á birgðum er gerð bæði fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina. Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð.
- **Biðminni birgða** - Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu. Þess vegna er hægt að skilgreina biðminni fyrir birgðir. Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager. Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir, þannig að birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.

## <a name="retail-server-interaction"></a>Samskipti Retail Server

Körfueiningin sækir upplýsingar um vörur með API fyrir Retail Server. Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Retail Server.

## <a name="add-a-cart-module-to-a-page"></a>Bæta körfueiningu við síðu

Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til brot sem er nefnt **körfubrot** og bættu körfueiningunni við það.
1. Í hólfinu **Línuatriði körfu** í körfueiningunni bætirðu við einingu fyrir línuatriði körfu.
1. Í hólfinu **Samantekt pöntunar** bætirðu við einingu fyrir samantekt á pöntun.
1. Í hólfinu **Kynningarkóði** bætirðu við einingu fyrir kynningarkóða.
1. Í hólfinu **Greiðsluferli** bætirðu við einingu fyrir greiðsluferli.
1. Í hólfinu **Finna í verslun** bætirðu við einingu til að sækja í verslun.
1. Í einingunni Sækja í verslun velurðu hólfið **Leita að verslun** og bætir við leit að verslunum með einingunni Bing Maps.
1. Athugaðu brotið og birtu það.
1. Búðu til sniðmát sem heitir **körfusniðmát** og bættu körfubrotinu sem þú bjóst til við það.
1. Vistaðu sniðmátið, athugaðu það og gefðu það út.
1. Búðu til síðu sem notar nýja sniðmátið.
1. Vistaðu og forskoðaðu síðuna.
1. Athuga á síðunni og birtu hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupkassaeining](add-buy-box.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
