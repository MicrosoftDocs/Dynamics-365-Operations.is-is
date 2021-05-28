---
title: Launaupplýsingar fyrir stöður
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019323"
---
# <a name="payroll-position"></a><span data-ttu-id="3bda9-103">Launastaða</span><span class="sxs-lookup"><span data-stu-id="3bda9-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3bda9-104">Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3bda9-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3bda9-105">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="3bda9-105">Properties</span></span>

| <span data-ttu-id="3bda9-106">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="3bda9-106">Property</span></span><br><span data-ttu-id="3bda9-107">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="3bda9-107">**Physical name**</span></span><br><span data-ttu-id="3bda9-108">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="3bda9-108">**_Type_**</span></span> | <span data-ttu-id="3bda9-109">Nota</span><span class="sxs-lookup"><span data-stu-id="3bda9-109">Use</span></span> | <span data-ttu-id="3bda9-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="3bda9-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3bda9-111">**Reglulegar árlegar vinnustundir**</span><span class="sxs-lookup"><span data-stu-id="3bda9-111">**Annual regular hours**</span></span><br><span data-ttu-id="3bda9-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="3bda9-112">annualregularhours</span></span><br><span data-ttu-id="3bda9-113">*Tugabrot*</span><span class="sxs-lookup"><span data-stu-id="3bda9-113">*Decimal*</span></span> | <span data-ttu-id="3bda9-114">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-114">Read-only</span></span><br><span data-ttu-id="3bda9-115">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-115">Required</span></span> | <span data-ttu-id="3bda9-116">Reglulegar árlegar vinnustundir skilgreindar fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="3bda9-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="3bda9-117">**Einingarkenni fyrir upplýsingar um launastöðu**</span><span class="sxs-lookup"><span data-stu-id="3bda9-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="3bda9-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="3bda9-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="3bda9-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="3bda9-119">*Guid*</span></span> | <span data-ttu-id="3bda9-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-120">Required</span></span><br><span data-ttu-id="3bda9-121">Búið til af kerfi.</span><span class="sxs-lookup"><span data-stu-id="3bda9-121">System generated.</span></span> | <span data-ttu-id="3bda9-122">GUID-gildi myndað af kerfinu til að auðkenna stöðu á einkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="3bda9-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="3bda9-123">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="3bda9-123">**Primary field**</span></span><br><span data-ttu-id="3bda9-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3bda9-124">mshr_primaryfield</span></span><br><span data-ttu-id="3bda9-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="3bda9-125">*String*</span></span> | <span data-ttu-id="3bda9-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-126">Required</span></span><br><span data-ttu-id="3bda9-127">Búið til af kerfi</span><span class="sxs-lookup"><span data-stu-id="3bda9-127">System generated</span></span> |  |
| <span data-ttu-id="3bda9-128">**Gildi fyrir kenni vinnustöðu**</span><span class="sxs-lookup"><span data-stu-id="3bda9-128">**Position job ID value**</span></span><br><span data-ttu-id="3bda9-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="3bda9-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="3bda9-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3bda9-130">*GUID*</span></span> | <span data-ttu-id="3bda9-131">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-131">Read-only</span></span><br><span data-ttu-id="3bda9-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-132">Required</span></span><br><span data-ttu-id="3bda9-133">Framandlykill:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="3bda9-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="3bda9-134">Kenni starfsins sem tengist stöðunni.</span><span class="sxs-lookup"><span data-stu-id="3bda9-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="3bda9-135">**Gildi fyrir kenni launafyrirkomulags fastra launa**</span><span class="sxs-lookup"><span data-stu-id="3bda9-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="3bda9-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="3bda9-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="3bda9-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3bda9-137">*GUID*</span></span> | <span data-ttu-id="3bda9-138">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-138">Read-only</span></span><br><span data-ttu-id="3bda9-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-139">Required</span></span><br><span data-ttu-id="3bda9-140">Framandlykill: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="3bda9-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="3bda9-141">Kenni launafyrirkomulags fastra launa sem tengist stöðunni.</span><span class="sxs-lookup"><span data-stu-id="3bda9-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="3bda9-142">**Kenni greiðsluferlis**</span><span class="sxs-lookup"><span data-stu-id="3bda9-142">**Pay cycle ID**</span></span><br><span data-ttu-id="3bda9-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3bda9-143">mshr_primaryfield</span></span><br><span data-ttu-id="3bda9-144">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="3bda9-144">*String*</span></span> | <span data-ttu-id="3bda9-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-145">Read-only</span></span><br><span data-ttu-id="3bda9-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-146">Required</span></span> | <span data-ttu-id="3bda9-147">Greiðsluferli skilgreint fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="3bda9-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="3bda9-148">**Greitt af lögaðila**</span><span class="sxs-lookup"><span data-stu-id="3bda9-148">**Paid by legal entity**</span></span><br><span data-ttu-id="3bda9-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="3bda9-149">paidbylegalentity</span></span><br><span data-ttu-id="3bda9-150">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="3bda9-150">*String*</span></span> | <span data-ttu-id="3bda9-151">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-151">Read-only</span></span><br><span data-ttu-id="3bda9-152">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-152">Required</span></span> | <span data-ttu-id="3bda9-153">Lögaðilinn sem er skilgreindur fyrir stöðuna sem ber ábyrgð á launagreiðslum.</span><span class="sxs-lookup"><span data-stu-id="3bda9-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="3bda9-154">**Auðkenni stöðuheitis**</span><span class="sxs-lookup"><span data-stu-id="3bda9-154">**Position ID**</span></span><br><span data-ttu-id="3bda9-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="3bda9-155">mshr_positionid</span></span><br><span data-ttu-id="3bda9-156">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="3bda9-156">*String*</span></span> | <span data-ttu-id="3bda9-157">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-157">Read-only</span></span><br><span data-ttu-id="3bda9-158">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-158">Required</span></span> | <span data-ttu-id="3bda9-159">Auðkenni stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="3bda9-159">The ID of the position.</span></span> |
| <span data-ttu-id="3bda9-160">**Gildir til**</span><span class="sxs-lookup"><span data-stu-id="3bda9-160">**Valid to**</span></span><br><span data-ttu-id="3bda9-161">validto</span><span class="sxs-lookup"><span data-stu-id="3bda9-161">validto</span></span><br><span data-ttu-id="3bda9-162">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="3bda9-162">*Date Time Offset*</span></span> | <span data-ttu-id="3bda9-163">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-163">Read-only</span></span><br><span data-ttu-id="3bda9-164">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-164">Required</span></span> |<span data-ttu-id="3bda9-165">Dagsetningin sem upplýsingar um stöðuna gilda frá.</span><span class="sxs-lookup"><span data-stu-id="3bda9-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="3bda9-166">**Gildir frá**</span><span class="sxs-lookup"><span data-stu-id="3bda9-166">**Valid from**</span></span><br><span data-ttu-id="3bda9-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="3bda9-167">validfrom</span></span><br><span data-ttu-id="3bda9-168">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="3bda9-168">*Date Time Offset*</span></span> | <span data-ttu-id="3bda9-169">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="3bda9-169">Read-only</span></span><br><span data-ttu-id="3bda9-170">Krafa</span><span class="sxs-lookup"><span data-stu-id="3bda9-170">Required</span></span> |<span data-ttu-id="3bda9-171">Dagsetningin sem upplýsingar um stöðuna gilda til.</span><span class="sxs-lookup"><span data-stu-id="3bda9-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="3bda9-172">**Fyrirspurn**</span><span class="sxs-lookup"><span data-stu-id="3bda9-172">**Query**</span></span>

<span data-ttu-id="3bda9-173">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="3bda9-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="3bda9-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="3bda9-174">**Response**</span></span>

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
