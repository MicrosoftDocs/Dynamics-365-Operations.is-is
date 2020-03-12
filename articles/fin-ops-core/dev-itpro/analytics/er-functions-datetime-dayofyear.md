---
title: DAYOFYEAR ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DAYOFYEAR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070668"
---
# <span data-ttu-id="57eca-103"><a name="DAYOFYEAR">DAYOFYEAR ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="57eca-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57eca-104">Aðgerðin `DAYOFYEAR` skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="57eca-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="57eca-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="57eca-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="57eca-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="57eca-106">Arguments</span></span>

<span data-ttu-id="57eca-107">`date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="57eca-107">`date`: *Date*</span></span>

<span data-ttu-id="57eca-108">Dagsetningargildi sem táknar dagsetninguna sem á að nota við útreikning á fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="57eca-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="57eca-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="57eca-109">Return values</span></span>

<span data-ttu-id="57eca-110">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="57eca-110">*Integer*</span></span>

<span data-ttu-id="57eca-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="57eca-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="57eca-112">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="57eca-112">Example 1</span></span>

<span data-ttu-id="57eca-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` skilar **61**.</span><span class="sxs-lookup"><span data-stu-id="57eca-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="57eca-114">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="57eca-114">Example 2</span></span>

<span data-ttu-id="57eca-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` skilar **1**.</span><span class="sxs-lookup"><span data-stu-id="57eca-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57eca-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="57eca-116">Additional resources</span></span>

[<span data-ttu-id="57eca-117">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="57eca-117">Date and time functions</span></span>](er-functions-category-datetime.md)
