---
title: Staða ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059185"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="84c67-103">Staða ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="84c67-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="84c67-104">Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="84c67-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="84c67-105">Raunlægt heiti: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="84c67-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="84c67-106">Þessi upptalning býður upp á valmöguleika fyrir stöðugildi RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="84c67-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="84c67-107">Virði</span><span class="sxs-lookup"><span data-stu-id="84c67-107">Value</span></span> | <span data-ttu-id="84c67-108">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="84c67-108">Label</span></span> | <span data-ttu-id="84c67-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="84c67-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="84c67-110">200000000</span><span class="sxs-lookup"><span data-stu-id="84c67-110">200000000</span></span> | <span data-ttu-id="84c67-111">Drög</span><span class="sxs-lookup"><span data-stu-id="84c67-111">Draft</span></span> | <span data-ttu-id="84c67-112">Beiðnin er í drögum og er ekki tilbúin fyrir virka ráðningu.</span><span class="sxs-lookup"><span data-stu-id="84c67-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="84c67-113">200000001</span><span class="sxs-lookup"><span data-stu-id="84c67-113">200000001</span></span> | <span data-ttu-id="84c67-114">Í endurskoðun</span><span class="sxs-lookup"><span data-stu-id="84c67-114">In Review</span></span> | <span data-ttu-id="84c67-115">Beiðnin hefur verið send og verið er að senda hana til samþykktar af verkflæði.</span><span class="sxs-lookup"><span data-stu-id="84c67-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="84c67-116">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="84c67-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="84c67-117">200000002</span><span class="sxs-lookup"><span data-stu-id="84c67-117">200000002</span></span> | <span data-ttu-id="84c67-118">Í biðstöðu</span><span class="sxs-lookup"><span data-stu-id="84c67-118">Pending</span></span> | <span data-ttu-id="84c67-119">Beiðnin bíður aðgerðar verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="84c67-119">The request is pending workflow action.</span></span> <span data-ttu-id="84c67-120">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="84c67-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="84c67-121">200000003</span><span class="sxs-lookup"><span data-stu-id="84c67-121">200000003</span></span> | <span data-ttu-id="84c67-122">Hætt við</span><span class="sxs-lookup"><span data-stu-id="84c67-122">Canceled</span></span> | <span data-ttu-id="84c67-123">Hætt var við beiðnina.</span><span class="sxs-lookup"><span data-stu-id="84c67-123">The request has been canceled.</span></span> <span data-ttu-id="84c67-124">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="84c67-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="84c67-125">200000004</span><span class="sxs-lookup"><span data-stu-id="84c67-125">200000004</span></span> | <span data-ttu-id="84c67-126">Hafnað</span><span class="sxs-lookup"><span data-stu-id="84c67-126">Denied</span></span> | <span data-ttu-id="84c67-127">Beiðninni var hafnað.</span><span class="sxs-lookup"><span data-stu-id="84c67-127">The request has been denied.</span></span> <span data-ttu-id="84c67-128">Aðeins í boði þegar verkflæði er virkt.</span><span class="sxs-lookup"><span data-stu-id="84c67-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="84c67-129">200000005</span><span class="sxs-lookup"><span data-stu-id="84c67-129">200000005</span></span> | <span data-ttu-id="84c67-130">Í gangi</span><span class="sxs-lookup"><span data-stu-id="84c67-130">Active</span></span> | <span data-ttu-id="84c67-131">Öllum verkflæðum er lokið og þau samþykkt og beiðnin er tilbúin fyrir virka ráðningu.</span><span class="sxs-lookup"><span data-stu-id="84c67-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="84c67-132">200000006</span><span class="sxs-lookup"><span data-stu-id="84c67-132">200000006</span></span> | <span data-ttu-id="84c67-133">Lokað</span><span class="sxs-lookup"><span data-stu-id="84c67-133">Closed</span></span> | <span data-ttu-id="84c67-134">Ráðningarbeiðnin er lokuð.</span><span class="sxs-lookup"><span data-stu-id="84c67-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="84c67-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="84c67-135">See also</span></span>

[<span data-ttu-id="84c67-136">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="84c67-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="84c67-137">Dæmi um fyrirspurn fyrir ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="84c67-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]