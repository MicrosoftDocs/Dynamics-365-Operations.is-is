---
title: Þróa og opna tilkynningar um lausar stöður
description: Ráðningarverk hjálpa til við að stjórna ráðningarferlið.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55260a4d25f41bc649f5e1f1f8c950c6b438ecfb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144042"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="4506d-103">Þróa og opna tilkynningar um lausar stöður</span><span class="sxs-lookup"><span data-stu-id="4506d-103">Develop and open job requisition</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4506d-104">Ráðningarverk hjálpa til við að stjórna ráðningarferlið.</span><span class="sxs-lookup"><span data-stu-id="4506d-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="4506d-105">Fyrir hvert ráðningarverk, getur þú sett upp upplýsingar, svo sem verk sem ráðningu er fyrir, nafn ráðningaraðila, stöðu verkefnisins og deild sem starfið verður staðsett í.</span><span class="sxs-lookup"><span data-stu-id="4506d-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="4506d-106">Eftir stofnun ráðningarverks, er hægt skrifa atvinnuauglýsingu fyrir verkið, birta auglýsinguna í sjálfsafgreiðslusíðum Starfsmanna, tengja starfsumsóknir við verkið og rekja aðgerðir fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="4506d-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="4506d-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="4506d-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4506d-108">Til að hefja ferlið, farið í Mannauður > Ráðningar > Ráðningarverk > Ráðningarverk</span><span class="sxs-lookup"><span data-stu-id="4506d-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="4506d-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4506d-109">Click New.</span></span>
2. <span data-ttu-id="4506d-110">Í svæðinu ráðningarverk, færið inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4506d-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="4506d-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="4506d-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="4506d-112">Í reitnum Ráðningaraðili skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4506d-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4506d-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4506d-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="4506d-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4506d-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4506d-115">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="4506d-115">Click Select.</span></span>
8. <span data-ttu-id="4506d-116">Í reitnum Deild skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4506d-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4506d-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4506d-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4506d-118">Í reitnum Starf skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4506d-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4506d-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4506d-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="4506d-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4506d-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4506d-121">Í svæðinu Fjölda opnana skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="4506d-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="4506d-122">Í reitnum Ráðningarstjóri skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4506d-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4506d-123">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4506d-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="4506d-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4506d-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="4506d-125">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="4506d-125">Click Select.</span></span>
18. <span data-ttu-id="4506d-126">Færa inn dagsetningu í svæði umsóknarfrestur.</span><span class="sxs-lookup"><span data-stu-id="4506d-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="4506d-127">Smellt er á Miðlar.</span><span class="sxs-lookup"><span data-stu-id="4506d-127">Click Media.</span></span>
    * <span data-ttu-id="4506d-128">Ráðningarverk með valkost til að tilgreina miðla sem nota á til að auglýsa opnar stöður.</span><span class="sxs-lookup"><span data-stu-id="4506d-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="4506d-129">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4506d-129">Click New.</span></span>
21. <span data-ttu-id="4506d-130">Í reitnum Miðlunarefni skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4506d-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="4506d-131">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4506d-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="4506d-132">Dagsetning er rituð í reitinn Upphafsdagur.</span><span class="sxs-lookup"><span data-stu-id="4506d-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="4506d-133">Dagsetning er rituð í reitinn Lokadagur.</span><span class="sxs-lookup"><span data-stu-id="4506d-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="4506d-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4506d-134">Click Save.</span></span>
26. <span data-ttu-id="4506d-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4506d-135">Close the page.</span></span>
27. <span data-ttu-id="4506d-136">Smellt er á starfsauglýsingar.</span><span class="sxs-lookup"><span data-stu-id="4506d-136">Click Job ads.</span></span>
28. <span data-ttu-id="4506d-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4506d-137">Click Save.</span></span>
29. <span data-ttu-id="4506d-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4506d-138">Close the page.</span></span>
30. <span data-ttu-id="4506d-139">Merkja eða afmerkja gátreitinn Birta á sjálfsafgreiðsla starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="4506d-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="4506d-140">Velja gátreitinn Sýna á sjálfsafgreiðslu starfsmanns til að gera ráðningarverkið sýnileg starfsmönnum á þeirra sjálfsafgreiðslusíðum Starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="4506d-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="4506d-141">Smellt er á Staða ráðningarverks.</span><span class="sxs-lookup"><span data-stu-id="4506d-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="4506d-142">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="4506d-142">Click Start.</span></span>
    * <span data-ttu-id="4506d-143">Stöðuna Byrjað merkir að verkið sé tilbúin til að fá umsóknir.</span><span class="sxs-lookup"><span data-stu-id="4506d-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="4506d-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4506d-144">Click OK.</span></span>

