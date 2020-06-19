---
title: Kaupkassaeining
description: Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 583937be92b62991cd13f0806df4a0a6c9ac049c
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411343"
---
# <a name="buy-box-module"></a>Kaupkassaeining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um kaupakassaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Hugtakið *kaupkassi* vísar venjulega til svæðisins á vöruupplýsingasíðunni sem er „yfir brotinu“ og hýsir allar mikilvægustu upplýsingarnar sem þarf til að kaupa vöru. (Svæði sem er „fyrir ofan brotið“ er sýnilegt þegar síðunni er fyrst hlaðið þannig að notendur þurfa ekki að fletta niður til að sjá hana.)

Kaupkassaeining er sérstakur gámur sem er notaður til að hýsa allar einingar sem sýndar eru á kaupkassasvæðinu á upplýsingasíðu vöru.

Vefslóð upplýsingasíðu inniheldur afurðakennið. Allar upplýsingar sem krafist er til að skila kaupkassaeiningar eru dregnar af þessu afurðakenni. Ef afurðakenni er ekki gefið upp verður kaupkassaeiningin ekki gefin rétt upp á síðu. Þess vegna er aðeins hægt að nota innkaupakassaeiningar á síðum sem eru með samhengi vöru. Til að nota það á síðu sem er ekki með samhengi vöru (til dæmis heimasíðu eða markaðssíðu) verður þú að gera viðbótarstillingar.

Eftirfarandi mynd sýnir dæmi um kaupgluggaeiningu á upplýsingasíðu afurðar.

![Dæmi um kaupgluggaeiningu](./media/ecommerce-pdp-buybox.PNG)

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
- **Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu. Frekari upplýsingar um þessa einingu er að finna í [Verslunarvalseining](store-selector.md).

## <a name="buy-box-module-settings"></a>Stillingar kaupkassaeiningar

Hægt er að skilgreina eftirfarandi stillingar fyrir kaupgluggaeiningar á **Stillingar svæðis \> viðbætur**:

- **Hámarksmagn körfulínu** - Þessi eiginleiki er notaður til að sýna hámarksfjölda hverrar vöru sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðir** - Frekari upplýsingar um hvernig á að nota birgðastillingar er að finna í [Nota birgðastillingar](inventory-settings.md).
- **Bæta í körfu** - Þessi eiginleiki er notaður til að sýna hegðun eftir að vöru hefur verið bætt í körfuna. Mögulegu gildin eru **Fara í körfu**, **Ekki fara í körfu** og **Sýna tilkynningar**. Þegar gildið er stillt á **Fara í körfu** er notendum vísað á körfusíðuna eftir að hafa bætt við vöru. Þegar gildið er stillt á **Ekki fara í körfu** er notendum ekki vísað á körfusíðuna eftir að hafa bætt við vöru. Þegar gildið er stillt á **Sýna tilkynningar** fá notendur staðfestingu og geta haldið áfram að vafra á upplýsingasíðu afurðar. 

    Eftirfarandi mynd sýnir dæmi um „bætt í körfu“ tilkynningu á Fabrikam-svæðinu.

    ![Dæmi um tilkynningareining](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Kaupgluggaeiningin sækir afurðarupplýsingar með því að nota forritunarviðmót Commerce Scale Unit. Afurðakenni af upplýsingasíðu vöru er notað til að sækja allar upplýsingar.

## <a name="add-a-buy-box-module-to-a-page"></a>Bæta kaupkassaeiningu við síðu

Fylgdu þessum skrefum til að bæta kaupkassaeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Síðubrot** og veldu **Nýtt** til að búa til nýtt síðubrot.
1. Í svarglugganum **Nýtt síðubrot** skal velja eininguna **Kaupkassi**.
1. Undir **Heiti síðubrots** skal slá inn heitið **Kaupkassabrot** og síðan velja **Í lagi**.
1. Í hólfinu **Efnissafn** í kaupgluggaeiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Efnissafn** og síðan velja **Í lagi**.
1. Í hólfinu **Verslunarval** í kaupgluggaeiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Verslunarval** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.
1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **PDP-sniðmát** og velja síðan **Í lagi**.
1. Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á sjálfgefnu síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við síðubroti**.
1. Í svarglugganum **Velja síðubrot** skal velja síðubrotið **Kaupkassabrot** sem var búið til áður og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja sniðmátið **PDP-sniðmát**. Undir **Síðuheiti** skal færa inn **PDP-síðu** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við síðubroti**.
1. Í svarglugganum **Velja síðubrot** skal velja síðubrotið **Kaupkassabrot** sem var búið til áður og síðan velja **Í lagi**.
1. Vistaðu og forskoðaðu síðuna. Bættu færibreytustreng fyrirspurnar **?productid=&lt;product id&gt;** við slóðina á forskoðunarsíðunni. Þannig er vörusamhengið notað til að hlaða og birta forskoðunarsíðuna.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana. Kaupkassi ætti að birtast á upplýsingasíðu afurða.

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
