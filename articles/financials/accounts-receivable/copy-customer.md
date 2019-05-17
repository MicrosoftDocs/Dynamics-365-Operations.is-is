---
title: Afrita viðskiptavini með því að nota samnýttar númeraraðir
description: Þetta efnisatriði útskýrir hvernig á að nota samnýtta númeraröð til að afrita viðskiptavin á annan lögaðila en halda sama kenni viðskiptavinar.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a92110cdbe58e2dbb913596ba08780ac3a6b50a7
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507060"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Afrita viðskiptavini með því að nota samnýttar númeraraðir

[!include [banner](../includes/banner.md)]

Hægt er að nota samnýttar númeraraðir til að úthluta kennum viðskiptavina. Samnýttar númeraraðir gera einnig kleift að afrita viðskiptavini frá einum lögaðila til annars lögaðila en nota sömu kenni viðskiptavinarins fyrir báða lögaðila.

## <a name="setup"></a>Setja upp

Þessi eiginleiki er virkjaður þegar samnýtt númeraröð er notuð til að úthluta kennum viðskiptavina. Nota verður sömu númeraröð fyrir hvern lögaðila sem á að afrita viðskiptavin til. Númeraröð viðskiptavinar er breytt á síðunni **Færibreytur viðskiptakrafna** fyrir hvern lögaðila. Veljið **Viðskiptakröfur** \> **Færibreytur**, og veljið síðan flipann **Númeraraðir**.

Einnig er hægt að setja upp númeraröð viðskiptavinar fyrir hvern viðskiptavinaflokk. Þessar númeraraðir verður einnig að samnýta. Númeraröðin fyrir viðskiptavinaflokk er notuð fyrst. Ef engin númeraröð er tilgreind fyrir viðskiptavinaflokk er númeraröðin sem er tilgreind á síðunni **Færibreytur viðskiptakrafna** notuð.

Einnig er hægt að afrita viðskiptavini milli lögaðila ef notuð eru handvirk kenni viðskiptavina. Ef hins vegar er reynt að afrita viðskiptavin til lögaðila þar sem kenni viðskiptavinar er þegar til fer afritunarferlið ekki í gang.

## <a name="copy-a-customer"></a>Afrita viðskiptavin

Til að afrita viðskiptavin skal velja **Nýr** á listasíðunni **Allir viðskiptavinir** til að opna svargluggann **Stofna viðskiptavin**. Takið eftir að nýju kenni viðskiptavinar er ekki úthlutað strax. Þetta er ólíkt því sem átti sér stað í fyrri útgáfum Microsoft Dynamics 365 for Finance and Operations. Þar sem viðskiptavinaflokkur hefur enn ekki verið valinn getur kerfið ekki ákvarðað rétta númeraröð til að nota. Þar að auki getur kerfið ekki ákvarðað hvort verið er að reyna að búa til nýjan viðskiptavin eða afrita viðskiptavin. Þess vegna er ekki hægt að úthluta kenni viðskiptavinar fyrr en valið er **Vista** neðst í svarglugganum.

Ef verið er að búa til nýjan viðskiptavin er hægt að halda áfram að fylla út alla reiti eins og venjulega. Þegar því er lokið og valið hefur verið **Vista** má sjá að kenni viðskiptavinar var úthlutað sjálfkrafa. Að öðrum kosti, þegar um er að ræða handvirkar númeraraðir, má sjá að handvirkt kenni viðskiptavinar var notað.

Til að afrita viðskiptavin skal slá inn eitt eða fleiri tákn í reitinn **Heiti** sem tákna viðskiptavininn sem leitað er að. Leitargluggi sýnir lista yfir aðila sem gætu táknað viðskiptavininn sem verið er að leita að. Þegar einn þeirra aðila er valinn birtast nánari upplýsingar hægra megin við svargluggann:

- Flipinn **Almennt** sýnir símanúmer og heimilisfang aðilans.
- Flipinn **Hlutverk** sýnir hlutverkin sem valinn aðili getur haft og lögaðilinn þar sem hann hefur hvert hlutverk.
- Flipinn **Skattskráningarkenni** sýnir þau skattskráningarkenni sem er úthlutað á viðkomandi aðila.

Aðeins er hægt að afrita aðila ef hann hefur hlutverk viðskiptavinar og ef hann hefur það hlutverk hjá lögaðila sem ekki er núgildandi lögaðili. Þegar aðili sem uppfyllir þessi viðmið er fundinn skal fylgja þessum skrefum.

1. Valkosturinn **Afrita viðskiptavin** birtist. Að sjálfgefnu er þessi valkostur stilltur á **Nei**. Til að afrita viðskiptavininn til núverandi lögaðila skal stilla valkostinn á **Já**. 
2. Reiturinn **Lögaðili** birtist. Veljið frá hvaða lögaðila á að afrita viðskiptavininn. Ef viðskiptavinurinn er aðeins til fyrir einn lögaðila er reiturinn að sjálfgefnu stilltur á þann lögaðila.
3. Veljið **Velja**. Nýi viðskiptavinurinn er stofnaður.

## <a name="validation"></a>Villuleit

Þegar viðskiptavinur er afritaður reynir kerfið að vista upplýsingar nýja viðskiptavinarins. Villuleitir eru keyrðar til að staðfesta að gögnin sem afrituð voru séu í lagi. Villuboð berast fyrir hverja villuleit sem mistekst. Villuboðin útskýra hvaða upplýsingar verður að uppfæra. Ekki er hægt að vista afrit viðskiptavinarins fyrr en öll villuboð hafa verið lagfærð.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Afrita viðskiptavin með því að nota leitareiginleika fyrir skattundanþágunúmer

Einnig er hægt að afrita viðskiptavini með því að nota leitareiginleika fyrir skattundanþágunúmer sem er í flokknum **Skráning** á flipanum **Viðskiptavinur** á aðgerðarúðunni á síðunni **Allir viðskiptavinir**. Í svarglugganum **Leita að skattundanþágunúmeri** sem birtist má sjá skattundanþágunúmer, kenni viðskiptavinar, heiti viðskiptavinar og lögaðilann þar sem skattundanþágukennið er notað. Aðeins er hægt að afrita viðskiptavin ef hann er hjá lögaðila sem ekki er núgildandi lögaðili. Eftir að viðskiptavinur sem uppfyllir þessar viðmiðanir hefur verið valinn skal fylgja þessum skrefum.

1. Valkosturinn **Afrita viðskiptavin** birtist. Að sjálfgefnu er þessi valkostur stilltur á **Nei**. Til að afrita viðskiptavininn til núverandi lögaðila skal stilla valkostinn á **Já**. 
2. Veljið **Velja**. Nýi viðskiptavinurinn er stofnaður.
