---
title: "Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur úr Microsoft Dynamics 365 for Sales í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="f0b8f-103">Samstilla sölutilboðshausa og línur úr Sales í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0b8f-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f0b8f-104">Áður en þú getur notað lausnina Prospect to cash þarftu að kynna þér [Dynamics 365 gagnasamþættingu](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="f0b8f-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="f0b8f-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla sölutilboðshausa og línur úr Microsoft Dynamics 365 for Sales (Sales) í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="f0b8f-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="f0b8f-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="f0b8f-106">Template and tasks</span></span>

<span data-ttu-id="f0b8f-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla sölutilboðshausa og línur úr Sales í Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="f0b8f-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="f0b8f-108">**Nafn sniðmáts:** Sölutilboð (Sales í Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f0b8f-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="f0b8f-109">**Heiti verkefnanna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="f0b8f-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="f0b8f-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f0b8f-110">QuoteHeader</span></span>
    - <span data-ttu-id="f0b8f-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f0b8f-111">QuoteLine</span></span>

<span data-ttu-id="f0b8f-112">Eftirfarandi samstillingarverk eru nauðsynleg áður en samstilling úr sölutilboðshausum og línum getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="f0b8f-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="f0b8f-113">Afurðir</span><span class="sxs-lookup"><span data-stu-id="f0b8f-113">Products</span></span>
- <span data-ttu-id="f0b8f-114">Lyklar (ef þeir eru notaðir)</span><span class="sxs-lookup"><span data-stu-id="f0b8f-114">Accounts (if used)</span></span>
- <span data-ttu-id="f0b8f-115">Tengiliðir (ef þeir eru notaðir)</span><span class="sxs-lookup"><span data-stu-id="f0b8f-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="f0b8f-116">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="f0b8f-116">Entity set</span></span>

| <span data-ttu-id="f0b8f-117">Sala</span><span class="sxs-lookup"><span data-stu-id="f0b8f-117">Sales</span></span>        | <span data-ttu-id="f0b8f-118">CDS</span><span class="sxs-lookup"><span data-stu-id="f0b8f-118">CDS</span></span>           | <span data-ttu-id="f0b8f-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0b8f-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="f0b8f-120">Tilvitnanir</span><span class="sxs-lookup"><span data-stu-id="f0b8f-120">Quotes</span></span>       | <span data-ttu-id="f0b8f-121">Tilboð</span><span class="sxs-lookup"><span data-stu-id="f0b8f-121">Quotation</span></span>     | <span data-ttu-id="f0b8f-122">Sölutilboðshausar</span><span class="sxs-lookup"><span data-stu-id="f0b8f-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="f0b8f-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="f0b8f-123">QuoteDetails</span></span> | <span data-ttu-id="f0b8f-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="f0b8f-124">QuotationLine</span></span> | <span data-ttu-id="f0b8f-125">CDS-sölutilboðslínur</span><span class="sxs-lookup"><span data-stu-id="f0b8f-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f0b8f-126">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="f0b8f-126">Entity flow</span></span>

<span data-ttu-id="f0b8f-127">Sölutilboð eru stofnuð í Sales og samstillt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="f0b8f-128">Sölutilboð úr Sales eru aðeins samstillt ef eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="f0b8f-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="f0b8f-129">Unnið er með allar afurðir í sölutilboðslínum utan frá.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="f0b8f-130">Sölutilboðið er virkt eða virkjað.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f0b8f-131">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="f0b8f-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f0b8f-132">Reitnum **Hefur aðeins afurðir sem unnið er með utan frá** hefur verið bætt við sölutilboðseininguna til að fylgjast með því hvort sölutilboð samanstendur eingöngu af afurðum sem unnið er með utan frá.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="f0b8f-133">Ef sölutilboð inniheldur aðeins afurðir sem unnið er með utan frá, er afurðunum stýrt í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-134">Þessi hegðun hjálpar til við að tryggja að þú reynir ekki að samstilla sölutilboðslínur við vörur sem eru óþekktar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="f0b8f-135">Allar afurðir og línur í tilboðinu eru uppfærðar með upplýsingunum í **Hefur aðeins afurðir sem unnið er með utan frá** úr tilboðshaus.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="f0b8f-136">Þessar upplýsingar má finna í reitnum **Tilboðið hefur aðeins afurðir sem unnið er með utan frá** á tilboðslínueiningu.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="f0b8f-137">Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-138">Þessi uppsetning styður ekki samþættingarvörpun eins og er.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="f0b8f-139">Í núverandi hönnun er reitunum **Verð**, **Afsláttur**, **Gjöld** og **Skattur** stýrt og meðhöndlaðir af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="f0b8f-140">I Sales gerir lausnin það að verkum að eftirfarandi reitir eru ritvarðir, þar sem gildin eru ekki samstillt við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="f0b8f-141">**Ritvarðir reitir í sölutilboðshaus:** Afsláttur % Afsláttur, Fraktupphæð</span><span class="sxs-lookup"><span data-stu-id="f0b8f-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="f0b8f-142">**Ritvarðir reitir í sölutilboðslínum:** Skattur</span><span class="sxs-lookup"><span data-stu-id="f0b8f-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f0b8f-143">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="f0b8f-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="f0b8f-144">Áður en þú samstillir sölutilboð í Sales, farðu í **Stillingar** &gt; **Stjórnun** &gt; **Kerfisstillingar** &gt; **Sala** og gakktu úr skugga um að reiturinn **Útreikningsaðferð afsláttar** sé stilltur á **Á hverja einingu**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="f0b8f-145">Þessi stilling hjálpar til við að tryggja að línuafsláttur vöru í Sales sé sá sami og stillingarnar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-146">Að öðrum kosti er afslátturinn ekki réttur í Finance and Operations, þar sem Finance and Operations les afsláttinn á hverja einingu þrátt fyrir að hann sé á hverja línu í Sales.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="f0b8f-147">Í Finance and Operations, farðu í **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="f0b8f-148">Í flipanum **Númeraröð** skaltu velja númeraröðina fyrir sölutilboðið og smelltu svo á **Skoða upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="f0b8f-149">Því næst, undir **Almenn uppsetning**, stilltu reitinn **Handvirkt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="f0b8f-150">Í Finance and Operations, farðu í **Viðskiptakröfur** &gt; **Uppsetning** &gt; **Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="f0b8f-151">Því næst, í flipanum **Sendingar**, stilltu reitinn **Stýring afhendingardagsetninga** á **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="f0b8f-152">Þessi stilling hjálpar til við að koma í veg fyrir að samstilling bregðist fyrir sölutilboð.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="f0b8f-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f0b8f-153">QuoteHeader</span></span>

- <span data-ttu-id="f0b8f-154">Reiturinn **Umbeðin afhendingardagsetning** er nauðsynlegur í Finance and Operations og samstilling gengur ekki eftir ef reiturinn er auður.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="f0b8f-155">Til að koma í veg fyrir þetta vandamál, ef reiturinn er auður, er sjálfgefin dagsetning sótt í **Uppruni &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="f0b8f-156">Dagsetningin skal uppfærð í æskilegt gildi.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="f0b8f-157">Sem stendur er ekki hægt að færa inn gildi eins og **Í dag** til að standa fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="f0b8f-158">Það verður að færa inn tiltekna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-158">You must enter a specific date.</span></span> <span data-ttu-id="f0b8f-159">Gildi sniðmátsgildsins fyrir **Umbeðna afhendingardagsetningu** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="f0b8f-160">Reiturinn **Svæðiskóði fyrir aðsetursland** er nauðsynlegur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-161">Til að koma í veg fyrir samstillingarvillur, er hægt að tilgreina sjálfgefið gildi sem er notað ef reiturinn er hafður auður í Sales.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="f0b8f-162">Þetta sjálfgefna gildi er einnig gagnlegt vegna þess að þú þarft ekki að færa handvirkt inn gildi í reitinn **Landsvæði** fyrir staðbundin aðsetur.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="f0b8f-163">Það er ekkert sjálfgefið sniðmátsgildi fyrir **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="f0b8f-164">Uppfærðu vörpunina fyrir **CDS-fyrirtækjaauðkenni** í **Uppruni &gt; CDS** þannig að hún samsvari **CDS-fyrirtæki** í fyrirtækiseiningunni:</span><span class="sxs-lookup"><span data-stu-id="f0b8f-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="f0b8f-165">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f0b8f-166">Sjálfgefið sniðmátsgildi fyrir **Account_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f0b8f-167">Sjálfgefið sniðmátsgildi fyrir **InvoiceAccount_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="f0b8f-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f0b8f-168">QuoteLine</span></span>

- <span data-ttu-id="f0b8f-169">Uppfærðu vörpunina fyrir **CDS-fyrirtækjaauðkenni** í **Uppruni &gt; CDS** þannig að hún samsvari **CDS-fyrirtæki** í fyrirtækiseiningunni:</span><span class="sxs-lookup"><span data-stu-id="f0b8f-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="f0b8f-170">Sjálfgefið sniðmátsgildi fyrir **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f0b8f-171">Sjálfgefið sniðmátsgildi fyrir **Product_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f0b8f-172">Sjálfgefið sniðmátsgildi fyrir **Quotation_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="f0b8f-173">Reiturinn **Umbeðin afhendingardagsetning** er nauðsynlegur í Finance and Operations og samstilling gengur ekki eftir ef reiturinn er auður.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="f0b8f-174">Til að koma í veg fyrir þetta vandamál, ef reiturinn er auður, er sjálfgefin dagsetning sótt í **Uppruni &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="f0b8f-175">Dagsetningin skal uppfærð í æskilegt gildi.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="f0b8f-176">Sem stendur er ekki hægt að færa inn gildi eins og **Í dag** til að standa fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="f0b8f-177">Það verður að færa inn tiltekna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-177">You must enter a specific date.</span></span> <span data-ttu-id="f0b8f-178">Gildi sniðmátsgildsins fyrir **Umbeðna afhendingardagsetningu** er **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="f0b8f-179">Hægt er að bæta við eftirfarandi vörpunum úr **CDS &gt; Viðtökustaður** til að hjálpa til við að tryggja að sölutilboðslínur séu fluttar inn í Finance and Operations ef það eru engar sjálfgefnar upplýsingar, hvorki frá viðskiptavini né afurð:</span><span class="sxs-lookup"><span data-stu-id="f0b8f-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="f0b8f-180">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-181">Það eru engin sjálfgefin sniðmátsgildi fyrir **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="f0b8f-182">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-183">Það er engin sjálfgefin sniðmátsgildi fyrir **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="f0b8f-184">Gakktu úr skugga um að nauðsynleg gildisvörpun fyrir sölu á mælieiningu (UOM) í Finance and Operations sé til í vörpuninni **CDS &gt; Viðtökustaður** fyrir **Magn_Mælieiningu** í **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f0b8f-185">Sniðmátsvörpun í gagnasamþáttara</span><span class="sxs-lookup"><span data-stu-id="f0b8f-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="f0b8f-186">Reitunum **Afsláttur**, **Gjöld** og **Skattur** er stýrt af flókinni uppsetningu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f0b8f-187">Þessi uppsetning styður ekki samþættingarvörpun eins og er.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="f0b8f-188">Í núverandi hönnun eru reitirnir **Verð**, **Afsláttur**, **Gjöld** og **Skattur** meðhöndlaðir af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="f0b8f-189">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="f0b8f-190">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f0b8f-191">Eftirfarandi skýringamyndir sýna dæmi um sniðmátsvörpun í gagnasamþáttara.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="f0b8f-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f0b8f-192">QuoteHeader</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="f0b8f-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f0b8f-195">QuoteLine</span></span>

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Sniðmátsvörpun í gagnasamþáttara](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="f0b8f-198">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="f0b8f-198">Related topics</span></span>

[<span data-ttu-id="f0b8f-199">Samstilla afurðir úr Finance and Operations í afurðir í Sales</span><span class="sxs-lookup"><span data-stu-id="f0b8f-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="f0b8f-200">Samstilla lykla frá Sales til viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0b8f-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="f0b8f-201">Samstilla tengiliði frá Sales til tengiliða eða viðskiptavina í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0b8f-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



