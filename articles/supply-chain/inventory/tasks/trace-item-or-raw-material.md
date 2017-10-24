---
title: "Rekja vöru eða hráefni"
description: "Þetta ferli sýnir hvernig á að nota vörurakning til að auðkenna þar sem vörur eða hráefni hafa verið notaðar eða eru í notkun."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="60349-103">Rekja vöru eða hráefni</span><span class="sxs-lookup"><span data-stu-id="60349-103">Trace an item or raw material</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60349-104">Þetta ferli sýnir hvernig á að nota vörurakning til að auðkenna þar sem vörur eða hráefni hafa verið notaðar eða eru í notkun.</span><span class="sxs-lookup"><span data-stu-id="60349-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="60349-105">Með þessu ferli er hægt að greina vöru, rekja hann til baka í uppruna og svo áframrekja í gegnum framleiðslu og sölu á endanlegu vöruna.</span><span class="sxs-lookup"><span data-stu-id="60349-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="60349-106">Hægt er að nota ferlið til að rannsaka viðskiptavini sem verða fyrir áhrifum, sölupantana sem verða fyrir áhrifum og fleira.</span><span class="sxs-lookup"><span data-stu-id="60349-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="60349-107">Þessi aðferð notar sýnigögn fyrirtækisins USP2.</span><span class="sxs-lookup"><span data-stu-id="60349-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="60349-108">Rekja vöru með afturábak með þekkt rununúmer </span><span class="sxs-lookup"><span data-stu-id="60349-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="60349-109">Farið í Birgðastjórnun > Fyrirspurnir og skýrslur > Rakningarvíddir > Vörurakning.</span><span class="sxs-lookup"><span data-stu-id="60349-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="60349-110">Í reitnum Vörunúmer velurðu P9100.</span><span class="sxs-lookup"><span data-stu-id="60349-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="60349-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="60349-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="60349-112">í reitnum Áfram eða afturábak Veljið 'Afturábak' </span><span class="sxs-lookup"><span data-stu-id="60349-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="60349-113">Í rununúmer reitinn, velja „as-12-344-01"</span><span class="sxs-lookup"><span data-stu-id="60349-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="60349-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="60349-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="60349-115">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="60349-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="60349-116">Auðkenna vöru, rekja áfram og gera greiningu</span><span class="sxs-lookup"><span data-stu-id="60349-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="60349-117">Topphnútur trés sem birtist hér táknar magn á lager valinnar vöru og runu.</span><span class="sxs-lookup"><span data-stu-id="60349-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="60349-118">Nauðsynlegt er að útvíkka hnúta í tré til að finna vöru sem á að keyra áframrakningu fyrir.</span><span class="sxs-lookup"><span data-stu-id="60349-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="60349-119">Í trénu, Útvíkka 'hnúta sem er lýst fyrir neðan og veljið svo síðasta hnútinn.</span><span class="sxs-lookup"><span data-stu-id="60349-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="60349-120">Útvíkka: ' P9100 / 1 / 10 / as-12-344-01 ● 2 tunna ● 7.00 gal \P9100 ● Tiltekið ● sölupöntun 000072 22/12/2015 ● -1 tunna ● -4.00 gal ● Svæði = 1, Vöruhús = 10, rununúmer = as-12-344-01 \P9100 ● Framleiðsla B-000050 ● 12/9/2015● 7 tunna ● 27.00 gal ● Svæði =1,Vöruhús =10,Rununúmer =as-12-344-01 ● hliðarafurðir: P9101' og veldu síðan þann hnút.</span><span class="sxs-lookup"><span data-stu-id="60349-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="60349-121">í trénu, Útvíkka 'hnúta lýst fyrir neðan og veljið svo þann hnút',</span><span class="sxs-lookup"><span data-stu-id="60349-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="60349-122">Frá hnút sem var nýverið valinn, Útvíkka ' M9103 ● framleiðslulínu B-000050 ● 12/9/2015 ● -160.00 lb ● Stærð = 70, Litur = í lagi, Svæði = 1, Vöruhús = 10, rununúmer = App01' og veldu síðan þann hnút.</span><span class="sxs-lookup"><span data-stu-id="60349-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="60349-123">Smellt er á Rakning frá hnút.</span><span class="sxs-lookup"><span data-stu-id="60349-123">Click Trace from node.</span></span>
4. <span data-ttu-id="60349-124">Smellt er á Áfram.</span><span class="sxs-lookup"><span data-stu-id="60349-124">Click Forward.</span></span>
5. <span data-ttu-id="60349-125">Í aðgerðasvæðinu er smellt á rekja.</span><span class="sxs-lookup"><span data-stu-id="60349-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="60349-126">Það eru nokkrar rakningarkosti sem veita upplýsingar um viðskiptavini sem verða fyrir áhrifum af vörunni sem verið er að rekja, og sölupantanir sem tengjast vörunni sem hafa og hafa ekki verið sendar.</span><span class="sxs-lookup"><span data-stu-id="60349-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="60349-127">Smellt er á Viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="60349-127">Click Customers.</span></span>
7. <span data-ttu-id="60349-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="60349-128">Close the page.</span></span>
8. <span data-ttu-id="60349-129">Í aðgerðasvæðinu er smellt á rekja.</span><span class="sxs-lookup"><span data-stu-id="60349-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="60349-130">Smellt er á Sölupantanir sem voru sendar.</span><span class="sxs-lookup"><span data-stu-id="60349-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="60349-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="60349-131">Close the page.</span></span>

