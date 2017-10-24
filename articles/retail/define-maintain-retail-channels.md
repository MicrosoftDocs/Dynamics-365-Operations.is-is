---
title: "Skilgreina og viðhalda Smásölurásir"
description: "Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem smásöluverslanir í Microsoft Dynamics 365 for Retail. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp smásöluverslun."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 700b8868a68be7f0172202d737b4f1ae9813ecf3
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="410a2-104">Skilgreina og viðhalda Smásölurásir</span><span class="sxs-lookup"><span data-stu-id="410a2-104">Define and maintain retail channels</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="410a2-105">Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem smásöluverslanir í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="410a2-105">This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="410a2-106">Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp smásöluverslun.</span><span class="sxs-lookup"><span data-stu-id="410a2-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="410a2-107">Dynamics 365 for Retail styður fjölda smásölurása, þ.m.t. netverslanir, þjónustuver og verslanir á staðnum.</span><span class="sxs-lookup"><span data-stu-id="410a2-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="410a2-108">Verslun á staðnum er kölluð smásöluverslun.</span><span class="sxs-lookup"><span data-stu-id="410a2-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="410a2-109">Hvert smásöluverslun getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="410a2-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="410a2-110">Setja verður upp allar þessar einingar fyrir smásöluverslun áður en hún er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="410a2-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="410a2-111">Eftir að þú stofnar smásöluverslun, úthluta þér afurðir sem þú vilt að verslunin selji.</span><span class="sxs-lookup"><span data-stu-id="410a2-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="410a2-112">Einnig er starfsmönnum, afgreiðslukössum og viðskiptavinum úthlutað til verslunar.</span><span class="sxs-lookup"><span data-stu-id="410a2-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="410a2-113">Að lokum bætirðu nýju versluninni við stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="410a2-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="410a2-114">Setja upp smásöluverslanir</span><span class="sxs-lookup"><span data-stu-id="410a2-114">Setting up retail stores</span></span>
<span data-ttu-id="410a2-115">Áður en hægt er að setja upp smásöluverslun í Dynamics 365 for Retail verður þú að ljúka nokkrum frumskilyrðisverkefni.</span><span class="sxs-lookup"><span data-stu-id="410a2-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="410a2-116">Hægt er að stofna smásöluverslunar og bæta við upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="410a2-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="410a2-117">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="410a2-117">Prerequisites</span></span>

<span data-ttu-id="410a2-118">Áður en hægt er að setja upp smásöluverslun, verður að ljúka við eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="410a2-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="410a2-119">Skilgreina skipulag fyrirtækis þíns og setja upp stigveldi fyrirtækis fyrir smásöluúrval, áfyllingar og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="410a2-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="410a2-120">Setja upp vöruhús til að tákna smásöluverslun.</span><span class="sxs-lookup"><span data-stu-id="410a2-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="410a2-121">Setja upp númeraraðir fyrir smásöluverslanir, verslunaruppgjör og uppgjör fylgiskjöl.</span><span class="sxs-lookup"><span data-stu-id="410a2-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="410a2-122">Skilgreina færibreytur fyrir smásölu.</span><span class="sxs-lookup"><span data-stu-id="410a2-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="410a2-123">Setja upp greiðsluhátt sem verslunin tekur á móti.</span><span class="sxs-lookup"><span data-stu-id="410a2-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="410a2-124">Til að vinna úr kreditkortafærslum á sölustað (POS) smásölukassa, er einnig hægt að setja upp greiðsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="410a2-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="410a2-125">Setja upp VSK-flokka.</span><span class="sxs-lookup"><span data-stu-id="410a2-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="410a2-126">Setja upp smásöluafurðir.</span><span class="sxs-lookup"><span data-stu-id="410a2-126">Set up retail products.</span></span> <span data-ttu-id="410a2-127">Sem hluti af þessu verki, er einnig sett upp stigveldi smásöluafurðar, afurðarafbrigði og úrvali afurða.</span><span class="sxs-lookup"><span data-stu-id="410a2-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="410a2-128">Setja upp verðflokka afurðar.</span><span class="sxs-lookup"><span data-stu-id="410a2-128">Set up product price groups.</span></span>
10. <span data-ttu-id="410a2-129">Setja upp verðlagningu smásöluafurða.</span><span class="sxs-lookup"><span data-stu-id="410a2-129">Set up retail product pricing.</span></span> <span data-ttu-id="410a2-130">Sem hluti af þessu verki, er einnig sett upp verðleiðrétting, afslættir og afsláttartímabil.</span><span class="sxs-lookup"><span data-stu-id="410a2-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="410a2-131">Setja upp starfsfólk</span><span class="sxs-lookup"><span data-stu-id="410a2-131">Set up staff members.</span></span> <span data-ttu-id="410a2-132">**Ábending:** einnig verður að úthluta viðeigandi heimildir fyrir starfsmenn, þannig að þeir geti skráð sig inn og framkvæma verkefni með því að nota Dynamics 365 for Retail fyrir Retail POS.</span><span class="sxs-lookup"><span data-stu-id="410a2-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="410a2-133">Skilgreina skal Retail POS forstillingar til að tengja við verslun.</span><span class="sxs-lookup"><span data-stu-id="410a2-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="410a2-134">Þetta felur í sér mörg verk, s.s. uppsetningu afgreiðslukassa, uppsetningu ótengt snið, og uppsetning snið kvittunar og forstillingar.</span><span class="sxs-lookup"><span data-stu-id="410a2-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="410a2-135">Fara yfir öll verk í sem eru innifalin í þessum frumskilyrðum, og ljúka aðeins þeim verkum sem eiga við þig.</span><span class="sxs-lookup"><span data-stu-id="410a2-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="410a2-136">Setja upp smásöluverslun</span><span class="sxs-lookup"><span data-stu-id="410a2-136">Set up a retail store</span></span>

