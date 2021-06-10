---
title: Undanþágustaða starfs
description: Þetta efnisatriði lýsir valmöguleika undanþágustöðu starfs fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053852"
---
# <a name="job-exempt-status"></a><span data-ttu-id="7a69e-103">Undanþágustaða starfs</span><span class="sxs-lookup"><span data-stu-id="7a69e-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7a69e-104">Þetta efnisatriði lýsir valmöguleika undanþágustöðu starfs fyrir Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7a69e-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7a69e-105">Raunlægt heiti: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="7a69e-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="7a69e-106">Þessi upptalning tilgreinir valmöguleika fyrir stöðugildi undanþágu á FLSA-starfi.</span><span class="sxs-lookup"><span data-stu-id="7a69e-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="7a69e-107">Boðið er upp á þetta í fyrirliggjandi valmöguleika cdm_jobexemptstatus.</span><span class="sxs-lookup"><span data-stu-id="7a69e-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="7a69e-108">Virði</span><span class="sxs-lookup"><span data-stu-id="7a69e-108">Value</span></span> | <span data-ttu-id="7a69e-109">Merkimiði</span><span class="sxs-lookup"><span data-stu-id="7a69e-109">Label</span></span> | <span data-ttu-id="7a69e-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="7a69e-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7a69e-111">200000000</span><span class="sxs-lookup"><span data-stu-id="7a69e-111">200000000</span></span> | <span data-ttu-id="7a69e-112">Undanþága</span><span class="sxs-lookup"><span data-stu-id="7a69e-112">Exempt</span></span> | <span data-ttu-id="7a69e-113">Starfið er með undanþágustöðu samkvæmt FLSA-leiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="7a69e-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="7a69e-114">200000001</span><span class="sxs-lookup"><span data-stu-id="7a69e-114">200000001</span></span> | <span data-ttu-id="7a69e-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="7a69e-115">NonExempt</span></span> | <span data-ttu-id="7a69e-116">Starfið er með ekki undanþágustöðu samkvæmt FLSA-leiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="7a69e-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="7a69e-117">200000002</span><span class="sxs-lookup"><span data-stu-id="7a69e-117">200000002</span></span> | <span data-ttu-id="7a69e-118">Á ekki við</span><span class="sxs-lookup"><span data-stu-id="7a69e-118">Does Not Apply</span></span> | <span data-ttu-id="7a69e-119">Stöðuleiðbeiningar FLSA eiga ekki við um starfið.</span><span class="sxs-lookup"><span data-stu-id="7a69e-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7a69e-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7a69e-120">See also</span></span>

[<span data-ttu-id="7a69e-121">Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda</span><span class="sxs-lookup"><span data-stu-id="7a69e-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7a69e-122">Dæmi um fyrirspurn fyrir ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="7a69e-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]