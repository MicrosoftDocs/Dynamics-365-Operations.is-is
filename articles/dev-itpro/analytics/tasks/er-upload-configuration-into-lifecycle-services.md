--- 
title: "Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) og hlaða upp í Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d24679a380ec824fe08c56aacb4bc348ff40440a
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="64206-103">Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="64206-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64206-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) og hlaða upp í Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="64206-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="64206-105">Í þessu dæmi, verður að stofna skilgreiningu og hlaða henni upp í LCS fyrir sýnifyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="64206-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="64206-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="64206-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="64206-107">Aðgangur að LCS er einnig nauðsynlegur til að ljúka þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="64206-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="64206-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="64206-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="64206-109">Velja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="64206-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="64206-110">og stillið sem virka.</span><span class="sxs-lookup"><span data-stu-id="64206-110">and set it as active.</span></span>
3. <span data-ttu-id="64206-111">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="64206-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="64206-112">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="64206-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="64206-113">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="64206-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="64206-114">Stofna verður skilgreiningu sem inniheldur dæmi um gagnalíkan fyrir rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="64206-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="64206-115">Skilgreining gagnalíkans verður hlaðið upp í LCS síðar.</span><span class="sxs-lookup"><span data-stu-id="64206-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="64206-116">Í svæðið Heiti, Færðu inn 'dæmi um skilgreining líkans '.</span><span class="sxs-lookup"><span data-stu-id="64206-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="64206-117">Dæmi um líkanaskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="64206-117">Sample model configuration</span></span>  
3. <span data-ttu-id="64206-118">Í svæðið lýsing, Færðu inn 'dæmi um skilgreining líkans '.</span><span class="sxs-lookup"><span data-stu-id="64206-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="64206-119">Dæmi um líkanaskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="64206-119">Sample model configuration</span></span>  
4. <span data-ttu-id="64206-120">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="64206-120">Click Create configuration.</span></span>
5. <span data-ttu-id="64206-121">Smellt er á hönnuður Líkana.</span><span class="sxs-lookup"><span data-stu-id="64206-121">Click Model designer.</span></span>
6. <span data-ttu-id="64206-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="64206-122">Click New.</span></span>
7. <span data-ttu-id="64206-123">Í reitnum Heiti skal færa inn 'aðgangsstaður'.</span><span class="sxs-lookup"><span data-stu-id="64206-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="64206-124">Aðgangsstaður</span><span class="sxs-lookup"><span data-stu-id="64206-124">Entry point</span></span>  
8. <span data-ttu-id="64206-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="64206-125">Click Add.</span></span>
9. <span data-ttu-id="64206-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="64206-126">Click Save.</span></span>
10. <span data-ttu-id="64206-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64206-127">Close the page.</span></span>
11. <span data-ttu-id="64206-128">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="64206-128">Click Change status.</span></span>
12. <span data-ttu-id="64206-129">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="64206-129">Click Complete.</span></span>
13. <span data-ttu-id="64206-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64206-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="64206-131">Skrá nýjan gagnasafn</span><span class="sxs-lookup"><span data-stu-id="64206-131">Register a new  repository</span></span>
1. <span data-ttu-id="64206-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64206-132">Close the page.</span></span>
2. <span data-ttu-id="64206-133">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="64206-133">Click Repositories.</span></span>
    * <span data-ttu-id="64206-134">Þannig er hægt að opna lista yfir gagnasöfn fyrir Litware, Inc. skilgreiningaveituna.</span><span class="sxs-lookup"><span data-stu-id="64206-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="64206-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64206-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="64206-136">Þannig er hægt að bæta við nýjum gagnasafni.</span><span class="sxs-lookup"><span data-stu-id="64206-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="64206-137">Í reitnum gerð gagnasafns fyrir skilgreiningar, veljið LCS.</span><span class="sxs-lookup"><span data-stu-id="64206-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="64206-138">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="64206-138">Click Create repository.</span></span>
