---
title: Samstilla vöruhús úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "340316"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="accff-103">Samstilla vöruhús úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="accff-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="accff-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="accff-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="accff-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="accff-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="accff-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="accff-106">Templates and tasks</span></span>
<span data-ttu-id="accff-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu vöruhúss milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="accff-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="accff-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="accff-108">**Template in Data integration**</span></span>
- <span data-ttu-id="accff-109">Vöruhús (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="accff-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="accff-110">**Verkefni í verki gagnasamþættingar**</span><span class="sxs-lookup"><span data-stu-id="accff-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="accff-111">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="accff-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="accff-112">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="accff-112">Entity set</span></span>
| <span data-ttu-id="accff-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="accff-113">Field Service</span></span>    | <span data-ttu-id="accff-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="accff-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="accff-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="accff-115">msdyn_warehouses</span></span> | <span data-ttu-id="accff-116">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="accff-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="accff-117">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="accff-117">Entity flow</span></span>
<span data-ttu-id="accff-118">Vöruhús sem eru búin til og unnið með í Finance and Operations er hægt að samstilla við Field Service í gegnum verk gagnasamþættingar Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="accff-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="accff-119">Vöruhús sem á að samstilla við Field Service er hægt að stýra með ítarlegri fyrirspurn og síun í verkinu.</span><span class="sxs-lookup"><span data-stu-id="accff-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="accff-120">Vöruhús sem samstillast úr Finance and Operations eru búin til í Field Service með reitinn **Er viðhaldið utan frá** stilltan á **Já** og færslan er gerð skrifvarin.</span><span class="sxs-lookup"><span data-stu-id="accff-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="accff-121">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="accff-121">Field Service CRM solution</span></span>
<span data-ttu-id="accff-122">Til að styðja við samþættingu milli Field Service og Finance and Operations, er þörf á frekari virkni frá CRM-lausn Field Service.</span><span class="sxs-lookup"><span data-stu-id="accff-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="accff-123">Í lausninni hefur reitnum **Er viðhaldið utan frá** verið bætt við eininguna **Vöruhús (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="accff-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="accff-124">Þessi reitur hjálpar til við að bera kennsl á hvort vöruhúsið sé meðhöndlað í Finance and Operations eða ef það er aðeins til í Field Service.</span><span class="sxs-lookup"><span data-stu-id="accff-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="accff-125">Stillingar fyrir þennan reit innihalda:</span><span class="sxs-lookup"><span data-stu-id="accff-125">The settings for this field include:</span></span>
- <span data-ttu-id="accff-126">**Já** – Vöruhús á uppruna í Finance and Operations og er ekki hægt að breyta í Sales.</span><span class="sxs-lookup"><span data-stu-id="accff-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="accff-127">**Nei** - Vöruhúsið var fært beint inn í Field Service og er unnið með það hér.</span><span class="sxs-lookup"><span data-stu-id="accff-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="accff-128">Reiturinn **Er viðhaldið að utan** hjálpar til við að stjórna samstillingu á birgðastöðum, leiðréttingum, flutningum og notkun á vinnupöntunum.</span><span class="sxs-lookup"><span data-stu-id="accff-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="accff-129">Aðeins ef **Er viðhaldið að utan** vöruhúss er stillt á **Já** er hægt að nota til að samstilla beint við sama vöruhúsið í öðru kerfi.</span><span class="sxs-lookup"><span data-stu-id="accff-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="accff-130">Mögulegt er að búa til mörg vöruhús í Field Service (með **Er viðhaldið utan frá** = Nei) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="accff-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="accff-131">Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi einfaldlega uppfærslur til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="accff-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="accff-132">Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="accff-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="accff-133">Viðbótarupplýsingar er að finna í [Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="accff-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="accff-134">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="accff-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="accff-135">Gagnasamþættingarverk</span><span class="sxs-lookup"><span data-stu-id="accff-135">Data Integration project</span></span>
<span data-ttu-id="accff-136">Á undan samstillingu vöruhúsa skal ganga úr skugga um að uppfæra ítarlega fyrirspurn og síun á verkinu til að hafa eingöngu með vöruhús sem þú vilt taka með úr Finance and Operations og yfir í Field Service.</span><span class="sxs-lookup"><span data-stu-id="accff-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="accff-137">Athugaðu að þú þarft vöruhúsið í Field Service til að nota það fyrir vinnupantanir, leiðréttingar og flutninga.</span><span class="sxs-lookup"><span data-stu-id="accff-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="accff-138">Til að ganga skugga um að **Samþættingarlykill** sé til fyrir **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="accff-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="accff-139">Farðu í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="accff-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="accff-140">Veldu flipann **Tengistilling**.</span><span class="sxs-lookup"><span data-stu-id="accff-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="accff-141">Veldu stillingu á tengingu sem er notuð fyrir samstillingu vinnupöntunar.</span><span class="sxs-lookup"><span data-stu-id="accff-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="accff-142">Veldu flipann **Samþættingarlykill**.</span><span class="sxs-lookup"><span data-stu-id="accff-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="accff-143">Finndu msdyn_warehouses og gakktu úr skugga um að lyklinum **msdyn_name (heiti)** hafi verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="accff-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="accff-144">Ef hann er ekki sýndur skaltu bæta honum við með því að smella á **Bæta við lykli** og smella á **Vista** efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="accff-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="accff-145">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="accff-145">Template mapping in Data integration</span></span>

<span data-ttu-id="accff-146">Eftirfarandi mynd sýnir sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="accff-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="accff-147">Vöruhús (Finance and Operations til Field Service): Vöruhús</span><span class="sxs-lookup"><span data-stu-id="accff-147">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="accff-148">[![Sniðmátsvörpun í Gagnasamþættingu](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="accff-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
