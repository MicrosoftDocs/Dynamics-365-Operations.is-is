---
title: "Birgðalokun"
description: "Sem hluti af ferlinu við að jafna úthreyfingarfærslur við innhreyfingarfærslur, er einnig hægt að velja að láta uppfæra fjárhag til að endurspegla leiðréttingarnar sem hafa verið gerðar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventClosing
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9ff992be8a2a4f1cc0cd3146f138d12267bb74ee
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="inventory-close"></a>Birgðalokun

[!include[banner](../includes/banner.md)]


Sem hluti af ferlinu við að jafna úthreyfingarfærslur við innhreyfingarfærslur, er einnig hægt að velja að láta uppfæra fjárhag til að endurspegla leiðréttingarnar sem hafa verið gerðar.

Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Sem hluti af jöfnunarferlinu er hægt að tilgreina að það eigi að uppfæra fjárhag, þannig að hann endurspegli leiðréttingarnar sem hafa verið gerðar. Hinsvegar, þangað til birgðalokun eða endurútreikningar eru keyrðir, eru úthreyfingarfærslur bókaðar skv. útreiknuðu hlaupandi meðaltali kostnaðarverðs. 

Eftir að birgðalokun hefur farið fram, er ekki lengur hægt að bóka á tímabilum sem voru fyrir dagsetningu birgðalokunar sem skilgreind var, nema fullgert birgðalokunarferli sé afturkallað. Til dæmis, ef birgðalokun er keyrð á tímabilinu sem endar 31 Janúar, er ekki hægt að bóka færslur sem hafa dagsetningu sem er fyrir 31 Janúar.  

Birgðavörur eru tengdar einni af tveimur tegundum birgða: vara, eða þjónusta Birgðalokun framkvæmir sömu aðgerðir í báðum gerðum. Hins vegar fyrir þjónustuvöru, jafnar birgðalokun samt sem áður úthreyfingar við innhreyfingar. 

Hve oft birgðalokunarferli er keyrt er breytilegt eftir fyrirtækjum. Hins vegar ætti færslumagn að hjálpa til við ákvarða hversu oft á að ákveða að keyra birgðalokun. Almennt séð, keyra flest fyrirtæki birgðalokun sem hluta af mánaðaruppgjöri sínu og uppgjörsferli.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Endurútreikningur birgða og fjárhagur
Ef leiðréttingar á birgðum og fjárhag eru nauðsynlegar innan mánaðarins eða á öðru birgðatímabili, er hægt að keyra endurútreikning birgða í stað birgðalokunar. Endurútreikningur birgða framkvæmir leiðréttingar, en býr ekki til uppgjör fyrir birgðafærslur. 

Við endurreikning birgða á lager eru lagerbirgðir og birgðafæslur leiðréttar, og endurútreikningar birgða og lokun birgða eru keyrðar. Þessi verk hafa áhrif á þá fjárhagslykla sem eru tengdir upphaflegu birgðafærslunni. 

**Dæmi** 

Ef sölupöntun er stofnuð úr innkaupapöntun verða fjárhagslyklarnir sem voru notaðir fyrir upprunalegu sölupöntunina uppfærðir. Jafnvel þó að fjárhagslyklarnir í vöruflokknum sem var úthlutaður þessari vöru hafi breyst síðan sölupöntunin var bókuð og þó að endurútreikningur birgða hafi stofnað leiðréttingarupphæð verður leiðréttingarupphæðin samt bókuð á upprunalegu fjárhagslyklana. Leiðrétt upphæð ekki bókuð á þá nýju fjárhagslykla sem eru úthlutaðir vörunni. 

Þegar uppfærslu er lokið, er hægt að fara yfir fjárhagsfylgiskjalið sem hefur verið bókað í framhaldi af einu þessara verkefna.

1.  Á síðunni **Lokun og leiðrétting** á flipanum **Yfirlit** skal velja uppfærslu til að fara yfir.
2.  Smelltu á **Upplýsingar**, og veljið svo **Fylgiskjal**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Áhrif birgðalokunarvinnslu á fjárhag
Nokkur þeirra verka sem hægt er að framkvæma á síðunni **Lokun og leiðrétting** valda uppfærslu í fjárhag. Til dæmis er fjárhagur uppfærður þegar gerðar eru leiðréttingar á lagerbirgðum og birgðaútreikningum, birgðaútreikningur keyrður og birgðalokun keyrð. 

