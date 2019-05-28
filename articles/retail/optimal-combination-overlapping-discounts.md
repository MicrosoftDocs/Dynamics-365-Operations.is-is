---
title: Ákvarða bestu samsetningu afsláttar sem skarast
description: Þegar afsláttur skarast, verður að ákvarða samsetningu afsláttar sem skarast, sem mun skapa lægstu heildarupphæð færslunnar eða hæsta heildarafslátt. Þegar afsláttarupphæð er breytileg eftir verði afurða sem eru keyptar, eins og hinn algengi smásöluafsláttur „Keyptu 1, fáðu 1 X prósent afslátt“ (BOGO), snýst þetta ferli um fínstillingu á samsetningum.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: eebb532071e7c6bae7cfae93bfe795e79bb16c63
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564996"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Ákvarða bestu samsetningu afsláttar sem skarast

[!include [banner](includes/banner.md)]

Þegar afsláttur skarast, verður að ákvarða samsetningu afsláttar sem skarast, sem mun skapa lægstu heildarupphæð færslunnar eða hæsta heildarafslátt. Þegar afsláttarupphæð er breytileg eftir verði afurða sem eru keyptar, eins og hin algenga „Keyptu 1, fáðu 1 X prósent afslátt“ smásöluafslátt (BOGO), verður þetta ferli vandamál fínstillingar á samsetningum.

Þessi grein á við um Microsoft Dynamics AX 2012 R3 með KB 3105973 (gefin út 2. nóvember 2015) eða síðar og við Microsoft Dynamics 365 for Retail. Við höfum innleitt aðferð til að nota afslætti sem skarast, til að hægt sé að ákvarða samsetningu afsláttar sem skarast tímanlega. Við köllum þessa nýju aðferð **Röðun jaðarvirðis**. Röðun jaðarvirðis er notuð þegar tíminn sem er nauðsynlegur til að meta mögulegar samsetningar á afslætti sem skarast fer yfir þröskuld sem er gerður skilgreinanlegur á síðunni **Færibreytur í Retail**. Í röðun jaðarvirðis, er virði reiknað fyrir hvern afslátt sem skarast með því að nota virði afsláttar á samnýttar afurðir. Afsláttur sem skarast gildir síðan úr tengdu hæsta hlutfallslega virði gegn lægsta hlutfallslega virði. Nánari upplýsingar um nýju greiðsluaðferðina er að finna í hlutanum „Jaðarvirði" síðar í þessari grein. Röðun jaðarvirðis er ekki notað þegar afsláttarupphæðir afurðar verða ekki fyrir áhrifum af annarri afurð í færslunni. Til dæmis er þessi aðferð ekki notuð fyrir tvo einfalda afslætti eða fyrir einfaldan afslátt og magnafslátt einnar afurðar.

## <a name="discount-examples"></a>Dæmi um afslætti

Hægt er að stofna ótakmarkaðan fjölda af smásöluafsláttum í sameiginlegu safni afurða. Hins vegar, þar sem engin takmörk eru geta afkastavandamál átt sér stað þegar reynt er að reikna út afslætti sem nota á mismunandi afurðir. Eftirfarandi dæmi sýna vandamálið nánar. Í dæmi 1 er byrjum við með tvær vörur og tvo afslætti sem skarast. Síðan, í dæmi 2 mælt er sýnt hvernig vandamálið þróast eftir því sem fleiri afurðum er bætt við.

### <a name="example-1-two-products-and-two-discounts"></a>Dæmi 1: Tvær vörur og tveir afslættir

Í þessu dæmi eru tvær afurðir nauðsynlegar til þess að vera hæfar fyrir hvern afslátt og ekki er hægt að sameina afslættina. Afslættir í þessu dæmi eru afslættir af **Besta verð**. Báðar afurðir eru hæfar fyrir báða afslætti. Hér eru þessir tveir afslættir.

![Samsetning afslátta sem skarast 01](./media/overlapping-discount-combo-01.jpg)

Fyrir hvaða tvær afurðir sem er, fer sá betri af tveimur afsláttum eftir verðum afurðanna tveggja. Þegar verð bæði afurðir er jafnt og eða nánast það sama er betra afsláttur 1. Þegar verð einni afurð er mikil minna en verð á vöru, er betra afsláttur 2. Hér er stærðfræðileg regla fyrir mat á þessum tveimur afsláttum gagnvart hvor öðrum.

