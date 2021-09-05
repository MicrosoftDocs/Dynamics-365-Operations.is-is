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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385724"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Bókun færslubókar mistekst vegna misræmis

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvers vegna misræmi gæti verið á debet- og kreditfærslum í fylgiskjalsfærslum þannig að ekki sé hægt að bóka færslurnar. Efnisatriðið inniheldur einnig skref til að laga þetta vandamál.

## <a name="symptom"></a>Einkenni

Í sumum tilvikum er ekki hægt að bóka færslubók og eftirfarandi skilboð eru sýnd: „Ekki er samræmi á færslum tiltekins fylgiskjals á ákveðinni dagsetningu (bókhaldsgjaldmiðill: 0,01 - skýrslugjaldmiðill: 0,06).“ Af hverju má ekki bóka færslubókina?

## <a name="resolution"></a>Lausn

Við bókun í fjárhag þurfa öll fylgiskjöl að vera jöfnuð í færslugjaldmiðli, bókhaldsgjaldmiðli og skýrslugjaldmiðli ef þessi gjaldmiðlar eru skilgreindir á síðunni **Fjárhagsuppsetning**. (Fylgiskjöl eru jöfnuð þegar samtala debetfærslna jafngildir samtölu kreditfærslna.)

Neðst á síðu færslubókarlína eru samtölur sýndar í bókhaldsgjaldmiðli og skýrslugjaldmiðli. Þær eru **ekki** sýndar í færslugjaldmiðli fyrir færslur í erlendum gjaldmiðli. Villuboð sem notendur fá við hermingu eða bókun sýna aðeins muninn í bókhaldsgjaldmiðli og skýrslugjaldmiðli. Þau eru ekki sýnd í færslugjaldmiðli vegna þess að eitt fylgiskjal getur haft fleiri en einn færslugjaldmiðil og færslubókin getur innihaldið fylgiskjöl í mismunandi færslugjaldmiðlum. Þess vegna er mikilvægt að þú staðfestir að upphæðir færslugjaldmiðils fyrir hvert fylgiskjal séu jafnaðar.

### <a name="transaction-currency"></a>Gjaldmiðill færslu

Við hermingu og bókun staðfestir kerfið að öll fylgiskjöl séu jöfnuð í færslugjaldmiðlinum. Fyrir hvert fylgiskjal sem er slegið inn geta verið einn eða fleiri gjaldmiðlar fyrir færslugjaldmiðilinn. Til dæmis gæti fylgiskjal sem er færti inn í almennu færslubókina verið með tvo færslugjaldmiðla þegar reiðufé er millifært af bankareikningi sem notar evrur (EUR) yfir á bankareikning sem notar kanadíska dollara (CAD).

Ef fylgiskjal er með aðeins einn færslugjaldmiðil verður samtala debetfærslna að jafngilda samtölu kreditfærslna fyrir það fylgiskjal. Viðskiptavinir hafa lent í eftirfarandi aðstæðum þar sem bókunin mistókst réttilega vegna þess að upphæðir færslugjaldmiðils voru ekki jafnaðar:

- Samtala debetfærslna og samtala kreditfærslna voru **ekki** jafnaðar í færslugjaldmiðlinum, en þær voru jafnaðar fyrir bókhaldsgjaldmiðilinn og skýrslugjaldmiðilinn. Viðskiptavinur gerði ráð fyrir að fylgiskjalið yrði samt bókað. Sú ályktun var hins vegar röng. **Upphæðir færslugjaldmiðils í fylgiskjali verða alltaf að vera jafnaðar þegar allar línur fylgiskjalsins eru með sama gjaldmiðilinn.**
- Fylgiskjal var flutt inn gegnum Microsoft Excel og notandinn hélt að upphæðir færslugjaldmiðilsins væru jafnaðar. Í Excel-vinnubókinni voru innfluttar upphæðir stilltar á **Tölustafagildi**, ekki **Gjaldmiðil**. Í þessum aðstæðu voru upphæðir tölustafa í vinnubókinni með fleiri en tvo aukastafi og fleiri en tveir aukastafir voru teknir með þegar upphæðirnar voru fluttar inn. Debetfærslurnar jafngiltu því ekki kreditfærslunum vegna þess að misræmi þeirra var upp á brot eða aura. Færslubókin endurspeglaði ekki þennan mun í línum fylgiskjalsins vegna þess að upphæðirnar sem eru sýndar eru aðeins með tvo aukastafi.
- Fylgiskjal var flutt inn gegnum Excel og notandinn hélt að upphæðir færslugjaldmiðilsins væru jafnaðar. Þótt fylgiskjalið hafi verið jafnað voru sumar línur fylgiskjalsins með mismunandi færsludagsetningum. Ef þú bættir við samtölu debetfærslna og samtölu kreditfærslna fyrir hvert fylgiskjal og færsludagsetningu, þá voru þær ekki jafnaðar. Kerfið kemur nú í veg fyrir þessar aðstæður. Fylgiskjal getur aðeins verið með eina færsludagsetningu. Þessari kröfu er framfylgt þegar þú slærð inn fylgiskjal í gegnum almenna dagbók í kerfinu. Henni var hins vegar ekki framfylgt upphaflega þegar fylgiskjal var flutt inn gegnum Excel.

