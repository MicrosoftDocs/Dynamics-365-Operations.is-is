---
title: "Yfirlit Uppgjörs fyrir miðstýrð greiðslur."
description: "Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota lögaðila sem sér um allar greiðslur. Þetta eyðir þörfinni á því að færa inn sömu færsluna í mörgum lögaðilum og sparar tíma með því að einfalda greiðslutillagnaferlið, jöfnunarferlið, breytingar á opnum færslum, og breytingar á lokuðum færslum fyrir miðstýrðar greiðslur."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: dd8e6fb1100cdbb8f0b5ad778b322243c72529ba
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="settlement-overview-for-centralized-payments"></a>Yfirlit Uppgjörs fyrir miðstýrð greiðslur.

[!include[banner](../includes/banner.md)]


Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota lögaðila sem sér um allar greiðslur. Þetta eyðir þörfinni á því að færa inn sömu færsluna í mörgum lögaðilum og sparar tíma með því að einfalda greiðslutillagnaferlið, jöfnunarferlið, breytingar á opnum færslum, og breytingar á lokuðum færslum fyrir miðstýrðar greiðslur. 

Þegar viðskiptavinar- eða lánardrottinsgreiðsla er færð inn í einu lögaðila og jöfnuð með reikningi sem var færður inn í öðru lögaðila er viðkomandi jöfnun og færslur sjálfkrafa gerðar fyrir hvort lögaðila. Jöfnunarfærsla er stofnuð fyrir hverja samsetningu reiknings og greiðslu í færslunni. Hver jöfnunarfærsla fær úthlutað nýju fylgisjalsnúmeri sem er byggð á númeraröð greiðsluskjals sem tilgreind er á í**Færibreytur viðskiptakrafna** síðu fyrir viðskiptavini og á **Færibreytur viðskiptaskulda** síðu fyrir lánardrottna. 

Ef viðbótar jöfnunarfærslur eru búnar til fyrir greiðsluafslætti, endurmat á erlendum gjaldmiðli, auramismun, ofgreiðslu eða vangreiðslu fá þær úthlutað síðari dagsetningu greiðslu- eða reikningsfærslunnar. Ef jöfnun á sér stað eftir að greiðslan er bókuð nota jöfnunarfærslurnar jöfnunarbókunardagsetninguna sem er tilgreind í skjámyndinni **Jafna opnar færslur**.
Bókunargerðir, færslugerðir og sjálfgefnar lýsingar
----------------------------------------------------------

Færslur fyrir fylgiskjöl samstæðujöfnunar nota bókunargerð samstæðujöfnunar, og samstæðujöfnun viðskiptavinar og færslugerðina samstæðujöfnun lánardrottins. Setja verður upp upplýsingar um færslugerðina í síðunni **sjálfgefnar lýsingar**. 

Eftirfarandi færslugerðir eru tiltækar til notkunar í eins fyrirtækis jöfnun og jöfnun milli fyrirtækja:

-   Jöfnun
-   Staðgreiðsluafsláttur
-   Endurmat á erlendum gjaldmiðli (inniheldur endurmat á innleystan og óinnleystan endurmat á erlendum gjaldmiðli)
-   Auramismunur
-   Ofgreiðsla/vangreiðsla

Hægt er einnig að skilgreina sjálfgefnar lýsingar fyrir fylgiskjöl samstæðujöfnunar.

<a name="currency-exchange-gains-or-losses"></a>Gengistap og -hagnaður
---------------------------------

Gengið sem er notað í viðskiptavina- eða lánardrottnafærslum er geymt með færslunni. Innleyst tap eða hagnaður af gengi gjaldmiðils er bókað annaðhvort á reikningslögaðilann eða greiðslulögaðilann, eftir því hvað er valið Í reitnum **Bóka hagnað eða tap af gjaldeyrisviðskiptum** á síðunni **Bókhald innan samstæðu** fyrir Lögaðili greiðslunnar. Eftirfarandi dæmi nota þessa gjaldmiðla
-   Bókhaldsgjaldmiðill greiðslu: EUR
-   Bókhaldsgjaldmiðill reiknings: USD
-   Gjaldmiðill greiðslufærslu: DKK
-   Gjaldmiðill reikningsfærslu: CAD

