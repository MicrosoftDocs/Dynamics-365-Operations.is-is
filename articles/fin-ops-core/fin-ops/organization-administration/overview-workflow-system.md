---
title: Yfirlit yfir verkflæðiskerfi
description: Þetta efnisatriði lýsir verkflæðiskerfinu.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef77a5d81d12ec92eea86b1dd9902d9e3d80b33
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812364"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="86cba-103">Yfirlit yfir verkflæðiskerfi</span><span class="sxs-lookup"><span data-stu-id="86cba-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86cba-104">Þetta efnisatriði lýsir verkflæðiskerfinu.</span><span class="sxs-lookup"><span data-stu-id="86cba-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="86cba-105">Hvað er verkflæði?</span><span class="sxs-lookup"><span data-stu-id="86cba-105">What is workflow?</span></span>

<span data-ttu-id="86cba-106">Hugtakið *verkflæði* er hægt að skilgreina á tvo vegu: sem kerfi og sem viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="86cba-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="86cba-107">Verkflæði er kerfi</span><span class="sxs-lookup"><span data-stu-id="86cba-107">Workflow is a system</span></span>

<span data-ttu-id="86cba-108">Workflow er kerfi sem keyrir á Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="86cba-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="86cba-109">Verkflæðiskerfi veitir aðgerðir sem þú getur notað til að mynda einstakt verkflæði, eða viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="86cba-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="86cba-110">Verkflæði er viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="86cba-110">Workflow is a business process</span></span>

<span data-ttu-id="86cba-111">Verkflæði endurspeglar viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="86cba-111">A workflow represents a business process.</span></span> <span data-ttu-id="86cba-112">Það skilgreinir hvernig skjal flæðir eða hreyfist gegnum kerfið með því að sýna hver verður að ljúka verki, taka ákvörðun eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="86cba-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="86cba-113">Til dæmis sýnir eftirfarandi teikning verkflæði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="86cba-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Verkflæði með einingum sem hefur verið úthlutað til notenda](./media/workflow_user.gif)

<span data-ttu-id="86cba-115">Til að skilja þetta verkflæði betur er gert ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 7,000 USD.</span><span class="sxs-lookup"><span data-stu-id="86cba-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="86cba-116">Í þessari lýsingu þarf Ivan að endurskoða kvittanirnar sem Sam sendi til hans.</span><span class="sxs-lookup"><span data-stu-id="86cba-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="86cba-117">Síðan verða Frank og Sue að samþykkja kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="86cba-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="86cba-118">Gerum nú ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 11.000.</span><span class="sxs-lookup"><span data-stu-id="86cba-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="86cba-119">Í þessari lýsingu verður Ivan að endurskoða kvittanirnar og Frank, Sue og Ann að samþykkja kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="86cba-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="86cba-120">Kostir við notkun Verkflæðiskerfisins</span><span class="sxs-lookup"><span data-stu-id="86cba-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="86cba-121">Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="86cba-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="86cba-122">**Samræmt ferli** — Hægt er að skilgreina hversu nákvæmlega skjöl, , eins og innkaupabeiðnir og kostnaðarskýrslur, skuli vera unnin.</span><span class="sxs-lookup"><span data-stu-id="86cba-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="86cba-123">Með því að nota verkflæðiskerfi er gengið úr skugga um að skjölin eru unnin og samþykkt með samræmdum og skilvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="86cba-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="86cba-124">**Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks.</span><span class="sxs-lookup"><span data-stu-id="86cba-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="86cba-125">Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.</span><span class="sxs-lookup"><span data-stu-id="86cba-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="86cba-126">**Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalista sem birtir verkflæðisverk og samþykktir sem tilheyra þeim.</span><span class="sxs-lookup"><span data-stu-id="86cba-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="86cba-127">Samhengi verkflæðis</span><span class="sxs-lookup"><span data-stu-id="86cba-127">Workflow content</span></span>

+ [<span data-ttu-id="86cba-128">Kerfisskipulag verkflæðis</span><span class="sxs-lookup"><span data-stu-id="86cba-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="86cba-129">Verkflæðiseiningar</span><span class="sxs-lookup"><span data-stu-id="86cba-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="86cba-130">Verkþættir í samþykktarferli verkflæðis</span><span class="sxs-lookup"><span data-stu-id="86cba-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="86cba-131">Yfirlit yfir stofnun verkflæðis</span><span class="sxs-lookup"><span data-stu-id="86cba-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="86cba-132">Skilgreining verkflæðiseiginleika</span><span class="sxs-lookup"><span data-stu-id="86cba-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="86cba-133">Skilgreina handvirk verk í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="86cba-134">Skilgreina sjálfvirk verk í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="86cba-135">Grunnstilla samþykktarferli í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="86cba-136">Grunnstilla samþykktarskref í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="86cba-137">Skilgreina handvirkar ákvarðanir í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="86cba-138">Skilgreina skilyrtar ákvöarðanir í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="86cba-139">Skilgreina hliðstæða verkþætti í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="86cba-140">Skilgreina samhliða greinar í verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="86cba-141">Skilgreina verkflæði línuatriða</span><span class="sxs-lookup"><span data-stu-id="86cba-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="86cba-142">Algengar spurningar um verkflæði</span><span class="sxs-lookup"><span data-stu-id="86cba-142">Workflow FAQ</span></span>](workflow-FAQ.md)
