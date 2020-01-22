---
title: ROUNDUP ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDUP í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917052"
---
# <span data-ttu-id="06ed2-103"><a name="ROUNDUP">ROUNDUP ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="06ed2-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06ed2-104">Aðgerðin `ROUNDUP` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð upp að tilgreindum fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="06ed2-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ed2-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="06ed2-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="06ed2-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="06ed2-106">Arguments</span></span>

<span data-ttu-id="06ed2-107">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="06ed2-107">`number`: *Real*</span></span>

<span data-ttu-id="06ed2-108">Tölugildi sem verður að vera sléttað upp.</span><span class="sxs-lookup"><span data-stu-id="06ed2-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="06ed2-109">`decimals`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="06ed2-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="06ed2-110">Tölugildi sem stendur fyrir fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="06ed2-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="06ed2-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="06ed2-111">Return values</span></span>

<span data-ttu-id="06ed2-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="06ed2-112">*Real*</span></span>

<span data-ttu-id="06ed2-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="06ed2-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="06ed2-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="06ed2-114">Usage notes</span></span>

<span data-ttu-id="06ed2-115">Þessi aðgerð hegðar sér eins og [ROUND](er-functions-mathematical-round.md), en hún námundar tilgreindri tölu upp (í átt frá núlli).</span><span class="sxs-lookup"><span data-stu-id="06ed2-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="06ed2-116">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="06ed2-116">Example 1</span></span>

<span data-ttu-id="06ed2-117">`ROUNDUP (1200.763, 2)` sléttar upp um tvo aukastafi og skilar **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="06ed2-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="06ed2-118">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="06ed2-118">Example 2</span></span>

<span data-ttu-id="06ed2-119">`ROUNDUP (1200.767, -3)` sléttar upp að næsta margfeldi svæðisins 1.000 og skilar **2000**.</span><span class="sxs-lookup"><span data-stu-id="06ed2-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06ed2-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="06ed2-120">Additional resources</span></span>

[<span data-ttu-id="06ed2-121">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="06ed2-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
