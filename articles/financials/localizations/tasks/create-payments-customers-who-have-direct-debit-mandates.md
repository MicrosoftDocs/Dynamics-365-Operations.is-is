--- 
title: "Stofna greiðslur fyrir viðskiptavin sem hefur beingreiðsluumboð"
description: "Þetta verk fer í gegnum hvernig á að mynda ISO20022-beingreiðsluskrá fyrir viðskiptavin sem hefur skilgreint beingreiðslu og reikning til greiðslu."
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6e1f6fea560db0e1f96123040f80e79f5fe80886
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="d30a1-103">Stofna greiðslur fyrir viðskiptavin sem hefur beingreiðsluumboð</span><span class="sxs-lookup"><span data-stu-id="d30a1-103">Create payments for a customer who have direct debit mandates</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d30a1-104">Þetta verk fer í gegnum hvernig á að mynda ISO20022-beingreiðsluskrá fyrir viðskiptavin sem hefur skilgreint beingreiðslu og reikning til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="d30a1-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="d30a1-105">Stofna og bóka reikning er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="d30a1-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="d30a1-106">Í stað þess að láta borga reikning geturðu valið umboð í færslubók áður en mynduð er greiðsluskrá, til að styðja við aðstæður fyrirframgreiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d30a1-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="d30a1-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="d30a1-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="d30a1-108">Þetta er fimmta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d30a1-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d30a1-109">Áður en hægt er að ljúka þessu verki, verður að klárað fyrri verkefni.</span><span class="sxs-lookup"><span data-stu-id="d30a1-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="d30a1-110">Fyrst þarf að flytja inn skilgreiningar rafænnar skýrslugerðar fyrir greiðsla viðskiptavinar, að skilgreina greiðsluhátt fyrir greiðslur og setja upp þínar fyrirtækis og viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d30a1-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="d30a1-111">Bóka reikningur með frjálsum texta með upplýsingum fyrir beingreiðsla</span><span class="sxs-lookup"><span data-stu-id="d30a1-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="d30a1-112">Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="d30a1-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="d30a1-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-113">Click New.</span></span>
3. <span data-ttu-id="d30a1-114">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d30a1-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="d30a1-115">Þú getur til dæmis valið DE-010.</span><span class="sxs-lookup"><span data-stu-id="d30a1-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="d30a1-116">Færa inn eða velja gildi í reitnum greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="d30a1-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="d30a1-117">Til dæmis:</span><span class="sxs-lookup"><span data-stu-id="d30a1-117">For example.</span></span> <span data-ttu-id="d30a1-118">velja Rafræna.</span><span class="sxs-lookup"><span data-stu-id="d30a1-118">select Electronic.</span></span>  
5. <span data-ttu-id="d30a1-119">Færa inn eða velja gildi í reitnum Kenni beingreiðsluumboðs.</span><span class="sxs-lookup"><span data-stu-id="d30a1-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="d30a1-120">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="d30a1-120">Click Add line.</span></span>
7. <span data-ttu-id="d30a1-121">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d30a1-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="d30a1-122">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d30a1-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="d30a1-123">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="d30a1-124">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-124">Click Post.</span></span>
11. <span data-ttu-id="d30a1-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="d30a1-126">Stofna greiðsla</span><span class="sxs-lookup"><span data-stu-id="d30a1-126">Create a payment</span></span>
1. <span data-ttu-id="d30a1-127">Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="d30a1-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="d30a1-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-128">Click New.</span></span>
3. <span data-ttu-id="d30a1-129">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="d30a1-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="d30a1-130">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-130">Click Lines.</span></span>
5. <span data-ttu-id="d30a1-131">Smellt er á Greiðslutillögur</span><span class="sxs-lookup"><span data-stu-id="d30a1-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="d30a1-132">Smellt er á Stofna greiðslutillögu</span><span class="sxs-lookup"><span data-stu-id="d30a1-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="d30a1-133">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="d30a1-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="d30a1-134">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="d30a1-134">Click Filter.</span></span>
9. <span data-ttu-id="d30a1-135">Á listanum, veljið línuna fyrir töflu fyrir færslur viðskiptavinar og reitinn greiðsluhátt.</span><span class="sxs-lookup"><span data-stu-id="d30a1-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="d30a1-136">Þú getur notað hvaða skilyrði sem er til að velja færslur viðskiptavinar til að greiða.</span><span class="sxs-lookup"><span data-stu-id="d30a1-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="d30a1-137">Í þessu dæmis skal nota rafrænt sem greiðsluaðferð til að sía færslur.</span><span class="sxs-lookup"><span data-stu-id="d30a1-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="d30a1-138">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="d30a1-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="d30a1-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-139">Click OK.</span></span>
12. <span data-ttu-id="d30a1-140">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d30a1-140">Click OK.</span></span>
13. <span data-ttu-id="d30a1-141">Smellt er á Stofna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="d30a1-141">Click Create payments.</span></span>

## <a name="generate-a-payment-file"></a><span data-ttu-id="d30a1-142">Mynda greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="d30a1-142">Generate a payment file</span></span>


