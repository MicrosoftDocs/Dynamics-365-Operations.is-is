---
title: Stofna greiðslur lánardrottins með greiðslutillögu
description: Þessi Umfjöllunarefni veitir yfirlit yfir valkosti greiðslutillagna og inniheldur dæmi sem sýna hvernig greiðslutillögur virka.
author: abruer
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57e8ce38241933b16252f1c918b0f763a8f1be08
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837397"
---
# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Stofnun greiðslna lánardrottins með greiðslutillögu

[!include [banner](../includes/banner.md)]

Þessi Umfjöllunarefni veitir yfirlit yfir valkosti greiðslutillagna og inniheldur dæmi sem sýna hvernig greiðslutillögur virka. Greiðslutillögur eru oft notaðar til að stofna greiðslur lánardrottna, þar sem hægt er að nota fyrirspurnina til að velja á skjótan hátt reikninga lánardrottins til greiðslu, á grundvelli skilyrða svo sem gjalddaga og staðgreiðsluafsláttar. 

Fyrirtæki nota oft greiðslutillögur til að stofna greiðslur lánardrottins þar sem hægt er að nota fyrirspurnina um greiðslutillögu til að velja reikningar lánardrottins til greiðslu byggt á gjalddaga, staðgreiðsluafslátt og öðrum skilyrðum. 

Fyrirspurn um greiðslutillögu inniheldur mismunandi flipa, sem hver um sig hefur mismunandi valkosti til að velja reikninga til greiðslu. Flipinn **Færibreyta** inniheldur valkosti sem meirihluti fyrirtækja nota oftast. Á flýtiflipanum **Færslur til að taka með** er hægt að tilgreina hvaða reikningar eða lánardrottnar á að hafa með í greiðslu með skilgreiningu sviða fyrir mismunandi einkenni. Fyrir dæmi, ef þú vilt greiða aðeins tilgreint svið lánardrottna, geturðu skilgreint afmörkun fyrir lánardrottnasvið. Þessi virkni er oft notuð til að að velja reikninga fyrir greiðslumáta. Til dæmis, ef skilgreind er sía þar sem **Greiðsluaðferð** = **Ávísun**, eru aðeins þeir reikningar sem hafa þann greiðslumáta valdir fyrir greiðslu, svo lengi sem þeir einnig uppfyllir önnur skilyrði sem eru tilgreindir í fyrirspurn. **Ítarlegar færibreytur** flipi inniheldur viðbótarvalkosti,°sumir sem hugsanlega ekki eiga við fyrirtækið. Til dæmis inniheldur þessi flipi valkosti fyrir greiðslu reikninga fyrir miðstýrðar greiðslur..

## <a name="parameters"></a>Færibreytur
-   **Velja reikninga eftir** – Reikninga innan tímabilsins sem er tilgreint í svæðunum **Frá dagsetningu** og **Til dagsetningar** er hægt að velja eftir gjalddaga, staðgreiðsluafsláttardagsetningu eða bæði. Ef dagsetning staðgreiðsluafsláttar er valin leitar kerfið fyrst eftir reikningum sem hafa dagsetningu staðgreiðsluafsláttar milli þeirra dagsetninga. Kerfið þá ákveður hvort reikningurinn er hæfur°fyrir staðgreiðsluafslátt með því að nota lotudagsetninguna til að ganga úr skugga um að dagsetning staðgreiðsluafsláttar sé ekki liðin.
-   **Frá dagsetningu** og **Til dagsetningar** – Reikningar sem hafa gjalddaga eða dagsetningu staðgreiðsluafsláttar innan þessa dagsetningabils eru valdar fyrir greiðslu.
-   **Dagsetning lágmarksgreiðslu** – færið Inn dagsetning lágmarksgreiðslu.. Til dæmis tilgreina svæðin **Frá dagsetningu** og **Til dagsetningar** bilið 1. september til 10. september og dagsetning lágmarksgreiðslu er 5. september. Í þessu tilfelli hafa allir reikningar með gjalddaga frá 1. september til 5. september greiðsludagsetninguna 5. september. Hins vegar hafa allir reikningar með gjalddaga frá 5. september til 10. september greiðsludagsetningu sem er sú sama og gjalddagi fyrir hvern reikning.
-   **Upphæðarmörk** – færið Inn hámarksheildarupphæð fyrir allar greiðslur.
-   **Stofna greiðslur án forskoðunar á reikningi** – Ef valkosturinn er settur á **Já**, verða greiðslur stofnaðar strax á **lánardrottnagreiðslur** síðu. Síðunni **Greiðslutillaga** verður sleppt. Þess vegna greiðslur verða stofnaðar fljótlegri hátt. Enn er hægt að breyta greiðslur frá **lánardrottnagreiðslur** síðu. Einnig er hægt að fara til baka á **greiðslutillögu** síðu með því að nota **Breyta reikningum fyrir valda greiðslu** hnappinn.

