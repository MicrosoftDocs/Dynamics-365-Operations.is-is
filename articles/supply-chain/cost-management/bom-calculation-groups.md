---
title: Flokkur uppskriftarútreiknings
description: Þessi skrá veitir upplýsingar um reikniflokka  fyrir uppskriftir (BOM) og hvernig þær eru settar upp. Til að keyra útreikning Uppskriftar skal þarf annaðhvort að setja upp reikniflokka og úthluta þeim á einstaka vörur eða stilla sjálfgefinn reikniflokk. Stillingar útreikninga úr reikniflokknum eru síðan notaðar sem sjálfgefið gildi á uppskriftarútreikning síðu við útreikning Uppskriftar.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 098a2fc065f6ace992dba1b1ae78756d456eb73a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579857"
---
# <a name="bom-calculations-groups"></a>Flokkur uppskriftarútreiknings

[!include [banner](../includes/banner.md)]

Þessi skrá veitir upplýsingar um reikniflokka  fyrir uppskriftir (BOM) og hvernig þær eru settar upp. Til að keyra útreikning Uppskriftar skal þarf annaðhvort að setja upp reikniflokka og úthluta þeim á einstaka vörur eða stilla sjálfgefinn reikniflokk. Stillingar útreikninga úr reikniflokknum eru síðan notaðar sem sjálfgefið gildi á uppskriftarútreikning síðu við útreikning Uppskriftar. 

Sjálfgefinn reikniflokkur er krafist í á **stjórnfæribreytur birgða og vöruhúss** síðu, eða afurðabundinn reikniflokkur er krafist í á **upplýsingar um losaðar afurðir** síðu. Kerfið leitar fyrst að uppsetningu reikniflokks á **upplýsingar um losaðar afurðir** síðu. Ef það finnur ekki reikniflokk þar, leitar það á síðunni **stjórnfæribreytur birgða og vöruhúss**. Ef kerfið finnur ekki reikniflokk, fær notandinn villuboð við útreikning. Reikniflokkur inniheldur reglur fyrir kostnaðarverðslíkanið, söluverðslíkan og gátlista viðvarana. Stillingar útreikninga úr reikniflokknum eru notaðar sem sjálfgefið gildi á **uppskriftarútreikning** síðu við útreikning Uppskriftar.

## <a name="purposes-of-bom-calculation-groups"></a>Tilgangur flokka uppskriftarútreiknings
Þú Úthluta flokkum uppskriftarútreiknings af nokkrum ástæðum:

-   Með því að stilla **kostnaðarverðslíkan** reitinn, Tilgreinirðu uppruna kostnaðarframlags keyptrar einingar á meðan verið er að reikna út áætlaður kostnaður fyrir framleidd vara. Sumir framleiðendur reikna út áætlaðan kostnað með því að nota innkaupaverð skv. viðskiptasamningum um keyptar einingar eða annan grunn, eins og innkaupaverðsfærslur innan kostnaðarútgáfunnar.
-   Tilgreinið hvernig gögn vörunnar verða notuð til þess að reikna út það söluverð sem lagt er til (með því að stilla **söluverðlíkan**). Hægt er að tilgreina annað hvort söluverð vöru eða kostnaðarflokk. Sumir framleiðendur vilja reikna út það söluverð sem lagt er til fyrir framleiddar vörur. Útreiknað söluverð getur endurspeglað nálgun verðs með samlagningu sem byggir á söluverðsfærslu einingarinnar. Hinsvegar, getur Útreiknað söluverð endurspeglað nálgun með kostnaði plús álagningu sem byggir á kostnaði einingarinnar og viðeigandi álagningarprósentu (sem tengist kostnaðarflokki vörunnar).
-   Með því að nota reitinn **stöðva niðurbrot** tilgreinirðu að framleidd vara skuli vera meðhöndluð sem keypt vara fyrir samantekt kostnaðar við útreikning uppskriftar. Dæmigerðar aðstæður er þegar keypt vara sem er einstaka sinnum framleidd eða þegar um er að ræða framleidda vöru sem skal núna kaupa. Varan er fyrst skilgreind sem framleidd vara til að skilgreina uppskrift (BOM) og leiðarupplýsingar og til að styðja framleiðslupantanir fyrir vöruna. Aftur á móti, kemur flaggið **stöðvun niðurbrots** í veg fyrir að kostnaðarútreikningar noti uppskrift og leið vörunnar. Þess í stað notar Útreikningur uppskrifta tilgreindan kostnað vörunnar.

## <a name="calculation-groups"></a>Reikniflokkar
Þú skilgreinir reikniflokka í **uppsetning fyrir reglur fyrirframákveðins kostnaðar** í kostnaðarstjórnun. Reikniflokka sem eru tengdir vörum leyfa þér að tilgreina hvernig kostnaðarverð eða söluverð, eins og það er tilgreint í reikniflokkunum, er fundið fyrir útreikninginn. Á **reikniflokka** síðu er hægt að skilgreina kostnaðarverðslíkan, annað kostnaðarverðslíkan, söluverðslíkan og viðvaranir.

