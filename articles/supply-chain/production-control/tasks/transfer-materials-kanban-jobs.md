---
title: Flytja efni innan kanban-vinnsla
description: Þetta ferli leggur áherslu á keyrslu kanban-afturköllunarvinnslu til að flytja efni.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8808b168d2b3845b315e6bbcfb376e37f31fe4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981032"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="28ccf-103">Flytja efni innan kanban-vinnsla</span><span class="sxs-lookup"><span data-stu-id="28ccf-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28ccf-104">Þetta ferli leggur áherslu á keyrslu kanban-afturköllunarvinnslu til að flytja efni.</span><span class="sxs-lookup"><span data-stu-id="28ccf-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="28ccf-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="28ccf-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="28ccf-106">Þetta ferli er ætluð fyrir starfsmaður í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="28ccf-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="28ccf-107">Birta flutningsvinnslur</span><span class="sxs-lookup"><span data-stu-id="28ccf-107">Display transfer jobs</span></span>
1. <span data-ttu-id="28ccf-108">Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir flutningsvinnslur.</span><span class="sxs-lookup"><span data-stu-id="28ccf-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="28ccf-109">Útvíkka eða draga saman hlutann Síur.</span><span class="sxs-lookup"><span data-stu-id="28ccf-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="28ccf-110">Í hlutanum Síur hægt er að tilgreina hvaða vinnslur sem óskað er að finna með því að sía á framleiðsluflæði, verkþáttarheitið, Úr vöruhús og staðsetning, og Til vöruhúss og staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="28ccf-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="28ccf-111">Færðu inn "11" í svæðið Úr vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="28ccf-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="28ccf-112">Í svæðinu Til staðsetningar, færið inn '12'.</span><span class="sxs-lookup"><span data-stu-id="28ccf-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="28ccf-113">Hefja flutningsvinnslu</span><span class="sxs-lookup"><span data-stu-id="28ccf-113">Start a transfer job</span></span>
1. <span data-ttu-id="28ccf-114">Á listanum afvelja valinni línu - ef einhver.</span><span class="sxs-lookup"><span data-stu-id="28ccf-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="28ccf-115">Í listanum skal velja línu 4.</span><span class="sxs-lookup"><span data-stu-id="28ccf-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="28ccf-116">Veljið fyrsta vinnslan með stöðuna Ekki áætlaðar.</span><span class="sxs-lookup"><span data-stu-id="28ccf-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="28ccf-117">Gangið úr skugga um að þetta er eina valda verkið.</span><span class="sxs-lookup"><span data-stu-id="28ccf-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="28ccf-118">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="28ccf-118">Click Start.</span></span>
    * <span data-ttu-id="28ccf-119">Athugið að tákn tilgreinir vinnslan er nú hafin.</span><span class="sxs-lookup"><span data-stu-id="28ccf-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="28ccf-120">Veljið seinni flutningsvinnslu og magni</span><span class="sxs-lookup"><span data-stu-id="28ccf-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="28ccf-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="28ccf-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28ccf-122">Hægt er að hafa margar vinnslur valdar en núna skal bara velja línu 5.</span><span class="sxs-lookup"><span data-stu-id="28ccf-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="28ccf-123">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="28ccf-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28ccf-124">Gangið úr skugga um að vinnslu í fyrra skrefi er sú eina sem er valin.</span><span class="sxs-lookup"><span data-stu-id="28ccf-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="28ccf-125">Afvelja öllum öðrum vinnslum.</span><span class="sxs-lookup"><span data-stu-id="28ccf-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="28ccf-126">Takið niður gildið í reitnum verkmagn til síðari tilvísunar</span><span class="sxs-lookup"><span data-stu-id="28ccf-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="28ccf-127">Stilla verkmagn á '30'.</span><span class="sxs-lookup"><span data-stu-id="28ccf-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="28ccf-128">Athugið viðvörunarboðin!</span><span class="sxs-lookup"><span data-stu-id="28ccf-128">Notice the warning!</span></span> <span data-ttu-id="28ccf-129">Ekki er leyfilegt að flytja 30.</span><span class="sxs-lookup"><span data-stu-id="28ccf-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="28ccf-130">Samkvæmt uppsetningu kanban-reglan er aðeins hægt að flytja upphaflegt magn.</span><span class="sxs-lookup"><span data-stu-id="28ccf-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="28ccf-131">Notið gildið sem tekið var niður í reitnum verkmagn</span><span class="sxs-lookup"><span data-stu-id="28ccf-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="28ccf-132">Stilla magn Vinnslu í fyrra gildið.</span><span class="sxs-lookup"><span data-stu-id="28ccf-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="28ccf-133">Hefja seinni flutningsvinnslu</span><span class="sxs-lookup"><span data-stu-id="28ccf-133">Start the second transfer job</span></span>
1. <span data-ttu-id="28ccf-134">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="28ccf-134">Click Start.</span></span>
    * <span data-ttu-id="28ccf-135">Þetta hefur flutning vinnslu í línu 5.</span><span class="sxs-lookup"><span data-stu-id="28ccf-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="28ccf-136">Ljúka bæði flutningsvinnslur</span><span class="sxs-lookup"><span data-stu-id="28ccf-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="28ccf-137">Í listanum skal velja línu 4.</span><span class="sxs-lookup"><span data-stu-id="28ccf-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="28ccf-138">Nú tvær flutningsvinnslur valdar á röð 4 og 5 línu.</span><span class="sxs-lookup"><span data-stu-id="28ccf-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="28ccf-139">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="28ccf-139">Click Complete.</span></span>
    * <span data-ttu-id="28ccf-140">Þetta lýkur við flutning á bæði vinnslur.</span><span class="sxs-lookup"><span data-stu-id="28ccf-140">This will complete the transfer of both jobs.</span></span>  

