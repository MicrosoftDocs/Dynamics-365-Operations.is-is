---
title: Matsstig
description: Þetta efnisatriði lýsir einingu matsstig fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125258"
---
# <a name="rating-level"></a><span data-ttu-id="9820a-103">Matsstig</span><span class="sxs-lookup"><span data-stu-id="9820a-103">Rating level</span></span>

<span data-ttu-id="9820a-104">Þetta efnisatriði lýsir einingu matsstig fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9820a-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9820a-105">Raunlægt heiti: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="9820a-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="9820a-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="9820a-106">Description</span></span>

<span data-ttu-id="9820a-107">Þessi eining býður upp á tiltæk matsstig fyrir hæfni.</span><span class="sxs-lookup"><span data-stu-id="9820a-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="9820a-108">Matsstig gilda yfir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="9820a-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9820a-109">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="9820a-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="9820a-110">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="9820a-110">Properties</span></span>

| <span data-ttu-id="9820a-111">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="9820a-111">Property</span></span><br><span data-ttu-id="9820a-112">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="9820a-112">**Physical name**</span></span><br><span data-ttu-id="9820a-113">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="9820a-113">**_Type_**</span></span> | <span data-ttu-id="9820a-114">Nota</span><span class="sxs-lookup"><span data-stu-id="9820a-114">Use</span></span> | <span data-ttu-id="9820a-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="9820a-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9820a-116">**Kenni fyrir einingu matsstigs**</span><span class="sxs-lookup"><span data-stu-id="9820a-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="9820a-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="9820a-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="9820a-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9820a-118">*GUID*</span></span> | <span data-ttu-id="9820a-119">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="9820a-119">Read-only</span></span><br><span data-ttu-id="9820a-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-120">Required</span></span><br><span data-ttu-id="9820a-121">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="9820a-121">System-generated</span></span> | <span data-ttu-id="9820a-122">Einkvæmt kerfismyndað auðkenni fyrir stigið.</span><span class="sxs-lookup"><span data-stu-id="9820a-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="9820a-123">**Auðkenni matsstigs**</span><span class="sxs-lookup"><span data-stu-id="9820a-123">**Rating Level ID**</span></span><br><span data-ttu-id="9820a-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="9820a-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="9820a-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9820a-125">*String*</span></span> | <span data-ttu-id="9820a-126">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="9820a-126">Read/write</span></span><br><span data-ttu-id="9820a-127">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-127">Required</span></span> | <span data-ttu-id="9820a-128">Notandalesvænt einkvæmt kenni fyrir stigið.</span><span class="sxs-lookup"><span data-stu-id="9820a-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="9820a-129">**Kenni matslíkans**</span><span class="sxs-lookup"><span data-stu-id="9820a-129">**Rating Model ID**</span></span><br><span data-ttu-id="9820a-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="9820a-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="9820a-131">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9820a-131">*String*</span></span> | <span data-ttu-id="9820a-132">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="9820a-132">Read/write</span></span><br><span data-ttu-id="9820a-133">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-133">Required</span></span> | <span data-ttu-id="9820a-134">Matslíkanið sem matsstigið tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="9820a-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="9820a-135">**Kenni fyrir einingu matslíkans**</span><span class="sxs-lookup"><span data-stu-id="9820a-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="9820a-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="9820a-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="9820a-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9820a-137">*GUID*</span></span> | <span data-ttu-id="9820a-138">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="9820a-138">Read-only</span></span><br><span data-ttu-id="9820a-139">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-139">Required</span></span><br><span data-ttu-id="9820a-140">Framandlykill: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="9820a-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="9820a-141">Kerfismyndað kenni fyrir matslíkanið sem matsstigið tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="9820a-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="9820a-142">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="9820a-142">**Description**</span></span><br><span data-ttu-id="9820a-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="9820a-143">mshr_description</span></span><br><span data-ttu-id="9820a-144">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9820a-144">*String*</span></span> | <span data-ttu-id="9820a-145">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="9820a-145">Read/write</span></span><br><span data-ttu-id="9820a-146">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-146">Required</span></span> | <span data-ttu-id="9820a-147">Lýsing á matsstiginu.</span><span class="sxs-lookup"><span data-stu-id="9820a-147">The description of the rating level.</span></span> |
| <span data-ttu-id="9820a-148">**Stuðull**</span><span class="sxs-lookup"><span data-stu-id="9820a-148">**Factor**</span></span><br><span data-ttu-id="9820a-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="9820a-149">mshr_factor</span></span><br><span data-ttu-id="9820a-150">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="9820a-150">*Integer*</span></span> | <span data-ttu-id="9820a-151">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="9820a-151">Read/write</span></span><br><span data-ttu-id="9820a-152">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-152">Required</span></span> | <span data-ttu-id="9820a-153">Stuðullinn fyrir matsstigið.</span><span class="sxs-lookup"><span data-stu-id="9820a-153">The factor for the rating level.</span></span> <span data-ttu-id="9820a-154">Þegar vörur eru bornar saman við annan fjölda matsstiga er stuðullinn notaður til að staðla skorið.</span><span class="sxs-lookup"><span data-stu-id="9820a-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="9820a-155">Gildið verður að vera heiltala á bilinu 0 til 9.</span><span class="sxs-lookup"><span data-stu-id="9820a-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="9820a-156">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="9820a-156">**Note**</span></span><br><span data-ttu-id="9820a-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="9820a-157">mshr_note</span></span><br><span data-ttu-id="9820a-158">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9820a-158">*String*</span></span> | <span data-ttu-id="9820a-159">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="9820a-159">Read/write</span></span><br><span data-ttu-id="9820a-160">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="9820a-160">Optional</span></span> | <span data-ttu-id="9820a-161">Allar athugsemdir sem tengjast matsstiginu.</span><span class="sxs-lookup"><span data-stu-id="9820a-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="9820a-162">**Aðalsvæði**</span><span class="sxs-lookup"><span data-stu-id="9820a-162">**Primary Field**</span></span><br><span data-ttu-id="9820a-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9820a-163">mshr_primaryfield</span></span><br><span data-ttu-id="9820a-164">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="9820a-164">*String*</span></span> | <span data-ttu-id="9820a-165">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="9820a-165">Read-only</span></span><br><span data-ttu-id="9820a-166">Krafa</span><span class="sxs-lookup"><span data-stu-id="9820a-166">Required</span></span> | <span data-ttu-id="9820a-167">Svæði sem á að nota sem kennimerki einingafærslu.</span><span class="sxs-lookup"><span data-stu-id="9820a-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="9820a-168">Samsetning af kenni matsstigs og kenni matslíkans.</span><span class="sxs-lookup"><span data-stu-id="9820a-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9820a-169">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9820a-169">See also</span></span>

[<span data-ttu-id="9820a-170">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="9820a-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9820a-171">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="9820a-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
