---
title: Nota verkflæði til að haga starfsmannaupplýsingum
description: Í þessari grein er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: aba7627877cd9b79dce5930e528f892e2d80baac
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058753"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="5da9b-104">Nota verkflæði til að haga starfsmannaupplýsingum</span><span class="sxs-lookup"><span data-stu-id="5da9b-104">Use workflows to manage employee information</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5da9b-105">Í þessari grein er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="5da9b-105">This article explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="5da9b-106">Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.</span><span class="sxs-lookup"><span data-stu-id="5da9b-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="5da9b-107">Verkflæðisgeta fyrir mannauð veitir fjölda verkflæða fyrir stjórnun mannauðsaðgerða.</span><span class="sxs-lookup"><span data-stu-id="5da9b-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="5da9b-108">Þar að auki eru fjölmargir valkostir tiltækir svo að hægt er að breyta tilteknum verkflæðum og tengja þau við skýrslustigveldi.</span><span class="sxs-lookup"><span data-stu-id="5da9b-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="5da9b-109">Verkflæði eru tiltæk til að aðstoða við stjórnun á breytingum á nokkrum stöðluðum gerðum starfsmannaupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="5da9b-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="5da9b-110">Hægt er að tengja verkflæði við stöðu.</span><span class="sxs-lookup"><span data-stu-id="5da9b-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="5da9b-111">Síðan, ef starfsmenn breyta skráningu sinni, er verkflæði hafið sem þarfnast samþykkis áður en nýju upplýsingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="5da9b-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="5da9b-112">Verkflæði eru forskilgreind fyrir eftirfarandi gerðir upplýsinga til að hjálpa við skilvirka stjórnun og halda starfsmannagögnum nákvæmum:</span><span class="sxs-lookup"><span data-stu-id="5da9b-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="5da9b-113">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="5da9b-113">Identification numbers</span></span>
-   <span data-ttu-id="5da9b-114">Námskeið</span><span class="sxs-lookup"><span data-stu-id="5da9b-114">Courses</span></span>
-   <span data-ttu-id="5da9b-115">Menntun</span><span class="sxs-lookup"><span data-stu-id="5da9b-115">Education</span></span>
-   <span data-ttu-id="5da9b-116">Mynd</span><span class="sxs-lookup"><span data-stu-id="5da9b-116">Image</span></span>
-   <span data-ttu-id="5da9b-117">Lánsvörur</span><span class="sxs-lookup"><span data-stu-id="5da9b-117">Loaned items</span></span>
-   <span data-ttu-id="5da9b-118">Starfsreynsla</span><span class="sxs-lookup"><span data-stu-id="5da9b-118">Professional experience</span></span>
-   <span data-ttu-id="5da9b-119">Verkreynsla</span><span class="sxs-lookup"><span data-stu-id="5da9b-119">Project experience</span></span>
-   <span data-ttu-id="5da9b-120">Hæfni</span><span class="sxs-lookup"><span data-stu-id="5da9b-120">Skills</span></span>
-   <span data-ttu-id="5da9b-121">Ábyrgðarstöður</span><span class="sxs-lookup"><span data-stu-id="5da9b-121">Positions of trust</span></span>
-   <span data-ttu-id="5da9b-122">Mannauðsaðgerðir</span><span class="sxs-lookup"><span data-stu-id="5da9b-122">Human resources actions</span></span>
-   <span data-ttu-id="5da9b-123">Námskeiðsskráning</span><span class="sxs-lookup"><span data-stu-id="5da9b-123">Course registration</span></span>

