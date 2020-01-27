---
title: RIGHT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin RIGHT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916730"
---
# <a name="RIGHT">RIGHT ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `RIGHT` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá lokum tiltekins strengs.

## <a name="syntax"></a>Málskipun

```
RIGHT (text, number)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Gildið *Strengur* sem táknar upprunalega textann.

`number`: *Heiltala*

Fjöldi stafa sem þarf að skila úr enda frumtextans.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`RIGHT ("Sample", 3)` skilar **"ple"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)
