---
title: Skilgreina greiðsluþóknanir lánardrottna
description: Setja upp greiðsluþóknun lánardrottins
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9e723ec54b6f34082c422ce4c8e48bf52d2e3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189454"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="9e780-103">Skilgreina greiðsluþóknanir lánardrottna</span><span class="sxs-lookup"><span data-stu-id="9e780-103">Define vendor payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e780-104">Setja upp greiðsluþóknun lánardrottins</span><span class="sxs-lookup"><span data-stu-id="9e780-104">Set up vendor payment fees.</span></span> <span data-ttu-id="9e780-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="9e780-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9e780-106">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluþóknun.</span><span class="sxs-lookup"><span data-stu-id="9e780-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="9e780-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e780-107">Click New.</span></span>
3. <span data-ttu-id="9e780-108">Færa inn gildi í reitnum Kenni greiðsla .</span><span class="sxs-lookup"><span data-stu-id="9e780-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="9e780-109">Kenni Þóknunar ætti að lýsa hvenær gjaldi verður notað eins og "EFT_Fee".</span><span class="sxs-lookup"><span data-stu-id="9e780-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="9e780-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9e780-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9e780-111">Færa inn gildi í lýsingarsvæðinu Þóknunar.</span><span class="sxs-lookup"><span data-stu-id="9e780-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="9e780-112">Bæta við lýsingu til að veita frekari upplýsingar um þegar þóknunin er metin.</span><span class="sxs-lookup"><span data-stu-id="9e780-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="9e780-113">Velja Lánardrottna eða Fjárhagslykla í svæðinu Gjalda.</span><span class="sxs-lookup"><span data-stu-id="9e780-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="9e780-114">Fjárhagur er notaður þegar þóknunar gjaldfærðar í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="9e780-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="9e780-115">Lánardrottinn er notaður þegar þóknunin verður metin til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="9e780-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="9e780-116">Færið inn aðallykil fyrir þar sem þóknunin verður kostnaðarfært.</span><span class="sxs-lookup"><span data-stu-id="9e780-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="9e780-117">Þessi valkostur er aðeins tiltækur þegar valinn er Fjárhag sem valkostur Gjalda.</span><span class="sxs-lookup"><span data-stu-id="9e780-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="9e780-118">Velja færslubók sem nota má þessa þóknun.</span><span class="sxs-lookup"><span data-stu-id="9e780-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="9e780-119">Fyrir Greiðsluþóknun lánardrottins, mundirðu velja færslubók 'Lánardrottinsgreiðsluna'.</span><span class="sxs-lookup"><span data-stu-id="9e780-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="9e780-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e780-120">Click Save.</span></span>
10. <span data-ttu-id="9e780-121">Smellt er á uppsetning Greiðsluþóknunar.</span><span class="sxs-lookup"><span data-stu-id="9e780-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="9e780-122">Halda áfram greiðsluþóknunaruppsetning til að skilgreina hvenær þóknun verði sjálfgefið á færslubókar sem er valin.</span><span class="sxs-lookup"><span data-stu-id="9e780-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="9e780-123">Veljið annað hvort Töflu, Flokk eða Allt.</span><span class="sxs-lookup"><span data-stu-id="9e780-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="9e780-124">Tafla er notuð til að velja einn bankareikning Flokkurinn er notaður til að velja bankaflokk og Allt er til að nota þessa uppsetningu þóknunar fyrir alla bankareikninga</span><span class="sxs-lookup"><span data-stu-id="9e780-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="9e780-125">Veljið bankaflokk eða bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="9e780-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="9e780-126">Uppfletting sýna bankaflokk ef valinn var Flokkur, og sýna bankareikninga ef Tafla var valin.</span><span class="sxs-lookup"><span data-stu-id="9e780-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="9e780-127">Velja Greiðsluhátt sem verður metið þessu gjaldi.</span><span class="sxs-lookup"><span data-stu-id="9e780-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="9e780-128">Velja greiðsluupplýsingar til að nota fyrir valinn greiðsluháttinn.</span><span class="sxs-lookup"><span data-stu-id="9e780-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="9e780-129">Greiðsluupplýsingar er notaður við rafræna sjóður greiðsluhættir flutning.</span><span class="sxs-lookup"><span data-stu-id="9e780-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="9e780-130">Velja hvort gjaldið er prósentu, upphæð eða bili.</span><span class="sxs-lookup"><span data-stu-id="9e780-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="9e780-131">Færa inn prósentu eða upphæð þóknunar.</span><span class="sxs-lookup"><span data-stu-id="9e780-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="9e780-132">Færa inn prósentu ef Þóknunin er prósenta.</span><span class="sxs-lookup"><span data-stu-id="9e780-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="9e780-133">Ef Gjaldið er upphæð, færið inn upphæð þóknunar.</span><span class="sxs-lookup"><span data-stu-id="9e780-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="9e780-134">Notið flipann Bil til að skilgreina lagskipt gjöld ef Þóknunin er millibili.</span><span class="sxs-lookup"><span data-stu-id="9e780-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="9e780-135">Í gjaldmiðill Þóknunar, veljið þann gjaldmiðil sem þóknunin verður metin.</span><span class="sxs-lookup"><span data-stu-id="9e780-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="9e780-136">Þessi gjaldmiðill er fyrir þóknun.</span><span class="sxs-lookup"><span data-stu-id="9e780-136">This currency is for the fee.</span></span> <span data-ttu-id="9e780-137">Greiðslugjaldmiðli er notuð til að skilgreina hvenær þóknun regluna ætti að vera metin á grundvelli gjaldmiðli greiðslu.</span><span class="sxs-lookup"><span data-stu-id="9e780-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="9e780-138">Til dæmis bankanum gæti gjaldfærð þóknun þegar greiðsla er gerð í EUR, en aðrar greiðslur ekki eru metnar fyrir þóknun.</span><span class="sxs-lookup"><span data-stu-id="9e780-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="9e780-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e780-139">Click Save.</span></span>

