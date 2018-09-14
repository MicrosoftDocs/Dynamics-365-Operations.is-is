--- 
title: "Stofna nýja kanban-reglu með því að afrita fyrirliggjandi kanban-reglu"
description: "Þetta ferli leggur áherslu á hvernig afrit af fyrirliggjandi kanban-reglu er stofnað."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7f72dbca0debf9e6a03ee700a979d4f4c110f819
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="5db95-103">Stofna nýja kanban-reglu með því að afrita fyrirliggjandi kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="5db95-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5db95-104">Þetta ferli leggur áherslu á hvernig afrit af fyrirliggjandi kanban-reglu er stofnað.</span><span class="sxs-lookup"><span data-stu-id="5db95-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="5db95-105">Þetta er gagnlegt ef ætlunin er að stofna nýjar kanban-reglur út frá fyrirliggjandi kanban-reglum.</span><span class="sxs-lookup"><span data-stu-id="5db95-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="5db95-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="5db95-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5db95-107">Þetta ferli er ætluð fyrir ferlishönnuð eða virðisstraumsstjóra þegar þeir undirbúa framleiðslu fyrir breytt framleiðsluflæði eða nýja áfyllingarreglu.</span><span class="sxs-lookup"><span data-stu-id="5db95-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="5db95-108">Velja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="5db95-108">Select a kanban rule</span></span>
1. <span data-ttu-id="5db95-109">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="5db95-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="5db95-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5db95-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5db95-111">Veldu kanban-reglu 000017 fyrir afurð M0006.</span><span class="sxs-lookup"><span data-stu-id="5db95-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="5db95-112">Afrita kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="5db95-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="5db95-113">Smellt er á Afrita kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="5db95-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="5db95-114">Við afritun á kanban-reglu, er hægt að breyta gerð dagsetningar, verkþætti og val afurða.</span><span class="sxs-lookup"><span data-stu-id="5db95-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="5db95-115">Breyttu afurðar fyrir þetta ferli í næsta þrepi.</span><span class="sxs-lookup"><span data-stu-id="5db95-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="5db95-116">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="5db95-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="5db95-117">Veldu M0007.</span><span class="sxs-lookup"><span data-stu-id="5db95-117">Select M0007.</span></span>  
3. <span data-ttu-id="5db95-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5db95-118">Click OK.</span></span>
    * <span data-ttu-id="5db95-119">Athugið að afrit af kanban-reglu 000017 er stofnað.</span><span class="sxs-lookup"><span data-stu-id="5db95-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    


