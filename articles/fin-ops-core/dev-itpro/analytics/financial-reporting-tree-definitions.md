---
title: Skipuritsskilgreiningar í fjárhagsskýrslum
description: Þessi skrá upplýsingar um skipuritsskilgreiningar. Skipuritsskilgreining er skýrsluhluti, eða eining, sem aðstoðar við að skilgreina byggingu og stigveldi fyrirtækisins þíns.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8127c694d21064392b1932525a87044b9554973d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181819"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Skipuritsskilgreiningar í fjárhagsskýrslum

[!include [banner](../includes/banner.md)]

Þessi skrá upplýsingar um skipuritsskilgreiningar. Skipuritsskilgreining er skýrsluhluti, eða eining, sem aðstoðar við að skilgreina byggingu og stigveldi fyrirtækisins þíns.

Fjárhagsskýrslugerð styður sveigjanlega skýrslugerð svo að auðvelt er að gera breytingar eftir því sem uppbygging starfsemi þinnar breytist. Skýrslur eru búnar til úr ýmsum þáttum, eða einingum. Eitt af þessum einingum er skipuritsskilgreining. skipuritsskilgreining aðstoðar við að skilgreina byggingu og stigveldi fyrirtækisins þíns. Hún er þvervíddarlegt stigveldi sem byggist á víddarvenslum innan fjárhagsgagnanna. Hún veitir upplýsinga á stigi einingar skipuritsins og á stigi samantektarinnar fyrir allar einingar í trénu. Skýrslugerð skilgreiningar hugbúnaðarhlutatrénu getur verið samsettur með dálkaskilgreiningar og skýrsluskilgreiningar sem á að stofna loka bygging flokk sem er hægt að nota með mörgum fyrirtækjum. eining skipurits er notuð fyrir hvern gátreit í skipuriti. Eining skipurits getur verið einstök deild úr fjárhagsgögnum eða hún getur verið samantektareining sem tvinnar saman upplýsingar frá öðrum einingum skipurits. Ein skýrsla er mynduð fyrir hverja einingu skipurits sem og fyrir samantektarstigið fyrir skýrsluskilgreiningu sem inniheldur skipurit. Allar þessar skýrslur nota línu- og dálkaskilgreiningar sem eru tilgreindar í skýrsluskilgreiningu, nema skýrsluskilgreining tilgreinir að nota eigi skipuritið úr línuskilgreiningunni. Línu- og dálkskilgreiningar eru mikilvægir íhlutir í hönnun og virkni fjárhagsskýrslna. Skipurit auka styrk íhlutanna og styðja við sveigjanlega skýrslugerð samhliða því að rekstrarskipulagið breytist. Fjárhagsskýrslur sem eru ekki byggðir á skipuriti nota aðeins hluta af getu reikningsskila. Hægt er að nota margar skipuritsskilgreiningar saman með sömu skilgreiningar á röðum og dálkum til að skoða gögn fyrirtækisins á mismunandi vegu.

## <a name="reporting-tree-best-practices"></a>Besta framkvæmd skipurits
Þegar skipurit er stofnuð skaltu íhuga eftirfarandi bestu framkvæmd:

- Fyrst að athuga hvaða skýrslugerðarvíddum lögaðila eða fyrirtækið þitt þarfnast.
- Íhugaðu hvernig þú settir upp uppbygginguna og teiknaðu síðan upp skipurit fyrirtækis þíns. Fyrirtækisskipuritið gefur myndræna sýn á hvernig flokka má einingar skipuritsins í eitt eða fleiri skipurit.
- Byrjið á lægsta tiltæka upplýsingastigi, svo sem deildum eða verkefnum sem skilgreind eru í fjárhagsgögnunum. Bættu eins mörgum reitum við nákvæmnistigið eins og þarf til að sýna svið eða svæði á hærra stigi. Hver reitur stendur fyrir hugsanlega einingu í stofnuðum skipuritum.
- Einnig þarf að ákvarða bestu leiðina til að byggja skipuritin upp. Þú getur notað sjálfvirkt byggingarferli til að mynda skipurit, eða þú getur handvirkt stofnað skipurit. Mikilvægt er að hafa skilning á báðum aðferðum áður en lagt er í hönnun trjánna.
- Hægt er að nota einingar skipurits sem eru skilgreindar í fjárhagsgagnakerfinu til að bæta einingum skipurits við skilgreiningu skipurits.

