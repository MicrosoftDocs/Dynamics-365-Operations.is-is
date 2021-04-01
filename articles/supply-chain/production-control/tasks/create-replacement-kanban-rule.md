---
title: Stofna kanban-reglu til að koma í staðinn
description: Þetta ferli leggur áherslu á kanban-regla er skipt út nýja kanban-reglu á tiltekinni dagsetningu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de048577ac372474b72728d7774e3159a159afc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221824"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="5f685-103">Stofna kanban-reglu til að koma í staðinn</span><span class="sxs-lookup"><span data-stu-id="5f685-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f685-104">Þetta ferli leggur áherslu á kanban-regla er skipt út nýja kanban-reglu á tiltekinni dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="5f685-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="5f685-105">Þetta er gagnlegt þegar breytingar í framleiðsluflæðis eða áfylling reglur þarf að samræmdur og raða.</span><span class="sxs-lookup"><span data-stu-id="5f685-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="5f685-106">Sýnifyrirtæki til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="5f685-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="5f685-107">Þetta ferli er ætluð fyrir ferlishönnuð eða virðisstraumsstjóra þegar þeir undirbúa framleiðslu fyrir breytt framleiðsluflæði eða nýja áfyllingarreglu.</span><span class="sxs-lookup"><span data-stu-id="5f685-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="5f685-108">Þetta verk kemur í stað 000022 kanban-reglu með nýja reglu og eykur hámarksmagn úr 48 í 100 fyrir nýju reglunnar.</span><span class="sxs-lookup"><span data-stu-id="5f685-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="5f685-109">Veljið kanban-regluna til að skipta út.</span><span class="sxs-lookup"><span data-stu-id="5f685-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="5f685-110">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="5f685-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="5f685-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5f685-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f685-112">Velja kanban-reglu 000022.</span><span class="sxs-lookup"><span data-stu-id="5f685-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="5f685-113">Stofna kanban-reglu til að koma í staðinn</span><span class="sxs-lookup"><span data-stu-id="5f685-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="5f685-114">Smella á Skipta út kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="5f685-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="5f685-115">Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="5f685-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="5f685-116">Veldu dagsetningu í framtíðinni, eins og eina viku frá núna.</span><span class="sxs-lookup"><span data-stu-id="5f685-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="5f685-117">Þetta er dagsetning og tími þegar nýja kanban-regla verður virk og kemur í stað gömlu kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="5f685-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="5f685-118">Ef kanban-reglu breytir slóðina í framleiðsluflæði er hægt að velja annan verkþátt.</span><span class="sxs-lookup"><span data-stu-id="5f685-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="5f685-119">Í þessu ferli munu verkþætti helst óbreytt.</span><span class="sxs-lookup"><span data-stu-id="5f685-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="5f685-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5f685-120">Click OK.</span></span>
    * <span data-ttu-id="5f685-121">Athugaðu að nýja kanban-regla er stofnuð til að koma í stað kanban-regla 000022.</span><span class="sxs-lookup"><span data-stu-id="5f685-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="5f685-122">Gildisdagsetning er stillt samkvæmt dagsetningu sem valin er þegar þú skiptir um kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="5f685-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="5f685-123">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5f685-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f685-124">Veljið 000022 útskipt kanban-regluna.</span><span class="sxs-lookup"><span data-stu-id="5f685-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="5f685-125">Athugaðu að útskipta kanban-regla hefur sama dagsetning og lokadagsetning vegna þess að þetta er dagsetningin þegar hún mun renna út.</span><span class="sxs-lookup"><span data-stu-id="5f685-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="5f685-126">Í listanum skal velja línu 1.</span><span class="sxs-lookup"><span data-stu-id="5f685-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="5f685-127">Veljið nýja kanban-reglu efst á listann.</span><span class="sxs-lookup"><span data-stu-id="5f685-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="5f685-128">Þetta er kanban-regla með hæsta kanban-reglunúmer.</span><span class="sxs-lookup"><span data-stu-id="5f685-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="5f685-129">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5f685-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5f685-130">Smellið á númer kanban-reglu sem opna kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="5f685-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="5f685-131">Breyta hámarksmagn fyrir staðgengil kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="5f685-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="5f685-132">Setja hámarksmagn á "100".</span><span class="sxs-lookup"><span data-stu-id="5f685-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="5f685-133">Útvíkka flýtiflipann Magn til að sjá svæðið Hámarksmagn.</span><span class="sxs-lookup"><span data-stu-id="5f685-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="5f685-134">Hámarksmagni breytt í 100 leyfir allt að 100 kanbans að vera vinna.</span><span class="sxs-lookup"><span data-stu-id="5f685-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="5f685-135">Þetta er síðasta skrefið í þessu verkefni.</span><span class="sxs-lookup"><span data-stu-id="5f685-135">This is the last step in this task.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]