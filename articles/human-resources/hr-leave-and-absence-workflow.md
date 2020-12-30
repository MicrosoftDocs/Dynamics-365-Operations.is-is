---
title: Stofna verkflæði fyrir beiðni um leyfi
description: Búðu til vinnuflæði fyrir leyfi og fjarveru til að stjórna stöðugt leyfisbeiðnum í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418962"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="0c191-103">Stofna verkflæði fyrir beiðni um leyfi</span><span class="sxs-lookup"><span data-stu-id="0c191-103">Create a leave request workflow</span></span>

<span data-ttu-id="0c191-104">Hægt er að stofna vinnuflæði í Dynamics 365 Human Resources til að stjórna stöðugt leyfis- og fjarvistarbeiðnum þínum.</span><span class="sxs-lookup"><span data-stu-id="0c191-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="0c191-105">Verkflæðið **Leyfi og fjarvera** gerir þér kleift að:</span><span class="sxs-lookup"><span data-stu-id="0c191-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="0c191-106">Skilgreina verkefni</span><span class="sxs-lookup"><span data-stu-id="0c191-106">Define tasks</span></span>
- <span data-ttu-id="0c191-107">Ákveða hverjir verða að klára verkefnin</span><span class="sxs-lookup"><span data-stu-id="0c191-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="0c191-108">Tilgreina hverjir geta samþykkt eða hafnað beiðnum</span><span class="sxs-lookup"><span data-stu-id="0c191-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="0c191-109">Stofna verkflæði fyrir beiðni um leyfi og fjarveru</span><span class="sxs-lookup"><span data-stu-id="0c191-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="0c191-110">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="0c191-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="0c191-111">Undir **Skipulag**, veldu **Vinnuflæði mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="0c191-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="0c191-112">Veldu **Nýtt** og veldu síðan **Beiðnir um leyfi og fjarveru**.</span><span class="sxs-lookup"><span data-stu-id="0c191-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="0c191-113">Þegar **Opna þessa skrá?** skilaboðakassi birtist, veldu **Opið** og skráðu þig inn með persónuskilríki fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="0c191-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="0c191-114">Notaðu verkflæðiritið til að búa til verkflæði fyrir leyfisbeiðnir þínar.</span><span class="sxs-lookup"><span data-stu-id="0c191-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="0c191-115">Nánari upplýsingar um vinnu með verkflæði, sjá [Búðu til yfirlit yfir verkflæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="0c191-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="0c191-116">Gagnaeiningar fyrir verkflæði leyfis- og fjarvistabeiðni</span><span class="sxs-lookup"><span data-stu-id="0c191-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="0c191-117">Hægt er að nota eftirfarandi gagnaeiningar til að stofna skilyrtar eða sjálfvirkar samþykktir í verkflæði fyrir beiðnir um leyfi og fjarvistir:</span><span class="sxs-lookup"><span data-stu-id="0c191-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="0c191-118">**Upphæð**</span><span class="sxs-lookup"><span data-stu-id="0c191-118">**Amount**</span></span>
- <span data-ttu-id="0c191-119">**Athugasemd**</span><span class="sxs-lookup"><span data-stu-id="0c191-119">**Comment**</span></span>
- <span data-ttu-id="0c191-120">**Fyrirt.**</span><span class="sxs-lookup"><span data-stu-id="0c191-120">**Company**</span></span>
- <span data-ttu-id="0c191-121">**Búið til af**</span><span class="sxs-lookup"><span data-stu-id="0c191-121">**Created by**</span></span>
- <span data-ttu-id="0c191-122">**Tími og dagsetning stofnunar**</span><span class="sxs-lookup"><span data-stu-id="0c191-122">**Created date and time**</span></span>
- <span data-ttu-id="0c191-123">**Lokadagur**</span><span class="sxs-lookup"><span data-stu-id="0c191-123">**End date**</span></span>
- <span data-ttu-id="0c191-124">**Gerð leyfis**</span><span class="sxs-lookup"><span data-stu-id="0c191-124">**Leave type**</span></span>
- <span data-ttu-id="0c191-125">**Breytt hefur**</span><span class="sxs-lookup"><span data-stu-id="0c191-125">**Modified by**</span></span>
- <span data-ttu-id="0c191-126">**Breytt dagsetning og tími**</span><span class="sxs-lookup"><span data-stu-id="0c191-126">**Modified date and time**</span></span>
- <span data-ttu-id="0c191-127">**Ástæðukóði**</span><span class="sxs-lookup"><span data-stu-id="0c191-127">**Reason code**</span></span>
- <span data-ttu-id="0c191-128">**Beiðnikenni**</span><span class="sxs-lookup"><span data-stu-id="0c191-128">**Request ID**</span></span>
- <span data-ttu-id="0c191-129">**Upphafsdagsetning**</span><span class="sxs-lookup"><span data-stu-id="0c191-129">**Start date**</span></span>
- <span data-ttu-id="0c191-130">**Staða**</span><span class="sxs-lookup"><span data-stu-id="0c191-130">**Status**</span></span> 
- <span data-ttu-id="0c191-131">**Sendidagur**</span><span class="sxs-lookup"><span data-stu-id="0c191-131">**Submission date**</span></span>
- <span data-ttu-id="0c191-132">**Sent af**</span><span class="sxs-lookup"><span data-stu-id="0c191-132">**Submitted by**</span></span>
- <span data-ttu-id="0c191-133">**Sent af mannauðsstjóra**</span><span class="sxs-lookup"><span data-stu-id="0c191-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="0c191-134">**Sent af stjórnanda**</span><span class="sxs-lookup"><span data-stu-id="0c191-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="0c191-135">**Sent fyrir hönd**</span><span class="sxs-lookup"><span data-stu-id="0c191-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="0c191-136">**Starfsmaður**</span><span class="sxs-lookup"><span data-stu-id="0c191-136">**Worker**</span></span>
- <span data-ttu-id="0c191-137">**Gerð starfskrafts**</span><span class="sxs-lookup"><span data-stu-id="0c191-137">**Worker type**</span></span>

<span data-ttu-id="0c191-138">Þessi dæmi sýna hvernig hægt er að stofna mismunandi skilyrði verkflæðis með þessum gagnaeiningum:</span><span class="sxs-lookup"><span data-stu-id="0c191-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="0c191-139">Notaðu **Ástæðukóði** í skilyrtri setningu til að beina leyfisbeiðnum með ástæðukóðanum **Skurðaðgerð** til samþykkis mannauðsdeildar, en alla aðra ástæðukóða til stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="0c191-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="0c191-140">Frekari upplýsingar um skilyrta setningu er að finna í [Skilgreina skilyrtar ákvarðanir í verkflæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="0c191-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="0c191-141">Notið **Sent af mannauðsstjóra** og **Sent af stjórnanda** í sjálfvirkri aðgerð til að samþykkja sjálfkrafa leyfisbeiðnir sem þessi hlutverk senda fyrir hönd starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="0c191-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="0c191-142">Frekari upplýsingar um sjálfvirkar aðgerðir er að finna í [Grunnstilla samþykktarferli í verkflæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="0c191-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="0c191-143">Nota skal **Leyfisgerðir** í skilyrtri setningu eða sjálfvirkri aðgerð til að hafa stjórn á því hvernig verkflæðisleiðir fara fram með tilteknum leyfisgerðum.</span><span class="sxs-lookup"><span data-stu-id="0c191-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c191-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0c191-144">See also</span></span>

- [<span data-ttu-id="0c191-145">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="0c191-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
