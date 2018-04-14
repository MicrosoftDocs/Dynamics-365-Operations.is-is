--- 
title: "Búa til spurningu sem er háð svari við fyrri spurningu"
description: "Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu."
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d3221a62079e719c1d9d6f2df8edf8c5ed5584b7
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="cdf4d-103">Búa til spurningu sem er háð svari við fyrri spurningu</span><span class="sxs-lookup"><span data-stu-id="cdf4d-103">Make a question dependent on the answer of the previous question</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cdf4d-104">Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="cdf4d-105">Til dæmis, ef spyrja „Finnst þér betra kaffi eða te", röklegt eftirfylgni spurningu getur verið ákvörðuð eftir því hvort svarandi velur kaffi eða te sem svar sitt.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="cdf4d-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="cdf4d-107">Finna fyrirliggjandi spurningalista</span><span class="sxs-lookup"><span data-stu-id="cdf4d-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="cdf4d-108">Fara í Spurningalisti > Hönnun > Spurningalistar.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="cdf4d-109">Velja spurningalistann WorkFH á listanum.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="cdf4d-110">Bæta við spurningum og undirspurningar við Spurningalista</span><span class="sxs-lookup"><span data-stu-id="cdf4d-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="cdf4d-111">Smellt er á Spurningar.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-111">Click Questions.</span></span>
2. <span data-ttu-id="cdf4d-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-112">Click New.</span></span>
3. <span data-ttu-id="cdf4d-113">Veljið númer spurningu 00016 í svæðinu Spurningu.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="cdf4d-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cdf4d-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cdf4d-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-116">Click Save.</span></span>
7. <span data-ttu-id="cdf4d-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="cdf4d-118">Stilla Röð Spurningalista á Skilyrt og gera spurninguna háða viðeigandi spurningu</span><span class="sxs-lookup"><span data-stu-id="cdf4d-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="cdf4d-119">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-119">Click Edit.</span></span>
2. <span data-ttu-id="cdf4d-120">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="cdf4d-121">Veljið 'Skilyrt' í svæðinu röðun Spurninga.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="cdf4d-122">Smellt er á Skilyrðisbundin spurning</span><span class="sxs-lookup"><span data-stu-id="cdf4d-122">Click Conditional question.</span></span>
5. <span data-ttu-id="cdf4d-123">Veljið ‚Spurningar\útskýra hvers vegna þú svaraðir fyrri spurningu eins og þú gerðir?', í trénu.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="cdf4d-124">Velja spurninguna 00009 í svæðinu aðalspurning</span><span class="sxs-lookup"><span data-stu-id="cdf4d-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="cdf4d-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cdf4d-126">Í svarreitnum, Færa inn Kenni svarraðar fyrir svarvalkost sem gera á spurningu háða.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="cdf4d-127">Settu Til dæmis inn 1 fyrir fyrsta svarvalkost.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="cdf4d-128">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-128">Click Save.</span></span>
10. <span data-ttu-id="cdf4d-129">Í trénu, velja ‚Spurningar\ Ég fæ sanngjörn laun fyrir mína vinnu.'.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="cdf4d-130">Athugið að spurningatréð var uppfært til að sýna háðar kringumstæður.</span><span class="sxs-lookup"><span data-stu-id="cdf4d-130">Note that the question tree updated to show the dependency.</span></span>  


