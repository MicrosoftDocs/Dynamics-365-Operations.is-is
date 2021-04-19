---
title: Skrá efnisnotkun með fartæki
description: Þetta efnisatriði lýsir verkflæði sem gerir kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abc8607e5c3c6ab63a3878b92072bde2ebb0216c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814537"
---
# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="1eed6-103">Skrá efnisnotkun með fartæki</span><span class="sxs-lookup"><span data-stu-id="1eed6-103">Register material consumption using a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1eed6-104">Þetta efnisatriði lýsir verkflæði sem gerir kleift að skrá hráefnanotkun í framleiðslu með því að nota lófatæki.</span><span class="sxs-lookup"><span data-stu-id="1eed6-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="1eed6-105">Inngangur</span><span class="sxs-lookup"><span data-stu-id="1eed6-105">Introduction</span></span>
------------

<span data-ttu-id="1eed6-106">Þessi verkflæði er við hæfi ef strangar kröfur eru um rekjanleika efnis.</span><span class="sxs-lookup"><span data-stu-id="1eed6-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="1eed6-107">Í þeim tilvikum verður að skrá nákvæman tíma og magn í hráefnanotkun svo hægt sé að viðhalda rekjanleika þeirra.</span><span class="sxs-lookup"><span data-stu-id="1eed6-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="1eed6-108">Það má bera þetta ferli saman við bakfærslukostnaðaraðferðir, þar sem það líður ákveðinn tími milli skráningar og þegar raunveruleg notkun á sér stað.</span><span class="sxs-lookup"><span data-stu-id="1eed6-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="1eed6-109">Þetta skýrir hvers vegna er ekki hægt að nota áætlun fyrir sjálfvirka notkun fyrir sum hráefni sem hafa kröfu um rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="1eed6-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="1eed6-110">Lítum á einfalt dæmi sem útskýrir hvernig á að setja upp verkflæði til að virkja skráningu hráefnisnotkunar í framleiðslu með handfrjálsu tæki.</span><span class="sxs-lookup"><span data-stu-id="1eed6-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="1eed6-111">[![setja upp verkflæði til að virkja skráningu hráefnisnotkunar með handfrjálsu tæki](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="1eed6-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="1eed6-112">Upplýsingar um dæmi</span><span class="sxs-lookup"><span data-stu-id="1eed6-112">Scenario details</span></span>

