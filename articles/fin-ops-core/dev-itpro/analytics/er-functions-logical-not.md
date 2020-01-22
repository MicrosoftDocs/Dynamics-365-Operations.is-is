---
title: NOT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NOT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916040"
---
# <span data-ttu-id="85eac-103"><a name="NOT">NOT ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="85eac-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85eac-104">Aðgerðin `NOT` skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi.</span><span class="sxs-lookup"><span data-stu-id="85eac-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="85eac-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="85eac-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="85eac-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="85eac-106">Arguments</span></span>

<span data-ttu-id="85eac-107">`condition`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="85eac-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="85eac-108">Gild skilyrt segð sem verður að snúa við.</span><span class="sxs-lookup"><span data-stu-id="85eac-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="85eac-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="85eac-109">Return values</span></span>

<span data-ttu-id="85eac-110">*Boole*</span><span class="sxs-lookup"><span data-stu-id="85eac-110">*Boolean*</span></span>

<span data-ttu-id="85eac-111">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="85eac-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="85eac-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="85eac-112">Example</span></span>

<span data-ttu-id="85eac-113">`NOT (TRUE)` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="85eac-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85eac-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="85eac-114">Additional resources</span></span>

[<span data-ttu-id="85eac-115">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="85eac-115">Logical functions</span></span>](er-functions-category-logical.md)
