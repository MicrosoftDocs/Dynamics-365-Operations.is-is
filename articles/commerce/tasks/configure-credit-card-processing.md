---
title: " Skilgreina kreditkortavinnslu"
description: Þetta ferli fer í gegnum hvernig skal skoða lista yfir greiðsluþjónustuaðila og hvernig skilgreina skal greiðslulykill fyrir viðskiptakröfur.
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13aa59ab1c6b0170ae9ab8972fb00bcf47e2b754
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789757"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="53abc-103"> Skilgreina kreditkortavinnslu</span><span class="sxs-lookup"><span data-stu-id="53abc-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53abc-104">Þetta ferli fer í gegnum hvernig skal skoða lista yfir greiðsluþjónustuaðila og hvernig skilgreina skal greiðslulykill fyrir viðskiptakröfur.</span><span class="sxs-lookup"><span data-stu-id="53abc-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="53abc-105">Þetta ferli notar sýnigögn USRT fyrirtæki og eru ætlaðar Kerfisstjórum og Tölvusérfræðingum.</span><span class="sxs-lookup"><span data-stu-id="53abc-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="53abc-106">Skoða lista yfir greiðsluþjónustuaðila</span><span class="sxs-lookup"><span data-stu-id="53abc-106">View a list of payment providers</span></span>
1. <span data-ttu-id="53abc-107">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluþjónusta.</span><span class="sxs-lookup"><span data-stu-id="53abc-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="53abc-108">Smellt er á Skoða tiltæka þjónustuaðila</span><span class="sxs-lookup"><span data-stu-id="53abc-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="53abc-109">Skilgreina greiðslulykil</span><span class="sxs-lookup"><span data-stu-id="53abc-109">Configure payment account</span></span>
1. <span data-ttu-id="53abc-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="53abc-110">Click New.</span></span>
2. <span data-ttu-id="53abc-111">í svæðinu Greiðsluþjónustu, færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="53abc-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="53abc-112">Í reitnum greiðslutengill, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="53abc-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="53abc-113">Víxla útvíkkun kaflans Greiðsluþjónustulykill.</span><span class="sxs-lookup"><span data-stu-id="53abc-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="53abc-114">Í umhverfinu: reitur, færðu inn „PROD“.</span><span class="sxs-lookup"><span data-stu-id="53abc-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="53abc-115">Smellt er á Kreditkortagerð.</span><span class="sxs-lookup"><span data-stu-id="53abc-115">Click Credit card types.</span></span>
7. <span data-ttu-id="53abc-116">Í reitnum greiðslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="53abc-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="53abc-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="53abc-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="53abc-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="53abc-118">Click Add.</span></span>
10. <span data-ttu-id="53abc-119">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="53abc-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="53abc-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="53abc-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="53abc-121">Í reitnum greiðslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="53abc-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="53abc-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="53abc-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="53abc-123">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="53abc-123">Click Add.</span></span>
15. <span data-ttu-id="53abc-124">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="53abc-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="53abc-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="53abc-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="53abc-126">Hægt er að endurtaka ferlið fyrir eins margar kortategundir eins og þarf.</span><span class="sxs-lookup"><span data-stu-id="53abc-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="53abc-127">Í reitnum greiðslubók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="53abc-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="53abc-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="53abc-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="53abc-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="53abc-129">Click Add.</span></span>
20. <span data-ttu-id="53abc-130">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="53abc-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="53abc-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="53abc-131">Click Save.</span></span>
22. <span data-ttu-id="53abc-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="53abc-132">Close the page.</span></span>
23. <span data-ttu-id="53abc-133">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="53abc-133">Click Validate.</span></span>
24. <span data-ttu-id="53abc-134">Smellt er á Sjálfgefinn örgjörvi fyrir gátreit fyrir ný kreditkort .</span><span class="sxs-lookup"><span data-stu-id="53abc-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="53abc-135">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="53abc-135">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]