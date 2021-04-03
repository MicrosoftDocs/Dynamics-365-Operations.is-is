---
title: Staða ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464647"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="53af5-103">Staða ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="53af5-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="53af5-104">Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="53af5-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="53af5-105">Raunlægt heiti: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="53af5-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="53af5-106">Þessi upptalning býður upp á valmöguleika fyrir stöðugildi RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="53af5-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="53af5-107">Virði</span><span class="sxs-lookup"><span data-stu-id="53af5-107">Value</span></span> | <span data-ttu-id="53af5-108">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="53af5-108">Label</span></span> | <span data-ttu-id="53af5-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="53af5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="53af5-110">200000000</span><span class="sxs-lookup"><span data-stu-id="53af5-110">200000000</span></span> | <span data-ttu-id="53af5-111">Drög</span><span class="sxs-lookup"><span data-stu-id="53af5-111">Draft</span></span> | <span data-ttu-id="53af5-112">Beiðnin er í drögum og er ekki tilbúin fyrir virka ráðningu.</span><span class="sxs-lookup"><span data-stu-id="53af5-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="53af5-113">200000001</span><span class="sxs-lookup"><span data-stu-id="53af5-113">200000001</span></span> | <span data-ttu-id="53af5-114">Í endurskoðun</span><span class="sxs-lookup"><span data-stu-id="53af5-114">In Review</span></span> | <span data-ttu-id="53af5-115">Beiðnin hefur verið send og verið er að senda hana til samþykktar af verkflæði.</span><span class="sxs-lookup"><span data-stu-id="53af5-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="53af5-116">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="53af5-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="53af5-117">200000002</span><span class="sxs-lookup"><span data-stu-id="53af5-117">200000002</span></span> | <span data-ttu-id="53af5-118">Í biðstöðu</span><span class="sxs-lookup"><span data-stu-id="53af5-118">Pending</span></span> | <span data-ttu-id="53af5-119">Beiðnin bíður aðgerðar verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="53af5-119">The request is pending workflow action.</span></span> <span data-ttu-id="53af5-120">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="53af5-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="53af5-121">200000003</span><span class="sxs-lookup"><span data-stu-id="53af5-121">200000003</span></span> | <span data-ttu-id="53af5-122">Hætt við</span><span class="sxs-lookup"><span data-stu-id="53af5-122">Canceled</span></span> | <span data-ttu-id="53af5-123">Hætt var við beiðnina.</span><span class="sxs-lookup"><span data-stu-id="53af5-123">The request has been canceled.</span></span> <span data-ttu-id="53af5-124">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="53af5-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="53af5-125">200000004</span><span class="sxs-lookup"><span data-stu-id="53af5-125">200000004</span></span> | <span data-ttu-id="53af5-126">Hafnað</span><span class="sxs-lookup"><span data-stu-id="53af5-126">Denied</span></span> | <span data-ttu-id="53af5-127">Beiðninni var hafnað.</span><span class="sxs-lookup"><span data-stu-id="53af5-127">The request has been denied.</span></span> <span data-ttu-id="53af5-128">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="53af5-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="53af5-129">200000005</span><span class="sxs-lookup"><span data-stu-id="53af5-129">200000005</span></span> | <span data-ttu-id="53af5-130">Í gangi</span><span class="sxs-lookup"><span data-stu-id="53af5-130">Active</span></span> | <span data-ttu-id="53af5-131">Öllum verkflæðum er lokið og þau samþykkt og beiðnin er tilbúin fyrir virka ráðningu.</span><span class="sxs-lookup"><span data-stu-id="53af5-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="53af5-132">200000006</span><span class="sxs-lookup"><span data-stu-id="53af5-132">200000006</span></span> | <span data-ttu-id="53af5-133">Lokað</span><span class="sxs-lookup"><span data-stu-id="53af5-133">Closed</span></span> | <span data-ttu-id="53af5-134">Ráðningarbeiðnin er lokuð.</span><span class="sxs-lookup"><span data-stu-id="53af5-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="53af5-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="53af5-135">See also</span></span>

[<span data-ttu-id="53af5-136">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="53af5-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="53af5-137">Dæmi um fyrirspurn fyrir ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="53af5-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]