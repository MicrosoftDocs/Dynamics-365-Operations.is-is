---
title: Yfir/undir færslur
description: Í þessari grein er að finna upplýsingar sem hjálpa til við að setja upp upplýsingar um reglur fyrir yfir-/undirfærslur þannig að kerfið geti ákvarðað hvernig á að stjórna yfirvinnslu og undirvinnslu á vörum við móttöku.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 79ce18a462f9c2f93dceec82da7ee0209ab61f78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844998"
---
# <a name="overunder-transactions"></a>Yfir/undir færslur

[!include [banner](../../includes/banner.md)]

Þegar unnið er úr pöntunum í ferð býst kerfið við því að vörumagnið sem er móttekið í vöruhúsi á lokaáfangastað til notkunar samsvari því magni sem tilgreint er í innkaupapöntunarlínunum sem tengjast ferðinni. En þar sem nákvæmt magn í innkaupapöntunarlínunum er ekki alltaf móttekið í vöruhúsinu, skilgreinir einingin **Heildarkostnaður** safn af reglum sem eru notaðar til að meðhöndla yfirmóttöku og undirmóttöku á vörum. Þessar reglur eru sérstaklega mikilvægar vegna þess að upprunalega innkaupapöntunin hefur verið reikningsfærð og ekki er lengur hægt að breyta henni. Með því að setja upp upplýsingar um reglur yfir-/undirfærslu er kerfinu gert kleift að ákvarða hvernig á að stjórna yfirvinnslu og undirvinnslu á vörum við móttöku. Einnig er hægt að stjórna yfir- og undirbirgðum handvirkt með því að nota **Yfir/undirfærslur**.

## <a name="overunder-tolerances"></a>Yfir/undir vikmörk

Yfirvikmörk og undirvikmörk eru stillt til að tilgreina yfir- og undirmagn eða rúmmál sem hægt er að vinna úr í ferð án þess að villa komi upp. Ef móttaka ferðalínu er utan þessara vikmarka þarf að breyta þeim og leysa málið áður en hægt verður að loka ferðalínunni og halda áfram með afgreiðsluna.

Til að skilgreina vikmörk skal fara í **Heildarkostnaður \> Uppsetning yfir/undir \> Yfir/undir vikmörk**. Þar er hægt að skoða, breyta, bæta við og fjarlægja vikmarkafærslur. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Kóði lykils | <p>Skilgreinið umfang lánardrottna sem vikmörkin eiga við um með því að velja eitt af eftirfarandi gildum:</p><ul><li>**Tafla** – Yfir-/undirvikmörkin eiga aðeins við um lánardrottin sem valinn er fyrir línuna.</li><li>**Flokkur** – yfir/undirvikmörkin eiga við um alla lánardrottna í vikmarkaflokki sem er valinn fyrir línuna.</li><li>**Allt** – yfir-/undirvikmörkin eiga við um alla lánardrottna.</li></ul> |
| Lyklavensl | Veljið lánardrottin eða lánardrottnaflokk sem yfir-/undirvikmörkin eiga við um eftir því hvaða gildi er valið í reitnum **Kóði lykils**. |
| Vörukóði | <p>Skilgreinið umfang vara sem vikmörkin eiga við um með því að velja eitt af eftirfarandi gildum:</p><ul><li>**Tafla** – Yfir-/undirvikmörkin eiga aðeins við um vöruna sem valin er fyrir línuna.</li><li>**Flokkur** – yfir/undirvikmörkin eiga við um allar vörur í vikmarkaflokki sem er valinn fyrir línuna.</li><li>**Allt** – yfir-/undirvikmörkin eiga við um allar vörur.</li></ul> |
| Vöruvensl | Veljið vöru eða vöruflokk sem yfir-/undirvikmörkin eiga við um eftir því hvaða gildi er valið í reitnum **Vörukóði**. |
| Vikmörk upphæðar | Færið inn vikmörk upphæðar sem á að nota í heilli innkaupapöntun. |
| Prósenta vikmarka | Færið inn prósentuvikmörk sem á að nota fyrir einstakar innkaupapöntunarlínur. |

## <a name="overunder-reasons"></a>Yfir/undir ástæður

Þegar yfir- eða undirmagn tengist línu ferðar sem er móttekin gæti þurft að gefa upp ástæðu fyrir yfir- eða undirmagninu. Í þessu tilviki er hægt að velja ástæðu yfirafhendingar eða undirafhendingar í móttökulínunni þegar vörurnar eru mótteknar.

Til að setja upp ástæður yfir- og undirafhendingar skal fara í **Heildarkostnaður \> Uppsetning yfir/undir \> Ástæður yfir/undir**. Þar er hægt að skoða, breyta, bæta við og fjarlægja tiltækar ástæður yfirafhendingar og undirafhendingar. Eftirfarandi tafla lýsir eritinum sem eru tiltæk fyrir hverja ástæðu.

