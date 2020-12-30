---
title: Samstilla vöruhús úr Supply Chain Management við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vöruhús úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 28445592d7a2a8964b1642ae52cff08be6feabbe
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529507"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="d01a4-103">Samstilla vöruhús úr Supply Chain Management við Field Service</span><span class="sxs-lookup"><span data-stu-id="d01a4-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d01a4-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vöruhús úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="d01a4-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="d01a4-105">[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="d01a4-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d01a4-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="d01a4-106">Templates and tasks</span></span>
<span data-ttu-id="d01a4-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu vöruhúsa úr Supply Chain Management í Field Service.</span><span class="sxs-lookup"><span data-stu-id="d01a4-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="d01a4-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="d01a4-108">**Template in Data integration**</span></span>
- <span data-ttu-id="d01a4-109">Vöruhús (Supply Chain Management við Field Service)</span><span class="sxs-lookup"><span data-stu-id="d01a4-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="d01a4-110">**Verkefni í verki gagnasamþættingar**</span><span class="sxs-lookup"><span data-stu-id="d01a4-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="d01a4-111">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="d01a4-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="d01a4-112">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="d01a4-112">Entity set</span></span>
| <span data-ttu-id="d01a4-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="d01a4-113">Field Service</span></span>    | <span data-ttu-id="d01a4-114">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="d01a4-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="d01a4-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="d01a4-115">msdyn_warehouses</span></span> | <span data-ttu-id="d01a4-116">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="d01a4-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="d01a4-117">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="d01a4-117">Entity flow</span></span>
<span data-ttu-id="d01a4-118">Vöruhús sem eru búin til og unnið með í Supply Chain Management er hægt að samstilla við Field Service í gegnum verk gagnasamþættingar Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="d01a4-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="d01a4-119">Vöruhús sem á að samstilla við Field Service er hægt að stýra með ítarlegri fyrirspurn og síun í verkinu.</span><span class="sxs-lookup"><span data-stu-id="d01a4-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="d01a4-120">Vöruhús sem samstillast úr Supply Chain Management eru búin til í Field Service með reitinn **Er viðhaldið utan frá** stilltan á **Já** og færslan er gerð skrifvarin.</span><span class="sxs-lookup"><span data-stu-id="d01a4-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d01a4-121">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="d01a4-121">Field Service CRM solution</span></span>
<span data-ttu-id="d01a4-122">Til að styðja við samþættingu milli Field Service og Supply Chain Management, er þörf á frekari virkni frá CRM-lausn Field Service.</span><span class="sxs-lookup"><span data-stu-id="d01a4-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="d01a4-123">Í lausninni hefur reitnum **Er viðhaldið utan frá** verið bætt við eininguna **Vöruhús (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="d01a4-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="d01a4-124">Þessi reitur hjálpar til við að bera kennsl á hvort vöruhúsið sé meðhöndlað í Supply Chain Management eða ef það er aðeins til í Field Service.</span><span class="sxs-lookup"><span data-stu-id="d01a4-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="d01a4-125">Stillingar fyrir þennan reit innihalda:</span><span class="sxs-lookup"><span data-stu-id="d01a4-125">The settings for this field include:</span></span>
- <span data-ttu-id="d01a4-126">**Já** – Vöruhúsið á uppruna í Supply Chain Management og er ekki hægt að breyta í Sales.</span><span class="sxs-lookup"><span data-stu-id="d01a4-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="d01a4-127">**Nei** - Vöruhúsið var fært beint inn í Field Service og er unnið með það hér.</span><span class="sxs-lookup"><span data-stu-id="d01a4-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="d01a4-128">Reiturinn **Er viðhaldið að utan** hjálpar til við að stjórna samstillingu á birgðastöðum, leiðréttingum, flutningum og notkun á vinnupöntunum.</span><span class="sxs-lookup"><span data-stu-id="d01a4-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="d01a4-129">Aðeins ef **Er viðhaldið að utan** vöruhúss er stillt á **Já** er hægt að nota til að samstilla beint við sama vöruhúsið í öðru kerfi.</span><span class="sxs-lookup"><span data-stu-id="d01a4-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="d01a4-130">Mögulegt er að búa til mörg vöruhús í Field Service (með **Er viðhaldið utan frá** = Nei) og síðan varpa þeim í stakt vöruhús, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="d01a4-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="d01a4-131">Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi aðeins uppfærslur til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d01a4-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="d01a4-132">Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d01a4-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="d01a4-133">Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="d01a4-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d01a4-134">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="d01a4-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="d01a4-135">Gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="d01a4-135">Data Integration project</span></span>
<span data-ttu-id="d01a4-136">Á undan samstillingu vöruhúsa skal ganga úr skugga um að uppfæra ítarlega fyrirspurn og síun á verkinu til að hafa eingöngu með vöruhús sem þú vilt taka með úr Supply Chain Management og yfir í Field Service.</span><span class="sxs-lookup"><span data-stu-id="d01a4-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="d01a4-137">Athugaðu að þú þarft vöruhúsið í Field Service til að nota það fyrir vinnupantanir, leiðréttingar og flutninga.</span><span class="sxs-lookup"><span data-stu-id="d01a4-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="d01a4-138">Til að ganga skugga um að **Samþættingarlykill** sé til fyrir **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="d01a4-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="d01a4-139">Farðu í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="d01a4-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="d01a4-140">Veldu flipann **Tengistilling**.</span><span class="sxs-lookup"><span data-stu-id="d01a4-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="d01a4-141">Veldu stillingu á tengingu sem er notuð fyrir samstillingu vinnupöntunar.</span><span class="sxs-lookup"><span data-stu-id="d01a4-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="d01a4-142">Veldu flipann **Samþættingarlykill**.</span><span class="sxs-lookup"><span data-stu-id="d01a4-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="d01a4-143">Finndu msdyn_warehouses og gakktu úr skugga um að lyklinum **msdyn_name (heiti)** hafi verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="d01a4-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="d01a4-144">Ef hann er ekki sýndur skaltu bæta honum við með því að smella á **Bæta við lykli** og smella á **Vista** efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="d01a4-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d01a4-145">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="d01a4-145">Template mapping in Data integration</span></span>

<span data-ttu-id="d01a4-146">Eftirfarandi mynd sýnir sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="d01a4-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="d01a4-147">Vöruhús (Supply Chain Management við Field Service): Warehouse</span><span class="sxs-lookup"><span data-stu-id="d01a4-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="d01a4-148">[![Sniðmátsvörpun í Gagnasamþættingu](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="d01a4-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
