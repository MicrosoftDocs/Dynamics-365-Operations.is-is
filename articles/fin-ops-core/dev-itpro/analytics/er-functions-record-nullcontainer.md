---
title: NULLCONTAINER ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig NULLCONTAINER rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 8efa4cce3bda1707eff052e882b74e3da9542353
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291765"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NULLCONTAINER` skilar núll gildi fyrir *Ílát (skrá)* sem hefur sama skipulag og tilgreindur skráalisti eða skrá.

## <a name="syntax"></a>Málskipun

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti* eða *Ílát (skrá)*

Gild slóð hlutar í gagnagjafa af annaðhvort gerðinni *Skráalisti* eða *Gámur (skrá)*.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

> [!NOTE] 
> Þessi aðgerð er úrelt. Notaði aðgerðina `EMPTYRECORD` í staðinn. Frekari upplýsingar er að finna á [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Dæmi

`NULLCONTAINER (SPLIT ("abc", 1))` skilar nýrri tómri skrá sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni. Frekari upplýsingar er að finna á [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Færsluvirkni](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
