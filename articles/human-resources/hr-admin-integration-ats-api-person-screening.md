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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467242"
---
# <a name="person-screening"></a><span data-ttu-id="ea449-103">Skoðun einstaklings</span><span class="sxs-lookup"><span data-stu-id="ea449-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ea449-104">Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea449-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ea449-105">Raunlægt heiti: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="ea449-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="ea449-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="ea449-106">Description</span></span>

<span data-ttu-id="ea449-107">Þessi eining lýsir síum sem umsækjandi hefur komist í gegnum eða verður að komast í gegnum til að vera ráðin(n).</span><span class="sxs-lookup"><span data-stu-id="ea449-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea449-108">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="ea449-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="ea449-109">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="ea449-109">Properties</span></span>

| <span data-ttu-id="ea449-110">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="ea449-110">Property</span></span><br><span data-ttu-id="ea449-111">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="ea449-111">**Physical name**</span></span><br><span data-ttu-id="ea449-112">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="ea449-112">**_Type_**</span></span> | <span data-ttu-id="ea449-113">Nota</span><span class="sxs-lookup"><span data-stu-id="ea449-113">Use</span></span> | <span data-ttu-id="ea449-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="ea449-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ea449-115">**Kenni fyrir einingu einstaklingssíunar**</span><span class="sxs-lookup"><span data-stu-id="ea449-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="ea449-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="ea449-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="ea449-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea449-117">*GUID*</span></span> | <span data-ttu-id="ea449-118">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="ea449-118">Read-only</span></span><br><span data-ttu-id="ea449-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea449-119">Required</span></span><br><span data-ttu-id="ea449-120">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="ea449-120">System-generated</span></span> | <span data-ttu-id="ea449-121">Einkvæmt aðalkenni fyrir síunarfærslur einstaklings.</span><span class="sxs-lookup"><span data-stu-id="ea449-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="ea449-122">**Aðilanúmer**</span><span class="sxs-lookup"><span data-stu-id="ea449-122">**Party Number**</span></span><br><span data-ttu-id="ea449-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="ea449-123">mshr_partynumber</span></span><br><span data-ttu-id="ea449-124">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea449-124">*String*</span></span> | <span data-ttu-id="ea449-125">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea449-125">Read/write</span></span><br><span data-ttu-id="ea449-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea449-126">Required</span></span> | <span data-ttu-id="ea449-127">Númer aðila (einstaklings) sem tengist umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="ea449-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="ea449-128">**Gildi fyrir auðkenni einstaklings**</span><span class="sxs-lookup"><span data-stu-id="ea449-128">**Person ID Value**</span></span><br><span data-ttu-id="ea449-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="ea449-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="ea449-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea449-130">*GUID*</span></span> | <span data-ttu-id="ea449-131">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="ea449-131">Read-only</span></span><br><span data-ttu-id="ea449-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea449-132">Required</span></span><br><span data-ttu-id="ea449-133">Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="ea449-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="ea449-134">Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings).</span><span class="sxs-lookup"><span data-stu-id="ea449-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="ea449-135">**Kenni skoðunargerðar**</span><span class="sxs-lookup"><span data-stu-id="ea449-135">**Screening Type ID**</span></span><br><span data-ttu-id="ea449-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="ea449-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="ea449-137">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea449-137">*String*</span></span> | <span data-ttu-id="ea449-138">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea449-138">Read/write</span></span><br><span data-ttu-id="ea449-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea449-139">Required</span></span><br><span data-ttu-id="ea449-140">Ytri lykill: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="ea449-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="ea449-141">Kenni síugerðar skilgreint í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea449-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="ea449-142">**Gildi fyrir kenni síugerðar**</span><span class="sxs-lookup"><span data-stu-id="ea449-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="ea449-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="ea449-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="ea449-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea449-144">*GUID*</span></span> | <span data-ttu-id="ea449-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="ea449-145">Read-only</span></span><br><span data-ttu-id="ea449-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea449-146">Required</span></span><br><span data-ttu-id="ea449-147">Framandlykill: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="ea449-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="ea449-148">Einkvæmt kerfismyndað kenni fyrir færslu síugerðar í tengdri einingu.</span><span class="sxs-lookup"><span data-stu-id="ea449-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="ea449-149">**Krafa sett fram af**</span><span class="sxs-lookup"><span data-stu-id="ea449-149">**Required By**</span></span><br><span data-ttu-id="ea449-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="ea449-150">mshr_requiredby</span></span><br><span data-ttu-id="ea449-151">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="ea449-151">*Datetime*</span></span> | <span data-ttu-id="ea449-152">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea449-152">Read/write</span></span><br><span data-ttu-id="ea449-153">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="ea449-153">Optional</span></span> | <span data-ttu-id="ea449-154">Dagsetningin sem þarf að klára síunina.</span><span class="sxs-lookup"><span data-stu-id="ea449-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="ea449-155">**Staða**</span><span class="sxs-lookup"><span data-stu-id="ea449-155">**Status**</span></span><br><span data-ttu-id="ea449-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="ea449-156">mshr_status</span></span><br><span data-ttu-id="ea449-157">*mshr_hcmcompletionstatus valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="ea449-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="ea449-158">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea449-158">Read/write</span></span><br><span data-ttu-id="ea449-159">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea449-159">Required</span></span> | <span data-ttu-id="ea449-160">Tilgreinir stöðu umsækjanda fyrir síunina.</span><span class="sxs-lookup"><span data-stu-id="ea449-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="ea449-161">**Lokið þann**</span><span class="sxs-lookup"><span data-stu-id="ea449-161">**Completed Date**</span></span><br><span data-ttu-id="ea449-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="ea449-162">mshr_completeddate</span></span><br><span data-ttu-id="ea449-163">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="ea449-163">*Datetime*</span></span> | <span data-ttu-id="ea449-164">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea449-164">Read/write</span></span><br><span data-ttu-id="ea449-165">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="ea449-165">Optional</span></span> | <span data-ttu-id="ea449-166">Sagsetning þegarlokið var við skoðun</span><span class="sxs-lookup"><span data-stu-id="ea449-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="ea449-167">**Athugasemdir**</span><span class="sxs-lookup"><span data-stu-id="ea449-167">**Notes**</span></span><br><span data-ttu-id="ea449-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="ea449-168">mshr_note</span></span><br><span data-ttu-id="ea449-169">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea449-169">*String*</span></span> | <span data-ttu-id="ea449-170">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea449-170">Read/write</span></span><br><span data-ttu-id="ea449-171">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="ea449-171">Optional</span></span> | <span data-ttu-id="ea449-172">Athugasemdir sem ráðningarstjórar og ráðningaraðilar nota.</span><span class="sxs-lookup"><span data-stu-id="ea449-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea449-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ea449-173">See also</span></span>

[<span data-ttu-id="ea449-174">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="ea449-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ea449-175">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="ea449-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]