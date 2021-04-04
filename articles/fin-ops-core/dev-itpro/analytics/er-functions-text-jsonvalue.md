---
title: JSONVALUE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin JSONVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570017"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `JSONVALUE` þáttar gögn í JavaScript Object Notation (JSON) sniði sem er aðgengilegt á tilgreindri slóð og dregur út tölugildi sem hefur tilgreint auðkenni. Hún skilar síðan útdregnu tölugildinu sem *Strengja*-gildi.

## <a name="syntax"></a>Málskipun

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Frumbreytur

`input`: *Strengur*

Gild slóð í gagnagjafa af gerðinni *Strengur* sem inniheldur JSON-gögn.

`path`: *Strengur*

Kennimerki tölugildis í JSON-gögnum.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

Gagnagjafinn **JsonField** inniheldur eftirfarandi gögn á JSON-sniði: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Í þessu tilfelli skilar segðin `JSONVALUE (JsonField, "BuildNumber")` eftirfarandi gildi af gagnagerðinni *Strengur*: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]