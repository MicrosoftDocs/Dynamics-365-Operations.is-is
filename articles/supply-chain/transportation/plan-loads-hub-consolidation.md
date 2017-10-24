---
title: "Áætla hleðslur með samstæðustöð"
description: "Greinin lýsir eiginleikanum að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3145febe40108e50b263514de1ca541dd914b7c5
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="a2896-103">Áætla hleðslur með samstæðustöð</span><span class="sxs-lookup"><span data-stu-id="a2896-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a2896-104">Greinin lýsir eiginleikanum að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="a2896-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="a2896-105">Það getur verið gagnlegt að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="a2896-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="a2896-106">Mynda hleðslur</span><span class="sxs-lookup"><span data-stu-id="a2896-106">Building loads</span></span>
<span data-ttu-id="a2896-107">Áður en hægt er að nota samstæðustöð þarf að virkja **áætlanagerð í flutningi**valkostinn á **færibreytur Flutningsstjórnunar** síðuna.</span><span class="sxs-lookup"><span data-stu-id="a2896-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="a2896-108">Einnig verður að stofna stöðvum þar sem sameiningu munu eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="a2896-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="a2896-109">Eftirfarandi skýringarmynd sýnir dæmi um samstæðustöð.</span><span class="sxs-lookup"><span data-stu-id="a2896-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="a2896-110">Í þessu tilfelli sölupantanir úr mismunandi vöruhúsum fara til sama viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="a2896-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="a2896-111">Grunnur hleðslur eru stofnaðar á grundvelli sölupantanir á hefðbundinn hátt með því að nota **vinnusvæði hleðsluáætlunar** síðu.</span><span class="sxs-lookup"><span data-stu-id="a2896-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="a2896-112">Til að sameina tvær hleðslurnar í stöð áður en þær eru sendar til viðskiptavinarins, á **vinnusvæði Hleðsluáætlunar** síðunni, í **Flutningur** svæðinu, veljið **samstæðustöð**.</span><span class="sxs-lookup"><span data-stu-id="a2896-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="a2896-113">Þegar velur rétt stöðvar fyrir hvern farm, farm hafa stöðvar sem ákvörðunarstað "afhenda".</span><span class="sxs-lookup"><span data-stu-id="a2896-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="a2896-114">Einnig mun veitast tvö "flutningsbeiðnilínur" í **Framboð og Eftirspurn** hlutanum á **Vinnusvæði Hleðsluáætlunar** síðu.</span><span class="sxs-lookup"><span data-stu-id="a2896-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="a2896-115">Hægt að bæta þessum tveimur línum í nýja hleðslu.</span><span class="sxs-lookup"><span data-stu-id="a2896-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="a2896-116">Þessi nýja hleðslu hafa bæði sölupöntunarlínur og mun einnig hafa stöðvar sem aðsetur "sækja" og viðskiptavinur A sem ákvörðunarstað "afhenda".</span><span class="sxs-lookup"><span data-stu-id="a2896-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="a2896-117">Hleðslurnar þrjár er hægt að gefa verð og beint eins og önnur hleðslu.</span><span class="sxs-lookup"><span data-stu-id="a2896-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="a2896-118">Hægt er að velja hvaða farmflytjanda sem kerfið leggur fyrir hvern farm.</span><span class="sxs-lookup"><span data-stu-id="a2896-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="a2896-119">[![Samstæðustöð](./media/hubconsol.jpg)](./media/hubconsol.jpg) Einnig er hægt að nota sömu aðferð til að sameina hleðslur fyrir margar pantanir.</span><span class="sxs-lookup"><span data-stu-id="a2896-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="a2896-120">Í þessu tilfelli viðskiptavina A í síðustu skýringarmynd er vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a2896-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="a2896-121">Einnig er hægt að sameina hleðslur fyrir margar innkaupapantanir, þar sem farmarnir eru sendar frá mismunandi lánardrottnum í sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="a2896-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="a2896-122">Hægt er að hafa fleiri en einni samsetningu stöðvar og sameina í mörgum stöðvum fyrir fleiri farm sem koma úr mismunandi vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="a2896-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="a2896-123">Eftir að byggja á grundvallar hleðsluna og nota valkosturinn stöðvar sameiningu þú byggja nýja farma með því að nota sameinaðar flutningsbeiðnilínur.</span><span class="sxs-lookup"><span data-stu-id="a2896-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="a2896-124">Þá gefur þú hleðslu verð og leið.</span><span class="sxs-lookup"><span data-stu-id="a2896-124">You then rate and route your loads.</span></span>




