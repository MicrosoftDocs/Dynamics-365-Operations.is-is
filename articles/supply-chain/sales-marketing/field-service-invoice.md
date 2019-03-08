---
title: Samstilla samkomulagsreikninga í Field Service við reikninga með frjálsum texta í Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla samningsreikninga úr Microsoft Dynamics 365 for Field Service við reikninga með frjálsum texta í Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "333255"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="cbba2-103">Samstilla reikningssamkomulag í Field Service við reikninga með frjálsum texta í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbba2-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cbba2-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla samningsreikninga úr Microsoft Dynamics 365 for Field Service við reikninga með frjálsum texta í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cbba2-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cbba2-105">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="cbba2-105">Templates and tasks</span></span>

<span data-ttu-id="cbba2-106">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að keyra samstillingu samkomulagsreikninga frá Field Service við reikninga með frjálsum texta í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cbba2-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="cbba2-107">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="cbba2-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cbba2-108">Samningsreikningar (Field Service við Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="cbba2-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="cbba2-109">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="cbba2-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="cbba2-110">Reikningshausar</span><span class="sxs-lookup"><span data-stu-id="cbba2-110">Invoice headers</span></span>
- <span data-ttu-id="cbba2-111">Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="cbba2-111">Invoice lines</span></span>

<span data-ttu-id="cbba2-112">Eftirfarandi samstillingar er krafist áður en samstilling samningsreikninga getur farið fram:</span><span class="sxs-lookup"><span data-stu-id="cbba2-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="cbba2-113">Lyklar (Sales til Fin and Ops) - Beint</span><span class="sxs-lookup"><span data-stu-id="cbba2-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="cbba2-114">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="cbba2-114">Entity set</span></span>

| <span data-ttu-id="cbba2-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="cbba2-115">Field Service</span></span>  | <span data-ttu-id="cbba2-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbba2-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="cbba2-117">reikningar</span><span class="sxs-lookup"><span data-stu-id="cbba2-117">invoices</span></span>       | <span data-ttu-id="cbba2-118">Frjálstextareikningshausar CDS viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cbba2-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="cbba2-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="cbba2-119">invoicedetails</span></span> | <span data-ttu-id="cbba2-120">Frjálstextareikningslínur CDS viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cbba2-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="cbba2-121">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="cbba2-121">Entity flow</span></span>

<span data-ttu-id="cbba2-122">Reikningar sem eru búnir til úr samningi í Field Service má samstilla við Finance and Operations með Common Data Service (CDS) gagnasamþættingarverki.</span><span class="sxs-lookup"><span data-stu-id="cbba2-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="cbba2-123">Uppfærslur á þessum reikningum verða samstilltar við reikninga með frjálsum texta í Finance and Operations ef bókhaldsstaða reiknings með frjálsum texta er **Í vinnslu**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="cbba2-124">Eftir að reikningar með frjálsum texta eru bókaðir í Finance and Operations og bókhaldsstaðan er uppfærð í **Lokið** verður ekki lengur hægt að samstilla uppfærslur frá Field Service.</span><span class="sxs-lookup"><span data-stu-id="cbba2-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cbba2-125">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="cbba2-125">Field Service CRM solution</span></span>

<span data-ttu-id="cbba2-126">Reitnum **Er með línur með samningsuppruna** hefur verið bætt við eininguna **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="cbba2-127">Þessi reitur hjálpar til við að tryggja að aðeins reikningar sem eru búnir til úr samningi séu samstilltir.</span><span class="sxs-lookup"><span data-stu-id="cbba2-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="cbba2-128">Gildið er **rétt** ef reikningurinn inniheldur að minnsta kosti eina reikningslínu sem kemur upprunalega úr samningi.</span><span class="sxs-lookup"><span data-stu-id="cbba2-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="cbba2-129">Reitnum **Er með samingsuppruna** hefur verið bætt við eininguna **Reikningslína**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="cbba2-130">Þessi reitur hjálpar til við að tryggja að aðeins reikningslínur sem eru búnar til úr samningi séu samstilltar.</span><span class="sxs-lookup"><span data-stu-id="cbba2-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="cbba2-131">Gildið er **rétt** ef reikningslínan kemur upprunalega úr samningi.</span><span class="sxs-lookup"><span data-stu-id="cbba2-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="cbba2-132">**Reikningsdagsetning** er áskilinn reitur í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cbba2-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="cbba2-133">Þess vegna verður reiturinn að hafa gildi í Field Service áður en samstillingin er gerð.</span><span class="sxs-lookup"><span data-stu-id="cbba2-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="cbba2-134">Til að uppfylla þessa kröfu er eftirfarandi reglu bætt við:</span><span class="sxs-lookup"><span data-stu-id="cbba2-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="cbba2-135">Ef reiturinn **Reikningsdagsetning** er auður á einingunni **Reikningur** (það er ef hann hefur ekkert gildi) er hann stilltur á núverandi dagsetningu þegar reikningslínu sem er upprunnin úr samningi er bætt við.</span><span class="sxs-lookup"><span data-stu-id="cbba2-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="cbba2-136">Notandi getur breytt reitnum **Reikningsdagsetning**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="cbba2-137">Hins vegar, þegar notandi reynir að vista reikning sem er upprunninn úr samningi, fær hann eða hún viðskiptaferilsvillu ef reiturinn **Reikningsdagsetning** er auður á reikningi.</span><span class="sxs-lookup"><span data-stu-id="cbba2-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cbba2-138">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="cbba2-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="cbba2-139">Í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbba2-139">In Finance and Operations</span></span>

<span data-ttu-id="cbba2-140">Setja verður upp uppruna reiknings fyrir samþættinguna til að greina reikninga með frjálsum texta í Finance and Operations sem eru búnir til úr samningsreikningum í Field Service.</span><span class="sxs-lookup"><span data-stu-id="cbba2-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="cbba2-141">Þegar reikningur hefur uppruna reiknings af gerðinni **Samþætting samningsreiknings** er reiturinn **Ytra reikningsnúmer** sýndur á haus **Sölureiknings**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="cbba2-142">Fyrir utan að birtast á reikningshausnum, er hægt að nota upplýsingarnar **Ytra reikningsnúmer** til að tryggja að reikningar sem eru búnir til úr samningsreikningum Field Service séu síaðir út við samstillingu reikninga úr Finance and Operations við Field Service.</span><span class="sxs-lookup"><span data-stu-id="cbba2-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="cbba2-143">Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Upprunakóðar reiknings**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="cbba2-144">Veldu **Nýr** til að búa til nýjan uppruna reiknings.</span><span class="sxs-lookup"><span data-stu-id="cbba2-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="cbba2-145">Í reitnum **Uppruni reiknings** skal færa inn heiti fyrir uppruna reiknings, t.d. **FS**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="cbba2-146">Í reitnum **Lýsing** skal færa inn lýsingu, t.d. **Samningsreikningur Field Service**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="cbba2-147">Veldu gátreitinn **Úthlutun upprunagerðar**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="cbba2-148">Stillið reitinn **Uppgrunagerð reiknings** á **Samþætting samningsreiknings**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="cbba2-149">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="cbba2-150">Í gagnasamþættingarverkinu</span><span class="sxs-lookup"><span data-stu-id="cbba2-150">In the Data Integration project</span></span>

<span data-ttu-id="cbba2-151">Verkefni: **Reikningslínur**</span><span class="sxs-lookup"><span data-stu-id="cbba2-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="cbba2-152">Gakktu úr skugga um að sjálfgefið gildi fyrir Finance and Operations reitinn **Birt gildi aðallykils** sé uppfært til að passa við æskilegt gildi.</span><span class="sxs-lookup"><span data-stu-id="cbba2-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="cbba2-153">Sjálfgefið sniðmátsgildi er **401100**.</span><span class="sxs-lookup"><span data-stu-id="cbba2-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cbba2-154">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="cbba2-154">Template mapping in Data integration</span></span>

<span data-ttu-id="cbba2-155">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="cbba2-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="cbba2-156">Samningsreikningar (Field Service to Fin og Ops): Reikningshausar</span><span class="sxs-lookup"><span data-stu-id="cbba2-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="cbba2-157">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="cbba2-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="cbba2-158">Samningsreikningar (Field Service to Fin og Ops): Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="cbba2-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="cbba2-159">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="cbba2-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
