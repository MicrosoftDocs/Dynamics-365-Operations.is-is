---
title: Uppsetning fartækja fyrir vöruhúsavinnu
description: Þessi grein lýsir því hvernig á að skilgreina valmyndaratriði sem starfsmenn í vöruhúsi nota til að framkvæma vinnu í fartæki.
author: Mirzaab
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef392fd744a68c54bc0438152b3487233ac5c7f3
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070350"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Uppsetning fartækja fyrir vöruhúsavinnu

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að skilgreina valmyndaratriði sem starfsmenn í vöruhúsi nota til að framkvæma vinnu í fartæki.

> [!NOTE]
> Þessi grein á við um eiginleika í vöruhúsastjórnun. Hún á ekki við um aðgerðir í birgðastjórnun. Valmyndaratriði sem birtast í valmyndum fartækis vöruhúss eru skilgreind á síðunni **Valmyndaratriði fartækis**. Þar sem hægt er að setja valmyndaratriðin á mismunandi valmyndir er auðvelt að skilgreina skipulag valmyndar þannig að aðeins tilteknar gerðir vinnu eru birtar tilgreindum notendum. Hægt er að skilgreina undirvalmynd til að gera eftirfarandi verk:

- Vinna úr fyrirspurn eða framkvæma verkþátt, svo sem að prenta merki, mynda númer númeraplötu, hefja framleiðslupöntun eða fletta upp upplýsingum um vörur á staðsetningu.
- Stofna vinnu sem þarf að framkvæma með öðru ferli. Til dæmis getur móttaka vöru fyrir innkaupapöntun stofnað frágangsvinnu fyrir annan starfsmann.
- Framkvæma vinnu sem var stofnað með annarri vinnslu (fyrirliggjandi vinna), eins og frágangsvinna sem var stofnuð þegar vara var móttekin fyrir innkaupapöntun.

Til að stofna valmyndaratriði fyrir verkþátt eða fyrirspurn er reiturinn **Máti** stilltur á **Óbeint**. Listi yfir valkosti **verkþáttarkóða** verður þá tiltækur, svo að hægt er að velja gerð fyrirspurnar eða aðgerðar sem valmyndaratriðið er fyrir. Til að stofna valmyndaratriði til að mynda vöruhúsavinnu er reiturinn **Máti** stilltur á **Vinna**. Listi yfir valkosti **Ferli vinnustofnunar** verður þá tiltækur. Til að stofna valmyndaratriði til að vinna úr fyrirliggjandi vöruhúsavinnu er reiturinn **Máti** stilltur á **Vinna** og svo valkosturinn **Nota fyrirliggjandi verk** á **Já**. 

> [!NOTE]
> Viðbótarreitir gætu verið tiltækir fyrir valmyndaratriði, eftir þeim máta sem er valinn fyrir valmyndaratriðið og hvort valmyndaratriði er notað til að framkvæma fyrirliggjandi vinnu. Sjá hlutann „Fleiri valkostir valmyndaratriðis“ sem er seinna í þessari grein fyrir upplýsingar um valið svæði.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Skilgreina valmyndaratriði fyrir aðgerðir og fyrirspurnir

Ef reiturinn **Máti** fyrir valmyndaratriði er stilltur á **Óbeint** er hægt að stofna valmyndaratriði til að framkvæma almennan verkþátt eða fyrirspurn sem stofnar ekki vinnu. Dæmi eru meðal annars endurprentun á númeraplötumerkjum og fyrirspurn um vörur á staðsetningu. Eftirfarandi tafla sýnir þá valkosti sem eru tiltækir.

