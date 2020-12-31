---
title: COUNT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COUNT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687721"
---
# <a name="count-er-function"></a>COUNT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `COUNT` skilar *Heiltölu*-gildi sem táknar fjölda skráa á tilgreindum lista, ef listinn er ekki tómur. Ef listinn er tómur skilar þessi aðgerð **0** (núlli).

## <a name="syntax"></a>Málskipun

```vb
COUNT (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Heiltala*

Tölugildið sem verður til.

## <a name="example"></a>Dæmi

`COUNT (SPLIT("abcd" , 3))` skilar **2**, vegna þess að aðgerðin `SPLIT` sem er notuð í þessu dæmi býr til lista sem samanstendur af tveimur skrám.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
