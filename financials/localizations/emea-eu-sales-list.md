---
title: "Skýrslugerð ESB-sölulista"
description: "Þessi grein gefur upplýsingar um skýrslugerð ESB-sölulista."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 06656fe519c82293d5a0eb2d48ae0f89ae0aef49
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="eu-sales-list-reporting"></a>Skýrslugerð ESB-sölulista

[!include[banner](../includes/banner.md)]


Þessi grein gefur upplýsingar um skýrslugerð ESB-sölulista.

<a name="eu-sales-list-reporting"></a>Skýrslugerð ESB-sölulista
-----------------------

Birgi sem er sér um birgðir innan bandalagsins af vörum eða þjónustu til fyrirtækja sem eru staðsett innan Evrópusambandsins (ESB) verður að senda inn yfirlýsingu um birgðir innan bandalagsins (esb-sölulista eða ESL). Almennt séð, þarf að senda í ESL til skattayfirvalda ekki síðar en síðasta dag mánaðarins eftir tímabil fjárhagsdagatals sem ESL nær yfir. Birgirinn verður að gefa upp auðkennisnúmer virðisaukaskatts (VSK) á ESL og verður einnig að gefa upp, eftir viðskiptavini, eftirfarandi upplýsingar:

-   VSK-auðkennisnúmer viðskiptavinar í ESB
-   Heildarvirði birgða innan bandalagsins af vörum og þjónustu sem eru gefnar út til viðskiptavinar í ESB á því tímabili. Birgirinn verður einnig aðskilja almennar birgðir af vörum úr þríhliða vöruviðskiptum. Þríhliða viðskiptafærslan felur í sér beina afhending varnings frá birgi á birgi til viðskiptavinar þegar báðir aðilarnir eru skráðir í öðru aðildarríki ESB.

Með því að nota í ESL geta skattyfirvöld í hverju aðildarríki ESB staðfest hvort VSK hafi verið greiddur fyrir hverja færslu innan bandalagsins. Samsetning skráningar og skila á VSK láta aðildarríki ESB skiptast á upplýsingum um vöruflæði innan ESB.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Yfirlit yfir skýrsluferli ESB-sölulista
Hægt er að ljúka eftirfarandi verkum fyrir skýrslu ESB-sölulista:

-   Safna upplýsingum um viðskiptafærslur innan bandalagsins. Færsla fyrir viðskipti innan bandalagsins getur verið sölureikningur, textareikningur, reikningsverk eða reikningur lánardrottins. Færsla er auðkennd samkvæmt landi/svæði mótaðilans. Viðskiptafærslum af mismunandi gerðum innan bandalagsins er safnað saman í töflu ESB-sölulista, þar sem þær birtast í skjámyndinni algengar. Hver færsla í ESL-töflunni stendur fyrir eina færslu og samanstendur af VSK-kenni mótaðila og því heildarvirði á vörum og þjónustu sem gefið var upp.
-   (Valfrjálst) Forskoða skýrsluna **ESB-sölulisti**. Hægt er að forskoða og villuleita skýrslu **ESB-sölulista** fyrir tiltekið tímabil í Microsoft Excel vinnubók.
-   Mynda skýrslugerð fyrir **ESB-sölulista**. Skýrslan **ESB-sölulisti** er mynduð á formi rafrænnar skráar fyrir tiltekið snið sem er sértækt fyrir hvert aðildarríki Evrópusambandsins. Almennt séð inniheldur skýrslan **ESB-sölulisti** grunnupplýsingar um skýrslugerð aðila og gildi birgða af vörum og þjónustu. Upplýsingar eru flokkaðar eftir landi og auðkenni VSK mótaðilans.
-   Lokaðu skýrslutímabili ESB-sölulista. Þegar **ESB-sölulista** skýrslan hefur verið mynduð og send til skattyfirvalda, er hægt að merkja færslurnar í ESL-töflunni sem **Lokað**. Þessar færslur ekki hafðar með í viðbótarskýrslum.

