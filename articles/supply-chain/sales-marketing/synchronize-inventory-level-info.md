---
title: Samstilla upplýsingar um birgðastöðu úr Supply Chain Management við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910281"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="73d1b-103">Samstilla upplýsingar um birgðastöðu úr Supply Chain Management við Field Service</span><span class="sxs-lookup"><span data-stu-id="73d1b-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="73d1b-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="73d1b-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="73d1b-105">[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="73d1b-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="73d1b-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="73d1b-106">Templates and tasks</span></span>
<span data-ttu-id="73d1b-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla lagerstig birgða úr Supply Chain Management í Field Service.</span><span class="sxs-lookup"><span data-stu-id="73d1b-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="73d1b-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="73d1b-108">**Template in Data integration**</span></span>
- <span data-ttu-id="73d1b-109">Vörubirgðir (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="73d1b-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="73d1b-110">**Verkefni í verki gagnasamþættingar**</span><span class="sxs-lookup"><span data-stu-id="73d1b-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="73d1b-111">Birgðir afurðar</span><span class="sxs-lookup"><span data-stu-id="73d1b-111">Product inventory</span></span>

<span data-ttu-id="73d1b-112">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling við birgðastöður getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="73d1b-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="73d1b-113">Vöruhús (Supply Chain Management við Field Service)</span><span class="sxs-lookup"><span data-stu-id="73d1b-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="73d1b-114">Afurðir Field Service við birgðaeiningu (Supply Chain Management við Sales)</span><span class="sxs-lookup"><span data-stu-id="73d1b-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="73d1b-115">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="73d1b-115">Entity set</span></span>

| <span data-ttu-id="73d1b-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="73d1b-116">Field Service</span></span>                      | <span data-ttu-id="73d1b-117">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="73d1b-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="73d1b-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="73d1b-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="73d1b-119">Dataverse birgðir á lager eftir vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="73d1b-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="73d1b-120">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="73d1b-120">Entity flow</span></span>
<span data-ttu-id="73d1b-121">Upplýsingar um birgðastöðu úr Finance and Operations eru sendar til Field Service fyrir valdar afurðir.</span><span class="sxs-lookup"><span data-stu-id="73d1b-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="73d1b-122">Upplýsingarnar um birgðastöðu fela í sér:</span><span class="sxs-lookup"><span data-stu-id="73d1b-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="73d1b-123">Lagermagn (núgildandi skráð efnislegt magn sem er staðsett í vöruhúsinu)</span><span class="sxs-lookup"><span data-stu-id="73d1b-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="73d1b-124">Pöntunarmagn (heildarskráð magn í pöntun, t.d. sölupantanir)</span><span class="sxs-lookup"><span data-stu-id="73d1b-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="73d1b-125">Pantað magn (samtals skráð pantað magn, t.d. innkaupapantanir)</span><span class="sxs-lookup"><span data-stu-id="73d1b-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="73d1b-126">Þessar upplýsingar eru sóttar fyrir hverja útgefna afurð fyrir hvert vöruhús og samstilltar á grunni breytingarakningar, þegar birgðastaða breytist.</span><span class="sxs-lookup"><span data-stu-id="73d1b-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="73d1b-127">Í Field Service býr samþættingarlausnin til birgðabækur fyrir delta, til að stöðurnar í Field Service passi við stöðurnar í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="73d1b-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="73d1b-128">Supply Chain Management virkar sem aðalsniðmátið fyrir birgðastöður.</span><span class="sxs-lookup"><span data-stu-id="73d1b-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="73d1b-129">Því er mikilvægt að setja upp samþættingu fyrir vinnupantanir, flutninga og leiðréttingar úr Field Service við Supply Chain Management ef þessi virkni er notuð í Field Service, ásamt samstillingu á birgðastöðum úr Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="73d1b-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="73d1b-130">Afurðir og vöruhús þar sem birgðastöður eru „mastered“ úr Supply Chain Management er hægt að stjórna með ítarlegri fyrirspurn og afmörkun (Power Query).</span><span class="sxs-lookup"><span data-stu-id="73d1b-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="73d1b-131">Mögulegt er að búa til mörg vöruhús í Field Services (með **Er viðhaldið utan frá = Nei**) og síðan varpa þeim í stakt vöruhús í Supply Chain Management, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="73d1b-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="73d1b-132">Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi eingöngu uppfærslur til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="73d1b-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="73d1b-133">Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="73d1b-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="73d1b-134">Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="73d1b-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="73d1b-135">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="73d1b-135">Field Service CRM solution</span></span>
<span data-ttu-id="73d1b-136">Einingin **Ytri birgðir afurðar** er aðeins notuð fyrir bakvinnslu í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="73d1b-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="73d1b-137">Þessi eining fær gildi fyrir birgðastöðu úr Supply Chain Management í samþættingunni og umbreytir síðan þessum gildum í Handvirkar birgðabækur sem síðan breytir afurðum birgða í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="73d1b-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="73d1b-138">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="73d1b-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="73d1b-139">Samþætting gagna</span><span class="sxs-lookup"><span data-stu-id="73d1b-139">Data integration</span></span>
<span data-ttu-id="73d1b-140">Til að verkið virki þarf að tryggja að samþættingarlykillinn sé uppfærður fyrir msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="73d1b-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="73d1b-141">Farið í **Gagnasamþætting > Tengjasöfn**.</span><span class="sxs-lookup"><span data-stu-id="73d1b-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="73d1b-142">Veljið notaða tengjasafnið.</span><span class="sxs-lookup"><span data-stu-id="73d1b-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="73d1b-143">Í flipanum **Samþættingarlykill** skal ganga úr skugga um að eftirfarandi lyklum sé bætt við msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="73d1b-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="73d1b-144">msdynce_productnumber (afurðarnúmer)</span><span class="sxs-lookup"><span data-stu-id="73d1b-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="73d1b-145">msdynce_warehouseid (auðkenni vöruhúss)</span><span class="sxs-lookup"><span data-stu-id="73d1b-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="73d1b-146">Gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="73d1b-146">Data integration project</span></span>
<span data-ttu-id="73d1b-147">Hægt er að nota síur með ítarlegri fyrirspurn og síun þannig að eingöngu ákveðnar afurðir og vöruhús sendi upplýsingar um birgðastöðu Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="73d1b-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="73d1b-148">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="73d1b-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="73d1b-149">Vörubirgðir (Supply Chain Management við Field Service): Product inventory</span><span class="sxs-lookup"><span data-stu-id="73d1b-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="73d1b-150">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="73d1b-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]