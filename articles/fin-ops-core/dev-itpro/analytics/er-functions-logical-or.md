---
title: OR ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin OR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917121"
---
# <span data-ttu-id="4e498-103"><a name="OR">OR ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="4e498-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e498-104">Aðgerðin `OR` skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn.</span><span class="sxs-lookup"><span data-stu-id="4e498-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="4e498-105">Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="4e498-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e498-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4e498-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="4e498-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4e498-107">Arguments</span></span>

<span data-ttu-id="4e498-108">`condition 1`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="4e498-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="4e498-109">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="4e498-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4e498-110">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="4e498-110">This argument is required.</span></span>

<span data-ttu-id="4e498-111">`condition N`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="4e498-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="4e498-112">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="4e498-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4e498-113">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="4e498-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e498-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4e498-114">Return values</span></span>

<span data-ttu-id="4e498-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="4e498-115">*Boolean*</span></span>

<span data-ttu-id="4e498-116">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="4e498-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="4e498-117">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4e498-117">Example</span></span>

<span data-ttu-id="4e498-118">`OR (1=2, "a"="a")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="4e498-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e498-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4e498-119">Additional resources</span></span>

[<span data-ttu-id="4e498-120">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="4e498-120">Logical functions</span></span>](er-functions-category-logical.md)
