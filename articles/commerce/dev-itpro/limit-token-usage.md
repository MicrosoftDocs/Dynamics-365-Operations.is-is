---
title: Takmarkaðu notkun greiðslulykils
description: Þessi grein lýsir eiginleikanum sem takmarkar hvernig greiðslutákn eru notuð í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709374"
---
# <a name="limit-payment-token-usage"></a>Takmarkaðu notkun greiðslulykils

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi grein lýsir eiginleikanum sem takmarkar hvernig greiðslutákn eru notuð í Microsoft Dynamics 365 Commerce. Táknnotkun er takmörkuð við umfang sölupöntunar eða, ef samþykki viðskiptavina er veitt, er hún geymd sem kort á skrá.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | Lýsing |
|---|---|
| Merki | Tilvísað XML-kubbur í Dynamics 365 kerfinu sem geymir greiðslutilvísanir í viðskiptalegum tilgangi. |
| Kort á skrá | Vistað kortaviðmiðunartákn sem samið er um til framtíðarnotkunar í Dynamics 365 kerfinu eða greiðslugáttinni og er sértækt fyrir reikning viðskiptavinar. |

Takmarkanir á notkun greiðslumerkja eiga við um hvaða umhverfi sem notar greiðslugáttarþjónustu þar sem endurteknir tákn eru notaðir. Út úr kassanum [Dynamics 365 greiðslutengi fyrir Adyen](adyen-connector.md) notar endurtekna greiðslutákn til að framkvæma síðari pöntunaraðgerðir, svo sem leiðréttingar á heimildum og endurheimildir.

Til að hjálpa til við að stjórna því hvernig þessi endurteknu greiðslutákn eru notuð í öllu kerfinu, er **Takmarka notkun greiðslumerkja við pöntunarsamhengi** eiginleiki takmarkar notkun endurtekins tákns við umfang sölupöntunar í kerfinu. Þegar það er virkt breytir eiginleikinn notendaviðmóti höfuðstöðva Commerce (UI) með því að uppfæra greiðsluinnsláttarsíður og takmarka möguleika á að velja fyrri greiðslutilvísanir viðskiptavina til notkunar í nýjum viðskiptatilvikum.

Þessi eiginleiki hjálpar til við að uppfylla notkunarreglur fyrir suma greiðsluútgefendur eins og Visa. Í sínu [Kjarnareglur Visa og vöru- og þjónustureglur Visa](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf), Visa tilgreinir að notkun greiðslumerkja eigi að vera takmörkuð við umfang viðskipta nema korthafi samþykki annað.

The **Takmarka notkun greiðslumerkja við pöntunarsamhengi** eiginleiki á aðeins við ef þú ert að nota greiðslugáttarþjónustu sem notar endurteknar tilvísanir í greiðslutákn.

## <a name="enable-the-feature"></a>Virkja eiginleikann

Til að virkja **Takmarka notkun greiðslumerkja við pöntunarsamhengi** eiginleiki, í höfuðstöðvum Commerce fyrir umhverfið þitt, farðu á **Vinnurými \> Eiginleikastjórnun**, finndu og veldu **Takmarka notkun greiðslumerkja við pöntunarsamhengi** á listanum og veldu síðan **Virkja núna**.

## <a name="limit-payment-token-usage"></a>Takmarkaðu notkun greiðslulykils

Þegar aðgerðin er virkjuð munu höfuðstöðvar Commerce-síðurnar sem eru notaðar til að fanga greiðslumáta uppfæra hvernig þær vísa til greiðslumáta viðskiptavina sem eru skráðar fyrir viðskiptavininn. Þessi uppfærsla mun fyrst og fremst hafa áhrif á tvö starfssvið:

- Hvernig viðskiptakort á skrá er fært inn fyrir hönd viðskiptavinar
- Hvernig greiðsluupplýsingar gagnvart viðskiptamanni eru geymdar fyrir framtíðargreiðslufærslur sölupöntunar

Þegar viðskiptavinur gerir viðskipti gegn viðskiptarásum eru greiðsluupplýsingar geymdar með sölupöntunarsamhengi. Sölupöntunarsamhengið takmarkar greiðslutáknið þannig að það verður ekki notað sem greiðsluviðmiðun á móti viðskiptamannaskránni á greiðslusíðum fyrir nýjar eða breyttar sölupöntunargreiðslur í höfuðstöðvum Commerce.

