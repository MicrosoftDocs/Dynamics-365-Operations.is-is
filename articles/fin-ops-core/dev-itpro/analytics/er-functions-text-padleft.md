---
title: PADLEFT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin PADLEFT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746244"
---
# <a name="padleft-er-function"></a>PADLEFT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `PADLEFT` skilar *strengjagildi* af tilgreindri lengd, þar sem upphaf tilgreinds strengs er fyllt með tilgreindum stöfum.

## <a name="syntax"></a>Málskipun

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gildið *Strengur* sem táknar upprunalega textann.

`length`: *Heiltala*

*Heiltölu*-gildi sem táknar lokafjölda stafa í fyllta strengnum.

`padding chars`: *Strengur*

Staftáknin sem á að nota við fyllingu.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`PADLEFT ("1234", 10, "`&nbsp;`")` skilar textastrengnum **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]