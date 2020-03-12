---
title: NOW ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NOW í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042344"
---
# <span data-ttu-id="10a87-103"><a name="NOW">NOW ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="10a87-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10a87-104">Aðgerðin `NOW` skilar *DateTime*-gildi sem táknar dagsetningu og tíma núverandi netþjóns hugbúnaðar.</span><span class="sxs-lookup"><span data-stu-id="10a87-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a87-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="10a87-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="10a87-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="10a87-106">Return values</span></span>

<span data-ttu-id="10a87-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="10a87-107">*DateTime*</span></span>

<span data-ttu-id="10a87-108">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="10a87-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="10a87-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="10a87-109">Example</span></span>

<span data-ttu-id="10a87-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` skilar núverandi dagsetningar-/tímagildi hugbúnaðarþjóns, 24. desember, 2015, sem **"24-12-2015"**, miðað við tilgreint sérsniðið snið.</span><span class="sxs-lookup"><span data-stu-id="10a87-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10a87-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="10a87-111">Additional resources</span></span>

[<span data-ttu-id="10a87-112">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="10a87-112">Date and time functions</span></span>](er-functions-category-datetime.md)
