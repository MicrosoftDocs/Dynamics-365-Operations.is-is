---
title: "Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations"
description: "Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="5b437-103">Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b437-104">Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölureiknings úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="5b437-105">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="5b437-105">Template and tasks</span></span>

<span data-ttu-id="5b437-106">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="5b437-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="5b437-107">**Heiti sniðmáts í Gagnaflutningi**</span><span class="sxs-lookup"><span data-stu-id="5b437-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="5b437-108">Sölupantanir (Sales við Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="5b437-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="5b437-109">**Heiti verksins í gagnaflutningsverki**</span><span class="sxs-lookup"><span data-stu-id="5b437-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="5b437-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="5b437-110">OrderHeader</span></span>
    - <span data-ttu-id="5b437-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="5b437-111">OrderLine</span></span>

<span data-ttu-id="5b437-112">Samstillingarverk er nauðsynlegt fyrir samstillingu hausa sölureiknings og lína:</span><span class="sxs-lookup"><span data-stu-id="5b437-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="5b437-113">Vörur (Fin og Ops til Sales )</span><span class="sxs-lookup"><span data-stu-id="5b437-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="5b437-114">Reikningar (Sales við Fin and Ops) (ef notað)</span><span class="sxs-lookup"><span data-stu-id="5b437-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="5b437-115">Tengiliðir við viðskiptavini (Sales við Fin and Ops) (ef notað)</span><span class="sxs-lookup"><span data-stu-id="5b437-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="5b437-116">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="5b437-116">Entity set</span></span>

| <span data-ttu-id="5b437-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-117">Finance and Operations</span></span> |    <span data-ttu-id="5b437-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="5b437-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="5b437-119">Sölur</span><span class="sxs-lookup"><span data-stu-id="5b437-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="5b437-120">Hausar CDS-sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="5b437-120">CDS sales order headers</span></span>| <span data-ttu-id="5b437-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="5b437-121">SalesOrder</span></span>     | <span data-ttu-id="5b437-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="5b437-122">SalesOrders</span></span> |
| <span data-ttu-id="5b437-123">CDS sölupöntunarlínur</span><span class="sxs-lookup"><span data-stu-id="5b437-123">CDS sales order lines</span></span>  | <span data-ttu-id="5b437-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="5b437-124">SalesOrderLine</span></span> | <span data-ttu-id="5b437-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="5b437-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="5b437-126">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="5b437-126">Entity flow</span></span>

<span data-ttu-id="5b437-127">Sölupantanir eru búnar til í Finance and Operations og samstilltar við Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="5b437-128">Síur í sniðmáti tryggja að aðeins viðeigandi sölupantanir séu innifaldar í samstillingu:</span><span class="sxs-lookup"><span data-stu-id="5b437-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="5b437-129">Bæði pöntun og innheimta viðskiptavinar á sölupöntun sem á uppruna sinn í Sales verða teknar með í samstillingu.</span><span class="sxs-lookup"><span data-stu-id="5b437-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="5b437-130">Í Finance and Operations er reitirnir **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** notaðir til að rekja samstillingu í gagnaeiningum.</span><span class="sxs-lookup"><span data-stu-id="5b437-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="5b437-131">**Sölupöntun** í Finance and Operations verður að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="5b437-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="5b437-132">Aðeins staðfestar sölupantanir eða sölupantanir með hærri vinnslustöðu, til dæmis, Sent eða Reikningsfært, eru samstilltar við Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="5b437-133">Eftir að sölupöntun er búin til eða henni breytt verður að keyra runuvinnsluna **Reikna heildarsölu** í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b437-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="5b437-134">Aðeins sölupantanir með reiknaðar samtölur verða samstilltar við CDS og Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="5b437-135">Skattur tengdur gjöldum á **Sölupöntunarhaus** er ekki tekinn með í samstillingu úr Finance and Operations í Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="5b437-136">Þetta er vegna þess að Sales styður ekki skattupplýsingar á hausstiginu.</span><span class="sxs-lookup"><span data-stu-id="5b437-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="5b437-137">Skattur sem tengist gjöldum á línustigi er innifalinn.</span><span class="sxs-lookup"><span data-stu-id="5b437-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5b437-138">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="5b437-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5b437-139">Nýjum reitum er bætt við eininguna **Pöntun** og birtir á síðunni:</span><span class="sxs-lookup"><span data-stu-id="5b437-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="5b437-140">**Er viðhaldið utanfrá** - Stillt á **Já** þegar pöntunin er úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b437-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="5b437-141">**Vinnslustaða** - Notuð til að sýna vinnslustöðu pantanar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b437-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="5b437-142">Gildi eru:</span><span class="sxs-lookup"><span data-stu-id="5b437-142">Values are:</span></span>

    - <span data-ttu-id="5b437-143">Í gangi</span><span class="sxs-lookup"><span data-stu-id="5b437-143">Active</span></span>
    - <span data-ttu-id="5b437-144">Staðfest</span><span class="sxs-lookup"><span data-stu-id="5b437-144">Confirmed</span></span>
    - <span data-ttu-id="5b437-145">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="5b437-145">Packing Slip</span></span>
    - <span data-ttu-id="5b437-146">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="5b437-146">Invoiced</span></span>
    - <span data-ttu-id="5b437-147">Tekið til</span><span class="sxs-lookup"><span data-stu-id="5b437-147">Picked</span></span>
    - <span data-ttu-id="5b437-148">Tínt að hluta</span><span class="sxs-lookup"><span data-stu-id="5b437-148">Partially Picked</span></span>
    - <span data-ttu-id="5b437-149">Tekið til að hluta</span><span class="sxs-lookup"><span data-stu-id="5b437-149">Partially Packed</span></span>
    - <span data-ttu-id="5b437-150">Sent</span><span class="sxs-lookup"><span data-stu-id="5b437-150">Shipped</span></span>
    - <span data-ttu-id="5b437-151">Afhent að hluta</span><span class="sxs-lookup"><span data-stu-id="5b437-151">Partially Shipped</span></span>
    - <span data-ttu-id="5b437-152">Reikningsfært að hluta</span><span class="sxs-lookup"><span data-stu-id="5b437-152">Partially Invoiced</span></span>
    - <span data-ttu-id="5b437-153">Afturkallað</span><span class="sxs-lookup"><span data-stu-id="5b437-153">Cancelled</span></span>

<span data-ttu-id="5b437-154">Stillingin **Er aðens með utanaðkomandi vörur** er notuð í öðrum sviðsmyndum sölupantana (úr Sales í Finance and Operation samstillingu) til að halda utan um það hvort sölupöntun sé eingöngu með **Vörur sem viðhaldið er utanfrá**, en í því tilfelli er vörum viðhaldið í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b437-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="5b437-155">Þetta tryggir að þú reynir ekki að samstilla sölupöntunarlínur með vörum sem eru óþekktar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b437-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="5b437-156">**Stofna reikning**, **Hætta við pöntun**, **Endurreikna**, **Sækja vörur** og **Leita að aðsetri** hnapparnir á síðunni **Sölupöntun** eru ufaldir fyrir pantanir sem er viðhaldið utan frá þar sem reikningar verða stofnaðir í Finance and Operations og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="5b437-157">Ekki er hægt að breyta pöntunarsíðunni þar sem upplýsingar um sölupantanir verða samstilltar úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b437-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="5b437-158">**Staða sölupöntunar** verður áfram virk til að tryggja að gjöld úr Finance and Operations geti flætt í **Sölupöntun** í Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="5b437-159">Þessu er stjórnað með því að stilla sjálfgefið **Statecode [Status]** á **Virkt** í gagnasamþættingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="5b437-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5b437-160">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="5b437-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="5b437-161">Fyrir samstillingu sölupantana er mikilvægt að uppfæra kerfin með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="5b437-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5b437-162">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="5b437-162">Setup in Sales</span></span>

- <span data-ttu-id="5b437-163">Gakktu úr skugga um að heimildir fyrir teymi sem notandinn (úr Sales **Tenging**) er úthlutaður á.</span><span class="sxs-lookup"><span data-stu-id="5b437-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="5b437-164">Ef þú ert að nota sýnigögn hefur notandinn venjulega aðgang að stjórnendum en ekki teyminu.</span><span class="sxs-lookup"><span data-stu-id="5b437-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="5b437-165">Án þessa færð þú villu sem um að aðalsteymi vanti þegar þú keyrir verkefnið úr Gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="5b437-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="5b437-166">Undir **Stillingar** > **Öryggi** > **Teymi**, velurðu viðkomandi teymi, smellir á **Stjórna hlutverkum** og velur hlutverk með viðkomandi heimildum, t.d. kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="5b437-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="5b437-167">Undir **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales**, skal tryggja að **Nota reikningskerfi verðs** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5b437-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="5b437-168">Farðu í **Stillingar**  >  **Stjórnun**  >  **Kerfisstillingar**  >  **Sales** og gakktu úr skugga um að reiturinn **Útreikningsaðferð afsláttar** sé stilltur á **Línatriði**.</span><span class="sxs-lookup"><span data-stu-id="5b437-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="5b437-169">Uppsetning Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="5b437-170">Stilltu **Sala og markaðssetning** > **Reglubundin verkefni** > **Reikna út samtölu sölupantana** til að keyra sem runuvinnsla þar sem **Reikna út samtölu sölupantana** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5b437-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="5b437-171">Þetta er mikilvægt vegna þess að aðeins sölupantanir með samtölum verða samstilltar við CDS og Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="5b437-172">Tíðni runuvinnslunnar ætti að vera í samræmi við tíðni samstillingu sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="5b437-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5b437-173">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="5b437-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="5b437-174">SalesHeader verkefni</span><span class="sxs-lookup"><span data-stu-id="5b437-174">SalesHeader task</span></span>

- <span data-ttu-id="5b437-175">Uppfæra vörpun fyrir **CDS Organization ID í uppruna** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="5b437-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="5b437-176">Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="5b437-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="5b437-177">Sjálfgefið sniðmátsgildi fyrir **InvoiceAccount_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="5b437-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="5b437-178">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="5b437-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="5b437-179">Gakktu úr skugga um að nauðsynleg vörpun sé til staðar í **Uppruna** > **CDS fyrir InvoiceCountryRegionId í BillingAddress_Country** og fyrir **DeliveryCountryRegionId í DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="5b437-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="5b437-180">Sniðmátsgildi er **ValueMap** með vörpun á fjölda landa.</span><span class="sxs-lookup"><span data-stu-id="5b437-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="5b437-181">**Verðlisti** er nauðsynlegur til að búa til pantanir í Sales.</span><span class="sxs-lookup"><span data-stu-id="5b437-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="5b437-182">Uppfæra **ValueMap** in **CDS** > **Áfangastaður** fyrir **pricelevelid.name [Price List Name]** í **Verðlisti** sem er notaður í Sales eftir gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="5b437-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="5b437-183">Þú getur annað hvort notað sjálfgefinn **verðlista** fyrir einn gjaldmiðil eða **ValueMap** ef **Verðlisti** er í mörgum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="5b437-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="5b437-184">Sjálfgefið sniðmátsgildi fyrir **pricelevelid.name [Price List Name]** er CRM Service USA (dæmi).</span><span class="sxs-lookup"><span data-stu-id="5b437-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="5b437-185">SalesLine verkefni</span><span class="sxs-lookup"><span data-stu-id="5b437-185">SalesLine task</span></span>

- <span data-ttu-id="5b437-186">Uppfæra vörpun fyrir **CDS Organization ID í uppruna** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="5b437-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="5b437-187">Sjálfgefið sniðmátsgildi fyrir **SalesOrder_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="5b437-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="5b437-188">Sjálfgefið sniðmátsgildi fyrir **Product_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="5b437-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="5b437-189">Gakktu úr skugga um að nauðsynleg vörpun sé til staðar í **Uppruna** > **CDS** fyrir **DeliveryCountryRegionId** í **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="5b437-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="5b437-190">Sniðmátsgildi er **ValueMap** með vörpun á fjölda landa.</span><span class="sxs-lookup"><span data-stu-id="5b437-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="5b437-191">Gakktu úr skugga um að nauðsynlegt **ValueMap** fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar í **Uppruni** > **CDS vörpun**.</span><span class="sxs-lookup"><span data-stu-id="5b437-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="5b437-192">Sniðmátsgildi með **ValueMap** er skilgreint **SalesUnitSymbol í Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="5b437-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="5b437-193">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="5b437-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="5b437-194">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="5b437-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="5b437-195">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="5b437-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5b437-196">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="5b437-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="5b437-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="5b437-197">OrderHeader</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="5b437-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="5b437-200">OrderLine</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="5b437-203">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="5b437-203">Related topics</span></span>

[<span data-ttu-id="5b437-204">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="5b437-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="5b437-205">Samstilla lykla úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="5b437-206">Samstilla tengiliði úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="5b437-207">Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="5b437-208">Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b437-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


