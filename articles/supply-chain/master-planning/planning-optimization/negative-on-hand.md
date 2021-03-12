---
title: Áætlunargerð með neikvætt lagermagn
description: Þetta efni útskýrir hvernig neikvæður lager er meðhöndlaður þegar þú notar fínstillingu áætlunargerðar.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983467"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="5dd26-103">Áætlunargerð með neikvætt lagermagn</span><span class="sxs-lookup"><span data-stu-id="5dd26-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5dd26-104">Ef kerfið sýnir neikvætt samanlagt birgðamagn, meðhöndlar áætlunarvélin magnið sem 0 (núll) til að koma í veg fyrir offramboð.</span><span class="sxs-lookup"><span data-stu-id="5dd26-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="5dd26-105">Svona virkar þessi virkni:</span><span class="sxs-lookup"><span data-stu-id="5dd26-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="5dd26-106">Fínstilling áætlunargerðar safnar saman lagermagninu á lægsta stigi þekjuvídda.</span><span class="sxs-lookup"><span data-stu-id="5dd26-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="5dd26-107">(Til dæmis ef *staðsetning* er ekki þekjuvídd safnar fínstilling áætlanagerðar saman lagermagni á stigi *vöruhúss*.)</span><span class="sxs-lookup"><span data-stu-id="5dd26-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="5dd26-108">Ef samanlagt lagermagn á lægsta stigi þekjuvídda er neikvætt, gerir kerfið ráð fyrir að lagermagnið sé í raun 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="5dd26-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5dd26-109">Áætlunarkerfið getur aðeins verið eins nákvæmt og inntaksgögnin.</span><span class="sxs-lookup"><span data-stu-id="5dd26-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="5dd26-110">Ef inntaksgögnin eru ónákvæm, munu neikvæðar lagerfærslur gefa til kynna að birgðagögnin í Microsoft Dynamics 365 Supply Chain Management eru ekki samstillt við hinn raunverulega heim.</span><span class="sxs-lookup"><span data-stu-id="5dd26-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="5dd26-111">Þess vegna verður niðurstaða áætlunargerðar gölluð.</span><span class="sxs-lookup"><span data-stu-id="5dd26-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="5dd26-112">Til að fá nákvæma niðurstöðu áætlanagerðar ættir þú að lágmarka fjölda skráa sem sýna neikvætt lagermagn.</span><span class="sxs-lookup"><span data-stu-id="5dd26-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="5dd26-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="5dd26-113">Example 1</span></span>

<span data-ttu-id="5dd26-114">Vöruhús 13 er stillt á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="5dd26-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="5dd26-115">**Þekjukóði:** Lágm./Hám.</span><span class="sxs-lookup"><span data-stu-id="5dd26-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="5dd26-116">**Lágmark:** 15 stykki (stk.)</span><span class="sxs-lookup"><span data-stu-id="5dd26-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="5dd26-117">**Hámark:** 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="5dd26-118">Lægsta stig umfjöllunar er *vöruhús* og eftirfarandi lagermagn er skráð á stig *staðsetningar*:</span><span class="sxs-lookup"><span data-stu-id="5dd26-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="5dd26-119">**Vefsvæði 1, vöruhús 13, staðsetning 1:** 20 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="5dd26-120">**Vefsvæði 1, vöruhús 13, staðsetning 2:** &minus;8 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="5dd26-121">Þess vegna er samanlagt magn á hendi fyrir vöruhús 13 12 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="5dd26-122">(= 20 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-122">(= 20 pcs.</span></span> <span data-ttu-id="5dd26-123">&minus; 8 stk.).</span><span class="sxs-lookup"><span data-stu-id="5dd26-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="5dd26-124">Í þessu tilfelli notar áætlunarvélin samanlagt lagermagn 12 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="5dd26-125">fyrir vöruhús 13.</span><span class="sxs-lookup"><span data-stu-id="5dd26-125">for warehouse 13.</span></span>

<span data-ttu-id="5dd26-126">Niðurstaðan er áætluð röð 13 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="5dd26-127">(= 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-127">(= 25 pcs.</span></span> <span data-ttu-id="5dd26-128">&minus; 12 stk.) til að fylla á vöruhús 13 frá 12 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="5dd26-129">í 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="5dd26-130">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="5dd26-130">Example 2</span></span>

<span data-ttu-id="5dd26-131">Vöruhús 13 er stillt á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="5dd26-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="5dd26-132">**Þekjukóði:** Lágm./Hám.</span><span class="sxs-lookup"><span data-stu-id="5dd26-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="5dd26-133">**Lágmark:** 15 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="5dd26-134">**Hámark:** 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="5dd26-135">Lægsta stig umfjöllunar er *vöruhús* og eftirfarandi lagermagn er skráð á stig *staðsetningar*:</span><span class="sxs-lookup"><span data-stu-id="5dd26-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="5dd26-136">**Vefsvæði 1, vöruhús 13, staðsetning 1:** 4 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="5dd26-137">**Vefsvæði 1, vöruhús 13, staðsetning 2:** &minus;8 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="5dd26-138">Þess vegna er samanlagt magn á hendi fyrir vöruhús 13 &minus;4 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="5dd26-139">(= 4 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-139">(= 4 pcs.</span></span> <span data-ttu-id="5dd26-140">&minus; 8 stk.).</span><span class="sxs-lookup"><span data-stu-id="5dd26-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="5dd26-141">Með öðrum orðum, minna en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="5dd26-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="5dd26-142">Í þessu tilfelli gerir áætlunarvélin ráð fyrir að lagermagn fyrir vöruhús 13 sé 0 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="5dd26-143">í staðinn fyrir &minus;4 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="5dd26-144">Niðurstaðan er áætluð röð 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="5dd26-145">(= 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-145">(= 25 pcs.</span></span> <span data-ttu-id="5dd26-146">&minus; 0 stk.) til að fylla á vöruhús 13 frá 0 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="5dd26-147">í 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5dd26-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5dd26-148">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="5dd26-148">Related resources</span></span>

[<span data-ttu-id="5dd26-149">Yfirlit yfir fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="5dd26-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5dd26-150">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="5dd26-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5dd26-151">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="5dd26-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5dd26-152">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="5dd26-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5dd26-153">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="5dd26-153">Cancel a planning job</span></span>](cancel-planning-job.md)
