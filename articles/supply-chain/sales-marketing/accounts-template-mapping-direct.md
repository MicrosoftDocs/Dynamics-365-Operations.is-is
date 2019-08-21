---
title: Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla lykla úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: 036389a1a52fdf15b73ab90c0a37108871a1a15e
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743349"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="8df5f-103">Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8df5f-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="8df5f-104">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="8df5f-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="8df5f-105">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla lykla beint úr Microsoft Dynamics 365 for Sales við Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="8df5f-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="8df5f-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="8df5f-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="8df5f-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="8df5f-108">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="8df5f-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8df5f-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="8df5f-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="8df5f-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="8df5f-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="8df5f-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="8df5f-111">Templates and tasks</span></span>

<span data-ttu-id="8df5f-112">Til að opna fyrirliggjandi sniðmát skaltu opna [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="8df5f-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="8df5f-113">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="8df5f-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8df5f-114">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla lykla frá Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8df5f-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="8df5f-115">**Heiti sniðmátsins í gagnaflutningi:** Reikningar (Sales í Fin and Ops) - beint</span><span class="sxs-lookup"><span data-stu-id="8df5f-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="8df5f-116">**Heiti verksins í verkefninu:** Reikningar - Viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="8df5f-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="8df5f-117">Ekki þarf að samstilla áður en samstilling Reiknings/Viðskiptamanns á sér stað.</span><span class="sxs-lookup"><span data-stu-id="8df5f-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="8df5f-118">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="8df5f-118">Entity set</span></span>

| <span data-ttu-id="8df5f-119">Sölur</span><span class="sxs-lookup"><span data-stu-id="8df5f-119">Sales</span></span>    | <span data-ttu-id="8df5f-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8df5f-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="8df5f-121">Lyklar</span><span class="sxs-lookup"><span data-stu-id="8df5f-121">Accounts</span></span> | <span data-ttu-id="8df5f-122">Viðskiptavinir V2</span><span class="sxs-lookup"><span data-stu-id="8df5f-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="8df5f-123">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="8df5f-123">Entity flow</span></span>

<span data-ttu-id="8df5f-124">Lyklum er stjórnað í Sales og þeir samstilltir við Finance and Operations sem viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="8df5f-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="8df5f-125">**Er viðhaldið utanfrá** eignin á þessum viðskiptamönnum er stillt á **Yes** til að rekja viðskiptamenn sem eiga uppruna sinn í Sales.</span><span class="sxs-lookup"><span data-stu-id="8df5f-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="8df5f-126">Við reikningsfærslu eru þessar upplýsingar notaðar til að sía reikninga sem eru samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="8df5f-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8df5f-127">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="8df5f-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="8df5f-128">Reiturinn **Lykilnúmer** er tiltækur á síðunni **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="8df5f-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="8df5f-129">Það er einkvæmur lykill til að styðja við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="8df5f-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="8df5f-130">Raunlykilseiginleikinn í Tengslastjórnunarlausninni (CRM) gæti haft áhrif á viðskiptavini sem nota þegar reitinn **Lykilnúmer** en nota ekki einkvæm **Lykilnúmersgildi** fyrir hvern lykil.</span><span class="sxs-lookup"><span data-stu-id="8df5f-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="8df5f-131">Eins og er styður samþættingarlausin ekki slík tilfelli.</span><span class="sxs-lookup"><span data-stu-id="8df5f-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="8df5f-132">Þegar nýr lykill er stofnaður, og ef **Lykilnúmersgildi** er ekki þegar til, er það sjálfkrafa búið til með talnaröð.</span><span class="sxs-lookup"><span data-stu-id="8df5f-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="8df5f-133">Gildið samanstendur af **ACC**, því næst hækkandi talnaröð og svo sex stafa viðskeyti.</span><span class="sxs-lookup"><span data-stu-id="8df5f-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="8df5f-134">Hér er dæmi: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="8df5f-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="8df5f-135">Þegar samþættingarlausnin fyrir Sales er notuð, stillir uppfærsluforskrift reitinn **Lykilnúmer** fyrir lykla sem þegar eru til í Sales.</span><span class="sxs-lookup"><span data-stu-id="8df5f-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="8df5f-136">Ef engin **Reikningsnúmer** gildi eru til staðar er númeraröðin sem var minnst á áður notuð.</span><span class="sxs-lookup"><span data-stu-id="8df5f-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="8df5f-137">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="8df5f-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="8df5f-138">**CustomerGroupId** vörpun verður að vera uppfærð í gilt gildi í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="8df5f-139">Hægt er að tilgreina sjálfgefið gildi eða setja upp gildi með því að nota gildisvörpun.</span><span class="sxs-lookup"><span data-stu-id="8df5f-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="8df5f-140">Sjálfgefið sniðmátsgildi er **10**.</span><span class="sxs-lookup"><span data-stu-id="8df5f-140">The default template value is **10**.</span></span>

- <span data-ttu-id="8df5f-141">Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="8df5f-142">Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.</span><span class="sxs-lookup"><span data-stu-id="8df5f-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="8df5f-143">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="8df5f-144">Sjálfgefið svæði er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="8df5f-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="8df5f-145">Sjálfgefið sniðmátsgildi er **1**.</span><span class="sxs-lookup"><span data-stu-id="8df5f-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="8df5f-146">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="8df5f-147">Sjálfgefið vöruhús er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="8df5f-148">Sjálfgefið sniðmátsgildi er **13**.</span><span class="sxs-lookup"><span data-stu-id="8df5f-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="8df5f-149">**LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="8df5f-150">Sjálfgefið er að tungumálið í pöntunarhausnum frá viðskiptavininum sé notað.</span><span class="sxs-lookup"><span data-stu-id="8df5f-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="8df5f-151">Sjálfgefið sniðmátsgildi er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="8df5f-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8df5f-152">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="8df5f-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="8df5f-153">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="8df5f-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="8df5f-154">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="8df5f-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="8df5f-155">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="8df5f-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="8df5f-156">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar ´ru Sales í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8df5f-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Sniðmátsvörpun í Gagnasamþættingu](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="8df5f-158">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="8df5f-158">Related topics</span></span>


[<span data-ttu-id="8df5f-159">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="8df5f-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="8df5f-160">Samstilla lykla beint úr Sales við viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8df5f-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="8df5f-161">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8df5f-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="8df5f-162">Samstilla hausa og línur sölupöntunar beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8df5f-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="8df5f-163">Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8df5f-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

