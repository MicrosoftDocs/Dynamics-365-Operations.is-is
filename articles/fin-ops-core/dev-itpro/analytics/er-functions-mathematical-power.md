---
title: POWER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin POWER í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750157"
---
# <a name="power-er-function"></a><span data-ttu-id="f9b63-103">POWER ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="f9b63-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9b63-104">Aðgerðin `POWER` skilar *Raun*-gildi sem táknar niðurstöðuna af því að hækka tilgreinda jákvæða tölu upp að tilgreindri valheimild.</span><span class="sxs-lookup"><span data-stu-id="f9b63-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b63-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="f9b63-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="f9b63-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="f9b63-106">Arguments</span></span>

<span data-ttu-id="f9b63-107">`number`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="f9b63-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="f9b63-108">Tölugildi sem þarf að hækka í tiltekinn kraft.</span><span class="sxs-lookup"><span data-stu-id="f9b63-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="f9b63-109">`power`: *Raun* eða *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="f9b63-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="f9b63-110">Tölugildi sem táknar tiltekinn kraft.</span><span class="sxs-lookup"><span data-stu-id="f9b63-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9b63-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="f9b63-111">Return values</span></span>

<span data-ttu-id="f9b63-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="f9b63-112">*Real*</span></span>

<span data-ttu-id="f9b63-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="f9b63-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f9b63-114">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f9b63-114">Example 1</span></span>

<span data-ttu-id="f9b63-115">`POWER (10, 2)` skilar **100**.</span><span class="sxs-lookup"><span data-stu-id="f9b63-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f9b63-116">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f9b63-116">Example 2</span></span>

<span data-ttu-id="f9b63-117">`POWER (4, 0.5)` skilar **2**.</span><span class="sxs-lookup"><span data-stu-id="f9b63-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9b63-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f9b63-118">Additional resources</span></span>

[<span data-ttu-id="f9b63-119">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="f9b63-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]