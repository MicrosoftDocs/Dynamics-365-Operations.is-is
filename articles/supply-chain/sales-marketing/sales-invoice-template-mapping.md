---
title: "Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations"
description: "Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales."
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="70dee-103">Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="70dee-104">Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="70dee-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="70dee-105">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="70dee-105">Templates and tasks</span></span>

<span data-ttu-id="70dee-106">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="70dee-107">**Heiti sniðmátsins í Gagnaflutningi**</span><span class="sxs-lookup"><span data-stu-id="70dee-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="70dee-108">Sölureikningar (Fin og Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="70dee-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="70dee-109">**Heiti verksins í gagnasamþættingarverki**</span><span class="sxs-lookup"><span data-stu-id="70dee-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="70dee-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="70dee-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="70dee-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="70dee-111">SalesInvoiceLine</span></span>

<span data-ttu-id="70dee-112">Samstillingarverk sem er nauðsynlegt fyrir samstillingu hausa sölureiknings og lína:</span><span class="sxs-lookup"><span data-stu-id="70dee-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="70dee-113">Vörur (Fin og Ops til Sales )</span><span class="sxs-lookup"><span data-stu-id="70dee-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="70dee-114">Reikningar (Sales við Fin and Ops) (ef notað)</span><span class="sxs-lookup"><span data-stu-id="70dee-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="70dee-115">Tengiliðir (Sales við Fin and Ops) (ef notað)</span><span class="sxs-lookup"><span data-stu-id="70dee-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="70dee-116">Sölupöntunarhaus og -línur (Fin og Ops við Sales)</span><span class="sxs-lookup"><span data-stu-id="70dee-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="70dee-117">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="70dee-117">Entity set</span></span>

| <span data-ttu-id="70dee-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-118">Finance and Operations</span></span>                               | <span data-ttu-id="70dee-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="70dee-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="70dee-120">Sölur</span><span class="sxs-lookup"><span data-stu-id="70dee-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="70dee-121">Sölureikningshausar viðskiptavinar sem unnið er með utan frá</span><span class="sxs-lookup"><span data-stu-id="70dee-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="70dee-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="70dee-122">SalesInvoice</span></span>     | <span data-ttu-id="70dee-123">Reikningar</span><span class="sxs-lookup"><span data-stu-id="70dee-123">Invoices</span></span>       |
| <span data-ttu-id="70dee-124">Sölureikningslínur viðskiptavinar sem unnið er með utan frá</span><span class="sxs-lookup"><span data-stu-id="70dee-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="70dee-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="70dee-125">SalesInvoiceLine</span></span> | <span data-ttu-id="70dee-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="70dee-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="70dee-127">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="70dee-127">Entity flow</span></span>

<span data-ttu-id="70dee-128">Sölureikningar eru búnir til í Finance and Operations og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="70dee-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="70dee-129">Skattur tengdur gjöldum á **Sölureikningshaus** er ekki tekinn með í samstillingu úr Finance and Operations í Sales.</span><span class="sxs-lookup"><span data-stu-id="70dee-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="70dee-130">Þetta er vegna þess að Sales styður ekki skattupplýsingar á hausstiginu.</span><span class="sxs-lookup"><span data-stu-id="70dee-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="70dee-131">Skattur sem tengist gjöldum á línustigi er innifalinn.</span><span class="sxs-lookup"><span data-stu-id="70dee-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="70dee-132">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="70dee-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="70dee-133">**Reikningsnúmerareitur** er bætt við eininguna **Reikningur** og birtur á síðunni.</span><span class="sxs-lookup"><span data-stu-id="70dee-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="70dee-134">Hnappurinn **Stofna reikning** á **Sölupöntun** síðunni er falinn vegna þess að reikningar verða búnir til í Finance and Operations og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="70dee-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="70dee-135">Ekki er hægt að breyta siðunni **Reikningur** vegna þess að reikningar verða samstilltir úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="70dee-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="70dee-136">**Staða sölupöntunar** breytist sjálfkrafa í **Reikningsfært** þegar tengdur reikningur úr Finance and Operations hefur verið samstilltur við Sales.</span><span class="sxs-lookup"><span data-stu-id="70dee-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="70dee-137">Einnig var eiganda sölupöntunar sem reikningurinn var búinn til úr úthlutað sem eiganda reikningsins.</span><span class="sxs-lookup"><span data-stu-id="70dee-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="70dee-138">Þetta gefur eiganda sölurekningsins færi á á skoða reikninginn.</span><span class="sxs-lookup"><span data-stu-id="70dee-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="70dee-139">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="70dee-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="70dee-140">Fyrir samstillingu sölureikninga er mikilvægt að uppfæra kerfin með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="70dee-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="70dee-141">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="70dee-141">Setup in Sales</span></span>