## <a name="advanced-options"></a>Ítarlegir valkostir
- **Athuga stöðu lánardrottins** – Ef þessi valkostur er stilltur á **Já**, staðfestir kerfið að lánardrottinn er ekki með debet-staða áður en neinn reikningur er greiddur. Ef lánardrottinn er með debet-stöðu, engin greiðsla er stofnuð. Til dæmis gæti lánardrottinn haft kreditreikningar eða greiðslur sem hafa verið bókaðar en ekki enn verið jafnaðar. Í þessum tilfellum ætti ekki að greiða lánardrottni. Þess í stað ætti að jafna kreditreikningar eða greiðslur á móti útistandandi reikningum.
- **Eyða neikvæðum greiðslum** – valkosturinn virkar öðruvísi, eftir því hvort greiðslur eru gerðar fyrir einstaka reikninga eða samtölu reikninga sem uppfylla skilyrði greiðslu. Þessi hegðun er skilgreind á greiðsluhætti.
- **Greiðsla fyrir hvern reikning** – Ef valkosturinn **Eyða neikvæðum greiðslum** er stilltur á **Já**, og ójafnaður reikningur og greiðsla er til fyrir lánardrottin, aðeins reikninginn er valinn fyrir greiðslu. Greiðslan°er ekki jafnað á móti reikningi. Ef í **Eyða neikvæðum greiðslum** valkostur er stilltur á **Nei**, og reiknings og greiðslu ekki eru kostnaðarjafnaðar jafnaðar, reikningur og greiðsla eru valdar fyrir greiðslu. Greiðsla er stofnuð fyrir greiðsluna og endurgreiðsla (neikvæð greiðsla) er stofnuð fyrir greiðsluna.
- **Greiðsla fyrir samtölu reikninga** - Ef valkosturinn **Eyða neikvæðum greiðslum** er stilltur á **Já**, og ójafnaður reikningur og greiðsla er til fyrir lánardrottin, bæði ójafnaði reikningurinn og greiðsla eru valdar fyrir greiðslu og upphæðir er bætt saman til að fá fram heildarupphæð greiðslu. Eina undantekning eref samtalan leiðir til endurgreiðslu. Í þessu tilfelli er hvorki reikningur eða greiðsla valinn. Ef valkosturinn **Eyða neikvæðum greiðslum** valkosturinn er stilltur á **Nei** og reikningur og greiðsla eru ekki jöfnuð eru bæði reikningurinn og greiðslan valin fyrir greiðslu og upphæðum er bætt við til að fá heildarupphæð greiðslu.
- **Prenta skýrslu eingöngu** – þessi valkostur er Stilltur á **Já** til að sjá niðurstöður greiðslutillagna í skýrslu, en°án þess að stofna neinar greiðslur.
- **Taka með reikninga lánardrottna frá öðrum lögaðilum** – Ef fyrirtækið hefur miðstýrðar vinnslu til greiðslu og greiðslutillagan á að taka með reikninga frá öðrum lögaðilum sem eru teknar með í leitarskilyrðum, setjið þennan valkost á **Já**.
- **Bjóða aðskildar greiðslur lánardrottins fyrir hvern lögaðila** – Ef þessi valkostur er stilltur á **Já**, er aðskilin greiðsla stofnuð fyrir hvern lögaðila fyrir hvern lánardrottinn. Lánardrottinn greiðslunnar er lánardrottinn úr reikningi frá hverjum lögaðila. Ef þessi valkostur er stilltur á **Nei**, og sami lánardrottinn á reikninga í mörgum lögaðilum, er ein greiðsla stofnuð fyrir heildarupphæð valinna reikninga. Lánardrottinn greiðslunnar er lánardrottinn núverandi lögaðila. Ef lánardrottnalykillinn er ekki til í núverandi lögaðila, er notaður lánardrottnalykill fyrsta reikningsins sem þarf að greiða.
- **Greiðslugjaldmiðill** – Þetta svæði tilgreinir þann gjaldmiðil sem allar greiðslur eru stofnaðar í. Ef gjaldmiðill er ekki skilgreindur, er hver reikningur greiddur í gjaldmiðli reikningsins.
- **Greiðsluvikudagur** – færið Inn dag vikunnar þegar greiðsla á að fara fram. Þetta svæði er bara notað ef greiðslumátinn er sett upp með samtals reikninga til greiðslu á ákveðnum degi vikunnar.
- **Gerð mótlykils** og **Mótlykill** – Stilla þessi svæði til að skilgreina gerð lykils (eins og **Fjárhag** eða **Banka**) og mótlykil (til dæmis tiltekins bankareiknings). Greiðsluhátt fyrir reikninginn skilgreinir sjálfgefna gerð mótlykils og mótlykil, en hægt er að nota svæðin til að hnekkja sjálfgefnum gildum.
- **Samantekin greiðsludagsetning** – Þetta er aðeins notað þegar reiturinn **Tímabil** á greiðslumáta er stilltur á **Samtals**. Ef dagsetning er tilgreind eru allar greiðslur stofnaðar á þessum degi. **Dagsetning lágmarksgreiðslu** svæðið er hunsað.
- **Auka síur** – Á flýtiflipanum **Færslur til að taka með** er hægt að skilgreina aukabil skilyrða. Fyrir dæmi, ef þú vilt greiða aðeins svið lánardrottna, geturðu skilgreint afmörkun fyrir lánardrottnasvið. Þessi virkni er oft notuð til að að velja reikninga fyrir greiðslumáta. Til dæmis, ef skilgreind er sía þar sem **Greiðsluaðferð** = **Ávísun**, eru aðeins þeir reikningar sem hafa þann greiðslumáta valdir fyrir greiðslu, svo lengi sem þeir einnig uppfyllir önnur skilyrði sem eru tilgreindir í fyrirspurn.

