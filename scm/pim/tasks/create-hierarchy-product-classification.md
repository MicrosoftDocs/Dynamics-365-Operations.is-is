--- 
title: "Stofna stigveldi afurðaflokkunar"
description: "Þessi verklýsing sýnir hvernig á að stofna nýtt tegundastigveldi og tengja gerð stigveldis vörukóða."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="1e8ab-103">Stofna stigveldi afurðaflokkunar</span><span class="sxs-lookup"><span data-stu-id="1e8ab-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e8ab-104">Þessi verklýsing sýnir hvernig á að stofna nýtt tegundastigveldi og tengja gerð stigveldis vörukóða.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="1e8ab-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1e8ab-106">Þetta ferli er ætluð fyrir stjórnanda tegundar.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="1e8ab-107">Stofna nýtt tegundastigveldi</span><span class="sxs-lookup"><span data-stu-id="1e8ab-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="1e8ab-108">Fara í Vöruupplýsingastjórnun > Uppsetning > Efnisflokkar og eigindir > Flokkastigveldi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="1e8ab-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-109">Click New.</span></span>
3. <span data-ttu-id="1e8ab-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1e8ab-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1e8ab-112">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="1e8ab-113">Byggja stigveldi</span><span class="sxs-lookup"><span data-stu-id="1e8ab-113">Build the hierarchy</span></span>
1. <span data-ttu-id="1e8ab-114">Smellt er á Nýr tegundahnútur.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-114">Click New category node.</span></span>
2. <span data-ttu-id="1e8ab-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="1e8ab-116">Í reitnum Kóði skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="1e8ab-117">Í reitinn stutt heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="1e8ab-118">Smellt er á Nýr tegundahnútur.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-118">Click New category node.</span></span>
6. <span data-ttu-id="1e8ab-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="1e8ab-120">Í reitnum Kóði skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="1e8ab-121">Í reitinn stutt heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="1e8ab-122">Smellt er á Nýr tegundahnútur.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-122">Click New category node.</span></span>
10. <span data-ttu-id="1e8ab-123">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="1e8ab-124">Í reitnum Kóði skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="1e8ab-125">Í reitinn stutt heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="1e8ab-126">Smellt er á Nýr tegundahnútur.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-126">Click New category node.</span></span>
14. <span data-ttu-id="1e8ab-127">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="1e8ab-128">Í reitnum Kóði skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="1e8ab-129">Í reitinn stutt heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="1e8ab-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="1e8ab-131">Flokka stigveldi</span><span class="sxs-lookup"><span data-stu-id="1e8ab-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="1e8ab-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="1e8ab-133">Á Aðgerðarúðu, smellið á  tegundastigveldi.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="1e8ab-134">Smellt er á Tengja stigveldistegund.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="1e8ab-135">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-135">Click New.</span></span>
5. <span data-ttu-id="1e8ab-136">Í reitnum Tegundastigveldi skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="1e8ab-137">Veljið Vörukóða gerðar tegundarstigveldiskóða fyrir flokkun afurðar.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="1e8ab-138">Í reitnum Tegundastigveld skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1e8ab-139">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1e8ab-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1e8ab-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1e8ab-141">Close the page.</span></span>


