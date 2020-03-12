---
title: ISEMPTY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ISEMPTY í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 6adca3c95c10e7d4b3287561925a9d9fe8a74121
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042045"
---
# <span data-ttu-id="d89c4-103"><a name="ISEMPTY">ISEMPTY ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="d89c4-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d89c4-104">Aðgerðin `ISEMPTY` skilar *Boole*-gildinu **TRUE** ef tilgreindur listi inniheldur engar skrár.</span><span class="sxs-lookup"><span data-stu-id="d89c4-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="d89c4-105">Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d89c4-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89c4-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="d89c4-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="d89c4-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="d89c4-107">Arguments</span></span>

<span data-ttu-id="d89c4-108">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="d89c4-108">`list`: *Record list*</span></span>

<span data-ttu-id="d89c4-109">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="d89c4-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d89c4-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d89c4-110">Return values</span></span>

<span data-ttu-id="d89c4-111">*Boole*</span><span class="sxs-lookup"><span data-stu-id="d89c4-111">*Boolean*</span></span>

<span data-ttu-id="d89c4-112">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="d89c4-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d89c4-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="d89c4-113">Example 1</span></span>

<span data-ttu-id="d89c4-114">Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` skilar segðin `ISEMPTY(DS)` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d89c4-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d89c4-115">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="d89c4-115">Example 2</span></span>

<span data-ttu-id="d89c4-116">Segðin `ISEMPTY (SPLIT ("",1))` skilar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="d89c4-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d89c4-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d89c4-117">Additional resources</span></span>

[<span data-ttu-id="d89c4-118">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="d89c4-118">List functions</span></span>](er-functions-category-list.md)
