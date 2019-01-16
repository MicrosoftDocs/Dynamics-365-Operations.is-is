---
title: "Aðgerðir í verkflæðissamþykki"
description: "Þessi grein útskýrir aðgerðir sem hver þátttakandi í verkflæðissamþykki getur gripið til."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 829ee16b8fd72a0808a657419524487d9c1b3123
ms.contentlocale: is-is
ms.lasthandoff: 12/18/2018

---

# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="56d9c-103">Aðgerðir í verkflæðissamþykki</span><span class="sxs-lookup"><span data-stu-id="56d9c-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56d9c-104">Þessi grein útskýrir aðgerðir sem hver þátttakandi í verkflæðissamþykki getur gripið til.</span><span class="sxs-lookup"><span data-stu-id="56d9c-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="56d9c-105">Verkflæði getur innihaldið nokkra hópa fólks: upphafsmann, viðtakanda verks, stjórnendur og samþykktaraðila.</span><span class="sxs-lookup"><span data-stu-id="56d9c-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="56d9c-106">Til dæmis í eftirfarandi verkflæði fyrir kostnaðarskýrslur er Samúel upphafsmaður, meðlimir í biðröð eru viðtakendur verks, Jón er stjórnandi og Friðrik, Súsanna og Anna eru samþykkjendur.</span><span class="sxs-lookup"><span data-stu-id="56d9c-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="56d9c-107">[![Verkflæði\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="56d9c-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="56d9c-108">Eftirfarandi kaflar útskýra þær verkflæðisaðgerðir sem hver flokkur getur framkvæmt.</span><span class="sxs-lookup"><span data-stu-id="56d9c-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="56d9c-109">Aðgerðir sem upphafsmaður getur framkvæmt</span><span class="sxs-lookup"><span data-stu-id="56d9c-109">Actions that an originator can perform</span></span>

<span data-ttu-id="56d9c-110">Stofnandinn byrjar verkflæðistilvik með því að senda skjal til vinnslu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="56d9c-111">Til dæmis verður Samúel að smella á hnappinn **Senda** á síðunni **Kostnaðarskýrsla** til að senda kostnaðarskýrsluna sína.</span><span class="sxs-lookup"><span data-stu-id="56d9c-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="56d9c-112">Aðgerðir sem verkþegi getur framkvæmt</span><span class="sxs-lookup"><span data-stu-id="56d9c-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="56d9c-113">Hægt er að úthluta verkefni til margra eða á vinnuliðalista sem er vaktaður af nokkrum einstaklingum.</span><span class="sxs-lookup"><span data-stu-id="56d9c-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="56d9c-114">Hins vegar getur aðeins ein manneskja lokið verkinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-114">However, only one person can complete a task.</span></span> <span data-ttu-id="56d9c-115">Til dæmis hefur Samúel sent kostnaðarskýrslu og vísað innhreyfingum sínum á kostnaðarskýrsludeild fyrirtækisins til endurskoðunar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="56d9c-116">Starfsmenn kostnaðarskýrsludeildar Adventure Works fylgjast með biðröðinni.</span><span class="sxs-lookup"><span data-stu-id="56d9c-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="56d9c-117">Júlía, starfsmaður í þeirri deild, hefur samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="56d9c-118">Nú getur hún framkvæmt eina af eftirfarandi aðgerðum: ljúka, hafna, úthluta, biðja um breytingu, endurúthluta eða losa.</span><span class="sxs-lookup"><span data-stu-id="56d9c-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="56d9c-119">Mismunandi aðgerðir eru til boða eftir því hvernig forritarinn hannaði verkefnið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="56d9c-120">Ljúka</span><span class="sxs-lookup"><span data-stu-id="56d9c-120">Complete</span></span>

<span data-ttu-id="56d9c-121">Þegar notandi lýkur verkefni er skjalinu sem var sent til vinnslu úthlutað til næsta notanda í verkflæðinu, ef næsti notandi er til staðar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="56d9c-122">Ef ekki er þörf á frekari vinnslu endar verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="56d9c-123">Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="56d9c-124">Eftir að Júlía lýkur endurskoðuninni er skjalinu úthlutað til Jóns.</span><span class="sxs-lookup"><span data-stu-id="56d9c-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="56d9c-125">Hafna</span><span class="sxs-lookup"><span data-stu-id="56d9c-125">Reject</span></span>

