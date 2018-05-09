---
title: "Afhendingaráætlanir"
description: "Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5e48d8f0ec434acdcfb72a38ccbf8dbc6938a256
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="delivery-schedules"></a><span data-ttu-id="397ca-103">Afhendingaráætlanir</span><span class="sxs-lookup"><span data-stu-id="397ca-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="397ca-104">Með afhendingaráætlunum er hægt að rekja magn í pöntunarlínu þegar notaðar eru margar afhendingar fyrir staka sölupöntun, sölutilboð eða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="397ca-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="397ca-105">Notaðu afhendingaráætlun þegar verður heildarmagn í pöntun eða tilboðslínu verður að vera afhent í mörgum sendingum.</span><span class="sxs-lookup"><span data-stu-id="397ca-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="397ca-106">Stakar sendingar eru táknaðar með afhendingarlínum.</span><span class="sxs-lookup"><span data-stu-id="397ca-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="397ca-107">Tvær eða fleiri afhendingarlínur mynda eina afhendingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="397ca-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="397ca-108">Afhendingarlínur getur haft mismunandi afhendingardagsetningar, magn, afhendingarmáta og geymsluvíddir, eins og svæði og vöruhús.</span><span class="sxs-lookup"><span data-stu-id="397ca-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="397ca-109">**Dæmi um afhendingaráætlun**</span><span class="sxs-lookup"><span data-stu-id="397ca-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="397ca-110">Heildarpöntun (upprunalegu pöntunarlína)</span><span class="sxs-lookup"><span data-stu-id="397ca-110">Total order (original order line)</span></span> | <span data-ttu-id="397ca-111">600 stólar</span><span class="sxs-lookup"><span data-stu-id="397ca-111">600 chairs</span></span>                               |
| <span data-ttu-id="397ca-112">Umbeðin afhendingaráætlun</span><span class="sxs-lookup"><span data-stu-id="397ca-112">Requested delivery schedule</span></span>       | <span data-ttu-id="397ca-113">100 stólar á mánuði</span><span class="sxs-lookup"><span data-stu-id="397ca-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="397ca-114">Umbeðinn tímarammi fyrir afhendingu</span><span class="sxs-lookup"><span data-stu-id="397ca-114">Requested time frame for delivery</span></span> | <span data-ttu-id="397ca-115">6 mánuðir, á fyrsta degi hvers mánaðar</span><span class="sxs-lookup"><span data-stu-id="397ca-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="397ca-116">Í þessu dæmi biður viðskiptavinur um afhendingu á 600 stólum í runum með 100 stólum yfir sex mánaða tímabil.</span><span class="sxs-lookup"><span data-stu-id="397ca-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="397ca-117">Til að rekja afhendingarkröfur skal stofna afhendingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="397ca-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="397ca-118">Á síðunni Afhendingaráætlun skal stofna sex aðskildar afhendingarlínur.</span><span class="sxs-lookup"><span data-stu-id="397ca-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="397ca-119">Hver afhendingarlína inniheldur 100 stóla og tekur fram afhendingardag fyrir þessa 100 stóla.</span><span class="sxs-lookup"><span data-stu-id="397ca-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="397ca-120">Í þessu tilfelli er hver lína mótfærsla fyrsta mánaðar fyrir sex samfellda mánuði.</span><span class="sxs-lookup"><span data-stu-id="397ca-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="397ca-121">Þegar þú stofnar afhendingaráætlun er gerð upprunalegrar pöntunarlínu sjálfkrafa breytt í **Sölupöntunarlínu með margar afhendingar**.</span><span class="sxs-lookup"><span data-stu-id="397ca-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="397ca-122">Lína af þessari gerð kallast viðskiptalína og er merkt með tákni.</span><span class="sxs-lookup"><span data-stu-id="397ca-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="397ca-123">Afhendingarlínan er merkt með öðru tákni.</span><span class="sxs-lookup"><span data-stu-id="397ca-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="397ca-124">Ef þetta magni er breytt í afhendingarlínu er sviðskiptalínan uppfærð í heildarmagn afhendingaráætlunar.</span><span class="sxs-lookup"><span data-stu-id="397ca-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="397ca-125">Ef magni í afhendingarlínu er breytt er viðskiptalínan uppfærð í heildarmagn afhendingaráætlunar, jafnvel þegar pöntun er skipt upp í aðskildar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="397ca-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="397ca-126">Pantanir sem hafa afhendingaráætlun eru unnar gegn afhendingarlínum.</span><span class="sxs-lookup"><span data-stu-id="397ca-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="397ca-127">Vinnsla felur í sér bókun á fylgiseðlum, innhreyfingarskjölum afurða og reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="397ca-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="397ca-128">Skjalaútprentun pantana og tilboða sem hafa afhendingaráætlun sýna aðeins afhendingarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="397ca-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="397ca-129">Hún sýnir ekki upprunalegar línur (viðskiptalínur).</span><span class="sxs-lookup"><span data-stu-id="397ca-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="397ca-130">**Ábending:** Þar að auki eru aðeins afhendingarlínur sýndar þegar þessar aðgerðir eru framkvæmdar:</span><span class="sxs-lookup"><span data-stu-id="397ca-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="397ca-131">Bóka</span><span class="sxs-lookup"><span data-stu-id="397ca-131">Post</span></span>
-   <span data-ttu-id="397ca-132">Afrita síður</span><span class="sxs-lookup"><span data-stu-id="397ca-132">Copy pages</span></span>
-   <span data-ttu-id="397ca-133">Fletta listasíðum og skýrslum</span><span class="sxs-lookup"><span data-stu-id="397ca-133">Browse list pages and reports</span></span>

<span data-ttu-id="397ca-134">Þegar sölutilboð er staðfest sýna myndaðar sölupantanir alla afhendingaráætlunina, jafnvel pöntunarlínur sem hafa margar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="397ca-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="397ca-135">Þar að auki er öll afhendingaráætlunin sýnd á öllum aðalsíðum, eins og sölupöntunum, sölutilboðum og innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="397ca-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




