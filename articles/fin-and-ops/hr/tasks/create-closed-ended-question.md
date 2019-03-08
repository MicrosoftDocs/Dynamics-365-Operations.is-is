---
title: Búa til afmarkaða spurningu
description: Lokaðar spurningar gera kleift að gefa upp valkosti fyrir svarendur til að velja úr.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b08988a3872cec39b7592732d23862e959aae79
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "332266"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="5f30d-103">Búa til afmarkaða spurningu</span><span class="sxs-lookup"><span data-stu-id="5f30d-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f30d-104">Lokaðar spurningar gera kleift að gefa upp valkosti fyrir svarendur til að velja úr.</span><span class="sxs-lookup"><span data-stu-id="5f30d-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="5f30d-105">Fyrst þarf að stofna svarflokkinn með svör, þá spurningu sem á að nota svarsafnið.</span><span class="sxs-lookup"><span data-stu-id="5f30d-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="5f30d-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="5f30d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="5f30d-107">Stofna svarsafn</span><span class="sxs-lookup"><span data-stu-id="5f30d-107">Create an answer group</span></span>
1. <span data-ttu-id="5f30d-108">Farið í Spurningalisti > Hönnun > Svarflokkar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="5f30d-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5f30d-109">Click New.</span></span>
3. <span data-ttu-id="5f30d-110">Í reitinn svarsafn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="5f30d-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="5f30d-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5f30d-112">Nota aðgerðina Slembiraða eigi að raða af handahófi svörin í mismunandi röð í hvert sinn sem svarsafn er notuð við spurningu.</span><span class="sxs-lookup"><span data-stu-id="5f30d-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="5f30d-113">Smellt er á Svar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-113">Click Answer.</span></span>
6. <span data-ttu-id="5f30d-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5f30d-114">Click New.</span></span>
    * <span data-ttu-id="5f30d-115">Raðnúmer stýrir röðinni sem svörin eru birt, nema Slembiröðun er valið fyrir svarsafnið.</span><span class="sxs-lookup"><span data-stu-id="5f30d-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="5f30d-116">Stig má gefa fyrir svör til þess að nota fyrir stigagjöf spurningalista.</span><span class="sxs-lookup"><span data-stu-id="5f30d-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="5f30d-117">Í reitinn stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5f30d-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="5f30d-118">Hægt er að merkja rétt svar til að tilgreina að valið svar er rétt.</span><span class="sxs-lookup"><span data-stu-id="5f30d-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="5f30d-119">Hægt er að nota þetta til stigagjöf spurningalista .</span><span class="sxs-lookup"><span data-stu-id="5f30d-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="5f30d-120">Í reitnum svarreitur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="5f30d-121">Halda áfram að stofna svar valkosti svarsafns.</span><span class="sxs-lookup"><span data-stu-id="5f30d-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="5f30d-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5f30d-122">Click New.</span></span>
10. <span data-ttu-id="5f30d-123">Í reitinn stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5f30d-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="5f30d-124">Í reitnum svarreitur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="5f30d-125">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="5f30d-125">Click New.</span></span>
13. <span data-ttu-id="5f30d-126">Í reitinn stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5f30d-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="5f30d-127">Í reitnum svarreitur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="5f30d-128">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="5f30d-128">Click New.</span></span>
16. <span data-ttu-id="5f30d-129">Í reitinn stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5f30d-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="5f30d-130">Í reitnum svarreitur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="5f30d-131">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="5f30d-131">Click New.</span></span>
19. <span data-ttu-id="5f30d-132">Í reitinn stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5f30d-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="5f30d-133">Í reitnum svarreitur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="5f30d-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5f30d-134">Close the page.</span></span>
22. <span data-ttu-id="5f30d-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5f30d-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="5f30d-136">Stofna Spurning.</span><span class="sxs-lookup"><span data-stu-id="5f30d-136">Create the question</span></span>
1. <span data-ttu-id="5f30d-137">Fara í Spurningalisti > Hönnun > Spurningar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="5f30d-138">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5f30d-138">Click New.</span></span>
3. <span data-ttu-id="5f30d-139">Gerðarsvæðið er notuð til að flokka saman spurningar sem eru tengdar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="5f30d-140">Hægt er að nota gátreit af gerðunum inntaks gerðir, aukahnappur eða samtvinnaður reitur fyrir lokaðar spurningar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="5f30d-141">Veljið valkost í svæðinu gerð Innsláttar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="5f30d-142">Færa inn eða veljið gildi í svæðinu svaraflokkar.</span><span class="sxs-lookup"><span data-stu-id="5f30d-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="5f30d-143">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5f30d-143">In the Text field, type a value.</span></span>

