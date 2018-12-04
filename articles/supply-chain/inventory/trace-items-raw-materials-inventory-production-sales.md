---
title: "Rakning á vörum og hráefni í birgðum, framleiðslu og sölu"
description: "Þetta efnisatriði lýsir því hvernig hægt er að nota vörurakning til að auðkenna þar sem vörur eða hráefni hafa verið notaðar, eru notaðar eða verða notaðar í framleiðslu- og söluferla."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 60edc05bb45db973eb2e16dd833015c9a4873918
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Rakning á vörum og hráefni í birgðum, framleiðslu og sölu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að nota vörurakning til að auðkenna þar sem vörur eða hráefni hafa verið notaðar, eru notaðar eða verða notaðar í framleiðslu- og söluferla.

Aðgerðin vörurakning er tiltæk á síðunni **Vörurakning**. Eftirfarandi kaflar lýsa því hvernig hægt er að nota vörurakningu og hvaða valkostir og takmarkanir eru.

## <a name="what-is-item-tracing"></a>Hvað er vörurakning?
Vörurakning er viðskiptagreindartól sem gefur uppsprettu og áfangastað vara og hráefna í framboðskeðjunni sýnileika. Framleiðendur geta rakið vörur, hráefni eða efni til baka til lánardrottins og áfram í gegnum framleiðslu og sölu á fullunninni vöru. Vörurakning hjálpar framleiðendum að uppfylla reglur og hjálpar einnig gæðayfirmönnum og framleiðslustjórnendum að greina og grípa til aðgerða til að takast á við dreifni í gæðum á vörum og efnum. Hér eru nokkur dæmi um leiðir sem framleiðendur geta notað vörurakningu:

