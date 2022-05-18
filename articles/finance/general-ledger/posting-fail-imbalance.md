---
title: Bókun færslubókar mistekst vegna misræmis
description: Þetta efnisatriði útskýrir hvers vegna misræmi gæti verið á debet- og kreditfærslum í fylgiskjalsfærslum þannig að ekki sé hægt að bóka færslurnar. Efnisatriðið inniheldur einnig skref til að laga þetta vandamál.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 07408e608496dcc19562b866449b3b27f5f80edd
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719933"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Bókun færslubókar mistekst vegna misræmis

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvers vegna misræmi gæti verið á debet- og kreditfærslum í fylgiskjalsfærslum þannig að ekki sé hægt að bóka færslurnar. Efnisatriðið inniheldur einnig skref til að laga þetta vandamál.

## <a name="symptom"></a>Einkenni

Í sumum tilvikum er ekki hægt að bóka færslubók og eftirfarandi skilboð eru sýnd: „Ekki er samræmi á færslum tiltekins fylgiskjals á ákveðinni dagsetningu (bókhaldsgjaldmiðill: 0,01 - skýrslugjaldmiðill: 0,06).“ Af hverju má ekki bóka færslubókina?

## <a name="resolution"></a>Lausn

Við bókun í fjárhag þurfa öll fylgiskjöl að vera jöfnuð í færslugjaldmiðli, bókhaldsgjaldmiðli og skýrslugjaldmiðli ef þessi gjaldmiðlar eru skilgreindir á síðunni **Fjárhagsuppsetning**. (Fylgiskjöl eru jöfnuð þegar samtala debetfærslna jafngildir samtölu kreditfærslna.)

Neðst á síðu færslubókarlína eru samtölur sýndar í bókhaldsgjaldmiðli og skýrslugjaldmiðli. Þær eru **ekki** sýndar í færslugjaldmiðli fyrir færslur í erlendum gjaldmiðli. Villuboð sem notendur fá við hermingu eða bókun sýna aðeins muninn í bókhaldsgjaldmiðli og skýrslugjaldmiðli. Þau eru ekki sýnd í færslugjaldmiðli vegna þess að eitt fylgiskjal getur haft fleiri en einn færslugjaldmiðil og færslubókin getur innihaldið fylgiskjöl í mismunandi færslugjaldmiðlum. Þess vegna er mikilvægt að þú staðfestir handvirkt að upphæðir færslugjaldmiðils fyrir hvert fylgiskjal sem aðeins hafa einn færslugjaldmiðil séu jafnaðar.

### <a name="transaction-currency"></a>Gjaldmiðill færslu

Við hermingu og bókun staðfestir kerfið að öll fylgiskjöl sem aðeins hafa einn færslugjaldmiðil séu jöfnuð í færslugjaldmiðlinum. Fyrir hvert fylgiskjal sem er slegið inn geta verið einn eða fleiri gjaldmiðlar fyrir færslugjaldmiðilinn. Til dæmis gæti fylgiskjal sem er færti inn í almennu færslubókina verið með tvo færslugjaldmiðla þegar reiðufé er millifært af bankareikningi sem notar evrur (EUR) yfir á bankareikning sem notar kanadíska dollara (CAD).

Ef fylgiskjal er með aðeins einn færslugjaldmiðil verður samtala debetfærslna að jafngilda samtölu kreditfærslna í færslugjaldmiðli fyrir það fylgiskjal. Viðskiptavinir hafa lent í eftirfarandi aðstæðum þar sem bókunin mistókst réttilega vegna þess að upphæðir færslugjaldmiðils voru ekki jafnaðar:

- Samtala debetfærslna og samtala kreditfærslna voru **ekki** jafnaðar í færslugjaldmiðlinum, en þær voru jafnaðar fyrir bókhaldsgjaldmiðilinn og skýrslugjaldmiðilinn. Viðskiptavinur gerði ráð fyrir að fylgiskjalið yrði samt bókað. Sú ályktun var hins vegar röng. **Upphæðir færslugjaldmiðils í fylgiskjali verða alltaf að vera jafnaðar þegar allar línur fylgiskjalsins eru með sama færslugjaldmiðilinn.**
- Fylgiskjal var flutt inn með gagnaeiningu gegnum gagnastjórnunarramma (DMF) og notandinn hélt að upphæðir færslugjaldmiðilsins væru jafnaðar. Í innflutningsskránni voru sumar upphæðir með fleiri en tvo aukastafi og fleiri en tveir aukastafir voru teknir með þegar upphæðirnar voru fluttar inn. Debetfærslurnar jafngiltu því ekki kreditfærslunum vegna þess að misræmi þeirra var upp á brot eða aura. Færslubókin endurspeglaði ekki þennan mun í línum fylgiskjalsins vegna þess að upphæðirnar sem eru sýndar eru aðeins með tvo aukastafi.
- Fylgiskjal var flutt inn með gagnaeiningu gegnum DMF og notandinn hélt að upphæðir færslugjaldmiðilsins væru jafnaðar. Þótt **fylgiskjalið** hafi verið jafnað voru sumar línur fylgiskjalsins með mismunandi færsludagsetningum. Ef þú bættir við samtölu debetfærslna og samtölu kreditfærslna í færslugjaldmiðlinum fyrir hvert **fylgiskjal og færsludagsetningu**, þá voru þær ekki jafnaðar. Þessari kröfu er framfylgt þegar þú slærð inn fylgiskjal í gegnum almenna dagbók í kerfinu. Hins vegar er því ekki framfylgt þegar fylgiskjal er flutt inn með gagnaeiningu í gegnum DMF.

