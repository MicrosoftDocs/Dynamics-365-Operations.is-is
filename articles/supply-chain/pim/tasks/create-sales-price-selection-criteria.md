--- 
title: "Stofna valskilyrði fyrir söluverð"
description: "Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8a651453fe9693fdb22875d860d7c118ea009b3e
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="cb45a-103">Stofna valskilyrði fyrir söluverð</span><span class="sxs-lookup"><span data-stu-id="cb45a-103">Create sales price selection criteria</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb45a-104">Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön.</span><span class="sxs-lookup"><span data-stu-id="cb45a-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="cb45a-105">Þetta ferli krefst þess að að minnsta kosti eitt afbrigðalíkan afurðar sé tiltækt.</span><span class="sxs-lookup"><span data-stu-id="cb45a-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="cb45a-106">Þetta dæmi notar verðlíkanið fyrir söluverðslíkan hátalaralausnar í sýnigagnafyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="cb45a-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="cb45a-107">Venjulega notar framleiðslustjóri þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="cb45a-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="cb45a-108">Bæta við nýju skilyrði fyrir fyrirliggjandi söluverðlíkan</span><span class="sxs-lookup"><span data-stu-id="cb45a-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="cb45a-109">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="cb45a-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="cb45a-110">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="cb45a-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="cb45a-111">Á listanum velurðu línuna fyrir vörulíkan hátalaralausnar, en smelltu ekki á tengilinn fyrir heiti líkans.</span><span class="sxs-lookup"><span data-stu-id="cb45a-111">In the list, select the row for the Speaker solution product model, but don’t click the link for the model name.</span></span>
4. <span data-ttu-id="cb45a-112">Í aðgerðasvæðinu er smellt á líkan.</span><span class="sxs-lookup"><span data-stu-id="cb45a-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="cb45a-113">Smelltu á Skilyrði verðlíkans.</span><span class="sxs-lookup"><span data-stu-id="cb45a-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="cb45a-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cb45a-114">Click New.</span></span>
7. <span data-ttu-id="cb45a-115">Í svæðið Heiti, slærðu inn 'Customer group 10'.</span><span class="sxs-lookup"><span data-stu-id="cb45a-115">In the Name field, type ‘Customer group 10’.</span></span>
    * <span data-ttu-id="cb45a-116">Heiti verðlíkans er notað til að finna undirliggjandi valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="cb45a-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="cb45a-117">Í reitinn Verðlíkan skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cb45a-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="cb45a-118">Í reitnum Gerð pöntunar velurðu Sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="cb45a-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="cb45a-119">Gerð pöntunar ákvarðar gagnagrunnsvæði sem eru tiltæk fyrir valfyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="cb45a-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="cb45a-120">Færa skal inn dagsetningu í svæðinu Gildir frá.</span><span class="sxs-lookup"><span data-stu-id="cb45a-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="cb45a-121">Í reitinn Fella úr gildi, skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="cb45a-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="cb45a-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="cb45a-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="cb45a-123">Búa til fyrirspurn fyrir valskilyrði</span><span class="sxs-lookup"><span data-stu-id="cb45a-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="cb45a-124">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="cb45a-124">Click Edit.</span></span>
2. <span data-ttu-id="cb45a-125">Í reitnum Tafla skal velja Viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="cb45a-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="cb45a-126">Í reitnum Reitur er valið Viðskiptamannsflokkur.</span><span class="sxs-lookup"><span data-stu-id="cb45a-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="cb45a-127">Í þessu dæmi notum við tiltekinn viðskiptavinaflokk fyrir valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="cb45a-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="cb45a-128">Í reitnum Skilyrði er valið Customer group 10.</span><span class="sxs-lookup"><span data-stu-id="cb45a-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="cb45a-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cb45a-129">Click OK.</span></span>


