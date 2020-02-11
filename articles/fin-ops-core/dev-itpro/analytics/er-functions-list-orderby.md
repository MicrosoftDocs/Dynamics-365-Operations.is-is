---
title: ORDERBY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ORDERBY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916201"
---
# <a name="ORDERBY">ORDERBY ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `ORDERBY` skilar tilgreindum lista sem *Skráalista*-gildi eftir að því hefur verið raðað í samræmi við tilgreindar frumbreytur. Þessi frumbreytur geta verið skilgreindar sem segðir.

## <a name="syntax"></a>Málskipun

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`expression 1`: *Reitur*

Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð. Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð. Þessi frumbreyta er áskilin.

`expression N`: *Reitur*

Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð. Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="example-1"></a>Dæmi 1

Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( ORDERBY( DS, DS. Value)).Value` textagildinu **"A"**.

## <a name="example-2"></a>Dæmi 2

Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) sem vísar til töflunnar VendTable skilar segðin `ORDERBY (Vendors, Vendors.'name()')` lista yfir lánardrottna sem er raðað eftir heiti í hækkandi röð.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)