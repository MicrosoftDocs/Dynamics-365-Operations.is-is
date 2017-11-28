---
title: "Dálkaskilgreiningar í Fjárhagsskýrslum"
description: "Þessi grein veitir upplýsingar um skýrsluskilgreiningar. Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu. Eins og línuskilgreiningar, grunnur dálkaskilgreiningar má nota á mörg skýrslum."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8c877a4ad6d4c29607159da52bf1cedae1476f92
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="column-definitions-in-financial-reports"></a>Dálkaskilgreiningar í Fjárhagsskýrslum

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um skýrsluskilgreiningar. Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu. Eins og línuskilgreiningar, grunnur dálkaskilgreiningar má nota á mörg skýrslum.

<a name="create-and-modify-a-column-definition"></a>Dálkskilgreining stofnuð og henni breytt
-------------------------------------

Dálkskilgreining getur innihaldið tvo til 255 dálka.

### <a name="create-a-column-definition"></a>Dálkskilgreining stofnuð

1.  Í Skýrsluhönnun, smellið á **Dálkskilgreiningar** á yfirlitssvæðinu.
2.  Á valmyndinni **Skrá** er smellt á **Nýtt** og svo á **dálkskilgreining**.
3.  Bæta við efni dálkskilgreiningar.

### <a name="open-a-column-definition"></a>Dálkskilgreining opnuð

1.  Í Skýrsluhönnun, smellið á **Dálkskilgreiningar** á yfirlitssvæðinu.
2.  Tvísmellið á skýrsluskilgreiningu til að opna hana.

### <a name="add-a-column-to-a-column-definition"></a>Dálki bætt við dálkskilgreiningu

1.  Smellið á **Dálkskilgreiningar** í Skýrsluhönnun og opnið síðan dálkskilgreininguna sem á að breyta.
2.  Veljið dálk þar sem setja á inn nýjan dálk.
3.  Á valmyndinni **Breyta** er smellt á **Setja inn dálk**. Nýi dálkurinn birtist vinstra megin við dálkinn sem var valinn.

### <a name="delete-a-column-from-a-column-definition"></a>Dálki eytt úr dálkskilgreiningu

1.  Smellið á **Dálkskilgreiningar** í Report Designer og opnið síðan dálkskilgreininguna sem á að breyta.
2.  Veljið dálkinn sem á að eyða.
3.  Á valmyndinni **Breyta** er smellt á **Eyða dálki**.

## <a name="contents-of-a-column-definition"></a>Innihald dálkskilgreiningar
Dálkskilgreining inniheldur eftirfarandi upplýsingar:

-   Dálkur lýsingar fyrir línuskilgreiningunni.
-   Upphæðardálka sem birta gögn úr fjárhagsgögnum, Microsoft Excel-Vinnublað eða útreikningi annarra gagna í dálkskilgreiningunni.
-   Sniðdálkar
-   Eigindadálka.

Þessar upplýsingar birtast í eftirfarandi tveimur svæðum í dálkskilgreiningunni:

-   Fyrirsagnasvæði dálkskilgreiningarinnar inniheldur fyrirsagnatextann og sniðið sem birtist í skýrslunni. Fyrirsögn getur átt við stakan gagnadálk, náð yfir marga dálka eða átt við dálka út frá ákveðnum skilyrðum. Dálkskilgreiningin getur innihaldið eins margar dálkfyrirsagnalínur og þörf er á. **Ábending:** Dálkfyrirsagnir eiga við um hvern gagnadálk í skýrslunni. Skýrsluhausar eiga við um alla skýrsluna. Skilgreinið skýrsluhausa á flipanum **Hausar og fætur** í skýrsluskilgreiningunni.
-   Dálkupplýsingalínur eru línurnar undir fyrirsagnalínunum í dálkskilgreiningunni. Dálkupplýsingalínur skilgreina upplýsingarnar sem teknar eru með í skýrslunni. Eftirfarandi tafla birtir og lýsir dálkupplýsingalínunum.

    | Heiti dálkupplýsingalínu                                                | Lýsing                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Gerð dálks                                                           | (Áskilið) Tilgreinir tegund gagna í dálkinum.                                                     |
    | Bókarkóði/Eigindaflokkur                                          | Tilgreinir fjárhagsgagnaupplýsingar fyrir dálktegundirnar **FD** og **ATTR**.                       |
    | Tímabil Fjárhagsárs þakinna tímabila                                    | Tilgreinir fjárhagsgagnaupplýsingar fyrir dálktegundirnar **FD**.                                     |
    | Formúla                                                               | Tilgreina reikniformúlu fyrir dálka af á **CALC** gerð.                                        |
    | Dálkabreidd Aukalegra Bila áður En Dálksnið Hnekkja Prentstjórnun | Tilgreinið sérstaka sniðvalkosti.                                                                        |
    | Dálktakmarkanir                                                   | Takmarkar gögn.                                                                                         |
    | Eining skipurits                                                        | Takmarkar dálkinn þannig að hann sýni einungis gögn fyrir tilgreinda einingu skipurits.                      |
    | Gjaldmiðilssíun Birtingarmyndar gjaldmiðils                                      | Sníðið gjaldmiðil.                                                                                       |
    | Víddarafmörkun                                                      | Tilgreinir afmörkun til að takmarka gögn við tilteknar fjárhagsgagnaeiningar skipurits.                           |
    | Afmörkun eiginda                                                      | Tilgreinir afmörkun til að takmarka fjárhagsgögnin.                                                       |
    | Upphafsdagur lokadagur                                                   | Takmarkið fjárhagsgögnin við tilteknar dagsetningar.                                                         |
    | Jöfnun                                                         | Vinstri jafnar, mið jafnar, eða hægri jafnar lýsingartextann sem tilgreindur er í línuskilgreiningunni. |

## <a name="column-restrictions-in-a-column-definition"></a>Dálktakmarkanir í dálkskilgreiningu
Hægt er að nota dálktakmarkanir til að tilgreina hvernig dálkskilgreining notar gögn eða reiknar upplýsingar. Einnig er hægt að takmarka skýrsludálk við tiltekna einingu eða fyrir tilteknar dagsetningar. **Ábending:** Kóði af gerðinni **Dálktakmarkanir** hnekkir öllum stillingum sem rekast á og hefur verið úthlutað í línuskilgreiningunni.

### <a name="column-restrictions-cell"></a>Hólf dálktakmarkana

Hólfið **Dálktakmarkanir** getur innihaldið kóða sem takmarka eða fela upplýsingar, svo sem línusnið, ítarupplýsingar og upphæðir, fyrir þann dálk.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Dálktakmörkun bætt við dálkskilgreiningu

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellt er á hólfið **Dálktakmarkanir** fyrir þann dálk sem á að takmarka.
3.  Í svarglugganum **Dálktakmarkanir** er einn eða fleiri kóðar valdir af listanum og því næst smellt á **Í lagi**.

### <a name="column-restriction-codes"></a>Dálktakmörkunarkóðar

Eftirfarandi tafla lýsir kóðum dálktakmarkana.

