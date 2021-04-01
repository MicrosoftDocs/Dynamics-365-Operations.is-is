---
title: Verkflæði innkaupa og aðfanga
description: Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e591007a1330fe11b3f586185f9daca845798908
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218466"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="9a74a-104">Verkflæði innkaupa og aðfanga</span><span class="sxs-lookup"><span data-stu-id="9a74a-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a74a-105">Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna.</span><span class="sxs-lookup"><span data-stu-id="9a74a-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="9a74a-106">Til að setja upp samþykktarferli er hægt að stofna verkflæði.</span><span class="sxs-lookup"><span data-stu-id="9a74a-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="9a74a-107">Verkflæði endurspeglar viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="9a74a-107">A workflow represents a business process.</span></span> <span data-ttu-id="9a74a-108">Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="9a74a-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="9a74a-109">Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="9a74a-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="9a74a-110">**Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="9a74a-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="9a74a-111">Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="9a74a-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="9a74a-112">**Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks.</span><span class="sxs-lookup"><span data-stu-id="9a74a-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="9a74a-113">Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.</span><span class="sxs-lookup"><span data-stu-id="9a74a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="9a74a-114">**Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalisti og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim þvert á allt verkflæði sem þeir taka þátt í..</span><span class="sxs-lookup"><span data-stu-id="9a74a-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="9a74a-115">Þetta er tiltæk á síðunni Vinnuliðir.</span><span class="sxs-lookup"><span data-stu-id="9a74a-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="9a74a-116"> Gerðir verkflæðis sem hægt er að stofna</span><span class="sxs-lookup"><span data-stu-id="9a74a-116">The types of workflows that you can create</span></span>

<span data-ttu-id="9a74a-117">Eftirfarandi verkflæðisgerðir eru tiltækar fyrir innkaup og aðföng.</span><span class="sxs-lookup"><span data-stu-id="9a74a-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="9a74a-118">Gerð</span><span class="sxs-lookup"><span data-stu-id="9a74a-118">Type</span></span> | <span data-ttu-id="9a74a-119">Notið þessa gerð til að</span><span class="sxs-lookup"><span data-stu-id="9a74a-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="9a74a-120">Endurskoða innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="9a74a-120">Purchase requisition review</span></span> | <span data-ttu-id="9a74a-121">Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="9a74a-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="9a74a-122">Endurskoða innkaupabeiðnilínu</span><span class="sxs-lookup"><span data-stu-id="9a74a-122">Purchase requisition line review</span></span> | <span data-ttu-id="9a74a-123">Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnalínur.</span><span class="sxs-lookup"><span data-stu-id="9a74a-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="9a74a-124">Verkflæði innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="9a74a-124">Purchase order workflow</span></span> | <span data-ttu-id="9a74a-125">Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="9a74a-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="9a74a-126">Verkflæði innkaupapöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="9a74a-126">Purchase order line workflow</span></span> | <span data-ttu-id="9a74a-127">stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="9a74a-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="9a74a-128">Verkflæði umsóknar um að bæta við lánardrottni</span><span class="sxs-lookup"><span data-stu-id="9a74a-128">Vendor add application workflow</span></span> | <span data-ttu-id="9a74a-129">Stofna endurskoðunar- og samþykkisverkflæði til að bæta við nýjum lánardrottnum gegnum beiðnir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="9a74a-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="9a74a-130">Þegar verið er að bæta við nýju verkflæði er einnig hægt að sjá eftirfarandi úrelt verkflæði sem skráð eru í svarglugganum **Stofna verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="9a74a-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="9a74a-131">Þetta tengist *staðfestingu kvittunar* virkninni sem var tiltæk í [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), en sem ekki er lengur boðið upp á.</span><span class="sxs-lookup"><span data-stu-id="9a74a-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="9a74a-132">Þessi verkflæði eru ekki studd eins og er.</span><span class="sxs-lookup"><span data-stu-id="9a74a-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="9a74a-133">Verkflæði tilkynningar um skiladag sendingar</span><span class="sxs-lookup"><span data-stu-id="9a74a-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="9a74a-134">Verkflæði tilkynninga um móttekinn reikning</span><span class="sxs-lookup"><span data-stu-id="9a74a-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="9a74a-135">Verkflæði tilkynninga um misheppnuð innhreyfingarskjöl afurða</span><span class="sxs-lookup"><span data-stu-id="9a74a-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="9a74a-136">Verkflæði tilkynninga um höfnun óstaðfestra innhreyfinga afurða</span><span class="sxs-lookup"><span data-stu-id="9a74a-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="9a74a-137">verkflæði stofnuð</span><span class="sxs-lookup"><span data-stu-id="9a74a-137">Creating a workflow</span></span>