### <a name="cost-price-model"></a>Kostnaðarverðslíkan

Það eru fjórar valkosti fyrir **kostnaðarverðslíkan** svæði:

-   **Kostnaðarverð vöru** – kostnaðarverð úr **útgefin afurð** töflu er notuð, eða samsetningu af vöruvíddum er notað sem kostnaðarverð.
-   **Innkaupaverð vöru** – innkaupaverð úr á **kostnaðarverð** reit á **Innkaupa** flipanum á **listi yfir útgefnar afurðir** síða er notuð.
-   **Viðskiptasamninga** – hægt er að skilgreina viðskiptasamninga fyrir tiltekna samsetningar vara og lánardrottna, eða fyrir tiltekin svæði. Svo þegar valin er **Viðskiptasamninga** valkostinum hér, eru notuð verðsamningur sem þú stofnaðir fyrir innkaupaverð ásamt vöru og svæði.
-   **Birgðaverð** – gildandi birgðavirði fyrir vöru er notað til að reikna einingarkostnað í útreikningi Uppskrifta. Kostnaðarverð einingar er aðeins reiknaður ef bókaða magnið og efnislegt magn er meira en 0 (núll).

### <a name="alternative-cost-price"></a>Annað kostnaðarverð

**Önnur kostnaðarverðs** svæði er með sömu valkosti og reiturinn **kostnaðarverðslíkan**. Hins vegar er þetta svæði aðeins notað þegar verð finnst ekki í aðal kostnaðarverðslíkani.

### <a name="sales-price-model"></a>Söluverðlíkan

Það eru tveir valkostir fyrir útreikning á **söluverð** svæðinu:

-   **Kostnaðarflokkur** – Þegar þessi valkostur er valinn, verður söluverð reiknað byggt á kostnaðarverði og hagnaðarprósentu stillingu úr kostnaðarflokk.
-   **Söluverð vörunnar** – Þegar þessi valkostur er valinn, er söluverð á **Selja** Flýtiflipa úr tafla Útgefinnar afurðar notað.

### <a name="stop-explosion"></a>Stöðva niðurbrot

**Stöðva niðurbrot** gátreiturinn er notaður til að tilgreina hvenær framleidd vara skuli vera meðhöndluð sem innkaupavara. Yfirleitt, skilurðu **Stöðva niðurbrot** gátreitinn eftir hreinsaðan. Með því að velja gátreitinn er gefa til kynna að framleidd vara skuli meðhöndluð eins og innkeypt vara frekar en sem framleiðsluvara þegar uppskriftaútreikningar eiga sér stað. Samkvæmt svæðinu, er Samt sem áður hægt að reikna út kostnað vörunnar með því að nota uppskriftaútreikninga. Niðurbrot áætlaðar innkaupapantanir og framleiðslupantanir er stöðvuð hjá Uppskrift, en íhlutir hennar eru tengdir við reikniflokk sem gátreiturinn **Stöðva niðurbrot** er valinn fyrir. Aðalröðun myndar áætlaðar pantanir í uppskriftinni sjálfri og ekki í vörunum sem eru innifalin í uppskriftinni. Í raun, með því að velja þennan gátreit er hægt að tilgreina kostnaði verður ekki bætt við útreikningi Uppskrifta fyrir vörur með þessum reikniflokki.

### <a name="warnings"></a>Viðvaranir

Á **Viðvaranir** flýtiflipa, velurðu valkosti fyrir öll viðvörunarboð sem notendur eiga að fá þegar þeir gera útreikninga Uppskrifta. 

Til dæmis, ef valið er **engin Uppskrift** gátreiturinn, fær notandinn viðvörun ef engin virk uppskriftarútgáfa finnst fyrir einn af íhlutina eða yfirvöru sem útreikning Uppskriftar er keyrður fyrir. ef valið er **engin leið** gátreiturinn, fær notandinn viðvörun ef engin virk leiðarútgáfa finnst. Ef verið er að nota tilföng á leiðum þínum og aðgerðum, geturðu látið kerfið athuga eftir þessum tilföngum. Svo, ef tilfang finnst ekki á hverri línu á virku leiðinni, fær notandinn viðvörun. 

Einnig er hægt að staðfesta og athuga notkun. Notkun er magn á tiltekinni leið. Yfirleitt stendur hún fyrir þann tíma sem krafist er til að framkvæma ákveðinni aðgerð fyrir framleiðsluferli. Hægt er að athuga hvort vara hefur ekki kostnaðarverð. Ef ekkert virkt kostnaðarverð er fyrir vöru, er engan kostnað bætt í útreikningi Uppskrifta. 

