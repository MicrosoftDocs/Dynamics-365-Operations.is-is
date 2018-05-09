--- 
title: "Senda sölupantanir án vöruhúsa"
description: "Þessi handbók sýnir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 16feadb3a2e30e3400d85829c73f6f20780e7b71
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="0c9c7-103">Senda sölupantanir án vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="0c9c7-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c9c7-104">Þessi handbók sýnir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="0c9c7-105">Leiðbeiningarnar eiga við um flæði uppfyllingar sem er ekki sett upp fyrir vöruhúsakerfi (hvorki grunnur eða ítarlegt vöruhús), og krefst þar af leiðandi ekki að afurð tiltektarlista sé skráð fyrir sendingu.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="0c9c7-106">Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="0c9c7-107">Í báðum tilvikum, áður en þú ræsir þetta verk, skal stofna sölupöntun fyrir afurð á lager sem hefur magn sem er meira en 1.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="0c9c7-108">Til að forðast bókunarvillu þarf að athuga að afurðamagn á lager á því svæði og vöruhúsi sem var valið í pöntuninni nái yfir pöntunarmagnið.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="0c9c7-109">Bóka fylgiseðil fyrir pöntun</span><span class="sxs-lookup"><span data-stu-id="0c9c7-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="0c9c7-110">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="0c9c7-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="0c9c7-111">Í listanum skal finna og velja pöntun sem var stofnuð fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="0c9c7-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0c9c7-113">Í aðgerðasvæðinu er smellt á Taka til og pakka.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="0c9c7-114">Smellt er á Bóka fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="0c9c7-115">Útvíkka eða draga saman hlutann Færibreytur.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="0c9c7-116">Veljið „Allt“ á svæðinu „Magn“.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="0c9c7-117">Aðrir valkostir eru Afhenda núna og Tekið til.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="0c9c7-118">Ef senda á pöntunarlínuna að hluta til og reiturinn Afhenda nú í pöntunarlínunni inniheldur magn, myndirðu velja Afhenda nú.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="0c9c7-119">Ef flæði uppfyllingar fyrirtækis þíns felur í sér tiltektarlista sem aðskilda ferli sem er stjórnað af og skráð með tiltektarlista, myndirðu velja Tiltekið.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="0c9c7-120">Athuga að valkosturinn Bókun sé stilltur á Já.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="0c9c7-121">Stilla valkostinn Prenta fylgiseðla á Já.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="0c9c7-122">Yfirlitsflipinn inniheldur lista yfir fylgiseðla til að mynda í þessari bókun.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="0c9c7-123">Ef þú ert að senda einstaka pöntun verður yfirleitt einn fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="0c9c7-124">Hins vegar ef pöntunarlínur eru til sendingar frá mismunandi svæðum verður bókun sjálfkrafa skipt í viðeigandi fjölda skjala.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="0c9c7-125">Þetta er áskilið skilyrði sem ekki er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="0c9c7-126">Á svipaðan hátt verður bókun einnig skipt upp í mörg skjöl ef senda á línur pöntunar á mismunandi afhendingaraðsetur og sendingarreglan er sett upp til að krefjast skiptingar.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="0c9c7-127">Á flipanum Lína velurðu röð fyrir pöntunarlínuna sem á að senda.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="0c9c7-128">Í reitnum Uppfæra skal slá inn tölu sem er lægri en upphaflegt magn.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="0c9c7-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-129">Click OK.</span></span>
12. <span data-ttu-id="0c9c7-130">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-130">Click Yes.</span></span>
13. <span data-ttu-id="0c9c7-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-131">Close the page.</span></span>
14. <span data-ttu-id="0c9c7-132">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="0c9c7-133">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-133">Click Change view.</span></span>
16. <span data-ttu-id="0c9c7-134">Smellið á skoða Haus.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-134">Click Header view.</span></span>
    * <span data-ttu-id="0c9c7-135">Ef allar línur í pöntun hafa verið afgreiddar að fullu breytist staða pöntunar úr Opið í Afhent.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="0c9c7-136">Í þessu dæmi hefur pöntunarlínan verið send að hluta.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="0c9c7-137">Þess vegna helst pöntunarstaðan opin.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-137">This is why the order status remains Open.</span></span>     
    * <span data-ttu-id="0c9c7-138">Reiturinn Staða skjals er stilltur á fylgiseðil þar sem að minnsta kosti ein af pöntunarlínunum hefur verið send.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="0c9c7-139">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="0c9c7-140">Smellt er á Línumagn.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-140">Click Line quantity.</span></span>
19. <span data-ttu-id="0c9c7-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-141">Close the page.</span></span>
20. <span data-ttu-id="0c9c7-142">Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="0c9c7-143">Smella skal á fylgiseðilinn.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-143">Click Packing slip.</span></span>
    * <span data-ttu-id="0c9c7-144">Síðan Færslubók fylgiseðla inniheldur öll skjöl fylgiseðla sem voru mynduð fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="0c9c7-145">Hægt er að fara yfir nákvæmar upplýsingar um hvert skjal og prenta þær, ef þörf er á.</span><span class="sxs-lookup"><span data-stu-id="0c9c7-145">You can review details of each document and print them, if needed.</span></span>  


