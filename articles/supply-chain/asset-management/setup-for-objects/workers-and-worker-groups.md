---
title: Viðhaldsstarfskraftar og starfskraftahópar
description: Þetta efni útskýrir viðhaldsstarfskrafta starfsmannahópa í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c85fc24cdf0b3cd1a188ccf0f477ffbfa5fab960
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783338"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="464ee-103">Viðhaldsstarfskraftar og starfskraftahópar</span><span class="sxs-lookup"><span data-stu-id="464ee-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="464ee-104">Þetta efni útskýrir viðhaldsstarfskrafta starfsmannahópa í eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="464ee-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="464ee-105">Í eignastjórnun geturðu tengt viðhaldsstarfsmenn við virka staði.</span><span class="sxs-lookup"><span data-stu-id="464ee-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="464ee-106">(Sjá frekari upplýsingar um hagnýta staði [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md) .) Þessi virkni gæti verið gagnleg ef þú ert til dæmis að skipuleggja viðhaldsstörf á vél sem er staðsett á hagnýtum stað 01 og þú vilt úthluta viðhaldsstarfsmönnum frá sama stað til að framkvæma verkið.</span><span class="sxs-lookup"><span data-stu-id="464ee-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="464ee-107">Þú getur einnig búið til hópa starfsmanna viðhalds og tengt viðhald starfsmanna við þá.</span><span class="sxs-lookup"><span data-stu-id="464ee-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="464ee-108">Þessi virkni er gagnleg þegar þú vinnur einfalda tímasetningu vinnu og þú vilt skipuleggja hóp viðhaldsstarfsmanna í vinnupöntun.</span><span class="sxs-lookup"><span data-stu-id="464ee-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="464ee-109">Þú getur notað viðhaldsstarfsmenn og hópa viðhaldsstarfsmanna til að setja upp valinn viðhaldsstarfsmenn og ábyrga viðhaldsstarfsmenn.</span><span class="sxs-lookup"><span data-stu-id="464ee-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="464ee-110">Stofna starfskrafta</span><span class="sxs-lookup"><span data-stu-id="464ee-110">Create workers</span></span>

1. <span data-ttu-id="464ee-111">Veldu **Eignastýring** \> **Uppsetning** \> **Starfskraftar** \> **Starfskraftar**.</span><span class="sxs-lookup"><span data-stu-id="464ee-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="464ee-112">Veldu **Nýtt** til að bæta nýjum starfskrafti við listann.</span><span class="sxs-lookup"><span data-stu-id="464ee-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="464ee-113">Í retinum **starfskraftur** velurðu starfskraftinn.</span><span class="sxs-lookup"><span data-stu-id="464ee-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="464ee-114">Stilltu **Virkur** kostur á **Já** til að tímasetja starfsmanninn eftir verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="464ee-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="464ee-115">Á flýtiflipanum **Almennt** eru reitirnir **Tilföng** og **Lýsing** sjálfkrafa fylltir út ef tilföng hafa verið valin fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="464ee-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="464ee-116">Reiturinn **Dagatal** er einnig sjálfkrafa fyllt út, að því tilskildu að þú hafir sett upp starfsmanninn sem auðlind og úthlutað dagatali til þess tilfanga á **Tilföng** síðu (**Fyrirtækjastjórnun** \> **Tilföng** \> **Tilföng**).</span><span class="sxs-lookup"><span data-stu-id="464ee-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="464ee-117">Á flýtiflipanum **Hópar** veldu **Bæta við**, og veldu síðan viðhald starfsmannahóps fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="464ee-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="464ee-118">Starfskraftur getur tengst fleiri en einum hóp.</span><span class="sxs-lookup"><span data-stu-id="464ee-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="464ee-119">Í venjulegu skipulagi er tengsl starfsmanns við hóp gildi frá og með þeim degi þegar þú bætir við hópnum og hann rennur aldrei út.</span><span class="sxs-lookup"><span data-stu-id="464ee-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="464ee-120">Þessi dagsetning er sýnd í reitnum **Virkt**.</span><span class="sxs-lookup"><span data-stu-id="464ee-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="464ee-121">Til að sjá reitinn **Virkt** veldu **Útsýni** \> **Allt**.</span><span class="sxs-lookup"><span data-stu-id="464ee-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="464ee-122">Ef tengsl starfsmanns við hóp ættu að takmarkast við ákveðið tímabil, notaðu **Árangursrík** og **Fyrning** reiti til að skilgreina tímabilið.</span><span class="sxs-lookup"><span data-stu-id="464ee-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="464ee-123">Á flýtiflipanum **Virkar staðsetningar** veldu **Bæta við**, og veldu síðan virka staðsetningu fyrir viðhaldsstarfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="464ee-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="464ee-124">Tilgreindu einnig hvaða staðsetning er aðal virkni staða starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="464ee-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="464ee-125">Þegar þú bætir starfsmanni við virkar stöðum birtast allar virkar eignir sem tengjast þessum virkni stöðum á ýmsum valmyndaratriðum, svo sem **Virku eignir mínar** og **Virku virku staðirnir mínir**.</span><span class="sxs-lookup"><span data-stu-id="464ee-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="464ee-126">Þeir birtast einnig í eignaleitunum sem eru sýndar þegar þú býrð til nýja eign, viðhaldsbeiðni eða vverkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="464ee-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="464ee-127">Reitirnir á flýtiflipanum **Upplýsingar** sýna fjölda viðhaldsstarfsmannahópa og virka staði sem valinn viðhaldsstarfsmaður er tengdur.</span><span class="sxs-lookup"><span data-stu-id="464ee-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="464ee-128">Stofna strafskraftahópa</span><span class="sxs-lookup"><span data-stu-id="464ee-128">Create worker groups</span></span>

