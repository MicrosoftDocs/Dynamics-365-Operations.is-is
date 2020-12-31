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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686979"
---
# <a name="or-er-function"></a><span data-ttu-id="b4639-103">OR ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="b4639-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4639-104">Aðgerðin `OR` skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn.</span><span class="sxs-lookup"><span data-stu-id="b4639-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="b4639-105">Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.</span><span class="sxs-lookup"><span data-stu-id="b4639-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4639-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="b4639-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="b4639-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="b4639-107">Arguments</span></span>

<span data-ttu-id="b4639-108">`condition 1`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="b4639-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="b4639-109">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="b4639-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="b4639-110">Þessi frumbreyta er áskilin.</span><span class="sxs-lookup"><span data-stu-id="b4639-110">This argument is required.</span></span>

<span data-ttu-id="b4639-111">`condition N`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="b4639-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="b4639-112">Gild skilyrt segð sem verður að prófa.</span><span class="sxs-lookup"><span data-stu-id="b4639-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="b4639-113">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="b4639-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b4639-114">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="b4639-114">Return values</span></span>

<span data-ttu-id="b4639-115">*Boole*</span><span class="sxs-lookup"><span data-stu-id="b4639-115">*Boolean*</span></span>

<span data-ttu-id="b4639-116">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="b4639-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="b4639-117">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b4639-117">Example</span></span>

<span data-ttu-id="b4639-118">`OR (1=2, "a"="a")` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b4639-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4639-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b4639-119">Additional resources</span></span>

[<span data-ttu-id="b4639-120">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="b4639-120">Logical functions</span></span>](er-functions-category-logical.md)