## <a name="prerequisites"></a>Skilyrði
Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tegund</th>
<th>Skilyrði</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Uppsetning:</strong>Setja upp lögaðila</td>
<td>Aðalaðsetur lögaðilans verður að vera í aðildarlandi Evrópusambandsins. Á síðunni <strong>Lögaðilar</strong> (smellt er á <strong>Fyrirtækisstjórnun</strong> &gt; <strong>Fyrirtæki</strong> &gt; <strong>Lögaðilar</strong>) er lögaðilinn valinn. Á flýtiflipanum <strong>Aðsetur</strong> skal stofna aðsetur, velja land/svæði og önnur aðsetursíhluti og merkja aðsetur sem <strong>Aðal</strong>. Á flýtiflipanum <strong>Skattskráning</strong> í reitnum <strong>Skattskráningarnúmer</strong> skal tilgreina skattskráningarnúmer fyrir fyrirtækið.</td>
</tr>
<tr class="even">
<td><strong>Uppsetning:</strong> Færibreytur auðkenniningar skattundanþágu</td>
<td>Setja upp færibreytur auðkenningar skattundanþágu á síðunni <strong>Færibreytur lands/svæðis</strong> (smellt er á <strong>Skattur</strong> &gt; <strong>Uppsetning</strong> &gt; <strong>VSK</strong> &gt; <strong>Færibreytur lands/svæðis</strong>). Fyrir hvert land/svæði þar sem þú hefur mótaðila býrðu til færslu á síðunni og tilgreinir eftirfarandi upplýsingar:
<ul>
<li><strong>Land/svæði</strong> – Veljið land/svæði til að tengja við kenni skattundanþágunúmers.</li>
<li><strong>Virðisaukaskattur</strong> – Færið inn auðkennisnúmer skattundanþágu (það er að segja forskeyti skattundanþágunúmers) fyrir valið land/svæði.</li>
<li><strong>Kanna skattundanþágunúmer</strong> – Veljið þennan gátreit til að villuleita kenni skattundanþágunúmer fyrir valið land/svæði.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Uppsetning: </strong>Skattundanþágunúmer</td>
<td>Stofnaðu skattundanþágunúmer fyrir mótaðila þína á síðunni <strong>Skattundanþágunúmer </strong> (smellt er á <strong>Skattur</strong> &gt; <strong>Uppsetning</strong> &gt; <strong>VSK</strong> &gt; <strong>Skattundanþágunúmer</strong>). Fyrir hvert skattundanþágunúmer er færsla stofnuð á síðunni og tilgreindar eftirfarandi upplýsingar:
<ul>
<li><strong>Land/svæði </strong>– Veljið land/svæði fyrir skráningu á mótaðilanum.</li>
<li><strong>Skattundanþágunúmer</strong> – Færið inn skattundanþágunúmer mótaðilans.</li>
<li><strong>Heiti fyrirtækis</strong> – (Valfrjálst) Sláið inn heiti mótaðilans.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Uppsetning: </strong>Skattskráning mótaðila</td>
<td>Setja upp upplýsingar um skattskráningu fyrir mótaðila annaðhvort á síðunni <strong>Allir viðskiptavinir</strong> (smellt er á <strong>Sala og markaðssetning</strong> &gt; <strong>Viðskiptavinir</strong> &gt; <strong>Allir viðskiptavinir</strong>, valin færsla viðskiptavinar og síðan smellt á <strong>Valkostir</strong> &gt; <strong>Breyta skjámynd</strong> &gt; <strong>Upplýsingayfirlit</strong>) eða síðunni <strong>Lánardrottnar</strong> (smellt er á <strong>Innkaup og aðföng</strong> &gt; <strong>Lánardrottnar</strong> &gt; <strong>Lánardrottnar</strong>, valin færsla lánardrottins og síðan smellt á <strong>Valkostir</strong> &gt; <strong>Breyta skjámynd</strong> &gt; <strong>Upplýsingayfirlit</strong>). Á flýtiflipanum <strong>Reikningur og afhending</strong> á síðunni <strong>Skattundanþágunúmer</strong> skal velja skattskráningarnúmer.</td>
</tr>
<tr class="odd">
<td><strong>Uppsetning: </strong>Virðisaukaskattur</td>
<td>Setja upp skattkóða til að hafa með í skýrslu <strong>ESB-sölulista</strong> á síðunni <strong>VSK-kóðar</strong> (smellt er á <strong>Skattur</strong> &gt; <strong>Óbeinn skattur</strong> &gt; <strong>VSK</strong> &gt; <strong>VSK-kóðar</strong>). Á flýtiflipanum <strong>Skýrsluuppsetning</strong>, fyrir hvern VSK-kóða sem á að hafa með í skýrslunni, skal hreinsa gátreitinn <strong>Útilokað </strong>. Setja upp færibreytur virðisaukaskatts á síðunni <strong>VSK-flokkar vöru</strong> (smellt er á <strong>Skattur</strong> &gt; <strong>Óbeinn skattur</strong> &gt; <strong>VSK</strong> &gt; <strong>VSK-flokkar vöru</strong>). Fyrir hvern VSK-flokk vöru skal slá inn gildi í reitinn <strong>Skýrslugerð</strong>. Gildið sem er valið ákvarðar dálk ESL-upphæðar sem línuupphæðin verður setti í.
<ul>
<li><strong>Autt</strong> – Línuupphæðin er innifalin í dálknum <strong>Ekki úthlutað virði</strong>.</li>
<li><strong>Vara</strong> – Línuupphæðin er innifalin í dálknum <strong>Vöruvirði</strong>.</li>
<li><strong>Þjónusta</strong> – Línuupphæðin er innifalin í dálknum <strong>Þjónustuvirði</strong>.</li>
<li><strong>Fjárfesting</strong> – Línuupphæðin er innifalin í dálknum <strong>Fjárfestingarvirði</strong>. Þessi dálkur á aðeins við um Belgíu.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Uppsetning:</strong> ESL skýrsla skilgreining</td>
<td>Flytja inn eða stofna rafrænar skilgreiningar á skýrslum fyrir ESL. Nánari upplýsingar um hvernig á að stofna og viðhalda grunnstillingum fyrir rafræna skýrslugerð, sjá fylgigögnin Rafræn skýrslugerð.</td>
</tr>
<tr class="odd">
<td><strong>Uppsetning: </strong>Almennar færibreytur</td>
<td>Setja upp færibreytur ESL-skýrslugerðar á síðunni <strong>Færibreytur erlendra viðskipta</strong> (smellt er á <strong>Skattur</strong> &gt; <strong>Uppsetning</strong> &gt; <strong>Erlend viðskipti</strong> &gt; <strong>Færibreytur erlendra viðskipta</strong>). Tilgreina skal eftirfarandi færibreytur:
<ul>
<li>Flipinn <strong>ESB-sölulisti</strong>:
<ul>
<li><strong>Skrá staðgreiðsluafslátt</strong> – Veljið gátreitinn ef staðgreiðsluafsláttur skal tekinn með í gildi þegar færsla er höfð með í ESL.</li>
<li><strong>Flytja innkaup</strong> – Veljið þennan gátreit til að taka innkaup með í ESL.</li>
<li><strong>Vörpun skráarsniðs</strong> – Veljið rafrænt skýrslusnið sem nota á þegar rafræn skrá er mynduð fyrir ESL.</li>
<li><strong>Vörpun skýrslusniðs</strong> – Veljið rafrænt skýrslusnið sem nota á þegar rafræn forskoðunarskrá er mynduð fyrir ESL.</li>
<li><strong>Sléttunarregla</strong> – Tilgreindu rauntölu sem nota á fyrir sléttun. ESL upphæðir verða sléttaðar upp í margfeldi af þessari tölu.</li>
<li><strong>Sléttunaraðferð</strong> – Veljið sléttunaraðferð sem nota á þegar ESL upphæðir eru sléttaðar (<strong>Venjulegt</strong>, <strong>Niður</strong> eða <strong>Sléttun upp</strong>).</li>
<li><strong>Nota lágmarksgildi</strong> – Veljið þennan gátreit ef óskað er eftir að upphæðir sem eru lægri en númer <strong>Sléttunarreglu</strong> séu sléttaðar upp að númeri <strong>Sléttunarreglu</strong>.</li>
<li><strong>Fjöldi aukastafa</strong> – Tilgreina fjölda aukastafa sem á að sýna í ESL-upphæðum (bæði í rafrænum skrám og í <strong>ESL-forskoðun</strong> skýrslunni).</li>
</ul></li>
<li>Flipinn <strong>Færibreytur lands/svæðis</strong>: Auðkenna aðildarríki ESB. Fyrir hvert skattundanþágunúmer er stofnuð færsla á síðunni og tilgreindar eftirfarandi upplýsingar:
<ul>
<li><strong>Land/svæði</strong> – Veljið land/svæði.</li>
<li><strong>Gerð lands/svæðis</strong> – Ef gildið <strong>Land/svæði</strong> er land/svæði sem fyrirtækið er skráð í skal velja <strong>Innanlands</strong>. Ef gildið <strong>Land/svæði</strong> er annað aðildarland Evrópusambandsins en fyrirtækið er skráð í skal velja <strong>ESB</strong>. Ef gildið <strong>Land/svæði</strong> er ekki aðildarríki ESB, veljið <strong>Þriðja land/svæði</strong>.</li>
</ul></li>
<li>Flipinn <strong>Númeraraðir</strong>: Á línunni þar sem gildið <strong>Tilvísun</strong> er <strong>ESB-sölulisti</strong>, skal velja kóða númeraraðar.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tengdar færslur</strong></td>
<td><ul>
<li>Skrá sölu á viðskiptavin í öðru aðildarríki EU.</li>
<li>Skrá sölu á textareikning fyrir viðskiptavin í öðru aðildarríki EU.</li>
<li>Skrá sölu á verkreikning fyrir viðskiptavin í öðru aðildarríki EU.</li>
<li>Skrá reikning frá lánardrottni í öðru aðildarríki ESB.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Unnið með ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Söfnun upplýsinga um viðskipti innan bandalagsins

