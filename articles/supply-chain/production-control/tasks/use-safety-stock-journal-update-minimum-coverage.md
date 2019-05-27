---
title: Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu
description: Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571428"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="e0338-103">Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu</span><span class="sxs-lookup"><span data-stu-id="e0338-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0338-104">Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.</span><span class="sxs-lookup"><span data-stu-id="e0338-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="e0338-105">Þetta er gert með því að nota öryggisbirgðabók.</span><span class="sxs-lookup"><span data-stu-id="e0338-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="e0338-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="e0338-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="e0338-107">Þetta verk er ætluð fyrir framleiðslustjóra, sem hjálpar við að viðhalda lágmarks þekju.</span><span class="sxs-lookup"><span data-stu-id="e0338-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="e0338-108">Stofnið nýja heiti öryggisbirgðabókar.</span><span class="sxs-lookup"><span data-stu-id="e0338-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="e0338-109">Fara í Heiti öryggisbirgðabóka</span><span class="sxs-lookup"><span data-stu-id="e0338-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="e0338-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e0338-110">Click New.</span></span>
3. <span data-ttu-id="e0338-111">Í reitinn Heiti skal slá inn "efni".</span><span class="sxs-lookup"><span data-stu-id="e0338-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="e0338-112">Í reitinn Lýsing skal slá inn "Efni".</span><span class="sxs-lookup"><span data-stu-id="e0338-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="e0338-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e0338-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="e0338-114">Stofna öryggisbirgðabók</span><span class="sxs-lookup"><span data-stu-id="e0338-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="e0338-115">Fara í Útreikningur öryggisbirgða</span><span class="sxs-lookup"><span data-stu-id="e0338-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="e0338-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e0338-116">Click New.</span></span>
3. <span data-ttu-id="e0338-117">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="e0338-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="e0338-118">Velja skal nafn öryggisbirgðabókar sem þú stofnaðir, til dæmis, Efni.</span><span class="sxs-lookup"><span data-stu-id="e0338-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="e0338-119">Smellið á Stofna línur .</span><span class="sxs-lookup"><span data-stu-id="e0338-119">Click Create lines.</span></span>
5. <span data-ttu-id="e0338-120">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="e0338-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="e0338-121">Stilla dagsetningu á „02-01-2015“.</span><span class="sxs-lookup"><span data-stu-id="e0338-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="e0338-122">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="e0338-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e0338-123">Stilla dagsetningu á 2015-12-30</span><span class="sxs-lookup"><span data-stu-id="e0338-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="e0338-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e0338-124">Click OK.</span></span>
    * <span data-ttu-id="e0338-125">Þetta stofnar línur fyrir víddir sem hafa birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="e0338-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="e0338-126">Reikna tillögu</span><span class="sxs-lookup"><span data-stu-id="e0338-126">Calculate proposal</span></span>
1. <span data-ttu-id="e0338-127">Smella á Reikna tillögu</span><span class="sxs-lookup"><span data-stu-id="e0338-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="e0338-128">Veldu valkostinn Nota meðaltal úthreyfinga á afhendingartíma.</span><span class="sxs-lookup"><span data-stu-id="e0338-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="e0338-129">Stilla Margfeldisstuðullinn á "10"</span><span class="sxs-lookup"><span data-stu-id="e0338-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="e0338-130">Margföldunarstuðullinn er notaður til að leiðrétta tillöguna.</span><span class="sxs-lookup"><span data-stu-id="e0338-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="e0338-131">Þar sem sýnigögn hefur aðeins nokkrar færslur, þarf að stilla stuðulinn til að fá raunhæfa tillögu.</span><span class="sxs-lookup"><span data-stu-id="e0338-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="e0338-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e0338-132">Click OK.</span></span>
    * <span data-ttu-id="e0338-133">Skruna niður til að finna M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="e0338-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="e0338-134">Skoða dálkinn reiknað lágmarksmagn.</span><span class="sxs-lookup"><span data-stu-id="e0338-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="e0338-135">Uppfæra lágmarksmagn</span><span class="sxs-lookup"><span data-stu-id="e0338-135">Update minimum quantity</span></span>
1. <span data-ttu-id="e0338-136">Í reitinn nýtt lágmarksmagn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="e0338-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="e0338-137">Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu.</span><span class="sxs-lookup"><span data-stu-id="e0338-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="e0338-138">Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.</span><span class="sxs-lookup"><span data-stu-id="e0338-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="e0338-139">T.d. er hægt að færa inn Reiknuð lágmarksmagn á þessu svæði fyrir M0002 sem er með vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="e0338-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="e0338-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e0338-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0338-141">Til dæmis, er hægt að velja M0002 sem er með vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="e0338-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="e0338-142">Í reitinn nýtt lágmarksmagn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="e0338-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="e0338-143">Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu.</span><span class="sxs-lookup"><span data-stu-id="e0338-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="e0338-144">Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.</span><span class="sxs-lookup"><span data-stu-id="e0338-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="e0338-145">Bóka nýtt lágmarksmagn og villuleita niðurstöður</span><span class="sxs-lookup"><span data-stu-id="e0338-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="e0338-146">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="e0338-146">Click Post.</span></span>
2. <span data-ttu-id="e0338-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e0338-147">Click OK.</span></span>
3. <span data-ttu-id="e0338-148">Smellið til að elta tengilinn í reitnum vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="e0338-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="e0338-149">Smellið til að elta tengilinn í reitnum vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="e0338-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="e0338-150">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="e0338-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="e0338-151">Smellt er á vöruþekju.</span><span class="sxs-lookup"><span data-stu-id="e0338-151">Click Item coverage.</span></span>
    * <span data-ttu-id="e0338-152">Athugaðu að Lágmarksmagn hefur verið uppfærður með nýtt lágmarksmagn úr öryggisbirgðabók.</span><span class="sxs-lookup"><span data-stu-id="e0338-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

