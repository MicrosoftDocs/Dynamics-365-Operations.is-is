---
title: "Eignafærslukostir"
description: "Þessi grein lýsir mismunandi aðferðum sem eru tiltækar til að stofna eignafærslu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 48364acbaa3fff4be9440256c6b337c0e2d2d9d0
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="f70ac-103">Eignafærslukostir</span><span class="sxs-lookup"><span data-stu-id="f70ac-103">Fixed asset transaction options</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f70ac-104">Þessi grein lýsir mismunandi aðferðum sem eru tiltækar til að stofna eignafærslu.</span><span class="sxs-lookup"><span data-stu-id="f70ac-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="f70ac-105">Þú getur sett upp eign fyrir sameiningu með viðskiptaskuldir, viðskiptakröfur, innkaup og uppruna og fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f70ac-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="f70ac-106">Einnig er hægt að flytja vörur í birgðastjórnun á eignir eigi að nota þær vörur innan kerfis.</span><span class="sxs-lookup"><span data-stu-id="f70ac-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="f70ac-107">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="f70ac-107">Accounts payable</span></span>
<span data-ttu-id="f70ac-108">Hægt er að færa inn eignafærslur í síðunni færslubókarfylgiskjal.</span><span class="sxs-lookup"><span data-stu-id="f70ac-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="f70ac-109">Þessa síða er aðeins hægt að opna úr skjámyndinni reikningabók.</span><span class="sxs-lookup"><span data-stu-id="f70ac-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="f70ac-110">Einnig er hægt að opna síðuna færslubókarfylgiskjal frá síðu færslubókarsamþykkt reiknings.</span><span class="sxs-lookup"><span data-stu-id="f70ac-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="f70ac-111">Í svæðinu mótlykill, veljið eignir.</span><span class="sxs-lookup"><span data-stu-id="f70ac-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="f70ac-112">Síðan, í  mótlykill reit verður að velja númer eignar.</span><span class="sxs-lookup"><span data-stu-id="f70ac-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="f70ac-113">Á flipanum eignir færirðu inn gildi í reitina færslugerð og bók.</span><span class="sxs-lookup"><span data-stu-id="f70ac-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="f70ac-114">Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="f70ac-114">Accounts receivable</span></span>
<span data-ttu-id="f70ac-115">Hægt er að færa inn eignafærslur í síðunni reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="f70ac-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="f70ac-116">Veljið línuatriði í síðunni reikningur með frjálsum texta, í hnitanetinu reikningslínur.</span><span class="sxs-lookup"><span data-stu-id="f70ac-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="f70ac-117">Smellið á flýtiflipa „Upplýsingar um línur“.</span><span class="sxs-lookup"><span data-stu-id="f70ac-117">Click the Line details FastTab.</span></span> <span data-ttu-id="f70ac-118">Færðu inn eignanúmer og bók fyrir afskráningarfærslu.</span><span class="sxs-lookup"><span data-stu-id="f70ac-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="f70ac-119">Fyrir reikninga með valfrjálsum texta er gerð eignafærslunnar alltaf afskráninga - sala.</span><span class="sxs-lookup"><span data-stu-id="f70ac-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="f70ac-120">Innkaup og aðföng</span><span class="sxs-lookup"><span data-stu-id="f70ac-120">Procurement and sourcing</span></span>
<span data-ttu-id="f70ac-121">Hægt er að færa inn eignafærslur í síðunni innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="f70ac-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="f70ac-122">Færa skal inn allar upplýsingar sem krafist er til að búa til innkaupapöntun og síðan smella á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="f70ac-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="f70ac-123">Í síðunni innkaupapöntun, Smellið á flýtiflipa „Upplýsingar um línur“.</span><span class="sxs-lookup"><span data-stu-id="f70ac-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="f70ac-124">Síðan skal færa inn upplýsingar um eignina á flipann Eignir.</span><span class="sxs-lookup"><span data-stu-id="f70ac-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="f70ac-125">Til að bóka kaupfærslu fyrir fyrirliggjandi eign skal tilgreina eignanúmer, bók og færslutegund.</span><span class="sxs-lookup"><span data-stu-id="f70ac-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="f70ac-126">Eign er hægt að bóka ef einhvern af þessum upplýsingum vantar.</span><span class="sxs-lookup"><span data-stu-id="f70ac-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="f70ac-127">Til að bóka kaupfærslu fyrir nýja eign skal velja valkostinn ný eign? og síðan velja eignaflokk til að úthluta nýrri eign á.</span><span class="sxs-lookup"><span data-stu-id="f70ac-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="f70ac-128">Hins vegar eru engin af eignasvæðunum fyrir hendi fyrir línu ef varan er í birgðalíkanaflokki sem notar birgðalíkan staðalkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="f70ac-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="f70ac-129">Þar að auki, valkostir sem eru skilgreindar í    síðunni færibreytur eignar ákvarða hvort hægt er að bóka kaupfærslur frá innkaupaeiningum.</span><span class="sxs-lookup"><span data-stu-id="f70ac-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="f70ac-130">Þegar færslubók innkaupapöntunar eða færslubók birgða til eigna eru notaðar fyrir eignakaup hefur það áhrif á birgðavirðið.</span><span class="sxs-lookup"><span data-stu-id="f70ac-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="f70ac-131">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f70ac-131">General ledger</span></span>
<span data-ttu-id="f70ac-132">Allar gerðir eignafærsla má bóka í  síðunni almenn færslubók.</span><span class="sxs-lookup"><span data-stu-id="f70ac-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="f70ac-133">Einnig er hægt að nota færslubækur í eignum til að bóka eignafærslur.</span><span class="sxs-lookup"><span data-stu-id="f70ac-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="f70ac-134">Valkostir innfærslu á eignafærslugerðum</span><span class="sxs-lookup"><span data-stu-id="f70ac-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="f70ac-135">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="f70ac-135">Transaction type</span></span>                    | <span data-ttu-id="f70ac-136">Kerfi</span><span class="sxs-lookup"><span data-stu-id="f70ac-136">Module</span></span>                   | <span data-ttu-id="f70ac-137">Valréttarsamningar</span><span class="sxs-lookup"><span data-stu-id="f70ac-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="f70ac-138">Yfirtaka, leiðrétting kaupa</span><span class="sxs-lookup"><span data-stu-id="f70ac-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="f70ac-139">Eignir</span><span class="sxs-lookup"><span data-stu-id="f70ac-139">Fixed assets</span></span>             | <span data-ttu-id="f70ac-140">Eignir, birgðir til eigna</span><span class="sxs-lookup"><span data-stu-id="f70ac-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="f70ac-141">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f70ac-141">General ledger</span></span>           | <span data-ttu-id="f70ac-142">Almenn færslubók</span><span class="sxs-lookup"><span data-stu-id="f70ac-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="f70ac-143">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="f70ac-143">Accounts payable</span></span>         | <span data-ttu-id="f70ac-144">Reikningabók, Staðfestingarbók reiknings</span><span class="sxs-lookup"><span data-stu-id="f70ac-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="f70ac-145">Innkaup og aðföng</span><span class="sxs-lookup"><span data-stu-id="f70ac-145">Procurement and sourcing</span></span> | <span data-ttu-id="f70ac-146">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="f70ac-146">Purchase order</span></span>                            |
| <span data-ttu-id="f70ac-147">Afskrift</span><span class="sxs-lookup"><span data-stu-id="f70ac-147">Depreciation</span></span>                        | <span data-ttu-id="f70ac-148">Eignir</span><span class="sxs-lookup"><span data-stu-id="f70ac-148">Fixed assets</span></span>             | <span data-ttu-id="f70ac-149">Eignir</span><span class="sxs-lookup"><span data-stu-id="f70ac-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="f70ac-150">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f70ac-150">General ledger</span></span>           | <span data-ttu-id="f70ac-151">Almenn færslubók</span><span class="sxs-lookup"><span data-stu-id="f70ac-151">General journal</span></span>                           |
| <span data-ttu-id="f70ac-152">Losun</span><span class="sxs-lookup"><span data-stu-id="f70ac-152">Disposal</span></span>                            | <span data-ttu-id="f70ac-153">Eignir</span><span class="sxs-lookup"><span data-stu-id="f70ac-153">Fixed assets</span></span>             | <span data-ttu-id="f70ac-154">Eignir</span><span class="sxs-lookup"><span data-stu-id="f70ac-154">Fixed assets</span></span>                              |
| <span data-ttu-id="f70ac-155">** **</span><span class="sxs-lookup"><span data-stu-id="f70ac-155">** **</span></span>                               | <span data-ttu-id="f70ac-156">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f70ac-156">General ledger</span></span>           | <span data-ttu-id="f70ac-157">Almenn færslubók</span><span class="sxs-lookup"><span data-stu-id="f70ac-157">General journal</span></span>                           |
| <span data-ttu-id="f70ac-158">** **</span><span class="sxs-lookup"><span data-stu-id="f70ac-158">** **</span></span>                               | <span data-ttu-id="f70ac-159">Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="f70ac-159">Accounts receivable</span></span>      | <span data-ttu-id="f70ac-160">Textareikningur</span><span class="sxs-lookup"><span data-stu-id="f70ac-160">Free text invoice</span></span>                         |



<span data-ttu-id="f70ac-161">Frekari upplýsingar eru í [Samþætting eigna](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="f70ac-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




