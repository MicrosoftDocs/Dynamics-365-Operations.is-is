---
title: Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla einingar tengiliðar (tengiliða) og tengiliðar (viðskiptavina) úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994046"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="def86-103">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="def86-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="def86-104">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Microsoft Dataverse fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="def86-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="def86-105">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla töflur tengiliðs (tengiliða) og tengiliðar (viðskiptavina) beint úr Dynamics 365 Sales við Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="def86-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="def86-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="def86-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="def86-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="def86-108">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="def86-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="def86-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="def86-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="def86-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="def86-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="def86-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="def86-111">Templates and tasks</span></span>

<span data-ttu-id="def86-112">Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="def86-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="def86-113">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="def86-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="def86-114">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla tengiliðatöflur (Tengiliðir) í Sales í tengiliðatölfur (Viðskiptavinir) í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="def86-115">**Heiti sniðmátanna í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="def86-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="def86-116">Tengiliðir (Sales til Supply Chain Management) - Bein</span><span class="sxs-lookup"><span data-stu-id="def86-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="def86-117">Tengiliðir við viðskiptavin (Sales til Supply Chain Management) - Beint</span><span class="sxs-lookup"><span data-stu-id="def86-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="def86-118">**Heiti verksins í gagnasamþættingarverki**</span><span class="sxs-lookup"><span data-stu-id="def86-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="def86-119">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="def86-119">Contacts</span></span>
    - <span data-ttu-id="def86-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="def86-120">ContactToCustomer</span></span>

