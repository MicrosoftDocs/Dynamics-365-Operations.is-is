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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 59f6a4131f6a27c0089a1259e3f849f91a47bc87
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2017

---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="f0402-103">Stofna valskilyrði fyrir söluverð</span><span class="sxs-lookup"><span data-stu-id="f0402-103">Create sales price selection criteria</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0402-104">Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön.</span><span class="sxs-lookup"><span data-stu-id="f0402-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="f0402-105">Þetta ferli krefst þess að að minnsta kosti eitt afbrigðalíkan afurðar sé tiltækt.</span><span class="sxs-lookup"><span data-stu-id="f0402-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="f0402-106">Þetta dæmi notar verðlíkanið fyrir söluverðslíkan hátalaralausnar í sýnigagnafyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="f0402-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="f0402-107">Venjulega notar framleiðslustjóri þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="f0402-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="f0402-108">Bæta við nýju skilyrði fyrir fyrirliggjandi söluverðlíkan</span><span class="sxs-lookup"><span data-stu-id="f0402-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="f0402-109">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="f0402-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="f0402-110">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="f0402-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="f0402-111">Á listanum velurðu línuna fyrir vörulíkan hátalaralausnar, en smelltu ekki á tengilinn fyrir heiti líkans.</span><span class="sxs-lookup"><span data-stu-id="f0402-111">In the list, select the row for the Speaker solution product model, but don’t click the link for the model name.</span></span>
4. <span data-ttu-id="f0402-112">Í aðgerðasvæðinu er smellt á líkan.</span><span class="sxs-lookup"><span data-stu-id="f0402-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="f0402-113">Smelltu á Skilyrði verðlíkans.</span><span class="sxs-lookup"><span data-stu-id="f0402-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="f0402-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f0402-114">Click New.</span></span>
7. <span data-ttu-id="f0402-115">Í svæðið Heiti, slærðu inn 'Customer group 10'.</span><span class="sxs-lookup"><span data-stu-id="f0402-115">In the Name field, type ‘Customer group 10’.</span></span>
    * <span data-ttu-id="f0402-116">Heiti verðlíkans er notað til að finna undirliggjandi valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="f0402-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="f0402-117">Í reitinn Verðlíkan skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="f0402-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="f0402-118">Í reitnum Gerð pöntunar velurðu Sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="f0402-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="f0402-119">Gerð pöntunar ákvarðar gagnagrunnsvæði sem eru tiltæk fyrir valfyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="f0402-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="f0402-120">Færa skal inn dagsetningu í svæðinu Gildir frá.</span><span class="sxs-lookup"><span data-stu-id="f0402-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="f0402-121">Í reitinn Fella úr gildi, skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f0402-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="f0402-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f0402-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="f0402-123">Búa til fyrirspurn fyrir valskilyrði</span><span class="sxs-lookup"><span data-stu-id="f0402-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="f0402-124">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="f0402-124">Click Edit.</span></span>
2. <span data-ttu-id="f0402-125">Í reitnum Tafla skal velja Viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="f0402-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="f0402-126">Í reitnum Reitur er valið Viðskiptamannsflokkur.</span><span class="sxs-lookup"><span data-stu-id="f0402-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="f0402-127">Í þessu dæmi notum við tiltekinn viðskiptavinaflokk fyrir valskilyrði.</span><span class="sxs-lookup"><span data-stu-id="f0402-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="f0402-128">Í reitnum Skilyrði er valið Customer group 10.</span><span class="sxs-lookup"><span data-stu-id="f0402-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="f0402-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f0402-129">Click OK.</span></span>