| Dálktakmörkunarkóði | Lýsing                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Felur undirstrikun í dálki þar sem skipun um annað hvort undirstrikun ( **---**) eða tvöföld undirstrikunarskipun (**===**) hefur verið færð inn í línuskilgreininguna. Til dæmis getur verið að ekki sé æskilegt að hafa strik undir upphæðum sem eru búið til af hlutfallsútreikningi.                                                                        |
| ST                      | Fela samtölur, þannig að aðeins upplýsingar birtast í dálknum (t.d. tölfræðilega dálk).                                                                                                                                                                                                                                      |
| SD                      | Felur ítarupplýsingar og birtir aðeins **TOT**- og **CAL**-línur, úr línuskilgreiningunni, í þessum dálki.                                                                                                                                                                                                                              |
| DR                      | Takmarkar upphæðirnar sem birtar eru í **FD**-dálki við debetupphæðir.                                                                                                                                                                                                                                                                              |
| CR                      | Takmarkar upphæðirnar sem birtar eru í **FD**-dálki við kreditupphæðir.                                                                                                                                                                                                                                                                             |
| ADJ                     | Takmarkar upphæðirnar sem birtar eru í dálkinum við upphæðir tímabilsleiðréttinga, ef þessar upphæðir eru til staðar.                                                                                                                                                                                                                                        |
| XAD                     | Takmarkar upphæðirnar sem birtar eru í dálkinum svo upphæðir tímabilsleiðréttinga sé sleppt.                                                                                                                                                                                                                                                     |
| PT                      | Takmarkar upphæðirnar sem birtar eru í dálkinum svo aðeins bókaðar færslur séu hafðar með, ef þessar færslur eru til staðar.                                                                                                                                                                                                                 |
| UPT                     | Takmarkar upphæðirnar sem birtar eru í dálkinum svo aðeins óbókaðar færslur séu hafðar með, ef þessar færslur eru til staðar. **Ábending:** Sumar gagnaveitur styðja ekki óbókaðar færslur. Frekari upplýsingar eru í [leiðbeiningum um samþættingu gagna](http://go.microsoft.com/fwlink/?LinkID=162565) fyrir Microsoft Dynamics ERP kerfið. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>dálkur takmarkaður við einingu skipurits

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á hólfið **Eining skipurits** til að takmarka dálkinn.
3.  Í svarglugganum **Einingaval skipurits** skal velja skipurit af listanum **Skipurit**.
4.  Stækkið eða fellið saman listann yfir einingar og veljið svo einingu skipurits og smellið á **Í lagi**.

## <a name="format-column-headers"></a>Dálkfyrirsagnir sniða
Hægt er að bæta við, breyta og eyða hausum sem birtast efst í dálkum í skýrslu. Einnig er hægt að grunnstilla dálkfyrirsagnir með skilyrt umfang samkvæmt reitnum **Tímabil** úr dálkskilgreiningum, og í reitnum **Grunntímabil**, úr skýrsluskilgreiningum. Grunntímabil er eiginleiki sem sparar tíma fyrir stofnun hlaupandi spáskýrslna.

### <a name="create-and-manage-column-headers"></a>Stofna og stjórna dálkahausum

Hægt er nota **dálkfyrirsögn** svarglugga til að bæta við, breyta og eyða hausum sem birtast efst í dálkum í skýrslu. **dálkfyrirsögn** svarglugginn inniheldur reitina sem lýst er í eftirfarandi töflu.

| Reitur                 | Lýsing                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Texti dálkfyrirsagnar    | Þessi texti birtist í dálkfyrirsögninni. Hægt er að færa textann beint inn í kassann eða smella á **Setja inn sjálfvirkan texta** til að velja að uppfæra dálkfyrirsögnina í hvert skipti sem skýrsla er mynduð. Til að setja inn marga sjálfvirka textakóða er smellt aftur á **Setja inn sjálfvirkan texta** og svo smellt á annan kóða á listanum. |
| Sniðvalkostir        | Nota sérsnið fyrir dálkfyrirsögn, t.d. kassa eða undirstrikun.                                                                                                                                                                                                                                                           |
| Byrjar á og Endar á | Tilgreinir dálkinn eða dálkana sem texti fyrirsagnarinnar tilheyrir.                                                                                                                                                                                                                                                            |
| Jöfnun         | Tilgreinir hvernig Texti dálkfyrirsagnar er jafnaður með tilliti til dálksins eða dálkanna sem tilgreindir eru í kössunum **Byrjar á** og **Endar á**.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Dálkfyrirsögn stofnuð

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á fyrirsagnarhólf.
3.  Í svarglugganum **Dálkfyrirsögn** skal færa inn texta dálkfyrirsagnarinnar. Annar valkostur er að smella á **Setja inn sjálfvirkan texta** og velja valkost.
4.  Veljið sniðstíl fyrir fyrirsögnina í reitnum **Sniðvalkostir**.
5.  Færið staf dálksins sem dálkfyrirsögnin á að byrja á yfir í reitinn **Byrjar á**. Færið staf dálksins sem dálkfyrirsögnin á að enda á yfir í reitinn **Endar á**.
6.  Undir **Jöfnun** skal velja hvort texti dálkfyrirsagnarinnar skal vera vinstri-, hægri- eða miðjujafnaður.
7.  Smelltu á **Í lagi**.

### <a name="add-a-column-header-row"></a>Línu fyrir dálkfyrirsögn bætt við

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Veljið hólf í fyrirsagnarlínunni.
3.  Á valmyndinni **Breyta** er smellt á **Setja inn línu**. Nýja línan er sett inn fyrir ofan línuna sem valin var í skrefi 2. **Ábending:** Ef skýrsla hefur fjórar eða fleiri línur sem innihalda fyrirsagnir munu fyrirsagnirnar skarast þegar skýrslan er flutt út í Excel-vinnublað. Til að skoða allar fyrirsagnir Á skýrslunni þarf að stækka efri spássíuna í skýrsluskilgreiningunni.

### <a name="delete-a-column-header-row"></a>Línu fyrir dálkfyrirsögn eytt

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Veljið hólf í fyrirsagnarlínunni til að eyða.
3.  Á valmyndinni **Breyta** er smellt á **Eyða línu**.

### <a name="create-an-automatically-generated-header"></a>Stofna sjálfvirkt myndaðan haus

Report Designer getur sjálfkrafa myndað dálkhausa byggða á kóðum sjálfvirks texta. Sjálfvirkir textakóðar eru breytur sem eru uppfærðar í hvert sinn sem skýrsla er mynduð. Allar dálkfyrirsagnir geta innihaldið þessa kóða til að tilgreina upplýsingar skýrslu sem geta verið mismunandi, á borð við dagsetningu eða tímabilsnúmer. Þess vegna er hægt að nota eina dálkskilgreiningu fyrir margar skýrsluskilgreiningar, tímabil og skipurit. Þar sem sjálfvirkur texti kóða notast við dagatalsupplýsingar úr hlutanum Upplýsingar í dálkskilgreiningu, eru þeir aðeins studdir fyrir dálkana **CALC**, **FD**, og **WKS** dálkana. Hvernig sjálfvirkur textakóði birtist í dálkfyrirsagnarhólfinu hefur áhrif á hvernig þær upplýsingar birtast í skýrslunni. Í svarglugganum **Dálkfyrirsögn** birtast sjálfvirku textakóðarnir með blöndu há- og lágstafa. Þess vegna er textinn sem birtist há- og lágstafa í skýrslunni. Á hefðbundnu almanaksári leysir **@CalMonthLong** úr mánuði **7** sem **júlí**. Ef heiti mánaðar á að vera með hástöfum í skýrslunni, s.s. **JÚLÍ**, er sjálfvirkur textakóði sleginn inn með hástöfum í reitinn **Texti dálkfyrirsagnar**. Til dæmis: Færið inn **@CALMONTHLONG**. Hægt er að nota kóða með texta. Til dæmis færirðu inn eftirfarandi fyrirsagnartexta: **Tímabil @FiscalPeriod-@FiscalYear frá @StartDate til @EndDate**. Fyrirsögn skýrslu sem er mynduð svipar eftirfarandi texta: **Tímabil 1-02 frá 01/01/02 til 31/01/02**. **Ábending:** Sniðið á sumum texta, svo sem löngum dagsetningum, fer eftir svæðisstillingunum sem eru valdar á Finance and Operations-þjóninum. Til að breyta þessum stillingum er smellt á **Ræsa** hnappinn, **Stjórnborð** valið og smellt á **Svæðisbundnir valkostir og tungumálavalkostir**. Eftirfarandi tafla inniheldur tiltækan sjálfvirkan texta fyrir dálkfyrirsagnir.

| Valkostir sjálfvirks texta og kóði                | lýsing                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mánaðarheiti (@CalMonthLong)              | Prentar heiti gildandi mánaðar í dálkfyrirsögnina. Ef ákveðið er að slétta upphæðirnar í skýrslunni að þúsundum, milljónum eða milljörðum eða ef dálkbreidd í skýrslunni er stillt á færri en níu stafi er mánaðarheitið stytt niður í fyrstu þrjá stafina. |
| Stytt mánaðarheiti (@CalMonthShort) | Prenta skammstafað heiti mánaðarins fyrir valið fjárhagstímabil.                                                                                                                                                                                                                          |
| Tímabilsnúmer (@FiscalPeriod)           | Prenta tölulega skjámyndina fjárhagstímabilsins sem er skilgreind fyrir þann dálk. Ef dálkurinn nær yfir mörg tímabil, síðasta tímabil í afmörkun er prentuð.                                                                                                                                   |
| Lýsing á tímabili (@FiscalPeriodName)  | Prenta lýsingu fjárhagstímabils sem er skilgreind í fjárhagsleg gögn.                                                                                                                                                                                                                    |
| Fjárhagsár (@FiscalYear)               | Prentar fjárhagsár fyrir dálkinn á talnasniði.                                                                                                                                                                                                                                            |
| Almanaksár (@CalYear)                | Prentar almanaksár fyrir dálkinn á talnasniði.                                                                                                                                                                                                                                          |
| Upphafsdagur (@StartDate)                 | Prenta upphafsdagsetningu fyrir dálk.                                                                                                                                                                                                                                                             |
| Lokadagur (@EndDate)                     | Prenta Lokadagur fyrir dálk                                                                                                                                                                                                                                                               |
| Einingarnafn úr tré (@UnitName)         | Ef dálkur er takmarkaður við tiltekna einingu í skipuritinu er einingarheitið prentað í dálkfyrirsögninni.                                                                                                                                                                                     |
| Lýsing einingar (@UnitDesc)            | Ef dálkur er takmarkaður við tiltekna einingu í skipuritinu er einingarlýsingin prentuð í dálkfyrirsögninni.                                                                                                                                                                              |
| Bókarkóði (@BookCode)                   | Prentar bókarkóðann sem tilgreindur er í dálknum.                                                                                                                                                                                                                                             |
| Auða línu (@Blank)                     | Setur inn auða línu í dálkfyrirsögnina.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Stofnun fyrirsagnar með skilyrt umfang

Fyrirsagnir með skilyrt umfang geta náð yfir marga dálka, sem byggja á tilteknum tímabilsgögnum. Ef til dæmis er til fjárhagsáætlunarskýrsla fyrir fjárhagsárið og birta á raunfjárhagsáætlanir síðustu mánaða ásamt spá um fjárhagsáætlanir komandi mánaða, er hægt að nota fyrirsögn með skilyrt umfang til að uppfæra skýrslufyrirsögnina sjálfvirkt. Athugið eftirfarandi aðstæður þegar búin er til fyrirsögn með skilyrt umfang:

-   Ef stöðvunarskilyrði (reiturinn **Endar á**) er stemmt af á undan upphafskilyrði (reiturinn **Byrjar á**) er það hunsað. Til dæmis, dálkur B hefur skilyrði bils skilgreint sem BASE+1 til BASE og ef BASE er í dálk C og BASE+1 í dálk D, í því tilfelli er stöðvunarskilyrðið í dálk C hunsað og prentun fyrirsagna hefst í dálk D.
-   Ef tilgreindar er dálkfyrirsagnir sem skarast prentast þær út þannig í skýrslunni. Skýrslan er mynduð, en eftirfarandi viðvörun birtist í **Biðraðarstaða skýrslu**: „Dálkfyrirsagnir sem nota BASE skarast við aðrar dálkfyrirsagnir og geta valdið því að texti skarist.“ Í þessu tilfelli er fyrirsagnarskilgreiningin í dálk B er B til BASE+1 og fyrirsagnarskilgreiningin í dálk D er BASE+1 til F, eru fyrirsagnirnar prentaðar hvor ofan í aðra og eru ólæsilegar. Þegar BASE er notað í **Byrjar á/Endar á** skilgreiningu skal passa að skoða skýrsluna sem var mynduð til að sjá hvort fyrirsagnirnar skarast.
-   Ef BASE er tilgreint í skilgreiningunni í dálk sem ekki á að prenta (**NP**) er það hunsað, án tillits til þess sem skilgreint er í dálkskilgreiningunni. Í raun eru þessar aðstæður það sama og að búa ekki til skilgreiningu dálkfyrirsagnar.
-   Fyrir skilyrta prentunardálka (**P&lt;B**, **P&gt;=B**) haga fyrirsagnir með skilyrt umföng sér eins og hver önnur skilgreining dálkfyrirsagnar. Til dæmis ef skilyrðið er til dæmis rangt, munu allir síðari dálkar sem samsvara bilskilyrðinu hefja fyrirsagnarprentun.

#### <a name="create-a-conditional-spanning-header"></a>Stofnun fyrirsagnar með skilyrt umfang

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á fyrirsagnarhólf.
3.  Í svarglugganum **Dálkfyrirsögn** skal færa inn texta dálkfyrirsagnarinnar. Annar valkostur er að smella á **Setja inn sjálfvirkan texta** og velja valkost.
4.   Veljið sniðstíl fyrir fyrirsögnina í reitnum **Sniðvalkostir**.
5.  Tilgreinið tímabil í samræmi við grunntímabilið sem tilgreint er þegar skýrslan er mynduð. færa skal inn einn af eftirfarandi valkostum í reitina **Byrjar á** og **Endar á**: **BASE**, **BASE-X** eða **BASE+X**, þar sem X táknar fjölda tímabila úr grunntímabilinu. Til dæmis ef slegið er inn **BASE** í reitinn **Byrjar á** byrjar texti skilyrts umfangs dálkfyrirsagnarinnar í dálkfyrirsögninni þar sem skýrsluskilgreiningin **Grunntímabil** er sama og dálkskilgreining gildi **Tímabils** Hún endar í dálkinn sem er tilgreint í á **Enda á** svæði. Þannig að ef bilið er BASE til M og skýrsluskilgreingin **Grunntímabil** = **4** hefst fyrirsögnin frá og með dálknum með tímabilið stillt á **4** og endar með dálknum M. Hausar stöðvast og hefjast við prentun dálka eingöngu.
6.  Undir **Jöfnun** skal velja hvort texti dálkfyrirsagnarinnar skal vera vinstri-, hægri- eða miðjujafnaður.
7.  Smelltu á **Í lagi**.

#### <a name="example-of-a-conditional-spanning-header"></a>Dæmi um fyrirsögn með skilyrt umfang

Pála er að búa til skýrslu fyrir sex mánaða spá. Hún vill að orðið Raunverulegt verði prentað fyrir ofan dálkana sem innihalda raungögn og að orðið Fjárhagsáætlun verði prentað fyrir ofan dálkana sem innihalda fjárhagsáætlunarspár. Í hverjum mánuði sem skýrslan er keyrð bætist við einn dálkur með fyrirsögnina Raunverulegt og fækkar um einn dálk með fyrirsögnina Fjárhagsáætlun. Hinsvegar, Pála getur breytt dálkskilgreiningunni handvirkt í hvert skipti sem skýrslan er mynduð til að aðlaga fyrirsagnirnar, hún ákveður að spara tíma og fyrirhöfn, hún ákveður að búa til fyrirsagnir með skilyrt umfang sem munu sjálfkrafa búa til fyrirsagnir yfir viðeigandi dálka í hvert skipti sem skýrslan er keyrð. Pála opnar Skýrsluhönnun, smellir á **Dálkskilgreining** í yfirlitssvæðinu og opnar dálkskilgreininguna fyrir skýrsluna. Hún færir síðan inn eftirfarandi upplýsingar. Grunntímabilið í skýrsluskilgreiningunni er 4.

|                     | Lista fyrir    | B             | K             | D             | E             | F             | G             | H             | I             | J             | K             | L             | M             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Haus 1            |      | Raunþyngd        | Fjárhagsáætlun        |               |               |               |               |               |               |               |               |               |               |
| Fyrirsögn 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Fyrirsögn 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Gerð dálks         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Bókarkóði/Eigind |      | ACTUAL        | Fjárhagsáætlun2012    | ACTUAL        | Fjárhagsáætlun2012    | ACTUAL        | Fjárhagsáætlun2012    | ACTUAL        | Fjárhagsáætlun2012    | ACTUAL        | Fjárhagsáætlun2012    | ACTUAL        | Fjárhagsáætlun2012    |
| Fjárhagsár         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Tímabil              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Tímabil sem er tekið með     |      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      |
| Dálkbreidd        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Prentstýringar       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Pála tvísmellir á dálkfyrirsagnarhólf til að opna svargluggann **Dálkfyrirsögn** þar sem hún færir inn eftirfarandi upplýsingar.

| Reitur              | Gildi                 |
|--------------------|-----------------------|
| Texti dálkfyrirsagnar | Rauntölur                |
| Setja inn sjálfvirkan texta    | Ekkert er valið |
| Sniðvalkostir     | Reitur                   |
| Jöfnun      | Ekkert er valið |
| Byrjar á        | B                     |
| Endar á          | BASE                  |
| Fyrirsögn fjárhagsáætlunar      | BASE+1 í lokadálk  |

Eftir að hún hefur lokið að færa inn upplýsingar, Pála smellir á **Í lagi**. Hún tvísmellir svo á dálkfyrirsagnarhólfið í dálk C til að opna svargluggann **Dálkfyrirsögn** þar sem hún færir inn eftirfarandi upplýsingar.

| Reitur              | Gildi                 |
|--------------------|-----------------------|
| Texti dálkfyrirsagnar | Fjárhagsáætlun                |
| Setja inn sjálfvirkan texta    | Ekkert er valið |
| Sniðvalkostir     | Reitur                   |
| Jöfnun      | Ekkert er valið |
| Byrjar á        | C                     |
| Endar á          | BASE+2                |

Í hvert skipti sem skýrsla er mynduð mun orðið Raunverulegt vera prentað fyrir ofan dálkana sem innihalda raungögn og að orðið Fjárhagsáætlun verði prentað fyrir ofan dálkana sem innihalda fjárhagsáætlunarspár. Þar að auki, fjölda dálka verður leiðréttir hvern mánuð.

## <a name="apply-column-justification"></a>Dálkar jafnaðir
Hólfið **Jöfnun** er notað til að jafna lýsingardálk í skýrslu. Þessi valkostur hefur einungis áhrif á dálklýsingar, ekki sjálf gildin.

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á hólfið **Jöfnun**.
3.  veljið eitt eftirfarandi gilda í listanum.
    -   **Ekkert** – Engin jöfnun er notuð.
    -   **Vinstri** – Dálklýsingar eru vinstristilltar.
    -   **Miðja** – Dálklýsingar eru miðjustilltar.
    -   **Hægri** – Dálklýsingar eru hægristilltar.

## <a name="add-special-formatting-options"></a>Sérstökum sniðvalkostum bætt við
Í dálkskilgreiningunni eru upplýsingalínur sniðdálksins notaðar til að nota sérstakt snið á valda dálka. Þótt sumir valkostir í **Stilling fyrir prentun** og **Dálktakmarkanir** eigi bara við **FD**-dálka eiga flestir valkostir við allar dálktegundir. Þetta snið hnekkir sniðinu sem er tilgreint í dálkskilgreiningunni og skýrsluskilgreiningunni. Hinsvegar, Þetta snið hnekkir sniðinu sem er tilgreint í línuskilgreiningunni og dálkaskilgreiningunni. Eftirfarandi línur flokkast sem sniðlínur:

-   Dálkbreidd
-   Aukabil á undan dálki
-   Hnekking sniðs/gjaldmiðils
-   Stilling fyrir prentun

### <a name="changing-the-column-width"></a>Dálkbreidd breytt

Hólfið **Dálkbreidd** tilgreinir hversu marga stafi er hægt að nota yfir breidd þessa dálks á prentaðri skýrslu. Dálkbreidd er sérstaklega mikilvæg fyrir dálka sem innihalda upphæðir (dálkgerð **CALC**, **WKS** eða **FD**), lýsingar (dálkgerð **DESC**) eða fyllingu (dálkagerð **FILL**). Að sjálfgefnu er **AutoFit** valkostur valinn, þannig að breidd hver dálkur er sjálfvirkt leiðrétt til að passa innihaldi.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Breidd dálks í skýrslu tilgreind

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Í hólfið **Dálkbreidd** er færður inn fjöldi bila fyrir breidd dálksins. Hámarksbreidd allra dálka er 255 stafir (þetta númer inniheldur sent, kommur, og sviga). Til að virkja Report Designer á að velja viðeigandi breidd fyrir dálk, á grunni innihalds hólfs er, tvísmellt á hólfið **Dálkbreidd** og svo smellt á **AutoFit**.

### <a name="add-space-between-columns"></a>Bæta við bili milli dálka

Hólfið **Aukabil á undan dálki** tilgreinir breidd skila á milli eins dálks og samliggjandi dálka í dálkskilgreiningu. Stillingin **Aukabil á undan dálki** virkar á allar dálkupplýsingalínur, en ekki dálkfyrirsagnarlínur, í þessum dálki. Þessi valkostur er notaður til að aðskilja dálkahópa eða til að bæta við nokkrum bilum á undan lýsingunni til að draga lýsingardálkinn inn frá vinstristilltum fyrirsögnum í skýrslunni. Sjálfgefinn fjöldi bila á milli dálka er tvö. Hægt er að breyta þessu **Stillingar** á flipanum í skýrsluskilgreiningunni.

#### <a name="specify-the-space-between-columns"></a>Bil milli dálka skilgreint

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Í hólfið **Aukabil á undan dálki** er færður inn fjöldi bila fyrir breidd dálksins.

### <a name="specify-a-currency"></a>Tilgreina gjaldmiðil

Hólfið **Hnekking sniðs/gjaldmiðils** tilgreinir snið tugabrota-, gjaldmiðils- og prósentuupphæða í þessum dálki. Þetta snið hnekkir því sniði sem tilgreint er í skýrsluskilgreiningu eða sjálfgefnum stillingum kerfis.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Hnekkingu á gjaldmiðilssniði úthlutað á skýrsludálk

1.  Opnið dálkskilgreiningu í Report Designer til að gera breytingar.
2.  Tvísmellið á hólfið **Hnekking sniðs/gjaldmiðils** í upphæðardálki.
3.  Snið er valið í svarglugganum **Hnekkja sniði**.

### <a name="add-a-print-control-code"></a>Bæta við kóða fyrir stillingu prentunar

Hólfið **Stilling fyrir prentun** inniheldur kóða sem stilla birtingar- eða prentunareiginleika dálks. Hægt er að velja um tvo mismunandi prentstjórnunarkóðar: venjulegar stillingar fyrir prentun og kóða fyrir skilyrtar stillingar fyrir prentun.

#### <a name="regular-print-control-codes"></a>Kóðar fyrir venjulega stillingu fyrir prentun

| Kóði fyrir stillingu prentunar | Þýðing                                     | Lýsing                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Ekki til prentunar                                     | Útilokar upphæðir í þessum dálki frá skýrslunni sem er prentuð og frá útreikningum. Til að taka dálk sem ekki er til prentunar með í útreikningi er vísað beint til dálksins í útreikningsformúlunni. Til dæmis er dálkur C, sem ekki er ætlaður til prentunar, tekinn með í eftirfarandi útreikningi: **B+C+D**. Hins vegar er dálkur C, sem ekki er ætlaður til prentunar, ekki tekinn með í eftirfarandi útreikningi: **B:D**.                                                                                                                                          |
| XCR                | Tákni breytt ef dæmigerð staða línunnar er kredit | Stofnar fjárhagsáætlun eða samanburðarskýrslu þar sem óæskileg frávik (t.d. tekjutap eða framúrkeyrsla í kostnaði) er alltaf neikvæð. Nota þessi kóði til að breyta tákni **CALC**-dálksupphæðar ef dæmigerð staða tiltekinnar línu er kredit (táknað með **C** í dálkinum **Eðlileg staða** í línuskilgreiningunni). **Athugið:** Fyr **TOT** línur og **CAL** línur sem yfirleitt eru með kreditstöðu, skal slá inn **C** í dálkinn **Eðlileg staða** í línuskilgreininguna. |
| X0                 | Dálkur falinn ef hann inniheldur bara núll eða eyður          | Útilokar **FD**-dálk frá skýrslunni ef öll hólf í þeim dálki eru annaðhvort tóm eða innihalda núll.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Sléttun falin                               | Kemur í veg fyrir að upphæðirnar í þessum dálki séu sléttaðar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Samantekt falin                                 | Felur samantekt. Ef notað er skipurit í skýrslunni eru upphæðirnar í þessari dálkur ekki teknar saman í yfirhnútum sem á eftir koma.                                                                                                                                                                                                                                                                                                                                                                                                   |
| LG                 | Dálkur endurtekinn á hverri síðu                      | Endurtekur tiltekinn dálk á hverri síðu skýrslu. Til dæmis er hægt að nota **RP** prentstýringarkóða til að taka með dálkategundina **ROW** sem tekur inn línukóða á hverri síðu.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Orðskrið                                      |  Ef texti í dálki er of langur er hægt að nota þennan valkost til að koma textanum fyrir í dálkinum.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Kóðar fyrir skilyrtar stillingar fyrir prentun

| Kóðar fyrir skilyrtar stillingar fyrir prentun | lýsing                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (ekkert)                         | Hreinsar skilyrta prentvalið.                                                  |
| P&lt;B                         | Birtir tiltekinn dálk aðeins ef tímabilið er minna en grunntímabilið.             |
| P&gt;B                         | Birtir tiltekinn dálk aðeins ef tímabilið er meira en grunntímabilið.             |
| P=B                            | Birtir tiltekinn dálk aðeins ef tímabilið er jafnt og grunntímabilið.              |
| P&lt;=B                        | Birtir tiltekinn dálk aðeins ef tímabilið er minna en eða jafnt og grunntímabilið. |
| P&gt;=B                        | Birtir tiltekinn dálk aðeins ef tímabilið er meira en eða jafnt og grunntímabilið. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Kóða stillingar fyrir prentun bætt við skýrsludálk

1.  Opnið dálkskilgreiningu í Report Designer til að gera breytingar.
2.  Tvísmellið á hólfið **Stilling fyrir prentun**.
3.  Í svarglugganum **Stilling fyrir prentun** er valinn kóði af listanum **Velja stillingarvalkosti prentunar**. Ef velja á fleiri en einn kóða skal halda niðri CTRL-takkanum um leið og kóðarnir eru valdir.
4.  Veljið valkost í reitnum **Skilyrtir prentvalkostir**. **(ekkert)** er sjálfgefið valið. Aðeins er hægt að velja einn skilyrtan prentkóða í einu.
5.  Smellið á **Í lagi**.

> [!TIP]
> Einnig er hægt að slá prentkóðana beint inn í reitinn **Prentstýringar**. Aðskiljið marga stillingakóða fyrir prentun með kommum.


## <a name="column-types"></a>Gerðir dálka
Tegund upplýsinganna sem kemur fram í hverjum dálki í skýrslu er tilgreindur með gildinu í línunni **Dálkgerð** í dálkskilgreiningunni. Hver dálkskilgreining verður að innihalda að minnsta kosti einn lýsingardálk (**DESC**) og einn upphæðardálk (**FD**, **WKS** eða **CALC**). **Ábending:** Kóðarnir fyrir Dálkategund eiga ekki við fyrir öll bókhaldskerfi. Ef valin er tegund sem er ekki gild fyrir viðeigandi bókhaldskerfi birtist sá dálkur auður í skýrslunni.

### <a name="specify-a-column-type"></a>Dálkategundir tilgreindar

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á hólf í línunni **Dálkategund** í viðeigandi dálki.
3.  Veljið dálkategund úr listanum. Eftirfarandi tafla lýsir mismunandi dálkagerðum.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Dálkategundarkóði</th>
    <th>Lýsing</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Sýna fjárhagsgögn eða gögn úr Excel-vinnublaði þegar notast er við dálkinn <strong>Tengill í fjárhagsvíddir</strong> eða dálkinn <strong>Tengill í vinnublað</strong> í línuskilgreiningum. Þegar dálkategundin <strong>FD</strong> er valin eru sjálfgefnar stillingar sjálfkrafa tilgreindar í eftirfarandi línum: <ul>
    <li><strong>Bókarkóði/Eigindaflokkur:</strong> – ACTUAL</li>
    <li><strong>Bókarkóði/Eigindaflokkur:</strong> – ACTUAL</li>
    <li><strong>Fjárhagsár:</strong> – BASE</li>
    <li><strong>Tímabil:</strong> – BASE</li>
    <li><strong>Tímabil sem er tekið með:</strong> – PERIODIC</li>
    <li><strong>Dálkbreidd:</strong> 14</li>
    </ul>
Hægt er að breyta þessum sjálfgefnu stillingum.</td>
    </tr>
    <tr class="even">
    <td>CALC</td>
    <td>birta þær niðurstöður úr einföldum eða flóknum útreikningi sem tilgreindar eru í hólfinu <strong>Formúla</strong>. Fyrir meiri upplýsingar sjá <a href="advanced-formatting-options-financial-reporting.md">Ítarlegir sniðsvalkostir í fjárhagsskýrslugerð</a>.</td>
    </tr>
    <tr class="odd">
    <td>DESC</td>
    <td>Birta lýsingu línu úr línuskilgreiningunni. Þrátt fyrir að lýsingardálkur sé oft fyrsti dálkurinn í skýrslunni getur hann verið í hvaða stöðu sem er.</td>
    </tr>
    <tr class="even">
    <td>ROW</td>
    <td>birta sérstaka línukóða fyrir fjárhagslínur úr dálknum <strong>Línukóði</strong> í skilgreiningu línunnar. Frekari upplýsingar eru í <a href="row-definitions-financial-reporting.md">Línuskilgreining í fjárhagsskýrslugerð</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (reikningskóðar)</td>
    <td>birta fjárhagsleg hlutagildi eða víddargildi sem eiga við hverja línu. Fyrir upplýsingaskýrslur um reikninga og skýrslur um færsluupplýsingar er prentaður heildstæður reikningur, (t.d. <strong>110140-070-0101</strong>). Hafi svið verið tilgreind í dálknum <strong>Tengill í fjárhagsvíddir</strong> í tengdri línuskilgreiningu er sviðið haft í hornklofum og meðhöndlað líkt og það væri eitt stakt gildi (til dæmis, <strong>[110140:110700]-070-[0101:0200]</strong>). Fjárhagsgagnatengillinn úr línuskilgreiningunni er prentaður fyrir fjárhagsskýrslur og efra-stigs skýrslur sem eru samsetning úr nokkrum reikningum, til dæmis <strong>1100:1200</strong>.</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>fylla inn í hólf með staf sem er hafður innan einfaldra gæsalappa. Sé ekki sleginn inn stafur er dálkurinn auður. Til dæmis til að fylla í dálk með úrfellingarmerki (...) er slegið inn <strong>FILL</strong><strong>'.'</strong>.</td>
    </tr>
    <tr class="odd">
    <td>PAGE</td>
    <td>setja inn lóðrétt síðuskil í skýrsluna. Dálkarnir sem eru til hægri við dálkinn <strong>PAGE</strong> birtast á annarri síðu.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>birta gögn sem eru sótt úr Excel-vinnublað. Þegar dálkategundin <strong>WKS</strong> er valin eru sjálfgefnar stillingar sjálfkrafa tilgreindar í eftirfarandi línum: <ul>
    <li><strong>Fjárhagsár</strong> – PERIODIC</li>
    <li><strong>Tímabil:</strong> – BASE</li>
    </ul>
Hægt er að breyta þessum sjálfgefnu stillingum.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Ef bókhaldskerfið sem unnið er með styður notkun eiginda, birtu þá eigind reiknings eða eigind færslu í dálknum. Eigind, sem verður að eiga við stakan reikning, nær í undirliggjandi reiknings- eða færsluupplýsingar úr fjárhagsgögnunum. Eigindir á reikningsstigi birta gögn úr reikningnum og eigindir á færslusviði birta gögn sem komu fram á þeim tíma sem færslan var bókuð. Ef <strong>ATTR</strong> er valið sem dálkategund er eigindaflokkur tilgreindur í upplýsingalínunni <strong>Bókarkóði/Eigindaflokkur</strong> fyrir dálkskilgreininguna.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Dálkurinn Fjárhagsvíddir

Eftirfarandi **Dálkskilgreining** línu eiga við um dálk með dálkategundina **FD** (upphæðir úr fjárhagsvíddum).

#### <a name="book-codeattribute-category-cell"></a>Hólf bókarkóða/eigindategundar

Hólfið **Bókarkóði/Eigindaflokkur** auðkennir bókarkóðann fyrir gögnin í dálkinum **FD**. Dálkskilgreiningin getur falið í sér marga raun-, fjárhags- og tölfræðidálka. Dálkskilgreiningin getur einnig birt mismunandi tímabil, eins og yfirstandandi eða það sem af er ári, og mismunandi upphæðir. Listinn yfir bókarkóða endurspeglar raun-, fjárhags- og tölfræðivalkosti (ekki fjárhagslega) sem hefur verið komið á í fjárhagsgögnum notanda.

#### <a name="fiscal-year-cell"></a>Hólf fjárhagsárs

Hólfið **Fjárhagsár** auðkennir fjárhagsárið sem taka ætti með í dálkinum. Árið getur verið í samræmi við grunnárið sem tilgreint er þegar skýrslan er mynduð. Eftirtaldir valkostir eru í boði.

| Valkostur  | Lýsing                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASE    | Notið grunnárið sem tilgreint á tíma skýrslunnar.                                                                          |
| BASE+\# | Nota árið sem er \# ára eftir grunngögn ár. Ef til dæmis á að nota þriðja ár eftir grunnárið skal skrifa  **BASE+3**. |
| BASE-\# | Nota árið sem er \# ára á undan grunngögn ár. Ef til dæmis á að nota árið á undan, færðu inn **BASE-1**.                 |
| \#      | Færið skal inn raunverulegt fjárhagsár.                                                                                                |

#### <a name="period-cell"></a>Tímabilshólf

Hólfið **tímabil** auðkennir tímabilin sem taka ætti með í dálkinum. Tímabilið getur verið í samræmi við grunntímabilið sem tilgreint er þegar skýrslan er mynduð. Eftirtaldir valkostir eru í boði.

| Valkostur          | lýsing                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BASE            | Notar grunntímabilið.                                                                                                                                                                                                                 |
| BASE+\#         | Nota árið sem er \# tímabil eftir grunngögn tímabil. Ef til dæmis á að nota þriðja tímabil eftir grunntímabilið skal skrifa inn **BASE+3**.                                                                                               |
| BASE-\#         | Nota árið sem er \# tímabil eftir grunngögn tímabil. Ef til dæmis á að nota tímabilið á undan, færðu inn **BASE-1**.                                                                                                                 |
| BASE-\#:BASE    | Notar mörg tímabil frá mismunandi tímabilum fyrir grunntímabilinu og í gegnum grunntímabilið. Ef til dæmis á að nota þrjú fyrrverandi tímabil og grunntímabilið skal skrifa inn **BASE-3:BASE**.                                                |
| BASE:BASE+\#    | Notar mörg tímabil úr grunntímabili yfir fjölda tímabila á eftir grunntímabilinu. Ef til dæmis á að nota grunntímabilið og tvö tímabil sem koma þar á eftir skal skrifa inn **BASE:BASE+2**.                                                  |
| BASE-\#:BASE+\# | Notar mörg tímabil frá mismunandi tímabilum fyrir grunntímabilinu til margra tímabila og eftir grunntímabilið. Ef til dæmis á að nota þrjú fyrri tímabil, grunntímabilið og tvö tímabil sem koma þar á eftir skal skrifa inn **BASE-3:BASE+2**. |
| 1:BASE          | Notar mörg tímabil, frá fyrsta tímabilinu og til og með grunntímabilinu.                                                                                                                                                                 |
| \#              | Notið alltaf tiltekið tímabilsnúmer. Ekki er mælt með notkun þessa valkosts þar sem hann dregur úr sveigjanleika dálkskilgreiningarinnar.                                                                                       |
| \#:\#           | Alltaf skal nota tiltekið svið tímabila. Ekki er mælt með notkun þessa valkosts þar sem hann dregur úr sveigjanleika dálkskilgreiningarinnar.                                                                                    |

Hægt er að fara yfir mörk fjárhagsársins í hvaða tímabilsskilgreiningu sem er, og hægt er að blanda saman árum innan tímabilasviðs. Til dæmis ef þú tilgreinir tímabilin sem **BASE-5** (til að sýna síðustu sex tímabilin) og keyrir skýrslu með grunntímabilið 2. Í þessu tilfelli sýnir skýrslan gögn fyrir fyrstu tvö tímabilin á tilgreindu fjárhagsári og síðustu fjögur tímabilin á fyrra fjárhagsári.

### <a name="specify-the-periods-for-an-fd-column"></a>Tímabilin tilgreind fyrir FD-dálk

1.  Opnið dálkskilgreiningu í Report Designer til að gera breytingar.
2.  Í dálkinum **FD** er tvísmellt á hólfið í línunni **Tímabil** og síðan er valkostur valinn á listanum.
3.  Á formúlustikunni (fyrir ofan yfirlitssvæðið) eða í hólfinu **Tímabil** skal ljúka við formúluna. Skipta út öllum númerstáknum (\#) fyrir viðeigandi gildi.

#### <a name="periods-covered-cell"></a>Hólf tímabila sem tekin eru með

Hólfið **Tímabil sem er tekið með** auðkennir upphæðina sem ætti að sýna í dálkinum. Þessi upphæð veltur á gildinu í hólfunum **Fjárhagsár** og **Tímabil** fyrir dálkinn. Eftirtaldir valkostir eru í boði.

| Valkostur      | Lýsing                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Birta samtölu aðgerðarinnar fyrir gildandi tímabil eða tímabilasvið. |
| PERIODIC/BB | Birtia upphafsstöðu fyrir gildandi tímabil eða tímabilasvið.   |
| YTD         | Birta samtölu aðgerða það sem af er ári.                               |
| YTD/BB      | Birta upphafsstöðu fyrir árið.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Tímabilin tilgreind sem eru tekin með fyrir FD-dálk

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Í dálkinum **FD** er tvísmellt á hólfið í línunni **Tímabil sem tekið með** og síðan er valkostur valinn á listanum.

### <a name="attribute-filter-in-a-column-definition"></a>Afmörkun eiginda í dálkskilgreiningu

Eigindir eru gildi fjárhagsgagna sem skilgreina ítarlegar reikning eða færslu. Reikningseigindir innihalda **Eign**, **Skuld**, **Tekjur** og **Kostnaður**. Eigindir færslna innihalda **Færslulýsingu** og **notkunardagsetning færslu**. Stuðningur við eigindir gætu verið mismunandi milli Microsoft Dynamics ERP kerfa. Hólfið **Afmörkun eiginda** afmarkar gögn fyrir **FD**-dálka við sértæk gildi eða svið fyrir eigindaflokka. Þó að þessi eiginleiki getu verið notaður samhliða **ATTR**-dálki er **ATTR**-dálksins ekki krafist. Í **FD**-dálkinum eru takmörk fyrir reikninga eða færslur sem teknar verða með í skýrslunni úr afmörkun eiginda. **Ábending:** Upplýsingar um hvaða eiginleika ERP-kerfið styður eru í leiðbeiningum um samþættingu gagna fyrir kerfið.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Afmörkun eiginda beitt á FD-dálk í skýrslu

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á hólfið **Afmörkun eiginda** fyrir **FD**-dálk.
3.  Í svarglugganum **Afmörkun eiginda** skal tvísmella á hólf í dálkinum **Eigind** og velja því næst gerð afmörkunar.
4.  Til að afmarka niðurstöðurnar enn frekar skal slá inn svið í dálkana **Frá** og **Til**. Hólfið **Frá** verður að innihalda gildi.
5.  Smelltu á **Í lagi**.

#### <a name="example-of-an-attribute-filter"></a>Dæmi um afmörkun eiginda

Eftirfarandi dæmi sýnir hluta af dálklýsingu með eigind reiknings í línunni **Tegund bókarkóða/eigindar**. Afmörkun eiginda fyrir þennan dálk tilgreinir svið gilda sem taka á með í skýrslunni.

|                              | Lista fyrir    | B                    |
|------------------------------|------|----------------------|
| Gerð dálks                  | DESC | FD                   |
| Bókarkóði/Eigindaflokkur |      | ACTUAL               |
| Fjárhagsár                  |      | BASE                 |
| Tímabil                       |      | 1:BASE               |
| Tímabil sem er tekið með              |      | PERIODIC             |
| ...                          |      |                      |
| Dálkbreidd                 | 30   |                      |
| ...                          |      |                      |
| Afmörkun eiginda             |      |  Tilvísun=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Víddarafmörkun í dálkskilgreiningu

Víddarafmörkun er notuð til að takmarka **FD**-dálkinn við tiltekin víddargildi. Afmörkunin getur tekið til stakrar víddar, vídda á tilteknu sviði eða hóps vídda. Afmörkunin getur einnig falið í sér víddargildissamstæður. Þar sem víddargildi geta verið breytileg þarf ..\financial-dimensions\dimension-byggt kerfi ekki að fylgja nákvæmri lengd. Afmörkunin er notuð óháð því hvort skýrslan inniheldur skipurit. Hægt er að nota algildisstafinn staf (\* eða?) í hvers kyns stöðu. Þegar margir lyklar eru tilgreindir, er sett komma á milli lykla, líkt og í eftirfarandi dæmi: +Lykill=\[1200\], +Lykill=\[1100\], Deild=\[01?\] Til að fá allar deildir fyrir tiltekinn lykil, er hægt að útiloka deildarvíddina úr víddarsíunni. Til dæmis eru bæði eftirfarandi víddarsíur meðhöndlað á sama hátt:

-   +Account=\[1100\],Department
-   +Account=\[1100\]

Einnig er hægt að nota hvaða samsetningu bók- og tölustafa sem er fyrir nákvæma samsvörun, auk þess sem hægt er að skilgreina hlutavíddir. Til dæmis **Staðsetningu = \[10 *\*\]** felur í sér allar staðsetningar víddagildi sem byrja með 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Víddarafmörkun notuð fyrir dálk á skýrslu

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á hólfið **Víddarafmörkun** fyrir **FD**-dálk.
3.  Færið inn afmörkun/afmarkanir sem á að nota í svarglugganum **Víddir**.
4.  Smelltu á **Í lagi**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Skýrsla fyrir marga gjaldmiðla sniðin í dálkskilgreiningu

Skýrsla með mörgum gjaldmiðlum getur birt upphæðir í eiginlegum gjaldmiðli (staðbundnum), virkum gjaldmiðli (sjálfgefnum) eða skýrslugjaldmiðli. Virkur gjaldmiðill fyrirtækis er skilgreindur í Microsoft Dynamics ERP kerfinu. Ekki rugla saman þessari ERP-stillingu við stillingar stýrikerfis svæðisbundna valkosta þar sem hægt er að stilla tákn sjálfgefna gjaldmiðilsins sem eru notaðar á skýrslum. Eftirfarandi hólf tengd gjaldmiðlum eru tiltæk í dálkskilgreiningunni:

-   **Birtingarmynd gjaldmiðils** – Tilgreinir tegund gjaldmiðils (eiginlegur, virkur eða skýrslugjaldmiðill) þar sem færslur eru birtar. Stundum er vísað til þessarar virkni sem umreikningur gjaldmiðils. umreikningur gjaldmiðils, gerir notanda kleift að skrá fjárhagsupphæðir í gjaldmiðli sem gæti verið annar en virkur gjaldmiðill fyrirtækisins eða annar gjaldmiðill en færslan var færð inn í.
-   **Afmörkun gjaldmiðils** – Tilgreina afmörkun gjaldmiðils. Aðeins færslur sem færðar eru inn í gjaldmiðlinum sem valinn er birtast í skýrslunni.

> [!NOTE]
> Til að stofna skýrslur sem nota marga gjaldmiðla verður að velja gátreitinn **Taka með alla skýrslugjaldmiðla** í flipanum **Skýrsla** í skýrsluskilgreiningu. Til að ákvarða virkan gjaldmiðil fyrirtækis skal að eftirfarandi skrefum:

1.  Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Fyrirtæki**.
2.  Í svarglugganum **Fyrirtæki** skal velja fyrirtæki og smella síðan á **Skoða**.
3.  Í  **Skoða Fyrirtæki** svarglugganum undir **Svæðisbundnir valkostir**, er hægt að skoða þann gjaldmiðil sem er skilgreint fyrir valið fyrirtæki.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>tilgreindu gjaldmiðil í skýrslu með marga gjaldmiðla

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Tvísmellið á hólfið **Birtingarmynd gjaldmiðils** í viðeigandi **FD** dálki og veljið svo valkost fyrir birtingu upplýsinga um gjaldmiðil: **Eiginlegur/upphaflegur gjaldmiðill**, **Virkur gjaldmiðill úr stofngögnum** eða skýrslugjaldmiðil.
3.  Tvísmellið á hólfið **Gjaldmiðilsafmörkun** í viðeigandi **FD** dálki og veljið svo viðeigandi gjaldmiðilskóða á listanum. Aðeins færslur sem færðar eru inn þessum gjaldmiðli birtast í skýrslunni.

> [!NOTE]
> Valkostirnir sem lýst er hér gætu verið öðruvísi, allt eftir ERP-kerfinu. Frekari upplýsingar eru í [Fylgiskjölum með Microsoft ERP kerfi](https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Dæmi um hólf birtingamyndar gjaldmiðils og gjaldmiðilsafmörkunar.

Pála hefur valið eftirfarandi gjaldmiðilsvalkosti í dálkskilgreiningu sinni:

-   **Gjaldmiðilsafmörkun** - Jen
-   **Birtingarmynd gjaldmiðils** – Virkur (Bandaríkjadalir)

Vegna valsins á gjaldmiðilsafmörkun sem Phyllis valdi, inniheldur skýrslan aðeins færslur sem færðar voru inn í jenum (JPY). Vegna valsins á birtingamynd gjaldmiðils sem hún valdi, birtir skýrslan þessar færslur í virkum gjaldmiðli (Bandaríkjadölum) (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Samsetning gjaldmiðilsafmörkunar og birtingamyndar gjaldmiðils.

Eftirfarandi tafla sýnir niðurstöður skýrslunnar sem geta átt sér stað fyrir ýmsar samsetningar af valkostum í hólfunum **Birtingarmynd gjaldmiðils** og **gjaldmiðilsafmörkun**  vegna valsins sem Phyllis gerði. Virki gjaldmiðillinn er USD.

| Hólf fyrir Birtingarmynd gjaldmiðils                        | Hólf fyrir Gjaldmiðilsafmörkun | Niðurstaða skýrslu                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eiginlegur/upphaflegur gjaldmiðill                 | **JEN**              | **Y6, 000** – niðurstöðurnar sýna einungis færslur sem voru færðar inn í JPY.                                                                                                                        |
| Virkur gjaldmiðill úr stofngögnum | **JEN**              | **$60** – niðurstöðurnar sýna einungis færslur sem voru færðar inn í JPY og sýnir færslur í USD. **Ábending:** umreikningsgengi er um það bil 100 JPY á USD.                    |
| Virkur gjaldmiðill úr stofngögnum | Autt                | **$2,310 \*\*** Niðurstöðurnar sýna öll gögn í virkum gjaldmiðli sem tilgreindur er í fyrirtækisupplýsingunum. **Ábending:** Þessari upphæð er samtala úr öllum færslum í virkum gjaldmiðli. |
| Eiginlegur/upphaflegur gjaldmiðill                 | Autt                | **$2,250** – niðurstöður sýnir allar upphæðir í gjaldmiðli sem færslan var framkvæmd í.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Útreikningsdálkur í dálkskilgreiningu

Dálkur af tegundinni **CALC** í dálkskilgreiningu styður flókna útreikninga í hólfinu **Formúla** og getur tekið með virkjana **+**, **-**, **\*** og **/**, ásamt yrðingunum **IF/THEN/ELSE**. Að auki getur útreikningsdálkur vísað í hvaða annan dálk sem er, þ. á m. dálka sem á eftir koma. Þar að auki, getur útreikningsdálkur einnig innifalið fjárhagsár og tímabil til að styðja hausa fyrir dálkinn. Útreikningsformúlan getur verið að hámarki 1,024 stafir að lengd. Til þess að sýna niðurstöður útreikningsins sem hlutfall skal notast við sérstaka hnekkingu sniðs. **Ábending:** Niðurstöður útreikningsformúla innihalda ekki gildin í sviðum dálka sem á ekki að prenta. Til dæmis prentar **A:D** út **0** (núll) þar sem **A+B+C** fyrir gildi sem ekki á að prenta út reiknar út gildið.

#### <a name="operators-in-calculation-columns"></a>Virkjar í útreikningsdálkum

Til að bæta við, draga frá, margfalda eða skipta dálkum eru dálkstafir færðir inn í útreikningsröð og viðeigandi virkjar notaðir til að skilja að hvern dálkstaf. Eftirfarandi tafla lýsir því hvaða virkja er hægt að nota í útreikningsdálki.

| Virki | Dæmi um útreikning | lýsing                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | Bæta upphæðinni í dálki A við upphæðina í dálki C.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Bæta við sviði samliggjandi dálka. Til dæmis bætir formúlan **A:C** við samtölum dálka A til C og formúlan **A:C-D** bætir við samtölu A til C og dregur frá upphæðina í dálki D.                          |
| -        | A-C                 | Draga upphæðina í dálki A frá upphæðinni í dálki C. **athugasemd:** Einnig má nota mínustáknið (-) til að umsnúa táknum í dálki. Til dæmis er **-A+B** notað til að bæta bakfærslu upphæðar í dálki A við upphæðina í dálki B. |
| \*       | A\*C                | Margfalda upphæðinni í dálki A með upphæðinni í dálki C.                                                                                                                                                                                     |
| /        | A/C                 | Deila upphæðinni í dálki A með upphæðinni í dálki C.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Útreikningsformúla notuð í dálkskilgreiningu

1.  Opnið dálkskilgreiningu í Skýrsluhönnun til að gera breytingar.
2.  Í viðeigandi **CALC**-dálki er formúla slegin inn í hólfið **Formúla**.

#### <a name="complex-calculations"></a>Flóknir útreikningar

Flókinn útreikningur getur innihaldið hvaða samsetningu sem er af hólfatilvísunum, virkjum, gildum og stigum faldaðra sviga. Til að reikna meðaltal dálkanna A og B er til dæmis notuð útreikningsformúlan **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Skýrsluhólf tilgreind í dálkaútreikningi

Hægt er að vísa til tiltekins skýrsluhólfs með því að færa inn dálkstaf og línukóða. Til dæmis, vísar **B.100** til línukóða 100 í dálki B. Hægt er að deila í heilan dálk með upphæð tiltekins skýrsluhólfs sem er í sama dálki. Til dæmis merkir útreikningurinn **B/B.100** að deila skuli í upphæðinni í dálki B með gildinu í dálki B, línukóða 100. Ef útreikningurinn vísar í dálk sem er háður öðrum dálki er leyst úr háða dálkinum fyrst. Ef notandi vísar dálki í annan dálk sem vísar svo til baka í fyrsta dálkinn veldurðu villuboð um hringvirka tilvísun. **Ábending:** útreikningurinn er hugsanlega rangur ef útreikningsforgangi fyrir skýrsluna er breytt. Hægt er að stilla útreikningsforgang á flipanum **Stillingar** í skýrsluskilgreiningunni.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Margföldun eða skipting dálks eftir grunnlínu

Hægt er að stofna dálk sem birtir öll gildi í tilgreindum dálki sem prósentuhlutfall grunntölu. Þessvegna er hægt að sýna tengsl á milli lína, svo sem prósentuhlutfall sölulínu eða prósentuhlutfall línu heildarkostnaðar. Til að margfalda eða skipta hverri línu í tilgreindum dálki eftir grunnlínu skal slá inn dálkinn verður notað við útreikninginn og slá svo inn **\*BASEROW** eða **/BASEROW**. Færðu til dæmis inn **C\*BASEROW** eða **C/BASEROW**. **Ábending:** Þegar útreikningur grunnlínu er notaður í dálkskilgreiningu verður að gæta þess að hver dálkskilgreining sem notuð er með þeirri dálkskilgreiningu innihaldi minnst eina grunnlínu til útreikninga.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Skiptu upphæð í dálki eftir fjölda tímabila.

Hægt er að skipta upphæð í dálki eftir tilgreindum fjölda tímabila. Til dæmis skiptir formúlan  **B/Tímabil** gildinu í dálki B eftir fjölda tímabila sem gefinn er upp í dálki B. Ef útreikningurinn nær yfir marga dálka þarf að tilgreina fjölda tímabila sem nota á í útreikningnum. Til dæmist bætir **(B+C)/Tímabil** formúlan við upphæðunum í dálki B og dálki C og deilir svo í niðurstöðuna með tímabilsgildinu.

<a name="see-also"></a>Sjá einnig
--------

[Línuskilgreiningar í fjárhagsskýrslugerð](row-definitions-financial-reporting.md)

[Ítarlegir sniðsvalkostir í fjárhagsskýrslugerð](advanced-formatting-options-financial-reporting.md)




