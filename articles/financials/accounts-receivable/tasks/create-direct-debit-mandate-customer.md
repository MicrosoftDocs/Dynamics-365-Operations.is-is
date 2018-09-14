--- 
title: "Stofna beingreiðsluumboð fyrir viðskiptavin"
description: "Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="da6af-103">Stofna beingreiðsluumboð fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="da6af-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da6af-104">Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.</span><span class="sxs-lookup"><span data-stu-id="da6af-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="da6af-105">Stofna skal bankareikning.</span><span class="sxs-lookup"><span data-stu-id="da6af-105">Create a bank account</span></span>
1. <span data-ttu-id="da6af-106">Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="da6af-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="da6af-107">Veljið til dæmis U.S. 001</span><span class="sxs-lookup"><span data-stu-id="da6af-107">For example, select US-001</span></span>
3. <span data-ttu-id="da6af-108">Í aðgerðasvæðinu er smellt á Viðskiptavinur.</span><span class="sxs-lookup"><span data-stu-id="da6af-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="da6af-109">Smellt er á bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="da6af-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="da6af-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="da6af-110">Click New.</span></span>
6. <span data-ttu-id="da6af-111">Í reitinn Bankareikningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da6af-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="da6af-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da6af-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="da6af-113">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da6af-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="da6af-114">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da6af-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="da6af-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="da6af-115">Click Save.</span></span>
11. <span data-ttu-id="da6af-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da6af-116">Close the page.</span></span>
12. <span data-ttu-id="da6af-117">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="da6af-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="da6af-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="da6af-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="da6af-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="da6af-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="da6af-120">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="da6af-120">Click Edit.</span></span>
16. <span data-ttu-id="da6af-121">Útvíkka aukakenni hluta.</span><span class="sxs-lookup"><span data-stu-id="da6af-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="da6af-122">Færa inn gildi í reitnum Kenni beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="da6af-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="da6af-123">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da6af-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="da6af-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da6af-124">Close the page.</span></span>
20. <span data-ttu-id="da6af-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da6af-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="da6af-126">Skilgreina rafrænu greiðsluaðferðina</span><span class="sxs-lookup"><span data-stu-id="da6af-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="da6af-127">Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="da6af-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="da6af-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="da6af-128">Click New.</span></span>
3. <span data-ttu-id="da6af-129">Færa inn gildi í svæðinu greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="da6af-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="da6af-130">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="da6af-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="da6af-131">Greiðslugerð fyrir aðferð umboð fyrir beingreiðsla verður að vera Rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="da6af-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="da6af-132">Velja skal Já í svæðinu krefjast umboðs.</span><span class="sxs-lookup"><span data-stu-id="da6af-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="da6af-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da6af-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="da6af-134">Bæta umboð fyrir beingreiðsla við viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="da6af-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="da6af-135">Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="da6af-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="da6af-136">Veljið til dæmis U.S. 001</span><span class="sxs-lookup"><span data-stu-id="da6af-136">For example, select US-001</span></span>
3. <span data-ttu-id="da6af-137">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="da6af-137">Click Edit.</span></span>
4. <span data-ttu-id="da6af-138">Útvíkka hlutann sjálfgildi Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="da6af-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="da6af-139">Færa inn eða velja gildi í reitnum greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="da6af-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="da6af-140">Útvíkka hlutann sjálfgildi Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="da6af-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="da6af-141">Útvíkka hlutann umboð fyrir beingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="da6af-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="da6af-142">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="da6af-142">Click Add.</span></span>
9. <span data-ttu-id="da6af-143">Færa inn eða veljið gildi í svæðinu bankareikning.</span><span class="sxs-lookup"><span data-stu-id="da6af-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="da6af-144">Sláið inn eða veldu gildi í reitnum Bankareikningur Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="da6af-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="da6af-145">Færið inn fjölda greiðslna sem búist er við fyrir þetta umboð.</span><span class="sxs-lookup"><span data-stu-id="da6af-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="da6af-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="da6af-146">Click OK.</span></span>
13. <span data-ttu-id="da6af-147">Smelltu á Prenta.</span><span class="sxs-lookup"><span data-stu-id="da6af-147">Click Print.</span></span>
14. <span data-ttu-id="da6af-148">Smellt er á umboðsskýrsla.</span><span class="sxs-lookup"><span data-stu-id="da6af-148">Click Mandate report.</span></span>
15. <span data-ttu-id="da6af-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da6af-149">Close the page.</span></span>
16. <span data-ttu-id="da6af-150">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="da6af-150">Click Edit.</span></span>
17. <span data-ttu-id="da6af-151">Færðu inn dagsetningu í svæðinu dagsetning undirskriftar</span><span class="sxs-lookup"><span data-stu-id="da6af-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="da6af-152">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="da6af-152">Click Yes.</span></span>
19. <span data-ttu-id="da6af-153">Færðu inn Staðurinn þar sem umboðið var undirritað</span><span class="sxs-lookup"><span data-stu-id="da6af-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="da6af-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="da6af-154">Click OK.</span></span>
21. <span data-ttu-id="da6af-155">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da6af-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="da6af-156">Stofna reikningur með frjálsum texta með umboði</span><span class="sxs-lookup"><span data-stu-id="da6af-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="da6af-157">Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="da6af-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="da6af-158">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="da6af-158">Click New.</span></span>
3. <span data-ttu-id="da6af-159">Veljið þann viðskiptavin sem umboðið var bætt við.</span><span class="sxs-lookup"><span data-stu-id="da6af-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="da6af-160">Færa inn eða velja gildi í reitnum Kenni beingreiðsluumboðs.</span><span class="sxs-lookup"><span data-stu-id="da6af-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


