---
title: POWER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin POWER í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744576"
---
# <a name="power-er-function"></a><span data-ttu-id="48f4e-103">POWER ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="48f4e-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48f4e-104">Aðgerðin `POWER` skilar *Raun*-gildi sem táknar niðurstöðuna af því að hækka tilgreinda jákvæða tölu upp að tilgreindri valheimild.</span><span class="sxs-lookup"><span data-stu-id="48f4e-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f4e-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="48f4e-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="48f4e-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="48f4e-106">Arguments</span></span>

<span data-ttu-id="48f4e-107">`number`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="48f4e-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="48f4e-108">Tölugildi sem þarf að hækka í tiltekinn kraft.</span><span class="sxs-lookup"><span data-stu-id="48f4e-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="48f4e-109">`power`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="48f4e-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="48f4e-110">Tölugildi sem táknar tiltekinn kraft.</span><span class="sxs-lookup"><span data-stu-id="48f4e-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="48f4e-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="48f4e-111">Return values</span></span>

<span data-ttu-id="48f4e-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="48f4e-112">*Real*</span></span>

<span data-ttu-id="48f4e-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="48f4e-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="48f4e-114">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="48f4e-114">Example 1</span></span>

<span data-ttu-id="48f4e-115">`POWER (10, 2)` skilar **100**.</span><span class="sxs-lookup"><span data-stu-id="48f4e-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="48f4e-116">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="48f4e-116">Example 2</span></span>

<span data-ttu-id="48f4e-117">`POWER (4, 0.5)` skilar **2**.</span><span class="sxs-lookup"><span data-stu-id="48f4e-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48f4e-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="48f4e-118">Additional resources</span></span>

[<span data-ttu-id="48f4e-119">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="48f4e-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
