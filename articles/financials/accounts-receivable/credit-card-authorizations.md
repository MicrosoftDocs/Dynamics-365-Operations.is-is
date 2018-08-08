---
title: "Uppsetningar á kreditkorti, heimild og sækja"
description: "Þessi grein veitir yfirlit yfir kreditkortaheimild í Microsoft Dynamics 365 for Finance and Operations. Þar á meðal eru upplýsingar um hvernig á að setja upp greiðsluþjónustu, bæta kreditkorti við sölupöntun, og ógilda heimild."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5a950a100fd5e9026300ea08eb1a6311a8e63129
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="1b497-104">Uppsetningar á kreditkorti, heimild og sækja</span><span class="sxs-lookup"><span data-stu-id="1b497-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="1b497-105">Þessi grein veitir yfirlit yfir kreditkortaheimild í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b497-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1b497-106">Þar á meðal eru upplýsingar um hvernig á að setja upp greiðsluþjónustu, bæta kreditkorti við sölupöntun, og ógilda heimild.</span><span class="sxs-lookup"><span data-stu-id="1b497-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="1b497-107">Setja upp greiðsluþjónustu kreditkorts</span><span class="sxs-lookup"><span data-stu-id="1b497-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="1b497-108">Til að nota kreditkort, verður að setja upp og virkja greiðsluþjónustu á síðunni greiðsluþjónusta.</span><span class="sxs-lookup"><span data-stu-id="1b497-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="1b497-109">Greiðsluþjónustu virkar eins og brú á milli lögaðila lögaðila þíns og bankans sem vinnur kreditkortagjöld viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="1b497-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="1b497-110">Þú Þarft að vinna með kreditkortaveitu sem er talin upp í svæðinu greiðslutengill og setja upp lykil hjá þessari veitu.</span><span class="sxs-lookup"><span data-stu-id="1b497-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="1b497-111">Svo er verður að setja upp aðra valkosti á síðunni greiðsluþjónusta, setja upp greiðslukortagerðir fyrir American Express, Discover, MasterCard og Discover á síðunni gerðir kreditkorts og virkja veitu sem sjálfgefna veitu.</span><span class="sxs-lookup"><span data-stu-id="1b497-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="1b497-112">Einnig verður að fylgja þessum skrefum til að ljúka uppsetningu:</span><span class="sxs-lookup"><span data-stu-id="1b497-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="1b497-113">Tilgreina færibreytur fyrir notkun kreditkortaheimilda á síðunni færibreytur viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="1b497-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="1b497-114">Greiðsluskilmálar fyrir kreditkort eru settir upp á síðunni Greiðsluskilmálar.</span><span class="sxs-lookup"><span data-stu-id="1b497-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="1b497-115">Í svæðinu  greiðslugerð er valin kreditkort.</span><span class="sxs-lookup"><span data-stu-id="1b497-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="1b497-116">Á síðunni kreditkort viðskiptavinar, sjak  Færa inn kreditkortaupplýsingar viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="1b497-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="1b497-117">Bæta við nýju kreditkorti</span><span class="sxs-lookup"><span data-stu-id="1b497-117">Adding a new credit card</span></span>
<span data-ttu-id="1b497-118">Hægt er að stofna nýjar kreditkortafærslur á síðunni Viðskiptavinir með því að nota Viðskiptavinur, Setja upp, kreditkort.</span><span class="sxs-lookup"><span data-stu-id="1b497-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="1b497-119">Einnig er hægt að stofna kreditkortafærslur þegar sölupantanir eru færðar inn á síðunni Vsk, með því að nota Stjórna, Viðskiptavinur, kreditkort, Afgreiðslukassi.</span><span class="sxs-lookup"><span data-stu-id="1b497-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>
<span data-ttu-id="1b497-120">Kreditkorti bætt við sölupöntun</span><span class="sxs-lookup"><span data-stu-id="1b497-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="1b497-121">Hægt er að bæta kreditkort við sölupöntun með því að velja greiðslukort í uppflettingu kreditkorta í Verð og afslátt flýtiflipa á síðunni Vsk.</span><span class="sxs-lookup"><span data-stu-id="1b497-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="1b497-122">Til að hefja heimildarferlið, á aðgerðarúðunni, á flipanum Stjórna, veljið kreditkort og heimila.</span><span class="sxs-lookup"><span data-stu-id="1b497-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>
<span data-ttu-id="1b497-123">Heimila kreditkort</span><span class="sxs-lookup"><span data-stu-id="1b497-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="1b497-124">Þegar kreditkort er gefin heimild, er kortanúmerið og nafn handhafa  sannvottuð og tiltæk lánsheimild staðfest.</span><span class="sxs-lookup"><span data-stu-id="1b497-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="1b497-125">Valkvætt er að staðfesta aðsetur og CVV-númer í korthafa.</span><span class="sxs-lookup"><span data-stu-id="1b497-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="1b497-126">Tiltæk Lánsheimild viðskiptavinar er síðan minnkuð sem nemur reikningnum..</span><span class="sxs-lookup"><span data-stu-id="1b497-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="1b497-127">Greiðsluþjónusta sendir upplýsingar um að kreditkortið hefur verið samþykkt eða hafnað.</span><span class="sxs-lookup"><span data-stu-id="1b497-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="1b497-128">Þegar sölupöntun er reikningsfærð, er kreditkortið rukkað (sótt) um upphæð reikningsins.</span><span class="sxs-lookup"><span data-stu-id="1b497-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="1b497-129">Sannprófunargildi korts</span><span class="sxs-lookup"><span data-stu-id="1b497-129">Card verification value</span></span>

