---
title: Fjárhagsvíddir
description: Þessi efnisgrein lýsir ýmsum gerðum fjárhagsvídda og hvernig þær eru settar upp.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2fb325e143eff067e1c9d0f23a1f913fc2dc36f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "317546"
---
# <a name="financial-dimensions"></a>Fjárhagsvíddir

[!include [banner](../includes/banner.md)]

Þessi efnisgrein útskýrir ýmsar gerðir fjárhagsvídda og hvernig þær eru settar upp.

Nota skal skjámyndina **Fjárhagsvíddir** til að stofna fjárhagsvíddir sem nota má sem hluta lykils fyrir bókhaldslykla. Til eru tvær gerðir fjárhagsvídda: sérsniðnar víddir og afritaðar víddir. Sérsniðnar víddir eru samnýttar á milli lögaðila og gildi eru færð inn og þeim stjórnað af notendum. Fyrir afritaðar víddir eru gildin skilgreind annars staðar í kerfinu, t.d. í viðskiptavina- eða verslunareiningu. Sumar afritaðar víddir eru samnýttar á milli lögaðila, en aðrar afritaðar víddir eru bundnar fyrirtækjum.

Eftir að búið er að stofna fjárhagsvíddir skal nota síðuna **Fjárhagsvíddargildi** til að úthluta fleiri eiginleikum fyrir hverja fjárhagsvídd.

Hægt er að nota fjárhagsvíddir til að tákna lögaðila. Ekki þarf að stofna lögaðila í Microsoft Dynamics 365 for Finance and Operations. Hins vegar eru fjárhagsvíddir ekki hannaðar til að takast á við rekstrar- eða viðskiptaskilyrði lögaðila. Eiginlekin millieiningabókhalds í Finance and Operations er hannaður til að eiga aðeins við bókhaldsfærslur sem eru stofnaðar fyrir hverja færslu.

Áður en fjárhagsvíddir eru settar upp sem lögaðilar skal meta viðskiptaferli á eftirfarandi svæðum til að ákvarða hvort þessi uppsetning muni gagnast fyrirtækinu:

- Birgðir
- Sölu og innkaup milli fjárhagsvíddir og lögaðila
- útreikningur VSK og skýrslugerð
- Aðgerðaskýrslugerð

Hér eru sumar af skorðunum:

- Hægt er að nota virkni virðisaukaskatts ekki með fjárhagsvíddum, aðeins við lögaðila.
- Sumar skýrslur innihalda ekki fjárhagsvíddir. Þar af leiðandi gæti þurft að breyta skýrslunum til að gera skýrslu eftir fjárhagsvídd.

## <a name="custom-dimensions"></a>Sérsniðnar víddir

