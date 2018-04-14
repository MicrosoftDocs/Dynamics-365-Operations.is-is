--- 
title: "Stofna innkaupavörulista"
description: "Þessi verklýsing sýnir hvernig á að stofna innkaupavörulista."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 66c0f41e1c98cf84b6a0afff5ee55e7c15fecd2d
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="a1508-103">Stofna innkaupavörulista</span><span class="sxs-lookup"><span data-stu-id="a1508-103">Create a procurement catalog</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1508-104">Þessi verklýsing sýnir hvernig á að stofna innkaupavörulista.</span><span class="sxs-lookup"><span data-stu-id="a1508-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="a1508-105">Þetta verk myndi venjulega framkvæmt af fagmanni á sviði innkaupa.</span><span class="sxs-lookup"><span data-stu-id="a1508-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="a1508-106">Einnig muntu læra hvernig starfsmenn geta notað vörulista þegar þeir stofna beiðni.</span><span class="sxs-lookup"><span data-stu-id="a1508-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="a1508-107">Áður en hægt er að stofna vörulista verður að vera tegundastigveldi innkaupa í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a1508-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="a1508-108">Stigveldið er erft af nýjum vörulista, ásamt öllum afurðum sem eru í stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="a1508-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="a1508-109">Hægt er að nota þessari handbók í sýnigögnum USMF-fyrirtækisins þar sem tegundastigveldi innkaupa er tiltækt, sem og dæmi sem notað er í skrefum ferlisins.</span><span class="sxs-lookup"><span data-stu-id="a1508-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="a1508-110">Tryggið að til tegundastigveldi innkaupa sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="a1508-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="a1508-111">Fara í Innkaup og uppruni > Innkaupaflokkar.</span><span class="sxs-lookup"><span data-stu-id="a1508-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="a1508-112">Tegundastigveldi innkaupa er tiltækt í sýnigögnum USMF-fyrirtækisins og afurðir hefur verið bætt við tegundirnar skrifstofuvélar/Tölvur.</span><span class="sxs-lookup"><span data-stu-id="a1508-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="a1508-113">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk þarf að aflæsa leiðarvísi fyrir verk til að fletta í gegnum tegundina.</span><span class="sxs-lookup"><span data-stu-id="a1508-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="a1508-114">Ef stigveldi var ekki tiltæk, yrði það stofnað með því að smella á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="a1508-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="a1508-115">Einungis er hægt að gera þetta einu sinni.</span><span class="sxs-lookup"><span data-stu-id="a1508-115">This can only be done once.</span></span>  
2. <span data-ttu-id="a1508-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a1508-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="a1508-117">Stofna vörulista</span><span class="sxs-lookup"><span data-stu-id="a1508-117">Create a catalog</span></span>
1. <span data-ttu-id="a1508-118">Fara í Innkaup og uppruni > vörulistar > Innkaupavörulistar.</span><span class="sxs-lookup"><span data-stu-id="a1508-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="a1508-119">Smellt er á Nýtt innkaupavörulisti til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a1508-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="a1508-120">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a1508-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a1508-121">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a1508-121">Click OK.</span></span>
5. <span data-ttu-id="a1508-122">Útvíkka 'CORP PROCUREMENT CATEGORIES', í trénu.</span><span class="sxs-lookup"><span data-stu-id="a1508-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="a1508-123">Í trénu skal víkka út 'OFFICE MACHINES'.</span><span class="sxs-lookup"><span data-stu-id="a1508-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="a1508-124">Í trénu skal velja „Tölvur“.</span><span class="sxs-lookup"><span data-stu-id="a1508-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="a1508-125">Afurðir fyrir innkaupategundina birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="a1508-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="a1508-126">Eigi að bæta vöru við tegund þarf að gera þetta á síðunni tegundastigveldi innkaupa eða á vöruupplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="a1508-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="a1508-127">Sjálfgefin uppfærslugerð ákvarðar hvort nýjar afurðir sem hefur verið bætt við tegundastigveldi innkaupa eru sýnileg strax í vörulistanum.</span><span class="sxs-lookup"><span data-stu-id="a1508-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="a1508-128">Ef gerð uppfærslu er stillt á Gagnvirkt, eru breytingar sýnileg strax.</span><span class="sxs-lookup"><span data-stu-id="a1508-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="a1508-129">Ef gerð uppfærslu er Föst, eru nýjar afurðir einungis sýnilegt fyrir fólk á vörulista eftir að vörulista hefur verið birt aftur.</span><span class="sxs-lookup"><span data-stu-id="a1508-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="a1508-130">Birtingaraðgerð er tiltæk í Aðgerðarúðunni efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="a1508-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="a1508-131">Ef vörur eru fjarlægðar úr tegundastigveldi innkaupa, sést breytingu strax, án tillits til gildisins í reitnum sjálfgefin uppfærslugerð.</span><span class="sxs-lookup"><span data-stu-id="a1508-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="a1508-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a1508-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a1508-133">Smellt er á Fela.</span><span class="sxs-lookup"><span data-stu-id="a1508-133">Click Hide.</span></span>
10. <span data-ttu-id="a1508-134">Á Aðgerðarúðu, smellið á .Yfirlit tegundar</span><span class="sxs-lookup"><span data-stu-id="a1508-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="a1508-135">Smellt er á gera óvirkt.</span><span class="sxs-lookup"><span data-stu-id="a1508-135">Click Disable.</span></span>
12. <span data-ttu-id="a1508-136">Á Aðgerðarúðu, smellið á .Yfirlit tegundar</span><span class="sxs-lookup"><span data-stu-id="a1508-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="a1508-137">Smella á Virkja.</span><span class="sxs-lookup"><span data-stu-id="a1508-137">Click Enable.</span></span>
14. <span data-ttu-id="a1508-138">Smella á Virkja vörulista</span><span class="sxs-lookup"><span data-stu-id="a1508-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="a1508-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a1508-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="a1508-140">Gera vörulista sýnilegan</span><span class="sxs-lookup"><span data-stu-id="a1508-140">Make the catalog visible</span></span>
1. <span data-ttu-id="a1508-141">Fara í Innkaup og uppruni > Uppsetning > reglur > innkaupareglur.</span><span class="sxs-lookup"><span data-stu-id="a1508-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="a1508-142">Velja innkaupastefnu USMF</span><span class="sxs-lookup"><span data-stu-id="a1508-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="a1508-143">Velja þarf innkaupastefna fyrir lögaðilann sem starfsmaðurinn sem er tengdur við þína forstillingu má panta vörur í.</span><span class="sxs-lookup"><span data-stu-id="a1508-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="a1508-144">Í Sýnigögn USMF, er kerfisstjóranotandanum tengd við starfsmann sem kallast Julia Funderburk, og hún pantar vörur í USMF að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="a1508-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="a1508-145">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a1508-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a1508-146">Velja vörulista sem nýverið var stofnuð</span><span class="sxs-lookup"><span data-stu-id="a1508-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="a1508-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a1508-147">Click OK.</span></span>
6. <span data-ttu-id="a1508-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a1508-148">Close the page.</span></span>
7. <span data-ttu-id="a1508-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a1508-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="a1508-150">Nota vörulista</span><span class="sxs-lookup"><span data-stu-id="a1508-150">Use the catalog</span></span>
1. <span data-ttu-id="a1508-151">Fara í Innkaup og uppruni > Innkaupabeiðnir > Allar Innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="a1508-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="a1508-152">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a1508-152">Click New.</span></span>
3. <span data-ttu-id="a1508-153">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a1508-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a1508-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a1508-154">Click OK.</span></span>
5. <span data-ttu-id="a1508-155">Smella á Bæta við afurðum.</span><span class="sxs-lookup"><span data-stu-id="a1508-155">Click Add products.</span></span>
6. <span data-ttu-id="a1508-156">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a1508-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a1508-157">Hægt er að nota tegundastigveldi vinstra megin eða sía efst á listanum til að sía vörurnar.</span><span class="sxs-lookup"><span data-stu-id="a1508-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="a1508-158">Smellt er á Bæta við línum.</span><span class="sxs-lookup"><span data-stu-id="a1508-158">Click Add to lines.</span></span>
8. <span data-ttu-id="a1508-159">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a1508-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a1508-160">Smellt er á Bæta við línum.</span><span class="sxs-lookup"><span data-stu-id="a1508-160">Click Add to lines.</span></span>
10. <span data-ttu-id="a1508-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a1508-161">Click OK.</span></span>


