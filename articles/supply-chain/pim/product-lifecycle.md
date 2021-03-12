---
title: Yfirlit yfir líftímastöðu afurðar
description: Lífferilsstaða afurðar skráir lífferilsstöðu útgefinnar vöru eða vöruafbrigðis.
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: cff4ee39d4c27e9a0dfc891e0f95278040ede877
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999782"
---
# <a name="product-lifecycle-state-overview"></a><span data-ttu-id="7dbe9-103">Yfirlit yfir líftímastöðu afurðar</span><span class="sxs-lookup"><span data-stu-id="7dbe9-103">Product lifecycle state overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dbe9-104">Lífferilsstaða afurðar skráir lífferilsstöðu útgefinnar vöru eða vöruafbrigðis.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="7dbe9-105">Lífferilsstöður afurða eru skilgreind af notanda, yfirleitt framleiðslustjóra eða vara aðalgagna-framleiðslustjóra.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="7dbe9-106">Tilteknir viðskiptaferlar, svo sem aðaláætlanagerð, geta orðið fyrir áhrifum af tiltekinni lífferilsstöðu.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>

<span data-ttu-id="7dbe9-107">Útgefin vara eða varaafbrigði getur tengst lífferilsstöðu afurðar sem skráir í hvaða lífferilsstöðu tiltekin afurð eða afbrigði er nú.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="7dbe9-108">Þú getur skilgreint hvaða fjölda lífferilsstöðu afurða sem er, með því að úthluta heiti og lýsingu á stöðunni.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="7dbe9-109">Þú getur valið eina lífferilsstöðu sem sjálfgefið stöðu fyrir nýjar útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="7dbe9-110">Útgefin afurðaafbrigði erfa sína lífferilsstöðu afurðar frá útgefnu afurðasniðmáti þeirra við sköpun.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="7dbe9-111">Þegar þú breytir lífferilsstöðu á útgefnu afurðasniðmáti, getur þú valið að uppfæra öll núverandi afbrigði sem hafa sama upprunalega stöðuna.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="7dbe9-112">Stofna nýja líftímastöðu afurðar</span><span class="sxs-lookup"><span data-stu-id="7dbe9-112">Create a new product lifecycle state</span></span>

