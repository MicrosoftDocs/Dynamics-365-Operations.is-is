--- 
title: "Stofna dagatal og mynda vinnutíma"
description: "Dagatöl lýsa afkastagetu og vinnutíma í rekstrartilföngum."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 97751310cee3441d80d57860bc90490cf5708de2
ms.contentlocale: is-is
ms.lasthandoff: 02/02/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="aa94e-103">Stofna dagatal og mynda vinnutíma</span><span class="sxs-lookup"><span data-stu-id="aa94e-103">Create a calendar and generate working times</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa94e-104">Dagatöl lýsa afkastagetu og vinnutíma í rekstrartilföngum.</span><span class="sxs-lookup"><span data-stu-id="aa94e-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="aa94e-105">Þetta ferli mun aðstoða við að skilgreina dagatal vinnu miðað við sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="aa94e-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="aa94e-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="aa94e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="aa94e-107">Farið í Öll vinnusvæði > Líftímastjórnun tilfanga.</span><span class="sxs-lookup"><span data-stu-id="aa94e-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="aa94e-108">Smellt er á Dagatöl.</span><span class="sxs-lookup"><span data-stu-id="aa94e-108">Click Calendars.</span></span>
3. <span data-ttu-id="aa94e-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="aa94e-109">Click New.</span></span>
4. <span data-ttu-id="aa94e-110">Í reitinn Dagatal skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="aa94e-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="aa94e-111">Þetta er Kenni fyrir dagatal sem er notað sem tilvísun við úthlutun dagatöl, eins og rekstrartilföng eða tilfangahóp.</span><span class="sxs-lookup"><span data-stu-id="aa94e-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="aa94e-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="aa94e-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="aa94e-113">Færið inn tölu í Staðlaður vinnudagur í klukkustundum svæði.</span><span class="sxs-lookup"><span data-stu-id="aa94e-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="aa94e-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="aa94e-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="aa94e-115">Smellt er á vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="aa94e-115">Click Working times.</span></span>
9. <span data-ttu-id="aa94e-116">Smella á búa til vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="aa94e-116">Click Compose working times.</span></span>
    * <span data-ttu-id="aa94e-117">Mynda vinnustundir fyrir hvern dag tímabilsins þar sem þú vilt að hægt sé að raða vinnu.</span><span class="sxs-lookup"><span data-stu-id="aa94e-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="aa94e-118">Þegar tíminn líður, er hægt að mynda vinnutíma fyrir fleiri tímabil.</span><span class="sxs-lookup"><span data-stu-id="aa94e-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="aa94e-119">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="aa94e-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="aa94e-120">Þetta er fyrsta daginn sem þetta dagatal verður að vera opin.</span><span class="sxs-lookup"><span data-stu-id="aa94e-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="aa94e-121">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="aa94e-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="aa94e-122">Þetta er síðasta daginn sem þetta dagatal er opin.</span><span class="sxs-lookup"><span data-stu-id="aa94e-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="aa94e-123">Færa inn eða velja gildi í reitnum sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="aa94e-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="aa94e-124">Sniðmát vinnutíma skilgreinir vinnustundir fyrir hvern dag vikunnar.</span><span class="sxs-lookup"><span data-stu-id="aa94e-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="aa94e-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="aa94e-125">Click OK.</span></span>
14. <span data-ttu-id="aa94e-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="aa94e-126">Close the page.</span></span>


