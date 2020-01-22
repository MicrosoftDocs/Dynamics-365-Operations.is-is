---
title: DAYOFYEAR ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DAYOFYEAR í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916339"
---
# <span data-ttu-id="9bf16-103"><a name="DAYOFYEAR">DAYOFYEAR ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="9bf16-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bf16-104">Aðgerðin `DAYOFYEAR` skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="9bf16-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf16-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9bf16-105">Syntax</span></span>

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="9bf16-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9bf16-106">Arguments</span></span>

<span data-ttu-id="9bf16-107">`date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="9bf16-107">`date`: *Date*</span></span>

<span data-ttu-id="9bf16-108">Dagsetningargildi sem táknar dagsetninguna sem á að nota við útreikning á fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="9bf16-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="9bf16-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9bf16-109">Return values</span></span>

<span data-ttu-id="9bf16-110">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="9bf16-110">*Integer*</span></span>

<span data-ttu-id="9bf16-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="9bf16-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9bf16-112">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="9bf16-112">Example 1</span></span>

<span data-ttu-id="9bf16-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` skilar **61**.</span><span class="sxs-lookup"><span data-stu-id="9bf16-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9bf16-114">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="9bf16-114">Example 2</span></span>

<span data-ttu-id="9bf16-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` skilar **1**.</span><span class="sxs-lookup"><span data-stu-id="9bf16-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bf16-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9bf16-116">Additional resources</span></span>

[<span data-ttu-id="9bf16-117">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="9bf16-117">Date and time functions</span></span>](er-functions-category-datetime.md)
