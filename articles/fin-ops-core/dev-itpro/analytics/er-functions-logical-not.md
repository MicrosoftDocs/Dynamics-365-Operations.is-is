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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744648"
---
# <a name="not-er-function"></a><span data-ttu-id="9b798-103">NOT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="9b798-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b798-104">Aðgerðin `NOT` skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi.</span><span class="sxs-lookup"><span data-stu-id="9b798-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b798-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9b798-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="9b798-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9b798-106">Arguments</span></span>

<span data-ttu-id="9b798-107">`condition`: *Boole-gildi*</span><span class="sxs-lookup"><span data-stu-id="9b798-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="9b798-108">Gild skilyrt segð sem verður að snúa við.</span><span class="sxs-lookup"><span data-stu-id="9b798-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b798-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9b798-109">Return values</span></span>

<span data-ttu-id="9b798-110">*Boole*</span><span class="sxs-lookup"><span data-stu-id="9b798-110">*Boolean*</span></span>

<span data-ttu-id="9b798-111">*Boole*-gildið sem myndast.</span><span class="sxs-lookup"><span data-stu-id="9b798-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="9b798-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9b798-112">Example</span></span>

<span data-ttu-id="9b798-113">`NOT (TRUE)` skilar **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9b798-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b798-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9b798-114">Additional resources</span></span>

[<span data-ttu-id="9b798-115">Rökvirkni</span><span class="sxs-lookup"><span data-stu-id="9b798-115">Logical functions</span></span>](er-functions-category-logical.md)