## <a name="create-multiple-reporting-trees"></a>Mörg skipurit stofnuð
Hægt er að stofna ótakmarkaðan fjölda af skipuritum til að skoða gögn fyrirtækisins á mismunandi vegu. Hvert skipurit getur innihaldið hvaða samsetningu af deildum og samantektareiningum sem er. Skýrsluskilgreining getur aðeins verið með tengil í eitt skipurit í einu. Með því að endurraða uppbyggingu eininga skipuritsins er hægt að stofna önnur skipurit. Síðan má nota sömu línu- og dálkaskilgreiningu fyrir hvert skipurit. Á þennan hátt geturðu stofnað á skjótan hátt mismunandi útlit fjárhagsskýrslna. Ef þú stofnar mörg skipurit, geturðu prentað nokkrar fjárhagsskýrslur í hverjum mánuði sem greina og sýna aðgerðir fyrirtækis þíns á mismunandi hátt. Fyrir frekar upplýsingar, sjá æmi um uppbyggingu einingar skipurits í lok þessa grein

## <a name="create-a-reporting-tree-definition"></a>Skilgreining skipurits stofnuð
skipuritsskilgreining inniheldur dálkana sem lýst er í eftirfarandi töflu.

| Skipuritsdálkur | Lýsing |
|-----------------------|-------------|
| Fyrirtæki               | Heiti fyrirtækis fyrir einingu skipurits. Gildið **@ANY**, sem er yfirleitt eingöngu tengt samantektarstiginu, gerir kleift að nota skipuritið fyrir öll fyrirtækin. Allar undirgreinar eru tengdar við fyrirtæki. |
| Einingarheiti             | Kóðinn sem auðkennir þessa einingu skipurits í myndræna skipuritinu. Gætið þess að koma á einkvæmt kóðunarkerfi sem er samkvæmt sjálfu sér, og sem er auðvelt að skilja fyrir notendur. |
| Lýsing einingar      | Titill skipuritseiningar kemur fram í haus eða fæti skýrslunnar ef **UnitDesc** er fært inn sem kóði í flipanum **Hausar og fætur** í skýrsluskilgreiningunni. Titillinn kemur fram í línulýsingu skýrslunnar ef **UnitDesc** er fært inn í hólfið **Lýsing** í línuskilgreiningunni. |
| Víddir            | Eining skipurits sem sækir upplýsingar beint úr fjárhagsgögnum. Skilgreinir tölfræðilega staðsetningu og lengdir fyrir reikninginn og tengda hluta. Allar línur skipuritseiningar verða að hafa vídd í þessum dálki. Þú getur einnig sett vídd í línu samantektareiningar, (t.d. fyrir útgjöld sem eru beint tengd við þá einingu). Ef vídd er sett inn í línu samantektareiningar ættu reikningar sem notaðir eru í yfireiningum ekki að vera notaðir í undireiningum. Annars gætu upphæðir verið tvíteknir. |
| Línuskilgreiningar       | Heiti línuskilgreiningar fyrir einingu skipurits. Sama línuskilgreining er notuð fyrir hverja einingu í skipuritinu. Þegar skýrsla er mynduð er þessi línuskilgreining notuð fyrir hverja einingu skipurits. Línuskilgreiningin getur innihaldið marga fjárhagsvíddartengla. Ef línuskilgreining er tilgreind í skipuriti er valinn gátreiturinn **Nota línuskilgreiningu úr skipuriti** í flipanum **Skýrsla** í skýrsluskilgreiningunni. |
| Línutengill              | Línutengillinn sem notaður er fyrir einingu skipurits. Línutenglar eru skilgreindir fyrir línuskilgreininguna til að auðkenna fjárhagsvíddirnar sem tengja á í. |
| Ytri tengill         | Línutengillinn sem notaður er fyrir þessa einingu skipurits. Línutenglar eru skilgreindar fyrir línuskilgreiningu til að auðkenna skýrslu sem tengja á við. |
| Ytri skrá         | Skráarslóð vinnublaðs reikningsskila til að sækja gögn úr. |
| Valkostir síðu          | Þessi dálkur Stýrir hvort upplýsingar fyrir eining skipurits er falin þegar skýrslan er skoðuð eða prentuð. |
| Samantekt %              | Hlutfall einingar skipurits sem úthluta á til yfireiningar. Hlutfallið sem fært er inn í þennan dálk á við um hverja línu í línuskilgreiningunni áður en gildinu í línunni er bætt við yfirskýrsluna. Sem dæmi má nefna að ef skipta verður undireiningu jafnt milli tveggja deilda eru fjárhæðirnar í hverri línu margfaldaðar með 50 prósentum áður en virðinu er bætt við deildarskýrsluna. Ein eining skipurits má ekki hafa tvær yfireiningar. Til að úthluta fjárhæðum úr einingu skipurits á tvær yfireiningar skal stofna aðra einingu skipurits með sömu vídd til að taka saman hin 50 prósentin. Færið inn heilar prósentutölur án tugakommu. Til dæmis **25** stendur fyrir úthlutun 25 prósenta til yfireiningarinnar. Ef aukastafur er hafður með (**.25**), er 0,25 prósent er úthlutað á yfireiningu. Til að nota prósentu sem er minni en einn prósent, skal nota **Leyfa Samantekt &lt;1%** valkost í skýrsluskilgreininguna. Þessi valkostur er í flipanum **Aukavalkostir** í svarglugganum **Skýrslustillingar**. Þú færð aðgang að þessum svarglugga úr **Annað** hnappinn á í **Stillingar** flipanum í skýrsluskilgreiningu. |
| Einingaröryggi         | Takmarkanir fyrir notendur og hópa sem geta fengið aðgang að upplýsingar fyrir eining skipurits. |
| Viðbótartexti       | Texti sem kemur fram í skýrslunni. |

