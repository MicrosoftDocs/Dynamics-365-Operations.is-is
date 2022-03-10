---
title: Yfirlit yfir reikningsjöfnun viðskiptaskulda
description: Reikningsjöfnun viðskiptaskulda felst í því að bera saman reikning lánardrottins, innkaupapöntun og upplýsingar á fylgiseðli.
author: sunfzam
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "27361"
- intro-internal
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2959df58dbde71ba516c1a230e64d38b885c23f5
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358265"
---
# <a name="accounts-payable-invoice-matching-overview"></a>Yfirlit yfir reikningsjöfnun viðskiptaskulda

[!include [banner](../includes/banner.md)]

Reikningsjöfnun viðskiptaskulda felst í því að bera saman reikning lánardrottins, innkaupapöntun og upplýsingar á fylgiseðli.

Þegar þessi skjöl eru látin samsvara sér, mismunur milli þessi skjöl kallast misræmi í samsvörun. Misræmi er borinn saman við vikmörk sem tilgreind eru. Ef jöfnunarmisræmi fer yfir vikmarkaprósenta eða upphæð, birtast stemma frávikstákn í síðunni reikningur Lánardrottins og síðunni reikningsferill og samsvörunarupplýsingar 

Til dæmis, Færð er inn innkaupapöntun með einni línuvöru fyrir 1.000 rafhlöður á verðinu 1,00 hver. Innkaupapöntunin er samþykkt og send til lánardrottins. Lánardrottinn sendir 1.000 rafhlöður og færður er inn innhreyfingarskjal afurða fyrir 1.000 rafhlöður á verðinu 1,00 hver. Birgðakostnaður rafhlaðanna er uppfærður með þessu verði. 

Reikningur berst fyrir 1.000 rafhlöður á 1,10 stykkið. Reglur lögaðila þíns leyfa 5% nettó vikmörk einingarverðs fyrir þessarar vörutegundar. Verðið 1,05 yrði samþykkt en ekki 1,10. Þegar reikningsupplýsingarnar eru færðar inn finnst jöfnunarmisræmi í verði og hægt er að vista reikninginn þar til misræmið er leyst.

Þú getur notað eftirfarandi gerðir af **Samsvörun viðskiptaskuldareikninga**:

-   **Samtölur reiknings stemma** – Jafnaðu heildarupphæðir á reikningi við heildarupphæðir á innkaupapöntuninni. Þessi gerð af reikningsjöfnun inniheldur minnsta magn upplýsinga, svo hægt er að nota þennan valkost til að setja upp stýringar sem minnka tíma sem starfsmaður þarf til að skoða upplýsingar um reikningsjöfnun.
-   **Tvíhliða samsvörun** – Passaðu verðupplýsingarnar á reikningnum við verðupplýsingarnar á innkaupapöntuninni.
-   **Þríhliða samsvörun** – Passaðu verðupplýsingarnar á reikningnum við verðupplýsingarnar á innkaupapöntuninni. Jafna einnig upplýsingar um magn á reikningi við upplýsingar um magn á innhreyfingarskjölum afurða sem eru valdar fyrir reikningnum.
-   **Gjöld passa** – Passaðu gjaldaupplýsingarnar (upphæðir) á reikningnum við gjaldaupplýsingarnar (upphæðir) á innkaupapöntuninni.

> [!NOTE]
> Hægt er að ljúka öðrum skjámyndum reikningaprófun með reikningsreglur lánardrottins. 

