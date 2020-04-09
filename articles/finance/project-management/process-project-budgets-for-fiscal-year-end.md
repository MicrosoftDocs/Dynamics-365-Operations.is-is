---
title: Flytja fjárhagsáætlanir verks við lok fjárhagsárs
description: Þessi grein veitir upplýsingar um hvernig á að flytja fjárhæðir sem eftir eru til komandi ára og búa til upplýsingar um fjárhagsáætlunarskrá.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172331"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="20556-103">Flytja fjárhagsáætlanir verks við lok fjárhagsárs</span><span class="sxs-lookup"><span data-stu-id="20556-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20556-104">Þegar þú vinnur að fjögurra ára verkefni gætirðu haft eftir fjárhagsáætlun í lok reikningsársins.</span><span class="sxs-lookup"><span data-stu-id="20556-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="20556-105">Þú getur flutt eftirstandandi fjárhagsáætlanaupphæðir á ókomið ár og stofnað upplýsingar fjárhagsáætlunarskráar fyrir upphæðir í tengdum fjárhagslyklum.</span><span class="sxs-lookup"><span data-stu-id="20556-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="20556-106">Áður en þú yfirfærir upphæðirnar skaltu fara yfir og greina eftirstandandi upphæðir fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="20556-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="20556-107">Yfirfarið og greinið eftirstandandi fjárhagsáætlunarupphæðir</span><span class="sxs-lookup"><span data-stu-id="20556-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="20556-108">Ljúkið eftirfarandi skrefum til að fara yfir áætlunarupphæðir ársloka fyrir verk en ekki yfirfæra upphæðirnar.</span><span class="sxs-lookup"><span data-stu-id="20556-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="20556-109">Farðu í **Verkefnisstjórnun og bókhald** > **Reglubundin** > **Fjárhagsáætlanir** > **Fjárhagsáætlanir frá fyrra tímabili**.</span><span class="sxs-lookup"><span data-stu-id="20556-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="20556-110">Á síðunni **Yfirfærsluferli verkáætlunar**, á flipanum **Valkostir í árslok**, staðfestirðu að **Yfirfæra eftirstöðvar á upphæð áætlunarverks** sé ekki virkt.</span><span class="sxs-lookup"><span data-stu-id="20556-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="20556-111">Á flipanum **Færibreytur**, í reitnum **Fjárhagsáætlunar verks**, velurðu fjárhagsárið sem þú vilt skoða eftirstandandi upphæð fjárhagsáætlunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="20556-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="20556-112">Í reitnum **Opnunarfjárhagsár** skal velja upphaf fjárhagsárs þar sem skoða á eftirstandandi fjárhagsáætlanaupphæð.</span><span class="sxs-lookup"><span data-stu-id="20556-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="20556-113">Í reitnum **Frá spálíkani** velurðu **Eftirstöðvar fjárhagsáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="20556-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="20556-114">Til að fela í sér verk sem uppfylla valin skilyrði og hafa enga eftirstandandi fjárhagsáætlun, velurðu **Birta eftirstöðvar sem núll**.</span><span class="sxs-lookup"><span data-stu-id="20556-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="20556-115">Á flipanum **Velja fjárhagsáætlanir** velurðu **Sæktu allar fjárhagsáætlanir** til að hlaða öllum fjárhagsáætlunum sem samsvara völdum forsendum og veldu síðan **Ferli**.</span><span class="sxs-lookup"><span data-stu-id="20556-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="20556-116">Til að hanna fyrirspurn gagnagrunns sem hleður tilteknu safni fjárhagsáætlana í gluggann velurðu **Sækja valdar fjárhagsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="20556-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="20556-117">Fyrir frekari upplýsingar um tiltekna línu á glugganum velurðu línuna og síðan **Skoða upplýsingar um fjárhagsáætlun** eða **Skoða reikninga**.</span><span class="sxs-lookup"><span data-stu-id="20556-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="20556-118">Yfirfæra eftirstöðvar upphæðar fjárhagsáætlunar</span><span class="sxs-lookup"><span data-stu-id="20556-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="20556-119">Þegar unnið er með eftirstandandi áætlunarupphæðir er hægt að stofna færslur í fjárhag fyrir upphæðir sem á að yfirfæra.</span><span class="sxs-lookup"><span data-stu-id="20556-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="20556-120">Til að stofna fjárhagsfærslur skal ljúka skrefunum í hlutanum [Yfirfæra fjárhagsáætlunarfjárhæðir og stofna fjárhagsfærslur](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="20556-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="20556-121">Fjárhagsáætlunarupphæðir sem eru yfirfærðar eru fluttar á spárlíkanið sem er valið á síðunni **Spárlíkön** sem spárlíkan yfirfærslu.</span><span class="sxs-lookup"><span data-stu-id="20556-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="20556-122">Yfirfæra fjárhagsáætlunarupphæðir og stofna fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="20556-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="20556-123">Veldu **Verkefnisstjórnun og bókhald** > **Reglubundin** > **Fjárhagsáætlanir** > **Fjárhagsáætlanir frá fyrra tímabili**.</span><span class="sxs-lookup"><span data-stu-id="20556-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="20556-124">Á síðunni **Framlag til verkefnaáætlunar** velurðu **Árslok** og virkjar síðan **Yfirfæra eftirstöðvar á upphæð áætlunarverks** og **Stofna færslur fjárhagsáætlunarskrár í fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="20556-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="20556-125">Á flipanum **Færibreytur**, í reitahópnum **Færibreytur verks** velurðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="20556-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="20556-126">**Fjárhagsáætlunarár verks**: Veldu upphaf fjárhagsárs þar sem skoða á eftirstandandi fjárhagsáætlanaupphæðir.</span><span class="sxs-lookup"><span data-stu-id="20556-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="20556-127">**Hagnaður og tap**: Stofnaðu hagnaðar - og tapsfærslurnar í fjárhag skal velja gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="20556-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="20556-128">**WIP**: Stofna færslur verka í vinnslu (WIP) í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="20556-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="20556-129">**Launaskrá**: Stofna launaskiptingarfærslur í fjárhag skal velja gátreitinn .</span><span class="sxs-lookup"><span data-stu-id="20556-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="20556-130">Í reitahópnum **Fjárhagur** gefurðu upp eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="20556-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="20556-131">Í svæðinu **Opnunarfjárhagsár** skal velja fjárhagsárið sem á að yfirfæra eftirstandandi fjárhagsáætlanaupphæðir á fyrir þessi verk.</span><span class="sxs-lookup"><span data-stu-id="20556-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="20556-132">Sjálfgefið gildi er eitt ár á eftir gildi í reitnum **Fjárhagsáætlunarár verks**.</span><span class="sxs-lookup"><span data-stu-id="20556-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="20556-133">Í reitnum **Yfirfærslutímabil** er valið tímabilið sem stofna á sundurliðun fjárhagsáætlunarskrár fyrir í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="20556-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="20556-134">Þetta er yfirleitt í fyrsta tímabili opnunarfjárhagsárs.</span><span class="sxs-lookup"><span data-stu-id="20556-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="20556-135">Í reitahópnum **Afrita úr/í** gefurðu upp eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="20556-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="20556-136">Í reitnum **Úr spárlíkani** skal velja spárlíkan fjárhagsáætlunar verksins sem tengist eftirstandandi fjárhagsáætlanaupphæðum sem á að yfirfæra fyrir verkin.</span><span class="sxs-lookup"><span data-stu-id="20556-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="20556-137">Í reitnum **Til fjárhagsáætlunarlíkans fjárhags** skal velja fjárhagsáætlunarlíkan verksins sem tengist eftirstandandi fjárhagsáætlanaupphæðum sem á að yfirfæra í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="20556-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="20556-138">Veldu **Flytja sölugjaldmiðil** til að nota sölugjaldmiðil verksins fyrir fjárhagsfærslurnar sem eru stofnaðar með því að flytja fjárhagsáætlunarupphæðir fyrir verk skal velja gátreitinn .</span><span class="sxs-lookup"><span data-stu-id="20556-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="20556-139">Þegar valkosturinn er ekki valinn nota færslurnar bókhaldsgjaldmiðilinn.</span><span class="sxs-lookup"><span data-stu-id="20556-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="20556-140">Veldu **Birta eftirstöðvar sem núll** til að hafa með verk sem hafa engar eftirstandandi áætlunarupphæðir, en sem uppfylla önnur skilyrði sem valin voru í verkunum sem eru sýndar í neðsta glugganum.</span><span class="sxs-lookup"><span data-stu-id="20556-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="20556-141">Á flipanum **Velja fjárhagsáætlanir** velurðu **Sækja allar fjárhagsáætlanir** til að hlaða öllum fjárhagsáætlunum sem samsvara völdum forsendum.</span><span class="sxs-lookup"><span data-stu-id="20556-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="20556-142">Ef þú vilt frekar hanna fyrirspurn gagnagrunns sem hleður tilteknu safni fjárhagsáætlana verks í gluggann velurðu **Sækja valdar fjárhagsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="20556-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="20556-143">Fyrir hvert verk sem á að vinna með skal velja valkostinn í upphafi línunnar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="20556-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="20556-144">Til að velja öll eða flest verk velurðu hakið efst í efra vinstra horninu.</span><span class="sxs-lookup"><span data-stu-id="20556-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="20556-145">Til að útiloka vinnslu á einhverju verki hreinsarðu gátreitinn fyrir það verk.</span><span class="sxs-lookup"><span data-stu-id="20556-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="20556-146">Til að flytja eftirstandandi fjárhagsáætlanaupphæðir fyrir valin verk á valið fjárhagsár og stofna sundurliðun fjárhagsáætlunarskrár í fjárhag velurðu **Ferli**.</span><span class="sxs-lookup"><span data-stu-id="20556-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="20556-147">Yfirfæra fjárhagsáætlunarupphæðir án þess að stofna fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="20556-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="20556-148">Farðu í **Verkefnisstjórnun og bókhald** > **Reglubundin** > **Fjárhagsáætlanir** > **Fjárhagsáætlanir frá fyrra tímabili**.</span><span class="sxs-lookup"><span data-stu-id="20556-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="20556-149">Á síðunni **Yfirfærsluferli verkáætlunar**, í reitnum **Valkostir í árslok**, velurðu **Yfirfæra eftirstöðvar á upphæð áætlunarverks**.</span><span class="sxs-lookup"><span data-stu-id="20556-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="20556-150">Í hópnum **Færibreytur**, í reitnum **Fjárhagsáætlunar verks**, velurðu fjárhagsárið sem þú vilt skoða eftirstandandi upphæðir fjárhagsáætlunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="20556-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="20556-151">Í hópnum **Afrita úr/í** gefurðu upp eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="20556-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="20556-152">Í reitnum **Úr spárlíkani** skal velja spárlíkan fjárhagsáætlunar verksins sem tengist eftirstandandi fjárhagsáætlanaupphæðum sem á að yfirfæra fyrir verkin.</span><span class="sxs-lookup"><span data-stu-id="20556-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="20556-153">Veldu **Birta eftirstöðvar sem núll** til að fela í sér verk sem hafa engar eftirstandandi upphæðir fjárhagsáætlunar sem uppfylla hin skilyrðin sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="20556-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="20556-154">Í hópnum **Velja fjárhagsáætlanir** velurðu **Sækja allar fjárhagsáætlanir** til að hlaða öllum fjárhagsáætlunum sem samsvara völdum forsendum.</span><span class="sxs-lookup"><span data-stu-id="20556-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="20556-155">Til að hanna fyrirspurn gagnagrunns sem hleður tilteknu safni fjárhagsáætlana verks í gluggann velurðu **Sækja valdar fjárhagsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="20556-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="20556-156">Fyrir hvert verk sem á að vinna með skal velja valkostinn í upphafi línunnar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="20556-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="20556-157">Veldu **Ferli** til að flytja eftirstandandi fjárhagsáætlanaupphæðir fyrir valin verk á valið fjárhagsár.</span><span class="sxs-lookup"><span data-stu-id="20556-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

