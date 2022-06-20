---
title: ROUNDAMOUNT ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig ROUNDAMOUNT rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 623024f4ee6ac0d237ec45d50d9678195d6c6cd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905171"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ROUNDAMOUNT` skilar *raungildi* sem niðurstöðuna af námundun á tilgreindri tölu að næsta margfeldi af annarri tölu í samræmi við tilgreinda námundunarreglu.

## <a name="syntax"></a>Málskipun

```vb
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

Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** hagar þessi aðgerð sér eins og [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-aðgerðin og [MROUND](../dev-ref/xpp-math-run-time-functions.md#round) X ++ aðgerðin.

## <a name="remarks"></a>Athugasemdir

Til að slétta tölulegt gildi í tiltekinn fjölda aukastafa skal nota aðgerðina [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Dæmi

Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.Ordinary** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.RoundDown** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.RoundUp** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)

[Reikniaðgerðir](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]