Til að stofna skipuritsskilgreiningu, skal fylgja eftirfarandi skrefum.

1. Opnið Skýrsluhönnun.
2. Smella á **Skrá** &gt; **Nýtt** &gt; **Skilgreining skipurits**.
3. Smellið á **Breyta** &gt; **Setja inn einingar skipurits úr víddum**.
4. Í svarglugganum **Setja inn einingar skipurits úr víddum** skal velja gátreitinn fyrir hverja vídd sem taka á með í skipuritinu. Í svarglugganum **Setja inn einingar skipurits úr víddum** birtast eftirfarandi hlutar.

    | Hluti                          | Lýsing |
    |----------------------------------|-------------|
    | Hlutun skipuritsvíddar | Notið hnappana **Skipta hlutum** og **Sameina hluta** til að breyta fjölda og lengd hluta.<blockquote>[!NOTE] Aðeins er hægt að sameina hluta sem hefur verið skipt upp. Til að sameina margar víddir skal nota algildi í víddargildunum.</blockquote> |
    | Hafa með/Staða stafs       | Þessi hluti Birtir víddirnar sem skilgreindar eru í fjárhagsgögnunum og sýnir fjölda stafa í lengsta skilgreinda gildi fyrir hverja vídd. Veljið þennan gátreit fyrir vídd sem skal hafa með í þeirri vídd í stigveldi skipuritsins. |
    | Hlutun stigveldis og sviða     | Þessi hluti sýnir stigveldi vídda. Hægt er að færa víddir til í listanum til að breyta röð þeirra í skýrslu. Tilgreina svið gilda innan hverrar víddar í á **Úr Vídd** og **Til Vídd** reiti. Ef ekkert svið er tilgreint verða öll víddargildi sett inn á skipuritið.<blockquote>[!NOTE] Ef verið er að nota fleiri en ein vídd munu aðeins víddarsamsetningar sem hefur verið bókað á skila sér í niðurstöðum.</blockquote> |

    Fyrir skjáskot sem sýnir dæmi um **Setja inn einingar skipurits úr víddum** svarglugganum, sjá hlutann "Dæmi um Setja inn einingar skipurits úr víddum-svarglugga" síðar í þessari grein.

5. Til að stofna viðbótarhluta, (svo sem að skipta einum hluta í tvo styttri), er smellt á rétta staðsetningu í reitnum **Staða stafs** og svo smella á **Skipta hlutum**.
6. Til að sameina tvo hluta í einn, er smellt í reit annars hlutans sem á að sameina og smella svo á **Sameina hluta**.
7. Stigveldið skilgreinir hvernig víddir heyra saman og einnig svið hverrar víddar. Til að breyta stigveldi víddanna, á svæðinu **Hlutun stigveldis og sviða**, er valin sú vídd sem á að færa, og smellt svo á **Flytja upp** eða **Flytja niður**.
8. Til að tilgreina svið víddagilda til að bæta við nýtt skipurit skal fylgja eftirfarandi skrefum á svæðinu **Hlutun stigveldis og sviða**:

    1. Færið inn fyrsta gildið í sviðinu fyrir víddina í reitnum **Úr vídd**.
    2. Í **Til Vídd** reitnum, skal færa inn síðasta gildi á bilinu.

