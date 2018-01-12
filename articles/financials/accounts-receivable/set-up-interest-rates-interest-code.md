---
title: "Setja upp vaxtastig fyrir vaxtakóða"
description: "Vaxtakóðar innihalda stillingar sem ákveða hvenær vextir eru gjaldfærðir og hvernig það er reiknað á gjaldfallna reikninga."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7ae0bfdc157a7e2e5b9f871dae487a6f85e889b9
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Setja upp vaxtastig fyrir vaxtakóða

[!include[banner](../includes/banner.md)]


Vaxtakóðar innihalda stillingar sem ákveða hvenær vextir eru gjaldfærðir og hvernig það er reiknað á gjaldfallna reikninga.

Hægt er að setja upp staka vaxtakóða og jafna hann við margar bókunarreglur viðskiptavina, innheimtukóða, eða tilteknar reikningslínur. Þegar upplýsingum vaxtakóða er breytt, munu allar aðgerðir sem nota kóðann sjálfkrafa innleiða breytingarnar í nýju færslunum. Fyrir hvern vaxtakóða er hægt að setja upp tvær gerðir taxta:
-   Taxtar fyrir vaxtatekjur− þeir tákna tekjur sem eru áunnar með því að skuldfæra vexti á reikninga eða vaxtanótur.
-   Taxtar fyrir vaxtagreiðslur − Þeir standa fyrir kostnað sem er greiddur fyrir vexti á kreditnótum.

Báðar þessar taxtategundir geta verið til á sama tíma og í sama vaxtakóða. Vextir geta byggst á þremur gerðum útreikninga:
-   Vextir Eftir prósentu
-   Vextir eftir upphæð
-   Vextir eftir sviði, sem leiðir til einnar prósentu eða upphæðar

Þegar vaxtakóði er notaður til að reikna vexti, er sérstök vaxtanóta stofnuð fyrir hvert vaxtastig sem er í gildi á þeim tíma er greiðsla hefur farið framyfir gjalddaga. Nota skal **hagnaður** flipanum á **Vaxtakóði** síðunni til að setja upp vexti fyrir vexti sem þú vinnur þér inn með því að rukka vexti.. Til að setja upp vaxtastig fyrir vexti sem greiddir eru skal nota **greiðslur** flipann.

## <a name="interest-rates-based-on-a-percentage"></a>Setja upp vexti á grundvelli prósenta
Hægt er að setja upp vaxtastig sem reiknar út tilgreinda prósentu.

-   Upphæð vaxta gildir um alla gjaldmiðla.
-   Hægt er að færa inn valfrjáls takmörk upphæðar fyrir vexti.
-   **Prósenta** er valin í **Reikna út vexti á grundvelli** svæðinu á síðunni **Setja upp vaxtakóða**.

Til dæmis til að setja upp vaxtakóða sem metur 5 prósent vexti fyrir hverja tvo mánuði sem reikningurinn fer umfram gjalddaga færslunnar, þá væri fært inn 2 í svæðið **reikna vexti fyrir hvern** og velja **Mánuður**.

## <a name="interest-rates-based-on-amounts"></a>Vextir á grundvelli upphæða
Hægt er að setja upp vaxtastig sem reiknar út tilgreinda upphæð fyrir hvern gjaldmiðil.
-   Vaxtaupphæð er tilgreind fyrir hvern gjaldmiðil í vaxtakóða.
-   Hægt er að færa inn valfrjáls takmörk upphæðar fyrir vexti.
-   **Upphæð** er valin í **Reikna út vexti á grundvelli** svæðinu á **Setja upp vaxtakóða** síðunni.

Til dæmis til að setja upp vaxtakóða sem metur 25,00 prósent vexti fyrir hverja 20 daga sem reikningurinn fer umfram gjalddaga færslunnar, þá væri fært inn 20 í svæðið **reikna vexti fyrir hvern** og velja **Dagur**.

