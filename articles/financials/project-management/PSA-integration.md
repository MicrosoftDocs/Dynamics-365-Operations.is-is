---
title: Project Service Automation
description: "Þessi lausn notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation í gegnum Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="2d5be-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2d5be-103">Project Service Automation</span></span>

<span data-ttu-id="2d5be-104">Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation í gegnum Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="2d5be-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="2d5be-105">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verk, verksamninga, verksamningslínur, áfanga verksamningslína, verk verkefna, kostnaðarfærsluflokka, tímaáætlanir og kostnaðaráætlanir frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="2d5be-106">Ef þú notar Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, verður þú að setja upp KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="2d5be-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="2d5be-107">Þetta gerir þér kleift að samþætta verk með föstu verði.</span><span class="sxs-lookup"><span data-stu-id="2d5be-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="2d5be-108">Ef þú notar Dynamics 365 for Finance and Operations útgáfu 8.0, getur þú notað samþættingu verkefna fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="2d5be-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="2d5be-109">Ef þú notar Dynamics 365 for Finance and Operations útgáfu 8.0.1, munt þú geta samstillt rauntölur.</span><span class="sxs-lookup"><span data-stu-id="2d5be-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="2d5be-110">Ef þú notar Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="2d5be-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="2d5be-111">Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="2d5be-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="2d5be-112">Áður en þú getur samþætt Project Service Automation við Finance and Operations þarftu að stilla samþættingarfæribreytur Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2d5be-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="2d5be-113">Nánari upplýsingar er að finna í samþættingarfæribreytum Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2d5be-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="2d5be-114">Þessi samþættingarlausn gerir beina samstillingu í eftirfarandi atburðarásum mögulega:</span><span class="sxs-lookup"><span data-stu-id="2d5be-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="2d5be-115">Viðhalda verksamningum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="2d5be-116">Búa til verk í Project Service Automation og samstillta þau beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="2d5be-117">Viðhalda verksamningslínum í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="2d5be-118">Viðhalda áföngum verksamningslína í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="2d5be-119">Viðhalda verkefnum verks í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="2d5be-120">Viðhalda kostnaðarfærsluflokkum í Finance and Operations og samstilla þá beint frá Finance and Operations við Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2d5be-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="2d5be-121">Búa til tímaáætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="2d5be-122">Búa til kostnaðaráætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="2d5be-123">Samstilling gagna</span><span class="sxs-lookup"><span data-stu-id="2d5be-123">Data synchronization</span></span>
<span data-ttu-id="2d5be-124">Eftirfarandi skýringarmynd sýnir hvernig gögn eru samstillt sem hluti af samþættingu milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2d5be-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="2d5be-125">Ekki eru öll sniðmát í boði eins og er.</span><span class="sxs-lookup"><span data-stu-id="2d5be-125">Not all templates are currently available.</span></span> <span data-ttu-id="2d5be-126">Sniðmát verða losuð þegar þau klárast.</span><span class="sxs-lookup"><span data-stu-id="2d5be-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="2d5be-127">[![Samþætting Project Service Automation við Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="2d5be-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="2d5be-128">Kerfisskilyrði fyrir Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d5be-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="2d5be-129">Til að nota samþættingarlausn Project Service Automation við Finance and Operations þarftu að setja upp Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 með verkvangsuppfærslu 12 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="2d5be-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="2d5be-130">Kerfisskilyrði fyrir Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2d5be-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="2d5be-131">Til að nota samþættingarlausn Project Service Automation við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2d5be-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="2d5be-132">Microsoft Dynamics 365 for Project Service Automation útgáfa 9.0.0.0 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="2d5be-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="2d5be-133">Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.14.0.0 (v14) eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="2d5be-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="2d5be-134">Lausn Project Service Automation to Operations fyrir Dynamics 365 for Project Service Automation útgáfa 1.0.0.0 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="2d5be-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="2d5be-135">Setja upp samþættingarlausn Project Service Automation við Finance and Operations í tilvikinu þínu af Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2d5be-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



