---
title: Búa til sniðmát ferlis í Attract
description: Þetta efnisatriði gefur upplýsingar um hvernig á að búa til sniðmát ferlis í Attract.
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 2b9cac68093be65584192757229c20b1a1546342
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2019
ms.locfileid: "304839"
---
# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="88dea-103">Búa til sniðmát ferlis í Attract</span><span class="sxs-lookup"><span data-stu-id="88dea-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="88dea-104">*Sniðmát ráðningarferlisins* inniheldur allar aðgerðir sem ætti að vera hluti af ráðningarferli fyrir starf.</span><span class="sxs-lookup"><span data-stu-id="88dea-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="88dea-105">Þetta efni lýsir grunnatriðum sniðmáts ferlis í Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="88dea-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="88dea-106">Það útskýrir einnig hvernig á að búa til sniðmát.</span><span class="sxs-lookup"><span data-stu-id="88dea-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="88dea-107">Sköpun sniðmáts er hluti af Viðbót við alhliða ráðningar fyrir Attract.</span><span class="sxs-lookup"><span data-stu-id="88dea-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="88dea-108">Stjórnun sniðmáts</span><span class="sxs-lookup"><span data-stu-id="88dea-108">Template management</span></span>

<span data-ttu-id="88dea-109">Fyrirtæki geta ákveðið hvort teymismeðlimir eða aðeins stjórnendur geta búið til sniðmát ferlis í Attract.</span><span class="sxs-lookup"><span data-stu-id="88dea-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="88dea-110">Til að stilla stjórnun sniðmáts skaltu fara í **Stjórnendamiðstöðina** \> **Stjórnun sniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="88dea-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="88dea-111">Til að leyfa teymismeðlimum að búa til eigin sniðmát skaltu kveikja á stjórnun sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="88dea-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="88dea-112">Ef þú kveikir ekki á stjórnun sniðmáts geta aðeins stjórnendur búið til sniðmát.</span><span class="sxs-lookup"><span data-stu-id="88dea-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="88dea-113">Sjálfgefið sniðmát</span><span class="sxs-lookup"><span data-stu-id="88dea-113">Default template</span></span>

<span data-ttu-id="88dea-114">Aðeins stjórnendur geta stillt sjálfgefið sniðmát.</span><span class="sxs-lookup"><span data-stu-id="88dea-114">Only admins can set the default template.</span></span> <span data-ttu-id="88dea-115">Sjálfgefið sniðmát er notað ef sniðmát er ekki valið þegar starf er búið til.</span><span class="sxs-lookup"><span data-stu-id="88dea-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="88dea-116">Til að stilla sjálfgefið sniðmát skaltu fara í **Stjórnendamiðstöðina** \> **Stjórnun sniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="88dea-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="88dea-117">Á spjaldinu fyrir sniðmátið sem ætti að vera sjálfgefið sniðmát skaltu velja þrípunktahnappinn (**...**) og veldu síðan **Velja sem sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="88dea-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="88dea-118">Búa til sniðmát ferlis</span><span class="sxs-lookup"><span data-stu-id="88dea-118">Create a process template</span></span>

<span data-ttu-id="88dea-119">Stjórnendur, ráðningaraðilar og mannauðsstjórar geta búið til sniðmát ferlis.</span><span class="sxs-lookup"><span data-stu-id="88dea-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="88dea-120">Sniðmát ferlis samanstendur af *stigum* og *aðgerðum*.</span><span class="sxs-lookup"><span data-stu-id="88dea-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="88dea-121">Stig hópa saman einum eða fleiri aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="88dea-121">Stages group together one or more activities.</span></span> <span data-ttu-id="88dea-122">Sjálfgefið hefur hvert sniðmát ferlis Viðfangs-, Umsóknar- og Tilboðsaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="88dea-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="88dea-123">Stigunum sem innihalda þessar aðgerðir má endurnefna.</span><span class="sxs-lookup"><span data-stu-id="88dea-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="88dea-124">Þú getur bætt fleiri stigum með því að velja **+ Nýtt stig**.</span><span class="sxs-lookup"><span data-stu-id="88dea-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="88dea-125">Þú getur virkjað aðgerðir á stigi annaðhvort með því að draga þá á viðeigandi stig eða með því að tvísmella þá á aðgerðalistanum.</span><span class="sxs-lookup"><span data-stu-id="88dea-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="88dea-126">Heiti stiga eru sýnileg umsækjendurm á **Staða umsóknar** síðu.</span><span class="sxs-lookup"><span data-stu-id="88dea-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="88dea-127">Þú ættir að íhuga þessa staðreynd þegar þú velur nöfn fyrir stig.</span><span class="sxs-lookup"><span data-stu-id="88dea-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="88dea-128">Til að læra meira um aðgerðir, sjá [Ráðningarferli í Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="88dea-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="88dea-129">Fylgdu þessum skrefum til að búa til sniðmát fyrir ráðningarferli.</span><span class="sxs-lookup"><span data-stu-id="88dea-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="88dea-130">Farðu í **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="88dea-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="88dea-131">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="88dea-131">Select **New**.</span></span>
3. <span data-ttu-id="88dea-132">Í **Heiti sniðmáts** reitnum, slá inn heiti fyrir sniðmátið, og þá velja **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="88dea-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="88dea-133">Í **Veldu samþykktarferli** listi, veldu **Sjálfgefið** til að krefjast samþykkis fyrir starf.</span><span class="sxs-lookup"><span data-stu-id="88dea-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="88dea-134">Veldu til að kveikja eða slökkva á viðföngum.</span><span class="sxs-lookup"><span data-stu-id="88dea-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="88dea-135">Valfrjáls: Bæta við eða fjarlægja stig.</span><span class="sxs-lookup"><span data-stu-id="88dea-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="88dea-136">Til að bæta við stigi skaltu velja **+ Nýtt stig**.</span><span class="sxs-lookup"><span data-stu-id="88dea-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="88dea-137">Til að fjarlægja stig skaltu setja bendilinn yfir stigið og veldu síðan ruslakörfuhnappinn sem birtist.</span><span class="sxs-lookup"><span data-stu-id="88dea-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="88dea-138">Ekki er hægt að fjarlægja viðfangs-, umsóknar- og tilboðsstig. en þau geta verið endurnefnd.</span><span class="sxs-lookup"><span data-stu-id="88dea-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="88dea-139">Valfrjáls: Bæta við eða fjarlægja aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="88dea-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="88dea-140">Til að bæta við aðgerð skaltu draga það úr aðgerðalistanum hægra megin við viðeigandi stig.</span><span class="sxs-lookup"><span data-stu-id="88dea-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="88dea-141">Einnig er hægt að tvísmella á aðgerðina og velja síðan stigið til að bæta því við.</span><span class="sxs-lookup"><span data-stu-id="88dea-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="88dea-142">Til að fjarlægja aðgerð skaltu stækka aðgerðina og velja síðan ruslakörfuhnappinn á verkþáttarhausnum.</span><span class="sxs-lookup"><span data-stu-id="88dea-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="88dea-143">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="88dea-143">Select **Save**.</span></span>
