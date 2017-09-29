--- 
title: "Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum"
description: "Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4f9f9473d0872d68571b87409b93e0cf5455364c
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="2dc49-103">Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum</span><span class="sxs-lookup"><span data-stu-id="2dc49-103">Create a bill of materials for a dimension-based product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2dc49-104">Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum.</span><span class="sxs-lookup"><span data-stu-id="2dc49-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="2dc49-105">Fyrstu 4 skráningar settu upp gögn sem þarf til að ljúka þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="2dc49-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="2dc49-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="2dc49-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2dc49-107">Þetta verk er yfirleitt í höndum hönnuðar afurðar.</span><span class="sxs-lookup"><span data-stu-id="2dc49-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="2dc49-108">Velja afurð</span><span class="sxs-lookup"><span data-stu-id="2dc49-108">Select the product</span></span>
1. <span data-ttu-id="2dc49-109">Smellið á Viðhald útgefinnar afurðar.</span><span class="sxs-lookup"><span data-stu-id="2dc49-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="2dc49-110">Smella á Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="2dc49-110">Click Released products.</span></span>
3. <span data-ttu-id="2dc49-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2dc49-112">Finna útgefin afurðarsniðmát með tækni fyrir víddaskilgreiningu sem var stofnaður í fyrsta leiðarvísi í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="2dc49-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="2dc49-113">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="2dc49-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="2dc49-114">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="2dc49-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="2dc49-115">Stofna nýja uppskrift og uppskriftarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="2dc49-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-116">Click New.</span></span>
2. <span data-ttu-id="2dc49-117">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="2dc49-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="2dc49-118">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2dc49-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2dc49-119">Stillingar svæðis</span><span class="sxs-lookup"><span data-stu-id="2dc49-119">Setting a site</span></span>  
    * <span data-ttu-id="2dc49-120">Í þessu ferli stillum við ekki inn tiltekið svæði fyrir Uppskriftina.</span><span class="sxs-lookup"><span data-stu-id="2dc49-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="2dc49-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-121">Click OK.</span></span>
5. <span data-ttu-id="2dc49-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-122">Click New.</span></span>
    * <span data-ttu-id="2dc49-123">Í þessu ferli er bætt við fjórar línur við Uppskrift.</span><span class="sxs-lookup"><span data-stu-id="2dc49-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="2dc49-124">Tvær línur sýna valkosti fyrir kapal og tvær línur sýna valkosti fyrir geymslu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="2dc49-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="2dc49-126">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="2dc49-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-127">Velja vörunúmer A0001, HDMI 6' Cables.</span><span class="sxs-lookup"><span data-stu-id="2dc49-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="2dc49-128">Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.</span><span class="sxs-lookup"><span data-stu-id="2dc49-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-129">Veljið afbrigðisflokk Kapla sem stofnuð var í handbók 4 í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="2dc49-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="2dc49-130">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-130">Click New.</span></span>
    * <span data-ttu-id="2dc49-131">Velja vörunúmer A0002, HDMI 12' Cables.</span><span class="sxs-lookup"><span data-stu-id="2dc49-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="2dc49-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="2dc49-133">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="2dc49-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="2dc49-134">Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.</span><span class="sxs-lookup"><span data-stu-id="2dc49-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-135">Velja aftur Afbirgðaflokkur kapla.</span><span class="sxs-lookup"><span data-stu-id="2dc49-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="2dc49-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-136">Click New.</span></span>
14. <span data-ttu-id="2dc49-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="2dc49-138">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="2dc49-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-139">Velja vörunúmer D0002 Cabinet.</span><span class="sxs-lookup"><span data-stu-id="2dc49-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="2dc49-140">Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.</span><span class="sxs-lookup"><span data-stu-id="2dc49-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-141">Veljið afbrigðaflokki Cabinet fyrir þessa uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="2dc49-142">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-142">Click New.</span></span>
18. <span data-ttu-id="2dc49-143">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="2dc49-144">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="2dc49-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-145">Veljið vörunúmer M0007 StandardCabinet sem síðustu uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="2dc49-146">Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.</span><span class="sxs-lookup"><span data-stu-id="2dc49-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2dc49-147">Veljið afbrigðaflokki Cabinet fyrir síðustu uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="2dc49-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="2dc49-148">Samþykkja og virkja</span><span class="sxs-lookup"><span data-stu-id="2dc49-148">Approve and activate</span></span>
1. <span data-ttu-id="2dc49-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2dc49-149">Close the page.</span></span>
2. <span data-ttu-id="2dc49-150">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="2dc49-150">Click Approve.</span></span>
3. <span data-ttu-id="2dc49-151">Sláið inn eða veldu gildi í reitnum samþykki eftir.</span><span class="sxs-lookup"><span data-stu-id="2dc49-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="2dc49-152">Veldu já í viltu einnig að samþykkja uppskriftina? reitur.</span><span class="sxs-lookup"><span data-stu-id="2dc49-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="2dc49-153">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2dc49-153">Click OK.</span></span>
6. <span data-ttu-id="2dc49-154">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="2dc49-154">Click Activate.</span></span>


