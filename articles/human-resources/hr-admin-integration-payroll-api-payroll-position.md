---
title: Launaupplýsingar fyrir stöður
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882004"
---
# <a name="payroll-position"></a><span data-ttu-id="f9290-103">Launastaða</span><span class="sxs-lookup"><span data-stu-id="f9290-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f9290-104">Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f9290-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="f9290-105">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="f9290-105">Properties</span></span>

| <span data-ttu-id="f9290-106">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="f9290-106">Property</span></span><br><span data-ttu-id="f9290-107">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="f9290-107">**Physical name**</span></span><br><span data-ttu-id="f9290-108">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="f9290-108">**_Type_**</span></span> | <span data-ttu-id="f9290-109">Nota</span><span class="sxs-lookup"><span data-stu-id="f9290-109">Use</span></span> | <span data-ttu-id="f9290-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="f9290-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f9290-111">**Reglulegar árlegar vinnustundir**</span><span class="sxs-lookup"><span data-stu-id="f9290-111">**Annual regular hours**</span></span><br><span data-ttu-id="f9290-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="f9290-112">annualregularhours</span></span><br><span data-ttu-id="f9290-113">*Tugabrot*</span><span class="sxs-lookup"><span data-stu-id="f9290-113">*Decimal*</span></span> | <span data-ttu-id="f9290-114">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-114">Read-only</span></span><br><span data-ttu-id="f9290-115">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-115">Required</span></span> | <span data-ttu-id="f9290-116">Reglulegar árlegar vinnustundir skilgreindar fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="f9290-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="f9290-117">**Einingarkenni fyrir upplýsingar um launastöðu**</span><span class="sxs-lookup"><span data-stu-id="f9290-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="f9290-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="f9290-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="f9290-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="f9290-119">*Guid*</span></span> | <span data-ttu-id="f9290-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-120">Required</span></span><br><span data-ttu-id="f9290-121">Búið til af kerfi.</span><span class="sxs-lookup"><span data-stu-id="f9290-121">System generated.</span></span> | <span data-ttu-id="f9290-122">GUID-gildi myndað af kerfinu til að auðkenna stöðu á einkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="f9290-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="f9290-123">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="f9290-123">**Primary field**</span></span><br><span data-ttu-id="f9290-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f9290-124">mshr_primaryfield</span></span><br><span data-ttu-id="f9290-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f9290-125">*String*</span></span> | <span data-ttu-id="f9290-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-126">Required</span></span><br><span data-ttu-id="f9290-127">Búið til af kerfi</span><span class="sxs-lookup"><span data-stu-id="f9290-127">System generated</span></span> |  |
| <span data-ttu-id="f9290-128">**Gildi fyrir kenni vinnustöðu**</span><span class="sxs-lookup"><span data-stu-id="f9290-128">**Position job ID value**</span></span><br><span data-ttu-id="f9290-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="f9290-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="f9290-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f9290-130">*GUID*</span></span> | <span data-ttu-id="f9290-131">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-131">Read-only</span></span><br><span data-ttu-id="f9290-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-132">Required</span></span><br><span data-ttu-id="f9290-133">Framandlykill:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="f9290-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="f9290-134">Kenni starfsins sem tengist stöðunni.</span><span class="sxs-lookup"><span data-stu-id="f9290-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="f9290-135">**Gildi fyrir kenni launafyrirkomulags fastra launa**</span><span class="sxs-lookup"><span data-stu-id="f9290-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="f9290-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="f9290-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="f9290-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f9290-137">*GUID*</span></span> | <span data-ttu-id="f9290-138">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-138">Read-only</span></span><br><span data-ttu-id="f9290-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-139">Required</span></span><br><span data-ttu-id="f9290-140">Framandlykill: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="f9290-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="f9290-141">Kenni launafyrirkomulags fastra launa sem tengist stöðunni.</span><span class="sxs-lookup"><span data-stu-id="f9290-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="f9290-142">**Kenni greiðsluferlis**</span><span class="sxs-lookup"><span data-stu-id="f9290-142">**Pay cycle ID**</span></span><br><span data-ttu-id="f9290-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f9290-143">mshr_primaryfield</span></span><br><span data-ttu-id="f9290-144">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f9290-144">*String*</span></span> | <span data-ttu-id="f9290-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-145">Read-only</span></span><br><span data-ttu-id="f9290-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-146">Required</span></span> | <span data-ttu-id="f9290-147">Greiðsluferli skilgreint fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="f9290-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="f9290-148">**Greitt af lögaðila**</span><span class="sxs-lookup"><span data-stu-id="f9290-148">**Paid by legal entity**</span></span><br><span data-ttu-id="f9290-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="f9290-149">paidbylegalentity</span></span><br><span data-ttu-id="f9290-150">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f9290-150">*String*</span></span> | <span data-ttu-id="f9290-151">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-151">Read-only</span></span><br><span data-ttu-id="f9290-152">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-152">Required</span></span> | <span data-ttu-id="f9290-153">Lögaðilinn sem er skilgreindur fyrir stöðuna sem ber ábyrgð á launagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="f9290-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="f9290-154">**Auðkenni stöðuheitis**</span><span class="sxs-lookup"><span data-stu-id="f9290-154">**Position ID**</span></span><br><span data-ttu-id="f9290-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="f9290-155">mshr_positionid</span></span><br><span data-ttu-id="f9290-156">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="f9290-156">*String*</span></span> | <span data-ttu-id="f9290-157">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-157">Read-only</span></span><br><span data-ttu-id="f9290-158">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-158">Required</span></span> | <span data-ttu-id="f9290-159">Auðkenni stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="f9290-159">The ID of the position.</span></span> |
| <span data-ttu-id="f9290-160">**Gildir til**</span><span class="sxs-lookup"><span data-stu-id="f9290-160">**Valid to**</span></span><br><span data-ttu-id="f9290-161">validto</span><span class="sxs-lookup"><span data-stu-id="f9290-161">validto</span></span><br><span data-ttu-id="f9290-162">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="f9290-162">*Date Time Offset*</span></span> | <span data-ttu-id="f9290-163">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-163">Read-only</span></span><br><span data-ttu-id="f9290-164">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-164">Required</span></span> |<span data-ttu-id="f9290-165">Dagsetningin sem upplýsingar um stöðuna gilda frá.</span><span class="sxs-lookup"><span data-stu-id="f9290-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="f9290-166">**Gildir frá**</span><span class="sxs-lookup"><span data-stu-id="f9290-166">**Valid from**</span></span><br><span data-ttu-id="f9290-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="f9290-167">validfrom</span></span><br><span data-ttu-id="f9290-168">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="f9290-168">*Date Time Offset*</span></span> | <span data-ttu-id="f9290-169">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="f9290-169">Read-only</span></span><br><span data-ttu-id="f9290-170">Krafa</span><span class="sxs-lookup"><span data-stu-id="f9290-170">Required</span></span> |<span data-ttu-id="f9290-171">Dagsetningin sem upplýsingar um stöðuna gilda til.</span><span class="sxs-lookup"><span data-stu-id="f9290-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="f9290-172">**Fyrirspurn**</span><span class="sxs-lookup"><span data-stu-id="f9290-172">**Query**</span></span>

<span data-ttu-id="f9290-173">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="f9290-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="f9290-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="f9290-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
