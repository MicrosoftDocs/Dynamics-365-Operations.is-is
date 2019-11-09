---
title: Greiðsluyfirlit lánardrottins
description: Þessi leiðarvísir fyrir verk fer í gegnum ýmsar aðferðir sem eru notuð til að stofna greiðslur lánardrottna, þar á meðal hvernig á að nota greiðslutillögu eða færa handvirkt inn eingreiðslu.
author: kweekley
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcf22a3e9564f991b0cb5ebbd6a2282e3e749990
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178296"
---
# <a name="vendor-payment-overview"></a><span data-ttu-id="67219-103">Greiðsluyfirlit lánardrottins</span><span class="sxs-lookup"><span data-stu-id="67219-103">Vendor payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67219-104">Þessi leiðarvísir fyrir verk fer í gegnum ýmsar aðferðir sem eru notuð til að stofna greiðslur lánardrottna, þar á meðal hvernig á að nota greiðslutillögu eða færa handvirkt inn eingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="67219-104">This task guide will walk you through various methods used to create vendor payments, including how to use a payment proposal or manually entering a one-off payment.</span></span> <span data-ttu-id="67219-105">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="67219-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="67219-106">Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Greiðslur > Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="67219-106">Go to **Navigation pane > Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="67219-107">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="67219-107">Click **New**.</span></span>
3. <span data-ttu-id="67219-108">Veljið greiðslubók þar sem á að vista greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="67219-108">Select the payment journal in which to save the vendor payments.</span></span> 
4. <span data-ttu-id="67219-109">Veljið færslubók eða færa það handvirkt inn.</span><span class="sxs-lookup"><span data-stu-id="67219-109">Select the journal or manually enter it.</span></span>
5. <span data-ttu-id="67219-110">Smellið á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="67219-110">Click **Lines**.</span></span>
6. <span data-ttu-id="67219-111">Í **aðgerðaglugganum** smellirðu á **Greiðslutillaga**.</span><span class="sxs-lookup"><span data-stu-id="67219-111">On **Ation pane**, click **Payment proposal**.</span></span>
7. <span data-ttu-id="67219-112">Smelltu á **Stofna greiðslutillögu**.</span><span class="sxs-lookup"><span data-stu-id="67219-112">Click **Create payment proposal**.</span></span> <span data-ttu-id="67219-113">Greiðslutillaga er fyrirspurn notuð til að velja reikninga til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="67219-113">The payment proposal is a query used to select invoices for payment.</span></span> <span data-ttu-id="67219-114">Hægt er að breyta lista yfir reikninga til greiðslu áður en þú stofnar eða myndar greiðslur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="67219-114">You can edit the list of invoices to pay before creating or generating the vendor payments.</span></span>
8. <span data-ttu-id="67219-115">Velja reikninga til greiðslu samkvæmt gjalddaga, staðgreiðsluafslátt, eða bæði.</span><span class="sxs-lookup"><span data-stu-id="67219-115">Select invoices for payment by due date, cash discount, or both.</span></span> 
9. <span data-ttu-id="67219-116">Færið inn dagsetningu til að bera saman við gjalddaga eða staðgreiðsluafslátt.</span><span class="sxs-lookup"><span data-stu-id="67219-116">Enter the date for comparing to the due date or cash discount.</span></span> 
10. <span data-ttu-id="67219-117">Valfrjálst: Færið Inn greiðsludagsetningu sem er notað fyrir allar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="67219-117">Optional: Enter a payment date used for all payments.</span></span> <span data-ttu-id="67219-118">Dagsetningin sem færð er inn hér verður greiðsludagur fyrir allar greiðslur sem eru stofnaðar, óháð gjalddaga eða dagsetning staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="67219-118">The date entered here will be the payment date for all payments created, regardless of the due date or cash discount date.</span></span>  
11. <span data-ttu-id="67219-119">Valfrjálst: Slá Inn lágmarks greiðsludag sem má nota sem greiðsludag.</span><span class="sxs-lookup"><span data-stu-id="67219-119">Optional: Enter a minimum payment date which may be used as the payment date.</span></span> <span data-ttu-id="67219-120">Lágmarks greiðsludagur verður fyrstu mögulegu dagsetningu sem er notaður þegar greiðslur eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="67219-120">The minimum payment date will be the earliest date used when creating payments.</span></span> <span data-ttu-id="67219-121">Til dæmis, ef reikningur er á gjalddaga eftir lágmarks greiðsludag, mun gjalddaga verða greiðsludagsetningu í stað lágmarks greiðsludags til að greiða reikninginn á síðustu mögulegu dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="67219-121">For example, if an invoice has a due date after the minimum payment date, the due date will become the payment date instead of the minimum payment date in order to pay the invoice on the latest possible date.</span></span>
12. <span data-ttu-id="67219-122">Færa inn viðbótarskilyrði fyrirspurnarinnar undir hlutann **Færslur að hafa með**.</span><span class="sxs-lookup"><span data-stu-id="67219-122">Enter additional query restrictions under **Records to include** section.</span></span> <span data-ttu-id="67219-123">Síunni er oft notað til að takmarka þá reikninga sem eru valdar fyrir greiðslu eftir lánardrottnaflokki eða greiðsluhætti.</span><span class="sxs-lookup"><span data-stu-id="67219-123">The filter is often used to restrict the invoices selected for payment by vendor group or method of payment.</span></span> <span data-ttu-id="67219-124">Til dæmis er hægt að bæta við síu til að greiða einungis reikninga með ávísun í þessari launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="67219-124">For example, you may add a filter to only pay invoices by check in this pay run.</span></span>
13. <span data-ttu-id="67219-125">Færa inn viðbótarskilyrði fyrirspurnarinnar eða sjálfgildi greiðslu.</span><span class="sxs-lookup"><span data-stu-id="67219-125">Enter additional query restriction or payment defaults.</span></span> <span data-ttu-id="67219-126">Viðbótar færibreytur er hægt að nota til að skilgreina greiðslugjaldmiðli eða til að virkja miðstýrðar greiðslur fyrir þessa launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="67219-126">The additional parameters can be used to define the payment currency or to enable centralized payments for this pay run.</span></span>  
14. <span data-ttu-id="67219-127">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="67219-127">Click **OK**.</span></span> <span data-ttu-id="67219-128">Niðurstöður fyrirspurnarinnar mun birtast þegar smellt er á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="67219-128">After clicking **OK**, the results of the query will appear.</span></span> <span data-ttu-id="67219-129">Ef ekki á að forskoða lista yfir reikninga sem eru valdir til greiðslu er hægt að fara aftur í flýtiflipann **Færibreytur** og breyta stillingunum **Stofna greiðslur án forskoðunar á reikningi** í Já.</span><span class="sxs-lookup"><span data-stu-id="67219-129">If you don't want to preview the list of invoices selected to pay, you can go back to the **Parameters** fast tab and change the setting **Create payments without invoice preview** to "Yes".</span></span>  
15. <span data-ttu-id="67219-130">Velja hnappinn **Sýna greiðsluyfirlit** til að skoða þær greiðslur sem verður stofnaðar fyrir lánardrottinn á völdum reikningi.</span><span class="sxs-lookup"><span data-stu-id="67219-130">Choose the **Show payment overview** button to view the payments that will be created for the vendor on the invoice selected.</span></span>
16. <span data-ttu-id="67219-131">Velja hnappinn **Fela greiðsluyfirlit** til fela greiðslur.</span><span class="sxs-lookup"><span data-stu-id="67219-131">Choose the **Hide payment overview** button to hide the payments.</span></span> 
17. <span data-ttu-id="67219-132">Smellt er á **Stofna greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="67219-132">Click **Create payments**.</span></span> <span data-ttu-id="67219-133">Áður en valið er að **Stofna greiðslur** er hægt að hægri-smella í hnitanetinu og flytja út lista af reikningum í Excel.</span><span class="sxs-lookup"><span data-stu-id="67219-133">Before choosing **Create payments**, you can right click on the grid and export the list of invoices to Excel.</span></span> <span data-ttu-id="67219-134">Hnappurinn til að **Stofna greiðslur** stofnar lánadrottnagreiðslur í greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="67219-134">The **Create payments** button will create the vendor payments in the payment journal.</span></span>  
18. <span data-ttu-id="67219-135">Skanna greiðslum og gangið úr skugga um að greiðsluaðferð er skilgreind fyrir allar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="67219-135">Scan your payments and make sure the method of payment is defined for all payments.</span></span> <span data-ttu-id="67219-136">Ef þú myndar greiðslurnar, eins og ávísun er prentuð eða stofnar rafræna greiðslu, verður að skilgreina greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="67219-136">If you generate the payments, such as printing a check or creating an electronic payment, the method of payment must be defined.</span></span> <span data-ttu-id="67219-137">Greiðsluháttur mun einnig falla í vanskil á bankareiknngnum frá því að greiðslan er gerð.</span><span class="sxs-lookup"><span data-stu-id="67219-137">The method of payment will also default the bank account from the payment will be made.</span></span>  
19. <span data-ttu-id="67219-138">Smella á **Nýtt** til að stofna eingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="67219-138">Click **New** to create a one-off payment.</span></span> <span data-ttu-id="67219-139">Hægt er að bæta eingreiðslu í greiðslubók hvenær sem er fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="67219-139">A one-off payment can be added to a payment journal at any time prior to posting.</span></span> <span data-ttu-id="67219-140">Þetta er gert með því að smella á hnappinn **Nýtt** og bæta upplýsingar um greiðslu handvirkt, frekar en að nota **greiðslutillöguna**.</span><span class="sxs-lookup"><span data-stu-id="67219-140">This is done by clicking the **New** button and adding the payment information manually, rather than using the **Payment proposal**.</span></span>  
20. <span data-ttu-id="67219-141">Veljið lánardrottinn sem greiðslan fer til.</span><span class="sxs-lookup"><span data-stu-id="67219-141">Select the vendor to whom the payment will be made.</span></span>
21. <span data-ttu-id="67219-142">Ef reikningur er til greiðslu, skal að velja **Jafna færslur** til að velja reikning til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="67219-142">If an invoice exists to pay, select **Settle transactions** to select the invoice for payment.</span></span> <span data-ttu-id="67219-143">Ef þetta er fyrirframgreiðsla er þetta þrep valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="67219-143">If this is a prepayment, this step is optional.</span></span> <span data-ttu-id="67219-144">Hægt er að stofna greiðslu án þess að velja neinn reikning.</span><span class="sxs-lookup"><span data-stu-id="67219-144">You can create the payment without selecting any invoice.</span></span> 
22. <span data-ttu-id="67219-145">Merkja allar reikninga sem verða greiddir.</span><span class="sxs-lookup"><span data-stu-id="67219-145">Mark any invoices that will be paid.</span></span> <span data-ttu-id="67219-146">Ef verið er að **Jafna færslur** er notuð til að velja reikninga til greiðslu er greiðsluupphæðin sjálfkrafa reiknuð út á samkvæmt þeim reikningum sem á að merkja til greiðslu og hvaða upphæð er færð inn í **Upphæð til jöfnunar**.</span><span class="sxs-lookup"><span data-stu-id="67219-146">If you use the **Settle transactions** to select the invoices for payment, the payment amount will automatically be calculated based on what invoices you mark for payment, and what amount you enter in the **Amount to settle**.</span></span>
23. <span data-ttu-id="67219-147">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="67219-147">Click **OK**.</span></span>
24. <span data-ttu-id="67219-148">Ef óskað er að eyða greiðslu skal merkja línuna.</span><span class="sxs-lookup"><span data-stu-id="67219-148">If you want to delete a payment, mark the row.</span></span>
25. <span data-ttu-id="67219-149">Smellið á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="67219-149">Click **Delete**.</span></span> <span data-ttu-id="67219-150">Eyðing greiðslu mun aðeins eyða greiðslunni.</span><span class="sxs-lookup"><span data-stu-id="67219-150">Deleting a payment will only delete the payment.</span></span> <span data-ttu-id="67219-151">Allir reikningar merktir til greiðslu verða enn tiltækir til greiðslu með annarri greiðslu.</span><span class="sxs-lookup"><span data-stu-id="67219-151">Any invoices marked for payment will still be available to be paid by another payment.</span></span>
26. <span data-ttu-id="67219-152">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="67219-152">Click **Yes**.</span></span>
27. <span data-ttu-id="67219-153">Velja **Mynda greiðslu** til að prenta ávísanir eða stofna rafræna greiðsluskrá.</span><span class="sxs-lookup"><span data-stu-id="67219-153">Choose **Generate payment** to print checks or create the electronic payment file.</span></span>
28. <span data-ttu-id="67219-154">Velja greiðsluhátt sem á að mynda.</span><span class="sxs-lookup"><span data-stu-id="67219-154">Select the method of payment that you want to generate.</span></span> <span data-ttu-id="67219-155">Greiðslubók getur innihaldið greiðslur fyrir bæði ávísanir, en einungis er hægt að mynda eina greiðslugerð í einu.</span><span class="sxs-lookup"><span data-stu-id="67219-155">The payment journal can contain payments for both Checks and electronic payments, but you can only generate one payment type at a time.</span></span>
29. <span data-ttu-id="67219-156">Velja bankareikninginn þaðan sem á að búa til greiðslur.</span><span class="sxs-lookup"><span data-stu-id="67219-156">Select the bank account from which to generate the payments.</span></span>
30. <span data-ttu-id="67219-157">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="67219-157">Click **OK**.</span></span> <span data-ttu-id="67219-158">Greiðslur verða aðeins myndaðar fyrir greiðslur sem samsvara þeim **greiðsluhætti** og **bankareikningi** sem var valinn.</span><span class="sxs-lookup"><span data-stu-id="67219-158">Payments will only be generated for payments that match the **Method of payment** and **Bank account** you selected.</span></span>
31. <span data-ttu-id="67219-159">Ef verið er að mynda **ávísanir**, veljið **Skjal** til að að tryggja að rétt prentara sé notaður fyrir ávísanirnar.</span><span class="sxs-lookup"><span data-stu-id="67219-159">If you are generating **Checks**, choose **Document** to ensure the correct print destination for the checks.</span></span>
32. <span data-ttu-id="67219-160">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="67219-160">Click **OK**.</span></span>
33. <span data-ttu-id="67219-161">Smellt er á **Í lagi** til að búa til greiðslur.</span><span class="sxs-lookup"><span data-stu-id="67219-161">Click **OK** to generate the payments.</span></span>
34. <span data-ttu-id="67219-162">Smellt er á **Bóka** ef allar greiðslur eru samþykktar og myndaðar.</span><span class="sxs-lookup"><span data-stu-id="67219-162">Click **Post** if all the payments are approved and generated.</span></span> 