Hægt er að líta á færslur af eftirfarandi gerðum sem viðskiptafærslur innan bandalagsins:

-   Sölureikningar
-   Textareikningar
-   Verkreikningar
-   Reikningar lánardrottins

Litið er á færslu sem færslu fyrir viðskipti innan bandalagsins ef afhendingaraðsetur færslunnar er í aðildarríki Evrópusambandsins. Fyrir slík lönd/svæði þarf færsla að vera til á flipanum **Færibreytur lands/svæðis** á síðunni **Færibreytur erlendra viðskipta** og gildið **Gerð lands/svæðis** ætti að vera stillt á **ESB**. Færslur fyrir viðskipti innan bandalagsins eru merktar í reitnum **Listakóðar**. Með þessu reit er einnig hægt að aðskilja almennar viðskiptafærslur innan bandalagsins frá þríhliða viðskiptafærslum. Hægt er að safna upplýsingum um færslur fyrir viðskipti innan bandalagsins á síðunni **ESB-sölulisti** (smellt er á **Skattur** &gt; **Skattframtöl** &gt; **Erlend viðskipti** &gt; **ESB-sölulisti**) með því að nota aðgerðina **Flytja**. Þessi aðgerð gerir það mögulegt að taka með færslur sem hafa upphæðir fyrir mismunandi skýrslugerðir (þ.e. vörur eða þjónustu), eftir þeim VSK-flokkum vöru sem eru tilgreindir á færslulínunum. Einnig er hægt að nota aðra síur til að skilgreina þær færslur sem eiga að fylgja með. Aðgerðin **Flytja** stofnar færslu á síðunni **ESB-sölulisti** fyrir hverja viðskiptafærslu innan bandalagsns sem eru hafðar með og tilgreinir lykilnúmer mótaðila, land/svæði, skattundanþágunúmer, reikningsnúmer og dagsetningu og heildarupphæðir lína eftir skýrslugerð. Hún afritar einnig gildi **Listakóða** úr færslunni. Hægt er að breyta fyrir færslu á síðunni **ESB-sölulisti**. Aðgerðin **Flytja** stofnar færslur þar sem gildið **Skýrslustaða** er stillt á **Innifalið**. Hægt er að villuleita upplýsingarnar sem safnað er á síðunni **ESB-sölulisti** með því að nota aðgerðina **Villuleita**.

