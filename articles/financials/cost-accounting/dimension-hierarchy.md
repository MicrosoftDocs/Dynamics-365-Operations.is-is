---
title: "Víddarstigveldi"
description: "Þetta efni inniheldur upplýsingar um víddastigveldi. Víddastigveldi eru notuð til að skilgreina skipulag skýrslugerðar, kostnaðarreglur og öryggisuppsetningu í kostnaðarbókhaldi."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 40a4a1d7549876b72186f30a9c0089f0d27cf3b6
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="dimension-hierarchy"></a>Víddarstigveldi

[!include[banner](../includes/banner.md)]

Þetta efni inniheldur upplýsingar um víddastigveldi. Víddastigveldi eru notuð til að skilgreina skipulag skýrslugerðar, kostnaðarreglur og öryggisuppsetningu í kostnaðarbókhaldi.  

## <a name="overview"></a>Yfirlit

Víddarstigveldi eru notuð á mismunandi stöðum í kostnaðarbókhaldi. Víddastigveldi gerir mögulegt að tilgreina eftirfarandi upplýsingar:

-  Skýrsluuppbygging sem hentar þörfum fyrirtækis þíns
-  Kostnaðarreglur
-  Öryggisuppsetningin

Hér er dæmi um víddastigveldi.

![Dæmi um víddastigveldi](./media/dimension-hierarchy.png)

Hægt er að stofna víddastigveldi fyrir eftirfarandi gerðir vídda:

-  Víddir kostnaðareiningar
-  Víddir kostnaðarhluta
-  Tölfræðilegar víddir

> [!NOTE]
> - Hægt er að stofna mörg víddastigveldi vídd fyrir sömu vídd ef mismunandi sjónarhorna er krafist.
> - Víddastigveldi má aðeins tengja við eina vídd.
> - Víddastigveldi getur haft ótakmörkuð stig í uppbyggingu sinni. Öll stig verða tiltæk í vinnusvæðinu **Kostnaðarstjórn**. Þegar Microsoft Excel eða Microsoft Power BI til skýrslugerðar eru notuð eru aðeins fyrstu 15 stig í stigveldi flutt út. Þessi takmörkun eru til staðar þar sem Excel og Power BI krefjast fasts skema.
> - Víddastigveldi er ekki dagsetnarvirkt. Þar af leiðandi eru allar breytingar á víddastigveldi strax vistaðar í skrána og ekki er hægt að bera saman fyrri og seinni dagsetningar.

## <a name="dimension-hierarchy-type"></a>Gerð víddastigveldis

Þegar nýtt víddastigveldi er búið til verður að velja tegund stigveldis. Farið í **Kostnaðarbókhald** > **Víddir** > **Víddarstigveldi**. Smellt er á **Nýtt** og valin gerð víddastigveldis. Hægt er að velja annaðhvort **Tegundastigveldi víddar** eða **Flokkunarstigveldi víddar**.

### <a name="dimension-categorization-hierarchy"></a>Stigveldi víddaflokkunar

Tegundin **Tegundastigveldi víddar** er notuð til skýrslugerðar. Hún styður einungis víddir kostnaðareininga. Þegar þessi gerð er valin gilda eftirfarandi reglur:

-  Víddarstakið getur verið tengt oftar en einu sinni í byggingu stigveldisins.
-  Hægt er að setja víddarstak kostnaðareiningar í mismunandi hnúta með því að úthluta kostnaðarhegðun á leaf-hnút.

### <a name="dimension-classification-hierarchy"></a>Stigveldi víddaflokkunar

Gerðin **Flokkunarstigveldi víddar** er notuð til að skilgreina reglur og til skýrslugerðar. Hún styður allar víddir á borð við kostnaðarhluti, kostnaðareiningar og tölfræðilegar víddir. Þegar þessi gerð er valin er aðeins hægt að tengja víddarstak einu sinni í byggingu stigveldisins.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Stofna og stjórna víddastigveldi

Víddastigveldi stofnast sem trjáskipulag með vensl hnúta og leaf-hnúta.

-  Hnútur getur haft 1:_n_ undirhnúta.
-  Hnútur getur ekki haft undirhnúta og leaf-hnútar tengda við sig.
-  Aðeins er hægt að úthluta leaf-hnút á lægsta stigi í stigveldi.