| Valkostur | Lýsing |
|---|---|
| Ekkert | Þetta sjálfgildi virkjar ekki verkþátt eða fyrirspurn. |
| Um | Skoða upplýsingar um kerfið, eins og útgáfunúmer, kenni vöruhúss og starfsmanninn sem er þegar skráður inn. |
| Breyta vöruhúsi | Breyttu vöruhúsi sem starfsmaður er skráður inn á. |
| Staðsetningarfyrirspurn | Skoða upplýsingar um allar vörur og magn fyrir staðsetningu. |
| Fyrirspurn vegna númeraplötu | Skoða magn vara í númeraplötu og staðsetningu númeraplötunar. |
| Hefja framleiðslupöntun | Hefja framleiðslupöntun. |
| Framleiðslurýrnun | Færið inn magn rýrnunar sem var stofnuð við framleiðslu fyrir hverja uppskriftarlínu. |
| Síðasta bretti framleiðslu | Benda til þess að síðasta vörubretti hafi verið framleitt fyrir framleiðslupöntun og að staða framleiðslupöntunar skuli uppfærð í **Tilkynna sem tilbúið**. Staða hráefnis sem var ekki notað í framleiðslu hefur verið breytt til baka úr **Tiltekið** í **Í pöntun** og hægt er að skila vörum í birgðir. |
| Vörufyrirspurn | Skannið vöru til að ákvarða hvar hún er í vöruhúsinu. Fyrirspurn skilar staðsetningar og magns fyrir skannaðrar vöru. |
| Endurprenta merkimiða | Prenta aftur merki á númeraplötu. |
| Röðun númeraplötu | Stofna í yfirnúmeraplötunni með því að sameina margar númeraplötur í sömu staðsetningu. Þetta er gagnlegt ef flytja á margar númeraplötur í einu. Eftir að yfireining númeraplötu er flutt, verður þú að gera númeraplötuhlé áður en þú getur tekið atriði úr hverri númeraplötu. <p></p>**Ábending:** Til að flytja yfirnúmeraplötunni, verður að nota fartækið sem er skilgreint til að stofna vinnu fyrir hreyfingar. |
| Númeraplötuskipti | Skipta upp röðun númeraplötu þannig að hægt er að taka vörur frá númeraplötur sem voru í í byggingu. |
| Innskráning ökumanns | Ef verið er að nota Flutningsstjórnun skal skrá komu ökumaðnns með því að skanna kenni farms á útleið, auðkenni móts eða kenni sendingarinnar. Fyrir þennan valkost þarf hleðsla að vera úthlutuð á mót og staða hleðslu verður að vera **Hlaðið**. |
| Útskráning ökumanns | Skrá að bílstjóri hafi lokið móti sínu. |
| Hreinsa númeraröð úr skyndiminni | Eyða númer raðnúmer frá í númeraröð úr skyndiminni. Þessi verkþáttur er yfirleitt framkvæmdur af kerfisstjóra til að leysa vandamál skyndiminnis þegar fartæki eru notuð. |
| Breyta runuráðstöfun | Leyfa starfsmanni að tilgreina ráðstöfunarkóða runu fyrir vöru og runu. Þetta val uppfærir ráðstöfunarkóða sem er tilgreindur fyrir runu. |
| Sýna opinn verkefnalista | Sýna lista yfir tiltæka vinnu til tiltekins notanda. Notandinn getur síðan valið vinnu til að framkvæma og verður beint að henni. Búist er við að þessi listi verði skoðaður á spjaldtölvum sem hafa skjástærð upp á 7 tommur eða meira. Þegar þessi valkostur er valinn verða **Breyta fyrirspurn** og **Svæðalisti** valmyndaratriðin tiltæk. Síðan **Breyta fyrirspurn** gerir kleift að setja upp skilyrði fyrir vinnu sem birtist í lista. Síðan **Reitalisti** gerir kleift að velja hvað reitir birtast í vinnulistanum. Til dæmis er hægt að draga úr fjölda reita sem birtast, svo að notandinn verði fljótari að velja mest viðeigandi vinnulið. Á flýtiflipanum **Almennt**, í reitnum **Færslur á síðu**, er einnig hægt að velja hversu margar verkfærslur á að birta á hverri síðu. Ef valkosturinn **Leyfa notendum að sía vinnu eftir færslugerð** er valinn, þá mun vinnulistinn innihalda stjórntækið **Sía vinnu** sem notandinn getur notað til að sía eftir færslugerð. Í vinnulistanum geta notendur aðeins séð vinnu sem þeir hafa heimild til að fá aðgang að. Það þarf að tryggja að notendur hafi heimild fyrir eina eða fleiri notandastýrð valmyndaratriði sem styðja tilteknar gerðir vinnuklasa sem þeir ættu að hafa aðgang að. Heimildir eru staðfestar þegar notandi reynir að framkvæma vinnu af listanum.|
| Stofna flutningspöntun úr númeraplötum | Gerir starfsmönnum vöruhúss kleift að stofna og vinna úr flutningspöntunum beint úr farsímaforriti vöruhúsakerfis. Starfsmenn í vöruhúsi byrja á því að velja vöruhús áfangastaðar og geta síðan skannað eina eða fleiri númeraplötur með því að nota forritið. Þegar starfsmaður í vöruhúsi velur **Ljúka við pöntun**, býr runuvinnsla til nauðsynlega flutningspöntun og pöntunarlínur samkvæmt skráðum lagerbirgðum fyrir þessar númeraplötur. Frekari upplýsingar er að finna í [Stofna flutningspantanir úr vöruhúsaforriti](create-transfer-order-from-warehouse-app.md).

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Skilgreina valmyndaratriði til að stofna vinnu fyrir annan starfsmann eða ferli

Þú getur sett upp valmyndaratriði sem býr til verk fyrir annan starfsmann eftir að upphafsaðgerð er gerð á fartækinu. Til dæmis þegar einn starfsmaður notar fartæki til að taka á móti vöru, er frágangsvinna stofnuð fyrir annan starfsmann. Til að setja upp valmyndaratriði sem býr til verk, á **Valmyndaratriði fartækis** síðunni í reitnum **Máti** skal velja **Vinna**. Í eftirfarandi töflu er valkostunum í **Ferli verkstofnunar** reitnum raðað eftir gerð verkstofnunar.

