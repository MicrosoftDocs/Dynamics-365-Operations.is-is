---
title: Stofna innkaupavörulista
description: Þetta efnisatriði útskýrir hvernig á að stofna innkaupavörulista.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836390"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="d8cb0-103">Stofna innkaupavörulista</span><span class="sxs-lookup"><span data-stu-id="d8cb0-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8cb0-104">Þetta efnisatriði útskýrir hvernig á að stofna innkaupavörulista.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="d8cb0-105">Þetta verk myndi venjulega framkvæmt af fagmanni á sviði innkaupa.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="d8cb0-106">Einnig muntu læra hvernig starfsmenn geta notað vörulista þegar þeir stofna beiðni.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="d8cb0-107">Áður en hægt er að stofna vörulista verður að vera tegundastigveldi innkaupa í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="d8cb0-108">Stigveldið er erft af nýjum vörulista, ásamt öllum afurðum sem eru í stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="d8cb0-109">Hægt er að nota þessari handbók í sýnigögnum USMF-fyrirtækisins þar sem tegundastigveldi innkaupa er tiltækt, sem og dæmi sem notað er í skrefum ferlisins.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="d8cb0-110">Tryggið að til tegundastigveldi innkaupa sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="d8cb0-111">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="d8cb0-112">Tegundastigveldi innkaupa er tiltækt í sýnigögnum USMF-fyrirtækisins og afurðir hefur verið bætt við flokkinn **Skrifstofuvélar/Tölvur**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="d8cb0-113">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk þarf að aflæsa leiðarvísi fyrir verk til að fletta í gegnum tegundina.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="d8cb0-114">Ef stigveldi var ekki tiltækt, yrði það stofnað með því að smella á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-114">If a hierarchy was not available, you’d create it by clicking **New**.</span></span> <span data-ttu-id="d8cb0-115">Einungis er hægt að gera þetta einu sinni.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-115">This can only be done once.</span></span>  
2. <span data-ttu-id="d8cb0-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="d8cb0-117">Stofna vörulista</span><span class="sxs-lookup"><span data-stu-id="d8cb0-117">Create a catalog</span></span>
1. <span data-ttu-id="d8cb0-118">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Vörulistar > Innkaupavörulistar**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="d8cb0-119">Smelltu á **Nýr innkaupavörulisti** til að opna fellilistann.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="d8cb0-120">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d8cb0-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-121">Select **OK**.</span></span>
5. <span data-ttu-id="d8cb0-122">Í trénu útvíkkarðu **CORP PROCUREMENT CATEGORIES**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="d8cb0-123">Í trénu skal útvíkka **OFFICE MACHINES**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="d8cb0-124">Í trénu skal velja **Tölvur**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="d8cb0-125">Afurðir fyrir innkaupategundina birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="d8cb0-126">Eigi að bæta vöru við flokk þarf að gera þetta á síðunni **Tegundastigveldi innkaupa** eða á síðunni **Vöruupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="d8cb0-127">**Sjálfgefin** uppfærslugerð ákvarðar hvort nýjar afurðir sem hefur verið bætt við tegundastigveldi innkaupa eru sýnileg strax í vörulistanum.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="d8cb0-128">Ef gerð uppfærslu er stillt á **Gagnvirkt**, eru breytingar sýnilegar strax.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="d8cb0-129">Ef gerð uppfærslu er **Föst**, eru nýjar afurðir einungis sýnilegt fyrir fólk á vörulista eftir að vörulista hefur verið birt aftur.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="d8cb0-130">Aðgerðin **Birta** er tiltæk í Aðgerðarúðunni efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="d8cb0-131">Ef vörur eru fjarlægðar úr tegundastigveldi innkaupa, sést breytingu strax, án tillits til gildisins í reitnum **sjálfgefin** uppfærslugerð.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="d8cb0-132">Á aðgerðarrúðunni velurðu **Yfirlit flokks** og tryggir að **Virkja** sé valið.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="d8cb0-133">Veldu **Virkja vörulista**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="d8cb0-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="d8cb0-135">Gera vörulista sýnilegan</span><span class="sxs-lookup"><span data-stu-id="d8cb0-135">Make the catalog visible</span></span>
1. <span data-ttu-id="d8cb0-136">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Innkaupareglur**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="d8cb0-137">Veldu **Innkaupareglu USMF**</span><span class="sxs-lookup"><span data-stu-id="d8cb0-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="d8cb0-138">Velja þarf innkaupastefna fyrir lögaðilann sem starfsmaðurinn sem er tengdur við þína forstillingu má panta vörur í.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="d8cb0-139">Í sýnigögnum USMF er kerfisstjóranotandinn tengdur við starfskraft sem kallast **Julia Funderburk** og hún pantar vörur í USMF að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="d8cb0-140">Velja vörulista sem nýverið var stofnuð</span><span class="sxs-lookup"><span data-stu-id="d8cb0-140">Select the catalog that you’ve just created.</span></span>
4. <span data-ttu-id="d8cb0-141">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="d8cb0-142">Nota vörulista</span><span class="sxs-lookup"><span data-stu-id="d8cb0-142">Use the catalog</span></span>
1. <span data-ttu-id="d8cb0-143">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupabeiðnir > Allar innkaupabeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="d8cb0-144">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-144">Select **New**.</span></span>
3. <span data-ttu-id="d8cb0-145">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d8cb0-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-146">Select **OK**.</span></span>
5. <span data-ttu-id="d8cb0-147">Veldu **Bæta afurðum við**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-147">Select **Add products**.</span></span>
6. <span data-ttu-id="d8cb0-148">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="d8cb0-149">Hægt er að nota tegundastigveldi vinstra megin eða sía efst á listanum til að sía vörurnar.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="d8cb0-150">Veldu **Bæta við línum**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="d8cb0-151">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8cb0-151">Select **OK**.</span></span>