<span data-ttu-id="9a74a-138">Til að stofna verkflæði er farið í Innkaup og aðföng &gt; Uppsetning &gt; verkflæði Innkaupa og uppruna og stofnað nýtt verkflæði með því að velja gerð verkflæðis sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="9a74a-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="9a74a-139">Í Verkflæðistriga er hægt að draga verkflæðiseiningar yfir hönnuðinn og tengja einingarnar í flæði.</span><span class="sxs-lookup"><span data-stu-id="9a74a-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="9a74a-140">einingar verkflæðisins ætti að skilgreina</span><span class="sxs-lookup"><span data-stu-id="9a74a-140">The workflow elements should be configured.</span></span> <span data-ttu-id="9a74a-141">Fyrir verkflæðiseiningar Samþykkis og verkefnis má skilgreina hvaða þátttakandi á að framkvæma aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="9a74a-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="9a74a-142">Gerð þátttakenda</span><span class="sxs-lookup"><span data-stu-id="9a74a-142">Types of participants</span></span>

<span data-ttu-id="9a74a-143">Hægt er að úthluta samþykktarskrefi til eftirfarandi flokka þátttakenda.</span><span class="sxs-lookup"><span data-stu-id="9a74a-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="9a74a-144">Notendaflokkur</span><span class="sxs-lookup"><span data-stu-id="9a74a-144">User group</span></span> | <span data-ttu-id="9a74a-145">Lýsing</span><span class="sxs-lookup"><span data-stu-id="9a74a-145">Description</span></span> |
|---|---|
| <span data-ttu-id="9a74a-146">Þátttakendur</span><span class="sxs-lookup"><span data-stu-id="9a74a-146">Participant</span></span> | <span data-ttu-id="9a74a-147">Úthluta samþykktarskrefinu til aðila í hópi eða hlutverki.</span><span class="sxs-lookup"><span data-stu-id="9a74a-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="9a74a-148">Stigveldi</span><span class="sxs-lookup"><span data-stu-id="9a74a-148">Hierarchy</span></span> | <span data-ttu-id="9a74a-149">Úthluta samþykktarskrefi til notenda í tilteknu stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="9a74a-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="9a74a-150">Verkflæðisnotandi</span><span class="sxs-lookup"><span data-stu-id="9a74a-150">Workflow user</span></span> | <span data-ttu-id="9a74a-151">Úthluta samþykktarskrefinu til notenda í þessu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="9a74a-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="9a74a-152">Biðröð</span><span class="sxs-lookup"><span data-stu-id="9a74a-152">Queue</span></span> | <span data-ttu-id="9a74a-153">Úthluta samþykktarskrefinu til vinnuliðalista.</span><span class="sxs-lookup"><span data-stu-id="9a74a-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="9a74a-154">Notandi</span><span class="sxs-lookup"><span data-stu-id="9a74a-154">User</span></span> | <span data-ttu-id="9a74a-155">Úthluta samþykktarskrefinu til tiltekinna notenda .</span><span class="sxs-lookup"><span data-stu-id="9a74a-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9a74a-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9a74a-156">Additional resources</span></span>

- [<span data-ttu-id="9a74a-157">Skilgreina viðskiptaferli verkflæði fyrir innkaupabeiðnir</span><span class="sxs-lookup"><span data-stu-id="9a74a-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="9a74a-158">Verkflæði innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="9a74a-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="9a74a-159">Nýliðun lánardrottna</span><span class="sxs-lookup"><span data-stu-id="9a74a-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]