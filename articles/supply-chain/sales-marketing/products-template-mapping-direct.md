---
title: "Samstilla afurðir beint úr Finance and Operations við afurðir í Sales"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vörur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: feb9fbc066162e2caa9fc5dbaeec2c063ae23060
ms.contentlocale: is-is
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="11a5d-103">Samstilla afurðir beint úr Finance and Operations við afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="11a5d-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="11a5d-104">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="11a5d-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="11a5d-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vörur beint úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="11a5d-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="11a5d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="11a5d-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="11a5d-108">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="11a5d-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="11a5d-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="11a5d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="11a5d-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="11a5d-111">Templates and tasks</span></span>

<span data-ttu-id="11a5d-112">Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="11a5d-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="11a5d-113">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="11a5d-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="11a5d-114">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla vörur úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11a5d-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="11a5d-115">**Heiti sniðmátsins í Gagnaflutningi:** Vörur (Fin og Ops í Sales) - beint</span><span class="sxs-lookup"><span data-stu-id="11a5d-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="11a5d-116">**Heiti verksins í gagnasamþættingarverki:** Vörur</span><span class="sxs-lookup"><span data-stu-id="11a5d-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="11a5d-117">Ekki þarf að samstilla áður en samstilling vöru á sér stað.</span><span class="sxs-lookup"><span data-stu-id="11a5d-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="11a5d-118">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="11a5d-118">Entity set</span></span>

| <span data-ttu-id="11a5d-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11a5d-119">Finance and Operations</span></span>     | <span data-ttu-id="11a5d-120">Sölur</span><span class="sxs-lookup"><span data-stu-id="11a5d-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="11a5d-121">Seljanlegar útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="11a5d-121">Sellable released products</span></span> | <span data-ttu-id="11a5d-122">Afurðir</span><span class="sxs-lookup"><span data-stu-id="11a5d-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="11a5d-123">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="11a5d-123">Entity flow</span></span>

<span data-ttu-id="11a5d-124">Afurðum er stýrt í Finance and Operations og þær eru samstilltar í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="11a5d-125">**Seljanlegar útgefnar afurðir** gagnaeiningin í Finance and Operations flytur aðeins út vörur sem eru *seljanlegar*.</span><span class="sxs-lookup"><span data-stu-id="11a5d-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="11a5d-126">Seljanlegar vörur eru vörur sem hafa þær upplýsingar sem þær þurfa til að nota á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="11a5d-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="11a5d-127">Sama regla gildir þegar vara er villuleituð með því að nota **Villuleita** virknina á síðunni **Útgefin afurð**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="11a5d-128">Vörunúmerið er notað sem lykill.</span><span class="sxs-lookup"><span data-stu-id="11a5d-128">The product number is used as a key.</span></span> <span data-ttu-id="11a5d-129">Þegar afurðarafbrigði eru samstillt við Sales hefur hvert afurðarafbrigði einkvæmt vörukenni.</span><span class="sxs-lookup"><span data-stu-id="11a5d-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="11a5d-130">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="11a5d-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="11a5d-131">Í Sales hefur nýjum **Er viðhaldið að utan** reit verið bætt við vörur til að tákna að viðkomandi vöru sé viðhaldið að utan.</span><span class="sxs-lookup"><span data-stu-id="11a5d-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="11a5d-132">Gildið er sjálfkrafa stillt á **Já** við innflutning í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="11a5d-133">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="11a5d-133">The following values are available:</span></span>

