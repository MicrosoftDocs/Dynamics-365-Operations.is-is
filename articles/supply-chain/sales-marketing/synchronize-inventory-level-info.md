---
title: Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535699"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="97ba5-103">Samstilla upplýsingar um birgðastöðu úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="97ba5-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="97ba5-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla upplýsingar á birgðastigi úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="97ba5-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="97ba5-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="97ba5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="97ba5-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="97ba5-106">Templates and tasks</span></span>
<span data-ttu-id="97ba5-107">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla stig birgða á lager úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="97ba5-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="97ba5-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="97ba5-108">**Template in Data integration**</span></span>
- <span data-ttu-id="97ba5-109">Birgðir afurðar (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="97ba5-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="97ba5-110">**Verkefni í verki gagnasamþættingar**</span><span class="sxs-lookup"><span data-stu-id="97ba5-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="97ba5-111">Birgðir afurðar</span><span class="sxs-lookup"><span data-stu-id="97ba5-111">Product inventory</span></span>

<span data-ttu-id="97ba5-112">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling við birgðastöður getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="97ba5-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="97ba5-113">Vöruhús (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="97ba5-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="97ba5-114">Afurðir Field Service með birgðaeiningu (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="97ba5-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="97ba5-115">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="97ba5-115">Entity set</span></span>

| <span data-ttu-id="97ba5-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="97ba5-116">Field Service</span></span>                      | <span data-ttu-id="97ba5-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97ba5-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="97ba5-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="97ba5-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="97ba5-119">CDS-birgðir á lager eftir vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="97ba5-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="97ba5-120">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="97ba5-120">Entity flow</span></span>
<span data-ttu-id="97ba5-121">Upplýsingar um birgðastöðu úr Finance and Operations eru sendar til Field Service fyrir valdar afurðir.</span><span class="sxs-lookup"><span data-stu-id="97ba5-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="97ba5-122">Upplýsingarnar um birgðastöðu fela í sér:</span><span class="sxs-lookup"><span data-stu-id="97ba5-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="97ba5-123">Lagermagn (núgildandi skráð efnislegt magn sem er staðsett í vöruhúsinu)</span><span class="sxs-lookup"><span data-stu-id="97ba5-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="97ba5-124">Pöntunarmagn (heildarskráð magn í pöntun, t.d. sölupantanir)</span><span class="sxs-lookup"><span data-stu-id="97ba5-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="97ba5-125">Pantað magn (samtals skráð pantað magn, t.d. innkaupapantanir)</span><span class="sxs-lookup"><span data-stu-id="97ba5-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="97ba5-126">Þessar upplýsingar eru sóttar fyrir hverja útgefna afurð fyrir hvert vöruhús og samstilltar á grunni breytingarakningar, þegar birgðastaða breytist.</span><span class="sxs-lookup"><span data-stu-id="97ba5-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="97ba5-127">Í Field Service býr samþættingarlausnin til birgðabækur fyrir delta, til að stöðurnar í Field Service passi við stöðurnar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97ba5-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="97ba5-128">Finance and Operations virkar sem aðalsniðmátið fyrir birgðastöður.</span><span class="sxs-lookup"><span data-stu-id="97ba5-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="97ba5-129">Því er mikilvægt að setja upp samþættingu fyrir vinnupantanir, flutninga og leiðréttingar úr Field Service við Finance and Operations ef þessi virkni er notuð í Field Service, ásamt samstillingu á birgðastöðum úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97ba5-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="97ba5-130">Afurðir og vöruhús þar sem birgðastöður eru „mastered“ úr Finance and Operations er hægt að stjórna með ítarlegri fyrirspurn og afmörkun (Power Query).</span><span class="sxs-lookup"><span data-stu-id="97ba5-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="97ba5-131">Mögulegt er að búa til mörg vöruhús í Field Services (með **Er viðhaldið utan frá = Nei**) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="97ba5-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="97ba5-132">Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi eingöngu uppfærslur til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97ba5-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="97ba5-133">Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="97ba5-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="97ba5-134">Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="97ba5-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="97ba5-135">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="97ba5-135">Field Service CRM solution</span></span>
<span data-ttu-id="97ba5-136">Einingin **Ytri birgðir afurðar** er aðeins notuð fyrir bakvinnslu í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="97ba5-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="97ba5-137">Þessi eining fær gildi fyrir birgðastöðu úr Finance and Operations í samþættingunni og umbreytir síðan þessum gildum í Handvirkar birgðabækur sem síðan breytir afurðum birgða í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="97ba5-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="97ba5-138">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="97ba5-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="97ba5-139">Samþætting gagna</span><span class="sxs-lookup"><span data-stu-id="97ba5-139">Data integration</span></span>
<span data-ttu-id="97ba5-140">Til að verkið virki þarf að tryggja að samþættingarlykillinn sé uppfærður fyrir msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="97ba5-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="97ba5-141">Farið í **Gagnasamþætting > Tengjasöfn**.</span><span class="sxs-lookup"><span data-stu-id="97ba5-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="97ba5-142">Veljið notaða tengjasafnið.</span><span class="sxs-lookup"><span data-stu-id="97ba5-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="97ba5-143">Í flipanum **Samþættingarlykill** skal ganga úr skugga um að eftirfarandi lyklum sé bætt við msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="97ba5-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="97ba5-144">msdynce_productnumber (afurðarnúmer)</span><span class="sxs-lookup"><span data-stu-id="97ba5-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="97ba5-145">msdynce_warehouseid (auðkenni vöruhúss)</span><span class="sxs-lookup"><span data-stu-id="97ba5-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="97ba5-146">Gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="97ba5-146">Data integration project</span></span>
<span data-ttu-id="97ba5-147">Hægt er að nota síur með ítarlegri fyrirspurn og síun þannig að eingöngu ákveðnar afurðir og vöruhús sendi upplýsingar um birgðastöðu úr Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="97ba5-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="97ba5-148">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="97ba5-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="97ba5-149">Birgðir afurðar (Fin and Ops til Field Service): Birgðir afurðar</span><span class="sxs-lookup"><span data-stu-id="97ba5-149">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="97ba5-150">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="97ba5-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
