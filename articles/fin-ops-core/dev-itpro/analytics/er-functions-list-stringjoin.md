---
title: STRINGJOIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin STRINGJOIN í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917190"
---
# <a name="STRINGJOIN">STRINGJOIN ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `STRINGJOIN` skilar *strengjagildi* sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindum lista. Hægt er að aðskilja gildin með tilgreindri afmörkun.

## <a name="syntax"></a>Málskipun

```
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