6. <span data-ttu-id="64206-139">Færa inn eða veljið gildi í svæðinu verk.</span><span class="sxs-lookup"><span data-stu-id="64206-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="64206-140">Veljið viðeigandi LCS-verk.</span><span class="sxs-lookup"><span data-stu-id="64206-140">Select the desired LCS project.</span></span> <span data-ttu-id="64206-141">Þú verður að hafa aðgang að verkinu.</span><span class="sxs-lookup"><span data-stu-id="64206-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="64206-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64206-142">Click OK.</span></span>
    * <span data-ttu-id="64206-143">Ljúka við nýja færslu í gagnasafni.</span><span class="sxs-lookup"><span data-stu-id="64206-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="64206-144">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="64206-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="64206-145">Velja LCS-færslu gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="64206-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="64206-146">Athugið að skráð gagnasafn er merkt eftir núverandi veitu þ.e.a.s aðeins skilgreiningar í eigu þeirrar veitu er hægt að setja í þetta gagnasafn, þar af leiðandi hlaðið upp í valið LCS-verk.</span><span class="sxs-lookup"><span data-stu-id="64206-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="64206-147">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="64206-147">Click Open.</span></span>
    * <span data-ttu-id="64206-148">Opna gagnasafn til að skoða lista yfir skilgreiningar Rafræn skýrslugerð .</span><span class="sxs-lookup"><span data-stu-id="64206-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="64206-149">Það verður auður ef þetta verk hefur ekki enn verið notað fyrir samnýtingu skilgreininga fyrir Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="64206-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="64206-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64206-150">Close the page.</span></span>
11. <span data-ttu-id="64206-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64206-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="64206-152">Hlaða skilgreiningu í LCS</span><span class="sxs-lookup"><span data-stu-id="64206-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="64206-153">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="64206-153">Click Configurations.</span></span>
2. <span data-ttu-id="64206-154">Veljið 'dæmi um skilgreiningu líkans', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64206-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="64206-155">Velja stofnaða skilgreiningu sem þegar hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="64206-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="64206-156">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="64206-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="64206-157">Veljið útgáfu valinnar skilgreiningar með stöðuna "Lokið".</span><span class="sxs-lookup"><span data-stu-id="64206-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="64206-158">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="64206-158">Click Change status.</span></span>
5. <span data-ttu-id="64206-159">Smellt er á samnýta.</span><span class="sxs-lookup"><span data-stu-id="64206-159">Click Share.</span></span>
    * <span data-ttu-id="64206-160">Staða Skilgreiningar breytist úr "Lokið" til 'Samnýttar' þegar hún er birt á LCS.</span><span class="sxs-lookup"><span data-stu-id="64206-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="64206-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64206-161">Click OK.</span></span>
7. <span data-ttu-id="64206-162">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="64206-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="64206-163">Veldu Útgáfa skilgreiningar stöðuna samnýtt.</span><span class="sxs-lookup"><span data-stu-id="64206-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="64206-164">Athugið að staða valda útgáfu hefur breyst úr "Lokið" í 'Samnýttar'.</span><span class="sxs-lookup"><span data-stu-id="64206-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="64206-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64206-165">Close the page.</span></span>
9. <span data-ttu-id="64206-166">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="64206-166">Click Repositories.</span></span>
    * <span data-ttu-id="64206-167">Þannig er hægt að opna lista yfir gagnasöfn fyrir Litware, Inc. skilgreiningaveituna.</span><span class="sxs-lookup"><span data-stu-id="64206-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="64206-168">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="64206-168">Click Open.</span></span>
    * <span data-ttu-id="64206-169">Velja lcs-gagnasafn og opna hana.</span><span class="sxs-lookup"><span data-stu-id="64206-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="64206-170">Athugið að valin skilgreining er sýnd sem eign valins LCS verks.</span><span class="sxs-lookup"><span data-stu-id="64206-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="64206-171">Opna LCS með https://lcs.dynamics.com. Opna verkið sem var notuð áður til skráningar gagnasafns, opna 'eignasafni' þessa verks og útvíkka innihald eignagerðarinnar 'GER skilgreining' – upphlaðin skilgreining Rafrænnar skýrslugerðar verða tiltæk.</span><span class="sxs-lookup"><span data-stu-id="64206-171">Open LCS using https://lcs.dynamics.com. Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="64206-172">Athugaðu að upphalaðri LCS skilgreiningu er hægt að flytja inn í annað tilvik af Microsoft Dynamics Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ef veiturnar hafa aðgang að þessu LCS verkinu.</span><span class="sxs-lookup"><span data-stu-id="64206-172">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  


