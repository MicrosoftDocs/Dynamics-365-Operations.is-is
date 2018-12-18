---
title: "Búa til verkflæði"
description: "Þetta efnisatriði útskýrir hvernig á að stofna verkflæði."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 7d4a3c5e12b226a7d801d8db9abcbd15738c1ce0
ms.contentlocale: is-is
ms.lasthandoff: 12/18/2018

---

# <a name="create-workflows"></a><span data-ttu-id="62d11-103">Búa til verkflæði</span><span class="sxs-lookup"><span data-stu-id="62d11-103">Create workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62d11-104">Þetta efnisatriði útskýrir hvernig á að stofna verkflæði.</span><span class="sxs-lookup"><span data-stu-id="62d11-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="62d11-105">Opnaðu ritstjóra verkflæðis</span><span class="sxs-lookup"><span data-stu-id="62d11-105">Open the workflow editor</span></span>

<span data-ttu-id="62d11-106">Einingin Microsoft Dynamics 365 for Finance and Operations sem þú ert að vinna í ákvarðar tegundir verkflæðis sem þú getur búið til.</span><span class="sxs-lookup"><span data-stu-id="62d11-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="62d11-107">Fylgið eftirfarandi skrefum til að velja gerð verkflæðis til að stofna og til að opna verkflæðisritill.</span><span class="sxs-lookup"><span data-stu-id="62d11-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="62d11-108">Fara í einingunni sem á að stofna nýtt verkflæði fyrir.</span><span class="sxs-lookup"><span data-stu-id="62d11-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="62d11-109">Til dæmis til að stofna verkflæði fyrir innkaupabeiðnir, smellið á **innkaup og aðföng**.</span><span class="sxs-lookup"><span data-stu-id="62d11-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="62d11-110">Smellið á **Uppsetning** &gt; **\[heiti Einingarinnar\] verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="62d11-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="62d11-111">Á listasíðu sem birtist, á Aðgerðasvæðinu skal smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="62d11-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="62d11-112">Á **Stofna verkflæði** síðunni, veljið þá tegund verkflæðis sem á að stofna og smellið svo á **Stofna verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="62d11-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="62d11-113">Verkflæðisritill birtist</span><span class="sxs-lookup"><span data-stu-id="62d11-113">The workflow editor appears.</span></span> <span data-ttu-id="62d11-114">Þú getur nú notað eftirfarandi ferli til að hanna verkflæði.</span><span class="sxs-lookup"><span data-stu-id="62d11-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="62d11-115">Draga verkflæðisþætti yfir á striga</span><span class="sxs-lookup"><span data-stu-id="62d11-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="62d11-116">Svæði **verkflæðiseining** í verkflæðisritill inniheldur þætti sem þú getur bætt við verkflæði.</span><span class="sxs-lookup"><span data-stu-id="62d11-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="62d11-117">Til að bæta einingar við verkflæðisins skal draga þær yfir í striga.</span><span class="sxs-lookup"><span data-stu-id="62d11-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="62d11-118">Tengja einingar</span><span class="sxs-lookup"><span data-stu-id="62d11-118">Connect the elements</span></span>

