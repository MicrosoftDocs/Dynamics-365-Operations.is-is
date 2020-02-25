---
title: Bókun á sölu á netinu og greiðslur
description: Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf7f72be22539271649aa7f5541735b3d24dab66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022894"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="3b573-103">Bókun á sölu á netinu og greiðslur</span><span class="sxs-lookup"><span data-stu-id="3b573-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3b573-104">Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.</span><span class="sxs-lookup"><span data-stu-id="3b573-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="3b573-105">Að birta sölu og greiðslur á netinu er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="3b573-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="3b573-106">Dragðu færslugögn netviðskipta inn í HQ.</span><span class="sxs-lookup"><span data-stu-id="3b573-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="3b573-107">Samstilling pantana til að búa til sölupantanir í HQ.</span><span class="sxs-lookup"><span data-stu-id="3b573-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="3b573-108">Að draga færslugögn á netinu má gera annaðhvort handvirkt með því að keyra P-vinnslu eða með því að búa til endurtekna runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="3b573-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="3b573-109">Að keyra P-vinnsluna handvirkt</span><span class="sxs-lookup"><span data-stu-id="3b573-109">Manually running the P-job</span></span>

1. <span data-ttu-id="3b573-110">Fara í Öll vinnusvæði > Upplýsingatækni Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b573-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="3b573-111">Smelltu á Dreifingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="3b573-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="3b573-112">Veldu P-0001.</span><span class="sxs-lookup"><span data-stu-id="3b573-112">Select P-0001.</span></span>
4. <span data-ttu-id="3b573-113">Stilltu gagnagrunnshópa rásar, ef þess þarf.</span><span class="sxs-lookup"><span data-stu-id="3b573-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="3b573-114">Smellt er á Keyra núna.</span><span class="sxs-lookup"><span data-stu-id="3b573-114">Click Run now.</span></span>
6. <span data-ttu-id="3b573-115">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="3b573-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="3b573-116">Tímasetning endurtekinna P-vinnsla</span><span class="sxs-lookup"><span data-stu-id="3b573-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="3b573-117">Fara í Öll vinnusvæði > Upplýsingatækni Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b573-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="3b573-118">Smelltu á Dreifingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="3b573-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="3b573-119">Veldu P-0001.</span><span class="sxs-lookup"><span data-stu-id="3b573-119">Select P-0001.</span></span>
4. <span data-ttu-id="3b573-120">Smelltu á Stofna runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="3b573-120">Click Create batch job.</span></span>
5. <span data-ttu-id="3b573-121">Smelltu á Keyra í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="3b573-121">Click Run in the background.</span></span>
5. <span data-ttu-id="3b573-122">Virkjaðu Runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="3b573-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="3b573-123">Smelltu á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="3b573-123">Click Recurrence..</span></span>
7. <span data-ttu-id="3b573-124">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="3b573-124">Select the No end date option.</span></span>
8. <span data-ttu-id="3b573-125">Í Teljarareitnum slærðu inn millibil á milli keyrsla í mínútum.</span><span class="sxs-lookup"><span data-stu-id="3b573-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="3b573-126">Venjulega myndi þetta vera 5-10.</span><span class="sxs-lookup"><span data-stu-id="3b573-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="3b573-127">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3b573-127">Click OK.</span></span>
10. <span data-ttu-id="3b573-128">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3b573-128">Click OK.</span></span>

<span data-ttu-id="3b573-129">Hægt er að samstilla pantanir annaðhvort með því að keyra vinnsluna „Samstilla pantanir“ handvirkt eða með því að stofna endurtekna runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="3b573-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="3b573-130">Handvirk keyrsla á samstillingu pöntunar</span><span class="sxs-lookup"><span data-stu-id="3b573-130">Manually running order synchronization</span></span> 