9. Fyrir hverja vídd á svæðinu **Hlutun stigveldis og sviða** skal endurtaka skref 7 til 8.
10. Þegar búið er að skilgreina hvernig setja á einingar skipuritsins inn í nýja skipuritið er smellt á **Í lagi**.
11. Smellið á **Skrá** &gt; **Vista** til að vista skipuritið. Færið inn einkvæmt heiti og lýsingu á skipuritinu og smellið svo á **Í lagi**.

### <a name="open-an-existing-reporting-tree-definition"></a>Fyrirliggjandi skilgreining skipurits opnuð

1. Í Skýrsluhönnun er smellt á **Skilgreiningar skipurits** á yfirlitssvæðinu.
2. Tvísmellið á heiti í skipuritalistanum til að opna það.
3. Hægrismellið á skipuritsskilgreiningu og veljið **Tengingar** til að skoða allar einingar sem tengjast því skipuriti.

### <a name="roll-up-data-in-a-reporting-tree"></a>Gögn tekin saman í skipuriti

Þegar þú notast við skipurit geturðu safnað upphæðum úr undireiningum skipurits á stigi yfireiningar skipuritsins. Þessi uppsöfnun er kölluð að taka saman gögn. Eftirfarandi reglur eru notaðar til að taka saman upphæðir í yfireiningar í skipuriti:

- Í skipuriti verða undireiningar að innihalda víddir, nema skipuritið sé á einu stigi. Yfireiningar innihalda yfirleitt ekki víddir í skipuriti.

    > [!NOTE]
    > Ef þú tilgreinir víddir fyrir undireiningar og yfireiningar gætirðu valdið tvítekningu gagna í skýrslunni.

- Einingar skipurits sem innihalda víddir í skipuritinu samsvara víddunum sem eru notaðar í línu- og dálkskilgreiningunum. Samsetning víddanna ákvarðar upphæðirnar sem er skilað fyrir þá einingu. Til dæmis, í dæmi 2 síðar í þessari grein, skila línur 6 og 7 aðeins gildunum fyrir deild 00 og 01, í þeirri röð.
- Upphæðirnar fyrir yfireiningar skipurits sem innihalda ekki víddir í skipuritinu eru ákvarðaðar út frá skýrslu undireiningarinnar og taka saman upphæðina í tilteknu yfireininguna. Til dæmis ef yfireining (sjá Contoso USA í dæmi 2 fyrir dæmi um samantekt gagna) er með tvær undireiningar (022 og 023) og inniheldur ekki víddir þá er mynduð skýrsla fyrir bæði undireininguna og yfireininguna. Samtala yfireiningarinnar er samtala hinna tveggja upphæða undireininganna.

### <a name="manage-reporting-units"></a>Einingum skipurits stjórnað

Hvert skipuritsskilgreining er birt í einkvæmum yfirlitum. Til er bæði yfirlit sem setur stigveldi yfir- og undireininga fram á myndrænan hátt og vinnublaðsyfirlit sem sýnir tilteknar upplýsingar fyrir hverja einingu skipurits. Myndræna yfirlitið og vinnublaðsyfirlitið eru tengd. Þegar eining skipurits er valin í einu yfirliti, er hún einnig valin í hinu yfirlitinu. Notandi getur byggt upp þvervíddarleg stigveldi sem byggjast á víddarvenslum innan fjárhagsgagnanna. Þegar skipuritsskilgreining er stofnuð er hægt að nota sömu línuskilgreiningar endurtekið, hvort sem verið er að mynda rekstrarreikning deildar eða samantekinn samstæðurekstrarreikning. Nota má víddir sem eru skilgreindar í línuskilgreiningunni ásamt víddum í skipuritsskilgreiningu til að bjóða upp á sveigjanlegt yfirlit yfir afkomu fyrirtækisins.

### <a name="reporting-unit-structure"></a>Uppbygging einingar skipurits

Eftirfarandi gerðir eininga skipurits eru notaðar í reikningsskilum:

- Upplýsingaeining tekur upplýsingar beint úr fjárhagsgögnum, úr Excel-töflureiknisskrá eða úr öðru vinnublaði reikningsskila.
- Samantektareining tekur saman gögn úr einingum á neðri stigum.

