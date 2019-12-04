---
title: Víddir kostnaðareiningar
description: Sem einn grunnstólpi kostnaðarbókhalds, eru víddir kostnaðareiningar notaðar til að flokka og rekja hvert kostnaður streymir.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 44d404aaafd124a5d5a9d92cac8add51f1ee846a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771985"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="7196f-103">Víddir kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="7196f-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7196f-104">Sem einn grunnstólpi kostnaðarbókhalds, eru víddir kostnaðareiningar notaðar til að flokka og rekja hvert kostnaður streymir.</span><span class="sxs-lookup"><span data-stu-id="7196f-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="7196f-105">Kostnaðareiningu samsvarar afurð sem tengist kostnaði í bókhaldslykum.</span><span class="sxs-lookup"><span data-stu-id="7196f-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="7196f-106">Nokkurn vegin, getur það verið hvaða gerð einingar á lægsta stigi í fyrirtæki þangað sem kostnaður getur streymt.</span><span class="sxs-lookup"><span data-stu-id="7196f-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="7196f-107">Kostnaðareiningar sem hugtak nær frá fjárhagslyklum til allra tilfanga sem tengjast kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7196f-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="7196f-108">Núna, kostnaðarbókhald styður fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="7196f-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="7196f-109">Tveimur gerðum kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="7196f-109">Two types of cost elements</span></span>
<span data-ttu-id="7196f-110">Til eru tvær gerðir kostnaðareiningar: Aðal kostnaðareining og auka kostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="7196f-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="7196f-111">Eftirfarandi tafla útskýrir mismuninn á milli tveggja gerða.</span><span class="sxs-lookup"><span data-stu-id="7196f-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7196f-112"><strong>Aðal Kostnaðareiningar</strong></span><span class="sxs-lookup"><span data-stu-id="7196f-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="7196f-113"><strong>Aukakostnaðareining</strong></span><span class="sxs-lookup"><span data-stu-id="7196f-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7196f-114">Aðal kostnaðareiningar tákna flæði kostnaðar frá fjárhagsbókhald í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="7196f-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="7196f-115">Skipulag kostnaðareiningar samsvarar skipulagi rekstrarreiknings í fjárhagi, þar sem kostnaðareining samsvarar aðallykill.</span><span class="sxs-lookup"><span data-stu-id="7196f-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="7196f-116">Ekki öll aðallykla þurfa endilega að koma fram sem kostnaðareining samkvæmt þörfum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="7196f-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="7196f-117">Dæmi um aðal kostnaðareiningar innifela:</span><span class="sxs-lookup"><span data-stu-id="7196f-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="7196f-118">Kostnaður seldra vara</span><span class="sxs-lookup"><span data-stu-id="7196f-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="7196f-119">Taka með óbeinan kostnað</span><span class="sxs-lookup"><span data-stu-id="7196f-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="7196f-120">Starfsmannakostnaður</span><span class="sxs-lookup"><span data-stu-id="7196f-120">Personnel costs</span></span></li>
<li><span data-ttu-id="7196f-121">Orkukostnaður</span><span class="sxs-lookup"><span data-stu-id="7196f-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="7196f-122">Auka kostnaðareiningar tákna flæði innri kostnaðar þar sem þessi kostnaður er stofnaður og notaður í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="7196f-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="7196f-123">Þeir eru notaðir til að tryggja hægt sé að rekja uppruna kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="7196f-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="7196f-124">Þessar kostnaðareiningar eru notaðir í úthlutun kostnaðar og óbeinn útreikninga.</span><span class="sxs-lookup"><span data-stu-id="7196f-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="7196f-125">Dæmi um auka kostnaðareiningu innifelur:</span><span class="sxs-lookup"><span data-stu-id="7196f-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="7196f-126">Framleiðslukostnaður</span><span class="sxs-lookup"><span data-stu-id="7196f-126">Production costs</span></span></li>
<li><span data-ttu-id="7196f-127">Framleiðsla, hráefni og kostnaður vegna markaðsstarfs</span><span class="sxs-lookup"><span data-stu-id="7196f-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="7196f-128">Víddir kostnaðareiningar og víddarstök kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="7196f-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="7196f-129">Kostnaðareiningar eru vísað til sem *víddir kostnaðareiningar* .</span><span class="sxs-lookup"><span data-stu-id="7196f-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="7196f-130">Einstaka víddargildi kallast *víddarstök kostnaðareiningar*.</span><span class="sxs-lookup"><span data-stu-id="7196f-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="7196f-131">Til dæmis, þú ert með skipulag fyrir bókhaldslykill US (COA) sem er grunnur fyrir þinni lögboðnu skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="7196f-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="7196f-132">Þessi COA er notað sem vídd kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="7196f-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="7196f-133">Lyklar sem eru aðal kostnaðareiningar, eru sýndar sem víddarstök kostnaðareiningar í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="7196f-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="7196f-134">Eftirfarandi skjámyndir sýna dæmi um Aðallykla sem vídd kostnaðareiningar með hennar raunverulegu aðallykla sem víddarstök kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="7196f-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="7196f-135">[![Skjámynd af aðalreikningum sem vídd kostnaðarþátta](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="7196f-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="7196f-136">Flytja inn víddarstök kostnaðareiningar með gagnatengjum.</span><span class="sxs-lookup"><span data-stu-id="7196f-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="7196f-137">Til að auðvelda uppsetningu víddarstök kostnaðareiningar í kostnaðarbókhald geturðu notað gagnatengi sem eru annað hvort for-innbyggð eða sérstaklega innbygð af þér til að sækja aðal kostnaðareiningar úr einu eða fleiru upprunakerfi.</span><span class="sxs-lookup"><span data-stu-id="7196f-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="7196f-138">Umhugsunarefni fyrir innleiðingu</span><span class="sxs-lookup"><span data-stu-id="7196f-138">Implementation considerations</span></span>
<span data-ttu-id="7196f-139">Þar sem kostnaðareiningar tákna lægsta stigið upplýsingar um kostnað, ættirðu að ganga úr skugga um að allar kostnaðareiningar sem krafist er að geri stjórnunarskýrslugerðina séu hafðar með þegar þú framkvæmir skipulag kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="7196f-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="7196f-140">Það er áskorun að finna viðeigandi fjölda kostnaðareininga fyrir kostnaðarstýringu.</span><span class="sxs-lookup"><span data-stu-id="7196f-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="7196f-141">Hafandi þúsundum kostnaðareiningar getur gert það erfitt að stýra hverja kostnaðareiningu.</span><span class="sxs-lookup"><span data-stu-id="7196f-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="7196f-142">Til vara geturðu flokka kostnaðareiningar og hafa umsjón með kostnaðarstýring á samanlögðum stigum.</span><span class="sxs-lookup"><span data-stu-id="7196f-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>



