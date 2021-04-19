---
title: Lean-þarfarakning úr sölupöntun
description: Þetta ferli leggur áherslu á villuleit fyrir þarfarakningartré úr sölulínu þar sem varan er framleidd með kanban.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff57169ea58a90d1113bb7ef0a581f900e62a9b2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828563"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="3fc27-103">Lean-þarfarakning úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="3fc27-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3fc27-104">Þetta ferli leggur áherslu á villuleit fyrir þarfarakningartré úr sölulínu þar sem varan er framleidd með kanban.</span><span class="sxs-lookup"><span data-stu-id="3fc27-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="3fc27-105">Eftir villuleit fyrir þarfarakningartré, eru allar kanban-vinnslur áætlaðar.</span><span class="sxs-lookup"><span data-stu-id="3fc27-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="3fc27-106">Þetta er gagnlegt fyrir pöntunaraðstæður þar sem pöntunarviðtaki þarf að tryggja að framleiðslan getur hafist strax.</span><span class="sxs-lookup"><span data-stu-id="3fc27-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="3fc27-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="3fc27-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3fc27-108">Þetta ferli er ætluð fyrir þróaðan viðtakanda pöntunar sem vinnur í lean fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="3fc27-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="3fc27-109">Stofna sölupöntun fyrir kanban sem er stýrt af vöru</span><span class="sxs-lookup"><span data-stu-id="3fc27-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="3fc27-110">Fara í Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="3fc27-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="3fc27-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3fc27-111">Click New.</span></span>
3. <span data-ttu-id="3fc27-112">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="3fc27-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="3fc27-113">Nota US-001.</span><span class="sxs-lookup"><span data-stu-id="3fc27-113">Use US-001.</span></span>  
4. <span data-ttu-id="3fc27-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3fc27-114">Click OK.</span></span>
5. <span data-ttu-id="3fc27-115">Sláið inn „L0001“ á svæðinu „Vörunúmer“.</span><span class="sxs-lookup"><span data-stu-id="3fc27-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="3fc27-116">Stillið magn á „30“.</span><span class="sxs-lookup"><span data-stu-id="3fc27-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="3fc27-117">Það er mikilvægt að magnið er hærra en 24 til að virkja tilviksreglur kanbans.</span><span class="sxs-lookup"><span data-stu-id="3fc27-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="3fc27-118">Opna í þarfarakningartré</span><span class="sxs-lookup"><span data-stu-id="3fc27-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="3fc27-119">Smellt er á Afurð og framboð.</span><span class="sxs-lookup"><span data-stu-id="3fc27-119">Click Product and supply.</span></span>
2. <span data-ttu-id="3fc27-120">Smellt er á Skoða þarfarakningartré.</span><span class="sxs-lookup"><span data-stu-id="3fc27-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="3fc27-121">Athugið að fyrir þarfarakningartré sýnir öll þarfarakning þarf fyrir línu í sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="3fc27-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="3fc27-122">Í þessu tilfelli eru tveimur stigum kanbana og allir nauðsynlegir íhlutir.</span><span class="sxs-lookup"><span data-stu-id="3fc27-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="3fc27-123">Áætla þarfarakningartré</span><span class="sxs-lookup"><span data-stu-id="3fc27-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="3fc27-124">Í trénu, skal velja sölulína ' 000832\Kanban 000558'.</span><span class="sxs-lookup"><span data-stu-id="3fc27-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="3fc27-125">Útvíkka hlutann Kanban vinnslur.</span><span class="sxs-lookup"><span data-stu-id="3fc27-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="3fc27-126">Athugið að stöðu vinnsla fyrir kanban-vinnsla er Ekki áætluð.</span><span class="sxs-lookup"><span data-stu-id="3fc27-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="3fc27-127">Smellt er á Áætlun alls þarfarakningartré.</span><span class="sxs-lookup"><span data-stu-id="3fc27-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="3fc27-128">Þetta mun áætla allar vinnslur kanban í þarfarakningartré, og breytir stöðunni úr er Ekki áætluð í Vinnsla Áætluð.</span><span class="sxs-lookup"><span data-stu-id="3fc27-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="3fc27-129">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="3fc27-129">Refresh the page.</span></span>
    * <span data-ttu-id="3fc27-130">Athugið að stöðu kanban var breytt úr Ekki áætluð í áætlað.</span><span class="sxs-lookup"><span data-stu-id="3fc27-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="3fc27-131">Veljið í trénu 'Sölulínu 000832\Kanban 000558\útgáfa fyrir L0001\Kanban 000559'.</span><span class="sxs-lookup"><span data-stu-id="3fc27-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="3fc27-132">Vinnslan fyrir kanban-vinnslan númer tvö er líka áætlaðar, þar sem allt þarfarakningartré er áætluð.</span><span class="sxs-lookup"><span data-stu-id="3fc27-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="3fc27-133">Athugið að stöðu kanban var breytt úr Ekki áætluð í áætlað.</span><span class="sxs-lookup"><span data-stu-id="3fc27-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]