-   Auðkenna upphæð vöru eða hráefnis sem er í birgðum á þeim tímapunkti og hvar það er geymt.
-   Ákvarða hversu mikið af vöru eða hráefni hefur verið sent og til hvaða viðskiptavina.
-   Auðkenna áætlaðan sendingar sem taka á vöruna eða hráefni.
-   Finna framleiðslupantanir sem nota vöruna eða hráefnið og eru fyrirhugaðar, í vinnslu eða skráð sem lokið.
-   Finna út hvar sem vara eða hráefni var keypt.
-   Rannsaka þar sem vara eða hráefni var notuð í framleiðslu á annarri vöru.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Það getur I rekja og það eru engar takmarkanir?
Hægt er að rekja sögulegar birgðafærslur fyrir vörur og hráefni samkvæmt vörunúmeri og rakningarvídd, svo sem raðnúmer, rununúmer eða rununúmer lánardrottins. Ef rakningarvídd er ekki úthlutað er ekki hægt að rekja vöruna eða hráefnið. Þar sem rakning er byggð á birgðafærslum, eru einhverjar takmarkanir þegar vörur eru raktar. Til dæmis eru takmarkanir tengdar færslum fyrir verk, eignir og smásölu. Þar að auki eru aukaafurðir sýndar í rakningaratriðum, en hliðarafurðir eru ekki hafðar með. Rakningin inniheldur allar vöruhúsafærslur frá einni staðsetningu til annarar. Þess vegna gætu notendur fundið magn upplýsinga svolítið yfirþyrmandi. Rakningin er sýnd fyrir einn lögaðila í einu. Engin eiginleikar milli fyrirtækja eru í samhengi innan samstæðu. Það þarf að hefja nýja rakningu fyrir hvert fyrirtæki þar sem vara er móttekin eða gefin út.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Hvaða skilyrði geta I tilgreina vöru rakningu?
Skilyrðin sem krafist er fyrir vörurakningu eru vörunúmer, rakningarvídd (eins og rununúmer eða raðnúmer) og stefna. Eftirfarandi tafla lýsir þeim skilyrðum sem hægt er að nota í vöru rakningu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Svæðaflokkur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vörunúmer</td>
<td>Færa inn kenni fyrir vöru eða hráefni sem verið er að rekja.</td>
</tr>
<tr class="even">
<td>Afurðarvíddir</td>
<td>Valfrjálst: Rekja tilteknum eiginleikum afurðarskilgreininguna, eins og skilgreining, stærð, lit eða stíl.</td>
</tr>
<tr class="odd">
<td>Rakningarvíddir</td>
<td>Færið inn rununúmer, rununúmer lánardrottins eða raðnúmer rakningarvíddar. Þegar rununúmer er notað sem skilyrði, birtist rununúmer lánardrottins ef þær upplýsingar hafa verið teknar.</td>
</tr>
<tr class="even">
<td>Geymsluvíddir</td>
<td>Valfrjálst: Rekja vörur sem hafa verið geymd á ákveðinni staðsetningu.</td>
</tr>
<tr class="odd">
<td>Tímabil</td>
<td>Valfrjálst: Sláðu inn dagsetningu og takmarka rakningu til tiltekins tíma. Rakningaratriðin munu aðeins birta skjöl og færslur sem voru stofnaðar milli þessara dagsetninga.</td>
</tr>
<tr class="even">
<td>Fram eða aftur</td>
<td>Veljið stefnu fyrir rakningu. Hægt er að rekja áfram eða afturábak:
<ul>
<li><strong>Afturábak</strong> - Leitið niður á við til að greina upprunann og magnið sem er enn til taks, og allar framleiðslupantarnir sem eru a.m.k. að hluta til tilkynntar sem tilbúnar.</li>
<li><strong>Fram á við</strong> - Leita upp á við til að bera kennsl á áfangastað. Hægt er að finna sölupantanir og viðskiptavini sem rakta varan eða hráefnið hefur verið sent til að minnsta kosti að hluta.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Hvaða upplýsingar fylgja í rakningarupplýsingunum?
Niðurstöður rakningar eru birtar í tímaröð í trénu á flýtiflipanum **Upplýsingar** í skjámyndinni **Vörurakning**. Pöntunin er breytileg eftir stefnu rakningu. Upplýsingarnar innihalda allar færslur í innkaupum vöru frá lánardrottni til sölu á vörunni til viðskiptavinarins. Rakninganiðurstöður innihalda einnig bráðabirgðaafurðir sem eru tengdar vöru- eða rakningarvídd sem tilgreind var í rakningarskilyrðum. Topphnúturinn sýnir magn vöru, í birgðaeiningum, sem eftir eru á lager eftir geymsluvíddunum sem tilgreindar voru í rakningarskilyrðum. **Athugið:** Upplýsingar um rakningu eru skyndimynd af upplýsingunum sem voru tiltækar þegar rakningin var framkvæmd. Upplýsingar um rakningu eru ekki uppfærðar ef upplýsingarnar breytast eftir að rakningin var framkvæmd.

## <a name="why-dont-some-nodes-contain-any-details"></a>Af hverju innihalda ekki sumir hnútar nainar upplýsingar?
Til að minnka magn upplýsinga í rakningarupplýsingunum, inniheldur aðeins hnúturinn fyrir fyrsta tilvik vöru eða hráefnis upplýsingar. Ef valinn hnútur inniheldur ekki upplýsingar, er hægt að skoða hnút sem er með þær með því að smella á **Fara í rakta línu**. Hægt er að snúa aftur í hnút sem farið var úr með því að smella á **Fara til baka**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Get ég skoðað aðeins ákveðinni gerð skjals? Til dæmis, get ég skoðað aðeins framleiðslupantanir, viðskiptavini eða lánardrottna?
Já, hægt er að opna lista yfir listasíður sem innihalda aðeins ákveðna gerð skjals eða færslu úr rakningaratriðunum. Hægt er að opna þessar síður frá valmyndaratriðinu **Rakning** á Aðgerðarrúðunni, í flokkunum **Vara**, **Sölur**, **Innkaup**, **Framleiðsla**, og **Gæði**. Til að skoða til dæmis lista yfir lánardrottna í rakningarupplýsingunum skal smella á **Rakning** &gt; **Innkaup** &gt; **Lánardrottnar**. Lista yfir listasíður saman færslur úr rakningaratriðunum eða skjöl. Listasíðurnar **Færslur í bið**, **Pantanir í bið**, og **Ósendar sölupantanir** sýna einnig aðrar upplýsingar sem eru ekki teknar með í rakningarupplýsingunum. Þar að auki sýna þær alltaf niðurstöður frá gildandi dagsetningu, óháð því hvort dagsetningarbil hefur verið tilgreint. Eftirfarandi tafla lýsir viðbótarupplýsingar sem hægt er að hafa þessar síður.

