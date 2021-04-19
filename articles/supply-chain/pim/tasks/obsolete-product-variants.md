---
title: Finna úrelt afurðarafbrigði
description: Þetta ferli sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 807297a87a7f0e59023d80fbd371bffbf2b086bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807993"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="1047d-103">Finna úrelt afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="1047d-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1047d-104">Þetta ferli sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir.</span><span class="sxs-lookup"><span data-stu-id="1047d-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="1047d-105">Forkröfur: Skilgreina þarf að minnsta kosti eina lífferlisstöðu afurðar sem er óvirk fyrir áætlanagerð áður en hægt er að spila þessar verkefnaleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="1047d-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="1047d-106">Keyra hermingu</span><span class="sxs-lookup"><span data-stu-id="1047d-106">Run a simulation</span></span>
1. <span data-ttu-id="1047d-107">Fara í Afurðaupplýsingastjórnun > Reglubundin verk > Breyta lífferilsstöðu fyrir úreltar vörur.</span><span class="sxs-lookup"><span data-stu-id="1047d-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="1047d-108">Sláið inn eða veljið gildi í reitnum Ný lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="1047d-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="1047d-109">Velja skal Já í Keyra hermun án þess að uppfæra afurðagagnareit.</span><span class="sxs-lookup"><span data-stu-id="1047d-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="1047d-110">Í reitinum Útiloka vörur sem voru búnar til innan þessa dagafjölda skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="1047d-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="1047d-111">Í reitinum Útiloka vörur sem hafa verið notaðar í færslum (í dagafjölda) skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="1047d-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="1047d-112">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="1047d-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="1047d-113">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="1047d-113">Click Filter.</span></span>
8. <span data-ttu-id="1047d-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1047d-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="1047d-115">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1047d-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="1047d-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1047d-116">Click OK.</span></span>
11. <span data-ttu-id="1047d-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1047d-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="1047d-118">Mælt er með því að keyra hermingu í lotu ef þú býst við að leita að fjölda vara.</span><span class="sxs-lookup"><span data-stu-id="1047d-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="1047d-119">Gakktu einnig úr skugga um að hermingin sé ekki keyrð á virkasta vinnutíma fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="1047d-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="1047d-120">Skoða niðurstöðuna fyrir herminguna</span><span class="sxs-lookup"><span data-stu-id="1047d-120">Review the simulation results</span></span>
1. <span data-ttu-id="1047d-121">Farið í Afurðarupplýsingastjórnun > Fyrirspurnir og skýrslur > Ferill lífferils- og viðhaldsstöðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="1047d-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="1047d-122">Á þessari síðu er hægt að sjá herminiðurstöðurnar og meta hversu margar vörur og afurðaafbrigði verða tengd nýrri lífferilsstöðu afurðar þegar uppfærslan er keyrð án hermunar.</span><span class="sxs-lookup"><span data-stu-id="1047d-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="1047d-123">Keyra skal uppfærslu Lífferlisstaða afurðar fyrir úreltar vörur</span><span class="sxs-lookup"><span data-stu-id="1047d-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="1047d-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1047d-124">Close the page.</span></span>
2. <span data-ttu-id="1047d-125">Fara í Afurðaupplýsingastjórnun > Reglubundin verk > Breyta lífferilsstöðu fyrir úreltar vörur.</span><span class="sxs-lookup"><span data-stu-id="1047d-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="1047d-126">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="1047d-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="1047d-127">Athugið að síðasta val hefur verið vistað.</span><span class="sxs-lookup"><span data-stu-id="1047d-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="1047d-128">Velja skal Nei í Keyra hermun án þess að uppfæra afurðagagnareit.</span><span class="sxs-lookup"><span data-stu-id="1047d-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="1047d-129">Stækka útvíkkun á liðnum Keyra í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="1047d-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="1047d-130">Íhuga ætti að keyra þessa vinnslu í lotu, eftir því hversu margar vörur og afurðarafbrigði eru valin.</span><span class="sxs-lookup"><span data-stu-id="1047d-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="1047d-131">Gangið úr skugga um að keyra ekki stórt uppfærsluverk á virkasta vinnutíma fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="1047d-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="1047d-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1047d-132">Click OK.</span></span>
7. <span data-ttu-id="1047d-133">Farið í Afurðarupplýsingastjórnun > Fyrirspurnir og skýrslur > Ferill lífferils- og viðhaldsstöðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="1047d-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="1047d-134">Skoða breyttar útgefnar vörur og vöruafbrigði.</span><span class="sxs-lookup"><span data-stu-id="1047d-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="1047d-135">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1047d-135">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]