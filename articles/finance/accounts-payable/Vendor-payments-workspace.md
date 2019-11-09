---
title: Vinnusvæði greiðslna lánardrottna
description: Þetta efnisatriði veitir upplýsingar um lánardrottnagreiðslu á fartækjavinnusvæði. Vinnusvæði greiðslur Lánardrottins sýnir upplýsingar sem tengjast vinnslu greiðslur til lánardrottna.
author: abruer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89ba0d68bd52413328dd583e87b09b01fd523d6f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178361"
---
# <a name="vendor-payments-workspace"></a><span data-ttu-id="78a61-104">Vinnusvæði greiðslna lánardrottna</span><span class="sxs-lookup"><span data-stu-id="78a61-104">Vendor payments workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78a61-105">Vinnusvæði **Greiðslur Lánardrottins** sýnir upplýsingar sem tengjast vinnslu greiðslur til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="78a61-105">The **Vendor payments** workspace shows information that is related to the processing of vendor payments.</span></span> <span data-ttu-id="78a61-106">Í þessu vinnusvæði er yfirlitið **Mín vinna** og síðan **Greiningar**.</span><span class="sxs-lookup"><span data-stu-id="78a61-106">This workspace includes a **My work** view and an **Analytics** page.</span></span> <span data-ttu-id="78a61-107">Í **Mínar vinnu** skoða sýnir samantekt tiles hnitanet færslu lánardrottins og tengdar lánardrottnaupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="78a61-107">The **My work** view shows summary tiles, vendor transaction grids, and related vendor information.</span></span> <span data-ttu-id="78a61-108">Síðan **Greiningar** notar getu Microsoft Power BI til að sýna myndefni sem tengjast stöðum greiðslum lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="78a61-108">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to vendor payments.</span></span>

## <a name="setup-needed-to-view-power-bi-content"></a><span data-ttu-id="78a61-109">Uppsetningu þarf til að skoða efni Power BI</span><span class="sxs-lookup"><span data-stu-id="78a61-109">Setup needed to view Power BI content</span></span>

<span data-ttu-id="78a61-110">Eftirfarandi uppsetningu þarf að vera lokið svo að gögn birtist í myndefni **Greiðslur lánardrottna** Power BI.</span><span class="sxs-lookup"><span data-stu-id="78a61-110">The following setup needs to be completed for data to display in **Vendor payments** Power BI visuals.</span></span>
1. <span data-ttu-id="78a61-111">Farðu í **Kerfisstjórnun > Uppsetning > Kerfisfæribreytur** til að stilla **Kerfisgjaldmiðil** og **Kerfisgengi**.</span><span class="sxs-lookup"><span data-stu-id="78a61-111">Go to **System administration > Setup > System Parameters** to set **System currency** and **System Exchange Rate**.</span></span>
2. <span data-ttu-id="78a61-112">Farðu í **Fjárhag > Uppsetning > Fjárhag** til að stilla **Bókhaldsgjaldmiðil** og **Gerð gengis**.</span><span class="sxs-lookup"><span data-stu-id="78a61-112">Go to **General Ledger > Setup > Ledger**  to set **Accounting Currency** and **Exchange Rate Type**.</span></span> 
2. <span data-ttu-id="78a61-113">Skilgreindu gengi á milli færslugjaldmiðla og bókhaldsgjaldmiðils, bókhaldsgjaldmiðils og kerfisgjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="78a61-113">Define exchange rates between Transaction currencies and Accounting currency, Accounting currency and System currency.</span></span> <span data-ttu-id="78a61-114">Til að gera þetta skaltu fara í **Fjárhag> Gjaldmiðla> Gengi gjaldmiðla**.</span><span class="sxs-lookup"><span data-stu-id="78a61-114">To do this, go to **General Ledger > Currencies > Currency exchange rates**.</span></span>
3. <span data-ttu-id="78a61-115">Farðu í **Kerfisstjórnun > Uppsetning > Einingaverslun** til að endurnýja uppsafnaða mælingu **VendPaymentBIMeasure**.</span><span class="sxs-lookup"><span data-stu-id="78a61-115">Go to **System administration > Setup > Entity Store** to refresh the **VendPaymentBIMeasure** aggregate measurement.</span></span> 

