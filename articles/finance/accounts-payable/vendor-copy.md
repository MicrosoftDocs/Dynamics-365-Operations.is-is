---
title: Afrita lánardrottna með því að nota samnýttar númeraraðir
description: Þessi grein útskýrir hvernig á að nota samnýtta númeraröð til að afrita lánardrottin á annan lögaðila en halda sama kenni lánardrottins.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7b7285cdf454955656c4fb20c3abf68f3f9c39dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904902"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Afrita lánardrottna með því að nota samnýttar númeraraðir

[!include [banner](../includes/banner.md)]

Hægt er að nota samnýttar númeraraðir til að úthluta kennum lánardrottins. Samnýttar númeraraðir gera einnig kleift að afrita lánardrottna frá einum lögaðila til annars lögaðila en nota sama kenni lánardrottins fyrir báða lögaðila.

## <a name="setup"></a>Setja upp

Þessi eiginleiki er virkjaður þegar samnýtt númeraröð er notuð til að úthluta kennum lánardrottna. Nota verður sömu númeraröð fyrir hvern lögaðila sem á að afrita lánardrottin til. Númeraröð lánardrottins er breytt á síðunni **Færibreytur viðskiptaskulda** fyrir hvern lögaðila. Veljið **Viðskiptaskuldir** \> **Uppsetning** \> **Færibreytur viðskiptaskulda**, og veljið síðan flipann **Númeraraðir**.

Einnig er hægt að setja upp númeraröð lánardrottins fyrir hvern lánardrottnaflokk. Þessar númeraraðir verður einnig að samnýta. Númeraröðin fyrir lánardrottnaflokk er notuð fyrst. Ef engin númeraröð er tilgreind fyrir lánardrottnaflokk er númeraröðin sem er tilgreind á síðunni **Færibreytur viðskiptaskulda** notuð.

Einnig er hægt að afrita lánardrottna milli lögaðila ef notuð eru handvirk kenni lánardrottna. Ef hins vegar er reynt að afrita lánardrottin til lögaðila þar sem kenni lánardrottins er þegar til fer afritunarferlið ekki í gang.

## <a name="copy-a-vendor"></a>Afrita lánardrottin

Til að afrita lánardrottin skal velja **Nýr** á listasíðunni **Allir lánardrottnar** til að opna síðuna **Allir lánardrottnar, ný færsla**. Nýju kenni lánardrottins er ekki úthlutað strax. Þetta er ólíkt því sem átti sér stað í fyrri útgáfum. Þar sem lánardrottnaflokkur hefur enn ekki verið valinn er ekki hægt að ákvarða rétta númeraröð sem á að nota. Þar að auki getur kerfið ekki ákvarðað hvort verið er að reyna að búa til nýjan lánardrottin eða afrita lánardrottin. Þess vegna er ekki hægt að úthluta kenni lánardrottins fyrr en valið er **Vista** neðst á síðunni.

Ef verið er að búa til nýjan lánardrottin er hægt að halda áfram að fylla út alla reiti eins og venjulega. Þegar því er lokið og valið hefur verið **Vista** er kenni lánardrottins úthlutað sjálfkrafa. Að öðrum kosti, þegar um er að ræða handvirkar númeraraðir, má sjá að handvirkt kenni lánardrottins var notað.

Til að afrita lánardrottin skal slá inn eitt eða fleiri tákn í reitinn **Heiti** sem tákna þann lánardrottin sem leitað er að. Leitargluggi sýnir lista yfir aðila sem gætu táknað þann lánardrottin sem verið er að leita að. Þegar einn þeirra aðila er valinn birtast nánari upplýsingar hægra megin við svargluggann:

- Flipinn **Almennt** sýnir símanúmer og heimilisfang aðilans.
- Flipinn **Hlutverk** sýnir hlutverkin sem valinn aðili getur haft og lögaðilinn þar sem hann hefur hvert hlutverk.
- Flipinn **Skattskráningarkenni** sýnir þau skattskráningarkenni sem er úthlutað á viðkomandi aðila.

Aðeins er hægt að afrita aðila ef hann hefur hlutverk lánardrottins og ef hann hefur það hlutverk hjá lögaðila sem ekki er núgildandi lögaðili. Þegar aðili sem uppfyllir þessi viðmið er fundinn skal fylgja þessum skrefum.

1. Valkosturinn **Afrita lánardrottin** birtist. Að sjálfgefnu er þessi valkostur stilltur á **Nei**. Til að afrita lánardrottininn til núverandi lögaðila skal stilla valkostinn á **Já**. 
2. Reiturinn **Lögaðili** birtist. Veljið frá hvaða lögaðila á að afrita lánardrottininn. Ef lánardrottinn er aðeins til fyrir einn lögaðila er reiturinn að sjálfgefnu stilltur á þann lögaðila.
3. Veljið **Velja**. Nýi lánardrottinninn er stofnaður.

## <a name="validation"></a>Villuleit

Þegar lánardrottinn er afritaður verður reynt að vista upplýsingar um nýjan lánardrottinn. Villuleitir eru keyrðar til að staðfesta að gögnin sem afrituð voru séu í lagi. Villuboð berast fyrir hverja villuleit sem mistekst. Villuboðin útskýra hvaða upplýsingar verður að uppfæra. Ekki er hægt að vista afrit lánardrottinsins fyrr en öll villuboð hafa verið lagfærð.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Afrita lánardrottin með því að nota leitareiginleikann fyrir skattundanþágunúmer

Einnig er hægt að afrita lánardrottna með því að nota leitareiginleika fyrir **skattundanþágunúmer** sem er í flokknum **Skráning** á flipanum **Lánardrottinn** á aðgerðasvæðinu á síðunni **Allir lánardrottnar**. Í svarglugganum **Leita að skattundanþágunúmeri** sem birtist má sjá skattundanþágunúmer, kenni lánardrottins, heiti lánardrottins og lögaðilann þar sem skattundanþágukennið er notað. Aðeins er hægt að afrita lánardrottin ef hann er hjá lögaðila sem ekki er núgildandi lögaðili. Eftir að lánardrottinn sem uppfyllir þessar viðmiðanir hefur verið valinn skal fylgja þessum skrefum.

1. Valkosturinn **Afrita lánardrottin** birtist. Að sjálfgefnu er þessi valkostur stilltur á **Nei**. Til að afrita lánardrottininn til núverandi lögaðila skal stilla valkostinn á **Já**.
2. Veljið **Velja**. Nýi lánardrottinninn er stofnaður.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
