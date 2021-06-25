---
title: Afhendingaráætlanir
description: Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193783"
---
# <a name="delivery-schedules"></a><span data-ttu-id="e757b-103">Afhendingaráætlanir</span><span class="sxs-lookup"><span data-stu-id="e757b-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e757b-104">Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="e757b-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="e757b-105">Notaðu afhendingaráætlun þegar verður heildarmagn í pöntun eða tilboðslínu verður að vera afhent í mörgum sendingum.</span><span class="sxs-lookup"><span data-stu-id="e757b-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="e757b-106">Stakar sendingar eru táknaðar með afhendingarlínum.</span><span class="sxs-lookup"><span data-stu-id="e757b-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="e757b-107">Tvær eða fleiri afhendingarlínur mynda eina afhendingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="e757b-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="e757b-108">Afhendingarlínur getur haft mismunandi afhendingardagsetningar, magn, afhendingarmáti og geymsluvíddir, eins og svæði og vöruhús.</span><span class="sxs-lookup"><span data-stu-id="e757b-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="e757b-109">**Dæmi um afhendingaráætlun**</span><span class="sxs-lookup"><span data-stu-id="e757b-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="e757b-110">vara</span><span class="sxs-lookup"><span data-stu-id="e757b-110">Item</span></span>                              | <span data-ttu-id="e757b-111">Virði</span><span class="sxs-lookup"><span data-stu-id="e757b-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="e757b-112">Heildarpöntun (upprunalegu pöntunarlína)</span><span class="sxs-lookup"><span data-stu-id="e757b-112">Total order (original order line)</span></span> | <span data-ttu-id="e757b-113">600 stólar</span><span class="sxs-lookup"><span data-stu-id="e757b-113">600 chairs</span></span>                               |
| <span data-ttu-id="e757b-114">Umbeðin afhendingaráætlun</span><span class="sxs-lookup"><span data-stu-id="e757b-114">Requested delivery schedule</span></span>       | <span data-ttu-id="e757b-115">100 stólar á mánuði</span><span class="sxs-lookup"><span data-stu-id="e757b-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="e757b-116">Umbeðinn tímarammi fyrir afhendingu</span><span class="sxs-lookup"><span data-stu-id="e757b-116">Requested time frame for delivery</span></span> | <span data-ttu-id="e757b-117">6 mánuðir, á fyrsta degi hvers mánaðar</span><span class="sxs-lookup"><span data-stu-id="e757b-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="e757b-118">Í þessu dæmi biður viðskiptavinur um afhendingu á 600 stólum í runum með 100 stólum yfir sex mánaða tímabil.</span><span class="sxs-lookup"><span data-stu-id="e757b-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="e757b-119">Til að rekja afhendingarkröfur skal stofna afhendingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="e757b-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="e757b-120">Á síðunni Afhendingaráætlun skal stofna sex aðskildar afhendingarlínur.</span><span class="sxs-lookup"><span data-stu-id="e757b-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="e757b-121">Hver afhendingarlína inniheldur 100 stóla og tekur fram afhendingardag fyrir þessa 100 stóla.</span><span class="sxs-lookup"><span data-stu-id="e757b-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="e757b-122">Í þessu tilfelli er hver lína mótfærsla fyrsta mánaðar fyrir sex samfellda mánuði.</span><span class="sxs-lookup"><span data-stu-id="e757b-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="e757b-123">Þegar þú stofnar afhendingaráætlun er gerð upprunalegrar pöntunarlínu sjálfkrafa breytt í **Sölupöntunarlínu með margar afhendingar**.</span><span class="sxs-lookup"><span data-stu-id="e757b-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="e757b-124">Lína af þessari gerð kallast viðskiptalína og er merkt með tákni.</span><span class="sxs-lookup"><span data-stu-id="e757b-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="e757b-125">Afhendingarlínan er merkt með öðru tákni.</span><span class="sxs-lookup"><span data-stu-id="e757b-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="e757b-126">Ef þetta magni er breytt í afhendingarlínu er sviðskiptalínan uppfærð í heildarmagn afhendingaráætlunar.</span><span class="sxs-lookup"><span data-stu-id="e757b-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="e757b-127">Ef magni í afhendingarlínu er breytt er viðskiptalínan uppfærð í heildarmagn afhendingaráætlunar, jafnvel þegar pöntun er skipt upp í aðskildar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="e757b-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="e757b-128">Pantanir sem hafa afhendingaráætlun eru unnar gegn afhendingarlínum.</span><span class="sxs-lookup"><span data-stu-id="e757b-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="e757b-129">Vinnsla felur í sér bókun á fylgiseðlum, innhreyfingarskjölum afurða og reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="e757b-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="e757b-130">Skjalaútprentun pantana og tilboða sem hafa afhendingaráætlun sýna aðeins afhendingarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="e757b-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="e757b-131">Hún sýnir ekki upprunalegar línur (viðskiptalínur).</span><span class="sxs-lookup"><span data-stu-id="e757b-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="e757b-132">**Ábending:** Þar að auki eru aðeins afhendingarlínur sýndar þegar þessar aðgerðir eru framkvæmdar:</span><span class="sxs-lookup"><span data-stu-id="e757b-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="e757b-133">Bóka</span><span class="sxs-lookup"><span data-stu-id="e757b-133">Post</span></span>
-   <span data-ttu-id="e757b-134">Afrita síður</span><span class="sxs-lookup"><span data-stu-id="e757b-134">Copy pages</span></span>
-   <span data-ttu-id="e757b-135">Fletta listasíðum og skýrslum</span><span class="sxs-lookup"><span data-stu-id="e757b-135">Browse list pages and reports</span></span>

<span data-ttu-id="e757b-136">Þegar sölutilboð er staðfest sýna myndaðar sölupantanir alla afhendingaráætlunina, jafnvel pöntunarlínur sem hafa margar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="e757b-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="e757b-137">Þar að auki er öll afhendingaráætlunin sýnd á öllum aðalsíðum, eins og sölupöntunum, sölutilboðum og innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="e757b-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]