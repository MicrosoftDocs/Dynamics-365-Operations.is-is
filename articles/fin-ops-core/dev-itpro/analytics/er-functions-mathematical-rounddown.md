---
title: ROUNDDOWN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDDOWN í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744528"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="9d412-103">ROUNDDOWN ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="9d412-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d412-104">Aðgerðin `ROUNDDOWN` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð niður að tilgreindum fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="9d412-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d412-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="9d412-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="9d412-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="9d412-106">Arguments</span></span>

<span data-ttu-id="9d412-107">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="9d412-107">`number`: *Real*</span></span>

<span data-ttu-id="9d412-108">Tölugildi sem verður að vera sléttað niður.</span><span class="sxs-lookup"><span data-stu-id="9d412-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="9d412-109">`decimals`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="9d412-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="9d412-110">Tölugildi sem stendur fyrir fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="9d412-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d412-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="9d412-111">Return values</span></span>

<span data-ttu-id="9d412-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="9d412-112">*Real*</span></span>

<span data-ttu-id="9d412-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="9d412-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9d412-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="9d412-114">Usage notes</span></span>

<span data-ttu-id="9d412-115">Þessi aðgerð hegðar sér eins og [ROUND](er-functions-mathematical-round.md), en hún námundar alltaf tilgreindri tölu niður (í átt að núlli).</span><span class="sxs-lookup"><span data-stu-id="9d412-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="9d412-116">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="9d412-116">Example 1</span></span>

<span data-ttu-id="9d412-117">`ROUNDDOWN (1200.767, 2)` sléttar niður um tvo aukastafi og skilar **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="9d412-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="9d412-118">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="9d412-118">Example 2</span></span>

<span data-ttu-id="9d412-119">`ROUNDDOWN (1700.767, -3)` sléttar niður að næsta margfeldi svæðisins 1.000 og skilar **1000**.</span><span class="sxs-lookup"><span data-stu-id="9d412-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d412-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9d412-120">Additional resources</span></span>

[<span data-ttu-id="9d412-121">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="9d412-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
