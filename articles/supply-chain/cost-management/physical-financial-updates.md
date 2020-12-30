---
title: fjárhagslegar og efnislegar uppfærslur
description: Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea79bd9c6561c4e4f6fad2c177f44fe62bdea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430519"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="3928f-103">fjárhagslegar og efnislegar uppfærslur</span><span class="sxs-lookup"><span data-stu-id="3928f-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3928f-104">Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn.</span><span class="sxs-lookup"><span data-stu-id="3928f-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="3928f-105">Birgðafærslur er hægt að uppfæra efnislega og fjárhagslega í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3928f-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3928f-106">Sumar gerðir efnislegra og fjárhagsfærslna auka birgðamagn, á meðan aðrar draga úr magninu.</span><span class="sxs-lookup"><span data-stu-id="3928f-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="3928f-107">Efnisleg aukning</span><span class="sxs-lookup"><span data-stu-id="3928f-107">Physical increases</span></span>
<span data-ttu-id="3928f-108">Þegar efnisleg færsla er bókuð er staða færsluskránnar **"Móttekið"**.</span><span class="sxs-lookup"><span data-stu-id="3928f-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="3928f-109">Eftirfarandi færslur skoðast sem efnisleg aukning:</span><span class="sxs-lookup"><span data-stu-id="3928f-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="3928f-110">Móttaka innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-110">Purchase order receipt</span></span>
-   <span data-ttu-id="3928f-111">Skil á fylgiseðli sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="3928f-112">Skrá framleiðslupöntun sem lokið</span><span class="sxs-lookup"><span data-stu-id="3928f-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="3928f-113">Aukaafurð á tiltektarlista framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="3928f-114">Fjárhagsleg aukning</span><span class="sxs-lookup"><span data-stu-id="3928f-114">Financial increases</span></span>
<span data-ttu-id="3928f-115">Þegar fjárhagsleg innhreyfingarfærsla er bókuð, er staða færsluskránnar sem eykur magnið **"Innkeypt".**</span><span class="sxs-lookup"><span data-stu-id="3928f-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="3928f-116">Eftirfarandi færslur skoðast sem fjárhagsleg aukning:</span><span class="sxs-lookup"><span data-stu-id="3928f-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="3928f-117">Reikningur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3928f-117">Vendor invoice</span></span>
-   <span data-ttu-id="3928f-118">Sölupöntunarreikningur vegna skila</span><span class="sxs-lookup"><span data-stu-id="3928f-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="3928f-119">Kostnaður framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-119">Production order costing</span></span>
-   <span data-ttu-id="3928f-120">Birgðabækur með jákvæðu magni, svo sem hreyfing, hagnaður/tap, talningabækur, uppskriftir og flutningur</span><span class="sxs-lookup"><span data-stu-id="3928f-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="3928f-121">Færslur sem auka magn</span><span class="sxs-lookup"><span data-stu-id="3928f-121">Transactions that increase quantity</span></span>
<span data-ttu-id="3928f-122">Færslur sem auka magn eru bókaðar á gildandi meðalkostnaðarverði.</span><span class="sxs-lookup"><span data-stu-id="3928f-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="3928f-123">Útreiknað gildandi meðalkostnaðarverð sem er byggt á kostnaði hverrar slíkrar færslu fyrir hverja birgðavídd sem er fjárhagslega rakin.</span><span class="sxs-lookup"><span data-stu-id="3928f-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="3928f-124">Sjá upplýsingar um hvernig keyra á meðalkostnaðarverð sjá [keyrsla á meðalkostnaðarverði](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="3928f-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="3928f-125">Færslur sem minnka magn</span><span class="sxs-lookup"><span data-stu-id="3928f-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="3928f-126">Útreiknað meðalkostnaðarverð er notað þegar hreyfing sem minnkar magn er bókuð án tillits til hver birgðalíkan er í félagi með því birgðir.</span><span class="sxs-lookup"><span data-stu-id="3928f-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="3928f-127">Þetta krefst þess að færslan sem minnkar magn var ekki áður merkt annarri færslu fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="3928f-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="3928f-128">Ef efnislegar lagerbirgðir verða neikvæðar er birgðakostnaðurinn sem er skilgreindur fyrir vöruna á síðunni **Vara** notaður.</span><span class="sxs-lookup"><span data-stu-id="3928f-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="3928f-129">Ef virkni fjölsíðna er virkjuð verður þessi kostnaður í staðinn vera birgðakostnaður sem er skilgreint fyrir síðuna í síðunni **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="3928f-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="3928f-130">Efnislegar úthreyfingar miðað við fjárhagslegar úthreyfingar</span><span class="sxs-lookup"><span data-stu-id="3928f-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="3928f-131">Þegar efnisleg úthreyfingarfærsla er bókuð er staða færsluskránnar **"Dregið frá"**.</span><span class="sxs-lookup"><span data-stu-id="3928f-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="3928f-132">Eftirfarandi færslur skoðast sem efnislegar úthreyfingar:</span><span class="sxs-lookup"><span data-stu-id="3928f-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="3928f-133">Tiltektarlistabók framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-133">Production order picking list journal</span></span>
-   <span data-ttu-id="3928f-134">Fylgiseðill sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-134">Sales order packing slip</span></span>
-   <span data-ttu-id="3928f-135">Skil á fylgiseðli innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="3928f-135">Purchase order packing slip return</span></span>

<span data-ttu-id="3928f-136">Þegar fjárhagsfærsla er bókuð, er staða færsluskránnar **"Selt"**.</span><span class="sxs-lookup"><span data-stu-id="3928f-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="3928f-137">Eftirfarandi færslur skoðast sem fjárhagslegar úthreyfingar:</span><span class="sxs-lookup"><span data-stu-id="3928f-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="3928f-138">Ljúka framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="3928f-138">Ending a production order</span></span>
-   <span data-ttu-id="3928f-139">Sölupöntunarreikningur</span><span class="sxs-lookup"><span data-stu-id="3928f-139">Sales order invoice</span></span>
-   <span data-ttu-id="3928f-140">Endursending reiknings lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3928f-140">Vendor invoice return</span></span>
-   <span data-ttu-id="3928f-141">Birgðabækur með neikvæðu magni, svo sem hreyfing, hagnaður/tap, talningabækur, uppskriftir og flutningur</span><span class="sxs-lookup"><span data-stu-id="3928f-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="3928f-142">Færslur sem minnka magn eru bókaðar á hlaupandi meðaltal kostnaðarverðs.</span><span class="sxs-lookup"><span data-stu-id="3928f-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="3928f-143">Þannig að birgðalokunarferlið þarf til að jafna úthreyfingarfærslur á innhreyfingarfærslur í samræmi við birgðalíkan sem tengt er við hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="3928f-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>
