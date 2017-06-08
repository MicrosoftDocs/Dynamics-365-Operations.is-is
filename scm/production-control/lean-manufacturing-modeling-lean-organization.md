---
title: "Gerð líkans af lean-fyrirtæki"
description: "Þessi grein veitir upplýsingar um lykilhugtök í mótun lean-framleiðslu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ec9191054a1b3587ebbde16acf278084cbd22660
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="modeling-a-lean-organization"></a>Gerð líkans af lean-fyrirtæki

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um lykilhugtök í mótun lean-framleiðslu. 

Lean-framleiðslu aðstæður eru yfirleitt meira en samsafn ótengdra kanban-reglna eða reglna um framboð efnis. Flæði efnis og afurða í gegnum vinnuflokka og staðsetningar fyrir ákveðna framleiðslupöntun eða framboðs aðstæður má lýsa sem röð eða litlu net ferli eða flutningsverkþáttum. Þessi röð eða net kallast framleiðsluflæði.

## <a name="production-flows-in-lean-manufacturing"></a>Framleiðsluflæði fyrir Lean framleiðslu
Við framleiðslukringumstæður á grundvelli framleiðslupantana er efni gefið út til tilgreindrar framleiðslupöntunar. Við röð aðgerða, byggt á uppskrift (BOM) og leiðir, afurðir eru stofnaðar og að lokum eru mótteknar við uppgefin staðsetning. Gegnumstreymistími framleiðslupantana getur verið breytilegur, frá mínútum í vikur. Öllum tengdum kostnaði, efni og vinnu er safnað upp á framleiðslupöntunina. 

Til að minnka biðtíma afhendingar og umfram birgðir milli vinnustöðva vegna runu framleiðslu, kynnir lean-framleiðsla kanban áfyllingu og geymslusvæði í framleiðslu- og áfyllingu. Þessi eiginleiki truflar yfirleitt framleiðslu hluta óháð kanban-ferli. Áfylling kanban fyrir hálfkláraða afurð er ekki lengur ræst af pöntun fyrir fullunna vöru. 

Til að koma aftur framleiðslu- og kostnaðargildi samhengi fyrir mismunandi aðstæður kanban lögð til í Microsoft Dynamics AX, er framleiðsluflæði byggt á verkþáttum hafa verið kynnt sem grundvöllur lean framleiðslu. Allar kanban-reglur vísa í þetta fyrirfram skilgreinda skipulag. Líkan byggt á verkþætti heimilar uppsetningu á breiðara sviði aðstæðna en eru studdar af fyrri útgáfur af Lean-framleiðslu fyrir Microsoft Dynamics AX. Hinsvegar, þetta líkan flækir ekki málin fyrir starfsmenn í vinnusal og allar áætlanir nota sama notendaviðmót byggt á verkþáttum.

## <a name="semi-finished-products-non-bom-levels"></a>Hálfkláraðar afurðir (ekki-uppskriftarstig)
Lean framleiðsla fyrir Dynamics AX samþættir kanban fyrir afurðir sem búið er að skrá og hálfkláraðar afurðir í einum ramma, og býður því notandanum samræmda reynslu fyrir öll tilvik. Vegna þessarar uppbyggingar þarf ekki lengur að kynna til leiks uppskriftarstig til að virkja kanbön sem nota á fyrir hálfkláraðar afurðir. Þessi uppbygging hjálpar einnig við minnka birgðafærslur að lágmarki.