### <a name="example"></a>Dæmi

Lítið fyrirtæki hefur eftirfarandi fyrirtækisskipulagið, þar sem Fjármál og mannauður eru deildir undir Stjórnun og Samsetningarinnar og Umbúðir eru deildir í Framleiðslu.

![Dæmi um skipulag fyrirtækis](./media/dimension-hierarchy-org.png)

Vídd kostnaðarhluta stendur fyrir alla kostnaðarstaði í fyrirtækinu.

- Vídd kostnaðarhlutar
    - Kostnaðarstaðir

Vídd kostnaðarhlutar sem sýnir alla kostnaðarstaði er hægt að setja eins og sýnt er hér.

| Kostnaðarstaðir | lýsing |
|--------------|-------------|
| CC001        | Mannauður          |
| CC002        | Fjármál     |
| CC003        | Skattur         |
| CC007        | AR/AP       |
| CC005        | Smölun    |
| CC006        | Pakkning   |

Vídd kostnaðareiningar stendur fyrir allar kostnaðareiningar í fyrirtækinu.

- Vídd kostnaðareiningar
    - Kostnaðareiningar

Vídd kostnaðareiningar sem sýnir allar kostnaðareiningar er hægt að setja eins og sýnt er hér.

| Kostnaðareiningar | lýsing |
|---------------|-------------|
| 10001         | Rafmagn |
| 10010         | Hreinsun    |
| 10011         | Hitun     |
| 40001         | Kostnaður seldra vara        |

Víddastigveldi sem uppfyllir skipulags tilkynningarskyldu hægt er að setja eins og sýnt er hér.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd    | Heiti gerðar víddarstigveldis      | Stigveldi aðgangslista |
|--------------------------|--------------|------------------------------------|-----------------------|
| Fyrirtæki             | Kostnaðarstaðir | Stigveldi víddaflokkunar | Númer                    |

Hægt er að setja upp víddastigveldi fyrir skýrslugerð eins og sýnt er hér.

|                   | Svið víddarstaks   |                         |
|-------------------|---------------------------|-------------------------|
| **Hnútar**         | **Úr víddarstaki** | **Til víddarstaks** |
| Fyrirtæki      |                           |                         |
| &nbsp;&nbsp;Stjórnandi         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Fjármál   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Mannauður        | CC001                     | CC001                   |
| &nbsp;&nbsp;Framleiðsla    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkning | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Smölun  | CC006                     | CC006                   |

Víddastigveldi sem uppfyllir reglur er hægt að setja upp eins og sýnt er hér.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd     | Heiti gerðar víddarstigveldis      |
|--------------------------|---------------|------------------------------------|
| Kostnaðarhegðun            | Kostnaðareiningar | Stigveldi víddaflokkunar |

Hægt er að setja upp víddastigveldi fyrir regluna eins og sýnt er hér.

|                   | Svið víddarstaks   |                         |
|-------------------|---------------------------|-------------------------|
| **Hnútar**         | **Úr víddarstaki** | **Til víddarstaks** |
| Kostnaðarhegðun     |                           |                         |
| &nbsp;&nbsp;Fastur kostnaður    | 10001                     | 10011                   |
|&nbsp;&nbsp;Breytilegur kostnaður | 40001                     | 40010                   |

> [!NOTE]
> Undir **Svið víddarstaks** getur hnútur innihaldið 1:_n_ svið víddarstaks. Hægt er að setja inn kenni víddarstaka sem eru ekki enn fyrir hendi sem víddarstök. Þessi aðferð gerir stigveldi endingargott fyrir seinni tíma.  

### <a name="copy-a-hierarchy"></a>Afrita stigveldi

Hægt er að afrita gildandi víddastigveldi sem upphafspunkt fyrir nýtt víddastigveldi. Þessi aðferð getur verið gagnleg ef vilji er til að bera saman fyrri víddastigveldi við nýtt víddastigveldi.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Endurraða hnútum í stigveldi

Hægt er að færa hnút upp og niður innan núgildandi stigs í uppbyggingu. Á þennan hátt er hægt að endurraða hnútum fyrir skýrslugerð á vinnusvæðinu **Kostnaðarstjórnun**.

