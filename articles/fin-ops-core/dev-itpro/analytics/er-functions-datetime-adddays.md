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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688444"
---
# <a name="adddays-er-function"></a><span data-ttu-id="36f21-103">ADDDAYS ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="36f21-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36f21-104">Aðgerðin `ADDDAYS` reiknar út *DateTime*-gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekinn upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="36f21-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f21-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="36f21-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="36f21-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="36f21-106">Arguments</span></span>

<span data-ttu-id="36f21-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="36f21-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="36f21-108">Dagsetningar-/tímagildi sem táknar upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="36f21-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="36f21-109">`days`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="36f21-109">`days`: *Integer*</span></span>

<span data-ttu-id="36f21-110">Dagafjöldi fyrir eða eftir `datetime`.</span><span class="sxs-lookup"><span data-stu-id="36f21-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="36f21-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="36f21-111">Return values</span></span>

<span data-ttu-id="36f21-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="36f21-112">*DateTime*</span></span>

<span data-ttu-id="36f21-113">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="36f21-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="36f21-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="36f21-114">Usage notes</span></span>

<span data-ttu-id="36f21-115">Jákvætt gildi fyrir `days` skilar framtíðardegi.</span><span class="sxs-lookup"><span data-stu-id="36f21-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="36f21-116">Neikvætt gildi skilar liðinni dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="36f21-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="36f21-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="36f21-117">Example 1</span></span>

<span data-ttu-id="36f21-118">`ADDDAYS (NOW(), 7)` skilar dagsetningu og tíma sjö daga fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="36f21-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="36f21-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="36f21-119">Example 2</span></span>

<span data-ttu-id="36f21-120">`ADDDAYS (NOW(), -3)` skilar dagsetningu og tíma þrjá daga aftur í tímann.</span><span class="sxs-lookup"><span data-stu-id="36f21-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36f21-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="36f21-121">Additional resources</span></span>

[<span data-ttu-id="36f21-122">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="36f21-122">Date and time functions</span></span>](er-functions-category-datetime.md)
