---
title: Samstilla hausa og línur sölutilboðs beint úr Sales í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboða beint úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 848464cbc62623502b9b87b9b41dcc17150e85ba
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839006"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="9cc1b-103">Samstilla hausa og línur sölutilboðs beint úr Sales í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9cc1b-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9cc1b-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla hausa og línur sölutilboða beint úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="9cc1b-105">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Microsoft Dataverse fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="9cc1b-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="9cc1b-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="9cc1b-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="9cc1b-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="9cc1b-108">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="9cc1b-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="9cc1b-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="9cc1b-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="9cc1b-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="9cc1b-111">Template and tasks</span></span>

<span data-ttu-id="9cc1b-112">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur beint úr Sales í Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="9cc1b-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="9cc1b-113">**Heiti sniðmátsins í Gagnaflutningi:** Sölutilboð (Sales til Supply Chain Management) - beint</span><span class="sxs-lookup"><span data-stu-id="9cc1b-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="9cc1b-114">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="9cc1b-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="9cc1b-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9cc1b-115">QuoteHeader</span></span>
    - <span data-ttu-id="9cc1b-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9cc1b-116">QuoteLine</span></span>

<span data-ttu-id="9cc1b-117">Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="9cc1b-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="9cc1b-118">Afurðir (Supply Chain Management itl Sales) - Beint</span><span class="sxs-lookup"><span data-stu-id="9cc1b-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="9cc1b-119">Lyklar (Sales til Supply Chain Management) - Bein (ef notað)</span><span class="sxs-lookup"><span data-stu-id="9cc1b-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="9cc1b-120">Tengiliðir við viðskiptavini (Sales til Supply Chain Management) - Beint (ef notað)</span><span class="sxs-lookup"><span data-stu-id="9cc1b-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="9cc1b-121">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="9cc1b-121">Entity set</span></span>

| <span data-ttu-id="9cc1b-122">Sala</span><span class="sxs-lookup"><span data-stu-id="9cc1b-122">Sales</span></span>        | <span data-ttu-id="9cc1b-123">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="9cc1b-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="9cc1b-124">Tilvitnanir</span><span class="sxs-lookup"><span data-stu-id="9cc1b-124">Quotes</span></span>       | <span data-ttu-id="9cc1b-125">Dataverse sölutilboðshaus</span><span class="sxs-lookup"><span data-stu-id="9cc1b-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="9cc1b-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="9cc1b-126">QuoteDetails</span></span> | <span data-ttu-id="9cc1b-127">Dataverse sölutilboðslínur</span><span class="sxs-lookup"><span data-stu-id="9cc1b-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="9cc1b-128">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="9cc1b-128">Entity flow</span></span>

<span data-ttu-id="9cc1b-129">Sölutilboð eru stofnuð í Sales og samstillt við Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="9cc1b-130">Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="9cc1b-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="9cc1b-131">Öllum tilboðsvörum á sölutilboðinu eru viðhaldið ytra.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="9cc1b-132">Eftir að þú smellir á **Virkja tilboð** er sölutilboðið virk.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9cc1b-133">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="9cc1b-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9cc1b-134">**Er aðens með utanaðkomandi vörur** reitnum hefur verið bætt við **Tilboð** til að fylgjast stöðugt með því hvort sölutilboð samanstanda aðeins af utanaðkomandi vörum.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="9cc1b-135">Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="9cc1b-136">Þetta tryggir að þú reynir ekki að virkja og samstilla sölutilboðslínur með vörum sem eru óþekktar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="9cc1b-137">Allar tilboðsvörur á sölutilboðinu eru uppfærðar með **Er aðeins með utanaðkomandi vörur** upplýsingar í sölutilboðshausnum.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="9cc1b-138">Þessar upplýsingar finnast í **Tilboð er aðeins með utanaðkomandi vörur** reitnum á einingunni **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="9cc1b-139">Hægt er að bæta við afslætti við tilboðsvöruna og hann verður samstilltur við Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="9cc1b-140">Reitirnir **Afsláttur**, **Gjöld** og **Skattur** á hausnum er stjórnað af uppsetningu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="9cc1b-141">Eins og er, styður þessi uppsetning ekki samþættingarvörpun.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="9cc1b-142">Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **skattur** viðhaldið í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="9cc1b-143">I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="9cc1b-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="9cc1b-144">Reitir með lesaðgangi í sölutilboðshaus: **Afsláttur %**, **Afsláttur** og **Flutningsupphæð**</span><span class="sxs-lookup"><span data-stu-id="9cc1b-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="9cc1b-145">Reitir aðeins með lesaðgangi á tilboðsvörum: **Skattur**</span><span class="sxs-lookup"><span data-stu-id="9cc1b-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9cc1b-146">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="9cc1b-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="9cc1b-147">Áður en sölutilboð eru samstillt er mikilvægt að eftirfarandi stillingar séu uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="9cc1b-148">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="9cc1b-148">Setup in Sales</span></span>