<span data-ttu-id="1eed6-113">Stöðugt framleiðsluferli (5) notar runustýrða hráefnið RM-100.</span><span class="sxs-lookup"><span data-stu-id="1eed6-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="1eed6-114">Hráefnið er tiltækt í lagerbirgðum í staðsetningu Laust 001 (1) á númeraplötu PL-1 með tvær runur, B1 og B2, hvor tveggja með 50 kg magn.</span><span class="sxs-lookup"><span data-stu-id="1eed6-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="1eed6-115">Vöruhúsavinna (2) er útgefin og unnin fyrir RM-100 og hráefnið er tekið til úr Laust-001 í staðsetningu framleiðsluinntaks PIL-01 (3), sem er skilgreind sem staðsetning sem er ekki númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="1eed6-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="1eed6-116">Starfsmaður á vél vigtar hráefnið út úr staðsetningu framleiðsluinntaks (3) og skráir þyngd og rununúmer eftir notkun (4).</span><span class="sxs-lookup"><span data-stu-id="1eed6-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="1eed6-117">Úr staðsetningu framleiðsluinntaks er hluta af hráefninu bætt handvirkt við framleiðsluferlið með skilgreindu millibili.</span><span class="sxs-lookup"><span data-stu-id="1eed6-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="1eed6-118">Þegar starfsmaður á vél bætir við hráefni er það vigtað á vigt og rununúmerið er skráð.</span><span class="sxs-lookup"><span data-stu-id="1eed6-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="1eed6-119">Setja upp verkflæðið til að skrá notkun með handfrjálsu tæki</span><span class="sxs-lookup"><span data-stu-id="1eed6-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="1eed6-120">Búðu til fullunna afurð, FG-100, með uppskrift sem inniheldur runustýrða hráefnið RM-100.</span><span class="sxs-lookup"><span data-stu-id="1eed6-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="1eed6-121">Bætið við tveimur runum, B1 og B2, af RM-100 í magninu 100 á staðsetningu: Bulk-001 á númeraplötu: PL-1.</span><span class="sxs-lookup"><span data-stu-id="1eed6-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="1eed6-122">Losunarreglan í uppskriftarlínunni fyrir RM-100 er stillt á **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="1eed6-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="1eed6-123">Setjið staðsetningu framleiðsluinntaks á PIL-01.</span><span class="sxs-lookup"><span data-stu-id="1eed6-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="1eed6-124">Það er hægt að gera með því að velja þessa staðsetningu sem sjálfgefna staðsetningu framleiðsluinntaks í vöruhúsi 51.</span><span class="sxs-lookup"><span data-stu-id="1eed6-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="1eed6-125">Nýtt valmyndaratriði fartækis stofnað:</span><span class="sxs-lookup"><span data-stu-id="1eed6-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="1eed6-126">**Nafn valmyndaratriðis** - Skrá efnisnotkun.</span><span class="sxs-lookup"><span data-stu-id="1eed6-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="1eed6-127">**Heiti** - Skrá hráefnanotkun.</span><span class="sxs-lookup"><span data-stu-id="1eed6-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="1eed6-128">**Máti** - Óbeint.</span><span class="sxs-lookup"><span data-stu-id="1eed6-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="1eed6-129">**Verkþáttarkóði** - Skrá efnisnotkun.</span><span class="sxs-lookup"><span data-stu-id="1eed6-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="1eed6-130">Bæta valmyndaratriði við valmyndina **Framleiðsla** í fartæki.</span><span class="sxs-lookup"><span data-stu-id="1eed6-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="1eed6-131">Framleiðslupöntun fyrir fullunnu afurðina stofnuð:</span><span class="sxs-lookup"><span data-stu-id="1eed6-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="1eed6-132">**Vörunúmer** - FG-100</span><span class="sxs-lookup"><span data-stu-id="1eed6-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="1eed6-133">**Svæði** - 5</span><span class="sxs-lookup"><span data-stu-id="1eed6-133">**Site** - 5</span></span> 
-    <span data-ttu-id="1eed6-134">**Vöruhús** - 51</span><span class="sxs-lookup"><span data-stu-id="1eed6-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="1eed6-135">**Magn** - 150</span><span class="sxs-lookup"><span data-stu-id="1eed6-135">**Quantity** - 150</span></span>

