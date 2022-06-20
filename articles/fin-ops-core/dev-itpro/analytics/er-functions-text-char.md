---
title: CHAR ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig CHAR rafræn skýrslugerð (ER) aðgerðin er notuð.
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
ms.openlocfilehash: 1fb1d25c2624894e7bb0fa34b7bc48905a9289a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881491"
---
# <a name="char-er-function"></a>CHAR ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CHAR` skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu.

## <a name="syntax"></a>Málskipun

```vb
CHAR (number)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Heiltala*

Tala sem samsvarar væntum stökum staf.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Strengurinn sem þessi aðgerð skilar veltur á kóðuninni sem er valin í yfireiningu **FILE** sniðsins. Fyrir lista yfir studdar kóðanir, sjá [Kóðunarflokkur](/dotnet/api/system.text.encoding).

## <a name="example"></a>Dæmi

`CHAR (255)` skilar **ÿ**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]