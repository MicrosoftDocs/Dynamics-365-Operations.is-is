---
title: ROUND ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUND í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744488"
---
# <a name="round-er-function"></a><span data-ttu-id="78109-103">ROUND ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="78109-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78109-104">Aðgerðin `ROUND` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð að tilgreindum fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="78109-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="78109-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="78109-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="78109-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="78109-106">Arguments</span></span>

<span data-ttu-id="78109-107">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="78109-107">`number`: *Real*</span></span>

<span data-ttu-id="78109-108">Tölugildi sem verður að vera sléttað.</span><span class="sxs-lookup"><span data-stu-id="78109-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="78109-109">`decimals`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="78109-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="78109-110">Tölugildi sem stendur fyrir fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="78109-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="78109-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="78109-111">Return values</span></span>

<span data-ttu-id="78109-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="78109-112">*Real*</span></span>

<span data-ttu-id="78109-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="78109-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="78109-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="78109-114">Usage notes</span></span>

<span data-ttu-id="78109-115">Ef gildi frumbreytunnar `decimals` er hærra en 0 (núll), er tilgreind tala námunduð að þetta mörgum aukastöfum.</span><span class="sxs-lookup"><span data-stu-id="78109-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="78109-116">Ef gildi `decimals` frumbreytu er **0** (núll), er tilgreind tala námunduð að næstu heiltölu.</span><span class="sxs-lookup"><span data-stu-id="78109-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="78109-117">Ef gildi frumbreytunnar `decimals` er lægra en 0 (núll), er tilgreind tala námunduð til vinstri við tugastafinn.</span><span class="sxs-lookup"><span data-stu-id="78109-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="78109-118">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="78109-118">Example 1</span></span>

<span data-ttu-id="78109-119">`ROUND (1200.767, 2)` sléttar um tvo aukastafi og skilar **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="78109-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="78109-120">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="78109-120">Example 2</span></span>

<span data-ttu-id="78109-121">`ROUND (1200.767, -3)` sléttar að næsta margfeldi svæðisins 1.000 og skilar **1000**.</span><span class="sxs-lookup"><span data-stu-id="78109-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="78109-122">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="78109-122">Example 3</span></span>

<span data-ttu-id="78109-123">`ROUND (1200.5, 0)` námundar að næstu heilli tölu og skilar **1200**, á meðan `ROUND (1201.5, 0)` gerir það sama og skilar **1202**.</span><span class="sxs-lookup"><span data-stu-id="78109-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78109-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="78109-124">Additional resources</span></span>

[<span data-ttu-id="78109-125">Stærðfræðilegar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="78109-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]