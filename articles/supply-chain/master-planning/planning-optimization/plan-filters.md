---
title: Nota síur á áætlun
description: Þetta efni útskýrir hvernig á að nota síur á áætlun þegar virknin fínstillingu skipulagningar er notuð.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ddf9934965bd06ec805731a1cc1a667846fa180
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323417"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="bed65-103">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="bed65-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bed65-104">Þegar virknin fínstillingar áætlunargerðar er notuð geturðu notað síu á áætlun.</span><span class="sxs-lookup"><span data-stu-id="bed65-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="bed65-105">**Áætlunarsíunni** verður alltaf beitt meðan á keyrslu aðaláætlunargerðar stendur.</span><span class="sxs-lookup"><span data-stu-id="bed65-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="bed65-106">**Áætlunarsía** er gagnleg þegar þú vilt takmarka áætlun við ákveðinn hóp af vörum og ganga úr skugga um að engar aðrar vörur séu með sem hluti af aðaláætlunargerðinni sem er gerð.</span><span class="sxs-lookup"><span data-stu-id="bed65-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="bed65-107">Ef **áætlunarsía** er notuð og keyrslutímasíu er einnig beitt meðan á keyrslu aðaláætlunargerðar stendur er aðeins skörun síanna tveggja innifalin í áætlunarkeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="bed65-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="bed65-108">Hægt er að fara í **áætlunarsíuna** úr **Aðaláætlunum** þegar fínstilling áætlunargerðar er notuð.</span><span class="sxs-lookup"><span data-stu-id="bed65-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="bed65-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="bed65-109">Example scenario</span></span>

<span data-ttu-id="bed65-110">Áætlunarsía er sett upp sem inniheldur vörur A, B og C. Aðalskipulagningarkeyrslur eru síðan keyrðar fyrir sömu áætlun, en mismunandi keyrslutímasíur eru notaðar:</span><span class="sxs-lookup"><span data-stu-id="bed65-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="bed65-111">**Keyrslutímasía sem inniheldur vöru D:** Engar vörur eru fyrirhugaðar þar sem engin skörun er á milli áætlunarsíunnar og keyrslutímasíunnar.</span><span class="sxs-lookup"><span data-stu-id="bed65-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="bed65-112">**Keyrslutímasía sem inniheldur vöru A og D:** Aðeins vara A er innifalin í áætlunarkeyrslunni þar sem vara D er ekki hluti af áætlunarsíunni.</span><span class="sxs-lookup"><span data-stu-id="bed65-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="bed65-113">**Keyrslutímasía sem inniheldur vöru B:** Aðeins vara B er innifalin í áætlunarkeyrslunni og fyrra úttaki áætlunargerðar fyrir vöru A er haldið.</span><span class="sxs-lookup"><span data-stu-id="bed65-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="bed65-114">**Keyrslutímasía sem inniheldur allar vörur (auð sía):** Vörur A, B og C eru innifaldar í áætlunarkeyrslunni og fyrra úttak áætlanagerðar fyrir vörurnar A og B er yfirskrifað.</span><span class="sxs-lookup"><span data-stu-id="bed65-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="bed65-115">Þú ættir að forðast að setja áætlunarsíu á áætlunina sem er valin sem **Gildandi kvik aðaláætlun** á síðunni **Færibreytur áætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="bed65-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="bed65-116">Annars verður virkni kvikrar aðaláætlunar takmörkuð við síaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="bed65-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="bed65-117">Til dæmis, ef nettóþarfir eru uppfærðar fyrir vöru sem er ekki hluti af áætlunarsíunni, verður engin niðurstaða gefin.</span><span class="sxs-lookup"><span data-stu-id="bed65-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="bed65-118">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="bed65-118">Related resources</span></span>

[<span data-ttu-id="bed65-119">Yfirlit yfir fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="bed65-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="bed65-120">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="bed65-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="bed65-121">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="bed65-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="bed65-122">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="bed65-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="bed65-123">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="bed65-123">Cancel a planning job</span></span>](cancel-planning-job.md)
