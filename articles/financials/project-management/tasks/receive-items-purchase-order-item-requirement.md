---
title: Taka við atriðum í innkaupapöntun fyrir vöruþörf
description: Þetta efni útskýrir hvernig á að taka við vörum í innkaupapöntun úr vöruþörf.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867296"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="21cf4-103">Taka við atriðum í innkaupapöntun fyrir vöruþörf</span><span class="sxs-lookup"><span data-stu-id="21cf4-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21cf4-104">Þetta efni útskýrir hvernig á að taka við vörum í innkaupapöntun úr vöruþörf.</span><span class="sxs-lookup"><span data-stu-id="21cf4-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="21cf4-105">Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="21cf4-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="21cf4-106">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="21cf4-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="21cf4-107">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verk > Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="21cf4-108">Í listanum skal velja tengilinn í æskilegri línu.</span><span class="sxs-lookup"><span data-stu-id="21cf4-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="21cf4-109">Í aðgerðarúðunni velurðu **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="21cf4-110">Veldu **Vöruþarfir**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="21cf4-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-111">Select **New**.</span></span>
6. <span data-ttu-id="21cf4-112">Í nýju röðinni færirðu inn eða velur gildi í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="21cf4-113">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="21cf4-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="21cf4-114">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-114">Select **Save**.</span></span>
9. <span data-ttu-id="21cf4-115">Á Aðgerðasvæðinu skal velja **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="21cf4-116">Veljið **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-116">Select **Functions**.</span></span>
11. <span data-ttu-id="21cf4-117">Veldu **Stofna innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="21cf4-118">Veldu gátreitinn **Taka allt með**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="21cf4-119">Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="21cf4-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="21cf4-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-120">Select **OK**.</span></span>
15. <span data-ttu-id="21cf4-121">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="21cf4-122">Í listanum skal velja tengilinn í æskilegri línu.</span><span class="sxs-lookup"><span data-stu-id="21cf4-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="21cf4-123">Í aðgerðasvæðinu velurðu **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="21cf4-124">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="21cf4-125">Í aðgerðasvæðinu velurðu **Móttaka**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="21cf4-126">Velja **Innhreyfingarskjal afurða**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="21cf4-127">Í reitinn **Innhreyfingarskjal afurða** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="21cf4-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="21cf4-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="21cf4-128">Select **OK**.</span></span>

