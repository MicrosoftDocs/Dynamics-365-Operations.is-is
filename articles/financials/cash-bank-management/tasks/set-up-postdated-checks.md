--- 
title: "Setja upp fyrirframdagsettar ávísanir"
description: "Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 47686504b8fd35898951e2d1e8db5e37110bbe65
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="ed881-103">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="ed881-103">Set up postdated checks</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed881-104">Í þessu efnisatriði er útskýrt hvernig á að tilgreina hvort eigi að bóka bókarfærslur fyrir fyrirframdagsettar ávísanir og hvaða bókunarbækur sem nota á fyrir færslur og lánardrottnagreiðslur.</span><span class="sxs-lookup"><span data-stu-id="ed881-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="ed881-105">Einnig er hægt að tilgreina millireikninga fyrir útgefnar ávísanir, mótteknar ávísanir og staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="ed881-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="ed881-106">Fyrirframdagsettar ávísanir sem eru gefnar út til að gera og móttaka greiðslur í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="ed881-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="ed881-107">Hægt er að tilgreina hvort ávísunin verði að koma fram í bókhaldsbókum fyrir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="ed881-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="ed881-108">Hlutverk þessa ferlis er fjárreiðustjóri.</span><span class="sxs-lookup"><span data-stu-id="ed881-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="ed881-109">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ed881-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="ed881-110">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="ed881-110">Set up postdated checks</span></span>
1. <span data-ttu-id="ed881-111">Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="ed881-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="ed881-112">Smellið á flipann Fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="ed881-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="ed881-113">Veldu eða hreinsaðu gátreitinn Virkja fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="ed881-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="ed881-114">Velja eða hreinsa gátreitinn Bóka bókarfærslur fyrir fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="ed881-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="ed881-115">Í reitnum Millireikningur fyrir útgefnar ávísanir skal tilgreina þau gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ed881-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="ed881-116">Tilgreinið gildin sem óskað er eftir í reitinn Millireikningur fyrir mótteknar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="ed881-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="ed881-117">Í reitinn Almenn færslubók fyrir jöfnun færslna skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ed881-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="ed881-118">Í reitinn Millifæra fyrirframdagsettar ávísanir á þessa færslubók lánardrottins skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ed881-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="ed881-119">Í reitnum Millireikningur staðgreiðsluskatts skal tilgreina þau gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ed881-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="ed881-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ed881-120">Click Save.</span></span>
11. <span data-ttu-id="ed881-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ed881-121">Close the page.</span></span>
12. <span data-ttu-id="ed881-122">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="ed881-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="ed881-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ed881-123">Click New.</span></span>
14. <span data-ttu-id="ed881-124">Færa inn gildi í svæðinu greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="ed881-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="ed881-125">Velja skal bókunarkostinn Millireikning fyrirframdagsettrar ávísunar til að tilgreina að upphæð ávísunarinnar er bókuð á millireikning.</span><span class="sxs-lookup"><span data-stu-id="ed881-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="ed881-126">Veljið 'Banki' í svæðinu gerð lykils.</span><span class="sxs-lookup"><span data-stu-id="ed881-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="ed881-127">Mótlykill greiðslumáta verður banki.</span><span class="sxs-lookup"><span data-stu-id="ed881-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="ed881-128">Í reitnum Greiðslulykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ed881-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="ed881-129">Veldu reikninginn sem er notaður til að draga reikningsupphæðina frá.</span><span class="sxs-lookup"><span data-stu-id="ed881-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="ed881-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ed881-130">Close the page.</span></span>
19. <span data-ttu-id="ed881-131">Farið í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="ed881-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="ed881-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ed881-132">Click New.</span></span>
21. <span data-ttu-id="ed881-133">Færa inn gildi í svæðinu greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="ed881-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="ed881-134">Velja skal bókunarkostinn Millireikning fyrirframdagsettrar ávísunar til að tilgreina að upphæð ávísunarinnar er bókuð á millireikning.</span><span class="sxs-lookup"><span data-stu-id="ed881-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="ed881-135">Veljið 'Banki' í svæðinu gerð lykils.</span><span class="sxs-lookup"><span data-stu-id="ed881-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="ed881-136">Mótlykill greiðslumáta verður banki.</span><span class="sxs-lookup"><span data-stu-id="ed881-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="ed881-137">Í reitnum Greiðslulykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ed881-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="ed881-138">Veldu reikninginn sem er notaður til að draga reikningsupphæðina frá.</span><span class="sxs-lookup"><span data-stu-id="ed881-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="ed881-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ed881-139">Close the page.</span></span>


