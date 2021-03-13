---
title: Vottorð einstaklings
description: Þetta efnisatriði lýsir einingu fyrir vottorð einstaklings fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125354"
---
# <a name="person-certificate"></a><span data-ttu-id="5742b-103">Vottorð einstaklings</span><span class="sxs-lookup"><span data-stu-id="5742b-103">Person certificate</span></span>

<span data-ttu-id="5742b-104">Þetta efnisatriði lýsir einingu fyrir vottorð einstaklings fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5742b-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5742b-105">Raunlægt heiti: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="5742b-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="5742b-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="5742b-106">Description</span></span>

<span data-ttu-id="5742b-107">Þessi eining lýsir faglegum vottorðum umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="5742b-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5742b-108">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="5742b-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="5742b-109">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="5742b-109">Properties</span></span>

| <span data-ttu-id="5742b-110">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="5742b-110">Property</span></span><br><span data-ttu-id="5742b-111">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="5742b-111">**Physical name**</span></span><br><span data-ttu-id="5742b-112">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="5742b-112">**_Type_**</span></span> | <span data-ttu-id="5742b-113">Nota</span><span class="sxs-lookup"><span data-stu-id="5742b-113">Use</span></span> | <span data-ttu-id="5742b-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="5742b-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5742b-115">**Kenni fyrir einingu vottorðs einstaklings**</span><span class="sxs-lookup"><span data-stu-id="5742b-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="5742b-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="5742b-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="5742b-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5742b-117">*GUID*</span></span> | <span data-ttu-id="5742b-118">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="5742b-118">Read-only</span></span><br><span data-ttu-id="5742b-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-119">Required</span></span> | <span data-ttu-id="5742b-120">Kerfismyndað einkvæmt kenni fyrir færslueiningu einstaklingsvottorðs.</span><span class="sxs-lookup"><span data-stu-id="5742b-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="5742b-121">**Aðilanúmer**</span><span class="sxs-lookup"><span data-stu-id="5742b-121">**Party Number**</span></span><br><span data-ttu-id="5742b-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="5742b-122">mshr_partynumber</span></span><br><span data-ttu-id="5742b-123">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="5742b-123">*String*</span></span> | <span data-ttu-id="5742b-124">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="5742b-124">Read/write</span></span><br><span data-ttu-id="5742b-125">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-125">Required</span></span> | <span data-ttu-id="5742b-126">Kenni aðila (einstaklings) fyrir umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="5742b-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="5742b-127">**Gildi fyrir auðkenni einstaklings**</span><span class="sxs-lookup"><span data-stu-id="5742b-127">**Person ID Value**</span></span><br><span data-ttu-id="5742b-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="5742b-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="5742b-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5742b-129">*GUID*</span></span> | <span data-ttu-id="5742b-130">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="5742b-130">Read-only</span></span><br><span data-ttu-id="5742b-131">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-131">Required</span></span><br><span data-ttu-id="5742b-132">Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="5742b-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="5742b-133">Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings).</span><span class="sxs-lookup"><span data-stu-id="5742b-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="5742b-134">**Gerð vottorðskennis**</span><span class="sxs-lookup"><span data-stu-id="5742b-134">**Certificate Type ID**</span></span><br><span data-ttu-id="5742b-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="5742b-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="5742b-136">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="5742b-136">*String*</span></span> | <span data-ttu-id="5742b-137">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="5742b-137">Read/write</span></span><br><span data-ttu-id="5742b-138">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-138">Required</span></span> |  <span data-ttu-id="5742b-139">Kenni vottorðagerðar skilgreint í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5742b-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="5742b-140">**Gildi fyrir kenni vottorðagerðar**</span><span class="sxs-lookup"><span data-stu-id="5742b-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="5742b-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="5742b-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="5742b-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5742b-142">*GUID*</span></span> | <span data-ttu-id="5742b-143">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="5742b-143">Read-only</span></span><br><span data-ttu-id="5742b-144">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-144">Required</span></span><br><span data-ttu-id="5742b-145">Framandlykill: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="5742b-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="5742b-146">Kerfismyndað einkvæmt kenni vottorðagerðar í tengdri einingu.</span><span class="sxs-lookup"><span data-stu-id="5742b-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="5742b-147">**Upphafsdagsetning**</span><span class="sxs-lookup"><span data-stu-id="5742b-147">**Start Date**</span></span><br><span data-ttu-id="5742b-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="5742b-148">mshr_startdate</span></span><br><span data-ttu-id="5742b-149">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="5742b-149">*Datetime*</span></span> | <span data-ttu-id="5742b-150">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="5742b-150">Read/write</span></span><br><span data-ttu-id="5742b-151">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-151">Required</span></span> | <span data-ttu-id="5742b-152">Dagsetningin þegar vottorð var gefið út.</span><span class="sxs-lookup"><span data-stu-id="5742b-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="5742b-153">**Lokadagsetning**</span><span class="sxs-lookup"><span data-stu-id="5742b-153">**End Date**</span></span><br><span data-ttu-id="5742b-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="5742b-154">mshr_enddate</span></span><br><span data-ttu-id="5742b-155">*Dagsetning og tími*</span><span class="sxs-lookup"><span data-stu-id="5742b-155">*Datetime*</span></span> | <span data-ttu-id="5742b-156">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="5742b-156">Read/write</span></span><br><span data-ttu-id="5742b-157">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="5742b-157">Optional</span></span> | <span data-ttu-id="5742b-158">Dagsetningin þegar vottorð rennur út.</span><span class="sxs-lookup"><span data-stu-id="5742b-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="5742b-159">**Athugasemdir**</span><span class="sxs-lookup"><span data-stu-id="5742b-159">**Notes**</span></span><br><span data-ttu-id="5742b-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="5742b-160">mshr_notes</span></span><br><span data-ttu-id="5742b-161">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="5742b-161">*String*</span></span> | <span data-ttu-id="5742b-162">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="5742b-162">Read/write</span></span><br><span data-ttu-id="5742b-163">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="5742b-163">Optional</span></span> | <span data-ttu-id="5742b-164">Athugasemdir sem ráðningarstjórar og ráðningaraðilar nota.</span><span class="sxs-lookup"><span data-stu-id="5742b-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="5742b-165">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="5742b-165">**Primary Field**</span></span><br><span data-ttu-id="5742b-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="5742b-166">mshr_primaryfield</span></span><br><span data-ttu-id="5742b-167">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="5742b-167">*String*</span></span> | <span data-ttu-id="5742b-168">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="5742b-168">Read-only</span></span><br><span data-ttu-id="5742b-169">Krafa</span><span class="sxs-lookup"><span data-stu-id="5742b-169">Required</span></span> |  <span data-ttu-id="5742b-170">Svæði sem á að nota sem kennimerki einingafærslu.</span><span class="sxs-lookup"><span data-stu-id="5742b-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="5742b-171">Samsetning aðilanúmers, kennisgerð vottorðs og upphafsdagsetning.</span><span class="sxs-lookup"><span data-stu-id="5742b-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5742b-172">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5742b-172">See also</span></span>

[<span data-ttu-id="5742b-173">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="5742b-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5742b-174">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="5742b-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

