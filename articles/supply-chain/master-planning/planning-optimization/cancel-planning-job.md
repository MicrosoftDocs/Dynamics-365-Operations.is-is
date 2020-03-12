---
title: Hætta við áætlunarvinnslu
description: Þetta efni útskýrir hvernig á að hætta við virka áætlunarvinnslu sem notar virknina fínstillingu skipulagningar.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
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
ms.openlocfilehash: 18c5c7b8030fc6adbc548dab750e4f454aebc867
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076347"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="ca47a-103">Hætta við áætlunarverk</span><span class="sxs-lookup"><span data-stu-id="ca47a-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ca47a-104">Í Microsoft Dynamics 365 Supply Chain Management er hægt að hætta við virka áætlunarvinnslu sem notar virknina fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="ca47a-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="ca47a-105">Þegar þú velur **Hætta við** í glugganum þegar fínstillingarvinnsla áætlunar virkjast beint úr notendaviðmótinu (ekki í bakgrunni) mun þetta ekki afturkalla fínstillingarvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="ca47a-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="ca47a-106">Jafnvel þó þú fáir viðvörun eins og „Aðgerð afturkölluð“, verður þú samt að nota eftirfarandi skref til að hætta við áætlunarvinnslu með fínstillingu áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="ca47a-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="ca47a-107">Fylgdu þessum skrefum til að hætta við virka áætlunarvinnslu.</span><span class="sxs-lookup"><span data-stu-id="ca47a-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="ca47a-108">Aðeins er hægt að hætta við virkar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="ca47a-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="ca47a-109">Farðu í **Aðaláætlanagerð \> Uppsetning \> Áætlanir**.</span><span class="sxs-lookup"><span data-stu-id="ca47a-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="ca47a-110">Veldu viðeigandi áætlun fyrir keyrslu áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="ca47a-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="ca47a-111">Veldu **Saga**.</span><span class="sxs-lookup"><span data-stu-id="ca47a-111">Select **History**.</span></span>
4. <span data-ttu-id="ca47a-112">Veldu áætlunarvinnslu sem á að hætta við.</span><span class="sxs-lookup"><span data-stu-id="ca47a-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="ca47a-113">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="ca47a-113">Select **Cancel**.</span></span>

<span data-ttu-id="ca47a-114">Vinnslustaðan verður **Hættir við** þar til fínstillingarþjónusta áætlunargerðar staðfestir að vinnslunni hafi verið aflýst.</span><span class="sxs-lookup"><span data-stu-id="ca47a-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="ca47a-115">Stöðunni verður síðan breytt í **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="ca47a-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="ca47a-116">Til að sjá stöðubreytingar verður þú að endurnýja síðuna með því að velja hnappinn **Endurhlaða**.</span><span class="sxs-lookup"><span data-stu-id="ca47a-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca47a-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ca47a-117">Additional resources</span></span>

[<span data-ttu-id="ca47a-118">Yfirlit yfir fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="ca47a-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="ca47a-119">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="ca47a-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="ca47a-120">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="ca47a-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="ca47a-121">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="ca47a-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="ca47a-122">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="ca47a-122">Apply filters to a plan</span></span>](plan-filters.md)
