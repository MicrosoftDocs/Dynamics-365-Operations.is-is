---
title: Innkaupapantanir fyrir verk
description: "Þessi grein lýsir ýmsum aðferðum sem hægt er að nota til að stofna innkaupapantanir fyrir verk. Aðferðin sem notuð er er háð tilgangi innkaupapöntunar, og þegar keyptar vörur eru notaðar og innheimtar á verk."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0cf1effee6fd9e08b85d30f90c5e83aa77bc22cc
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="87dd8-104">Innkaupapantanir fyrir verk</span><span class="sxs-lookup"><span data-stu-id="87dd8-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="87dd8-105">Þessi grein lýsir ýmsum aðferðum sem hægt er að nota til að stofna innkaupapantanir fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="87dd8-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="87dd8-106">Aðferðin sem notuð er er háð tilgangi innkaupapöntunar, og þegar keyptar vörur eru notaðar og innheimtar á verk.</span><span class="sxs-lookup"><span data-stu-id="87dd8-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="87dd8-107">Í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition er hægt að nota margar aðferðir til að stofna innkaupapantanir fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="87dd8-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="87dd8-108">Aðferðin sem notuð er er háð tilgangi innkaupapöntunar, þegar keyptar vörur eru notaðar og þegar keyptar vörur eru reikningsfærðar á verk.</span><span class="sxs-lookup"><span data-stu-id="87dd8-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="87dd8-109">Aðferðir til að búa til innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="87dd8-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="87dd8-110">Hægt er að nota eina af eftirfarandi aðferðum til að stofna innkaupapöntun í Verkefnastjórnun og bókhald.</span><span class="sxs-lookup"><span data-stu-id="87dd8-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="87dd8-111">Tilgangur innkaupapöntunar ákvarðar hvenær innkaupapöntunin er notuð og þar með hvenær vörur eru innheimtar á verk.</span><span class="sxs-lookup"><span data-stu-id="87dd8-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87dd8-112">Aðferð</span><span class="sxs-lookup"><span data-stu-id="87dd8-112">Method</span></span></th>
<th><span data-ttu-id="87dd8-113">Tilgangur</span><span class="sxs-lookup"><span data-stu-id="87dd8-113">Purpose</span></span></th>
<th><span data-ttu-id="87dd8-114">Notkun vara</span><span class="sxs-lookup"><span data-stu-id="87dd8-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87dd8-115">Stofna innkaupapöntun beint úr verki.</span><span class="sxs-lookup"><span data-stu-id="87dd8-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="87dd8-116">Notið þessa aðferð til að kaupa inn vörur frá ytri lánardrottni fyrir notkun í verki.</span><span class="sxs-lookup"><span data-stu-id="87dd8-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="87dd8-117">Hægt er að stofna innkaupapöntun á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="87dd8-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="87dd8-118">Frá verkinu sjálfu.</span><span class="sxs-lookup"><span data-stu-id="87dd8-118">From the project itself.</span></span> <span data-ttu-id="87dd8-119">Í þessu tilfelli hefur verkið þegar verið tilgreint fyrir innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="87dd8-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="87dd8-120">Með því að fletta að verkið innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="87dd8-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="87dd8-121">Velja þarf bæði lánardrottinn og verk sem stofna á innkaupapöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="87dd8-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="87dd8-122">Vörur eru notaðar þegar reikningur lánardrottins er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="87dd8-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87dd8-123">Stofna innkaupapöntun úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="87dd8-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="87dd8-124">Notið þessa aðferð til að kaupa vörur þegar sölupöntun er stofnuð úr verki.</span><span class="sxs-lookup"><span data-stu-id="87dd8-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="87dd8-125">Vörur eru notaðar þegar sölupöntun er reikningsfærð til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87dd8-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87dd8-126">Stofnið innkaupapöntun úr vöruþörf.</span><span class="sxs-lookup"><span data-stu-id="87dd8-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="87dd8-127">Notið þessa aðferð til að kaupa vörur þegar vöruþörf er stofnuð úr verki.</span><span class="sxs-lookup"><span data-stu-id="87dd8-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="87dd8-128">Vörur eru notaðar þegar fylgiseðill vöruþarfar er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="87dd8-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="87dd8-129">Þegar reikningur lánardrottins eða fylgiseðill er uppfærður ertu hvattur til að uppfæra fylgiseðilinn í vöruþörf.</span><span class="sxs-lookup"><span data-stu-id="87dd8-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="87dd8-130">Frekari upplýsingar, sjá [Fá vörur úr innkaupapöntun frá vöruþörf](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="87dd8-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


