--- 
title: "Skrá og bóka fyrirframdagsetta ávísun fyrir viðskiptavin"
description: "Hægt er að skrá upplýsingar um fyrirframdagsetta ávísun sem er móttekin frá viðskiptavini."
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 131e4f364c62d03b95fb4b77f472828b9483d5e1
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="ac715-103">Skrá og bóka fyrirframdagsetta ávísun fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="ac715-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac715-104">Hægt er að skrá upplýsingar um fyrirframdagsetta ávísun sem er móttekin frá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="ac715-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="ac715-105">Einnig er hægt að bóka fyrirframdagsettu ávísunina og mynda fjárhagslegar færslur.</span><span class="sxs-lookup"><span data-stu-id="ac715-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="ac715-106">Ljúkið eftirtöldum verkefnum áður en hægt er að skrá og bóka fyrirframdagsettar ávísanir sem bárust frá viðskiptavini: • Setja upp fyrirframdagsettar ávísanir á síðunni Reiðufjár- og bankastjórnun • Setja upp greiðsluhátt fyrir fyrirframdagsettar ávísanir Hlutverk þessa ferlis er fjárreiðustjóri.</span><span class="sxs-lookup"><span data-stu-id="ac715-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="ac715-107">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ac715-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="ac715-108">Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="ac715-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ac715-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ac715-109">Click New.</span></span>
3. <span data-ttu-id="ac715-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ac715-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ac715-111">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="ac715-111">Click Lines.</span></span>
5. <span data-ttu-id="ac715-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ac715-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ac715-113">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ac715-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="ac715-114">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="ac715-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="ac715-115">Færðu inn upphæðina sem er tilgreind á fyrirframdagsettu ávísuninni.</span><span class="sxs-lookup"><span data-stu-id="ac715-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="ac715-116">Smellið á flipann Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="ac715-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="ac715-117">Færa inn gildi í svæðinu greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="ac715-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="ac715-118">Veldu greiðsluaðferð fyrir fyrirframdagsettu ávísunina.</span><span class="sxs-lookup"><span data-stu-id="ac715-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="ac715-119">Smellið á flipann Fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="ac715-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="ac715-120">Dagsetning er rituð í reitinn Gjalddagi.</span><span class="sxs-lookup"><span data-stu-id="ac715-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="ac715-121">Færið inn dagsetningu sem greiða skal fyrirframdagsetta ávísun fyrir.</span><span class="sxs-lookup"><span data-stu-id="ac715-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="ac715-122">Í reitinn Útibú útgáfubanka skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ac715-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="ac715-123">Færið inn bankaupplýsingar fyrirframdagsettrar ávísunar.</span><span class="sxs-lookup"><span data-stu-id="ac715-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="ac715-124">Í reitinn ávísunarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ac715-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="ac715-125">Í reitinn Heiti útgáfubanka skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ac715-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="ac715-126">Færið inn bankaupplýsingar fyrirframdagsettrar ávísunar.</span><span class="sxs-lookup"><span data-stu-id="ac715-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="ac715-127">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="ac715-127">Click Post.</span></span>
16. <span data-ttu-id="ac715-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ac715-128">Close the page.</span></span>


