---
title: Staða á lokið
description: Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468204"
---
# <a name="completion-status"></a><span data-ttu-id="3d54a-103">Staða á lokið</span><span class="sxs-lookup"><span data-stu-id="3d54a-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3d54a-104">Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3d54a-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3d54a-105">Raunlægt heiti: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="3d54a-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="3d54a-106">Þessi tölusetning býður upp á valkost stöðugilda fyrir síun umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="3d54a-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="3d54a-107">Virði</span><span class="sxs-lookup"><span data-stu-id="3d54a-107">Value</span></span> | <span data-ttu-id="3d54a-108">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="3d54a-108">Label</span></span> | <span data-ttu-id="3d54a-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="3d54a-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3d54a-110">200000000</span><span class="sxs-lookup"><span data-stu-id="3d54a-110">200000000</span></span> | <span data-ttu-id="3d54a-111">Ekki tilbúið</span><span class="sxs-lookup"><span data-stu-id="3d54a-111">Not Complete</span></span> | <span data-ttu-id="3d54a-112">Umsækjandi hefur ekki enn lokið síun.</span><span class="sxs-lookup"><span data-stu-id="3d54a-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="3d54a-113">200000001</span><span class="sxs-lookup"><span data-stu-id="3d54a-113">200000001</span></span> | <span data-ttu-id="3d54a-114">Staðið</span><span class="sxs-lookup"><span data-stu-id="3d54a-114">Pass</span></span> | <span data-ttu-id="3d54a-115">Umsækjandi komst í gegnum síuna.</span><span class="sxs-lookup"><span data-stu-id="3d54a-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="3d54a-116">200000002</span><span class="sxs-lookup"><span data-stu-id="3d54a-116">200000002</span></span> | <span data-ttu-id="3d54a-117">Fella</span><span class="sxs-lookup"><span data-stu-id="3d54a-117">Fail</span></span> | <span data-ttu-id="3d54a-118">Umsækjandi komst ekki í gegnum síuna.</span><span class="sxs-lookup"><span data-stu-id="3d54a-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3d54a-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3d54a-119">See also</span></span>

[<span data-ttu-id="3d54a-120">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="3d54a-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3d54a-121">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="3d54a-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]