## <a name="scenarios"></a>Sviðsmyndir

| Lánardrottinn | Reikningur | Dagsetning reiknings | Reikningsupphæð | Gjalddagi | Dagsetning staðgreiðsluafsláttar | Upphæð staðgreiðsluafsláttar |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. júní      | 500,00         | 15. júlí  | 29. júní            | 10,00                |
| 3050   | 1002    | 20. júní      | 600,00         | 20. júlí  | 4. júlí             | 12                |
| 3075   | 1003    | 15. júní      | 250,00         | 29. júní  |                    | 0,00                 |
| 3100   | 1004    | 17. júní      | 100,00         | 17. júlí  | 1. júlí             | 1,00                 |

1. Júlí greiðir Arnie lánardrottnum. Hún notar greiðslutillögu til að auðvelda sér að ljúka þessu verki á hagkvæman hátt.

### <a name="option-1-by-cash-discount"></a>Valkostur 1: Eftir staðgreiðsluafslætti

Apríl velur **staðgreiðsluafsláttur** sem gerð reikningstillögu. Hún færir inn dagsetningatímabilið 26.júní til 10.júlí. Eftirfarandi reikningar eru ekki teknir með í tillögunni:

-   1002, þar sem afsláttardagsetningin 4. Júlí er svið greiðsludagsetninga.
-   1004, þar sem afsláttardagsetningin 1. Júlí er svið greiðsludagsetninga.

Eftirfarandi reikningar eru ekki teknir með í tillögunni:

-   1001, því afsláttardagsetningin 29.júní er þegar liðin, þessi reikningur er ekki lengur hæfur til staðgreiðsluafsláttar.
-   1003, þar sem þessi reikningur er ekki með afsláttardagsetningu.

### <a name="option-2-by-due-date"></a>Valkostur 2: Eftir gjalddaga

