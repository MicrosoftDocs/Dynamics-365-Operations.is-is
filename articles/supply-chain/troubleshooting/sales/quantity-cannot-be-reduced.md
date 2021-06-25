---
title: Ekki er hægt að minnka magn þegar hætt er við sölupöntun
description: Ekki er hægt að minnka magn þegar hætt er við sölupöntun.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230837"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="58300-103">Ekki er hægt að minnka magn þegar hætt er við sölupöntun</span><span class="sxs-lookup"><span data-stu-id="58300-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="58300-104">Villukóði SYS138831</span><span class="sxs-lookup"><span data-stu-id="58300-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="58300-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="58300-105">Symptoms</span></span>

<span data-ttu-id="58300-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="58300-106">The system shows the following error message:</span></span>

> <span data-ttu-id="58300-107">Ekki er hægt að draga úr magninu.</span><span class="sxs-lookup"><span data-stu-id="58300-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="58300-108">Fjöldi birgðafærslna í pöntun er of lítill vegna þess að úttakspöntun eða framleiðslupöntun vísar í magnið eða hluta þess, eða vegna þess framleiðslupöntun er merkt á móti öðrum færslum.</span><span class="sxs-lookup"><span data-stu-id="58300-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="58300-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="58300-109">Cause</span></span>

<span data-ttu-id="58300-110">Ef vinna tengist sölupöntun er ekki hægt að hætta við sölupöntunina fyrr en hætt er við vinnu og hún bakfærð.</span><span class="sxs-lookup"><span data-stu-id="58300-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="58300-111">Þessi krafa gildir jafnvel þótt vinnan sem tengist sölupöntuninni sé lokuð.</span><span class="sxs-lookup"><span data-stu-id="58300-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="58300-112">Lausn</span><span class="sxs-lookup"><span data-stu-id="58300-112">Resolution</span></span>

<span data-ttu-id="58300-113">Til að leysa þetta vandamál skal ljúka eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="58300-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="58300-114">Hætta við opin verk.</span><span class="sxs-lookup"><span data-stu-id="58300-114">Cancel open work.</span></span>
1. <span data-ttu-id="58300-115">Eyðið farminum.</span><span class="sxs-lookup"><span data-stu-id="58300-115">Delete the load.</span></span>
1. <span data-ttu-id="58300-116">Minnka tiltekið magn.</span><span class="sxs-lookup"><span data-stu-id="58300-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="58300-117">Hætta við opin verk</span><span class="sxs-lookup"><span data-stu-id="58300-117">Cancel open work</span></span>

<span data-ttu-id="58300-118">Til að hætta við opið verk skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="58300-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="58300-119">Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="58300-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="58300-120">Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni** og sem hefur gildið **Vinnustaða** *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.</span><span class="sxs-lookup"><span data-stu-id="58300-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="58300-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="58300-121">Select **OK**.</span></span>
1. <span data-ttu-id="58300-122">Veljið **Já** til að staðfesta að hætta skuli við verkið.</span><span class="sxs-lookup"><span data-stu-id="58300-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="58300-123">Eyðið farminum</span><span class="sxs-lookup"><span data-stu-id="58300-123">Delete the load</span></span>

<span data-ttu-id="58300-124">Til að eyða hleðslu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="58300-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="58300-125">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="58300-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="58300-126">Viðeigandi sölupöntun er opnuð.</span><span class="sxs-lookup"><span data-stu-id="58300-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="58300-127">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Vöruhús \> Upplýsingar um verk**.</span><span class="sxs-lookup"><span data-stu-id="58300-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="58300-128">Á síðunni **Vinna**, á aðgerðasvæðinu, í flipanum **Verk**, í flokknum **Verk**, skal velja **Hætta við verk**.</span><span class="sxs-lookup"><span data-stu-id="58300-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="58300-129">Staðfestið að reiturinn **Staða verks** sé stilltur á *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="58300-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="58300-130">Lokaðu síðunni **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="58300-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="58300-131">Á síðunni upplýsingar um sölupöntun, í flýtiflipanum **Sölupöntunarlínur**, skal velja **Vöruhús \> Upplýsingar hleðslu**.</span><span class="sxs-lookup"><span data-stu-id="58300-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="58300-132">Á aðgerðasvæðinu skal velja **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="58300-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="58300-133">Veljið **Já** til að staðfesta að ætlunin sé að eyða hleðslunni.</span><span class="sxs-lookup"><span data-stu-id="58300-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="58300-134">Loka síðunni **Hleðsla**.</span><span class="sxs-lookup"><span data-stu-id="58300-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="58300-135">Minnka tiltekið magn</span><span class="sxs-lookup"><span data-stu-id="58300-135">Reduce the picked quantity</span></span>

<span data-ttu-id="58300-136">Eftir að hætt hefur verið við alla vinnu skal fylgja þessum skrefum til að draga úr tiltektarmagninu.</span><span class="sxs-lookup"><span data-stu-id="58300-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="58300-137">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="58300-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="58300-138">Viðeigandi sölupöntun er opnuð.</span><span class="sxs-lookup"><span data-stu-id="58300-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="58300-139">Í flipanum **Sölupöntunarlínur** skal velja **Uppfæra línu \> Tiltekt** úr tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="58300-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="58300-140">Á síðunni **Tiltekt** í hlutanum **Færslur** er valin sú lína þar sem reiturinn **Staða máls** er stilltur á *Tekið til*.</span><span class="sxs-lookup"><span data-stu-id="58300-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="58300-141">Í hlutanum **Færslur** skal velja **Bæta við tiltektarlínu** úr tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="58300-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="58300-142">Í hlutanum **Tiltektarlínur** skal velja **Staðfesta tiltekt á öllu** úr tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="58300-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="58300-143">Lokið síðunni **Tiltekt**.</span><span class="sxs-lookup"><span data-stu-id="58300-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="58300-144">Á upplýsingasíðu sölupöntunar, á aðgerðasvæðinu, í flipanum **Sölupöntun**, í hópnum **Vinna með**, skal velja **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="58300-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="58300-145">Veljið **Já** til að staðfesta að hætta skuli við sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="58300-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
