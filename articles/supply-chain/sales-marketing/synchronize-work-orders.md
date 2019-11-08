---
title: Samstilla vinnupantanir við verk (úr Field Service í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Dynamics 365 Field Service við Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5c57b8d1e09fd57611accec83ec3da4bc596fd00
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627552"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="0d186-103">Samstilla vinnupantanir við verk (úr Field Service í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d186-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0d186-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Dynamics 365 Field Service við Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d186-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0d186-105">[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="0d186-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="0d186-106">Notaða sniðmátið **Vinnupantanir með Project (Field Service til Supply Chain Management)** er byggt á sniðmátinu **Vinnupantanir (Field Service til Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="0d186-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="0d186-107">Frekari upplýsingar er að finna í [Samstilla vinnupantanir úr Field Service við sölupantanir í Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="0d186-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="0d186-108">Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja:</span><span class="sxs-lookup"><span data-stu-id="0d186-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="0d186-109">**Verkbeiðnir við verk úr (Field Service í Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="0d186-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="0d186-110">**Verkbeiðnir verk úr (Field Service í Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="0d186-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="0d186-111">Helsti munurinn er sá að þetta sniðmát inniheldur vörpun verknúmers sem er úthlutað til vinnupöntunar í Field Service, sem tryggir að sölupöntunin sem er búin til í Supply Chain Management innihaldi verknúmerið og að reikningsfærsla geti átt sér stað fyrir tengt verk.</span><span class="sxs-lookup"><span data-stu-id="0d186-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="0d186-112">Að auki notar sniðmátið ítarlega fyrirspurn og síun.</span><span class="sxs-lookup"><span data-stu-id="0d186-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0d186-113">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="0d186-113">Templates and tasks</span></span>

<span data-ttu-id="0d186-114">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="0d186-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="0d186-115">Verkbeiðnir við verk úr (Field Service í Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="0d186-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="0d186-116">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="0d186-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="0d186-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0d186-117">WorkOrderHeader</span></span>
- <span data-ttu-id="0d186-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="0d186-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="0d186-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="0d186-119">WorkOrderProduct</span></span>
- <span data-ttu-id="0d186-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="0d186-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="0d186-121">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="0d186-121">Field Service CRM solution</span></span>
<span data-ttu-id="0d186-122">Reitnum **Ytra verk** hefur verið bætt við eininguna Vinnupantanir.</span><span class="sxs-lookup"><span data-stu-id="0d186-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="0d186-123">Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d186-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="0d186-124">Þegar **Kerfisstaða** breytist úr Opin - Í vinnslu (690.970.000) yfir í hærri stöðu, verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="0d186-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0d186-125">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="0d186-125">Template mapping in Data integration</span></span>

<span data-ttu-id="0d186-126">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="0d186-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="0d186-127">Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="0d186-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="0d186-128">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="0d186-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="0d186-129">Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="0d186-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="0d186-130">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="0d186-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="0d186-131">Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="0d186-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="0d186-132">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="0d186-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="0d186-133">Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="0d186-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="0d186-134">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="0d186-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
