---
title: Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum
description: Þetta efnisatriði útskýrir hvernig gildin í svæðunum jaðargrunnur og útreikningsaðferð ákvarða skatthlutfall í sölu- og innkaupafærslum.
author: ShylaThompson
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c98bde5bff55d6c1b1af47e7cd150f828e73655275901591aaf698c0831f7d01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768316"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig gildin í svæðunum jaðargrunnur og útreikningsaðferð ákvarða skatthlutfall í sölu- og innkaupafærslum.

Jaðargrunnurinn á flýtiflipanum Útreikningur á síðunni VSK-kóðar ákvarðar hvaða upphæð er notuð til að velja viðeigandi skatthlutfall úr skatthlutfallinu á síðunni Gildi VSK-kóða. Gerð upphæðar í jaðargrunni ásamt aðferðinni í reitnum Útreikningsaðferð ákvarðar rökin til að finna rétt skatthlutfalls fyrir færslu. 

Mismunandi samsetning gilda í þessum svæðum leiðir til mjög ólíkra VSK-útreikninga, eins og sést í eftirfarandi dæmum. Dæmin nota sömu gildi skattatímabila, sem eru sett upp fyrir hvern skattkóða á síðunni Gildi VSK-kóða. Til að opna þessa síðu er smellt á VSK-kóði &gt; Gildi á síðunni VSK-kóði.

> [!Important]                                                                                                                  
> Ef jaðargrunnurinn í einum eða fleiri VSK-kóðanna er byggður á línuupphæðum eða einingu, verður gildið í reitnum Útreikningsaðferð í skjámyndinni Færðibreytur fjárhags að vera stillt á Lína. |

## <a name="net-amount-per-line"></a>Nettóupphæð á línu
Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggðan á nettóupphæð í reikningslínum, án allra annarra skatta.

### <a name="example"></a>Dæmi

Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:

| Upphæðarbil    | Skatthlutfall |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

> [!NOTE]                                                                                                             
> Efri mörkin núll (0) í síðasta tímabili þýðir að allar upphæðir yfir 100 eru hafðar með í bilinu.

Jaðargrunnur: **Nettóupphæð á línu** 

Útreikningsaðferð: **Tímabil** 

Keyptir eru 8 lampar sem kosta 25,00 hver. 

Nettóupphæðin fyrir reikningslínuna er 200,00. 

Skatturinn er reiknaður sem hér segir: 

Heildarsöluskattur = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00 

Heildarupphæð reiknings = 200,00 + 35,00 = 235,00 

**Breytileiki** 

Ef reikningur hefur tvær línur með fjórum atriðum í hverri línu er nettóupphæð í hverri línu 100,00 og virðisaukaskattur er reiknaður á eftirfarandi hátt: 

Virðisaukaskattslína 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00 

Virðisaukaskattslína 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00 

Heildarupphæð virðisaukaskatts = 25,00 + 25,00 = 50,00 

Heildarupphæð reiknings = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a>Nettóupphæð á einingu
Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggðan á gildi hverrar einingar, án allra annarra skatta. Þegar eining út jaðargrunnurinn er valin verður einnig að tilgreina einingu fyrir VSK-kóðann.

### <a name="example"></a>Dæmi

Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:

| Upphæð             | Skatthlutfall |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Jaðargrunnur: **Nettóupphæð á einingu** 

Reikningsaðferð: **Öll upphæðin** 

Keyptir eru 8 lampar sem kosta 25,00 hver. 

Nettóupphæðin fyrir reikningslínuna er 200,00. 

Skatturinn er reiknaður sem hér segir: VSK á einingu = 25,00 x 30% = 7,50 Heildarupphæð vsk = 7,50 x 8 einingar = 60,00 Heildarreikningsupphæð = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a>Nettóupphæð af reikningsstöðu

Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggt á heildarvirði reikningsins, án allra annarra skatta.

### <a name="example"></a>Dæmi

Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:

| Upphæð            | Skatthlutfall |
|-------------------|----------|
| 0 - 50            | 30%      |
| 50 - 100          | 20%      |
| 100 -0 (&gt; 100) | 10%      |

Jaðargrunnur: **Nettóupphæð af reikningsstöðu** 