Þú færir hnút í nýja staðsetningu í stigveldinu með því að velja markhnútinn. Tvær leiðir eru til að færa hnút:

- **Færa niður fyrir** – Færið valinn hnút úr gildandi stöðu í stigveldinu og setjið hann **undir** valinn markhnút.
- **Færa aftur fyrir** – Færið valinn hnút úr gildandi stöðu í stigveldinu og setjið hann **aftur fyrir** valinn markhnút á stigi sínu í víddastigveldi.

> [!NOTE] 
> Röð hnúta er ekki viðhaldið þegar gögn eru flutt út í Excel- eða Power BI, þar sem þau verkfæri nota staftöluröðun sjálfgefið. Það ætti að endurraða pöntuninni handvirkt.

## <a name="define-dimension-hierarchies-for-reporting"></a>Skilgreina víddastigveldi fyrir skýrslugerð

Víddastigveldi eru mikilvæg fyrir skýrslugerð. Þau gera mögulegt að skilgreina ákveðið skipulag sem passar inn í einstök fyrirtæki. Uppsafnanirnar sem gerðar eru við hnútastig í stigveldi láta hagsmunaaðila á öllum stigum fyrirtækisins sjá gögn á öllum stigum.

Víddastigveldi eru tiltæk í eftirfarandi skýrslutækjum. Þessi aðferð hjálpar til við að tryggja samræmi í skýrslugerð.

- Vinnusvæðið **Kostnaðarstýring** (Biðlari):

    - Stýrt af samskipan.

- Vinnusvæði **kostnaðarstýringar** (fartækjaforrit):

    - Stýrt af samskipan.

- Excel

    - Býður upp á að velja tiltekið víddastigveldi á skilgreiningu útflutnings:

        - Eitt víddarstigveldi kostnaðareiningar (skylda)
        - Eitt víddarstigveldi kostnaðarhlutar (valfrjálst)
        - Eitt tölfræðilegt víddarstigveldi (valfrjálst)

- Power BI:

    - Öll víddastigveldi eru tiltæk.
    
Ef þú stofnar skýrslur með því að nota Excel eða Power BI eru aðeins fyrstu 15 stig í stigveldi flutt út. Þessi takmörkun er til staðar þar sem Excel og Power BI krefjast fasts skema. Ef stigveldi hefur fleiri en 15 stig verða aukastigin ekki flutt út. Stöðluð tafla inniheldur færslu fyrir hvert víddarstak í stigveldinu. Þess vegna verður sjálfvirk uppsöfnun. Þessi hegðun hjálpar til við að tryggja samræmda stöðu á hvern 15 tiltæk stig í stigveldinu eru enn rétt.

Eftirfarandi dæmi sýnir hvernig víddastigveldi gæti litið út í uppbyggingu skýrslu.

| Víddarstigveldi kostnaðarhlutar - Stig 1 | Víddarstigveldi kostnaðarhlutar - Stig 2 | Víddarstigveldi kostnaðarhlutar - Stig 3 | Víddarstigveldi kostnaðarhlutar - Stig 4 | Víddarstigveldi kostnaðarhlutar - Stig 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Fyrirtæki                              | Stjórnandi                                     | Fjármál                                   | CC002                                     |                                            |
| Fyrirtæki                              | Stjórnandi                                     | Fjármál                                   | CC003                                     |                                            |
| Fyrirtæki                              | Stjórnandi                                     | Fjármál                                   | CC007                                     |                                            |
| Fyrirtæki                              | Stjórnandi                                     | Mannauður                                        | CC001                                     |                                            |
| Fyrirtæki                              | Framleiðsla                                | Pakkning                                 | CC005                                     |                                            |
| Fyrirtæki                              | Framleiðsla                                | Smölun                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Uppfæra víddastigveldi sem eru notuð fyrir skýrslugerð 

Með tímanum verður að uppfæra víddastigveldi sem eru notuð í áður nefndum skýrslugerðarverkfærum. Hægt er að uppfæra víddastigveldi með endurnýjun biðlara.

- Vinnusvæðið **Kostnaðarstýring** (Biðlari)
- Vinnusvæði **kostnaðarstýringar** (fartækjaforrit)

