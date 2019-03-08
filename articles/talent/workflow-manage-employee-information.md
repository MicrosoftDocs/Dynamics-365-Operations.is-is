---
title: Verkflæði eru notuð til að stjórna upplýsingum starfsmanns
description: Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0ffae206ae1956e5dc41487f04561ed2c48bd20b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304776"
---
# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="b13c2-104">Verkflæði eru notuð til að stjórna upplýsingum starfsmanns</span><span class="sxs-lookup"><span data-stu-id="b13c2-104">Use workflows to manage employee information</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b13c2-105">Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="b13c2-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="b13c2-106">Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.</span><span class="sxs-lookup"><span data-stu-id="b13c2-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="b13c2-107">Verkflæðisgeta fyrir mannauð veitir fjölda verkflæða fyrir stjórnun mannauðsaðgerða.</span><span class="sxs-lookup"><span data-stu-id="b13c2-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="b13c2-108">Þar að auki eru fjölmargir valkostir tiltækir svo að hægt er að breyta tilteknum verkflæðum og tengja þau við skýrslustigveldi.</span><span class="sxs-lookup"><span data-stu-id="b13c2-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="b13c2-109">Verkflæði eru tiltæk til að aðstoða við stjórnun á breytingum á nokkrum stöðluðum gerðum starfsmannaupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="b13c2-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="b13c2-110">Hægt er að tengja verkflæði við stöðu.</span><span class="sxs-lookup"><span data-stu-id="b13c2-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="b13c2-111">Síðan, ef starfsmenn breyta skráningu sinni, er verkflæði hafið sem þarfnast samþykkis áður en nýju upplýsingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="b13c2-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="b13c2-112">Verkflæði eru forskilgreind fyrir eftirfarandi gerðir upplýsinga til að hjálpa við skilvirka stjórnun og halda starfsmannagögnum nákvæmum:</span><span class="sxs-lookup"><span data-stu-id="b13c2-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="b13c2-113">Auðkennisnúmer</span><span class="sxs-lookup"><span data-stu-id="b13c2-113">Identification numbers</span></span>
-   <span data-ttu-id="b13c2-114">Námskeið</span><span class="sxs-lookup"><span data-stu-id="b13c2-114">Courses</span></span>
-   <span data-ttu-id="b13c2-115">Menntun</span><span class="sxs-lookup"><span data-stu-id="b13c2-115">Education</span></span>
-   <span data-ttu-id="b13c2-116">Mynd</span><span class="sxs-lookup"><span data-stu-id="b13c2-116">Image</span></span>
-   <span data-ttu-id="b13c2-117">Lánsvörur</span><span class="sxs-lookup"><span data-stu-id="b13c2-117">Loaned items</span></span>
-   <span data-ttu-id="b13c2-118">Starfsreynsla</span><span class="sxs-lookup"><span data-stu-id="b13c2-118">Professional experience</span></span>
-   <span data-ttu-id="b13c2-119">Verkreynsla</span><span class="sxs-lookup"><span data-stu-id="b13c2-119">Project experience</span></span>
-   <span data-ttu-id="b13c2-120">Hæfni</span><span class="sxs-lookup"><span data-stu-id="b13c2-120">Skills</span></span>
-   <span data-ttu-id="b13c2-121">Ábyrgðarstöður</span><span class="sxs-lookup"><span data-stu-id="b13c2-121">Positions of trust</span></span>
-   <span data-ttu-id="b13c2-122">Mannauðsaðgerðir</span><span class="sxs-lookup"><span data-stu-id="b13c2-122">Human resources actions</span></span>
-   <span data-ttu-id="b13c2-123">Námskeiðsskráning</span><span class="sxs-lookup"><span data-stu-id="b13c2-123">Course registration</span></span>

