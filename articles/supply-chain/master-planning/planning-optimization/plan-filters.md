---
title: Nota síur á áætlun
description: Þetta efni útskýrir hvernig á að nota síur á áætlun þegar virknin fínstillingu skipulagningar er notuð.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773983"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="cdae4-103">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="cdae4-103">Apply filters to a plan</span></span>

<span data-ttu-id="cdae4-104">Þegar virknin fínstillingar áætlunargerðar er notuð geturðu notað síu á áætlun.</span><span class="sxs-lookup"><span data-stu-id="cdae4-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="cdae4-105">Áætlunarsíunni verður alltaf beitt meðan á aðalskipulagningu stendur.</span><span class="sxs-lookup"><span data-stu-id="cdae4-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="cdae4-106">Áætlunarsía er gagnleg þegar þú vilt takmarka áætlun við ákveðinn hóp af vörum og ganga úr skugga um að engar aðrar vörur séu með sem hluti af aðalskipulagningu.</span><span class="sxs-lookup"><span data-stu-id="cdae4-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="cdae4-107">Ef áætlunarsía er notuð og keyrslutímasíu er einnig beitt meðan á aðalskipulagningunni stendur er aðeins skörun síanna tveggja innifalin í áætlunarkeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="cdae4-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="cdae4-108">Dæmi</span><span class="sxs-lookup"><span data-stu-id="cdae4-108">Example scenario</span></span>

<span data-ttu-id="cdae4-109">Áætlunarsía er sett upp sem inniheldur vörur A, B og C. Aðalskipulagningarkeyrslur eru síðan keyrðar fyrir sömu áætlun, en mismunandi keyrslutímasíur eru notaðar:</span><span class="sxs-lookup"><span data-stu-id="cdae4-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="cdae4-110">**Keyrslutímasía sem inniheldur vöru D:** Engar vörur eru fyrirhugaðar þar sem engin skörun er á milli áætlunarsíunnar og keyrslutímasíunnar.</span><span class="sxs-lookup"><span data-stu-id="cdae4-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="cdae4-111">**Keyrslutímasía sem inniheldur vöru A og D:** Aðeins vara A er innifalin í áætlunarkeyrslunni þar sem vara D er ekki hluti af áætlunarsíunni.</span><span class="sxs-lookup"><span data-stu-id="cdae4-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="cdae4-112">**Keyrslutímasía sem inniheldur vöru B:** Aðeins vara B er innifalin í áætlunarkeyrslunni og fyrra úttaki áætlunargerðar fyrir vöru A er haldið.</span><span class="sxs-lookup"><span data-stu-id="cdae4-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="cdae4-113">**Keyrslutímasía sem inniheldur allar vörur (auð sía):** Vörur A, B og C eru innifaldar í áætlunarkeyrslunni og fyrra úttak áætlanagerðar fyrir vörurnar A og B er yfirskrifað.</span><span class="sxs-lookup"><span data-stu-id="cdae4-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="cdae4-114">Þú ættir að forðast að setja áætlunarsíu á áætlunina sem er valin sem **Gildandi kvik aðaláætlun** á síðunni **Færibreytur áætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="cdae4-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="cdae4-115">Annars verður virkni kvikrar aðaláætlunar takmörkuð við síaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="cdae4-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="cdae4-116">Til dæmis, ef nettóþarfir eru uppfærðar fyrir vöru sem er ekki hluti af áætlunarsíunni, verður engin niðurstaða gefin.</span><span class="sxs-lookup"><span data-stu-id="cdae4-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="cdae4-117">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="cdae4-117">Related resources</span></span>

[<span data-ttu-id="cdae4-118">Yfirlit yfir fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="cdae4-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="cdae4-119">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="cdae4-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="cdae4-120">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="cdae4-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="cdae4-121">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="cdae4-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="cdae4-122">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="cdae4-122">Cancel a planning job</span></span>](cancel-planning-job.md)
