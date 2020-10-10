---
title: Vista valeiningu
description: Þetta efni fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 4438e46d4653a0cd2060092695f08613cd696f4e
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818251"
---
# <a name="store-selector-module"></a>Vista valeiningu

[!include [banner](includes/banner.md)]

Þetta efni fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Viðskiptavinir geta notað valeiningu verslunar til að sækja vöru í valdri verslun eftir kaup á netinu. Í Commerce-útgáfu 10.0.13 felur valeining verslunar einnig í sér fleiri möguleika sem geta birt **Finna verslun** síðu sem sýnir nálægar verslanir.

Valeining verslunar leyfir notendum að slá inn staðsetningu (borg, ríki, aðsetur og svo framvegis) til að leita að verslunum innan leitarradíuss. Þegar einingin er opnuð í fyrsta skipti, notar hún staðsetningu á vafra viðskiptavinarins til að finna verslanir (ef samþykki er veitt).

## <a name="store-selector-module-usage-in-e-commerce"></a>Notkun verslunarvalseiningar í e-Commerce

- Hægt er að nota valeiningu verslunar á upplýsingasíðu afurðar til að velja verslun til að sækja í.
- Hægt er að nota valeiningu verslunar á körfusíðu til að velja verslun til að sækja í.
- Hægt er að nota valeiningu verslunar á sjálfstæðri síðu sem sýnir allar tiltækar verslanir.

## <a name="bing-maps-integration"></a>Samþætting Bing-korta