<span data-ttu-id="1eed6-136">Framleiðslupöntun er **Áætluð** og **Útgefin** og vöruhúsavinna er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="1eed6-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="1eed6-137">Ljúktu við verkið með verkflæðinu fyrir tiltekt hráefnis fyrir lófatækið.</span><span class="sxs-lookup"><span data-stu-id="1eed6-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="1eed6-138">Þetta færir hráefnið úr biðstaðsetningu í staðsetningu framleiðsluinntaks PIL-01.</span><span class="sxs-lookup"><span data-stu-id="1eed6-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="1eed6-139">Eftir að vinnu er lokið er efnið með stöðuna **Tekið til á staðsetningu framleiðsluinntaks**.</span><span class="sxs-lookup"><span data-stu-id="1eed6-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="1eed6-140">Staðan eftir að verk er fullunnið getur verið annaðhvort **Tekið til** eða **Frátekið á lager**.</span><span class="sxs-lookup"><span data-stu-id="1eed6-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="1eed6-141">Það er skilgreint með færibreytunni **Gefa út stöðu eftir að sett er í skjámyndina vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="1eed6-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="1eed6-142">Settu framleiðslupöntunina í gang, annaðhvort úr biðlaranum eða úr lófatækinu með valmyndaratriðinu **Byrja framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="1eed6-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="1eed6-143">Eftir að framleiðslupöntun hefur verið ræst er hægt að skrá hráefnisnotkun með verkflæðinu fyrir lófatækið.</span><span class="sxs-lookup"><span data-stu-id="1eed6-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="1eed6-144">Við skulum byrja á því að skrá notkun upp á 25 pund af runu B1.</span><span class="sxs-lookup"><span data-stu-id="1eed6-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="1eed6-145">Veljið valmyndaratriðið **Skrá efni** **Notkun** í valmyndinni fyrir handfrjálsa tækið og sláið inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="1eed6-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="1eed6-146">Númer framleiðslupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="1eed6-146">The production order number.</span></span> 
-    <span data-ttu-id="1eed6-147">Staðsetningin þar sem hráefnið verður notað er í þessu tilviki PIL-01.</span><span class="sxs-lookup"><span data-stu-id="1eed6-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="1eed6-148">Vörunúmer RM-100.</span><span class="sxs-lookup"><span data-stu-id="1eed6-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="1eed6-149">Rununúmer B1.</span><span class="sxs-lookup"><span data-stu-id="1eed6-149">Batch number B1.</span></span> 
-    <span data-ttu-id="1eed6-150">Magn upp á 25.</span><span class="sxs-lookup"><span data-stu-id="1eed6-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="1eed6-151">Veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1eed6-151">Select **OK**.</span></span>

<span data-ttu-id="1eed6-152">Takið eftir að skilaboðin „Færslubókarlína er stofnuð“ birtast á skjánum.</span><span class="sxs-lookup"><span data-stu-id="1eed6-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="1eed6-153">Í framleiðslupöntun er opin færslubók af gerðinni **Tiltektarlisti framleiðslu** fyrir vörunúmer RM-100 og rununúmer B1.</span><span class="sxs-lookup"><span data-stu-id="1eed6-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="1eed6-154">Nú er hægt að velja að halda áfram skráninguna, til dæmis fyrir rununúmerið B2, og í hvert sinn sem þú velur **í lagi** er nýrri færslubókarlínu bætt við opna færslubók.</span><span class="sxs-lookup"><span data-stu-id="1eed6-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="1eed6-155">Þegar skráningunni er lokið skal velja **Lokið** til að bóka færslubókina og ljúka verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="1eed6-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="1eed6-156">Frekari athugasemdir</span><span class="sxs-lookup"><span data-stu-id="1eed6-156">Additional comments</span></span> 

-   <span data-ttu-id="1eed6-157">Ef notandi hættir verkflæðinu eftir að færslubókarlína er búin til, er færslubókin í með stöðuna óbókað en ef notandinn notar síðar meir verkflæðið fyrir sömu framleiðslupöntun, þá verður línunum bætt við opnu færslubókina frekar en nýja færslubók.</span><span class="sxs-lookup"><span data-stu-id="1eed6-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="1eed6-158">Nýja verkflæðið styður einnig skráningu raðnúmera.</span><span class="sxs-lookup"><span data-stu-id="1eed6-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="1eed6-159">Aðeins er hægt að skrá vörunúmer sem er skilgreint í uppskrift eða í formúlunni fyrir valda framleiðslupöntun eða runupöntun.</span><span class="sxs-lookup"><span data-stu-id="1eed6-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="1eed6-160">Hægt er að ofnota hráefni.</span><span class="sxs-lookup"><span data-stu-id="1eed6-160">Material can be overconsumed.</span></span> <span data-ttu-id="1eed6-161">Sem dæmi um þetta má nefna að ef ætlað er að nota hráefni með magnið 50 kg er hægt að ofnota það með magni sem til dæmis nemur 52 kg.</span><span class="sxs-lookup"><span data-stu-id="1eed6-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]