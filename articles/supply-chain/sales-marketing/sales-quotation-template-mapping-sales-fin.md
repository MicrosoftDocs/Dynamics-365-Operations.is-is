---
title: Samstilla hausa og línur sölutilboðs beint úr Sales við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboðs beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: 0894f4728d3f1df21db130cd9e87d9881726e7fa
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743372"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="f1c07-103">Samstilla hausa og línur sölutilboðs beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f1c07-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1c07-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboðs beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f1c07-105">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="f1c07-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="f1c07-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="f1c07-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="f1c07-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="f1c07-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="f1c07-108">Prospect to cash sniðmát sem eru í boði með eiginleika gagnasamþættingar leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantanir og sölureikninga milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="f1c07-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="f1c07-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="f1c07-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="f1c07-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="f1c07-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="f1c07-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="f1c07-111">Template and tasks</span></span>

<span data-ttu-id="f1c07-112">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur beint úr Sales í Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="f1c07-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="f1c07-113">**Heiti sniðmátsins í gagnaflutningi:** Sölutilboð (Sales í Fin and Ops) - beint</span><span class="sxs-lookup"><span data-stu-id="f1c07-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="f1c07-114">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="f1c07-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="f1c07-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f1c07-115">QuoteHeader</span></span>
    - <span data-ttu-id="f1c07-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f1c07-116">QuoteLine</span></span>