## <a name="my-work-view"></a><span data-ttu-id="78a61-116">Skoða Mína vinnu</span><span class="sxs-lookup"><span data-stu-id="78a61-116">My work view</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="78a61-117">Samantektarreitir</span><span class="sxs-lookup"><span data-stu-id="78a61-117">Summary tiles</span></span>

<span data-ttu-id="78a61-118">Reitirnir í hlutanum **Samantekt** veita yfirlit yfir stöðu greiðsluupplýsinganna.</span><span class="sxs-lookup"><span data-stu-id="78a61-118">The tiles in the **Summary** section give an overview of the state of your payment information.</span></span> <span data-ttu-id="78a61-119">Hægt er að skoða greiðslubækur sem ekki hafa enn verið bókaðar, reikninga sem eru fram yfir gjalddaga, alla lánardrottna og viðskiptavini sem eru í bið.</span><span class="sxs-lookup"><span data-stu-id="78a61-119">You can see payment journals that aren't yet posted, invoices that are past due, all vendors, and vendors that are on hold.</span></span> <span data-ttu-id="78a61-120">Frá því **Samantekt** hluta, er hægt að stofna nýja launatímabili.</span><span class="sxs-lookup"><span data-stu-id="78a61-120">From the **Summary** section, you can create a new pay run.</span></span>

<span data-ttu-id="78a61-121">Upplýsingum í **Samantekt** hluti er fyrir fyrirtækið sem er afskriftareglur skráður í.</span><span class="sxs-lookup"><span data-stu-id="78a61-121">The information in the **Summary** section is for the company that you're signed in to.</span></span>

### <a name="vendor-transactions-grids"></a><span data-ttu-id="78a61-122">Færslur lánardrottna hnitanet</span><span class="sxs-lookup"><span data-stu-id="78a61-122">Vendor transactions grids</span></span>

<span data-ttu-id="78a61-123">Hlutinn **Lánardrottnafærslur** inniheldur hnitanet sem sýnir reikninga sem eru gjaldfallnir og greiðslur sem ekki eru jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="78a61-123">The **Vendor transactions** section contains grids that show the invoices that are past due and payments that aren't settled.</span></span> <span data-ttu-id="78a61-124">Úr hnitanetinu **Gjaldfallnir reikningar** er hægt að skoða jöfnunarsögu fyrir valinn reikning.</span><span class="sxs-lookup"><span data-stu-id="78a61-124">From the **Invoices past due** grid, you can view the settlement history for a selected invoice.</span></span> <span data-ttu-id="78a61-125">Úr hnitanetinu **Ójafnaðar greiðslur** er hægt að skoða jöfnunarsögu fyrir valinn reikning og jafna reikning.</span><span class="sxs-lookup"><span data-stu-id="78a61-125">From the **Payments not settled** grid, you can view the settlement history for a selected invoice and settle an invoice.</span></span>

<span data-ttu-id="78a61-126">Sé æskilegt að miðstýrðum greiðslum sölumenn með síu sem birtist efst á hverja hnitanetinu til að velja fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="78a61-126">Centralized payment clerks can use a filter that appears at the top of each grid to select a company.</span></span> <span data-ttu-id="78a61-127">Taflan er síðan síuð þannig að það sýnir einungis fyrirtækin sem eru skilgreindar á miðstýrðum greiðslum stigveldisskipan sem afgreiðslumaður miðstýrðum greiðslum hafi heimildir til að skoða.</span><span class="sxs-lookup"><span data-stu-id="78a61-127">The grid is then filtered so that it shows only those companies that are defined in the centralized payment organizational hierarchy that the centralized payment clerk has rights to view.</span></span>

<span data-ttu-id="78a61-128">Í **Finna færslur** flipanum á **lánardrottnafærslur** hlutanum kleift að leita í færslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="78a61-128">The **Find transactions** tab in the **Vendor transactions** section lets you search for a vendor transaction.</span></span>

### <a name="related-information"></a><span data-ttu-id="78a61-129">Tengdar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="78a61-129">Related information</span></span>

