--- 
title: "Setja upp og mynda aldursgreiningarupplýsingar fyrir viðskiptakröfur"
description: "Þessari handbók hjálpar til við að setja upp skilgreiningu aldursgreiningar, greina aldur stöðu viðskiptavinar og skoða stöðu í á listanum aldursgreindar stöður og síðan Innheimtu."
author: mikefalkner
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
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2e9f393acaa47d485a583b99ace459474f30be6a
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="d3533-103">Setja upp og mynda aldursgreiningarupplýsingar fyrir viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="d3533-103">Set up and generate accounts receivable aging information</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3533-104">Þessari handbók hjálpar til við að setja upp skilgreiningu aldursgreiningar, greina aldur stöðu viðskiptavinar og skoða stöðu í á listanum aldursgreindar stöður og síðan Innheimtu.</span><span class="sxs-lookup"><span data-stu-id="d3533-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="d3533-105">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="d3533-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="d3533-106">Stofna skilgreiningu aldurstímabils</span><span class="sxs-lookup"><span data-stu-id="d3533-106">Create an aging period definition</span></span>
1. <span data-ttu-id="d3533-107">Fara í Skuldir og innheimta > Uppsetning > Skilgreiningar aldurstímabila.</span><span class="sxs-lookup"><span data-stu-id="d3533-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="d3533-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3533-108">Click New.</span></span>
3. <span data-ttu-id="d3533-109">Í reitnum Skilgreining aldurstímabils skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d3533-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="d3533-110">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d3533-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d3533-111">Stutt er á  bæta við til að setja inn nýja aldurstímabil.</span><span class="sxs-lookup"><span data-stu-id="d3533-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="d3533-112">Í svæðinu Tímabil skal færa inn lýsingu til að sýna á skýrslur aldurstímabils.</span><span class="sxs-lookup"><span data-stu-id="d3533-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="d3533-113">Í reitnum Eining skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="d3533-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="d3533-114">Í reitnum Millibil skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="d3533-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="d3533-115">Fjárhagstímabil samsvarar tímabili í dagatali fjárhags.</span><span class="sxs-lookup"><span data-stu-id="d3533-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="d3533-116">Dagur, vika, mánuður, ársfjórðungur og ár skilgreina stærð tímabila eftir gerð.</span><span class="sxs-lookup"><span data-stu-id="d3533-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="d3533-117">Ótakmarkað velur allar færslur fyrir eða eftir fyrra tímabil, allt eftir hvort það er fyrsta eða síðasta tímabil.</span><span class="sxs-lookup"><span data-stu-id="d3533-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="d3533-118">Í reitnum Öldrunarvísir skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="d3533-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="d3533-119">Veljið tímabil efst í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="d3533-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="d3533-120">Uppfæra lýsingu til að lýsa elsta tímabil í skilgreiningu aldurstímabils</span><span class="sxs-lookup"><span data-stu-id="d3533-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="d3533-121">Í svæðinu Tímabil skal færa inn nýja lýsing aldurstímabilið.</span><span class="sxs-lookup"><span data-stu-id="d3533-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="d3533-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d3533-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="d3533-123">Aldursgreina stöður</span><span class="sxs-lookup"><span data-stu-id="d3533-123">Age the balances</span></span>
1. <span data-ttu-id="d3533-124">Fara í Skuldir og innheimta > Reglubundin verk > Aldursgreina stöður viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d3533-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="d3533-125">Velja skilgreiningu aldurstímabils sem var stofnaður í svæðinu skilgreiningu Aldurstímabils.</span><span class="sxs-lookup"><span data-stu-id="d3533-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="d3533-126">Hægt er að hafa eina virka skyndimynd fyrir hverja skilgreiningu aldurstímabils.</span><span class="sxs-lookup"><span data-stu-id="d3533-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="d3533-127">Allir viðskiptavinir eru keyrðir í gegnum vinnslu að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="d3533-127">All customers are processed by default.</span></span> <span data-ttu-id="d3533-128">Hægt er að nota þetta val til að reikna út einstakt safn viðskiptavinahópa.</span><span class="sxs-lookup"><span data-stu-id="d3533-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="d3533-129">Veljið dagsetningu úr færslunnar sem verður notað fyrir aldursgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d3533-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="d3533-130">Velja skal "frá og með" dagsetningu fyrir aldursgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d3533-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="d3533-131">Sjálfgefið gildi er í dag en ef þetta svæði er breytt í Valin dagsetning, er hægt að velja dagsetningu sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="d3533-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="d3533-132">Fyrir runuvinnslu, notið Dagsins í dag.</span><span class="sxs-lookup"><span data-stu-id="d3533-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="d3533-133">Útvíkka svið Fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="d3533-133">Expand the Company range.</span></span> <span data-ttu-id="d3533-134">Hægt er að velja fyrirtæki sem verða teknar með í skyndimyndar.</span><span class="sxs-lookup"><span data-stu-id="d3533-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="d3533-135">Núgildandi fyrirtæki er sjálfvirkt valið.</span><span class="sxs-lookup"><span data-stu-id="d3533-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="d3533-136">Smellt er á í Lagi til að vinna skyndimyndar.</span><span class="sxs-lookup"><span data-stu-id="d3533-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="d3533-137">Það tekur smá tíma fyrir sleði að hverfa og athuga í skilaboðamiðstöð eftir skilaboðum.</span><span class="sxs-lookup"><span data-stu-id="d3533-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="d3533-138">Skoða stöðu á listanum Aldursgreindar stöður og síðunni Innheimta</span><span class="sxs-lookup"><span data-stu-id="d3533-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="d3533-139">Fara í skuldir og innheimta > Innheimta > Aldursgreindar stöður.</span><span class="sxs-lookup"><span data-stu-id="d3533-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="d3533-140">listasíðu sýnir stöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d3533-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="d3533-141">Aldursgreiningartáknið sýnir aldurstímabilið fyrir elsta færslunnar.</span><span class="sxs-lookup"><span data-stu-id="d3533-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="d3533-142">Velja skal viðskiptavin með stöðu.</span><span class="sxs-lookup"><span data-stu-id="d3533-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="d3533-143">Útvíkka skal svæði Aldursgreiningar í  upplýsingakassa til að skoða aldursgreindar stöður.</span><span class="sxs-lookup"><span data-stu-id="d3533-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="d3533-144">Skilgreining aldurstímabils fyrir upplýsingakassann er tekið úr sjálfgefnu skilgreining aldurstímabils sem tilgreint er í færibreytum.</span><span class="sxs-lookup"><span data-stu-id="d3533-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="d3533-145">Hægt er að breyta henni með því að nota valmyndina Innheimta.</span><span class="sxs-lookup"><span data-stu-id="d3533-145">You can change it using the Collect menu.</span></span>  


