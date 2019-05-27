---
title: Stofna beingreiðsluumboð fyrir viðskiptavin
description: Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572536"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="5a05f-103">Stofna beingreiðsluumboð fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="5a05f-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a05f-104">Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.</span><span class="sxs-lookup"><span data-stu-id="5a05f-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="5a05f-105">Stofna skal bankareikning.</span><span class="sxs-lookup"><span data-stu-id="5a05f-105">Create a bank account</span></span>
1. <span data-ttu-id="5a05f-106">Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="5a05f-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="5a05f-107">Veljið til dæmis U.S. 001</span><span class="sxs-lookup"><span data-stu-id="5a05f-107">For example, select US-001</span></span>
3. <span data-ttu-id="5a05f-108">Í aðgerðasvæðinu er smellt á Viðskiptavinur.</span><span class="sxs-lookup"><span data-stu-id="5a05f-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="5a05f-109">Smellt er á bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="5a05f-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="5a05f-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-110">Click New.</span></span>
6. <span data-ttu-id="5a05f-111">Í reitinn Bankareikningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5a05f-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="5a05f-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5a05f-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="5a05f-113">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5a05f-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="5a05f-114">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5a05f-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="5a05f-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-115">Click Save.</span></span>
11. <span data-ttu-id="5a05f-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5a05f-116">Close the page.</span></span>
12. <span data-ttu-id="5a05f-117">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="5a05f-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="5a05f-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5a05f-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5a05f-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5a05f-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="5a05f-120">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-120">Click Edit.</span></span>
16. <span data-ttu-id="5a05f-121">Útvíkka aukakenni hluta.</span><span class="sxs-lookup"><span data-stu-id="5a05f-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="5a05f-122">Færa inn gildi í reitnum Kenni beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="5a05f-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="5a05f-123">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5a05f-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="5a05f-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5a05f-124">Close the page.</span></span>
20. <span data-ttu-id="5a05f-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5a05f-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="5a05f-126">Skilgreina rafrænu greiðsluaðferðina</span><span class="sxs-lookup"><span data-stu-id="5a05f-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="5a05f-127">Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="5a05f-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="5a05f-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-128">Click New.</span></span>
3. <span data-ttu-id="5a05f-129">Færa inn gildi í svæðinu greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="5a05f-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="5a05f-130">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5a05f-131">Greiðslugerð fyrir aðferð umboð fyrir beingreiðsla verður að vera Rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="5a05f-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="5a05f-132">Velja skal Já í svæðinu krefjast umboðs.</span><span class="sxs-lookup"><span data-stu-id="5a05f-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="5a05f-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5a05f-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="5a05f-134">Bæta umboð fyrir beingreiðsla við viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="5a05f-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="5a05f-135">Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="5a05f-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="5a05f-136">Veljið til dæmis U.S. 001</span><span class="sxs-lookup"><span data-stu-id="5a05f-136">For example, select US-001</span></span>
3. <span data-ttu-id="5a05f-137">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-137">Click Edit.</span></span>
4. <span data-ttu-id="5a05f-138">Útvíkka hlutann sjálfgildi Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="5a05f-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="5a05f-139">Færa inn eða velja gildi í reitnum greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="5a05f-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="5a05f-140">Útvíkka hlutann sjálfgildi Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="5a05f-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="5a05f-141">Útvíkka hlutann umboð fyrir beingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="5a05f-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="5a05f-142">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="5a05f-142">Click Add.</span></span>
9. <span data-ttu-id="5a05f-143">Færa inn eða veljið gildi í svæðinu bankareikning.</span><span class="sxs-lookup"><span data-stu-id="5a05f-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="5a05f-144">Sláið inn eða veldu gildi í reitnum Bankareikningur Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="5a05f-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="5a05f-145">Færið inn fjölda greiðslna sem búist er við fyrir þetta umboð.</span><span class="sxs-lookup"><span data-stu-id="5a05f-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="5a05f-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-146">Click OK.</span></span>
13. <span data-ttu-id="5a05f-147">Smelltu á Prenta.</span><span class="sxs-lookup"><span data-stu-id="5a05f-147">Click Print.</span></span>
14. <span data-ttu-id="5a05f-148">Smellt er á umboðsskýrsla.</span><span class="sxs-lookup"><span data-stu-id="5a05f-148">Click Mandate report.</span></span>
15. <span data-ttu-id="5a05f-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5a05f-149">Close the page.</span></span>
16. <span data-ttu-id="5a05f-150">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-150">Click Edit.</span></span>
17. <span data-ttu-id="5a05f-151">Færðu inn dagsetningu í svæðinu dagsetning undirskriftar</span><span class="sxs-lookup"><span data-stu-id="5a05f-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="5a05f-152">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="5a05f-152">Click Yes.</span></span>
19. <span data-ttu-id="5a05f-153">Færðu inn Staðurinn þar sem umboðið var undirritað</span><span class="sxs-lookup"><span data-stu-id="5a05f-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="5a05f-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-154">Click OK.</span></span>
21. <span data-ttu-id="5a05f-155">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5a05f-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="5a05f-156">Stofna reikningur með frjálsum texta með umboði</span><span class="sxs-lookup"><span data-stu-id="5a05f-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="5a05f-157">Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="5a05f-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="5a05f-158">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5a05f-158">Click New.</span></span>
3. <span data-ttu-id="5a05f-159">Veljið þann viðskiptavin sem umboðið var bætt við.</span><span class="sxs-lookup"><span data-stu-id="5a05f-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="5a05f-160">Færa inn eða velja gildi í reitnum Kenni beingreiðsluumboðs.</span><span class="sxs-lookup"><span data-stu-id="5a05f-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

