---
title: Stofna sölupöntun fyrir skilgreinanlega afurð
description: Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39ccb68ba76cd710412df6a46fc624608d02902b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844538"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="bda1b-103">Stofna sölupöntun fyrir skilgreinanlega afurð</span><span class="sxs-lookup"><span data-stu-id="bda1b-103">Create a sales order for a configurable product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bda1b-104">Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="bda1b-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="bda1b-105">Þetta dæmi notar D0006 líkanið í USMF sýnigögnum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="bda1b-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="bda1b-106">Venjulega notar sölupantanavinnsla þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="bda1b-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="bda1b-107">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="bda1b-107">Create a sales order</span></span>
1. <span data-ttu-id="bda1b-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="bda1b-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="bda1b-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bda1b-109">Click New.</span></span>
3. <span data-ttu-id="bda1b-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="bda1b-110">Click Sales order.</span></span>
4. <span data-ttu-id="bda1b-111">Í reitnum Viðskiptavinalykill velurðu US-001.</span><span class="sxs-lookup"><span data-stu-id="bda1b-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="bda1b-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bda1b-112">Click OK.</span></span>
6. <span data-ttu-id="bda1b-113">Í svæðið vörunúmer veldu 'D0006'.</span><span class="sxs-lookup"><span data-stu-id="bda1b-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="bda1b-114">Fyrir þetta verk þarf að velja samskipanlega afurð.</span><span class="sxs-lookup"><span data-stu-id="bda1b-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="bda1b-115">Smellt er á Afurð og framboð.</span><span class="sxs-lookup"><span data-stu-id="bda1b-115">Click Product and supply.</span></span>
8. <span data-ttu-id="bda1b-116">Smellt er á Skilgreina línu.</span><span class="sxs-lookup"><span data-stu-id="bda1b-116">Click Configure line.</span></span>
    * <span data-ttu-id="bda1b-117">Athugið að verði hefur verið breytt, byggt á stillingunni sem var valin, og að Taka köplum svæðið er núna stillt á Satt.</span><span class="sxs-lookup"><span data-stu-id="bda1b-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="bda1b-118">Athugið sjálfgefna verð- og stillingar sem eru valdar fyrir á köplum.</span><span class="sxs-lookup"><span data-stu-id="bda1b-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="bda1b-119">Smellt er á Hlaða sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="bda1b-119">Click Load template.</span></span>
    * <span data-ttu-id="bda1b-120">Þetta dæmi sýnir hvernig hægt er að nota sniðmát til að velja forskilgreind afbrigði.</span><span class="sxs-lookup"><span data-stu-id="bda1b-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="bda1b-121">Ef þetta ferli er notað sem leiðarvísi fyrir verk og til að sjá aðrar eigindargildin sem eru tiltækar verður að smella á hnappinn Aflæsa.</span><span class="sxs-lookup"><span data-stu-id="bda1b-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="bda1b-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bda1b-122">Click OK.</span></span>
11. <span data-ttu-id="bda1b-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bda1b-123">Click OK.</span></span>
12. <span data-ttu-id="bda1b-124">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="bda1b-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="bda1b-125">Smellið á flipann Afurðar.</span><span class="sxs-lookup"><span data-stu-id="bda1b-125">Click the Product tab.</span></span>
    * <span data-ttu-id="bda1b-126">Afbrigði vörunnar er nú skráður undir afurðarvíddum.</span><span class="sxs-lookup"><span data-stu-id="bda1b-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="bda1b-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bda1b-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="bda1b-128">Veljið vöruafbrigði.</span><span class="sxs-lookup"><span data-stu-id="bda1b-128">Select the product configuration</span></span>

