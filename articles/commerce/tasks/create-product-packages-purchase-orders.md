---
title: Stofna afurðapakka fyrir innkaupapantanir
description: Þetta ferli fer í gegnum stofna Umbúðir afurðar og nota það í innkaupapöntun.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413207"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="09bcb-103">Stofna afurðapakka fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="09bcb-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09bcb-104">Þetta ferli fer í gegnum stofna Umbúðir afurðar og nota það í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="09bcb-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="09bcb-105">Innkaupapöntun verður notuð til að stofna pöntun fyrir fyrirfram skilgreindan afurðasett.</span><span class="sxs-lookup"><span data-stu-id="09bcb-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="09bcb-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="09bcb-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="09bcb-107">Stofna umbúðir vöru</span><span class="sxs-lookup"><span data-stu-id="09bcb-107">Create a product package</span></span>
1. <span data-ttu-id="09bcb-108">Fara í Retail og Commerce > Birgðastjórnun > Áfylling > Umbúðir afurðar.</span><span class="sxs-lookup"><span data-stu-id="09bcb-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="09bcb-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-109">Click New.</span></span>
3. <span data-ttu-id="09bcb-110">Færa inn gildi í reitnum númer umbúða.</span><span class="sxs-lookup"><span data-stu-id="09bcb-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="09bcb-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09bcb-112">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="09bcb-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="09bcb-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="09bcb-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="09bcb-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="09bcb-114">Click Add.</span></span>
8. <span data-ttu-id="09bcb-115">Í svæðið númers, færðu inn '0160'.</span><span class="sxs-lookup"><span data-stu-id="09bcb-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="09bcb-116">Í reitnum Stærð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="09bcb-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="09bcb-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="09bcb-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="09bcb-118">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="09bcb-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="09bcb-119">Click Add.</span></span>
13. <span data-ttu-id="09bcb-120">Í svæðið númers, færðu inn '0160'.</span><span class="sxs-lookup"><span data-stu-id="09bcb-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="09bcb-121">Í reitnum númer vöruvíddasamsetningar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="09bcb-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="09bcb-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="09bcb-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="09bcb-123">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="09bcb-124">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="09bcb-124">Click Add.</span></span>
18. <span data-ttu-id="09bcb-125">Í svæðið númer vöru, færðu inn '0175'.</span><span class="sxs-lookup"><span data-stu-id="09bcb-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="09bcb-126">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="09bcb-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-127">Click Save.</span></span>
21. <span data-ttu-id="09bcb-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09bcb-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="09bcb-129">Bæta umbúðum við innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="09bcb-129">Add package to purchase order</span></span>
1. <span data-ttu-id="09bcb-130">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="09bcb-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="09bcb-131">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-131">Click New.</span></span>
3. <span data-ttu-id="09bcb-132">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="09bcb-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="09bcb-133">Á listanum, veljið sama lánardrottni og umbúðir afurðar var áður búið til fyrir, ef lánardrottinn var valinn.</span><span class="sxs-lookup"><span data-stu-id="09bcb-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="09bcb-134">Víxla útvíkkun á liðnum Almennt.</span><span class="sxs-lookup"><span data-stu-id="09bcb-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="09bcb-135">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="09bcb-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="09bcb-136">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="09bcb-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="09bcb-137">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="09bcb-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="09bcb-138">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="09bcb-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="09bcb-139">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="09bcb-139">Click OK.</span></span>
11. <span data-ttu-id="09bcb-140">Víxla útvíkkun á liðnum línuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="09bcb-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="09bcb-141">Smellið á flipann umbúðir Vöru.</span><span class="sxs-lookup"><span data-stu-id="09bcb-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="09bcb-142">Smellt er á Innkaup Innkaupapöntunarlína</span><span class="sxs-lookup"><span data-stu-id="09bcb-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="09bcb-143">Smellt er á Stofna línur úr umbúðum</span><span class="sxs-lookup"><span data-stu-id="09bcb-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="09bcb-144">á listanum, Finna og velja umbúðir afurðar sem stofnaði í fyrra skrefi .</span><span class="sxs-lookup"><span data-stu-id="09bcb-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="09bcb-145">Í reitinn magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="09bcb-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="09bcb-146">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-146">Click Create.</span></span>
18. <span data-ttu-id="09bcb-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="09bcb-147">Click Save.</span></span>

