---
title: Skilgreina og viðhalda Smásölurásir
description: Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem verslanir í Dynamics 365 Commerce. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp verslun.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057915"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="751b5-104">Skilgreina og vinna með smásölurásir</span><span class="sxs-lookup"><span data-stu-id="751b5-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="751b5-105">Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem verslanir í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="751b5-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="751b5-106">Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp verslun.</span><span class="sxs-lookup"><span data-stu-id="751b5-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="751b5-107">Commerce styður fjölda smásölurása, þ.m.t. netverslanir og markaðstorg á netinu og verslanir á staðnum.</span><span class="sxs-lookup"><span data-stu-id="751b5-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="751b5-108">Verslun á staðnum er kölluð verslun.</span><span class="sxs-lookup"><span data-stu-id="751b5-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="751b5-109">Hver verslun getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="751b5-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="751b5-110">Setja verður upp allar þessar einingar fyrir verslun áður en hún er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="751b5-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="751b5-111">Eftir að þú stofnar verslun, úthluta þér afurðir sem þú vilt að verslunin selji.</span><span class="sxs-lookup"><span data-stu-id="751b5-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="751b5-112">Einnig er starfsmönnum, afgreiðslukössum og viðskiptavinum úthlutað til verslunar.</span><span class="sxs-lookup"><span data-stu-id="751b5-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="751b5-113">Að lokum bætirðu nýju versluninni við stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="751b5-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="751b5-114">Setja upp verslanir</span><span class="sxs-lookup"><span data-stu-id="751b5-114">Setting up stores</span></span>

<span data-ttu-id="751b5-115">Áður en þú getur sett upp verslun í Commerce verður þú að ljúka nokkrum frumskilyrðisverkefnum.</span><span class="sxs-lookup"><span data-stu-id="751b5-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="751b5-116">Hægt er að stofna verslunar og bæta við upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="751b5-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="751b5-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="751b5-117">Prerequisites</span></span>

<span data-ttu-id="751b5-118">Áður en hægt er að setja upp verslun, verður að ljúka við eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="751b5-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="751b5-119">Skilgreina skipulag fyrirtækis þíns og setja upp stigveldi fyrirtækis fyrir smásöluúrval, áfyllingar og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="751b5-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="751b5-120">Setja upp vöruhús til að tákna verslun.</span><span class="sxs-lookup"><span data-stu-id="751b5-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="751b5-121">Setja upp númeraraðir fyrir verslanir, verslunaruppgjör og uppgjör fylgiskjöl.</span><span class="sxs-lookup"><span data-stu-id="751b5-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="751b5-122">Skilgreina færibreytur fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="751b5-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="751b5-123">Setja upp greiðsluhátt sem verslunin tekur á móti.</span><span class="sxs-lookup"><span data-stu-id="751b5-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="751b5-124">Til að vinna úr kreditkortafærslum á sölustað (POS) kassa, er einnig hægt að setja upp greiðsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="751b5-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="751b5-125">Setja upp VSK-flokka.</span><span class="sxs-lookup"><span data-stu-id="751b5-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="751b5-126">Setja upp afurðir.</span><span class="sxs-lookup"><span data-stu-id="751b5-126">Set up products.</span></span> <span data-ttu-id="751b5-127">Sem hluti af þessu verki, er einnig sett upp stigveldi afurðar, afurðarafbrigði og úrvali afurða.</span><span class="sxs-lookup"><span data-stu-id="751b5-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="751b5-128">Setja upp verðflokka afurðar.</span><span class="sxs-lookup"><span data-stu-id="751b5-128">Set up product price groups.</span></span>
10. <span data-ttu-id="751b5-129">Setja upp afurðaverðlagningu.</span><span class="sxs-lookup"><span data-stu-id="751b5-129">Set up product pricing.</span></span> <span data-ttu-id="751b5-130">Sem hluti af þessu verki, er einnig sett upp verðleiðrétting, afslættir og afsláttartímabil.</span><span class="sxs-lookup"><span data-stu-id="751b5-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="751b5-131">Setja upp starfsfólk</span><span class="sxs-lookup"><span data-stu-id="751b5-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="751b5-132">Einnig verður að úthluta viðeigandi heimildum fyrir starfsmenn, þannig að þeir geti skráð sig inn og framkvæmt verkefni með því að nota kerfið POS.</span><span class="sxs-lookup"><span data-stu-id="751b5-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="751b5-133">Skilgreina skal sölustaðaforstillingar til að úthluta á verslun.</span><span class="sxs-lookup"><span data-stu-id="751b5-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="751b5-134">Þetta felur í sér mörg verk, s.s. uppsetningu afgreiðslukassa, uppsetningu ótengt snið, og uppsetning snið kvittunar og forstillingar.</span><span class="sxs-lookup"><span data-stu-id="751b5-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="751b5-135">Fara yfir öll verk í sem eru innifalin í þessum frumskilyrðum, og ljúka aðeins þeim verkum sem eiga við þig.</span><span class="sxs-lookup"><span data-stu-id="751b5-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="751b5-136">Setja upp verslun</span><span class="sxs-lookup"><span data-stu-id="751b5-136">Set up a store</span></span>