<span data-ttu-id="3b573-131">Fylgdu þessum skrefum til að keyra starfið „Samstilla pantanir“ handvirkt einu sinni.</span><span class="sxs-lookup"><span data-stu-id="3b573-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="3b573-132">Opna Öll vinnusvæði > Fjármál verslunar.</span><span class="sxs-lookup"><span data-stu-id="3b573-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="3b573-133">Smellt er á Samstilla pantanir</span><span class="sxs-lookup"><span data-stu-id="3b573-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3b573-134">Í svæðinu stigveldi Fyrirtækis, veljið „Verslanir eftir Svæði”.</span><span class="sxs-lookup"><span data-stu-id="3b573-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="3b573-135">Annað hvort velja ákveðna verslun á netinu, eða velja hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="3b573-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3b573-136">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="3b573-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3b573-137">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="3b573-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3b573-138">Afvirkjaðu Runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="3b573-138">Disable Batch processing</span></span>
6. <span data-ttu-id="3b573-139">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="3b573-139">Click Recurrence.</span></span>
7. <span data-ttu-id="3b573-140">Veldu valkostinn lok eftir</span><span class="sxs-lookup"><span data-stu-id="3b573-140">Select End After option</span></span>
8. <span data-ttu-id="3b573-141">Í reitinn Lok eftir skal slá inn 1.</span><span class="sxs-lookup"><span data-stu-id="3b573-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="3b573-142">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3b573-142">Click OK.</span></span>
10. <span data-ttu-id="3b573-143">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3b573-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="3b573-144">Tímasetning endurteknar pöntunarsamstillingar</span><span class="sxs-lookup"><span data-stu-id="3b573-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="3b573-145">Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.</span><span class="sxs-lookup"><span data-stu-id="3b573-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="3b573-146">Þetta ferli notar sýnigögn fyrirtæki USRT.</span><span class="sxs-lookup"><span data-stu-id="3b573-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3b573-147">Opna Öll vinnusvæði > Fjármál verslunar.</span><span class="sxs-lookup"><span data-stu-id="3b573-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="3b573-148">Smellt er á Samstilla pantanir</span><span class="sxs-lookup"><span data-stu-id="3b573-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3b573-149">Í svæðinu stigveldi Fyrirtækis, veljið „Verslanir eftir Svæði”.</span><span class="sxs-lookup"><span data-stu-id="3b573-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="3b573-150">Annað hvort velja ákveðna verslun á netinu, eða velja hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.</span><span class="sxs-lookup"><span data-stu-id="3b573-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3b573-151">Smella á örina til að bæta vali.</span><span class="sxs-lookup"><span data-stu-id="3b573-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3b573-152">Smella á Keyra í bakgrunni flipanum.</span><span class="sxs-lookup"><span data-stu-id="3b573-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3b573-153">Virkjaðu Runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="3b573-153">Enable Batch processing</span></span>
6. <span data-ttu-id="3b573-154">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="3b573-154">Click Recurrence.</span></span>
7. <span data-ttu-id="3b573-155">Velja Valkosturinn enginn valkostur um lokadag.</span><span class="sxs-lookup"><span data-stu-id="3b573-155">Select the No end date option.</span></span>
8. <span data-ttu-id="3b573-156">Í Teljarareitnum slærðu inn millibil á milli keyrsla í mínútum.</span><span class="sxs-lookup"><span data-stu-id="3b573-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="3b573-157">Venjulega myndi þetta vera 2-20</span><span class="sxs-lookup"><span data-stu-id="3b573-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="3b573-158">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3b573-158">Click OK.</span></span>
10. <span data-ttu-id="3b573-159">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3b573-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="3b573-160">Gagnaeiningar sem taka þátt í ferlinu</span><span class="sxs-lookup"><span data-stu-id="3b573-160">Data entities involved in the process</span></span>

- <span data-ttu-id="3b573-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="3b573-161">RetailTransactionTable</span></span>
- <span data-ttu-id="3b573-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="3b573-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="3b573-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="3b573-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="3b573-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="3b573-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="3b573-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="3b573-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="3b573-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="3b573-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="3b573-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="3b573-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="3b573-171">RetailTransactionAttributeTrans</span></span>
