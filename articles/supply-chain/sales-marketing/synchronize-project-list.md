---
title: Samstilla verklista úr Supply Chain Management við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
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
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430001"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="c04f7-103">Samstilla verklista úr Supply Chain Management við Field Service</span><span class="sxs-lookup"><span data-stu-id="c04f7-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c04f7-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="c04f7-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="c04f7-105">[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="c04f7-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c04f7-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="c04f7-106">Templates and tasks</span></span>
<span data-ttu-id="c04f7-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu verka úr Supply Chain Management í Field Service.</span><span class="sxs-lookup"><span data-stu-id="c04f7-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="c04f7-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="c04f7-108">**Template in Data integration**</span></span>
- <span data-ttu-id="c04f7-109">Verk (Supply Chain Management við Field Service)</span><span class="sxs-lookup"><span data-stu-id="c04f7-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="c04f7-110">**Verkefni í verki gagnasamþættingar**</span><span class="sxs-lookup"><span data-stu-id="c04f7-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="c04f7-111">Verk</span><span class="sxs-lookup"><span data-stu-id="c04f7-111">Projects</span></span>

<span data-ttu-id="c04f7-112">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling á verklista getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="c04f7-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="c04f7-113">Lyklar (Sales til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="c04f7-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c04f7-114">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="c04f7-114">Entity set</span></span>
| <span data-ttu-id="c04f7-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c04f7-115">Field Service</span></span>           | <span data-ttu-id="c04f7-116">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="c04f7-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="c04f7-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="c04f7-117">msdynce_externalprojects</span></span> | <span data-ttu-id="c04f7-118">Verk</span><span class="sxs-lookup"><span data-stu-id="c04f7-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="c04f7-119">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="c04f7-119">Entity flow</span></span>
<span data-ttu-id="c04f7-120">Verkefni eru búin til í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c04f7-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="c04f7-121">Verk með **Gerð verks** stillt á **Tími og efni** og **Verkstig** still á **Í vinnslu** samstillast við eininguna **Ytri verk** í Field Service, þ.m.t. verknúmer, verkheiti, verkstig og upplýsingar um viðskiptavinalykil.</span><span class="sxs-lookup"><span data-stu-id="c04f7-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="c04f7-122">Listinn **Ytri verk** er notaður til að para saman vinnupantanir Field Service við verk Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c04f7-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c04f7-123">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="c04f7-123">Field Service CRM solution</span></span>
<span data-ttu-id="c04f7-124">Einingin **Ytra verk** fær öll verkefnin úr Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c04f7-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="c04f7-125">Reitnum **Ytra verk** hefur verið bætt við eininguna **Vinnupöntun**.</span><span class="sxs-lookup"><span data-stu-id="c04f7-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="c04f7-126">Þetta er uppflettireitur, og með því að merkja verkbeiðnina með verki mun sölupöntun verða tengd við verk innan Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c04f7-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="c04f7-127">Þegar **Kerfisstaða** breytist úr **Opin - Í vinnslu (690.970.000)** yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="c04f7-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c04f7-128">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="c04f7-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="c04f7-129">Birgðakeðjustjórnun</span><span class="sxs-lookup"><span data-stu-id="c04f7-129">Supply Chain Management</span></span>
<span data-ttu-id="c04f7-130">Virkja rakningarbreytingu fyrir verk gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="c04f7-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c04f7-131">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="c04f7-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="c04f7-132">Verk (Supply Chain Management við Field Service): Projects</span><span class="sxs-lookup"><span data-stu-id="c04f7-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="c04f7-133">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="c04f7-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