- <span data-ttu-id="7dbe9-113">Til að búa til nýja lífferilsstöðu afurðar, sjá [Búðu til nýja lífferilsstöðu afurðar](tasks/new-product-lifecycle-state.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe9-113">To create a new product lifecycle state, see [Create a new product lifecycle state](tasks/new-product-lifecycle-state.md).</span></span>

- <span data-ttu-id="7dbe9-114">Til að búa til sjálfgefið lífferilsstaða afurðar, sjá [Búa til sjálfgefið lífferilsstaða afurðar](tasks/default-product-lifecycle-state.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe9-114">To create a default product lifecycle state, see [Create a default product lifecycle state](tasks/default-product-lifecycle-state.md).</span></span>

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="7dbe9-115">Tengja lífferilsstöðu afurðar við útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="7dbe9-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="7dbe9-116">Það eru margar leiðir til að tengja lífferilsstöðu afurðar við útgefnar afurðir eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

- <span data-ttu-id="7dbe9-117">Við stofnun nýrrar útgefinnar afurðar er sjálfgefin **Lífferilsstaða afurðar** úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span>
- <span data-ttu-id="7dbe9-118">Við útgáfu afurðar til lögaðila, er sjálfgefin **Lífferilsstaða afurðar** úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span>
- <span data-ttu-id="7dbe9-119">Við útgáfu afurðaafbrigða til lögaðila, er **Lífferilsstaða afurðar** sem tengd er við útgefið afurðasniðmát í þessum lögaðila, sjálfkrafa úthlutað til nýja afbrigðisins.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span>

<span data-ttu-id="7dbe9-120">Hægt er að uppfæra lífferilsstöðu afurðar handvirkt með því að nota:</span><span class="sxs-lookup"><span data-stu-id="7dbe9-120">You can manually update the product lifecycle state by using:</span></span>

- <span data-ttu-id="7dbe9-121">Listasíða **Útgefnar afurðir** eða **Upplýsingar yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-121">The **Released products** list page or **Details view**.</span></span>
- <span data-ttu-id="7dbe9-122">Listasíða **Útgefin afurðaafbrigði** lista síðu eða **Upplýsingar yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-122">The **Released product variants** list page or **Details view**.</span></span>
- <span data-ttu-id="7dbe9-123">Finndu úreltar afurðir eða afurðaafbrigði sem byggist á eftirspurn og tengdu við það lífferilsstöðu.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="7dbe9-124">Frekari upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="7dbe9-124">For more information:</span></span>

- <span data-ttu-id="7dbe9-125">Til að tengja lífferilsstöðu afurðar við útgefinn afurðasniðmát sjá [Úthlutaðu lífferilsstöðu afurðar til útgefins afurðasniðmáts](tasks/product-lifecycle-state-released-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe9-125">To associate a product lifecycle state to a released product master, see [Assign a product lifecycle state to a released product master](tasks/product-lifecycle-state-released-product-master.md).</span></span>

- <span data-ttu-id="7dbe9-126">Til að tengja lífferilsstöðu afurðar við útgefna afurð s´já [Úthlutaðu lífferilsstöðu afurðar til útgefinnar afurðar](tasks/product-lifecycle-state-released-product.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe9-126">To associate a product lifecycle state to a release product, see [Assign a product lifecycle state to a released product](tasks/product-lifecycle-state-released-product.md).</span></span>

## <a name="impact-on-master-planning"></a><span data-ttu-id="7dbe9-127">Áhrif á aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="7dbe9-127">Impact on master planning</span></span>

<span data-ttu-id="7dbe9-128">Lífferilsstaða afurðar hefur aðeins eina stýringarmerki: **Er virkt fyrir áætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="7dbe9-129">Sjálfgefið er þetta stillt á **Já** fyrir allar tilbúnar lífferilsstöðu afurðar, en það er hægt að breyta í **Nei**.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="7dbe9-130">Þegar stillt er á **Nei**, eru tengdir útgefnar afurðir eða útgefin afurðaafbrigði:</span><span class="sxs-lookup"><span data-stu-id="7dbe9-130">When set to **No**, the associated released products or released product variants are:</span></span>

- <span data-ttu-id="7dbe9-131">Útilokuð frá aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-131">Excluded from master planning.</span></span>
- <span data-ttu-id="7dbe9-132">Útilokuð frá útreikningi á BOM-stigi.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-132">Excluded from BOM-level calculation.</span></span>

<span data-ttu-id="7dbe9-133">Nánari upplýsingar um hvernig á að nota lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð og útreikningum á BOM-stigi, sjá [Búðu til lífferilsstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð](tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe9-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, see [Create a product lifecycle state to exclude products from Master planning](tasks/exclude-products-master-planning.md)</span></span>

> [!NOTE]
> <span data-ttu-id="7dbe9-134">Af ástæðum tengdum afköstum, er mjög mælt með því að tengja allar úreltar afurðir eða afurðaafbrigði, sérstaklega þegar unnið er með óendurnotanleg grunnstillingaafbrigði afurða, við lífferilsstöðu afurðar sem er óvirkt fyrir aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  

## <a name="default-migration-import-and-export"></a><span data-ttu-id="7dbe9-135">Sjálfgefinn flutningur, innflutningur, og útflutningur</span><span class="sxs-lookup"><span data-stu-id="7dbe9-135">Default migration, import, and export</span></span>

<span data-ttu-id="7dbe9-136">Líftímastöður afurðar eru ekki studdar af gagnaeiningum og líftímastöðu er hægt að stilla í breytilega stöðu gegnum annaðhvort gagnaeiningu útgefinnar afurðar eða gagnaeiningu útgefins afbrigðis.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-136">The product lifecycle states are supported by data entities, and the lifecycle state can be set to a variable state through either the released product data entity or the released variant data entity.</span></span>

## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="7dbe9-137">Finna úreltar afurðir og afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="7dbe9-137">Find obsolete products and products variants</span></span>

<span data-ttu-id="7dbe9-138">Þú getur keyrt hermigreiningu til að finna úreltar afurðir eða afurðaafbrigði og síðan uppfæra lífferilsstaða afurðar þeirra.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-138">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="7dbe9-139">Til að finna úreldar afurðir, sjá [Finna úrelt afurðaafbrigði og úthluta lífferilsstöðu afurðar](tasks/obsolete-product-variants.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe9-139">To find obsolete products, see [Find obsolete product variants and assign a product lifecycle state](tasks/obsolete-product-variants.md).</span></span> <span data-ttu-id="7dbe9-140">Þetta efni sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-140">This topic shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="7dbe9-141">Það sýnir einnig hvernig skal skoða herminiðurstöðurnar og meta hversu margar afurðir og afurðaafbrigði verða tengd nýjum lífferilsstaða afurðar þegar keyrð er uppfærslan án hermunar.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-141">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

<span data-ttu-id="7dbe9-142">Með því að keyra greininguna í hermistillingu, birtist afurðir og afurðaafbrigði sem eru úreltar á tilteknu formi, þar sem hægt er að endurskoða þær auðveldlega.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-142">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="7dbe9-143">Greiningin leitar að færslum og tilteknum aðalgögnum til að bera kennsl á afurðir sem hafa enga eftirspurn innan breytilegs tímabils og engar aðalgögn sem geta leitt til eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-143">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="7dbe9-144">Nýjar afurðir sem gefnar eru út innan breytilegs tíma má útiloka frá greiningunni.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-144">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="7dbe9-145">Þegar hermigreiningin skilar áætluðum niðurstöðum getur notandinn keyrt greininguna og sett nýtt lífferilsstaða afurðar til allra afurða sem auðkenndar eru úreltar með greiningunni.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-145">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  

> [!NOTE]
> <span data-ttu-id="7dbe9-146">Athugaðu að allar greiningar og uppfærslur verða að vera gerðar innan sama lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-146">Note that all analysis and updates must be done within the same legal entity.</span></span>  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="7dbe9-147">Viðmiðanir til að velja og uppfæra útgefnar afurðir eða afurðaafbrigði</span><span class="sxs-lookup"><span data-stu-id="7dbe9-147">Criteria to select and update released products or product variants</span></span>

<span data-ttu-id="7dbe9-148">Notaðu eftirfarandi viðmiðanir til að velja og uppfæra útgefnar afurðir eða afurðaafbrigði:</span><span class="sxs-lookup"><span data-stu-id="7dbe9-148">Use the following criteria to select and update the released products and product variants:</span></span>

- <span data-ttu-id="7dbe9-149">Lífferilsstaða afurðar eða afurðarafbrigðis verður að vera frábrugðin nýju, áformuðu ástandi.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-149">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span>
- <span data-ttu-id="7dbe9-150">Afurðin eða afurðarafbrigðið var búið til fyrir nokkrum dögum síðan miðað við fjölda daga sem þú slærð inn í svargluggann fyrir val.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-150">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span>
- <span data-ttu-id="7dbe9-151">Það eru engar opnar framleiðslupantanir (= staða < lokið) fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-151">There are no open production orders (= status < ended) for the product or product variant.</span></span>
- <span data-ttu-id="7dbe9-152">Það eru engar opnar birgðafærslur (= staða útgáfa ReservPhysical til QuotationIssue eða staða innhreyfingar Skráð í QuotationReceipt) fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-152">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span>
- <span data-ttu-id="7dbe9-153">Engin birgðafærslur eiga sér stað á síðustu dögum fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-153">There are no inventory transactions within the last number of days for the product or product variant.</span></span>
- <span data-ttu-id="7dbe9-154">Það er engin framtíðareftirspurn eða framboðspá fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-154">There is no future demand or supply forecast for the product or product variant.</span></span>  
- <span data-ttu-id="7dbe9-155">Engin lágmarks birgðir hefur verið stillt í vöruþekju fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-155">No minimum stock level has been set in item coverage for the product or product variant.</span></span>
- <span data-ttu-id="7dbe9-156">Engin föst kanban-regla virk fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-156">No active fixed quantity kanban rule for the product or product variant.</span></span>  
- <span data-ttu-id="7dbe9-157">Engar þjónustupöntunarlínur fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-157">No service order line for the product or product variant.</span></span>
- <span data-ttu-id="7dbe9-158">Engar virkar eða framtíðar sölu- eða innkaupsamningslínur fyrir afurð eða afurðaafbrigði.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-158">No active or future sales or purchase agreement lines for the product or product variant.</span></span>
- <span data-ttu-id="7dbe9-159">Afurð eða afurðaafbrigði er ekki notuð í BOM sem tengist samþykktri BOM útgáfu sem ekki er útrunnin fyrir afurð eða afbrigði sem er virk fyrir áætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="7dbe9-159">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dbe9-160">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="7dbe9-160">Related topics</span></span>

- [<span data-ttu-id="7dbe9-161">Stofna nýja líftímastöðu afurðar</span><span class="sxs-lookup"><span data-stu-id="7dbe9-161">Create a new product lifecycle state</span></span>](tasks/new-product-lifecycle-state.md)
- [<span data-ttu-id="7dbe9-162">Stofna sjálfgefna líftímastöðu afurðar</span><span class="sxs-lookup"><span data-stu-id="7dbe9-162">Create a default product lifecycle state</span></span>](tasks/default-product-lifecycle-state.md)
- [<span data-ttu-id="7dbe9-163">Úthluta líftímastöðu afurðar til útgefins afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="7dbe9-163">Assign a product lifecycle state to a released product master</span></span>](tasks/product-lifecycle-state-released-product-master.md)
- [<span data-ttu-id="7dbe9-164">Úthluta líftímastöðu afurðar til útgefinnar afurðar</span><span class="sxs-lookup"><span data-stu-id="7dbe9-164">Assign a product lifecycle state to a released product</span></span>](tasks/product-lifecycle-state-released-product.md)
- [<span data-ttu-id="7dbe9-165">Finna úrelt afurðaafbrigði og úthluta lífferilsstöðu afurðar</span><span class="sxs-lookup"><span data-stu-id="7dbe9-165">Find obsolete product variants and assign a product lifecycle state</span></span>](tasks/obsolete-product-variants.md)
- [<span data-ttu-id="7dbe9-166">Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="7dbe9-166">Create a product lifecycle state to exclude products from Master planning</span></span>](tasks/exclude-products-master-planning.md)
