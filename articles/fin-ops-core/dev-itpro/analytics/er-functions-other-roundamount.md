---
title: ROUNDAMOUNT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDAMOUNT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 2a80587236d17160a996d701ca4ae38be21c818c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563295"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="363a3-103">ROUNDAMOUNT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="363a3-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="363a3-104">Aðgerðin `ROUNDAMOUNT` skilar *raungildi* sem niðurstöðuna af námundun á tilgreindri tölu að næsta margfeldi af annarri tölu í samræmi við tilgreinda námundunarreglu.</span><span class="sxs-lookup"><span data-stu-id="363a3-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="363a3-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="363a3-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="363a3-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="363a3-106">Arguments</span></span>

<span data-ttu-id="363a3-107">`number`: *Int* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="363a3-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="363a3-108">Tölugildi sem verður að vera sléttað.</span><span class="sxs-lookup"><span data-stu-id="363a3-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="363a3-109">`decimals`: *Int* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="363a3-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="363a3-110">Talan sem gildi færibreytunnar `number` verður að vera námundað í margfeldi af.</span><span class="sxs-lookup"><span data-stu-id="363a3-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="363a3-111">`round rule`: *Upptaln.gildi*</span><span class="sxs-lookup"><span data-stu-id="363a3-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="363a3-112">Upptalningargildi upptalningarinnar **RoundOffType** sem skilgreinir námundunarreglu.</span><span class="sxs-lookup"><span data-stu-id="363a3-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="363a3-113">Þessi upptalning býður upp á eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="363a3-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="363a3-114">Venjulegt (venjulegt)</span><span class="sxs-lookup"><span data-stu-id="363a3-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="363a3-115">Niður (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="363a3-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="363a3-116">Uppjöfnun (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="363a3-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="363a3-117">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="363a3-117">Return values</span></span>

<span data-ttu-id="363a3-118">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="363a3-118">*Real*</span></span>

<span data-ttu-id="363a3-119">Tölulegt gildi sem myndast er margfeldi af gildinu sem er tilgreint af færibreytunni `decimals` og er næst því gildi sem tilgreint er af færibreytunni `number`.</span><span class="sxs-lookup"><span data-stu-id="363a3-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="363a3-120">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="363a3-120">Usage notes</span></span>

<span data-ttu-id="363a3-121">Þegar færibreytan `number` er núll skilar þessi aðgerð alltaf núlli.</span><span class="sxs-lookup"><span data-stu-id="363a3-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="363a3-122">Þegar færibreytan `decimals` er núll námundar þessi aðgerð í sjálfgefna sléttunargildi.</span><span class="sxs-lookup"><span data-stu-id="363a3-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="363a3-123">Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** er sjálfgefið sléttunargildi **0,01**.</span><span class="sxs-lookup"><span data-stu-id="363a3-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="363a3-124">Að öðrum kosti er sjálfgefið sléttunargildi **1,0**.</span><span class="sxs-lookup"><span data-stu-id="363a3-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="363a3-125">Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** er þessi aðgerð sléttuð í næstu sléttunarupphæð.</span><span class="sxs-lookup"><span data-stu-id="363a3-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="363a3-126">Þegar færibreytan `round rule` er stillt á **RoundOffType.RoundDown** er þessi aðgerð sléttuð upp að núlli í næstu sléttunarupphæð.</span><span class="sxs-lookup"><span data-stu-id="363a3-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="363a3-127">Þegar færibreytan `round rule` er stillt á **RoundOffType.RoundUp** er þessi aðgerð sléttuð frá núlli í næstu sléttunarupphæð.</span><span class="sxs-lookup"><span data-stu-id="363a3-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="363a3-128">Þegar færibreytan `round rule` er stillt á **RoundOffType.Ordinary** hagar þessi aðgerð sér eins og [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-aðgerðin og [MROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X ++ aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="363a3-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="363a3-129">Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="363a3-129">Remarks</span></span>

<span data-ttu-id="363a3-130">Til að slétta tölulegt gildi í tiltekinn fjölda aukastafa skal nota aðgerðina [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="363a3-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="363a3-131">Dæmi</span><span class="sxs-lookup"><span data-stu-id="363a3-131">Example</span></span>

<span data-ttu-id="363a3-132">Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.Ordinary** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="363a3-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="363a3-133">Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.RoundDown** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="363a3-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="363a3-134">Ef færibreytan **model.RoundOff** er stillt á **RoundOffType.RoundUp** skilar `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.</span><span class="sxs-lookup"><span data-stu-id="363a3-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="363a3-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="363a3-135">Additional resources</span></span>

[<span data-ttu-id="363a3-136">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="363a3-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="363a3-137">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="363a3-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]