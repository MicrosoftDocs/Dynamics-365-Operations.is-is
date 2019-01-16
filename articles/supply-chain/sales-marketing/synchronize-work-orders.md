---
title: "Samstilla vinnupantanir úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem er notað til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations."
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="25fa1-103">Samstilla vinnupantanir með verki úr Field Service við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="25fa1-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="25fa1-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem er notað til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25fa1-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="25fa1-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="25fa1-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="25fa1-106">Notaða sniðmátið **Afurðir Field Service (Finance and Operations til Field Service)** er byggt á sniðmátinu **Afurðir (Finance and Operations til Sales) - Beint** úr Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="25fa1-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="25fa1-107">Nánari upplýsingar er að finna í [Afurðir (Finance and Operations til Sales) - Beint](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="25fa1-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="25fa1-108">Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Finance and Operations til Field Service)** og **Afurðir Field Service (Finance and Operations til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="25fa1-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="25fa1-109">Helsti munurinn er sá að þetta sniðmát inniheldur vörpun verknúmers sem er úthlutað til vinnupöntunar í Field Service, sem tryggir að sölupöntunin sem er búin til í Finance and Operations innihaldi verknúmerið og að reikningsfærsla geti átt sér stað fyrir tengt verk.</span><span class="sxs-lookup"><span data-stu-id="25fa1-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="25fa1-110">Að auki notar sniðmátið ítarlega fyrirspurn og síun.</span><span class="sxs-lookup"><span data-stu-id="25fa1-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="25fa1-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="25fa1-111">Templates and tasks</span></span>

<span data-ttu-id="25fa1-112">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="25fa1-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="25fa1-113">Vinnupantanir með verki (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="25fa1-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="25fa1-114">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="25fa1-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="25fa1-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="25fa1-115">WorkOrderHeader</span></span>
- <span data-ttu-id="25fa1-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="25fa1-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="25fa1-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="25fa1-117">WorkOrderProduct</span></span>
- <span data-ttu-id="25fa1-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="25fa1-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="25fa1-119">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="25fa1-119">Field Service CRM solution</span></span>
<span data-ttu-id="25fa1-120">Reitnum **Ytra verk** hefur verið bætt við eininguna Vinnupantanir.</span><span class="sxs-lookup"><span data-stu-id="25fa1-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="25fa1-121">Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25fa1-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="25fa1-122">Þegar **Kerfisstaða** breytist úr Opin - Í vinnslu (690.970.000) yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="25fa1-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="25fa1-123">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="25fa1-123">Template mapping in Data integration</span></span>

<span data-ttu-id="25fa1-124">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="25fa1-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="25fa1-125">Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="25fa1-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="25fa1-126">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="25fa1-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="25fa1-127">Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="25fa1-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="25fa1-128">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="25fa1-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="25fa1-129">Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="25fa1-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="25fa1-130">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="25fa1-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="25fa1-131">Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="25fa1-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="25fa1-132">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="25fa1-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

