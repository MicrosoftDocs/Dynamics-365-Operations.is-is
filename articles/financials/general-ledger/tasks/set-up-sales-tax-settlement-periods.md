--- 
title: "Setja upp virðisaukaskatttímabil"
description: "Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d30a3271114574d2776921fb31b360389a1b3466
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="23314-103">Setja upp virðisaukaskatttímabil</span><span class="sxs-lookup"><span data-stu-id="23314-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23314-104">Virðisaukaskattsuppgjörstímabil innihalda upplýsingar um tímabil fyrir hvaða virðisaukaskatt þarf að vera tilkynntur og greiddur.</span><span class="sxs-lookup"><span data-stu-id="23314-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="23314-105">Hægt er að keyra jöfnunarferli fyrir jöfnunartímabil fyrir tiltekin dagsetningarbil.</span><span class="sxs-lookup"><span data-stu-id="23314-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="23314-106">Allar skattkóði sem tengist jöfnunartímabil verða jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="23314-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="23314-107">Eftir að setja upp tengd virðisaukaskattsyfirvald er skattskuld bókuð í annað hvort lánardrottinn eða fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="23314-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="23314-108">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="23314-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="23314-109">Fara á Skattur > Óbeinir skattar > Virðisaukaskattur > VSK-uppgjörstímabil.</span><span class="sxs-lookup"><span data-stu-id="23314-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="23314-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23314-110">Click New.</span></span>
3. <span data-ttu-id="23314-111">Færa inn gildi í reitnum jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="23314-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="23314-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="23314-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23314-113">Í yfirvalds svæði, velurðu virðisaukaskattsyfirvald sem tekur við skýrslan og greiðsla sem eru stofnaðar fyrir jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="23314-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="23314-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="23314-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="23314-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="23314-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="23314-116">Í reitnum greiðsluskilmálar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="23314-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="23314-117">Tengdar virðisaukaskattsyfirvald má setja upp sem lánardrottinn og virðisaukauppgjör mun stofna opnum lánardrottnareikningi.</span><span class="sxs-lookup"><span data-stu-id="23314-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="23314-118">Greiðsluskilmálar skilgreina Gjalddaga fyrir the opinn reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="23314-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="23314-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="23314-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="23314-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="23314-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="23314-121">Velja gerð fyrir tímabilum jöfnunartímabils.</span><span class="sxs-lookup"><span data-stu-id="23314-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="23314-122">Færið inn fjölda eininga fyrir tímabilið á hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="23314-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="23314-123">Til dæmis ársfjórðungur hefur 3 mánuði.</span><span class="sxs-lookup"><span data-stu-id="23314-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="23314-124">Velja eða hreinsa Nota runuvinnslu fyrir gátreit fyrir virðisaukauppgjör.</span><span class="sxs-lookup"><span data-stu-id="23314-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="23314-125">Hægt er að vinna úr jöfnunarferlið fyrir tímabil sem runuvinnslu í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="23314-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="23314-126">Þetta er ráðlagt fyrir mikinn fjölda skattafærslur innan tímabil.</span><span class="sxs-lookup"><span data-stu-id="23314-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="23314-127">Útvíkka flipanum tímabilum.</span><span class="sxs-lookup"><span data-stu-id="23314-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="23314-128">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="23314-128">Click Add.</span></span>
16. <span data-ttu-id="23314-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="23314-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="23314-130">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="23314-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="23314-131">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="23314-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="23314-132">Smellt er á Nýtt tímabil.</span><span class="sxs-lookup"><span data-stu-id="23314-132">Click New period interval.</span></span>
    * <span data-ttu-id="23314-133">Þegar hefur verið fært inn fyrsta tímabilið, hægt að stofna ný tímabil sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="23314-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="23314-134">Hægt er að koma aftur og bæta við nýrri tímabilum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23314-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="23314-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23314-135">Close the page.</span></span>


