---
title: ROUNDAMOUNT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDAMOUNT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c68933352da1f9c7dc5dad76e8635981f8a89fce
ms.sourcegitcommit: 9291e6dc0de076a16684980e528c5aa98845bb34
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918980"
---
# <a name="ROUNDAMOUNT">ROUNDAMOUNT ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `ROUNDAMOUNT` skilar *raungildi* sem niðurstöðuna af námundun á tilgreindri tölu að næsta margfeldi af annarri tölu í samræmi við tilgreinda námundunarreglu.

## <a name="syntax"></a>Málskipun

```
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Int* eða *Raun*

Tölugildi sem verður að vera sléttað.

`decimals`: *Int* eða *Raun*

Talan sem gildi færibreytunnar `number` verður að vera námundað í margfeldi af.

`round rule`: *Upptaln.gildi*

Upptalningargildi upptalningarinnar **RoundOffType** sem skilgreinir námundunarreglu. Þessi upptalning býður upp á eftirfarandi gildi:

- Venjulegt (venjulegt)
- Niður (RoundDown)
- Uppjöfnun (RoundUp)

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölulegt gildi sem myndast er margfeldi af gildinu sem er tilgreint af færibreytunni `decimals` og er næst því gildi sem tilgreint er af færibreytunni `number`.

## <a name="usage-notes"></a>Notkunarbréf

Þegar færibreytan `number` er núll skilar þessi aðgerð alltaf núlli.

Þegar færibreytan `decimals` er núll námundar þessi aðgerð í sjálfgefna sléttunargildi. Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** er sjálfgefið sléttunargildi **0,01**. Að öðrum kosti er sjálfgefið sléttunargildi **1,0**.

Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** er þessi aðgerð sléttuð í næstu sléttunarupphæð.

Þegar færibreytan `round rule` er stillt á **RoundOffType.RoundDown** er þessi aðgerð sléttuð upp að núlli í næstu sléttunarupphæð.

Þegar færibreytan `round rule` er stillt á **RoundOffType.RoundUp** er þessi aðgerð sléttuð frá núlli í næstu sléttunarupphæð.

Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** hagar þessi aðgerð sér eins og [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-aðgerðin og [MROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X ++ aðgerðin.

## <a name="remarks"></a>Athugasemdir

Til að slétta tölulegt gildi í tiltekinn fjölda aukastafa skal nota aðgerðina [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Dæmi

Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.Ordinary** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.RoundDown** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.RoundUp** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)

[Reikniaðgerðir](er-functions-category-mathematical.md)