### <a name="payment-form-changes"></a>Breytingar á greiðsluformi

Þegar notandi símaver eða höfuðstöðvar viðskipta tekur við greiðslu fyrir viðskiptavin gegn sölupöntun sýnir greiðslusíðan upplýsingar um val á greiðslumáta. Þegar **Takmarka notkun greiðslumerkja við pöntunarsamhengi** eiginleiki er virkur ef notandi velur plúsmerkið (**+**) á greiðslusíðunni eru aðeins vistaðar „kort á skrá“ færslur sýndar. Breytingar krefjast þess að notandi símaversins eða höfuðstöðvar viðskipta slær inn allar greiðsluupplýsingarnar sem viðskiptavinurinn gaf upp þegar hann fyllti út **Sláðu inn greiðsluupplýsingar viðskiptavina** síðu fyrir nýju sölupöntunarfærsluna.

Listi yfir gildi fyrir **Númer** reiturinn inniheldur aðeins kortatilvísanir sem eru tengdar þeim viðskiptavini sem hefur kortið á skrá. Það síar út allar fyrri greiðslutilvísanir sem eru ekki settar í sölupöntun.

Plús merkið (**+**) undir **Númer** reiturinn er áfram tiltækur og hægt er að nota hann til að slá inn greiðsluupplýsingarnar sem viðskiptavinurinn gaf upp fyrir færsluna sem tengist sölupöntuninni sem er í vinnslu.

### <a name="how-cards-on-file-work"></a>Hvernig spil á skrá virka

Þegar **Takmarka notkun greiðslumerkja við pöntunarsamhengi** eiginleiki er virkur, kort sem skráð er er endurtekið greiðslumerki sem er vistað gegn viðskiptaskrá og er ekki takmarkað við umfang sölupöntunar. Skráð kort gerir notendum höfuðstöðva Commerce fljótlega kleift þegar þeir fylla út greiðslusíðuna fyrir nýja sölupöntunargreiðslu. Þessi tákntilvísun á aðeins við um Dynamics 365 umhverfið. Fyrir netrásir sem nota greiðslugáttarþjónustu sem gerir notendum kleift að vista greiðslumáta til framtíðarnotkunar í greiðslunni iFrame mát, greiðslugáttin geymir þessar tilvísanir á öruggan hátt sem sérstaka tilvísun í Dynamics 365 kortið á skrá.

Til dæmis, ef Dynamics 365 Commerce Payment Connector fyrir Adyen er notað í netrás, viðskiptavinir sem slá inn kreditkortaupplýsingar sínar í greiðslunni iFrame mát sjá aðeins gáttarþjónustuna vistaðar kortatilvísanir fyrir næstu kaup á netinu þegar þær eru staðfestar. Þeir sjá ekki Dynamics 365 umhverfi vistað kortið á skrá sem valmöguleika í greiðslunni iFrame mát. Á svipaðan hátt, þegar kaupendur leggja inn pöntun í gegnum símaver, eru vistaðar kortatilvísanir þeirra á netinu ekki sýndar sem valkostir fyrir notanda símaversins. Notandi símaversins sér aðeins fyrra kort á skráartilvísunum frá Dynamics 365 kerfinu (eins og viðskiptavinurinn samþykkir) til að vista fyrir pantanir í framtíðinni.

Notendur höfuðstöðva viðskipta geta vistað kort á skrá fyrir viðskiptavin með því að fara á **Verslun og verslun \> Viðskiptavinir** og velja reikning viðskiptavinar. Í **Viðskiptavinur \> Setja upp** kafla geta notendur sem hafa heimildir til að vinna úr greiðslusíðunum notað **Kreditkort** færslusíða til að slá inn greiðslukort sem verður geymt á skrá fyrir framtíðarfærslur. Þessi aðgerð hjálpar til við að spara tíma þegar framtíðargreiðslur sölupöntunar eru unnar fyrir viðskiptavininn. Notendur símavera og höfuðstöðva viðskipta ættu aðeins að slá inn kortið á skráarkortaupplýsingar ef viðskiptavinurinn samþykkir að nota kortaviðmiðunina fyrir framtíðarviðskipti.