<span data-ttu-id="1b497-130">Hægt er að krefjast CVV-númers, sem er stundum er kallað öryggisnúmer korts.</span><span class="sxs-lookup"><span data-stu-id="1b497-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="1b497-131">Þetta er fjögurra stafa gildi fyrir American Express.</span><span class="sxs-lookup"><span data-stu-id="1b497-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="1b497-132">Fyrir Discover, MasterCard og Visa, er gildið þriggja stafa.</span><span class="sxs-lookup"><span data-stu-id="1b497-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="1b497-133">Staðfesting aðseturs</span><span class="sxs-lookup"><span data-stu-id="1b497-133">Address verification</span></span>

<span data-ttu-id="1b497-134">Sannprófun aðsetursupplýsinga er alltaf sent í greiðsluþjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="1b497-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="1b497-135">Hægt er að velja hversu mikils af upplýsingum er krafist til að færsla sé samþykkt.</span><span class="sxs-lookup"><span data-stu-id="1b497-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="1b497-136">Gætið þess að hafa samband við veitu til að ákvarða hvort hún samþykkir þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1b497-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="1b497-137">Hér eru valkostir aðseturssannvottunar:</span><span class="sxs-lookup"><span data-stu-id="1b497-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="1b497-138">**Alltaf samþykkja færslu** – Samþykkja færsluna, án tillits til niðurstaða aðsetursstaðfestingar.</span><span class="sxs-lookup"><span data-stu-id="1b497-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="1b497-139">**Handhafi lykils** – bera Saman nafn korthafa í færslunni við upplýsingar um kreditkort hjá fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="1b497-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="1b497-140">**Innheimtuaðsetur** – bera Saman nafn korthafa og innheimtuaðsetur færslunnar við upplýsingum um kreditkort hjá fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="1b497-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="1b497-141">**Innheimtupóstnúmer** – bera Saman nafn korthafa og innheimtuaðsetur og póstnúmer færslunnar við upplýsingum um kreditkort hjá fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="1b497-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="1b497-142">Gagnastuðningur</span><span class="sxs-lookup"><span data-stu-id="1b497-142">Data support</span></span>
<span data-ttu-id="1b497-143">Fyrir hverja tegund kreditkorts sem er studd, er hægt að tilgreina í gagnastuðningsstig.</span><span class="sxs-lookup"><span data-stu-id="1b497-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="1b497-144">Stigið stýrir hversu mikið af upplýsingum um færslu er flutt í greiðsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="1b497-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="1b497-145">Gætið þess að hafa samband við veitu til að ákvarða hvort hún geti veitt þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1b497-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="1b497-146">Hér eru valkostir fyrir gagnastuðningsstig:</span><span class="sxs-lookup"><span data-stu-id="1b497-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="1b497-147">**Stig 1** - flytja færsludagsetningu, færsluupphæð og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="1b497-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="1b497-148">**Stig 2** flytja upplýsingar um Stig 1 og einnig aðsetur sendingar- og söluaðila, og skattaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1b497-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="1b497-149">**Stig 3** flytja yfir allar upplýsingar um Stig 2, auk upplýsingar pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="1b497-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="1b497-150">Hlutagreiðslur</span><span class="sxs-lookup"><span data-stu-id="1b497-150">Partial payments</span></span>
<span data-ttu-id="1b497-151">Ef þú flytur hluta af pöntun, er magn af hlutapöntun sótt , og heimildin, sem var fyrir upphæð allrar pöntunarinnar, er lokað.</span><span class="sxs-lookup"><span data-stu-id="1b497-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="1b497-152">Ný heimild er þá send inn fyrir eftirstandandi fjárhæð pöntunar sem ekki hefur verið send.</span><span class="sxs-lookup"><span data-stu-id="1b497-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="1b497-153">Ógilda heimild</span><span class="sxs-lookup"><span data-stu-id="1b497-153">Voiding an authorization</span></span>
<span data-ttu-id="1b497-154">Til að ógilda heimild fyrir kreditkort, er hægt að breyta greiðsluhætti í annan greiðslumáta sem ekki hefur tegund kreditkorts.</span><span class="sxs-lookup"><span data-stu-id="1b497-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>






