---
title: "Verkflæði innkaupa og aðfanga"
description: "Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 75daeed0d0e979165d3669e83e98cf278d7fb736
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="2a39a-104">Verkflæði innkaupa og aðfanga</span><span class="sxs-lookup"><span data-stu-id="2a39a-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a39a-105">Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna.</span><span class="sxs-lookup"><span data-stu-id="2a39a-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="2a39a-106">Til að setja upp samþykktarferli er hægt að stofna verkflæði.</span><span class="sxs-lookup"><span data-stu-id="2a39a-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="2a39a-107">Verkflæði endurspeglar viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="2a39a-107">A workflow represents a business process.</span></span> <span data-ttu-id="2a39a-108">Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="2a39a-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="2a39a-109">Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="2a39a-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="2a39a-110">**Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="2a39a-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="2a39a-111">Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="2a39a-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="2a39a-112">**Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks.</span><span class="sxs-lookup"><span data-stu-id="2a39a-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="2a39a-113">Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.</span><span class="sxs-lookup"><span data-stu-id="2a39a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="2a39a-114">**Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalisti og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim þvert á allt verkflæði sem þeir taka þátt í..</span><span class="sxs-lookup"><span data-stu-id="2a39a-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="2a39a-115">Þetta er tiltæk á síðunni Vinnuliðir.</span><span class="sxs-lookup"><span data-stu-id="2a39a-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="2a39a-116"> Gerðir verkflæðis sem hægt er að stofna</span><span class="sxs-lookup"><span data-stu-id="2a39a-116">The types of workflows that you can create</span></span>
<span data-ttu-id="2a39a-117">Eftirfarandi verkflæðisgerðir eru tiltækar fyrir innkaup og aðföng.</span><span class="sxs-lookup"><span data-stu-id="2a39a-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2a39a-118">**Gerð**</span><span class="sxs-lookup"><span data-stu-id="2a39a-118">**Type**</span></span>                         | <span data-ttu-id="2a39a-119">**Notið þessa gerð til að**</span><span class="sxs-lookup"><span data-stu-id="2a39a-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="2a39a-120">Endurskoða innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="2a39a-120">Purchase requisition review</span></span>      | <span data-ttu-id="2a39a-121">Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="2a39a-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="2a39a-122">Endurskoða innkaupabeiðnilínu</span><span class="sxs-lookup"><span data-stu-id="2a39a-122">Purchase requisition line review</span></span> | <span data-ttu-id="2a39a-123">Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnalínur.</span><span class="sxs-lookup"><span data-stu-id="2a39a-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="2a39a-124">Verkflæði innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="2a39a-124">Purchase order workflow</span></span>          | <span data-ttu-id="2a39a-125">Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="2a39a-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="2a39a-126">Verkflæði innkaupapöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="2a39a-126">Purchase order line workflow</span></span>     | <span data-ttu-id="2a39a-127">stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="2a39a-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="2a39a-128">Verkflæði umsóknar um að bæta við lánardrottni</span><span class="sxs-lookup"><span data-stu-id="2a39a-128">Vendor add application workflow</span></span>  | <span data-ttu-id="2a39a-129">Stofna endurskoðunar- og samþykkisverkflæði til að bæta við nýjum lánardrottnum gegnum beiðnir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="2a39a-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="2a39a-130">verkflæði stofnuð</span><span class="sxs-lookup"><span data-stu-id="2a39a-130">Creating a workflow</span></span>
<span data-ttu-id="2a39a-131">Til að stofna verkflæði er farið í Innkaup og aðföng &gt; Uppsetning &gt; verkflæði Innkaupa og uppruna og stofnað nýtt verkflæði með því að velja gerð verkflæðis sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="2a39a-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="2a39a-132">Í Verkflæðistriga er hægt að draga verkflæðiseiningar yfir hönnuðinn og tengja einingarnar í flæði.</span><span class="sxs-lookup"><span data-stu-id="2a39a-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="2a39a-133">einingar verkflæðisins ætti að skilgreina</span><span class="sxs-lookup"><span data-stu-id="2a39a-133">The workflow elements should be configured.</span></span> <span data-ttu-id="2a39a-134">Fyrir verkflæðiseiningar Samþykkis og verkefnis má skilgreina hvaða þátttakandi á að framkvæma aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="2a39a-134">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="2a39a-135">Gerð þátttakenda</span><span class="sxs-lookup"><span data-stu-id="2a39a-135">Types of participants</span></span>
----------------------

<span data-ttu-id="2a39a-136">Hægt er að úthluta samþykktarskrefi til eftirfarandi flokka þátttakenda.</span><span class="sxs-lookup"><span data-stu-id="2a39a-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="2a39a-137">Notendaflokkur</span><span class="sxs-lookup"><span data-stu-id="2a39a-137">User group</span></span>    | <span data-ttu-id="2a39a-138">Lýsing</span><span class="sxs-lookup"><span data-stu-id="2a39a-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="2a39a-139">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="2a39a-139">Participant</span></span>   | <span data-ttu-id="2a39a-140">Úthluta samþykktarskrefinu til aðila í hópi eða hlutverki.</span><span class="sxs-lookup"><span data-stu-id="2a39a-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="2a39a-141">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="2a39a-141">Hierarchy</span></span>     | <span data-ttu-id="2a39a-142">Úthluta samþykktarskrefi til notenda í tilteknu stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="2a39a-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="2a39a-143">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="2a39a-143">Workflow user</span></span> | <span data-ttu-id="2a39a-144">Úthluta samþykktarskrefinu til notenda í þessu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="2a39a-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="2a39a-145">Biðröð</span><span class="sxs-lookup"><span data-stu-id="2a39a-145">Queue</span></span>         | <span data-ttu-id="2a39a-146">Úthluta samþykktarskrefinu til vinnuliðalista.</span><span class="sxs-lookup"><span data-stu-id="2a39a-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="2a39a-147">Notandi</span><span class="sxs-lookup"><span data-stu-id="2a39a-147">User</span></span>          | <span data-ttu-id="2a39a-148">Úthluta samþykktarskrefinu til tiltekinna notenda .</span><span class="sxs-lookup"><span data-stu-id="2a39a-148">Assign the approval step to specific users.</span></span>                               |



<a name="additional-resources"></a><span data-ttu-id="2a39a-149">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2a39a-149">Additional resources</span></span>
--------

[<span data-ttu-id="2a39a-150">Skilgreina viðskiptaferli verkflæði fyrir innkaupabeiðnir</span><span class="sxs-lookup"><span data-stu-id="2a39a-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="2a39a-151">Verkflæði innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="2a39a-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

[<span data-ttu-id="2a39a-152">Innleiðing nýrra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="2a39a-152">Onboarding vendors</span></span>](vendor-onboarding.md)


