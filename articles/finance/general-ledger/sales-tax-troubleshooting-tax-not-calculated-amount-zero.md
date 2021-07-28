---
title: Skatturinn er ekki reiknaður eða skattupphæðin er núll
description: Þetta efnisatriði inniheldur villuleitarupplýsingar sem geta hjálpað þegar skattaupphæðin er 0 (núll) eða skatturinn er ekki reiknaður.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c731e0284b720394059384e21deea1ea4407718c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352811"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Skatturinn er ekki reiknaður eða skattupphæðin er núll

[!include [banner](../includes/banner.md)]

Færsla gæti verið með línuupphæð sem er ekki 0 (núll) en annaðhvort er skatturinn ekki reiknaður eða reiknaður skattupphæð er 0. Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Staðfestu að skattkóðar séu rétt valdir af færslunni

Ef færslan velur ekki rétta skattkóða eða, ef hún velur enga skattkóða, verða skattar ekki reiknaðir út af henni. Fylgið eftirfarandi skrefum til að staðfesta að skattkóðar séu rétt valdir af færslunni. 

1. Í færslulínunni, í flýtiflipanum **Upplýsingar um línu**, í flipanum **Uppsetning**, í hlutanum **Virðisaukaskattur**, skal staðfesta réttur skattflokkur hafi verið valinn í reitunum **VSK-flokkur vöru** og **VSK-flokkur**. Ef réttir skattflokkar eru ekki valdir skaltu velja þá.

    [![Reitir VSK-flokks vöru og VSK-flokks.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkar**.
3. Veljið viðeigandi VSK-flokk og síðan í flýtiflipanum **Uppsetning** skal hafa í huga skattkóðann í reitnum **VSK-kóði**.

    [![Síða VSK-flokks.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **VSK-flokkur vöru**.
5. Veljið viðeigandi VSK-flokk vöru og síðan í flýtiflipanum **Uppsetning** skal staðfesta að skattkóðinn í reitnum **VSK-kóði** passi við skattkóða VSK-flokksins.

    [![Síðan VSK-flokkur vöru.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Ef VSK-kóðarnir passa ekki saman skaltu uppfæra VSK-kóðann fyrir einn af hópunum.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Staðfestið að vödlu skattkóðarnir séu ekki undanþegnir og að þeir hafi rétt skatthlutfallsgildi

Ef skattkóðarnir eru undanþegnir, eða ef skatthlutfallið er 0 (núll), verður útreikningsniðurstaða skatts 0. Fylgið eftirfarandi skrefum til að ákvarða hvort valdir skattkóðar séu undanþegnir og til að staðfesta að rétt skatthlutfall sé notað fyrir þá.

1. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkar**.
2. Veljið viðeigandi VSK-flokk og síðan í flýtiflipanum **Uppsetning** skal staðfesta að gátreiturinn **Undanþegið** sé hreinsaður. Ef hann er valinn skal hreinsa hann.

    [![Gátreitur undanþágu á síðu VSK-flokka.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.
4. Veljið viðeigandi VSK-kóða og staðfestið síðan að skatthlutfallsgildi í reitnum **Gildi** sé ekki 0 (núll). Ef það er 0 skal uppfæra reitinn þannig að hann sé stilltur á rétt skatthlutfall.

    [![Reitur gildis á síðu fyrir gildi VSK-kóða.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Ákvarðið hvort núll sé rétt skattupphæð

Í sumum tilvikum er skattfjárhæðin 0 (núll) rétt. Fylgið eftirfarandi skrefum til að ákvarða hvort 0 sé rétt skattfjárhæð fyrir færsluna.

1. Opnið **Fjárhagur** \> **Fjárhagsuppsetning** \> **Færibreytur fyrir fjárhag**.
2. Á flipanum **Söluskattur** í reitnum **Útreikningsaðferð** skal staðfesta að **Alls** sé valin.

    [![Reitur reikningsaðferðar á færibreytusíðu fjárhags.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.
4. Veljið viðeigandi VSK-kóða, veljið **Útreikningur** \> **Jaðargrunnur** og staðfestið að jaðargrunnurinn sé stilltur á **Nettóupphæð af reikningsstöðu** eða **Samtala reiknings að meðtöldum öðrum VSK-upphæðum**. Frekari upplýsingar eru í [Samtala reiknings að meðtöldum öðrum VSK-upphæðum](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Ef rétt gildi eru stillt í skrefum 2 og 4 skal ákvarða hvort heildarupphæð færslunnar sé 0 (núll). Ef heildarupphæðin er 0 er skattupphæð 0 væntanleg niðurstaða. Þar sem skattaútreikningurinn er byggður á heildarupphæð reikningsupphæðarinnar, og upphæðin er ekki lína fyrir línu, verður skattupphæðinni 0 úthlutað á hverja línu eftir skattaútreikninginn.

## <a name="determine-whether-customization-exists"></a>Ákvarða hvort sérstilling sé til staðar

Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar. Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
