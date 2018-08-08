--- 
title: "Stofna beiðni um notkun"
description: "Þetta ferli fer í gegnum ferlið fyrir myndun á innkaupabeiðni."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="abd44-103">Stofna beiðni um notkun</span><span class="sxs-lookup"><span data-stu-id="abd44-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abd44-104">Þetta ferli fer í gegnum ferlið fyrir myndun á innkaupabeiðni.</span><span class="sxs-lookup"><span data-stu-id="abd44-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="abd44-105">Hún sýnir mismunandi leiðir til að leita að afurðum í þínu innkaupavörulista og hvernig á að bæta við afurð sem er ekki í vörulistanum þínum.</span><span class="sxs-lookup"><span data-stu-id="abd44-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="abd44-106">Áður en þetta ferli er hafið, verður að hafa innkaupastefna uppsetta með Notkun sem sjálfgefna gerð beiðni.</span><span class="sxs-lookup"><span data-stu-id="abd44-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="abd44-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="abd44-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="abd44-108">Ferlið getur aðeins verið framkvæmt af forstillingu notanda sem þegar er sett upp sem starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="abd44-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="abd44-109">Þetta verk myndi venjulega framkvæmt af starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="abd44-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="abd44-110">öryggishlutverk Starfsmanns gerir þér kleift að framkvæma þau verk, eða ef verið er að nota USMF er hægt að skrá sig inn sem Alicia.</span><span class="sxs-lookup"><span data-stu-id="abd44-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="abd44-111">Stofna nýja innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="abd44-111">Create a new requisition</span></span>
1. <span data-ttu-id="abd44-112">Fara í Innkaup og uppruni > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef.</span><span class="sxs-lookup"><span data-stu-id="abd44-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="abd44-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="abd44-113">Click New.</span></span>
3. <span data-ttu-id="abd44-114">Í svæðið Heiti skal nefna beiðnina.</span><span class="sxs-lookup"><span data-stu-id="abd44-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="abd44-115">Dagsetning er rituð í reitinn umbeðin dagsetning:.</span><span class="sxs-lookup"><span data-stu-id="abd44-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="abd44-116">Sjálfgefið er að umbeðin dagsetning og dagsetning reikningsskila sé afritaðar í innkaupabeiðnilínur.</span><span class="sxs-lookup"><span data-stu-id="abd44-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="abd44-117">Hægt er að breyta þeim á línustigi.</span><span class="sxs-lookup"><span data-stu-id="abd44-117">They can be changed at the line level.</span></span> <span data-ttu-id="abd44-118">Umbeðin dagsetning er umbeðinn afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="abd44-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="abd44-119">Dagsetning er rituð í reitinn dagsetning reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="abd44-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="abd44-120">Bókhaldsdagsetningin er notuð til að skrá bókhaldsfærsluna í fjárhag og staðfesta að fjármagn sé tiltækt.</span><span class="sxs-lookup"><span data-stu-id="abd44-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="abd44-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="abd44-121">Click OK.</span></span>
7. <span data-ttu-id="abd44-122">Í reitnum Ástæða skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="abd44-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="abd44-123">Sjálfgefið er að sú réttlæting viðskipta sem þú velja birtast fyrir innkaupabeiðnilínur, en hægt er að breyta því á línustigi.</span><span class="sxs-lookup"><span data-stu-id="abd44-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="abd44-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="abd44-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="abd44-125">Veljið ástæðu</span><span class="sxs-lookup"><span data-stu-id="abd44-125">Select the reason</span></span>
10. <span data-ttu-id="abd44-126">Í reitinn Upplýsingar skal slá inn meira lýsandi réttlætingu fyrir beiðninni.</span><span class="sxs-lookup"><span data-stu-id="abd44-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="abd44-127">Bæta línu við í innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="abd44-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="abd44-128">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="abd44-128">Click Add line.</span></span>
    * <span data-ttu-id="abd44-129">Til eru tvær leiðir á að bæta línum við innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="abd44-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="abd44-130">Ef þegar vitað afurðarnúmer eða þegar vitað að beðið er um afurð sem er ekki í vörulista, þá geturðu bæta línunni beint með "Bæta Við línu".</span><span class="sxs-lookup"><span data-stu-id="abd44-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="abd44-131">Hin leiðin er að nota "Bæta við afurðir" þar sem hægt er að nota leit og síun til að finna vörur í vörulista.</span><span class="sxs-lookup"><span data-stu-id="abd44-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="abd44-132">Smellt er á línunni sem nýverið var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="abd44-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="abd44-133">Umsækjandinn er starfsmaður sem hefur beðið um beiðnina.</span><span class="sxs-lookup"><span data-stu-id="abd44-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="abd44-134">Sjálfgefið er að einstaklingurinn sem sér um undirbúning innkaupabeiðni er starfsmaður sem hefur beðið um hana.</span><span class="sxs-lookup"><span data-stu-id="abd44-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="abd44-135">Það þarf að veita heimild til að útbúa innkaupabeiðnilínu fyrir hönd annars starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="abd44-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="abd44-136">Ef slíkar heimildir eru til staðar munu hinir starfsmenn birtast í þessari uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="abd44-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="abd44-137">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="abd44-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="abd44-138">Vörur sem eru tiltækar til að velja takmarkast við aðgangsreglur tegundarinnar og innkaupavörulistann fyrir innkaupalögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="abd44-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="abd44-139">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="abd44-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="abd44-140">Bæta fleiri afurðum við innkaupabeiðnina</span><span class="sxs-lookup"><span data-stu-id="abd44-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="abd44-141">Smella á Bæta við afurðum.</span><span class="sxs-lookup"><span data-stu-id="abd44-141">Click Add products.</span></span>
    * <span data-ttu-id="abd44-142">Þetta er valkosturinn þar sem hægt er að leita að afurðir í vörulistanum.</span><span class="sxs-lookup"><span data-stu-id="abd44-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="abd44-143">Í reitnum Finna innkaupa tegund hnúts, Sláðu inn fyrri hluti heitis tegundar þú leitar, og smellið síðan á Enter.</span><span class="sxs-lookup"><span data-stu-id="abd44-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="abd44-144">Til dæmis, skráið tölva.</span><span class="sxs-lookup"><span data-stu-id="abd44-144">For example, type comput.</span></span>  
