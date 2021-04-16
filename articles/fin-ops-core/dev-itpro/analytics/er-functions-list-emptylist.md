---
title: EMPTYLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin EMPTYLIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746676"
---
# <a name="emptylist-er-function"></a>EMPTYLIST ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `EMPTYLIST` skilar tómu *Skráarlista*-gildi með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.

## <a name="syntax"></a>Málskipun

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="example"></a>Dæmi

`EMPTYLIST (SPLIT ("abc", 1))` skilar nýjum tómum lista sem hefur sömu uppbyggingu og listinn sem skilað er með `SPLIT`-aðgerðinni sem er notuð.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]