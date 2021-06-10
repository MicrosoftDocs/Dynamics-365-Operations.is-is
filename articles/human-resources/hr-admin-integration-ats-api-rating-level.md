---
title: Matsstig
description: Þetta efnisatriði lýsir einingu matsstig fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054837"
---
# <a name="rating-level"></a><span data-ttu-id="0eb47-103">Matsstig</span><span class="sxs-lookup"><span data-stu-id="0eb47-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0eb47-104">Þetta efnisatriði lýsir einingu matsstig fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0eb47-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0eb47-105">Raunlægt heiti: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="0eb47-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="0eb47-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="0eb47-106">Description</span></span>

<span data-ttu-id="0eb47-107">Þessi eining býður upp á tiltæk matsstig fyrir hæfni.</span><span class="sxs-lookup"><span data-stu-id="0eb47-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="0eb47-108">Matsstig gilda yfir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0eb47-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0eb47-109">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="0eb47-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="0eb47-110">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="0eb47-110">Properties</span></span>

| <span data-ttu-id="0eb47-111">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="0eb47-111">Property</span></span><br><span data-ttu-id="0eb47-112">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="0eb47-112">**Physical name**</span></span><br><span data-ttu-id="0eb47-113">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="0eb47-113">**_Type_**</span></span> | <span data-ttu-id="0eb47-114">Nota</span><span class="sxs-lookup"><span data-stu-id="0eb47-114">Use</span></span> | <span data-ttu-id="0eb47-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="0eb47-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0eb47-116">**Kenni fyrir einingu matsstigs**</span><span class="sxs-lookup"><span data-stu-id="0eb47-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="0eb47-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="0eb47-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="0eb47-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0eb47-118">*GUID*</span></span> | <span data-ttu-id="0eb47-119">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="0eb47-119">Read-only</span></span><br><span data-ttu-id="0eb47-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-120">Required</span></span><br><span data-ttu-id="0eb47-121">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="0eb47-121">System-generated</span></span> | <span data-ttu-id="0eb47-122">Einkvæmt kerfismyndað auðkenni fyrir stigið.</span><span class="sxs-lookup"><span data-stu-id="0eb47-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="0eb47-123">**Auðkenni matsstigs**</span><span class="sxs-lookup"><span data-stu-id="0eb47-123">**Rating Level ID**</span></span><br><span data-ttu-id="0eb47-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="0eb47-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="0eb47-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="0eb47-125">*String*</span></span> | <span data-ttu-id="0eb47-126">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="0eb47-126">Read/write</span></span><br><span data-ttu-id="0eb47-127">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-127">Required</span></span> | <span data-ttu-id="0eb47-128">Notandalesvænt einkvæmt kenni fyrir stigið.</span><span class="sxs-lookup"><span data-stu-id="0eb47-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="0eb47-129">**Kenni matslíkans**</span><span class="sxs-lookup"><span data-stu-id="0eb47-129">**Rating Model ID**</span></span><br><span data-ttu-id="0eb47-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="0eb47-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="0eb47-131">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="0eb47-131">*String*</span></span> | <span data-ttu-id="0eb47-132">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="0eb47-132">Read/write</span></span><br><span data-ttu-id="0eb47-133">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-133">Required</span></span> | <span data-ttu-id="0eb47-134">Matslíkanið sem matsstigið tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="0eb47-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="0eb47-135">**Kenni fyrir einingu matslíkans**</span><span class="sxs-lookup"><span data-stu-id="0eb47-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="0eb47-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="0eb47-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="0eb47-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0eb47-137">*GUID*</span></span> | <span data-ttu-id="0eb47-138">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="0eb47-138">Read-only</span></span><br><span data-ttu-id="0eb47-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-139">Required</span></span><br><span data-ttu-id="0eb47-140">Framandlykill: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="0eb47-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="0eb47-141">Kerfismyndað kenni fyrir matslíkanið sem matsstigið tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="0eb47-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="0eb47-142">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="0eb47-142">**Description**</span></span><br><span data-ttu-id="0eb47-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="0eb47-143">mshr_description</span></span><br><span data-ttu-id="0eb47-144">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="0eb47-144">*String*</span></span> | <span data-ttu-id="0eb47-145">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="0eb47-145">Read/write</span></span><br><span data-ttu-id="0eb47-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-146">Required</span></span> | <span data-ttu-id="0eb47-147">Lýsing á matsstiginu.</span><span class="sxs-lookup"><span data-stu-id="0eb47-147">The description of the rating level.</span></span> |
| <span data-ttu-id="0eb47-148">**Stuðull**</span><span class="sxs-lookup"><span data-stu-id="0eb47-148">**Factor**</span></span><br><span data-ttu-id="0eb47-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="0eb47-149">mshr_factor</span></span><br><span data-ttu-id="0eb47-150">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="0eb47-150">*Integer*</span></span> | <span data-ttu-id="0eb47-151">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="0eb47-151">Read/write</span></span><br><span data-ttu-id="0eb47-152">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-152">Required</span></span> | <span data-ttu-id="0eb47-153">Stuðullinn fyrir matsstigið.</span><span class="sxs-lookup"><span data-stu-id="0eb47-153">The factor for the rating level.</span></span> <span data-ttu-id="0eb47-154">Þegar vörur eru bornar saman við annan fjölda matsstiga er stuðullinn notaður til að staðla skorið.</span><span class="sxs-lookup"><span data-stu-id="0eb47-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="0eb47-155">Gildið verður að vera heiltala á bilinu 0 til 9.</span><span class="sxs-lookup"><span data-stu-id="0eb47-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="0eb47-156">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="0eb47-156">**Note**</span></span><br><span data-ttu-id="0eb47-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="0eb47-157">mshr_note</span></span><br><span data-ttu-id="0eb47-158">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="0eb47-158">*String*</span></span> | <span data-ttu-id="0eb47-159">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="0eb47-159">Read/write</span></span><br><span data-ttu-id="0eb47-160">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="0eb47-160">Optional</span></span> | <span data-ttu-id="0eb47-161">Allar athugsemdir sem tengjast matsstiginu.</span><span class="sxs-lookup"><span data-stu-id="0eb47-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="0eb47-162">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="0eb47-162">**Primary Field**</span></span><br><span data-ttu-id="0eb47-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0eb47-163">mshr_primaryfield</span></span><br><span data-ttu-id="0eb47-164">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="0eb47-164">*String*</span></span> | <span data-ttu-id="0eb47-165">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="0eb47-165">Read-only</span></span><br><span data-ttu-id="0eb47-166">Krafa</span><span class="sxs-lookup"><span data-stu-id="0eb47-166">Required</span></span> | <span data-ttu-id="0eb47-167">Svæði sem á að nota sem kennimerki einingafærslu.</span><span class="sxs-lookup"><span data-stu-id="0eb47-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="0eb47-168">Samsetning af kenni matsstigs og kenni matslíkans.</span><span class="sxs-lookup"><span data-stu-id="0eb47-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0eb47-169">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0eb47-169">See also</span></span>

[<span data-ttu-id="0eb47-170">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="0eb47-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0eb47-171">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="0eb47-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]