--- 
title: "Stofna sölupöntun fyrir skilgreinanlega afurð"
description: "Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 646606237f593d24792a0ae072948f2e12782283
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="41e31-103">Stofna sölupöntun fyrir skilgreinanlega afurð</span><span class="sxs-lookup"><span data-stu-id="41e31-103">Create a sales order for a configurable product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41e31-104">Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="41e31-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="41e31-105">Þetta dæmi notar D0006 líkanið í USMF sýnigögnum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="41e31-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="41e31-106">Venjulega notar sölupantanavinnsla þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="41e31-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="41e31-107">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="41e31-107">Create a sales order</span></span>
1. <span data-ttu-id="41e31-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="41e31-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="41e31-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="41e31-109">Click New.</span></span>
3. <span data-ttu-id="41e31-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="41e31-110">Click Sales order.</span></span>
4. <span data-ttu-id="41e31-111">Í reitnum Viðskiptavinalykill velurðu US-001.</span><span class="sxs-lookup"><span data-stu-id="41e31-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="41e31-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="41e31-112">Click OK.</span></span>
6. <span data-ttu-id="41e31-113">Í svæðið vörunúmer veldu 'D0006'.</span><span class="sxs-lookup"><span data-stu-id="41e31-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="41e31-114">Fyrir þetta verk þarf að velja samskipanlega afurð.</span><span class="sxs-lookup"><span data-stu-id="41e31-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="41e31-115">Smellt er á Afurð og framboð.</span><span class="sxs-lookup"><span data-stu-id="41e31-115">Click Product and supply.</span></span>
8. <span data-ttu-id="41e31-116">Smellt er á Skilgreina línu.</span><span class="sxs-lookup"><span data-stu-id="41e31-116">Click Configure line.</span></span>
    * <span data-ttu-id="41e31-117">Athugið að verði hefur verið breytt, byggt á stillingunni sem var valin, og að Taka köplum svæðið er núna stillt á Satt.</span><span class="sxs-lookup"><span data-stu-id="41e31-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="41e31-118">Athugið sjálfgefna verð- og stillingar sem eru valdar fyrir á köplum.</span><span class="sxs-lookup"><span data-stu-id="41e31-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="41e31-119">Smellt er á Hlaða sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="41e31-119">Click Load template.</span></span>
    * <span data-ttu-id="41e31-120">Þetta dæmi sýnir hvernig hægt er að nota sniðmát til að velja forskilgreind afbrigði.</span><span class="sxs-lookup"><span data-stu-id="41e31-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="41e31-121">Ef þetta ferli er notað sem leiðarvísi fyrir verk og til að sjá aðrar eigindargildin sem eru tiltækar verður að smella á hnappinn Aflæsa.</span><span class="sxs-lookup"><span data-stu-id="41e31-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="41e31-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="41e31-122">Click OK.</span></span>
11. <span data-ttu-id="41e31-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="41e31-123">Click OK.</span></span>
12. <span data-ttu-id="41e31-124">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="41e31-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="41e31-125">Smellið á flipann Afurðar.</span><span class="sxs-lookup"><span data-stu-id="41e31-125">Click the Product tab.</span></span>
    * <span data-ttu-id="41e31-126">Afbrigði vörunnar er nú skráður undir afurðarvíddum.</span><span class="sxs-lookup"><span data-stu-id="41e31-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="41e31-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="41e31-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="41e31-128">Veljið vöruafbrigði.</span><span class="sxs-lookup"><span data-stu-id="41e31-128">Select the product configuration</span></span>


