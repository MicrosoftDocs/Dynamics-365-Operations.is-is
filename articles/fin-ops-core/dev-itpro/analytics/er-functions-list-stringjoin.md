---
title: STRINGJOIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin STRINGJOIN í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 651cc261e6a33b1a824feb94afa767e439196e249bb13b0fc4886dc72bfdd184
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776099"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `STRINGJOIN` skilar *strengjagildi* sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindum lista. Hægt er að aðskilja gildin með tilgreindri afmörkun.

## <a name="syntax"></a>Málskipun

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`field`: *Reitur*

Gild slóð á reiti af gagnagerðinni *Strengur* í tilgreindum lista.

`delimiter`: *Strengur*

Afmarkari sem er notaður til að aðgreina undirstrengi.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

Ef þú slærð inn `SPLIT("abc" , 1)` sem gagnagjafa **DS** skilar segðin `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]