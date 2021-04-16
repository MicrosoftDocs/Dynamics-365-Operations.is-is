---
title: Staða á lokið
description: Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798370"
---
# <a name="completion-status"></a><span data-ttu-id="9731c-103">Staða á lokið</span><span class="sxs-lookup"><span data-stu-id="9731c-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9731c-104">Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9731c-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9731c-105">Raunlægt heiti: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="9731c-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="9731c-106">Þessi tölusetning býður upp á valkost stöðugilda fyrir síun umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="9731c-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="9731c-107">Virði</span><span class="sxs-lookup"><span data-stu-id="9731c-107">Value</span></span> | <span data-ttu-id="9731c-108">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="9731c-108">Label</span></span> | <span data-ttu-id="9731c-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="9731c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9731c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="9731c-110">200000000</span></span> | <span data-ttu-id="9731c-111">Ekki tilbúið</span><span class="sxs-lookup"><span data-stu-id="9731c-111">Not Complete</span></span> | <span data-ttu-id="9731c-112">Umsækjandi hefur ekki enn lokið síun.</span><span class="sxs-lookup"><span data-stu-id="9731c-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="9731c-113">200000001</span><span class="sxs-lookup"><span data-stu-id="9731c-113">200000001</span></span> | <span data-ttu-id="9731c-114">Staðið</span><span class="sxs-lookup"><span data-stu-id="9731c-114">Pass</span></span> | <span data-ttu-id="9731c-115">Umsækjandi komst í gegnum síuna.</span><span class="sxs-lookup"><span data-stu-id="9731c-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="9731c-116">200000002</span><span class="sxs-lookup"><span data-stu-id="9731c-116">200000002</span></span> | <span data-ttu-id="9731c-117">Fella</span><span class="sxs-lookup"><span data-stu-id="9731c-117">Fail</span></span> | <span data-ttu-id="9731c-118">Umsækjandi komst ekki í gegnum síuna.</span><span class="sxs-lookup"><span data-stu-id="9731c-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9731c-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9731c-119">See also</span></span>

[<span data-ttu-id="9731c-120">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="9731c-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9731c-121">Dæmi um fyrirspurn fyrir umsækjanda til ráðningar</span><span class="sxs-lookup"><span data-stu-id="9731c-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]