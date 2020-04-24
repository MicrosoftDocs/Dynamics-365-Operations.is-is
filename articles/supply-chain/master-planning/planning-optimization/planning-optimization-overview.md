---
title: Yfirlit yfir fínstillingu skipulagningar
description: Þessi grein veitir yfirlit yfir virkni fínstillingar áætlunargerðar.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
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
ms.openlocfilehash: f88ee8067fdd816ba6890ee28bafe8fa4d3b3ac5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208732"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="efe02-103">Yfirlit yfir fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="efe02-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="efe02-104">Viðbótin Fínstilling skipulagningar fyrir Microsoft Dynamics 365 Supply Chain Management gerir útreikning á aðaláætlunargerð mögulega utan Dynamics 365 Supply Chain Management og tengds SQL gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="efe02-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="efe02-105">Ávinningurinn sem tengist virkninni fínstilling skipulags felur í sér bætt afköst og lágmarks áhrif á SQL gagnagrunn meðan á keyrslu aðaláætlunargerðar stendur.</span><span class="sxs-lookup"><span data-stu-id="efe02-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="efe02-106">Hægt er að framkvæma skjótar áætlunarkeyrslur jafnvel á skrifstofutíma, þannig að skipuleggjendur geta strax brugðist við breytingum á kröfum eða færibreytum.</span><span class="sxs-lookup"><span data-stu-id="efe02-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="efe02-107">Til að nota fínstillingu skipulags verður þú að setja upp viðbótina fínstilling skipulags úr verkinu í Microsoft Dynamics Lifecycle Services (LCS) og kveikja á virkninni fínstilling skipulagningar í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="efe02-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="efe02-108">Frekari upplýsingar er að finna í [Hafist handa með fínstillingu skipulags](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="efe02-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="efe02-109">Eftirfarandi mynd sýnir kostinn við að keyra fínstillingu skipulags á skrifstofutíma.</span><span class="sxs-lookup"><span data-stu-id="efe02-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Kostur þess að keyra fínstillingu skipulags á skrifstofutíma](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="efe02-111">Bætt afköst</span><span class="sxs-lookup"><span data-stu-id="efe02-111">Improved performance</span></span>

<span data-ttu-id="efe02-112">Fínstillingu skipulags er hægt að nota í atburðarásum sem fela í sér tímafrekar aðaláætlanir.</span><span class="sxs-lookup"><span data-stu-id="efe02-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="efe02-113">Hún er sérstaklega hönnuð fyrir afar hraða útreikninga sem fela í sér mjög mikið magn af gögnum.</span><span class="sxs-lookup"><span data-stu-id="efe02-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="efe02-114">Vegna þess að hún er byggð sem kvarðanleg fjölhæf þjónusta geta mörg tilvik unnið saman samtímis til að reikna áætlunina.</span><span class="sxs-lookup"><span data-stu-id="efe02-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="efe02-115">Að auki fjarlægir skipulagsþjónustan álag aðaláætlunar úr kerfinu og vinnur með gagnastrreymi sem lágmarkar álag á netþjóninn.</span><span class="sxs-lookup"><span data-stu-id="efe02-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="efe02-116">Fínstilling skipulags getur hjálpað þér að ná eftirfarandi markmiðum:</span><span class="sxs-lookup"><span data-stu-id="efe02-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="efe02-117">Bæta áætlunarafköst með styttri keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="efe02-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="efe02-118">Draga úr áhrifum á aðra ferla meðan á keyrslu aðaláætlunargerðar stendur.</span><span class="sxs-lookup"><span data-stu-id="efe02-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="efe02-119">Gera tíðari áætlunarkeyrslur.</span><span class="sxs-lookup"><span data-stu-id="efe02-119">Do more frequent planning runs.</span></span> <span data-ttu-id="efe02-120">(Þú takmarkast ekki við daglega keyrslu.)</span><span class="sxs-lookup"><span data-stu-id="efe02-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="efe02-121">Treystu því að framtíðarvöxtur fyrirtækisins mun ekki leggja of mikið á áætlunarkerfið.</span><span class="sxs-lookup"><span data-stu-id="efe02-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="efe02-122">Skipulag og gagnaflæði</span><span class="sxs-lookup"><span data-stu-id="efe02-122">Architecture and data flow</span></span>

<span data-ttu-id="efe02-123">Þegar viðbótin fínstilling áætlunargerðar er sett upp úr LCS er komið á öruggri tengingu við þjónustuna Fínstilling skipulags.</span><span class="sxs-lookup"><span data-stu-id="efe02-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="efe02-124">Þjónustan er staðsett í sama landi eða svæði gagnaversins og tengd tilvik af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="efe02-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="efe02-125">Þegar fínstilling skipulagningar hefur verið sett upp eru aðalgögn og færslugögn send úr Supply Chain Management í þjónustu Fínstilling skipulags þegar aðaláætlunargerð er keyrð.</span><span class="sxs-lookup"><span data-stu-id="efe02-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="efe02-126">Ef viðbótin fínstilling skipulagningar er fjarlægð eru öll tengd gögn í þjónustu fínstillingar skipulags fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="efe02-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="efe02-127">Hátt stig gagnaflæðis fyrir endurmyndunarkeyrslur</span><span class="sxs-lookup"><span data-stu-id="efe02-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="efe02-128">Biðlari Supply Chain Management sendir merki til að biðja um áætlunarkeyrslu úr Fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="efe02-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="efe02-129">Fínstilling skipulagningar fer fram á nauðsynleg gögn um samþætt tengi.</span><span class="sxs-lookup"><span data-stu-id="efe02-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="efe02-130">SQL gagnagrunnurinn sendir umbeðnar upplýsingar um uppsetningar-, meistara- og færslugögn til fínstillingar skipulags í gegnum tengið.</span><span class="sxs-lookup"><span data-stu-id="efe02-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="efe02-131">Tengingin þýðir upplýsingar á milli þjónustunnar Supply Chain Management og fínstillingar skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="efe02-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="efe02-132">Þjónustan Fínstilling skipulags geymir áætlunargerðarstengd gögn í minni og gerir nauðsynlega útreikninga.</span><span class="sxs-lookup"><span data-stu-id="efe02-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="efe02-133">Niðurstöður áætlunar eru sendar í gagnagrunn Supply Chain Management í gegnum tengið.</span><span class="sxs-lookup"><span data-stu-id="efe02-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="efe02-134">Niðurstöðurnar innihalda upplýsingar eins og fyrirhugaðar pantanir og upplýsingar um þarfarakningu.</span><span class="sxs-lookup"><span data-stu-id="efe02-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="efe02-135">Fínstilling skipulags sendir merki til Supply Chain Management til að gefa til kynna að áætlunarkeyrslunni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="efe02-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="efe02-136">Hún sendir einnig viðeigandi skilaboð og viðvaranir.</span><span class="sxs-lookup"><span data-stu-id="efe02-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="efe02-137">Eftirfarandi skýringarmynd sýnir gagnaflæðið.</span><span class="sxs-lookup"><span data-stu-id="efe02-137">The following illustration shows the data flow.</span></span>

![Gagnaflæði fyrir endurmyndunarkeyrslur](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="efe02-139">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="efe02-139">Related resources</span></span>

[<span data-ttu-id="efe02-140">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="efe02-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="efe02-141">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="efe02-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="efe02-142">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="efe02-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="efe02-143">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="efe02-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="efe02-144">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="efe02-144">Cancel a planning job</span></span>](cancel-planning-job.md)
