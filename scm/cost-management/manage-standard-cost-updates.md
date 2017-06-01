---
title: "Stjórnun uppfærslu staðalkostnaðar"
description: "Hægt er að stýra uppfærslum á staðalkostnaðargögnum með því að nota tvær mismunandi nálganir: eins útgáfu nálgun og tveggja útgáfu nálgun."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d1d498b1a843415e106c90330dd661b78bc2865e
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="manage-standard-cost-updates"></a>Stjórnun uppfærslu staðalkostnaðar

[!include[banner](../includes/banner.md)]


Hægt er að stýra uppfærslum á staðalkostnaðargögnum með því að nota tvær mismunandi nálganir: eins útgáfu nálgun og tveggja útgáfu nálgun. 

Eins útgáfu nálgun notar eina kostnaðarútgáfu sem inniheldur allar kostnaðarfærslur. Þessar færslur innifela upprunalegan kostnað og öllum kostnaðaruppfærslum.
Tveggja útgáfu nálgun notar eina kostnaðarútgáfu sem inniheldur færslur upprunalegs kostnaðar og hin útgáfan inniheldur skráningar á öllum kostnaðaruppfærslum. Aðalkosturinn við nálgunina tvær útgáfur er skýr útlistun og rakning kostnaðaruppfærslna í mismunandi útgáfum kostnaðarútreiknings án þess að upprunalega útgáfa kostnaðarútreikningsins verði fyrir áhrifum af því. Tveggja útgáfu nálgun er hægt að nota til að skilgreina margar stigvaxandi uppfærslur, þar sem hver stigvaxandi uppfærsla hefur sína eigin útgáfu kostnaðarútreiknings sem inniheldur stigvaxandi kostnaðarfærslurnar. **Dæmi** eftirfarandi dæmi sýnir hvernig hægt er að nota einnar útgáfu og tveggja-útgáfu nálganir fyrir uppfærslu staðalkostnaðar í framleiðsluumhverfi. Til dæmis uppfærslur sem endurspegla nýjar vörur eða leiðréttingar á villum. Gefum okkur að stök útgáfa kostnaðarútreiknings standi fyrir staðalkostnað núverandi árs. Kenni fyrir þessa útgáfu er 2016 STD. Útgáfa 2016 STD inniheldur núgildandi virkan kostnað fyrir allar vörur. Hún inniheldur allar leiðartengdar kostnaðartegundir og útreikningsformúlur stjórnunarkostnaðar sem þekktust í byrjun árs 2016. 2016-STD er upprunalega kostnaðarútgáfan.
-   **Einnar útgáfu nálgun við uppfærslu kostnaðargagna** − Í Einnar útgáfu nálgun inniheldur upprunalega kostnaðarútgáfa 2016-STD allar kostnaðarfærslur. Kostnaðaruppfærslur eru skráðar í 2016-STD-CHANGES og eru stillt á stöðuna "Í Bið." Biðkostnaður er hægt að færa inn handvirkt fyrir nýju keyptu vörurnar eða þær geta verið reiknað út fyrir framleidda vöru til að endurspegla leiðréttingar. Þegar einnar útgáfu nálgun er notuð, þurfa  uppskriftarútreikningar ekki varaúrræði gagnagjafa af því að allur virkur kostnaður er í kostnaðarútgáfunni. Eftir að búið er að virkja biðstöðukostnaðinn inniheldur upprunalega útgáfa kostnaðarútreikningsins 2016-STD aftur allan núgildandi virkan kostnað.
-   **Tveggja útgáfu nálgun á uppfærslur kostnaðargagna** − tveggja útgáfu nálgunin krefst viðbótar kostnaðarútgáfu sem inniheldur aðeins kostnaðaruppfærslur. kennimerki fyrir þessa útgáfu er 2016-STD-CHANGES Kostnaðaruppfærslur eru skráðar í 2016-STD-CHANGES og eru stillt á stöðuna "Í Bið." Með Tveggja-útgáfu nálgun krefjast uppskriftaútreikninga með kostnað í bið fyrir framleiddar vörur vara gagnagjafa. Þetta er vegna þess að viðbótar kostnaðarútgáfu 2016-STD-CHANGES inniheldur aðeins hlutmengi kostnaðargagna. Hægt er að birta vararegluna sem virka kostnaðinn eða kostnaðarútgáfu 2016-STD vegna þess að bæði tilgreina uppruna kostnaðargagnanna þegar hann er ekki innifalinn í 2016-STD-CHANGES. Eftir að búið er að virkja biðstöðukostnaðinn inniheldur kostnaðarútgáfan 2016-STD-CHANGES núgildandi virka kostnaðinn sem endurspeglar uppfærslurnar á meðan upprunalega kostnaðarútgáfan 2016-STD helst óbreytt. Þegar tveggja útgáfu nálgunin er notuð ætti að setja upp lokunarreglur fyrir upphaflegu kostnaðarútgáfuna til að koma í veg fyrir uppfærslur. Alveg eins lokunarreglur ætti að setja upp fyrir aukalegu kostnaðarútgáfuna, nema fyrir tilgreinda frá-dagsetningu og valfrjálsri notkun lokunarreglna til að gera uppfærslur leyfilegar. Uppfæra ætti dagsetninguna sem tilgreint er frá með hverri breytingarunu til að endurspegla áætlaða virkjunardagsetningu.

Þetta dæmi notaði eina aukaútgáfu kostnaðarútgáfu við stjórnun uppfærslna í gegnum árið 2016. Fleiri en eina aukaútgáfu kostnaðarútgáfu er hægt að nota, eins og aðskilda útgáfu fyrir hverja uppfærslurunu. Þegar fleiri en ein viðbótar kostnaðarútreikningur er notað, verður varaútgáfan að vera sýnd sem virka kostnaðinn, af því virkan kostnað eru dreifast yfir margar kostnaðarútgáfur.