#### <a name="currency-calculations"></a>Gjaldmiðilsútreikningar

Þegar reikningur er jafnaður í einu lögaðili með greiðslu sem er færð inn í öðru lögaðili er færslugjaldmiðill greiðslunnar (DKK) umreiknaður í þremur áföngum:
1.  Umreiknað í bókhaldsgjaldmiðli greiðslunnar (EUR) samkvæmt gengi greiðslulögaðilans.
2.  Umreiknað í bókhaldsgjaldmiðli reikningsins (USD)
3.  Umreiknað í færslugjaldmiðil reikningsins (CAD) samkvæmt gengi reikningslögaðilans.

Umreikningsferlið notar gengi greiðsludagsetningarinnar. Ef greiðsluupphæðin sem reiknuð er út í færslugjaldmiðli reikningsins (CAD) er jöfn reikningsupphæðinni (CAD) telst reikningurinn fullgreiddur. 

Þegar síðan **jafna opnar færslur** er opnuð í greiðslubók þar sem greiðsluupphæðin var ekki færð er upphæðin til jöfnunar reiknuð samkvæmt reikningunum sem eru valdir til jöfnunar í síðunni **jafna opnar færslur**. Upphæðin til jöfnunar er umreiknuð í þremur áföngum:
1.  Umreiknuð í bókhaldsgjaldmiðli reikningsins (USD) samkvæmt gengi reikningslögaðilans frá og með greiðsludegi.
2.  Umreiknað í bókhaldsgjaldmiðli greiðslunnar (EUR) með því að nota gengi greiðslulögaðilans frá og með dagsetningu greiðslu.
3.  Umreiknuð í færslugjaldmiðil greiðslunnar (DKK)

Greiðsluupphæðin sem er reiknuð er flutt í greiðslubókarlínuna þegar síðunni **jafna opnar færslur** er lokað.

#### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Bókun hagnaðar eða taps vegna mismunandi bókhaldsgjaldmiðla

Ef um gengishagnað eða -tap er að ræða er tap eða hagnaður bókað á lögaðili sem er tilgreint í svæðinu **Bóka gengishagnað eða -tap** síðunni **Bókhald innan samstæðu** fyrir greiðslulögaðila. Upphæðin er umreiknuð í bókhaldsgjaldmiðill lögaðila þar sem hagnaður eða tap er bókuð með því að nota gengið sem er skilgreint fyrir þann lögaðili.

<a name="cash-discounts"></a>Staðgreiðsluafslættir
--------------

Staðgreiðsluafslættir sem verða til í jöfnunarferlinu milli fyrirtækja eru bókaðir annaðhvort á reikningslögaðila eða greiðslulögaðila eftir því hvað er valið í svæðinu **Bóka staðgreiðsluafslátt** í síðunni **Bókhald innan samstæðu** fyrir greiðslulögaðila. Samsvarandi jöfnunarfærsla er búin til í reikningslögaðila.

<a name="overpayments-and-underpayments"></a>Ofgreiðslur og vangreiðslur
------------------------------

Ofgreiðslur, vangreiðslur og vikmörk auramismunar eru ákveðin samkvæmt greiðslulögaðilanum þegar um ofgreiðslu er að ræða og samkvæmt reikningslögaðilanum ef um vangreiðslu er að ræða. Bókunarlykillinn sem er notaður ræðst af stillingunni í **stýring staðgreiðsluafsláttar** reit í síðunni **Færibreytur viðskiptakrafna** fyrir viðskiptavini, og **stýring staðgreiðsluafsláttar** reit á **Færibreytur viðskiptaskulda** síðu fyrir lánardrottna.

