---
title: DAYOFYEAR ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DAYOFYEAR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba63c96355a6a7a1eccaddf39e47a3edb2d1e651
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563535"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="d9a1a-103">DAYOFYEAR ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="d9a1a-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9a1a-104">Aðgerðin `DAYOFYEAR` skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a1a-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="d9a1a-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="d9a1a-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="d9a1a-106">Arguments</span></span>

<span data-ttu-id="d9a1a-107">`date`: *Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="d9a1a-107">`date`: *Date*</span></span>

<span data-ttu-id="d9a1a-108">Dagsetningargildi sem táknar dagsetninguna sem á að nota við útreikning á fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="d9a1a-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d9a1a-109">Return values</span></span>

<span data-ttu-id="d9a1a-110">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="d9a1a-110">*Integer*</span></span>

<span data-ttu-id="d9a1a-111">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d9a1a-112">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="d9a1a-112">Example 1</span></span>

<span data-ttu-id="d9a1a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` skilar **61**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d9a1a-114">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="d9a1a-114">Example 2</span></span>

<span data-ttu-id="d9a1a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` skilar **1**.</span><span class="sxs-lookup"><span data-stu-id="d9a1a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9a1a-116">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d9a1a-116">Additional resources</span></span>

[<span data-ttu-id="d9a1a-117">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="d9a1a-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]