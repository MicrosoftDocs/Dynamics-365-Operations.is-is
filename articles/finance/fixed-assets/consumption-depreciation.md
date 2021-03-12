---
title: Notkunarafskriftir
description: Þessi grein gefur yfirlit yfir notkunaraðferð afskriftar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e78e2481724aede93ecb997d95a0ef8032618bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989028"
---
# <a name="consumption-depreciation"></a>Notkunarafskriftir

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir notkunaraðferð afskriftar.

Ef afskriftaregla fyrir eignir er sett upp og valið er **notkun** í reitnum **Aðferð** á skjámyndinni **Afskriftaaðferðir** eru eignir tengdar þessari afskriftareglu og samkvæmt notkun þeirra. Ekki þarf að setja upp prósentur og tímabil í á **afskriftareglur** síðu. Eftir að þú stofnar afskriftarregla sem notar notkunaraðferð, er hægt að setja aðferðina upp á nokkra vegu.

## <a name="set-up-and-use-consumption-depreciation"></a>Setja upp og nota notkunarafskrift.
1.  Á síðunni **afskriftarregla** skal stofna afskriftarreglu. Fyrir notkunarútreikninga verður afskriftareglan að innihalda kenni, heiti og **notkun** verður að vera valin í reitnum **aðferð**.
2.  Á **Notkunarstuðull** síða, setja upp notkunarstuðull. Hvern notkunarstuðul verður að hafa Kenni og heiti, og notkunarstuðul sem er tilgreindur sem magn eða prósenta.
3.  Á **notkunareining** síðuna setja upp notkunareiningar. Hver notkunareining verður að hafa Kenni og heiti Afskriftareiningar eru notaðar til að reikna notkunarafskrift á **notkunarafskrift** síðu. Dæmi um einingar eru kílómetrar (km), kílógrömm (kg) og klukkustund.
4.  Á **Eignir** síðu setja upp einstaka eignir. Fyrir hverja eign, veldu Virðislíkön og afskriftarbækur sem eru með afskriftarreglur. Setja verður upp virðislíkan eða afskriftarbók fyrir notkunarafskrift ef einhver af eignum þínum notar afskriftarregla sem byggist á notkunaraðferðinni. Þessari uppsetningu er að gera annaðhvort á í **Afskriftir** flipanum á **Virðislíkön** síðu eða á í **Almennt** flýtiflipi af **afskriftareglu** síðu. Hægt er að nota sama virðislíkan fyrir margar eignir. Afskriftareglur eru hluti af virðislíkani eða afskriftarbók sem valin er fyrir hverja eign. Ekki er hægt að bæta við eða breyta afskriftareglur beint á í **Eignir** síðu. Hægt er að breyta afskriftarreglum aðeins á **afskriftabækur** síðu.
5.  Á síðunni **Virðislíkan** eða síðunni **Afskriftarbók** í reitahópnum **Notkunarafskrift** skal færa upplýsingar í eftirtalin svæði:
    -   Notkunarstuðull
    -   Eining
    -   Einingaafskriftir
    -   Metin notkun

    Svæðið **bókun notkun** sýnir notkunarafskriftareiningar, sem hafa þegar verið bókaðar annað hvort blöndu af eign og virðislíkan, eða fyrir afskriftarbók Handvirkt er ekki hægt að uppfæra gildið í þessu svæði.

## <a name="examples"></a>Dæmi
### <a name="example-1"></a>Dæmi 1

Eftirfarandi notkunarstuðull er settur upp fyrir 31. janúar:

-   Magnið 1,000.
-   Afskriftarverð einingar sem er tilgreint fyrir eignarinnar er 1,5.

Afskriftatillagan þann 31. Janúar er á eftirfarandi: Magn × einingarafskrift 1.000 × 1,5 = 1,500 Ef stuðullinn sem er tilgreint fyrir eignina er prósentustuðull er magnið sem metið er í **Metin notkun** reit fyrir virðislíkan eignarinnar er margfaldað með prósentunni sem sett er upp fyrir valda lokadagsetningu. Meðfylgjandi magnið er svo lagt til sem afskriftarmagn fyrir tímabilið.

### <a name="example-2"></a>Dæmi 2

Eftirfarandi stuðull fyrir notkunarafskrift er setja upp fyrir janúar 31:

-   Prósenta er 10 prósent.
-   Afskriftarverð einingar sem er tilgreint fyrir eignarinnar er 1,5.
-   Metið magn eignarinnar er 2.000.

Afskriftatillagan þann 31. Janúar er á eftirfarandi hátt: áætlað magn × Prósentu × einingarafskrift 2.000 ×.10 × 1,5 = 300



