---
title: Samstilla vinnupantanir með verki úr Field Service við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2019
ms.locfileid: "836443"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="8005b-103">Samstilla vinnupantanir með verki úr Field Service við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8005b-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8005b-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8005b-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="8005b-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="8005b-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="8005b-106">Notaða sniðmátið **Vinnupantanir með Project (Field Service til Fin and Ops)** er byggt á sniðmátinu **Vinnupantanir (Field Service til Fin and Ops)**.</span><span class="sxs-lookup"><span data-stu-id="8005b-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="8005b-107">Frekari upplýsingar er að finna í [Samstilla vinnupantanir úr Field Service við sölupantanir í Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="8005b-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="8005b-108">Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja:</span><span class="sxs-lookup"><span data-stu-id="8005b-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="8005b-109">**Vinnupantanir með Project (Field Service til Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="8005b-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="8005b-110">**Vinnupantanir (Field Service til Fin and Ops)**</span><span class="sxs-lookup"><span data-stu-id="8005b-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="8005b-111">Helsti munurinn er sá að þetta sniðmát inniheldur vörpun verknúmers sem er úthlutað til vinnupöntunar í Field Service, sem tryggir að sölupöntunin sem er búin til í Finance and Operations innihaldi verknúmerið og að reikningsfærsla geti átt sér stað fyrir tengt verk.</span><span class="sxs-lookup"><span data-stu-id="8005b-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="8005b-112">Að auki notar sniðmátið ítarlega fyrirspurn og síun.</span><span class="sxs-lookup"><span data-stu-id="8005b-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="8005b-113">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="8005b-113">Templates and tasks</span></span>

<span data-ttu-id="8005b-114">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="8005b-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="8005b-115">Vinnupantanir með Project (Field Service til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="8005b-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="8005b-116">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="8005b-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="8005b-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="8005b-117">WorkOrderHeader</span></span>
- <span data-ttu-id="8005b-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="8005b-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="8005b-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="8005b-119">WorkOrderProduct</span></span>
- <span data-ttu-id="8005b-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="8005b-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="8005b-121">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="8005b-121">Field Service CRM solution</span></span>
<span data-ttu-id="8005b-122">Reitnum **Ytra verk** hefur verið bætt við eininguna Vinnupantanir.</span><span class="sxs-lookup"><span data-stu-id="8005b-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="8005b-123">Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8005b-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="8005b-124">Þegar **Kerfisstaða** breytist úr Opin - Í vinnslu (690.970.000) yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="8005b-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8005b-125">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="8005b-125">Template mapping in Data integration</span></span>

<span data-ttu-id="8005b-126">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="8005b-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="8005b-127">Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="8005b-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="8005b-128">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="8005b-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="8005b-129">Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="8005b-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="8005b-130">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="8005b-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="8005b-131">Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="8005b-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="8005b-132">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="8005b-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="8005b-133">Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="8005b-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="8005b-134">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="8005b-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
