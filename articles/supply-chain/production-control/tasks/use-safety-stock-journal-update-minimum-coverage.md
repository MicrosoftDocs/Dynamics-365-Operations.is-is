---
title: Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu
description: Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430563"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="86413-103">Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu</span><span class="sxs-lookup"><span data-stu-id="86413-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86413-104">Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.</span><span class="sxs-lookup"><span data-stu-id="86413-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="86413-105">Þetta er gert með því að nota öryggisbirgðabók.</span><span class="sxs-lookup"><span data-stu-id="86413-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="86413-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="86413-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="86413-107">Þetta verk er ætluð fyrir framleiðslustjóra, sem hjálpar við að viðhalda lágmarks þekju.</span><span class="sxs-lookup"><span data-stu-id="86413-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="86413-108">Stofnið nýja heiti öryggisbirgðabókar.</span><span class="sxs-lookup"><span data-stu-id="86413-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="86413-109">Í **skoðunarrúðunni** ferðu í **Aðaláætlanagerð > Uppsetning > Heiti færslubókar öryggisbirgða**.</span><span class="sxs-lookup"><span data-stu-id="86413-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="86413-110">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="86413-110">Click **New**.</span></span>
3. <span data-ttu-id="86413-111">Í reitinn **Heiti** skal slá inn "efni".</span><span class="sxs-lookup"><span data-stu-id="86413-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="86413-112">Í reitinn **Lýsing** skal slá inn "Efni".</span><span class="sxs-lookup"><span data-stu-id="86413-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="86413-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="86413-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="86413-114">Stofna öryggisbirgðabók</span><span class="sxs-lookup"><span data-stu-id="86413-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="86413-115">Í **skoðunarrúðunni** ferðu í **Aðaláætlanagerð > Aðaláætlanagerð > Keyra > Útreikningur öryggisbirgða**.</span><span class="sxs-lookup"><span data-stu-id="86413-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="86413-116">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="86413-116">Click **New**.</span></span>
3. <span data-ttu-id="86413-117">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="86413-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="86413-118">Velja skal nafn öryggisbirgðabókar sem þú stofnaðir, til dæmis, Efni.</span><span class="sxs-lookup"><span data-stu-id="86413-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="86413-119">Smelltu á **Stofna línur**.</span><span class="sxs-lookup"><span data-stu-id="86413-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="86413-120">Í reitnum **Frá dags.** færirði inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="86413-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="86413-121">Í reitnum **Til dags.** færirðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="86413-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="86413-122">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="86413-122">Click **OK**.</span></span> <span data-ttu-id="86413-123">Þetta stofnar línur fyrir víddir sem hafa birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="86413-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="86413-124">Reikna tillögu</span><span class="sxs-lookup"><span data-stu-id="86413-124">Calculate proposal</span></span>
1. <span data-ttu-id="86413-125">Smelltu á **Reikna tillögu**.</span><span class="sxs-lookup"><span data-stu-id="86413-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="86413-126">Veldu valkostinn **Nota meðaltal úthreyfinga á afhendingartíma**.</span><span class="sxs-lookup"><span data-stu-id="86413-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="86413-127">Stilltu **Margfeldisstuðullinn** á "10".</span><span class="sxs-lookup"><span data-stu-id="86413-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="86413-128">Margföldunarstuðullinn er notaður til að leiðrétta tillöguna.</span><span class="sxs-lookup"><span data-stu-id="86413-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="86413-129">Þar sem sýnigögn hefur aðeins nokkrar færslur, þarf að stilla stuðulinn til að fá raunhæfa tillögu.</span><span class="sxs-lookup"><span data-stu-id="86413-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="86413-130">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="86413-130">Click **OK**.</span></span> <span data-ttu-id="86413-131">Skruna niður til að finna M0002 og M0003.</span><span class="sxs-lookup"><span data-stu-id="86413-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="86413-132">Skoða dálkinn **Reiknað lágmarksmagn**.</span><span class="sxs-lookup"><span data-stu-id="86413-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="86413-133">Uppfæra lágmarksmagn</span><span class="sxs-lookup"><span data-stu-id="86413-133">Update minimum quantity</span></span>
1. <span data-ttu-id="86413-134">Í reitinn **Nýtt lágmarksmagn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="86413-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="86413-135">Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu.</span><span class="sxs-lookup"><span data-stu-id="86413-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="86413-136">Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.</span><span class="sxs-lookup"><span data-stu-id="86413-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="86413-137">T.d. er hægt að færa inn Reiknuð lágmarksmagn á þessu svæði fyrir M0002 sem er með vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="86413-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="86413-138">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="86413-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="86413-139">Til dæmis, er hægt að velja M0002 sem er með vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="86413-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="86413-140">Í reitinn **Nýtt lágmarksmagn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="86413-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="86413-141">Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu.</span><span class="sxs-lookup"><span data-stu-id="86413-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="86413-142">Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.</span><span class="sxs-lookup"><span data-stu-id="86413-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="86413-143">Bóka nýtt lágmarksmagn og villuleita niðurstöður</span><span class="sxs-lookup"><span data-stu-id="86413-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="86413-144">Smelltu á **bóka.**</span><span class="sxs-lookup"><span data-stu-id="86413-144">Click **Post**.</span></span>
2. <span data-ttu-id="86413-145">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="86413-145">Click **OK**.</span></span>
3. <span data-ttu-id="86413-146">Smellið til að fylgja tenglinum í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="86413-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="86413-147">Smellið til að fylgja tenglinum í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="86413-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="86413-148">Í **Aðgerðarrúðunni** er smellt á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="86413-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="86413-149">Smelltu á **Vöruþekju**.</span><span class="sxs-lookup"><span data-stu-id="86413-149">Click **Item coverage**.</span></span> <span data-ttu-id="86413-150">Athugaðu að **Lágmarksmagn** hefur verið uppfært með nýju lágmarksmagni úr öryggisbirgðabók.</span><span class="sxs-lookup"><span data-stu-id="86413-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

