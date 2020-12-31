---
title: REVERSE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin REVERSE í rafrænni skýrslugerð (ER) er notuð.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 895d5f13f065b2188f245d081fa69e7e63555dde
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686441"
---
# <a name="reverse-er-function"></a>REVERSE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `REVERSE` skilar tilgreindum lista sem *Skráalista*-gildi í öfugri röð.

## <a name="syntax"></a>Málskipun

```vb
REVERSE (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="example-1"></a>Dæmi 1

Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` textagildinu **"C"**.

## <a name="example-2"></a>Dæmi 2

Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) sem vísar til töflunnar VendTable skilar segðin `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` lista yfir lánardrottna sem er raðað eftir nafni í lækkandi röð.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
