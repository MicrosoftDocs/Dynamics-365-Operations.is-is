---
title: Stofna áfyllingarpöntun vörusendingar
description: Þessi verklýsing sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845547"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="5bd67-103">Stofna áfyllingarpöntun vörusendingar</span><span class="sxs-lookup"><span data-stu-id="5bd67-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5bd67-104">Þessi verklýsing sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir.</span><span class="sxs-lookup"><span data-stu-id="5bd67-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="5bd67-105">Hún sýnir einnig hvernig á að skrá innhreyfingar afurða þannig að vörusendingabirgðir eru skráðar sem lagerbirgðir í lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="5bd67-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="5bd67-106">Þetta ferli myndi er yfirleitt framkvæmt af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="5bd67-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="5bd67-107">Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="5bd67-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="5bd67-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="5bd67-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="5bd67-109">Stofna áfyllingarpöntun vörusendingar</span><span class="sxs-lookup"><span data-stu-id="5bd67-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="5bd67-110">Fara í Innkaup og uppruni > vörusending > vörusending áfylling Pantanir.</span><span class="sxs-lookup"><span data-stu-id="5bd67-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="5bd67-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-111">Click New.</span></span>
3. <span data-ttu-id="5bd67-112">Í svæðinu Lánardrottnalykill skal slá inn 'US-104'.</span><span class="sxs-lookup"><span data-stu-id="5bd67-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="5bd67-113">Velja þarf lánardrottinn sem skráður er sem er eigandi á síðunni birgðaeigendur.</span><span class="sxs-lookup"><span data-stu-id="5bd67-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="5bd67-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-114">Click OK.</span></span>
5. <span data-ttu-id="5bd67-115">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-115">Click Add line.</span></span>
6. <span data-ttu-id="5bd67-116">Í svæðið vörunúmer færðu inn 'M9211CI.'.</span><span class="sxs-lookup"><span data-stu-id="5bd67-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="5bd67-117">Þú verður að velja vöru sem er uppsett fyrir vörusendingabirgðir.</span><span class="sxs-lookup"><span data-stu-id="5bd67-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="5bd67-118">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="5bd67-119">Dagsetning er rituð í reitinn umbeðin dagsetning afhendingar:.</span><span class="sxs-lookup"><span data-stu-id="5bd67-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="5bd67-120">Umbeðnar og staðfestar dagsetningar eru notaðar af MRP-vélinni (vél lánstímaálags) vegna áætlaðrar komu varningsins.</span><span class="sxs-lookup"><span data-stu-id="5bd67-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="5bd67-121">Dagsetning er rituð í reitinn staðfestur afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="5bd67-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="5bd67-122">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="5bd67-123">Smellið á flipann Birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="5bd67-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="5bd67-124">Til að sýna eiganda í reitnum eigandi birgðavídda, skal endurnýja síðuna.</span><span class="sxs-lookup"><span data-stu-id="5bd67-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="5bd67-125">Lánardrottininn US-104 er nú skráður sem eiganda.</span><span class="sxs-lookup"><span data-stu-id="5bd67-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="5bd67-126">Athugaðu staða birgðafærslunnar.</span><span class="sxs-lookup"><span data-stu-id="5bd67-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="5bd67-127">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="5bd67-127">Click Inventory.</span></span>
2. <span data-ttu-id="5bd67-128">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="5bd67-128">Click Transactions.</span></span>
3. <span data-ttu-id="5bd67-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="5bd67-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5bd67-130">Athugið svæðið móttaka er stillt á Pantað.</span><span class="sxs-lookup"><span data-stu-id="5bd67-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="5bd67-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5bd67-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="5bd67-132">Taka á móti vörum</span><span class="sxs-lookup"><span data-stu-id="5bd67-132">Receive items</span></span>
1. <span data-ttu-id="5bd67-133">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-133">Click Product receipt.</span></span>
2. <span data-ttu-id="5bd67-134">Sláið inn gildi í reitinn Ytra innhreyfingarskjal afurða.</span><span class="sxs-lookup"><span data-stu-id="5bd67-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="5bd67-135">Í reitinn magn skal slá inn númer sem er lægra en númerið sem er sýnt þar.</span><span class="sxs-lookup"><span data-stu-id="5bd67-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="5bd67-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="5bd67-137">Athuga birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="5bd67-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="5bd67-138">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="5bd67-138">Click Inventory.</span></span>
2. <span data-ttu-id="5bd67-139">Smelltu Á lager.</span><span class="sxs-lookup"><span data-stu-id="5bd67-139">Click On-hand.</span></span>
3. <span data-ttu-id="5bd67-140">Smelltu á Yfirlit.</span><span class="sxs-lookup"><span data-stu-id="5bd67-140">Click Overview.</span></span>
    * <span data-ttu-id="5bd67-141">Vörur sem hafa verið mótteknar sem vörusendingabirgðir í eigu lánardrottins eru tiltæk á lager.</span><span class="sxs-lookup"><span data-stu-id="5bd67-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="5bd67-142">Eftirstandandi magn á áfyllingarpöntun vörusendingar er birt í reitnum Samtals pantað.</span><span class="sxs-lookup"><span data-stu-id="5bd67-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="5bd67-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5bd67-143">Close the page.</span></span>
5. <span data-ttu-id="5bd67-144">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="5bd67-144">Click Close.</span></span>