<span data-ttu-id="5da9b-124">Þegar starfsmenn eru ráðnir, fluttir eða hættir getur verkflæðið innihaldið endurskoðunarferli.</span><span class="sxs-lookup"><span data-stu-id="5da9b-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="5da9b-125">Á þennan hátt er hægt að endurskoða skjal eða skilgreina skilmála aðgerðar sem hluta af verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="5da9b-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="5da9b-126">Þegar endurskoðunarferli er lokið er skjalið eða aðgerð lokið og verkflæðið færist yfir í endanlegt samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="5da9b-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="5da9b-127">Tengja verkflæði við stigveldi stöðu</span><span class="sxs-lookup"><span data-stu-id="5da9b-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="5da9b-128">Hægt er að tengja verkflæði við öll stigveldi sem eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="5da9b-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="5da9b-129">Til dæmis, ef staða tengist fylki skýrslustigveldis gætirðu skilgreint verkflæði sem beinir kostnaði fyrir tiltekið verk til verksins í stað stjórnanda þess starfsmanns sem tengist þeirri stöðu.</span><span class="sxs-lookup"><span data-stu-id="5da9b-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="5da9b-130">Til að stofna nýtt verkflæði eða breyta fyrirliggjandi verkflæði á síðunni **Verkflæði fyrir mannauð** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="5da9b-131">Veldu verkflæði í listanum til að hefja Verkflæðishönnuð.</span><span class="sxs-lookup"><span data-stu-id="5da9b-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="5da9b-132">Hægt er að nota hönnuðinn til að stofna nýtt verkflæði eða breyta skrefum í fyrirliggjandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="5da9b-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="5da9b-133">Þegar fyrirliggjandi verkflæði er breytt eru breytingarnar vistaðar sem ný útgáfa.</span><span class="sxs-lookup"><span data-stu-id="5da9b-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="5da9b-134">Þess vegna er hægt alltaf fara til baka í fyrri útgáfu ef þarf.</span><span class="sxs-lookup"><span data-stu-id="5da9b-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="5da9b-135">Grunnstilla verkflæði fyrir mannauð</span><span class="sxs-lookup"><span data-stu-id="5da9b-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="5da9b-136">Til að grunnstilla grunnverkflæði sem ræsist þegar starfsmenn biðja um breytingar á persónuupplýsingum sínum, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="5da9b-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="5da9b-137">Á síðunni **Verkflæði fyrir mannauð** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="5da9b-138">Í listanum yfir tiltæk verkflæði velurðu **Auðkennisnúmer**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="5da9b-139">Smellið á **Keyra** til að hefja Verkflæðishönnuð og færið síðan inn notandanafn þitt og aðgangsorð við kvaðningu.</span><span class="sxs-lookup"><span data-stu-id="5da9b-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="5da9b-140">Draga skal eininguna **Samþykkja auðkennisnúmer** úr listanum yfir verkflæðiseiningar á hönnunarstrigann.</span><span class="sxs-lookup"><span data-stu-id="5da9b-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="5da9b-141">Tengja samþykktareininguna við **Ræsa** og **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="5da9b-142">Tvísmellið á **Samþykkja einingu** og hægrismellið svo og veljið **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="5da9b-143">Fylgja skal þessum skrefum til að bæta við vöruleiðbeiningum:</span><span class="sxs-lookup"><span data-stu-id="5da9b-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="5da9b-144">Veldu **Úthlutun** og veldu síðan **Stigveldi** undir úthlutunargerð.</span><span class="sxs-lookup"><span data-stu-id="5da9b-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="5da9b-145">Undir valinu **Stigveldi** skal velja **Skilgreinanleg stigveldi**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="5da9b-146">Bæta við stöðvunarskilyrði og loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="5da9b-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="5da9b-147">Lokið öllum viðbótarleiðbeiningum (engar aðrar viðvaranir eiga að vera til).</span><span class="sxs-lookup"><span data-stu-id="5da9b-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="5da9b-148">Smellið á **Vista og loka**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-148">Click **Save and close**.</span></span> <span data-ttu-id="5da9b-149">Virkja nýja verkflæðið þegar svarglugginn opnast og velja **Gera virka**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="5da9b-150">Fara í **Mannauð** &gt; **Stöður** &gt; **Stigveldisgerðir stöðu**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="5da9b-151">Velja **Fylki**.</span><span class="sxs-lookup"><span data-stu-id="5da9b-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="5da9b-152">Bæta við verkflæðinu **Auðkennisnúmer starfsmanns** við listann.</span><span class="sxs-lookup"><span data-stu-id="5da9b-152">Add the **Worker identification number** workflow to the list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5da9b-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5da9b-153">Additional resources</span></span>

[<span data-ttu-id="5da9b-154">Skoða og hafa umsjón með breytingum á aðsetri</span><span class="sxs-lookup"><span data-stu-id="5da9b-154">View and manage address changes</span></span>](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]