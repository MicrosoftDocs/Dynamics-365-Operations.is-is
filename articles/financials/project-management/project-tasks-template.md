---
title: "Samstilla verkefni verks beint frá Project Service Automation við Finance and Operations"
description: "Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Microsoft Dynamics 365 for Project Service Automation við Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="84288-103">Samstilla verkefni verks beint frá Project Service Automation við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="84288-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="84288-104">Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verkefni sem notuð eru til að samstilla verkefni verks beint frá Microsoft Dynamics 365 for Project Service Automation við Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="84288-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="84288-105">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing eru í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="84288-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="84288-106">Ef þú notar Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="84288-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="84288-107">Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="84288-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="84288-108">Samþætting á rauntölum er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="84288-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="84288-109">Gagnaflæði fyrir Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="84288-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="84288-110">Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="84288-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="84288-111">Samþættingarsniðmátið sem er tiltækt með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verkefni verks frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="84288-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="84288-112">Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="84288-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="84288-113">[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="84288-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="84288-114">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="84288-114">Template and task</span></span>

<span data-ttu-id="84288-115">Til að fá aðgang að sniðmátinu, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.</span><span class="sxs-lookup"><span data-stu-id="84288-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="84288-116">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla verkefni verks frá Project Service Automation við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="84288-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="84288-117">**Heiti sniðmátsins í gagnasamþættingu:** Verkefni verks (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="84288-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="84288-118">**Heiti verkefnis í verkinu:** Verkefni verks</span><span class="sxs-lookup"><span data-stu-id="84288-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="84288-119">Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.</span><span class="sxs-lookup"><span data-stu-id="84288-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="84288-120">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="84288-120">Entity set</span></span>

| <span data-ttu-id="84288-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="84288-121">Project Service Automation</span></span> | <span data-ttu-id="84288-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="84288-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="84288-123">Verkefni</span><span class="sxs-lookup"><span data-stu-id="84288-123">Project Tasks</span></span>              | <span data-ttu-id="84288-124">Samþættingareining fyrir verkefni</span><span class="sxs-lookup"><span data-stu-id="84288-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="84288-125">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="84288-125">Entity flow</span></span>

<span data-ttu-id="84288-126">Verksamningum er stjórnað í Project Service Automation og þeir eru samstilltir við Finance and Operations sem verkþættir verks.</span><span class="sxs-lookup"><span data-stu-id="84288-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="84288-127">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="84288-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="84288-128">Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.</span><span class="sxs-lookup"><span data-stu-id="84288-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="84288-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="84288-129">Power Query</span></span>

<span data-ttu-id="84288-130">Þú verður að nota Microsoft Power Query fyrir Excel til að sía gögn ef þetta skilyrði er uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="84288-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="84288-131">Þú ert með sértækar færslur tilfangs í verkefni verks.</span><span class="sxs-lookup"><span data-stu-id="84288-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="84288-132">Ef þú verður að nota Power Query skaltu fylgja þessum leiðbeiningum:</span><span class="sxs-lookup"><span data-stu-id="84288-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="84288-133">Sniðmát fyrir verkefni verks (PSA til Fin and Ops) hefur sjálfgefna síu til að útiloka sértækar færslur tilfangs frá verkefni fyrir verk með því að stilla síuna á **IsLineTask** á **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="84288-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="84288-134">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.</span><span class="sxs-lookup"><span data-stu-id="84288-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="84288-135">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="84288-135">Template mapping in Data integration</span></span>

<span data-ttu-id="84288-136">Eftirfarandi skýringarmynd sýnir dæmi vörpunarsniðmáts í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="84288-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="84288-137">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="84288-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="84288-138">[![Kortlagning sniðmáts](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="84288-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>