A **Geymdu til notkunar í framtíðinni** gátreitur neðst á greiðslusíðum höfuðstöðva Commerce gerir notendum kleift að vista kortið á skrá til notkunar í framtíðinni. Þessi gátreit ætti aðeins að nota ef viðskiptavinurinn samþykkir að nota kortið á skrá fyrir framtíðarviðskipti. Þú getur sýnt eða takmarkað **Geymdu til notkunar í framtíðinni** gátreitinn með því að nota **Leyfa viðskiptamannakort á skrá** valmöguleika á **Greiðsla** flipi á **Færibreytur símavera** síðu í höfuðstöðvum Commerce. Þegar þessi valkostur er stilltur á **Já**, Notendur höfuðstöðva Commerce sem hafa leyfi til að vinna úr greiðslusíðum geta vistað kort á skrá með því að nota **Geymdu til notkunar í framtíðinni** gátreit. Þegar valkosturinn er stilltur á **Nei**, gátreiturinn er ekki í boði fyrir notendur Commerce höfuðstöðva sem hafa heimildir til að vinna úr greiðslusíðum. The **Leyfa viðskiptamannakort á skrá** Hægt er að nota valmöguleikann ef fyrirtæki þitt vill takmarka notkun endurtekinna tákna í höfuðstöðvum Commerce, en það vill ekki enn leyfa vistun korts á skrá án málsmeðferðar til að tryggja að samþykki viðskiptavina sé veitt.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Viðskiptasíður höfuðstöðvar þar sem endurteknum takmörkunum á táknum er framfylgt

Tákntakmarkanir hafa áhrif á eftirfarandi svæði í höfuðstöðvum Commerce þegar eiginleikinn er virkur:

- Greiðsluupplýsingar viðskiptavina á **Sölupöntun \> Greiðslur \> Sláðu inn greiðslu viðskiptavina**
- Samfelldar pantanir
- Afborgunargreiðslur
- Viðskiptakröfur kreditkortagreiðslur

### <a name="manage-payment-tokens-archiving-or-removal"></a>Hafa umsjón með greiðslutáknum (geymsla eða fjarlæging)

Greiðslutákn sem voru búin til fyrir **Takmarka notkun greiðslumerkja við pöntunarsamhengi** eiginleikafáni var virkjaður (eða meðan eiginleikinn var gerður óvirkur) verður áfram "unscoped" í kerfinu og hægt er að vísa í hann í vallistum á greiðslusíðu viðskipta höfuðstöðva. Þessi tákn er hægt að fjarlægja reglulega á tvo vegu í höfuðstöðvum Commerce:

- Nota **Geymdu upplýsingar um kreditkortafærslur** síðu til að setja upp starf sem reglulega hreinsar eða geymir greiðslutákn. Ef þú stillir **Eyða gögnum án þess að setja í geymslu** valmöguleika til **Já**, táknin sem mæta **Lágmarksaldur viðskipta (í dögum)** stilling verður eytt. Fyrir frekari upplýsingar, sjá [Geymdu upplýsingar um kreditkortafærslur](archive-cc-data.md).
- Notaðu nýja **Hreinsaðu kreditkortamerki** síða (**Reikningur fáanlegur \> Fyrirspurnir og skýrslur \> Hreinsaðu til \> Hreinsaðu kreditkortamerki**), sem gerir þér kleift að keyra eða setja upp runuvinnu sem eyðir greiðslutáknum. Stillið eftirfarandi færibreytur:

    - The **Lágmarks aldur í dögum** gildi verður að vera 90 dagar eða meira.
    - The **Hlaupa í bakgrunni** Hægt er að nota stillingar til að skilgreina **Endurkoma** eða **Viðvaranir** stillingar.
    - Hægt er að úthluta runuhópi til að keyra verkefnið fyrir ákveðinn hóp.
    - Ef **Einkamál** valkostur er stilltur á **Já**, aðeins notandinn sem býr til verkið getur keyrt það.
    - Stilling á **Já** fyrir **Krítískt starf** valkostur tryggir að kerfið fylgist virkan með stöðu starfsins.

Ekki er hægt að endurheimta eyddar tákn. Stilltu **Lágmarks aldur í dögum** reit í svið sem hentar langvarandi viðskiptalífi fyrir umhverfið þitt (frá heimild til handtöku eða endurgreiðslu).

## <a name="additional-resources"></a>Frekari upplýsingar

[Algengar spurningar um greiðslur](payments-retail.md)

[Greiðsluferliseining](../add-checkout-module.md)

[Greiðslueining](../payment-module.md)
