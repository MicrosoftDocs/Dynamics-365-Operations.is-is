--- 
title: " Skilgreina kreditkortavinnslu"
description: "Þetta ferli fer í gegnum hvernig skal skoða lista yfir greiðsluþjónustuaðila og hvernig skilgreina skal greiðslulykill fyrir viðskiptakröfur."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3b54cfdb22c0c9daa9564ae36ad2bb89edb81f11
ms.contentlocale: is-is
ms.lasthandoff: 01/19/2018

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="57303-103"> Skilgreina kreditkortavinnslu</span><span class="sxs-lookup"><span data-stu-id="57303-103">Configure credit card processing</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="57303-104">Þetta ferli fer í gegnum hvernig skal skoða lista yfir greiðsluþjónustuaðila og hvernig skilgreina skal greiðslulykill fyrir viðskiptakröfur.</span><span class="sxs-lookup"><span data-stu-id="57303-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="57303-105">Þetta ferli notar sýnigögn USRT fyrirtæki og eru ætlaðar Kerfisstjórum og Tölvusérfræðingum.</span><span class="sxs-lookup"><span data-stu-id="57303-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="57303-106">Skoða lista yfir greiðsluþjónustuaðila</span><span class="sxs-lookup"><span data-stu-id="57303-106">View a list of payment providers</span></span>
1. <span data-ttu-id="57303-107">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluþjónusta.</span><span class="sxs-lookup"><span data-stu-id="57303-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="57303-108">Smellt er á Skoða tiltæka þjónustuaðila</span><span class="sxs-lookup"><span data-stu-id="57303-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="57303-109">Skilgreina greiðslulykil</span><span class="sxs-lookup"><span data-stu-id="57303-109">Configure payment account</span></span>
1. <span data-ttu-id="57303-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="57303-110">Click New.</span></span>
2. <span data-ttu-id="57303-111">í svæðinu Greiðsluþjónustu, færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="57303-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="57303-112">Í reitnum greiðslutengill, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="57303-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="57303-113">Víxla útvíkkun kaflans Greiðsluþjónustulykill.</span><span class="sxs-lookup"><span data-stu-id="57303-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="57303-114">Í umhverfinu: reitur, færðu inn „PROD“.</span><span class="sxs-lookup"><span data-stu-id="57303-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="57303-115">Smellt er á Kreditkortagerð.</span><span class="sxs-lookup"><span data-stu-id="57303-115">Click Credit card types.</span></span>
7. <span data-ttu-id="57303-116">Í reitnum greiðslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="57303-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="57303-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="57303-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="57303-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="57303-118">Click Add.</span></span>
10. <span data-ttu-id="57303-119">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="57303-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="57303-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="57303-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="57303-121">Í reitnum greiðslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="57303-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="57303-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="57303-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="57303-123">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="57303-123">Click Add.</span></span>
15. <span data-ttu-id="57303-124">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="57303-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="57303-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="57303-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57303-126">Hægt er að endurtaka ferlið fyrir eins margar kortategundir eins og þarf.</span><span class="sxs-lookup"><span data-stu-id="57303-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="57303-127">Í reitnum greiðslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="57303-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="57303-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="57303-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="57303-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="57303-129">Click Add.</span></span>
20. <span data-ttu-id="57303-130">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="57303-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="57303-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="57303-131">Click Save.</span></span>
22. <span data-ttu-id="57303-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="57303-132">Close the page.</span></span>
23. <span data-ttu-id="57303-133">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="57303-133">Click Validate.</span></span>
24. <span data-ttu-id="57303-134">Smellt er á Sjálfgefinn örgjörvi fyrir gátreit fyrir ný kreditkort .</span><span class="sxs-lookup"><span data-stu-id="57303-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="57303-135">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="57303-135">Click Save.</span></span>


