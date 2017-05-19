---
title: "Víddir kostnaðarhluta"
description: "Þegar greina kostnað, nota víddir kostnaðareiningar til að ákvarða hvert kostnaður streyma í. Víddir kostnaðarhlutar eru notaðar til að ákvarða hvert á að úthluta kostnaði. Þetta efni inniheldur upplýsingar um víddir kostnaðarhlutar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d38f0aa1c3272d5361e6fcca57d693cfa0042f3c
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="cost-object-dimensions"></a>Víddir kostnaðarhluta

[!include[banner](../includes/banner.md)]


Þegar greina kostnað, nota víddir kostnaðareiningar til að ákvarða hvert kostnaður streyma í. Víddir kostnaðarhlutar eru notaðar til að ákvarða hvert á að úthluta kostnaði. Þetta efni inniheldur upplýsingar um víddir kostnaðarhlutar.

Kostnaðarhlutur getur verið hvaða gerð hlutar sem á að áætla, úthluta kostnaði á, eða mæla beint. Dæmigerður kostnaðarhlutur inniheldur afurðir, verk, tilföng, deildir, kostnaðarstaði og landfræðileg svæði. Stjórnun notar kostnaðarhlutur til að magngreina kostnað, en einnig til að keyra arðsemisgreiningu.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Víddir kostnaðahluta og víddarstök kostnaðareiningar.
Kostnaðarhlutir eru þekkt sem *víddir kostnaðarhlutar*. Eftir að búið er að ákvarða hvaða til hvaða einingar vídd kostnaðareiningar vísar til, verður að tilgreina einstaka víddargildi eða flytja þær inn í kostnaðarbókhald úr öðrum upprunakerfum. Einstaka víddargildi kallast *víddarstök kostnaðarhlutar*. T.d. á að nota fjárhagsvídd sem nefnist kostnaðarstað sem vídd kostnaðarhlutar. Til að sjá hvernig kostnaður streymir til stakar kostnaðarstaðir, þarf að flytja inn víddarstök kostnaðarhlutar. Í þessu tilfelli eru víddarstök kostnaðarhlutar hin raunverulega kostnaðarstöðum, eins og sala, Framleiðslu, Stjórnun og Landfræðilegum staðsetningar. Eftirfarandi skjámyndir sýna dæmi um kostnaðarstaður sem vídd kostnaðarhlutar með hennar raunverulegu kostnaðarstaður sem víddarstök kostnaðahlutar. 

[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Flytja inn víddarstök kostnaðarhlutar með gagnatengjum.
Til þess að auðvelda innflutningi víddarstök kostnaðarhlutar, notarðu gagnatengi til að sækja gildi úr einingum sem á að nota sem víddir kostnaðarhlutar. Þú getur notað for-uppsett gagnatengi eða sérsniðin gagnatengi sem þú byggir sjálfur.




