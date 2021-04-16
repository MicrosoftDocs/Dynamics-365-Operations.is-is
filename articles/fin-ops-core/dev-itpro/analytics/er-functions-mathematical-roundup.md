---
title: ROUNDUP ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDUP í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744440"
---
# <a name="roundup-er-function"></a><span data-ttu-id="3544f-103">ROUNDUP ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="3544f-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3544f-104">Aðgerðin `ROUNDUP` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð upp að tilgreindum fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="3544f-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="3544f-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="3544f-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="3544f-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="3544f-106">Arguments</span></span>

<span data-ttu-id="3544f-107">`number`: *Rauntala*</span><span class="sxs-lookup"><span data-stu-id="3544f-107">`number`: *Real*</span></span>

<span data-ttu-id="3544f-108">Tölugildi sem verður að vera sléttað upp.</span><span class="sxs-lookup"><span data-stu-id="3544f-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="3544f-109">`decimals`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="3544f-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="3544f-110">Tölugildi sem stendur fyrir fjölda aukastafa.</span><span class="sxs-lookup"><span data-stu-id="3544f-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="3544f-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="3544f-111">Return values</span></span>

<span data-ttu-id="3544f-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="3544f-112">*Real*</span></span>

<span data-ttu-id="3544f-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="3544f-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3544f-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="3544f-114">Usage notes</span></span>

<span data-ttu-id="3544f-115">Þessi aðgerð hegðar sér eins og [ROUND](er-functions-mathematical-round.md), en hún námundar tilgreindri tölu upp (í átt frá núlli).</span><span class="sxs-lookup"><span data-stu-id="3544f-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="3544f-116">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="3544f-116">Example 1</span></span>

<span data-ttu-id="3544f-117">`ROUNDUP (1200.763, 2)` sléttar upp um tvo aukastafi og skilar **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="3544f-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3544f-118">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="3544f-118">Example 2</span></span>

<span data-ttu-id="3544f-119">`ROUNDUP (1200.767, -3)` sléttar upp að næsta margfeldi svæðisins 1.000 og skilar **2000**.</span><span class="sxs-lookup"><span data-stu-id="3544f-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3544f-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3544f-120">Additional resources</span></span>

[<span data-ttu-id="3544f-121">Reikniaðgerðir</span><span class="sxs-lookup"><span data-stu-id="3544f-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]