<span data-ttu-id="b13c2-124">Þegar starfsmenn eru ráðnir, fluttir eða hættir getur verkflæðið innihaldið endurskoðunarferli.</span><span class="sxs-lookup"><span data-stu-id="b13c2-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="b13c2-125">Á þennan hátt er hægt að endurskoða skjal eða skilgreina skilmála aðgerðar sem hluta af verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="b13c2-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="b13c2-126">Þegar endurskoðunarferli er lokið er skjalið eða aðgerð lokið og verkflæðið færist yfir í endanlegt samþykktarskref.</span><span class="sxs-lookup"><span data-stu-id="b13c2-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="b13c2-127">Tengja verkflæði við stigveldi stöðu</span><span class="sxs-lookup"><span data-stu-id="b13c2-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="b13c2-128">Hægt er að tengja verkflæði við öll stigveldi sem eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="b13c2-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="b13c2-129">Til dæmis, ef staða tengist fylki skýrslustigveldis gætirðu skilgreint verkflæði sem beinir kostnaði fyrir tiltekið verk til verksins í stað stjórnanda þess starfsmanns sem tengist þeirri stöðu.</span><span class="sxs-lookup"><span data-stu-id="b13c2-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="b13c2-130">Til að stofna nýtt verkflæði eða breyta fyrirliggjandi verkflæði á síðunni **Verkflæði fyrir mannauð** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="b13c2-131">Veldu verkflæði í listanum til að hefja Verkflæðishönnuð.</span><span class="sxs-lookup"><span data-stu-id="b13c2-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="b13c2-132">Hægt er að nota hönnuðinn til að stofna nýtt verkflæði eða breyta skrefum í fyrirliggjandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="b13c2-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="b13c2-133">Þegar fyrirliggjandi verkflæði er breytt eru breytingarnar vistaðar sem ný útgáfa.</span><span class="sxs-lookup"><span data-stu-id="b13c2-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="b13c2-134">Þess vegna er hægt alltaf fara til baka í fyrri útgáfu ef þarf.</span><span class="sxs-lookup"><span data-stu-id="b13c2-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="b13c2-135">Grunnstilla verkflæði fyrir mannauð</span><span class="sxs-lookup"><span data-stu-id="b13c2-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="b13c2-136">Til að grunnstilla grunnverkflæði sem ræsist þegar starfsmenn biðja um breytingar á persónuupplýsingum sínum, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b13c2-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="b13c2-137">Á síðunni **Verkflæði fyrir mannauð** er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="b13c2-138">Í listanum yfir tiltæk verkflæði velurðu **Auðkennisnúmer**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="b13c2-139">Smellið á **Keyra** til að hefja Verkflæðishönnuð og færið síðan inn notandanafn þitt og aðgangsorð við kvaðningu.</span><span class="sxs-lookup"><span data-stu-id="b13c2-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="b13c2-140">Draga skal eininguna **Samþykkja auðkennisnúmer** úr listanum yfir verkflæðiseiningar á hönnunarstrigann.</span><span class="sxs-lookup"><span data-stu-id="b13c2-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="b13c2-141">Tengja samþykktareininguna við **Ræsa** og **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="b13c2-142">Tvísmellið á **Samþykkja einingu** og hægrismellið svo og veljið **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="b13c2-143">Fylgja skal þessum skrefum til að bæta við vöruleiðbeiningum:</span><span class="sxs-lookup"><span data-stu-id="b13c2-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="b13c2-144">Veldu **Úthlutun** og veldu síðan **Stigveldi** undir úthlutunargerð.</span><span class="sxs-lookup"><span data-stu-id="b13c2-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="b13c2-145">Undir valinu **Stigveldi** skal velja **Skilgreinanleg stigveldi**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="b13c2-146">Bæta við stöðvunarskilyrði og loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="b13c2-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="b13c2-147">Lokið öllum viðbótarleiðbeiningum (engar aðrar viðvaranir eiga að vera til).</span><span class="sxs-lookup"><span data-stu-id="b13c2-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="b13c2-148">Smellið á **Vista og loka**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-148">Click **Save and close**.</span></span> <span data-ttu-id="b13c2-149">Virkja nýja verkflæðið þegar svarglugginn opnast og velja **Gera virka**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="b13c2-150">Fara í **Mannauð**&gt;**Stöður**&gt;**Stigveldisgerðir stöðu**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="b13c2-151">Velja **Fylki**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="b13c2-152">Bæta við verkflæðinu **Auðkennisnúmer starfsmanns** við listann.</span><span class="sxs-lookup"><span data-stu-id="b13c2-152">Add the **Worker identification number** workflow to the list.</span></span>