<table>
<tbody>
<tr>
<th>Gerð verkpöntunar</th>
<th>Valkostur</th>
<th>Lýsing</th>
</tr>
<tr>
<td rowspan="8">Innkaupapöntun</td>
<td>Móttaka innkaupapöntunarlínu</td>
<td>Skrá móttöku á magni vöru með því að nota númer innkaupapöntunar og línu innkaupapöntunarnúmers og stofna frágangsvinnu fyrir annan starfsmann.</td>
</tr>
<tr>
<td>Móttaka og frágangur innkaupapöntunarlínu</td>
<td>Skrá inngreiðsla á magn vara með því að nota númer innkaupapöntunar og lína númer innkaupapöntunarinnar og frágangur vörur. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td>Móttaka innkaupapöntunarvöru</td>
<td>Skrá móttöku á magni af vöru fyrir innkaupapöntun með því að skrá númer innkaupapöntunar og vörunúmer og stofna frágangsvinnu fyrir annan starfsmann.</td>
</tr>
<tr>
<td>Móttaka og frágangur innkaupapöntunarvöru</td>
<td>Skrá inngreiðsla á magn af vöru fyrir innkaupapöntun með því að skrá númer innkaupapöntunar og frágangur vöru. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td>Móttaka númeraplötu</td>
<td>Taka við tilkynningu um sendingu á innleið (ASN) með kenni númeraplötu.</td>
</tr>
<tr>
<td>Móttaka og frágangur númeraplötu</td>
<td>Taka við og ganga frá tilkynningu um sendingu á innleið (ASN) með kenni númeraplötu.</td>
</tr>
<tr>
<td>Móttaka farmvöru</td>
<td>Skrá móttöku á magni fyrir hleðslu með hleðslukenni og stofna frágangsvinnu fyrir annan starfsmann. Vara fjölda- og afurðarvíddir stemma innhreyfingar við innkaupapöntunarlínur.</td>
</tr>
<tr>
<td>Móttaka og frágangur farmvöru</td>
<td>Skrá móttöku á farmi með því að nota Farmkennið og ganga frá vörur. Vara fjölda- og afurðarvíddir stemma innhreyfingar við innkaupapöntunarlínur. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td rowspan="2">Skila pöntun</td>
<td>Móttaka skilapöntunar</td>
<td>Skrá móttöku á vörumagni með því að skrá RMA-númer og stofna frágang vinnu fyrir annan starfsmann.</td>
</tr>
<tr>
<td>Móttaka og frágangur skilapöntunar</td>
<td>Skrá inngreiðsla á magn vara með því að skrá RMA-númer og ganga frá vörur. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td rowspan="6">Flutningspöntun</td>
<td>Móttaka flutningspöntunarvöru</td>
<td>Skrá móttöku á vörumagni og stofna frágang vinnu fyrir annan starfsmann.

<strong>Athugið:</strong> Notaðu þennan valkost aðeins ef vörurnar voru sendar frá vöruhúsi sem er ekki virkt fyrir vöruhúsastjórnunarferli (WMS).</td>
</tr>
<tr>
<td>Móttaka og frágangur flutningspöntunarvöru</td>
<td>Skrá inngreiðsla á magn af vöru og frágangur vörur. Sami starfsmaður framkvæmir báðar aðgerðir.

<strong>Athugið:</strong> Notaðu þennan valkost aðeins ef vörurnar voru sendar frá vöruhúsi sem er ekki virkt fyrir vöruhúsastjórnunarferli (WMS).</td>
</tr>
<tr>
<td>Móttaka flutningspöntunarlínu</td>
<td>Skrá móttöku á vörumagni og stofna frágang vinnu fyrir annan starfsmann.</td>
</tr>
<tr>
<td>Móttaka og frágangur flutningspöntunarlínu</td>
<td>Skrá inngreiðsla á magn af vöru og frágangur vörur. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td>Móttaka númeraplötu</td>
<td>Taka við tilkynningu um sendingu á innleið (ASN) með kenni númeraplötu.</td>
</tr>
<tr>
<td>Móttaka og frágangur númeraplötu</td>
<td>Taka við og ganga frá tilkynningu um sendingu á innleið (ASN) með kenni númeraplötu.</td>
</tr>
<tr>
<td rowspan="4">Vinnsla</td>
<td>Bóka tilbúið</td>
<td>Skrá inn magn tilbúinnar vöru sem hefur verið lokið fyrir framleiðslu og stofna frágangsvinnu fyrir annan starfsmann. Magnið má sum eða öll magnið sem var áætlað fyrir framleiðslu.</td>
</tr>
<tr>
<td>Bóka sem tilbúið og ganga frá</td>
<td>Skrá inn magn tilbúinnar vöru sem hefur verið lokið fyrir framleiðslu og ganga frá vörur. Magnið má sum eða öll magnið sem var áætlað fyrir framleiðslu. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Benda til þess að Kanban sé lokið og stofna frágangsvinnu fyrir annan starfsmann.</td>
</tr>
<tr>
<td>Kanban-frágangur</td>
<td>Benda til þess að Kanban sé lokið og ganga frá vörum. Sami starfsmaður framkvæmir báðar aðgerðir.</td>
</tr>
<tr>
<td rowspan="5">Birgðir</td>
<td>Hreyfing</td>
<td>Skrá vörur sem hafa verið flutt af einum staðsetning á annan. Starfsmaðurinn tilgreinir staðsetning sem vörur eru fluttar úr og þar sem þau eru færð.</td>
</tr>
<tr>
<td>Biðgeymsla</td>
<td>Breyta stöðu birgðir á lager fyrir númeraplötu eða staðsetningu til að gera við skemmdar eða óvirkur vantar birgðavörur.</td>
</tr>
<tr>
<td>Hreyfingar eftir sniðmáti</td>
<td>Færa vörur af einum stað á annan á hálfsjálfvirkan hátt. Starfsmaðurinn velur staðsetningu til að flytja vörurnar úr og kerfið notar staðsetningarleiðbeiningarnar til að ákvarða hvert á að færa vörurnar.</td>
</tr>
<tr>
<td>Flutningur í vöruhús</td>
<td>Skrá vörur hafa verið fluttar úr einu vöruhúsi í annað. Þetta krefst að starfsmaðurinn hafi leyfi til að vinna í báðum vöruhúsum.