Uppfærslur á víddastigveldi eru tínd á 24 tíma fresti af áður vistaðri vinnslu. Eftir að útflutt gögn eru uppfærð eru uppfærð víddastigveldi tiltæk í eftirfarandi verkfærum:

- Excel
- Power BI

> [!NOTE] 
> Til að kalla fram uppfærslu á skyndiminni víddastigveldi handvirkt, er hægt að stofna nýjar útflutning í Excel fyrir víddastigveldi eða stigveldi sem þarf að uppfæra.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Skilgreina víddastigveldi fyrir kostnaðarreglur

Kostnaðarbókhald samanstendur af mörgum reglum þar sem ítarlegar reglur eru skilgreindar. Það verður að skilgreina eitt eða fleiri víddastigveldi reglna fyrir eftirfarandi reglur:

- Kostnaðarhegðun
- Kostnaðardreifing
- Kostnaðarúthlutun
- Samantekt kostnaðar

Víddastigveldi auðvelda stofnun á reglum. Til að komast hjá því að stofna reglur fyrir hverja vídd, er hægt nýta uppsafnanir yfir víddarstök sem veitt eru af stigum víddastigvelda. Ef reglur skarast, verður að skilgreina tilteknar reglur sem kerfið mun hafa í huga þegar það reiknar út fastakostnað.

### <a name="example-define-a-cost-behavior-policy"></a>Dæmi: Tilgreina reglu kostnaðarhegðunar

Ný regla kostnaðarhegðunar er stofnuð og viðeigandi víddastigveldi er úthlutað á þá reglu, eins og sýnt er hér.

**Regla kostnaðarhegðunar**

| Stefnuheiti   | Víddarstigveldi kostnaðareiningar | Víddarstigveldi kostnaðarhlutar | Bókhaldsgjaldmiðill |
|---------------|----------------------------------|---------------------------------|---------------------|
| Kostnaðarhegðun | Kostnaðarhegðun                    | Fyrirtæki                    | USD                 |

**Reglur**

| Hnútur á víddarstigveldi kostnaðareiningar | Hnútur á víddarstigveldi kostnaðarhlutar | Föst prósenta | Föst upphæð | Gildir frá | Gildir til |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fastur kostnaður                            | Fyrirtæki                         | 100,00           | 0,00         | 1/1/2017   | Aldrei    |
| 10001                                 | Fyrirtæki                         | 0,00             | 150.00       | 1/1/2017   | Aldrei    |
| 10001 (\*)                             | Fjármál                              |                  | 50,00        | 1/1/2017   | Aldrei    |
| Kostnaðarhegðun eða Breytilegan kostnað (\*\*)   | Fyrirtæki                         | 0,00             | 0,00         | 1/1/2017   | Aldrei    |

\* Hnútur breytilegs kostnaðar er ekki nauðsynlegur. Ef kostnaður er ekki flokkaður sem fastakostnaður, verður að vera breytilegan kostnað.

\*\* Ítarlega regla er stofnuð fyrir samsetningar á kostnaði einingarinnar stak 10001 og alla kostnaðarflokka stökum þjónustuhlutar sem eru tekin saman í á Fjármál stigsveldisstig (CC002 CC003, CC007).

Fyrrgreindar reglur sýna sveigjanleika sem víddastigveldi veita. Með því að skilgreina reglur á háu stigi er hægt að lágmarka viðhald. Síðan er hægt að skilgreina nákvæmar relgur sem passa í tilteknum viðskiptum markmið.

Ef víddastigveldi sem eru notuð í reglur eru uppfærð færir kerfið uppfærslurnar sjálfkrafa áfram.

Ef ekki er lengur þörf á grófleikastigi í reglunum er hægt að afskrifa regluna.

Til dæmis er ekki lengur þörf á hegðun reglu tilgreindan kostnað Fjármál kostnað hlutar vídd stigveldi hnútar. Í þessu tilfelli þarf að smella á **Afskrifa reglu** að afskrifa regluna.

