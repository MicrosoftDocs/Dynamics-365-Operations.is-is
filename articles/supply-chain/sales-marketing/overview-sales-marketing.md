---
title: "Sala og markaðsstarf"
description: "Hægt er að nota Sölu og markaðsstarfs til að fá, geyma og nota ýmsar gögn í söluflæði. Þessi gögn inniheldur upprunalega sölupöntun átaki, síðari eftirfylgni og frekari sölu."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d810ff4028884cce5089c59d424aa92981dc5673
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="sales-and-marketing"></a>Sala og markaðsstarf

[!include[banner](../includes/banner.md)]


Hægt er að nota Sölu og markaðsstarfs til að fá, geyma og nota ýmsar gögn í söluflæði. Þessi gögn inniheldur upprunalega sölupöntun átaki, síðari eftirfylgni og frekari sölu.

<a name="marketing"></a>Kynning
---------

Þú notar markaðsherferð og starfsemi til að finna og byggja upp sambönd við mögulega viðskiptavini, þannig að fyrstu samskipti geta þróast í sölusambönd. Eftirfarandi flæði sýnir viðskiptaferli sölu- og markaðsstarfs. [![Viðskiptaferli fyrir markaðssetningu](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Vensl

Í sölu og markaðssetningu, fyrstu samskipti sem þú hefur við mögulega viðskiptavini geta komið í ýmsum aðstæðum. Til dæmis, þú gætir finna tilvonandi viðskiptavini meðan þú ert að mæta á viðskiptasýningu, eða þú gætir hafa mögulega verið með gott forskot eftir póstlistaherferð fyrirtækis þíns. Það er mjög mikilvægt að skilja flæði einingar aðila áður en sá aðili verður viðskiptavinur. Eftirfarandi mynd sýnir á flæði í samböndum aðila þegar hugsanlegur viðskiptavinur verður raunverulegur viðskiptavinur. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Herferðir

Herferð miðar á tengiliði fyrir góðar horfur, leiðir, tækifæri og viðskiptavini sem hafa verið valdir til að taka þátt í herferðinni. Í Microsoft Dynamics 365 for Finance and Operations er hægt að stofna margar gerðir herferða, eins og símsölu, póstsendingar og tölvupóstherferðir, til að hámarka mögulega viðskiptavini. Sem herferðin líður og þú færð jákvæð viðbrögð, getur þú byrjað á söluferli með þeim viðtakenda sem hafa brugðist jákvætt við herferð.

## <a name="sales"></a>Sala
Söluvirknin er notuð til að stofna tilboð, söluviðauka og krosssölu til nýja og fyrirliggjandi viðskiptavinum, stofna sölupantanir og stofna sölureikninga  fyrir viðskiptavina. Eftirfarandi flæði sýnir viðskiptaferli sölu. [![Viðskiptaferli fyrir sölu](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Sölutilboð

Þú stofnar sölutilboð til að birta viðskiptavinum tilboð á vörum eða þjónustu sem þú munt veita. Viðskiptavinur gæti beðið um tilboð eða þú gætir stofnað tilboð til að svara beiðni frá mögulegum eða núverandi viðskiptavini. Þegar viðskiptavinur samþykkir sölutilboð, er hægt að breyta því í sölupöntun.

### <a name="up-sellcross-sell"></a>Söluaukandi vörur og krosssölur

söluviðauki og krosssölu eru tækni til að selja afurðir þegar pöntun er færð inn fyrir viðskiptavin. Í söluviðauki, er er stungið upp á annarrar afurðar í staðinn fyrir núverandi vöru. Í krosssölu, er stungið upp á annarrar afurðar til viðbótar við núverandi vöru. Þegar þú setur upp afurðalista er Hægt að stofna reglur til að tilgreina hvenær skal leggja til vöru sem krosssölu- eða söluviðaukaafurð.

### <a name="sales-orders"></a>Sölupantanir

Þegar þú stofnar núja sölupöntun, verður þú að velja tegund sölupöntunar til að stofna. Þú hefur fimm valkosti. **Athugasemd:** Eftir að þú stofna sölupöntun, getur verið hvaða gerð pöntunar verið breytt, að undanskildu **Vöruþarfir** gerð ef sölupöntunin er með stöðuna **Afhent**.

| Gerð sölupöntunar  | Lýsing                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Færslubók           | Notið þessa gerð sem uppkast fyrir sölupöntun. Þessi gerð hefur engin áhrif á lagermagn og býr ekki til vörufærslur.                                                                                                                                                                    |
| Áskrift      | Notið þessa gerð fyrir endurteknar pantanir. Þegar pöntunin er reikningsfærð er pöntunarstaðan sjálfkrafa stillt á opin pöntun. afhent Magn sem var reikningsfært og eftirstandandi afhendingar eru uppfærðar. Ekki er hægt að nota þessa gerð sölupöntunarinnar ef verið er að nota virkni vöruhúsakerfis. |
| Sölupöntun       | Notið þessa gerð þegar viðskiptavinur hefur gert eða staðfest pöntun.                                                                                                                                                                                                                                        |
| Skilapöntun    | Notið þessa gerð þegar viðskiptavinur skilar vöru. Skilavörunúmer (RMA-númer) er úthlutað sjálfkrafa.                                                                                                                                                                                            |
| Vöruþörf | Þessi gerð Stofnast sjálfkrafa þegar gerð er vörusala í gegnum Verk.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Sölusamningar

Sölusamning er samningur sem bindur viðskiptavin til að kaupa vöru í ákveðnu magni eða ákveðna upphæð yfir tíma í skiptum fyrir for sérstakt verð og afslætti. Verð og afslættir af sölusamnings hunsa verð og afslætti sem eru tilgreindar í hvaða viðskiptasamninga sem ríkir. Sölusamning gildir fyrir skilgreint tímabil. Umbeðna sendingardagsetningu sem tilgreind er fyrir sölu á **sölupöntun** síðu ætti að vera í gildistíma. Að sjálfgefnu er sölusamning í bið. Einungis er hægt að panta úr sölusamningi þegar hann er stilltur á **virkt**.

### <a name="backorders"></a>Biðpantanir

Þegar pantanir eru færðar inn eða staðfestar þarf hugsanlega að sjá um biðpantanir og undantekningar áður en hægt er að ljúka sölunni. Biðpantanir eru annað hvort innkaupapantanir sem hafa ekki enn verið afhentar frá lánardrottni eða sölupöntunum sem hafa ekki enn verið afhentar til viðskiptavinar. Það er mikilvægt að fylgja biðpöntunum eftir. Til dæmis, ef vörum seinkar frá lánardrottni, gæti þurft að breyta afhendingardagsetningu til viðskiptavinar og láta viðskiptavinin vita af seinkuninni. Hægt er að skoða biðpantanir eftir vöru, viðskiptavinar eða lánardrottins.

#### <a name="viewing-backorders-by-item"></a>Skoða biðpantanir eftir vörum

Með því að skoða biðpantanir eftir vörum, er hægt að fylgja eftir áætluðu framtíðarflæði færslna fyrir tiltekinni vöru. Til dæmis, Hægt er að athuga eftirfarandi upplýsingar:

-   Fjölda innlagðra sölupantana á vöru.
-   Hvort afhending varnings frá lánardrottinn er enn óafgreidd.
-   Hvort panta eigi fleiri vörur til að geta staðið við afhendingar á öllum sölupöntunum á tilætluðum tíma.

Með því að gera þessa athugun, getur þú brugðist við beiðnir frá viðskiptavini um tímasetningu afhendingartíma vöru. Þar að auki, er hægt að forgangsraða sölubiðpöntunum og skipta vörum á lager á milli pantana.

#### <a name="viewing-backorders-by-customer"></a>Skoða Biðpantanir eftir viðskiptavinum

Þegar þú skoðar biðpantana eftir viðskiptavinum gerir kleift að skoða stöðuna á eftirstöðvum pantana viðskiptavinarins. Þessa athugun er gagnleg þegar þarf að svara viðskiptavinum sem eru að bíða eftir vörur sem hafa verið seinkað.

#### <a name="viewing-backorders-by-vendor"></a>Skoða biðpantanir eftir lánardrottni

Þegar þú skoðar biðpantana eftir lánardrottnum, er hægt að fylgja eftir óafgreiddar pantanir og áætluðum afhendingardagsetningum. Þessi athugun er einnig hentugt til forgangsröðunar biðpanana þegar varningur kemur frá lánardrottni og taka þarf til sölupantanir til afhendingar.

### <a name="invoices"></a>Reikningar

Hægt er að stofna þrjár gerðir af reikningum í söluferli:

-   Reikningur viðskiptavinar
-   Textareikningur
-   Bráðabirgðareikningur

#### <a name="customer-invoice"></a>Reikningur viðskiptavinar

Reikningur viðskiptavinar er seðill sem fyrirtæki gefur viðskiptavini í tengslum við sölu. Þú Stofna þessa gerð reiknings viðskiptavinar byggt á sölupöntun sem inniheldur haus og ein eða fleiri línur fyrir vörur eða þjónustu. Reikningur viðskiptamanns lýkur við sölupöntun, fylgiseðil og sölureikningsferli.  

Hægt er að bóka og prenta reikningur viðskiptavinar fyrir einn viðskiptavin, byggt á annaðhvort sölupöntun eða fylgiseðill og dagsetningu. Þú getur einnig Bóka og prenta marga reikninga viðskiptamanna saman, byggða á fylgiseðlum og dagsetningum Þegar reikningur viðskiptavinar fyrir einn viðskiptavin er bókaður eftir sölupöntun, er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu reikningsfærðs magns úr valinni sölupöntun.  

Ef bæði magnið **Reikningsafgangur** og **Afhendingarafgangur** fyrir allar vörur á sölupöntuninni jafngildir núlli (0), breytist staða sölupöntunarinnar í **Reikningsfært**. Ef magnið  í hvorugum reit jafngildir ekki núlli er staða sölupöntunarinnar óbreytt og hægt að færa inn viðbótarreikninga. Ef ætlunin er að bóka og prenta einn eða fleiri reikninga viðskiptavinar byggður á fylgiseðla, verður hafa þegar bókað einn fylgiseðill í það minnsta fyrir hverja sölupöntun. Reikningur viðskiptamanns er byggður á viðkomandi fylgiseðlum og endurspeglar magnið eru skráð.  

Hægt er að stofna reikningur viðskiptavinar út frá línuvörum fylgiseðils sem sendar hafa verið fram að þessu, jafnvel þótt allar vörur tiltekinnar sölupöntunar hafi ekki verið sendar ennþá. Þetta gæti til dæmis átt við, ef fyrirtækið gefur út einn reikning fyrir viðskiptavin mánaðarlega sem nær yfir allar afhendingar sem sendar eru þann mánuð. Hver fylgiseðill stendur fyrir hlutaafhendingu eða fulla afhendingu á vörum í sölupöntuninni.  

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu afhents magns úr völdum fylgiseðlum. Ef magnið **Reikningsafgangur** og **Afhendingarafgangur** fyrir allar vörur á sölupöntuninni jafngildir núlli (0), breytist staða sölupöntunarinnar í **Reikningsfært**. Ef magnið jafngildir ekki núlli er staða sölupöntunarinnar óbreytt og hægt að færa inn viðbótarreikninga. Birgðafærslur eru uppfærðar með reikningsnúmeri og staða á línu í sölupöntuninni breytist í **Reikningsfært**.

#### <a name="free-text-invoice"></a>Textareikningur

Reikningur með frjálsum texta er reikningur sem er ekki tengd sölupöntun. Hann inniheldur pöntunarlínur sem fela í sér fjárhagslykla, frjálsar textalýsingar, og söluupphæð. Ekki er hægt að færa inn vörunúmer á þessa gerð reiknings og skylda er að færa inn viðeigandi VSK-upplýsingar. Aðallykill fyrir söluna tilgreindur á hverri reikningslínu. staða viðskiptavinarins er bókuð í safnlykil úr bókunarregla sem notuð er fyrir reikningur með frjálsum texta.

#### <a name="pro-forma-invoice"></a>Bráðabirgðareikningur

Bráðabirgðareikningur  er reikningur sem er útbúinn sem mat á raunverulegu reikningsupphæðinni áður en reikningurinn er bókaður. Hægt er að prenta út bráðabirgðareikning fyrir annað hvort reikningur viðskiptavinar eða reikningur með frjálsum texta.