<strong>Athugið:</strong> Þetta valmyndaratriði krefst sjálfgefinnar birgðaflutningabókar þar sem reiturinn <strong>Útgáfa fylgiskjals</strong> er stilltur á <strong>Bókun</strong>.</td>
</tr>
<tr>
<td>Hleðsla númeraplötu</td>
<td>Notið þennan valkost þegar vöruhúsið er sett upp í fyrsta skinn.&#39; Skanna allra númeraplötur í öllum staðsetningum í vöruhúsi. Staðsetningar verða að vera númeraplötustýrðar. Ekki er hægt að nota þennan valkost ef <strong>Raðnúmer</strong> eða <strong>Rununúmer</strong> er talið fyrir ofan <strong>Staðsetningu</strong> í frátekningarstigveldi birgða.</td>
</tr>
<tr>
<td rowspan="3">Regluleg talning</td>
<td>Leiðrétting inn</td>
<td>Auka magn af vörum í birgðum. Tilgreina staðsetningu, númeraplötu, vöru, magn, mælieiningu og stöðu.</td>
</tr>
<tr>
<td>Leiðrétting út</td>
<td>Draga úr vörumagni í birgðum. Tilgreina staðsetningu, númeraplötu, vöru, magn, mælieiningu og stöðu birgða.</td>
</tr>
<tr>
<td>Regluleg stundartalning</td>
<td>Byrja að telja fyrir staðsetningu. Starfsmaðurinn verður að telja allar vörur á staðsetningu. Þegar niðurstöður talningu er minni en áætlað magn vantar magn telst tap.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Skilgreina valmyndaratriði til að vinna úr fyrirliggjandi vinnu
Auk þess að setja upp valmyndaratriði til að stofna vöruhúsavinnu, er hægt að setja upp valmyndaratriði til að vinna verk sem hafa þegar verið stofnuð. Stilla reitinn **Máti** á **Vinna** og velja valkostinn **Nota fyrirliggjandi vinnu**. Sumar viðbótarvalkostir verða svo tiltækir á flipanum **Almennt**. Hægt er að stjórna aðgangi að valmyndaratriðinu með því að tengja einn eða fleiria vinnuklasa á flýtiflipanum **Vinnuklasi**. Vinnuklasar skilgreina vinnu sem valmyndaratriðið getur unnið. Einnig er hægt að nota vinnuklasann til að veita aðgang að tilgreindum notendahlutverkum eða í aðskilda vinnslu fyrir mismunandi gerðir aðgerða. Eftirfarandi tafla lýsir þeim valkostum sem tiltækir eru. Hægt er að velja valkostinn undir **Stýrt af** reitnum á síðunni **Valmyndaratriði fartækis**. 

<table>




