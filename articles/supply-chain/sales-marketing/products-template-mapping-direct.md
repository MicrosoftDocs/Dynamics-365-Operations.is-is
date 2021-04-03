---
title: Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla vörur úr Dynamics 365 Supply Chain Management við Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f5e91d4dac8ea6d19fa32abca4e9ff73c7cd4a88
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234994"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="5a69c-103">Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales</span><span class="sxs-lookup"><span data-stu-id="5a69c-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="5a69c-104">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Microsoft Dataverse fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="5a69c-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="5a69c-105">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verk sem notuð eru til að samstilla vörur beint úr Dynamics 365 Supply Chain Management við Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5a69c-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="5a69c-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5a69c-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="5a69c-108">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5a69c-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5a69c-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5a69c-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5a69c-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="5a69c-111">Templates and tasks</span></span>

<span data-ttu-id="5a69c-112">Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="5a69c-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5a69c-113">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="5a69c-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5a69c-114">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla afurðir frá Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="5a69c-115">**Heiti sniðmátsins í Gagnaflutningi:** Vörur (Supply Chain Management í Sales) - beint</span><span class="sxs-lookup"><span data-stu-id="5a69c-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="5a69c-116">**Heiti verksins í gagnasamþættingarverki:** Vörur</span><span class="sxs-lookup"><span data-stu-id="5a69c-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="5a69c-117">Ekki þarf að samstilla áður en samstilling vöru á sér stað.</span><span class="sxs-lookup"><span data-stu-id="5a69c-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5a69c-118">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="5a69c-118">Entity set</span></span>

| <span data-ttu-id="5a69c-119">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="5a69c-119">Supply Chain Management</span></span>    | <span data-ttu-id="5a69c-120">Sala</span><span class="sxs-lookup"><span data-stu-id="5a69c-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="5a69c-121">Seljanlegar útgefnar afurðir</span><span class="sxs-lookup"><span data-stu-id="5a69c-121">Sellable released products</span></span> | <span data-ttu-id="5a69c-122">Afurðir</span><span class="sxs-lookup"><span data-stu-id="5a69c-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5a69c-123">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="5a69c-123">Entity flow</span></span>

<span data-ttu-id="5a69c-124">Afurðum er stjórnað í Supply Chain Management og þær samstilltar við Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="5a69c-125">**Seljanlegar útgefnar afurðir** gagnaeiningin í Supply Chain Management flytur aðeins út vörur sem eru *seljanlegar*.</span><span class="sxs-lookup"><span data-stu-id="5a69c-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="5a69c-126">Seljanlegar vörur eru vörur sem hafa þær upplýsingar sem þær þurfa til að nota á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="5a69c-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="5a69c-127">Sama regla gildir þegar vara er villuleituð með því að nota **Villuleita** virknina á síðunni **Útgefin afurð**.</span><span class="sxs-lookup"><span data-stu-id="5a69c-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="5a69c-128">Vörunúmerið er notað sem lykill.</span><span class="sxs-lookup"><span data-stu-id="5a69c-128">The product number is used as a key.</span></span> <span data-ttu-id="5a69c-129">Þegar afurðarafbrigði eru samstillt við Sales hefur hvert afurðarafbrigði einkvæmt vörukenni.</span><span class="sxs-lookup"><span data-stu-id="5a69c-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5a69c-130">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="5a69c-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5a69c-131">Í Sales hefur nýjum **Er viðhaldið að utan** reit verið bætt við vörur til að tákna að viðkomandi vöru sé viðhaldið að utan.</span><span class="sxs-lookup"><span data-stu-id="5a69c-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="5a69c-132">Gildið er sjálfkrafa stillt á **Já** við innflutning í Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="5a69c-133">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="5a69c-133">The following values are available:</span></span>

