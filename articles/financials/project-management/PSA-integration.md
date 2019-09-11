---
title: Yfirlit Project Service Automation
description: Þetta efnisatriði veitir upplýsingar um samþættingarlausn Project Service Automation við Finance and Operations. Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation um Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865629"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="424a7-104">Yfirlit Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="424a7-104">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="424a7-105">Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation í gegnum Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="424a7-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="424a7-106">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verk, verksamninga, verksamningslínur, áfanga verksamningslína, verk verkefna, kostnaðarfærsluflokka, tímaáætlanir og kostnaðaráætlanir frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="424a7-107">Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="424a7-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="424a7-108">Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="424a7-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="424a7-109">Ef þú notar Finance and Operations 7.3.0, verður þú að setja upp KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="424a7-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="424a7-110">Þetta gerir þér kleift að samþætta verk með föstu verði.</span><span class="sxs-lookup"><span data-stu-id="424a7-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="424a7-111">Ef þú notar Finance and Operations 7.3.0 og þú færir þóknunarfærslur yfir frá Project Service Automation verður þú að setja upp KB 4345320 til þess að geta tekið við þessum þóknunum í verkreikningi.</span><span class="sxs-lookup"><span data-stu-id="424a7-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="424a7-112">Ef þú notar Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0, getur þú notað samþættingu verkefnis fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="424a7-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="424a7-113">Ef þú notar Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða síðar, munt þú geta samstillt rauntölur.</span><span class="sxs-lookup"><span data-stu-id="424a7-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="424a7-114">Áður en þú getur samþætt Project Service Automation við Finance and Operations þarftu að stilla samþættingarfæribreytur Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="424a7-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="424a7-115">Nánari upplýsingar er að finna í [samþættingarfæribreytum Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="424a7-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="424a7-116">Þessi samþættingarlausn gerir beina samstillingu í eftirfarandi atburðarásum mögulega:</span><span class="sxs-lookup"><span data-stu-id="424a7-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="424a7-117">Viðhalda verksamningum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-118">Búa til verk í Project Service Automation og samstillta þau beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-119">Viðhalda verksamningslínum í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-120">Viðhalda áföngum verksamningslína í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-121">Viðhalda verkefnum verks í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-122">Viðhalda kostnaðarfærsluflokkum í Finance and Operations og samstilla þá beint frá Finance and Operations við Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="424a7-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="424a7-123">Búa til tímaáætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-124">Búa til kostnaðaráætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="424a7-125">Búa til rauntölur tíma, kostnaðar og þóknunar fyrir verk í Project Service Automation og búa til verkfærslur í færslubók samþættingar fyrir Project Service Automation svo hægt sé að bóka þær í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="424a7-126">Samstilling gagna</span><span class="sxs-lookup"><span data-stu-id="424a7-126">Data synchronization</span></span>

<span data-ttu-id="424a7-127">Eftirfarandi skýringarmynd sýnir hvernig gögn eru samstillt sem hluti af samþættingu milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="424a7-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="424a7-128">Ekki eru öll sniðmát í boði eins og er.</span><span class="sxs-lookup"><span data-stu-id="424a7-128">Not all templates are currently available.</span></span> <span data-ttu-id="424a7-129">Sniðmát verða losuð þegar þau klárast.</span><span class="sxs-lookup"><span data-stu-id="424a7-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="424a7-130">[![Samþætting Project Service Automation við Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="424a7-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="424a7-131">Kerfisskilyrði fyrir Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="424a7-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="424a7-132">Til að nota samþættingarlausn Project Service Automation við Finance and Operations þarftu að setja upp Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 með verkvangsuppfærslu 12 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="424a7-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="424a7-133">Kerfisskilyrði fyrir Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="424a7-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="424a7-134">Til að nota samþættingarlausn Project Service Automation við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="424a7-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="424a7-135">Microsoft Dynamics 365 for Project Service Automation útgáfa 9.0.0.0 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="424a7-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="424a7-136">Prospect to cash lausn fyrir Microsoft Dynamics 365 for Sales, útgáfa 1.14.0.0 (v14) eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="424a7-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="424a7-137">Lausn Project Service Automation to Finance and Operations fyrir Microsoft Dynamics 365 for Project Service Automation útgáfa 1.0.0.0 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="424a7-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="424a7-138">Setja upp samþættingarlausn Project Service Automation við Finance and Operations í tilvikinu þínu af Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="424a7-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="424a7-139">Sækja samþættingarlausn Project Service Automation við Finance and Operations hjá [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) og fylgja leiðbeiningum sem fylgja með lausninni.</span><span class="sxs-lookup"><span data-stu-id="424a7-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