<thead>
<tr class="header">
<th>Valkostur</th>
<th>lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Enginn</td>
<td>Þetta sjálfgildi vinnur ekki úr vinnu.&#39;</td>
</tr>
<tr class="even">
<td>Stýrt af kerfi</td>
<td>Supply Chain Management stýrir gerð vinnu sem er úthlutað á starfskraft og pöntunina sem starfskrafturinn framkvæmir vinnuna á. Þegar þessi valkostur er valinn er hægt að velja <strong>Kerfisstýrt verk</strong> í aðgerðarúðunni til að opna síðuna <strong>Kerfisleiðbeindir röðunarkostir</strong> þar sem hægt er að setja upp röðunarskilyrði fyrir vinnuna. Röðunarforsendur að stýra röðinni sem starfskraftur framkvæmir vinnuna. Hægt er að bæta við eins mörgum skilyrðum og þarf.</td>
</tr>
<tr class="odd">
<td>Stýrt af notanda</td>
<td>Starfsmaðurinn velur að framkvæma vinnu og röðina sem á að framkvæma hana eftir.</td>
</tr>
<tr class="even">
<td>Notendaflokkun</td>
<td>Starfsmaðurinn flokkar handvirkt vinnu. Þessi valkostur er til dæmis gagnlegur þegar starfsmaður getur tekið saman margar vörur í einu á staðsetningu. Eftir að starfskraftur hefur lokið við að velja allar vörur sem þarf getur hann gengið frá þeim vörum.</td>
</tr>
<tr class="odd">
<td>Kerfisflokkun</td>
<td>Supply Chain Management-hópar vinna fyrir starfskraft á grundvelli ákveðins reits. Til dæmis tiltekt vinnu eru flokkaðar þegar starfsmaður skannar Auðkenni sendingar, Hleðsluauðkenni eða gildi sem hægt er að tengja hverrar vinnueiningar. Ef þessi valkostur er valinn, er krafa um eftirfarandi svæði:
<ul>
<li><strong>Kerfisflokkunarsvæði</strong> - Veldu reit sem starfsmaður mun skima til að flokka verkið.</li>
<li><strong>Kerfisflokkunarmerki</strong> - Sláðu inn texta til að leiðbeina starfsmanni um hvað ég á að skanna til að flokka verkið.</li>
</ul></td>
</tr>
<tr class="even">
<td>Stýrt af staðfestum notanda</td>
<td>Starfsmaðurinn velur vinnu sem á að framkvæma þegar verk er tengt stærri einingu, eins og farmi eða sendingu. Starfskrafturinn ákvarðar röðina sem vörurnar eru tíndar í. Ef þessi valkostur er valinn, er krafa um eftirfarandi svæði:
<ul>
<li><strong>Reit stýrt af staðfestum notanda</strong> - Veldu reit sem starfsmaður mun skima til að flokka verkið.</li>
<li><strong>Merkimiða stýrt af staðfestum notanda</strong> - Sláðu inn textann sem leiðbeinir starfsmanni um hvað á að skima þegar tínsluverk er flokkað af kerfinu.</li>
</ul>
Þessi valkostur er til dæmis gagnlegur þegar mörg bretti eru sett upp fyrir hleðslu. Ef reiturinn <strong>LoadId</strong> í <strong>Stýrt af staðfestum notanda</strong> er valinn getur starfsmaðurinn tekið öll bretti sem eru tengd við hleðslu. Starfskrafturinn fær villuboð ef hann skannar vöru sem er ekki tengd við hleðslu.&#39;</td>
</tr>
<tr class="odd">
<td>Klasatiltekt</td>
<td>Flokka starfsmanna sem vinna í klasa. Klasar leyfa starfsmönnum að taka vörur frá einni staðsetningu fyrir margar pantanir vinnu á sama tíma.</td>
</tr>
<tr class="even">
<td>Flokkun reglulegrar talningar</td>
<td>Starfsmaðurinn velur svæði, vinnuhópi eða staðsetningu, og Supply Chain Management úthlutar vinnu sem byggir á vali. Ef þessi valkostur er valinn, er einnig hægt að smella á <strong>Regluleg talning</strong> til að tilgreina viðbótarupplýsingar til að birta og tilgreina hversu oft starfskrafturinn verður að endurtaka talninguna ef mismunur fannst.</td>
</tr>
 <tr class="odd">
<td>Farmflutningur</td>
<td>Þessi eiginleiki gerir nokkrum starfskröftum í vöruhúsi kleift að hlaða birgðum frá sömu hleðslu eða öðrum hleðslum á sama vörubílnum, með hleðslum sem hafa verið sendar að fullu eða að hluta.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Fleiri valkostir valmyndaratriðis
Fleiri valkostir valmyndaratriða eru tiltækir á síðunni **Valmyndaratriði fartækis**. Valkostirnir eru mismunandi, eftir ferlinu sem verið er að skilgreina valmyndaratriði fyrir. 

Eftirfarandi tafla lýsir þessum valkostum.

<table>




