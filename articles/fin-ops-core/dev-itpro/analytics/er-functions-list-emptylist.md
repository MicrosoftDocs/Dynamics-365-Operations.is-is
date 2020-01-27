---
title: EMPTYLIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin EMPTYLIST í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917397"
---
# <a name="EMPTYLIST">EMPTYLIST ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `EMPTYLIST` skilar tómu *Skráarlista*-gildi með því að nota tilgreindan lista sem uppruna fyrir skipulag lista.

## <a name="syntax"></a>Málskipun

```
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