Yfireining í skipuriti er samantektareining sem safnar saman samantektarupplýsingum úr upplýsingaeiningu. samantektareining getur verið bæði upplýsingaeining og samantektareining. Þess vegna getur samantektareining tekið upplýsingar úr einingu á neðra stigi, fjárhagsgögnum, eða Excel-vinnublaði. Yfireining getur verið undireining hærra skipaðrar yfireiningar. Undireining í skipuriti getur verið upplýsingaeining sem sækir upplýsingar beint úr fjárhagsgögnum eða excel-vinnublaði. Undireining í einingu skipurits getur einnig verið millisamantektareining. Með öðrum orðum, það getur verið yfireining af einingar af neðra stigi, og einnig undireining samantektareiningar á hærra stigi. Við Algengustu aðstæður fyrir einingar í skipuriti, hafa yfireiningar auð hólf í dálknum **Víddir** , og undireiningar hafa tengla í tilteknar víddarsamsetningar eða algildisvíddarsamsetningar

### <a name="organize-reporting-units"></a>Einingar skipurits skipulagðar

Hægt er að endurskipuleggja skipulag skipuritsskilgreiningarinnar með því að færa skipuritseiningar í myndræna yfirlitinu. Einnig er hægt að færa einingar í skipuriti upp á hærra stig í skipuritinu eða færa þær á lægra stig í skipuritinu.

1. Opnið skilgreiningu skipuritsins í Skýrsluhönnun til að gera breytingar.
2. Veljið skipuritseiningu í myndrænu yfirliti skilgreiningar skipuritsins.
3. Draga einingu í nýja stöðu. Annars má líka hægrismella á eininguna og veljið síðan **Færa upp einingu skipurits** eða **Færa niður einingu skipurits**.
4. Smellið á **Skrá** &gt; **Vista** til að vista breytingar.

### <a name="add-text-about-a-reporting-unit"></a>Bæta inn Texta um einingu skipurits

Viðbótartextafærsla er fastur textastrengur, allt að 255 stafir, sem bætir upplýsingum við skipuritsskilgreininguna. Til dæmis getur viðbótartexti verið stutt lýsing á fyrirtæki. Hægt er að stofna allt að tíu viðbótartextafærslur fyrir hverja einingu skipurits í skipuritsskilgreiningu. Viðbótartextinn birtist í skýrslunni fyrir skipuritseininguna sem textanum var úthlutað til. Hægt er að bæta við textafærslum frá dálkinum **Lýsing** í línuskilgreiningunni og frá flipanum **Hausar og fætur** í skýrsluskilgreiningunni.

1. Opnið skilgreiningu skipuritsins í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið **Viðbótartexti** fyrir línu einingar skipurits.
3. Í svarglugganum **Viðbótartexti** í fyrstu auðu línunni, skal færa inn textann. Vísað er til fyrstu línunnar sem inniheldur texta sem UnitText1 burtséð frá stöðu hans í svarglugganum **Viðbótartexti**.
4. Ef bæta á við fleiri textafærslum fyrir þessa skipuritseiningu skal færa textann inn í auða línu.
5. Smelltu á **Í lagi**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Viðbótartexti fjarlægður úr einingu skipurits

1. Opnið skilgreiningu skipuritsins í Report Designer til að gera breytingar.
2. Tvísmellið á hólfið **Viðbótartexti** fyrir línu skipuritseiningar.
3. Í svarglugganum **Viðbótartexti** skal velja færsluna sem á að fjarlægja og síðan smella á **Hreinsa**. Einnig er hægrismellt á færslu og veljið svo **Klippa**.
4. Smelltu á **Í lagi**.

### <a name="restrict-access-to-a-reporting-unit"></a>Aðgangur að einingu skipurits takmarkaður

Hægt er að koma í veg fyrir að tilteknir notendur eða hópar fái aðgang að skipuritseiningu. Einnig er hægt að tilgreina takmarkanir þannig að þær eiga við undireiningar skipurits fyrir eining skipurits.

1. Opnið skilgreiningu skipuritsins í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið **Einingaröryggi** fyrir einingarlínu skipuritsins til að takmarka aðganginn.
3. Í svarglugganum **Einingaröryggi** er smellt á **Notendur og hópar**.
4. Veljið notendur eða hópa sem eiga að fá aðgang að einingu skipurits, og smellið síðan á **Í lagi**.
5. Ef takmarka á aðgang að undireiningu skipurits er valinn gátreiturinn **Bæta öryggi við undireiningar skipurits.**
6. Smelltu á **Í lagi**.