| Hnútur á víddarstigveldi kostnaðareiningar | Hnútur á víddarstigveldi kostnaðarhlutar | Föst prósenta | Föst upphæð | Gildir frá | Gildir til  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fastur kostnaður                            | Fyrirtæki                         | 100,00           | 0,00         | 1/1/2017   | Aldrei     |
| 10001                                 | Fyrirtæki                         | 0,00             | 150,00       | 1/1/2017   | Aldrei     |
| 10001                                 | Fjármál                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Kostnaðarhegðun eða Breytilegan kostnað        | Fyrirtæki                         | 0,00             | 0,00         | 1/1/2017   | Aldrei     |

Allar útreikningsformúlur sem eru keyrðar eftir 20. janúar 2017 taka ekki lengur tillit til þessarar reglu.

> [!NOTE] 
> Retirnir **Gildir frá** og **Gildir til** eru dagsetningarvirkir og tímavirkir. Reglan renna út og keyrt nýtt útreikningsformúlur á þeim sama degi.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Skilgreina víddastigveldi fyrir öryggisuppsetningu

Gögn kostnaðarbókhalds skulu vera tiltæk fyrir alla stjórnendur sem bera ábyrgð á skýrslueiningu. Í orðalista kostnaðarbókhalds er skýrslueining sýnd sem kostnaðarhlutur eða safn kostnaðarhluta.

Mögulega munu allir stjórnendur geta opnað mjög viðkvæm viðskiptagögn slíkar tekjum og framlegð. Þess vegna er mikilvægt að setja upp öryggi svo að stjórnendur sjá aðeins gögnin sem eru viðeigandi fyrir þá. Til að stýra gögnum öryggi skal skilgreina víddastigveldi.

- Notkun víddastigvelda gildir aðeins þegar víddargildi sem valið er í víddastigveldi er vídd kostnaðarhlutar.
- Aðeins er hægt að virkja eitt víddastigveldi á vídd kostnaðarhlutar í stigveldi aðgangslista.

**Upplýsingar um víddarstigveldi**

| Heiti víddarstigveldis | Vídd    | Heiti gerðar víddarstigveldis      | Stigveldi aðgangslista |
|--------------------------|--------------|------------------------------------|-----------------------|
| Fyrirtæki             | Kostnaðarstaðir | Stigveldi víddaflokkunar | **Já**               |

Nýr flýtiflipi **Notendur** er tiltækur í stigveldishönnuði. Hér er hægt að færa inn eitt eða fleiri notandakenni í hverjum hnúti innan stigveldisins.

|                 | Notendur            | Svið víddarstaks   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Hnútar**       | **Notandakenni**      | **Úr víddarstaki** | **Til víddarstaks** |
| Fyrirtæki    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Stjórnandi         | Apríl            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Fjármál   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Mannauður        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Framleiðsla    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakkning | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Smölun  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Kostnaðarbókarar skulu vera í efsta stigi stigveldisins svo þeir geti séð allar færslur í kostnaðarbókhaldi.

Til að virkja stigveldi aðgangslista og öryggisstillinga hans, er farið í **kostnaðarbókhald** > **Uppsetningu** > **Færibreytur** > **Almennt**. Veldu færibreytuna **Virkja skoðunaraðgang fyrir víddarstök kostnaðarhlutar**.

Stillingar fyrir stigveldi aðgangslista eru notaðar til að stjórna gögnunum sem birtast á eftirfarandi svæðum:

- Vinnusvæðið **Kostnaðarstýring** (Biðlari):

    - Gögn í skjámyndum sem notaðar eru til að bora í gegnum tilvik

- Vinnusvæði **kostnaðarstýringar** (fartækjaforrit):

    - Stöður í spjöldum

- Power BI:

    - Gögn sem birtast í myndrænni framsetningu Power BI
    - Myndræn framsetning á gögnum Power BI sem eru felld inn í biðlara Microsoft Dynamics 365 for Finance and Operations

> [!NOTE] 
> - Áður en stigveldi aðgangslista getur haft áhrif á gögn í Power BI verður að para stigveldi aðgangslista og öryggi á línustigi í Power BI. Nánari upplýsingar eru í [Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Stigveldi aðgangslista tryggir ekki útflutning á gögnum í Excel. Þar af leiðandi ætti það skýrslugerðartæki aðeins að verað notað af kostnaðarbókunum og stjórnendum sem verða að hafa ótakmarkaðan aðgang til að skoða gögn.