<thead>
<tr class="header">
<th>Reitur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Leyfa skiptingu vinnu</td>
<td>Veljið þennan valkost til að leyfa notendum að setja vörur fyrir vinnupantanir á fleiri en eina númeraplötu markmiðs. Þessi valkostur er til dæmis gagnlegur þegar númeraplata markmiðs er full og starfsmaður þarf að bæta eftirstandandi vörum á aðra númeraplötu. Starfskrafturinn getur valið <strong>Fullt</strong> til að tilgreina númeraplatan er full og stöðva móttöku tiltekt vinnu fyrir hana. Staðsetning frágangs fyrir tilteknar vörur er síðan birt og tiltekt vinnu sem er þegar lokið er færð í nýja pöntun vinnu. Eftirstöðvar vinnu fyrir yfirnúmeraplötunni tiltekt lágmarksstiginu á vinnu á upprunalegu pöntuninni.</td>
</tr>
<tr class="even">
<td>Festing</td>
<td>Veljið þennan valkost til að leyfa starfsmönnum að tilgreina staðsetninguna sem hnekkir ráðlagðri sviðsetningar- eða hleðslustaðsetningu. Allri eftirstandandi frágangsvinnu er beint á nýja staðsetningu. Þessi valkostur er til dæmis gagnlegur þegar starfsmaður sem verður að setja vörur í pöntun 1 í sviðsetningarstaðsetningu á dreifingarstöð 1 getur það ekki, þar sem fyrri farmur hefur ekki verið hreinsaður af staðsetningu. Frekar en að bíða eftir að sviðsetningarstaðsetning á dreifingarstöð 1 verði tiltæk getur starfsmaðurinn ákveðið að nota staðsetningu sviðsetningar fyrir dreifingarstöð 2. Í þessu tilfelli hnekkir starfsmaðurinn ráðlagðri staðsetningu sviðsetningar. Frágangsstaðsetning fyrir allar eftirstandandi vörur er síðan uppfærð í staðsetningu sviðsetningar á dreifingarstöð 2. Ef þessi valkostur er valinn verður að velja reitinn <strong>Festa eftir</strong>.</td>
</tr>
<tr class="odd">
<td>Akkeri með</td>
<td>Ef festing er notuð verður að tilgreina hvort eigi að festa eftir sendingu eða farmi.&#39;</td>
</tr>
<tr class="even">
<td>Auðkenni endurskoðunarsniðmátsins</td>
<td>Veljið endurskoðunarsniðmátinu sem mun rjúfa vinnuferli fyrir þessu valmyndaratriði þannig að hægt sé að framkvæma aðra aðgerð. Til dæmis, ef þetta valmyndaratriði er fyrir vinnu á innleið gæti endurskoðunarsniðmátið krafist að starfsmaður athugi hitastig í geymi afhendingar. Punkturinn þegar ferlið er rofið er tilgreindur í endurskoðunarsniðinu. Þessi tímapunktur getur til dæmis verið þegar vinna er hafin eða lokið, eða þegar staða hennar breytist.</td>
</tr>
<tr class="odd">
<td>Auðkenni klasanotandaupplýsinga</td>
<td>Veljið klasanotandaupplýsingar sem nota á við klasatínslu. Klasanotandaupplýsingar innihalda stillingar eins og hvort eigi að stofna klasa sjálfkrafa, nöfn á stöðum og fjölda vinnueininga sem hægt er að úthluta á þær, hvenær á að brjóta klasa upp í stakar einingar og hvort sannprófun áskilin. Þessi reitur er aðeins tiltækur ef <strong>Klasatiltekt</strong> er valin í reitnum <strong>Stýrt af</strong>.</td>
</tr>
<tr class="even">
<td>Telja heildarmagn vöru fyrst</td>
<td>Veljið þennan valkost til að krefjast starfsmanns til að telja heildarmagn fyrst meðan á talningu stendur. Ef mismunur er fannst verður starfsmaður að veita viðbótarupplýsingar, eins og númeraplötunúmer, rununúmer og raðnúmer.</td>
</tr>
<tr class="odd">
<td>Stofna hreyfingu</td>
<td>Veljið þennan gátreit til að leyfa starfsmanni til að stofna vinnu fyrir hreyfingu án þess að krefjast að starfsmaðurinn til að framkvæma verkið strax. Þessi valkostur er til dæmis gagnlegur ef gæðaeftirliti hefur verið lokið og eftirlitsaðilinn vill láta flytja vöru af gæðaeftirlitssvæðinu.</td>
</tr>
<tr class="even">
<td>Leiðbeiningarkóði</td>
<td>Til að nota tilteknar staðsetningarleiðbeiningar skal velja leiðbeiningarkóða sem tengist staðsetningarleiðbeiningum. Þessi reitur er tiltækur þegar vinna er stofnuð og myndunarferli vinnu er <strong>Hreyfingar eftir sniðmáti</strong>.</td>
</tr>
<tr class="odd">
<td>Gera þröskuld fyrir reglulega talningu óvirkan</td>
<td>Veljið þennan valkost til að hunsa þröskulda fyrir reglulega talningu. Ef þessi valkostur er valinn stofnast vinna reglulegrar talningar ekki þegar farið er yfir þröskuldargildi.&#39;</td>
</tr>
<tr class="even">
<td>Birta ráðstöfunarkóða runu</td>
<td>Veljið þennan valkost til að birta ráðstöfunarkóða runu. Til dæmis er hægt að birta ráðstöfunarkóða runu við móttöku skilaðrar runu. Síðan geta starfsmenn metið stöðu eða gæði runu og valið viðeigandi kóða. Reglur um ráðstöfunarkóða runu ákvarða hvort runuvinnslan verður tiltæk í öðru ferli vöruhúsa. Ef þessi valkostur er ekki valinn er einn eftirfarandi ráðstöfunarkóða runu notaður:&#39;
<ul>
<li>Ef nýtt rununúmer er móttekið er sjálfgefinn ráðstöfunarkóði runu sem er tilgreint í vörulíkanaflokk.</li>
<li>Ráðstöfunarkóði runu sem er þegar úthlutaður á rununa.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Birta ráðstöfunarkóða</td>
<td>Veljið þennan valkost til að birta ráðstöfunarkóða. Til dæmis er hægt að birta ráðstöfunarkóða við móttöku skilavöru. Síðan geta starfsmenn metið stöðu eða gæði vöru og valið viðeigandi kóða. Reglur um ráðstöfunarkóða sem ákvarða hvort vörurnar verða tiltækar fyrir önnur vöruhús ferli.</td>
</tr>
<tr class="even">
<td>Birta birgðastöðu</td>
<td>Veljið þennan valkost til að birta stöðu á vörum í birgðum. Þessi valkostur er tiltækur fyrir alla valmyndaratriði sem nota fyrirliggjandi vinnu nema reglulega talningu.</td>
</tr>
<tr class="odd">
<td>Birta samantekt af tiltektarskjá</td>
<td>Veljið þennan valkost til að birta yfirlit yfir tiltekt vinnu fyrir valda vinnustöð. Yfirlit er birt þar til fyrstu vinnulínunni er unnin fyrir vinnustöðina.</td>
</tr>
<tr class="even">
<td>Mynda númeraplötu</td>
<td>Veljið þennan valkost til að mynda einkvæmt númeraplötunúmer út frá val númeraraðar. Til dæmis er hægt að mynda númeraplötunúmer fyrir vörur sem er mótteknar fyrir innkaupapantanir.</td>
</tr>
<tr class="odd">
<td>Frágangur hóps</td>
<td>Veljið þennan valkost til að flokka frágangsvinnu. Þessi kostur er tiltækur þegar vinnunni var flokkað af starfsmanni eða af Supply Chain Management. Þegar starfsmaðurinn hefur lokið allri tiltektarvinnu í flokki, er frágangur stofnaður fyrir sama flokk.</td>
</tr>
<tr class="even">
<td>Gerðir leiðréttinga á birgðaskrá</td>
<td>Veljið gerð leiðrétting á birgðaskrá sem ákvarðar birgðamagn talningarbókar sem er notuð til að bóka leiðréttingar og hvort á að fjarlægja frátekningar. Þessi reitur er aðeins í boði stofnunarferlið <strong>Leiðrétting inn</strong> eða <strong>Leiðrétting út</strong>.</td>
</tr>
<tr class="odd">
<td>Hnekkja rununúmeri</td>
<td>Veljið þennan valkost til að leyfa starfsmönnum sem skrá magn sem tilbúið fyrir framleiðslupöntun að færa inn rununúmer sem eru önnur en rununúmer sem eru tengd við framleiðslupöntun.</td>
</tr>
<tr class="even">
<td>Hnekkja yfirnúmeraplötu</td>
<td>Veljið þennan valkost til að leyfa starfsmönnum að tilgreina mark númeraplötunúmer sem er önnur en ráðlögð marknúmeraplata. Notið þennan valkost þegar fyrsta tiltekt fyrir vinnu er fyrir allt magn vöru á númeraplötu. Þess valkostur er til dæmis gagnlegur þegar bretti eru notuð aftur.</td>
</tr>
<tr class="odd">
<td>Taka til og pakka</td>
<td>Veljið þennan valkost til að leyfa starfsmönnum að sameina vinnu fyrir sölupöntun eða hleðslu í staka vinnueiningu. Starfsmaður getur unnið vinnu aðeins fyrir sölupöntun eða hleðslu. Þessi valkostur er til dæmis gagnlegur þegar auka þarf magn fyrir sölupöntun eftir að hleðsla, sending og vinna hefur verið stofnuð fyrir sölupöntunina. Þessi valkostur er tiltækur þegar valmyndaratriðið notar fyrirliggjandi vinnu og vinnu sem er stýrt af notanda eða kerfið.</td>
</tr>
<tr class="even">
<td>Tína elstu runu</td>
<td>Gefa til kynna hvort starfsmaður verði að velja elstu rununa í staðsetningu fyrst. Eftirtaldir valkostir eru í boði:
<ul>
<li><strong>Ekkert</strong> - Starfsmaður getur tekið til hvaða lotu sem er á staðnum. Starfsmaðurinn fær engin skilaboð.</li>
<li><strong>Vara við</strong> - Starfsmaður getur valið hvaða lotu sem er á stað, en hann fær viðvörunarboð ef lotan er ekki elsta lotan.&#39;</li>
<li><strong>Þvinga</strong> - Starfsmaður verður að taka til elstu lotu á staðnum. Starfsmaðurinn fær villuboð ef lotan er ekki elsta lotan.&#39; <strong>Ábending:</strong> Þessi valkostur er aðeins viðeigandi ef <strong>Rununúmer</strong> er lægra en <strong>Staðsetning</strong> í frátekningarstigveldinu sem er úthluta á vöruna.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Prenta merki</td>
<td>Veljið þennan gátreit til að leyfa starfsmönnum að prenta merkimiða á númeraplötu.</td>
</tr>
<tr class="even">
<td>Kerfisflokkunarsvæði</td>
<td>Velja reitinn sem ákvarðar hvernig Supply Chain Management flokkar tiltektarvinnu fyrir starfsmenn. Til dæmis, ef þú velur <strong>ShipmentId</strong> svæðinu starfsmaður verður skanna Sendingarkennið til að flokka vinnuna tiltekt. Öll vinna fyrir sendingunni er síðan úthlutað til starfsmanns. Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu. Einnig verður að færa inn texta í reitinn <strong>Kerfisflokkunarmerki</strong> til að sýna starfsmanni hvað á að skanna.</td>
</tr>
<tr class="odd">
<td>Kerfisflokkunarmerki</td>
<td>Sláðu inn textann sem leiðbeinir starfsmanni um hvað á að skima þegar tínsluverk er flokkað af Supply Chain Management. Til dæmis, ef verið er að nota í <strong>ShipmentId</strong> á flokki tiltekt vinnu með sendingu, gætirðu fært inn <strong>Sendingarkennið</strong> í svæðinu.&#39; Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu. Einnig verður að velja reitinn til að flokka eftir í reitnum <strong>Kerfisflokkunarsvæði</strong>.</td>
</tr>
<tr class="even">
<td>Nota sjálfgefinn gagnagrunn</td>
<td>Veljið þennan valkost til að virkja hnappinn <strong>Sjálfgefin gögn</strong> í aðgerðarúðunni, þar sem hægt er að velja reiti til að birta gögn sem starfskraftur þarf yfirleitt í dagleg störfum. Þessi valkostur er til dæmis gagnlegur ef starfsmaður tekur oft til vörur frá sömu staðsetningu. Hægt er að velja reitinn <strong>Frá staðsetningu</strong> til að birta staðsetninguna sjálfgefið.</td>
</tr>
<tr class="odd">
<td>Reit stýrt af staðfestum notanda</td>
<td>Velja svæðið sem starfsmaðurinn mun skanna til að flokka vinnuna. Til dæmis, ef þú velur <strong>LoadId</strong>, getur starfsmaður tekið til alla vinnu sem er tengd við völdu hleðsluna. Einnig verður að færa inn texta í reitinn <strong>Merkimiða stýrt af staðfestum notanda</strong> til að sýna starfsmanni hvað á að skanna.</td>
</tr>
<tr class="even">
<td>Merkimiða stýrt af staðfestum notanda</td>
<td>Sláðu inn textann sem leiðbeinir starfsmanni um hvað á að skima þegar tínsluverk er flokkað af staðfestum notanda. Til dæmis, ef þú notar reitinn <strong>LoadId</strong> til að flokka tiltektarvinnu fyrir hlass, ættirðu að færa inn <strong>Hleðsluauðkenni</strong> í reitnum.</td>
</tr>
<tr class="odd">
<td>Kóði vinnusniðmáts</td>
<td>Veljið vinnusniðmátið sem mun stofna vinnu fyrir ferli. Til dæmis ef þú móttekur vöru í innkaupapöntun verður frágangsvinna mynduð samkvæmt vinnusniðmátinu. Ef vinnusniðmát er ekki valið úthlutar Supply Chain Management sniðmáti, samkvæmt skilyrðum fyrirspurnar. Sjá frekari upplýsingar um vinnusniðmát í <a href="control-warehouse-location-directives.md">Vöruhúsavinnu stýrt með vinnusniðmátum og staðsetningarleiðbeiningar</a>.</td>
<tr class="even">
<td>Sýna vinnulínulista</td>
<td>Veljið valkost fyrir það hvernig starfskraftar geta skoðað og haft áhrif á línurnar fyrir þá tiltektarvinnu sem er valin. Frekari upplýsingar um þennan valkost fást í <a href="pick-line-overview.md">Setja upp valmyndaratriði fartækis til að birta yfirlit yfir val á línu</a></td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Krefjast að starfsmenn staðfesti afurð, staðsetningu eða magn við tiltekt á vörum