3. <span data-ttu-id="abd44-145">Nota InvokeDefaultButton flýtivísunina.</span><span class="sxs-lookup"><span data-stu-id="abd44-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="abd44-146">Nota Síu til að sía lista yfir vörur í völdu tegundinni.</span><span class="sxs-lookup"><span data-stu-id="abd44-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="abd44-147">Veldu vöruspjaldið sem á að bæta við innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="abd44-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="abd44-148">Smellt er á Bæta við línum.</span><span class="sxs-lookup"><span data-stu-id="abd44-148">Click Add to lines.</span></span>
7. <span data-ttu-id="abd44-149">Í reitinn magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="abd44-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="abd44-150">Í reitnum Finna innkaupa tegund hnúts, Sláðu inn fyrri hluti heitis tegundar þú leitar, og smellið síðan á Enter.</span><span class="sxs-lookup"><span data-stu-id="abd44-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="abd44-151">Til dæmis skráið Há (highlighters).</span><span class="sxs-lookup"><span data-stu-id="abd44-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="abd44-152">Nota InvokeDefaultButton flýtivísunina.</span><span class="sxs-lookup"><span data-stu-id="abd44-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="abd44-153">Smella á bæta Við óskráðum afurðar á línur til að bæta við vöru sem er ekki skráður í innkaupavörulista.</span><span class="sxs-lookup"><span data-stu-id="abd44-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="abd44-154">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="abd44-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="abd44-155">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="abd44-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="abd44-156">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="abd44-156">Click OK.</span></span>
14. <span data-ttu-id="abd44-157">Bæta við lýsingu á afurðina í lýsingarsvæði Vöru.</span><span class="sxs-lookup"><span data-stu-id="abd44-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="abd44-158">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="abd44-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="abd44-159">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="abd44-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="abd44-160">Ef þú þekkir verð fyrir tiltekna lánardrottna (sem er valin í svæðinu lánardrottnalykill) þá er hægt að færa inn verðið.</span><span class="sxs-lookup"><span data-stu-id="abd44-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="abd44-161">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="abd44-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="abd44-162">Lánardrottna sem eru tiltækar í þessu svæði eru háð innkaupareglur og stöðu sem lánardrottinn hefur fyrir gildandi innkaupategundina.</span><span class="sxs-lookup"><span data-stu-id="abd44-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="abd44-163">Auk þess að velja lánardrottin hér, hægt að smella á hnappinn Leggja til lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="abd44-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="abd44-164">Veljið lánardrottinn sem á að nota í listanum.</span><span class="sxs-lookup"><span data-stu-id="abd44-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="abd44-165">Í reitnum ytra vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="abd44-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="abd44-166">Þetta er tilvísunarnúmer fyrir afurð sem lánardrottinn þekkir.</span><span class="sxs-lookup"><span data-stu-id="abd44-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="abd44-167">Til dæmis, gæti þetta verið vörunúmer afurðar í eigin vörulista lánardrottins .</span><span class="sxs-lookup"><span data-stu-id="abd44-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="abd44-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="abd44-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="abd44-169">Dreifa upphæðum</span><span class="sxs-lookup"><span data-stu-id="abd44-169">Distribute amounts</span></span>
1. <span data-ttu-id="abd44-170">Smelltu á Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="abd44-170">Click Financials.</span></span>
2. <span data-ttu-id="abd44-171">Smellt er á Dreifa upphæðum.</span><span class="sxs-lookup"><span data-stu-id="abd44-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="abd44-172">Þetta ferli sýnir hvernig á að dreifa kostnaði í fyrstu línunni á milli 2 lykla.</span><span class="sxs-lookup"><span data-stu-id="abd44-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="abd44-173">Einnig má gera það seinna þegar innkaupabeiðni er í yfirferð.</span><span class="sxs-lookup"><span data-stu-id="abd44-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="abd44-174">Smellt er á Skipta til að stofna nýja dreifingarlínu.</span><span class="sxs-lookup"><span data-stu-id="abd44-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="abd44-175">Í svæðinu fjárhagslykill, veljið fyrst kostnaðarstaður sem á að taka þátt í kostnaðinum.</span><span class="sxs-lookup"><span data-stu-id="abd44-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="abd44-176">Veljið aðra dreifingarlínuna.</span><span class="sxs-lookup"><span data-stu-id="abd44-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="abd44-177">Í fjárhagslykil svæðinu, tilgreinið hitt kostnaðarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="abd44-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="abd44-178">Smellt er á Dreifa jafnt.</span><span class="sxs-lookup"><span data-stu-id="abd44-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="abd44-179">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="abd44-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="abd44-180">Skoða línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="abd44-180">View line details</span></span>
1. <span data-ttu-id="abd44-181">Víxla útvíkkun á liðnum línuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="abd44-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="abd44-182">Senda innkaupabeiðnina</span><span class="sxs-lookup"><span data-stu-id="abd44-182">Submit the requisition</span></span>
1. <span data-ttu-id="abd44-183">Smellt er á Verkflæði til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="abd44-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="abd44-184">Smelltu á Senda.</span><span class="sxs-lookup"><span data-stu-id="abd44-184">Click Submit.</span></span>
3. <span data-ttu-id="abd44-185">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="abd44-185">Close the page.</span></span>
4. <span data-ttu-id="abd44-186">Í svæðinu Athugasemd, færðu inn gerð athugasemdar fyrir samþykkjandi innkaupabeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="abd44-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="abd44-187">Smelltu á Senda.</span><span class="sxs-lookup"><span data-stu-id="abd44-187">Click Submit.</span></span>
6. <span data-ttu-id="abd44-188">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="abd44-188">Close the page.</span></span>
7. <span data-ttu-id="abd44-189">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="abd44-189">Refresh the page.</span></span>


