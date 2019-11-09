---
title: Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn
description: Þú getur skráð upplýsingar fyrirframdagsett ávísun áður en þú gefur út ávísun til lánardrottinn með því að nota færslubókarfylgiskjal.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe29e106055177dbd12c39ee3fc9de609059f73b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178299"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="e90f8-103">Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="e90f8-103">Register and post a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e90f8-104">Þú getur skráð upplýsingar fyrirframdagsett ávísun áður en þú gefur út ávísun til lánardrottinn með því að nota færslubókarfylgiskjal.</span><span class="sxs-lookup"><span data-stu-id="e90f8-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="e90f8-105">Einnig er hægt að bóka fyrirframdagsettu ávísunina og mynda fjárhagslegar færslur.</span><span class="sxs-lookup"><span data-stu-id="e90f8-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="e90f8-106">Áður en fyrirframdagsett ávísun frá lánardrottni er skráð og bókuð skal ljúka eftirfarandi verkefni:</span><span class="sxs-lookup"><span data-stu-id="e90f8-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="e90f8-107">Setja upp fyrirframdagsettar ávísanir í Reiðufjár- og bankastjórnun síðunni.</span><span class="sxs-lookup"><span data-stu-id="e90f8-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="e90f8-108">Hlutverk þetta leiðbeiningar fyrir verk er Gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="e90f8-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="e90f8-109">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="e90f8-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e90f8-110">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók</span><span class="sxs-lookup"><span data-stu-id="e90f8-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="e90f8-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e90f8-111">Click New.</span></span>
3. <span data-ttu-id="e90f8-112">Í svæðið Heiti skal slá inn ‚VendPay'.</span><span class="sxs-lookup"><span data-stu-id="e90f8-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="e90f8-113">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="e90f8-113">Click Lines.</span></span>
5. <span data-ttu-id="e90f8-114">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e90f8-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="e90f8-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e90f8-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e90f8-116">Í reitnum Debet skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="e90f8-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="e90f8-117">Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e90f8-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e90f8-118">Veldu greiðsluaðferð fyrir fyrirframdagsettu ávísunina</span><span class="sxs-lookup"><span data-stu-id="e90f8-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="e90f8-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e90f8-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e90f8-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e90f8-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e90f8-121">Smellið á flipann Fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="e90f8-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="e90f8-122">Í reitinn Ávísunarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e90f8-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="e90f8-123">Færðu inn eða breyttu númera fyrirframdagsett ávísun.</span><span class="sxs-lookup"><span data-stu-id="e90f8-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="e90f8-124">Í reitinn Heiti útgáfubanka skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e90f8-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="e90f8-125">færið inn upplýsingar um banka fyrir banka sem gefur út.</span><span class="sxs-lookup"><span data-stu-id="e90f8-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="e90f8-126">Smellt er á listinn flipann.</span><span class="sxs-lookup"><span data-stu-id="e90f8-126">Click the List tab.</span></span>
15. <span data-ttu-id="e90f8-127">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="e90f8-127">Click Post.</span></span>
16. <span data-ttu-id="e90f8-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e90f8-128">Close the page.</span></span>
17. <span data-ttu-id="e90f8-129">Smellið á flipann Fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="e90f8-129">Click the Postdated checks tab.</span></span>
