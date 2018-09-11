--- 
title: "Greiðsluyfirlit viðskiptavina"
description: "Þessar verkefnaleiðbeiningar fara yfir ýmsar aðferðir sem notaðar eru til að færa inn greiðslur viðskiptavina."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0e534a468a49f0221c3ee2b8999264a3fbeaf774
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="customer-payment-overview"></a><span data-ttu-id="1390f-103">Greiðsluyfirlit viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="1390f-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1390f-104">Þessar verkefnaleiðbeiningar fara yfir ýmsar aðferðir sem notaðar eru til að færa inn greiðslur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="1390f-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="1390f-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="1390f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1390f-106">Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="1390f-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="1390f-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1390f-107">Click New.</span></span>
3. <span data-ttu-id="1390f-108">Veljið greiðslubók þar sem greiðslur viðskiptavina verða vistaðar.</span><span class="sxs-lookup"><span data-stu-id="1390f-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="1390f-109">Veljið eða færið handvirkt inn í færslubók.</span><span class="sxs-lookup"><span data-stu-id="1390f-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="1390f-110">Smellið á „Færa inn greiðslur viðskiptavina“.</span><span class="sxs-lookup"><span data-stu-id="1390f-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="1390f-111">„Færa inn greiðslur viðskiptavina“ er notað til að færa inn eina greiðslu viðskiptavinar í senn.</span><span class="sxs-lookup"><span data-stu-id="1390f-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="1390f-112">Greiðsluupplýsingarnar eru færðar inn efst og þá er hægt að merkja við reikningana sem voru borgaðir með greiðslunni, allt á sömu síðunni.</span><span class="sxs-lookup"><span data-stu-id="1390f-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="1390f-113">Færðu inn viðskiptavin sem greiðsla var móttekin frá.</span><span class="sxs-lookup"><span data-stu-id="1390f-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="1390f-114">Ef notandinn veit ekki hver viðskiptavinurinn er en veit hvaða færsla var greidd er hægt að nota færslureitinn til að færa inn greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="1390f-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="1390f-115">Færið inn eða veljið reikning í færslureitnum.</span><span class="sxs-lookup"><span data-stu-id="1390f-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="1390f-116">Þegar færsla hefur verið valin birtist viðskiptavinurinn sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="1390f-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="1390f-117">Færið inn greiðslutilvísun í greiðslutilvísunarreitnum.</span><span class="sxs-lookup"><span data-stu-id="1390f-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="1390f-118">Greiðslutilvísun gætu verið ávísunarnúmer viðskiptavinarins eða tilvísun úr rafræna greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="1390f-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="1390f-119">Aðeins er krafist greiðslutilvísunar ef merkt er við að greiðslan sé tekin með á innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="1390f-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="1390f-120">Veljið hvort greiðslu verður að höfð með á innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="1390f-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="1390f-121">Færa inn upphæð greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="1390f-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="1390f-122">Greiðsluupphæðin birtist ekki sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="1390f-122">The payment amount will not default.</span></span> <span data-ttu-id="1390f-123">Hana verður að slá inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="1390f-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="1390f-124">Merkið við reikningana sem voru greiddir af viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="1390f-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="1390f-125">Ef greiðslan er fyrirframgreiðsla er ekki nauðsynlegt að merkja neina reikninga fyrir uppgjör.</span><span class="sxs-lookup"><span data-stu-id="1390f-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="1390f-126">Samt sem áður er hægt að vista og bóka greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="1390f-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="1390f-127">Hægt er að gera upp reikninginn síðar.</span><span class="sxs-lookup"><span data-stu-id="1390f-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="1390f-128">Færið inn upphæð greiðslunnar sem á að jafna á merktan reikning.</span><span class="sxs-lookup"><span data-stu-id="1390f-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="1390f-129">Hægt er að nota þetta svæði þegar greiðslan er með hlutagreiðslu.</span><span class="sxs-lookup"><span data-stu-id="1390f-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="1390f-130">Ef engin upphæð er slegin inn verður uppgjörsupphæðin ákvörðuð sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="1390f-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="1390f-131">Smellið á „Vista“ í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="1390f-131">Click Save in journal.</span></span>
    * <span data-ttu-id="1390f-132">Ganga skal úr skugga um að mótlykill hafi verið skilgreindur áður en greiðslan er vistuð í færslubókina.</span><span class="sxs-lookup"><span data-stu-id="1390f-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="1390f-133">Með því að smella á „Vista í færslubók“ er greiðslan vistuð og færð í færslubókina.</span><span class="sxs-lookup"><span data-stu-id="1390f-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="1390f-134">Þá er hægt að halda áfram og færa inn næstu greiðslu.</span><span class="sxs-lookup"><span data-stu-id="1390f-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="1390f-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1390f-135">Close the page.</span></span>
