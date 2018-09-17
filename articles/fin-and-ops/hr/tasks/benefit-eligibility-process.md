--- 
title: "Feril fyrir hæfni til fríðinda"
description: "Þetta ferli sýnir hvernig ferli um hæfni til fríðinda virkar."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 859bf2ef369173ce4b6bc380820ea157ae86e13a
ms.contentlocale: is-is
ms.lasthandoff: 09/17/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="e1c7c-103">Feril fyrir hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="e1c7c-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1c7c-104">Þetta ferli sýnir hvernig ferli um hæfni til fríðinda virkar.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="e1c7c-105">Þegar ferlinu er lokið er hægt að skoða niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="e1c7c-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e1c7c-107">Farið í Mannauður > Fríðindi > Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="e1c7c-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e1c7c-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e1c7c-110">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-110">Click Edit.</span></span>
5. <span data-ttu-id="e1c7c-111">Veljið 'Reglumiðað' í svæðinu Hæfni.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="e1c7c-112">í svæðinu Reglu, Velja á stefnureglu fríðinda sem þú vilt beita á fríðinda .</span><span class="sxs-lookup"><span data-stu-id="e1c7c-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="e1c7c-113">Í aðgerðasvæðinu er smellt á fríðindi.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="e1c7c-114">Smellt er á Stofna hæfnistilvikinu til að opna svargluggann fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="e1c7c-115">Í reitinn tilvik skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="e1c7c-116">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="e1c7c-117">Í svæðinu Gerð tilviks, veljið 'Opna innskráningu'.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="e1c7c-118">Í svæðinu upphafsdagur tryggingar, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="e1c7c-119">Í svæði upphafsdagur  skráningartímabils, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="e1c7c-120">Í reitinn skráningardagar skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="e1c7c-121">Smellt er á Stofna tilvikið.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-121">Click Create event.</span></span>
16. <span data-ttu-id="e1c7c-122">Smella á bæta Við í Flýtiflipanum Starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="e1c7c-123">Í svæðinu Sýna eftir gerð, velja 'Starfsmenn'.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="e1c7c-124">Í  svæðinu Sýna eftir lögaðila, velja 'Núverandi lögaðila'.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="e1c7c-125">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="e1c7c-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-126">Click OK.</span></span>
21. <span data-ttu-id="e1c7c-127">Smellið á Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-127">Click Process.</span></span>
22. <span data-ttu-id="e1c7c-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-128">Click OK.</span></span>
23. <span data-ttu-id="e1c7c-129">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-129">Refresh the page.</span></span>
24. <span data-ttu-id="e1c7c-130">Smellt er á Sýna niðurstöður</span><span class="sxs-lookup"><span data-stu-id="e1c7c-130">Click Show results.</span></span>
25. <span data-ttu-id="e1c7c-131">Opnið dálkasía Stöðu.</span><span class="sxs-lookup"><span data-stu-id="e1c7c-131">Open Status column filter.</span></span>
26. <span data-ttu-id="e1c7c-132">Raða frá A til Ö</span><span class="sxs-lookup"><span data-stu-id="e1c7c-132">Sort A to Z</span></span>


