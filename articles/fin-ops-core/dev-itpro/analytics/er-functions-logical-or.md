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
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041677"
---
# <span data-ttu-id="02cb6-103"><a name="OR">OR ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="02cb6-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02cb6-104">Aðgerðin `OR` skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn.</span><span class="sxs-lookup"><span data-stu-id="02cb6-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="02cb6-105">Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="02cb6-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cb6-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="02cb6-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="02cb6-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="02cb6-107">Arguments</span></span>

<span data-ttu-id="02cb6-108">`condition 1`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="02cb6-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="02cb6-109">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="02cb6-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="02cb6-110">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="02cb6-110">This argument is required.</span></span>

<span data-ttu-id="02cb6-111">`condition N`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="02cb6-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="02cb6-112">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="02cb6-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="02cb6-113">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="02cb6-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="02cb6-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="02cb6-114">Return values</span></span>

<span data-ttu-id="02cb6-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="02cb6-115">*Boolean*</span></span>

<span data-ttu-id="02cb6-116">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="02cb6-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="02cb6-117">Dæmi</span><span class="sxs-lookup"><span data-stu-id="02cb6-117">Example</span></span>

<span data-ttu-id="02cb6-118">`OR (1=2, "a"="a")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="02cb6-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02cb6-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="02cb6-119">Additional resources</span></span>

[<span data-ttu-id="02cb6-120">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="02cb6-120">Logical functions</span></span>](er-functions-category-logical.md)
