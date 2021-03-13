---
title: Gerð skírteinis
description: Þetta efnisatriði lýsir einingu vottorðagerðar fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125714"
---
# <a name="certificate-type"></a><span data-ttu-id="52534-103">Gerð skírteinis</span><span class="sxs-lookup"><span data-stu-id="52534-103">Certificate type</span></span>

<span data-ttu-id="52534-104">Þetta efnisatriði lýsir einingu vottorðagerðar fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52534-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="52534-105">Raunlægt heiti: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="52534-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="52534-106">lýsing</span><span class="sxs-lookup"><span data-stu-id="52534-106">Description</span></span>

<span data-ttu-id="52534-107">Þessi eining skilgreinir lista yfir faglegar vottorðagerðir sem settar eru upp í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="52534-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="52534-108">Einingin er ekki sértæk fyrir lögaðila (fyrirtæki).</span><span class="sxs-lookup"><span data-stu-id="52534-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="52534-109">JSON-framsetning</span><span class="sxs-lookup"><span data-stu-id="52534-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="52534-110">Eiginleikar</span><span class="sxs-lookup"><span data-stu-id="52534-110">Properties</span></span>

| <span data-ttu-id="52534-111">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="52534-111">Property</span></span><br><span data-ttu-id="52534-112">**Efnislegt heiti**</span><span class="sxs-lookup"><span data-stu-id="52534-112">**Physical name**</span></span><br><span data-ttu-id="52534-113">**_Gerð_**</span><span class="sxs-lookup"><span data-stu-id="52534-113">**_Type_**</span></span> | <span data-ttu-id="52534-114">Nota</span><span class="sxs-lookup"><span data-stu-id="52534-114">Use</span></span> | <span data-ttu-id="52534-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="52534-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="52534-116">**Kenni fyrir einingu vottorðagerðar**</span><span class="sxs-lookup"><span data-stu-id="52534-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="52534-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="52534-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="52534-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="52534-118">*GUID*</span></span> | <span data-ttu-id="52534-119">Lesa eingöngu</span><span class="sxs-lookup"><span data-stu-id="52534-119">Read-only</span></span><br><span data-ttu-id="52534-120">Krafa</span><span class="sxs-lookup"><span data-stu-id="52534-120">Required</span></span> 
<span data-ttu-id="52534-121">Myndað af kerfinu</span><span class="sxs-lookup"><span data-stu-id="52534-121">System-generated</span></span> | <span data-ttu-id="52534-122">Einkvæmt aðalkenni fyrir vottorðagerðina.</span><span class="sxs-lookup"><span data-stu-id="52534-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="52534-123">**Gerð vottorðs**</span><span class="sxs-lookup"><span data-stu-id="52534-123">**Certificate Type**</span></span><br><span data-ttu-id="52534-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="52534-124">mshr_certificatetype</span></span><br><span data-ttu-id="52534-125">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="52534-125">*String*</span></span> | <span data-ttu-id="52534-126">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="52534-126">Read/write</span></span><br><span data-ttu-id="52534-127">Krafa</span><span class="sxs-lookup"><span data-stu-id="52534-127">Required</span></span> | <span data-ttu-id="52534-128">Einkvæmt lesanlegt kenni fyrir vottorðagerðina.</span><span class="sxs-lookup"><span data-stu-id="52534-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="52534-129">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="52534-129">**Description**</span></span><br><span data-ttu-id="52534-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="52534-130">mshr_description</span></span><br><span data-ttu-id="52534-131">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="52534-131">*String*</span></span> | <span data-ttu-id="52534-132">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="52534-132">Read/write</span></span><br><span data-ttu-id="52534-133">Krafa</span><span class="sxs-lookup"><span data-stu-id="52534-133">Required</span></span> | <span data-ttu-id="52534-134">Lýsing á vottorðagerð.</span><span class="sxs-lookup"><span data-stu-id="52534-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="52534-135">**Krefjast endurnýjunar**</span><span class="sxs-lookup"><span data-stu-id="52534-135">**Require Renewal**</span></span><br><span data-ttu-id="52534-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="52534-136">mshr_requirerenewal</span></span><br><span data-ttu-id="52534-137">*mshr_noyes valkostur stilltur*</span><span class="sxs-lookup"><span data-stu-id="52534-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="52534-138">Lesa/skrifa</span><span class="sxs-lookup"><span data-stu-id="52534-138">Read/write</span></span><br><span data-ttu-id="52534-139">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="52534-139">Optional</span></span> | <span data-ttu-id="52534-140">Tilgreinir hvort krafist sé endurnýjunar á vottorði.</span><span class="sxs-lookup"><span data-stu-id="52534-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="52534-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="52534-141">See also</span></span>

[<span data-ttu-id="52534-142">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="52534-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="52534-143">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="52534-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

