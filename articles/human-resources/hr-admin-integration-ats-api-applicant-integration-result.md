---
title: Niðurstöður samþættingar umsækjanda
description: Þetta efnisatriði lýsir valkostum fyrir niðurstöðu samþættingar umsækjanda fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467554"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="356a8-103">Niðurstöður samþættingar umsækjanda</span><span class="sxs-lookup"><span data-stu-id="356a8-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="356a8-104">Þetta efnisatriði lýsir valkostum fyrir niðurstöðu samþættingar umsækjanda fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="356a8-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="356a8-105">Raunlægt heiti: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="356a8-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="356a8-106">Þessi tölusetning býður upp á stöðu fyrir færslu umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="356a8-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="356a8-107">Virði</span><span class="sxs-lookup"><span data-stu-id="356a8-107">Value</span></span> | <span data-ttu-id="356a8-108">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="356a8-108">Label</span></span> | <span data-ttu-id="356a8-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="356a8-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="356a8-110">200000000</span><span class="sxs-lookup"><span data-stu-id="356a8-110">200000000</span></span> | <span data-ttu-id="356a8-111">Ekki farið í ferli</span><span class="sxs-lookup"><span data-stu-id="356a8-111">Not processed</span></span> | <span data-ttu-id="356a8-112">Umsækjandi kemur enn til greina.</span><span class="sxs-lookup"><span data-stu-id="356a8-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="356a8-113">200000001</span><span class="sxs-lookup"><span data-stu-id="356a8-113">200000001</span></span> | <span data-ttu-id="356a8-114">Ráðin(n)</span><span class="sxs-lookup"><span data-stu-id="356a8-114">Hired</span></span> | <span data-ttu-id="356a8-115">Umsækjandi hefur verið ráðinn.</span><span class="sxs-lookup"><span data-stu-id="356a8-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="356a8-116">200000002</span><span class="sxs-lookup"><span data-stu-id="356a8-116">200000002</span></span> | <span data-ttu-id="356a8-117">Ekki ráðnir</span><span class="sxs-lookup"><span data-stu-id="356a8-117">Not hired</span></span> | <span data-ttu-id="356a8-118">Ákvörðun var tekin um að ráða ekki umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="356a8-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="356a8-119">200000003</span><span class="sxs-lookup"><span data-stu-id="356a8-119">200000003</span></span> | <span data-ttu-id="356a8-120">Hunsað</span><span class="sxs-lookup"><span data-stu-id="356a8-120">Dismissed</span></span> | <span data-ttu-id="356a8-121">Umsækjandi kemur ekki lengur til greina.</span><span class="sxs-lookup"><span data-stu-id="356a8-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="356a8-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="356a8-122">See also</span></span>

[<span data-ttu-id="356a8-123">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="356a8-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="356a8-124">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="356a8-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]