---
title: Launafyrirkomulag fastra launa
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launafyrirkomulags fastra launa í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059089"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="62244-103">Launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="62244-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="62244-104">Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launafyrirkomulags fastra launa í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="62244-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="62244-105">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="62244-105">Properties</span></span>

| <span data-ttu-id="62244-106">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="62244-106">Property</span></span><br><span data-ttu-id="62244-107">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="62244-107">**Physical name**</span></span><br><span data-ttu-id="62244-108">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="62244-108">**_Type_**</span></span> | <span data-ttu-id="62244-109">Nota</span><span class="sxs-lookup"><span data-stu-id="62244-109">Use</span></span> | <span data-ttu-id="62244-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="62244-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="62244-111">**Kenni starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="62244-111">**Employee ID**</span></span><br><span data-ttu-id="62244-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="62244-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="62244-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="62244-113">*GUID*</span></span> | <span data-ttu-id="62244-114">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-114">Read-only</span></span><br><span data-ttu-id="62244-115">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-115">Required</span></span><br><span data-ttu-id="62244-116">Framandlykill:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="62244-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="62244-117">Kenni starfsmanns</span><span class="sxs-lookup"><span data-stu-id="62244-117">Employee ID</span></span> |
| <span data-ttu-id="62244-118">**Launataxti**</span><span class="sxs-lookup"><span data-stu-id="62244-118">**Pay rate**</span></span><br><span data-ttu-id="62244-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="62244-119">mshr_payrate</span></span><br><span data-ttu-id="62244-120">*Tugabrot*</span><span class="sxs-lookup"><span data-stu-id="62244-120">*Decimal*</span></span> | <span data-ttu-id="62244-121">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-121">Read-only</span></span><br><span data-ttu-id="62244-122">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-122">Required</span></span> | <span data-ttu-id="62244-123">Launataxti skilgreindur í launafyrirkomulagi fastra launa.</span><span class="sxs-lookup"><span data-stu-id="62244-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="62244-124">**Kenni áætlunar**</span><span class="sxs-lookup"><span data-stu-id="62244-124">**Plan ID**</span></span><br><span data-ttu-id="62244-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="62244-125">mshr_planid</span></span><br><span data-ttu-id="62244-126">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="62244-126">*String*</span></span> | <span data-ttu-id="62244-127">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-127">Read-only</span></span><br><span data-ttu-id="62244-128">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-128">Required</span></span> |<span data-ttu-id="62244-129">Tilgreinir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="62244-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="62244-130">**Gildir frá**</span><span class="sxs-lookup"><span data-stu-id="62244-130">**Valid from**</span></span><br><span data-ttu-id="62244-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="62244-131">mshr_validfrom</span></span><br><span data-ttu-id="62244-132">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="62244-132">*Date Time Offset*</span></span> |  <span data-ttu-id="62244-133">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-133">Read-only</span></span><br><span data-ttu-id="62244-134">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-134">Required</span></span> |<span data-ttu-id="62244-135">Sú dagsetning sem föst laun starfsmanns gilda frá.</span><span class="sxs-lookup"><span data-stu-id="62244-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="62244-136">**Eining launafyrirkomulags fastra launa**</span><span class="sxs-lookup"><span data-stu-id="62244-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="62244-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="62244-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="62244-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="62244-138">*GUID*</span></span> | <span data-ttu-id="62244-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-139">Required</span></span><br><span data-ttu-id="62244-140">Búið til af kerfi</span><span class="sxs-lookup"><span data-stu-id="62244-140">Sytem generated</span></span> | <span data-ttu-id="62244-141">GUID-gildi myndað af kerfinu til að auðkenna launafyrirkomulag á einkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="62244-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="62244-142">**Greiðslutíðni**</span><span class="sxs-lookup"><span data-stu-id="62244-142">**Pay frequency**</span></span><br><span data-ttu-id="62244-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="62244-143">mshr_payfrequency</span></span><br><span data-ttu-id="62244-144">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="62244-144">*String*</span></span> | <span data-ttu-id="62244-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-145">Read-only</span></span><br><span data-ttu-id="62244-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-146">Required</span></span> |<span data-ttu-id="62244-147">Tíðnin sem starfsmaðurinn fær greitt.</span><span class="sxs-lookup"><span data-stu-id="62244-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="62244-148">**Gildir til**</span><span class="sxs-lookup"><span data-stu-id="62244-148">**Valid to**</span></span><br><span data-ttu-id="62244-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="62244-149">mshr_validto</span></span><br><span data-ttu-id="62244-150">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="62244-150">*Date Time Offset*</span></span> | <span data-ttu-id="62244-151">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-151">Read-only</span></span> <br><span data-ttu-id="62244-152">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-152">Required</span></span> | <span data-ttu-id="62244-153">Sú dagsetning sem föst laun starfsmanns gilda til.</span><span class="sxs-lookup"><span data-stu-id="62244-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="62244-154">**Auðkenni stöðuheitis**</span><span class="sxs-lookup"><span data-stu-id="62244-154">**Position ID**</span></span><br><span data-ttu-id="62244-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="62244-155">mshr_positionid</span></span><br><span data-ttu-id="62244-156">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="62244-156">*String*</span></span> | <span data-ttu-id="62244-157">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-157">Read-only</span></span> <br><span data-ttu-id="62244-158">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-158">Required</span></span> | <span data-ttu-id="62244-159">Auðkenni stöðu sem tengist skráningu starfsmanns og launafyrirkomulags fastra launa.</span><span class="sxs-lookup"><span data-stu-id="62244-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="62244-160">**Gjaldmiðill**</span><span class="sxs-lookup"><span data-stu-id="62244-160">**Currency**</span></span><br><span data-ttu-id="62244-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="62244-161">mshr_currency</span></span><br><span data-ttu-id="62244-162">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="62244-162">*String*</span></span> | <span data-ttu-id="62244-163">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-163">Read-only</span></span> <br><span data-ttu-id="62244-164">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-164">Required</span></span> |<span data-ttu-id="62244-165">Gjaldmiðillinn sem er skilgreindur fyrir launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="62244-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="62244-166">**Númer starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="62244-166">**Personnel number**</span></span><br><span data-ttu-id="62244-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="62244-167">mshr_personnelnumber</span></span><br><span data-ttu-id="62244-168">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="62244-168">*String*</span></span> | <span data-ttu-id="62244-169">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="62244-169">Read-only</span></span><br><span data-ttu-id="62244-170">Krafa</span><span class="sxs-lookup"><span data-stu-id="62244-170">Required</span></span> |<span data-ttu-id="62244-171">Einkvæmt númer starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="62244-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="62244-172">**Fyrirspurn**</span><span class="sxs-lookup"><span data-stu-id="62244-172">**Query**</span></span>

<span data-ttu-id="62244-173">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="62244-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="62244-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="62244-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