| Listar                    | Lýsing                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sölupantanir sem voru ekki sendar | Skoða sölupöntunarlínur sem hafa ekki verið teknar til og birtast því ekki í rakningarupplýsingunum.                                                                                                                                                                                                                        |
| Pantanir í bið           | Skoða allar pantanir yfirvofandi framleiðslu fyrir rakin vara, rakningarvíddir sem voru notaðir í rakningarskilyrðum. Einnig er hægt að skoða framleiðslupantanir í bið þar sem er rakin vara er efni, og þar sem engar skráningar hafa verið gerðar og engar færslur eru skráðar sem loknar fyrir pöntunina. |
| Færslur í bið     | Skoða biðfærslur rakin vara sem inniheldur tilgreinda rakningarvíddir eða autt rakningarvídd. Einnig er hægt að skoða birgðafærslur í bið fyrir vörur og rakningarvíddasamsetningar, eða autt gildi, í rakningarupplýsingunum.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Hversu mörg stig get ég rakið upp eða niður í uppskrift eða formúlu?
Hægt er að rekja eitt stig upp eða niður í uppskrift eða formúlu. T.d. ef verið er að keyra rakningu á hráefni, hægt er að sjá hvaða aukaafurðir og endanlegu vöruna. Hins vegar ef aukaafurð er rakin innihalda rakningaratriðin ekki endanlega vöru.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Hvernig get ég skoðað frekari upplýsingar um skjalið eða færslu í rakningarupplýsingunum?
Á flýtflipanum **Upplýsingar** eru tvær leiðir til að skoða frekari upplýsingar um valið skjal eða færslu í rakningarupplýsingum:

-   Þegar hnútur í rakningarupplýsingunum á flýtiflipanum **Upplýsingar** er valinn, birta aðrir flýtiflipar í skjámyndinni upplýsingar um skjalið eða færslu í hnútnum.
-   Opnið upplýsingaskjámyndina fyrir skjalið í völdum hnút með því að smella á **Skoða upplýsingar**. Til dæmis, ef verið er að velja hnút sem lýsir framleiðslupöntun og smellt er á **Skoða upplýsingar**, birtist síðan **Upplýsingar um framleiðslupöntun**.

Sumir flýtiflipar veita aðgang að viðbótarupplýsingum um valinn hnút. Til dæmis í flýtiflipanum **Ósamkvæmnitilvik** er hægt að smella á **Fyrirspurnir** til að athuga hvort saga sé um ósamkvæmni. Á flýtiflipanum **Runa** er hægt að smella á **Listi á lager** til að skoða magn af efnislegum birgðum sem eru á lager, og allar birgðafærslur sem innihalda rununa.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Get ég keyrt fleiri en eina rakningu og borið svo saman upplýsingarnar?
Eftir að þú hefur keyrt rakningu er hægt að nota valkostina á hnappnum **Rekja úr hnút** til að keyra nýja rakningu á færslu í völdum hnút:

-   **Afturábak** eða **Fram á við** - Byrja nýja rakningu fyrir valinn hnút, og skrifa yfir upplýsingar um núverandi rakningu.
-   **Nýtt afturábak** eða **Nýtt fram á við** - Byrja nýja rakningu í nýjum glugga og geyma upplýsingar um núverandi rakningu.

Viljir þú nota valkostina **Nýtt afturábak** eða **Nýtt fram á við**, verður að nota aðgerðina **Opna í nýjum glugga** til að hafa nýja rakningu í nýjum glugga.

