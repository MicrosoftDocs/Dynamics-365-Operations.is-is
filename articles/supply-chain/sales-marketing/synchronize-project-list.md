---
title: Samstilla verklista úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/14/2019
ms.locfileid: "842605"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c278f-103">Samstilla verklista úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="c278f-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c278f-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c278f-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c278f-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="c278f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c278f-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="c278f-106">Templates and tasks</span></span>
<span data-ttu-id="c278f-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á verkum milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c278f-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c278f-108">**Sniðmát í gagnasamþættingu**</span><span class="sxs-lookup"><span data-stu-id="c278f-108">**Template in Data integration**</span></span>
- <span data-ttu-id="c278f-109">Verk (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="c278f-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="c278f-110">**Verkefni í verki gagnasamþættingar**</span><span class="sxs-lookup"><span data-stu-id="c278f-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="c278f-111">Verk</span><span class="sxs-lookup"><span data-stu-id="c278f-111">Projects</span></span>

<span data-ttu-id="c278f-112">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling á verklista getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="c278f-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="c278f-113">Lyklar (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c278f-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c278f-114">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="c278f-114">Entity set</span></span>
| <span data-ttu-id="c278f-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c278f-115">Field Service</span></span>           | <span data-ttu-id="c278f-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c278f-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="c278f-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="c278f-117">msdynce_externalprojects</span></span> | <span data-ttu-id="c278f-118">Verk</span><span class="sxs-lookup"><span data-stu-id="c278f-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="c278f-119">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="c278f-119">Entity flow</span></span>
<span data-ttu-id="c278f-120">Verk eru búin til í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c278f-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="c278f-121">Verk með **Gerð verks** stillt á **Tími og efni** og **Verkstig** still á **Í vinnslu** samstillast við eininguna **Ytri verk** í Field Service, þ.m.t. verknúmer, verkheiti, verkstig og upplýsingar um viðskiptavinalykil.</span><span class="sxs-lookup"><span data-stu-id="c278f-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="c278f-122">Listinn **Ytri verk** er notaður til að para saman vinnupantanir Field Service við verk Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c278f-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c278f-123">CRM-lausn Field Service</span><span class="sxs-lookup"><span data-stu-id="c278f-123">Field Service CRM solution</span></span>
<span data-ttu-id="c278f-124">Einingin **Ytra verk** fær öll verkefnin úr Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c278f-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="c278f-125">Reitnum **Ytra verk** hefur verið bætt við eininguna **Vinnupöntun**.</span><span class="sxs-lookup"><span data-stu-id="c278f-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="c278f-126">Þetta er uppflettireitur og með því að merkja vinnupöntunina þína við verk mun sölupöntunin tengjast við verkið innan Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c278f-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="c278f-127">Þegar **Kerfisstaða** breytist úr **Opin - Í vinnslu (690.970.000)** yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="c278f-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c278f-128">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="c278f-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="c278f-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c278f-129">Finance and Operations</span></span>
<span data-ttu-id="c278f-130">Virkja rakningarbreytingu fyrir verk gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="c278f-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c278f-131">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="c278f-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="c278f-132">Verk (Fin and Ops til Field Service): Verk</span><span class="sxs-lookup"><span data-stu-id="c278f-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="c278f-133">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="c278f-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
