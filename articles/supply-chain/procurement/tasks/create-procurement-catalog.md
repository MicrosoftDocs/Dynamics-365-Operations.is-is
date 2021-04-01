---
title: Stofna innkaupavörulista
description: Þetta efnisatriði útskýrir hvernig á að stofna innkaupavörulista.
author: RichardLuan
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c377b2d155fb7b53ef9a15fa9d6e80cd69ed44
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237252"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="4c597-103">Stofna innkaupavörulista</span><span class="sxs-lookup"><span data-stu-id="4c597-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c597-104">Þetta efnisatriði útskýrir hvernig á að stofna innkaupavörulista.</span><span class="sxs-lookup"><span data-stu-id="4c597-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="4c597-105">Þetta verk myndi venjulega framkvæmt af fagmanni á sviði innkaupa.</span><span class="sxs-lookup"><span data-stu-id="4c597-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="4c597-106">Einnig muntu læra hvernig starfsmenn geta notað vörulista þegar þeir stofna beiðni.</span><span class="sxs-lookup"><span data-stu-id="4c597-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="4c597-107">Áður en hægt er að stofna vörulista verður að vera tegundastigveldi innkaupa í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="4c597-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="4c597-108">Stigveldið er erft af nýjum vörulista, ásamt öllum afurðum sem eru í stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="4c597-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="4c597-109">Hægt er að nota þessari handbók í sýnigögnum USMF-fyrirtækisins þar sem tegundastigveldi innkaupa er tiltækt, sem og dæmi sem notað er í skrefum ferlisins.</span><span class="sxs-lookup"><span data-stu-id="4c597-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="4c597-110">Tryggið að til tegundastigveldi innkaupa sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="4c597-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="4c597-111">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4c597-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="4c597-112">Tegundastigveldi innkaupa er tiltækt í sýnigögnum USMF-fyrirtækisins og afurðir hefur verið bætt við flokkinn **Skrifstofuvélar/Tölvur**.</span><span class="sxs-lookup"><span data-stu-id="4c597-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="4c597-113">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk þarf að aflæsa leiðarvísi fyrir verk til að fletta í gegnum tegundina.</span><span class="sxs-lookup"><span data-stu-id="4c597-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="4c597-114">Ef stigveldi var ekki tiltækt er það stofnað með því að smella á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4c597-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="4c597-115">Einungis er hægt að gera þetta einu sinni.</span><span class="sxs-lookup"><span data-stu-id="4c597-115">This can only be done once.</span></span>  
2. <span data-ttu-id="4c597-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4c597-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="4c597-117">Stofna vörulista</span><span class="sxs-lookup"><span data-stu-id="4c597-117">Create a catalog</span></span>
1. <span data-ttu-id="4c597-118">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Vörulistar > Innkaupavörulistar**.</span><span class="sxs-lookup"><span data-stu-id="4c597-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="4c597-119">Smelltu á **Nýr innkaupavörulisti** til að opna fellilistann.</span><span class="sxs-lookup"><span data-stu-id="4c597-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="4c597-120">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4c597-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="4c597-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4c597-121">Select **OK**.</span></span>
5. <span data-ttu-id="4c597-122">Í trénu útvíkkarðu **CORP PROCUREMENT CATEGORIES**.</span><span class="sxs-lookup"><span data-stu-id="4c597-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="4c597-123">Í trénu skal útvíkka **OFFICE MACHINES**.</span><span class="sxs-lookup"><span data-stu-id="4c597-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="4c597-124">Í trénu skal velja **Tölvur**.</span><span class="sxs-lookup"><span data-stu-id="4c597-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="4c597-125">Afurðir fyrir innkaupategundina birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="4c597-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="4c597-126">Eigi að bæta vöru við flokk þarf að gera þetta á síðunni **Tegundastigveldi innkaupa** eða á síðunni **Vöruupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="4c597-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="4c597-127">**Sjálfgefin** uppfærslugerð ákvarðar hvort nýjar afurðir sem hefur verið bætt við tegundastigveldi innkaupa eru sýnileg strax í vörulistanum.</span><span class="sxs-lookup"><span data-stu-id="4c597-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="4c597-128">Ef gerð uppfærslu er stillt á **Gagnvirkt**, eru breytingar sýnilegar strax.</span><span class="sxs-lookup"><span data-stu-id="4c597-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="4c597-129">Ef gerð uppfærslu er **Föst**, eru nýjar afurðir einungis sýnilegt fyrir fólk á vörulista eftir að vörulista hefur verið birt aftur.</span><span class="sxs-lookup"><span data-stu-id="4c597-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="4c597-130">Aðgerðin **Birta** er tiltæk í Aðgerðarúðunni efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="4c597-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="4c597-131">Ef vörur eru fjarlægðar úr tegundastigveldi innkaupa, sést breytingu strax, án tillits til gildisins í reitnum **sjálfgefin** uppfærslugerð.</span><span class="sxs-lookup"><span data-stu-id="4c597-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="4c597-132">Á aðgerðarrúðunni velurðu **Yfirlit flokks** og tryggir að **Virkja** sé valið.</span><span class="sxs-lookup"><span data-stu-id="4c597-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="4c597-133">Veldu **Virkja vörulista**.</span><span class="sxs-lookup"><span data-stu-id="4c597-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="4c597-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4c597-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="4c597-135">Gera vörulista sýnilegan</span><span class="sxs-lookup"><span data-stu-id="4c597-135">Make the catalog visible</span></span>
1. <span data-ttu-id="4c597-136">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Innkaupareglur**.</span><span class="sxs-lookup"><span data-stu-id="4c597-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="4c597-137">Veldu **Innkaupareglu USMF**</span><span class="sxs-lookup"><span data-stu-id="4c597-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="4c597-138">Velja þarf innkaupastefna fyrir lögaðilann sem starfsmaðurinn sem er tengdur við þína forstillingu má panta vörur í.</span><span class="sxs-lookup"><span data-stu-id="4c597-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="4c597-139">Í sýnigögnum USMF er kerfisstjóranotandinn tengdur við starfskraft sem kallast **Julia Funderburk** og hún pantar vörur í USMF að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="4c597-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="4c597-140">Veldu vörulistann sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="4c597-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="4c597-141">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4c597-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="4c597-142">Nota vörulista</span><span class="sxs-lookup"><span data-stu-id="4c597-142">Use the catalog</span></span>
1. <span data-ttu-id="4c597-143">Farðu í **skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupabeiðnir > Allar innkaupabeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="4c597-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="4c597-144">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4c597-144">Select **New**.</span></span>
3. <span data-ttu-id="4c597-145">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4c597-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="4c597-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4c597-146">Select **OK**.</span></span>
5. <span data-ttu-id="4c597-147">Veldu **Bæta afurðum við**.</span><span class="sxs-lookup"><span data-stu-id="4c597-147">Select **Add products**.</span></span>
6. <span data-ttu-id="4c597-148">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4c597-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="4c597-149">Hægt er að nota tegundastigveldi vinstra megin eða sía efst á listanum til að sía vörurnar.</span><span class="sxs-lookup"><span data-stu-id="4c597-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="4c597-150">Veldu **Bæta við línum**.</span><span class="sxs-lookup"><span data-stu-id="4c597-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="4c597-151">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4c597-151">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]