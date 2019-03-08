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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "341098"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="257b5-103">Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu</span><span class="sxs-lookup"><span data-stu-id="257b5-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="257b5-104">Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.</span><span class="sxs-lookup"><span data-stu-id="257b5-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="257b5-105">Þetta er gert með því að nota öryggisbirgðabók.</span><span class="sxs-lookup"><span data-stu-id="257b5-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="257b5-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="257b5-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="257b5-107">Þetta verk er ætluð fyrir framleiðslustjóra, sem hjálpar við að viðhalda lágmarks þekju.</span><span class="sxs-lookup"><span data-stu-id="257b5-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="257b5-108">Stofnið nýja heiti öryggisbirgðabókar.</span><span class="sxs-lookup"><span data-stu-id="257b5-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="257b5-109">Fara í Heiti öryggisbirgðabóka</span><span class="sxs-lookup"><span data-stu-id="257b5-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="257b5-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="257b5-110">Click New.</span></span>
3. <span data-ttu-id="257b5-111">Í reitinn Heiti skal slá inn "efni".</span><span class="sxs-lookup"><span data-stu-id="257b5-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="257b5-112">Í reitinn Lýsing skal slá inn "Efni".</span><span class="sxs-lookup"><span data-stu-id="257b5-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="257b5-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="257b5-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="257b5-114">Stofna öryggisbirgðabók</span><span class="sxs-lookup"><span data-stu-id="257b5-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="257b5-115">Fara í Útreikningur öryggisbirgða</span><span class="sxs-lookup"><span data-stu-id="257b5-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="257b5-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="257b5-116">Click New.</span></span>
3. <span data-ttu-id="257b5-117">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="257b5-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="257b5-118">Velja skal nafn öryggisbirgðabókar sem þú stofnaðir, til dæmis, Efni.</span><span class="sxs-lookup"><span data-stu-id="257b5-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="257b5-119">Smellið á Stofna línur .</span><span class="sxs-lookup"><span data-stu-id="257b5-119">Click Create lines.</span></span>
5. <span data-ttu-id="257b5-120">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="257b5-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="257b5-121">Stilla dagsetningu á „02-01-2015“.</span><span class="sxs-lookup"><span data-stu-id="257b5-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="257b5-122">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="257b5-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="257b5-123">Stilla dagsetningu á 2015-12-30</span><span class="sxs-lookup"><span data-stu-id="257b5-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="257b5-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="257b5-124">Click OK.</span></span>
    * <span data-ttu-id="257b5-125">Þetta stofnar línur fyrir víddir sem hafa birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="257b5-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="257b5-126">Reikna tillögu</span><span class="sxs-lookup"><span data-stu-id="257b5-126">Calculate proposal</span></span>
1. <span data-ttu-id="257b5-127">Smella á Reikna tillögu</span><span class="sxs-lookup"><span data-stu-id="257b5-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="257b5-128">Veldu valkostinn Nota meðaltal úthreyfinga á afhendingartíma.</span><span class="sxs-lookup"><span data-stu-id="257b5-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="257b5-129">Stilla Margfeldisstuðullinn á "10"</span><span class="sxs-lookup"><span data-stu-id="257b5-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="257b5-130">Margföldunarstuðullinn er notaður til að leiðrétta tillöguna.</span><span class="sxs-lookup"><span data-stu-id="257b5-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="257b5-131">Þar sem sýnigögn hefur aðeins nokkrar færslur, þarf að stilla stuðulinn til að fá raunhæfa tillögu.</span><span class="sxs-lookup"><span data-stu-id="257b5-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="257b5-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="257b5-132">Click OK.</span></span>
    * <span data-ttu-id="257b5-133">Skruna niður til að finna M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="257b5-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="257b5-134">Skoða dálkinn reiknað lágmarksmagn.</span><span class="sxs-lookup"><span data-stu-id="257b5-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="257b5-135">Uppfæra lágmarksmagn</span><span class="sxs-lookup"><span data-stu-id="257b5-135">Update minimum quantity</span></span>
1. <span data-ttu-id="257b5-136">Í reitinn nýtt lágmarksmagn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="257b5-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="257b5-137">Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu.</span><span class="sxs-lookup"><span data-stu-id="257b5-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="257b5-138">Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.</span><span class="sxs-lookup"><span data-stu-id="257b5-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="257b5-139">T.d. er hægt að færa inn Reiknuð lágmarksmagn á þessu svæði fyrir M0002 sem er með vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="257b5-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="257b5-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="257b5-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="257b5-141">Til dæmis, er hægt að velja M0002 sem er með vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="257b5-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="257b5-142">Í reitinn nýtt lágmarksmagn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="257b5-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="257b5-143">Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu.</span><span class="sxs-lookup"><span data-stu-id="257b5-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="257b5-144">Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.</span><span class="sxs-lookup"><span data-stu-id="257b5-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="257b5-145">Bóka nýtt lágmarksmagn og villuleita niðurstöður</span><span class="sxs-lookup"><span data-stu-id="257b5-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="257b5-146">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="257b5-146">Click Post.</span></span>
2. <span data-ttu-id="257b5-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="257b5-147">Click OK.</span></span>
3. <span data-ttu-id="257b5-148">Smellið til að elta tengilinn í reitnum vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="257b5-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="257b5-149">Smellið til að elta tengilinn í reitnum vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="257b5-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="257b5-150">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="257b5-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="257b5-151">Smellt er á vöruþekju.</span><span class="sxs-lookup"><span data-stu-id="257b5-151">Click Item coverage.</span></span>
    * <span data-ttu-id="257b5-152">Athugaðu að Lágmarksmagn hefur verið uppfærður með nýtt lágmarksmagn úr öryggisbirgðabók.</span><span class="sxs-lookup"><span data-stu-id="257b5-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

