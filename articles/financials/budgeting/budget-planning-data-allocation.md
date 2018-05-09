---
title: "Úthlutunargögn fjárhagsáætlunargerðar"
description: "Þessi grein lýsir mismunandi úthlutunaraðferðum sem eru tiltækar í Microsoft Dynamics 365 for Finance and Operations og hvernig hægt er að nota þær."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 20dd11ad8b632de279855c1641f7bdeddb33cb4b
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="698f2-103">Gagnaúthlutun fjárhagsáætlunargerðar</span><span class="sxs-lookup"><span data-stu-id="698f2-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="698f2-104">Þessi grein lýsir mismunandi úthlutunaraðferðum sem eru tiltækar í Microsoft Dynamics 365 for Finance and Operations og hvernig hægt er að nota þær.</span><span class="sxs-lookup"><span data-stu-id="698f2-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations and how they can be used.</span></span>  

<span data-ttu-id="698f2-105">Hægt er að dreifa gögnum í fjárhagsáætlun á ýmsa vegu til að sýna nákvæmlega áætlaðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="698f2-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="698f2-106">Úthlutunarreglur</span><span class="sxs-lookup"><span data-stu-id="698f2-106">Allocation methods</span></span>
<span data-ttu-id="698f2-107">Hægt er að nota þrjár úthlutunaraðferðir (Úthlutun yfir mörg tímabil, Úthlutun á víddir og Nota úthlutunarreglur höfuðbókar) til að stofna línur fjárhagsáætlunargerðar sem byggja á línum í sömu fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="698f2-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="698f2-108">Þrjár aðrar aðferðir (uppsöfnun, dreifing og afrita úr fjárhagsáætlunargerð) er hægt að nota til að stofna línur fjárhagsáætlunargerðar í öðrum fjárhagsáætlunum.</span><span class="sxs-lookup"><span data-stu-id="698f2-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="698f2-109">Fyrir allar sex úthlutunaraðferðirnar þarf að tilgreina aðstæður endastaðar.</span><span class="sxs-lookup"><span data-stu-id="698f2-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="698f2-110">Aðstæður endastaðar geta verið annað hvort sama og upprunaaðstæður eða frábrugðnar upprunaaðstæðum.</span><span class="sxs-lookup"><span data-stu-id="698f2-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="698f2-111">Þar að auki er hægt að tilgreina hvort nýjum línum er skeytt við fjárhagsáætlunargerðina eða gildandi línum skipt út fyrir nýjar línur í fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="698f2-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="698f2-112">[![ÚthlutunYfirMörgTímabil](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Úthlutun yfir mörg tímabil** – flokkur fyrir tímabilsúthlutun er notaður til að úthluta fjárhagsáætlunarlínum úr uppruna fjárhagsáætlunargerðarinnar yfir mörg tímabil í aðstæðum endastaðar.</span><span class="sxs-lookup"><span data-stu-id="698f2-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="698f2-113">Upprunaupphæð er úthlutað á margar línur í aðstæðum endastaðar, byggt á prósentu og dagsetningu sem eru skilgreindar í flokknum tímabilsúthlutun.</span><span class="sxs-lookup"><span data-stu-id="698f2-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="698f2-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Úthlutun á víddir** – línum fjárhagsáætlunargerðarinnar er úthlutað úr  upprunalegri fjárhagsáætlunargerð sem ein eða fleiri línur í aðstæðum endastaðar, byggt á prósentu og fjárhagslegum víddum sem eru skilgreind í heiti fjárhagsúthlutunar.</span><span class="sxs-lookup"><span data-stu-id="698f2-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="698f2-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Uppsöfnun** – Línur fjárhagsáætlunar eru lagðar saman úr upprunalegri fjárhagsáætlunargerð í undirfjárhagsáætlun á endastað í yfirfjárhagsáætluninni.</span><span class="sxs-lookup"><span data-stu-id="698f2-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="698f2-116">Þessi aðferð gerir kleift að sameina á hærra stigi fjárhagsáætlunarupphæðir sem eru teknar saman á neðri stigum í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="698f2-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="698f2-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Dreifing** – Línum fjárhagsáætlunar er dreift úr upprunalegri fjárhagsáætlunargerð í aðalfjárhagsáætluninni yfir í undirfjárhagsáætlunargerðir, byggt á fjárhagsvíddum í skipulagseiningum tengra áætlana.</span><span class="sxs-lookup"><span data-stu-id="698f2-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="698f2-118">Þessi aðferð gerir kleift að sýna áætlunarupphæðir á lægri stigum í fyrirtækingu sem eru teknar saman á hærri stigum í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="698f2-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="698f2-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Nota úthlutunarreglur fjárhags** – Línum fjárhagsáætlunar er dreift er úr upprunalegri fjárhagsáætlunargerð til endastaðar, byggt á þeirri úthlutunarreglu höfuðbókar sem er valin. úthlutunarreglna höfuðbókar</span><span class="sxs-lookup"><span data-stu-id="698f2-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="698f2-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Afrita af fjárhagsáætlun** – Eins og í dreifingarúthlutunaraðferð eru línur fjárhagsáætlunargerðar stofnaðar í ákvörðunarstað, byggð á línum í tengdri fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="698f2-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="698f2-121">Hins vegar með þessari aðferð, þarf upprunalega fjárhagsáætlunargerðarin ekki að vera aðalfjárhagsáætlun en getur verið á hærra stigi í stigveldi fjárhagsáætlunargerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="698f2-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="698f2-122">Úthlutunaraðferð þessi er gagnleg ef sameinaðar upphæðir eru upphaflega úr fjárhagsáætlunum á mun efri stigum og þarf að flytja á neðri stig fyrirtækisins til  nákvæmrar yfirferðar og leiðréttingar áður en þær geta fengið samþykki efri stiga.</span><span class="sxs-lookup"><span data-stu-id="698f2-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="698f2-123">Að nota úthlutunaraðferðir í fjárhagsáætlunargerð</span><span class="sxs-lookup"><span data-stu-id="698f2-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="698f2-124">Til að framkvæma úthlutanir á fjárhagsáætlunarsíðunni skal velja línur til að úthluta og smellið síðan á **Úthlutun fjárhagsáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="698f2-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="698f2-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="698f2-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="698f2-126">Næst skal velja úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="698f2-126">Next, select an allocation method.</span></span> <span data-ttu-id="698f2-127">Svæðin sem eftir eru eru síðan stillt samkvæmt aðferðinni sem var valin.</span><span class="sxs-lookup"><span data-stu-id="698f2-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="698f2-128">Þessi svæði fela meðal annars í sér uppruna og áfangastað fjárhagsáætlunargagna og valkost sem gerir kleift að margfalda uppruna með tilgreindum stuðli þegar upphæðir áfangastaðar eru stofnaðar til að einfalda fjöldaafritunar leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="698f2-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="698f2-129">Einnig er hægt að stilla valkostinn **skeyta við áætlun**.</span><span class="sxs-lookup"><span data-stu-id="698f2-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="698f2-130">Velja **Nei** til að skipta út fyrirliggjandi línum fjárhagsáætlunargerðarinnar, eða veljið **Já** að varðveita fyrirliggjandi línur fjárhagsáætlunargerðar og bæta við nýjum línum fyrir úthlutaðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="698f2-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="698f2-131">Að gera sjálfvirkar úthlutanir við verkflæði</span><span class="sxs-lookup"><span data-stu-id="698f2-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="698f2-132">Ein öflug aðgerð gerir kleift að framkvæma úthlutanir sjálfkrafa sem hluta af verkflæði fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="698f2-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="698f2-133">Eftir því sem fjárhagsáætlunargerð fer í gegnum sitt verkflæði geta sjálfvirk verk framkallað úthlutun á tilgreindu stigi fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="698f2-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="698f2-134">Til að setja upp sjálfvirka úthlutun, verður fyrst að stofna úthlutunaráætlun á síðunni **stillingar fjárhagsáætlunargerðar**.</span><span class="sxs-lookup"><span data-stu-id="698f2-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="698f2-135">Úthlutunaráætlunin skilgreinir úthlutunaraðferð sem á að nota þegar sjálfvirk úthlutun er keyrð og gildi fyrir mismunandi úthlutunarvalkosti (sjá fyrri hluta varðandi lýsingar).</span><span class="sxs-lookup"><span data-stu-id="698f2-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="698f2-136">Næst er stig úthlutunar stofnað á síðunni **skilgreining fjárhagsáætlunargerðar**.</span><span class="sxs-lookup"><span data-stu-id="698f2-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="698f2-137">Stig úthlutunar tengir úthlutunaráætlun við verkflæði og stig fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="698f2-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="698f2-138">Loks er bætt við sjálfvirku verki fyrir stigsúthlutun fjárhagsáætlunargerðar á æskilegu verkflæðistigi.</span><span class="sxs-lookup"><span data-stu-id="698f2-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="698f2-139">Í eftirfarandi dæmi hafa tvær stigsúthlutanir fjárhagsáætlunargerðar (rauðmerktar) verið færðar inn í verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="698f2-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="698f2-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="698f2-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




