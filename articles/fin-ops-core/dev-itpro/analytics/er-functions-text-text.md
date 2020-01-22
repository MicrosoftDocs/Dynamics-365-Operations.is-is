---
title: TEXT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TEXT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915557"
---
# <a name="TEXT">TEXT ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `TEXT` skilar tilgreindri tölu sem *strengjagildi* eftir að því hefur verið breytt í textastreng sem er sniðið í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki forrits.

## <a name="syntax"></a>Málskipun

```
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