## <a name="interest-rates-based-on-ranges"></a>Vextir á grundvelli sviða
Hægt er að setja upp vaxtastig sem eru mismunandi eftir því hvaða upphæð fallin í gjalddaga, fjölda þeirra daga sem upphæðin er komin fram yfir, eða fjölda mánaða sem upphæðin komin fram yfir.
-   Hægt er að nota **Hagnaður eftir Gjaldmiðli** flipa til að skilgreina stillingar fyrir ákveðna vexti fyrir hvern gjaldmiðil. Þetta er einnig þar sem verður að skilgreina svið.
-   Nota skal **svið** hnappinn til að bæta við línum sem tákna svið sem á að setja upp. **Frá** gildi stendur fyrir upphaf sviðsins og **Vaxtagildi** númer stendur fyrir annað hvort hlutfall eða upphæð, eftir því sem valið er í **Reikna vexti á grundvelli** í **Setja upp vaxtakóða** síðu.

## <a name="example-1-interest-by-range--amount"></a>Dæmi 1: Vextir eftir afmörkun = upphæð
Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir þriðja hvern mánuð sem reikningurinn er umfram gjalddaga færslunnar. Óskað er eftir að byggja útreikning á prósentugildi vaxta, samkvæmt skrefskiptum upphæðarbilum. Vaxtagildið verður 1 prósent fyrir reikningsupphæðir allt að 1.000,00, 2 prósent fyrir upphæðir frá 1.001,00 til 5.000,00 og 3 prósent fyrir upphæðir hærri en 5.000,00. Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.

| **Nafn svæðis**                  | **Svæðisgildi** |
|---------------------------------|-----------------|
| **Vaxtakóði**               | 3M%ByAmt        |
| **Reikna vexti hverja**    | 3/Mánuður         |
| **Vextir eftir afmörkun**           | Upphæð          |
| **Reikna vexti út frá** | Prósenta      |

Settar eru upp upplýsingar um afmörkun sem hér segir.

| **Frá gildi** | **Vaxtagildi** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Dæmi 2: Vextir eftir afmörkun = Dagar
--------------------------------------------------

Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir 15. hvern dag sem reikningurinn er umfram gjalddaga færslunnar. Óskað er eftir að byggja útreikning á upphæðargildi vaxta, samkvæmt skrefskiptum dagabilum. Gildi vaxta verður 10,00 á 15 daga á fyrstu 60 dögunum, 15,00 á 15 daga á dögum 61 til 90 og 20,00 á 15 daga frá deginum 91 og síðar. Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.

| **Nafn svæðis**                  | **Svæðisgildi** |
|---------------------------------|-----------------|
| **Vaxtakóði**               | 15DAmtXDay      |
| **Reikna vexti hverja**    | 15/Dagur          |
| **Vextir eftir afmörkun**           | Dagar            |
| **Reikna vexti út frá** | Upphæð          |

Settar eru upp upplýsingar um afmörkun sem hér segir.

| **Frá gildi** | **Vaxtagildi** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Dæmi 3: Vextir eftir afmörkun = mánuðir
----------------------------------------------------

Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir hvern mánuð sem reikningurinn er umfram gjalddaga færslunnar. Óskað er eftir að byggja útreikning á prósentugildi vaxta, samkvæmt skrefskiptum mánaðarbilum. Vaxta gildi verður 1,5 prósent hvern mánuð fyrir fyrstu þrjá gjaldfallna mánuðina, 2,0 prósent fyrir næstu þrjá mánuði og 2,5 prósent á mánuði fyrir hvern mánuð umfram fyrstu sex mánuði. Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.

| **Nafn svæðis**                  | **Svæðisgildi** |
|---------------------------------|-----------------|
| **Vaxtakóði**               | 1M%ByMth        |
| **Reikna vexti hverja**    | 1/mánuður         |
| **Vextir eftir afmörkun**           | Mánuðir          |
| **Reikna vexti út frá** | Prósenta      |

Settar eru upp upplýsingar um afmörkun sem hér segir.

| **Frá gildi** | **Vaxtagildi** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Nýjar útgáfur
Vaxtakóðar eru gildir eftir dagsetningum. Ef þú vilt breyta vöxtum, geturðu stofnað **nýja útgáfu** sem tekur gildi frá og með framtíðardagsetningu.

Til að skoða mismunandi útgáfur er hægt að nota í **frá og með** val til að velja lokadagsetninguna. Einnig er hægt að velja **Birta allar færslur** til að skoða allar vaxtakóðum á síðunni.




