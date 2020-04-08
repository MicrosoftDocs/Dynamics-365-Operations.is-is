---
title: Stofna dagatöl og mynda vinnutíma
description: Dagatöl lýsa afkastagetu og vinnutíma í rekstrartilföngum. Þessi grein útskýrir hvernig eigi að skilgreina dagatal vinnu miðað við sniðmát vinnutíma.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38c0482c62e86e3e12e4bdd67f6d8f090ddfbfeb
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009389"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="dcc31-104">Stofna dagatöl og mynda vinnutíma</span><span class="sxs-lookup"><span data-stu-id="dcc31-104">Create calendars and generate working times</span></span>



<span data-ttu-id="dcc31-105">Dagatöl lýsa afkastagetu og vinnutíma í rekstrartilföngum.</span><span class="sxs-lookup"><span data-stu-id="dcc31-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="dcc31-106">Þessi grein útskýrir hvernig eigi að skilgreina dagatal vinnu miðað við sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="dcc31-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="dcc31-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="dcc31-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="dcc31-108">Á heimasíðunni velurðu **Líftímastjórnun tilfanga**.</span><span class="sxs-lookup"><span data-stu-id="dcc31-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="dcc31-109">Veldu **Dagatöl**.</span><span class="sxs-lookup"><span data-stu-id="dcc31-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="dcc31-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="dcc31-110">Select **New**.</span></span>
4. <span data-ttu-id="dcc31-111">Í reitnum **Dagatal** flokkaðru dagatalið þitt.</span><span class="sxs-lookup"><span data-stu-id="dcc31-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="dcc31-112">Þetta er Kenni fyrir dagatal sem er notað sem tilvísun við úthlutun dagatöl, eins og rekstrartilföng eða tilfangahóp.</span><span class="sxs-lookup"><span data-stu-id="dcc31-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="dcc31-113">Í reitinum **Heiti** skal færa dagatalið inn.</span><span class="sxs-lookup"><span data-stu-id="dcc31-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="dcc31-114">Í reitnum **Staðlaðir vinnudagar í klukkustundum** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dcc31-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="dcc31-115">Gakktu úr skugga um að röðin sé valin og veldu síðan **Vinnutímar** úr aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="dcc31-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="dcc31-116">Veldu **Byggja upp vinnutíma**.</span><span class="sxs-lookup"><span data-stu-id="dcc31-116">Select **Compose working times**.</span></span> <span data-ttu-id="dcc31-117">Mynda vinnustundir fyrir hvern dag tímabilsins þar sem þú vilt að hægt sé að raða vinnu.</span><span class="sxs-lookup"><span data-stu-id="dcc31-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="dcc31-118">Þegar tíminn líður, er hægt að mynda vinnutíma fyrir fleiri tímabil.</span><span class="sxs-lookup"><span data-stu-id="dcc31-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="dcc31-119">Í reitnum **Frá dags.** færirði inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="dcc31-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="dcc31-120">Þetta er fyrsta daginn sem þetta dagatal verður að vera opin.</span><span class="sxs-lookup"><span data-stu-id="dcc31-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="dcc31-121">Í reitnum **Til dags.** færirðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="dcc31-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="dcc31-122">Þetta er síðasta daginn sem þetta dagatal er opin.</span><span class="sxs-lookup"><span data-stu-id="dcc31-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="dcc31-123">Í reinum **Sniðmát vinnutíma** færirðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="dcc31-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="dcc31-124">Sniðmát vinnutíma skilgreinir vinnustundir fyrir hvern dag vikunnar.</span><span class="sxs-lookup"><span data-stu-id="dcc31-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="dcc31-125">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="dcc31-125">Select **OK**.</span></span>
13. <span data-ttu-id="dcc31-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dcc31-126">Close the page.</span></span>
