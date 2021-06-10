---
title: Skoðun einstaklings
description: Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059281"
---
# <a name="person-screening"></a><span data-ttu-id="ea4cd-103">Skoðun einstaklings</span><span class="sxs-lookup"><span data-stu-id="ea4cd-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ea4cd-104">Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ea4cd-105">Raunlægt heiti: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="ea4cd-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="ea4cd-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="ea4cd-106">Description</span></span>

<span data-ttu-id="ea4cd-107">Þessi eining lýsir síum sem umsækjandi hefur komist í gegnum eða verður að komast í gegnum til að vera ráðin(n).</span><span class="sxs-lookup"><span data-stu-id="ea4cd-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea4cd-108">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="ea4cd-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="ea4cd-109">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="ea4cd-109">Properties</span></span>

| <span data-ttu-id="ea4cd-110">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="ea4cd-110">Property</span></span><br><span data-ttu-id="ea4cd-111">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-111">**Physical name**</span></span><br><span data-ttu-id="ea4cd-112">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-112">**_Type_**</span></span> | <span data-ttu-id="ea4cd-113">Nota</span><span class="sxs-lookup"><span data-stu-id="ea4cd-113">Use</span></span> | <span data-ttu-id="ea4cd-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="ea4cd-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ea4cd-115">**Kenni fyrir einingu einstaklingssíunar**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="ea4cd-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="ea4cd-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="ea4cd-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-117">*GUID*</span></span> | <span data-ttu-id="ea4cd-118">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="ea4cd-118">Read-only</span></span><br><span data-ttu-id="ea4cd-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-119">Required</span></span><br><span data-ttu-id="ea4cd-120">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="ea4cd-120">System-generated</span></span> | <span data-ttu-id="ea4cd-121">Einkvæmt aðalkenni fyrir síunarfærslur einstaklings.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="ea4cd-122">**Aðilanúmer**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-122">**Party Number**</span></span><br><span data-ttu-id="ea4cd-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="ea4cd-123">mshr_partynumber</span></span><br><span data-ttu-id="ea4cd-124">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-124">*String*</span></span> | <span data-ttu-id="ea4cd-125">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-125">Read/write</span></span><br><span data-ttu-id="ea4cd-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-126">Required</span></span> | <span data-ttu-id="ea4cd-127">Númer aðila (einstaklings) sem tengist umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="ea4cd-128">**Gildi fyrir auðkenni einstaklings**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-128">**Person ID Value**</span></span><br><span data-ttu-id="ea4cd-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="ea4cd-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="ea4cd-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-130">*GUID*</span></span> | <span data-ttu-id="ea4cd-131">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="ea4cd-131">Read-only</span></span><br><span data-ttu-id="ea4cd-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-132">Required</span></span><br><span data-ttu-id="ea4cd-133">Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="ea4cd-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="ea4cd-134">Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings).</span><span class="sxs-lookup"><span data-stu-id="ea4cd-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="ea4cd-135">**Kenni skoðunargerðar**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-135">**Screening Type ID**</span></span><br><span data-ttu-id="ea4cd-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="ea4cd-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="ea4cd-137">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-137">*String*</span></span> | <span data-ttu-id="ea4cd-138">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-138">Read/write</span></span><br><span data-ttu-id="ea4cd-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-139">Required</span></span><br><span data-ttu-id="ea4cd-140">Ytri lykill: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="ea4cd-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="ea4cd-141">Kenni síugerðar skilgreint í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="ea4cd-142">**Gildi fyrir kenni síugerðar**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="ea4cd-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="ea4cd-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="ea4cd-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-144">*GUID*</span></span> | <span data-ttu-id="ea4cd-145">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="ea4cd-145">Read-only</span></span><br><span data-ttu-id="ea4cd-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-146">Required</span></span><br><span data-ttu-id="ea4cd-147">Framandlykill: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="ea4cd-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="ea4cd-148">Einkvæmt kerfismyndað kenni fyrir færslu síugerðar í tengdri einingu.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="ea4cd-149">**Krafa sett fram af**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-149">**Required By**</span></span><br><span data-ttu-id="ea4cd-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="ea4cd-150">mshr_requiredby</span></span><br><span data-ttu-id="ea4cd-151">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-151">*Datetime*</span></span> | <span data-ttu-id="ea4cd-152">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-152">Read/write</span></span><br><span data-ttu-id="ea4cd-153">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="ea4cd-153">Optional</span></span> | <span data-ttu-id="ea4cd-154">Dagsetningin sem þarf að klára síunina.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="ea4cd-155">**Staða**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-155">**Status**</span></span><br><span data-ttu-id="ea4cd-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="ea4cd-156">mshr_status</span></span><br><span data-ttu-id="ea4cd-157">*mshr_hcmcompletionstatus valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="ea4cd-158">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-158">Read/write</span></span><br><span data-ttu-id="ea4cd-159">Krafa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-159">Required</span></span> | <span data-ttu-id="ea4cd-160">Tilgreinir stöðu umsækjanda fyrir síunina.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="ea4cd-161">**Lokið þann**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-161">**Completed Date**</span></span><br><span data-ttu-id="ea4cd-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="ea4cd-162">mshr_completeddate</span></span><br><span data-ttu-id="ea4cd-163">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-163">*Datetime*</span></span> | <span data-ttu-id="ea4cd-164">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-164">Read/write</span></span><br><span data-ttu-id="ea4cd-165">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="ea4cd-165">Optional</span></span> | <span data-ttu-id="ea4cd-166">Sagsetning þegarlokið var við skoðun</span><span class="sxs-lookup"><span data-stu-id="ea4cd-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="ea4cd-167">**Athugasemdir**</span><span class="sxs-lookup"><span data-stu-id="ea4cd-167">**Notes**</span></span><br><span data-ttu-id="ea4cd-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="ea4cd-168">mshr_note</span></span><br><span data-ttu-id="ea4cd-169">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="ea4cd-169">*String*</span></span> | <span data-ttu-id="ea4cd-170">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="ea4cd-170">Read/write</span></span><br><span data-ttu-id="ea4cd-171">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="ea4cd-171">Optional</span></span> | <span data-ttu-id="ea4cd-172">Athugasemdir sem ráðningarstjórar og ráðningaraðilar nota.</span><span class="sxs-lookup"><span data-stu-id="ea4cd-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea4cd-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ea4cd-173">See also</span></span>

[<span data-ttu-id="ea4cd-174">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="ea4cd-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ea4cd-175">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="ea4cd-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]