| Svæði | lýsing |
|---|---|
| Yfir/undir ástæða | Færið inn einkvæmt heiti fyrir ástæðu fyrir færslu yfirafhendingar eða undirafhendingar. |
| lýsing | Færið inn lýsingu á ástæðu yfir/undir. |
| Hreyfing | Veljið hreyfingabókina sem tengist ástæðu yfir/undir. Þetta svæði birtir lista yfir allar tiltækar færslubækur sem færslubókargerðin *Hreyfing* tengist á síðunni **Heiti birgðabóka** (**Uppsetning birgðastjórnunar \> Færslubókarheiti \> Birgðir**). |

## <a name="item-overunder-tolerance-groups"></a>Yfir/undir vikmarkaflokkar vöru

Vörur með svipuð vikmörk er hægt að flokka saman. Á þennan hátt er hægt að stilla yfir-/undirvikmörk samtímis fyrir allar vörur í þeim flokki.

Til að setja upp yfir-/undirvikmarkaflokka skal fara í **Heildarkostnaður \> Uppsetning yfir/undir \> Yfir/undir vikmarkaflokkar vöru**. Þar er hægt að skoða, breyta, bæta við og fjarlægja yfir/undir færslur vikmarkahóps. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Yfir/undir vikmarkaflokkur | Færið inn einkvæmt heiti fyrir flokkinn. Veljið heiti sem lýsir vikmörkum, t.d. *1% frá*. |
| lýsing | Færa inn lýsingu á flokknum. |

## <a name="vendor-overunder-tolerance-groups"></a>Yfir/undir vikmarkaflokkar lánardrottins

Hægt er að flokka saman lánardrottna sem afhenda yfir eða undir með reglulegu millibili. Síðan er hægt að stilla yfir-/undirvikmörk fyrir hvern flokk.

Til að setja upp yfir-/undirvikmarkaflokka lánardrottins skal fara í **Heildarkostnaður \> Uppsetning yfir/undir \> Yfir/undir vikmarkaflokkar lánardrottins**. Þar er hægt að skoða, breyta, bæta við og fjarlægja yfir/undir færslur vikmarkahóps. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Yfir/undirhópar | Færið inn einkvæmt heiti fyrir flokkinn. Velja skal heiti sem lýsir gerð lánardrottna sem tilheyra flokknum. |
| lýsing | Færa inn lýsingu á flokknum. |

## <a name="view-and-process-overunder-transactions"></a>Skoða og vinna úr yfir-/undirfærslum

Yfir- og undirfærslur eru myndaðar þegar vörumagnið sem gengið er frá samsvarar ekki upphaflegu magni. Magn í komubók ætti aðeins að uppfæra með magninu sem gengið er frá.

Þegar búið er að vinna úr móttöku ferðalína er hægt að stilla yfir-/undirvikmörk fyrir lánardrottin. Vörurnar verða síðan yfirfarnar og staðfestar. Hægt er að stilla vikmörkin sem prósentu, staðbundna upphæð eða bæði.

Ef vara sem er móttekin er innan vikmarka mun kerfið búa til hreyfingabók. Hægt er að tilgreina þessa færslubók á færibreytusíðu ferðarinnar. Að auki verður stofnuð yfir-/undirfærsla. Til dæmis er virði pöntunar $100, virði móttöku er $99 og þessi gildi uppfylla reglur vikmarka. Í þessu tilfelli verður neikvæð birgðabók stofnuð fyrir undirafgreitt magn.

Ef vara sem er móttekin er utan vikmarka mun kerfið stofna yfir-/undirfærslu fyrir mismuninn á magninu.

Til að skoða og vinna úr yfir-/undirfærslum skal fara í **Heildarkostnaður \> Fyrirspurnir \> Yfir/undirfærslur**. Þar verður yfir-/undirfærsla tengd við allar vörurnar í ferð sem eru yfirmótteknar eða undirmótteknar. Mælt er með því að nota síðuna **Yfir/undirfærslur** til að leysa úr öllum yfir-/undirfærslum sem tengjast ferðum. Einnig er mælt með því að nota **ekki** hreyfinga- eða talningarbók til að leysa handvirkt úr vöruhúsafærslum undirafhendingar. Þess í stað ætti að nota síðuna **Yfir/undirfærslur** til að stjórna magni undirafhendingar í vöruhúsi.

### <a name="upper-overview-tab"></a>Efri yfirlitsflipinn

Til að skoða yfir-/undirfærslurnar skal velja flipann **Yfirlit** í efri hluta síðunnar **Yfir/undirfærslur**. Eftirfarandi tafla lýsir reitum sem eru tiltækir í töflunni.

