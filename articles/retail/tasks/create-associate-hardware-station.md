---
title: " Búa til og tengja vélbúnaðarstöð"
description: Þetta ferli fer í gegnum hvernig á að stofna nýja vébúnaðarstöð
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80df4fa663d208e28f5c9b031b6610d29286171c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548394"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="ebfb7-103"> Búa til og tengja vélbúnaðarstöð</span><span class="sxs-lookup"><span data-stu-id="ebfb7-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ebfb7-104">Þetta ferli fer í gegnum hvernig á að stofna nýja vébúnaðarstöð</span><span class="sxs-lookup"><span data-stu-id="ebfb7-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="ebfb7-105">Ný forstilling vélbúnaðar verður stofnuð og notuð til að bæta nýjum vélbúnaðarstöðvar við fyrirfram skilgreindu verslunar (rás).</span><span class="sxs-lookup"><span data-stu-id="ebfb7-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="ebfb7-106">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ebfb7-107">Fara í Grunnþættir viðskipta > Rásir > ..</span><span class="sxs-lookup"><span data-stu-id="ebfb7-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="ebfb7-108">> ..</span><span class="sxs-lookup"><span data-stu-id="ebfb7-108">> ..</span></span> <span data-ttu-id="ebfb7-109">> ..</span><span class="sxs-lookup"><span data-stu-id="ebfb7-109">> ..</span></span> <span data-ttu-id="ebfb7-110">> Forstillingar vélbúnaðarstöðvar.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="ebfb7-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-111">Click New.</span></span>
3. <span data-ttu-id="ebfb7-112">Í reitnum Kenni vélbúnaðarstöðvar færðu inn 'TestHWProfile'.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="ebfb7-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ebfb7-114">Í reitinn númer tengis skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="ebfb7-115">Í reitnum forstilling vélbúnaðar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ebfb7-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ebfb7-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ebfb7-118">Í reitnum Heiti pakka skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ebfb7-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ebfb7-120">Þetta er stöðluð pakka sem er fengin með nýju umhverfi.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="ebfb7-121">Útgáfunúmer getur verið mismunandi.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-121">The version number may vary.</span></span>  
11. <span data-ttu-id="ebfb7-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-122">Click Save.</span></span>
12. <span data-ttu-id="ebfb7-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-123">Close the page.</span></span>
13. <span data-ttu-id="ebfb7-124">Fara í Smásölu og viðskipti > rásir > allar smásöluverslanir.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="ebfb7-125">Í listanum skal velja línu 17.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="ebfb7-126">Ef verið er að nota sýnigögn fyrirtækisins USRT, þá er þetta Houston verslun.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="ebfb7-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ebfb7-128">Víxla útvíkkun á liðnum vélbúnaðarstöð.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="ebfb7-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-129">Click Add.</span></span>
18. <span data-ttu-id="ebfb7-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="ebfb7-131">Í reitnum forstilling kennis skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="ebfb7-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ebfb7-133">Þetta hlýtur að vera ný forstilling vélbúnaðarstöðvar sem var stofnuð í fyrri skrefum.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="ebfb7-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="ebfb7-135">Í reitinn Heiti móðurtölvu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="ebfb7-136">Í reitnum kenni EFT afgreiðslustöðvar, færðu inn gildi</span><span class="sxs-lookup"><span data-stu-id="ebfb7-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="ebfb7-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ebfb7-137">Click Save.</span></span>