Tvíhliða samsvörun og þríhliða samsvörun stemma alltaf við verðupplýsingar eftir einingaverði. Einnig er hægt að skilgreina þessar samsvörunarreglur til að jafna upplýsingar um verð eftir verðsamtölunni.
-   **Nettó einingarverðssamsvörun** – Samsvöruðu verðupplýsingar fyrir tvíhliða samsvörun eða þríhliða samsvörun með því að bera saman nettó einingarverð fyrir hverja línu á reikningnum við samsvarandi nettó einingarverð á innkaupapöntuninni. Nettó einingaverð er ákvarðað af eftirfarandi formúlu: nettóupphæð línunnar, deilt með magni línunnar.
-   **Verðsamtölur passa saman** – Passaðu verðupplýsingar fyrir tvíhliða samsvörun eða þríhliða samsvörun með því að bera saman nettóupphæð (verðheild) fyrir hverja línu á reikningi við samsvarandi nettóupphæð á innkaupapöntuninni. Nettóupphæð ákvarðast af eftirfarandi formúlu: *(einingarverð \* línumagn) + línugjöld - línuafsláttur*. Þegar samtölur verðs eru samsvaraðar eftir prósentu ber kerfið saman gildi með færslugjaldmiðlinum. Þegar samtölur verðs eru samsvaraðar eftir upphæð ber kerfið saman gildi með bókhaldsgjaldmiðlinum. Þegar innkaupapöntunarlína er reikningsfærð að hluta til verður gerð samsvarandi jöfnun á síðasta reikningi fyrir þá línu. 

Venjulega eru reikningssamsvörunarútreikningar sjálfkrafa framkvæmdir þegar þú breytir reikningum lánardrottins á **Reikningur seljanda** síðu. Einnig er hægt að framkvæma reikningsjöfnun eftir þörfum. Samsvörun reikninga á eftirspurn er undir stjórn lögaðilans **Uppfærðu reikning sjálfkrafa** haus staða á **Færibreytur viðskiptaskulda** síðu á **Staðfesting reikninga** flipa. Samsvörun reikninga er einnig hægt að framkvæma sem hluta af endurskoðunarferli reikninga. Þú getur skoðað niðurstöður samsvörunar reikninga á **Reikningur seljanda** síðu og tengdar reikningssamsvörunarsíður.

## <a name="invoice-totals-matching"></a>Samtölur reiknings stemma
Hægt er að nota samtölur reikningsjöfnunar sem stemma til að ganga úr skugga um að heildarupphæð reiknings hviki ekki frá upphæðum sem búist er við meira en innan ásættanlegra vikmarka. Sex heildartölur eru bornar saman á **Samtölur reikninga samsvara upplýsingum** síðu, eins og sýnt er í eftirfarandi töflu. Ef leyfileg vikmörk fyrir samtölur reiknings stemma er 20% er 100% frávikaprósenta fyrir heildarafsláttarupphæð er talin jöfnunarmisræmi.

| Reitur samtölu    | Raunveruleg heildarupphæð reiknings | Áætlaðar heildarupphæð reiknings | Frávikaprósenta | Samsvörunarstaða |
|----------------|----------------------|------------------------|---------------------|--------------|
| Staða        | 495,00               | 495,00                 | 0%                  | Stóðst       |
| Heildarafsláttur | 0,00                 | 9,90                   | 100%                | Stóðst ekki       |
| Gjöld        | 64,90                | 64,90                  | 0%                  | Stóðst       |
| Virðisaukaskattur      | 139,98               | 137,50                 | 2%                  | Stóðst       |
| Sléttun      | 0,00                 | 0,00                   | 0%                  | Stóðst       |
| Reikningsupphæð | 699,88               | 687,50                 | 2%                  | Stóðst       |

Samsvörun reikninga er stjórnað af lögaðilanum **Samsíða heildartölur reikninga** kveikja á **Færibreytur viðskiptaskulda** síðu. Jöfnun er framkvæmd í áætlaðra samtalna reiknings og raunverulegra samtalna reiknings. Áætluð heildarupphæð reiknings eru reiknaðar út frá verð, gjöld og vsk-upplýsingar úr innkaupapöntun og magni úr magninu úr reikningnum.

