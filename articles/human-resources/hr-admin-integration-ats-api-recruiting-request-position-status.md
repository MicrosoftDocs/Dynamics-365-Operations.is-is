---
title: Staða starfs í ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu starfs í ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464719"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="de9b7-103">Staða starfs í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="de9b7-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="de9b7-104">Þetta efnisatriði lýsir valmöguleika fyrir stöðu starfs í ráðningarbeiðni fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9b7-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="de9b7-105">Raunlægt heiti: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="de9b7-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="de9b7-106">Þessi upptalning býður upp á valmöguleika fyrir stöðugildi fyrir hverja stöðu í ráðningarbeiðni í einingunni RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="de9b7-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="de9b7-107">Virði</span><span class="sxs-lookup"><span data-stu-id="de9b7-107">Value</span></span> | <span data-ttu-id="de9b7-108">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="de9b7-108">Label</span></span> | <span data-ttu-id="de9b7-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="de9b7-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="de9b7-110">200000000</span><span class="sxs-lookup"><span data-stu-id="de9b7-110">200000000</span></span> | <span data-ttu-id="de9b7-111">Opnar</span><span class="sxs-lookup"><span data-stu-id="de9b7-111">Open</span></span> | <span data-ttu-id="de9b7-112">Staðan í ráðningarbeiðninni er opin fyrir ráðningu.</span><span class="sxs-lookup"><span data-stu-id="de9b7-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="de9b7-113">Þetta gefur ekki til kynna að engin virk stöðuúthlutun er í gangi fyrir stöðuna.</span><span class="sxs-lookup"><span data-stu-id="de9b7-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="de9b7-114">Það kann að vera að starfsmaður sé í stöðunni á ráðningartímanum.</span><span class="sxs-lookup"><span data-stu-id="de9b7-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="de9b7-115">Það gefur aðeins til kynna að staðan er tiltækt fyrir ráðningu í samhengi ráðningarbeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="de9b7-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="de9b7-116">200000001</span><span class="sxs-lookup"><span data-stu-id="de9b7-116">200000001</span></span> | <span data-ttu-id="de9b7-117">Útfyllt</span><span class="sxs-lookup"><span data-stu-id="de9b7-117">Filled</span></span> | <span data-ttu-id="de9b7-118">Starfskraftur hefur verið valinn fyrir úthlutun á stöðuna.</span><span class="sxs-lookup"><span data-stu-id="de9b7-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="de9b7-119">200000002</span><span class="sxs-lookup"><span data-stu-id="de9b7-119">200000002</span></span> | <span data-ttu-id="de9b7-120">Hætt við</span><span class="sxs-lookup"><span data-stu-id="de9b7-120">Canceled</span></span> | <span data-ttu-id="de9b7-121">Hætt hefur verið við beiðni um ráðningu fyrir þessa stöðu.</span><span class="sxs-lookup"><span data-stu-id="de9b7-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="de9b7-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="de9b7-122">See also</span></span>

[<span data-ttu-id="de9b7-123">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="de9b7-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="de9b7-124">Dæmi um fyrirspurn fyrir ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="de9b7-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]