--- 
title: " Stofna heimildaflokka sölustaða"
description: "Þetta ferli mun sýna hvernig á að stofna heimildaflokk Sölustaðar."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b17f4a07fdc35e06f993dac11e5a88e5e96e72cc
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="11da5-103"> Stofna heimildaflokka sölustaða</span><span class="sxs-lookup"><span data-stu-id="11da5-103">Create POS permission groups</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="11da5-104">Þetta ferli mun sýna hvernig á að stofna heimildaflokk Sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="11da5-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="11da5-105">Sýnigögn fyrirtækisins til að stofna verkið er USRT.</span><span class="sxs-lookup"><span data-stu-id="11da5-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="11da5-106">Þetta verk er ætluð fyrir hlutverk stjórnanda Smásölu aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="11da5-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="11da5-107">Fara á heimildaflokkur.</span><span class="sxs-lookup"><span data-stu-id="11da5-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="11da5-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="11da5-108">Click New.</span></span>
3. <span data-ttu-id="11da5-109">Færa inn gildi í reitnum Kenni heimildaflokkur sölustaðar .</span><span class="sxs-lookup"><span data-stu-id="11da5-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="11da5-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="11da5-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="11da5-111">Velja skal Já í svæðinu Skoða færslur stimpilklukku .</span><span class="sxs-lookup"><span data-stu-id="11da5-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="11da5-112">Nú er hægt að virkja eða óvirkja mismunandi heimildir fyrir heimildaflokk Sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="11da5-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="11da5-113">Í sumum heimild hægt að stilla gildi sem verður notað til að meta ef notanda sölustaður getur framkvæmt aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="11da5-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="11da5-114">Þessi leiðarvísi fyrir verk virkjar nokkrar heimild sem hugsanlega má veita gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="11da5-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="11da5-115">Velja skal Já í Leyfa það að stofna pöntunarsvæðið.</span><span class="sxs-lookup"><span data-stu-id="11da5-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="11da5-116">Velja skal Já í svæðinu Leyfa breyta pöntun.</span><span class="sxs-lookup"><span data-stu-id="11da5-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="11da5-117">Velja skal Já í svæðinu Leyfa sækja pöntun.</span><span class="sxs-lookup"><span data-stu-id="11da5-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="11da5-118">Velja skal Já í Leyfa svæði fyrir breytingu á aðgangsorðs.</span><span class="sxs-lookup"><span data-stu-id="11da5-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="11da5-119">Velja skal Já í Leyfa svæði falið loka.</span><span class="sxs-lookup"><span data-stu-id="11da5-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="11da5-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="11da5-120">Click Save.</span></span>
    * <span data-ttu-id="11da5-121">Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á smásölurása.</span><span class="sxs-lookup"><span data-stu-id="11da5-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="11da5-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="11da5-122">Close the page.</span></span>
13. <span data-ttu-id="11da5-123">Fara í vinnslur.</span><span class="sxs-lookup"><span data-stu-id="11da5-123">Go to Jobs.</span></span>
    * <span data-ttu-id="11da5-124">Næsta verður að úthluta heimildaflokk Sölustaðar til Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="11da5-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="11da5-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="11da5-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="11da5-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="11da5-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="11da5-127">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="11da5-127">Click Edit.</span></span>
17. <span data-ttu-id="11da5-128">Útvíkka hlutann flokkun Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="11da5-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="11da5-129">Í reitinn Heimildaflokkur sölustaðar skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11da5-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="11da5-130">Allir starfsmenn í stöðum fyrir þessa vinnslu Munu nota stillingar þessa heimildaflokk Sölustaðar nema heimildir Sölustaðar starfsmanna hafi verið hnekkt á stigi Stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="11da5-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="11da5-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="11da5-131">Click Save.</span></span>
    * <span data-ttu-id="11da5-132">Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á smásölurása.</span><span class="sxs-lookup"><span data-stu-id="11da5-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