Fjárhagslyklar sem eru uppfærðir vegna þessara verka eru tengdir upphaflegu birgðafærslunni. Til dæmis ef sölupöntun er jöfnuð við innkaupapöntun verða fjárhagslyklarnir sem voru notaðir fyrir upprunalega sölupöntun leiðréttir. Þetta gerist jafnvel þó að fjárhagslyklarnir fyrir vöruflokkinn sem er úthlutaður þessari vöru hafi breyst síðan sölupöntunin var bókuð. Eftir að birgðalokun stofnar upphæð til jöfnunar, er jöfnunarupphæð samt bókuð á upprunalegu fjárhagslyklana, í staðinn fyrir þá nýju fjárhagslykla sem úthlutað var á vöruna. Einnig gæti fjárhagur verið uppfærður ef birgðalokun er bakfærð. 

**Athugasemdir :**

-   Ekki er krafist birgðalokunar með Matsaðferð staðlaðs kostnaðar.
-   Áður en lokunarferlið er keyrt, geturðu skoðað lista yfir vörur sem ekki er hægt að jafna við uppfærslu.
-   Mælt er með því að birgðalokun sé keyrð utan háannatíma til þess að tölvubúnaðurinn nýtist betur.

## <a name="the-inventory-close-log"></a>birgðalokunarkladdi
Þegar birgðalokunarferli er lokið geta komið upp skilaboð sem segja að kostnaðarverð einingar sé hugsanlega rangt því ekki hafi tekist að fulljafna færslu. 

Áður en þessi boð birtast tilgreinir Dynamics AX vörunúmer og viðkomandi færslu. Þessi boð segja að kostnaðarupphæðin sem var notuð fyrir færsluna hafi ekki verið uppfærð vegna birgðalokunar. Þau birtast þegar ekki er hægt að jafna færslu af gerðinni úthreyfing. 

Við lokun birgðalokununarferlis er hver fjárhagsvídd athuguð til að gá hvort eru fleiri úthreyfingar en innhreyfingar fram að tilgreindri lokunardagsetningu. Þetta ójafnvægi getur orðið þegar birgðafærsla úr innkaupapöntun er ekki fyllilega jöfnuð fjárhagslega vegna þess að reikningur lánardrottins hefur ekki verið móttekinn eða vegna þess að uppskriftaríhlutir sem eru með í framleiðslu á hærra stigi eru ekki fjárhagslega bókaðir. Ef þetta gerist leiðréttir síðari lokun ekki allar úthreyfingar yfir í gildandi kostnaðarverð því ekki eru fullnægjandi upplýsingar um innhreyfingar. 

Fyrir hverja lokunarkeyrslu gefur kerfið til kynna hvort kladdi sem geymir viðvaranirnar er geymdur og hvort hægt er að skoða hann. 

Ef margar viðvaranir berast í skilaboðunum, er mælt með að bregðast við á eftirfarandi hátt:

-   Uppfæra innhreyfingar fjárhagslega
-   Flýta lokunardagsetningunni.
-   Endurmeta ferli fyrirtækis.

Það kunna að koma upp aðstæður þar sem ekki er mögulegt að bregðast við viðvörunum. Þegar til dæmis merking er notuð þar sem merkta innkaupapöntunin er með fjárhagslega dagsetningu eftir lokunardagsetninguna er ekki hægt að breyta lokunardagsetningunni.

## <a name="reversing-a-completed-inventory-close"></a>Afturkalla birgðalokun sem lokið hefur verið við
Í sumum tilvikum getur þurft að bakfæra birgðalokun sem hefur verið framkvæmd, og koma birgðajöfnunum aftur á það form sem þær höfðu áður en jöfnun var framkvæmd. Þegar lokin birgðalokun er bakfærð, eru birgðir enduropnaðar til að virkja bókun á tímabilinu sem nær yfir birgðalokunina. Tengdar breytingar má einnig gera í fjárhag. Þegar þú hefur lokið að gera leiðréttingar getur þú keyrt birgðaskrá aftur fyrir tímabilið sem þú ert að vinna með. 

**Athugið:** Aðeins er hægt að opna aftur síðasta birgðatímabil sem var lokað. Til að bakfæra fyrri birgðalokun verður að bakfæra hverja síðari birgðalokun eina í einu, byrja á nýjustu lokuninni.