Í einum studdum aðstæðum getur fylgiskjal verið með fleiri en einn færslugjaldmiðil. Í þessu tilviki staðfestir kerfið **ekki** að debetfærslurnar jafngildi kreditfærslunum í færslugjaldmiðlinum vegna þess að gjaldmiðlarnir stemma ekki. Þess í stað staðfestir kerfið að upphæðir bókhaldsgjaldmiðils séu jafnaðar.

### <a name="accounting-currency"></a>Bókhaldsgjaldmiðill

Ef allar línur fylgiskjalsins eru með sömu færslugjaldmiðilinn og ef upphæðir færslugjaldmiðilsins eru jafnaðar, staðfestir kerfið að upphæðir bókhaldsgjaldmiðilsins séu jafnaðar. Ef fylgiskjalið er fært inn í erlendum gjaldmiðli er gengið í fylgiskjalslínunum notað til að umreikna upphæðir færslugjaldmiðilsins í bókhaldsgjaldmiðilinn. Fyrst er hver lína fylgiskjalsins umreiknuð. Því næst eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Þar sem hver lína er umreiknuð er ekki víst að samtala debetfærslna og samtala kreditfærslna séu jafnaðar. Engu að síður, ef munurinn er innan gildis fyrir **Hámarks auramismunur** sem er skilgreint á síðunni **Færibreytur fjárhags** verður fylgiskjalið bókað og munurinn verður sjálfkrafa bókaður á lykil auramismunar.

Ef fylgiskjalið er með fleiri en einn færslugjaldmiðil er hver lína fylgiskjalsins umreiknuð í bókhaldsgjaldmiðilinn og síðan eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Til að teljast jafnað þurfa debetfærslurnar og kreditfærslurnar að vera jafnaðar og ekki má vera neinn sléttunarmismunur á aurum.

### <a name="reporting-currency"></a>Skýrslugjaldmiðill

Ef allar línur fylgiskjalsins eru með sömu færslugjaldmiðilinn og ef upphæðir færslugjaldmiðilsins eru jafnaðar, staðfestir kerfið að upphæðir skýrslugjaldmiðilsins séu jafnaðar. Ef fylgiskjalið er fært inn í erlendum gjaldmiðli er gengið í fylgiskjalslínunum notað til að umreikna upphæðir færslugjaldmiðilsins í skýrslugjaldmiðilinn. Fyrst er hver lína fylgiskjalsins umreiknuð. Því næst eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Þar sem hver lína er umreiknuð er ekki víst að samtala debetfærslna og samtala kreditfærslna séu jafnaðar. Engu að síður, ef munurinn er innan gildis fyrir **Hámarksaurasléttun í skýrslugjaldmiðlinum** sem er skilgreint á síðunni **Færibreytur fjárhags** verður fylgiskjalið bókað og munurinn verður sjálfkrafa bókaður á lykil auramismunar.

Ef fylgiskjalið er með fleiri en einn færslugjaldmiðil er hver lína fylgiskjalsins umreiknuð í skýrslugjaldmiðilinn og síðan eru línurnar lagðar saman til að finna út samtölu debetfærslna og samtölu kreditfærslna. Til að teljast jafnað þurfa debetfærslurnar og kreditfærslurnar að vera jafnaðar og ekki má vera neinn sléttunarmismunur á aurum.