<span data-ttu-id="56d9c-126">Þegar notandi hafnar skjali endar verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="56d9c-127">Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="56d9c-128">Þegar Júlía hefur samþykkt kostnaðarskýrsluna lýkur verkflæðiferlinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="56d9c-129">Samúel getur síðan sent kostnaðarskýrsluna aftur.</span><span class="sxs-lookup"><span data-stu-id="56d9c-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="56d9c-130">Hann getur gert breytingar fyrst eða hann getur endursent upprunalega útgáfu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="56d9c-131">Ef Samúel sendir kostnaðarskýrsluna aftur, hefst verkflæðisferlið á handvirkri endurskoðun.</span><span class="sxs-lookup"><span data-stu-id="56d9c-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="56d9c-132">Fulltrúi</span><span class="sxs-lookup"><span data-stu-id="56d9c-132">Delegate</span></span>

<span data-ttu-id="56d9c-133">Þegar notandi skipar fulltrúa fyrir verkefni, er verkefninu úthlutað til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="56d9c-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="56d9c-134">Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="56d9c-135">Júlía úthlutar verkinu til Tim sem er aðstoðarmaður hennar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="56d9c-136">Síðan starfar Tim fyrir hönd Júlíu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="56d9c-137">Þess vegna er kostnaðarskýrslunni úthlutað til Jóns þegar Tim lýkur yfirferð sinni, rétt eins og Júlía hefði lokið verkinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="56d9c-138">Beiðni um breytingu</span><span class="sxs-lookup"><span data-stu-id="56d9c-138">Request change</span></span>

<span data-ttu-id="56d9c-139">Þegar notandi biður um breytingu á skjalinu sem var sent, er það sent aftur til stofnandans.</span><span class="sxs-lookup"><span data-stu-id="56d9c-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="56d9c-140">Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="56d9c-141">Júlía tekur eftir villum í kostnaðarskýrslunni og gerir beiðni um breytingar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="56d9c-142">Kostnaðarskýrslan er send til baka til Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="56d9c-143">Samúel getur sent kostnaðarskýrsluna aftur.</span><span class="sxs-lookup"><span data-stu-id="56d9c-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="56d9c-144">Hann getur gert umbeðnar breytingar fyrst eða hann getur endursent upprunalega útgáfu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="56d9c-145">Ef Samúel endursendir kostnaðarskýrsluna, verður starfsmaður í vinnuliðalistanum að endurskoða innhreyfingarnar aftur.</span><span class="sxs-lookup"><span data-stu-id="56d9c-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="56d9c-146">Endurúthluta</span><span class="sxs-lookup"><span data-stu-id="56d9c-146">Reassign</span></span>

<span data-ttu-id="56d9c-147">Meðlimir vinnuliðalista geta endurúthlutað skjölum sem eru í þeirri biðröð yfir á aðra biðröð.</span><span class="sxs-lookup"><span data-stu-id="56d9c-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="56d9c-148">Til dæmis er Júlía, starfsmaður kostnaðarskýrsludeildar Adventure Works, fylgjast með biðröðinni.</span><span class="sxs-lookup"><span data-stu-id="56d9c-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="56d9c-149">Til að dreifa vinnuálaginu getur hún endurúthlutað kostnaðarskýrslunni og innhreyfingum sem fylgja með henni í aðra biðröð.</span><span class="sxs-lookup"><span data-stu-id="56d9c-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="56d9c-150">Losun</span><span class="sxs-lookup"><span data-stu-id="56d9c-150">Release</span></span>