## <a name="two-way-price-totals-matching"></a>Tvíhliða, samsvörun samtalna verðs
Nota tvíhliða jöfnun til að aðstoða við að tryggja að frávikið á milli upplýsingar um verð á innkaupapöntuninni og reikningnum er innan ásættanlegra vikmarka. Hægt er að bera saman upplýsingar um verð fyrir nettóupphæð á hverja línu á reikningi og allar reikningslínur í bið og áður bókaðar, með nettóupphæð samsvarandi innkaupapöntunarlínu. Þetta kallast samsvörun á samtölur verðs. 

Jöfnun samtalna verðs getur verið byggt á prósentu, upphæð eða prósenta og upphæð. 

Ef vikmarkaprósenta samtölu innkaupaverðs er tilgreind, eru fimm reitirnir bornir saman eins og sýnt er í eftirfarandi töflu. Þar sem vikmarkaprósenta heildar innkaupsverðs er 10% táknar fráviksprósenta heildarverðs upp á 50% misræmi í jöfnun.

| Samsvörunarstaða | Nettóupphæð reiknings | Áætluð nettóupphæð | Ójöfnuð samtala innkaupaverðs (fráviksupphæð) | Ójafnað samtala innkaupaverðs fyrir prósentu (fráviksprósenta) | Vikmarkaprósenta samtölu innkaupaverðs |
|--------------|--------------------|---------------------|--------------------------------------------------|--------------------------------|---------------------------|
| Stóðst       | 105,00             | 100,00              | 5,00                                             | 5%                             | 10%                 |
| Stóðst ekki       | 150,00             | 100,00              | 50,00                                            | 50%                            | 10%                     |

Ef vikmarkaupphæð samtölu innkaupaverðs er tilgreind, eru fimm reitirnir bornir saman eins og sýnt er í eftirfarandi töflu. Þar sem vikmarkaupphæð heildar innkaupsverðs er 100.00% táknar fráviksupphæð heildarverðs upp á 105.00 misræmi í jöfnun.

| Samsvörunarstaða | Nettóupphæð reiknings | Áætluð nettóupphæð | Ójöfnuð samtala innkaupaverðs (fráviksupphæð) | Ójafnað samtala innkaupaverðs í bókhaldsgjaldmiðill (fráviksupphæð) | Vikmörk samtölu innkaupaverðs |
|--------------|--------------------|---------------------|-----------------------------------------------|-------------------------------|--------------------------------|
| Stóðst       | 150,00             | 100,00              | 50,00                                            | 50,00                    | 100,00                         |
| Stóðst ekki       | 205,00             | 100,00              | 105,00                                           | 105,00                  | 100,00                         |

Ef jöfnun verðsamtalna er sett upp með prósentum vikmörk og upphæð vikmörk, stundum er vísað til sem ekki--fara upphæð, bæði vikmörk teknar til athugunar þegar meta hvort lína hafi jöfnunarmisræmi. Ef prósentan eða upphæð sem fer vikmörk, eins og sýnt er í línum 150,00 og 205,00 í eftirfarandi töflu, hefur línan jöfnunarmisræmi.

| Samsvörunarstaða | Nettóupphæð reiknings | Áætluð nettóupphæð | Ójafnað samtala innkaupaverðs fyrir prósentu (fráviksprósenta) | Vikmarkaprósenta samtölu innkaupaverðs | Ójafnað samtala innkaupaverðs í bókhaldsgjaldmiðill (fráviksupphæð) | Vikmörk samtölu innkaupaverðs |
|--------------|--------------------|---------------------|-----------------------------|------------------|----------------------------------|--------------------------------|
| Stóðst       | 105,00             | 100,00              | 5%                     | 10%                         | 5,00           | 100,00                         |
| Stóðst ekki       | 150,00             | 100,00              | 50%                   | 10%                     | 50,00            | 100,00                         |
| Stóðst ekki       | 205,00             | 100,00              | 105%                 | 10%                      | 105,00                                  | 100,00                         |

