---
title: Setja upp viðskiptavini bankareikninga viðskiptavina fyrir ISO20022-beingreiðslur
description: Þetta verk fer í gegnum uppsetningu á bankareikning viðskiptavinar og í umboð viðskiptavinar fyrir beingreiðsla sem eru nauðsynlegar til að mynda greiðsluskrá fyrir viðskiptavin eins og ISO20022-beingreiðslu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85c1faebe9a61ad2e708ba26c7a5f0cad15f5f8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988202"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="afc6e-103">Setja upp viðskiptavini bankareikninga viðskiptavina fyrir ISO20022-beingreiðslur</span><span class="sxs-lookup"><span data-stu-id="afc6e-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="afc6e-104">Þetta verk fer í gegnum uppsetningu á bankareikning viðskiptavinar og í umboð viðskiptavinar fyrir beingreiðsla sem eru nauðsynlegar til að mynda greiðsluskrá fyrir viðskiptavin eins og ISO20022-beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="afc6e-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="afc6e-105">Eftir því hvaða greiðslusnið viðskiptavar er sett upp gæti verið krafist viðbótarupplýsinga, sem ekki er fjallað um í þessu ferli, vegna viðskiptavinar eða bankareikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="afc6e-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="afc6e-106">Þetta verkefni var stofnuð með fyrirtækis sýnigögnum DEMF með aðalaðsetur lögaðila í Þýskalandi.</span><span class="sxs-lookup"><span data-stu-id="afc6e-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="afc6e-107">Þetta er fjórða af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="afc6e-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="afc6e-108">Uppsetning bankareikningur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="afc6e-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="afc6e-109">Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="afc6e-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="afc6e-110">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="afc6e-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="afc6e-111">Til dæmis, sía svæðið með gildið 'DE-010'.</span><span class="sxs-lookup"><span data-stu-id="afc6e-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="afc6e-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="afc6e-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="afc6e-113">Í aðgerðasvæðinu er smellt á Viðskiptavinur.</span><span class="sxs-lookup"><span data-stu-id="afc6e-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="afc6e-114">Smellt er á bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="afc6e-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="afc6e-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="afc6e-115">Click New.</span></span>
7. <span data-ttu-id="afc6e-116">Í reitinn Bankareikningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="afc6e-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="afc6e-117">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="afc6e-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="afc6e-118">Til dæmis má færa inn 'EUR bank'.</span><span class="sxs-lookup"><span data-stu-id="afc6e-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="afc6e-119">Færa inn eða veljið gildi í svæðinu bankaflokkur.</span><span class="sxs-lookup"><span data-stu-id="afc6e-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="afc6e-120">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="afc6e-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="afc6e-121">Til dæmis færðu inn 'DE36200400000628808808'.</span><span class="sxs-lookup"><span data-stu-id="afc6e-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="afc6e-122">Í svæðinu SWIFT-kóði færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="afc6e-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="afc6e-123">Til dæmis færðu inn 'COBADEFFXXX'.</span><span class="sxs-lookup"><span data-stu-id="afc6e-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="afc6e-124">Vinsamlegast Athugið að SWIFT\BIC er ekki krafist fyrir margar greiðslusnið hins vegar er mælt með að slíkt sé skráð fyrir bankareikning.</span><span class="sxs-lookup"><span data-stu-id="afc6e-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="afc6e-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="afc6e-125">Click Save.</span></span>
13. <span data-ttu-id="afc6e-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="afc6e-126">Close the page.</span></span>
14. <span data-ttu-id="afc6e-127">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="afc6e-127">Click Edit.</span></span>
15. <span data-ttu-id="afc6e-128">Útvíkka hlutann sjálfgildi Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="afc6e-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="afc6e-129">Færa inn eða veljið gildi í svæðinu bankareikning.</span><span class="sxs-lookup"><span data-stu-id="afc6e-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="afc6e-130">Bæta við umboði fyrir beingreiðslu</span><span class="sxs-lookup"><span data-stu-id="afc6e-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="afc6e-131">Útvíkka hlutann umboð fyrir beingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="afc6e-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="afc6e-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="afc6e-132">Click Add.</span></span>
3. <span data-ttu-id="afc6e-133">Sláið inn eða veldu gildi í reitnum Bankareikningur Lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="afc6e-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="afc6e-134">Veljið til dæmis DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="afc6e-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="afc6e-135">Færðu inn dagsetningu í svæðinu dagsetning undirskriftar</span><span class="sxs-lookup"><span data-stu-id="afc6e-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="afc6e-136">Smellt er á Já til að staðfesta uppfærslu dagsetningar .</span><span class="sxs-lookup"><span data-stu-id="afc6e-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="afc6e-137">Sláðu inn eða veldu gildi reitnum Í staðsetning undirskriftar.</span><span class="sxs-lookup"><span data-stu-id="afc6e-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="afc6e-138">Í Áætlað fjölda greiðslur svæðinu, færið inn tölu.</span><span class="sxs-lookup"><span data-stu-id="afc6e-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="afc6e-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="afc6e-139">Click OK.</span></span>
9. <span data-ttu-id="afc6e-140">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="afc6e-140">Click Save.</span></span>

