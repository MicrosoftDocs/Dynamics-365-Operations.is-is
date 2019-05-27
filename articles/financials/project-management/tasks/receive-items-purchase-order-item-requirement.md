---
title: Taka við atriðum í innkaupapöntun fyrir vöruþörf
description: Þetta ferli sýnir hvernig á að taka við vörum í innkaupapöntun úr vöruþörf.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26572a49426719fba520338a5eccd7e0af78890e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572374"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="cb201-103">Taka við atriðum í innkaupapöntun fyrir vöruþörf</span><span class="sxs-lookup"><span data-stu-id="cb201-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb201-104">Þetta ferli sýnir hvernig á að taka við vörum í innkaupapöntun úr vöruþörf.</span><span class="sxs-lookup"><span data-stu-id="cb201-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="cb201-105">Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="cb201-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="cb201-106">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="cb201-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="cb201-107">Farið í Verkefnastjórnun og bókhald > Verkefni > Öll verkefni.</span><span class="sxs-lookup"><span data-stu-id="cb201-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="cb201-108">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="cb201-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="cb201-109">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cb201-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="cb201-110">Smellt er á Vöruþarfir.</span><span class="sxs-lookup"><span data-stu-id="cb201-110">Click Item requirements.</span></span>
5. <span data-ttu-id="cb201-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cb201-111">Click New.</span></span>
6. <span data-ttu-id="cb201-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="cb201-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="cb201-113">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cb201-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="cb201-114">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="cb201-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="cb201-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="cb201-115">Click Save.</span></span>
10. <span data-ttu-id="cb201-116">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="cb201-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="cb201-117">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="cb201-117">Click Functions.</span></span>
12. <span data-ttu-id="cb201-118">Smellt er á Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="cb201-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="cb201-119">Velja gátreitur Taka með.</span><span class="sxs-lookup"><span data-stu-id="cb201-119">Select the Include check box.</span></span>
14. <span data-ttu-id="cb201-120">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="cb201-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="cb201-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cb201-121">Click OK.</span></span>
16. <span data-ttu-id="cb201-122">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="cb201-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="cb201-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="cb201-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="cb201-124">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cb201-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="cb201-125">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="cb201-125">Click Confirm.</span></span>
20. <span data-ttu-id="cb201-126">Smellið á „Móttaka“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cb201-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="cb201-127">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="cb201-127">Click Product receipt.</span></span>
22. <span data-ttu-id="cb201-128">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="cb201-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="cb201-129">Í reitinn innhreyfingarskjal afurða skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cb201-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="cb201-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cb201-130">Click OK.</span></span>

