---
title: Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun
description: Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 319eb0070a3677035e2a5d89744e80cd38c08d8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430409"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="d65aa-103">Stofna innkaupapöntun sem stjórnast af fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="d65aa-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d65aa-104">Nota þetta ferli til að stofna innkaupapöntun sem er athuguð í tiltækri fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="d65aa-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="d65aa-105">Þessi skráning notar USMF sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="d65aa-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="d65aa-106">Yfirfara skilgreiningu fjárhagsáætlunarstýringar</span><span class="sxs-lookup"><span data-stu-id="d65aa-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="d65aa-107">Fara í Fjárhagsáætlun > Uppsetning > fjárhagsáætlunarstýring > uppsetning fjárhagsáætlunarstýringar.</span><span class="sxs-lookup"><span data-stu-id="d65aa-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="d65aa-108">Smella á flipann Tiltækt fjármagn úr fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="d65aa-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="d65aa-109">Smella á flipann Skjöl og færslubækur</span><span class="sxs-lookup"><span data-stu-id="d65aa-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="d65aa-110">Smella á flipann Skilgreina reglur fjárhagsáætlunarstýringar</span><span class="sxs-lookup"><span data-stu-id="d65aa-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="d65aa-111">Smella á flipann Skilgreina fjárhagsáætlunarflokka</span><span class="sxs-lookup"><span data-stu-id="d65aa-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="d65aa-112">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d65aa-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="d65aa-113">Stofna haus innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="d65aa-113">Create the purchase order header</span></span>
1. <span data-ttu-id="d65aa-114">Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="d65aa-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="d65aa-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-115">Click New.</span></span>
3. <span data-ttu-id="d65aa-116">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="d65aa-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="d65aa-117">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="d65aa-117">Expand the General section.</span></span>
5. <span data-ttu-id="d65aa-118">Í reitnum Dagsetning reikningsskila skal stilla dagsetningu á „2016-01-01“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="d65aa-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="d65aa-120">Bæta við innkaupapöntunarlína</span><span class="sxs-lookup"><span data-stu-id="d65aa-120">Add a purchase order line</span></span>
1. <span data-ttu-id="d65aa-121">Slá inn eða velja gildi í reitnum innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="d65aa-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="d65aa-122">Stilla magn á „2“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="d65aa-123">Í reitinn eining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d65aa-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="d65aa-124">Stilla Einingarverð á „10000“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="d65aa-125">Smelltu á Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="d65aa-125">Click Financials.</span></span>
6. <span data-ttu-id="d65aa-126">Smellt er á Dreifa upphæðum.</span><span class="sxs-lookup"><span data-stu-id="d65aa-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="d65aa-127">Í reitnum Fjárhagslykill skal tilgreina gildin „601300-001-023--“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="d65aa-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d65aa-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="d65aa-129">Framkvæma athugun á fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="d65aa-129">Perform budget checking</span></span>
1. <span data-ttu-id="d65aa-130">Smelltu á Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="d65aa-130">Click Financials.</span></span>
2. <span data-ttu-id="d65aa-131">Smella á Framkvæma athugun á fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="d65aa-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="d65aa-132">Smelltu á Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="d65aa-132">Click Financials.</span></span>
4. <span data-ttu-id="d65aa-133">Smella á athugun á villum eða viðvörunum í fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="d65aa-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="d65aa-134">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="d65aa-134">Click Close.</span></span>

