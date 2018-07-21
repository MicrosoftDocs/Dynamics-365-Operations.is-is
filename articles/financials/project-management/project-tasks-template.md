---
title: "Samstilla verkefni verks frá Project Service Automation"
description: "Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verk sem notuð eru til að samstilla verkefni verks beint úr Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: is-is
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="0a0f5-103">Samstilla verkefni verks frá Project Service Automation beint við verkþætti verks í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a0f5-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="0a0f5-104">Þetta efnisatriði fjallar um sniðmátið og undirliggjandi verk sem notuð eru til að samstilla verkefni verks beint úr Microsoft Dynamics 365 for Project Service Automation við Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="0a0f5-105">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="0a0f5-106">Gagnaflæði fyrir Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a0f5-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="0a0f5-107">Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="0a0f5-108">Samþættingarsniðmátið sem er tiltækt með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verkefni verks frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0a0f5-109">Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="0a0f5-110">[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="0a0f5-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="0a0f5-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="0a0f5-111">Template and task</span></span>

<span data-ttu-id="0a0f5-112">Til að fá aðgang að sniðmátinu, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="0a0f5-113">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla verkefni verks frá Project Service Automation við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="0a0f5-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="0a0f5-114">-**Heiti sniðmátsins í gagnasamþættingu:** Verkefni verks (PSA til Fin and Ops) -**Heiti verkefnis í verkinu:** Verkefni verks</span><span class="sxs-lookup"><span data-stu-id="0a0f5-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="0a0f5-115">Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="0a0f5-116">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="0a0f5-116">Entity set</span></span>

|<span data-ttu-id="0a0f5-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0a0f5-117">Project Service Automation</span></span>               | <span data-ttu-id="0a0f5-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a0f5-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="0a0f5-119">Verkefni</span><span class="sxs-lookup"><span data-stu-id="0a0f5-119">Project Tasks</span></span>                           | <span data-ttu-id="0a0f5-120">Samþættingareining fyrir verkefni.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="0a0f5-121">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="0a0f5-121">Entity flow</span></span>

<span data-ttu-id="0a0f5-122">Verksamningum er stjórnað í Project Service Automation og þeir eru samstilltir við Finance and Operations sem verkþættir verks.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="0a0f5-123">Skilyrði og vörpunaruppsetning</span><span class="sxs-lookup"><span data-stu-id="0a0f5-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="0a0f5-124">Áður en samstilling verksamninga getur átt sér stað verður þú að samstilla verksamninga og verk.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="0a0f5-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="0a0f5-125">Power Query</span></span>

<span data-ttu-id="0a0f5-126">Þú verður að nota Microsoft Power Query til að sía gögn ef þessi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="0a0f5-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="0a0f5-127">Þú hefur sértækar færslur tilfangs innan verkefnis á verki.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="0a0f5-128">Ef þú verður að nota Power Query skaltu fylgja þessum leiðbeiningum:</span><span class="sxs-lookup"><span data-stu-id="0a0f5-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="0a0f5-129">Sniðmát fyrir verkefni verks (PSA til Fin and Ops) hefur sjálfgefna síu til að útiloka sértækar færslur tilfangs innan verkefnis fyrir verk með því að stilla síuna á **IsLineTask** á **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="0a0f5-130">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0a0f5-131">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="0a0f5-131">Template mapping in Data integration</span></span>

<span data-ttu-id="0a0f5-132">Eftirfarandi skýringarmynd sýnir dæmi vörpunarsniðmáts í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="0a0f5-133">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a0f5-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="0a0f5-134">[![Kortlagning sniðmáts](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="0a0f5-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


