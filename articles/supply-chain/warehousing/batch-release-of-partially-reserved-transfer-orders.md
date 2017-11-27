---
title: "Runulosun flutningspantana sem eru fráteknar að hluta"
description: "Í þessu efnisatriði er lýst hvernig eigi að setja upp aog jafna runulosun hlutafrátekinna flutningspantana úr fartæki."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="54fe1-103">Runulosun flutningspantana sem eru fráteknar að hluta</span><span class="sxs-lookup"><span data-stu-id="54fe1-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="54fe1-104">Virkni fyrir runulosun hlutafrátekinna flutningspantana gerir klefit að losa að hluta flutningspantanir til vöruhúss með því að nota runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="54fe1-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="54fe1-105">Þar sem í boði er að losa hluta magns þarf ekki að bíða eftir því að allt magn pöntunar verði tiltækt í vöruhúsi áður en pöntun er losuð.</span><span class="sxs-lookup"><span data-stu-id="54fe1-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="54fe1-106">Losun á pöntun í vöruhús er ferli í ítarlegri vöruhúsastjórnun.</span><span class="sxs-lookup"><span data-stu-id="54fe1-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="54fe1-107">Þetta ferli felur í sér aðgerðir svo sem tiltekt, pökkun og sendingu sem starfsmaður í vöruhúsi getur framkvæmt með fartæki.</span><span class="sxs-lookup"><span data-stu-id="54fe1-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="54fe1-108">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="54fe1-108">Where it applies</span></span>

<span data-ttu-id="54fe1-109">Fyrir þessa virkni eru flutningspantanir losaðar í vöruhús með því að nota runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="54fe1-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="54fe1-110">Þessi virkni er gagnleg þegar ekki eru nægilegar birgðir í vöruhúsi en þú vilt samt flytja vörur úr einu vöruhúsi í annað.</span><span class="sxs-lookup"><span data-stu-id="54fe1-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="54fe1-111">Hvernig er það sett upp</span><span class="sxs-lookup"><span data-stu-id="54fe1-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="54fe1-112">Tilgreina þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir</span><span class="sxs-lookup"><span data-stu-id="54fe1-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="54fe1-113">Áður en losa má pöntun að hluta í vöruhús í runu verður að uppfylla uppfyllingarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="54fe1-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="54fe1-114">Þessi uppfyllingarskilyrði eru ákvörðuð með uppfyllingarstefnu.</span><span class="sxs-lookup"><span data-stu-id="54fe1-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="54fe1-115">Tilgreina þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir á fyrirtækisstigi</span><span class="sxs-lookup"><span data-stu-id="54fe1-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="54fe1-116">Allt eftir uppsetning uppfyllingarreglna verður losun pantana í runu samþykkt eða hafnað.</span><span class="sxs-lookup"><span data-stu-id="54fe1-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="54fe1-117">Pantanir verða unnar í samræmi við það.</span><span class="sxs-lookup"><span data-stu-id="54fe1-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="54fe1-118">Til að stofna uppfyllingarreglur fyrir flutningspantanir og sölupantanir er smellt á **Vöruhúsastjórnun** \> **Uppsetning** \> **Losa í vöruhús** \> **Uppfyllingarregla**, og stofnaðu svo uppfyllingarreglu með því að færa inn nafn og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="54fe1-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="54fe1-119">Til að tilgreina uppfyllingartíðni, gildisgerð og skilaboð sem birtast ef uppfyllingarreglur eru brotnar, smelltu á  **Vöruhúsakerfi** \> **Uppsetning** \> **Losa í vöruhús** \> **uppfyllingarregla**, og stiltu svo reitina **uppfyllingartíðni**, **gerð gildis**, og **skilaboð vegna brota á uppfyllingu**.</span><span class="sxs-lookup"><span data-stu-id="54fe1-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="54fe1-120">Stilla þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir</span><span class="sxs-lookup"><span data-stu-id="54fe1-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="54fe1-121">Til að stilla uppfyllingarreglur fyrir flutningspantanir er smellt á **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur fyrir birgða- og vöruhúsastjórnun** \> **Flutningspantanir** \> **Vöruhúsastjórnun**, og því næst valin uppfyllingarregla fyrir flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="54fe1-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="54fe1-122">Til að stilla uppfyllingarreglur fyrir sölupantanir er smellt á **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur fyrir Viðskiptakröfur** \> **Vöruhúsastjórnun**, og því næst valin uppfyllingarregla fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="54fe1-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="54fe1-123">Leyfa losun í runu og tilgreina magn sem á að losa í runu</span><span class="sxs-lookup"><span data-stu-id="54fe1-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="54fe1-124">Runuvinnsla er notuð til að losa pantanir í vöruhús í runum.</span><span class="sxs-lookup"><span data-stu-id="54fe1-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="54fe1-125">Færibreytur sem greina að pantanir sem á að keyra í runuvinnsla eru stilltar í runuvinnslunni sjálfri.</span><span class="sxs-lookup"><span data-stu-id="54fe1-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="54fe1-126">Færibreytan **Magn** tilgreinir hvort losa á í runu allt magnið eða efnislega frátekið magn.</span><span class="sxs-lookup"><span data-stu-id="54fe1-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="54fe1-127">Færibreytan **Leyfa losun pantana sem hafa verið losaðar að hluta** ákvarðar hvort pantanir í runu á að samþykkja eða hafna ef þær voru losaðar að hluta fyrr.</span><span class="sxs-lookup"><span data-stu-id="54fe1-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="54fe1-128">Til að stilla færibreyturnar **Magn** og **Leyfa losun pantana sem hafa verið losaðar að hluta** skal smella á  **Vöruhúsastjórnun** \> **Losa í vöruhús** \> **Sjálfvirk losun flutningspantana**.</span><span class="sxs-lookup"><span data-stu-id="54fe1-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="54fe1-129">Til að stilla færibreyturnar **Magn** og **Leyfa losun pantana sem hafa verið losaðar að hluta** fyrir sölupantanir skal smella á  **Vöruhúsastjórnun** \> **Losa í vöruhús** \> **Sjálfvirk losun flutningspantana**.</span><span class="sxs-lookup"><span data-stu-id="54fe1-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