## <a name="products-and-material-in-work-in-progress"></a>Afurðir og Efni í Verk í Vinnslu (VÍV)
Lækkun á runustærðum í tilvalda stöðu flæðis eitt stykki í lean framleiðslu getur valdið verulegri hækkun á birgðafærslur ef hver tiltekt eða kanban-skráning veldur færslum fyrir notaðar vörur. Uppbygging flæðisframleiðslu leyfir flutningur á efni til framleiðsluflæðis ásamt úttektarkanbönum í geymslu eða flutnings meðhöndlun í einingastærðum. Gildi útgefins efnis er bætt við VÍV lykla sem tengjast framleiðsluflæði. Þessi hegðun svipar hegðun fyrir efni sem er gefinn út á framleiðslupöntun. Hægt er að nota sömu reglu fyrir hálfkláraðar afurðir og afurðir. Birgðafærslur eru valfrjálsar — ekki skylda, nema þessar vörur sé stofnaðar, fluttar eða notaðar innan framleiðsluflæðis. Eftir að vörurnar eru bókaðar í birgðir, er vív-lykillinn fyrir framleiðsluflæðið lækkaður með því að draga frá tengdan staðalkostnað.

## <a name="value-streams-and-value-stream-mapping"></a>Virðisstraumar og gildisvörpun virðisstrauma
Uppbygging Lean-framleiðslu fyrir Dynamics AX er innblásin eftir fimm Lean reglum mynduðum af Womack og Jones: Gildi viðskiptavinar, Virðisstreymi, Flæði, Tog og Fullkomnun. Ein samþykkt aðferð fyrir innleiðingu lean-framleiðslulausna í efnisheiminum er vörpun virðisstreymis (VSM). Þessi aðferð var kynnt af Rother og Shook í útgáfu þeirra „Lært að sjá“ í Lean-framleiðslustofnuninni. 

Í Dynamics AX, framtíðarstaða virðisstreymis getur verið sett upp sem líkan sem útgáfa framleiðsluflæðis. Öll ferli í virðisstreyminu eru sett upp sem vinnsluverkþættir. Hreyfingar eða flutninga er hægt að setja upp sem flutningsverkþætti ef skrá þarf flutningsstöðuna eða ef samþættingar birgðatiltektar eða sameinaðar sendingar er krafist. 

Virðisstreymið sjálft er byggt upp sem rekstrareining í Dynamics AX. Þess vegna er hægt að nota virðisstraum sem fjárhagsvídd.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Kostnaðarútreikning fyrir lean framleiðslu byggt á framleiðsluflæði
Reglubundin samlegð kostnaðar fyrir framleiðsluflæði leiðréttir tengdan vív-lykil og leyfir ákvörðun frávika fyrir afurðir sem fylgja framleiðsluflæði.

## <a name="continuous-improvement"></a> Samfelldar umbótaraðgerðir
Til að styðja betur samfellda bætingu, er framleiðsluflæði útfært í tímasparandi útgáfum. Þetta leyfir afritun fyrirliggjandi framleiðsluflæðisútgáfu, þar á meðal allar tengdar kanban-reglur, yfir í síðari útgáfur framleiðsluflæðis. Þar að auki framleiðsluflæði í framtíðinni má móta áður en hún er villuleituð og virkjuð fyrir framleiðslu. Fyrirliggjandi kanbön úr eldri útgáfum framleiðsluflæðisins eru sjálfkrafa tengd við nýju útgáfuna til að tryggja samþætt efnisflæði á breytingardagsetningunni og áfram.

## <a name="simplicity"></a>Einfaldleiki
Fyrir innleiðingar Lean Framleiðslu fyrir Dynamics AX, völdum við nálgun á framleiðsluflæði og verkþátt sem gerir mögulegt að móta einfaldar og flóknar framleiðsluaðstæður í eina kvarða uppbyggingu. Nánari skoðun á virknihugtakinu leiðir í ljós nýja einföldun fyrir þá notendur sem þurfa á því að halda: Starfsmenn í vinnusal og vörustjórnun. Með því að gefa skýrslu um verk byggð á verkþáttum í stað birgðafærslna getur sameinaða notendaviðmótið sem á við alla þætti Lean-framleiðslu flutt margbreytileika fyrirtækisins frá notendaviðmótinu þangað sem það á raunverulega heima: Til framleiðsluflæðisins sem er hornsteinn Lean-framleiðslunnar.



