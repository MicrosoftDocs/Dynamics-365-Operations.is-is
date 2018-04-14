---
title: "Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings beint úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6cf267d85795f6a7c253782b826cc75abef89d9f
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="15941-103">Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15941-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="15941-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings beint úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="15941-105">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="15941-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="15941-106">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="15941-107">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="15941-108">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="15941-109">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="15941-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="15941-110">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="15941-110">Templates and tasks</span></span>

<span data-ttu-id="15941-111">Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="15941-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="15941-112">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="15941-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="15941-113">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15941-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="15941-114">**Heiti sniðmátsins í Gagnaflutningi:** Sölureikningar (Fin og Ops í Sales) - beint</span><span class="sxs-lookup"><span data-stu-id="15941-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="15941-115">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="15941-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="15941-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="15941-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="15941-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="15941-117">SalesInvoiceLine</span></span>

<span data-ttu-id="15941-118">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar sölureikningshausa og línum geta átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="15941-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="15941-119">Vörur (Fin og Ops til Sales) - bein</span><span class="sxs-lookup"><span data-stu-id="15941-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="15941-120">Reikningar (Sales við Fin and Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="15941-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="15941-121">Tengiliðir (Sales við Fin and Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="15941-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="15941-122">Sölupöntunarhaus og -línur (Fin og Ops við Sales) - Beint</span><span class="sxs-lookup"><span data-stu-id="15941-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="15941-123">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="15941-123">Entity set</span></span>

| <span data-ttu-id="15941-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15941-124">Finance and Operations</span></span>                               | <span data-ttu-id="15941-125">Sölur</span><span class="sxs-lookup"><span data-stu-id="15941-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="15941-126">Sölureikningshausar viðskiptavinar sem unnið er með utan frá</span><span class="sxs-lookup"><span data-stu-id="15941-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="15941-127">Reikningar</span><span class="sxs-lookup"><span data-stu-id="15941-127">Invoices</span></span>       |
| <span data-ttu-id="15941-128">Sölureikningslínur viðskiptavinar sem unnið er með utan frá</span><span class="sxs-lookup"><span data-stu-id="15941-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="15941-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="15941-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="15941-130">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="15941-130">Entity flow</span></span>

<span data-ttu-id="15941-131">Sölureikningar eru búnir til í Finance and Operations og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="15941-132">Eins og er er skattur tengdur gjöldum á sölureikningshaus er ekki tekinn með í samstillingu úr Finance and Operations í Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="15941-133">Sales styður ekki skattupplýsingar á hausstiginu.</span><span class="sxs-lookup"><span data-stu-id="15941-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="15941-134">Hinsvegar er skattur sem tengist gjöldum á línustigi er innifalinn í samstillingu.</span><span class="sxs-lookup"><span data-stu-id="15941-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="15941-135">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="15941-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="15941-136">Reitnum **Reikningsnúmer** er bætt við eininguna **Reikningur** og birtur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="15941-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="15941-137">Hnappurinn **Stofna reikning** á **Sölupöntun** síðunni er falinn vegna þess að reikningar verða búnir til í Finance and Operations og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="15941-138">Ekki er hægt að breyta siðunni **Reikningur** vegna þess að reikningar verða samstilltir úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15941-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="15941-139">**Staða sölupöntunar** breytist sjálfkrafa í **Reikningsfært** þegar tengdur reikningur úr Finance and Operations hefur verið samstilltur við Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="15941-140">Einnig var eiganda sölupöntunar sem reikningurinn var búinn til úr úthlutað sem eiganda reikningsins.</span><span class="sxs-lookup"><span data-stu-id="15941-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="15941-141">Því getur eigandi sölurekningsins skoðað reikninginn.</span><span class="sxs-lookup"><span data-stu-id="15941-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="15941-142">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="15941-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="15941-143">Áður en sölureikningar eru samstilltir er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.</span><span class="sxs-lookup"><span data-stu-id="15941-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="15941-144">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="15941-144">Setup in Sales</span></span>

<span data-ttu-id="15941-145">Farið í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:</span><span class="sxs-lookup"><span data-stu-id="15941-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="15941-146">**Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="15941-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="15941-147">**Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="15941-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="15941-148">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="15941-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="15941-149">SalesInvoiceHeader task</span><span class="sxs-lookup"><span data-stu-id="15941-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="15941-150">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **InvoiceCountryRegionId** í **BillingAddress\_Land**.</span><span class="sxs-lookup"><span data-stu-id="15941-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="15941-151">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.</span><span class="sxs-lookup"><span data-stu-id="15941-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="15941-152">Verðlisti er nauðsynlegur til að búa til reikninga í Sales.</span><span class="sxs-lookup"><span data-stu-id="15941-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="15941-153">Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="15941-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="15941-154">Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="15941-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="15941-155">Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="15941-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="15941-156">Sniðmátsgildið fyrir **pricelevelid.name \[Heiti verðlista\]** er gildisvörpun sem byggir á gjaldmiðli með USD = CRM Service USA (dæmi).</span><span class="sxs-lookup"><span data-stu-id="15941-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="15941-157">SalesInvoiceLine verkefni</span><span class="sxs-lookup"><span data-stu-id="15941-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="15941-158">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Mælieining**.</span><span class="sxs-lookup"><span data-stu-id="15941-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="15941-159">Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="15941-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="15941-160">Sniðmátsgildi með gildisvörpun er skiglreint fyrir **SalesUnitSymbol** í **Magn\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="15941-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="15941-161">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="15941-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="15941-162">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="15941-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="15941-163">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="15941-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="15941-164">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="15941-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="15941-165">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15941-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="15941-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="15941-166">SalesInvoiceHeader</span></span>

![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="15941-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="15941-168">SalesInvoiceLine</span></span>

![Sniðmátsvörpun í Gagnasamþættingu](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="15941-170">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="15941-170">Related topics</span></span>

[<span data-ttu-id="15941-171">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="15941-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="15941-172">Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15941-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="15941-173">Samstilla afurðir beint úr Finance and Operations við afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="15941-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="15941-174">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15941-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="15941-175">Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15941-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