<span data-ttu-id="f1c07-117">Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="f1c07-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="f1c07-118">Vörur (Fin og Ops til Sales) - bein</span><span class="sxs-lookup"><span data-stu-id="f1c07-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="f1c07-119">Reikningar (Sales við Fin and Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="f1c07-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="f1c07-120">Tengiliðir við viðskiptavini (Sales við Fin og Ops) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="f1c07-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="f1c07-121">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="f1c07-121">Entity set</span></span>

| <span data-ttu-id="f1c07-122">Sölur</span><span class="sxs-lookup"><span data-stu-id="f1c07-122">Sales</span></span>        | <span data-ttu-id="f1c07-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f1c07-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="f1c07-124">Tilvitnanir</span><span class="sxs-lookup"><span data-stu-id="f1c07-124">Quotes</span></span>       | <span data-ttu-id="f1c07-125">CDS-sölutilboðshaus</span><span class="sxs-lookup"><span data-stu-id="f1c07-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="f1c07-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="f1c07-126">QuoteDetails</span></span> | <span data-ttu-id="f1c07-127">CDS-sölutilboðslínur</span><span class="sxs-lookup"><span data-stu-id="f1c07-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="f1c07-128">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="f1c07-128">Entity flow</span></span>

<span data-ttu-id="f1c07-129">Sölutilboð eru stofnuð í Sales og samstillt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="f1c07-130">Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="f1c07-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="f1c07-131">Öllum tilboðsvörum á sölutilboðinu eru viðhaldið ytra.</span><span class="sxs-lookup"><span data-stu-id="f1c07-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="f1c07-132">Eftir að þú smellir á **Virkja tilboð** er sölutilboðið virk.</span><span class="sxs-lookup"><span data-stu-id="f1c07-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f1c07-133">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="f1c07-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f1c07-134">**Er aðens með utanaðkomandi vörur** reitnum hefur verið bætt við **Tilboð** til að fylgjast stöðugt með því hvort sölutilboð samanstanda aðeins af utanaðkomandi vörum.</span><span class="sxs-lookup"><span data-stu-id="f1c07-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="f1c07-135">Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="f1c07-136">Þetta tryggir að þú reynir ekki að virkja og samstilla sölutilboðslínur með vörum sem eru óþekktar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="f1c07-137">Allar tilboðsvörur á sölutilboðinu eru uppfærðar með **Er aðeins með utanaðkomandi vörur** upplýsingar í sölutilboðshausnum.</span><span class="sxs-lookup"><span data-stu-id="f1c07-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="f1c07-138">Þessar upplýsingar finnast í **Tilboð er aðeins með utanaðkomandi vörur** reitnum á einingunni **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="f1c07-139">Hægt er að bæta við afslætti við tilboðsvöruna og hann verður samstilltur við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="f1c07-140">Reitirnir **Afsláttur**, **Gjöld** og **Skattur** á hausnum er stjórnað af uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="f1c07-141">Eins og er, styður þessi uppsetning ekki samþættingarvörpun.</span><span class="sxs-lookup"><span data-stu-id="f1c07-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="f1c07-142">Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **skattur** viðhaldið í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="f1c07-143">I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="f1c07-144">Reitir með lesaðgangi í sölutilboðshaus: **Afsláttur %**, **Afsláttur** og **Flutningsupphæð**</span><span class="sxs-lookup"><span data-stu-id="f1c07-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="f1c07-145">Reitir aðeins með lesaðgangi á tilboðsvörum: **Skattur**</span><span class="sxs-lookup"><span data-stu-id="f1c07-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f1c07-146">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="f1c07-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="f1c07-147">Áður en sölutilboð eru samstillt er mikilvægt að eftirfarandi stillingar séu uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="f1c07-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="f1c07-148">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="f1c07-148">Setup in Sales</span></span>

- <span data-ttu-id="f1c07-149">Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á.</span><span class="sxs-lookup"><span data-stu-id="f1c07-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="f1c07-150">Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki.</span><span class="sxs-lookup"><span data-stu-id="f1c07-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="f1c07-151">Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.</span><span class="sxs-lookup"><span data-stu-id="f1c07-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="f1c07-152">Til að setja upp heimildir fyrir teymið ferðu í **Stillingar** &gt; **Öryggi** &gt; **Teymi** og velur teymið.</span><span class="sxs-lookup"><span data-stu-id="f1c07-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="f1c07-153">Veldu **Stjórna hlutverkum** og svo hltuverk með viðkomandi heimildir, svo sem **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="f1c07-154">Farið í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sala** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:</span><span class="sxs-lookup"><span data-stu-id="f1c07-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="f1c07-155">**Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="f1c07-156">**Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="f1c07-157">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="f1c07-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="f1c07-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f1c07-158">QuoteHeader</span></span>

- <span data-ttu-id="f1c07-159">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="f1c07-160">Í gildisvörpuninni er hægt að skilgreina sjálfgefið gildi sem er notað ef gildið er autt.</span><span class="sxs-lookup"><span data-stu-id="f1c07-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="f1c07-161">Slepptu aðeins vinstri hliðinni og settu hægri hliðina í viðkomandi land eða svæði.</span><span class="sxs-lookup"><span data-stu-id="f1c07-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="f1c07-162">Á þennan hátt þarf ekki að slá inn landið eða svæði fyrir innlendar pantanir.</span><span class="sxs-lookup"><span data-stu-id="f1c07-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="f1c07-163">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð og þegar autt gildi jafngildir gildini **US**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="f1c07-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f1c07-164">QuoteLine</span></span>

- <span data-ttu-id="f1c07-165">Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** sé til staðar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="f1c07-166">Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.</span><span class="sxs-lookup"><span data-stu-id="f1c07-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="f1c07-167">Sniðmátsgildi með gildisvörpun er skilgreint fyrir **oumid.name** í **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="f1c07-168">Valfrjálst: Hægt er að bæta við eftirfarandi vörpun til að tryggja að sölutilboðslínur séu fluttar inn í Finance and Operations ef engar sjálfgefnar upplýsingar eru frá viðskiptavinum eða vörunni:</span><span class="sxs-lookup"><span data-stu-id="f1c07-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="f1c07-169">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f1c07-170">Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="f1c07-171">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f1c07-172">Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="f1c07-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f1c07-173">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="f1c07-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="f1c07-174">Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f1c07-175">Eins og er, styður þessi uppsetning ekki samþættingarvörpun.</span><span class="sxs-lookup"><span data-stu-id="f1c07-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="f1c07-176">Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f1c07-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="f1c07-177">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="f1c07-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="f1c07-178">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="f1c07-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f1c07-179">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="f1c07-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="f1c07-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f1c07-180">QuoteHeader</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="f1c07-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f1c07-182">QuoteLine</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="f1c07-184">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="f1c07-184">Related topics</span></span>

[<span data-ttu-id="f1c07-185">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="f1c07-185">Prospect to cash</span></span>](prospect-to-cash.md)

