---
title: Samstilla birgðaflutninga og leiðréttingar úr Field Service við Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c989e6efff88768f0b370fc81eea971c5c11bcef
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251636"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="a5ba8-103">Samstilla birgðaleiðréttingar úr Field Service við Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a5ba8-103">Synchronize inventory adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a5ba8-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla birgðaleiðréttingar og flutninga úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="a5ba8-105">[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="a5ba8-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a5ba8-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="a5ba8-106">Templates and tasks</span></span>
<span data-ttu-id="a5ba8-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að samstilla birgpaleiðréttingar og -flutning úr Field Service í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="a5ba8-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="a5ba8-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="a5ba8-109">Birgðaleiðréttingar (Field Service við Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="a5ba8-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="a5ba8-110">Birgðaflutningur (Field Service við Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="a5ba8-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="a5ba8-111">**Verkefni í gagnasamþættingarverkum**</span><span class="sxs-lookup"><span data-stu-id="a5ba8-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="a5ba8-112">Birgðaleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="a5ba8-112">Inventory Adjustments</span></span>
- <span data-ttu-id="a5ba8-113">Birgðaflutningar</span><span class="sxs-lookup"><span data-stu-id="a5ba8-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="a5ba8-114">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="a5ba8-114">Entity set</span></span>
| <span data-ttu-id="a5ba8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="a5ba8-115">Field Service</span></span>                     | <span data-ttu-id="a5ba8-116">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="a5ba8-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="a5ba8-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="a5ba8-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="a5ba8-118">CDS-færslubókarhausar og línur leiðréttingar á birgðaskrá</span><span class="sxs-lookup"><span data-stu-id="a5ba8-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="a5ba8-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="a5ba8-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="a5ba8-120">CDS-færslubókarhausar og línur fyrir birgðaflutning á birgðaskrá</span><span class="sxs-lookup"><span data-stu-id="a5ba8-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="a5ba8-121">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="a5ba8-121">Entity flow</span></span>
<span data-ttu-id="a5ba8-122">Birgðaleiðréttingar og flutningar sem gerðir eru í Field Service samstillast við Supply Chain Management eftir að **Staða bókunar** breytist úr **Stofnað** í **Bókað**.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="a5ba8-123">Þegar þetta gerist verður leiðréttingin eða flutningspöntunin læst og verða aðeins skrifvarið.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="a5ba8-124">Þetta þýðir að bóka megi leiðréttingar og flutninga í Supply Chain Management, en ekki er hægt að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="a5ba8-125">Í Supply Chain Management er hægt að setja upp runuvinnslu til að bóka færslubækur leiðréttinga og birgðaflutninga sjálfvirkt sem myndast við samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="a5ba8-126">Sjá eftirfarandi skilyrði til að fá upplýsingar um hvernig eigi að virkja runuvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="a5ba8-127">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="a5ba8-127">Field Service CRM solution</span></span> 
<span data-ttu-id="a5ba8-128">Reitnum **Birgðaeining** hefur verið bætt við **Afurðareiningu**.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="a5ba8-129">Þessi reitur er nauðsynlegur úr því að Sölu- og birgðaeiningin er ekki alltaf sú sama í Supply Chain Management, og þörf er á birgðaeiningunni fyrir birgðir í vöruhúsi í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="a5ba8-130">Þegar þú setur afurðina á afurð birgðaleiðréttingar fyrir bæði Birgðaleiðréttingar og Birgðaflutninga verður einingin sótt úr gildi afurðar í birgðum.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="a5ba8-131">Ef gildi finnst verður reitnum **Eining** læst á Afurð birgðaleiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="a5ba8-132">Reitnum **Staða bókunar** hefur verið bætt við bæði einingu **Birgðaleiðréttingar** og einingu **Birgðaflutnings**.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="a5ba8-133">Þessi reitur er notaður sem sía þegar leiðrétting eða flutningur er sendur til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="a5ba8-134">Sjálfgildi fyrir þennan reit er Stofnað (1), en það er hins vegar ekki sent til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="a5ba8-135">Þegar gildið er uppfært í Bókað (2) er það sent yfir í Supply Chain Management, en eftir það verður ekki lengur hægt að breyta leiðréttingunni eða flutningnum eða bæta nýjum línum við.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="a5ba8-136">Reitnum **Númeraröð** hefur verið bætt við eininguna **Afurð birgðaleiðréttingar**.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="a5ba8-137">Þessi reitur tryggir að samþættingin hafi einkvæmt númer, þannig að samþættingin geti búið til og uppfært leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="a5ba8-138">Þegar þú stofnar þína fyrstu afurð birgðaleiðréttingar verður ný færsla til í **P2C AutoNumber** einingunni til að viðhalda númeraröðunum og forskeytinu sem er notað.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a5ba8-139">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="a5ba8-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="a5ba8-140">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="a5ba8-140">Supply Chain Management</span></span>
<span data-ttu-id="a5ba8-141">Birgðabækur samþættingar sem samþættingin bjó til er hægt að bóka sjálfvirkt með því að nota runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="a5ba8-142">Þetta er virkjað í: **Birgðastjórnun > Reglubundin verkefni > CDS samþætting > Bóka samþættingarbirgðabækur**.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5ba8-143">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="a5ba8-143">Template mapping in Data integration</span></span>

<span data-ttu-id="a5ba8-144">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="a5ba8-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="a5ba8-145">Birgðaleiðrétting (Field Service við Supply Chain Management): Inventory adjustment</span><span class="sxs-lookup"><span data-stu-id="a5ba8-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="a5ba8-146">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="a5ba8-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="a5ba8-147">Birgðaflutningur (Field Service við Supply Chain Management): Inventory transfer</span><span class="sxs-lookup"><span data-stu-id="a5ba8-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="a5ba8-148">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="a5ba8-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
