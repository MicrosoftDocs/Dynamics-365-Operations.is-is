---
title: Skoðunargerðir
description: Þetta efnisatriði lýsir einingu skoðunargerðar fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126171"
---
# <a name="screening-types"></a><span data-ttu-id="74cfc-103">Skoðunargerðir</span><span class="sxs-lookup"><span data-stu-id="74cfc-103">Screening types</span></span>

<span data-ttu-id="74cfc-104">Þetta efnisatriði lýsir einingu skoðunargerðar fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="74cfc-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="74cfc-105">Raunlægt heiti: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="74cfc-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="74cfc-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="74cfc-106">Description</span></span>

<span data-ttu-id="74cfc-107">Þessi eining lýsir skoðunargerðum sem settar eru upp af fyrirtækinu á undan ráðningu og fyrir yfirstandandi skoðunarferli starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="74cfc-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="74cfc-108">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="74cfc-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="74cfc-109">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="74cfc-109">Properties</span></span>

| <span data-ttu-id="74cfc-110">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="74cfc-110">Property</span></span><br><span data-ttu-id="74cfc-111">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="74cfc-111">**Physical name**</span></span><br><span data-ttu-id="74cfc-112">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="74cfc-112">**_Type_**</span></span> | <span data-ttu-id="74cfc-113">Nota</span><span class="sxs-lookup"><span data-stu-id="74cfc-113">Use</span></span> | <span data-ttu-id="74cfc-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="74cfc-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="74cfc-115">**Kenni fyrir einingu skoðunargerðar**</span><span class="sxs-lookup"><span data-stu-id="74cfc-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="74cfc-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="74cfc-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="74cfc-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="74cfc-117">*GUID*</span></span> | <span data-ttu-id="74cfc-118">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="74cfc-118">Read-only</span></span><br><span data-ttu-id="74cfc-119">Krafa</span><span class="sxs-lookup"><span data-stu-id="74cfc-119">Required</span></span><br><span data-ttu-id="74cfc-120">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="74cfc-120">System-generated</span></span> | <span data-ttu-id="74cfc-121">Einkvæmt aðalkenni fyrir færslu skoðunargerðar.</span><span class="sxs-lookup"><span data-stu-id="74cfc-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="74cfc-122">**Kenni skoðunargerðar**</span><span class="sxs-lookup"><span data-stu-id="74cfc-122">**Screening Type ID**</span></span><br><span data-ttu-id="74cfc-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="74cfc-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="74cfc-124">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="74cfc-124">*String*</span></span> | <span data-ttu-id="74cfc-125">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="74cfc-125">Read/write</span></span><br><span data-ttu-id="74cfc-126">Krafa</span><span class="sxs-lookup"><span data-stu-id="74cfc-126">Required</span></span> | <span data-ttu-id="74cfc-127">Notandaskilgreint einkvæmt kenni fyrir skoðunargerðina.</span><span class="sxs-lookup"><span data-stu-id="74cfc-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="74cfc-128">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="74cfc-128">**Description**</span></span><br><span data-ttu-id="74cfc-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="74cfc-129">mshr_description</span></span><br><span data-ttu-id="74cfc-130">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="74cfc-130">*String*</span></span> | <span data-ttu-id="74cfc-131">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="74cfc-131">Read/write</span></span><br><span data-ttu-id="74cfc-132">Krafa</span><span class="sxs-lookup"><span data-stu-id="74cfc-132">Required</span></span> | <span data-ttu-id="74cfc-133">Lýsing á skoðunargerðinni.</span><span class="sxs-lookup"><span data-stu-id="74cfc-133">The description of the screening type.</span></span> |
| <span data-ttu-id="74cfc-134">**Tíðnieining**</span><span class="sxs-lookup"><span data-stu-id="74cfc-134">**Frequency Unit**</span></span><br><span data-ttu-id="74cfc-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="74cfc-135">mshr_frequencyunit</span></span><br><span data-ttu-id="74cfc-136">*mshr_hcmfrequencyunit valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="74cfc-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="74cfc-137">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="74cfc-137">Read/write</span></span><br><span data-ttu-id="74cfc-138">Krafa</span><span class="sxs-lookup"><span data-stu-id="74cfc-138">Required</span></span> | <span data-ttu-id="74cfc-139">Lýsir því hversu fljótt þarf að ljúka skoðun fyrir úthlutaðan einstakling.</span><span class="sxs-lookup"><span data-stu-id="74cfc-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="74cfc-140">**Mynda úr**</span><span class="sxs-lookup"><span data-stu-id="74cfc-140">**Generate From**</span></span><br><span data-ttu-id="74cfc-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="74cfc-141">mshr_generatefrom</span></span><br><span data-ttu-id="74cfc-142">*mshr_hcmfrequencygeneratefrom valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="74cfc-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="74cfc-143">Lesa-skrifa</span><span class="sxs-lookup"><span data-stu-id="74cfc-143">Read-write</span></span><br><span data-ttu-id="74cfc-144">Krafa</span><span class="sxs-lookup"><span data-stu-id="74cfc-144">Required</span></span> | <span data-ttu-id="74cfc-145">Ef tíðnigildið er eitthvað annað gildi en „Aðeins einu sinni“, ákvarðar GenerateForm-gildið dagsetninguna þegar á reikna út næsta skoðunartilvik.</span><span class="sxs-lookup"><span data-stu-id="74cfc-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="74cfc-146">**Tímabil**</span><span class="sxs-lookup"><span data-stu-id="74cfc-146">**Frequency Interval**</span></span><br><span data-ttu-id="74cfc-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="74cfc-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="74cfc-148">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="74cfc-148">*Integer*</span></span> | <span data-ttu-id="74cfc-149">Lesa-skrifa</span><span class="sxs-lookup"><span data-stu-id="74cfc-149">Read-write</span></span><br><span data-ttu-id="74cfc-150">Krafa</span><span class="sxs-lookup"><span data-stu-id="74cfc-150">Required</span></span> | <span data-ttu-id="74cfc-151">Ef tíðnigildið er eitthvað annað gildi en „Aðeins einu sinni“ þarf að skilgreina tímabil fyrir tímaeiningar á milli skoðunartilvika.</span><span class="sxs-lookup"><span data-stu-id="74cfc-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="74cfc-152">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="74cfc-152">See also</span></span>

[<span data-ttu-id="74cfc-153">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="74cfc-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="74cfc-154">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="74cfc-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
