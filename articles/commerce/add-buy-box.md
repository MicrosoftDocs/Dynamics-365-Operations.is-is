---
title: Kaupkassaeining
description: Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
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
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811142"
---
# <a name="buy-box-module"></a>Kaupkassaeining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Hugtakið *kaupkassi* vísar venjulega til svæðisins á vöruupplýsingasíðunni sem er „yfir brotinu“ og hýsir allar mikilvægustu upplýsingarnar sem þarf til að kaupa vöru. (Svæði sem er „fyrir ofan brotið“ er sýnilegt þegar síðunni er fyrst hlaðið þannig að notendur þurfa ekki að fletta niður til að sjá hana.)

Kaupkassaeining er sérstakur gámur sem er notaður til að hýsa allar einingar sem sýndar eru á kaupkassasvæðinu á upplýsingasíðu vöru.

Vefslóð upplýsingasíðu inniheldur afurðakennið. Allar upplýsingar sem krafist er til að skila kaupkassaeiningar eru dregnar af þessu afurðakenni. Ef afurðakenni er ekki gefið upp verður kaupkassaeiningin ekki gefin rétt upp á síðu. Þess vegna er ekki hægt að nota kaupkassaeiningar á síðu sem er ekki með afurðasamhengi (til dæmis heimasíða eða markaðssíðu).

## <a name="buy-box-module-properties-and-slots"></a>Eiginleikar og hólf kaupkassaeininga 

Sem gámur stjórnar kaupkassaeining sumum grunneiginleikum, svo sem breiddinni. Breiddarstillingin ákvarðar hvort einingarnar í gámnum verða að passa innan í þann gám eða hvort þær geta fyllt skjáinn.

Á vöruupplýsingasíðu er kaupkassa skipt í tvö svæði: miðlasvæði til vinstri og innihaldssvæði til hægri. Þessi tvö svæði eru táknuð með hólfum í kaupkassaeiningunni. Hvert hólf er fyrirfram stillt til að samþykkja aðeins sérstakar einingar sem eru studdar af hólfinu. Til dæmis styður hólfið **Miðlar** eingöngu miðlasafnið.

Sjálfgefið er að hlutfall dálkabreiddar fyrir miðlasvæðið og innihaldssvæðið sé 2:1. Hins vegar er hægt að hnekkja dálkabreiddunum með þemanu. Að auki er svæðunum tveimur staflað í fartækjum, þannig að eitt svæði birtist fyrir neðan hitt svæðið.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Einingar sem hægt er að nota í kaupkassaeiningu

- **Miðlasafn** - Þessi eining er notuð til að sýna myndir af afurð á upplýsingasíðu afurðar. Það getur stutt eina til margar myndir. Það styður einnig smámyndir. Hægt er að raða smámyndunum annaðhvort lárétt (sem röð fyrir neðan myndina) eða lóðrétt (sem dálki við hliðina á myndinni). Hægt er að bæta miðlasafnseiningunni við hólfið **Miðlar** í kaupkassaeiningunni. Eins og stendur styður það aðeins myndir og myndbönd.
- **Titill afurðar** - Þessi eining sýnir titil afurðar á upplýsingasíðu afurðar. Sjálfgefið er að fyrirsagnarmerkið **H1** sé notað, en hægt er að breyta fyrirsagnarmerkinu eftir þörfum.
- **Afurðamat** - Þessi eining sýnir stjörnugjöf, byggð á mati viðskiptavina fyrir afurð. Kaupkassaeiningin sækir afurðareinkunnir fyrir hverja afurð frá matsþjónustunni.
- **Vöruverð** - Þessi eining sýnir verð vörunnar. Verðið felur í sér gegnumstrikunarverð og afslætti.
- **Afurðalýsing** - Þessi eining sýnir lýsingu vörunnar.
- **Afurðarstillingar** - Þessi eining sýnir stærð, stíl og víddir vörunnar. Hægt er að stafla víddarvalinu lóðrétt, eða það getur birst hlið við hlið. Þegar afurðarafbrigði er valið eru aðrir eiginleikar í kaupkassanum (til dæmis afurðarlýsingin og myndirnar) uppfærðir til að endurspegla upplýsingar um afbrigðið.
- **Afurðamagn** - Þessi eining er notuð til að stilla magn afurðarinnar. Stilling takmarkar magn vöru eða afbrigði sem hægt er að bæta í körfuna.
- **Bæta í körfu** - Þessi eining er notuð til að framkvæma aðgerðina „bæta við körfu“. Aðeins er hægt að setja afurð eða afbrigði í körfuna. Með öðrum orðum er ekki hægt að setja aðalafurð í körfuna. Einingin er með eiginleikann **Fara í körfu** sem vefhöfundur getur stillt. Þegar þessi eiginleiki er stilltur á **Satt** er notandinn færður á körfusíðuna í hvert skipti sem aðgerðin „setja í körfu“ er sett af stað. Þegar hann er stilltur á **Rangt** getur viðskiptavinurinn haldið áfram að fletta á vöruupplýsingasíðunni eftir að hlutum er bætt í körfuna.
- **Bæta á óskalista** - Þessi eining er notuð til að bæta hlut við óskalista viðskiptavinarins. Aðeins er hægt að setja afurð eða afbrigði á óskalistann. Að auki verður viðskiptavinurinn að vera skráður inn á síðuna. Einingin felur í sér villuhöndlun rökfræði til að ganga úr skugga um að bæði þessi skilyrði séu uppfyllt.
- **Finna í verslun** - Þessi eining kveikir á flæðinu „kaupa á netinu, sækja í verslun“.
- **Sækja í verslun** - Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Sjálfgefið er að þessi eining sýnir verslanir sem eru innan 50 mílna radíuss frá staðsetningu viðskiptavinarins. Hins vegar er hægt að aðlaga leitaradíusinn í einingunni. Fyrir hverja verslun er úttekt á birgðum gerð, ef kveikt er á virkni birgðaeftirlitsins og viðeigandi skilaboð eru sýnd um að vara sé á lager eða ekki á lager.
- **Leita að verslunum með Bing Maps** – Hægt er að nota þessa einingu í einingunni Sækja í verslun. Hún gerir viðskiptavinum kleift að leita að verslunum með því að slá inn staðsetningu. Bing Maps forritunarviðmót (API) landskóðunar er notað til að umbreyta tilgreindri staðsetningu í breiddar- og lengdargráðu. Ef þessi eining er notuð eru aðeins verslanir sem eru nálægt núverandi staðsetningu viðskiptavinarins sýndar og viðskiptavinurinn getur ekki leitað að öðrum stað.
- **Eining með fjölbreyttu efni** - Þessi eining getur sýnt skilaboð sem höfundur eða smásali vefsíðunnar vill auglýsa í kaupkassanum, eins og „Vegna vandamála við pöntun skal hafa samband við 1-800-FABRIKAM“ eða „Ókeypis sending á pöntunum yfir $100.“ Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS).

