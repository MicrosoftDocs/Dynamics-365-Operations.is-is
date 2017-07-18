---
title: Yfirlit yfir sameiningu og losun
description: "Þessi grein veitir almennar upplýsingar um sameiningar- og losunarferli. Í því eru svör við Algengar spurningar"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c9568d1cac05db83d00108e8b16c03aa4c807cac
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="consolidation-and-elimination-overview"></a>Yfirlit yfir sameiningu og losun

[!include[banner](../includes/banner.md)]


Þessi grein veitir almennar upplýsingar um sameiningar- og losunarferli. Í því eru svör við Algengar spurningar

Hægt er að nota sameiningaraðgerðir til að sameina°fjárhagsniðurstöður fyrir nokkur dótturfyrirtæki í niðurstöður fyrir eitt sameinað fyrirtæki. Dótturfyrirtæki getur verið í mismunandi útgáfum eða kerfum, hugsanlega ekki í fullri eigu og þau geta notað mismunandi gjaldmiðla. Það eru margir valkostir fyrir sameiningu gagna:

-   **Sameina á netinu** – Þessi valkostur sameinar daglega stöðu eftir völdum lyklum og víddum og vistar þær í samstæðufyrirtæki.
-   **Fjárhagsskýrslugerð** – Þessi valkostur gerir sameiningu færslna og stöðu mögulega og hægt er að mynda hvenær sem er. Hægt er að stofna mörg stig stigveldis og má skoða skýrslugerð marga gjaldmiðla.
-   **Sameina með innflutningi** – Þessi valkostur flytur stöður inn í samstæðufyrirtækið.
-   **Flytja út stöður fyrirtæki** – Þessi valkostur veitir útflutningsskrá með stöðu fyrirtækisins. Síðan er hægt að innflytja skrána í önnur tilvik eða kerfi. Fjárhagsskýrslugerð er einnig hægt að nota til að flytja út stöður í Microsoft°Excel-skrá.

Hægt er að skrá losun á marga vegu:

-   Losunarreglur geta verið settar upp í kerfinu og unnar meðan á sameiningarferlinu stendur eða með losunartillögum. Hægt er að bóka reglur°í hvaða fyrirtæki sem hefur **Nota fyrir losunarferli fjárhags** valið í uppsetningu lögaðila.
-   Aðskilið fyrirtæki getur verið stofnað og notað til að ákvarða og bóka losunarfærslur handvirkt. Þetta fyrirtæki er hægt að nota í sameiningarferlinu eða í fjárhagsskýrslu.
-   Lyklar og fjárhagsvíddirnar sem eru notaðar til að ákvarða samstæðu verkþátt er hægt að sía í línuskilgreiningu eða dálkskilgreiningu í Fjárhagsskýrslu og hægt er að nota fulla köfunargetu. Reiknaður dálkur eða línu hægt að nota til að fjarlægja lykla og fjárhagsvíddir úr uppsafnaða samtölu.

Til eru margar aðstæður sameiningar og hver aðferð ræður við aðstæður á mismunandi vegu.

## <a name="frequently-asked-questions"></a>Algengar spurningar
1.  Ég kýs að bóka losunarbók í gagnagrunni. Hverjir eru valkostir mínir?

Margir valkostir eru í stöðunni. Hægt er að nota valkostinn **Sameina á netinu** og taka með útilokanir við vinnslu eða sem tillögu. Færslurnar verða bókaðar í samstæðufyrirtækinu. Einnig er hægt að hafa aðskilið fyrirtæki þar sem losanir eru stofnaðar handvirkt og nota svo það fyrirtæki í Fjárhagsskýrslugerð eða í sameiningarferlinu.

2.  Við þurfum að fá sameiningarniðurstöður okkar í mörgum gjaldmiðilsskrám.

Valkosturinn **Fjárhagsskýrslugerð** hefur ótakmarkaðar gjaldmiðilsskrár. Gögn eru umreiknuð við myndun skýrslunnar,miðað við gerð gengis og aðferð við umreikning gjaldmiðils sem eru stillt í aðallyklinum. Hins vegar, þar sem valkosturinn **Sameina á netinu** hefur aðeins einn skýrslugjaldmiðil, er fyrirtækjasamstæðu krafist fyrir hvern skýrslugjaldmiðill ef sá valkostur er notaður. Mælt er með að nota valkostinn **Fjárhagsskýrsla**.

