---
title: Stofna dagatöl og mynda vinnutíma
description: Dagatöl lýsa afkastagetu og vinnutíma í rekstrartilföngum. Þessi grein útskýrir hvernig eigi að skilgreina dagatal vinnu miðað við sniðmát vinnutíma.
author: andreabichsel
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16decd94f72e6aefe4e1d058f4cfd6215d14f569
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058897"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="56227-104">Stofna dagatöl og mynda vinnutíma</span><span class="sxs-lookup"><span data-stu-id="56227-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="56227-105">Dagatöl lýsa afkastagetu og vinnutíma í rekstrartilföngum.</span><span class="sxs-lookup"><span data-stu-id="56227-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="56227-106">Þessi grein útskýrir hvernig eigi að skilgreina dagatal vinnu miðað við sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="56227-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="56227-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="56227-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="56227-108">Á heimasíðunni velurðu **Líftímastjórnun tilfanga**.</span><span class="sxs-lookup"><span data-stu-id="56227-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="56227-109">Veldu **Dagatöl**.</span><span class="sxs-lookup"><span data-stu-id="56227-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="56227-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="56227-110">Select **New**.</span></span>
4. <span data-ttu-id="56227-111">Í reitnum **Dagatal** flokkaðru dagatalið þitt.</span><span class="sxs-lookup"><span data-stu-id="56227-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="56227-112">Þetta er Kenni fyrir dagatal sem er notað sem tilvísun við úthlutun dagatöl, eins og rekstrartilföng eða tilfangahóp.</span><span class="sxs-lookup"><span data-stu-id="56227-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="56227-113">Í reitinum **Heiti** skal færa dagatalið inn.</span><span class="sxs-lookup"><span data-stu-id="56227-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="56227-114">Í reitnum **Staðlaðir vinnudagar í klukkustundum** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="56227-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="56227-115">Gakktu úr skugga um að röðin sé valin og veldu síðan **Vinnutímar** úr aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="56227-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="56227-116">Veldu **Byggja upp vinnutíma**.</span><span class="sxs-lookup"><span data-stu-id="56227-116">Select **Compose working times**.</span></span> <span data-ttu-id="56227-117">Mynda vinnustundir fyrir hvern dag tímabilsins þar sem þú vilt að hægt sé að raða vinnu.</span><span class="sxs-lookup"><span data-stu-id="56227-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="56227-118">Þegar tíminn líður, er hægt að mynda vinnutíma fyrir fleiri tímabil.</span><span class="sxs-lookup"><span data-stu-id="56227-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="56227-119">Í reitnum **Frá dags.** færirði inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="56227-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="56227-120">Þetta er fyrsta daginn sem þetta dagatal verður að vera opin.</span><span class="sxs-lookup"><span data-stu-id="56227-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="56227-121">Í reitnum **Til dags.** færirðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="56227-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="56227-122">Þetta er síðasta daginn sem þetta dagatal er opin.</span><span class="sxs-lookup"><span data-stu-id="56227-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="56227-123">Í reinum **Sniðmát vinnutíma** færirðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="56227-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="56227-124">Sniðmát vinnutíma skilgreinir vinnustundir fyrir hvern dag vikunnar.</span><span class="sxs-lookup"><span data-stu-id="56227-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="56227-125">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56227-125">Select **OK**.</span></span>
13. <span data-ttu-id="56227-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="56227-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]