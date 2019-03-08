---
title: 'Stofna verkþáttarvensl: næsti þáttur'
description: Flæði aðgerða í lean-framleiðsluflæði er skráð með vensl verkþáttar.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5e5844939e1eb40e31530c434c096c5b3be7abe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "325458"
---
# <a name="create-activity-relation-successor"></a><span data-ttu-id="3913c-103">Stofna verkþáttarvensl: Næsti þáttur</span><span class="sxs-lookup"><span data-stu-id="3913c-103">Create activity relation: Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3913c-104">Flæði aðgerða í lean-framleiðsluflæði er skráð með vensl verkþáttar.</span><span class="sxs-lookup"><span data-stu-id="3913c-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="3913c-105">Þessi skráning sýnir hvernig á að stofna verkþáttarvensl.</span><span class="sxs-lookup"><span data-stu-id="3913c-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="3913c-106">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="3913c-106">Prerequisites:</span></span>

- <span data-ttu-id="3913c-107">- Framleiðsluflæði og útgáfa í ham fyrir drög.</span><span class="sxs-lookup"><span data-stu-id="3913c-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="3913c-108">- Tveir verkþætti sem elta hvert annað í framleiðsluflæði eru stofnuð en ekki tengdar.</span><span class="sxs-lookup"><span data-stu-id="3913c-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="3913c-109">Finndu útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="3913c-109">Find the production flow version</span></span> 
1. <span data-ttu-id="3913c-110">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="3913c-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="3913c-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3913c-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3913c-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3913c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3913c-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3913c-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="3913c-114">Í listanum skal velja útgáfu draga.</span><span class="sxs-lookup"><span data-stu-id="3913c-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="3913c-115">Hægt er að bæta við verkþáttarvenslum við bæði drög eða virkar útgáfur framleiðsluflæðis.</span><span class="sxs-lookup"><span data-stu-id="3913c-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="3913c-116">Opna yfirlit verkþátta</span><span class="sxs-lookup"><span data-stu-id="3913c-116">Open the activity overview</span></span>
1. <span data-ttu-id="3913c-117">Smellt er á Verkþætti.</span><span class="sxs-lookup"><span data-stu-id="3913c-117">Click Activities.</span></span>
    * <span data-ttu-id="3913c-118">Athugið að skjámyndin sýnir alla verkþætti framleiðsluflæðis sem er úthlutað á þá Útgáfu framleiðsluflæðis sem unnið er í.</span><span class="sxs-lookup"><span data-stu-id="3913c-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="3913c-119">Bæta við arftaka</span><span class="sxs-lookup"><span data-stu-id="3913c-119">Add a Successor</span></span>
1. <span data-ttu-id="3913c-120">Smelltu á Bæta við arftaka.</span><span class="sxs-lookup"><span data-stu-id="3913c-120">Click Add successor.</span></span>
2. <span data-ttu-id="3913c-121">Í reitnum Verkþáttur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3913c-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3913c-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3913c-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3913c-123">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3913c-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3913c-124">Veldu gátreitinn Skorður.</span><span class="sxs-lookup"><span data-stu-id="3913c-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="3913c-125">Í reitinn Skorðugildi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="3913c-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="3913c-126">Tími skorða er sá tími sem er áætlaður á milli áætlaðra loka forvera (gjalddagi og tími) og áætlaðs upphafs arftaka.</span><span class="sxs-lookup"><span data-stu-id="3913c-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="3913c-127">Í reitinn Einingar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="3913c-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="3913c-128">Færið inn tölu í reitnum Hlutfall ferlistíma.</span><span class="sxs-lookup"><span data-stu-id="3913c-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="3913c-129">Ef báðir verkþættir eru keyrðir á sama framleiðslutíma ætti hlutfall ferlistíma að vera 1.</span><span class="sxs-lookup"><span data-stu-id="3913c-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="3913c-130">Ef forveri sem keyrist við tvöföld þjónustuhraða, hlutfall ætti að vera 2.</span><span class="sxs-lookup"><span data-stu-id="3913c-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="3913c-131">Hlutfall ferlistíma eru notuð til að reikna út einstaka ferlistíma fyrir verkþætti framleiðsluflæðis.</span><span class="sxs-lookup"><span data-stu-id="3913c-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="3913c-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3913c-132">Click OK.</span></span>
10. <span data-ttu-id="3913c-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3913c-133">Close the page.</span></span>
11. <span data-ttu-id="3913c-134">Smellt er á flipann GridPanel.</span><span class="sxs-lookup"><span data-stu-id="3913c-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="3913c-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3913c-135">Close the page.</span></span>
13. <span data-ttu-id="3913c-136">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="3913c-136">Refresh the page.</span></span>