<span data-ttu-id="56d9c-151">Einstaka sinnum gæti meðlimur vinnuliðalista samþykkt verk en síðan ákveðið að hann eða hún geti ekki lokið verkinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="56d9c-152">Í þessu tilfelli getur sá aðili sem samþykkti verkið losað skjalið aftur í vinnuliðalistann.</span><span class="sxs-lookup"><span data-stu-id="56d9c-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="56d9c-153">Til dæmis hefur Júlía, starfsmaður í kostnaðarskýrsludeild Adventure Works, samþykkt verk til endurskoðunar á kostnaðarskýrslu og innhreyfingum Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="56d9c-154">Ef Júlía ákveður að hún geti ekki lokið verkinu getur hún losað skjalið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="56d9c-155">Kostnaðarskýrslunni er skilað til baka í biðröðina, svo að aðrir starfsmenn kostnaðarskýrsludeildar Adventure Works geti lokið verkinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="56d9c-156">Aðgerðir sem stjórnandi getur framkvæmt</span><span class="sxs-lookup"><span data-stu-id="56d9c-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="56d9c-157">Yfirleitt er skjal tengt stjórnanda, þar sem það er spurning sem stjórnandinn verður að svara spurningu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="56d9c-158">Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="56d9c-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="56d9c-159">Ef stjórnandi velur ekki einn af þessum valkostum getur hann eða hún úthlutað ákvörðuninni.</span><span class="sxs-lookup"><span data-stu-id="56d9c-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="56d9c-160">\[Choice 1\] eða \[Choice 2\]</span><span class="sxs-lookup"><span data-stu-id="56d9c-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="56d9c-161">Stjórnandi verður að svara spurningu sem tengist skjalinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="56d9c-162">Svar við spurningunni er yfirleitt **Já** eða **Nei**, eða **Satt** eða **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="56d9c-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="56d9c-163">Svarið sem stjórnandinn velur ákvarðar þá verkflæðisgrein sem er notuð til að vinna skjalið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="56d9c-164">Til dæmis er kostnaðarskýrslu Samúels úthlutað á Jón.</span><span class="sxs-lookup"><span data-stu-id="56d9c-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="56d9c-165">Jón verður að ákveða hvort upplýsingarnar í skjalinu krefjast símtals til yfirmanns Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="56d9c-166">Ef Jón ákveður að símtal sé nauðsynlegt er kostnaðarskýrslunni úthlutað til Agnesar, sem verður þá að hringja í yfirmann Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="56d9c-167">Ef Jón ákveður að símtal sé ekki nauðsynlegt er kostnaðarskýrslunni úthlutað til Friðriks til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="56d9c-168">Fulltrúi</span><span class="sxs-lookup"><span data-stu-id="56d9c-168">Delegate</span></span>

<span data-ttu-id="56d9c-169">Þegar stjórnandi framselur ákvörðun, er skjalinu úthlutað til annars notanda sem þarf að taka ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="56d9c-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="56d9c-170">Til dæmis er kostnaðarskýrslu Samúels úthlutað á Jón.</span><span class="sxs-lookup"><span data-stu-id="56d9c-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="56d9c-171">Jón framselur ákvörðuninni til Maríu, sem er aðstoðarmaður hans.</span><span class="sxs-lookup"><span data-stu-id="56d9c-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="56d9c-172">Síðan starfar María fyrir hönd Jóns.</span><span class="sxs-lookup"><span data-stu-id="56d9c-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="56d9c-173">Ef María ákveður að símtal til yfirmanns Samúels sé nauðsynlegt er kostnaðarskýrslunni úthlutað til Agnesar, sem verður þá að hringja í yfirmann Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="56d9c-174">Ef María ákveður að símtal sé ekki nauðsynlegt er kostnaðarskýrslunni úthlutað til Friðriks til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="56d9c-175">Aðgerðir sem samþykktaraðili getur framkvæmt</span><span class="sxs-lookup"><span data-stu-id="56d9c-175">Actions that an approver can perform</span></span>

<span data-ttu-id="56d9c-176">Þegar skjali er úthlutað til samþykkjanda getur hann gripið til eftirfarandi aðgerða: Samþykkja, hafna, framselja eða biðja um breytingar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="56d9c-177">Samþykkja</span><span class="sxs-lookup"><span data-stu-id="56d9c-177">Approve</span></span>

