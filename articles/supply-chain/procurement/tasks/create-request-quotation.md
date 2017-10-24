--- 
title: "Stofna beiðni um tilboð"
description: "Þessi verklýsing sýnir hvernig á að stofna beiðni um tilboð."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="400b6-103">Stofna beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="400b6-103">Create a request for quotation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="400b6-104">Þessi verklýsing sýnir hvernig á að stofna beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="400b6-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="400b6-105">Þetta verk myndi yfirleitt gert af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="400b6-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="400b6-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="400b6-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="400b6-107">Þú Þarft að hafa sett upp beiðnigerðir áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="400b6-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="400b6-108">Þegar þessu verki hefur verið lokið og stofnuð og send hefur verið beiðni um TILBOÐ, er hægt að færa svör fyrir hvern lánardrottinn, gera samanburð á þeim og veita samninga.</span><span class="sxs-lookup"><span data-stu-id="400b6-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="400b6-109">Útbúa skal nýja beiðni um tilboð</span><span class="sxs-lookup"><span data-stu-id="400b6-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="400b6-110">Fara í innkaup og aðföng  > Beiðnir um tilboð  > Allar beiðnir um tilboð.</span><span class="sxs-lookup"><span data-stu-id="400b6-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="400b6-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="400b6-111">Click New.</span></span>
    * <span data-ttu-id="400b6-112">Eftirfarandi gerðir innkaupa eru tiltækar: Innkaupapöntun (það er sjálfgefið): skjal sem staðfestir tilboð um að kaupa afurðir, eða samþykki tilboðs um að selja afurðir in skiptum fyrir greiðslu.</span><span class="sxs-lookup"><span data-stu-id="400b6-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="400b6-113">Innkaupabeiðni – Þessi gerð er sjálfkrafa valin ef stofna á tilboðsbeiðni beint úr innkaupabeiðni.</span><span class="sxs-lookup"><span data-stu-id="400b6-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="400b6-114">Ef þessi valkostur er valinn handvirk kemur upp villa.</span><span class="sxs-lookup"><span data-stu-id="400b6-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="400b6-115">Innkaupasamningur - samningur um að kaupa ákveðið magn eða virði vöru yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="400b6-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="400b6-116">Ef þessi valkostur er valinn verður að velja dagsetningabilið sem á við innkaupasamninginn.</span><span class="sxs-lookup"><span data-stu-id="400b6-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="400b6-117">Í reitinn Titill skjals skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="400b6-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="400b6-118">Færa inn eða veljið gildi í svæðinu beiðnigerð.</span><span class="sxs-lookup"><span data-stu-id="400b6-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="400b6-119">Ef stigagjafaraðferð er tengd gerð beiðni verður hún sjálfgefin gerð beðini fyrir tilboð sem verið er að stofna.</span><span class="sxs-lookup"><span data-stu-id="400b6-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="400b6-120">Þá er mögulegt að breyta aðferð við stigagjöf seinna.</span><span class="sxs-lookup"><span data-stu-id="400b6-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="400b6-121">Dagsetning er rituð í reitinn afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="400b6-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="400b6-122">Velja skal þá dagsetningu þegar á að taka á móti afurðunum.</span><span class="sxs-lookup"><span data-stu-id="400b6-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="400b6-123">Færa inn dagsetningu og tíma í reitnum fyrir lokadag og gildistíma.</span><span class="sxs-lookup"><span data-stu-id="400b6-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="400b6-124">Tilgreina skal dagsetninguna og tímann innan hvers lánardrottnar verða svara beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="400b6-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="400b6-125">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="400b6-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="400b6-126">Afhendingaraðsetur mun vera sjálfgefið aðsetur vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="400b6-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="400b6-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="400b6-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="400b6-128">Bæta við línum</span><span class="sxs-lookup"><span data-stu-id="400b6-128">Add lines</span></span>
    * <span data-ttu-id="400b6-129">Eftir að þú hefur tilgreint grunnupplýsingar um tilboðsbeiðnir þínar, þú að tilgreina vörur eða þjónustu sem þú vilt að lánardrottnar geri tilboð í.</span><span class="sxs-lookup"><span data-stu-id="400b6-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="400b6-130">Þetta er sjálfgefin línugerð.</span><span class="sxs-lookup"><span data-stu-id="400b6-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="400b6-131">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="400b6-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="400b6-132">Ef verið er að nota USMF er hægt að velja 'T0020'.</span><span class="sxs-lookup"><span data-stu-id="400b6-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="400b6-133">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="400b6-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="400b6-134">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="400b6-134">Click Add line.</span></span>
