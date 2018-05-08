---
title: "Inn- og útflutningsvinnsla gagna"
description: "Notaðu vinnusvæðið Gögnastjórnun til að búa til og stjórna Inn- og útflutningsvinnslu gagna."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fc47f6cd9cfe4a850e0959bf89da086ca82f3b69
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="data-import-and-export-jobs"></a>Inn- og útflutningsvinnsla gagna

[!include [banner](../includes/banner.md)]

Til að búa til og stjórna inn- og útflutningsvinnslu gagna í Microsoft Dynamics 365 for Finance and Operations skal nota vinnusvæðið **Gagnastjórnun**. Sjálfgefið er að Inn- og útflutningsferli gagna skapi uppsetningartöflu fyrir hverja einingu í markgagnagrunninum. Millistigsvistunartöflu leyfir þér að staðfesta, hreinsa upp eða breyta gögnum áður en þú færir þau.

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

| **Skrársnið**        | **Afmarkari fyrir línu/dálk**                   | **XML-stíll**             |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-NA-                     |
| XML                    | \-NA-                                      | XML-eining XML-eigind |
| Afmarkað, föst breidd | Komma, semíkomma, flipi, lóðrétt strik, tvípunktur | \-NA-                     |



### <a name="sequence-the-entities"></a>Einingunum raðað
Einingum má raða í gagnasniði, eða í innflutnings- og útflutningssverkum. Þegar þú keyrir verk sem inniheldur fleiri en eina gagnaeiningu verður þú að ganga úr skugga um að einingunum sé rétt raðað. Einingum er raðað til að geta leyst hugsanleg virknitengsl milli eininga. Ef einingar eru ekki með virknitengsl  er hægt að tímastilla þær fyrir samhliða inn- og útflutning.

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

Valmyndin **Endurröðun** er í boði þegar margar einingar eru valdar. Hægt er að endurraða á grundvelli valkostanna framkvæmdareiningar, stigs eða raðar. Þú getur stillt stighækkun til að endurraða einingum sem voru valdar.  Einingin, stigið og / eða raðnúmerið sem er valið fyrir hverja einingu er uppfært með tilgreindri stighækkun.

#### <a name="sorting"></a>Röðun
Hægt er að nota valkostinn **Raða eftir** til að skoða einingalistann í röð.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Staðfesta að heimildargögn og markgögn sé varpað rétt
Vörpun er aðgerð sem gildir um bæði innflutnings- og útflutningsverk.

- Í tengslum við innflutningsverk lýsir vörpun hvaða dálkar í upprunalistanum verða dálkarnir í sviðsetningartöflunni. Þess vegna getur kerfið ákvarðað hvaða dálkargögn í upprunaskránni þarf að afrita í hvaða dálk á sviðsetningartöflunni.
- Í samhengi við útflutningsverk lýsir vörpun því hvaða dálkar í sviðsetningartöflu (þ.e. uppruninn) verða að dálkum í markskránni.

Ef dálknöfnin í sviðsetningartöflunni og skránni passa saman, stofnar kerfið sjálfkrafa vörpun, byggt á nöfnum. Hins vegar, ef nöfnin eru frábrugðin, eru dálkar ekki merkt sjálfkrafa. Í þessum tilvikum verður þú að klára vörpunina með því að velja **Skoða vörpun**á einingunni í gagnaverkinu.

Það eru tvö vörpunaryfirlit: **Myndræn framsetning vörpunar**, sem er sjálfgefið yfirlit og **Upplýsingar um vörpun**. Rauð stjarna (\*) auðkennir alla áskilda reiti í einingunni. Þessa reiti þarf að varpa áður en hægt er að vinna með eininguna. Þú getur afvarpað af öðrum reitum eftir þörfum þegar unnið er með eininguna. Til að afvarpa  reit velurðu reitinn í annað hvort dálkinum **Eining** eða dálkinum **Uppruni**  og velur svo **Eyða vali**. Veldu **Vista** til að vista breytingar og lokaðu svo síðunni til að fara aftur í verk. Þú getur notað sömu aðferð til að breyta vörpun reita frá upprunagögnum til millivistunar eftir að þú flytur inn.

Þú getur búið til vörpun á síðunni með því að velja**Búa til upprunavörpun**. Tilbúin vörpun hegðar sér eins og sjálfvirk vörpun. Þess vegna verður þú að varpa öllum óvörpuðum reitum handvirkt.