Tvíhliða samsvörun er stjórnað af lögaðilanum **Línusamsvörun stefna** sviði á **Færibreytur viðskiptaskulda** síðu. Það fer eftir úrvali í **Leyfa hnekkingu samsvörunarstefnu** reit, getur þú valið tvíhliða samsvörun fyrir tiltekinn seljanda, vöru eða samsetningu vöru og lánardrottins á **Samsvörunarstefna** síðu, og fyrir tiltekna innkaupapöntun á **Pöntun** síðu.

Samsvörun verðsamanlags er stjórnað af lögaðilanum **Samsvarandi heildarverð** sviði á **Færibreytur viðskiptaskulda** síðu. Verð prósentuvikmörk heildarinnkaupaverðs og vikmarkaupphæð (ekki-fara -yfir upphæð) eru einnig tilgreindar á þeirri síðu.

## <a name="two-way-net-unit-price-matching"></a>Tvíhliða, Samsvörun nettóeiningaverðs
Nota tvíhliða jöfnun til að aðstoða við að tryggja að frávikið á milli upplýsingar um verð á innkaupapöntuninni og reikningnum er innan ásættanlegra vikmarka. Hægt er að bera saman upplýsingar um verð fyrir nettóeiningaverð hvers atriðis á reikningnum. Þetta kallast Samsvörun nettóeiningaverðs 

Níu línuupphæðir eru bornar saman á **Samsvörunarupplýsingar reikninga** síðu, eins og sýnt er í eftirfarandi töflu. Ef leyfileg verðvikmörk fyrir jöfnun nettóeiningaverðs er 10% er 22.61% frávik fyrir nettóeiningaverð talin jöfnunarmisræmi.

| Reitur línu                    | Reikningsvirði | Gildi Innkaupapöntunar | Frávikaprósenta | Samsvörunarstaða |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Einingarverð                    | 55,40         | 55,38                | 0%                  | Stóðst       |
| Einingarverð                    | 1,00          | 1,00                 | 0%                  | Stóðst       |
| Gjöld á innkaupum          | 50,00         | 0,00                 | 100%                | Stóðst ekki       |
| Afsláttur                      | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Afsláttarprósenta              | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Samvalsafsláttur            | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Samvalsafsláttarprósenta | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Nettóupphæð                    | 271,60        | 221,52               | 22,61%              | Stóðst ekki       |
| Nettó einingaverð                | 67,9000       | 55,3800              | 22,61%              | Stóðst ekki       |

Tvíhliða samsvörun er stjórnað af lögaðilanum **Línusamsvörun stefna** sviði á **Færibreytur viðskiptaskulda** síðu. Það fer eftir úrvali í **Leyfa hnekkingu samsvörunarstefnu** reit, getur þú valið tvíhliða samsvörun fyrir tiltekinn seljanda, vöru eða samsetningu vöru og lánardrottins á **Samsvörunarstefna** síðu, og fyrir tiltekna innkaupapöntun á **Pöntun** síðu. 

Nettó verðsamsvörun er stjórnað af lögaðilanum **Virkja reikningssamsvörun** sviði á **Færibreytur viðskiptaskulda** síðu. Hægt er að stilla vikmörk fyrir nettó einingarverð fyrir vörur, vöruflokka, lánardrottna, lánardrottnahópa, vöru- og lánardrottnasamsetningar eða lögaðila með því að nota **Verðvikmörk** síðu.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a>Tvíhliða, samsvörun samtalna verðs og samsvörun nettóeiningaverðs
Þú getur notað samsvörun samtalna verðs og samsvörun nettóeiningaverðs saman. Þetta dæmi gerir ráð fyrir að eftirfarandi skilgreiningu:

-   Vikmörk Nettóeiningaverðs fyrir USB Drif vöru er 10%.
-   Vikmörk Samsvörunar samtalna verðs fyrir lögaðilann er 15% eða 500,00.

Innkaupapöntun inniheldur eftirfarandi línu.

| Vörunúmer | Magn | Einingarverð | Nettóupphæð |
|-------------|----------|------------|------------|
| USB drif   | 1.000    | 10,00      | 10.000,00  |