## <a name="can-i-save-the-trace-details"></a>Get ég vista rakningaratriðunum?
Hægt er að vista upplýsingar sem xml-skrá í flipanum <strong>Upplýsingar</strong> með því að smella á <strong>Flytja út</strong> fyrir neðan aðgerðina *<strong><em>Rakning</em></strong>* á aðgerðasvæðinu. Til viðbótar upplýsingum um rakningu, inniheldur xml skráin rakningarskilyrði, yfirhnúta og magn á lager. Getan til að vista upplýsingar um rakningu er gagnleg, til dæmis, ef óskað er að tengja upplýsingar gæðapöntun eða öðrum samræmingarskjölum. Hægt er að tilgreina hvar vista skrána. Veljið valkostinn <strong>Sýna skjal</strong> til að skoða skrána þegar í stað. <strong>Athugið:</strong>Skráin er alltaf vistuð, jafnvel ef eingöngu á að skoða hana. Að sjálfgefnu opnar xml-skrána í vafra glugga. Hins vegar er hægt að hægrismella á skrána, velja <strong>Opna með</strong>, og velja síðan forritið sem nota skal til að birta efnið.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Get ég að reiknað út stöðu fyrir tiltekna vöru eða innihaldsefnisins?
Hægt er að flytja upplýsingar úr samantektarskjámyndum yfir í Microsoft Excel. Opnið viðeigandi síðu, smellið á táknið **Opna í Microsoft Office** og veljið svo **Flytja út í Microsoft Excel**. Þetta er sérlega gagnlegt þegar á að reikna út fjöldajanfvægi fyrir vöru eða efni frá síðunni **Samantekt á færslum**. Á síðunni **Samantekt á færslum** er hægt að afmarka vöruna eða efnið, og framleiðslulotu ef óskað er, og flytja síðan upplýsingarnar til Excel. Í Excel er til dæmis hægt að einangra magn á lager, magn sem var selt, og upphæð sem var notuð í framleiðslu.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Get ég athugað hvort saga sé um vandamál varðandi vörur eða hráefni?
Rakningaratriðin innihalda upplýsingar um gæðapantanir og ósamkvæmnitilvik sem snerta vöru eða hráefni. Hægt er að skoða yfirlit yfir gæðapantanir og ósamkvæmni með því að smella á **Gæðapantanir** eða **Ósamkvæmnitilvik** á Aðgerðarrúðunni. **Athugið:** Eyðileggingargæðapantanir geta birst oftar en einu sinni í rakningarupplýsingunum. Þegar eyðileggingargæðapöntun er stofnuð fyrir skjal eins og innkaupapöntun, birtist hún fyrir hverja færslu fyrir skjalið.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Eru einhverjar skýrslugerðaraðgerðir sem eru tengdar vörurakningu?
Hægt er að mynda skýrsluna **Sent til viðskiptavina** til að auðkenna magn vöru eða hráefnis sem hefur verið sent og viðskiptavinina  sem það var sent til. Fyrir fyrirspurn sem tengist samræmi, er hægt að mynda skýrslu fyrir alla viðskiptavini. Fyrir fyrirspurn sem tengist þjónustudeild, er hægt að mynda skýrslu fyrir valinn viðskiptavin. Ef varan var hráefni sem var notaður í framleiðslu á tilbúinni vöru, tilbúna vöru er einnig tekin með. **Athugið:** Ef verið er að nota aðgerðir fyrir eyðingu- eða safnvistun sölupantana, hafa niðurstöður skýrslunnar einnig með allar sölupantanir sem hefur verið eytt eða safnvistaðar.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Get ég rakið aukaafurðir og hliðarafurðir?
Hægt er að rekja aukaafurðir, en ekki er hægt að rekja hliðarafurð því rakningarvíddum er yfirleitt ekki úthlutað á þær. Þegar vara er rakin, eru allar tengdar aukaafurðir teknar með í rakningarupplýsingunum. Hnútur sem inniheldur aukaafurð inniheldur orðið "aukaafurð" í upplýsingar. Einnig er hægt að skoða upplýsingar um aukaafurð með því að velja hnútinn í rakningarupplýsingunum, og smella svo á flýtiflipann **Framleiðsla**.

