---
title: TEXT ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin TEXT Rafræn skýrslugerð (ER) er notuð.
author: kfend
ms.date: 12/10/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: a32da5588c5231b20bc8166d20888c1611ca273e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278857"
---
# <a name="text-er-function"></a>TEXT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `TEXT` skilar tilgreindri tölu sem *strengjagildi* eftir að því hefur verið breytt í textastreng sem er sniðið í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki forrits.

## <a name="syntax"></a>Málskipun

```vb
TEXT (number)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Heiltala* eða *Raun*

Tala sem þarf umreikna í textastreng.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Fyrir gildi í af gerðinni *rauntala* takmarkast umbreyting strengs við sem nemur tveimur tugasætum.

## <a name="example"></a>Dæmi

Ef netþjónninn á Microsoft Dynamics 365 Fjármálatilvik er skilgreint sem **EN-US**,`TEXT (NOW ())` skilar núverandi dagsetningu fjármálafundar, 17. desember 2015, sem textastreng **"12/17/2015 07:59:23 AM"**. `TEXT (1/3)` skilar **"0.33"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
