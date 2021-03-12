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
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967731"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="75b78-104">Kostnaðarútreikningsstig</span><span class="sxs-lookup"><span data-stu-id="75b78-104">Cost calculation level</span></span>

<span data-ttu-id="75b78-105">Uppskriftarstigið sem heitir **Kostnaðarútreikningsstig** tekur ekki mið af framleiðslupöntunum og runupöntunum í útreikningum sínum.</span><span class="sxs-lookup"><span data-stu-id="75b78-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="75b78-106">Kerfið notar þetta stig þegar kostnaðarútreikningar eru keyrðir í kostnaðarútgáfum.</span><span class="sxs-lookup"><span data-stu-id="75b78-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="75b78-107">Í úrvinnslum á borð við endurútreikningum og birgðalokunum notar kerfið uppskriftarstigið **Kostnaðarútreikningsstig** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="75b78-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="75b78-108">Eftirfarandi einföld atburðarás sýnir muninn milli uppskriftarstiganna **Kostnaðarútreikningsstig** og **Kostnaðarstig**.</span><span class="sxs-lookup"><span data-stu-id="75b78-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="75b78-109">Þú ert með þrjár afurðir: A, B og C. Afurð C er hluti af afurð B, og afurð B er hluti af afurð A.</span><span class="sxs-lookup"><span data-stu-id="75b78-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="75b78-110">**Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="75b78-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="75b78-111">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="75b78-111">**Product A:** 0</span></span>
    - <span data-ttu-id="75b78-112">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="75b78-112">**Product B:** 1</span></span>
    - <span data-ttu-id="75b78-113">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="75b78-113">**Product C:** 2</span></span>

- <span data-ttu-id="75b78-114">**Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="75b78-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="75b78-115">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="75b78-115">**Product A:** 0</span></span>
    - <span data-ttu-id="75b78-116">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="75b78-116">**Product B:** 1</span></span>
    - <span data-ttu-id="75b78-117">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="75b78-117">**Product C:** 2</span></span>

<span data-ttu-id="75b78-118">Framleiðslupöntun fyrir afurð C er þá stofnuð og afurð A er bætt við uppskrift framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="75b78-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="75b78-119">Eftir að pöntun er áætluð eru uppskriftarstig uppfærð á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="75b78-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="75b78-120">**Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="75b78-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="75b78-121">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="75b78-121">**Product B:** 1</span></span>
    - <span data-ttu-id="75b78-122">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="75b78-122">**Product C:** 2</span></span>
    - <span data-ttu-id="75b78-123">**Vara A:** 3</span><span class="sxs-lookup"><span data-stu-id="75b78-123">**Product A:** 3</span></span>

- <span data-ttu-id="75b78-124">**Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:</span><span class="sxs-lookup"><span data-stu-id="75b78-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="75b78-125">**Vara A:** 0</span><span class="sxs-lookup"><span data-stu-id="75b78-125">**Product A:** 0</span></span>
    - <span data-ttu-id="75b78-126">**Afurð B:** 1</span><span class="sxs-lookup"><span data-stu-id="75b78-126">**Product B:** 1</span></span>
    - <span data-ttu-id="75b78-127">**Afurð C:** 2</span><span class="sxs-lookup"><span data-stu-id="75b78-127">**Product C:** 2</span></span>

<span data-ttu-id="75b78-128">Þessi hegðun tryggir að breytingar á uppskriftum framleiðslupantana hafa ekki áhrif á væntanlega kostnaðarútreikninga.</span><span class="sxs-lookup"><span data-stu-id="75b78-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
