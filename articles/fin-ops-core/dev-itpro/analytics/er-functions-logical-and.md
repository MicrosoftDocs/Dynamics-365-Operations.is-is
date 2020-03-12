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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041815"
---
# <span data-ttu-id="4278b-103"><a name="AND">AND ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="4278b-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4278b-104">Aðgerðin `AND` skilar *Boolean*-gildi **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="4278b-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="4278b-105">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4278b-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4278b-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="4278b-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="4278b-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="4278b-107">Arguments</span></span>

<span data-ttu-id="4278b-108">`condition 1`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="4278b-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="4278b-109">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="4278b-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4278b-110">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="4278b-110">This argument is required.</span></span>

<span data-ttu-id="4278b-111">`condition N`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="4278b-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="4278b-112">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="4278b-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4278b-113">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="4278b-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4278b-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="4278b-114">Return values</span></span>

<span data-ttu-id="4278b-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="4278b-115">*Boolean*</span></span>

<span data-ttu-id="4278b-116">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="4278b-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4278b-117">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="4278b-117">Usage notes</span></span>

<span data-ttu-id="4278b-118">Í röksemdum rökréttra aðgerða er hægt að nota tilvísanir í gagnagjafa, tölu- og textagildi, Boole-gildi, samanburðarrekstraraðila og aðrar rafrænar skýrslur (ER) aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="4278b-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="4278b-119">Hins vegar verður að meta allar frumbreyturnar við *Boole*-gildið **TRUE** eða **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4278b-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="4278b-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4278b-120">Example</span></span>

<span data-ttu-id="4278b-121">`AND (1=1, "a"="a")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="4278b-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="4278b-122">`AND (1=2, "a"="a")` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4278b-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4278b-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4278b-123">Additional resources</span></span>

[<span data-ttu-id="4278b-124">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="4278b-124">Logical functions</span></span>](er-functions-category-logical.md)