![Samsetning afslátta sem skarast 02](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Þegar verð afurðar 1 jafnast á við tvo þriðju hluta af verði afurðar 2, eru þessir tveir afslættir jafnir. Í þessu dæmi, er gild afsláttarprósenta fyrir afslátt 1 breytileg um nokkur prósent (þegar mikill munur er á verði afurðanna tveggja) að hámarki 25 prósent (þegar afurðnar tvær hafa sama verð). Gildi afsláttarprósentu fyrir afslátt 2 er föst. Það er alltaf 20 prósent. Þar sem gildi afsláttarprósentu fyrir afslátt 1 hefur svið sem getur verið meira en eða minna en 2 afsláttur, fer besti afslátturinn eftir verði afurðanna tveggja sem verða að hafa afslátt. Í þessu dæmi er útreikningi lokið á fljótlegan hátt, þar sem aðeins þessum tveimur afsláttum er beitt á aðeins tvær afurðir. Það eru tvær aðeins mögulegar samsetningar: ein notkun á afsláttur 1 eða ein notkun á afsláttar 2. Það er engin umröðun til að reikna. Virði hvors afsláttar er reiknað með því að nota báðar afurðir og besti afslátturinn er notaður.

### <a name="example-2-four-products-and-two-discounts"></a>Dæmi 2: Fjórar vörur og tveir afslættir

Næst notum við fjórar afurðir og sama þessum tveimur afsláttum. Allar fjórar afurðirnar eru hæfar fyrir báða afslætti. Það eru tólf mögulegar samsetningar. Í lokin verða tveir afsláttum notað í færslunni í einni af þremur samsetningum: tvær beitingar á afslætti 1, tvær beitingar afslætti 2, eða ein beiting á afslætti 1 og ein beiting á afslætti 2. Til að sýna mögulegar samsetningar, lítum við þvínæst á tvö mismunandi pör fjögurra afurða sem hafa mismunandi verð:

- Allar fjórar afurðir hafa sama verð $15,00. Í þessu tilfelli er besta samsetning afsláttur tvær beitingar á afsláttar 1. Tvær afurðir verða á fullu verði og tvær verða með 50 prósent afslætti. Samtala með afslætti færslunnar er $45 (15 + 15 + 7,50 + 7,50), sem er $15 (25 prósent) af samtala $60 án afsláttar. Afsláttur 2 er aðeins $12 (20 prósent).
- Tvær afurðir eru $20 hvor, ein afurð er $15 og ein afurð er $5. Í þessu tilfelli er besta afsláttarsamsetningin ein beiting á afsláttur 2 og ein beiting á afsláttar 1. Eftirfarandi töflur sýnir afslættina.

Til að lesa töflurnar þarf að nota eina afurð úr línu og eina vöru úr dálki. Til dæmis í töflunni fyrir afslátt 1, þegar tvær $20 afurðir eru sameinaðar færðu $10 í afslátt. Til dæmis í töflunni fyrir afslátt 2, þegar $15 afurð og $5 afurð eru sameinaðar færðu $4 í afslátt.

![Samsetning afslátta sem skarast 03](./media/overlapping-discount-combo-03.jpg)

Fyrst finnum við hæsta afsláttinn sem er í boði úr hvaða tveimur afurðum sem er með því að nota annan hvorn afsláttinn. Töflurnar tvær sýna afsláttarupphæð fyrir allar samsetningar á afurðunum tveimur. Skyggðu hlutar töflunnar tákna annaðhvort tilfelli þar sem afurð er pöruð með sjálfri sér, sem við getum ekki gert, eða er bakfærð pörun tveggja afurða sem verður að sömu afsláttarupphæð og má hunsa. Með því að líta á töflur, hægt er að sjá að afsláttur 1 fyrir tvær vörur á $20 er stærsti afsláttar sem er tiltækt fyrir annað hvort afslætti á allar fjórar afurðir. (Þessi afsláttur er upplýstur með grænu í fyrstu töflunni.) Þá eru aðeins $15 afurðin og $5 afurðin eftir. Með því að líta á tvær töflurnar aftur er hægt að sjá að fyrir þessar tvær afurðir veitir afsláttur 1 $2,50 afslátt, en afsláttur 2 veitir aftur á móti $4 afslátt. Þess vegna veljum við afslátt 2. Heildarafslátturinn er $14. Til að auðvelda að gera þessa umræðu sér í hugarlund eru hér tvær viðbótartöflur sem sýna gildi afsláttarprósentu fyrir allar mögulegar tveggja afurða samsetningar fyrir bæði afsláttur 1 og 2 afsláttar. Aðeins helmingurinn af lista með samsetningum er hafður með, því að fyrir þessa tvo afslætti skiptir ekki máli í hvaða röð í afslættinum afurðirnar tvær eru settar í. Hæsta gildi afsláttar (25%) er upplýst í grænu og lægsta gildi afsláttar (10 prósent) er upplýstur rauður.

![Samsetning afslátta sem skarast 04](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Þegar verð eru mismunandi og tveir eða fleiri afslættir keppa, er eina leiðin til að tryggja bestu samsetningu af afsláttum er að meta báða afslætti og bera þá saman.

## <a name="total-possible-combinations"></a>Mögulegar samsetningar alls

Þessi hluti heldur áfram með dæmi úr fyrri kafla. Við munum bæta við fleiri afurðum og öðrum afslætti og sjá hversu margar samsetningar er hægt að reikna út og bera saman. Eftirfarandi tafla sýnir fjölda mögulegra afsláttarsamsetninga eftir því sem afurðarmagn hækkar. Taflan sýnir hvað gerist bæði þegar það eru tveir afslættir sem skarast, eins og í fyrra dæmi, og þegar það eru þrír afslættir sem skarast. Fjöldi mögulegar afsláttarsamsetningar sem þarf að meta fljótlega fer yfir það sem jafnvel fljótvirk tölva getur reiknað út og borið saman nógu fljótt til að vera viðunandi fyrir smásölufærslur.

![Samsetning afslátta sem skarast 05](./media/overlapping-discount-combo-05.jpg)

Þegar enn fleiri afslættir sem skarast eru notaðir, fer heildarfjöldi mögulegra afsláttasamsetninga fljótlega í milljónir, og tíminn sem þarf til að meta og velja bestu mögulegu samsetninguna verður fljótlega tilfinnanlegur. Einhver fínstilling hefur verið gert í smásöluverðsvélinni til að draga úr þeim heildarfjölda samsetninga sem þarf að meta. Hins vegar, þar sem fjöldi afslátta sem skarast og magns í færslu eru ekki takmörkuð, mun mikill fjöldi samsetninga alltaf verða að vera metinn í hvert skipti sem afslættir skarast. Þetta vandamál er vandamál sem aðferð röðunar jaðarvirðis tekur á.

## <a name="marginal-value-method"></a>Aðferð jaðarvirðis

Til að leysa vandamál stigveldisvaxandi fjölda samsetninga sem þarf að meta, eru fínstillingar til staðar sem reikna virði á samnýttrar afurðar á hverja afsláttur á hóp afurða sem hægt er að nota tvær eða fleiri afslætti á. Við vísum til þessa virðis sem **jaðarvirðis** afsláttar fyrir samnýttar afurðir. Jaðarvirði er meðaltal á afurðahækkun í heildarupphæð afsláttar þegar samnýttar afurðir eru taldar með fyrir hvern afslátt. Jaðarvirði er reiknað með því að taka afsláttarupphæð samtals (DTotal), draga frá afsláttarupphæð án samnýtta afurðir (DMinus\\ Samnýttum), og deila þeim mismun með fjölda samnýtta afurða (ProductsShared).

![Samsetning afslátta sem skarast 06](./media/overlapping-discount-combo-06.jpg)

Eftir að jaðarvirði fyrir hvern afslátt á samnýtta hópa afurða hefur verið reiknað út, er afsláttum beitt á samnýttar afurðir í tæmandi röð frá hæsta jaðarvirði til lægsta jaðarvirðis. Fyrir þessa aðferð eru allir eftirstandandi afsláttarmöguleikar ekki bornir saman í hvert skipti sem eitt tilvik afsláttar er sett á. Þess í stað eru afslættir sem skarast bornir saman einu sinni og síðan notað í röð. Enginn viðbótarsamanburður er gerður. Hægt er að skilgreina þröskuld til að skipta yfir í aðferð jaðarvirðis á flipanum **Afsláttur** á síðunni **Færibreytur Retail**. Viðunandi tími til að reikna heildarafslátt er breytilegur milli atvinnugreina smásölu. Hins vegar er þessi tími almennt á bili tíu millisekúnda til einnar sekúndu.
