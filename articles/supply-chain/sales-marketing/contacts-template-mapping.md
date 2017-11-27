---
title: "Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla Tengilið (Tengiliðir) og Tengilið (Viðskiptavinir) úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="09ec5-103">Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="09ec5-104">Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="09ec5-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="09ec5-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla Tengiliðseiningar (Tengiliðir) og Tengilið (Viðskiptavinir) úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="09ec5-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="09ec5-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="09ec5-106">Templates and tasks</span></span>

<span data-ttu-id="09ec5-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla Tengilið (Tengiliðir) í Sales við Tengilið (Viðskiptavinir) í Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="09ec5-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="09ec5-108">**Heiti sniðmátanna:**</span><span class="sxs-lookup"><span data-stu-id="09ec5-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="09ec5-109">Tengiliðir (Sales við Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="09ec5-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="09ec5-110">Tengiliðir við Viðskiptavin (Sales við Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="09ec5-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="09ec5-111">**Heiti verkefnanna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="09ec5-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="09ec5-112">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="09ec5-112">Contacts</span></span>
    - <span data-ttu-id="09ec5-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="09ec5-113">ContactToCustomer</span></span>

<span data-ttu-id="09ec5-114">Eftirfarandi samstilliningarverkefni er nauðsynlegt fyrir samstilingu Tengiliðar: Lyklar (Sales við Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="09ec5-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="09ec5-115">Einingastamstæður</span><span class="sxs-lookup"><span data-stu-id="09ec5-115">Entity sets</span></span>

| <span data-ttu-id="09ec5-116">Sala</span><span class="sxs-lookup"><span data-stu-id="09ec5-116">Sales</span></span>    | <span data-ttu-id="09ec5-117">CDS</span><span class="sxs-lookup"><span data-stu-id="09ec5-117">CDS</span></span>     | <span data-ttu-id="09ec5-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="09ec5-119">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="09ec5-119">Contacts</span></span> | <span data-ttu-id="09ec5-120">Tengiliður</span><span class="sxs-lookup"><span data-stu-id="09ec5-120">Contact</span></span> | <span data-ttu-id="09ec5-121">Tengiliðir fyrir skuldatryggingu</span><span class="sxs-lookup"><span data-stu-id="09ec5-121">CDS Contacts</span></span>           |
| <span data-ttu-id="09ec5-122">Tengiliðir</span><span class="sxs-lookup"><span data-stu-id="09ec5-122">Contacts</span></span> | <span data-ttu-id="09ec5-123">Lykill</span><span class="sxs-lookup"><span data-stu-id="09ec5-123">Account</span></span> | <span data-ttu-id="09ec5-124">Viðskiptavinir V2</span><span class="sxs-lookup"><span data-stu-id="09ec5-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="09ec5-125">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="09ec5-125">Entity flow</span></span>

<span data-ttu-id="09ec5-126">Tengiliðum er stjórnað í Sales og samstilltir við Common Data Service (CDS) og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="09ec5-127">Tengiliður í Sales getur orðið Tengiliður í CDS og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="09ec5-128">Hinn kosturinn er að verða Lykill í CDS og Viðskiptavinur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="09ec5-129">Til að ákvarða hvort tengliður ætti að vera tekinn úr Sales fyrir samstillingu við CDS og Finance and Operations (til dæmis Tengiliðir í Sales &gt; Tengiliður í CDS &gt; Tengliðir í Finance and Operations) leitar kerfið að eftirfarandi eiginleikum Tengiliðar í Sales:</span><span class="sxs-lookup"><span data-stu-id="09ec5-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="09ec5-130">**Samstilla við Lykil í CDS og Viðskiptavin í Finance and Operations:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Já**</span><span class="sxs-lookup"><span data-stu-id="09ec5-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="09ec5-131">**Samstilla við Tengilið í CDS og Tengilið í Finance and Operations:** Tengiliðir þar sem **Er virkur viðskiptavinur** er stillt á **Nei** og **Fyrirtæki** (Yfirlykill/Tengiliður) bendir á Lykil (ekki Tengilið)</span><span class="sxs-lookup"><span data-stu-id="09ec5-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="09ec5-132">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="09ec5-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="09ec5-133">Nýjum **Er virkur viðskiptavinur** reit hefur verið bætt við Tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="09ec5-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="09ec5-134">Þessi reitur er notaður til að greina á milli Tengiliða sem hafa söluvirkni og Tengiliða sem hafa ekki söluvirkni.</span><span class="sxs-lookup"><span data-stu-id="09ec5-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="09ec5-135">**Er virkur viðskiptavinur** er aðeins stillt á **Já** fyrir Tengiliði sem hafa tengd tilboð, pantanir eða reikninga.</span><span class="sxs-lookup"><span data-stu-id="09ec5-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="09ec5-136">Aðeins þeir Tengiliðir eru samstillir við Finance and Operations sem Viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="09ec5-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="09ec5-137">Nýjum **IsCompanyAnAccount** reit hefur verið bætt við Tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="09ec5-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="09ec5-138">Þessi reitur er notaður til að gefa til kynna hvort Tengiliður er tengdur við Fyrirtæki (Yfirlykil/Tengilið) af gerðinni **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="09ec5-139">Þessar upplýsingar eru notaðar til að auðkenna Tengiliði sem samstilla á við Finance and Operations sem Tengiliði.</span><span class="sxs-lookup"><span data-stu-id="09ec5-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="09ec5-140">Nýjum reit fyrir **Númer Tengiliðar** hefur verið bætt við Tengiliðinn til að tryggja einkvæman raunlykil fyrir samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="09ec5-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="09ec5-141">Þegar nýr Tengiliður er stofnaður verður gildið **Númer tengiliðar** sjálfkrafa til með því að nota númeraröð.</span><span class="sxs-lookup"><span data-stu-id="09ec5-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="09ec5-142">Gildið samanstendur af **CON**, því næst hækkandi talnaröð og svo sex stafa viðskeyti.</span><span class="sxs-lookup"><span data-stu-id="09ec5-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="09ec5-143">Hér er dæmi: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="09ec5-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="09ec5-144">Þegar samþættingarlausninni fyrir Sales er bætt við Sales stillir uppfærsluforskrift reitinn **Númer tengiliðar** fyrir Tengiliði sem fyrir eru með því að nota talnaröðina sem var nefnd áður.</span><span class="sxs-lookup"><span data-stu-id="09ec5-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="09ec5-145">Uppfærsluforskriftin stillir líka reitinn **Er virkur viðskiptavinur** á **Já** fyrir alla Tengiliði með söluvirkni.</span><span class="sxs-lookup"><span data-stu-id="09ec5-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="09ec5-146">Í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-146">In Finance and Operations</span></span> 

<span data-ttu-id="09ec5-147">Tengiliðir eru merktir með eiginleikanum **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="09ec5-148">Þessi eiginleiki gefur til kynna að tilteknum Tengilið sé stjórnað utan frá.</span><span class="sxs-lookup"><span data-stu-id="09ec5-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="09ec5-149">Í þessu tilfelli er Tengiliðum sem er stjórnað utan frá stjórnað í Sales.</span><span class="sxs-lookup"><span data-stu-id="09ec5-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="09ec5-150">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="09ec5-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="09ec5-151">Frá Tengilið til Tengiliðs</span><span class="sxs-lookup"><span data-stu-id="09ec5-151">Contact to Contact</span></span>

- <span data-ttu-id="09ec5-152">Uppfærðu **CDS-fyrirtækjaauðkenni** í **Uppruna &gt; CDS** vörpun.</span><span class="sxs-lookup"><span data-stu-id="09ec5-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="09ec5-153">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId [Fyrirtækjaauðkenni]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="09ec5-154">Sjálfgefið sniðmátsgildi fyrir **PrimaryAccount_Organization_OrganizationId [Fyrirtækjaauðkenni]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="09ec5-155">**Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="09ec5-156">Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi í vörpununum **CDS &gt; Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="09ec5-157">Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="09ec5-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="09ec5-158">Sjálfgefið sniðmátsgildi fyrir **PrimaryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="09ec5-159">Gakktu úr skugga um að gildi fyrir eftirfarandi reiti séu til staðar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="09ec5-160">Ef upplýsingarnar eru ekki nauðsynlegar í Finance and Operations er hægt að fjarlægja vörpunina úr vörpununum **CDS &gt; Ákvörðunarstaður**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="09ec5-161">**Heiti reits í Finance and Operations::** Ákvörðun</span><span class="sxs-lookup"><span data-stu-id="09ec5-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="09ec5-162">**Vörpun:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="09ec5-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="09ec5-163">Frá Tengilið til Viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="09ec5-163">Contact to Customer</span></span>

- <span data-ttu-id="09ec5-164">Uppfærðu **CDS-fyrirtækjaauðkenni** í **Uppruna &gt; CDS** vörpun.</span><span class="sxs-lookup"><span data-stu-id="09ec5-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="09ec5-165">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId [Fyrirtækjaauðkenni]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="09ec5-166">**Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="09ec5-167">Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi í vörpununum **CDS &gt; Ákvörðunarstaður**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="09ec5-168">Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="09ec5-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="09ec5-169">Sjálfgefið sniðmátsgildi fyrir **PrimaryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="09ec5-170">**CustomerGroup** er nauðsynlegt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="09ec5-171">Til að koma í veg fyrir samstillingarvillur er hægt að tilgreina sjálfgefið gildi í vörpununum **CDS &gt; Ákvörðunarstaður**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="09ec5-172">Sjálfgefna gildið er svo notaðu ef reiturinn er skilinn eftir auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="09ec5-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="09ec5-173">Sjálfgefið sniðmátsgildi fyrir **CustomerGroupId** er **10**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="09ec5-174">Með því að bæta eftirfarandi vörpunum úr **CDS &gt; Ákvörðunarstað** geturðu dregið úr fjölda handvirkra uppfærslna í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="09ec5-175">Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="09ec5-176">**SiteId** - Einnig er hægt að skilgreina sjálfgefið svæði fyrir vörur í inance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="09ec5-177">Svæði er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="09ec5-178">Sniðmátsgildi fyrir **SiteId** er ekki skilgreint.</span><span class="sxs-lookup"><span data-stu-id="09ec5-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="09ec5-179">**WarehouseId** - Einnig er hægt að skilgreina sjálfgefið vöruhús fyrir vörur í inance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="09ec5-180">Vöruhús er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="09ec5-181">Sniðmátsgildi fyrir **WarehouseId** er ekki skilgreint.</span><span class="sxs-lookup"><span data-stu-id="09ec5-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="09ec5-182">**LanguageId** - Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09ec5-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="09ec5-183">Sjálfgefið sniðmátsgildi fyrir **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="09ec5-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="09ec5-184">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="09ec5-184">Template mapping in data integrator</span></span>

<span data-ttu-id="09ec5-185">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="09ec5-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="09ec5-186">Frá Tengilið til Tengiliðs</span><span class="sxs-lookup"><span data-stu-id="09ec5-186">Contact to Contact</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun fyrir Tengiliði í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="09ec5-189">Frá Tengilið til Viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="09ec5-189">Contact to Customer</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun fyrir Tengiliði í gagnasamþáttara](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="09ec5-192">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="09ec5-192">Related topics</span></span>

[<span data-ttu-id="09ec5-193">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="09ec5-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="09ec5-194">Samstilla lykla frá Sales til viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="09ec5-195">Samstilla hausa og línur sölutilboðs úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="09ec5-196">Samstilla hausa og línur sölupöntunar úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="09ec5-197">Samstilla hausa og línur sölureiknings úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="09ec5-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

