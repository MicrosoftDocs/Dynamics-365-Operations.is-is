---
title: Launaupplýsingar fyrir stöður
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056781"
---
# <a name="payroll-position"></a><span data-ttu-id="13ddb-103">Launastaða</span><span class="sxs-lookup"><span data-stu-id="13ddb-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="13ddb-104">Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="13ddb-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="13ddb-105">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="13ddb-105">Properties</span></span>

| <span data-ttu-id="13ddb-106">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="13ddb-106">Property</span></span><br><span data-ttu-id="13ddb-107">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="13ddb-107">**Physical name**</span></span><br><span data-ttu-id="13ddb-108">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="13ddb-108">**_Type_**</span></span> | <span data-ttu-id="13ddb-109">Nota</span><span class="sxs-lookup"><span data-stu-id="13ddb-109">Use</span></span> | <span data-ttu-id="13ddb-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="13ddb-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="13ddb-111">**Reglulegar árlegar vinnustundir**</span><span class="sxs-lookup"><span data-stu-id="13ddb-111">**Annual regular hours**</span></span><br><span data-ttu-id="13ddb-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="13ddb-112">annualregularhours</span></span><br><span data-ttu-id="13ddb-113">*Tugabrot*</span><span class="sxs-lookup"><span data-stu-id="13ddb-113">*Decimal*</span></span> | <span data-ttu-id="13ddb-114">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-114">Read-only</span></span><br><span data-ttu-id="13ddb-115">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-115">Required</span></span> | <span data-ttu-id="13ddb-116">Reglulegar árlegar vinnustundir skilgreindar fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="13ddb-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="13ddb-117">**Einingarkenni fyrir upplýsingar um launastöðu**</span><span class="sxs-lookup"><span data-stu-id="13ddb-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="13ddb-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="13ddb-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="13ddb-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="13ddb-119">*Guid*</span></span> | <span data-ttu-id="13ddb-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-120">Required</span></span><br><span data-ttu-id="13ddb-121">Búið til af kerfi.</span><span class="sxs-lookup"><span data-stu-id="13ddb-121">System generated.</span></span> | <span data-ttu-id="13ddb-122">GUID-gildi myndað af kerfinu til að auðkenna stöðu á einkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="13ddb-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="13ddb-123">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="13ddb-123">**Primary field**</span></span><br><span data-ttu-id="13ddb-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="13ddb-124">mshr_primaryfield</span></span><br><span data-ttu-id="13ddb-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="13ddb-125">*String*</span></span> | <span data-ttu-id="13ddb-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-126">Required</span></span><br><span data-ttu-id="13ddb-127">Búið til af kerfi</span><span class="sxs-lookup"><span data-stu-id="13ddb-127">System generated</span></span> |  |
| <span data-ttu-id="13ddb-128">**Gildi fyrir kenni vinnustöðu**</span><span class="sxs-lookup"><span data-stu-id="13ddb-128">**Position job ID value**</span></span><br><span data-ttu-id="13ddb-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="13ddb-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="13ddb-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="13ddb-130">*GUID*</span></span> | <span data-ttu-id="13ddb-131">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-131">Read-only</span></span><br><span data-ttu-id="13ddb-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-132">Required</span></span><br><span data-ttu-id="13ddb-133">Framandlykill:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="13ddb-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="13ddb-134">Kenni starfsins sem tengist stöðunni.</span><span class="sxs-lookup"><span data-stu-id="13ddb-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="13ddb-135">**Gildi fyrir kenni launafyrirkomulags fastra launa**</span><span class="sxs-lookup"><span data-stu-id="13ddb-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="13ddb-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="13ddb-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="13ddb-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="13ddb-137">*GUID*</span></span> | <span data-ttu-id="13ddb-138">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-138">Read-only</span></span><br><span data-ttu-id="13ddb-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-139">Required</span></span><br><span data-ttu-id="13ddb-140">Framandlykill: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="13ddb-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="13ddb-141">Kenni launafyrirkomulags fastra launa sem tengist stöðunni.</span><span class="sxs-lookup"><span data-stu-id="13ddb-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="13ddb-142">**Kenni greiðsluferlis**</span><span class="sxs-lookup"><span data-stu-id="13ddb-142">**Pay cycle ID**</span></span><br><span data-ttu-id="13ddb-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="13ddb-143">mshr_primaryfield</span></span><br><span data-ttu-id="13ddb-144">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="13ddb-144">*String*</span></span> | <span data-ttu-id="13ddb-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-145">Read-only</span></span><br><span data-ttu-id="13ddb-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-146">Required</span></span> | <span data-ttu-id="13ddb-147">Greiðsluferli skilgreint fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="13ddb-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="13ddb-148">**Greitt af lögaðila**</span><span class="sxs-lookup"><span data-stu-id="13ddb-148">**Paid by legal entity**</span></span><br><span data-ttu-id="13ddb-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="13ddb-149">paidbylegalentity</span></span><br><span data-ttu-id="13ddb-150">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="13ddb-150">*String*</span></span> | <span data-ttu-id="13ddb-151">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-151">Read-only</span></span><br><span data-ttu-id="13ddb-152">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-152">Required</span></span> | <span data-ttu-id="13ddb-153">Lögaðilinn sem er skilgreindur fyrir stöðuna sem ber ábyrgð á launagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="13ddb-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="13ddb-154">**Auðkenni stöðuheitis**</span><span class="sxs-lookup"><span data-stu-id="13ddb-154">**Position ID**</span></span><br><span data-ttu-id="13ddb-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="13ddb-155">mshr_positionid</span></span><br><span data-ttu-id="13ddb-156">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="13ddb-156">*String*</span></span> | <span data-ttu-id="13ddb-157">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-157">Read-only</span></span><br><span data-ttu-id="13ddb-158">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-158">Required</span></span> | <span data-ttu-id="13ddb-159">Auðkenni stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="13ddb-159">The ID of the position.</span></span> |
| <span data-ttu-id="13ddb-160">**Gildir til**</span><span class="sxs-lookup"><span data-stu-id="13ddb-160">**Valid to**</span></span><br><span data-ttu-id="13ddb-161">validto</span><span class="sxs-lookup"><span data-stu-id="13ddb-161">validto</span></span><br><span data-ttu-id="13ddb-162">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="13ddb-162">*Date Time Offset*</span></span> | <span data-ttu-id="13ddb-163">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-163">Read-only</span></span><br><span data-ttu-id="13ddb-164">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-164">Required</span></span> |<span data-ttu-id="13ddb-165">Dagsetningin sem upplýsingar um stöðuna gilda frá.</span><span class="sxs-lookup"><span data-stu-id="13ddb-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="13ddb-166">**Gildir frá**</span><span class="sxs-lookup"><span data-stu-id="13ddb-166">**Valid from**</span></span><br><span data-ttu-id="13ddb-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="13ddb-167">validfrom</span></span><br><span data-ttu-id="13ddb-168">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="13ddb-168">*Date Time Offset*</span></span> | <span data-ttu-id="13ddb-169">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="13ddb-169">Read-only</span></span><br><span data-ttu-id="13ddb-170">Krafa</span><span class="sxs-lookup"><span data-stu-id="13ddb-170">Required</span></span> |<span data-ttu-id="13ddb-171">Dagsetningin sem upplýsingar um stöðuna gilda til.</span><span class="sxs-lookup"><span data-stu-id="13ddb-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="13ddb-172">**Fyrirspurn**</span><span class="sxs-lookup"><span data-stu-id="13ddb-172">**Query**</span></span>

<span data-ttu-id="13ddb-173">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="13ddb-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="13ddb-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="13ddb-174">**Response**</span></span>

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
