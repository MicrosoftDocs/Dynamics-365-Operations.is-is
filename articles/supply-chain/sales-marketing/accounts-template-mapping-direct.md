---
title: Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla reikninga úr Dynamics 365 Sales í Supply Chain Management.
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
ms.openlocfilehash: ebca416e94f44d0448a4f4d0be08f13e30e749e9
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813225"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="b4fd2-103">Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4fd2-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b4fd2-104">Áður en þú getur notað Prospect to cash lausnina ættirðu að kynna þér [Sameina gögn í Common Data Service fyrir forrit](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b4fd2-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="b4fd2-105">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla reikninga beint úr Dynamics 365 Sales í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b4fd2-106">Gagnaflæði í Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="b4fd2-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b4fd2-107">Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="b4fd2-108">Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="b4fd2-109">Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="b4fd2-110">[![Gagnaflæði í Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b4fd2-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b4fd2-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="b4fd2-111">Templates and tasks</span></span>

<span data-ttu-id="b4fd2-112">Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b4fd2-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b4fd2-113">Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b4fd2-114">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla lykla frá Sales til Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="b4fd2-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="b4fd2-115">**Heiti sniðmátsins í gagnaflutningi:** Reikningar (Sales í Fin and Ops) - beint</span><span class="sxs-lookup"><span data-stu-id="b4fd2-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="b4fd2-116">**Heiti verksins í verkefninu:** Reikningar - Viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="b4fd2-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="b4fd2-117">Ekki þarf að samstilla áður en samstilling Reiknings/Viðskiptamanns á sér stað.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b4fd2-118">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="b4fd2-118">Entity set</span></span>

| <span data-ttu-id="b4fd2-119">Sala</span><span class="sxs-lookup"><span data-stu-id="b4fd2-119">Sales</span></span>    | <span data-ttu-id="b4fd2-120">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="b4fd2-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="b4fd2-121">Lyklar</span><span class="sxs-lookup"><span data-stu-id="b4fd2-121">Accounts</span></span> | <span data-ttu-id="b4fd2-122">Viðskiptavinir V2</span><span class="sxs-lookup"><span data-stu-id="b4fd2-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b4fd2-123">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="b4fd2-123">Entity flow</span></span>

<span data-ttu-id="b4fd2-124">Lyklum er stjórnað í Sales og þeir samstilltir við Supply Chain Management sem viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="b4fd2-125">**Er viðhaldið utanfrá** eignin á þessum viðskiptamönnum er stillt á **Yes** til að rekja viðskiptamenn sem eiga uppruna sinn í Sales.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="b4fd2-126">Við reikningsfærslu eru þessar upplýsingar notaðar til að sía reikninga sem eru samstilltir við Sales.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b4fd2-127">Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="b4fd2-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b4fd2-128">Reiturinn **Lykilnúmer** er tiltækur á síðunni **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="b4fd2-129">Það er einkvæmur lykill til að styðja við samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="b4fd2-130">Raunlykilseiginleikinn í Tengslastjórnunarlausninni (CRM) gæti haft áhrif á viðskiptavini sem nota þegar reitinn **Lykilnúmer** en nota ekki einkvæm **Lykilnúmersgildi** fyrir hvern lykil.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="b4fd2-131">Eins og er styður samþættingarlausin ekki slík tilfelli.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="b4fd2-132">Þegar nýr lykill er stofnaður, og ef **Lykilnúmersgildi** er ekki þegar til, er það sjálfkrafa búið til með talnaröð.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="b4fd2-133">Gildið samanstendur af **ACC**, því næst hækkandi talnaröð og svo sex stafa viðskeyti.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="b4fd2-134">Hér er dæmi: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="b4fd2-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="b4fd2-135">Þegar samþættingarlausnin fyrir Sales er notuð, stillir uppfærsluforskrift reitinn **Lykilnúmer** fyrir lykla sem þegar eru til í Sales.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="b4fd2-136">Ef engin **Reikningsnúmer** gildi eru til staðar er númeraröðin sem var minnst á áður notuð.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b4fd2-137">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="b4fd2-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="b4fd2-138">**CustomerGroupId** vörpun verður að vera uppfærð í gilt gildi í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="b4fd2-139">Hægt er að tilgreina sjálfgefið gildi eða setja upp gildi með því að nota gildisvörpun.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="b4fd2-140">Sjálfgefið sniðmátsgildi er **10**.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-140">The default template value is **10**.</span></span>

- <span data-ttu-id="b4fd2-141">Með því að bæta við eftirfarandi vörpunum er hægt að hjálpa til við að minnka fjölda handvirkra uppfærslna sem eru nauðsynlegar í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="b4fd2-142">Hægt er að nota sjálfgefið gildi eða gildisvörpun frá til dæmis **Land/Svæði** eða **Borg**.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="b4fd2-143">**SiteId** – Svæði er nauðsynlegt til að búa til tilboð og sölupöntunarlínu í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="b4fd2-144">Sjálfgefið svæði er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="b4fd2-145">Sjálfgefið sniðmátsgildi er **1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="b4fd2-146">**WarehouseId** – Vöruhús er nauðsynlegt til að vinna úr tilboðum og sölupöntunarlínum í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="b4fd2-147">Sjálfgefið vöruhús er hægt að taka annaðhvort frá vörunni eða viðskiptavininum úr pöntunarhausnum í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="b4fd2-148">Sjálfgefið sniðmátsgildi er **13**.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="b4fd2-149">**LanguageId** – Tungumál er nauðsynlegt til að búa til tilboð og sölupantanir í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="b4fd2-150">Sjálfgefið er að tungumálið í pöntunarhausnum frá viðskiptavininum sé notað.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="b4fd2-151">Sjálfgefið sniðmátsgildi er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b4fd2-152">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="b4fd2-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="b4fd2-153">Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="b4fd2-154">Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b4fd2-155">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b4fd2-156">Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar úr Sales í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b4fd2-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Sniðmátsvörpun í Gagnasamþættingu](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="b4fd2-158">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="b4fd2-158">Related topics</span></span>


[<span data-ttu-id="b4fd2-159">Viðfang til sjóðstreymis</span><span class="sxs-lookup"><span data-stu-id="b4fd2-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b4fd2-160">Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4fd2-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b4fd2-161">Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4fd2-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="b4fd2-162">Samstilling sölupantana beint á milli Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b4fd2-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="b4fd2-163">Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales</span><span class="sxs-lookup"><span data-stu-id="b4fd2-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

