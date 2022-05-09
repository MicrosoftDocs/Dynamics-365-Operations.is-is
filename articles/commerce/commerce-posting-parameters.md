---
title: Færibreytur viðskiptafærslu
description: Þetta efnisatriði lýsir færibreytum sem eru sértækar fyrir bókun fjárhags- og efnisfærslna í Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649179"
---
# <a name="commerce-posting-parameters"></a>Færibreytur viðskiptafærslu

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir færibreytum sem eru sértækar fyrir bókun fjárhags- og efnisfærslna í Microsoft Dynamics 365 Commerce. Viðskiptabirtingarfæribreytur eru staðsettar í höfuðstöðvum Commerce kl **Verslun og verslun \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskiptabreytur \> Birting**.

## <a name="periodic-discount-parameters"></a>Reglubundnar afsláttarfæribreytur

Eftirfarandi tafla sýnir færibreytur reglubundinna afsláttar sem eru sértækar fyrir bókun fjárhags- og efnisfærslna.

| Færibreyta | Lýsing |
|-----------|-------------|
| Bóka tímabundinn afslátt | Þessi valkostur stjórnar hvort reglubundin tilboð séu bókuð á fjárhagslykla. Blönduð tilboð, magnafslættir og afsláttartilboð eru tímabundnir afslættir. Þegar þessi færibreyta er virkjuð er hægt að stilla fleiri reiti í **Reglubundin afsláttur** kafla. |
| Gerð fjárhagslykils | <p>Veldu tegund reiknings sem er notaður til að bóka reglulega afslætti:</p><ul><li>**Standard** – Kerfið notar ekki afsláttartengda reiti á þessari síðu. Þess í stað notar það reikningana sem eru skilgreindir á **Birting** síða í höfuðstöðvum viðskipta (**Vörustjórnun \> Uppsetning \> Birting \> Birtingareyðublöð**).</li><li>**Reglubundið** – Kerfið notar Commerce afsláttarreikninga sem tilgreindir eru af afsláttartengdu reitunum á þessari síðu. Ef þú velur þennan valkost verður þú að tilgreina fjárhagsreikning (GL) fyrir hverja tegund tilboðs (afsláttur, blanda saman, magn og þröskuldur). Þegar þú setur upp hvern afslátt geturðu skilgreint reikning. Þegar bókunareiginleikinn afsláttarreikningur er notaður á afsláttaruppsetningarsíðunni er viðbótardebetfærsla og kreditfærsla gerð til að endurflokka afsláttarbókunina frá Commerce afsláttarreikningnum yfir í afsláttarreikninginn. Fyrir frekari upplýsingar, sjá [Smásöluafsláttur](retail-discounts-overview.md).</li></ul> |
| Póstupplýsingakóði afsláttur | Þessi valkostur er ekki lengur notaður í stöðluðu viðskiptalausninni og verður úreltur. |
| Bóka tímabundinn afslátt fyrir pantanir | Þessi valkostur stjórnar hvort reglubundinn smásöluafsláttur sé bókaður í fjárhagsbókina fyrir pantanir viðskiptavinar og símaver. |

## <a name="inventory-update-parameters"></a>Færibreytur birgðauppfærslu

Eftirfarandi tafla sýnir færibreytur birgðauppfærslu sem eru sértækar fyrir bókun fjárhags- og efnisfærslna.

| Færibreyta | Lýsing |
|-----------|-------------|
| Notaðu sjálfgefið lotuauðkenni þegar lotunúmer finnast ekki | Þessi valkostur stjórnar hvort sjálfgefið runuauðkenni sé notað fyrir lotuvirkar vörur ef lotunúmer finnast ekki og neikvæðar birgðir eru leyfðar. |
| Sjálfgefið lotuauðkenni | Lotunúmerið sem á að nota ef lotunúmer fyrir vörur finnast ekki og **Notaðu sjálfgefið lotuauðkenni þegar lotunúmer finnast ekki** færibreytan er virkjuð. |