<span data-ttu-id="78a61-130">Hægt er að skoða í **Lánardrottins aldursgreiningarramma** skýrslu og **samantekt Greiðslu með** skýrslu með því að nota tenglana í í **Tengdar upplýsingar** hluta vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="78a61-130">You can view the **Vendor aging** report and the **Payment summary by date** report by using the links in the **Related information** section of the workspace.</span></span>

## <a name="analytics-page"></a><span data-ttu-id="78a61-131">Greiningasíða</span><span class="sxs-lookup"><span data-stu-id="78a61-131">Analytics page</span></span>

<span data-ttu-id="78a61-132">Í **Samantektarlíkön** síða veitir mikilvæg mælikvörðum, svo sem reikninga lánardrottna sem eru fram gjalddaga og reikningar lánardrottins sem hafa gjalddaga í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="78a61-132">The **Analytics** page provides important metrics, such as vendor invoices that are past due and vendor invoices that are due in the future.</span></span> <span data-ttu-id="78a61-133">Þessi síða inniheldur níu skýrslusíður.</span><span class="sxs-lookup"><span data-stu-id="78a61-133">This page contains nine report pages.</span></span> <span data-ttu-id="78a61-134">Ein síða veitir yfirlit og aðrar átta síður veita upplýsingar um Reikninga lánardrottna greiðslu mælikvörðum.</span><span class="sxs-lookup"><span data-stu-id="78a61-134">One page provides an overview, and the other eight pages provide details about Accounts payable payment metrics.</span></span>

<span data-ttu-id="78a61-135">Eftirfarandi tafla sýnir sýnigögn sem eru tiltæk á hverri skýrslusíðu.</span><span class="sxs-lookup"><span data-stu-id="78a61-135">The following table shows the visualizations that are available on each report page.</span></span>