4. <span data-ttu-id="400b6-135">Veljið Flokkur í reitnum Gerð línu.</span><span class="sxs-lookup"><span data-stu-id="400b6-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="400b6-136">Hægt er að nota línugerðina Tegund til að stofna Tilboðsbeiðnir fyrir vörur eða þjónustu sem eru ekki hluti af birgðum.</span><span class="sxs-lookup"><span data-stu-id="400b6-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="400b6-137">Svo þarf að velja gerð af vörur eða þjónustu úr stigveldi innkaupaflokka.</span><span class="sxs-lookup"><span data-stu-id="400b6-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="400b6-138">Slá inn eða velja gildi í reitnum innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="400b6-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="400b6-139">Í reitinn Afurðarheiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="400b6-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="400b6-140">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="400b6-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="400b6-141">Í reitinn eining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="400b6-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="400b6-142">Bæta við lánardrottnum</span><span class="sxs-lookup"><span data-stu-id="400b6-142">Add vendors</span></span>
1. <span data-ttu-id="400b6-143">Smellt er á Hausnum til að breyta úr línuyfirliti í hausyfirlit.</span><span class="sxs-lookup"><span data-stu-id="400b6-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="400b6-144">Stækka hlutann Lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="400b6-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="400b6-145">Smellt er á Bæta lánardrottnum sjálfkrafa við.</span><span class="sxs-lookup"><span data-stu-id="400b6-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="400b6-146">Þú getur bæta lánardrottnum á beiðni um tilboð sjálfkrafa samkvæmt innkaupategund umbeðnu varanna.</span><span class="sxs-lookup"><span data-stu-id="400b6-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="400b6-147">Ef það eru engir lánardrottnar samþykkt fyrir tegundum í línum er hægt að bæta lánardrottnum við handvirkt.</span><span class="sxs-lookup"><span data-stu-id="400b6-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="400b6-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="400b6-148">Click Add.</span></span>
5. <span data-ttu-id="400b6-149">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="400b6-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="400b6-150">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="400b6-150">Click Add.</span></span>
7. <span data-ttu-id="400b6-151">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="400b6-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="400b6-152">Þegar lánardrottinn var valinn, er staða Stofnuð.</span><span class="sxs-lookup"><span data-stu-id="400b6-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="400b6-153">Upplýsingar lánardrottinsins hafa samkvæmt þessu verið vistaðar í beiðninni um tilboð, en notandi hefur ekki sent beiðni um tilboð til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="400b6-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="400b6-154">Hægt er að bæta lánardrottni við tilboðsbeiðni óháð stöðu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="400b6-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="400b6-155">Senda beiðni um tilboð til lánardrottna</span><span class="sxs-lookup"><span data-stu-id="400b6-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="400b6-156">Smellt er á Senda.</span><span class="sxs-lookup"><span data-stu-id="400b6-156">Click Send.</span></span>
    * <span data-ttu-id="400b6-157">Í síðunni senda beiðni um tilboð skal gengið úr skugga um að lánardrottnar í listanum séu þeir sem á að senda tilboðsbeiðni til.</span><span class="sxs-lookup"><span data-stu-id="400b6-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="400b6-158">Smelltu á Prenta.</span><span class="sxs-lookup"><span data-stu-id="400b6-158">Click Print.</span></span>
    * <span data-ttu-id="400b6-159">Þessi svargluggi gerir notanda kleift að prenta beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="400b6-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="400b6-160">Ef kosið er að prenta svarblað er innihald þessa skilgreint í færibreytum innkaupa og aðfanga.</span><span class="sxs-lookup"><span data-stu-id="400b6-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="400b6-161">Til að velja hvernig á að prenta svarblöð, þegar búið er að opna prentglugga, smella á Ítarlegir prentunarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="400b6-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="400b6-162">Ein beiðni um tilboð verður prentuð fyrir hvern lánardrottinn sem inniheldur línur sem hafa stöðuna Stofnað eða Sent.</span><span class="sxs-lookup"><span data-stu-id="400b6-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="400b6-163">Línur sem hætt var við og línur með skráðum svörum verða ekki prentaðar.</span><span class="sxs-lookup"><span data-stu-id="400b6-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="400b6-164">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="400b6-164">Click Cancel.</span></span>
4. <span data-ttu-id="400b6-165">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="400b6-165">Click OK.</span></span>
5. <span data-ttu-id="400b6-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="400b6-166">Close the page.</span></span>
6. <span data-ttu-id="400b6-167">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="400b6-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="400b6-168">Skoða færslubók tilboðsbeiðna</span><span class="sxs-lookup"><span data-stu-id="400b6-168">View the RFQ journal</span></span>
1. <span data-ttu-id="400b6-169">Fara í innkaup og aðföng > Beiðnir um tilboð > eftirfylgni við Beiðni um tilboð > Færslubækur beiðna um tilboð.</span><span class="sxs-lookup"><span data-stu-id="400b6-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="400b6-170">Smellt er á Forskoða/prenta.</span><span class="sxs-lookup"><span data-stu-id="400b6-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="400b6-171">Smellt er á forskoðunina Upprunalegt.</span><span class="sxs-lookup"><span data-stu-id="400b6-171">Click Original preview.</span></span>
4. <span data-ttu-id="400b6-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="400b6-172">Close the page.</span></span>
5. <span data-ttu-id="400b6-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="400b6-173">Close the page.</span></span>