## <a name="aggregation-parameters"></a>Söfnunarfæribreytur

Eftirfarandi tafla sýnir uppsafnaðarfæribreytur sem eru sértækar fyrir bókun fjárhags- og efnisfærslna.

| Færibreyta | Lýsing |
|-----------|-------------|
| Peningaflutningur í öryggisskáp | Virkjaðu þessa færibreytu til að safna saman öllum færslum við bókun yfirlits og búa til eina línu í færslubókinni til að bóka í stað sérstakrar línu fyrir hverja niðurfellingu. |
| Peningaflutningur í banka | Virkjaðu þessa færibreytu til að safna saman öllum færslum við bókun yfirlits og búa til eina línu í færslubókinni til að bóka í stað sérstakrar línu fyrir hverja niðurfellingu. |
| Sölufærslur | Virkjaðu þessa færibreytu til að sameina færslurnar sem hluta af bókunarferli færsluyfirlits. Við mælum með að þú virkir þessa færibreytu. Það var áður nefnt **Viðskipti með skírteini**. |
| Ekki safna upp skilum | Ef þessi valkostur er valinn verður hver skilafærsla bókuð sem sérstök sölupöntun þegar smásöluyfirlit er bókað. |

## <a name="batch-processing-parameters"></a>Lotuvinnslubreytur

Eftirfarandi tafla sýnir runuvinnslufæribreytur sem eru sértækar fyrir bókun fjárhags- og efnisfærslna.

| Færibreyta | Lýsing |
|-----------|-------------|
| Hámarksfjöldi samhliða fullyrðinga | Þessi reitur skilgreinir fjölda runuverkefna sem eru notuð til að bóka margar yfirlýsingar. |
| Hámarksfjöldi þráða fyrir úrvinnslu pöntunar á hvert yfirlit | Þessi reitur táknar hámarksfjölda þráða sem runuvinna yfirlitsbókunar notar til að stofna og reikningsfæra sölupantanir fyrir eitt yfirlit. Heildarfjöldi þráða sem færsluferlið yfirlýsingar notar er reiknað með því að margfalda gildi þessarar færibreytu með gildinu **Hámarksfjöldi samhliða yfirlýsingabirtinga** breytu. Ef gildi þessarar færibreytu er of hátt getur það haft neikvæð áhrif á frammistöðu bókunarferlis yfirlits. |
| Hámarksfjöldi færslulína í uppsöfnun | Þessi reitur skilgreinir fjölda færslulína sem eru innifalin í einni uppsöfnuðum færslu áður en ný færsla er stofnuð. Safnaðar færslur eru búnar til á grundvelli mismunandi söfnunarviðmiða, eins og viðskiptavinur, viðskiptadagsetning eða fjárhagsvíddir. Athugaðu að línum úr einni færslu verður ekki skipt yfir mismunandi uppsafnaðar færslur. Því gæti fjöldi lína í samantekinni færslu verið aðeins hærri eða lægri, byggt á þáttum eins og fjölda aðskildra vara. |
| Hámarksfjöldi þráða til að villuleita í færslum verslunar | Þessi reitur skilgreinir hámarksfjölda þráða sem eru notaðir til að staðfesta færslur. Staðfesting viðskipta er nauðsynlegt skref sem verður að eiga sér stað áður en hægt er að draga viðskiptin inn í yfirlitin. Þú verður einnig að skilgreina gjafakortsvöru á **Gjafakort** Flýtiflipi á **Birting** flipi á **Viðskiptabreytur** síðu, jafnvel þótt samtökin noti ekki gjafakort. |

Eftirfarandi tafla sýnir ráðlögð gildi fyrir færibreyturnar í töflunni á undan. Þessi gildi ættu að vera prófuð og sníða að uppsetningu dreifingar og tiltækra innviða. Gildi sem fara yfir ráðlögð gildi geta haft slæm áhrif á aðra lotuvinnslu og ætti að staðfesta það.