<span data-ttu-id="62d11-119">Til að tengja eina verkflæðiseiningu við aðra skal halda bendlinum yfir einingu þar til tengipunktar birtast.</span><span class="sxs-lookup"><span data-stu-id="62d11-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="62d11-120">Smella skal á tengipunktinn og draga hann yfir í aðra einingu.</span><span class="sxs-lookup"><span data-stu-id="62d11-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="62d11-121">Gætið þess að tengja saman allar einingarnar.</span><span class="sxs-lookup"><span data-stu-id="62d11-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="62d11-122">Skilgreina eiginleika verkflæðis</span><span class="sxs-lookup"><span data-stu-id="62d11-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="62d11-123">Fylgið eftirfarandi skrefum til að skilgreina eiginleika verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="62d11-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="62d11-124">Smellt er á striga til að tryggja að enginn verkflæðiseiningunni er valinn.</span><span class="sxs-lookup"><span data-stu-id="62d11-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="62d11-125">Smellið á **eiginleikar** til að opna í **Eiginleika** fyrir verkflæðið.</span><span class="sxs-lookup"><span data-stu-id="62d11-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="62d11-126">Farið að ferlinu í efninu [stilla eiginleika fyrir Verkflæði](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="62d11-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="62d11-127">Skilgreinið einingar verkflæðisins</span><span class="sxs-lookup"><span data-stu-id="62d11-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="62d11-128">Stilla hverja einingu sem er valinn og dreginn á striga.</span><span class="sxs-lookup"><span data-stu-id="62d11-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="62d11-129">Nánari upplýsingar um hvernig á að skilgreina hverja verkflæðiseiningu er að finna í eftirfarandi efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="62d11-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="62d11-130">Skilgreina handvirkt verk</span><span class="sxs-lookup"><span data-stu-id="62d11-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="62d11-131">Skilgreina sjálfvirkt verk</span><span class="sxs-lookup"><span data-stu-id="62d11-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="62d11-132">Skilgreining samþykktarferlis</span><span class="sxs-lookup"><span data-stu-id="62d11-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="62d11-133">Skilgreining samþykktarskrefs</span><span class="sxs-lookup"><span data-stu-id="62d11-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="62d11-134">Skilgreining handvirkrar ákvörðunar</span><span class="sxs-lookup"><span data-stu-id="62d11-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="62d11-135">Skilgreining skilyrtrar ákvörðunar</span><span class="sxs-lookup"><span data-stu-id="62d11-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="62d11-136">Skilgreining hliðstæðs verkþáttar</span><span class="sxs-lookup"><span data-stu-id="62d11-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="62d11-137">Skilgreina Hliðstæður grein</span><span class="sxs-lookup"><span data-stu-id="62d11-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="62d11-138">Skilgreina Verkflæði línuatriðis</span><span class="sxs-lookup"><span data-stu-id="62d11-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="62d11-139">Leysa allar villur eða viðvaranir</span><span class="sxs-lookup"><span data-stu-id="62d11-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="62d11-140">Svæðið **Villur og athugasemdir**, neðst á verkflæðisritill, birtir skilaboð sem hafa verið búnir til fyrir verkflæði.</span><span class="sxs-lookup"><span data-stu-id="62d11-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="62d11-141">Til að finna einingu þar sem villa eða viðvörun kemur upp, skal tvísmella á villuna eða viðvörunina.</span><span class="sxs-lookup"><span data-stu-id="62d11-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="62d11-142">Allar villur og viðvaranir verður að leysa áður en hægt er að gera verkflæði virka.</span><span class="sxs-lookup"><span data-stu-id="62d11-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="62d11-143">Vista og virkja verkflæðið</span><span class="sxs-lookup"><span data-stu-id="62d11-143">Save and activate the workflow</span></span>

<span data-ttu-id="62d11-144">Þegar þú ert tilbúinn til að vista og virkja verkflæði skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="62d11-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="62d11-145">Smellið á **Vista og loka** til að loka verkflæðisritlinum og opna í **Vista verkflæði** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="62d11-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="62d11-146">Færðu inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="62d11-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="62d11-147">Ef villur og viðvaranir hefur verið leyst, **Virkja verkflæði** birtist.</span><span class="sxs-lookup"><span data-stu-id="62d11-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="62d11-148">Veldu einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="62d11-148">Select one of the following options:</span></span>

    - <span data-ttu-id="62d11-149">Smellið til að virkja þessa útgáfu verkflæðisins á **virkja nýja útgáfu**.</span><span class="sxs-lookup"><span data-stu-id="62d11-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="62d11-150">Þegar verkflæði er virkt, notendur senda skjöl í hana í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="62d11-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="62d11-151">Eigi ekki að virkja þessa útgáfu, smellið á **Ekki virkja nýju útgáfuna**.</span><span class="sxs-lookup"><span data-stu-id="62d11-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="62d11-152">Hægt er að virkja verkflæðið síðar.</span><span class="sxs-lookup"><span data-stu-id="62d11-152">You can activate the workflow later.</span></span>

