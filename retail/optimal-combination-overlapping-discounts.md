---
title: "Ákvarða bestu samsetning afslættir skarast"
description: "Þegar afslættir skarast, verður að ákvarða samsetning skarast afslætti sem verður að framleiða lægsta heildarupphæð færslunnar eða hæsta heildarafsláttar. Þegar upphæð afsláttar er breytilegt eftir verði afurðir sem eru keyptar, svo sem almenn og &quot;Kaupa 1, sækja 1 X prósent&quot; smásöluafsláttar (BOGO), þetta ferli verður úthreyfing combinatorial fínstilling."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Ákvarða bestu samsetning afslættir skarast

Þegar afslættir skarast, verður að ákvarða samsetning skarast afslætti sem verður að framleiða lægsta heildarupphæð færslunnar eða hæsta heildarafsláttar. Þegar upphæð afsláttar er breytilegt eftir verði afurðir sem eru keyptar, svo sem almenn og "Kaupa 1, sækja 1 X prósent" smásöluafsláttar (BOGO), þetta ferli verður úthreyfing combinatorial fínstilling.

Þessi skrá við Microsoft Dynamics AX 2012 R3 með KB 3105973 (losuð 2 Nóvember 2015) eða síðar og Febrúar 2016 losa Microsoft Dynamics ax. Til að ákvarða samsetningu skarast afslætti til að nota í tæka tíð, og halda áfram til að veita rich discounting virkni sem er tiltækt í Microsoft Dynamics AX for Retail, mælt hefur verið kynnt aðferð við að nota afslættir skarast. Mælt kallaðferð þennan nýja **marginal gildi vægi**. Vægi marginal gildið er notað þegar tímann sem nauðsynlegur er til að meta mögulegar samsetningar á afslættir skarast yfir þröskuldi sem er gerð skilgreinanleg á í **færibreytur Retail** síðu í Dynamics AX. Marginal gildi vægi aðferð, gildi er reiknuð fyrir hverja skarast afslátt með því að nota gildi sem afsláttur á samnýtt afurðir. Overlapped afslættir gilda síðan úr tengdri hæsta gildi afstæðar lægsta gildi. Nánari upplýsingar um nýju greiðsluaðferðina, í hlutanum "Marginal gildi" síðar í þessari grein. Vægi marginal gildi er ekki notaður þegar afsláttarupphæðir afurðar ekki eru kostnaðarjafnaðar hefur áhrif á aðra afurð í færslunni. Til dæmis þessi aðferð er ekki notaður fyrir einfalt þessum tveimur afsláttum eða einfaldur afsláttur og magnafsláttur einni afurð.

## <a name="discount-examples"></a>Dæmi um afslætti
Hægt er að stofna ótakmarkaðan fjölda af smásöluafslætti í almennt safn afurðir í Dynamics AX. Hins vegar, þar sem engin takmörk eru afkastavandamála getur átt sér stað þegar reynt er að reikna út afslætti sem nota á mismunandi afurðir. Eftirfarandi dæmi sýna vandamálið nánar. Í dæmi 1 er mælt með að byrja tvær vörur og tvö afslættir skarast. Síðan, í dæmi 2 mælt sýna hvernig vandamálið evolves sem eru að bæta fleiri afurðum.

### <a name="example-1-two-products-and-two-discounts"></a>Dæmi 1: Tvær vörur og þessum tveimur afsláttum

