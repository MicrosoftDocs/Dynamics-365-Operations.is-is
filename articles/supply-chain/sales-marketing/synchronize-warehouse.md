---
title: "Samstilla vöruhús úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="d8f1a-103">Samstilla vöruhús úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="d8f1a-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d8f1a-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla vöruhús úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d8f1a-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="d8f1a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d8f1a-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="d8f1a-106">Templates and tasks</span></span>
<span data-ttu-id="d8f1a-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á vöruhúsum úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d8f1a-108">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="d8f1a-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="d8f1a-109">Vöruhús (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="d8f1a-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="d8f1a-110">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="d8f1a-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="d8f1a-111">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="d8f1a-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="d8f1a-112">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="d8f1a-112">Entity set</span></span>
| <span data-ttu-id="d8f1a-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="d8f1a-113">Field Service</span></span>    | <span data-ttu-id="d8f1a-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d8f1a-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="d8f1a-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="d8f1a-115">msdyn_warehouses</span></span> | <span data-ttu-id="d8f1a-116">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="d8f1a-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="d8f1a-117">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="d8f1a-117">Entity flow</span></span>
<span data-ttu-id="d8f1a-118">Vöruhús sem eru búin til og unnið með í Finance and Operations er hægt að samstilla við Field Service í gegnum verk gagnasamþættingar Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="d8f1a-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="d8f1a-119">Æskileg vöruhús sem samstillast við Field Service er hægt að stýra með ítarlegri fyrirspurn og síun í verkinu.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="d8f1a-120">Vöruhús sem samstillast úr Finance and Operations eru búin til í Field Service með reitinn Er viðhaldið utanfrá stilltan á Já og færslan er gerð skrifvarin.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="d8f1a-121">CRM-lausn Field Service Til að styðja við samþættingu milli Field Service og Finance and Operations, er þörf á frekari virkni frá CRM-lausn Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="d8f1a-122">Lausnin inniheldur eftirfarandi breytingar.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-122">The solution includes the following changes.</span></span>
<span data-ttu-id="d8f1a-123">Reitnum **Er viðhaldið utanfrá** hefur verið bætt við eininguna **Vöruhús (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="d8f1a-124">Þessi reitur hjálpar til við að bera kennsl á hvort vöruhúsið sé meðhöndlað í Operations eða ef það er aðeins til í Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="d8f1a-125">Já – Vöruhús á uppruna í Finance and Operations og er ekki hægt að breyta í Sales.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="d8f1a-126">Nei - Vöruhúsið var fært beint inn í Field Service og er unnið með það hér.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="d8f1a-127">Reiturinn **Er viðhaldið að utan** hjálpar til við að stjórna samstillingu á birgðastöðum, leiðréttingum, flutningum og notkun á vinnupöntunum.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="d8f1a-128">Aðeins vöruhús með **Er viðhaldið að utan** = Já er hægt að nota til að samstilla beint við sama vöruhúsið í öðru kerfi.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="d8f1a-129">Athugið: Mögulegt er að búa til mörg vöruhús í Field Services (með **Er viðhaldið utan frá** = Nei) og síðan varpa þeim í stakt vöruhús í Finance and Operations, með eiginleikanum fyrir ítarlega fyrirspurn og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="d8f1a-130">Þetta er notað í kringumstæðum þar sem þú vilt að Field Service sjái um ítarlega birgðastöðu og sendi einfaldlega uppfærslur til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="d8f1a-131">Í þessu tilfelli fær Field Service ekki uppfærslur á birgðastöðu frá Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="d8f1a-132">Sjá viðbótarupplýsingar í Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations og Samstilla vinnupantanir í Field Service við sölupantanir sem eru tengdar verki í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d8f1a-133">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="d8f1a-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="d8f1a-134">Í gagnasamþættingarverkinu</span><span class="sxs-lookup"><span data-stu-id="d8f1a-134">In the Data Integration project</span></span>
<span data-ttu-id="d8f1a-135">Á undan samstillingu vöruhúsa skal ganga úr skugga um að uppfæra ítarlega fyrirspurn og síun á verkinu til að hafa eingöngu með vöruhús sem þú vilt taka með úr Finance and Operations og yfir í Field Service.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="d8f1a-136">Athugaðu að þú þarft vöruhúsið í Field Service til að nota það fyrir vinnupantanir, leiðréttingar og flutninga.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="d8f1a-137">Gakktu úr skugga um að **Samþættingarlykill** sé til fyrir **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="d8f1a-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="d8f1a-138">Farðu í gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="d8f1a-138">Go to Data Integration</span></span>
2. <span data-ttu-id="d8f1a-139">Veldu flipann **Tenging stillt**</span><span class="sxs-lookup"><span data-stu-id="d8f1a-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="d8f1a-140">Veldu stillingu á tengingu sem er notuð fyrir samstillingu vinnupöntunar</span><span class="sxs-lookup"><span data-stu-id="d8f1a-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="d8f1a-141">Veldu flipann **Samþættingarlykill**</span><span class="sxs-lookup"><span data-stu-id="d8f1a-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="d8f1a-142">Finndu msdyn_warehouses og athugaðu hvort lyklinum **msdyn_name (heiti)** hafi verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="d8f1a-143">Ef hann er ekki sýndur skaltu bæta honum við með því að smella á **Bæta við lykli** og smella á **Vista** efst á síðunni</span><span class="sxs-lookup"><span data-stu-id="d8f1a-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d8f1a-144">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="d8f1a-144">Template mapping in Data integration</span></span>

<span data-ttu-id="d8f1a-145">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="d8f1a-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="d8f1a-146">Vöruhús (Finance and Operations til Field Service): Vöruhús</span><span class="sxs-lookup"><span data-stu-id="d8f1a-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="d8f1a-147">[![Sniðmátsvörpun í Gagnasamþættingu](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="d8f1a-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