<span data-ttu-id="410a2-137">Eftir að þú hefur lokið við frumskilyrðisverk skaltu ljúka þessum verkefnum til að setja upp upplýsingar fyrir smásöluverslun:</span><span class="sxs-lookup"><span data-stu-id="410a2-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="410a2-138">Stofna smásöluverslun.</span><span class="sxs-lookup"><span data-stu-id="410a2-138">Create a retail store.</span></span>
2.  <span data-ttu-id="410a2-139">Úthluta VSK-flokki á verslunina.</span><span class="sxs-lookup"><span data-stu-id="410a2-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="410a2-140">Úthluta viðurkenndum greiðsluaðferðum á verslun.</span><span class="sxs-lookup"><span data-stu-id="410a2-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="410a2-141">Bæta upplýsingum við afurðalýsingar fyrir afurðir sem á að bjóða í verslununum smásölu.</span><span class="sxs-lookup"><span data-stu-id="410a2-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="410a2-142">Til dæmis er hægt að bæta rtf-texta og myndum.</span><span class="sxs-lookup"><span data-stu-id="410a2-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="410a2-143">Þessar upplýsingar um afurð birst í mismunandi samhengi. eins og á afgreiðslukassa Sölustaðar eða prentaðir merkimiðar.</span><span class="sxs-lookup"><span data-stu-id="410a2-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="410a2-144">Bæta versluninni við sjálfgefið stigveldi fyrirtækis sem er úthlutað á málefni fyrir **vöruúrval smásölu**, **smásöluáfyllingu** eða **skýrslugerð í smásölu**.</span><span class="sxs-lookup"><span data-stu-id="410a2-144">Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="410a2-145">Eftir að þú setur upp smásöluverslun</span><span class="sxs-lookup"><span data-stu-id="410a2-145">After you set up a retail store</span></span>

<span data-ttu-id="410a2-146">Eftir að þú slærð inn upplýsingar fyrir smásöluverslun þarf að ljúka þessum verkum til að senda ný gögn smásöluverslunarinnar til Retail POS:</span><span class="sxs-lookup"><span data-stu-id="410a2-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="410a2-147">Skilgreina afgreiðslukassa sölustaðar fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="410a2-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="410a2-148">Úthluta vöruúrvali á verslunina.</span><span class="sxs-lookup"><span data-stu-id="410a2-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="410a2-149">Vinna úr úrvali til að mynda lista yfir afurðir sem eru teknar með í úrvalið og til að nálgast afurðir í smásöluverslunar.</span><span class="sxs-lookup"><span data-stu-id="410a2-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="410a2-150">Senda gögn eins og númeraraðir, vélbúnaðarreglur, útlit afgreiðsluskjás sölustaðar til afgreiðslukassi.</span><span class="sxs-lookup"><span data-stu-id="410a2-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="410a2-151">Birta smásöluverslun til að senda gögn Retail POS.</span><span class="sxs-lookup"><span data-stu-id="410a2-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="410a2-152">Keyra vinnslur til að senda gögn verslunar til  Retail POS.</span><span class="sxs-lookup"><span data-stu-id="410a2-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="410a2-153">Stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="410a2-153">Organization hierarchies</span></span>
<span data-ttu-id="410a2-154">Retail notar stigveldi stofnunar fyrir uppbyggingu smásölurás.</span><span class="sxs-lookup"><span data-stu-id="410a2-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="410a2-155">Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri.</span><span class="sxs-lookup"><span data-stu-id="410a2-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="410a2-156">Þegar að settar eru upp verslanir er hægt að bæta þeim við stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="410a2-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="410a2-157">Verslanir deila sem notaður er fyrir úrval áfyllingar og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="410a2-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




