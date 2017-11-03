---
title: "Rakning hlaupandi meðaltalskostnaðar á hverja birgðavídd"
description: "Hver einstök birgðavara verður að vera tengd við ákveðinn birgðavíddarflokk. Hlaupandi meðaltal kostnaðarverðs fyrir vöru er þess vegna reiknað út miðað við val birgðavídda sem er verið að rekja fjárhagslega."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb2a3a193585944810c5dfac1eb3c019e074008f
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="f8acc-104">Rakning hlaupandi meðaltalskostnaðar á hverja birgðavídd</span><span class="sxs-lookup"><span data-stu-id="f8acc-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="f8acc-105">Hver einstök birgðavara verður að vera tengd við ákveðinn birgðavíddarflokk.</span><span class="sxs-lookup"><span data-stu-id="f8acc-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="f8acc-106">Hlaupandi meðaltal kostnaðarverðs fyrir vöru er þess vegna reiknað út miðað við val birgðavídda sem er verið að rekja fjárhagslega.</span><span class="sxs-lookup"><span data-stu-id="f8acc-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="f8acc-107">Það eru þrjár gerðir af birgðavíddum: afurð, geymsla og rakning.</span><span class="sxs-lookup"><span data-stu-id="f8acc-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="f8acc-108">Vöruvíddir innihalda skilgreiningu, stærð, og lit.</span><span class="sxs-lookup"><span data-stu-id="f8acc-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="f8acc-109">Vöruvíddir eru alltaf raktar fjárhagslega.</span><span class="sxs-lookup"><span data-stu-id="f8acc-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="f8acc-110">Geymsluvíddir og rakningarvíddir innihalda staðsetningu, vöruhús, birgðastöðu, númeraplötu, rununúmer og raðnúmer.</span><span class="sxs-lookup"><span data-stu-id="f8acc-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="f8acc-111">Hægt er að velja hvaða geymsluvíddir og rakningarvíddir verða raktar fjárhagslega.</span><span class="sxs-lookup"><span data-stu-id="f8acc-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="f8acc-112">**Dæmi 1**</span><span class="sxs-lookup"><span data-stu-id="f8acc-112">**Example 1**</span></span> 

<span data-ttu-id="f8acc-113">Ef birgðavíddarflokkurinn sem er tengdur vörunni er rakinn fjárhagslega af vöruhúsinu, er hlaupandi meðaltal kostnaðarverðs reiknað út fyrir hvert vöruhús fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="f8acc-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="f8acc-114">Eftirfarandi innkaupapantanir hafa verið reikningsfærðar:</span><span class="sxs-lookup"><span data-stu-id="f8acc-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="f8acc-115">Innkaupapöntun fyrir magnið 2 á kostnaðarverði 10,00 USD hefur verið reikningsfærð fyrir vöruhús GW.</span><span class="sxs-lookup"><span data-stu-id="f8acc-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="f8acc-116">Innkaupapöntun fyrir magnið 3 á kostnaðarverði 12,00 USD hefur verið reikningsfærð fyrir vöruhús GW.</span><span class="sxs-lookup"><span data-stu-id="f8acc-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="f8acc-117">Innkaupapöntun fyrir magnið 5 á kostnaðarverði 15,00 USD hefur verið reikningsfærð fyrir vöruhús MW.</span><span class="sxs-lookup"><span data-stu-id="f8acc-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="f8acc-118">Hlaupandi meðaltal kostnaðarverðs fyrir vöruhús GW er 11,20 USD og hlaupandi meðaltal kostnaðarverðs fyrir vöruhús MW er 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="f8acc-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="f8acc-119">Sölupöntunarreikningur er bókaður fyrir vöruhús GW.</span><span class="sxs-lookup"><span data-stu-id="f8acc-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="f8acc-120">Verðmæti birgða og kostnaður seldrar vöru (áður en birgðalokun er keyrð og án merkingar) er 11,20 USD.</span><span class="sxs-lookup"><span data-stu-id="f8acc-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="f8acc-121">Önnur sölupöntun er bókuð fyrir vöruhús MW.</span><span class="sxs-lookup"><span data-stu-id="f8acc-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="f8acc-122">Verðmæti birgða og kostnaður seldrar vöru (áður en birgðalokun er keyrð og án merkingar) er 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="f8acc-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="f8acc-123">**Dæmi 2** Ef geymsluvíddaflokkur sem tengist vörunni er rakinn fjárhagslega af vöruhúsinu og rakningarvíddaflokkur er rakinn fjárhagslega af rununúmeri, reiknast hlaupandi meðaltal kostnaðarverðs fyrir hverja runu.</span><span class="sxs-lookup"><span data-stu-id="f8acc-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="f8acc-124">**Ábending:**Mælt er með því að kostnaðarverð sé alltaf skoðað fyrir allar fjárhagsvíddir sem er verið að rekja.</span><span class="sxs-lookup"><span data-stu-id="f8acc-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="f8acc-125">Eftirfarandi innkaupapantanir hafa verið reikningsfærðar:</span><span class="sxs-lookup"><span data-stu-id="f8acc-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="f8acc-126">Innkaupapöntun fyrir magnið 2 á kostnaðarverði 10,00 USD, hefur verið reikningsfært fyrir vöruhús GW og runu AAA.</span><span class="sxs-lookup"><span data-stu-id="f8acc-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="f8acc-127">Innkaupapöntun fyrir magnið 3 á kostnaðarverði 12,00 USD, hefur verið reikningsfært fyrir vöruhús GW og runu AAA.</span><span class="sxs-lookup"><span data-stu-id="f8acc-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="f8acc-128">Innkaupapöntun fyrir magnið 2 á kostnaðarverði 15,00 USD, hefur verið reikningsfært fyrir vöruhús GW og runu BBB.</span><span class="sxs-lookup"><span data-stu-id="f8acc-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="f8acc-129">Hlaupandi meðaltal kostnaðarverðs fyrir vöruhús GW og runu AAA er 11,20 USD og hlaupandi meðaltal kostnaðarverðs fyrir vöruhús GW og runu BBB er 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="f8acc-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




