--- 
title: "Setja upp vinnusniðmát fyrir innkaupapantanir"
description: "Þetta ferli leggur áherslu á setja upp einfaldar vinnusniðmáts sem nota á þegar taka á frá mótteknar vörur."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4c388a8ed6a852a92caa3a1eff2d0e8017694bcd
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="7a78e-103">Setja upp vinnusniðmát fyrir innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="7a78e-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a78e-104">Þetta ferli leggur áherslu á setja upp einfaldar vinnusniðmáts sem nota á þegar taka á frá mótteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="7a78e-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="7a78e-105">Vinnusniðmát ákvarða safn leiðbeiningarnar sem birtast starfsmanns vöruhús í farsíma þegar fluttar eru vörur frá móttöku svæði.</span><span class="sxs-lookup"><span data-stu-id="7a78e-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="7a78e-106">Hægt er að nota þessi ferli með gögn sem eru nefnd í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="7a78e-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="7a78e-107">Áður en byrjað er í þessari handbók, stofna kenni vinnuhóps.</span><span class="sxs-lookup"><span data-stu-id="7a78e-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="7a78e-108">Í þessu dæmi er kenni vinnuhóps kallað inn í Á innleið notað.</span><span class="sxs-lookup"><span data-stu-id="7a78e-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="7a78e-109">Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="7a78e-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="7a78e-110">Fara í vöruhúsakerfi  > Uppsetning  > Vinna  > Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="7a78e-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="7a78e-111">Í reitnum Verkbeiðni velurðu „Innkaupapantanir“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="7a78e-112">Stofna haus fyrir sniðmát verks</span><span class="sxs-lookup"><span data-stu-id="7a78e-112">Create a work template header</span></span>
1. <span data-ttu-id="7a78e-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-113">Click New.</span></span>
2. <span data-ttu-id="7a78e-114">Í reitinn raðnúmer skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7a78e-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="7a78e-115">Þetta er númeraröð sem vinnusniðmát eru metnar fyrir.</span><span class="sxs-lookup"><span data-stu-id="7a78e-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="7a78e-116">Hægt er að breyta röð, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="7a78e-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="7a78e-117">Færa inn gildi í reitnum Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="7a78e-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="7a78e-118">Þetta er einkvæmt kenni fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="7a78e-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="7a78e-119">Færa inn gildi í reitnum lýsingu Vinnusniðmáts.</span><span class="sxs-lookup"><span data-stu-id="7a78e-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="7a78e-120">Gildur valkostur ekki athugaður þar til þú hefur verið lokið allar upplýsingar sem þörf er á í sniðmáti og ert búinn að smellt á Vista.</span><span class="sxs-lookup"><span data-stu-id="7a78e-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="7a78e-121">Vinnupöntun af gerðinni Innkaupapöntun er ekki hægt að vinna sjálfkrafa, hafðu því valkostinn vinna sjálfkrafa stillt á nei.</span><span class="sxs-lookup"><span data-stu-id="7a78e-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="7a78e-122">Færa inn gildi í reitnum Kenni Vinnuhóp .</span><span class="sxs-lookup"><span data-stu-id="7a78e-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="7a78e-123">Hægt er að nota kenni vinnuhópa til að skipuleggja vinnu í flokka.</span><span class="sxs-lookup"><span data-stu-id="7a78e-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="7a78e-124">Gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem er stofnuð með þessu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="7a78e-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="7a78e-125">Í svæðinu forgangur Vinnu, færið inn '1'.</span><span class="sxs-lookup"><span data-stu-id="7a78e-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="7a78e-126">Þetta tilgreinir mikilvægi vinnu og gildið sem er valin hér verða sjálfgildi fyrir allar vinnu sem eru stofnaðir með þessu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="7a78e-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="7a78e-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-127">Click Save.</span></span>
    * <span data-ttu-id="7a78e-128">Vista verður haus vinnusniðmáts áður en að Breyta Fyrirspurn hnappurinn verður tiltækur.</span><span class="sxs-lookup"><span data-stu-id="7a78e-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="7a78e-129">Setja upp fyrirspurn fyrir vinnusniðmátið</span><span class="sxs-lookup"><span data-stu-id="7a78e-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="7a78e-130">Smellt er á Breyta fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="7a78e-130">Click Edit query.</span></span>
    * <span data-ttu-id="7a78e-131">Við setjum takmörkun þannig að sniðmátið getur einungis verið notuð í ákveðnu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="7a78e-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="7a78e-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a78e-132">Click Add.</span></span>
3. <span data-ttu-id="7a78e-133">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7a78e-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7a78e-134">Í svæði Svæðið, færa inn "vöruhúsið".</span><span class="sxs-lookup"><span data-stu-id="7a78e-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="7a78e-135">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7a78e-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="7a78e-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-136">Click OK.</span></span>
7. <span data-ttu-id="7a78e-137">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="7a78e-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="7a78e-138">Stilla upplýsingar vinnusniðmáts</span><span class="sxs-lookup"><span data-stu-id="7a78e-138">Set work template details</span></span>
1. <span data-ttu-id="7a78e-139">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-139">Click New.</span></span>
2. <span data-ttu-id="7a78e-140">Veljið í svæðinu vinnutegund 'Taka'.</span><span class="sxs-lookup"><span data-stu-id="7a78e-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="7a78e-141">í Kenni Vinnuklasa svæðið  færðu inn 'innkaupa'.</span><span class="sxs-lookup"><span data-stu-id="7a78e-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="7a78e-142">Vinnuklasa sem valin er hér verður sjálfkrafa í öllum vinnulínum af gerðinni Tiltekt sem eru stofnaðir með þessu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="7a78e-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="7a78e-143">Vinnuklasinn er ekki hægt að hnekkja frá vinnu pöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="7a78e-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="7a78e-144">Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlínur sem starfsmanns vöruhús getur vinna í farsíma.</span><span class="sxs-lookup"><span data-stu-id="7a78e-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="7a78e-145">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-145">Click New.</span></span>
5. <span data-ttu-id="7a78e-146">Í reitnum Vinnutegund velurðu ‚Frágangur‘.</span><span class="sxs-lookup"><span data-stu-id="7a78e-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="7a78e-147">Færa inn gildi í reitnum Kenni Vinnuklasa .</span><span class="sxs-lookup"><span data-stu-id="7a78e-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="7a78e-148">Tiltekt og frágangs leiðbeiningar eru stilltar.</span><span class="sxs-lookup"><span data-stu-id="7a78e-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="7a78e-149">Tiltektar-/frágangspör verða að hafa sama vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="7a78e-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="7a78e-150">Notið sama vinnuklasa sem fram voru lögð fyrir tiltektarfyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="7a78e-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="7a78e-151">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7a78e-151">Click Save.</span></span>
    * <span data-ttu-id="7a78e-152">Athugið að Gilt gátreitinn er nú merkt.</span><span class="sxs-lookup"><span data-stu-id="7a78e-152">Note that the Valid checkbox is now checked.</span></span>  


