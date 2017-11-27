---
title: "Samstilla hausa og línur sölutilboðs beint úr Sales við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur beint úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 8a75c6dd91020ab3e676e2bb40d5c822731e244f
ms.contentlocale: is-is
ms.lasthandoff: 11/14/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="472be-103">Samstilla hausa og línur sölutilboðs beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="472be-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="472be-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur beint úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="472be-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="472be-105">Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 Data samþættingu](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="472be-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="472be-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="472be-106">Template and tasks</span></span>

<span data-ttu-id="472be-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur beint úr Sales í Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="472be-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="472be-108">**Heiti sniðmátsins í gagnaflutningi:** Sölutilboð (Sales í Fin and Ops) - beint</span><span class="sxs-lookup"><span data-stu-id="472be-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="472be-109">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="472be-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="472be-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="472be-110">QuoteHeader</span></span>
    - <span data-ttu-id="472be-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="472be-111">QuoteLine</span></span>

<span data-ttu-id="472be-112">Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="472be-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="472be-113">Vörur (Fin og Ops til Sales) - bein</span><span class="sxs-lookup"><span data-stu-id="472be-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="472be-114">Reikningar (Sales við Fin and Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="472be-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="472be-115">Tengiliðir við viðskiptavini (Sales við Fin og Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="472be-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="472be-116">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="472be-116">Entity set</span></span>

| <span data-ttu-id="472be-117">Sölur</span><span class="sxs-lookup"><span data-stu-id="472be-117">Sales</span></span>        | <span data-ttu-id="472be-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="472be-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="472be-119">Tilvitnanir</span><span class="sxs-lookup"><span data-stu-id="472be-119">Quotes</span></span>       | <span data-ttu-id="472be-120">CDS-sölutilboðshaus</span><span class="sxs-lookup"><span data-stu-id="472be-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="472be-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="472be-121">QuoteDetails</span></span> | <span data-ttu-id="472be-122">CDS-sölutilboðslínur</span><span class="sxs-lookup"><span data-stu-id="472be-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="472be-123">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="472be-123">Entity flow</span></span>

<span data-ttu-id="472be-124">Sölutilboð eru stofnuð í Sales og samstillt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="472be-125">Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="472be-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="472be-126">Öllum tilboðsvörum á sölutilboðinu eru viðhaldið ytra.</span><span class="sxs-lookup"><span data-stu-id="472be-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="472be-127">Eftir að þú smellir á **Virkja tilboð** er sölutilboðið virk.</span><span class="sxs-lookup"><span data-stu-id="472be-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="472be-128">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="472be-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="472be-129">**Er aðens með utanaðkomandi vörur** reitnum hefur verið bætt við **Tilboð** til að fylgjast stöðugt með því hvort sölutilboð samanstanda aðeins af utanaðkomandi vörum.</span><span class="sxs-lookup"><span data-stu-id="472be-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="472be-130">Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="472be-131">Þetta tryggir að þú reynir ekki að virkja og samstilla sölutilboðslínur með vörum sem eru óþekktar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="472be-132">Allar tilboðsvörur á sölutilboðinu eru uppfærðar með **Er aðeins með utanaðkomandi vörur** upplýsingar í sölutilboðshausnum.</span><span class="sxs-lookup"><span data-stu-id="472be-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="472be-133">Þessar upplýsingar finnast í **Tilboð er aðeins með utanaðkomandi vörur** reitnum á einingunni **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="472be-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="472be-134">Hægt er að bæta við afslætti við tilboðsvöruna og hann verður samstilltur við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="472be-135">Reitirnir **Afsláttur**, **Gjöld** og **Skattur** á hausnum er stjórnað af uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="472be-136">Eins og er, styður þessi uppsetning ekki samþættingarvörpun.</span><span class="sxs-lookup"><span data-stu-id="472be-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="472be-137">Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **skattur** viðhaldið í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="472be-138">I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="472be-139">Reitir með lesaðgangi í sölutilboðshaus: **Afsláttur %**, **Afsláttur** og **Flutningsupphæð**</span><span class="sxs-lookup"><span data-stu-id="472be-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="472be-140">Reitir aðeins með lesaðgangi á tilboðsvörum: **Skattur**</span><span class="sxs-lookup"><span data-stu-id="472be-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="472be-141">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="472be-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="472be-142">Áður en sölutilboð eru samstillt er mikilvægt að eftirfarandi stillingar séu uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="472be-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="472be-143">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="472be-143">Setup in Sales</span></span>

- <span data-ttu-id="472be-144">Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á.</span><span class="sxs-lookup"><span data-stu-id="472be-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="472be-145">Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki.</span><span class="sxs-lookup"><span data-stu-id="472be-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="472be-146">Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.</span><span class="sxs-lookup"><span data-stu-id="472be-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="472be-147">Til að setja upp heimildir fyrir teymið ferðu í **Stillingar** &gt; **Öryggi** &gt; **Teymi** og velur teymið.</span><span class="sxs-lookup"><span data-stu-id="472be-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="472be-148">Veldu **Stjórna hlutverkum** og svo hltuverk með viðkomandi heimildir, svo sem **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="472be-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="472be-149">Farið í **Stillingar**&gt;**Stjórnun**&gt;**Kerfisstillingar**&gt;**Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:</span><span class="sxs-lookup"><span data-stu-id="472be-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="472be-150">**Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="472be-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="472be-151">**Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="472be-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="472be-152">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="472be-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="472be-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="472be-153">QuoteHeader</span></span>

- <span data-ttu-id="472be-154">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="472be-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="472be-155">Í gildisvörpuninni er hægt að skilgreina sjálfgefið gildi sem er notað ef gildið er autt.</span><span class="sxs-lookup"><span data-stu-id="472be-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="472be-156">Slepptu aðeins vinstri hliðinni og settu hægri hliðina í viðkomandi land eða svæði.</span><span class="sxs-lookup"><span data-stu-id="472be-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="472be-157">Á þennan hátt þarf ekki að slá inn landið eða svæði fyrir innlendar pantanir.</span><span class="sxs-lookup"><span data-stu-id="472be-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="472be-158">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð og þegar autt gildi jafngildir gildini **US**.</span><span class="sxs-lookup"><span data-stu-id="472be-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="472be-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="472be-159">QuoteLine</span></span>

- <span data-ttu-id="472be-160">Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** sé til staðar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="472be-161">Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.</span><span class="sxs-lookup"><span data-stu-id="472be-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="472be-162">Sniðmátsgildi með gildisvörpun er skilgreint fyrir **oumid.name** í **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="472be-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="472be-163">Valfrjálst: Hægt er að bæta við eftirfarandi vörpun til að tryggja að sölutilboðslínur séu fluttar inn í Finance and Operations ef engar sjálfgefnar upplýsingar eru frá viðskiptavinum eða vörunni:</span><span class="sxs-lookup"><span data-stu-id="472be-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="472be-164">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="472be-165">Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="472be-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="472be-166">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="472be-167">Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="472be-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="472be-168">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="472be-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="472be-169">Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="472be-170">Eins og er, styður þessi uppsetning ekki samþættingarvörpun.</span><span class="sxs-lookup"><span data-stu-id="472be-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="472be-171">Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="472be-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="472be-172">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="472be-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="472be-173">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="472be-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="472be-174">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="472be-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="472be-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="472be-175">QuoteHeader</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="472be-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="472be-177">QuoteLine</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="472be-179">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="472be-179">Related topics</span></span>

[<span data-ttu-id="472be-180">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="472be-180">Prospect to cash</span></span>](prospect-to-cash.md)