Valeining verslunar er samþætt við [REST forritunarviðmót Bing-korta](https://docs.microsoft.com/bingmaps/rest-services/) til að nota landkóðun og sjálfvirkar tillögur Bing. API-lykill Bing-korta er nauðsynlegur og verður að bæta honum við samnýtta færibreytusíðu í Commerce Headquarters. API-landkóðun er notuð til að umbreyta staðsetningu í gildi breiddar- og lengdargráða. Samþætting við API fyrir sjálfvirkar tillögur er notuð til að sýna leitartillögur þegar notendur slá inn staðsetningar í leitarreitinn.

Fyrir REST API sjálfvirkar tillögur, þarf að ganga úr skugga um að eftirfarandi vefslóðir séu leyfðar (einnig þekkt sem „undanþágulisti“) í öryggisreglum vefsvæðisins. Þessi uppsetning er gerð í Commerce-vefsmiðnum með því að bæta leyfðum vefslóðum við ýmsar öryggisleiðbeiningar fyrir vefsvæðið (t.d. **img-src**). Nánari upplýsingar er að finna í [Öryggisregla um innihald](manage-csp.md). 

- Í leiðbeininguna **connect-src** skal bæta við **&#42;.bing.com**.
- Í leiðbeininguna **img-src** skal bæta við **&#42;.virtualearth.net**.
- Í leiðbeininguna **script-src** skal **bæta við &#42;.bing.com, &#42;.virtualearth.net**.
- Í leiðbeininguna **script style-src** skal bæta við **&#42;.bing.com**.
 
## <a name="pickup-in-store-mode"></a>Sækja í verslun

Valeining verslunar styður stillinguna **Sækja í verslun** sem sýnir lista yfir verslanir þar sem hægt er að sækja vöru. Hún sýnir einnig opnunartíma verslunar og birgðir fyrir hverja verslun á listanum. Valeining verslunar krefst vörusamhengis til að sýna vöruframboð og leyfa notendum að bæta vörunni við körfuna, ef afhendingarsnið vörunnar er stillt á **sækja** í valdri verslun. Frekari upplýsingar er að finna í [Birgðastillingar](inventory-settings.md). 

Hægt er að bæta valeiningu verslunar við kaupgluggaeiningu á upplýsingasíðu afurðar til að sýna verslanir þar sem boðið er upp á að sækja vöruna. Það er einnig hægt að bæta við körfu mát. Í slíku tilfelli sýnir valeining verslunar valkosti til að sækja fyrir hverja vörulínu í körfunni. Einnig er hægt að bæta verslunarvaleiningunni við aðrar síður eða einingar með viðbótum og sérstillingum.

Til að þessar aðstæður geti virkað, þarf að skilgreina afurðir þannig að afhendingarmátann **sækja** er notað. Annars verður einingin ekki sýnd á síðum afurða. Frekari upplýsingar um hvernig á að skilgreina afhendingarmáta er að finna í [Setja upp afhendingarmáta](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Eftirfarandi mynd sýnir dæmi um verslunarvalseiningu sem er notuð á PDP.

![Dæmi um verslunarvalseiningu sem notuð er á PDP](./media/BOPIS.PNG)

## <a name="find-stores-mode"></a>Finna verslanir

Verslunarvaleiningin styður einnig stillinguna **Finna verslanir**. Hægt er að nota þessa stillingu til að búa til síðu fyrir staðsetningar verslana sem sýnir verslanir sem í boði eru og upplýsingar um þær. Í þessari stillingu virkar verslunarvaleiningin án vörusamhengis og er hægt að nota hana sem sjálfstæða einingu á hvaða síðu sem er. Að auki, ef kveikt er á viðeigandi stillingum fyrir eininguna, geta notendur valið verslun sem sína eftirlætis verslun. Þegar verslun er valin sem eftirlætis verslun, er auðkenni verslunarinnar geymt í vefkökum vafrans. Notandinn verður því að samþykkja kökur í skilaboðum um slíkt.

Eftirfarandi mynd sýnir dæmi um verslunarvaleiningu sem er notuð saman með kortaeiningu á staðsetningarsíðu verslunar.

![Dæmi um verslunarvaleiningu og kortaeiningu á staðsetningarsíðu verslunar.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Birta kort

Hægt er að nota verslunarvaleininguna saman með kortaeiningunni til að sýna staðsetningar verslana á korti. Frekari upplýsingar um kortaeininguna er að finna í [Kortaeining](map-module.md)

## <a name="store-selector-module-properties"></a>Eiginleikar verslunarvalseiningar

| Nafn eiginleika | Virði | lýsing |
|---------------|-------|-------------|
| Yfirskrift | Texti | Fyrirsögn einingarinnar. |
| Máti | **Finna verslanir** eða **Sækja í verslun** | Sniðið **Finna verslanir** sýnir tiltækar verslanir. Sniðið **Sækja í verslun** leyfir notendum að velja verslun til að sækja í. |
| Stíll | **Svargluggi** eða **Innfellt** | Hægt er að birta eininguna annaðhvort sem innfellda eða í svarglugga. |
| Nota sem valda verslun | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er stilltur á **Satt** geta notendur stillt æskilega verslun. Þessi eiginleiki krefst þess að notendur samþykki vefkökur í slíkum skilaboðum. |
| Sýna allar verslanir | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er stilltur á **Satt** geta notendur sleppt **Leitarradíus** og skoðað allar verslanir. |
| Valmöguleikar sjálfvirkrar tillögu: Hámarksfjöldi niðurstaða | Númer | Þessi eiginleiki skilgreinir hámarksfjölda af niðurstöðum sjálfvirkrar tillögu sem hægt er að sýna í gegnum API sjálfvirkrar tillögu Bing. |
| Leitarradíus | Númer | Þessi eiginleiki skilgreinir leitarradíus fyrir verslanir, í mílum. Ef ekkert gildi er tilgreint er sjálfgefinn leitarradíus upp á 50 mílur notaður. |
| Þjónustuskilmálar | URL |  Þessi eiginleiki tilgreinir vefslóð skilmála sem eru nauðsynlegir til að nota Bing-kortaþjónustuna. |

## <a name="add-a-store-selector-module-to-a-page"></a>Bæta við verslunarvalseiningu á síðu

Aðeins er hægt að nota eininguna **Sækja í verslun** á upplýsingasíðu afurðar og körfusíðum. Stilla þarf sniðið **Sækja í verslun** á eiginleikasvæði einingarinnar.

- Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við innkaupakassaeiningar, sjá [Kaupkassaeiningu](add-buy-box.md). 
- Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við körfueiningar, sjá [Körfueiningu](add-cart-module.md).

Til að skilgreina verslunarvaleininguna til að sýna tiltækar verslanir fyrir staðsetningarsíðu verslana, eins og á skýringarmyndinni sem sýnd var fyrr í þessu efnisatriði, skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Markaðssniðmát** og velja síðan **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja sniðmátið **Markaðssniðmát**. Undir **Síðuheiti** skal færa inn **Staðsetningar verslana** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf með tveimur dálkum** og síðan velja **Í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Stillið gildið **Dálkaskilgreining mjög lítillar yfirlitsgáttar** á **100%**.
1. Stillið gildið **Dálkaskilgreining lítillar yfirlitsgáttar** á **100%**.
1. Stillið gildið **Dálkaskilgreining meðalstórrar yfirlitsgáttar** á **33% 67%**.
1. Stillið gildið **Dálkaskilgreining stórrar yfirlitsgáttar** á **33% 67%**.
1. Í hólfinu **Hólf með tveimur dálkum** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Verslunarval** og síðan velja **Í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla gildið **Snið** á **Finna verslanir**.
1. Stillið gildið **Leitarradíus** á mílur.
1. Stillið aðra eiginleika, t.d. **Velja sem æskilega verslun**, **Sýna allar verslanir** og **Virkja sjálfvirkar tillögur** eftir þörfum.
1. Í hólfinu **Hólf með tveimur dálkum** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Kort** og síðan velja **Í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla alla frekari eiginleika eftir þörfum.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
 
## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Stutt kynning um PDP](quick-tour-pdp.md)

[Stutt kynning á körfu og greiðsluferli](quick-tour-cart-checkout.md)

[Setja upp afhendingarmáta](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Stjórna Bing-kortum fyrir þitt fyrirtæki](dev-itpro/manage-bing-maps.md)

[REST API Bing-korta](https://docs.microsoft.com/bingmaps/rest-services/)

[Kortaeining](map-module.md)
