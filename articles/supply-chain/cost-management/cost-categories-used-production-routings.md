---
title: "Um kostnaðartegundir notaðar í leiðum framleiðslu"
description: "Þessi skrá veitir upplýsingar um kostnaðartegundirnar sem eiga við um framleiðsluumhverfi sem nota leiðir."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b1c3af55423677a95e9ab5a230c91913058f91ef
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="cost-categories-used-in-production-routing"></a>Um kostnaðartegundir notaðar í leiðum framleiðslu

[!include[banner](../includes/banner.md)]


Þessi skrá veitir upplýsingar um kostnaðartegundirnar sem eiga við um framleiðsluumhverfi sem nota leiðir.

Kostnaðartegundir eiga við um framleiðsluumhverfi sem nota leiðir. Kostnaðartegundir eru úthlutaðar rekstrartilföngum og leiðaraðgerðum í þeim tilgangi að skilgreina tímakostnað og hluta kostnaðarframlegð útreiknuðum kostnaði framleiddrar vöru. Kostnaðarflokkurinn sem er úthlutaður kostnaðartegundinni flokkar framlegð framleiðslukostnaðar eftir rekstrartilföngum og gerð verkþáttar eins og uppsetningar- og keyrslutíma. Sérhæfni úthlutunar kostnaðarflokka gerir kleift að reikna út grundvöllinn fyrir framleiðslurekstrarkostnaði á grundvelli leiðarupplýsinga. 

**Athugið:**Kostnaðartegundir hafa nokkur samheiti innan framleiðsluumhverfa eins og vinnutaxtakóðar eða vélataxtakóðar. 

Hver kostnaðartegund hefur sína tengda kostnaðarfærslu og úthlutaðan kostnaðarflokk. Mismunandi kostnaðartegundir þarf til að styðja mismunandi framleiðslutilgang.

-   Að úthluta mismunandi tímakostnaði, eftir aðgerðum tilfanga. Til dæmis getur kostnaður verið misjafn fyrir ýmsar gerðir af vinnuhæfni, vélum eða framleiðsluhólfum.
-   Úthluta mismunandi tímakostnaði til uppsetningartíma eða keyrslutíma sem er tengdur við leiðaraðgerð.
-   Úthluta vinnustöðvarkostnaði á grundvelli úttaksmagns frekar en tímakostnaðar eins og stykkjataxta fyrir greiðslu vinnu.
-   Kostnaðarflokkun vöru býður upp á sundurliðun kostnaðarframlags í útreiknuðum kostnaði framleiddrar vöru. T.d. er hægt að sundurliða vinnu og vélarkostnað.
-   Útvega kostnaðarflokknum grundvöll fyrir útreikningsformúlur rekstrarkostnaðar eins og vinnutengdum og vélatengdum rekstrarkostnaði eða rekstrarkostnaði sem er tengdur uppsetningu og keyrslutíma.

Hægt er að úthluta kostnaðartegund til uppsetningartímans, vinnslutímans og magnsins fyrir leiðaraðgerð. Þegar kostnaður eða hlutun kostnaðarflokka eru til dæmis mismunandi á milli uppsetningar- og vinnslutíma ætti að skilgreina mismunandi kostnaðartegundir og úthluta þeim á uppsetningar- og vinnslutíma. Sérvalin notkun kostnaðartegunda fyrir uppsetningartíma, vinnslutíma og magn ákvarðast af leiðarflokknum sem er úthlutaður aðgerð. Úthlutun kostnaðartegunda til tíma og magns er hægt að gera að skyldu á grundvelli þeirra fyrirtækisreglna sem eru felldar inn í skjámyndina **Færibreytur framleiðslustýringar**. 

Hver kostnaðartegund hefur sinn tengda kostnað sem er byggður á skilgreiningunni á kostnaðarfærslum innan kostnaðarútgáfu. Nota skal síðuna **Kostnaðartegundarverð** til að skilgreina kostnaðarfærslurnar fyrir tiltekna útgáfu kostnaðarútreiknings og setur. Þegar kostnaðarfærsla kostnaðartegundar er upphaflega færð inn hefur hún stöðuna **Í bið** og áætlaða gildisdagsetningu. Þegar kostnaðarfærsla vöru er virkjuð uppfærist staðan í **Nú í gildi** og gildisdagsetningin er uppfærð í virkjunardagsetningu. Mismunandi kostnaðarfærslur geta endurspeglað ólík svæði, gildisdagsetningu eða stöðu. Uppskriftarútreikningar fyrir dagsetningu í framtíðinni eða fortíðinni munu nota kostnaðarfærslur með viðeigandi gildisdagsetningu. Gildandi virka kostnaðarfærslan verður notuð til að meta framleiðslupöntunarkostnað og virða skráðan tíma á móti framleiðslupöntun. 

Kostnaðarfærslurnar fyrir kostnaðartegund geta endurspeglað reikniformúlu fyrir fyrirtæki eða ákveðið svæði. Kostnaðarfærslan mun eiga við um setur er henni er úthlutað setur. Annars þýðir autt gildi að kostnaðarfærslan muni eiga við um öll setur innan fyrirtækisins. Vegna þess að kostnaður getur verið mismunandi á milli setra þarf til dæmis að skilgreina kostnaðarfærslur sem svo að þær eigi við um eitt setur. 

Leiðaraðgerð fær yfirleitt kostnaðartegundirnar sem eru úthlutaðar rekstrartilföngum eða aðalaðgerðinni. Þegar framleiðslupöntun er stofnuð endurspegla leiðaraðgerðirnar innan framleiðsluleiðarinnar völdu leiðaraðgerðina. Hægt er að hnekkja kostnaðartegundunum sem úthlutaðar eru aðgerðum framleiðsluleiðarinnar. 

Sumar gerðir framleiðslu geta átt við um mat á verktíma og skýrslur. Í þessu tilfelli er kostnaðartegundar krafist fyrir framleiðslu og verk. Nánari verktengdar upplýsingar þarf að skilgreina þegar kostnaðartegund er merkt til notkunar í verkum.




