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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743376"
---
# <a name="adddays-er-function"></a><span data-ttu-id="2e022-103">ADDDAYS ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="2e022-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e022-104">Aðgerðin `ADDDAYS` reiknar út *DateTime*-gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekinn upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="2e022-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e022-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="2e022-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="2e022-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="2e022-106">Arguments</span></span>

<span data-ttu-id="2e022-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="2e022-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="2e022-108">Dagsetningar-/tímagildi sem táknar upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="2e022-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="2e022-109">`days`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="2e022-109">`days`: *Integer*</span></span>

<span data-ttu-id="2e022-110">Dagafjöldi fyrir eða eftir `datetime`.</span><span class="sxs-lookup"><span data-stu-id="2e022-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e022-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="2e022-111">Return values</span></span>

<span data-ttu-id="2e022-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="2e022-112">*DateTime*</span></span>

<span data-ttu-id="2e022-113">Dagsetningar-/tímagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="2e022-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2e022-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="2e022-114">Usage notes</span></span>

<span data-ttu-id="2e022-115">Jákvætt gildi fyrir `days` skilar framtíðardegi.</span><span class="sxs-lookup"><span data-stu-id="2e022-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="2e022-116">Neikvætt gildi skilar liðinni dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="2e022-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="2e022-117">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="2e022-117">Example 1</span></span>

<span data-ttu-id="2e022-118">`ADDDAYS (NOW(), 7)` skilar dagsetningu og tíma sjö daga fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="2e022-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="2e022-119">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="2e022-119">Example 2</span></span>

<span data-ttu-id="2e022-120">`ADDDAYS (NOW(), -3)` skilar dagsetningu og tíma þrjá daga aftur í tímann.</span><span class="sxs-lookup"><span data-stu-id="2e022-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e022-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2e022-121">Additional resources</span></span>

[<span data-ttu-id="2e022-122">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="2e022-122">Date and time functions</span></span>](er-functions-category-datetime.md)
