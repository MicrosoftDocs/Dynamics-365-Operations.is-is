---
title: Setja upp vinnusniðmát fyrir innkaupapantanir
description: Þetta efni lýsir hvernig setja skal upp einfalt vinnusniðmát sem nota á þegar taka á frá mótteknar vörur.
author: ShylaThompson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 473bb133159bb6cdcbbd30ab2c8452eb69f8cfaf
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148197"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="24ba1-103">Setja upp vinnusniðmát fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="24ba1-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24ba1-104">Þetta efni lýsir hvernig setja skal upp einfalt vinnusniðmát sem nota á þegar taka á frá mótteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="24ba1-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="24ba1-105">Vinnusniðmát ákvarða safn leiðbeiningarnar sem birtast starfsmanns vöruhús í farsíma þegar fluttar eru vörur frá móttöku svæði.</span><span class="sxs-lookup"><span data-stu-id="24ba1-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="24ba1-106">Hægt er að nota þessi ferli með gögn sem eru nefnd í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="24ba1-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="24ba1-107">Áður en byrjað er í þessari handbók, stofna kenni vinnuhóps.</span><span class="sxs-lookup"><span data-stu-id="24ba1-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="24ba1-108">Í þessu dæmi er kenni vinnuhóps kallað inn í Á innleið notað.</span><span class="sxs-lookup"><span data-stu-id="24ba1-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="24ba1-109">Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="24ba1-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vinna > Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="24ba1-111">Í reitnum **Gerð verkbeiðni** velurðu **Innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="24ba1-112">Stofna haus fyrir sniðmát verks</span><span class="sxs-lookup"><span data-stu-id="24ba1-112">Create a work template header</span></span>
1. <span data-ttu-id="24ba1-113">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-113">Select **New**.</span></span>
2. <span data-ttu-id="24ba1-114">Í reitinn **Raðnúmer** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="24ba1-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="24ba1-115">Þetta er númeraröð sem vinnusniðmát eru metnar fyrir.</span><span class="sxs-lookup"><span data-stu-id="24ba1-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="24ba1-116">Hægt er að breyta röð, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="24ba1-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="24ba1-117">Í reitnum **Vinnusniðmát** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="24ba1-118">Þetta er einkvæmt kenni fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="24ba1-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="24ba1-119">Í reitinn **Lýsing vinnusniðmáts** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="24ba1-120">Valkosturinn **Gildir** verður ekki athugaður fyrr en þú hefur lokið við allar upplýsingar sem þörf er á í sniðmátinu og hefur valið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="24ba1-121">Verkbeiðni af gerðinni **Innkaupapöntun** er ekki hægt að vinna sjálfkrafa, hafðu því valkostinn **Vinna sjálfkrafa** stilltan á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="24ba1-122">Í reitinn **Kenni vinnuhóps** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="24ba1-123">Hægt er að nota kenni vinnuhópa til að skipuleggja vinnu í flokka.</span><span class="sxs-lookup"><span data-stu-id="24ba1-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="24ba1-124">Gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem er stofnuð með þessu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="24ba1-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="24ba1-125">Í svæðinu **Vinnuforgangur** færirðu inn `1`.</span><span class="sxs-lookup"><span data-stu-id="24ba1-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="24ba1-126">Þetta tilgreinir mikilvægi vinnu og gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem eru stofnaðir með þessu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="24ba1-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="24ba1-127">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-127">Select **Save**.</span></span> <span data-ttu-id="24ba1-128">Vista verður haus vinnusniðmáts áður en hnappurinn **Breyta fyrirspurn** verður tiltækur.</span><span class="sxs-lookup"><span data-stu-id="24ba1-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="24ba1-129">Setja upp fyrirspurn fyrir vinnusniðmátið</span><span class="sxs-lookup"><span data-stu-id="24ba1-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="24ba1-130">Veldu **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-130">Select **Edit query**.</span></span> <span data-ttu-id="24ba1-131">Við setjum takmörkun þannig að sniðmátið getur einungis verið notuð í ákveðnu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="24ba1-132">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-132">Select **Add**.</span></span>
3. <span data-ttu-id="24ba1-133">Í reitnum **Reitur** í nýju línunni slærðu inn `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="24ba1-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="24ba1-134">Í reitnum **Skilyrði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="24ba1-135">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-135">Select **OK**.</span></span>
6. <span data-ttu-id="24ba1-136">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="24ba1-137">Stilla upplýsingar vinnusniðmáts</span><span class="sxs-lookup"><span data-stu-id="24ba1-137">Set work template details</span></span>
1. <span data-ttu-id="24ba1-138">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-138">Select **New**.</span></span>
2. <span data-ttu-id="24ba1-139">Í reitnum **Vinnutegund** velurðu **Tína**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="24ba1-140">í reitinn **Kenni vinnuklasa** slærðu inn `purchase`.</span><span class="sxs-lookup"><span data-stu-id="24ba1-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="24ba1-141">Vinnuklasa sem valin er hér verður sjálfkrafa í öllum vinnulínum af gerðinni Tiltekt sem eru stofnaðir með þessu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="24ba1-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="24ba1-142">Vinnuklasinn er ekki hægt að hnekkja frá vinnu pöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="24ba1-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="24ba1-143">Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlínur sem starfsmanns vöruhús getur vinna í farsíma.</span><span class="sxs-lookup"><span data-stu-id="24ba1-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="24ba1-144">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-144">Select **New**.</span></span>
5. <span data-ttu-id="24ba1-145">Í reitnum **Verkbeiðni** velurðu **Frágangur**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="24ba1-146">Í reitinn **Kenni vinnuklasa** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="24ba1-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="24ba1-147">Tiltekt og frágangs leiðbeiningar eru stilltar.</span><span class="sxs-lookup"><span data-stu-id="24ba1-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="24ba1-148">Tiltektar-/frágangspör verða að hafa sama vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="24ba1-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="24ba1-149">Notið sama vinnuklasa sem fram voru lögð fyrir tiltektarfyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="24ba1-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="24ba1-150">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-150">Select **Save**.</span></span> <span data-ttu-id="24ba1-151">Athugaðu að núna er merkt í gátreitinn **Gildir**.</span><span class="sxs-lookup"><span data-stu-id="24ba1-151">Note that the **Valid** checkbox is now checked.</span></span>  