1. <span data-ttu-id="464ee-129">Veldu **Eignastýring** \> **Uppsetning** \> **Starfskraftar** \> **Hópar viðhaldsstarfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="464ee-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="464ee-130">Veldu **Nýtt** til að bæta nýjum starfsmannahóp við listann.</span><span class="sxs-lookup"><span data-stu-id="464ee-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="464ee-131">Í **Hópur viðhaldsstarfsmanna** reitinn, sláðu inn kenni hópsins.</span><span class="sxs-lookup"><span data-stu-id="464ee-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="464ee-132">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="464ee-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="464ee-133">Á flýtiflipanum **Starfskraftar** veldu **Bæta við**, og veldu síðan viðhald starfsmannahóps fyrir starfsmannahópinn.</span><span class="sxs-lookup"><span data-stu-id="464ee-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="464ee-134">Fyrir upplýsingar um **Árangursrík** og **Fyrning** reitir, sjá skref 6 í fyrri aðferð.</span><span class="sxs-lookup"><span data-stu-id="464ee-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="464ee-135">Ef tilfangahópur ætti að tengjast völdum hópi viðhaldsstarfsmanna skaltu velja **Afrita úr tilfangahóp**.</span><span class="sxs-lookup"><span data-stu-id="464ee-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="464ee-136">Í **Hópur** reitinn, veldu auðlindahópinn sem á að afrita dagatalstillingar frá.</span><span class="sxs-lookup"><span data-stu-id="464ee-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="464ee-137">Síðan, í **starfsmannahópur** veldu starfsmannahópinn sem á að afrita dagatalsstillingar auðlindahópsins til.</span><span class="sxs-lookup"><span data-stu-id="464ee-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="464ee-138">Þetta skref skiptir aðeins máli ef þú vilt að viðhaldsstarfsmenn noti dagatalið sem er tengt auðlindinni (vinnumiðstöð) við tímasetningu vinnu.</span><span class="sxs-lookup"><span data-stu-id="464ee-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="464ee-139">Reitirnir á flýtiflipanum **Upplýsingar** sýna fjölda viðhaldsstarfsmannahópa og virka staði sem valinn viðhaldsstarfsmaður er tengdur.</span><span class="sxs-lookup"><span data-stu-id="464ee-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
