---
title: NOT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NOT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751715"
---
# <a name="not-er-function"></a><span data-ttu-id="40dd4-103">NOT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="40dd4-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40dd4-104">Aðgerðin `NOT` skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi.</span><span class="sxs-lookup"><span data-stu-id="40dd4-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="40dd4-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="40dd4-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="40dd4-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="40dd4-106">Arguments</span></span>

<span data-ttu-id="40dd4-107">`condition`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="40dd4-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="40dd4-108">Gild skilyrt segð sem verður að snúa við.</span><span class="sxs-lookup"><span data-stu-id="40dd4-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="40dd4-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="40dd4-109">Return values</span></span>

<span data-ttu-id="40dd4-110">*Boole*</span><span class="sxs-lookup"><span data-stu-id="40dd4-110">*Boolean*</span></span>

<span data-ttu-id="40dd4-111">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="40dd4-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="40dd4-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="40dd4-112">Example</span></span>

<span data-ttu-id="40dd4-113">`NOT (TRUE)` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="40dd4-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40dd4-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="40dd4-114">Additional resources</span></span>

[<span data-ttu-id="40dd4-115">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="40dd4-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]