### <a name="remove-access-to-a-reporting-unit"></a>Aðgangur að einingu skipurits fjarlægður

1. Opnið skilgreiningu skipuritsins í Skýrsluhönnun til að gera breytingar.
2. Tvísmellið á hólfið **Einingaröryggi** fyrir línu skipuritsins sem á að fjarlægja aðganginn að.
3. Í svarglugganum **Einingaröryggi** er heiti valið og síðan smellt á **Fjarlægja**.
4. Smelltu á **Í lagi**.

### <a name="link-toreports"></a>Tenglar í skýrslur

Þegar dálkur af gerðinni **skýrsla** hefur verið stofnaður í línuskilgreiningunni og tilgreind hefur verið skýrsla sem taka á með í skýrslunni, verður að uppfæra skipuritið með tengda dálknum og skýrsluupplýsingunum. Hægt er að flytja inn skýrslu í hvaða einingu sem er í skipuritinu.

### <a name="identify-the-report-in-a-reporting-tree"></a>Auðkenna skýrsluna í skipuritinu

1. Opnið skilgreiningu skipuritsins í Skýrsluhönnun til að gera breytingar.
2. Hólfin í dálkinum **Línuskilgreiningar** birta upplýsingar byggðar á upplýsingum um valda línu, vegna þess að nota verður sömu línuskilgreiningu í öllum einingum skipuritsins. Tvísmellið á hólfið **Línuskilgreiningar** og veljið línuskilgreininguna sem inniheldur upplýsingar um skýrsluna.
3. Í hólfinu **Vinnublaðstengill** fyrir eining skipurits, skal velja heiti tengilsins sem samsvarar skýrslunni.
4. Í hólfinu **Vinnubókar- eða skýrsluslóð** fyrir eining skipurits, er slegið inn heiti skýrslunnar eða flett til að velja skýrsluna.
5. Til að tilgreina vinnublaðs í skýrslu, sláið inn nafn vinnublaðs í á **vinnublaðsheiti** hólf.
6. Endurtakið skref 3 til 5 fyrir hverja eining skipurits sem á að fá gögn úr skýrslu. Til að koma í veg fyrir að röng gögn birtist í skýrslunni þarf að tryggja að rétt skýrsluheiti birtist í samsvarandi einingu í skipuritinu

## <a name="examples"></a>Dæmi
### <a name="reporting-unit-structure--example-1"></a>Uppbygging einingar skipurits - dæmi 1

Hér er Uppbygging einingar skipurits í eftirfarandi skipuriti:

- Eining skipurits fyrir Contoso Japan er yfireining sölu fyrir Contoso Japan og undireiningar Contoso Japan ráðgjöf.
- Eining söludeildar Contoso Japan er bæði undireining einingarinnar Contoso Japan, og yfireining fyrir einingarnar Home Sales og Auto Sales.
- Eining skipurits á læsta upplýsingastigi (Home Sales, Auto Sales, Client Services, og Operations) stendur fyrir deildir í fjárhagsgögnunum. Þessar einingar skipuritsins eru í skyggða svæðinu í skipuritinu.
- Samantektareiningar á hærri stigum taka saman upplýsingar frá upplýsingaeiningum.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Uppbygging einingar skipurits - dæmi 2

Eftirfarandi skipurit sýnir skipurit sem er með uppbyggingu fyrirtækis sem er skipt niður í viðskiptaaðgerðir.

[![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Dæmi um Setja inn einingar skipurits úr víddum svarglugga

Eftirfarandi mynd sýnir dæmi um **Setja inn einingar skipurits úr víddum** svarglugga. Í þessu dæmi skila niðurstöður samsetning viðskiptaeiningar, kostnaðarstaði og deildir.

[![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png)

skipuritsskilgreining sem verður til er raðað eftir viðskiptaeining, og svo eftir kostnaðarstað og svo eftir deild. Vídd fyrir fimmtu eining skipurits er **Viðskiptaeining = \[001\], Kostnaðarstaður =\[\], Deild = \[022\]** og auðkennir eining skipurits fyrir lykla sem tengjast viðskiptaeiningu 001 og deild 022.

[![Skipurit](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Dæmi um samantekt gagna

Eftirfarandi dæmi sýna mögulegar upplýsingar sem eru notaðar í skipuritsskilgreining sem dæmi um það hvernig á að taka saman gögn.

#### <a name="example-1"></a>Dæmi 1

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Dæmi 2

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Fjárhagsskýrslugerð](financial-reporting-intro.md)
