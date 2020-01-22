---
title: CHAR ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CHAR í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915741"
---
# <a name="CHAR">CHAR ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `CHAR` skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu.

## <a name="syntax"></a>Málskipun

```
CHAR (number)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Heiltala*

Tala sem samsvarar væntum stökum staf.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Strengurinn sem þessi aðgerð skilar veltur á kóðuninni sem er valin í yfireiningu **FILE** sniðsins. Fyrir lista yfir studdar kóðanir, sjá [Kóðunarflokkur](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Dæmi

`CHAR (255)` skilar **ÿ**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)
