---
title: "Samstilla birgðaflutninga og leiðréttingar úr Field Service við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla birgðaleiðréttingar og færslur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="e96cb-103">Samstilla birgðaleiðréttingar úr Field Service við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e96cb-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e96cb-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla birgðaleiðréttingar og færslur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e96cb-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e96cb-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="e96cb-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e96cb-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="e96cb-106">Templates and tasks</span></span>
<span data-ttu-id="e96cb-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu birgðaleiðréttinga og færslna úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e96cb-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="e96cb-108">**Heiti sniðmátanna í gagnasamþættingu:**</span><span class="sxs-lookup"><span data-stu-id="e96cb-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="e96cb-109">Birgðaleiðrétting (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e96cb-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="e96cb-110">Birgðaflutningar (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="e96cb-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="e96cb-111">**Heiti verka í gagnasamþættingarverkum:**</span><span class="sxs-lookup"><span data-stu-id="e96cb-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="e96cb-112">Birgðaleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="e96cb-112">Inventory Adjustments</span></span>
- <span data-ttu-id="e96cb-113">Birgðaflutningar</span><span class="sxs-lookup"><span data-stu-id="e96cb-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="e96cb-114">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="e96cb-114">Entity set</span></span>
| <span data-ttu-id="e96cb-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="e96cb-115">Field Service</span></span>                     | <span data-ttu-id="e96cb-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e96cb-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="e96cb-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="e96cb-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="e96cb-118">CDS-færslubókarhausar og línur leiðréttingar á birgðaskrá</span><span class="sxs-lookup"><span data-stu-id="e96cb-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="e96cb-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="e96cb-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="e96cb-120">CDS-færslubókarhausar og línur fyrir birgðaflutning á birgðaskrá</span><span class="sxs-lookup"><span data-stu-id="e96cb-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="e96cb-121">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="e96cb-121">Entity flow</span></span>
<span data-ttu-id="e96cb-122">Birgðaleiðréttingar og flutningar sem gerðir eru í Field Service samstillast við Finance and Operations um leið og **Staða bókunar** breytist frá stofnað til bókað.</span><span class="sxs-lookup"><span data-stu-id="e96cb-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="e96cb-123">Þegar þetta gerist læsist leiðréttingin eða flutningspöntunin og verður skrifvarin því að leiðréttingar og flutningar kunna að vera bókaðar í Finance and Operations og er þar af leiðandi ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="e96cb-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="e96cb-124">Í Finance and Operations er hægt að setja upp runuvinnslu til að bóka breytingarnar sjálfvirkt og flytja birgðabækur sem myndast við samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="e96cb-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="e96cb-125">Sjá forsendur hér að neðan til að fá upplýsingar um hvernig eigi að virkja runuvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="e96cb-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e96cb-126">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="e96cb-126">Field Service CRM solution</span></span> 
<span data-ttu-id="e96cb-127">Reitnum Birgðaeining hefur verið bætt við Afurðareiningu.</span><span class="sxs-lookup"><span data-stu-id="e96cb-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="e96cb-128">Þessi reitur er nauðsynlegur úr því að Sölu- og birgðaeiningin er ekki alltaf sú sama í Operations, og við þurfum birgðaeininguna fyrir Birgðir í vöruhúsi í Operations.</span><span class="sxs-lookup"><span data-stu-id="e96cb-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="e96cb-129">Þegar þú setur afurðina á afurð birgðaleiðréttingar fyrir bæði Birgðaleiðréttingar og Birgðaflutninga verður einingin sótt úr gildinu fyrir afurð birgðaafurðar.</span><span class="sxs-lookup"><span data-stu-id="e96cb-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="e96cb-130">Ef gildi finnst verður reitnum Eining læst á Afurð birgðaleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="e96cb-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="e96cb-131">Reitnum Staða bókunar hefur verið bætt við bæði einingu Birgðaleiðréttingar og einingu Birgðaflutnings.</span><span class="sxs-lookup"><span data-stu-id="e96cb-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="e96cb-132">Þessi reitur er notaður sem sía þegar leiðrétting eða flutningur er sendur til Operations.</span><span class="sxs-lookup"><span data-stu-id="e96cb-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="e96cb-133">Reiturinn er sjálfgefinn á Stofnað (1) og er þá ekki sendur yfir í Operations.</span><span class="sxs-lookup"><span data-stu-id="e96cb-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="e96cb-134">Þegar honum er breytt í Bókað (2) er hann sendur yfir í Operations, en þá verður ekki lengur hægt að breyta neinu í Leiðréttingum eða Flutningi eða bæta nýjum línum við hann.</span><span class="sxs-lookup"><span data-stu-id="e96cb-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="e96cb-135">Reitnum Númeraröð hefur verið bætt við afurðareiningu birgðaleiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="e96cb-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="e96cb-136">Þessi reitur hjálpar samþættingunni að hafa einkvæmt númer svo samþættingin viti hvenær verið er að stofna og hvenær uppfæra.</span><span class="sxs-lookup"><span data-stu-id="e96cb-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="e96cb-137">Þegar þú stofnar þína fyrstu afurð birgðaleiðréttingar verður ný færsla til í P2C AutoNumber einingunni til að viðhalda númeraröðunum og forskeytinu sem er notað.</span><span class="sxs-lookup"><span data-stu-id="e96cb-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e96cb-138">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="e96cb-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="e96cb-139">Í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e96cb-139">In Finance and Operations</span></span>
<span data-ttu-id="e96cb-140">Birgðabækur samþættingar sem samþættingin bjó til er hægt að bóka sjálfvirkt með runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="e96cb-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="e96cb-141">Þetta er virkjað í: Birgðastjórnun > Reglubundin verkefni > CDS samþætting > Bóka samþættingarbirgðabækur</span><span class="sxs-lookup"><span data-stu-id="e96cb-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e96cb-142">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="e96cb-142">Template mapping in Data integration</span></span>

<span data-ttu-id="e96cb-143">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="e96cb-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="e96cb-144">Birgðaleiðrétting (Field Service til Finance and Operations): Birgðaleiðrétting</span><span class="sxs-lookup"><span data-stu-id="e96cb-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="e96cb-145">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="e96cb-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="e96cb-146">Birgðaflutningar (Field Service til Finance and Operations): Birgðaflutningur</span><span class="sxs-lookup"><span data-stu-id="e96cb-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="e96cb-147">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="e96cb-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

