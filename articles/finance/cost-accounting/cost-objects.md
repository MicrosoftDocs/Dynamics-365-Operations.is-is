---
title: Víddir kostnaðarhluta
description: Þegar kostnaður er greindur, notarðu víddir kostnaðareiningar til að ákvarða hvert kostnaður streymir. Víddir kostnaðarhlutar eru notaðar til að ákvarða hvert á að úthluta kostnaði. Þetta efni inniheldur upplýsingar um víddir kostnaðarhlutar.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 90d9176a2ca37b581ef82306cc1ceef515ceb624
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187890"
---
# <a name="cost-object-dimensions"></a>Víddir kostnaðarhluta

[!include [banner](../includes/banner.md)]

Þegar kostnaður er greindur, notarðu víddir kostnaðareiningar til að ákvarða hvert kostnaður streymir. Víddir kostnaðarhlutar eru notaðar til að ákvarða hvert á að úthluta kostnaði. Þetta efni inniheldur upplýsingar um víddir kostnaðarhlutar.

Kostnaðarhlutur getur verið hvaða gerð hlutar sem á að áætla, úthluta kostnaði á, eða mæla beint. Dæmigerður kostnaðarhlutur inniheldur afurðir, verk, tilföng, deildir, kostnaðarstaði og landfræðileg svæði. Stjórnun notar kostnaðarhlutur til að magngreina kostnað, en einnig til að keyra arðsemisgreiningu.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Víddir kostnaðahluta og víddarstök kostnaðareiningar.
Kostnaðarhlutir eru þekkt sem *víddir kostnaðarhlutar*. Eftir að búið er að ákvarða hvaða til hvaða einingar vídd kostnaðareiningar vísar til, verður að tilgreina einstaka víddargildi eða flytja þær inn í kostnaðarbókhald úr öðrum upprunakerfum. Einstaka víddargildi kallast *víddarstök kostnaðarhlutar*. T.d. á að nota fjárhagsvídd sem nefnist kostnaðarstað sem vídd kostnaðarhlutar. Til að sjá hvernig kostnaður streymir til stakar kostnaðarstaðir, þarf að flytja inn víddarstök kostnaðarhlutar. Í þessu tilfelli eru víddarstök kostnaðarhlutar hin raunverulega kostnaðarstöðum, eins og sala, Framleiðslu, Stjórnun og Landfræðilegum staðsetningar. Eftirfarandi skjámyndir sýna dæmi um kostnaðarstaður sem vídd kostnaðarhlutar með hennar raunverulegu kostnaðarstaður sem víddarstök kostnaðahlutar. 

[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Flytja inn víddarstök kostnaðarhlutar með gagnatengjum.
Til þess að auðvelda innflutningi víddarstök kostnaðarhlutar, notarðu gagnatengi til að sækja gildi úr einingum sem á að nota sem víddir kostnaðarhlutar. Þú getur notað for-uppsett gagnatengi eða sérsniðin gagnatengi sem þú byggir sjálfur.