### <a name="generating-the-eu-sales-list-report"></a>Myndun skýrslu fyrir ESB-sölulsta

Hægt er að mynda skýrslu **ESB-sölulista** með því að nota aðgerðina **Skýrslugerð**á síðunni **ESB-sölulisti**. Aðgerðin gerir kleift að velja skýrslutímabil og nota síur til að skilgreina ESL-færslur til að hafa með. Þar að auki er hægt að tilgreina aðrar færibreytur sem eru sértækar fyrir hvert land/svæði. Einnig er hægt að velja að búa til forskoðunarskýrslu, rafræna skrá eða hvort tveggja. Aðgerðin **Skýrslugerð** notar skýrslu- og skráarsniðsstillingar sem tilgreindar eru á síðunni **Færibreytur erlendra viðskipta**. Almennt samanstendur **ESB-sölulisti** skýrsla af aðskildum línum sem sýna heildarfjölda birgða á land/svæði mótaðila, skattundanþágunúmer og skýrslugerð (þríhliða viðskiptafærslur eru hafðar með). Þegar búið er að mynda **ESB-sölulisti** skýrslu fyrir tiltekið tímabil er hægt að merkja ESL-færslurnar sem eru teknar með í skýrslunni með því að stilla gildi **Skýrslustöðu** gildi sem **Skráð**. Til að setja þessa stöðu er notuð aðgerðin **Merkja sem tilkynnt** á síðunni **ESB-sölulisti**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>Loka skýrslutímabili ESB-sölulista.

Þegar skýrsluferlinu hefur verið fyrir tiltekið tímabil (til dæmis þegar skattayfirvöld hafa samþykkt **esb-sölulista** skýrslu), er hægt að merkja ESL færslurnar sem eru teknar með í skýrslunni fyrir tímabilið með því að stilla gildið **Skýrslustaða** sem **Lokað**. Til að setja þessa stöðu er notuð aðgerðin **Merkja sem lokað** á síðunni **ESB-sölulisti**. Ef lokun tímabilsins er afturkölluð er hægt að merkja ESL-færslur með því að stilla gildið **Skýrslustaða** sem **Innifalið**. Síðan er hægt að taka þessar færslur með í **esb-sölulista** skýrsluna aftur. Til að setja þessa stöðu er notuð aðgerðin **Merkja sem** **innifalið**aðgerðin á síðunni **EU-sölulisti**.