<span data-ttu-id="def86-121">Eftirfarandi samstilliningarverkefni er nauðsynlegt til að samstiling Tengiliðar geti farið fram: Lyklar (Sales við Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="def86-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="def86-122">Einingastamstæður</span><span class="sxs-lookup"><span data-stu-id="def86-122">Entity sets</span></span>

| <span data-ttu-id="def86-123">Sala</span><span class="sxs-lookup"><span data-stu-id="def86-123">Sales</span></span>    | <span data-ttu-id="def86-124">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="def86-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="def86-125">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="def86-125">Contacts</span></span> | <span data-ttu-id="def86-126">Dataverse-tengiliðir</span><span class="sxs-lookup"><span data-stu-id="def86-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="def86-127">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="def86-127">Contacts</span></span> | <span data-ttu-id="def86-128">Viðskiptavinir V2</span><span class="sxs-lookup"><span data-stu-id="def86-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="def86-129">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="def86-129">Entity flow</span></span>

<span data-ttu-id="def86-130">Tengiliðum er stjórnað í Sales og þeir samstilltir við Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="def86-131">Tengiliður í Sales getur orðið tengiliður eða viðskiptavinur í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="def86-132">Til að ákvarða hvort tengiliður í Sales eigi að samstilla við Supply Chain Management sem tengilið eða viðskiptamann, lítur kerfið á eftirfarandi eiginleika tengiliðarins í Sales:</span><span class="sxs-lookup"><span data-stu-id="def86-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="def86-133">**Samstilling við viðskiptavin í Supply Chain Management:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Já**</span><span class="sxs-lookup"><span data-stu-id="def86-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="def86-134">**Samstilling við tengilið í Supply Chain Management:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Nei** og **Fyrirtæki** (yfirreikningur/tengiliður) vísar í reikning (ekki tengilið)</span><span class="sxs-lookup"><span data-stu-id="def86-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="def86-135">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="def86-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="def86-136">Nýjum **Er virkur viðskiptavinur** dálki hefur verið bætt við tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="def86-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="def86-137">Dálkurinn er notaður til að aðgreina tengiliði sem hafa sölustarfsemi og tengiliði sem hafa ekki sölustarfsemi.</span><span class="sxs-lookup"><span data-stu-id="def86-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="def86-138">**Er virkur viðskiptavinur** er stillt á **Já** aðeins fyrir tengiliði sem hafa tengd tilboð, pantanir eða reikninga.</span><span class="sxs-lookup"><span data-stu-id="def86-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="def86-139">Aðeins þeir tengiliðir eru samstilltir við Supply Chain Management sem viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="def86-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="def86-140">Nýjum **IsCompanyAnAccount** dálki hefur verið bætt við tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="def86-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="def86-141">Dálkurinn gefur til kynna hvort tengiliður er tengdur við fyrirtæki (yfirreikning/tengilið) af gerðinni **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="def86-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="def86-142">Þessar upplýsingar eru notaðar til að auðkenna tengiliði sem ætti að samstilla við Supply Chain Management sem tengiliði.</span><span class="sxs-lookup"><span data-stu-id="def86-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="def86-143">Nýjum **Númer tengiliðs** dálki hefur verið bætt við tengiliðinn til að hjálpa við að tryggja einkvæman lykil fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="def86-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="def86-144">Þegar nýr tengiliður er búinn til er sjálfkrafa myndað **Númer tengiliðs** gildi með því að nota númeraröð.</span><span class="sxs-lookup"><span data-stu-id="def86-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="def86-145">Gildið samanstendur af **CON**, því næst hækkandi talnaröð og svo sex stafa viðskeyti.</span><span class="sxs-lookup"><span data-stu-id="def86-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="def86-146">Hér er dæmi: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="def86-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="def86-147">Þegar samþættingarlausn fyrir Sales er beitt stillir uppfærsluforskrift dálkinn **Númer tengiliðs** fyrir fyrirliggjandi tengiliði með því að nota númeraröðina sem áður var getið.</span><span class="sxs-lookup"><span data-stu-id="def86-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="def86-148">Uppfærsluforskriftin stillir einnig **Er virkur viðskiptavinur** dálkinn á **Já** fyrir alla tengiliði með söluaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="def86-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="def86-149">Í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="def86-149">In Supply Chain Management</span></span>

<span data-ttu-id="def86-150">Tengiliðir eru merktir með eiginleikanum **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="def86-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="def86-151">Þessi eign gefur til kynna að unnið sé með tilteknum tengilið utan frá.</span><span class="sxs-lookup"><span data-stu-id="def86-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="def86-152">Í því tilfelli er utanaðkomandi tengiliðum viðhaldið í Sales.</span><span class="sxs-lookup"><span data-stu-id="def86-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="def86-153">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="def86-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="def86-154">Tengiliður í viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="def86-154">Contact to customer</span></span>

- <span data-ttu-id="def86-155">**Viðskiptavinahópur** er krafist í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="def86-156">Til að forðast samstillingarvillur er hægt að tilgreina sjálfgildi í vörpun.</span><span class="sxs-lookup"><span data-stu-id="def86-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="def86-157">Sjálfgefið gildi er síðan notað ef dálkurinn er hafður auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="def86-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="def86-158">Sjálfgefið sniðmátsgildi er **10**.</span><span class="sxs-lookup"><span data-stu-id="def86-158">The default template value is **10**.</span></span>

- <span data-ttu-id="def86-159">Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="def86-160">Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.</span><span class="sxs-lookup"><span data-stu-id="def86-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="def86-161">**SiteId** – Einnig er hægt að tilgreina sjálfgefið svæði vara í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="def86-162">Svæði er nauðsynlegt til að búa til tilboð og sölupöntunum í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="def86-163">Sniðmátsgildi fyrir **SiteId** er ekki skilgreint.</span><span class="sxs-lookup"><span data-stu-id="def86-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="def86-164">**WarehouseId** – Einnig er hægt að tilgreina sjálfgefið vöruhús vara í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="def86-165">Vöruhús er nauðsynlegt til að búa til tilboð og sölupöntunum í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="def86-166">Sniðmátsgildi fyrir **WarehouseId** er ekki skilgreint.</span><span class="sxs-lookup"><span data-stu-id="def86-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="def86-167">**LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="def86-168">Sjálfgefið sniðmátsgildi er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="def86-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="def86-169">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="def86-169">Template mapping in Data integration</span></span>

<span data-ttu-id="def86-170">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="def86-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="def86-171">Vörpunin sýnir hvaða dálkupplýsingar verða samstilltar úr Sales í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="def86-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="def86-172">Tengiliður í tengilið</span><span class="sxs-lookup"><span data-stu-id="def86-172">Contact to contact</span></span>

![Sniðmátsvörpun í Gagnasamþáttara](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="def86-174">Tengiliður í viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="def86-174">Contact to customer</span></span>

![Sniðmátsvörpun í Gagnasamþáttara](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="def86-176">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="def86-176">Related topics</span></span>

[<span data-ttu-id="def86-177">Viðfang til sjóðstreymis</span><span class="sxs-lookup"><span data-stu-id="def86-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="def86-178">Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="def86-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="def86-179">Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales</span><span class="sxs-lookup"><span data-stu-id="def86-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="def86-180">Samstilling sölupantana beint á milli Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="def86-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="def86-181">Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales</span><span class="sxs-lookup"><span data-stu-id="def86-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