| Færibreyta | Ráðlagt gildi | Upplýsingar |
|-----------|-------------------|---------|
| Hámarksfjöldi samhliða yfirlitsbókana | <p>Stilltu þessa færibreytu á fjölda runuverkefna sem eru tiltæk fyrir runuhópinn sem keyrir **Yfirlýsing** starf.</p><p>**Almenn regla:** Margfaldaðu fjölda sýndarþjóna (AOS) með fjölda lotuverkefna sem eru í boði á hvern AOS sýndarþjón.</p> | Þessi færibreyta á ekki við þegar **Smásöluyfirlit - Trickle feed** eiginleiki er virkur. |
| Hámarksfjöldi þráða fyrir úrvinnslu pöntunar á hvert yfirlit | Byrjaðu að prófa gildi kl **4**. Venjulega ætti gildið ekki að fara yfir **8**. | Þessi færibreyta skilgreinir fjölda þráða sem eru notaðir til að stofna og bóka sölupantanir. Það táknar fjölda þráða sem eru tiltækir til birtingar á hverja yfirlýsingu. |
| Hámarksfjöldi færslulína í uppsöfnun | Byrjaðu að prófa gildi kl **1000**. Það fer eftir uppsetningu Commerce höfuðstöðva, smærri pantanir gætu verið hagstæðari fyrir frammistöðu. | Þessi færibreyta skilgreinir fjölda lína sem eru innifalin í hverri sölupöntun við bókun yfirlits. Eftir að þessum fjölda er náð verður línum skipt í nýja röð. Fjöldi sölulína mun ekki nákvæmlega jafngilda fjöldanum sem þú tilgreinir, vegna þess að skiptingin á sér stað á sölupöntunarstigi. Engu að síður mun talan vera nálægt þeirri tölu sem er stillt. Þessi færibreyta er notuð til að búa til sölupantanir fyrir smásölufærslur sem eru ekki með nafngreindan viðskiptavin. |
| Hámarksfjöldi þráða til að villuleita í færslum verslunar | Við mælum með að þú stillir þessa færibreytu á **4**, og að þú auki það aðeins ef þú nærð ekki viðunandi árangri. Fjöldi þráða sem þetta ferli notar má ekki fara yfir fjölda örgjörva sem eru tiltækir fyrir hópþjóninn. Ef fjöldi þráða er of mikill gæti önnur lotuvinnsla haft áhrif. | Þessi færibreyta stjórnar fjölda færslna sem hægt er að staðfesta á sama tíma fyrir tiltekna verslun. |

> [!NOTE]
> Allar stillingar og færibreytur sem tengjast bókun uppgjörs og sem eru skilgreindar í verslunum og á síðunni **Færibreytur Commerce** eiga við í endurbættum eiginleika fyrir bókun uppgjörs.

## <a name="invoice-parameters"></a>Reikningsfæribreytur

Eftirfarandi tafla sýnir reikningsfæribreytur sem eru sértækar fyrir bókun fjárhags- og efnisfærslna.

| Færibreyta | Lýsing |
|-----------|-------------|
| Heiti færslubókar | Heiti greiðslubókar sem er notað þegar greiðslubækur viðskiptavina fyrir sölupöntunargreiðslur eru stofnaðar. Þessi stilling á við um allar pöntunargreiðslur sem eru bókaðar fyrir sölustað (POS), símaver og pantanir fyrir rafræn viðskipti. |
| Heiti lykils | Heiti greiðslureiknings. |
| Forgangsraða víddum frá greiðslumáta | Þegar þetta flagg er virkt forgangsraða greiðslubækur víddum frá greiðslumáta í stað vídda úr verslun. |
| Hegðun skattaútreiknings | Þessi færibreyta tilgreinir hegðun þegar sölupantanir sem eru búnar til við bókun yfirlits eru reikningsfærðar:<ul><li>**Endurreikna** – Reiknaðu skatta aftur.</li><li> **Ekki endurreikna** – Notaðu skattupphæðirnar sem eru reiknaðar í POS.</li></ul> |
| Heiti færslubókar | Heiti færslubókar sem er notað þegar greiðslubók viðskiptavinar fyrir endurgreiðslu er stofnuð. Þessi stilling á við um allar pöntunargreiðslur sem eru bókaðar fyrir POS, símaver og rafrænar rásarpantanir. |

