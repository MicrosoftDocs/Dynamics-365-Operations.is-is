---
title: Yfirlit yfir inn- og útflutningsvinnslu gagna
description: Notaðu vinnusvæðið Gögnastjórnun til að búa til og stjórna Inn- og útflutningsvinnslu gagna.
author: Sunil-Garg
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cb38c812aed60bddadce25f66ec77f4e428be71
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751001"
---
# <a name="data-import-and-export-jobs-overview"></a>Yfirlit yfir inn- og útflutningsvinnslu gagna

[!include [banner](../includes/banner.md)]

Til að búa til og stjórna inn- og útflutningsvinnslu gagna í skaltu nota vinnusvæðið **Gagnastjórnun**. Sjálfgefið er að Inn- og útflutningsferli gagna skapi uppsetningartöflu fyrir hverja einingu í markgagnagrunninum. Millistigsvistunartöflu leyfir þér að staðfesta, hreinsa upp eða breyta gögnum áður en þú færir þau.

> [!NOTE]
> Þetta efni gerir ráð fyrir að þú þekkir [gagnaeiningar](data-entities.md).

## <a name="data-importexport-process"></a>Inn- og útflutningsferli gagna
Hér eru skrefin til að flytja gögn inn eða út.

1. Stofnaðu innflutnings- eða útflutningsverk þar sem eftirfarandi verkefnum þarf að ljúka:

    - Skilgreina verktegund.
    - Greina einingar til að flytja inn eða út.
    - Velja gagnasnið fyrir verkið.
    - Raða einingum þannig að þeir þær verði unnar í rökréttum hópum og skynsamlegri röð.
    - Tilgreinið hvort nota skuli sviðsetningartöflur.

2. Staðfesta að upprunagögn og markgögn séu rétt vörpuð
3. Staðfestu öryggi fyrir innflutnings- eða útflutningsverkið.
4. Bætið við eða fjarlægja svæði fyrir inn- eða útflutningsverkið.
5. Staðfesta að starfið hafi gengið eins og búist var við með því að skoða starfsferilinn.
6. Hreinsa sviðsetningartöflurnar.

Nánari upplýsingar um hvert skref í ferlinu eru í öðrum hlutum þessa efnisatriðis.

> [!NOTE]
> Til þess að geta endurnýjað skjámyndina fyrir innflutning/útflutning gagna svo hægt sé að sjá nýjustu stöðuna skal nota endurnýjunartáknið. Ekki er mælt með endurnýjun á vafrastigi vegna þess að það truflar innflutnings-/útflutningsvinnslur sem eru ekki keyrðar í runum.

## <a name="create-an-import-or-export-job"></a>Stofna inn- eða útflutningsverk
Inn- eða útflutningsverk gagna má keyra einu sinni eða oft.

### <a name="define-the-project-category"></a>Skilgreina verktegund.
Við mælum með að þú takir tíma til að velja viðeigandi verktegund fyrir innflutnings- eða útflutningsverkið. Verktegundir geta hjálpað þér að stjórna skyldum störfum.

### <a name="identify-the-entities-to-import-or-export"></a>Greina einingar til að flytja inn eða út
Þú getur bætt tilteknum einingum við innflutnings- eða útflutningsverk eða valið sniðmát til að nota. Sniðmát fyllir verk með lista yfir einingar. Sniðmátið **Virkja sniðmát** er í boði eftir að þú gefur verki nafn og vistar það.

### <a name="set-the-data-format-for-the-job"></a>Velja gagnasnið fyrir verkið.
Þegar þú velur einingu verður þú að velja snið gagna sem verða flutt út eða inn. Þú skilgreinir snið með því að nota reitinn **Uppsetning uppruna gagna**. Snið upprunagagna er blanda af **Tegund**, **Skráarsniði**, **Línuafmörkun** og **Dálkaafmörkun**. Það eru líka aðrir eiginleikar en þetta eru lykilatriðin til að skilja. Eftirfarandi tafla sýnir gildar samsetningar.

| Skrársnið            | Afmarkari fyrir línu/dálk                       | XML-stíll                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-NA-                     |
| XML                    | \-NA-                                      | XML-eining XML-eigind |
| Afmarkað, föst breidd | Komma, semíkomma, flipi, lóðrétt strik, tvípunktur | \-NA-                     |