Þrjár reikningar eru færðir inn, eins og sýnt er í eftirfarandi töflu. Það er jöfnunarmisræmi fyrir Reikningur 3 þar sem frávik á uppá 1,880.00 er hærri en upphæð vikmarka heildarinnkaupsverðs uppá 500,00. Fyrir samsvörun samtalna verðs, inniheldur nettóupphæð reiknings alla áður bókaða reikninga auk reikninginn sem verið er að vinna að núna.

| Vörunúmer          | Magn | Einingarverð | Nettóupphæð | Verðsamsvörun | Samtala verðs jöfnuð |
|----------------------|----------|------------|------------|-------------|-------------------|
| Reikningur 1: USB drif | 800      | 10,80      | 8.640,00   | Stóðst      | Stóðst            |
| Reikningur 2: USB drif | 100      | 10,80      | 1.080,00   | Stóðst      | Stóðst            |
| Reikningur 3: USB drif | 200      | 10,80      | 2.160,00   | Stóðst      | Stóðst ekki            |
| Samtals                |          |            | 11.880,00  |             |                   |

## <a name="three-way-matching"></a>Þríhliða jöfnun

Nota þríhliða jöfnun til að aðstoða við að tryggja að frávikið á milli upplýsingar um verð á innkaupapöntuninni og reikningnum er innan ásættanlegra vikmarka og til að ganga úr skugga um að magnið á reikningnum samsvari magninu á viðkomandi innhreyfingarskjal afurða.

Sömu línuupphæðir eru borin saman á upplýsingasíða reikningsjöfnun, eins og fyrir tvíhliða samsvörun. Þar að auki er magn á reikningi samsvarað við magn innhreyfingarskjal afurða sem hafa verið mótteknar. Ef magn á reikningi eru önnur en jafnað innhreyfingarskjali afurða , er til staðar villa í magnsamsvörun.

| Reitur línu                    | Reikningsvirði | Gildi Innkaupapöntunar | Frávikaprósenta | Samsvörunarstaða |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Einingarverð                    | 55,40         | 55,38                | 0%                  | Stóðst       |
| Einingarverð                    | 1,00          | 1,00                 | 0%                  | Stóðst       |
| Gjöld á innkaupum          | 50,00         | 0,00                 | 100%                | Stóðst ekki       |
| Afsláttur                      | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Afsláttarprósenta              | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Samvalsafsláttur            | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Samvalsafsláttarprósenta | 0,00          | 0,00                 | 0%                  | Stóðst       |
| Nettóupphæð                    | 271,60        | 221,52               | 22,61%              | Stóðst ekki       |
| Nettó einingaverð                | 67,9000       | 55.3800              | 22,61%              | Stóðst ekki       |

| Reitur línu                     | Reikningsvirði | Samsvörunarstaða |
|--------------------------------|---------------|--------------|
| Magn á reikningi               | 4,00          |              |
| Samtala paraðra innhreyfinga afurða | 0,00          | Stóðst ekki       |

Þríhliða samsvörun er stjórnað af lögaðilanum **Línusamsvörun stefna** sviði á **Færibreytur viðskiptaskulda** síðu. Það fer eftir úrvali í **Leyfa hnekkingu samsvörunarstefnu** reit, getur þú valið þríhliða samsvörun fyrir tiltekinn seljanda, hlut eða samsetningu vöru og lánardrottins á **Samsvörunarstefna** síðu, og fyrir tiltekna innkaupapöntun á **Pöntun** síðu.

## <a name="charges-matching"></a>Gjöld stemma
Hægt er að nota jöfnun gjalda til að ganga úr skugga um að upphæðir gjalda hviki ekki frá upphæðum sem búist er við meira en innan ásættanlegra vikmarka. Heildarupphæðir fyrir hvern gjaldkóða sem á við reikninginn og innkaupapöntunina eru bornar saman í **Bera saman gjaldgildi - Reikningur:** síðu, eins og sýnt er í eftirfarandi töflu. Ef leyfilegt vikmörk fyrir gjaldkóðann er 25% er 99,999,999,999.99% frávikshlutfallið fyrir **Kóði leyfisgjalda** er talið samsvarandi misræmi.