- <span data-ttu-id="9cc1b-149">Gakktu úr skugga um að heimildir séu settar upp fyrir teymi sem notandinn úr tengingunni sem stillt er í Sales er úthlutaður á.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="9cc1b-150">Ef þú ert að nota sýnigögn hefur notandinn venjulega stjórnendaaðgang en teymið ekki.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="9cc1b-151">Ef teymið hefur ekki stjórnendaaðgang þegar þú keyri verkefnið úr gagnasamþáttara færðu villuskilaboð sem segir að aðalteymi vantar.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="9cc1b-152">Til að setja upp heimildir fyrir teymið ferðu í **Stillingar** &gt; **Öryggi** &gt; **Teymi** og velur teymið.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="9cc1b-153">Veldu **Stjórna hlutverkum** og svo hltuverk með viðkomandi heimildir, svo sem **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="9cc1b-154">Farið í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sala** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:</span><span class="sxs-lookup"><span data-stu-id="9cc1b-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="9cc1b-155">**Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="9cc1b-156">**Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="9cc1b-157">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="9cc1b-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="9cc1b-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9cc1b-158">QuoteHeader</span></span>

- <span data-ttu-id="9cc1b-159">Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Shipto\_land** í **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="9cc1b-160">Í gildisvörpuninni er hægt að skilgreina sjálfgefið gildi sem er notað ef gildið er autt.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="9cc1b-161">Slepptu aðeins vinstri hliðinni og settu hægri hliðina í viðkomandi land eða svæði.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="9cc1b-162">Á þennan hátt þarf ekki að slá inn landið eða svæði fyrir innlendar pantanir.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="9cc1b-163">Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð og þegar autt gildi jafngildir gildini **US**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="9cc1b-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9cc1b-164">QuoteLine</span></span>

- <span data-ttu-id="9cc1b-165">Gangið úr skugga um að nauðsynleg gildisvörpun sé til staðar fyrir **SalesUnitSymbol** í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="9cc1b-166">Gangið úr skugga um að nauðsynelgar einingar séu skilgreindar í Sales.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="9cc1b-167">Sniðmátsgildi með gildisvörpun er skilgreint fyrir **oumid.name** í **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="9cc1b-168">Valfrjálst: Hægt er að bæta við eftirfarandi vörpun til að tryggja að sölutilboðslínur séu fluttar inn í Supply Chain Management ef engar sjálfgefnar upplýsingar eru frá viðskiptavinum eða vörunni:</span><span class="sxs-lookup"><span data-stu-id="9cc1b-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="9cc1b-169">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="9cc1b-170">Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="9cc1b-171">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="9cc1b-172">Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="9cc1b-173">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="9cc1b-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="9cc1b-174">Reitirnir **Afsláttur**, **Gjöld** og **Skattur** er stjórnað af flókinni uppsetningu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="9cc1b-175">Eins og er, styður þessi uppsetning ekki samþættingarvörpun.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="9cc1b-176">Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="9cc1b-177">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="9cc1b-178">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9cc1b-179">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="9cc1b-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="9cc1b-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9cc1b-180">QuoteHeader</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="9cc1b-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9cc1b-182">QuoteLine</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="9cc1b-184">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="9cc1b-184">Related topics</span></span>

[<span data-ttu-id="9cc1b-185">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="9cc1b-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]