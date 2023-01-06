---
title: Yfirlit yfir sjálfvirka vinnslu á reikningi lánardrottins
description: Í þessari grein er lýst möguleikanum á að gera reikningsferli lánardrottins sjálfvirkt og ávinningin af því að nota sjálfvirkt ferli.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d2c629ed2d064a3350ec8ffe53940098d12ab0b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883446"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Yfirlit yfir sjálfvirka vinnslu á reikningi lánardrottins

[!include [banner](../includes/banner.md)]

Í þessari grein er lýst möguleikanum á að gera reikningsferli lánardrottins sjálfvirkt og ávinningin af því að nota sjálfvirkt ferli. Þessi möguleiki samanstendur af eiginleikum sem kveikt er á í eiginleikastjórnun. Þessir eiginleikar eiga aðeins við um reikninga lánardrottins, ekki reikninga sem unnið er úr með síðunni **Reikningabók** eða **Komubók reikninga**.

Fyrirtæki vinna oft með þriðja aðila til að vinna úr pappírsreikningum með því að nota þjónustuveitu stafakennsla. Þjónustuveitan skilar lýsigögnum reiknings sem tölvan getur lesið. Til að hjálpa til við sjálfvirkni gera sjálfvirknieiginleikar viðskiptaskulda þér kleift að nota þessa gervinga úr Viðskiptaskuldum.

Hægt er að gera sum reikningsferli lánardrottna í Viðskiptaskuldum sjálfvirk. Þessi ferli fela í sér að senda inn innflutta reikninga lánardrottins í verkflæðiskerfið og stemma bókaðar innhreyfingarlínur afurða við reikningslínur lánardrottins í bið. Sjálfvirka ferlið sýnir upplýsingar um framvindu lánardrottnareikninga þar sem það fer í gegnum hvert ferli. Þessi möguleiki getur hjálpað starfsfólki og stjórnendum Viðskiptaskulda að vinna úr reikningum lánardrottna á skilvirkari hátt. Hann dregur líka úr villum og óskilvirkni sem getur átt sér stað þegar upplýsingar eru færðar inn og meðhöndlaðar handvirkt.

Sjálfvirk ferli er hægt að nota til að framkvæma eftirfarandi verk:

- Nota fyrirframgreiðslur sjálfkrafa í reikningum lánardrottins
- Senda innflutta reikninga sjálfkrafa í verkflæðiskerfið.
- Jafna innhreyfingarskjöl afurðar við reikningslínur lánardrottins sem eru í biðstöðu.
- Herma eftir bókun áður en lánardrottnareikningur er bókaður.
- Skoða á fljótlegan og skilvirkan hátt verkflæði og sjálfvirknisögu.
- Skoða og greina niðurstöður á sjálfvikri úrvinnslu lánardrottnareikninga.
- Halda sjálfvirku ferli áfram fyrir marga reikninga.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Senda innflutta reikninga í verkflæðiskerfið

Sem hluti af snertilausu reikningsfærsluferli Viðskiptaskulda, er hægt að senda sjálfkrafa inn innfluttan reikning í verkflæðiskerfið. Ferlið verður keyrt í bakgrunni, eins oft og gefið er upp (annaðhvort á klukkutíma fresti eða daglega). Möguleikinn til að senda sjálfkrafa inn innflutta reikninga í verkflæðiskerfið krefst þess að ferlið hefjist á innfluttum reikningi. Til að tryggja að hægt sé að vinna úr reikningnum frá upphafi til enda án afskipta notandans, þarf að hafa með sjálfvirkt bókunarverk í skilgreiningu verkflæðisins.


Reikningar sem eru tengdir innkaupapöntunum og reikningar sem innihalda innkaupategund sem tengist hvorki innkaupapöntun né birgðalínum, er hægt að senda sjálfkrafa inn í verkflæðiskerfið. Reikningar sem eru færðir handvirkt inn og reikningar sem eru stofnaðir með því að nota vinnusvæðið **Reikningsfærsla fyrir samstarf lánardrottna** verða að vera sendir handvirkt inn í verkflæðiskerfið. Framkvæma verður jöfnunarferli fyrirframgreiðslu handvirkt fyrir innflutta reikninga. Hægt er að nota fyrirframgreiðslur handvirkt fyrir eða eftir bókun innflutts reiknings. Hægt er að nota fyrirframgreiðslur handvirkt til að afbóka staðlaða reikninga með því að nota síðuna **Reikningar lánardrottins**. Eftir bókun verður jöfnuð fyrirframgreiðsla í boði til að nota handvirkt á aðra reikninga frá þessum lánardrottni á síðunni **Lánardrottnar** (**Viðskiptaskuldir \> Almennar \> Lánardrottnar \> Allir lánardrottnar \> Reikningsflipi \> Nota**).

Sjálfvirknieiginleikinn veitir sveigjanlegan ramma sem gerir þér kleift að skilgreina reglur fyrirtækisins fyrir innsendingu á innfluttum reikningum lánardrottins í verkflæðiskerfið og stemma bókaðar innhreyfingarlínur afurða við reikningslínur lánardrottins í bið.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Jafna innhreyfingarskjöl afurða við reikningslínur sem eru með þríhliða jöfnunarreglu