|            <span data-ttu-id="78a61-136">Skýrslusíða</span><span class="sxs-lookup"><span data-stu-id="78a61-136">Report page</span></span>            |                                                                                                                                                                                <span data-ttu-id="78a61-137">Myndbirting</span><span class="sxs-lookup"><span data-stu-id="78a61-137">Visualization</span></span>                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="78a61-138">Yfirlit yfir greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="78a61-138">Vendor payments overview</span></span>      | <ul><li><span data-ttu-id="78a61-139">Gjaldfallnir reikningar</span><span class="sxs-lookup"><span data-stu-id="78a61-139">Invoices past due</span></span></li><li><span data-ttu-id="78a61-140">Reikningar á gjalddaga í dag</span><span class="sxs-lookup"><span data-stu-id="78a61-140">Invoices due today</span></span></li><li><span data-ttu-id="78a61-141">Afslættir gerð tapað afslætti</span><span class="sxs-lookup"><span data-stu-id="78a61-141">Discounts taken to discounts lost</span></span></li><li><span data-ttu-id="78a61-142">Reikningar til greiðslu í framtíðinni eftir staðgreiðsluafsláttardagsetningu</span><span class="sxs-lookup"><span data-stu-id="78a61-142">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="78a61-143">Reikningar til greiðslu í framtíðinni eftir gjalddaga</span><span class="sxs-lookup"><span data-stu-id="78a61-143">Invoices due in future by due date</span></span></li><li><span data-ttu-id="78a61-144">Reikningar greiddir seint reikningar greiddir tímanlega</span><span class="sxs-lookup"><span data-stu-id="78a61-144">Invoices paid late to invoices paid on time</span></span></li><li><span data-ttu-id="78a61-145">Greiðsluverkflæðisúthlutun</span><span class="sxs-lookup"><span data-stu-id="78a61-145">Payment workflow assignment</span></span></li><li><span data-ttu-id="78a61-146">Staða lánardrottins/viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="78a61-146">Vendor to customer balance</span></span></li><li><span data-ttu-id="78a61-147">Opnir reikningar með greiðslubið</span><span class="sxs-lookup"><span data-stu-id="78a61-147">Open invoices with payment hold</span></span></li></ul> |
|         <span data-ttu-id="78a61-148">Gjaldfallnir reikningar</span><span class="sxs-lookup"><span data-stu-id="78a61-148">Invoices past due</span></span>         |                                                                                             <ul><li><span data-ttu-id="78a61-149">Gjaldfallnir reikningar</span><span class="sxs-lookup"><span data-stu-id="78a61-149">Invoices past due</span></span></li><li><span data-ttu-id="78a61-150">Gjalddagaupplýsingar reikninga</span><span class="sxs-lookup"><span data-stu-id="78a61-150">Invoices past due details</span></span></li><li><span data-ttu-id="78a61-151">Samtala opinna reikninga</span><span class="sxs-lookup"><span data-stu-id="78a61-151">Total open invoices</span></span></li><li><span data-ttu-id="78a61-152">Gjaldfallnir reikningar eftir lánardrottnahóp</span><span class="sxs-lookup"><span data-stu-id="78a61-152">Invoices past due per vendor group</span></span></li><li><span data-ttu-id="78a61-153">Gjaldfallnir reikningar á hvert fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-153">Invoices past due per company</span></span></li></ul>                                                                                              |
|        <span data-ttu-id="78a61-154">Reikningar á gjalddaga í dag</span><span class="sxs-lookup"><span data-stu-id="78a61-154">Invoices due today</span></span>         |                                                                                                         <ul><li><span data-ttu-id="78a61-155">Reikningar á gjalddaga í dag</span><span class="sxs-lookup"><span data-stu-id="78a61-155">Invoices due today</span></span></li><li><span data-ttu-id="78a61-156">Upplýsingar um reikninga á gjalddaga í dag</span><span class="sxs-lookup"><span data-stu-id="78a61-156">Invoices due today details</span></span></li><li><span data-ttu-id="78a61-157">Rikningar gjaldfallnir í dag á hvert fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-157">Invoices due today per company</span></span></li><li><span data-ttu-id="78a61-158">Reikningar gjaldfallnir í dag eftir lánardrottnahóp</span><span class="sxs-lookup"><span data-stu-id="78a61-158">Invoices due today per vendor group</span></span></li></ul>                                                                                                          |
| <span data-ttu-id="78a61-159">Afslættir gerð tapað afslætti</span><span class="sxs-lookup"><span data-stu-id="78a61-159">Discounts taken to discounts lost</span></span> |                                                                             <ul><li><span data-ttu-id="78a61-160">Notaður afsláttur til tapaðs afsláttar</span><span class="sxs-lookup"><span data-stu-id="78a61-160">Discounts taken to discount lost</span></span></li><li><span data-ttu-id="78a61-161">Upplýsingar um notaðan afslátt til tapaðs afsláttar</span><span class="sxs-lookup"><span data-stu-id="78a61-161">Discounts taken to discount lost details</span></span></li><li><span data-ttu-id="78a61-162">Notaður afsláttur til tapaðs afsláttar eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-162">Discounts taken to discount lost per company</span></span></li><li><span data-ttu-id="78a61-163">Notaður afsláttur til tapaðs afsláttar eftir lánardrottnahóp</span><span class="sxs-lookup"><span data-stu-id="78a61-163">Discounts taken to discount lost per vendor group</span></span></li></ul>                                                                              |
|      <span data-ttu-id="78a61-164">Reikningar gjaldfallir í framtíðinni</span><span class="sxs-lookup"><span data-stu-id="78a61-164">Invoices due in future</span></span>       |                                                 <ul><li><span data-ttu-id="78a61-165">Reikningar gjaldfallir í framtíðinni</span><span class="sxs-lookup"><span data-stu-id="78a61-165">Invoices due in future</span></span></li><li><span data-ttu-id="78a61-166">Upplýsingar um reikninga sem gjaldfalla í framtíðinni</span><span class="sxs-lookup"><span data-stu-id="78a61-166">Invoices due in future details</span></span></li><li><span data-ttu-id="78a61-167">Reikningar greiðslu í framtíðinni fyrir hvert fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-167">Invoices due in future per company</span></span></li><li><span data-ttu-id="78a61-168">Reikningar gjaldfallnir í framtíðinni eftir lánardrottnahóp</span><span class="sxs-lookup"><span data-stu-id="78a61-168">Invoices due in future per vendor group</span></span></li><li><span data-ttu-id="78a61-169">Reikningar til greiðslu í framtíðinni eftir staðgreiðsluafsláttardagsetningu</span><span class="sxs-lookup"><span data-stu-id="78a61-169">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="78a61-170">Reikningar til greiðslu í framtíðinni eftir gjalddaga</span><span class="sxs-lookup"><span data-stu-id="78a61-170">Invoices due in future by due date</span></span></li></ul>                                                  |
|        <span data-ttu-id="78a61-171">Reikningar greiddir seint</span><span class="sxs-lookup"><span data-stu-id="78a61-171">Invoices paid late</span></span>         |                                                         <ul><li><span data-ttu-id="78a61-172">Reikningar greiddir eftir gjalddaga</span><span class="sxs-lookup"><span data-stu-id="78a61-172">Invoices paid after due date</span></span></li><li><span data-ttu-id="78a61-173">Upplýsingar um reikninga greidda eftir gjalddaga</span><span class="sxs-lookup"><span data-stu-id="78a61-173">Invoices paid after due date details</span></span></li><li><span data-ttu-id="78a61-174">Reikningar greiddir eftir gjalddaga eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-174">Invoices paid after due date per company</span></span></li><li><span data-ttu-id="78a61-175">Reikningar greiddir eftir gjalddaga eftir lánardrottnahóp</span><span class="sxs-lookup"><span data-stu-id="78a61-175">Invoices paid after due date per vendor group</span></span></li><li><span data-ttu-id="78a61-176">Reikningar greiddir seint á móti reikningum greiddum tímanlega</span><span class="sxs-lookup"><span data-stu-id="78a61-176">Invoices paid late versus invoices paid on time</span></span></li></ul>                                                          |
|         <span data-ttu-id="78a61-177">Greiðsluverkflæði</span><span class="sxs-lookup"><span data-stu-id="78a61-177">Payment workflow</span></span>          |                                                                                <ul><li><span data-ttu-id="78a61-178">Verkflæðistilvik lánardrottnagreiðslna</span><span class="sxs-lookup"><span data-stu-id="78a61-178">Vendor payment workflow instances</span></span></li><li><span data-ttu-id="78a61-179">Verkflæðistilvik lánardrottnagreiðslna eftir samþykktaraðila</span><span class="sxs-lookup"><span data-stu-id="78a61-179">Vendor payment workflow instances per approver</span></span></li><li><span data-ttu-id="78a61-180">Verkflæðistilvik lánardrottnagreiðslna eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-180">Vendor payment workflow instances per company</span></span></li><li><span data-ttu-id="78a61-181">Meðaltal daga í verkflæði eftir samþykkjanda</span><span class="sxs-lookup"><span data-stu-id="78a61-181">Average days in workflow by approver</span></span></li></ul>                                                                                |
|    <span data-ttu-id="78a61-182">Staða lánardrottins/viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="78a61-182">Vendor to customer balance</span></span>     |                                                                                                                   <ul><li><span data-ttu-id="78a61-183">Staða lánardrottins/viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="78a61-183">Vendor to customer balance</span></span></li><li><span data-ttu-id="78a61-184">Staða lánardrottins/viðskiptavinar eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-184">Vendor to customer balance per company</span></span></li><li><span data-ttu-id="78a61-185">Upplýsingar um stöðu lánardrottins/viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="78a61-185">Vendor to customer balance details</span></span></li></ul>                                                                                                                    |
|    <span data-ttu-id="78a61-186">Reikningar með greiðslubið</span><span class="sxs-lookup"><span data-stu-id="78a61-186">Invoices with payment hold</span></span>     |                                                                                         <ul><li><span data-ttu-id="78a61-187">Reikningar með greiðslubið</span><span class="sxs-lookup"><span data-stu-id="78a61-187">Invoices with payment hold</span></span></li><li><span data-ttu-id="78a61-188">Reikningar með upplýsingar um greiðslubið</span><span class="sxs-lookup"><span data-stu-id="78a61-188">Invoices with payment hold details</span></span></li><li><span data-ttu-id="78a61-189">Reikningar með greiðslubið eftir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="78a61-189">Invoices with payment hold per company</span></span></li><li><span data-ttu-id="78a61-190">Reikningar með greiðslubið eftir lánardrottnahóp</span><span class="sxs-lookup"><span data-stu-id="78a61-190">Invoices with payment hold per vendor group</span></span></li></ul>                                                                                          |
