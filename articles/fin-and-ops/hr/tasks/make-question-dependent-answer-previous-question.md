---
title: Búa til spurningu sem er háð svari við fyrri spurningu
description: Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb79398f5a0ebdbdb774c106c90ca50a69c275e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "341282"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="eb4ba-103">Búa til spurningu sem er háð svari við fyrri spurningu</span><span class="sxs-lookup"><span data-stu-id="eb4ba-103">Make a question dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb4ba-104">Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="eb4ba-105">Til dæmis, ef spyrja „Finnst þér betra kaffi eða te", röklegt eftirfylgni spurningu getur verið ákvörðuð eftir því hvort svarandi velur kaffi eða te sem svar sitt.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="eb4ba-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="eb4ba-107">Finna fyrirliggjandi spurningalista</span><span class="sxs-lookup"><span data-stu-id="eb4ba-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="eb4ba-108">Fara í Spurningalisti > Hönnun > Spurningalistar.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="eb4ba-109">Velja spurningalistann WorkFH á listanum.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="eb4ba-110">Bæta við spurningum og undirspurningar við Spurningalista</span><span class="sxs-lookup"><span data-stu-id="eb4ba-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="eb4ba-111">Smellt er á Spurningar.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-111">Click Questions.</span></span>
2. <span data-ttu-id="eb4ba-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-112">Click New.</span></span>
3. <span data-ttu-id="eb4ba-113">Veljið númer spurningu 00016 í svæðinu Spurningu.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="eb4ba-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="eb4ba-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="eb4ba-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-116">Click Save.</span></span>
7. <span data-ttu-id="eb4ba-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="eb4ba-118">Stilla Röð Spurningalista á Skilyrt og gera spurninguna háða viðeigandi spurningu</span><span class="sxs-lookup"><span data-stu-id="eb4ba-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="eb4ba-119">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-119">Click Edit.</span></span>
2. <span data-ttu-id="eb4ba-120">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="eb4ba-121">Veljið 'Skilyrt' í svæðinu röðun Spurninga.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="eb4ba-122">Smellt er á Skilyrðisbundin spurning</span><span class="sxs-lookup"><span data-stu-id="eb4ba-122">Click Conditional question.</span></span>
5. <span data-ttu-id="eb4ba-123">Veljið ‚Spurningar\útskýra hvers vegna þú svaraðir fyrri spurningu eins og þú gerðir?', í trénu.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="eb4ba-124">Velja spurninguna 00009 í svæðinu aðalspurning</span><span class="sxs-lookup"><span data-stu-id="eb4ba-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="eb4ba-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eb4ba-126">Í svarreitnum, Færa inn Kenni svarraðar fyrir svarvalkost sem gera á spurningu háða.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="eb4ba-127">Settu Til dæmis inn 1 fyrir fyrsta svarvalkost.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="eb4ba-128">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-128">Click Save.</span></span>
10. <span data-ttu-id="eb4ba-129">Í trénu, velja ‚Spurningar\ Ég fæ sanngjörn laun fyrir mína vinnu.'.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="eb4ba-130">Athugið að spurningatréð var uppfært til að sýna háðar kringumstæður.</span><span class="sxs-lookup"><span data-stu-id="eb4ba-130">Note that the question tree updated to show the dependency.</span></span>  