## <a name="buy-box-module-settings"></a>Stillingar kaupkassaeiningar

Kaupkassaeiningar hafa þrjár stillingar sem hægt er að stilla:

- **Hámarksmagn** - Hámarksfjöldi hvers hlutar sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager. Þessi úttekt á birgðum er gerð bæði fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina. Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð.
- **Biðminni birgða** - Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu. Þess vegna er hægt að skilgreina biðminni fyrir birgðir. Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager. Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir, þannig að birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.

## <a name="retail-server-interaction"></a>Samskipti Retail Server

Kaupkassaeiningin sækir upplýsingar um vörur með API fyrir Retail Server. Afurðakenni af upplýsingasíðu vöru er notað til að sækja allar upplýsingar.

## <a name="add-a-buy-box-module-to-a-page"></a>Bæta kaupkassaeiningu við síðu

Fylgdu þessum skrefum til að bæta kaupkassaeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Búðu til brot sem er nefnt **kaupa kassabrot** og bættu kaupkassaeiningunni við það.
1. Í hólfinu **Miðlar** í kaupkassaeiningunni bætirðu við miðlasafnseiningu.
1. Í hólfinu **Efni** í kaupkassaeiningunni bætirðu við eftirfarandi einingum: afurðarheiti, afurðarmati, vöruverði, vörulýsingu, afurðarstillingu, setja í körfu, bæta við óskalista og finna í verslun. Þú getur endurraðað einingunum í hólfinu **Efni** til að ná tilætluðu útliti.
1. Veldu eininguna Finna í verslun. Í hólfinu innan í einingunni bætirðu við einingunni Sækja í verslun.
1. Í hólfinu í einingunni Sækja í verslun bætirðu við verslunarleit með einingunni Bing Maps.
1. Athuga á síðunni og birtu hana.
1. Búðu til sniðmát fyrir vöruupplýsingasíðu og nefndu það **PDP-sniðmát**.
1. Bæta við sjálfgefinni síðu.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við kaupkassabroti.
1. Vistaðu sniðmátið, athugaðu það og gefðu það út.
1. Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **PDP-síðu**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við kaupkassabroti.
1. Vistaðu og forskoðaðu síðuna. Bættu færibreytustreng fyrirspurnar **?productid=&lt;product id&gt;** við slóðina á forskoðunarsíðunni. Þannig er vörusamhengið notað til að hlaða og birta forskoðunarsíðuna.
1. Athuga á síðunni og birtu hana. Kaupkassi ætti að birtast á upplýsingasíðu afurða.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
