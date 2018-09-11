--- 
title: "Skilgreina greiðsluskilmála lánardrottna"
description: "Setja upp greiðsluskilmála fyrir reikninga lánardrottins."
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6d9eaf271220437869ff90610e9953a6e2f8a474
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="3136f-103">Skilgreina greiðsluskilmála lánardrottna</span><span class="sxs-lookup"><span data-stu-id="3136f-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3136f-104">Setja upp greiðsluskilmála fyrir reikninga lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3136f-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="3136f-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="3136f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3136f-106">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluskilmálar.</span><span class="sxs-lookup"><span data-stu-id="3136f-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="3136f-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3136f-107">Click New.</span></span>
    * <span data-ttu-id="3136f-108">Skilmála greiðslu síða er notuð til að skilgreina hvernig verður að reikna út gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="3136f-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="3136f-109">Það er ekki notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="3136f-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="3136f-110">Færa inn gildi í svæðinu greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="3136f-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="3136f-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="3136f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3136f-112">Í reitinn dagar skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="3136f-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="3136f-113">Númerið sem fært er inn hér verður notað til að bæta við gjalddaga eða við lok tímabils sem skilgreind er í greiðsluaðferðina.</span><span class="sxs-lookup"><span data-stu-id="3136f-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="3136f-114">Til dæmis, ef Nettó er valið, verður númerið bætt við gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="3136f-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="3136f-115">Ef valið er Gildandi mánuður, það bætir númeri bætt við síðasta dags núverandi mánaðar til að reikna út gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="3136f-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="3136f-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3136f-116">Click Save.</span></span>
7. <span data-ttu-id="3136f-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3136f-117">Close the page.</span></span>
8. <span data-ttu-id="3136f-118">Fara í Viðskiptakröfur > Greiðsluuppsetning > Staðgreiðsluafsláttur.</span><span class="sxs-lookup"><span data-stu-id="3136f-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="3136f-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3136f-119">Click New.</span></span>
10. <span data-ttu-id="3136f-120">Færið inn Kenni í svæðinu staðgreiðsluafslátt.</span><span class="sxs-lookup"><span data-stu-id="3136f-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="3136f-121">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="3136f-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="3136f-122">Ef lánardrottinn býður upp á lagskipt afslátt, velja næsta staðgreiðsluafsláttinn eftir að sá gildandi er útrunnið.</span><span class="sxs-lookup"><span data-stu-id="3136f-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="3136f-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3136f-123">Close the page.</span></span>
14. <span data-ttu-id="3136f-124">Í reitinn dagar skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="3136f-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="3136f-125">Magnið sem er fært inn í svæðið Daga verður notuð til að reikna út dagsetningu staðgreiðsluafsláttar, á grundvelli hvaða valkostur var valinn í svæðinu Nettó/Gildandi.</span><span class="sxs-lookup"><span data-stu-id="3136f-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="3136f-126">Ef Nettó var valinn er magn bætt við dagsetningu reiknings til að ákvarða dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="3136f-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="3136f-127">Ef Núverandi mánuður var valinn er magn verður bætt við lok gjaldmiðilsmánaðar til að ákvarða dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="3136f-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="3136f-128">Færið inn hlutfall staðgreiðsluafslátt í svæðinu Afsláttar.</span><span class="sxs-lookup"><span data-stu-id="3136f-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="3136f-129">Færið inn aðallykils sem verður að staðgreiðsluafslátt verður bókaður fyrir reikninga viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="3136f-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="3136f-130">Færið inn aðallykils sem verður að bóka staðgreiðsluafslátt fyrir reikninga lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3136f-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="3136f-131">Ef 'Afsláttar mótlykils' er stillt til að Nota aðallykill fyrir afslátt lánardrottins, þá verður aðallykils notaður.</span><span class="sxs-lookup"><span data-stu-id="3136f-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="3136f-132">Ef valkosturinn er stillt á Lyklana á reikningslínum, verður staðgreiðsluafslátturinn bókaður á eignar/kostnaðarlykla í línum á reikningi.</span><span class="sxs-lookup"><span data-stu-id="3136f-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="3136f-133">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3136f-133">Click Save.</span></span>


