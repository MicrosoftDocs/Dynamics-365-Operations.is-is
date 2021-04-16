---
title: OR ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin OR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 9763cdbabfbaba1af433c1fd753b03982ecb550d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751720"
---
# <a name="or-er-function"></a><span data-ttu-id="25d20-103">OR ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="25d20-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25d20-104">Aðgerðin `OR` skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn.</span><span class="sxs-lookup"><span data-stu-id="25d20-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="25d20-105">Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="25d20-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d20-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="25d20-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="25d20-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="25d20-107">Arguments</span></span>

<span data-ttu-id="25d20-108">`condition 1`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="25d20-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="25d20-109">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="25d20-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="25d20-110">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="25d20-110">This argument is required.</span></span>

<span data-ttu-id="25d20-111">`condition N`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="25d20-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="25d20-112">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="25d20-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="25d20-113">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="25d20-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="25d20-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="25d20-114">Return values</span></span>

<span data-ttu-id="25d20-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="25d20-115">*Boolean*</span></span>

<span data-ttu-id="25d20-116">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="25d20-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="25d20-117">Dæmi</span><span class="sxs-lookup"><span data-stu-id="25d20-117">Example</span></span>

<span data-ttu-id="25d20-118">`OR (1=2, "a"="a")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="25d20-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25d20-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="25d20-119">Additional resources</span></span>

[<span data-ttu-id="25d20-120">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="25d20-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]