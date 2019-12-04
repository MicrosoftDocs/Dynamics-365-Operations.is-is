---
title: Hætta við áætlunarvinnslu
description: Þetta efni útskýrir hvernig á að hætta við virka áætlunarvinnslu sem notar virknina fínstillingu skipulagningar.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773984"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="df79f-103">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="df79f-103">Cancel a planning job</span></span>

<span data-ttu-id="df79f-104">Í Microsoft Dynamics 365 Supply Chain Management er hægt að hætta við virka áætlunarvinnslu sem notar virknina fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="df79f-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="df79f-105">Fylgdu þessum skrefum til að hætta við virka áætlunarvinnslu.</span><span class="sxs-lookup"><span data-stu-id="df79f-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="df79f-106">Aðeins er hægt að hætta við virkar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="df79f-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="df79f-107">Farðu í **Aðaláætlanagerð \> Uppsetning \> Áætlanir**.</span><span class="sxs-lookup"><span data-stu-id="df79f-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="df79f-108">Veldu viðeigandi áætlun fyrir keyrslu áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="df79f-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="df79f-109">Veldu **Saga**.</span><span class="sxs-lookup"><span data-stu-id="df79f-109">Select **History**.</span></span>
4. <span data-ttu-id="df79f-110">Veldu áætlunarvinnslu sem á að hætta við.</span><span class="sxs-lookup"><span data-stu-id="df79f-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="df79f-111">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="df79f-111">Select **Cancel**.</span></span>

<span data-ttu-id="df79f-112">Vinnslustaðan verður **Hættir við** þar til fínstillingarþjónusta áætlunargerðar staðfestir að vinnslunni hafi verið aflýst.</span><span class="sxs-lookup"><span data-stu-id="df79f-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="df79f-113">Stöðunni verður síðan breytt í **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="df79f-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="df79f-114">Til að sjá stöðubreytingar verður þú að endurnýja síðuna með því að velja hnappinn **Endurhlaða**.</span><span class="sxs-lookup"><span data-stu-id="df79f-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="df79f-115">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="df79f-115">Related resources</span></span>

[<span data-ttu-id="df79f-116">Yfirlit yfir fínstillingu skipulagningar</span><span class="sxs-lookup"><span data-stu-id="df79f-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="df79f-117">Byrjaðu með hagræðingu skipulags</span><span class="sxs-lookup"><span data-stu-id="df79f-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="df79f-118">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="df79f-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="df79f-119">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="df79f-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="df79f-120">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="df79f-120">Apply filters to a plan</span></span>](plan-filters.md)
