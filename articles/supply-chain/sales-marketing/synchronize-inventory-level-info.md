---
title: "Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla upplýsingar um birgðastöðu úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e2e65-103">Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="e2e65-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2e65-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla upplýsingar um birgðastöðu úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e2e65-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e2e65-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e2e65-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e2e65-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="e2e65-106">Templates and tasks</span></span>
<span data-ttu-id="e2e65-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á birgðastöðu á lager úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e2e65-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e2e65-108">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="e2e65-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e2e65-109">Birgðir afurðar (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e2e65-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="e2e65-110">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="e2e65-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e2e65-111">Birgðir afurðar</span><span class="sxs-lookup"><span data-stu-id="e2e65-111">Product inventory</span></span>

<span data-ttu-id="e2e65-112">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling við birgðastöður getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="e2e65-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e2e65-113">Vöruhús (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e2e65-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="e2e65-114">Afurðir Field Service með birgðaeiningu (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="e2e65-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e2e65-115">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="e2e65-115">Entity set</span></span>

| <span data-ttu-id="e2e65-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e2e65-116">Field Service</span></span>                      | <span data-ttu-id="e2e65-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2e65-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e2e65-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e2e65-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e2e65-119">CDS-birgðir á lager eftir vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="e2e65-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e2e65-120">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="e2e65-120">Entity flow</span></span>
<span data-ttu-id="e2e65-121">Upplýsingar um birgðastöðu úr Finance and Operations eru sendar til Field Service fyrir valdar afurðir.</span><span class="sxs-lookup"><span data-stu-id="e2e65-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="e2e65-122">Upplýsingar um birgðastöðu innihalda:</span><span class="sxs-lookup"><span data-stu-id="e2e65-122">The inventory level information include:</span></span> 
- <span data-ttu-id="e2e65-123">Lagermagn (núgildandi skráð raunmagn sem er staðsett í vöruhúsinu)</span><span class="sxs-lookup"><span data-stu-id="e2e65-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="e2e65-124">Pöntunarmagn (samtals skráð magn í pöntun - t.d. sölupöntun)</span><span class="sxs-lookup"><span data-stu-id="e2e65-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="e2e65-125">Pantað magn (samtals skráð pantað magn - t.d. innkaupapöntun)</span><span class="sxs-lookup"><span data-stu-id="e2e65-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="e2e65-126">Þessar upplýsingar eru sóttar fyrir hverja útgefna afurð fyrir hvert vöruhús og samstilltar á grunni breytingarakningar, þegar birgðastaða breytist.</span><span class="sxs-lookup"><span data-stu-id="e2e65-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e2e65-127">Í Field Service bjó samþættingarlausnin til birgðabækur fyrir delta, til að stöðurnar í Field Service til að passa við stöðurnar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2e65-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="e2e65-128">Finance and Operations virkar sem aðalsniðmátið fyrir birgðastöður.</span><span class="sxs-lookup"><span data-stu-id="e2e65-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="e2e65-129">Því er mikilvægt að setja upp samþættingu fyrir vinnupantanir, flutninga og leiðréttingar úr Field Service við Finance and Operations ef þessi virkni er notuð í Field Service, ásamt samstillingu á birgðastöðum úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2e65-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="e2e65-130">Afurðir og vöruhús þar sem birgðastöður eru „mastered“ úr Finance and Operations er hægt að stjórna með ítarlegri fyrirspurn og afmörkun (Power Query).</span><span class="sxs-lookup"><span data-stu-id="e2e65-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="e2e65-131">Athugið: Mögulegt er að búa til mörg vöruhús í Field Services (með Er viðhaldið utan frá = Nei) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="e2e65-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e2e65-132">Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi einfaldlega uppfærslur til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2e65-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="e2e65-133">Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2e65-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="e2e65-134">Sjá viðbótarupplýsingar í Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations og Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2e65-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e2e65-135">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="e2e65-135">Field Service CRM solution</span></span>
<span data-ttu-id="e2e65-136">Birgðaeining ytri afurðar er ný eining sem er aðeins notuð fyrir bakvinnslu í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="e2e65-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="e2e65-137">Hún fær gildi fyrir birgðastöðu úr Finance and Operations í samþættingunni og umbreytir síðan þessum gildum í Handvirkar birgðabækur sem síðan breytir afurðum birgða í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="e2e65-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e2e65-138">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="e2e65-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="e2e65-139">Í gagnasamþættingarverkinu</span><span class="sxs-lookup"><span data-stu-id="e2e65-139">In the Data Integration project</span></span>
<span data-ttu-id="e2e65-140">Nota síur með ítarlegri fyrirspurn og síun til að stýra því að eingöngu æskilegar afurðir og vöruhús sendi upplýsingar um birgðastöðu úr Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="e2e65-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e2e65-141">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="e2e65-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="e2e65-142">Birgðir afurðar (Finance and Operations til Field Service): Birgðir afurðar</span><span class="sxs-lookup"><span data-stu-id="e2e65-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="e2e65-143">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e2e65-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