![Gagnavörpun](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Staðfestu öryggi fyrir innflutnings- eða útflutningsstarfið
Aðgangur að vinnusvæðinu **Gagnastjórnun**er hægt að takmarka, svo að notendur sem ekki eru stjórnandi geta aðeins fengið aðgang að tilteknum gagnastörfum. Aðgangur að gagnaverki felur í sér fullan aðgang að framkvæmdarsögu þess starfs og aðgang að sviðsetningartöflunum. Þess vegna verður þú að ganga úr skugga um að viðeigandi aðgangsstýringar séu til staðar þegar þú stofnar gagnastarf

### <a name="secure-a-job-by-roles-and-users"></a>Tryggja öryggi starfs eftir hlutverkum og notendum
Notaðu valmyndina **Gildandi hlutverk** til að takmarka starfið við eitt eða fleiri öryggishlutverk. Aðeins notendur í þessum hlutverkum munu hafa aðgang að starfi.

Þú getur einnig takmarkað starf við tiltekna notendur. Þegar þú tryggir starf eftir notendum í stað eftir hlutverki, er meiri stjórn þegar fleiri notendum er úthlutað hlutverki.

### <a name="secure-a-job-by-legal-entity"></a>Tryggja starf eftir einingu
Gagnastörf eru altæk í eðli sínu. Ef gagnastarf var stofnað og notað af lögaðila verður starfið því sýnilegt öðrum lögaðilum í kerfinu. Þessi sjálfgefna hegðun gæti verið valin í sumum notkunaraðstæðum. Til dæmis getur fyrirtæki sem flytur inn reikninga með því að nota gagnaeiningar útvegað miðlægt vinnsluteymi reikninga sem ber ábyrgð á að annast reikningavillur fyrir allar deildir fyrirtækisins. Við þessar aðstæður er gagnlegt fyrir miðlæga reikningsvinnsluhópinn að hafa aðgang að innheimtuvinnu frá öllum lögaðilum. Þess vegna uppfyllir sjálfgefið hegðun kröfu að því er varðar lögaðila.

Samt sem áður gæti fyrirtækið viljað hafa reikningsvinnsluhópa fyrir hvern lögaðila. Í þessu tilviki ætti teymi hjá lögaðila aðeins að hafa aðgang að reikningsinnflutningsstarfinu hjá eigin lögaðila. Til að mæta þeirri kröfu er hægt að skilgreina lögaðilamiðaða aðgangsstýringu fyrir gagnastörfin með því að nota valmyndina **Gildandi lögaðilar** inni í gagnastarfinu. Eftir að skilgreiningar eru valdar geta notendur aðeins séð störf sem eru í boði hjá lögaðila sem þeir eru skráðir inn á. Til að sjá störf frá öðrum lögaðila verða notendur að skipta yfir í þann lögaðila.

Starf getur verið tryggt eftir hlutverkum, notendum og lögaðilum á sama tíma.

## <a name="run-the-import-or-export-job"></a>Keyra inn- eða útflutningsstarfið
Þú getur keyrt vinnu starf sinni með því að velja hnappinn **Flytja inn** eða **Flytja út** eftir að þú skilgreinir starfið. Til að setja upp endurtekið starf skal velja **Stofna endurtekna gagnavinnslu**.

## <a name="validate-that-the-job-ran-as-expected"></a>Staðfesta að vinnslan hafi gengið eins og búist var við með því að skoða vinnsluferilinn.
Vinnsluferillinn er tiltækur vegna villuleitar og skoðunar fyrir bæði innflutnings- og útflutningsvinnslu Sögulegar vinnslukeyrslur eru skipulögð eftir tímalengdum.

![Tímalengd vinnsluferils](./media/dixf-job-history.md.png)

Fyrir hverja vinnslu sem er keyrð fást eftirfarandi upplýsingar:

- Upplýsingar um framkvæmd
- Aðgerðaskrá

Upplýsingar um framkvæmd sýna stöðu hverrar gagnaeiningar sem unnin var í vinnslunni. Því er fljótlegt að finna eftirfarandi upplýsingar:

- Hvaða einingar var unnið með
- Fyrir einingu, hversu margir færslur voru unnar með góðum árangri og hversu margar mistókst
- Sviðsetninggögn fyrir hverja einingu

Þú getur sótt sviðsetningargögn í skrá fyrir útflutningsvinnslu eða sótt hana sem pakka til að flytja inn og flytja störf.

Eftir framkvæmdarupplýsingunum er einnig hægt að opna framkvæmdarkladda

## <a name="clean-up-the-staging-tables"></a>Hreinsa sviðsetningartöflurnar
Þú getur hreinsað sviðsetningartöflur með því að nota eiginleikann **Hreinsun sviðsetningar** í vinnusvæðinu **Gagnastjórnun**. Þú getur notað eftirfarandi valkosti til að velja hvaða færslur skuli eytt úr hvaða sviðsetningartöflu:

- **Eining**- Ef aðeins eining er gefin upp verður öllum færslum úr sviðsetningartöflu þeirrar einingar eytt. Veldu þennan möguleika til að hreinsa öll gögnin fyrir eininguna þvert á öll gögn og störf.
- **Vinnslukenni** – Ef aðeins er valið vinnslukenni verður öllum skrám fyrir allar einingar í valinni vinnslu  eytt úr viðeigandi sviðsetningartöflum.
- **Gagnaverkefni**- Ef aðeins gagnaverkefni er valið eru allar skrár fyrir alla aðila og yfir öll störf fyrir valið gagnaverkefni eytt.

Þú getur einnig sameinað valkostina til að takmarka enn frekar skráarsettið sem er eytt.

