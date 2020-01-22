---
title: ROUND ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUND í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917075"
---
# <span data-ttu-id="b76f7-103"><a name="ROUND">ROUND ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="b76f7-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b76f7-104">Aðgerðin `ROUND` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð að tilgreindum fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="b76f7-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b76f7-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="b76f7-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b76f7-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="b76f7-106">Arguments</span></span>

<span data-ttu-id="b76f7-107">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="b76f7-107">`number`: *Real*</span></span>

<span data-ttu-id="b76f7-108">Tölugildi sem verður að vera sléttað.</span><span class="sxs-lookup"><span data-stu-id="b76f7-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="b76f7-109">`decimals`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="b76f7-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b76f7-110">Tölugildi sem stendur fyrir fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="b76f7-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b76f7-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="b76f7-111">Return values</span></span>

<span data-ttu-id="b76f7-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="b76f7-112">*Real*</span></span>

<span data-ttu-id="b76f7-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="b76f7-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b76f7-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="b76f7-114">Usage notes</span></span>

<span data-ttu-id="b76f7-115">Ef gildi frumbreytunnar `decimals` er hærra en 0 (núll), er tilgreind tala námunduð að þetta mörgum aukastöfum.</span><span class="sxs-lookup"><span data-stu-id="b76f7-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="b76f7-116">Ef gildi frumbreytunnar `decimals` er **0** (núll), er tilgreind tala námunduð að næstu heiltölu.</span><span class="sxs-lookup"><span data-stu-id="b76f7-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="b76f7-117">Ef gildi frumbreytunnar `decimals` er lægra en 0 (núll), er tilgreind tala námunduð til vinstri við tugastafinn.</span><span class="sxs-lookup"><span data-stu-id="b76f7-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="b76f7-118">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="b76f7-118">Example 1</span></span>

<span data-ttu-id="b76f7-119">`ROUND (1200.767, 2)` sléttar um tvo aukastafi og skilar **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="b76f7-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b76f7-120">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="b76f7-120">Example 2</span></span>

<span data-ttu-id="b76f7-121">`ROUND (1200.767, -3)` sléttar að næsta margfeldi svæðisins 1.000 og skilar **1000**.</span><span class="sxs-lookup"><span data-stu-id="b76f7-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b76f7-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b76f7-122">Additional resources</span></span>

[<span data-ttu-id="b76f7-123">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="b76f7-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
