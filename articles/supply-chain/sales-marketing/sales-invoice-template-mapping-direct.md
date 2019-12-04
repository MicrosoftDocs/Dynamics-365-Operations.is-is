---
title: Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur reikninga beint úr Dynamics 365 Supply Chain Management við Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fb5073fe8db0b51c4ea378cac57097e15e88bf83
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814053"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="45b0d-103">Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="45b0d-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45b0d-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur reikninga beint úr Dynamics 365 Supply Chain Management við Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="45b0d-105">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="45b0d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="45b0d-106">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="45b0d-107">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="45b0d-108">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="45b0d-109">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="45b0d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="45b0d-110">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="45b0d-110">Templates and tasks</span></span>

<span data-ttu-id="45b0d-111">Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="45b0d-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="45b0d-112">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="45b0d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="45b0d-113">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla reikningshausa og línur úr Supply Chain Management í Sales:</span><span class="sxs-lookup"><span data-stu-id="45b0d-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="45b0d-114">**Heiti sniðmátsins í Gagnaflutningi:** Sölureikningar (Fin og Ops í Sales) - beint</span><span class="sxs-lookup"><span data-stu-id="45b0d-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="45b0d-115">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="45b0d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="45b0d-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="45b0d-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="45b0d-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="45b0d-117">SalesInvoiceLine</span></span>

<span data-ttu-id="45b0d-118">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar sölureikningshausa og línum geta átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="45b0d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="45b0d-119">Afurðir (Supply Chain Management itl Sales) - Beint</span><span class="sxs-lookup"><span data-stu-id="45b0d-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="45b0d-120">Lyklar (Sales til Supply Chain Management) - Bein (ef notað)</span><span class="sxs-lookup"><span data-stu-id="45b0d-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="45b0d-121">Tengiliðir (Sales til Supply Chain Management) - Bein (ef notað)</span><span class="sxs-lookup"><span data-stu-id="45b0d-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="45b0d-122">Hausar og línur sölupantana (Supply Chain Management í Sales) - Beint</span><span class="sxs-lookup"><span data-stu-id="45b0d-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="45b0d-123">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="45b0d-123">Entity set</span></span>

| <span data-ttu-id="45b0d-124">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="45b0d-124">Supply Chain Management</span></span>                              | <span data-ttu-id="45b0d-125">Sala</span><span class="sxs-lookup"><span data-stu-id="45b0d-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="45b0d-126">Sölureikningshausar viðskiptavinar sem unnið er með utan frá</span><span class="sxs-lookup"><span data-stu-id="45b0d-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="45b0d-127">Reikningar</span><span class="sxs-lookup"><span data-stu-id="45b0d-127">Invoices</span></span>       |
| <span data-ttu-id="45b0d-128">Sölureikningslínur viðskiptavinar sem unnið er með utan frá</span><span class="sxs-lookup"><span data-stu-id="45b0d-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="45b0d-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="45b0d-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="45b0d-130">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="45b0d-130">Entity flow</span></span>

<span data-ttu-id="45b0d-131">Sölureikningar eru búnir til í Supply Chain Management og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="45b0d-132">Eins og er er skattur tengdur gjöldum á sölureikningshaus er ekki tekinn með í samstillingu úr Supply Chain Management í Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="45b0d-133">Sales styður ekki skattupplýsingar á hausstiginu.</span><span class="sxs-lookup"><span data-stu-id="45b0d-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="45b0d-134">Hinsvegar er skattur sem tengist gjöldum á línustigi er innifalinn í samstillingu.</span><span class="sxs-lookup"><span data-stu-id="45b0d-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="45b0d-135">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="45b0d-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="45b0d-136">Reitnum **Reikningsnúmer** er bætt við eininguna **Reikningur** og birtur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="45b0d-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="45b0d-137">Hnappurinn **Stofna reikning** á **Sölupöntun** síðunni er falinn vegna þess að reikningar verða búnir til í Supply Chain Management og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="45b0d-138">Ekki er hægt að breyta siðunni **Reikningur** vegna þess að reikningar verða samstilltir úr Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45b0d-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="45b0d-139">**Staða sölupöntunar** breytist sjálfkrafa í **Reikningsfært** þegar tengdur reikningur úr Supply Chain Management hefur verið samstilltur við Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="45b0d-140">Einnig var eiganda sölupöntunar sem reikningurinn var búinn til úr úthlutað sem eiganda reikningsins.</span><span class="sxs-lookup"><span data-stu-id="45b0d-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="45b0d-141">Því getur eigandi sölurekningsins skoðað reikninginn.</span><span class="sxs-lookup"><span data-stu-id="45b0d-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="45b0d-142">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="45b0d-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="45b0d-143">Áður en sölureikningar eru samstilltir er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.</span><span class="sxs-lookup"><span data-stu-id="45b0d-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="45b0d-144">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="45b0d-144">Setup in Sales</span></span>

<span data-ttu-id="45b0d-145">Farið í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:</span><span class="sxs-lookup"><span data-stu-id="45b0d-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="45b0d-146">**Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="45b0d-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="45b0d-147">**Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="45b0d-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="45b0d-148">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="45b0d-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="45b0d-149">SalesInvoiceHeader task</span><span class="sxs-lookup"><span data-stu-id="45b0d-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="45b0d-150">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **InvoiceCountryRegionId** í **BillingAddress\_Land**.</span><span class="sxs-lookup"><span data-stu-id="45b0d-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="45b0d-151">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.</span><span class="sxs-lookup"><span data-stu-id="45b0d-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="45b0d-152">Verðlisti er nauðsynlegur til að búa til reikninga í Sales.</span><span class="sxs-lookup"><span data-stu-id="45b0d-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="45b0d-153">Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="45b0d-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="45b0d-154">Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="45b0d-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="45b0d-155">Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="45b0d-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="45b0d-156">Sniðmátsgildið fyrir **pricelevelid.name \[Heiti verðlista\]** er gildisvörpun sem byggir á gjaldmiðli með USD = CRM Service USA (dæmi).</span><span class="sxs-lookup"><span data-stu-id="45b0d-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="45b0d-157">SalesInvoiceLine verkefni</span><span class="sxs-lookup"><span data-stu-id="45b0d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="45b0d-158">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Mælieining**.</span><span class="sxs-lookup"><span data-stu-id="45b0d-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="45b0d-159">Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Supply Chain Management sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="45b0d-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="45b0d-160">Sniðmátsgildi með gildisvörpun er skiglreint fyrir **SalesUnitSymbol** í **Magn\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="45b0d-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="45b0d-161">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="45b0d-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="45b0d-162">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="45b0d-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="45b0d-163">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="45b0d-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="45b0d-164">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="45b0d-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="45b0d-165">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar úr Sales í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45b0d-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="45b0d-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="45b0d-166">SalesInvoiceHeader</span></span>

![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="45b0d-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="45b0d-168">SalesInvoiceLine</span></span>

![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="45b0d-170">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="45b0d-170">Related topics</span></span>

[<span data-ttu-id="45b0d-171">Viðfang til sjóðstreymis</span><span class="sxs-lookup"><span data-stu-id="45b0d-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="45b0d-172">Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45b0d-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="45b0d-173">Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales</span><span class="sxs-lookup"><span data-stu-id="45b0d-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="45b0d-174">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45b0d-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="45b0d-175">Samstilling sölupantana beint á milli Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="45b0d-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
