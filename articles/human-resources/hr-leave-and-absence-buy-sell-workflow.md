---
title: Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum
description: Stofna skal verkflæði fyrir beiðni um kaup og sölu á leyfisdögum til að stjórna betur beiðnum um kaup og sölu á leyfisdögum í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712601"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="75161-103">Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="75161-103">Create a buy and sell leave request workflow</span></span>

<span data-ttu-id="75161-104">Hægt er að stofna verkflæði í Dynamics 365 Human Resources til að stjórna betur beiðnum um kaup og sölu á leyfisdögum.</span><span class="sxs-lookup"><span data-stu-id="75161-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="75161-105">Verkflæði fyrir **Kaupa og selja leyfisdaga** gerir þér kleift að:</span><span class="sxs-lookup"><span data-stu-id="75161-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="75161-106">Skilgreina verkefni</span><span class="sxs-lookup"><span data-stu-id="75161-106">Define tasks</span></span>
- <span data-ttu-id="75161-107">Ákveða hverjir verða að klára verkefnin</span><span class="sxs-lookup"><span data-stu-id="75161-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="75161-108">Tilgreina hverjir geta samþykkt eða hafnað beiðnum</span><span class="sxs-lookup"><span data-stu-id="75161-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="75161-109">Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="75161-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="75161-110">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="75161-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="75161-111">Undir **Skipulag**, veldu **Vinnuflæði mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="75161-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="75161-112">Velja **Ný** og síðan velja **Beiðni um að kaupa og selja leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="75161-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="75161-113">Þegar **Opna þessa skrá?** skilaboðakassi birtist, veldu **Opið** og skráðu þig inn með persónuskilríki fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="75161-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="75161-114">Notaðu verkflæðiritið til að búa til verkflæði fyrir leyfisbeiðnir þínar.</span><span class="sxs-lookup"><span data-stu-id="75161-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="75161-115">Nánari upplýsingar um vinnu með verkflæði, sjá [Búðu til yfirlit yfir verkflæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="75161-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="75161-116">Gagnaeiningar fyrir verkflæði leyfis- og fjarvistabeiðni</span><span class="sxs-lookup"><span data-stu-id="75161-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="75161-117">Hægt er að nota eftirfarandi gagnaeiningar til að stofna skilyrtar eða sjálfvirkar samþykktir í verkflæðum fyrir beiðnir um kaup og sölu á leyfisdögum:</span><span class="sxs-lookup"><span data-stu-id="75161-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="75161-118">**Upphæð**</span><span class="sxs-lookup"><span data-stu-id="75161-118">**Amount**</span></span>
- <span data-ttu-id="75161-119">**Regla um kaup og sölu leyfisdaga**</span><span class="sxs-lookup"><span data-stu-id="75161-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="75161-120">**Fyrirt.**</span><span class="sxs-lookup"><span data-stu-id="75161-120">**Company**</span></span>
- <span data-ttu-id="75161-121">**Stofnað af**</span><span class="sxs-lookup"><span data-stu-id="75161-121">**Created by**</span></span>
- <span data-ttu-id="75161-122">**Tími og dagsetning stofnunar**</span><span class="sxs-lookup"><span data-stu-id="75161-122">**Created date and time**</span></span>
- <span data-ttu-id="75161-123">**Lokadagsetning**</span><span class="sxs-lookup"><span data-stu-id="75161-123">**End date**</span></span>
- <span data-ttu-id="75161-124">**Leyfisgerð**</span><span class="sxs-lookup"><span data-stu-id="75161-124">**Leave type**</span></span>
- <span data-ttu-id="75161-125">**Breytt hefur**</span><span class="sxs-lookup"><span data-stu-id="75161-125">**Modified by**</span></span>
- <span data-ttu-id="75161-126">**Breytt dagsetning og tími**</span><span class="sxs-lookup"><span data-stu-id="75161-126">**Modified date and time**</span></span>
- <span data-ttu-id="75161-127">**Beiðnikenni**</span><span class="sxs-lookup"><span data-stu-id="75161-127">**Request ID**</span></span>
- <span data-ttu-id="75161-128">**Upphafsdagsetning**</span><span class="sxs-lookup"><span data-stu-id="75161-128">**Start date**</span></span>
- <span data-ttu-id="75161-129">**Staða**</span><span class="sxs-lookup"><span data-stu-id="75161-129">**Status**</span></span> 
- <span data-ttu-id="75161-130">**Dagsetning innsendingar**</span><span class="sxs-lookup"><span data-stu-id="75161-130">**Submission date**</span></span>
- <span data-ttu-id="75161-131">**Sent hefur**</span><span class="sxs-lookup"><span data-stu-id="75161-131">**Submitted by**</span></span>
- <span data-ttu-id="75161-132">**Sent af mannauðsstjóra**</span><span class="sxs-lookup"><span data-stu-id="75161-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="75161-133">**Sent af stjórnanda**</span><span class="sxs-lookup"><span data-stu-id="75161-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="75161-134">**Sent fyrir hönd**</span><span class="sxs-lookup"><span data-stu-id="75161-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="75161-135">**Starfsmaður**</span><span class="sxs-lookup"><span data-stu-id="75161-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="75161-136">Dæmi um verkflæði</span><span class="sxs-lookup"><span data-stu-id="75161-136">Workflow examples</span></span>

<span data-ttu-id="75161-137">Þessi dæmi sýna hvernig hægt er að stofna mismunandi skilyrði verkflæðis með þessum gagnaeiningum:</span><span class="sxs-lookup"><span data-stu-id="75161-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="75161-138">Notið **Sent af mannauðsstjóra** og **Sent af stjórnanda** í sjálfvirkri aðgerð til að samþykkja sjálfkrafa kaup og sölu leyfisbeiðna sem þessi hlutverk senda fyrir hönd starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="75161-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="75161-139">Frekari upplýsingar um sjálfvirkar aðgerðir er að finna í [Grunnstilla samþykktarferli í verkflæði](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="75161-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="75161-140">Nota skal **Leyfisgerðir** í skilyrtri setningu eða sjálfvirkri aðgerð til að hafa stjórn á því hvernig verkflæðisleiðir fara fram með tilteknum leyfisgerðum.</span><span class="sxs-lookup"><span data-stu-id="75161-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="75161-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="75161-141">See also</span></span>

[<span data-ttu-id="75161-142">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="75161-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="75161-143">Stjórna reglum fyrir kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="75161-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

