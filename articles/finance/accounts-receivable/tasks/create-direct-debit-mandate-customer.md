---
title: Stofna beingreiðsluumboð fyrir viðskiptavin
description: Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178328"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="be037-103">Stofna beingreiðsluumboð fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="be037-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be037-104">Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.</span><span class="sxs-lookup"><span data-stu-id="be037-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="be037-105">Stofna skal bankareikning.</span><span class="sxs-lookup"><span data-stu-id="be037-105">Create a bank account</span></span>
1. <span data-ttu-id="be037-106">Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="be037-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="be037-107">Í listanum velurðu skrá.</span><span class="sxs-lookup"><span data-stu-id="be037-107">In the list, select a record.</span></span> <span data-ttu-id="be037-108">Veljið til dæmis U.S. 001</span><span class="sxs-lookup"><span data-stu-id="be037-108">For example, select US-001</span></span>
3. <span data-ttu-id="be037-109">Í aðgerðasvæðinu er smellt á **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="be037-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="be037-110">Smelltu á **Bankareikninga**.</span><span class="sxs-lookup"><span data-stu-id="be037-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="be037-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="be037-111">Click **New**.</span></span>
6. <span data-ttu-id="be037-112">Í reitinn **Bankareikningar** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="be037-113">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="be037-114">Í reitinn **IBAN** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="be037-115">Í reitinn **Gjaldmiðill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="be037-116">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="be037-116">Click **Save**.</span></span>
11. <span data-ttu-id="be037-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="be037-117">Close the page.</span></span>
12. <span data-ttu-id="be037-118">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="be037-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="be037-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="be037-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="be037-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="be037-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="be037-121">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="be037-121">Click **Edit**.</span></span>
16. <span data-ttu-id="be037-122">Útvíkkaðu flýtiflipann **Aukakenni**.</span><span class="sxs-lookup"><span data-stu-id="be037-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="be037-123">Í reitinn **Beingreiðslukenni** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="be037-124">Í reitinn **IBAN** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="be037-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="be037-125">Close the page.</span></span>
20. <span data-ttu-id="be037-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="be037-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="be037-127">Skilgreina rafrænu greiðsluaðferðina</span><span class="sxs-lookup"><span data-stu-id="be037-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="be037-128">Í **skoðunarrúðunni** ferðu í **Kerfi > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir**.</span><span class="sxs-lookup"><span data-stu-id="be037-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="be037-129">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="be037-129">Click **New**.</span></span>
3. <span data-ttu-id="be037-130">Í reitinn **Greiðsluháttur** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="be037-131">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="be037-132">Í reitinn **Greiðslugerð** skal velja „Rafræna greiðslu“.</span><span class="sxs-lookup"><span data-stu-id="be037-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="be037-133">Greiðslugerð fyrir aðferð umboð fyrir beingreiðsla verður að vera Rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="be037-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="be037-134">Veldu já í reitnum **Krefjast umboðs**.</span><span class="sxs-lookup"><span data-stu-id="be037-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="be037-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="be037-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="be037-136">Bæta umboð fyrir beingreiðsla við viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="be037-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="be037-137">Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="be037-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="be037-138">Í listanum velurðu skrá.</span><span class="sxs-lookup"><span data-stu-id="be037-138">In the list, select a record.</span></span> <span data-ttu-id="be037-139">Veljið til dæmis U.S. 001</span><span class="sxs-lookup"><span data-stu-id="be037-139">For example, select US-001</span></span>
3. <span data-ttu-id="be037-140">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="be037-140">Click **Edit**.</span></span>
4. <span data-ttu-id="be037-141">Útvíkkaðu flýtiflipann **Sjálfgildi greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="be037-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="be037-142">Færa inn eða velja gildi í reitnum **Greiðsluaðferð**.</span><span class="sxs-lookup"><span data-stu-id="be037-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="be037-143">Útvíkkaðu flýtiflipann **Sjálfgildi greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="be037-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="be037-144">Útvíkkaðu flýtiflipann **Umboð fyrir beingreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="be037-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="be037-145">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="be037-145">Click **Add**.</span></span>
9. <span data-ttu-id="be037-146">Færa inn eða veljið gildi í svæðinu **Bankareikningur**.</span><span class="sxs-lookup"><span data-stu-id="be037-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="be037-147">Í reitinn **Bankareikningur lánardrottins** skal rita eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="be037-148">Í reitinn **Greiðslutíðni** skal færa inn fjölda greiðslna sem búist er við fyrir þetta umboð.</span><span class="sxs-lookup"><span data-stu-id="be037-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="be037-149">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="be037-149">Click **OK**.</span></span>
13. <span data-ttu-id="be037-150">Smelltu á **Prenta**.</span><span class="sxs-lookup"><span data-stu-id="be037-150">Click **Print**.</span></span>
14. <span data-ttu-id="be037-151">Smellt er á **Umboðsskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="be037-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="be037-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="be037-152">Close the page.</span></span>
16. <span data-ttu-id="be037-153">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="be037-153">Click **Edit**.</span></span>
17. <span data-ttu-id="be037-154">Í reitinn **Dagsetning undirskriftar** skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="be037-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="be037-155">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="be037-155">Click **Yes**.</span></span>
19. <span data-ttu-id="be037-156">Færðu inn Staðurinn þar sem umboðið var undirritað</span><span class="sxs-lookup"><span data-stu-id="be037-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="be037-157">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="be037-157">Click **OK**.</span></span>
21. <span data-ttu-id="be037-158">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="be037-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="be037-159">Stofna reikningur með frjálsum texta með umboði</span><span class="sxs-lookup"><span data-stu-id="be037-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="be037-160">Í **skoðunarrúðunni** ferðu í **Einingar > Viðskiptakröfur > Reikningar > Allir frjálsir textareikningar**.</span><span class="sxs-lookup"><span data-stu-id="be037-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="be037-161">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="be037-161">Click **New**.</span></span>
3. <span data-ttu-id="be037-162">Veljið þann viðskiptavin sem umboðið var bætt við.</span><span class="sxs-lookup"><span data-stu-id="be037-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="be037-163">Í reitinn **Kenni beingreiðsluumboðs** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="be037-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>