Einnig er hægt að athuga og staðfesta aldur kostnaðarverðs. Til dæmis, færa inn **60** til að gefa til kynna að kostnaðarverð einingar verður að vera endurmetið eftir 60 daga. Ef þessi þessum mörkum er náð, myndar kerfið viðvörun. Til dæmis var kostnaðarverð færð inn fyrir vöru í Janúar á þessu ári. Ef það er nú Ágúst, sem er meira en 60 daga eftir að kostnaðarverð var færð inn, fær notandinn viðvörun þegar Útreikningur uppskrifta er keyrð. Hægt er að færa inn prósentu í á **lágmarks framlegð** svæði. Þetta gildi gefur til kynna þann punkt sem lágmarks framlegð er ekki uppfyllt. Ef framlegð á tilteknum íhlut er ekki uppfyllt fær notandinn viðvörun. Þess vegna hjálpar svæðið að tryggja að þú verðleggir ekki undir kostnaði og viðbótar birgðahaldskostnaði sem gæti verið nauðsynleg fyrir vörurnar.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Sjálfgefin uppsetning í Færibreytur birgða- og vöruhússstjórnunarkerfis

Vegna þess að reikniflokka er krafist til að keyra útreikning, verður að setja upp sjálfgefinn reikniflokka í færibreytur birgðastjórnunar. Þessi uppsetning gerir fyrirtækjum kleift að hafa flokk staðalkostnaðar og hagnaðarstillingu fyrir allar vörur. Svo, ef tiltekin vara hefur þarfir fyrir sérstakan útreikning, getur notandi úthluta annan reikniflokk á þá vörunni. Venjulega er hægt að stilla reikniflokka á íhlut uppskriftarvörur í staðinn fyrir á uppskriftarvörur. Hins vegar þegar viðvörunarskilaboð eru sýnd, má beita reikniflokkum. Reikniflokkur sem er úthlutað á vörur hnekkir sjálfgefin gildi sem sett er upp í færibreytum birgðastjórnunar. 

Hægt er að setja upp sjálfgefna færibreytu á **kostnaðarstjórnun** &gt; **uppsetning á reglum birgðabókhalds** &gt; **Færibreytum** &gt; **birgðabókhald** &gt; **reikniflokkur**. Með því að setja upp sjálfgefið afbrigðisflokkur, má einnig skilgreina viðvörunarskilyrði sem láta notendur vita á meðan á ferli Útreikningur uppskrifta stendur, ef valdir íhlutir gætu valdið villum í útreikningi.

### <a name="view-warning-messages-on-the-complete-page"></a>Skoða viðvörunarskilaboð á síðunni lokið

Útreikningur uppskrifta myndar viðvörunarskilaboð. Hægt er að skoða viðvaranir um valda vöruna. Til dæmis í Sölu og markaðssetningar, stofna nýja sölupöntun fyrir vöru D0001. Síðan, á sölupöntunarlínuna, á **Uppfæra línu** valmynd, smellið á **Reikna Byggt á Uppskrift/Formúlu** til að skoða upplýsingar um útreikning og viðvaranir. Einnig er hægt að skoða niðurstöður Útreikningur uppskrifta á síðunni **Lokið**. Fyrir viðvörunarboðin, eiga einungis Tvö viðvörunarskilyrði við um framleidda vöru, en fjögur viðvörunarskilyrði eiga við um allar vörur.
-   Greinið hvenær framleidd vara hefur ekki virkum uppskriftum.
-   Greinið hvenær framleidd vara hefur ekki virka leið.
-   Greinið þegar varan í uppskriftarlínunni er með magn skráð 0 (núll).
-   Greinið þegar varan í uppskriftarlínunni er með kostnað skráð 0 (núll), eða þegar það er ekki með kostnaðarfærslu.
-   Greinið þegar varan í uppskriftarlínunni er með skráðan úreltan kostnað. Viðvörunin endurspeglar samanburð á dagsetningu útreiknings við þann skilgreinda aldur sem kostnaður má hafa.
-   Greinið þegar vara í uppskriftarlínu hefur lægri arðsemisprósentu heldur en óskað er eftir.

Hægt er að skilgreina margar flokka uppskriftaútreikninga, eftir kröfum fyrir frávik í viðvörunarskilaboðum. Til dæmis, einn flokkur uppskriftarútreiknings með viðvörunarskilyrðum um virka uppskrift, magn íhluta uppá 0 (núll), og kostnaður íhlutar uippá 0 (núll) gæti verið nóg. viðvörunarskilyrði sem tengjast flokki uppskriftaútreikninga má hnekkja þegar uppskriftarútreikningar eru settir af stað. Einnig er hægt að bæta við eða fjarlægja viðvörunarskilyrði. Til dæmis, er hægt að fjarlægja tiltækt viðvörunarskilyrði um virka leið þegar ákveðnar aðstæður fela ekki í sér leiðargögn. **Athugið:** Tíma og viðveru inniheldur í **reikniflokka** síðu, en sú síðu hefur engin tengsl við flokka uppskriftaútreikninga. Í Tími og viðvera er hægt að úthluta starfsmönnum á reikniflokka sem endurspegla hóp starfsmanna sem eru tengdir við sama yfirmann eða stjórnandi. Útreikning á starfsmannaskráningu er gert annað hvort sjálfvirkt eða handvirkt af yfirmaður eða stjórnandi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]