Þú getur sett upp verkstaðfestingar sem krefjast þess að starfskraftur noti fartækið til að skrá staðsetningu eða magn þegar vinna er unnin í vöruhúsi. Verkstaðfestingar hjálpa við að tryggja að starfsmaðurinn sé á réttum stað eða sé að meðhöndla rétt magn vara. Einnig er hægt að virkja Supply Chain Management til að staðfesta skráningu starfsmanns sjálfkrafa. Ef sjálfvirk staðfesting er virkjuð er ekki hægt að krefjast einnig staðfestinga fyrir staðsetningu eða magn. Verkstaðfestingar innihalda einnig afurðir og afurðarafbrigði. Þar að auki er hægt að skrá staðfestingar með því að skanna strikamerki. Til að staðfesta afurðir og afurðarafbrigði, verður að færa inn kenni fyrir afurð eða afurðarafbrigði. Þetta kenni getur verið Afurðakenni, Afurðarkenni leit, ytri Kenni, GTIN eða strikamerki. Eftir að þú slærð inn kennið eða skannar strikamerki eru stærðir fyrir afurðarafbrigði birt á farsímanum. 

Eftirfarandi tafla lýsir mismunandi gerðum vinnu sem hægt er að nota verkstaðfestingar með.

| Valkostur | Lýsing |
|------------------------|----------------------------------------------------------------------------|
| Taka til | Óska eftir staðfestingu við tiltekt á vörum. |
| Frágangur | Óska eftir staðfestingu þegar vörur eru settar á staðsetningu. |
| Talning | Óska eftir staðfestingu við reglulega talningu. |
| Leiðréttingar | Óska eftir staðfestingu þegar birgðamagn er leiðrétt. |
| Sérstilla | Óska eftir staðfestingu sérsniðinnar vinnu. |
| Biðgeymsla | Óska eftir staðfestingu þegar vörur eru fluttar í biðgeymslu. |
| Röðun númeraplötu | Óska eftir staðfestingu þegar vörur eru sameinaðar til að byggja númeraplötu. |
| Prenta | Óska eftir staðfestingu við prentun merkimiða á númeraplötu. |
| Stöðubreyting | Óska eftir staðfestingu við breytingu á stöðu birgða. |

> [!NOTE]
> Aðeins er hægt að fara fram á staðfestingu afurðar fyrir gerðirnar tínslu og frágang.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Setja upp valmyndaratriði fartækis til að ljúka vinnu af gerðinni innkaupapöntun](tasks/set-up-mobile-device-menu.md)
- [Setja upp valmyndaratriði fartækis til að skrá mótteknar vörur](tasks/set-up-mobile-device-menu-item-register-received-items.md)
- [Birgðastöður](../inventory/inventory-statuses.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
