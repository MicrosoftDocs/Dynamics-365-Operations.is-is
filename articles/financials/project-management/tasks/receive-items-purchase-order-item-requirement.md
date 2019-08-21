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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fee2c965b0c065f00564b849ec93504336fb3f60
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838248"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="ef15e-103">Taka við atriðum í innkaupapöntun fyrir vöruþörf</span><span class="sxs-lookup"><span data-stu-id="ef15e-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef15e-104">Þetta ferli sýnir hvernig á að taka við vörum í innkaupapöntun úr vöruþörf.</span><span class="sxs-lookup"><span data-stu-id="ef15e-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="ef15e-105">Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="ef15e-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="ef15e-106">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="ef15e-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ef15e-107">Farið í Verkefnastjórnun og bókhald > Verkefni > Öll verkefni.</span><span class="sxs-lookup"><span data-stu-id="ef15e-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="ef15e-108">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ef15e-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="ef15e-109">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="ef15e-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="ef15e-110">Smellt er á Vöruþarfir.</span><span class="sxs-lookup"><span data-stu-id="ef15e-110">Click Item requirements.</span></span>
5. <span data-ttu-id="ef15e-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-111">Click New.</span></span>
6. <span data-ttu-id="ef15e-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ef15e-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="ef15e-113">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="ef15e-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="ef15e-114">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="ef15e-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-115">Click Save.</span></span>
10. <span data-ttu-id="ef15e-116">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="ef15e-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="ef15e-117">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="ef15e-117">Click Functions.</span></span>
12. <span data-ttu-id="ef15e-118">Smellt er á Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="ef15e-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="ef15e-119">Velja gátreitur Taka með.</span><span class="sxs-lookup"><span data-stu-id="ef15e-119">Select the Include check box.</span></span>
14. <span data-ttu-id="ef15e-120">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="ef15e-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="ef15e-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-121">Click OK.</span></span>
16. <span data-ttu-id="ef15e-122">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="ef15e-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="ef15e-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ef15e-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ef15e-124">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="ef15e-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="ef15e-125">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-125">Click Confirm.</span></span>
20. <span data-ttu-id="ef15e-126">Smellið á „Móttaka“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="ef15e-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="ef15e-127">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-127">Click Product receipt.</span></span>
22. <span data-ttu-id="ef15e-128">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ef15e-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="ef15e-129">Í reitinn innhreyfingarskjal afurða skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ef15e-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="ef15e-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ef15e-130">Click OK.</span></span>

