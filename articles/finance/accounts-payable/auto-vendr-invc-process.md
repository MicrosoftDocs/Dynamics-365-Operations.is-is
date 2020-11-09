---
title: Yfirlit yfir sjálfvirka vinnslu á reikningi lánardrottins
description: Í þessu efnisatriði er lýst möguleikanum á að gera reikningsferli lánardrottins sjálfvirkt og ávinningin af því að nota sjálfvirkt ferli.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec3598ebd158cc23ac7c02d7e33557141d5901bc
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022497"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Yfirlit yfir sjálfvirka vinnslu á reikningi lánardrottins

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst möguleikanum á að gera reikningsferli lánardrottins sjálfvirkt og ávinningin af því að nota sjálfvirkt ferli. Þessi möguleiki samanstendur af eiginleikum sem kveikt er á í eiginleikastjórnun. Þessir eiginleikar eiga aðeins við um reikninga lánardrottins, ekki reikninga sem eru unnir í gegnum síðuna **Reikningabók** eða **Komubók reikninga**.

Fyrirtæki vinna oft með þriðja aðila til að vinna úr pappírsreikningum með því að nota þjónustuveitu stafakennsla. Þjónustuveitan skilar lýsigögnum reiknings sem tölvan getur lesið. Til að hjálpa til við sjálfvirkni gera sjálfvirknieiginleikar viðskiptaskulda þér kleift að nota þessa gervinga úr Viðskiptaskuldum.

Hægt er að gera sum reikningsferli lánardrottna í Viðskiptaskuldum sjálfvirk. Þessi ferli fela í sér að senda inn innflutta reikninga lánardrottins í verkflæðiskerfið og stemma bókaðar innhreyfingarlínur afurða við reikningslínur lánardrottins í bið. Sjálfvirka ferlið sýnir upplýsingar um framvindu lánardrottnareikninga þar sem það fer í gegnum hvert ferli. Þessi möguleiki getur hjálpað starfsfólki og stjórnendum Viðskiptaskulda að vinna úr reikningum lánardrottna á skilvirkari hátt. Hann dregur líka úr villum og óskilvirkni sem getur átt sér stað þegar upplýsingar eru færðar inn og meðhöndlaðar handvirkt.

Sjálfvirk ferli er hægt að nota til að framkvæma eftirfarandi verk:

- Senda innflutta reikninga sjálfkrafa í verkflæðiskerfið.
- Jafna innhreyfingarskjöl afurðar við reikningslínur lánardrottins sem eru í biðstöðu.
- Herma eftir bókun áður en lánardrottnareikningur er bókaður.
- Skoða á fljótlegan og skilvirkan hátt verkflæðissögu.
- Skoða og greina niðurstöður á sjálfvikri úrvinnslu lánardrottnareikninga.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Sjálfvirkni lánardrottnareikninga – Senda innflutta reikninga í verkflæðiskerfið

Sem hluti af snertilausu reikningsfærsluferli Viðskiptaskulda, er hægt að fá kerfið til að senda sjálfkrafa inn innfluttan reikning í verkflæðiskerfið. Ferlið verður keyrt í bakgrunni, eins oft og gefið er upp (annaðhvort á klukkutíma fresti eða daglega). Möguleikinn til að senda sjálfkrafa inn innflutta reikninga í verkflæðiskerfið krefst þess að ferlið hefjist á innfluttum reikningi. Til að tryggja að hægt sé að vinna úr reikningnum frá upphafi til enda án afskipta notandans, þarf að hafa með sjálfvirkt bókunarverk í skilgreiningu verkflæðisins.

Reikningar sem eru tengdir innkaupapöntunum og reikningar sem innihalda innkaupategund sem tengist hvorki innkaupapöntun né birgðalínum, er hægt að senda sjálfkrafa inn í verkflæðiskerfið. Reikningar sem eru færðir handvirkt inn og reikningar sem eru stofnaðir í gegnum vinnusvæðið **Reikningsfærsla fyrir samstarf lánardrottna** verða að sendir handvirkt inn í verkflæðiskerfið.

Sjálfvirknieiginleikinn veitir sveigjanlegan ramma sem gerir þér kleift að skilgreina reglur fyrirtækisins fyrir innsendingu á innfluttum reikningum lánardrottins í verkflæðiskerfið og stemma bókaðar innhreyfingarlínur afurða við reikningslínur lánardrottins í bið.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Sjálfvirkni reikninga lánardrottins - Jafna innhreyfingarskjöl afurða við reikningslínur sem eru með þríhliða jöfnunarreglu skilgreinda

Kerfið getur sjálfkrafa jafnað innhreyfingarskjöl afurða við reikningslínur sem eru með þríhliða jöfnunarreglu skilgreinda. Vinnslan keyrir þangað til magn jafnaðs innhreyfingarskjals afurðar jafngildir magni reiknings. Sem hluti af þessu ferli er hægt að tilgreina hámarksfjölda skipta sem kerfið á að reyna að jafna innhreyfingarskjöl afurðar við reikningslínu áður en ákveðið er að vinnslan hafi mistekist. Ferlið verður keyrt í bakgrunni, annaðhvort á klukkutíma fresti eða daglega. Hægt er að keyra sjálfvirka jöfnunarferlið sem hluta af ferlinu við að senda reikninga í verkflæðiskerfið. Að öðrum kosti er hægt að keyra það sem sjálfstæðan ferli.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Sjálfvirkni lánardrottnareiknings – Villuleita lánardrottnareikning fyrir bókun

Bókunarhermir lýkur villuleitarskrefunum sem eru gerð í bókunarferlinu fyrir reikninga lánardrottins, en engir lyklar eru uppfærðir. Til að keyra vinnsluna er hægt að velja annaðhvort einn reikning eða marga reikninga á síðunni **Reikningar frá lánardrottni í bið**.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Sjálfvirkni lánardrottnareiknings – Aukin upplifun til að skoða ferilgögn verkflæðis fyrir reikninga lánardrottna

Auðlesið yfirlit yfir verkflæðissögu lánardrottnareikninga er veitt. Hægt er að opna verkflæðissögu lánardrottnareiknings beint úr reikningi lánardrottins. Þess vegna þarf færri smelli til að finna þær upplýsingar.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Sjálfvirkni lánardrottnareiknings - Greiningar og mælingar

Vinnusvæðið **Reikningsfærsla lánardrottins** gerir þér kleift að einblína á reikninga lánardrottins sem komust ekki í gegnum sjálfvirka ferlið. Reitirnir á vinnusvæðinu sýna upplýsingar um reikninga lánardrottins sem ekki tókst að senda í verkflæðiskerfið, ekki tókst að flytja inn eða jafna við innhreyfingarskjöl afurða. Einnig er boðið upp á Microsoft Power BI mælingar til að veita stjórnendum viðskiptaskulda innsýn í skilvirknina sem fylgir sjálfvirkni lánardrottnareikninga.
