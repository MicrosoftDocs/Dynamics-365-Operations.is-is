---
title: fjárhagslegar og efnislegar uppfærslur
description: Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba628dbf63d3b124583e6b873530f1459b07562
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "322583"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="74ed1-103">fjárhagslegar og efnislegar uppfærslur</span><span class="sxs-lookup"><span data-stu-id="74ed1-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74ed1-104">Þetta efnisatriði veitir yfirlit yfir hvaða gerðir færslna auka eða minnka birgðamagn.</span><span class="sxs-lookup"><span data-stu-id="74ed1-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="74ed1-105">Birgðafærslur er hægt að uppfæra efnislega og fjárhagslega í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="74ed1-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="74ed1-106">Sumar gerðir efnislegra og fjárhagsfærslna auka birgðamagn, á meðan aðrar draga úr magninu.</span><span class="sxs-lookup"><span data-stu-id="74ed1-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="74ed1-107">Efnisleg aukning</span><span class="sxs-lookup"><span data-stu-id="74ed1-107">Physical increases</span></span>
<span data-ttu-id="74ed1-108">Þegar efnisleg færsla er bókuð er staða færsluskránnar **"Móttekið"**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="74ed1-109">Eftirfarandi færslur skoðast sem efnisleg aukning:</span><span class="sxs-lookup"><span data-stu-id="74ed1-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="74ed1-110">Móttaka innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-110">Purchase order receipt</span></span>
-   <span data-ttu-id="74ed1-111">Skil á fylgiseðli sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="74ed1-112">Skrá framleiðslupöntun sem lokið</span><span class="sxs-lookup"><span data-stu-id="74ed1-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="74ed1-113">Aukaafurð á tiltektarlista framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="74ed1-114">Fjárhagsleg aukning</span><span class="sxs-lookup"><span data-stu-id="74ed1-114">Financial increases</span></span>
<span data-ttu-id="74ed1-115">Þegar fjárhagsleg innhreyfingarfærsla er bókuð, er staða færsluskránnar sem eykur magnið **"Innkeypt".**</span><span class="sxs-lookup"><span data-stu-id="74ed1-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="74ed1-116">Eftirfarandi færslur skoðast sem fjárhagsleg aukning:</span><span class="sxs-lookup"><span data-stu-id="74ed1-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="74ed1-117">Reikningur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="74ed1-117">Vendor invoice</span></span>
-   <span data-ttu-id="74ed1-118">Sölupöntunarreikningur vegna skila</span><span class="sxs-lookup"><span data-stu-id="74ed1-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="74ed1-119">Kostnaður framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-119">Production order costing</span></span>
-   <span data-ttu-id="74ed1-120">Birgðabækur með jákvæðu magni, svo sem hreyfing, hagnaður/tap, talningabækur, uppskriftir og flutningur</span><span class="sxs-lookup"><span data-stu-id="74ed1-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="74ed1-121">Færslur sem auka magn</span><span class="sxs-lookup"><span data-stu-id="74ed1-121">Transactions that increase quantity</span></span>
<span data-ttu-id="74ed1-122">Færslur sem auka magn eru bókaðar á gildandi meðalkostnaðarverði.</span><span class="sxs-lookup"><span data-stu-id="74ed1-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="74ed1-123">Finance and Operations reiknar út gildandi meðalkostnaðarverð sem er byggt á kostnaði hverrar slíkrar færslu fyrir hverja birgðavídd sem er rakin fjárhagslega.</span><span class="sxs-lookup"><span data-stu-id="74ed1-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="74ed1-124">Sjá upplýsingar um hvernig keyra á meðalkostnaðarverð sjá [keyrsla á meðalkostnaðarverði](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="74ed1-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="74ed1-125">Færslur sem minnka magn</span><span class="sxs-lookup"><span data-stu-id="74ed1-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="74ed1-126">Finance and Operations notar reiknaða keyrslu á meðalkostnaðarverði þegar hreyfing sem minnkar magn er bókuð án tillits til birgðalíkansins sem er tengt þeim birgðum.</span><span class="sxs-lookup"><span data-stu-id="74ed1-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="74ed1-127">Þetta krefst þess að færslan sem minnkar magn var ekki áður merkt annarri færslu fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="74ed1-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="74ed1-128">Ef efnislegar lagerbirgðir verða neikvæðar notar Finance and Operations þann birgðakostnað sem er skilgreindur fyrir vöruna á síðunni **Vara**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="74ed1-129">**Athugasemd** Ef virkni fjölsíðna er virkjuð verður þessi kostnaður í staðinn vera birgðakostnaður sem er skilgreint fyrir síðuna í síðunni **sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="74ed1-130">Efnislegar úthreyfingar miðað við fjárhagslegar úthreyfingar</span><span class="sxs-lookup"><span data-stu-id="74ed1-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="74ed1-131">Þegar efnisleg úthreyfingarfærsla er bókuð er staða færsluskránnar **"Dregið frá"**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="74ed1-132">Eftirfarandi færslur skoðast sem efnislegar úthreyfingar:</span><span class="sxs-lookup"><span data-stu-id="74ed1-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="74ed1-133">Tiltektarlistabók framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-133">Production order picking list journal</span></span>
-   <span data-ttu-id="74ed1-134">Fylgiseðill sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-134">Sales order packing slip</span></span>
-   <span data-ttu-id="74ed1-135">Skil á fylgiseðli innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="74ed1-135">Purchase order packing slip return</span></span>

<span data-ttu-id="74ed1-136">Þegar fjárhagsfærsla er bókuð, er staða færsluskránnar **"Selt"**.</span><span class="sxs-lookup"><span data-stu-id="74ed1-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="74ed1-137">Eftirfarandi færslur skoðast sem fjárhagslegar úthreyfingar:</span><span class="sxs-lookup"><span data-stu-id="74ed1-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="74ed1-138">Ljúka framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="74ed1-138">Ending a production order</span></span>
-   <span data-ttu-id="74ed1-139">Sölupöntunarreikningur</span><span class="sxs-lookup"><span data-stu-id="74ed1-139">Sales order invoice</span></span>
-   <span data-ttu-id="74ed1-140">Endursending reiknings lánardrottins</span><span class="sxs-lookup"><span data-stu-id="74ed1-140">Vendor invoice return</span></span>
-   <span data-ttu-id="74ed1-141">Birgðabækur með neikvæðu magni, svo sem hreyfing, hagnaður/tap, talningabækur, uppskriftir og flutningur</span><span class="sxs-lookup"><span data-stu-id="74ed1-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="74ed1-142">Færslur sem minnka magn eru bókaðar á hlaupandi meðaltal kostnaðarverðs.</span><span class="sxs-lookup"><span data-stu-id="74ed1-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="74ed1-143">Þannig að birgðalokunarferlið þarf til að jafna úthreyfingarfærslur á innhreyfingarfærslur í samræmi við birgðalíkan sem tengt er við hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="74ed1-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>



