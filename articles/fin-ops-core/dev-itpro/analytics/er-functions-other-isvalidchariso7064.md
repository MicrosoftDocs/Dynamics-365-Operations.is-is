---
title: ISVALIDCHARACTERISO7064 ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISVALIDCHARACTERISO7064 í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 1f102a6a3eafe3b066101370b94fa2f17ad3ad8b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748294"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ISVALIDCHARACTERISO7064` skilar *Boolean*-gildinu **TRUE** ef tilgreindur strengur táknar gildan alþjóðlegan bankareikning (IBAN). Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.

## <a name="syntax"></a>Málskipun

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Textagildi sem táknar IBAN.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` skilar **TRUE**. 

`ISVALIDCHARACTERISO7064 ("AT61")` skilar **FALSE**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]