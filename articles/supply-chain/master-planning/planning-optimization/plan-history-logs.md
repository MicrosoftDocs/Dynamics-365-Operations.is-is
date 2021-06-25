---
title: Skoða áætlunarsögu og skipulagsskrár
description: Þetta efni útskýrir hvernig á að skoða sögu áætlunarvinnsla sem fara af stað vegna virkni fínstillingar áætlunargerðar.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187248"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="a5f78-103">Skoða áætlunarsögu og skipulagsskrár</span><span class="sxs-lookup"><span data-stu-id="a5f78-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5f78-104">Þetta efni útskýrir hvernig á að skoða sögu áætlunarvinnsla sem fara af stað vegna virkni fínstillingar áætlunargerðar í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5f78-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a5f78-105">Til að skoða sögu fyrir áætlun, opnaðu áætlunina með því að fara til **Aðaláætlunargerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir** og velja **Saga**.</span><span class="sxs-lookup"><span data-stu-id="a5f78-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="a5f78-106">Í sögunni eru allar vinnslur fyrir valda áætlun.</span><span class="sxs-lookup"><span data-stu-id="a5f78-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="a5f78-107">Listinn nær yfir loknar og virkar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="a5f78-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="a5f78-108">Verkferillinn fyrir keyrslur aðaláætlanagerðar á fínstillingu skipulagningar geymir að hámarki 60 færslur fyrir hverja aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="a5f78-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="a5f78-109">Í hvert sinn sem nýr útreikningur aðaláætlanagerð verður elstu ferilfærslu áætlunarinnar eytt.</span><span class="sxs-lookup"><span data-stu-id="a5f78-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="a5f78-110">Auk þess að sjá upphafstíma og stöðu á vinnslum geturðu skoðað kladda fyrir tiltekna vinnslu.</span><span class="sxs-lookup"><span data-stu-id="a5f78-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="a5f78-111">Í kladdanum eru viðbótarupplýsingar og viðvaranir.</span><span class="sxs-lookup"><span data-stu-id="a5f78-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="a5f78-112">Ekki eru allar vinnslur með kladda.</span><span class="sxs-lookup"><span data-stu-id="a5f78-112">Not all jobs have a log.</span></span> <span data-ttu-id="a5f78-113">Til að skoða kladda fyrir vinnslu velurðu **Kladdi**.</span><span class="sxs-lookup"><span data-stu-id="a5f78-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="a5f78-114">Kladdafærslur eru aðeins geymdar í 30 daga frá deginum sem verkið klárast og er eytt sjálfkrafa eftir það.</span><span class="sxs-lookup"><span data-stu-id="a5f78-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="a5f78-115">Tengd tilföng</span><span class="sxs-lookup"><span data-stu-id="a5f78-115">Related resources</span></span>

- [<span data-ttu-id="a5f78-116">Yfirlit yfir fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="a5f78-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="a5f78-117">Hafist handa með fínstillingu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="a5f78-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="a5f78-118">Greining á samsvörun áætlunarfínstillingar</span><span class="sxs-lookup"><span data-stu-id="a5f78-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="a5f78-119">Nota síur á áætlun</span><span class="sxs-lookup"><span data-stu-id="a5f78-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="a5f78-120">Hætta við áætlunarvinnslu</span><span class="sxs-lookup"><span data-stu-id="a5f78-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]