Í þessu dæmi tvær afurðir eru nauðsynlegar til þess að viðurkenna fyrir hvern afslátt og ekki er hægt að sameina afslætti. Afsláttur í þessu dæmi er **Besta verð** afslætti. Bæði afurðir lágmarkspöntunargildi bæði afslætti. Hér eru á þessum tveimur afsláttum. [![Afsláttur sem skarast samsettra 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) Fyrir allar afurðir tvær betur af þessum tveimur afsláttum er háð verð tvær vörur. Þegar verð bæði afurðir er jafnt og eða sú sama og nánast er betra afsláttur 1. Þegar verð einni afurð er mikil minna en verð á vöru, er betra afsláttur 2. Hér er stærðfræðilega reglu fyrir mat á þessum tveimur afsláttum saman: [![Overlapping afsláttur samsettra 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) Athugið þegar verð afurðarinnar 1 er sú sama og tveggja thirds verð vöru 2, þessum tveimur afsláttum jafnar. Í þessu dæmi gildi afsláttarprósentu fyrir afslátt 1 er breytileg eftir fyrirtækjum nokkrar prósent (þegar verð tvær afurðir eru langt apart) hámark 25 prósent (þegar tvær vörur með sömu verð). Gildi afsláttarprósentu fyrir afslátt 2 er föst. Það er alltaf 20 prósent. Þar sem gildi afsláttarprósentu fyrir afslátt 1 hefur sviðs sem getur verið meira en eða minna en 2 afsláttur, fer bestu afsláttur verð tvær afurða sem verður að vera afsláttur. Í þessu dæmi útreikningi er lokið á fljótlegan hátt, þar sem aðeins þessum tveimur afsláttum er beitt á tveimur aðeins afurðir. Það eru tvær aðeins mögulegar samsetningar: eina forritið afsláttur 1 eða einn forritið afsláttar 2. Það eru engar permutations til að reikna út. Gildi fyrir hverja afsláttur er reiknaður með því að nota bæði afurðir og bestu afslátturinn er notað.

### <a name="example-2-four-products-and-two-discounts"></a>Dæmi 2: Fjórum afurðir og þessum tveimur afsláttum

Næst skal mælt mun nota fjórar afurðir og sama þessum tveimur afsláttum. Allar afurðir fjórum lágmarkspöntunargildi bæði afslætti. Það eru twelve mögulegar samsetningar. Í lok á þessum tveimur afsláttum verður notað fyrir færslu í einu af þremur samsetningar: 2, eða eitt forritið afsláttur 1 og ein forritið afsláttar 2 tvö forrit afsláttar 1, tvö forrit fyrir afslætti. Til að sýna mögulegar samsetningar, mælt verður þvínæst söfn fjórum afurðir sem hafa mismunandi verð:

-   Allar afurðir fjórum hafa sama verð $15.00. Í þessu tilfelli er bestu afsláttur samsetningu tvö forrit afsláttar 1. Tvær afurðir verða fullt verð og tvær verður 50 prósent af. Samtala með afslætti færslunnar slökkt er á $45 (15 + 15 + 7,50 + 7,50), sem er $15 (25 prósent) undiscounted samtala $60. Afsláttur 2 er aðeins $12 (20 prósent).
-   Tvær afurðir eru $20 hverja einni afurð er $15 og einni afurð er $5. Í þessu tilfelli bestu samsetningu afsláttur er einn afsláttur 2 og ein umsókn afsláttar 1. Eftirfarandi töflur sýnir afslætti.

Lesa töflur, að nota eina afurð úr línu og eina vöru úr dálk. Til dæmis í töflunni fyrir afslátt 1 er að sameina tvær $20 afurðir kvikna þegar $10. Í töflunni fyrir afsláttur 2 er að sameina $15 afurða og afurða $5, kvikna þegar $4. [![Afsláttur sem skarast samsettra 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) Fyrst, stærsta afsláttar sem er tiltækt frá tveimur afurðir með því að nota afsláttinn hvoru mælt fannst. Tvö töflur sýna afsláttarupphæð fyrir allar samsetningar af tvær vörur. Skyggðu hluti af töflum tákna annaðhvort tilfellum þar sem afurð er pöruð með sjálfri sem mælt er ekki hægt að gera eða er bakfærð upp para vélbúnaðarstöðina tvær afurða sem verður sama upphæð afsláttar og má hunsa. Með því að líta á töflur, hægt er að sjá sem afslátt 1 fyrir tvær vörur $20 er stærsta afsláttar sem er tiltækt fyrir annað hvort afslætti á allar fjórar afurðir. (Þessi afsláttur er upplýstur grænu í fyrstu töflunni.) Aðeins $15 afurða og afurða $5 sem skilur. Með því að líta á tvær töflurnar aftur, hægt er að sjá sem, fyrir þessar tvær afurðir afsláttur 1 gefur $2.50 afsláttur, en afsláttur 2 gefur $4 afslátt. Þess vegna er mælt velja afsláttur 2. Heildarupphæð afsláttar er $14. Til að gera þessa umræðu auðvelda visualize, hér eru tvær viðbótar töflum sem sýna gildi afsláttarprósentu fyrir allar mögulegar tveggja afurð samsetningar fyrir bæði afsláttur 1 og 2 afsláttar. Aðeins hálft lista með samsetningum höfð með, því þessum tveimur afsláttum pöntun sem tvær vörur eru settar í afsláttur ekki mikilvægt. Grænt er upplýstur hæsta gildi afsláttinn (25%) og lægsta gildi afsláttinn (10 prósent) er upplýstur rauður. [![Afsláttur sem skarast samsettra 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Athugasemd:** Þegar mismunandi verð og afsláttur tvær eða fleiri keppa, er eina leiðin til að tryggja samræmda bestu samsetningu af afslætti til að meta bæði afslætti og bera þær saman.

## <a name="total-possible-combinations"></a>Samtals mögulegar samsetningar
Í þessum hluta heldur dæmi úr fyrri kafla. Við höfum verður að bæta fleiri afurðir og öðrum afslætti og sjá hversu margar samsetningar verður reiknað út og bornar saman. Eftirfarandi tafla sýnir fjölda mögulegar afsláttarsamsetningar sem hækkana magn afurðar. Taflan sýnir hvað gerist bæði þegar það eru tvær skarast afslætti og fyrri dæmi, og þegar það eru þrjár skarast afsláttur. Fjöldi mögulegar afsláttarsamsetningar sem þarf að meta fljótlega fer yfir hvað jafnvel skjóta tölvu getur reiknað út og bera saman fljótt nógu að viðunandi fyrir smásölufærslur. [![Afsláttur sem skarast samsettra 05](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) jafnvel Þegar meira magn eða fleiri afslættir skarast eru notaðar, fjöldi mögulegar afsláttarsamsetningar fljótt fer í í milljónum og tíma sem þarf til að meta og veljið besta mögulega samsetningu fljótt verður virkni. Sumar optimizations hefur verið gert í smásölu vélar verð til að draga úr fjölda sem þarf að meta. Hins vegar þar sem númer afslættir skarast og magn í færslu sem ekki eru kostnaðarjafnaðar takmörkuð, mikinn fjölda samsetningar verður alltaf að hafa til að meta hvenær afslættir skarast. Vandamálið er vandamál sem marginal gildi vægi aðferð aðsetur.

## <a name="marginal-value-method"></a>Aðferð marginal gildið
Til að leysa eð auka fjölda samsetningar sem þarf að meta, fínstillingar er til staðar sem reiknar gildi á samnýttrar afurðar á hverja afsláttur á hóp afurða sem hægt er að nota tvær eða fleiri afslætti. Í þessu gildi sem er **marginal gildi** afsláttar fyrir samnýttar afurðir. Marginal gildið er meðaltal eftir afurð hækkun heildarupphæð afsláttar þegar samnýtt afurðir eru í hvern afslátt. Marginal gildið er reiknað með því að taka afsláttarupphæð samtals (DTotal) því að draga afsláttarupphæð án samnýtta afurðir (DMinus\\ Samnýttum), og því sem mismunur að deila með fjölda samnýtta afurða (ProductsShared). [![Afsláttur sem skarast samsettra 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) Eftir marginal gildi fyrir hvern afslátt á samnýtt hóp afurða er reiknaður út afslætti eru notuð í samnýtta afurðir í röð exhaustively, hæsta gildi marginal marginal lægsta gildi. Fyrir þessa aðferð allar eftirstöðvar möguleika afsláttur ekki eru kostnaðarjafnaðar borið er saman í hvert skipti eftir eitt tilvik af afsláttur er veittur. Þess í stað skarast afslætti eru samanburði einu sinni og svo notað í röð. Enginn viðbótar samanburð lokið. Hægt er að skilgreina þröskuld til að skipta aðferðina marginal gildi við **Afsláttur** flipanum í **færibreytur Retail** síðu. Viðunandi tíma til að reikna heildarafslátt er breytileg milli atvinnugreina smásölu. Hins vegar, þennan tíma almennt fellur í sviði tens millisekúndum á eina sekúndu.


