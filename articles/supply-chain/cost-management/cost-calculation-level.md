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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410957"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="da852-104">Kostnaðarútreikningsstig</span><span class="sxs-lookup"><span data-stu-id="da852-104">Cost calculation level</span></span>

<span data-ttu-id="da852-105">Uppskriftarstigið sem heitir **Kostnaðarútreikningsstig** tekur ekki mið af framleiðslupöntunum og runupöntunum í útreikningum sínum.</span><span class="sxs-lookup"><span data-stu-id="da852-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="da852-106">Kerfið notar þetta stig þegar kostnaðarútreikningar eru keyrðir í kostnaðarútgáfum.</span><span class="sxs-lookup"><span data-stu-id="da852-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="da852-107">Í úrvinnslum á borð við endurútreikningum og birgðalokunum notar kerfið uppskriftarstigið **Kostnaðarútreikningsstig** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="da852-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="da852-108">Eftirfarandi einföld atburðarás sýnir muninn milli uppskriftarstiganna **Kostnaðarútreikningsstig** og **Kostnaðarstig**.</span><span class="sxs-lookup"><span data-stu-id="da852-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="da852-109">Þú ert með þrjár afurðir: A, B og C. Afurð C er hluti af afurð B, og afurð B er hluti af afurð A.</span><span class="sxs-lookup"><span data-stu-id="da852-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="da852-110">**Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="da852-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="da852-111">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="da852-111">**Product A:** 0</span></span>
    - <span data-ttu-id="da852-112">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="da852-112">**Product B:** 1</span></span>
    - <span data-ttu-id="da852-113">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="da852-113">**Product C:** 2</span></span>

- <span data-ttu-id="da852-114">**Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="da852-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="da852-115">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="da852-115">**Product A:** 0</span></span>
    - <span data-ttu-id="da852-116">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="da852-116">**Product B:** 1</span></span>
    - <span data-ttu-id="da852-117">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="da852-117">**Product C:** 2</span></span>

<span data-ttu-id="da852-118">Framleiðslupöntun fyrir afurð C er þá stofnuð og afurð A er bætt við uppskrift framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="da852-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="da852-119">Eftir að pöntun er áætluð eru uppskriftarstig uppfærð á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="da852-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="da852-120">**Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="da852-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="da852-121">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="da852-121">**Product B:** 1</span></span>
    - <span data-ttu-id="da852-122">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="da852-122">**Product C:** 2</span></span>
    - <span data-ttu-id="da852-123">**Vara A:** 3</span><span class="sxs-lookup"><span data-stu-id="da852-123">**Product A:** 3</span></span>

- <span data-ttu-id="da852-124">**Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="da852-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="da852-125">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="da852-125">**Product A:** 0</span></span>
    - <span data-ttu-id="da852-126">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="da852-126">**Product B:** 1</span></span>
    - <span data-ttu-id="da852-127">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="da852-127">**Product C:** 2</span></span>

<span data-ttu-id="da852-128">Þessi hegðun tryggir að breytingar á uppskriftum framleiðslupantana hafa ekki áhrif á væntanlega kostnaðarútreikninga.</span><span class="sxs-lookup"><span data-stu-id="da852-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
