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
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190006"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="90000-103">Yfirlit yfir verkflæðiskerfi</span><span class="sxs-lookup"><span data-stu-id="90000-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90000-104">Þetta efnisatriði lýsir verkflæðiskerfinu.</span><span class="sxs-lookup"><span data-stu-id="90000-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="90000-105">Hvað er verkflæði?</span><span class="sxs-lookup"><span data-stu-id="90000-105">What is workflow?</span></span>

<span data-ttu-id="90000-106">Hugtakið *verkflæði* er hægt að skilgreina á tvo vegu: sem kerfi og sem viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="90000-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="90000-107">Verkflæði er kerfi</span><span class="sxs-lookup"><span data-stu-id="90000-107">Workflow is a system</span></span>

<span data-ttu-id="90000-108">Workflow er kerfi sem keyrir á Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="90000-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="90000-109">Verkflæðiskerfi veitir aðgerðir sem þú getur notað til að mynda einstakt verkflæði, eða viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="90000-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="90000-110">Verkflæði er viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="90000-110">Workflow is a business process</span></span>

<span data-ttu-id="90000-111">Verkflæði endurspeglar viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="90000-111">A workflow represents a business process.</span></span> <span data-ttu-id="90000-112">Það skilgreinir hvernig skjal flæðir eða hreyfist gegnum kerfið með því að sýna hver verður að ljúka verki, taka ákvörðun eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="90000-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="90000-113">Til dæmis sýnir eftirfarandi teikning verkflæði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="90000-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Verkflæði með einingum sem hefur verið úthlutað til notenda](./media/workflow_user.gif)

<span data-ttu-id="90000-115">Til að skilja þetta verkflæði betur er gert ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 7,000 USD.</span><span class="sxs-lookup"><span data-stu-id="90000-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="90000-116">Í þessari lýsingu þarf Ivan að endurskoða kvittanirnar sem Sam sendi til hans.</span><span class="sxs-lookup"><span data-stu-id="90000-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="90000-117">Síðan verða Frank og Sue að samþykkja kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="90000-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="90000-118">Gerum nú ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 11.000.</span><span class="sxs-lookup"><span data-stu-id="90000-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="90000-119">Í þessari lýsingu verður Ivan að endurskoða kvittanirnar og Frank, Sue og Ann að samþykkja kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="90000-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="90000-120">Kostir við notkun Verkflæðiskerfisins</span><span class="sxs-lookup"><span data-stu-id="90000-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="90000-121">Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="90000-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="90000-122">**Samræmt ferli** — Hægt er að skilgreina hversu nákvæmlega skjöl, , eins og innkaupabeiðnir og kostnaðarskýrslur, skuli vera unnin.</span><span class="sxs-lookup"><span data-stu-id="90000-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="90000-123">Með því að nota verkflæðiskerfi er gengið úr skugga um að skjölin eru unnin og samþykkt með samræmdum og skilvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="90000-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="90000-124">**Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks.</span><span class="sxs-lookup"><span data-stu-id="90000-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="90000-125">Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.</span><span class="sxs-lookup"><span data-stu-id="90000-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="90000-126">**Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalista sem birtir verkflæðisverk og samþykktir sem tilheyra þeim.</span><span class="sxs-lookup"><span data-stu-id="90000-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="90000-127">Samhengi verkflæðis</span><span class="sxs-lookup"><span data-stu-id="90000-127">Workflow content</span></span>

+ [<span data-ttu-id="90000-128">Uppbygging verkflæðis</span><span class="sxs-lookup"><span data-stu-id="90000-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="90000-129">Verkflæðiseiningar</span><span class="sxs-lookup"><span data-stu-id="90000-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="90000-130">Verkflæðisaðgerðir</span><span class="sxs-lookup"><span data-stu-id="90000-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="90000-131">Verkflæði stofnað</span><span class="sxs-lookup"><span data-stu-id="90000-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="90000-132">Skilgreining verkflæðiseiginleika</span><span class="sxs-lookup"><span data-stu-id="90000-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="90000-133">Skilgreina handvirkt verk í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="90000-134">Skilgreina sjálfvirkt verki í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="90000-135">Skilgreina samþykktarferli í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="90000-136">Skilgreina samþykktarskref í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="90000-137">Skilgreina handvirka ákvörðun í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="90000-138">Skilgreina skilyrta ákvörðun í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="90000-139">Grunnstilla hliðstæðan verkþátt í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="90000-140">Grunnstilla samhliða grein í verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="90000-141">Skilgreining verkflæðis línuatriðis</span><span class="sxs-lookup"><span data-stu-id="90000-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="90000-142">Algengar spurningar um verkflæði</span><span class="sxs-lookup"><span data-stu-id="90000-142">Workflow FAQ</span></span>](workflow-FAQ.md)