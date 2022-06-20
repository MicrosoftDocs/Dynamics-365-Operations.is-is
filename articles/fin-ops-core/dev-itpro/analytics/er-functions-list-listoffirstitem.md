---
title: LISTOFFIRSTITEM ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin LISTOFFIRSTITEM Rafræn skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f4715becfb158826a2b5678aac6a58c987433192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881160"
---
# <a name="listoffirstitem-er-function"></a>LISTOFFIRSTITEM ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `LISTOFFIRSTITEM` skilar *Skráalista*-gildi sem samanstendur af aðeins fyrstu skránni á tilgreindum lista.

## <a name="syntax"></a>Málskipun

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="example"></a>Dæmi

Segðin `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` skilar textagildinu **"A"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]