- <span data-ttu-id="5a69c-134">**Já** – Vara á uppruna í Supply Chain Management og er ekki hægt að breyta í Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="5a69c-135">**Nei** – varan var upphaflega færð inn í Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="5a69c-136">**(Autt)** – Varan var til staðar í Sales áður en Prospect to cash lausnin var virkjuð.</span><span class="sxs-lookup"><span data-stu-id="5a69c-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="5a69c-137">Reiturinn **Er viðhaldið að utan** hjálpar til við að tryggja að aðeins tilboð og sölupantanir með ytri vörur verði samstilltar við Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a69c-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="5a69c-138">Vörum sem er viðhaldið að utan er sjálfkrafa bætt við fyrsta gilda verðlistann með sama gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="5a69c-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="5a69c-139">Verðlistar eru skipulagðir í stafrófsröð.</span><span class="sxs-lookup"><span data-stu-id="5a69c-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="5a69c-140">Söluverð vöru úr Supply Chain Management er notað sem verð á verðlistanum.</span><span class="sxs-lookup"><span data-stu-id="5a69c-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="5a69c-141">Því verður verðlisti að vera til staðar í Sales fyrir alla sölugjaldmiðla vöru í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a69c-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="5a69c-142">Gengi gjaldmiðilsins á seljanlegu vörunni er stillt á bókhaldsgjaldmiðilinn í lögaðilanum sem varan er flutt út frá.</span><span class="sxs-lookup"><span data-stu-id="5a69c-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="5a69c-143">Vörusamstilling mun ekki heppnast nema til sé verðlisti sem hefur samsvarandi gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="5a69c-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="5a69c-144">Þú getur stjórnað verðskránni sem er notuð með samþættingunni með vörpun pricelevelid.name [Sjálfgildi Verðlisti (Nafn)] í Gagnasamþætting verkefninu.</span><span class="sxs-lookup"><span data-stu-id="5a69c-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="5a69c-145">Inntakið verður að vera í lágstöfum eingöngu.</span><span class="sxs-lookup"><span data-stu-id="5a69c-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="5a69c-146">Til dæmis yrði sjálfgildið fyrir verðlista í Sölu sem kallast „Staðlaður“: Áfangasvæði: pricelevelid.name [Sjálfgildi Verðskrá (Nafn)] og Kortategund: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="5a69c-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5a69c-147">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="5a69c-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="5a69c-148">Áður en samstilling er keyrð í fyrsta skipti þarf að fylla út Einkvæm afurð töfluna fyrir fyrirliggjandi vörur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a69c-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="5a69c-149">Fyrirliggjandi vörur verða ekki samstilltar fyrr en verki er lokið.</span><span class="sxs-lookup"><span data-stu-id="5a69c-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="5a69c-150">Notaðu Leit í Supply Chain Management til að leita að **Fylla út töflu fyrir einkvæma afurð**.</span><span class="sxs-lookup"><span data-stu-id="5a69c-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="5a69c-151">Velja skal **Mynda töflu fyrir einkvæma afurð** til að keyra verkið.</span><span class="sxs-lookup"><span data-stu-id="5a69c-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="5a69c-152">Aðeins má keyra verkið einu sinni.</span><span class="sxs-lookup"><span data-stu-id="5a69c-152">This job must be run only one time.</span></span>

- <span data-ttu-id="5a69c-153">Gakktu úr skugga um að nauðsynleg virðisvörpun fyrir sölueininguna á milli Supply Chain Management og Sales sé til staðar í vörpun **SalesUnitSymbol** í **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="5a69c-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="5a69c-154">Uppfæra skal virðisvörpun fyrir **Einingarflokk** (**defaultuomscheduleid.name**) þannig að hann passi við **Einingarflokka** í Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="5a69c-155">Sjálfgefið sniðmátsgildi er **Sjálfgefin eining**.</span><span class="sxs-lookup"><span data-stu-id="5a69c-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="5a69c-156">Ganga skal úr skugga um að mælieining fyrir allar vörur úr Supply Chain Management séu til staðar í Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="5a69c-157">Ganga skal úr skugga um að verðlisti sé til staðar í Sales fyrir alla sölugjaldmiðla vöru í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a69c-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="5a69c-158">Þegar vörur eru stofnaðar í Sales geta þær haft stöðuna **Drög** eða **Virkar**.</span><span class="sxs-lookup"><span data-stu-id="5a69c-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="5a69c-159">Þessu er stjórnað í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** í Sales.</span><span class="sxs-lookup"><span data-stu-id="5a69c-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="5a69c-160">Vörur sem hafa stöðuna **Drög** þegar þær eru búin til verður að virkja áður en hægt er að bæta við tilboðum eða sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="5a69c-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5a69c-161">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="5a69c-161">Template mapping in Data integration</span></span>

<span data-ttu-id="5a69c-162">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="5a69c-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5a69c-163">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar úr Sales í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a69c-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Sniðmátsvörpun í Gagnasamþáttara](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="5a69c-165">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="5a69c-165">Related topics</span></span>

[<span data-ttu-id="5a69c-166">Viðfang til sjóðstreymis</span><span class="sxs-lookup"><span data-stu-id="5a69c-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5a69c-167">Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5a69c-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5a69c-168">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5a69c-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5a69c-169">Samstilling sölupantana beint á milli Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5a69c-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5a69c-170">Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales</span><span class="sxs-lookup"><span data-stu-id="5a69c-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]