| Svæði | lýsing |
|---|---|
| Yfir/undir færslunúmer | Einkvæmt heiti á skrá yfir-/undirfærslu sem var sjálfkrafa búin til þegar unnið var úr birgðabókinni. |
| Ferð | Ferð sem innkaupalínan var tengd við. |
| Gámur | Gámurinn sem innkaupalínan var tengd við. |
| Komubók | Komubókin sem yfir-/undirlínan var mynduð úr. |
| Tilvísun | Tilvísun í annaðhvort innkaupapöntun eða flutningspöntun sem tengist yfir-/undirfærslunni. |
| Númer | Innkaupapöntunin sem vísað er til í yfir-/undirfærslunni. |
| Lykill lánardrottins | Lánardrottinn sem yfir eða undir tengist. |
| Númer á vörum í flutningi | Númer á vörum í flutningi ef það á við. |
| Vörunúmer | Vörunúmerið sem yfir eða undir tengist. |
| Upphaflegt magn | Upprunalegt magn innkaupapöntunarlínu sem er tengd við sendinguna. |
| Móttekið magn | Magnið sem var raunverulega móttekið. |
| Mismunur | Mismunurinn á væntanlegri upphæð komubókar og upphæðar sem var bókuð í komubókina. Neikvætt gildi gefur til kynna yfirafhendingu á vörum. |
| Eftirstandandi magn | Magnið sem er eftir í komubókarlínunni. |
| Of-/vanafhending | Gildi sem segir til um hvort magnið sem var móttekið er yfir eða undir. |
| Staða | Staða yfir-/undirfærslunnar. Það fer eftir stillingunum á síðunni **[Færibreytur heildarkostnaðar](landed-cost-parameters.md)** hvort yfirafhending geti sjálfkrafa stofnað hreyfingabók fyrir upphæð yfirafhendingar og bókað færslubókina. Í þessu tilfelli fær yfir-/undirfærslan stöðuna *Lokið*. Ef krafist er aðgerðar til að færa vörurnar úr vöruhúsi undirafhendingar fær skráin stöðuna *Í vinnslu*. |
| Yfir/undir ástæða | Ástæðan sem tengist yfir-/undirfærslunni. |
| Aðrar birgðavíddir | Hægt er að sýna dálka fyrir fleiri víddir í hnitanetinu eftir þörfum. Þessar víddir fela í sér rununúmer, birgðastöðu og vöruhús. Á aðgerðasvæðinu skal velja **Birgðir \> Sýna víddir** til að opna svarglugga þar sem hægt er að velja víddirnar sem á að hafa með. |

### <a name="upper-general-tab"></a>Efri almenni flipinn

Til að skoða frekari upplýsingar um línuna sem er valin í efri flipanum **Yfirlit** skal velja flipann **Almennt** í efri hluta síðunnar **Yfir/undirfærslur**. Upplýsingarnar á þessum flipa innihalda gildin fyrir allar tiltækar víddir. Þessar upplýsingar eru fengnar úr upprunalegri innkaupapöntun.

### <a name="lower-overview-tab"></a>Neðri yfirlitsflipinn

Til að skoða skjalagerðina fyrir línuna sem er valin í efri flipanum **Yfirlit** skal velja flipann **Yfirlit** í neðri flipa síðunnar **Yfir/undirfærslur**. Eftirfarandi tafla lýsir svæðum sem eru tiltæk.

| Svæði | lýsing |
|---|---|
| Ný gerð skjals | Þessi reitur er stilltur á annaðhvort *Hreyfingabók* eða *Innkaupapöntun* eftir því hvaða aðgerð er sýnd í valinni línu yfir-/undirfærslu. |
| Númer | Tilvísun og tengill á annaðhvort innkaupapöntunina eða hreyfingabókina sem tengist valinni línu yfir-/undirfærslu. |
| Yfir/undir ástæða | Ástæðan sem tengist valinni línu yfir-/undirfærslu. |
| Magn | Magnið sem er valið fyrir innkaupapöntunina eða hreyfingabókina sem tengist valinni línu yfir-/undirfærslu. |

### <a name="lower-general-tab"></a>Neðri almenni flipinn

Til að skoða númer yfir-/undirfærslu, lotukenni og númer víddar sem tengjast valdri línu yfir-/undirfærslu skal velja flipann **Almennt** í neðri hluta síðunnar **Yfir/undirfærslur**. 

### <a name="process-overunder-transactions"></a>Meðhöndla yfir-/undirfærslur

Aðgerðasvæðið á síðunni **Yfir/undirfærslur** býður upp á eftirfarandi skipanir fyrir úrvinnslu á færslum sem valdar eru á síðunni. Hver skipun gerir kleift að velja hvernig á að vinna úr hverri færslu.

- **Stofna \> Hreyfing** – Stofnið og bókið hreyfingabók fyrir valda færslu. Fyrir undirfærslur er hreyfingabók sjálfkrafa stofnuð og bókuð fyrir mismuninum á væntanlegu og raunverulegu magni sem er móttekið. Veljið þessa skipun fyrir yfirfærslur ef ætlunin er að lánardrottinn taki til greina mismun í kostnaði.
- **Stofna \> Innkaupapöntun** – Stofnið innkaupapöntun fyrir mismuninum á væntanlegu og raunverulegu magni sem er móttekið fyrir valda færslu. Veljið þessa skipun fyrir yfirfærslur ef fyrirtækið mun taka til greina mismun í kostnaði.
- **Stofna \> Flytja á áfangastað** – Þessi skipun á aðeins við um flutningspantanir. Veljið hana ef á að flytja yfir- eða undirmagnið í vöruhús áfangastaðar.
- **Stofna \> Flytja á upprunastað** -Þessi skipun á aðeins við um flutningspantanir. Veljið hana ef á að flytja yfir- eða undirmagn í upprunalegt vöruhús.
