---
title: Stofna áfyllingarpöntun vörusendingar
description: Þetta efni útskýrir sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018354"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="d1326-103">Stofna áfyllingarpöntun vörusendingar</span><span class="sxs-lookup"><span data-stu-id="d1326-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1326-104">Þetta efni útskýrir sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir.</span><span class="sxs-lookup"><span data-stu-id="d1326-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="d1326-105">Hún sýnir einnig hvernig á að skrá innhreyfingar afurða þannig að vörusendingabirgðir eru skráðar sem lagerbirgðir í lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="d1326-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="d1326-106">Þetta ferli myndi er yfirleitt framkvæmt af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="d1326-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="d1326-107">Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="d1326-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="d1326-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="d1326-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="d1326-109">Stofna áfyllingarpöntun vörusendingar</span><span class="sxs-lookup"><span data-stu-id="d1326-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="d1326-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Vörusending > Áfyllingarpantanir vörusendingar**.</span><span class="sxs-lookup"><span data-stu-id="d1326-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="d1326-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d1326-111">Select **New**.</span></span>
3. <span data-ttu-id="d1326-112">Í reitnum **Lánardrottnareikningur** velurðu lánardrottinn **US-104** (þú verður að velja lánardrottinn sem er skráður sem eigandi á síðunni **birgðaeigendur** ).</span><span class="sxs-lookup"><span data-stu-id="d1326-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="d1326-113">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d1326-113">Select **OK**.</span></span>
5. <span data-ttu-id="d1326-114">Veldu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="d1326-114">Select **Add line**.</span></span>
6. <span data-ttu-id="d1326-115">Í reitnum **Vörunúmer** slærðu inn `M9211CI` (þú verður að velja hlut sem er settur upp fyrir vörusendingarbirgðum).</span><span class="sxs-lookup"><span data-stu-id="d1326-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="d1326-116">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="d1326-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="d1326-117">Í reitinn **Umbeðin afhendingardagsetning** skal rita dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="d1326-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="d1326-118">Umbeðnar og staðfestar dagsetningar eru notaðar af MRP-vélinni (vél lánstímaálags) vegna áætlaðrar komu varningsins.</span><span class="sxs-lookup"><span data-stu-id="d1326-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="d1326-119">Í reitnum **Staðfestur afhendingardagur** skal rita dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="d1326-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="d1326-120">Útvíkkaðu hlutann **upplýsingar Línu**.</span><span class="sxs-lookup"><span data-stu-id="d1326-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="d1326-121">Veldu flipann **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="d1326-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="d1326-122">Til að sýna eiganda í reitnum **Eigandi birgðavídda** skal endurnýja síðuna.</span><span class="sxs-lookup"><span data-stu-id="d1326-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="d1326-123">Lánardrottininn US-104 er nú skráður sem eiganda.</span><span class="sxs-lookup"><span data-stu-id="d1326-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="d1326-124">Athugaðu staða birgðafærslunnar.</span><span class="sxs-lookup"><span data-stu-id="d1326-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="d1326-125">Veldu **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="d1326-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="d1326-126">Veldu **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="d1326-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="d1326-127">Í æskilegri línu skaltu athuga að reiturinn **Innhreyfinng** er stillt á **Pantað**.</span><span class="sxs-lookup"><span data-stu-id="d1326-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="d1326-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d1326-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="d1326-129">Taka á móti vörum</span><span class="sxs-lookup"><span data-stu-id="d1326-129">Receive items</span></span>
1. <span data-ttu-id="d1326-130">Velja **Innhreyfingarskjal afurða**.</span><span class="sxs-lookup"><span data-stu-id="d1326-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="d1326-131">Í reitnum **Ytra innhreyfingarskjal afurða** skal rita gildi.</span><span class="sxs-lookup"><span data-stu-id="d1326-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="d1326-132">Í reitinn **Magn** skal slá inn tölu sem er lægri en talan sem er sýnd þar.</span><span class="sxs-lookup"><span data-stu-id="d1326-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="d1326-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d1326-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="d1326-134">Athuga birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="d1326-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="d1326-135">Veldu **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="d1326-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="d1326-136">Veldu **Á lager**.</span><span class="sxs-lookup"><span data-stu-id="d1326-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="d1326-137">Veldu **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="d1326-137">Select **Overview**.</span></span> <span data-ttu-id="d1326-138">Vörur sem hafa verið mótteknar sem vörusendingabirgðir í eigu lánardrottins eru tiltæk á lager.</span><span class="sxs-lookup"><span data-stu-id="d1326-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="d1326-139">Eftirstandandi magn á áfyllingarpöntun vörusendingar er birt í reitnum **Samtals pantað**.</span><span class="sxs-lookup"><span data-stu-id="d1326-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="d1326-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d1326-140">Close the page.</span></span>

