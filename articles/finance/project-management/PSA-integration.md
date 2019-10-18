---
title: Yfirlit Project Service Automation
description: Í þessu efnisatriði er að finna upplýsingar um samþættingarlausnina Dynamics 365 Project Service Automation til Dynamics 365 Finance.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250554"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="c474d-103">Yfirlit Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c474d-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c474d-104">Samþættingarlausn Project Service Automation við Finance notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Dynamics 365 Finance og Dynamics 365 Project Service Automation í gegnum Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c474d-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="c474d-105">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gerir gögnum kleift að flæða varðandi verk, verksamninga, verksamningslínur, áfanga verksamningslína, verk verkefna, kostnaðarfærsluflokka, tímaáætlanir og kostnaðaráætlanir frá Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c474d-106">Ef þú notar útgáfu 7.3.0, verður þú að setja upp KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="c474d-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="c474d-107">Þetta gerir þér kleift að samþætta verk með föstu verði.</span><span class="sxs-lookup"><span data-stu-id="c474d-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="c474d-108">Ef þú notar útgáfu 7.3.0 og þú færir þóknunarfærslur yfir frá Project Service Automation verður þú að setja upp KB 4345320 til þess að geta tekið við þessum þóknunum í verkreikningi.</span><span class="sxs-lookup"><span data-stu-id="c474d-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="c474d-109">Ef þú notar útgáfu 8.0, getur þú notað samþættingu verkefnis fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="c474d-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="c474d-110">Ef þú notar útgáfu 8.0.1eða síðar, munt þú geta samstillt rauntölur.</span><span class="sxs-lookup"><span data-stu-id="c474d-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="c474d-111">Áður en þú getur samþætt Project Service Automation við Finance þarftu að stilla samþættingarfæribreytur Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c474d-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="c474d-112">Nánari upplýsingar er að finna í [samþættingarfæribreytum Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c474d-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="c474d-113">Þessi samþættingarlausn gerir beina samstillingu í eftirfarandi atburðarásum mögulega:</span><span class="sxs-lookup"><span data-stu-id="c474d-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="c474d-114">Viðhalda verksamningum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-115">Búa til verk í Project Service Automation og samstillta þau beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-116">Viðhalda verksamningslínum í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-117">Viðhalda línuáföngum verksamnings í Project Service Automation og samstilla þá beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-118">Viðhalda verkum í Project Service Automation og samstilla þau beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-119">Viðhalda kostnaðarfærsluflokkum í Finance and Operations og samstilla þá beint frá Finance við Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c474d-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="c474d-120">Búa til tímaáætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-121">Búa til kostnaðaráætlanir verks í Project Service Automation og samstilla þær beint frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c474d-122">Búa til rauntölur tíma, kostnaðar og þóknunar fyrir verk í Project Service Automation og búa til verkfærslur í færslubók samþættingar fyrir Project Service Automation svo hægt sé að bóka þær í Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="c474d-123">Samstilling gagna</span><span class="sxs-lookup"><span data-stu-id="c474d-123">Data synchronization</span></span>

<span data-ttu-id="c474d-124">Eftirfarandi skýringarmynd sýnir hvernig gögn eru samstillt sem hluti af samþættingu milli Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="c474d-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="c474d-125">Ekki eru öll sniðmát í boði eins og er.</span><span class="sxs-lookup"><span data-stu-id="c474d-125">Not all templates are currently available.</span></span> <span data-ttu-id="c474d-126">Sniðmát verða losuð þegar þau klárast.</span><span class="sxs-lookup"><span data-stu-id="c474d-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="c474d-127">[![Samþætting Project Service Automation við Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c474d-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="c474d-128">Kerfisskilyrði fyrir Finance</span><span class="sxs-lookup"><span data-stu-id="c474d-128">System requirements for Finance</span></span>

<span data-ttu-id="c474d-129">Til að nota samþættingarlausn Project Service Automation við Finance þarftu að setja upp Enterprise Edition 7.3 með verkvangsuppfærslu 12 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="c474d-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="c474d-130">Kerfisskilyrði fyrir Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c474d-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="c474d-131">Til að nota samþættingarlausn Project Service Automation við Finance verður að setja upp eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="c474d-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="c474d-132">Dynamics 365 Project Service Automation útgáfa 9.0.0.0 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="c474d-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="c474d-133">Prospect to cash lausn fyrir Dynamics 365 Sales, útgáfa 1.14.0.0 (v14) eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="c474d-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="c474d-134">Lausn Project Service Automation to Finance fyrir Dynamics 365 Project Service Automation útgáfa 1.0.0.0 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="c474d-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="c474d-135">Setja upp samþættingarlausn Project Service Automation við Finance í tilvikinu af Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c474d-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="c474d-136">Sækja samþættingarlausn Project Service Automation við Finance hjá [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) og fylgja leiðbeiningum sem fylgja með lausninni.</span><span class="sxs-lookup"><span data-stu-id="c474d-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
