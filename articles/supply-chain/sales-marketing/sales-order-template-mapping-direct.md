---
title: "Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations"
description: "Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölupöntunar beint úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: e311b0becbb243cebdc265eccf3059eb46217dee
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="4d49d-103">Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d49d-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4d49d-104">Þetta efnisatriði ræðir sniðmát og undirliggjandi verk sem eru notuð til að samstilla hausa og línur sölupöntunar beint úr Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition við Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="4d49d-105">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="4d49d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="4d49d-106">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="4d49d-107">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="4d49d-108">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="4d49d-109">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="4d49d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4d49d-110">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="4d49d-110">Templates and tasks</span></span>

<span data-ttu-id="4d49d-111">Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="4d49d-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="4d49d-112">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="4d49d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4d49d-113">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="4d49d-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="4d49d-114">**Heiti sniðmátsins í Gagnaflutningi:** Sölupantanir (Fin og Ops í Sales) - Beint</span><span class="sxs-lookup"><span data-stu-id="4d49d-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="4d49d-115">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="4d49d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="4d49d-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="4d49d-116">OrderHeader</span></span>
    - <span data-ttu-id="4d49d-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="4d49d-117">OrderLine</span></span>

<span data-ttu-id="4d49d-118">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar sölureikningshausa og línum geta átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="4d49d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="4d49d-119">Vörur (Fin og Ops til Sales) - bein</span><span class="sxs-lookup"><span data-stu-id="4d49d-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="4d49d-120">Reikningar (Sales við Fin and Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="4d49d-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="4d49d-121">Tengiliðir við viðskiptavini (Sales við Fin og Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="4d49d-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="4d49d-122">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="4d49d-122">Entity set</span></span>

| <span data-ttu-id="4d49d-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d49d-123">Finance and Operations</span></span>  | <span data-ttu-id="4d49d-124">Sölur</span><span class="sxs-lookup"><span data-stu-id="4d49d-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="4d49d-125">Hausar CDS-sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="4d49d-125">CDS sales order headers</span></span> | <span data-ttu-id="4d49d-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="4d49d-126">SalesOrders</span></span>       |
| <span data-ttu-id="4d49d-127">CDS sölupöntunarlínur</span><span class="sxs-lookup"><span data-stu-id="4d49d-127">CDS sales order lines</span></span>   | <span data-ttu-id="4d49d-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="4d49d-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="4d49d-129">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="4d49d-129">Entity flow</span></span>

<span data-ttu-id="4d49d-130">Sölupantanir eru búnar til í Finance and Operations og samstilltar við Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="4d49d-131">Síur í sniðmáti auðvelda að aðeins viðeigandi sölupantanir séu innifaldar í samstillingu:</span><span class="sxs-lookup"><span data-stu-id="4d49d-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="4d49d-132">Á sölupöntun þarf bæði viðskiptavinurinn sem pantar og sá sem reikningsfært að eiga uppruna sinn í Sales til að vera teknir með í samstillingu.</span><span class="sxs-lookup"><span data-stu-id="4d49d-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="4d49d-133">Í Finance and Operations er reitirnir **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** notaðir til að rekja samstillingu í gagnaeiningum.</span><span class="sxs-lookup"><span data-stu-id="4d49d-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="4d49d-134">Sölupöntun í Finance and Operations verður að vera staðfest.</span><span class="sxs-lookup"><span data-stu-id="4d49d-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="4d49d-135">Aðeins staðfestar sölupantanir eða sölupantanir með hærri vinnslustöðu, til dæmis, **Sent** eða **Reikningsfært**, eru samstilltar við Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="4d49d-136">Eftir að sölupöntun er búin til eða henni breytt verður að keyra runuvinnsluna **Reikna heildarsölu** í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="4d49d-137">Aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="4d49d-138">Eins og er er skattur tengdur gjöldum á sölupöntunarhaus er ekki tekinn með í samstillingu úr Finance and Operations í Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="4d49d-139">Sales styður ekki skattupplýsingar á hausstiginu.</span><span class="sxs-lookup"><span data-stu-id="4d49d-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="4d49d-140">Hinsvegar er skattur sem tengist gjöldum á línustigi er innifalinn í samstillingu.</span><span class="sxs-lookup"><span data-stu-id="4d49d-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4d49d-141">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="4d49d-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4d49d-142">Nýjum reitum hefur verið bætt við eininguna **Pöntun** og birtist á síðunni:</span><span class="sxs-lookup"><span data-stu-id="4d49d-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="4d49d-143">**Er viðhaldið utanfrá** - Stillið á **Já** þegar pöntunin er úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="4d49d-144">**Vinnslustaða** - Þessi reitur sýnir vinnslustöðu pantanar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="4d49d-145">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="4d49d-145">The following values are available:</span></span>

    - <span data-ttu-id="4d49d-146">Í gangi</span><span class="sxs-lookup"><span data-stu-id="4d49d-146">Active</span></span>
    - <span data-ttu-id="4d49d-147">Staðfest</span><span class="sxs-lookup"><span data-stu-id="4d49d-147">Confirmed</span></span>
    - <span data-ttu-id="4d49d-148">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="4d49d-148">Packing Slip</span></span>
    - <span data-ttu-id="4d49d-149">Reikningsfært</span><span class="sxs-lookup"><span data-stu-id="4d49d-149">Invoiced</span></span>
    - <span data-ttu-id="4d49d-150">Tekið til</span><span class="sxs-lookup"><span data-stu-id="4d49d-150">Picked</span></span>
    - <span data-ttu-id="4d49d-151">Tínt að hluta</span><span class="sxs-lookup"><span data-stu-id="4d49d-151">Partially Picked</span></span>
    - <span data-ttu-id="4d49d-152">Tekið til að hluta</span><span class="sxs-lookup"><span data-stu-id="4d49d-152">Partially Packed</span></span>
    - <span data-ttu-id="4d49d-153">Sent</span><span class="sxs-lookup"><span data-stu-id="4d49d-153">Shipped</span></span>
    - <span data-ttu-id="4d49d-154">Afhent að hluta</span><span class="sxs-lookup"><span data-stu-id="4d49d-154">Partially Shipped</span></span>
    - <span data-ttu-id="4d49d-155">Reikningsfært að hluta</span><span class="sxs-lookup"><span data-stu-id="4d49d-155">Partially Invoiced</span></span>
    - <span data-ttu-id="4d49d-156">Afturkallað</span><span class="sxs-lookup"><span data-stu-id="4d49d-156">Cancelled</span></span>

<span data-ttu-id="4d49d-157">Stillingin **Er aðens með utanaðkomandi vörur** er notuð í öðrum sviðsmyndum sölupantana (til dæmis samstillingu úr Sales í Finance and Operation) til að halda utan um það hvort sölupöntun sé eingöngu með Vörur sem viðhaldið er utanfrá.</span><span class="sxs-lookup"><span data-stu-id="4d49d-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="4d49d-158">Ef sölupöntun inniheldur aðeins utanaðkomandi vörur er vörunum viðhaldið í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="4d49d-159">Þetta tryggir að þú reynir ekki að virkja og samstilla sölupöntunarlínur með vörum sem eru óþekktar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="4d49d-160">**Stofna reikning**, **Hætta við pöntun**, **Endurreikna**, **Sækja vörur** og **Leita að aðsetri** hnapparnir á síðunni **Sölupöntun** síðan er falin fyrir pantanir sem er viðhaldið að utan, þar sem reikningar verða stofnaðir í Finance and Operations og samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="4d49d-161">Ekki er hægt að breyta pöntunarsíðunni vegna þess að sölupantanir verða samstilltar úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="4d49d-162">Staða sölupöntunar verður áfram **Virk** til að tryggja að gjöld úr Finance and Operations geti flætt í sölupöntun í Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="4d49d-163">Til að stjórna þessu er sjálfgefið **Statecode \[Status\]** stillt á **Virkt** í gagnasamþættingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="4d49d-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4d49d-164">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="4d49d-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="4d49d-165">Áður en sölupantanir eru samstilltar er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.</span><span class="sxs-lookup"><span data-stu-id="4d49d-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="4d49d-166">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="4d49d-166">Setup in Sales</span></span>

- <span data-ttu-id="4d49d-167">Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á.</span><span class="sxs-lookup"><span data-stu-id="4d49d-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="4d49d-168">Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki.</span><span class="sxs-lookup"><span data-stu-id="4d49d-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="4d49d-169">Ef teymi hefur ekki stjórnandaaðgang, þegar þú keyrir verkefnið úr Gagnasamþáttara færðu villuskilaboð sem segja að aðalteymi vantar.</span><span class="sxs-lookup"><span data-stu-id="4d49d-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="4d49d-170">Undir **Stillingar** > **Öryggi** > **Teymi**, velurðu viðkomandi teymi, smellir á **Stjórna hlutverkum** og velur hlutverk með viðkomandi heimildum, t.d. **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="4d49d-171">Farið í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:</span><span class="sxs-lookup"><span data-stu-id="4d49d-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="4d49d-172">**Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="4d49d-173">**Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="4d49d-174">Uppsetning Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d49d-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="4d49d-175">Stilltu **Sala og markaðssetning** > **Reglubundin verkefni** > **Reikna heildarsölu** til að keyra sem runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="4d49d-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="4d49d-176">Stilltu **Reikna út samtölu sölupantana** valkostinn á **Já**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="4d49d-177">Þetta skref er mikilvægt þar sem aðeins sölurekningar þar sem sölutölur eru reiknaðar verður samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="4d49d-178">Tíðni runuvinnslunnar ætti að vera í samræmi við tíðni samstillingu sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="4d49d-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="4d49d-179">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="4d49d-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="4d49d-180">SalesHeader verkefni</span><span class="sxs-lookup"><span data-stu-id="4d49d-180">SalesHeader task</span></span>

- <span data-ttu-id="4d49d-181">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **InvoiceCountryRegionId** to **BillingAddress\_land** og fyrir **DeliveryCountryRegionId** í **DeliveryAddress\_land**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="4d49d-182">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.</span><span class="sxs-lookup"><span data-stu-id="4d49d-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="4d49d-183">Verðlisti er nauðsynlegur til að búa til pantanir í Sales.</span><span class="sxs-lookup"><span data-stu-id="4d49d-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="4d49d-184">Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="4d49d-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="4d49d-185">Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="4d49d-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="4d49d-186">Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="4d49d-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="4d49d-187">Sjálfgefið sniðmátsgildi fyrir **pricelevelid.name \[Heiti verðlista\]** er **CRM Service USA (dæmi)**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="4d49d-188">SalesLine verkefni</span><span class="sxs-lookup"><span data-stu-id="4d49d-188">SalesLine task</span></span>

- <span data-ttu-id="4d49d-189">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **DeliveryCountryRegionId** to **DeliveryAddress\_land**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="4d49d-190">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.</span><span class="sxs-lookup"><span data-stu-id="4d49d-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="4d49d-191">Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Finance and Operations sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="4d49d-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="4d49d-192">Sniðmátsgildi með gildisvörpun er skiglreint fyrir **SalesUnitSymbol** í **Magn\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="4d49d-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4d49d-193">Template mapping in Data integration</span><span class="sxs-lookup"><span data-stu-id="4d49d-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="4d49d-194">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="4d49d-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="4d49d-195">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="4d49d-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="4d49d-196">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="4d49d-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="4d49d-197">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4d49d-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="4d49d-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="4d49d-198">OrderHeader</span></span>

![Sniðmátsvörpun í Gagnasamþáttara](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="4d49d-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="4d49d-200">OrderLine</span></span>

![Sniðmátsvörpun í Gagnasamþáttara](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="4d49d-202">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="4d49d-202">Related topics</span></span>

[<span data-ttu-id="4d49d-203">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="4d49d-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="4d49d-204">Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d49d-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="4d49d-205">Samstilla vörur beint úr Finance and Operations við vörur í Sales</span><span class="sxs-lookup"><span data-stu-id="4d49d-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="4d49d-206">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d49d-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="4d49d-207">Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4d49d-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




