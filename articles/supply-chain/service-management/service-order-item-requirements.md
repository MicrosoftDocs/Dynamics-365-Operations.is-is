---
title: Þjónustupöntun vöruþarfar
description: Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8866d8a4d6ad879f2c43b470af98457cb7c75721
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985741"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="59081-103">Þjónustupöntun vöruþarfar</span><span class="sxs-lookup"><span data-stu-id="59081-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="59081-104">Þú getur búið til þjónustupöntun til að fylgjast með og stjórna þjónustu sem þú veitir viðskiptavinum þínum.</span><span class="sxs-lookup"><span data-stu-id="59081-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="59081-105">Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="59081-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="59081-106">Hægt er að neyta vörukröfu strax úr birgðum, eða hún getur hafið framleiðslupöntun fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="59081-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="59081-107">Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="59081-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="59081-108">Liður kröfur um þjónustu pantanir eru unnin í gegnum verkefni.</span><span class="sxs-lookup"><span data-stu-id="59081-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="59081-109">Til að stofna vöruþörf í þjónustupöntun verður þjónustupöntunin að vera tengd við verk.</span><span class="sxs-lookup"><span data-stu-id="59081-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="59081-110">Um leið og vöruþörf er stofnuð fyrir þjónustupöntun er hægt að skoða hana í **Verkefni** í einstökum þjónustupöntunum eða í gegnum skjámyndina **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="59081-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="59081-111">Skoða vöruþörf úr þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="59081-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="59081-112">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="59081-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="59081-113">Smelltu á **Afgreiða** og smelltu síðan á **Vörukrafa** til að opna skjámyndina **Vörukröfur**.</span><span class="sxs-lookup"><span data-stu-id="59081-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="59081-114">Smelltu á flipann **Verkefni** og athugaðu reitinn **Þjónustupöntun** til að sjá þjónustupantanir vörukröfunnar.</span><span class="sxs-lookup"><span data-stu-id="59081-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="59081-115">Eyða þjónustupöntunum með vöruþörfum</span><span class="sxs-lookup"><span data-stu-id="59081-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="59081-116">Ef vöruþörf er búin til í þjónustupöntun er ekki hægt að eyða þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="59081-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="59081-117">Fyrst þarf að eyða vöruþörfinni áður en hægt er að eyða þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="59081-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="59081-118">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="59081-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="59081-119">Smelltu á **Afgreiða** og smelltu síðan á **Vörukrafa** til að opna skjámyndina **Vörukröfur**.</span><span class="sxs-lookup"><span data-stu-id="59081-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="59081-120">Skjámyndin birtir lista yfir vöruþarfir sem eru myndaðar á þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="59081-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="59081-121">Veldu vörukröfuna sem á að eyða og smelltu síðan á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="59081-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="59081-122">– eða –</span><span class="sxs-lookup"><span data-stu-id="59081-122">–or–</span></span>

1.  <span data-ttu-id="59081-123">Smelltu á **Verkefnastjórnun og bókhald** \> **Almenn** \> **Verkefni** \> **Öll verkefni**.</span><span class="sxs-lookup"><span data-stu-id="59081-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="59081-124">Opnaðu verkefnið sem hefur þjónustupöntun þar sem vörukrafa er búin til.</span><span class="sxs-lookup"><span data-stu-id="59081-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="59081-125">Í skjámyndinni **Verkefni**, í hægri glugganum, skal smella á **Vörukröfur**.</span><span class="sxs-lookup"><span data-stu-id="59081-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="59081-126">Skjámyndin **Vöruþörf** birtir lista yfir vöruþarfir sem eru tengdar völdu verki.</span><span class="sxs-lookup"><span data-stu-id="59081-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="59081-127">Veldu vörukröfuna sem á að eyða og smelltu síðan á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="59081-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="59081-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="59081-128">See also</span></span>

<span data-ttu-id="59081-129">[Vöruþörf (skjámynd)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="59081-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

