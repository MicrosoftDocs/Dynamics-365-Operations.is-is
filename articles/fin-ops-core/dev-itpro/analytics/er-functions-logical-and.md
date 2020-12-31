---
title: AND ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin AND í rafrænni skýrslugerð (ER) er notuð.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687075"
---
# <a name="and-er-function"></a><span data-ttu-id="49227-103">AND ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="49227-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49227-104">Aðgerðin `AND` skilar *Boolean*-gildi **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="49227-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="49227-105">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="49227-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="49227-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="49227-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="49227-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="49227-107">Arguments</span></span>

<span data-ttu-id="49227-108">`condition 1`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="49227-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="49227-109">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="49227-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="49227-110">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="49227-110">This argument is required.</span></span>

<span data-ttu-id="49227-111">`condition N`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="49227-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="49227-112">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="49227-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="49227-113">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="49227-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="49227-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="49227-114">Return values</span></span>

<span data-ttu-id="49227-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="49227-115">*Boolean*</span></span>

<span data-ttu-id="49227-116">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="49227-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="49227-117">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="49227-117">Usage notes</span></span>

<span data-ttu-id="49227-118">Í röksemdum rökréttra aðgerða er hægt að nota tilvísanir í gagnagjafa, tölu- og textagildi, Boole-gildi, samanburðarrekstraraðila og aðrar rafrænar skýrslur (ER) aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="49227-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="49227-119">Hins vegar verður að meta allar frumbreyturnar við *Boole*-gildið **TRUE** eða **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="49227-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="49227-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="49227-120">Example</span></span>

<span data-ttu-id="49227-121">`AND (1=1, "a"="a")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="49227-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="49227-122">`AND (1=2, "a"="a")` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="49227-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49227-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="49227-123">Additional resources</span></span>

[<span data-ttu-id="49227-124">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="49227-124">Logical functions</span></span>](er-functions-category-logical.md)
