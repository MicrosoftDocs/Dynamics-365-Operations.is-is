---
title: Kaupkassaeining
description: Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 35b7027e0f0b680dd82ebfcea754fef1617c0163
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261399"
---
# <a name="buy-box-module"></a>Kaupkassaeining


[!include [banner](includes/banner.md)]

Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Hugtakið *kaupkassi* vísar venjulega til svæðisins á vöruupplýsingasíðunni sem er „yfir brotinu“ og hýsir allar mikilvægustu upplýsingarnar sem þarf til að kaupa vöru. (Svæði sem er „fyrir ofan brotið“ er sýnilegt þegar síðunni er fyrst hlaðið þannig að notendur þurfa ekki að fletta niður til að sjá hana.)

Kaupkassaeining er sérstakur gámur sem er notaður til að hýsa allar einingar sem sýndar eru á kaupkassasvæðinu á upplýsingasíðu vöru.

Vefslóð upplýsingasíðu inniheldur afurðakennið. Allar upplýsingar sem krafist er til að skila kaupkassaeiningar eru dregnar af þessu afurðakenni. Ef afurðakenni er ekki gefið upp verður kaupkassaeiningin ekki gefin rétt upp á síðu. Þess vegna er aðeins hægt að nota innkaupakassaeiningar á síðum sem eru með samhengi vöru. Til að nota það á síðu sem er ekki með samhengi vöru (til dæmis heimasíðu eða markaðssíðu) verður þú að gera viðbótarstillingar.

## <a name="buy-box-module-properties-and-slots"></a>Eiginleikar og hólf kaupkassaeininga 

Á vöruupplýsingasíðu er kaupkassa skipt í tvö svæði: miðlasvæði til vinstri og innihaldssvæði til hægri. Sjálfgefið er að hlutfall breiddar dálks fjölmiðlasvæðisins og breiddar dálks innihaldssvæðisins sé 2:1. Í fartækjum er svæðunum tveimur staflað, þannig að eitt svæði birtist fyrir neðan hitt svæðið. Hægt er að nota þemu til að sérsníða súlubreidd og staflaröðun.

Kaupkassaeining gefur titil, lýsingu, verð og einkunnir afurðar. Hún gerir viðskiptavinum einnig kleift að velja vöruafbrigði sem hafa mismunandi afurðareigindir, svo sem stærð, stíl og lit. Þegar afurðarafbrigði er valið eru aðrir eiginleikar í kaupkassanum (til dæmis afurðarlýsingin og myndirnar) uppfærðir til að endurspegla upplýsingar um afbrigðið. 

Magnval er veitt svo að viðskiptavinir geti tilgreint magn varanna sem á að kaupa. Hægt er að skilgreina hámarksmagn sem hægt er að kaupa í stillingum vefsvæðisins.

Í kaupboxinu geta viðskiptavinir einnig framkvæmt aðgerðir eins og að bæta vöru við körfuna, bæta vöru við óskalistann sinn og velja afhendingarstað. Þessar aðgerðir er hægt að framkvæma á afurð eða afurðarafbrigði. Til að bæta afurð við óskalista verður viðskiptavinurinn að vera skráður inn.

Þemu er hægt að nota til að fjarlægja eða breyta röð afurðaeiginleika og aðgerðastýringa kaupkassa. 

## <a name="module-properties"></a>Eiginleikar einingar

- **Merki fyrirsagna** – Þessi eiginleiki skilgreinir merki fyrirsagna fyrir afurðarheitið. Ef kaupkassinn er efst á síðunni ætti að stilla þennan eiginleika á **h1** til að uppfylla aðgengisstaðla. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Einingar sem hægt er að nota í kaupkassaeiningu

- **Miðlasafn** - Þessi eining er notuð til að sýna myndir af afurð á upplýsingasíðu afurðar. Það getur stutt eina til margar myndir. Það styður einnig smámyndir. Hægt er að raða smámyndunum annaðhvort lárétt (sem röð fyrir neðan myndina) eða lóðrétt (sem dálki við hliðina á myndinni). Hægt er að bæta miðlasafnseiningunni við hólfið **Miðlar** í kaupkassaeiningunni. Eins og stendur styður það aðeins myndir. 
- **Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu. Fyrir frekari upplýsingar um þessa einingu, sjá [Verslunarvalseiningu](store-selector.md).

## <a name="buy-box-module-settings"></a>Stillingar kaupkassaeiningar

Kaupkassaeiningar hafa þrjár stillingar sem hægt er að stilla á **Svæðisstillingar \> Viðbætur**:

- **Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager. Þessi úttekt á birgðum er gerð fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina. Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð. Nánari upplýsingar um hvernig á að stilla birgðastillingar í bakvinnslu er að finna í [Reikna birgðaframboð fyrir smásölurásir](calculated-inventory-retail-channels.md).

- **Birgðabiðminni** - Þessi eiginleiki er notaður til að tilgreina biðminnisnúmer fyrir birgðir. Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu. Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager. Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir og birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Kaupkassaeiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce. Afurðakenni af upplýsingasíðu vöru er notað til að sækja allar upplýsingar.

## <a name="add-a-buy-box-module-to-a-page"></a>Bæta kaupkassaeiningu við síðu

Fylgdu þessum skrefum til að bæta kaupkassaeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til brot sem er nefnt **kaupa kassabrot** og bættu kaupkassaeiningunni við það.
1. Í hólfinu **Miðlar** í kaupkassaeiningunni bætirðu við miðlasafnseiningu.
1. Í hólfinu **Verslunarval** í kaupkassaeiningunni skal bæta við verslunarvalseiningunni.
1. Athuga á síðunni og birtu hana.
1. Búðu til sniðmát fyrir vöruupplýsingasíðu og nefndu það **PDP-sniðmát**.
1. Bæta við sjálfgefinni síðu.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við kaupkassabroti.
1. Vistaðu sniðmátið, ljúktu við að breyta því og birtu það.
1. Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **PDP-síðu**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við kaupkassabroti.
1. Vistaðu og forskoðaðu síðuna. Bættu færibreytustreng fyrirspurnar **?productid=&lt;product id&gt;** við slóðina á forskoðunarsíðunni. Þannig er vörusamhengið notað til að hlaða og birta forskoðunarsíðuna.
1. Vistaðu síðuna, ljúktu við að breyta henni og birtu hana. Kaupkassi ætti að birtast á upplýsingasíðu afurða.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Vista valeiningu](store-selector.md)

[Hólfeining](add-container-module.md)

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining pöntunarstaðfestingar](order-confirmation-module.md)

[Eining síðuhauss](author-header-module.md)

[Eining síðufótar](author-footer-module.md)

[Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md)