## <a name="statement-parameters"></a>Yfirlýsingafæribreytur

Eftirfarandi tafla sýnir yfirlitsfæribreytur sem eru sértækar fyrir bókun fjárhags- og efnisfærslna.

| Færibreyta | Lýsing |
|-----------|-------------|
| Taka frá birgðafærslur við útreikning | Þegar þessi færibreyta er virkjuð, tekur útreikningur yfirlits frá birgðum tímabundið þar til yfirlitið er bókað. Þessi færibreyta er sjálfkrafa óvirk til að bæta árangur útreikninga yfirlits. Hægt er að reikna út uppfærðar birgðaupplýsingar með því að nota **Settu inn birgðahald** lotuvinna. Athugið að **Post** birgðalotuvinna er ekki lengur notuð þegar [driffóður](trickle-feed.md) – Byggð pöntunargerð fyrir viðskipti í smásöluverslun er virkjuð. |
| Gera þarf talningu óvirka | Þessi fáni slekkur á talningu við færslu í höfuðstöðvum Commerce. |
| Endurreikna fjárhagsvíddir við villu | Þegar þessi færibreyta er virkjuð er hægt að endurmeta fjárhagsvíddir á síðari yfirlitsbókunum ef uppgjörsbókun mistekst. |
| Nota fjárhagsvíddir úr skilaverslun | Þegar þessi færibreyta er virkjuð er hægt að stofna tengdar sölupantanir fyrir skila sem nota fjárhagsvíddir verslunarinnar í stað fjárhagsvíddanna frá upphaflegu færslunni. |
| Aftengja skil | Þegar þessi færibreyta er virkjuð getur yfirlýsingin búið til skil á óbókuðum sölu sem blind skil. Þessi færibreyta er sjálfkrafa óvirk og við mælum með að þú haldir henni óvirkri. |
| Slökktu á bókun á námundunarmun | Þessi færibreyta slekkur á bókun á sléttunarmismun á milli færslugreiðslu og brúttóupphæðar við greiðsluvinnslu. |
| Jafna innborganir viðskiptavina sjálfkrafa | Þegar þessi færibreyta er virkjuð eru innstæður viðskiptavinar sem eru bókaðar við bókun smásöluyfirlits jafnaðar á móti opnum færslum viðskiptavinar. |
| Virkjaðu og notaðu afstemmingu peningastjórnunar frá POS | Þegar þessi færibreyta er virkjuð er afstemming sjóðstýringar gerð í POS, og gildin eru send í gegnum smásölubókun fjárhagsyfirlits til að búa til yfirlitslínur. |
| Upplýsingastig fjárhagsskírteinis | Þessi færibreyta skilgreinir smáatriðin sem er innifalin í fjárhagsfylginu fyrir valdar færslur sem koma frá POS. Færslugerðir innihalda tekjur, gjöld og afslætti. Fyrir afslætti er þessi færibreyta aðeins tekin til greina þegar reikningsnúmerið fyrir reglubundinn afslátt og reikningsnúmerið fyrir venjulegan afslátt er ekki það sama. Nema upplýsingar séu nauðsynlegar, **Samantekt** er ráðlagt gildi fyrir þessar færslur. Þegar birting á yfirlitsstigi er skilgreind, **TransactionDiscountTrans.RecID** verður ekki fyllt út. Í útgáfu útgáfu Commerce 10.0.27 var þessi fáni endurnefndur og færður. Það var áður nefnt **Upplýsingar stig** og var í **Birgðauppfærsla** kafla. |
