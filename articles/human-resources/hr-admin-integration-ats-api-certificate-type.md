---
title: Gerð skírteinis
description: Þetta efnisatriði lýsir einingu vottorðagerðar fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054693"
---
# <a name="certificate-type"></a><span data-ttu-id="14aa7-103">Gerð skírteinis</span><span class="sxs-lookup"><span data-stu-id="14aa7-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="14aa7-104">Þetta efnisatriði lýsir einingu vottorðagerðar fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="14aa7-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="14aa7-105">Raunlægt heiti: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="14aa7-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="14aa7-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="14aa7-106">Description</span></span>

<span data-ttu-id="14aa7-107">Þessi eining skilgreinir lista yfir faglegar vottorðagerðir sem settar eru upp í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="14aa7-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="14aa7-108">Einingin er ekki sértæk fyrir lögaðila (fyrirtæki).</span><span class="sxs-lookup"><span data-stu-id="14aa7-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="14aa7-109">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="14aa7-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="14aa7-110">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="14aa7-110">Properties</span></span>

| <span data-ttu-id="14aa7-111">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="14aa7-111">Property</span></span><br><span data-ttu-id="14aa7-112">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="14aa7-112">**Physical name**</span></span><br><span data-ttu-id="14aa7-113">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="14aa7-113">**_Type_**</span></span> | <span data-ttu-id="14aa7-114">Nota</span><span class="sxs-lookup"><span data-stu-id="14aa7-114">Use</span></span> | <span data-ttu-id="14aa7-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="14aa7-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="14aa7-116">**Kenni fyrir einingu vottorðagerðar**</span><span class="sxs-lookup"><span data-stu-id="14aa7-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="14aa7-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="14aa7-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="14aa7-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="14aa7-118">*GUID*</span></span> | <span data-ttu-id="14aa7-119">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="14aa7-119">Read-only</span></span><br><span data-ttu-id="14aa7-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="14aa7-120">Required</span></span> 
<span data-ttu-id="14aa7-121">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="14aa7-121">System-generated</span></span> | <span data-ttu-id="14aa7-122">Einkvæmt aðalkenni fyrir vottorðagerðina.</span><span class="sxs-lookup"><span data-stu-id="14aa7-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="14aa7-123">**Gerð vottorðs**</span><span class="sxs-lookup"><span data-stu-id="14aa7-123">**Certificate Type**</span></span><br><span data-ttu-id="14aa7-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="14aa7-124">mshr_certificatetype</span></span><br><span data-ttu-id="14aa7-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="14aa7-125">*String*</span></span> | <span data-ttu-id="14aa7-126">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="14aa7-126">Read/write</span></span><br><span data-ttu-id="14aa7-127">Krafa</span><span class="sxs-lookup"><span data-stu-id="14aa7-127">Required</span></span> | <span data-ttu-id="14aa7-128">Einkvæmt lesanlegt kenni fyrir vottorðagerðina.</span><span class="sxs-lookup"><span data-stu-id="14aa7-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="14aa7-129">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="14aa7-129">**Description**</span></span><br><span data-ttu-id="14aa7-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="14aa7-130">mshr_description</span></span><br><span data-ttu-id="14aa7-131">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="14aa7-131">*String*</span></span> | <span data-ttu-id="14aa7-132">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="14aa7-132">Read/write</span></span><br><span data-ttu-id="14aa7-133">Krafa</span><span class="sxs-lookup"><span data-stu-id="14aa7-133">Required</span></span> | <span data-ttu-id="14aa7-134">Lýsing á vottorðagerð.</span><span class="sxs-lookup"><span data-stu-id="14aa7-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="14aa7-135">**Krefjast endurnýjunar**</span><span class="sxs-lookup"><span data-stu-id="14aa7-135">**Require Renewal**</span></span><br><span data-ttu-id="14aa7-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="14aa7-136">mshr_requirerenewal</span></span><br><span data-ttu-id="14aa7-137">*mshr_noyes valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="14aa7-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="14aa7-138">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="14aa7-138">Read/write</span></span><br><span data-ttu-id="14aa7-139">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="14aa7-139">Optional</span></span> | <span data-ttu-id="14aa7-140">Tilgreinir hvort krafist sé endurnýjunar á vottorði.</span><span class="sxs-lookup"><span data-stu-id="14aa7-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="14aa7-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="14aa7-141">See also</span></span>

[<span data-ttu-id="14aa7-142">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="14aa7-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="14aa7-143">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="14aa7-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]