Útreikningsaðferð: **Bil** Sölureikningur með 2 línur með 4 lampa hverja línur fyrir 25,00 hver. Nettóupphæð af reikningsstöðu er 4 x 25,00 + 4 x 25,00 = 200,00. Skatturinn er reiknaður sem hér segir: Heildarsöluskattur = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 +10 = 35,00 Heildarreikningsupphæð = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a>Brúttó upphæð eftir línu

Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggt á línunni, ásamt öllum öðrum sköttum fyrir línuna.

> [!NOTE]
> Í VSK-flokki er aðeins hægt að hafa einn VSK-kóða með þessu vali í reitnum Jaðargrunnur.

### <a name="example"></a>Dæmi

Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:

| Upphæð             | Skatthlutfall |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Jaðargrunnurinn: **Brúttóupphæð eftir línu** Útreikningsaðferð: **Bil** Þar að auki er annar VSK-kóði reiknaður fyrir sérstakt gjald upp á 5,00 fyrir hvern lampa. Gjaldinu er bætt við nettóupphæðina áður en VSK er reiknaður út. Keyptir eru 8 lampar sem kosta 25,00 hver. Nettóupphæðin fyrir reikningslínuna er 200,00. Brúttóupphæð fyrir reikningslínuna er 8 x 25,00 + 8 x 5,00 = 240,00. Skatturinn er reiknaður sem hér segir: Heildarvirðisaukaskattur = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Heildargjöld = 5,00 x 8 = 40,00 Heildarreikningsupphæð = 200,00 + 39,00 + 40,00 = 279,00

**Breytileiki** 

Ef reikningur er stofnaður með því að nota 2 reikningslínur með 4 vörum í hverri línu er nettóupphæð fyrir línu 100,00. Brúttóupphæð (með gjaldi 4 x 5,00) hverrar reikningslínu væri 120,00 og VSK er stofnuður á eftirfarandi hátt: Lína VSK-reiknings 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Lína VSK-reiknings 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Samtals virðisaukaskattur = 27,00 + 27,00 = 54,00 Heildargjöld = 5,00 x 8 = 40,00 Heildarreikningsupphæð = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a>Brúttó upphæð á einingu

Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggðan á einingunni, ásamt öllum öðrum sköttum.

> [!NOTE]
> Í VSK-flokki er aðeins hægt að hafa einn VSK-kóða með þessu vali í reitnum Jaðargrunnur.

### <a name="example"></a>Dæmi

Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:

| Upphæð             | Skatthlutfall |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Jaðargrunnurinn: **Brúttóupphæð á einingu** Það er sérstakt gjald upp á 5,00 fyrir hvern lampa. Gjaldinu er bætt við nettóupphæðina áður en VSK er reiknaður út. Keyptir eru 8 lampar sem kosta 25,00 hver. Brúttóupphæð á einingu er 30,00. Skatturinn er reiknaður sem hér segir: Virðisaukaskattur á einingu = 30 x 30% = 9,00 Heildarvirðisaukaskattur = 9,00 x 8 = 72,00 Heildargjöld = 5,00 x 8 + 40,00 Heildarreikningsupphæð = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a>Samtala reiknings að meðtöldum öðrum VSK-upphæðum

Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggt á heildarvirði reikningsins, ásamt öllum öðrum sköttum.
> [!NOTE]
> Í VSK-flokki er aðeins hægt að hafa einn VSK-kóða með þessu vali í reitnum Jaðargrunnur

### <a name="example"></a>Dæmi

Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:

| Upphæð             | Skatthlutfall |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100 - 0 (&gt; 100) | 10%      |

Jaðargrunnur: **Heildarupphæð reiknings að meðtöldum öðrum VSK-upphæðum** Útreikningsaðferð: **Bil**   
Það er sérstakt gjald upp á 5,00 fyrir hvern lampa. Gjaldinu er bætt við nettóupphæðina áður en VSK er reiknaður út. Keyptir eru 8 lampar sem kosta 25,00 hver. Nettóupphæðin fyrir reikning er 200,00. Brúttóupphæð fyrir reikningslínuna er 200,00 + (8 x 5,00) = 240,00. Skatturinn er reiknaður sem hér segir: Heildarvirðisaukaskattur = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Heildargjöld = 5,00 x 8 = 40,00 Heildarreikningsupphæð = 200,00 + 39,00 + 40,00 = 279,00

Frekari upplýsingar eru í [Útreikningsaðferð heildarupphæðar og tímabils fyrir VSK-kóða](whole-amount-interval-options-sales-tax-codes.md) og [Aðferðir útreiknings VSK í upprunareitnum](sales-tax-calculation-methods-origin-field.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]