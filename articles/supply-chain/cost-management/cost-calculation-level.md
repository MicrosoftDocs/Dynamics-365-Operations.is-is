---
title: Kostnaðarútreikningsstig
description: Þetta efnisatriði útskýrir uppskriftarstig sem heitir kostnaðarútreikningsstig. Þetta uppskriftarstig tekur ekki mið af framleiðslu og runupöntunum í útreikningum sínum.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251027"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="15d76-104">Kostnaðarútreikningsstig</span><span class="sxs-lookup"><span data-stu-id="15d76-104">Cost calculation level</span></span>

<span data-ttu-id="15d76-105">Uppskriftarstigið sem heitir **Kostnaðarútreikningsstig** tekur ekki mið af framleiðslupöntunum og runupöntunum í útreikningum sínum.</span><span class="sxs-lookup"><span data-stu-id="15d76-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="15d76-106">Kerfið notar þetta stig þegar kostnaðarútreikningar eru keyrðir í kostnaðarútgáfum.</span><span class="sxs-lookup"><span data-stu-id="15d76-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="15d76-107">Í úrvinnslum á borð við endurútreikningum og birgðalokunum notar kerfið uppskriftarstigið **Kostnaðarútreikningsstig** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="15d76-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="15d76-108">Eftirfarandi einföld atburðarás sýnir muninn milli uppskriftarstiganna **Kostnaðarútreikningsstig** og **Kostnaðarstig**.</span><span class="sxs-lookup"><span data-stu-id="15d76-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="15d76-109">Þú ert með þrjár afurðir: A, B og C. Afurð C er hluti af afurð B, og afurð B er hluti af afurð A.</span><span class="sxs-lookup"><span data-stu-id="15d76-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="15d76-110">**Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="15d76-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="15d76-111">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="15d76-111">**Product A:** 0</span></span>
    - <span data-ttu-id="15d76-112">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="15d76-112">**Product B:** 1</span></span>
    - <span data-ttu-id="15d76-113">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="15d76-113">**Product C:** 2</span></span>

- <span data-ttu-id="15d76-114">**Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="15d76-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="15d76-115">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="15d76-115">**Product A:** 0</span></span>
    - <span data-ttu-id="15d76-116">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="15d76-116">**Product B:** 1</span></span>
    - <span data-ttu-id="15d76-117">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="15d76-117">**Product C:** 2</span></span>

<span data-ttu-id="15d76-118">Framleiðslupöntun fyrir afurð C er þá stofnuð og afurð A er bætt við uppskrift framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="15d76-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="15d76-119">Eftir að pöntun er áætluð eru uppskriftarstig uppfærð á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="15d76-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="15d76-120">**Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="15d76-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="15d76-121">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="15d76-121">**Product B:** 1</span></span>
    - <span data-ttu-id="15d76-122">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="15d76-122">**Product C:** 2</span></span>
    - <span data-ttu-id="15d76-123">**Vara A:** 3</span><span class="sxs-lookup"><span data-stu-id="15d76-123">**Product A:** 3</span></span>

- <span data-ttu-id="15d76-124">**Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="15d76-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="15d76-125">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="15d76-125">**Product A:** 0</span></span>
    - <span data-ttu-id="15d76-126">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="15d76-126">**Product B:** 1</span></span>
    - <span data-ttu-id="15d76-127">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="15d76-127">**Product C:** 2</span></span>

<span data-ttu-id="15d76-128">Þessi hegðun tryggir að breytingar á uppskriftum framleiðslupantana hafa ekki áhrif á væntanlega kostnaðarútreikninga.</span><span class="sxs-lookup"><span data-stu-id="15d76-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]