### <a name="sequence-the-entities"></a>Einingunum raðað
Einingum má raða í gagnasniði, eða í innflutnings- og útflutningssverkum. Þegar þú keyrir verk sem inniheldur fleiri en eina gagnaeiningu verður þú að ganga úr skugga um að einingunum sé rétt raðað. Einingum er raðað til að geta leyst hugsanleg virknitengsl milli eininga. Ef einingar eru ekki með virknitengsl er hægt að tímastilla þær fyrir samhliða inn- og útflutning.

#### <a name="execution-units-levels-and-sequences"></a>Framkvæmdareiningar, stig og raðir
Framkvæmdareiningin, stig í framkvæmdareiningunni og röð einingar hjálpa til við að stjórna röðinni sem gögnin eru flutt út eða flutt inn í.

- Einingar í mismunandi framkvæmdareiningum eru unnar samhliða.
- Í hverri framkvæmdareiningu eru einingar unnar samhliða ef þeir hafa sama stig.
- Á hverju stigi eru einingar unnar í samræmi við raðnúmer þeirra á því stigi.
- Eftir að eitt stig hefur verið unnið, er næsta stig unnið.

#### <a name="resequencing"></a>Endurröðun
Þú gætir viljað endurraða einingunum þínum í eftirfarandi tilvikum:

- Ef aðeins eitt gagnaverk er notað fyrir allar breytingar þínar geturðu notað endurstillingarvalkosti til að hámarka framkvæmdartíma fyrir allt verkið. Í þessum tilvikum er hægt að nota framkvæmdareininguna til að tákna eininguna, stigið til að tákna eiginleikarasvæðið í einingunni og röðina til að tákna eininguna. Með því að nota þessa aðferð getur þú unnið yfir einingar samhliða, en þú getur samt unnið í röð í einingu. Til að tryggja að samhliða starfsemi nái árangri verður þú að íhuga öll tengsl.
- Ef margar gagnasöfn eru notuð (til dæmis eitt verk fyrir hverja einingu) geturðu notað röðun til að hafa áhrif á stig og röð eininga til að ná sem bestum árangri.
- Ef það er engin tengsl yfirleitt er hægt að raða einingum á mismunandi framkvæmdareiningar til að hámarka hagræðingu.

Valmyndin **Endurröðun** er í boði þegar margar einingar eru valdar. Hægt er að endurraða á grundvelli valkostanna framkvæmdareiningar, stigs eða raðar. Þú getur stillt stighækkun til að endurraða einingum sem voru valdar. Einingin, stigið og / eða raðnúmerið sem er valið fyrir hverja einingu er uppfært með tilgreindri stighækkun.

#### <a name="sorting"></a>Röðun
Hægt er að nota valkostinn **Raða eftir** til að skoða einingalistann í röð.

### <a name="truncating"></a>Stýfing
Fyrir innflutt verk er hægt að velja að stýfa færslur í einingunum fyrir innflutning. Þetta er gagnlegt ef það þarf að flytja færslur inn í autt töflusafn. Þessi stilling er sjálfkrafa óvirk.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Staðfesta að heimildargögn og markgögn sé varpað rétt
Vörpun er aðgerð sem gildir um bæði innflutnings- og útflutningsverk.

- Í tengslum við innflutningsverk lýsir vörpun hvaða dálkar í upprunalistanum verða dálkarnir í sviðsetningartöflunni. Þess vegna getur kerfið ákvarðað hvaða dálkargögn í upprunaskránni þarf að afrita í hvaða dálk á sviðsetningartöflunni.
- Í samhengi við útflutningsverk lýsir vörpun því hvaða dálkar í sviðsetningartöflu (þ.e. uppruninn) verða að dálkum í markskránni.

Ef dálknöfnin í sviðsetningartöflunni og skránni passa saman, stofnar kerfið sjálfkrafa vörpun, byggt á nöfnum. Hins vegar, ef nöfnin eru frábrugðin, eru dálkar ekki merkt sjálfkrafa. Í þessum tilvikum verður þú að klára vörpunina með því að velja **Skoða vörpun** á einingunni í gagnaverkinu.

Það eru tvö vörpunaryfirlit: **Myndræn framsetning vörpunar**, sem er sjálfgefið yfirlit og **Upplýsingar um vörpun**. Rauð stjarna (\*) auðkennir alla áskilda reiti í einingunni. Þessa reiti þarf að varpa áður en hægt er að vinna með eininguna. Þú getur afvarpað af öðrum reitum eftir þörfum þegar unnið er með eininguna. Til að afvarpa reit velurðu reitinn í annaðhvort dálkinum **Eining** eða dálkinum **Uppruni** og velur svo **Eyða vali**. Veldu **Vista** til að vista breytingar og lokaðu svo síðunni til að fara aftur í verk. Þú getur notað sömu aðferð til að breyta vörpun reita frá upprunagögnum til millivistunar eftir að þú flytur inn.

