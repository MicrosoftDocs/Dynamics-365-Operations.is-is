---
title: Yfirlit yfir áætlun farms með samstæðustöð
description: Greinin lýsir eiginleikanum að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74f152a227bec3b402eba9384dfb5db53b46d83a
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866066"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a><span data-ttu-id="8275c-103">Yfirlit yfir áætlun farms með samstæðustöð</span><span class="sxs-lookup"><span data-stu-id="8275c-103">Plan loads using hub consolidation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8275c-104">Greinin lýsir eiginleikanum að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="8275c-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="8275c-105">Það getur verið gagnlegt að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="8275c-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="8275c-106">Mynda hleðslur</span><span class="sxs-lookup"><span data-stu-id="8275c-106">Building loads</span></span>
<span data-ttu-id="8275c-107">Áður en hægt er að nota samstæðustöð þarf að virkja **áætlanagerð í flutningi** valkostinn á **færibreytur Flutningsstjórnunar** síðuna.</span><span class="sxs-lookup"><span data-stu-id="8275c-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="8275c-108">Einnig verður að stofna stöðvum þar sem sameiningu munu eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="8275c-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="8275c-109">Eftirfarandi skýringarmynd sýnir dæmi um samstæðustöð.</span><span class="sxs-lookup"><span data-stu-id="8275c-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="8275c-110">Í þessu tilfelli sölupantanir úr mismunandi vöruhúsum fara til sama viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="8275c-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="8275c-111">Grunnur hleðslur eru stofnaðar á grundvelli sölupantanir á hefðbundinn hátt með því að nota **vinnusvæði hleðsluáætlunar** síðu.</span><span class="sxs-lookup"><span data-stu-id="8275c-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="8275c-112">Til að sameina tvær hleðslurnar í stöð áður en þær eru sendar til viðskiptavinarins, á **vinnusvæði Hleðsluáætlunar** síðunni, í **Flutningur** svæðinu, veljið **samstæðustöð**.</span><span class="sxs-lookup"><span data-stu-id="8275c-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="8275c-113">Þegar velur rétt stöðvar fyrir hvern farm, farm hafa stöðvar sem ákvörðunarstað "afhenda".</span><span class="sxs-lookup"><span data-stu-id="8275c-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="8275c-114">Einnig mun veitast tvö "flutningsbeiðnilínur" í **Framboð og Eftirspurn** hlutanum á **Vinnusvæði Hleðsluáætlunar** síðu.</span><span class="sxs-lookup"><span data-stu-id="8275c-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="8275c-115">Hægt að bæta þessum tveimur línum í nýja hleðslu.</span><span class="sxs-lookup"><span data-stu-id="8275c-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="8275c-116">Þessi nýja hleðslu hafa bæði sölupöntunarlínur og mun einnig hafa stöðvar sem aðsetur "sækja" og viðskiptavinur A sem ákvörðunarstað "afhenda".</span><span class="sxs-lookup"><span data-stu-id="8275c-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="8275c-117">Hleðslurnar þrjár er hægt að gefa verð og beint eins og önnur hleðslu.</span><span class="sxs-lookup"><span data-stu-id="8275c-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="8275c-118">Hægt er að velja hvaða farmflytjanda sem kerfið leggur fyrir hvern farm.</span><span class="sxs-lookup"><span data-stu-id="8275c-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="8275c-119">[![Samstæðustöð](./media/hubconsol.jpg)](./media/hubconsol.jpg) Einnig er hægt að nota sömu aðferð til að sameina hleðslur fyrir margar pantanir.</span><span class="sxs-lookup"><span data-stu-id="8275c-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="8275c-120">Í þessu tilfelli viðskiptavina A í síðustu skýringarmynd er vöruhús.</span><span class="sxs-lookup"><span data-stu-id="8275c-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="8275c-121">Einnig er hægt að sameina hleðslur fyrir margar innkaupapantanir, þar sem farmarnir eru sendar frá mismunandi lánardrottnum í sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="8275c-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="8275c-122">Hægt er að hafa fleiri en einni samsetningu stöðvar og sameina í mörgum stöðvum fyrir fleiri farm sem koma úr mismunandi vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="8275c-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="8275c-123">Eftir að byggja á grundvallar hleðsluna og nota valkosturinn stöðvar sameiningu þú byggja nýja farma með því að nota sameinaðar flutningsbeiðnilínur.</span><span class="sxs-lookup"><span data-stu-id="8275c-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="8275c-124">Þá gefur þú hleðslu verð og leið.</span><span class="sxs-lookup"><span data-stu-id="8275c-124">You then rate and route your loads.</span></span>