Í einum studdum aðstæðum getur fylgiskjal verið með fleiri en einn færslugjaldmiðil. Í þessu tilviki staðfestir kerfið **ekki** að debetfærslurnar jafngildi kreditfærslunum í færslugjaldmiðlinum vegna þess að gjaldmiðlarnir stemma ekki. Þess í stað staðfestir kerfið að upphæðir bókhaldsgjaldmiðils og skýrslugjaldmiðils séu jafnaðar.

### <a name="accounting-currency"></a>Bókhaldsgjaldmiðill

Ef allar línur fylgiskjalsins eru með sömu færslugjaldmiðilinn og ef upphæðir færslugjaldmiðilsins eru jafnaðar, staðfestir kerfið að upphæðir bókhaldsgjaldmiðilsins séu jafnaðar. Ef fylgiskjalið er fært inn í erlendum gjaldmiðli er gengið í fylgiskjalslínunum notað til að umreikna upphæðir færslugjaldmiðilsins í bókhaldsgjaldmiðilinn. Fyrst er hver lína fylgiskjalsins umreiknuð og sléttuð í tvo aukastafi. Því næst eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Þar sem hver lína er umreiknuð er ekki víst að samtala debetfærslna og samtala kreditfærslna séu jafnaðar. Engu að síður, ef algildi munarins er innan gildis fyrir **Hámarks auramismunur** sem er skilgreint á síðunni **Færibreytur fjárhags** verður fylgiskjalið bókað og munurinn verður sjálfkrafa bókaður á lykil auramismunar.

Ef fylgiskjalið er með fleiri en einn færslugjaldmiðil er hver lína fylgiskjalsins umreiknuð í bókhaldsgjaldmiðilinn og sléttuð í tvo aukastafi og síðan eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Til að teljast jafnvægi verða skuldir og inneignir að vera í jafnvægi í bókhaldsgjaldmiðlinum.  Peningamunareikningi er aldrei bætt við skírteinið í bókhaldsgjaldmiðlinum til að koma debet- og inneigninni í jafnvægi. 

### <a name="reporting-currency"></a>Skýrslugjaldmiðill

Ef allar línur fylgiskjalsins eru með sömu færslugjaldmiðilinn og ef upphæðir færslugjaldmiðilsins eru jafnaðar, staðfestir kerfið að upphæðir skýrslugjaldmiðilsins séu jafnaðar. Ef fylgiskjalið er fært inn í erlendum gjaldmiðli er gengið í fylgiskjalslínunum notað til að umreikna upphæðir færslugjaldmiðilsins í skýrslugjaldmiðilinn. Fyrst er hver lína fylgiskjalsins umreiknuð og sléttuð í tvo aukastafi. Því næst eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Þar sem hver lína er umreiknuð er ekki víst að samtala debetfærslna og samtala kreditfærslna séu jafnaðar. Engu að síður, ef munurinn er innan gildis fyrir **Hámarksaurasléttun í skýrslugjaldmiðlinum** sem er skilgreint á síðunni **Færibreytur fjárhags** verður fylgiskjalið bókað og munurinn verður sjálfkrafa bókaður á lykil auramismunar.

Ef fylgiskjalið er með fleiri en einn færslugjaldmiðil er hver lína fylgiskjalsins umreiknuð í skýrslugjaldmiðilinn og síðan eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Til að teljast jafnvægi verða skuldir og inneignir að vera í jafnvægi í skýrslugjaldmiðlinum.  Peningamunareikningi er aldrei bætt við skírteinið í skýrslugjaldmiðlinum til að koma skuldfærslunum og inneignunum í jafnvægi.

### <a name="example-for-an-accounting-currency-imbalance"></a>Dæmi um ójafnvægi í bókhaldsgjaldmiðli

> [!NOTE]
> Skýrslugjaldmiðilsupphæðin er reiknuð úr færslugjaldmiðilsupphæðinni á sama hátt og bókhaldsgjaldmiðilsupphæðin.

Gengi: 1,5

| Lína | Fylgiskjal | Lykill | Gjaldmiðill | Debet (færsla) | Kredit (færsla) | Debet (bókhald) | Kredit (bókhald) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10,00 | | 15.00 |
| **Alls** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Mismunur bókhaldsgjaldmiðilsins er 0,01. Svo lengi sem hámarks aurasléttun í bókhaldsgjaldmiðli er minnst 0,01 verður mismunurinn sjálfkrafa bókaður á auramismunalykilinn og fylgiskjalið bókað.
