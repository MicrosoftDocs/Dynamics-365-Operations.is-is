---
title: Senda sölupantanir án vöruhúsa
description: Þetta efni útskýrir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6b1dbb4d53785c226f7c9d40339d9dd19f47152
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984155"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="1e8db-103">Senda sölupantanir án vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="1e8db-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e8db-104">Þetta efni útskýrir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="1e8db-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="1e8db-105">Leiðbeiningarnar eiga við um flæði uppfyllingar sem er ekki sett upp fyrir vöruhúsakerfi (hvorki grunnur eða ítarlegt vöruhús), og krefst þar af leiðandi ekki að afurð tiltektarlista sé skráð fyrir sendingu.</span><span class="sxs-lookup"><span data-stu-id="1e8db-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="1e8db-106">Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="1e8db-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="1e8db-107">Í báðum tilvikum, áður en þú ræsir þetta verk, skal stofna sölupöntun fyrir afurð á lager sem hefur magn sem er meira en 1.</span><span class="sxs-lookup"><span data-stu-id="1e8db-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="1e8db-108">Til að forðast bókunarvillu þarf að athuga að afurðamagn á lager á því svæði og vöruhúsi sem var valið í pöntuninni nái yfir pöntunarmagnið.</span><span class="sxs-lookup"><span data-stu-id="1e8db-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="1e8db-109">Bóka fylgiseðil fyrir pöntun</span><span class="sxs-lookup"><span data-stu-id="1e8db-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="1e8db-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="1e8db-111">Í listanum skal finna og velja pöntun sem var stofnuð fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="1e8db-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="1e8db-112">Á aðgerðasvæðinu velurðu **Taka til og pakka**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="1e8db-113">Veldu **Bóka fylgiseðil**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="1e8db-114">Útvíkka eða draga saman hlutann **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="1e8db-115">Í reitnum **Magn** velurðu **Allt**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="1e8db-116">Aðrir valkostir eru **Afhenda núna** og **Tekið til**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="1e8db-117">Ef senda á pöntunarlínuna að hluta til og reiturinn **Afhenda núna** í pöntunarlínunni inniheldur magn, myndirðu velja **Afhenda núna**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="1e8db-118">Ef flæði uppfyllingar fyrirtækis þíns felur í sér tiltektarlista sem aðskilda ferli sem er stjórnað af og skráð með tiltektarlista, myndirðu velja **Tiltekið**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="1e8db-119">Athuga að valkosturinn **Bókun** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="1e8db-120">Stilla valkostinn **Prenta fylgiseðla** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="1e8db-121">Flipinn **Yfirlit** inniheldur lista yfir fylgiseðla til að mynda í þessari bókun.</span><span class="sxs-lookup"><span data-stu-id="1e8db-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="1e8db-122">Ef þú ert að senda einstaka pöntun verður yfirleitt einn fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="1e8db-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="1e8db-123">Hins vegar ef pöntunarlínur eru til sendingar frá mismunandi svæðum verður bókun sjálfkrafa skipt í viðeigandi fjölda skjala.</span><span class="sxs-lookup"><span data-stu-id="1e8db-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="1e8db-124">Þetta er áskilið skilyrði sem ekki er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="1e8db-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="1e8db-125">Á svipaðan hátt verður bókun einnig skipt upp í mörg skjöl ef senda á línur pöntunar á mismunandi afhendingaraðsetur og sendingarreglan er sett upp til að krefjast skiptingar.</span><span class="sxs-lookup"><span data-stu-id="1e8db-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="1e8db-126">Á flipanum **Línur** velurðu röð fyrir pöntunarlínuna sem á að senda.</span><span class="sxs-lookup"><span data-stu-id="1e8db-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="1e8db-127">Í reitnum **Uppfæra** skal slá inn tölu sem er lægri en upphaflegt magn.</span><span class="sxs-lookup"><span data-stu-id="1e8db-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="1e8db-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-128">Select **OK**.</span></span>
11. <span data-ttu-id="1e8db-129">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-129">Select **Yes**.</span></span>
12. <span data-ttu-id="1e8db-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1e8db-130">Close the page.</span></span>
13. <span data-ttu-id="1e8db-131">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="1e8db-132">Veldu **Breyta skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-132">Select **Change view**.</span></span>
15. <span data-ttu-id="1e8db-133">Veldu **Hausyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-133">Select **Header view**.</span></span>
    - <span data-ttu-id="1e8db-134">Ef allar línur í pöntun hafa verið afgreiddar að fullu breytist staða pöntunar úr Opið í Afhent.</span><span class="sxs-lookup"><span data-stu-id="1e8db-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="1e8db-135">Í þessu dæmi hefur pöntunarlínan verið send að hluta.</span><span class="sxs-lookup"><span data-stu-id="1e8db-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="1e8db-136">Þess vegna helst pöntunarstaðan opin.</span><span class="sxs-lookup"><span data-stu-id="1e8db-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="1e8db-137">Reiturinn **Staða skjals** er stilltur á fylgiseðil þar sem að minnsta kosti ein af pöntunarlínunum hefur verið send.</span><span class="sxs-lookup"><span data-stu-id="1e8db-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="1e8db-138">Í aðgerðasvæðinu velurðu **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="1e8db-139">Velja **Línumagn**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="1e8db-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1e8db-140">Close the page.</span></span>
19. <span data-ttu-id="1e8db-141">Á aðgerðasvæðinu velurðu **Taka til og pakka**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="1e8db-142">Velja **Fylgiseðil**.</span><span class="sxs-lookup"><span data-stu-id="1e8db-142">Select **Packing slip**.</span></span> <span data-ttu-id="1e8db-143">Síðan **Færslubók fylgiseðla** inniheldur öll skjöl fylgiseðla sem voru mynduð fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="1e8db-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="1e8db-144">Hægt er að fara yfir nákvæmar upplýsingar um hvert skjal og prenta þær, ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="1e8db-144">You can review details of each document and print them, if you wish.</span></span>  