14. <span data-ttu-id="1390f-136">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="1390f-136">Click Lines.</span></span>
    * <span data-ttu-id="1390f-137">Þegar „Línur“ eru opnaðar birtast allar greiðslur sem hafa verið færðar inn á síðunni „Færa inn greiðslur viðskiptavinar“ og vistaðar í færslubókina.</span><span class="sxs-lookup"><span data-stu-id="1390f-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="1390f-138">Síðuna er einnig hægt að nota til að slá inn nýjar greiðslur viðskiptavina eða breyta núverandi greiðslu viðskiptavinar áður en þær eru birtar.</span><span class="sxs-lookup"><span data-stu-id="1390f-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="1390f-139">Smellið á „Nýtt“ til að stofna aðra greiðslu.</span><span class="sxs-lookup"><span data-stu-id="1390f-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="1390f-140">Veldu viðskiptavin sem greiðsla var móttekin frá.</span><span class="sxs-lookup"><span data-stu-id="1390f-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="1390f-141">Ef notandinn veit ekki hver viðskiptavinurinn er en veit hvaða reikningur var greiddur með greiðslunni er hægt að nota reikningssvæðið til að velja reikninginn eða færa hann inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="1390f-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="1390f-142">Þegar reikningur hefur verið valinn birtist viðskiptavinurinn sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="1390f-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="1390f-143">Smellið á „Gera upp færslur“ til að merkja reikninga sem voru greiddir.</span><span class="sxs-lookup"><span data-stu-id="1390f-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="1390f-144">Ekki er nauðsynlegt að gera upp greiðslu fyrir neina reikninga.</span><span class="sxs-lookup"><span data-stu-id="1390f-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="1390f-145">Ef þetta er fyrirframgreiðsla eða ef ekki er ljóst hvaða reikningur var greiddur er hægt að slá inn greiðsluna og bóka hana.</span><span class="sxs-lookup"><span data-stu-id="1390f-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="1390f-146">Greiðsluna er hægt að gera upp fyrir reikning síðar.</span><span class="sxs-lookup"><span data-stu-id="1390f-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="1390f-147">Merkið við reikningana sem voru greiddir með greiðslunni.</span><span class="sxs-lookup"><span data-stu-id="1390f-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="1390f-148">Færið inn upphæð greiðslunnar sem á að jafna á reikning.</span><span class="sxs-lookup"><span data-stu-id="1390f-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="1390f-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1390f-149">Click OK.</span></span>
21. <span data-ttu-id="1390f-150">Færið inn greiðslutilvísun í greiðslutilvísunarreitnum.</span><span class="sxs-lookup"><span data-stu-id="1390f-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="1390f-151">.</span><span class="sxs-lookup"><span data-stu-id="1390f-151">.</span></span>
    * <span data-ttu-id="1390f-152">Aðeins er krafist greiðslutilvísunar ef merkt er við að greiðslan sé tekin með á innborgunarseðli.</span><span class="sxs-lookup"><span data-stu-id="1390f-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="1390f-153">Bókið greiðslur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="1390f-153">Post the customer payments.</span></span> 