Þú getur búið til vörpun á síðunni með því að velja **Búa til upprunavörpun**. Tilbúin vörpun hegðar sér eins og sjálfvirk vörpun. Þess vegna verður þú að varpa öllum óvörpuðum reitum handvirkt.

![Gagnavörpun](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Staðfestu öryggi fyrir innflutnings- eða útflutningsstarfið
Aðgangur að vinnusvæðinu **Gagnastjórnun** er hægt að takmarka, svo að notendur sem ekki eru stjórnandi geta aðeins fengið aðgang að tilteknum gagnastörfum. Aðgangur að gagnaverki felur í sér fullan aðgang að framkvæmdarsögu þess starfs og aðgang að sviðsetningartöflunum. Þess vegna verður þú að ganga úr skugga um að viðeigandi aðgangsstýringar séu til staðar þegar þú stofnar gagnastarf

### <a name="secure-a-job-by-roles-and-users"></a>Tryggja öryggi starfs eftir hlutverkum og notendum
Notaðu valmyndina **Gildandi hlutverk** til að takmarka starfið við eitt eða fleiri öryggishlutverk. Aðeins notendur í þessum hlutverkum munu hafa aðgang að starfi.

Þú getur einnig takmarkað starf við tiltekna notendur. Þegar þú tryggir starf eftir notendum í stað eftir hlutverki, er meiri stjórn þegar fleiri notendum er úthlutað hlutverki.

### <a name="secure-a-job-by-legal-entity"></a>Tryggja starf eftir einingu
Gagnastörf eru altæk í eðli sínu. Ef gagnastarf var stofnað og notað af lögaðila verður starfið því sýnilegt öðrum lögaðilum í kerfinu. Þessi sjálfgefna hegðun gæti verið valin í sumum notkunaraðstæðum. Til dæmis getur fyrirtæki sem flytur inn reikninga með því að nota gagnaeiningar útvegað miðlægt vinnsluteymi reikninga sem ber ábyrgð á að annast reikningavillur fyrir allar deildir fyrirtækisins. Við þessar aðstæður er gagnlegt fyrir miðlæga reikningsvinnsluhópinn að hafa aðgang að innheimtuvinnu frá öllum lögaðilum. Þess vegna uppfyllir sjálfgefið hegðun kröfu að því er varðar lögaðila.

Samt sem áður gæti fyrirtækið viljað hafa reikningsvinnsluhópa fyrir hvern lögaðila. Í þessu tilviki ætti teymi hjá lögaðila aðeins að hafa aðgang að reikningsinnflutningsstarfinu hjá eigin lögaðila. Til að mæta þeirri kröfu er hægt að skilgreina lögaðilamiðaða aðgangsstýringu fyrir gagnastörfin með því að nota valmyndina **Gildandi lögaðilar** inni í gagnastarfinu. Eftir að skilgreiningar eru valdar geta notendur aðeins séð störf sem eru í boði hjá lögaðila sem þeir eru skráðir inn á. Til að sjá störf frá öðrum lögaðila verða notendur að skipta yfir í þann lögaðila.

Starf getur verið tryggt eftir hlutverkum, notendum og lögaðilum á sama tíma.

## <a name="run-the-import-or-export-job"></a>Keyra inn- eða útflutningsstarfið
Þú getur keyrt vinnu starf sinni með því að velja hnappinn **Flytja inn** eða **Flytja út** eftir að þú skilgreinir starfið. Til að setja upp endurtekið starf skal velja **Stofna endurtekna gagnavinnslu**.

> [!NOTE]
> Hægt er að keyra innflutnings- eða útflutningsvinnslu með því að velja hnappinn **Innflutningur** eða **Útflutningur**. Þetta mun áætla keyrslu runuvinnsla einu sinni. Vinnslan verður ekki keyrð strax ef runuþjónusta er takmörkuð vegna álags á runuþjónustunni. Einnig er hægt að keyra vinnslurnar ósamstillt með því að velja **Flytja inn núna** eða **Flytja út núna**. Þetta setur vinnsluna strax af stað og er gagnlegt ef runa byrjar ekki sökum takmörkunar. Einnig er hægt að tímasetja vinnslur á að keyra síðar. Þetta er hægt að gera með því að velja **Keyra í runu** valkostinn. Runutilföng heyra undir takmörkun og getur því verið að runuvinnslan hefjist ekki strax. Ráðlagt er að nota runu vegna þess að hún hjálpar til við mikið gagnamagn sem þarf að flytja inn eða flytja út. Hægt er að áætla keyrslu á runuvinnslum í tilteknum runuflokk sem leyfir meiri stjórn hvað snertir álagsjöfnun.

## <a name="validate-that-the-job-ran-as-expected"></a>Staðfesta að vinnslan hafi gengið eins og búist var við með því að skoða vinnsluferilinn.
Vinnsluferillinn er tiltækur vegna villuleitar og skoðunar fyrir bæði innflutnings- og útflutningsvinnslu Sögulegar vinnslukeyrslur eru skipulögð eftir tímalengdum.

![Tímalengd vinnsluferils](./media/dixf-job-history.md.png)

Fyrir hverja vinnslu sem er keyrð fást eftirfarandi upplýsingar:

- Upplýsingar um framkvæmd
- Aðgerðaskrá

Upplýsingar um framkvæmd sýna stöðu hverrar gagnaeiningar sem unnin var í vinnslunni. Því er fljótlegt að finna eftirfarandi upplýsingar:

- Hvaða einingar var unnið með.
- Fyrir einingu, hversu margir færslur voru unnar með góðum árangri og hversu margar tókust ekki.
- Sviðsetninggögn fyrir hverja einingu.

Þú getur sótt sviðsetningargögn í skrá fyrir útflutningsvinnslu eða sótt hana sem pakka til að flytja inn og flytja störf.

Eftir framkvæmdarupplýsingunum er einnig hægt að opna framkvæmdarkladda

## <a name="parallel-imports"></a>Samhliða innflutningur
Til að flýta fyrir innflutningi gagna er hægt að virkja samhliða vinnslu á að flytja inn skrá ef einingin styður samhliða innflutning. Til að stilla samhliða innflutning fyrir eining verður að fylgja eftirfarandi skrefum.

1. Opnaðu **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.
2. Í hlutanum **Innflutningur / útflutningur** skaltu velja **Færibreytur ramma** til að opna síðuna **Færibreytur ramma fyrir inn- og útflutning gagna**.
3. Á flipanum **Stillingar einingar** skaltu velja **Grunnstilla framkvæmdafæribreytur einingar** til að opna síðuna **Framkvæmdafæribreytur innflutningseininga** page.
4. Stilltu eftirfarandi svæði til að grunnstilla samhliða innflutning fyrir einingu:

    - Veldu eininguna á svæðinu **Eining**.
    - Færðu inn færslufjölda innflutningsmarka til innflutnings á svæðinu **Færslufjöldi innflutningsmarka**. Þetta ákvarðar færslufjöldann sem á að vinna úr þræði. Ef skrá er með 10K færslur þýðir færslufjöldinn 2500 með verkfjölda 4 að hver þráður vinnur úr 2500 færslum.
    - Sláðu inn fjölda innflutningsverka á svæðið **Fjöldi innflutningsverka**. Þetta má ekki fara yfir hámark runuþráða sem úthlutað er til lotuvinnslu í **Kerfisstjórnun \>Grunnstilling netþjóns**.

## <a name="clean-up-the-staging-tables"></a>Hreinsa sviðsetningartöflurnar
Frá og með uppfærslu 29 á palli hefur þessari aðgerð verið úrelt. Þessu er skipt út fyrir nýja útgáfu af starfssöguhreinsunaraðgerðum sem lýst er hér að neðan.

Þú getur hreinsað sviðsetningartöflur með því að nota eiginleikann **Hreinsun sviðsetningar** í vinnusvæðinu **Gagnastjórnun**. Þú getur notað eftirfarandi valkosti til að velja hvaða færslur skuli eytt úr hvaða sviðsetningartöflu:

- **Eining**- Ef aðeins eining er gefin upp verður öllum færslum úr sviðsetningartöflu þeirrar einingar eytt. Veldu þennan möguleika til að hreinsa öll gögnin fyrir eininguna þvert á öll gögn og störf.
- **Vinnslukenni** – Ef aðeins er valið vinnslukenni verður öllum skrám fyrir allar einingar í valinni vinnslu eytt úr viðeigandi sviðsetningartöflum.
- **Gagnaverkefni**- Ef aðeins gagnaverkefni er valið eru allar skrár fyrir alla aðila og yfir öll störf fyrir valið gagnaverkefni eytt.

Þú getur einnig sameinað valkostina til að takmarka enn frekar skráarsettið sem er eytt.

## <a name="job-history-clean-up-available-in-platform-update-29-and-later"></a>Atvinnusaga hreinsun (fæst í uppfærslu pallsins 29 og nýrri)

Nota verður starfshreinsunarreynslu í gagnastjórnun til að skipuleggja reglubundna hreinsun á framkvæmdarsögunni. Þessi aðgerð kemur í stað fyrri hreinsunaraðgerða sviðsetningarborðsins, sem nú er úrelt. Eftirfarandi töflur verða hreinsaðar upp með hreinsunarferlinu.

-   Allar stigatöflur

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Virkja verður eiginleikann **Hreinsun vinnsluferils** í eiginleikastjórnun og síðan er hægt að opna hann í **Gagnastjórnun \> Hreinsun vinnsluferils**.

### <a name="scheduling-parameters"></a>Færibreytur röðunar

Við tímasetningu hreinsunarferilsins verður að tilgreina eftirfarandi breytur til að skilgreina hreinsunarviðmið.

-   **Fjöldi daga til að halda sögu** - Þessi stilling er notuð til að stjórna magni af framkvæmdarsögunni sem á að varðveita. Þetta er tilgreint í fjölda daga. Þegar hreinsunarstarfið er tímaáætlað sem endurtekið hópastarf mun þessi stilling virka eins og stöðugur hreyfanlegur gluggi, þannig að sagan verður alltaf skilin eftir tiltekinn fjölda daga ósnortinn meðan afganginum er eytt. Sjálfgildið er 7 dagar.

-   **Fjöldi klukkustunda til að framkvæma vinnsluna** - Það fer eftir upphæðinni sem þarf að hreinsa upp, heildar framkvæmdatími fyrir hreinsunarstarfið getur verið breytilegt frá nokkrum mínútum til nokkurra klukkustunda. Þessi færibreyta verður að vera stillt á fjölda klukkustunda sem vinnslan mun keyra. Eftir að hreinsunarvinnslan hefur keyrt í tiltekinn fjölda klukkustunda mun vinnslan stöðvast og hefja hreinsunina næst þegar hún er keyrð út frá endurkomuáætlun.

    Hægt er að tilgreina hámarks framkvæmdartíma með því að setja hámarksmörk á fjölda klukkustunda sem starfið verður að keyra með þessari stillingu. Hreinsunarmöguleikinn fer í gegnum eitt kennsl á framkvæmdastarfi í einu í tímaröð sem er raða, þar sem elsta er fyrst fyrir hreinsun tengdra framkvæmdasögu. Það mun hætta að taka upp ný framkvæmdarauðkenni til hreinsunar þegar eftirstöðvunartíminn er innan síðustu 10% af tiltekinni tímalengd. Í sumum tilvikum er búist við að hreinsunarstarfið haldi áfram yfir tilgreindan hámarkstíma. Þetta mun að mestu leyti ráðast af fjölda gagna sem á að eyða fyrir núverandi framkvæmdarauðkenni sem byrjað var áður en 10% þröskuldinum var náð. Hreinsun sem var hafin verður að vera lokið til að tryggja heilleika gagna, sem þýðir að hreinsunin mun halda áfram þrátt fyrir að fara yfir tilgreind mörk. Þegar þessu er lokið, eru ný framkvæmdarauðkenni ekki sótt og hreinsunarvinnslunni lokið. Sú framkvæmdaferð sem eftir er sem ekki var hreinsuð upp vegna skorts á nægum framkvæmdartíma, verður sótt næst þegar áætlað er að gera upp hreinsunarvinnsluna. Sjálfgefið og lágmarksgildi fyrir þessa stillingu er stillt á 2 klukkustundir.

-   **Endurtekin runa** - Hægt er að keyra hreinsunarstarfið sem staka, handvirka framkvæmd eða einnig er hægt að skipuleggja endurtekna framkvæmd í runu. Hægt er að skipuleggja rununa með stillingunum **Keyra í bakgrunni**, sem er venjulegi hópurinn sem settur er upp.

> [!NOTE]
> Ef færslur í sviðsetningatöflunum eru ekki hreinsaðar alveg upp skaltu tryggja að hreinsunarvinnslan sé áætluð til að keyra endurtekið. Eins og lýst er hér að ofan, í öllum hreinsunarframkvæmdum mun vinnslan aðeins hreinsa upp eins mörg framkvæmdakenni og hægt er innan hámarkstímanna. Til að halda áfram að hreinsa allar eftirstandandi sviðsetningarskrár verður að vinnslan að vera áætluð í reglulega keyrslu.

## <a name="job-history-clean-up-and-archival-available-for-preview-in-platform-update-39-or-version-10015"></a>Hreinsun vinnsluferils og safnskráar (í boði fyrir forskoðun í verkvangsuppfærslu 39 eða útgáfu 10.0.15)
Hreinsun vinnsluferils og virkni safnskráar kemur í stað fyrri útgáfa af virkni hreinsunar. Þessi hluti útskýrir þessa nýju eiginleika.

Ein af helstu breytingunum á virkni hreinsunar er notkun runuvinnslu kerfis til að hreinsa ferilinn. Notkun runuvinnslu kerfis gerir Finance and Operations -forritum kleift að hreinsa runuvinnsluna samkvæmt sjálfkrafa áætlun og keyra um leið og kerfið er tilbúið. Ekki er lengur nauðsynlegt að timasetja runuvinnsluna handvirkt. Í þessari sjálfgefnu framkvæmdarstillingu keyrir runuvinnslan hverja klukkustund og byrjar 12 á miðnætti og heldur eftir framkvæmdarferlinum fyrir næstu 7 daga þar á undan. Hreinsaði ferillinn er safnvistaður til heimtingar seinna meir.

> [!NOTE]
> Þetta er forskoðun þessarar virkni og því um runuvinnsla kerfis ekki eyða framkvæmdarferli þar til slíkt er virkjað með forútgáfunni DMFEnableExecutionHistoryCleanupSystemJob. Þegar eiginleikinn er almennt tiltækur í síðari útgáfu verður forútgáfunnar ekki krafist og runuvinnsla kerfisins hefst á hreinsun og safnvistun um leið og kerfið er tilbúið samkvæmt skilgreindu áætluninni eins og lýst er hér á undan. 

> [!NOTE]
> Í síðari útgáfu verða fyrri útgáfur eiginleika hreinsunar fjarlægðar úr Finance and Operations -forritum.

Önnur breytingin á hreinsunarferlinu er safnvistun á hreinsuðum framkvæmdarferli. Hreinsunarvinnslan safnvistar eyddum færslum í BLOB-geymslu sem DIXF notar fyrir reglubundnar samþættingar. Safnvistaða skráin verður á DIXF-pakkasniði og verður tiltæk í 7 daga í BLOB og verður hægt að hlaða hana niður á því tímabili. Hægt er að breyta sjálfgefinni tímalengd 7 daga fyrir safnvistuðu skrána í að hámarki 90 daga í færibreytunum.

### <a name="changing-the-default-settings"></a>Breyting á sjálfgefnum stillingum
Þessi virkni er í forskoðun og þarf að kveikja á henni með því að virkja forútgáfuna DMFEnableExecutionHistoryCleanupSystemJob. Einnig verður að kveikja á eiginleika hreinsunar í sviðsetningu í eiginleikastjórnun.

Til að breyta sjálfgefnu stillingunni fyrir tímalengd safnvistuðu skáarinnar skal fara á vinnusvæði gagnastjórnunar og velja **Hreinsun vinnsluferils**. Stillið **Dagar sem varðveita á pakka í BLOB** á gildi á milli 7 og 90 (til og með). Þetta mun taka gildi í skjalasöfnum sem stofnuð voru eftir að þessi breyting var gerð.

### <a name="downloading-the-archived-package"></a>Hlaða niður safnvistaða pakkanum
Þessi virkni er í forskoðun og þarf að kveikja á henni með því að virkja forútgáfuna DMFEnableExecutionHistoryCleanupSystemJob. Einnig verður að kveikja á eiginleika hreinsunar í sviðsetningu í eiginleikastjórnun.

Til að hlaða niður safnvistaða vinnsluferlinum skaltu fara á vinnusvæði gagnastjórnunar og velja **Hreinsun vinnsluferils**. Veldu **Öryggisafritunarferill pakka** til að opna eyðublað ferils. Þetta eyðublað sýnir lista yfir alla safnvistaða pakka. Hægt er að velja safn og hlaða niður með því að velja **Sækja pakka**. Upphalspakkinn verður á DIXF-pakkasniði og inniheldur eftirfarandi skrár:

-   Skrá millistigsvistunartöflu einingar sviðsetningar
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   DMFSTAGINGLOG
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]