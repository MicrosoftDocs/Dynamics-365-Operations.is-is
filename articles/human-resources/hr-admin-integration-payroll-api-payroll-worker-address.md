---
title: Heimilisfang starfskrafts á launaskrá
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu aðseturs fyrir starfsmann á launaskrá í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052290"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="7423d-103">Heimilisfang starfskrafts á launaskrá</span><span class="sxs-lookup"><span data-stu-id="7423d-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7423d-104">Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu aðseturs fyrir starfsmann á launaskrá í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7423d-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="7423d-105">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="7423d-105">Properties</span></span>

| <span data-ttu-id="7423d-106">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="7423d-106">Property</span></span><br><span data-ttu-id="7423d-107">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="7423d-107">**Physical name**</span></span><br><span data-ttu-id="7423d-108">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="7423d-108">**_Type_**</span></span> | <span data-ttu-id="7423d-109">Nota</span><span class="sxs-lookup"><span data-stu-id="7423d-109">Use</span></span> | <span data-ttu-id="7423d-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="7423d-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7423d-111">**Póststöð**</span><span class="sxs-lookup"><span data-stu-id="7423d-111">**City**</span></span><br><span data-ttu-id="7423d-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="7423d-112">mshr_city</span></span><br><span data-ttu-id="7423d-113">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-113">*String*</span></span> | <span data-ttu-id="7423d-114">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-114">Read-only</span></span><br><span data-ttu-id="7423d-115">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-115">Required</span></span> | <span data-ttu-id="7423d-116">Borgin sem er skilgreind fyrir aðsetrið.</span><span class="sxs-lookup"><span data-stu-id="7423d-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="7423d-117">**Númer starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="7423d-117">**Personnel number**</span></span><br><span data-ttu-id="7423d-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="7423d-118">mshr_personnelnumber</span></span><br><span data-ttu-id="7423d-119">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-119">*String*</span></span> | <span data-ttu-id="7423d-120">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-120">Read-only</span></span><br><span data-ttu-id="7423d-121">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-121">Required</span></span> | <span data-ttu-id="7423d-122">Einkvæmt númer starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7423d-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="7423d-123">**Landsvæði**</span><span class="sxs-lookup"><span data-stu-id="7423d-123">**Country region**</span></span><br><span data-ttu-id="7423d-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="7423d-124">mshr_countryregionid</span></span><br><span data-ttu-id="7423d-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-125">*String*</span></span> | <span data-ttu-id="7423d-126">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-126">Read-only</span></span><br><span data-ttu-id="7423d-127">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-127">Required</span></span> | <span data-ttu-id="7423d-128">Landsvæðið sem er skilgreint fyrir heimilisfangið</span><span class="sxs-lookup"><span data-stu-id="7423d-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="7423d-129">**Gildir frá**</span><span class="sxs-lookup"><span data-stu-id="7423d-129">**Valid from**</span></span><br><span data-ttu-id="7423d-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="7423d-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="7423d-131">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="7423d-131">*Date Time Offset*</span></span> | <span data-ttu-id="7423d-132">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-132">Read-only</span></span> <br><span data-ttu-id="7423d-133">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-133">Required</span></span> | <span data-ttu-id="7423d-134">Dagsetningin sem aðsetrið gildir frá.</span><span class="sxs-lookup"><span data-stu-id="7423d-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="7423d-135">**Starfað á aðsetri**</span><span class="sxs-lookup"><span data-stu-id="7423d-135">**Worked in address**</span></span><br><span data-ttu-id="7423d-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="7423d-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="7423d-137">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-137">Read-only</span></span><br><span data-ttu-id="7423d-138">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-138">Required</span></span> | <span data-ttu-id="7423d-139">Táknar hvort starfsmaðurinn starfi á viðkomandi heimilisfangi.</span><span class="sxs-lookup"><span data-stu-id="7423d-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="7423d-140">**Sýsla**</span><span class="sxs-lookup"><span data-stu-id="7423d-140">**County**</span></span><br><span data-ttu-id="7423d-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="7423d-141">mshr_county</span></span><br><span data-ttu-id="7423d-142">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-142">*String*</span></span> | <span data-ttu-id="7423d-143">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-143">Read-only</span></span><br><span data-ttu-id="7423d-144">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-144">Required</span></span> | <span data-ttu-id="7423d-145">Sýsla sem er skilgreind fyrir aðsetrið.</span><span class="sxs-lookup"><span data-stu-id="7423d-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="7423d-146">**Kenni heimilisfangs starfskrafts á launaskrá**</span><span class="sxs-lookup"><span data-stu-id="7423d-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="7423d-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="7423d-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="7423d-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7423d-148">*GUID*</span></span> | <span data-ttu-id="7423d-149">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-149">Required</span></span><br><span data-ttu-id="7423d-150">Búið til af kerfi</span><span class="sxs-lookup"><span data-stu-id="7423d-150">System generated</span></span> | <span data-ttu-id="7423d-151">GUID-gildi myndað af kerfinu til að auðkenna heimilisfang á einkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="7423d-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="7423d-152">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="7423d-152">**Primary field**</span></span><br><span data-ttu-id="7423d-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="7423d-153">mshr_primaryfield</span></span><br><span data-ttu-id="7423d-154">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-154">*String*</span></span> | <span data-ttu-id="7423d-155">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-155">Read-only</span></span><br><span data-ttu-id="7423d-156">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-156">Required</span></span> |  |
| <span data-ttu-id="7423d-157">**Gata**</span><span class="sxs-lookup"><span data-stu-id="7423d-157">**Street**</span></span><br><span data-ttu-id="7423d-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="7423d-158">mshr_street</span></span><br><span data-ttu-id="7423d-159">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-159">*String*</span></span> | <span data-ttu-id="7423d-160">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-160">Read-only</span></span><br><span data-ttu-id="7423d-161">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-161">Required</span></span> | <span data-ttu-id="7423d-162">Gatan sem er skilgreind fyrir aðsetrið.</span><span class="sxs-lookup"><span data-stu-id="7423d-162">The street defined for the address.</span></span> |
| <span data-ttu-id="7423d-163">**Gildir til**</span><span class="sxs-lookup"><span data-stu-id="7423d-163">**Valid to**</span></span><br><span data-ttu-id="7423d-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="7423d-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="7423d-165">*Mótfærð dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="7423d-165">*Date Time Offset*</span></span> | <span data-ttu-id="7423d-166">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-166">Read-only</span></span> <br><span data-ttu-id="7423d-167">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-167">Required</span></span> | <span data-ttu-id="7423d-168">Dagsetningin sem aðsetrið gildir til.</span><span class="sxs-lookup"><span data-stu-id="7423d-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="7423d-169">**Staðsetningarkenni**</span><span class="sxs-lookup"><span data-stu-id="7423d-169">**Location ID**</span></span><br><span data-ttu-id="7423d-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="7423d-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="7423d-171">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-171">Read-only</span></span> <br><span data-ttu-id="7423d-172">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-172">Required</span></span> | <span data-ttu-id="7423d-173">Auðkenni aðsetursins.</span><span class="sxs-lookup"><span data-stu-id="7423d-173">The ID for the address.</span></span>  |
| <span data-ttu-id="7423d-174">**Póstnúmer**</span><span class="sxs-lookup"><span data-stu-id="7423d-174">**Postal code**</span></span><br><span data-ttu-id="7423d-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="7423d-175">mshr_zipcode</span></span><br><span data-ttu-id="7423d-176">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-176">*String*</span></span> | <span data-ttu-id="7423d-177">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-177">Read-only</span></span> <br><span data-ttu-id="7423d-178">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-178">Required</span></span> |<span data-ttu-id="7423d-179">Auðkennisnúmerið sem er skilgreint fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="7423d-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="7423d-180">**Bjó á aðsetri**</span><span class="sxs-lookup"><span data-stu-id="7423d-180">**Lived in address**</span></span><br><span data-ttu-id="7423d-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="7423d-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="7423d-182">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-182">Read-only</span></span><br><span data-ttu-id="7423d-183">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-183">Required</span></span> | <span data-ttu-id="7423d-184">Táknar hvort starfsmaðurinn búi á viðkomandi heimilisfangi.</span><span class="sxs-lookup"><span data-stu-id="7423d-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="7423d-185">**Ríki**</span><span class="sxs-lookup"><span data-stu-id="7423d-185">**State**</span></span><br><span data-ttu-id="7423d-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="7423d-186">mshr_state</span></span><br><span data-ttu-id="7423d-187">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7423d-187">*String*</span></span> | <span data-ttu-id="7423d-188">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="7423d-188">Read-only</span></span><br><span data-ttu-id="7423d-189">Krafa</span><span class="sxs-lookup"><span data-stu-id="7423d-189">Required</span></span> | <span data-ttu-id="7423d-190">Fylkið sem er skilgreint fyrir aðsetrið.</span><span class="sxs-lookup"><span data-stu-id="7423d-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="7423d-191">Dæmi um fyrirspurn</span><span class="sxs-lookup"><span data-stu-id="7423d-191">Example query</span></span>

<span data-ttu-id="7423d-192">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="7423d-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="7423d-193">**Svar**</span><span class="sxs-lookup"><span data-stu-id="7423d-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
