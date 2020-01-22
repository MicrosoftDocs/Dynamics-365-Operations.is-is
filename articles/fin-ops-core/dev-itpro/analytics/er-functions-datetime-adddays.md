---
title: ADDDAYS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ADDAYS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916454"
---
# <span data-ttu-id="fb3d4-103"><a name="ADDDAYS">ADDDAYS ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="fb3d4-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb3d4-104">Aðgerðin `ADDDAYS` reiknar út *DateTime*-gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekinn upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3d4-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="fb3d4-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="fb3d4-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="fb3d4-106">Arguments</span></span>

<span data-ttu-id="fb3d4-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="fb3d4-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="fb3d4-108">Dagsetningar-/tímagildi sem táknar upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="fb3d4-109">`days`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="fb3d4-109">`days`: *Integer*</span></span>

<span data-ttu-id="fb3d4-110">Dagafjöldi fyrir eða eftir `datetime`.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb3d4-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="fb3d4-111">Return values</span></span>

<span data-ttu-id="fb3d4-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="fb3d4-112">*DateTime*</span></span>

<span data-ttu-id="fb3d4-113">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fb3d4-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="fb3d4-114">Usage notes</span></span>

<span data-ttu-id="fb3d4-115">Jákvætt gildi fyrir `days` skilar framtíðardegi.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="fb3d4-116">Neikvætt gildi skilar liðinni dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="fb3d4-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="fb3d4-117">Example 1</span></span>

<span data-ttu-id="fb3d4-118">`ADDDAYS (NOW(), 7)` skilar dagsetningu og tíma sjö daga fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="fb3d4-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="fb3d4-119">Example 2</span></span>

<span data-ttu-id="fb3d4-120">`ADDDAYS (NOW(), -3)` skilar dagsetningu og tíma þrjá daga aftur í tímann.</span><span class="sxs-lookup"><span data-stu-id="fb3d4-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb3d4-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fb3d4-121">Additional resources</span></span>

[<span data-ttu-id="fb3d4-122">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="fb3d4-122">Date and time functions</span></span>](er-functions-category-datetime.md)
