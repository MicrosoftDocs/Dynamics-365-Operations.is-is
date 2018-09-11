--- 
title: "Auðkenna og beita verkfærum við val á umsækjendum"
description: "Finna hæf hóp af umsækjendum til að fylla lausar stöður getur verið erfitt, sérstaklega þegar stöðu krefst sérstaks safns af hæfileikum."
author: kherr75
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 552009ae1cae0797191b4cdaeba3a1731b501a7d
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="b1c78-103">Auðkenna og beita verkfærum við val á umsækjendum</span><span class="sxs-lookup"><span data-stu-id="b1c78-103">Identify and deploy candidate selection tools</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1c78-104">Finna hæf hóp af umsækjendum til að fylla lausar stöður getur verið erfitt, sérstaklega þegar stöðu krefst sérstaks safns af hæfileikum.</span><span class="sxs-lookup"><span data-stu-id="b1c78-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="b1c78-105">Hins vegar umsækjendur með hæfni sem þarf gæti þegar verið ráðinn í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b1c78-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="b1c78-106">Hægt er að leita að sérþekkingu á meðal núverandi starfsmanna eða nýrra umsækjenda.</span><span class="sxs-lookup"><span data-stu-id="b1c78-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="b1c78-107">Þetta leyfir ráðningaraðila til að safna og skoða umsækjendur sem hafa sótt um opna stöðu nú eða í áður eða til að finna möguleg umsækjendur úr þeirra fyrirliggjandi hóp starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="b1c78-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="b1c78-108">Þessi verkskráningu er notuð til að fræðast um hvernig virkni hæfnisskrár getur hjálpað við að finna réttan einstaklingur fyrir opna stöðu.</span><span class="sxs-lookup"><span data-stu-id="b1c78-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="b1c78-109">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="b1c78-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b1c78-110">Farið í Mannauður > Hæfni > Hæfnigreining > Forstillingar hæfnisskráningar.</span><span class="sxs-lookup"><span data-stu-id="b1c78-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="b1c78-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1c78-111">Click New.</span></span>
3. <span data-ttu-id="b1c78-112">Í svæðinu hæfnisskrá, færið inn heiti fyrir þitt hæfnisskrá.</span><span class="sxs-lookup"><span data-stu-id="b1c78-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="b1c78-113">Dæmi: Bókari.</span><span class="sxs-lookup"><span data-stu-id="b1c78-113">Example: Accountant.</span></span>
4. <span data-ttu-id="b1c78-114">Færið inn lýsingu á hæfnisskrá í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="b1c78-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="b1c78-115">Dagsetning er rituð í reitinn Dagetning.</span><span class="sxs-lookup"><span data-stu-id="b1c78-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="b1c78-116">Smellt er á sækja forstilling.</span><span class="sxs-lookup"><span data-stu-id="b1c78-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="b1c78-117">Nota Sækja forstillingu til að sækja á vottorð, Hæfni, og Menntun úr völdum Aðila, Vinnslu eða Námskeið sem grunn fyrir leitina.</span><span class="sxs-lookup"><span data-stu-id="b1c78-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="b1c78-118">Síðan er hægt að bæta við eða fjarlægja skilyrði, ef skilyrði er valfrjáls og meta mikilvægi skilyrða.</span><span class="sxs-lookup"><span data-stu-id="b1c78-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="b1c78-119">Smellt er á verk</span><span class="sxs-lookup"><span data-stu-id="b1c78-119">Click Job.</span></span>
8. <span data-ttu-id="b1c78-120">Sláið inn eða veldu gildi í reitnum Verk.</span><span class="sxs-lookup"><span data-stu-id="b1c78-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="b1c78-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1c78-121">Click OK.</span></span>
10. <span data-ttu-id="b1c78-122">Víkka flýtiflipann svið, og bættu við einhverjum viðbótarupplýsingar, eins og deild.</span><span class="sxs-lookup"><span data-stu-id="b1c78-122">Expand the range fast tab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="b1c78-123">Víkka flýtiflipann skírteini til að skoða eða breyta skírteini.</span><span class="sxs-lookup"><span data-stu-id="b1c78-123">Expand the certificates fast tab to view or edit the certificates.</span></span>
12. <span data-ttu-id="b1c78-124">Víkka flýtiflipann Hæfni til að skoða eða breyta hæfni.</span><span class="sxs-lookup"><span data-stu-id="b1c78-124">Expand the Skills fast tab to view or edit the skills.</span></span>
13. <span data-ttu-id="b1c78-125">Víkka flýtiflipann Menntun til að skoða eða breyta skilyrðum menntun.</span><span class="sxs-lookup"><span data-stu-id="b1c78-125">Expand the Education fast tab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="b1c78-126">Smelltu á Keyra.</span><span class="sxs-lookup"><span data-stu-id="b1c78-126">Click Execute.</span></span>
15. <span data-ttu-id="b1c78-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1c78-127">Click OK.</span></span>
16. <span data-ttu-id="b1c78-128">Smelltu á Niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="b1c78-128">Click Result.</span></span>
17. <span data-ttu-id="b1c78-129">Smelltu á Niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="b1c78-129">Click Result.</span></span>
18. <span data-ttu-id="b1c78-130">Smellt er á Halda áfram.</span><span class="sxs-lookup"><span data-stu-id="b1c78-130">Click Resume.</span></span>
19. <span data-ttu-id="b1c78-131">Smellt er á Skírteini.</span><span class="sxs-lookup"><span data-stu-id="b1c78-131">Click Certificates.</span></span>
    * <span data-ttu-id="b1c78-132">Hægt er að kafa frekar í hvern einstakling fram og til að sjá upplýsingar varðandi þeirra menntun, hæfni, starfsreynslu o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="b1c78-132">You can drill further into each person listed and see details regarding their education, skills, professional experience etc.</span></span>  
20. <span data-ttu-id="b1c78-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1c78-133">Close the page.</span></span>
21. <span data-ttu-id="b1c78-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1c78-134">Close the page.</span></span>
22. <span data-ttu-id="b1c78-135">Velja niðurstöðu aftur.</span><span class="sxs-lookup"><span data-stu-id="b1c78-135">Select result again.</span></span>
23. <span data-ttu-id="b1c78-136">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="b1c78-136">Click Report.</span></span>
    * <span data-ttu-id="b1c78-137">Skýrslan verður að birta besta samsvörun efst á skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b1c78-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="b1c78-138">Þú getur séð að eyða kemur fram á listanum.</span><span class="sxs-lookup"><span data-stu-id="b1c78-138">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="b1c78-139">Það er mismunurinn á stigi sem var skráð á hæfnisskrá og stig hæfninnar sem er úthlutað á þann einstakling.</span><span class="sxs-lookup"><span data-stu-id="b1c78-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="b1c78-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1c78-140">Close the page.</span></span>
25. <span data-ttu-id="b1c78-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1c78-141">Click Save.</span></span>


