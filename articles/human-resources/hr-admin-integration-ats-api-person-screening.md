---
title: Skoðun einstaklings
description: Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125378"
---
# <a name="person-screening"></a><span data-ttu-id="cc096-103">Skoðun einstaklings</span><span class="sxs-lookup"><span data-stu-id="cc096-103">Person screening</span></span>

<span data-ttu-id="cc096-104">Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cc096-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cc096-105">Raunlægt heiti: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="cc096-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="cc096-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="cc096-106">Description</span></span>

<span data-ttu-id="cc096-107">Þessi eining lýsir síum sem umsækjandi hefur komist í gegnum eða verður að komast í gegnum til að vera ráðin(n).</span><span class="sxs-lookup"><span data-stu-id="cc096-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cc096-108">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="cc096-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="cc096-109">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="cc096-109">Properties</span></span>

| <span data-ttu-id="cc096-110">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="cc096-110">Property</span></span><br><span data-ttu-id="cc096-111">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="cc096-111">**Physical name**</span></span><br><span data-ttu-id="cc096-112">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="cc096-112">**_Type_**</span></span> | <span data-ttu-id="cc096-113">Nota</span><span class="sxs-lookup"><span data-stu-id="cc096-113">Use</span></span> | <span data-ttu-id="cc096-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="cc096-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cc096-115">**Kenni fyrir einingu einstaklingssíunar**</span><span class="sxs-lookup"><span data-stu-id="cc096-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="cc096-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="cc096-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="cc096-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cc096-117">*GUID*</span></span> | <span data-ttu-id="cc096-118">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="cc096-118">Read-only</span></span><br><span data-ttu-id="cc096-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="cc096-119">Required</span></span><br><span data-ttu-id="cc096-120">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="cc096-120">System-generated</span></span> | <span data-ttu-id="cc096-121">Einkvæmt aðalkenni fyrir síunarfærslur einstaklings.</span><span class="sxs-lookup"><span data-stu-id="cc096-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="cc096-122">**Aðilanúmer**</span><span class="sxs-lookup"><span data-stu-id="cc096-122">**Party Number**</span></span><br><span data-ttu-id="cc096-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="cc096-123">mshr_partynumber</span></span><br><span data-ttu-id="cc096-124">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="cc096-124">*String*</span></span> | <span data-ttu-id="cc096-125">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="cc096-125">Read/write</span></span><br><span data-ttu-id="cc096-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="cc096-126">Required</span></span> | <span data-ttu-id="cc096-127">Númer aðila (einstaklings) sem tengist umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="cc096-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="cc096-128">**Gildi fyrir auðkenni einstaklings**</span><span class="sxs-lookup"><span data-stu-id="cc096-128">**Person ID Value**</span></span><br><span data-ttu-id="cc096-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="cc096-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="cc096-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cc096-130">*GUID*</span></span> | <span data-ttu-id="cc096-131">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="cc096-131">Read-only</span></span><br><span data-ttu-id="cc096-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="cc096-132">Required</span></span><br><span data-ttu-id="cc096-133">Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="cc096-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="cc096-134">Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings).</span><span class="sxs-lookup"><span data-stu-id="cc096-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="cc096-135">**Kenni skoðunargerðar**</span><span class="sxs-lookup"><span data-stu-id="cc096-135">**Screening Type ID**</span></span><br><span data-ttu-id="cc096-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="cc096-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="cc096-137">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="cc096-137">*String*</span></span> | <span data-ttu-id="cc096-138">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="cc096-138">Read/write</span></span><br><span data-ttu-id="cc096-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="cc096-139">Required</span></span><br><span data-ttu-id="cc096-140">Ytri lykill: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="cc096-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="cc096-141">Kenni síugerðar skilgreint í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cc096-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="cc096-142">**Gildi fyrir kenni síugerðar**</span><span class="sxs-lookup"><span data-stu-id="cc096-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="cc096-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="cc096-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="cc096-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cc096-144">*GUID*</span></span> | <span data-ttu-id="cc096-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="cc096-145">Read-only</span></span><br><span data-ttu-id="cc096-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="cc096-146">Required</span></span><br><span data-ttu-id="cc096-147">Framandlykill: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="cc096-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="cc096-148">Einkvæmt kerfismyndað kenni fyrir færslu síugerðar í tengdri einingu.</span><span class="sxs-lookup"><span data-stu-id="cc096-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="cc096-149">**Krafa sett fram af**</span><span class="sxs-lookup"><span data-stu-id="cc096-149">**Required By**</span></span><br><span data-ttu-id="cc096-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="cc096-150">mshr_requiredby</span></span><br><span data-ttu-id="cc096-151">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="cc096-151">*Datetime*</span></span> | <span data-ttu-id="cc096-152">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="cc096-152">Read/write</span></span><br><span data-ttu-id="cc096-153">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="cc096-153">Optional</span></span> | <span data-ttu-id="cc096-154">Dagsetningin sem þarf að klára síunina.</span><span class="sxs-lookup"><span data-stu-id="cc096-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="cc096-155">**Staða**</span><span class="sxs-lookup"><span data-stu-id="cc096-155">**Status**</span></span><br><span data-ttu-id="cc096-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="cc096-156">mshr_status</span></span><br><span data-ttu-id="cc096-157">*mshr_hcmcompletionstatus valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="cc096-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="cc096-158">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="cc096-158">Read/write</span></span><br><span data-ttu-id="cc096-159">Krafa</span><span class="sxs-lookup"><span data-stu-id="cc096-159">Required</span></span> | <span data-ttu-id="cc096-160">Tilgreinir stöðu umsækjanda fyrir síunina.</span><span class="sxs-lookup"><span data-stu-id="cc096-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="cc096-161">**Lokið þann**</span><span class="sxs-lookup"><span data-stu-id="cc096-161">**Completed Date**</span></span><br><span data-ttu-id="cc096-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="cc096-162">mshr_completeddate</span></span><br><span data-ttu-id="cc096-163">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="cc096-163">*Datetime*</span></span> | <span data-ttu-id="cc096-164">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="cc096-164">Read/write</span></span><br><span data-ttu-id="cc096-165">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="cc096-165">Optional</span></span> | <span data-ttu-id="cc096-166">Sagsetning þegarlokið var við skoðun</span><span class="sxs-lookup"><span data-stu-id="cc096-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="cc096-167">**Athugasemdir**</span><span class="sxs-lookup"><span data-stu-id="cc096-167">**Notes**</span></span><br><span data-ttu-id="cc096-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="cc096-168">mshr_note</span></span><br><span data-ttu-id="cc096-169">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="cc096-169">*String*</span></span> | <span data-ttu-id="cc096-170">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="cc096-170">Read/write</span></span><br><span data-ttu-id="cc096-171">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="cc096-171">Optional</span></span> | <span data-ttu-id="cc096-172">Athugasemdir sem ráðningarstjórar og ráðningaraðilar nota.</span><span class="sxs-lookup"><span data-stu-id="cc096-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cc096-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cc096-173">See also</span></span>

[<span data-ttu-id="cc096-174">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="cc096-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cc096-175">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="cc096-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

