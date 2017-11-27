---
title: "Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="0322a-103">Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0322a-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0322a-104">Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="0322a-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="0322a-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="0322a-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="0322a-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="0322a-106">Template and tasks</span></span>

<span data-ttu-id="0322a-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur úr Sales í Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="0322a-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="0322a-108">**Nafn sniðmáts:** Sölutilboð (Sales í Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="0322a-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="0322a-109">**Heiti verkefnanna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="0322a-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="0322a-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="0322a-110">QuoteHeader</span></span>
    - <span data-ttu-id="0322a-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="0322a-111">QuoteLine</span></span>

<span data-ttu-id="0322a-112">Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="0322a-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="0322a-113">Vörur (Fin og Ops til Sales )</span><span class="sxs-lookup"><span data-stu-id="0322a-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="0322a-114">Reikningar (Sales við Fin and Ops) (ef notað)</span><span class="sxs-lookup"><span data-stu-id="0322a-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="0322a-115">Tengiliðir við viðskiptavini (Sales við Fin and Ops) (ef notað)</span><span class="sxs-lookup"><span data-stu-id="0322a-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="0322a-116">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="0322a-116">Entity set</span></span>

| <span data-ttu-id="0322a-117">Sölur</span><span class="sxs-lookup"><span data-stu-id="0322a-117">Sales</span></span>        | <span data-ttu-id="0322a-118">CDS</span><span class="sxs-lookup"><span data-stu-id="0322a-118">CDS</span></span>           | <span data-ttu-id="0322a-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0322a-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="0322a-120">Tilvitnanir</span><span class="sxs-lookup"><span data-stu-id="0322a-120">Quotes</span></span>       | <span data-ttu-id="0322a-121">Tilboð</span><span class="sxs-lookup"><span data-stu-id="0322a-121">Quotation</span></span>     | <span data-ttu-id="0322a-122">Sölutilboðshausar</span><span class="sxs-lookup"><span data-stu-id="0322a-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="0322a-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="0322a-123">QuoteDetails</span></span> | <span data-ttu-id="0322a-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="0322a-124">QuotationLine</span></span> | <span data-ttu-id="0322a-125">CDS-sölutilboðslínur</span><span class="sxs-lookup"><span data-stu-id="0322a-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="0322a-126">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="0322a-126">Entity flow</span></span>

<span data-ttu-id="0322a-127">Sölutilboð eru stofnuð í Sales og samstillt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="0322a-128">Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="0322a-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="0322a-129">Unnið er með allar afurðir í sölutilboðslínum utan frá.</span><span class="sxs-lookup"><span data-stu-id="0322a-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="0322a-130">Sölutilboðið er virkt eða virkjað.</span><span class="sxs-lookup"><span data-stu-id="0322a-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0322a-131">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="0322a-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="0322a-132">Reitnum **Hefur aðeins afurðir sem unnið er með utan frá** hefur verið bætt við sölutilboðseininguna til að fylgjast með því hvort sölutilboð samanstendur eingöngu af afurðum sem unnið er með utan frá.</span><span class="sxs-lookup"><span data-stu-id="0322a-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="0322a-133">Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="0322a-134">Þessi hegðun hjálpar til við að tryggja að þú reynir ekki að samstilla sölutilboðslínur við vörur sem eru óþekktar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="0322a-135">Allar afurðir og línur í tilboðinu eru uppfærðar með upplýsingunum í **Hefur aðeins afurðir sem unnið er með utan frá** úr tilboðshaus.</span><span class="sxs-lookup"><span data-stu-id="0322a-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="0322a-136">Þessar upplýsingar má finna í reitnum **Tilboðið hefur aðeins afurðir sem unnið er með utan frá** á tilboðslínueiningu.</span><span class="sxs-lookup"><span data-stu-id="0322a-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="0322a-137">Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="0322a-138">Þessi uppsetning styður ekki samþættingarvörpun eins og er.</span><span class="sxs-lookup"><span data-stu-id="0322a-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="0322a-139">Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **Skattur** stýrt og meðhöndlaðir af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="0322a-140">I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="0322a-141">**Ritvarðir reitir í sölutilboðshaus:** Afsláttur % Afsláttur, Fraktupphæð</span><span class="sxs-lookup"><span data-stu-id="0322a-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="0322a-142">**Ritvarðir reitir í sölutilboðslínum:** Skattur</span><span class="sxs-lookup"><span data-stu-id="0322a-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0322a-143">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="0322a-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="0322a-144">Fyrir samstillingu sölupantana er mikilvægt að uppfæra kerfin með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="0322a-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="0322a-145">Uppsetning í Sales</span><span class="sxs-lookup"><span data-stu-id="0322a-145">Setup in Sales</span></span>

- <span data-ttu-id="0322a-146">Farðu í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sales** og gakktu úr skugga um að reiturinn **Reikningsaðferð reikningsafsláttar** sé stilltur á **Á einingu**.</span><span class="sxs-lookup"><span data-stu-id="0322a-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="0322a-147">Þessi stilling hjálpar til við að tryggja að línuafsláttur vöru í Sales sé sá sami og stillingarnar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="0322a-148">Að öðrum kosti er afslátturinn ekki réttur í Finance and Operations, þar sem Finance and Operations les afsláttinn á hverja einingu þrátt fyrir að hann sé á hverja línu í Sales.</span><span class="sxs-lookup"><span data-stu-id="0322a-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="0322a-149">Uppsetning Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0322a-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="0322a-150">Farðu í **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="0322a-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="0322a-151">Í flipanum **Númeraröð** skaltu velja númeraröðina fyrir sölutilboðið og smelltu svo á **Skoða upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="0322a-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="0322a-152">Því næst, undir **Almenn uppsetning**, stilltu reitinn **Handvirkt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0322a-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="0322a-153">Farðu í **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakröfu**.</span><span class="sxs-lookup"><span data-stu-id="0322a-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="0322a-154">Því næst, í flipanum **Sendingar**, stilltu reitinn **Stýring afhendingardagsetninga** á **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="0322a-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="0322a-155">Þessi stilling hjálpar til við að koma í veg fyrir að samstilling bregðist fyrir sölutilboð.</span><span class="sxs-lookup"><span data-stu-id="0322a-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="0322a-156">Setja upp gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="0322a-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="0322a-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="0322a-157">QuoteHeader</span></span>

- <span data-ttu-id="0322a-158">Reiturinn **Umbeðin afhendingardagsetning** er nauðsynlegur í Finance and Operations og samstilling gengur ekki eftir ef reiturinn er auður.</span><span class="sxs-lookup"><span data-stu-id="0322a-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="0322a-159">Til að koma í veg fyrir þetta vandamál, ef reiturinn er auður, er sjálfgefin dagsetning sótt í **Uppruni &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="0322a-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="0322a-160">Dagsetningin skal uppfærð í æskilegt gildi.</span><span class="sxs-lookup"><span data-stu-id="0322a-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="0322a-161">Sem stendur er ekki hægt að færa inn gildi eins og **Í dag** til að standa fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="0322a-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="0322a-162">Það verður að færa inn tiltekna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="0322a-162">You must enter a specific date.</span></span> <span data-ttu-id="0322a-163">Gildi sniðmátsgildsins fyrir **Umbeðna afhendingardagsetningu** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="0322a-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="0322a-164">Reiturinn **Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="0322a-165">Til að koma í veg fyrir samstillingarvillur, er hægt að tilgreina sjálfgefið gildi sem er notað ef reiturinn er hafður auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="0322a-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="0322a-166">Þetta sjálfgefna gildi er einnig gagnlegt vegna þess að þú þarft ekki að færa handvirkt inn gildi í reitinn **Landsvæði** fyrir staðbundin aðsetur.</span><span class="sxs-lookup"><span data-stu-id="0322a-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="0322a-167">Það er ekkert sjálfgefið sniðmátsgildi fyrir **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="0322a-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="0322a-168">Uppfærðu vörpunina fyrir **CDS-fyrirtækjaauðkenni** í **Uppruni &gt; CDS** þannig að hún samsvari **CDS-fyrirtæki** í fyrirtækiseiningunni:</span><span class="sxs-lookup"><span data-stu-id="0322a-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="0322a-169">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0322a-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="0322a-170">Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0322a-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="0322a-171">Sjálfgefið sniðmátsgildi fyrir **InvoiceAccount_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0322a-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="0322a-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="0322a-172">QuoteLine</span></span>

- <span data-ttu-id="0322a-173">Uppfærðu vörpunina fyrir **CDS-fyrirtækjaauðkenni** í **Uppruni &gt; CDS** þannig að hún samsvari **CDS-fyrirtæki** í fyrirtækiseiningunni:</span><span class="sxs-lookup"><span data-stu-id="0322a-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="0322a-174">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0322a-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="0322a-175">Sjálfgefið sniðmátsgildi fyrir **Product_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0322a-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="0322a-176">Sjálfgefið sniðmátsgildi fyrir **Quotation_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0322a-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="0322a-177">Reiturinn **Umbeðin afhendingardagsetning** er nauðsynlegur í Finance and Operations og samstilling gengur ekki eftir ef reiturinn er auður.</span><span class="sxs-lookup"><span data-stu-id="0322a-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="0322a-178">Til að koma í veg fyrir þetta vandamál, ef reiturinn er auður, er sjálfgefin dagsetning sótt í **Uppruni &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="0322a-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="0322a-179">Dagsetningin skal uppfærð í æskilegt gildi.</span><span class="sxs-lookup"><span data-stu-id="0322a-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="0322a-180">Sem stendur er ekki hægt að færa inn gildi eins og **Í dag** til að standa fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="0322a-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="0322a-181">Það verður að færa inn tiltekna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="0322a-181">You must enter a specific date.</span></span> <span data-ttu-id="0322a-182">Gildi sniðmátsgildsins fyrir **Umbeðna afhendingardagsetningu** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="0322a-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="0322a-183">Hægt er að bæta við eftirfarandi vörpunum úr **CDS &gt; Viðtökustaður** til að hjálpa til við að tryggja að sölutilboðslínur séu fluttar inn í Finance and Operations ef það eru engar sjálfgefnar upplýsingar, hvorki frá viðskiptavini né afurð:</span><span class="sxs-lookup"><span data-stu-id="0322a-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="0322a-184">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="0322a-185">Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="0322a-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="0322a-186">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="0322a-187">Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="0322a-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="0322a-188">Gakktu úr skugga um að nauðsynleg gildisvörpun fyrir sölu á mælieiningu (UOM) í Finance and Operations sé til í vörpuninni **CDS &gt; Viðtökustaður** fyrir **Magn_Mælieiningu** í **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="0322a-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0322a-189">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="0322a-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="0322a-190">Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="0322a-191">Þessi uppsetning styður ekki samþættingarvörpun eins og er.</span><span class="sxs-lookup"><span data-stu-id="0322a-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="0322a-192">Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0322a-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="0322a-193">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="0322a-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="0322a-194">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="0322a-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="0322a-195">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="0322a-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="0322a-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="0322a-196">QuoteHeader</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="0322a-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="0322a-199">QuoteLine</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="0322a-202">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="0322a-202">Related topics</span></span>

[<span data-ttu-id="0322a-203">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="0322a-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="0322a-204">Samstilla lykla úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0322a-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0322a-205">Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0322a-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



