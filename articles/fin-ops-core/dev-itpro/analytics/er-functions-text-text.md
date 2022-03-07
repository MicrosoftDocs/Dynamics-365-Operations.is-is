---
title: TEXT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TEXT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 38550b8b5181b49bcb8504129932f185ea95e038e38d4581bc3e0fa076f4fb50
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762453"
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

Ef þjónsstaðsetning á tilviki Microsoft Dynamics 365 Finance er skilgreind sem **EN-US** skilar `TEXT (NOW ())` gildandi setudagsetningu Finance, desember 17, 2015, sem textastrenginn **12/17/2015 07:59:23 fyrir hádegi**. `TEXT (1/3)` skilar **"0.33"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]