> [!NOTE] 
> Fráviksprósenta uppá 99,999,999,999.99 % þýðir að áætluð upphæð byggð á innkaupapöntun er núll og raunveruleg upphæð á reikningi er jákvætt gildi. 

| Samsvörunarstaða gjalds | Kóði reikningsgjalda | Raunveruleg reiknuð heildarupphæð | Áætluð reiknuð heildarupphæð | Upphæð frávika | Frávikaprósenta | Vikmarkaprósenta |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Stóðst ekki               | Leyfi              | 25                            | 0                               | 25              | 99.999.999.999,99%  | 25%                  |
| Stóðst               | Farmur              | 200                           | 200                             | 0               | 0%                  | 25%                  |
| Stóðst ekki               | Flýta             | 4                             | 2                               | 2               | 100%                | 25%                  |

Samsvörun gjalda er stjórnað af lögaðilanum **Samsvörunargjöld** kveikja á **Færibreytur viðskiptaskulda** síðu. Þú getur sett upp frávikaprósentur fyrir gjöld á **Hleðsluvikmörk** síðu.

> [!NOTE]
> Gjaldsamsvörun er aðeins framkvæmd á gjaldakóðum sem **Berðu saman innkaupapöntun og reikningsgildi** skipti er valið á **Gjaldkóði** síðu.

## <a name="related-functionality"></a>Tengdar aðgerðir
Reikningar lánardrottna eru oft byggðir á innhreyfingarskjal afurða sem standa fyrir raunverulegri sendingu, í stað innkaupapöntunum. Stundum passa reikningsupphæðir ekki við upphæðir innkaupapantana og stundum er sent magn ekki hið sama og magn á reikningi. Hægt er að hjálpa til við að stjórna þessum upplýsingum á eftirfarandi vegu:
-   Stofna reikning lánardrottins á grundvelli innhreyfingarskjal afurða Innhreyfingarskjöl afurða eru sjálfkrafa lagðir til fyrir reikninga, og notandi getur valið hvaða innhreyfingarskjal afurða skuli nota. Einnig er hægt að velja tilteknar línuatriði innhreyfingarskjals afurðar úr mörgum innkaupapöntunum ef þarf.
-   Skoðið og samþykkið magnmismun milli reikningsfærða magnsins á reikningnum og móttekna magnsins á innhreyfingarskjal afurða. Ef mismunur er má vista reikninginn og stemma hann síðar af við annan innhreyfingarskjal afurða eða breyta reikningsmagninu svo að það stemmi við móttekna magnið.
-   Færið inn reikningsupphæðir sem voru ekki með á upphaflega innkaupareikningnum svo að reikningsupplýsingarnar stemmi við reikninginn frá lánardrottninum. Hægt er að bera saman gjöld fyrir innkaupapöntunum við gjöld fyrir reikningum. Ef með þarf er hægt að bæta gjöldum við reikninga og úthluta á reikningslínur.
-   Skoðið og samþykkið verðmisræmi milli nettó einingarverðs á reikningi og á innkaupapöntun. Hægt er að setja upp vikmarkaprósentur verðs fyrir lögaðila, lánardrottna og vörur. Ef línuverð á reikningi lánardrottins er ekki innan vikmarkanna er hægt að geyma reikninginn þar til hann er samþykktur til bókunar eða þar til leiðrétting kemur frá lánardrottni.

Frekari upplýsingar eru í [Þríhliða jöfnunarreglur](three-way-matching-policies.md) og [Setja upp sannprófun reikningsjöfnunar viðskiptaskulda](tasks/set-up-accounts-payable-invoice-matching-validation.md). 






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