3.  Ég vil sjá upplýsingar um færslustig fyrir hvert fyrirtæki.

Valkosturinn **Fjárhagsskýrslugerð** er lausnin, þar sem hægt er að skoða upplýsingar um færslustig fyrir eins mörg fyrirtæki og eru tekin með í skilgreiningu skipuritsins.

4.  Við erum að nota fjárhagsáætlunargerð eða fjárhagsáætlunarstýringu, og það verður að sameina.
Valkosturinn **Fjárhagsskýrslugerð** er lausnin til að sameina allar fjárhagsáætlunargerðir eða gögn fjárhagsáætlunarstýringar.

5.  Dótturfyrirtæki okkar eru dreifð um heiminn og við höfum marga bókhaldslykla. Hver er besta aðferðin til að sameina gögn okkar?

Margir valkostir eru þegar°þarf°að vinna með marga bókhaldslykla. Hægt er að nota valkostinn **Sameina á netinu** og velja svo að nota annað hvort samstæðulykil sem er skilgreindur á aðallykilinn eða flokk samstæðulykla. Einnig er hægt að nota valkostinn**Fjárhagsskýrsla**, hafa marga tengla í fjárhagsvíddir í línuskilgreiningu og kortleggja lykla.

6.  Við krefjumst sameiningar á mörgum stigum. Með öðrum orðum mælt, sameinum við fyrst öll evrópsku dótturfyrirtæki okkar í breska pundið (GBP). Síðan tökum við gögnin og umreiknum sameinaða upphæð yfir í bandaríska dollara. Hvernig er þetta gert?

Þegar margra samstæðustiga er krafist og mismunandi gjaldmiðlar eru notaðir á hverju stigi, verður að nota valkostinn **Sameina á netinu**. Stofna þarf mörg samstæðufyrirtæki sem nota mismunandi gjaldmiðla í reikningsskilum og skýrslugerð. Sameiningin þarf síðan að keyra mörgum sinnum. Valkosturinn **Fjárhagsskýrsla** umreiknar alltaf gjaldmiðla í reikningsskilum yfir í valinn gjaldmiðil fyrir hvert upprunafyrirtæki.

7.  Við erum með dótturfyrirtæki í öðru kerfi. Hvernig er hægt að sameina þær?

Notið valkostinn **Sameina með innflutningi** til að flytja stöðurnar inn í samstæðufyrirtækið.

8.  Sum dótturfyrirtækja okkar eru ekki í fullri eigu. Hver er besta aðferðin til að sameina þau?

Margir valkostir eru fyrir dótturfyrirtæki í hlutaeigu. Með því að nota valkostinn **Fjárhagsskýrsla** er hægt að skilgreina skýrsluskipurit og eignarhald. Einnig má nota reiknaða röð eða dálk til að tákna upphæð í hlutaeigu. Hægt er jafnvel að birta hlutdeild minnihluta sem eigin línu í skýrslu. Einnig er hægt að nota valkostinn **Sameina á netinu**. Flipinn **Lögaðilar** hefur dálk sem kallast **Eignarhald**, þar sem hægt er að tilgreina þá prósentu sem er í eigu móðurfyrirtækisins.

9.  Fyrirtæki okkar verður að sýna samstæður eftir viðskiptaeiningu eða vill nota stigveldi fyrirtækis.

Valkosturinn **Fjárhagsskýrsla** er lausnin. Hægt er að skrá stigveldi fyrirtækja sem hafa lögaðila eða fjárhagsvíddir í þeim í fjárhagsskýrslum. Einnig er hægt að stofna eigin margstiga stigveldi með skýrsluskipuriti sem felur í sér samsetningu lögaðila og víddargildi.

10. Við höfum meira en eina útgáfu af kerfinu.

Með því að nota valkostinn **Flytja út stöður í fyrirtækinu** til að flytja út úr einu tilviki og nota svo°valkostinn **Sameina með innflutningi** fyrir hina útgáfuna er hægt að sameina gögnin.


Frekari upplýsingar eru í [Endurmat gjaldmiðils í samstæðufyrirtæki](..\general-ledger\currency-revaluation-consolidation-company.md).



