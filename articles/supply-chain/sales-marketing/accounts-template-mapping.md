---
title: "Samstilla reikninga frá Sales til viðskiptavina í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla lykla úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu."
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
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="768ab-103">Samstilla reikninga frá Sales til viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="768ab-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="768ab-104">Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="768ab-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="768ab-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla lykla úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="768ab-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="768ab-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="768ab-106">Template and task</span></span>

<span data-ttu-id="768ab-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla lykla úr Sales í Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="768ab-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="768ab-108">**Nafn sniðmáts:** Lyklar (Sales í Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="768ab-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="768ab-109">**Heiti á verkefninu í verkinu:** - Lyklar - Lykill - Viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="768ab-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="768ab-110">Samstilling verkefna nauðsynleg fyrir samstillingu Lykils/Viðskiptavinar: Engin</span><span class="sxs-lookup"><span data-stu-id="768ab-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="768ab-111">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="768ab-111">Entity set</span></span>

| <span data-ttu-id="768ab-112">Sala</span><span class="sxs-lookup"><span data-stu-id="768ab-112">Sales</span></span>    | <span data-ttu-id="768ab-113">CDS</span><span class="sxs-lookup"><span data-stu-id="768ab-113">CDS</span></span>     | <span data-ttu-id="768ab-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="768ab-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="768ab-115">Lyklar</span><span class="sxs-lookup"><span data-stu-id="768ab-115">Accounts</span></span> | <span data-ttu-id="768ab-116">Lykill</span><span class="sxs-lookup"><span data-stu-id="768ab-116">Account</span></span> | <span data-ttu-id="768ab-117">Viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="768ab-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="768ab-118">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="768ab-118">Entity flow</span></span>

<span data-ttu-id="768ab-119">Lyklum er stýrt í Sales og þeir eru samstilltir í Finance and Operations sem Viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="768ab-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="768ab-120">Eiginleikinn **Unnið með utan frá** á þessum Viðskiptavinum er stilltur á **Já** til að rekja Viðskiptavini sem koma frá Sales.</span><span class="sxs-lookup"><span data-stu-id="768ab-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="768ab-121">Við reikningsfærslu eru þessar upplýsingar notaðar til að sía reikninga sem eru samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="768ab-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="768ab-122">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="768ab-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="768ab-123">Reiturinn **Lykilnúmer** er tiltækur á síðunni **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="768ab-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="768ab-124">Hann hefur verið gerður einkvæmur raunlykill til að styðja samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="768ab-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="768ab-125">Raunlykilseiginleikinn í Tengslastjórnunarlausninni (CRM) gæti haft áhrif á viðskiptavini sem nota þegar reitinn **Lykilnúmer** en nota ekki einkvæm **Lykilnúmersgildi** fyrir hvern lykil.</span><span class="sxs-lookup"><span data-stu-id="768ab-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="768ab-126">Eins og er styður samþættingarlausin ekki slík tilfelli.</span><span class="sxs-lookup"><span data-stu-id="768ab-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="768ab-127">Þegar nýr lykill er stofnaður, og ef **Lykilnúmersgildi** er ekki þegar til, er það sjálfkrafa búið til með talnaröð.</span><span class="sxs-lookup"><span data-stu-id="768ab-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="768ab-128">Gildið samanstendur af **ACC**, því næst hækkandi talnaröð og svo sex stafa viðskeyti.</span><span class="sxs-lookup"><span data-stu-id="768ab-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="768ab-129">Hér er dæmi: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="768ab-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="768ab-130">Þegar samþættingarlausnin fyrir Sales er notuð, stillir uppfærsluforskrift reitinn **Lykilnúmer** fyrir lykla sem þegar eru til í Sales.</span><span class="sxs-lookup"><span data-stu-id="768ab-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="768ab-131">Ef það eru engin **Lykilnúmersgildi** er talnaröðin sem var lýst hér á undan notuð.</span><span class="sxs-lookup"><span data-stu-id="768ab-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="768ab-132">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="768ab-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="768ab-133">Vörpun **CustomerGroupId** úr **CDS &gt; áfangastaðnum** verður að uppfæra í tækt gildi í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="768ab-134">Hægt er að tilgreina sjálfgefið gildi eða setja upp gildi með því að nota gildisvörpun.</span><span class="sxs-lookup"><span data-stu-id="768ab-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="768ab-135">Sjálfgefið sniðmátsgildi er **10**.</span><span class="sxs-lookup"><span data-stu-id="768ab-135">The default template value is **10**.</span></span>
- <span data-ttu-id="768ab-136">**Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="768ab-137">Til að forðast samstillingarvillur er hægt að tilgreina sjálfgildi í vörpun úr **CDS &gt; áfangastað**.</span><span class="sxs-lookup"><span data-stu-id="768ab-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="768ab-138">Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="768ab-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="768ab-139">Sjálfgefið sniðmátsgildi fyrir **AddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="768ab-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="768ab-140">Sjálfgefið sniðmátsgildi fyrir **DeliveryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="768ab-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="768ab-141">Með því að bæta eftirfarandi vörpunum úr **CDS &gt; Ákvörðunarstað** geturðu dregið úr fjölda handvirkra uppfærslna sem nauðsynlegar eru í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="768ab-142">Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.</span><span class="sxs-lookup"><span data-stu-id="768ab-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="768ab-143">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="768ab-144">Sjálfgefið svæði er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="768ab-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="768ab-145">Sjálfgefið sniðmátsgildi fyrir **SiteId** er **1**.</span><span class="sxs-lookup"><span data-stu-id="768ab-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="768ab-146">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="768ab-147">Sjálfgefið vöruhús er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="768ab-148">Sjálfgefið sniðmátsgildi fyrir **WarehouseId** er **13**.</span><span class="sxs-lookup"><span data-stu-id="768ab-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="768ab-149">**LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="768ab-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="768ab-150">Sjálfgefið er að tungumálið í pöntunarhausnum frá viðskiptavininum sé notað.</span><span class="sxs-lookup"><span data-stu-id="768ab-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="768ab-151">Sjálfgefið sniðmátsgildi fyrir **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="768ab-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="768ab-152">Uppfærðu CDS-fyrirtækjaauðkenni (**Organization_OrganizationId**) í **Uppruni &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="768ab-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="768ab-153">Sjálfgefið sniðmátsgildi er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="768ab-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="768ab-154">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="768ab-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="768ab-155">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="768ab-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="768ab-156">Til að varpa þessum reitum verður að setja upp á gildisvörpun.</span><span class="sxs-lookup"><span data-stu-id="768ab-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="768ab-157">Gildisvarpanir eiga sérstaklega við um gögnin í fyrirtækjunum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="768ab-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="768ab-158">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="768ab-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/accounts-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun fyrir Lykla í gagnasamþáttara](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="768ab-161">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="768ab-161">Related topics</span></span>

[<span data-ttu-id="768ab-162">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="768ab-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="768ab-163">Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="768ab-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="768ab-164">Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="768ab-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="768ab-165">Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="768ab-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="768ab-166">Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="768ab-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