<span data-ttu-id="751b5-137">Eftir að þú hefur lokið við frumskilyrðisverk skaltu ljúka þessum verkefnum til að setja upp upplýsingar fyrir verslun:</span><span class="sxs-lookup"><span data-stu-id="751b5-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="751b5-138">Búa til verslun.</span><span class="sxs-lookup"><span data-stu-id="751b5-138">Create a store.</span></span>
2. <span data-ttu-id="751b5-139">Úthluta VSK-flokki á verslunina.</span><span class="sxs-lookup"><span data-stu-id="751b5-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="751b5-140">Úthluta viðurkenndum greiðsluaðferðum á verslun.</span><span class="sxs-lookup"><span data-stu-id="751b5-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="751b5-141">Bæta upplýsingum við afurðalýsingar fyrir afurðir sem á að bjóða í verslununum.</span><span class="sxs-lookup"><span data-stu-id="751b5-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="751b5-142">Til dæmis er hægt að bæta rtf-texta og myndum.</span><span class="sxs-lookup"><span data-stu-id="751b5-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="751b5-143">Þessar upplýsingar um afurð birst í mismunandi samhengi. eins og á afgreiðslukassa Sölustaðar eða prentaðir merkimiðar.</span><span class="sxs-lookup"><span data-stu-id="751b5-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="751b5-144">Bæta versluninni við sjálfgefið stigveldi fyrirtækis sem er úthlutað á málefni fyrir **vöruúrval smásölu**, **smásöluáfyllingu** eða **skýrslugerð í smásölu**.</span><span class="sxs-lookup"><span data-stu-id="751b5-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="751b5-145">Eftir að þú setur upp verslun</span><span class="sxs-lookup"><span data-stu-id="751b5-145">After you set up a store</span></span>

<span data-ttu-id="751b5-146">Eftir að þú slærð inn upplýsingar fyrir verslun þarf að ljúka þessum verkum til að senda ný gögn verslunarinnar til POS.</span><span class="sxs-lookup"><span data-stu-id="751b5-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="751b5-147">Skilgreina afgreiðslukassa sölustaðar fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="751b5-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="751b5-148">Úthluta vöruúrvali á verslunina.</span><span class="sxs-lookup"><span data-stu-id="751b5-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="751b5-149">Vinna úr úrvali til að mynda lista yfir afurðir sem eru teknar með í úrvalið og til að nálgast afurðir í verslunar.</span><span class="sxs-lookup"><span data-stu-id="751b5-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="751b5-150">Senda gögn eins og númeraraðir, vélbúnaðarreglur, útlit afgreiðsluskjás sölustaðar til afgreiðslukassi.</span><span class="sxs-lookup"><span data-stu-id="751b5-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="751b5-151">Birta verslun til að senda gögn verslunar til sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="751b5-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="751b5-152">Keyra vinnslur til að senda gögn verslunar til sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="751b5-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="751b5-153">Stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="751b5-153">Organization hierarchies</span></span>

<span data-ttu-id="751b5-154">Commerce notar stigveldi stofnunar fyrir uppbyggingu á rásum.</span><span class="sxs-lookup"><span data-stu-id="751b5-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="751b5-155">Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri.</span><span class="sxs-lookup"><span data-stu-id="751b5-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="751b5-156">Þegar að settar eru upp verslanir er hægt að bæta þeim við stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="751b5-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="751b5-157">Verslanir deila sem notaður er fyrir úrval áfyllingar og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="751b5-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="751b5-158">Til að nota söluaðgerðir Commerce verður stillingarlykilinn fyrir **Sent mörgum** að vera virkur.</span><span class="sxs-lookup"><span data-stu-id="751b5-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="751b5-159">Þennan stillingarlykil er að finna í lyklunum **Stillingu viðskipta** undir **Kerfisstjórnun**\> **Uppsetning** \> **Stilling leyfis**.</span><span class="sxs-lookup"><span data-stu-id="751b5-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="751b5-160">Þetta er nauðsynlegt vegna ýmissa sannprófana á grundvelli afhendingarfangs sem er stillt á sölupöntunarlínustig.</span><span class="sxs-lookup"><span data-stu-id="751b5-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