- <span data-ttu-id="11a5d-134">**Já** – Vara á uppruna í Finance and Operations og er ekki hægt að breyta í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="11a5d-135">**Nei** – varan var upphaflega færð inn í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="11a5d-136">**(Autt)** – Varan var til staðar í Sales áður en Prospect to cash lausnin var virkjuð.</span><span class="sxs-lookup"><span data-stu-id="11a5d-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="11a5d-137">Reiturinn **Er viðhaldið að utan** hjálpar til við að tryggja að aðeins tilboð og sölupantanir með ytri vörur verði samstilltar við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11a5d-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="11a5d-138">Vörum sem er viðhaldið að utan er sjálfkrafa bætt við fyrsta gilda verðlistann með sama gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="11a5d-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="11a5d-139">Verðlistar eru skipulagðir í stafrófsröð.</span><span class="sxs-lookup"><span data-stu-id="11a5d-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="11a5d-140">Söluverð vöru úr Finance and Operations er notað sem verð á verðlistanum.</span><span class="sxs-lookup"><span data-stu-id="11a5d-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="11a5d-141">Því verður verðlisti að vera til staðar í Sales fyrir alla sölugjaldmiðla vöru í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11a5d-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="11a5d-142">Gengi gjaldmiðilsins á seljanlegu vörunni er stillt á bókhaldsgjaldmiðilinn í lögaðilanum sem varan er flutt út frá.</span><span class="sxs-lookup"><span data-stu-id="11a5d-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="11a5d-143">Vörusamstilling mun ekki heppnast nema til sé verðlisti sem hefur samsvarandi gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="11a5d-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="11a5d-144">Þú getur stjórnað verðskránni sem er notuð með samþættingunni með vörpun pricelevelid.name [Sjálfgildi Verðlisti (Nafn)] í Gagnasamþætting verkefninu.</span><span class="sxs-lookup"><span data-stu-id="11a5d-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="11a5d-145">Inntakið verður að vera í lágstöfum eingöngu.</span><span class="sxs-lookup"><span data-stu-id="11a5d-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="11a5d-146">Til dæmis yrði sjálfgildið fyrir verðlista í Sölu sem kallast „Staðlaður“: Áfangasvæði: pricelevelid.name [Sjálfgildi Verðskrá (Nafn)] og Kortategund: [ {"transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="11a5d-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="11a5d-147">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="11a5d-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="11a5d-148">Áður en samstilling er keyrð í fyrsta skipti þarf að fylla út Einkvæm afurð töfluna fyrir fyrirliggjandi vörur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11a5d-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="11a5d-149">Fyrirliggjandi vörur verða ekki samstilltar fyrr en verki er lokið.</span><span class="sxs-lookup"><span data-stu-id="11a5d-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="11a5d-150">Notaðu Leit í Finance and Operations til að leita að **Fylla út töflu fyrir einkvæma afurð**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-150">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="11a5d-151">Velja skal **Mynda töflu fyrir einkvæma afurð** til að keyra verkið.</span><span class="sxs-lookup"><span data-stu-id="11a5d-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="11a5d-152">Aðeins má keyra verkið einu sinni.</span><span class="sxs-lookup"><span data-stu-id="11a5d-152">This job must be run only one time.</span></span>

- <span data-ttu-id="11a5d-153">Gakktu úr skugga um að nauðsynleg virðisvörpun fyrir sölueininguna á milli Finance and Operations og Sales sé til staðar í vörpun **SalesUnitSymbol** í **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-153">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="11a5d-154">Uppfæra skal virðisvörpun fyrir **Einingarflokk** (**defaultuomscheduleid.name**) þannig að hann passi við **Einingarflokka** í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="11a5d-155">Sjálfgefið sniðmátsgildi er **Sjálfgefin eining**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="11a5d-156">Ganga skal úr skugga um að mælieining fyrir allar vörur úr Finance and Operations séu til staðar í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-156">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="11a5d-157">Ganga skal úr skugga um að verðlisti sé til staðar í Sales fyrir alla sölugjaldmiðla vöru í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11a5d-157">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="11a5d-158">Þegar vörur eru stofnaðar í Sales geta þær haft stöðuna **Drög** eða **Virkar**.</span><span class="sxs-lookup"><span data-stu-id="11a5d-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="11a5d-159">Þessu er stjórnað í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** í Sales.</span><span class="sxs-lookup"><span data-stu-id="11a5d-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="11a5d-160">Vörur sem hafa stöðuna **Drög** þegar þær eru búin til verður að virkja áður en hægt er að bæta við tilboðum eða sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="11a5d-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="11a5d-161">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="11a5d-161">Template mapping in Data integration</span></span>

<span data-ttu-id="11a5d-162">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="11a5d-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="11a5d-163">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11a5d-163">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Sniðmátsvörpun í Gagnasamþáttara](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="11a5d-165">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="11a5d-165">Related topics</span></span>

[<span data-ttu-id="11a5d-166">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="11a5d-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="11a5d-167">Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11a5d-167">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="11a5d-168">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11a5d-168">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="11a5d-169">Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11a5d-169">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="11a5d-170">Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11a5d-170">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




