---
title: INDEX ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INDEX í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 05/20/2021
ms.topic: article
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087752"
---
# <a name="index-er-function"></a>INDEX ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `INDEX` skilar gildinu *Ílát (skrá)* sem er valið með því að nota tilgreindan töluvísi í tilgreindum lista. Ef vísirinn er utan marka fyrir skrárnar í tilgreindum lista er undantekningu beitt.

## <a name="syntax"></a>Málskipun

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`index`: *Heiltala*

Töluvísitala sem gefur til kynna staðsetningu viðkomandi skráar á tilgreindum lista.

> [!NOTE]
> Þar sem einhliða númerun er notuð fyrir þessa aðgerð skal tilgreina gildið **1** til að skila fyrstu færslu tilgreinds lista.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="example-1"></a>Dæmi 1

Ef þú slærð inn gagnagjafann **DS** í reitinn *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` skilar segðin `DS.Value` textagildinu **"B"** fyrir seinni skrána í skráalistanum. Segðin `INDEX (SPLIT ("A|B|C", "|"), 2).Value` skilar líka textagildinu **"B"**.

## <a name="example-2"></a>Dæmi 2

Ef þú slærð inn gagnagjafa **DS** af gerðinni *Reiknaður reiður* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` beitir segðin `INDEX (SPLIT ("A|B|C", "|"), 4).Value` undantekningu á keyrslutíma.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