Arnie velur **Gjalddagi** sem gerð reikningstillögu. Hún færir inn dagsetningatímabilið 26.júní til 10.júlí. Eftirfarandi reikningar eru ekki teknir með í tillögunni:

-   1003, þar sem afsláttardagsetningin 29. Júní er innan tímabils greiðsludagsetninga.

Eftirfarandi reikningar eru ekki teknir með í tillögunni:

-   1001, þar sem gjalddaginn 15.Júlí er utan tímabils greiðsludagsetninga.
-   1002, þar sem gjalddaginn 20.Júlí er utan tímabils greiðsludagsetninga.
-   1004, þar sem gjalddaginn 17.Júlí er utan tímabils greiðsludagsetninga.

### <a name="option-3-by-due-date-and-cash-discount"></a>Valkostur 3: Eftir gjalddagi og dagsetning staðgreiðsluafsláttar

Arnie velur **Gjalddagi og staðgreiðsluafsláttur** sem gerð reikningstillögu. Hún færir inn dagsetningatímabilið 26.júní til 10.júlí. Eftirfarandi reikningar eru ekki teknir með í tillögunni:

-   1003, þar sem afsláttardagsetningin 29. Júní er innan tímabils greiðsludagsetninga.
-   1002, þar sem afsláttardagsetningin 4. Júlí er svið greiðsludagsetninga.
-   1004, þar sem afsláttardagsetningin 1. Júlí er svið greiðsludagsetninga.

Eftirfarandi reikningar eru ekki teknir með í tillögunni:

-   1001, þar sem 29.Júní dagsetning afsláttar er þegar liðin, því er þessi reikningur er ekki lengur hæfur fyrir staðgreiðsluafslátt og gjalddaginn 15. Júlí er einnig utan dagsetningasviðs

## <a name="country-specific-considerations"></a>Atriði sem varða tiltekin lönd
### <a name="norway"></a>Noregur

#### <a name="dimension-control"></a>Víddarstýring

Víddarstjórnun gera notandanum kleift að stjórna flokkun myndaðra lína með greiðslutillögu og stilla sjálfgefnar víddir á grundvelli fjárhagsvíddir sem notaðar eru fyrir notaða reikninga. Hvað varðar Noreg er hver fjárhagsvíddarflipi fyrir hvern greiðsluhátt þar sem þú getur virkjað víddarstjórnun sem og að vikja flokkun fyrir hverja vídd. Tiltækir valmöguleikar eru:

-   **Víddarstýring** svæðið er gert óvirkt. Greiðslutillaga hagar sér eins og í hverju öðru landi.
-   **Víddarstýring** svæðið er virkjað án þess að skilgreina víddir frekar. Án þess að taka tillit til vídda verða stofnaðar greiðslutillögur. Stofnuð færsla erfir engar víddir úr notaðri færslu.
-   **Víddarstýring** svæðið er virkjað og frekari víddir eru virkjaðar. Nú skilgreinirðu hvernig víddir verða afritaðar í færslubókina. Til dæmis: • Veljið gátreitinn **BusinessUnit** til þess að stofna greiðslutillögu fyrir hverja viðskiptaeiningu sem greiðslumáta, • Veljið gátreitinn **kostnaðarstaður** til þess að stofna greiðslutillögu sem greiðsluhátt fyrir hvern kostnaðarstað

> [[!NOTE]
> Ef þú velur fleiri en eina vídd í þriðja valkostinum er greiðslutillaga búin til fyrir víddarsamsetninguna.

#### <a name="bank-account-selection"></a>Val á bankareikningi

Þú getur skilgreint staðlaðan greiðslulykil fyrir debet samkvæmt greiðsluhætti óháð um hvaða land ræðir. Þetta er stillt í greiðslulínur sem voru myndaðar af tillögu. Með aðgerðinni bankareikningur, er hægt að skilgreina mörgum bankareikningum fyrir debet sem er stjórnað eftir vídd og gjaldmiðill eða samsetningu þessara til að nota mismunandi bankareikninga fyrir debet, allt eftir samsetningu hvers fyrir sig. Hægt er að setja upp þessar samsetningar í **Greiðsluaðferðir** síðu með því að nota **bankareikninga** hnappinn sem er tiltæk fyrir hvern greiðslumáta með **Gerð bókunarlykils** = **Banka**.



