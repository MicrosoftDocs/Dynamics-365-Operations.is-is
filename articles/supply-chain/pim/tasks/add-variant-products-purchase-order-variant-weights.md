--- 
title: "Bæta afbrigðum afurða við innkaupapantanir með því að nota þyngd afbrigða"
description: "Þetta ferli fer í gegnum skrefin til að nota vöruvíddasamsetningar þyngdar til að sjálfvirk útfylla innkaupapöntunarlínur fyrir hverja vöruvíddasamsetningu vöru."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3db13646c82ea6dc6949aaa714a5769f9c5ad2a9
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="94a06-103">Bæta afbrigðum afurða við innkaupapantanir með því að nota þyngd afbrigða</span><span class="sxs-lookup"><span data-stu-id="94a06-103">Add variant products to purchase orders using variant weights</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94a06-104">Þetta ferli fer í gegnum skrefin til að nota vöruvíddasamsetningar þyngdar til að sjálfvirk útfylla innkaupapöntunarlínur fyrir hverja vöruvíddasamsetningu vöru.</span><span class="sxs-lookup"><span data-stu-id="94a06-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="94a06-105">Þegar magn vörunnar sem á að kaupa valið, er innkaupapöntunarlínur stofnaðar fyrir vöruvíddasamsetningar afurðar með tillögur byggðar á þyngd sem skilgreind var fyrir afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="94a06-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="94a06-106">Þetta ferli ekki innihalda skref til að skilgreina gildi þyngdar á víddir afurð og afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="94a06-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="94a06-107">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="94a06-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="94a06-108">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="94a06-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="94a06-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="94a06-109">Click New.</span></span>
3. <span data-ttu-id="94a06-110">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="94a06-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="94a06-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="94a06-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="94a06-112">Víxla útvíkkun á liðnum Almennt.</span><span class="sxs-lookup"><span data-stu-id="94a06-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="94a06-113">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="94a06-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="94a06-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="94a06-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="94a06-115">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="94a06-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="94a06-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="94a06-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="94a06-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="94a06-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="94a06-118">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="94a06-118">Click OK.</span></span>
12. <span data-ttu-id="94a06-119">Víxla útvíkkun á liðnum línuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="94a06-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="94a06-120">Smellt er á flipann Vöruvíddasamsetning.</span><span class="sxs-lookup"><span data-stu-id="94a06-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="94a06-121">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="94a06-121">Click Add line.</span></span>
15. <span data-ttu-id="94a06-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="94a06-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="94a06-123">Í svæðið númer vöru, færðu inn '0140'.</span><span class="sxs-lookup"><span data-stu-id="94a06-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="94a06-124">Stillið magn á „1000“.</span><span class="sxs-lookup"><span data-stu-id="94a06-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="94a06-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="94a06-125">Click Save.</span></span>