-   Ef stillingin á stjórnun staðgreiðsluafsláttar er sértæk, eða ef stillingin er ósértæk og notaður afslátturinn er bókaður á annað fyrirtæki frá ofgreiðsla er sjálfvirkur lykill fyrir staðgreiðsluafslátt viðskiptavinar, staðgreiðsluafslátt lánardrottins eða auramismunur í bókhaldsgjaldmiðli notaður. Hægt Er að tilgreina þessa lykla í **Reikningar fyrir sjálfvirkar færslur** síðu.
-   Ef stillingin á stjórnun staðgreiðsluafsláttar er Ótilgreint og staðgreiðsluafsláttur er bókaður á sama lögaðili og ofgreiðslan (greiðslulögaðili og reikningslögaðili er hið sama) er reikningur staðgreiðsluafsláttar leiðréttur. Ef t.d. reikningur fyrir 100,00 með staðgreiðsluafslætti 3,00 er jafnaður við greiðslu sem nemur 98,00 er staðgreiðsluafslátturinn leiðréttur um 1,00. Nettóstaðgreiðsluafsláttarupphæðin er 2,00.
-   Ef stillingin á stjórnun staðgreiðsluafsláttar er Ótilgreint er staðgreiðsluafslátturinn bókaður á sama lögaðila og ofgreiðslan og ofgreiðslan eða vangreiðslan er jöfnuð með mörgum reikningum með staðgreiðsluafsláttum er staðgreiðsluafsláttarlykill síðasta reikningsins leiðréttur.

Ef stillingin á stjórnun staðgreiðsluafsláttar er Ótilgreint eiga ótilgreindar greiðslujöfnunarreglur aðeins við í eftirfarandi tilfellum:
-   Um ofgreiðslu er að ræða
-   Ofgreiðslan er jöfnuð með einum eða fleiri reikningum sem eru með staðgreiðsluafslátt.
-   Staðgreiðsluafslátturinn er bókaður í sama lögaðili og ofgreiðslan.

Í öllum öðrum tilvikum eru of- eða vangreiðslur bókaðar á sjálfvirka reikninginn fyrir staðgreiðsluafslátt Viðskiptavinar, staðgreiðsluafslátt Lánardrottins eða auramismunur í bókhaldsgjaldmiðli.

## <a name="sales-tax"></a>Virðisaukaskattur
Virðisaukaskattfærslur verða áfram í lögaðili þar sem þær voru upphaflega bókaðar. 

Ef virðisaukaskattur var bókaður vegna fyrirframgreiðslu bakfærir jöfnunin milli fyrirtækja virðisaukaskattinn á fyrirframgreiðsluna í fyrirframgreiðslulögaðilanum. Skatturinn í reikningslögaðilanum verður áfram þar.

## <a name="financial-dimensions"></a>Fjárhagsvíddir
Ef um viðskiptavinagreiðslur er að ræða nota færslurnar í greiðslulögaðila fjárhagsvíddirnar sem eru tilgreindar fyrir safnlykil viðskiptavina úr greiðslunni sem er verið að jafna. Í reikningslögaðilanum nota færslurnar fjárhagsfærslurnar sem eru tilgreindar fyrir safnlykil viðskiptavina úr reikningnum sem er verið að jafna. 

Ef um lánardrottinnsgreiðslur er að ræða nota færslurnar í greiðslulögaðila fjárhagsvíddirnar sem eru tilgreindar fyrir safnlykil viðskiptaskulda úr greiðslunni sem er verið að jafna. Í reikningslögaðilanum nota færslurnar fjárhagsfærslurnar sem eru tilgreindar fyrir safnlykil viðskiptaskulda úr reikningnum sem er verið að jafna.

## <a name="withholding-tax"></a>Staðgreiðsluskattur
Lánardrottnalykillinn sem reikningurinn tengist er notað til að ákvarða hvort á að reikna skuli staðgreiðsluskatt. Ef staðgreiðsluskattur á við hann reiknaður í lögaðila sem tengist reikningnum. Ef lögaðila nota aðra gjaldmiðla, er notað gengi frá lögaðila sem tengist reikningnum.






