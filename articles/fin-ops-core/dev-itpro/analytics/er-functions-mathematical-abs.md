---
title: ABS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ABS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565785"
---
# <a name="abs-er-function"></a><span data-ttu-id="ff340-103">ABS ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="ff340-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff340-104">Aðgerðin `ABS` skilar algeru gildi (leifastofn) tiltekins fjölda sem *Raun*-gildi.</span><span class="sxs-lookup"><span data-stu-id="ff340-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="ff340-105">Með öðrum orðum skilar hún tölunni án táknsins.</span><span class="sxs-lookup"><span data-stu-id="ff340-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff340-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="ff340-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="ff340-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="ff340-107">Arguments</span></span>

<span data-ttu-id="ff340-108">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="ff340-108">`number`: *Real*</span></span>

<span data-ttu-id="ff340-109">Tölugildi sem þú vilt fá stuðullinn á.</span><span class="sxs-lookup"><span data-stu-id="ff340-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff340-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="ff340-110">Return values</span></span>

<span data-ttu-id="ff340-111">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="ff340-111">*Real*</span></span>

<span data-ttu-id="ff340-112">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="ff340-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="ff340-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ff340-113">Example</span></span>

<span data-ttu-id="ff340-114">`ABS (-1)` skilar **1**.</span><span class="sxs-lookup"><span data-stu-id="ff340-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff340-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ff340-115">Additional resources</span></span>

[<span data-ttu-id="ff340-116">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="ff340-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]