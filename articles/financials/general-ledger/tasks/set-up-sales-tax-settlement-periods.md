--- 
title: "Setja upp virðisaukaskatttímabil"
description: "Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur."
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 81214cc52b1488bb70ac5fd6ccc817f6f979163d
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="84efe-103">Setja upp virðisaukaskatttímabil</span><span class="sxs-lookup"><span data-stu-id="84efe-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84efe-104">Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur.</span><span class="sxs-lookup"><span data-stu-id="84efe-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="84efe-105">Hægt er að keyra jöfnunarferli fyrir jöfnunartímabil fyrir tiltekin dagsetningarbil.</span><span class="sxs-lookup"><span data-stu-id="84efe-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="84efe-106">Allar skattkóði sem tengist jöfnunartímabil verða jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="84efe-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="84efe-107">Eftir að setja upp tengd virðisaukaskattsyfirvald er skattskuld bókuð í annað hvort lánardrottinn eða fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="84efe-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="84efe-108">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="84efe-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="84efe-109">Fara á Skattur > Óbeinir skattar > Virðisaukaskattur > VSK-uppgjörstímabil.</span><span class="sxs-lookup"><span data-stu-id="84efe-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="84efe-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="84efe-110">Click New.</span></span>
3. <span data-ttu-id="84efe-111">Færa inn gildi í reitnum jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="84efe-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="84efe-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="84efe-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84efe-113">Í yfirvalds svæði, velurðu virðisaukaskattsyfirvald sem tekur við skýrslan og greiðsla sem eru stofnaðar fyrir jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="84efe-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="84efe-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="84efe-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="84efe-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="84efe-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="84efe-116">Í reitnum greiðsluskilmálar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="84efe-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="84efe-117">Tengdar virðisaukaskattsyfirvald má setja upp sem lánardrottinn og virðisaukauppgjör mun stofna opnum lánardrottnareikningi.</span><span class="sxs-lookup"><span data-stu-id="84efe-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="84efe-118">Greiðsluskilmálar skilgreina Gjalddaga fyrir the opinn reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="84efe-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="84efe-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="84efe-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="84efe-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="84efe-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="84efe-121">Velja gerð fyrir tímabilum jöfnunartímabils.</span><span class="sxs-lookup"><span data-stu-id="84efe-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="84efe-122">Færið inn fjölda eininga fyrir tímabilið á hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="84efe-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="84efe-123">Til dæmis ársfjórðungur hefur 3 mánuði.</span><span class="sxs-lookup"><span data-stu-id="84efe-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="84efe-124">Velja eða hreinsa Nota runuvinnslu fyrir gátreit fyrir virðisaukauppgjör.</span><span class="sxs-lookup"><span data-stu-id="84efe-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="84efe-125">Hægt er að vinna úr jöfnunarferlið fyrir tímabil sem runuvinnslu í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="84efe-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="84efe-126">Þetta er ráðlagt fyrir mikinn fjölda skattafærslur innan tímabil.</span><span class="sxs-lookup"><span data-stu-id="84efe-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="84efe-127">Veldu eða hreinsaðu gátreitinn „Koma í veg fyrir að mótfærsluskattafærslur myndist“.</span><span class="sxs-lookup"><span data-stu-id="84efe-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="84efe-128">Sjálfgefið framleiðir kerfið upp á mótfærsluskattafærslur við uppgjörsferlið, sem getur valdið frammistöðuvandamálum ef fjöldi skattafærslna er innan tímabils.</span><span class="sxs-lookup"><span data-stu-id="84efe-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="84efe-129">Veljið þennan gátreit til að koma í veg fyrir að mótfærsluskattafærslur myndist.</span><span class="sxs-lookup"><span data-stu-id="84efe-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="84efe-130">Útvíkka flipanum tímabilum.</span><span class="sxs-lookup"><span data-stu-id="84efe-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="84efe-131">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="84efe-131">Click Add.</span></span>
17. <span data-ttu-id="84efe-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="84efe-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="84efe-133">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="84efe-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="84efe-134">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="84efe-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="84efe-135">Smellt er á Nýtt tímabil.</span><span class="sxs-lookup"><span data-stu-id="84efe-135">Click New period interval.</span></span>
    * <span data-ttu-id="84efe-136">Þegar hefur verið fært inn fyrsta tímabilið, hægt að stofna ný tímabil sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="84efe-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="84efe-137">Hægt er að koma aftur og bæta við nýrri tímabilum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="84efe-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="84efe-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="84efe-138">Close the page.</span></span>