Innhreyfingarskjöl afurða geta verið jafnaðar sjálfkrafa við reikningslínur sem eru með þríhliða jöfnunarreglu skilgreinda. Vinnslan keyrir þangað til magn jafnaðs innhreyfingarskjals afurðar jafngildir magni reiknings. Sem hluti af þessu ferli er hægt að tilgreina hámarksfjölda skipta sem kerfið á að reyna að jafna innhreyfingarskjöl afurðar við reikningslínu áður en ákveðið er að vinnslan hafi mistekist. Ferlið verður keyrt í bakgrunni, annaðhvort á klukkutíma fresti eða daglega. Hægt er að keyra sjálfvirka jöfnunarferlið sem hluta af ferlinu við að senda reikninga í verkflæðiskerfið. Að öðrum kosti er hægt að keyra það sem sjálfstæðan ferli.

## <a name="pre-validate-vendor-invoice-posting"></a>Villuleita lánardrottnareikning fyrir bókun

Bókunarhermir lýkur villuleitarskrefunum sem eru gerð í bókunarferlinu fyrir reikninga lánardrottins, en engir lyklar eru uppfærðir. Til að keyra vinnsluna er hægt að velja annaðhvort einn reikning eða marga reikninga á síðunni **Reikningar frá lánardrottni í bið**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Aukin upplifun til að skoða ferilgögn og sjálfvirkni verkflæðis fyrir reikninga lánardrottna

Auðlesið yfirlit yfir verkflæðissögu lánardrottnareikninga er veitt. Hægt er að opna verkflæðissögu lánardrottnareiknings beint úr reikningi lánardrottins. Þess vegna þarf færri smelli til að finna þær upplýsingar. Ef fyrirtækið hefur virkjað möguleikana á að senda innflutta reikninga lánardrottins sjálfkrafa í verkflæði er sjálfvirkniferill gefin upp fyrir innfluttu reikningana. Sjálfvirkniferill hjálpar til við að auðkenna núverandi skref ferlis, sem og skrefin sem þegar hefur verið lokið. Ef skref mistekst eru ítarlegar upplýsingar veittar til að hjálpa við að skilja ástæðuna fyrir því að það mistókst.

## <a name="analytics-and-metrics"></a>Greiningar og mælingar

Vinnusvæðið **Reikningsfærsla lánardrottins** gerir þér kleift að einblína á reikninga lánardrottins sem komust ekki í gegnum sjálfvirka ferlið. Reitirnir á vinnusvæðinu sýna upplýsingar um reikninga lánardrottins sem ekki tókst að senda í verkflæðiskerfið, ekki tókst að flytja inn eða jafna við innhreyfingarskjöl afurða. einnig er boðið upp á Microsoft Power BI mælingar til að veita stjórnendum viðskiptaskulda innsýn í skilvirknina sem fylgir sjálfvirkni lánardrottnareikninga.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Halda sjálfvirku ferli áfram fyrir marga reikninga

Þegar ekki tekst að flytja inn reikning í verkflæði með sjálfvirka ferlinu mun kerfið fjarlægja hann frá frekari sjálfvirkri vinnslu. Starfsmaður viðskiptaskulda getur yfirfarið og breytt reikningi áður en sjálfvirka vinnslan sendir hann aftur í verkflæði. Þegar hægt er að leysa úr ástæðu þess að bilun kom upp fyrir marga reikninga er hægt að endurræsa sjálfvirka ferlið á síðunni **Halda áfram sjálfvirkri úrvinnslu reikninga**. 

## <a name="tracking-the-invoice-received-date-value"></a>Rakning á gildi móttökudagsetningar reiknings

Gildið fyrir **Móttökudagsetningu reiknings** gefur til kynna daginn sem fyrirtækið tók á móti reikningnum frá lánardrottni. Það er byrjunarreitur rakningar á framvindu reikningsins í gegnum sjálfvirku vinnslurnar. Hægt er að hafa þetta gildi með í innfluttum gögnum fyrir reikning lánardrottins. Fyrir reiknings sem voru stofnaðir handvirkt er hægt að tilgreina dagsetninguna. Ef ekkert gildi er slegið inn verður dagurinn í dag notaður.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Rakning á gildum innfluttrar reikningsupphæðar og innfluttrar upphæðar virðisaukaskatts

Gildin **Innflutt reikningsupphæð** og **Innflutt upphæð virðisaukaskatts** fyrir reikninga lánardrottins er hægt að bjóða upp í innflutningsskrá lánardrottnareikninga. Yfirleitt eru þessi gildi í reikningi sem var skannaður af utanaðkomandi þjónustuaðila og höfð með í innflutningsskránni. Þegar unnið er úr reikningnum í viðskiptaskuldum eru gildin reiknuð út frá gögnum reikningsins. Aðeins er hægt að bóka reikninginn ef innflutt gildi stemma við reiknuð gildi. Að stemma gildi tryggir að reikningurinn feli í sér þá upphæð sem lánardrottinn á að fá. Ef fyrirtækið leyfir að sjálfkrafa flytja inn innflutta reikninga í verkflæðiskerfið er valfrjálst hægt að krefjast þess að innfluttar samtölur stemmi við reiknaðar samtölur áður en hægt er að senda inn reikninginn í verkflæðiskerfið.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Sjálfvirkni reiknings lánardrottins - halda sjálfvirknivinnslu áfram fyrir marga reikninga
Þegar innfluttur reikningur hefur ekki verið sendur í verkflæði í gegnum sjálfvirka ferlið verður hann fjarlægður úr frekari sjálfvirkri vinnslu. Starfsmaður viðskiptaskulda getur yfirfarið og breytt reikningi áður en sjálfvirka vinnslan sendir hann aftur í verkflæði. Þegar hægt er að leysa úr ástæðu þess að bilun kom upp fyrir marga reikninga er hægt að endurræsa sjálfvirka ferlið á síðunni **Halda áfram sjálfvirkri úrvinnslu reikninga**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
