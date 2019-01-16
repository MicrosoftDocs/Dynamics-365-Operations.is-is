---
title: "Samstilla verklista úr Finance and Operations við Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: is-is
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="5e5c6-103">Samstilla verklista úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="5e5c6-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5e5c6-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem eru notuð til að samstilla verk úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="5e5c6-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="5e5c6-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5e5c6-106">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="5e5c6-106">Templates and tasks</span></span>
<span data-ttu-id="5e5c6-107">Eftirfarandi sniðmát og undirliggjandi verk eru notuð til að keyra samstillingu á verkum úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="5e5c6-108">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="5e5c6-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="5e5c6-109">Verk (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="5e5c6-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="5e5c6-110">**Heiti verksins í gagnasamþættingarverki:**</span><span class="sxs-lookup"><span data-stu-id="5e5c6-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="5e5c6-111">Verk</span><span class="sxs-lookup"><span data-stu-id="5e5c6-111">Projects</span></span>

<span data-ttu-id="5e5c6-112">Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstilling á verklista getur átt sér stað:</span><span class="sxs-lookup"><span data-stu-id="5e5c6-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="5e5c6-113">Lyklar (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="5e5c6-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="5e5c6-114">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="5e5c6-114">Entity set</span></span>
<span data-ttu-id="5e5c6-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e5c6-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="5e5c6-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="5e5c6-116">Field Service</span></span>           | <span data-ttu-id="5e5c6-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e5c6-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="5e5c6-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="5e5c6-118">msdynce_externalprojects</span></span> | <span data-ttu-id="5e5c6-119">Verk</span><span class="sxs-lookup"><span data-stu-id="5e5c6-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="5e5c6-120">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="5e5c6-120">Entity flow</span></span>
<span data-ttu-id="5e5c6-121">Verk eru búin til í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="5e5c6-122">Verk með **Gerð verks** tími og efni og **Verkstig** í vinnslu samstillast við eininguna **Ytri verk** í Field Service, þ.m.t. verknúmer, verkheiti, verkstig og upplýsingar um viðskiptavinalykil.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="5e5c6-123">Listinn yfir **Ytri verk** er notaður til að para saman vinnupantanir Field Service við verk Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="5e5c6-124">Ytra verk CRM-lausnir Field Service er ný eining sem fær öll verkin úr Operations.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="5e5c6-125">Reitnum Ytri verk hefur verið bætt við eininguna Vinnupantanir.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="5e5c6-126">Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Operations.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="5e5c6-127">Þegar kerfisstaða breytist í Opin - Í vinnslu (690.970.000) yfir í hærri stöðu verður reitnum Ytri verk læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="5e5c6-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="5e5c6-128">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="5e5c6-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="5e5c6-129">Í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e5c6-129">In Finance and Operations</span></span>
<span data-ttu-id="5e5c6-130">Virkja rakningarbreytingu fyrir verk gagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="5e5c6-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5e5c6-131">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="5e5c6-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="5e5c6-132">Verk (Finance and Operations til Field Service): Verk</span><span class="sxs-lookup"><span data-stu-id="5e5c6-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="5e5c6-133">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="5e5c6-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

