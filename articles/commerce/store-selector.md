---
title: Eining til að velja verslun
description: Þessi grein fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268341"
---
# <a name="store-selector-module"></a>Eining til að velja verslun

[!include [banner](includes/banner.md)]

Þessi grein fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður í Microsoft Dynamics 365 Commerce.

Viðskiptavinir geta notað valeiningu verslunar til að sækja vöru í valdri verslun eftir kaup á netinu. Í Commerce-útgáfu 10.0.13 felur valeining verslunar einnig í sér fleiri möguleika sem geta birt **Finna verslun** síðu sem sýnir nálægar verslanir.

Valeining verslunar leyfir notendum að slá inn staðsetningu (borg, ríki, aðsetur og svo framvegis) til að leita að verslunum innan leitarradíuss. Þegar einingin er opnuð í fyrsta skipti, notar hún staðsetningu á vafra viðskiptavinarins til að finna verslanir (ef samþykki er veitt).

## <a name="store-selector-module-usage"></a>Notkun á valeiningu verslunar

- Hægt er að nota valeiningu verslunar á upplýsingasíðu afurðar til að velja verslun til að sækja í.
- Hægt er að nota valeiningu verslunar á körfusíðu til að velja verslun til að sækja í.
- Hægt er að nota valeiningu verslunar á sjálfstæðri síðu sem sýnir allar tiltækar verslanir.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Uppsetning uppfyllingarflokks í Commerce Headquarters