<span data-ttu-id="56d9c-178">Þegar samþykkjandi samþykkir skjal er því úthlutað til næsta notanda í verkflæðinu, ef næsti notandi er til staðar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="56d9c-179">Ef ekki er þörf á frekari vinnslu endar verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="56d9c-180">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $6,000 og þessu skjali hefur verið úthlutað til Friðriks.</span><span class="sxs-lookup"><span data-stu-id="56d9c-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="56d9c-181">Þegar Friðrik samþykkir skjalið er því úthlutað til Súsönnu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="56d9c-182">Þegar Súsanna samþykkir kostnaðarskýrsluna lýkur verkflæðiferlinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="56d9c-183">Hafna</span><span class="sxs-lookup"><span data-stu-id="56d9c-183">Reject</span></span>

<span data-ttu-id="56d9c-184">Þegar samþykkjandi hafnar skjali endar verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="56d9c-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="56d9c-185">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $12,000 og þessu skjali hefur verið úthlutað til Súsönnu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="56d9c-186">Ef Súsanna hafnar kostnaðarskýrslunni lýkur verkflæðiferlinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="56d9c-187">Samúel getur sent kostnaðarskýrsluna aftur.</span><span class="sxs-lookup"><span data-stu-id="56d9c-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="56d9c-188">Hann getur gert breytingar fyrst eða endursent upprunalega útgáfu af kostnaðarskýrslunni.</span><span class="sxs-lookup"><span data-stu-id="56d9c-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="56d9c-189">Ef Samúel sendir kostnaðarskýrsluna aftur, hefst verkflæðisferlið á samþykktarferlinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="56d9c-190">Fulltrúi</span><span class="sxs-lookup"><span data-stu-id="56d9c-190">Delegate</span></span>

<span data-ttu-id="56d9c-191">Þegar samþykkjandi skipar fulltrúa fyrir skjal, er skjalinu úthlutað til annars notanda til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="56d9c-192">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $12,000 og þessu skjali hefur verið úthlutað til Friðriks.</span><span class="sxs-lookup"><span data-stu-id="56d9c-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="56d9c-193">Friðrik úthlutar kostnaðarskýrslunni til Önnu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="56d9c-194">Síðan starfar Anna fyrir hönd Friðriks.</span><span class="sxs-lookup"><span data-stu-id="56d9c-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="56d9c-195">Þetta þýðir að þegar Anna samþykkir skjalið þá er því úthlutað til Súsönnu til samþykktar, rétt eins og ef Friðrik hafi samþykkt það.</span><span class="sxs-lookup"><span data-stu-id="56d9c-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="56d9c-196">Þegar Súsanna samþykkir skjalið er það sent til Önnu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="56d9c-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="56d9c-197">Beiðni um breytingu</span><span class="sxs-lookup"><span data-stu-id="56d9c-197">Request change</span></span>

<span data-ttu-id="56d9c-198">Þegar samþykkjandi biður um breytingu á skjalinu er það sent aftur til stofnandans.</span><span class="sxs-lookup"><span data-stu-id="56d9c-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="56d9c-199">Til dæmis hefur Samúel sent kostnaðarskýrslu upp á $12,000 og þessu skjali hefur verið úthlutað til Súsönnu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="56d9c-200">Ef Súsanna biður um breytingu er kostnaðarskýrslan send til baka til Samúels.</span><span class="sxs-lookup"><span data-stu-id="56d9c-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="56d9c-201">Samúel getur sent kostnaðarskýrsluna aftur.</span><span class="sxs-lookup"><span data-stu-id="56d9c-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="56d9c-202">Hann getur gert umbeðnar breytingar fyrst eða endursent upprunalega útgáfu af kostnaðarskýrslunni.</span><span class="sxs-lookup"><span data-stu-id="56d9c-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="56d9c-203">Ef Samúel endursendir kostnaðarskýrsluna þá er hún send til Friðriks til samþykktar, því að Friðrik var fyrsti samþykkjandinn í samþykktarferlinu.</span><span class="sxs-lookup"><span data-stu-id="56d9c-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>

