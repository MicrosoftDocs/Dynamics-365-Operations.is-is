---
title: Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók
description: Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota ítarleg vöruhúsakerfisferli.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea8b5e03282aa21aa9dfa486b1deaced6af4601c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976925"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="8f362-103">Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók</span><span class="sxs-lookup"><span data-stu-id="8f362-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f362-104">Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota ítarleg vöruhúsakerfisferli.</span><span class="sxs-lookup"><span data-stu-id="8f362-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="8f362-105">Þetta væri yfirleitt gert með af móttöku starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="8f362-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="8f362-106">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="8f362-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="8f362-107">Þú þarft að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu áður en byrjað er á þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="8f362-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="8f362-108">Vara í línu verður að vera í birgðum og því verður að nota afurðarafbrigði og má ekki hafa rakningarvíddir.</span><span class="sxs-lookup"><span data-stu-id="8f362-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="8f362-109">Og varan þarf að vera tengd við vöruhúsakerfisferli með virkan geymsluvíddarflokk.</span><span class="sxs-lookup"><span data-stu-id="8f362-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="8f362-110">Vöruhús sem er notað verður að vera virkt fyrir vöruhúsakerfisferli og staðsetning sem er notað fyrir móttöku verður að vera númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="8f362-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="8f362-111">Ef verið er að nota USMF er hægt að nota reikningsskil 1001, Vöruhús 51 og vöru M9200 til að stofna Innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="8f362-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="8f362-112">Skráðu niður númer innkaupapöntunarinnar sem er stofnuð og athugaðu einnig vörunúmer og svæði sem voru notuð fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="8f362-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="8f362-113">Stofna haus vörukomubókar</span><span class="sxs-lookup"><span data-stu-id="8f362-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="8f362-114">Fara á Vörukomu.</span><span class="sxs-lookup"><span data-stu-id="8f362-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="8f362-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8f362-115">Click New.</span></span>
3. <span data-ttu-id="8f362-116">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="8f362-117">Ef verið er að nota USMF, er hægt að færa inn vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="8f362-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="8f362-118">Ef verið er að nota önnur gögn, verður heiti færslubókar þú hefur valið að hafa eftirfarandi eiginleika: Athuga tiltektarstaðsetningu verður að vera stillt á Nei og biðgeymslustjórnun verður að vera stillt á nei.</span><span class="sxs-lookup"><span data-stu-id="8f362-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="8f362-119">Í reitnum Númer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="8f362-120">Í reitinn Svæði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="8f362-121">Veljið svæðið sem notað er fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="8f362-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="8f362-122">Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="8f362-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="8f362-123">Ef þú notaðir vöruhús 51 í USMF velurðu svæði 5.</span><span class="sxs-lookup"><span data-stu-id="8f362-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="8f362-124">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="8f362-125">Velja gilt vöruhús fyrir svæðið sem var valið.</span><span class="sxs-lookup"><span data-stu-id="8f362-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="8f362-126">Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="8f362-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="8f362-127">Ef verið er að nota dæmagildi í USMF, veljið 51.</span><span class="sxs-lookup"><span data-stu-id="8f362-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="8f362-128">Í reitinn staðsetning skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="8f362-129">Velja gilda staðsetningu í vöruhúsinu sem var valið.</span><span class="sxs-lookup"><span data-stu-id="8f362-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="8f362-130">Staðsetning verður að vera tengd við forstillingu staðsetningar, sem er númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="8f362-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="8f362-131">Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="8f362-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="8f362-132">Ef verið er að nota gildi dæmi í USMF, veljið Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="8f362-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="8f362-133">Hægrismellið á felliörina í reitnum Númeraplata og veldu síðan Skoða upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8f362-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="8f362-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8f362-134">Click New.</span></span>
10. <span data-ttu-id="8f362-135">Í reitinn Númeraplata skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="8f362-136">Skráið niður gildið.</span><span class="sxs-lookup"><span data-stu-id="8f362-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="8f362-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8f362-137">Click Save.</span></span>
12. <span data-ttu-id="8f362-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8f362-138">Close the page.</span></span>
13. <span data-ttu-id="8f362-139">Í reitinn Númeraplata skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="8f362-140">Færið inn gildi í númeraplötu sem nýverið var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="8f362-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="8f362-141">Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="8f362-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="8f362-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8f362-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="8f362-143">Bæta við línu</span><span class="sxs-lookup"><span data-stu-id="8f362-143">Add a line</span></span>
1. <span data-ttu-id="8f362-144">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="8f362-144">Click Add line.</span></span>
2. <span data-ttu-id="8f362-145">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8f362-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8f362-146">Færið inn vörunúmerið sem var notað í línu innkaupapöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="8f362-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="8f362-147">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="8f362-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8f362-148">Færið inn magnið sem á að skrá.</span><span class="sxs-lookup"><span data-stu-id="8f362-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="8f362-149">Reiturinn Dagsetning ákvarðar dagsetninguna sem verður að skrá magn á lager fyrir þessa vöru í birgðum.</span><span class="sxs-lookup"><span data-stu-id="8f362-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="8f362-150">Lotukenni er fyllt út af kerfinu ef hægt er að auðkenna það úr uppgefnum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="8f362-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="8f362-151">Annars verður að bæta þessu við handvirkt.</span><span class="sxs-lookup"><span data-stu-id="8f362-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="8f362-152">Þetta er skyldusvæði sem tengir þessa skráningu við tiltekna upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="8f362-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="8f362-153">Ljúka við skráninguna</span><span class="sxs-lookup"><span data-stu-id="8f362-153">Complete the registration</span></span>
1. <span data-ttu-id="8f362-154">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="8f362-154">Click Validate.</span></span>
    * <span data-ttu-id="8f362-155">Þetta athugar hvort færslubókin sé tilbúin til bókunar.</span><span class="sxs-lookup"><span data-stu-id="8f362-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="8f362-156">Ef sannvottun bregst verður að lagfæra villurnar áður en hægt er að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="8f362-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="8f362-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8f362-157">Click OK.</span></span>
    * <span data-ttu-id="8f362-158">Athugaðu skilaboðin eftir að smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="8f362-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="8f362-159">Það ættu að vera skilaboð sem segja að færslubókin sé í lagi.</span><span class="sxs-lookup"><span data-stu-id="8f362-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="8f362-160">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="8f362-160">Click Post.</span></span>
4. <span data-ttu-id="8f362-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8f362-161">Click OK.</span></span>
    * <span data-ttu-id="8f362-162">Eftir að smellt hefur verið í lagi, athuga skilaboðastikunni.</span><span class="sxs-lookup"><span data-stu-id="8f362-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="8f362-163">Það ættu að vera skilaboð sem segja að aðgerðinni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="8f362-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="8f362-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8f362-164">Close the page.</span></span>

