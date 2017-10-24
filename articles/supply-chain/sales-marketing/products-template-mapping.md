---
title: "Samstilla afurðir úr Finance and Operations í afurðir í Sales"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations, Enterprise edition í Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="c85dc-103">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="c85dc-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c85dc-104">Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="c85dc-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="c85dc-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations, Enterprise edition í Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="c85dc-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="c85dc-106">Template and task</span></span>

<span data-ttu-id="c85dc-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) í Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="c85dc-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="c85dc-108">Nafn sniðmáts: Afurðir (Fin and Ops í Sales)</span><span class="sxs-lookup"><span data-stu-id="c85dc-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="c85dc-109">Nafn verkefnis í verki: Afurðir</span><span class="sxs-lookup"><span data-stu-id="c85dc-109">Name of task in project: Products</span></span>

<span data-ttu-id="c85dc-110">Samstilla verkefni nauðsynleg fyrir samstillingu afurðar: Ekkert</span><span class="sxs-lookup"><span data-stu-id="c85dc-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="c85dc-111">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="c85dc-111">Entity set</span></span>

| <span data-ttu-id="c85dc-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="c85dc-112">**Finance and Operations**</span></span> | <span data-ttu-id="c85dc-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="c85dc-113">**CDS**</span></span> | <span data-ttu-id="c85dc-114">**Sala**</span><span class="sxs-lookup"><span data-stu-id="c85dc-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="c85dc-115">Seljanlegar útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="c85dc-115">Sellable released products</span></span> | <span data-ttu-id="c85dc-116">Afurð</span><span class="sxs-lookup"><span data-stu-id="c85dc-116">Product</span></span> | <span data-ttu-id="c85dc-117">Afurðir</span><span class="sxs-lookup"><span data-stu-id="c85dc-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c85dc-118">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="c85dc-118">Entity flow</span></span>

<span data-ttu-id="c85dc-119">Afurðum er stýrt í Finance and Operations og þær eru samstilltar í Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="c85dc-120">Gagnaeiningin **Seljanlegar útgefnar afurðir** í Finance and Operations flytja aðeins út afurðir sem eru seljanlegar, sem þýðir að afurðir hafi þær upplýsingar sem þarf að nota í sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="c85dc-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="c85dc-121">Sömu reglur gilda þegar afurð er villuleituð með virkninni **Villuleita** á síðunni **Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="c85dc-122">**Afurðarnúmerið** er notað sem lykill, sem þýðir að afurðarafbrigði eru samstillt í CDS og Sales með einstökum **Auðkennum afurðar** á hvert **Afurðarafbrigði**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c85dc-123">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="c85dc-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c85dc-124">Í Sales er nýjum reitum í afurðum sem er **Unnið með utan frá** bætt við til að gefa til kynna að gefinni afurð sé bætt við utan frá.</span><span class="sxs-lookup"><span data-stu-id="c85dc-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="c85dc-125">Gildið er sjálfkrafa stillt á **Já** við innflutning í Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="c85dc-126">**Unnið með utan frá = Já**: Afurð á uppruna sinn í Finance and Operations og ekki er hægt að breyta henni í Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="c85dc-127">**Unnið með utan frá = Nei**: Afurð er skráð beint inn í Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="c85dc-128">**Unnið með utan frá = Autt**: Afurð er til í Sales áður en lausnin Prospect to cash er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="c85dc-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="c85dc-129">Upplýsingarnar í **Unnið með utan frá** eru notaðar til að tryggja að aðeins **Verðtilboð** og **Sölupantanir** með **Afurðum sem unnið er með utan frá** séu samstilltar við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c85dc-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="c85dc-130">**Afurðum sem unnið er með utan frá** er sjálfkrafa bætt við fyrsta gilda **Verðlistann** með sama gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="c85dc-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="c85dc-131">Athugaðu að listanum er raðað í stafrófsröð eftir **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="c85dc-132">Söluverð afurðar úr Finance and Operations er notað sem verð í **Verðlistanum**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="c85dc-133">Þetta þýðir að það verður að hafa **Verðlista** í Sales fyrir hvern **Sölugjaldmiðil afurðar** í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c85dc-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="c85dc-134">Gjaldmiðill í útgefnum seljanlegum afurðum er stilltur á bókhaldsgjaldmiðilinn í þeim lögaðila, þaðan sem afurðin er flutt út frá.</span><span class="sxs-lookup"><span data-stu-id="c85dc-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="c85dc-135">Afurðarsamstilling gengur ekki eftir án **Verðlista** með samsvarandi gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="c85dc-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c85dc-136">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="c85dc-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="c85dc-137">Áður en fyrsta samstilling er keyrð, verður að fylla út **Töflu fyrir einkvæma afurð** fyrir núverandi afurðir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c85dc-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="c85dc-138">Núverandi afurðir samstillast ekki fyrr en þessu er lokið.</span><span class="sxs-lookup"><span data-stu-id="c85dc-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="c85dc-139">Notaðu Leit í Finance and Operations til að leita að **Fylla út töflu fyrir einkvæma afurð**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="c85dc-140">Smelltu á **Fylla út töflu fyrir einkvæma afurð** til að keyra vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="c85dc-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="c85dc-141">Aðeins þarf að keyra þessa vinnslu einu sinni.</span><span class="sxs-lookup"><span data-stu-id="c85dc-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="c85dc-142">Vertu viss um að nauðsynlegt **ValueMap** fyrir sölu á **Mælieiningu** (UOM) í Finance and Operations sé til í **Uppruna -\> CDS vörpun SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="c85dc-143">Uppfærðu **CDS-fyrirtækjaauðkenni Organization_OrganizationId** í **Uppruni -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="c85dc-144">Sniðmátsgildi er sjálfkrafa ORG001.</span><span class="sxs-lookup"><span data-stu-id="c85dc-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="c85dc-145">Uppfærðu **ValueMap** fyrir **Einingahóp** (**defaultuomscheduleid.name**) í **CDS -\> Viðtökustaður** svo það hæfi **Einingahópum** í Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="c85dc-146">Sniðmátsgildi er sjálfkrafa á **Sjálfgefin eining**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="c85dc-147">Vertu viss um að allar afurðir sem selja mælieiningar úr Finance and Operations séu til í Sales með gildi **CDS-tiltektarlista**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="c85dc-148">Vertu viss um að **Verðlistar** séu til í Sales fyrir hvern sölugjaldmiðil afurðar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c85dc-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="c85dc-149">Hægt er að stofna afurðir í Sales með stöðunni **Drög** eða **Virk**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="c85dc-150">Þessu er stýrt í **Kerfisstillingar** undir **Sala** í Sales.</span><span class="sxs-lookup"><span data-stu-id="c85dc-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="c85dc-151">Virkja þarf afurðir sem stofnaðar eru með stöðu fyrir drög áður en hægt er að bæta þeim við **Verðtilboð** eða **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="c85dc-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c85dc-152">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="c85dc-152">Template mapping in data integrator</span></span>

<span data-ttu-id="c85dc-153">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="c85dc-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![sniðmátsvörpun í gagnasamþáttara](./media/products-template-mapping-data-integrator-1.png)

![sniðmátsvörpun fyrir afurðir í gagnasamþáttara](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="c85dc-156">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="c85dc-156">Related topics</span></span>

[<span data-ttu-id="c85dc-157">Samstilla lykla frá Sales til viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c85dc-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="c85dc-158">Samstilla tengiliði úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c85dc-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="c85dc-159">Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c85dc-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="c85dc-160">Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c85dc-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="c85dc-161">Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c85dc-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


