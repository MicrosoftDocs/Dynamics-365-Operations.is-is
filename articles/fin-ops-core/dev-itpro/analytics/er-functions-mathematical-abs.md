---
title: ABS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ABS í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041654"
---
# <span data-ttu-id="7903d-103"><a name="ABS">ABS ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="7903d-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7903d-104">Aðgerðin `ABS` skilar algeru gildi (leifastofn) tiltekins fjölda sem *Raun*-gildi.</span><span class="sxs-lookup"><span data-stu-id="7903d-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="7903d-105">Með öðrum orðum skilar hún tölunni án táknsins.</span><span class="sxs-lookup"><span data-stu-id="7903d-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="7903d-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="7903d-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="7903d-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="7903d-107">Arguments</span></span>

<span data-ttu-id="7903d-108">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="7903d-108">`number`: *Real*</span></span>

<span data-ttu-id="7903d-109">Tölugildi sem þú vilt fá stuðullinn á.</span><span class="sxs-lookup"><span data-stu-id="7903d-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="7903d-110">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="7903d-110">Return values</span></span>

<span data-ttu-id="7903d-111">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="7903d-111">*Real*</span></span>

<span data-ttu-id="7903d-112">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="7903d-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7903d-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="7903d-113">Example</span></span>

<span data-ttu-id="7903d-114">`ABS (-1)` skilar **1**.</span><span class="sxs-lookup"><span data-stu-id="7903d-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7903d-115">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7903d-115">Additional resources</span></span>

[<span data-ttu-id="7903d-116">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="7903d-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