- <span data-ttu-id="70dee-142">Undir **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales**, skal tryggja að **Nota reikningskerfi verðs** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="70dee-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="70dee-143">Farðu í **Stillingar**  >  **Stjórnun**  >  **Kerfisstillingar**  >  **Sales** og gakktu úr skugga um að reiturinn **Útreikningsaðferð afsláttar** sé stilltur á **Línatriði**.</span><span class="sxs-lookup"><span data-stu-id="70dee-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="70dee-144">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="70dee-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="70dee-145">SalesInvoiceHeader task</span><span class="sxs-lookup"><span data-stu-id="70dee-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="70dee-146">Uppfæra vörpun fyrir **CDS Organization ID** í **Uppruni** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="70dee-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="70dee-147">Sjálfgefið sniðmátsgildi fyrir **SalesOrder_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="70dee-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="70dee-148">Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="70dee-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="70dee-149">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="70dee-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="70dee-150">Gakktu úr skugga um að nauðsynleg kortlagning sé fyrir hendi í **Uppruni** > **CDS fyrir InvoiceCountryRegionId** í **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="70dee-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="70dee-151">Sniðmátsgildi er **ValueMap** með vörpun á fjölda landa.</span><span class="sxs-lookup"><span data-stu-id="70dee-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="70dee-152">**Verðskrá** er nauðsynleg til að búa til reikninga í Sales.</span><span class="sxs-lookup"><span data-stu-id="70dee-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="70dee-153">Uppfærið **ValueMap** í **CDS** > **Áfangastaður fyrir pricelevelid.name [Price List Name]** í **Verðlisti** notaður í Sales eftir gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="70dee-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="70dee-154">Þú getur annað hvort notað sjálfgefinn **verðlista** fyrir einn gjaldmiðil eða **ValueMap** ef **Verðlisti** er í mörgum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="70dee-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="70dee-155">Sniðmátsgildi fyrir **pricelevelid.name [Price List Name]** er **ValueMap** byggt á **Gjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="70dee-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="70dee-156">usd: CRM Service USA (dæmi).</span><span class="sxs-lookup"><span data-stu-id="70dee-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="70dee-157">SalesInvoiceLine verkefni</span><span class="sxs-lookup"><span data-stu-id="70dee-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="70dee-158">Gakktu úr skugga um að nauðsynleg vörpun sé til staðar í **Uppruni** > **CDS fyrir mælieiningu**.</span><span class="sxs-lookup"><span data-stu-id="70dee-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="70dee-159">Gakktu úr skugga um að nauðsynlegt **ValueMap** fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar í **Uppruni** > **CDS vörpun**.</span><span class="sxs-lookup"><span data-stu-id="70dee-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="70dee-160">Sniðmátsgildi með **ValueMap** er skilgreint **SalesUnitSymbol í Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="70dee-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="70dee-161">Uppfæra vörpun fyrir **CDS Organization ID í uppruna** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="70dee-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="70dee-162">Sjálfgefið sniðmátsgildi fyrir **SalesInvoicer_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="70dee-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="70dee-163">Sjálfgefið sniðmátsgildi fyrir **Product_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="70dee-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="70dee-164">Sniðmátsvörpun í Gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="70dee-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="70dee-165">**Greiðsluskilmálar**, **Farmskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefinni vörpun.</span><span class="sxs-lookup"><span data-stu-id="70dee-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="70dee-166">Vörpun þessara reita krefst þess að gildisvörpun sé sett upp, sem gildir sérstaklega fyrir gögnin í fyrirtækinu sem verið er að samstilla eininguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="70dee-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="70dee-167">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="70dee-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="70dee-172">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="70dee-172">Related topics</span></span>

[<span data-ttu-id="70dee-173">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="70dee-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="70dee-174">Samstilla lykla úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="70dee-175">Samstilla tengiliði úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="70dee-176">Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="70dee-177">Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="70dee-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