Til að stofna notandaskilgreinda fjárhagsvídd, í **Nota gildi** frá reit skal velja **Sérsniðin vídd**.

Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir. Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik (-). Einnig er hægt að slá inn tölumerki (\#) og og-merki (&) sem frátakara fyrir stafi sem breytast í hvert skipti sem víddargildi er stofnað. Notaðu tölumerki (\#) sem frátakara fyrir tölu og og-merki (&) sem frátakara fyrir staf. Reiturinn fyrir sniðsíðu er aðeins tiltækur þegar valið er **Sérsniðin vídd** í reitnum **Nota gildi frá**.

**Dæmi**

Til að takmarka víddargildi við stafina „CC“ og þrjár tölur færirðu inn **CC-\#\#\#** sem sniðsíu.

## <a name="entity-backed-dimensions"></a>Einingastuddar víddir

Að búa til einingastuddar fjárhagsvíddir skal í svæðinu **Nota gildi frá** velja kerfisskilgreindar einingar til að byggja fjárhagsvídd á. Fjárhagsvíddargildi eru síðan stofnuð úr þeirri einingu. Til dæmis skal velja Verk til að stofna víddargildi fyrir **Verk**. Víddargildi eru síðan stofnuð fyrir hvert heiti verks. Síðan **Fjárhagsvíddargildi** sýna gildi fyrir eininguna. Ef þessi gildi eru bundin tilteknu fyrirtæki sýnir síðan einnig fyrirtækið.

## <a name="activating-dimensions"></a>Notkun vídda

Þegar fjárhagsvídd er virkjuð er taflan uppfærð þannig að hún felur í sér heiti fjárhagsvíddarinnar. Eyddar víddir eru fjarlægðar. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð. Hins vegar er ekki hægt að nota fjárhagsvídd neins staðar fyrri en hún er gerð virk. Til dæmis er ekki hægt að bæta fjárhagsvídd við lykilskipulag þar til að fjárhagsvídd hefur verið virkjuð. Þegar þú velur **Virkja** eru allar víddir uppfærðar og sýna stöðubreytingar.

## <a name="translations"></a>Þýðingar

Á síðunni **Textaþýðing** er hægt að færa inn texta fyrir valda fjárhagsvídd á mismunandi tungumálum. Á síðunni **Þýðing aðallykils** er hægt að færa inn texta fyrir aðallykil á mismunandi tungumálum. 

## <a name="legal-entity-overrides"></a>Lögaðili hnekkir

Ekki eru allar víddir gildar fyrir alla lögaðila. Þar að auki kunna sumar víddir að vera aðeins viðeigandi fyrir tiltekið tímabil. Í þessum tilfellum er hægt að nota hlutann **Lögaðili hnekkir** til að tilgreina hvaða fyrirtæki ætti ekki að nota víddir fyrir, hver er eigandi og tímabilið sem víddin er virk.

## <a name="deleting-financial-dimensions"></a>Eyðing fjárhagsvídda

Til að viðhalda heilleika gagna er sjaldan hægt að eyða fjárhagsvíddum. Ef reynt er að eyða fjárhagsvíddum eru eftirfarandi skilyrði metin:

- Hefur fjárhagsvíddin verið notuð á einhverjar bókaðar eða óbókaðar færslur, eða einhverri gerð af fjárhagsvíddarsamsetningu?
- Er fjárhagsvíddin notuð í öllu virku lykilskipulagi, ítarleg reglu skipulag fjárhagsvídd eða fjárhagsvídd set?
- Er fjárhagsvídd hluti af sjálfgefinu samþættingarsniði fjárhagsvíddar?
- Hefur fjárhagsvídd verið uppsett sem sjálfgefin vídd?

Ef einhverjum skilyrðum er mætt er ekki hægt að eyða fjárhagsvíddinni.

## <a name="default-dimension-values"></a>Sjálfgefin víddargildi

Þú getur notað gildi frá aðalskrám, svo sem viðskiptavini og lánardrottni, sem sjálfgefin gildi í nýjum víddum. Þegar nýju víddirnar eru búnar til er auðkenni aðalskrárinnar slegið inn í víddargildin fyrir þessar aðalskrár. Til dæmis þegar þú stofnar nýjan viðskiptavin er auðkenni hans slegið inn í vídd viðskiptavinar. Þegar þú býrð til sölupantanir, reikninga eða önnur skjöl sem krefjast auðkennis viðskiptavinar, eru núverandi sjálfgefnar reglur notaðar og auðkenni viðskiptavinarins er bætt við skjalið.

Þessum eiginleika er stjórnað af stillingu í víddinni. Þessi stilling er nefnd **Afrita gildi í þessa vídd fyrir hvert nýtt DimensionName sem er búið til** þar sem **DimensionName** er nafn víddarinnar. Sjálfgefið er að slökkt sé á stillingunni. Hins vegar er hægt að kveikja á henni hvenær sem er.

Ef skrár eru til fyrir víddina eru aðalskrárnar uppfærðar þegar þú kveikir á eiginleikanum. Hins vegar eru núverandi skjöl og færslur ekki uppfærðar.

Ef notað er sniðmát til að stofna aðalskrá skal tryggja að gildi sniðmátsins fyrir aðalvíddina sé autt. Til dæmis ef stofnaðir eru viðskiptavinir úr sniðmáti skal tryggja að vídd viðskiptavinar í sniðmáti sé auð. Víddargildi viðskiptavinar er sjálfgefið úr nýju númeri viðskiptavinar þegar nýr viðskiptavinur er stofnaður.  

## <a name="derived-dimensions"></a>Afleiddar víddir

Þú getur stillt vídd þannig að upplýsingar um aðrar víddir séu sjálfkrafa færðar inn þegar þú slærð inn þá vídd í skjal. Til dæmis, ef þú slærð inn kostnaðarstað 10, er hægt að færa sjálfkrafa inn gildið **20** í deildarvíddina.

Hægt er að setja upp afleidd gildi á víddarsíðunni.

1. Veldu vídd og veldu síðan **Afleiddar víddir**.

    Síðan **Afleiddar víddir** inniheldur hnitanet. Valdi víddarhlutinn er fyrsti dálkurinn í þessu hnitaneti.

2. Bæta þeim hlutum við sem ættu að vera afleiddir. Hver hluti birtist sem dálkur.

Sláðu inn víddarsamsetningar sem ættu að vera fengnar úr víddinni í fyrsta dálknum. Til dæmis, til að nota kostnaðarstaðinn sem víddina sem deildin og staðsetningin koma frá skaltu slá inn kostnaðarstað 10, deild 20 og staðsetningu 30. Þegar þú slærð inn kostnaðarstað 10 í aðalskrá eða á færslusíðu eru deild 20 og staðsetning 30 slegin inn sjálfgefið.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Yfirfærsla núverandi gilda með afleiddum víddum
 
Sjálfgefið er að afleidda víddarferlið hnekkir ekki fyrirliggjandi gildum fyrir afleiddar víddir. Til dæmis, ef þú slærð inn kostnaðarstað 10 og engin önnur vídd er slegin inn eru deild 20 og staðsetning 30 slegin inn sjálfgefið. Hins vegar ef þú breytir kostnaðarstaðnum eru gildin sem þegar hafa verið staðfest ekki breytt. Þess vegna getur þú sett sjálfgefnar víddir í aðalskrár og þessum víddum verður ekki breytt af afleiddum víddum.

Þú getur breytt hegðun afleiddra vídda til að hnekkja núverandi gildum með því að velja **Skipta út núverandi víddargildum fyrir afleiddar víddir** gátreitinn á **Afleiddar víddir** síðu. Ef þetta reit er valið getur þú slegið inn vídd með afleiddum víddargildum og þau afleiddu víddargildi mun hnekkja öll gildi sem þegar eru til staðar. Til að nota fyrra dæmi; ef þú slærð inn kostnaðarstað 10 og engin önnur vídd er slegin inn eru deild 20 og staðsetning 30 slegin inn sjálfgefið. Hins vegar, ef gildin voru þegar deild 50 og staðsetning 60, verða gildi nú breytt í deild 20 og staðsetningu 30.
 
Afleiddar víddir með þessari stillingu skipta ekki sjálfkrafa út núverandi sjálfgefnum víddum þegar víddargildin eru sjálfgefin. Víddargildi eru aðeins hnekkt þegar þú slærð inn nýtt víddargildi á síðu og það eru núverandi afleidd gildi fyrir þá vídd á síðunni.

### <a name="preventing-changes-with-derived-dimensions"></a>Koma í veg fyrir breytingar á afleiddum víddum
 
Þegar þú notar **Bæta við hluta"** á **Afleiddar víddir** síðunni til að bæta við hluta sem afleidd vídd er valkostur gefinn neðst á síðunni **Bæta við hluta** sem gerir þér kleift að koma í veg fyrir breytingar á þessari vídd þegar hún er afleidd á síðu. Sjálfgefið stilling er slökkt svo að það kemur ekki í veg fyrir að unnt sé að breyta afleiddu víddargildunum. Breyttu stillingunni við **Já** ef þú vilt koma í veg fyrir að víddin sé breytt eftir að hún hefur verið afleidd. Til dæmis, ef gildi fyrir deildarvíddina er afleidd frá gildi kostnaðarstaðsvíddarinnar, er ekki hægt að breyta deildarverðinu ef **Koma í veg fyrir breytingar** stilling er stillt á **Já**. 
 
Stillingin kemur ekki í veg fyrir breytingar ef víddargildi er gilt en er ekki skráð í listanum yfir afleiddar víddir. Til dæmis, ef deild 20 er fengin frá kostnaðarstað 10 og þú slærð inn kostnaðarstað 10, þá geturðu ekki breytt deild 20. Hins vegar, ef þú slærð inn kostnaðarsta' 20 og það er ekki á listanum yfir afleiddar víddir fyrir kostnaðarstaðinn, þá er hægt að breyta deildargildinu. 
 
Í öllum tilvikum verður reikningsgildið og öll víddargildin ennþá villuleituð gegn lykilskipulaginu eftir að gildum afleiddu víddanna hafa verið beitt. Ef þú notar afleiddar víddir og þær standast ekki villuleit þega þær eru notaðar á síðu þarftu að breyta gildum afleiddu víddanna áður en þú getur notað þau í færslum. 
 
Þegar þú breytir stærð á **Fjárhagsvíddum** flýtiflipanum er víddinni sem er merkt til að koma í veg fyrir breytingar ekki hægt að breyta. Ef þú ert að slá inn reikning og víddir í hlutafærslustýringunni á síðu er hægt að breyta víddunum. Hins vegar þegar þú færir merkið af hlutafærslustýringunni og færir þig í annað reit eða tekur til aðgerða verður reikningurinn og víddirnar villuleitaðar gagnvart listanum með afleiddu víddunum og lykilskipulaginu til að tryggja að þú hafir slegið inn viðeigandi gildi. 

### <a name="derived-dimensions-and-entities"></a>Afleiddar víddir og einingar

Hægt er að setja upp afleidda víddarhluta og gildi með því að nota einingar.

- Afleidda víddareiningin setur upp keyrsluvíddir og hlutana sem eru notaðir fyrir þessar víddir.
- Eining gilda afleiddra vídda gerir þér kleift að flytja inn gildi sem ætti að vera fengin fyrir hverja keyrsluvídd.

Þegar þú notar einingu til að flytja inn gögn, ef þessi eining flytur inn víddir, eru reglur um afleiddar víddir notar við innflutninginn nema einingin hnekki sérstaklega þessum víddum.

Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Skilgreina fjárhagsvíddir](tasks/define-financial-dimensions.md)
- [Viðhalda sjálfgefnum sniðmátum fjárhagsvídda](tasks/maintain-financial-dimension-default-templates.md)