Til að verslunarvalið geti sýnt tiltækar verslanir þarf að setja upp uppfyllingarflokkinn í Commerce Headquarters. Frekari upplýsingar er að finna í [Setja upp uppfyllingarflokka](customer-orders-overview.md#set-up-fulfillment-groups).

Í uppfyllingarflokknum þarf auk þess að skilgreina lengdar- og breiddargráðu á staðsetningu verslunar í höfuðstöðvum.

Til að færa inn gildi fyrir lengdar- og breiddargráðu fyrir staðsetningu verslunar í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Birgðastjórnun \> Uppsetning \> Sundurliðun birgða**.
1. Veljið staðsetningu vöruhúss á svæðinu vinstra megin.
1. Í flýtiflipanum **Aðsetur** skal velja **Ítarlegt**.

    ![Dæmi um verslunarupplýsingar í höfuðstöðvum.](./media/Store-address.png)

1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Almennt** skal færa inn gildi fyrir **Breiddargráðu** og **Lengdargráða**.

    ![Dæmi um uppsetningu breiddargráðu og lengdargráðu fyrir verslun í höfuðstöðvum.](./media/Store-latitude-longitude.png)

1. Í aðgerðarúðunni skal velja **Vista**. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Fela verslun frá verslunarvalseiningunni

Sumar verslanir í uppfyllingarhópi eru hugsanlega ekki gildar afhendingarstaðir. Til að tryggja að aðeins gildar afhendingarstaðir birtist sem valkostir í verslunarvalseiningunni skaltu fylgja þessum skrefum í höfuðstöðvum Commerce.

1. Fara til **Verslun og verslun \> Uppsetning viðskipta \> Uppfyllingarhópar \> Allar verslanir**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Undir **Uppsetning**, fyrir hverja verslun sem er ekki gild afhendingarstaður, hreinsaðu af **Er afhendingarstaður** gátreit.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Keyra 1070 **Rásar stillingar** dreifingaráætlunarstarf.

## <a name="bing-maps-integration"></a>Samþætting Bing-korta

Valeining verslunar er samþætt við [REST forritunarviðmót Bing-korta](/bingmaps/rest-services/) til að nota landkóðun og sjálfvirkar tillögur Bing. API-lykill Bing-korta er nauðsynlegur og verður að bæta honum við samnýtta færibreytusíðu í Commerce Headquarters. API-landkóðun er notuð til að umbreyta staðsetningu í gildi breiddar- og lengdargráða. Samþætting við API fyrir sjálfvirkar tillögur er notuð til að sýna leitartillögur þegar notendur slá inn staðsetningar í leitarreitinn.

Fyrir REST API sjálfvirkar tillögur, þarf að ganga úr skugga um að eftirfarandi vefslóðir séu leyfðar í öryggisreglum vefsvæðisins. Þessi uppsetning er gerð í Commerce-vefsmiðnum með því að bæta leyfðum vefslóðum við ýmsar öryggisleiðbeiningar fyrir vefsvæðið (t.d. **img-src**). Nánari upplýsingar er að finna í [Öryggisregla um innihald](manage-csp.md). 

- Í leiðbeininguna **connect-src** skal bæta við **&#42;.bing.com**.
- Í leiðbeininguna **img-src** skal bæta við **&#42;.virtualearth.net**.
- Í leiðbeininguna **script-src** skal **bæta við &#42;.bing.com, &#42;.virtualearth.net**.
- Í leiðbeininguna **script style-src** skal bæta við **&#42;.bing.com**.

## <a name="pickup-in-store-mode"></a>Sækja í verslun

Valeining verslunar styður stillinguna **Sækja í verslun** sem sýnir lista yfir verslanir þar sem hægt er að sækja vöru. Hún sýnir einnig opnunartíma verslunar og birgðir fyrir hverja verslun á listanum. Valeining verslunar krefst vörusamhengis til að sýna vöruframboð og leyfa notendum að bæta vörunni við körfuna, ef afhendingarsnið vörunnar er stillt á **sækja** í valdri verslun. Frekari upplýsingar er að finna í [Birgðastillingar](inventory-settings.md). 

Hægt er að bæta valeiningu verslunar við kaupgluggaeiningu á upplýsingasíðu afurðar til að sýna verslanir þar sem boðið er upp á að sækja vöruna. Það er einnig hægt að bæta við körfu mát. Í slíku tilfelli sýnir valeining verslunar valkosti til að sækja fyrir hverja vörulínu í körfunni. Einnig er hægt að bæta verslunarvaleiningunni við aðrar síður eða einingar með viðbótum og sérstillingum.

Til að þessar aðstæður geti virkað, þarf að skilgreina afurðir þannig að afhendingarmátann **sækja** er notað. Annars verður einingin ekki sýnd á síðum afurða. Frekari upplýsingar um hvernig á að skilgreina afhendingarmáta er að finna í [Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Eftirfarandi mynd sýnir dæmi um verslunarvalseiningu sem er notuð á PDP.

![Dæmi um verslunarvalseiningu sem notuð er á PDP.](./media/BOPIS.PNG)

> [!NOTE]
> Í útgáfu 10.0.16 og nýrri er hægt að virkja nýja eiginleika sem gerir fyrirtæki kleift að skilgreina marga afhendingarmáta fyrir viðskiptavini.  Ef þessi eiginleiki er virkur er verslunarval og aðrar einingar í e-Commerce endurbættar til að leyfa kaupandanum að velja úr hugsanlega mörgum valkostum fyrir afhendingarmáta ef það er skilgreint.  Frekari upplýsingar um þennan eiginleika má finna í [þessum fylgigögnum](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Finna verslanir

Verslunarvaleiningin styður einnig stillinguna **Finna verslanir**. Hægt er að nota þessa stillingu til að búa til síðu fyrir staðsetningar verslana sem sýnir verslanir sem í boði eru og upplýsingar um þær. Í þessari stillingu virkar verslunarvaleiningin án vörusamhengis og er hægt að nota hana sem sjálfstæða einingu á hvaða síðu sem er. Að auki, ef kveikt er á viðeigandi stillingum fyrir eininguna, geta notendur valið verslun sem sína eftirlætis verslun. Þegar verslun er valin sem eftirlætis verslun, er auðkenni verslunarinnar geymt í vefkökum vafrans. Notandinn verður því að samþykkja kökur í skilaboðum um slíkt.

Eftirfarandi mynd sýnir dæmi um verslunarvaleiningu sem er notuð saman með kortaeiningu á staðsetningarsíðu verslunar.

![Dæmi um verslunarvalseiningu og kortaeiningu á staðsetningarsíðu verslunar.](./media/ecommerce-Storelocator.PNG)

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

## <a name="site-settings"></a>Stillingar svæðis

Verslunarvalseining fellur undir [Stillingar fyrir Bæta vöru í körfu](add-cart-settings.md). Þegar vöru hefur verið bætt við körfuna úr verslunarvalseiningunni munu notendur vefsvæðisins sjá skilgreind verkflæði sem eiga við.

## <a name="add-a-store-selector-module-to-a-page"></a>Bæta við verslunarvalseiningu á síðu

Aðeins er hægt að nota eininguna **Sækja í verslun** á upplýsingasíðu afurðar og körfusíðum. Stilla þarf sniðið **Sækja í verslun** á eiginleikasvæði einingarinnar.

- Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við innkaupakassaeiningar, sjá [Kaupkassaeiningu](add-buy-box.md). 
- Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við körfueiningar, sjá [Körfueiningu](add-cart-module.md).

Til að stilla verslunareininguna til að sýna tiltækar verslanir fyrir verslunarstaðsetningarsíðu, eins og á myndinni sem birtist fyrr í þessari grein, skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í **Nýtt sniðmát** svargluggi, undir **Nafn sniðmáts**, koma inn **Markaðssetning sniðmát**, og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Staðsetningar verslana**, og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu **Markaðssetning sniðmát** sem þú bjóst til og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**. 
1. Í **Aðal** rauf á nýju síðunni, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Gámur með 2 súlum** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Stillið gildið **Dálkaskilgreining mjög lítillar yfirlitsgáttar** á **100%**.
1. Stillið gildið **Dálkaskilgreining lítillar yfirlitsgáttar** á **100%**.
1. Stillið gildið **Dálkaskilgreining meðalstórrar yfirlitsgáttar** á **33% 67%**.
1. Stillið gildið **Dálkaskilgreining stórrar yfirlitsgáttar** á **33% 67%**.
1. Í **Gámur með 2 súlum** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Verslunarval** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla gildið **Snið** á **Finna verslanir**.
1. Stillið gildið **Leitarradíus** á mílur.
1. Stillið aðra eiginleika, t.d. **Velja sem æskilega verslun**, **Sýna allar verslanir** og **Virkja sjálfvirkar tillögur** eftir þörfum.
1. Í **Gámur með 2 súlum** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Kort** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla alla frekari eiginleika eftir þörfum.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
 
## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Stutt kynning um PDP](quick-tour-pdp.md)

[Stutt kynning á körfu og greiðsluferli](quick-tour-cart-checkout.md)

[Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Stjórna Bing-kortum fyrir þitt fyrirtæki](dev-itpro/manage-bing-maps.md)

[REST API Bing-korta](/bingmaps/rest-services/)

[Kortaeining](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
