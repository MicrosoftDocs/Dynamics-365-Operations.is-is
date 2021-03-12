---
title: Stofna lögaðila
description: Þetta efni lýsir því hvernig á að stofna lögaðila í Microsoft Dynamics 365 Commerce, sem verður að búa til og stilla áður en rásir eru stofnaðar.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9491feb004366a02155225bfb323773e130f3dc9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993604"
---
# <a name="create-legal-entities"></a><span data-ttu-id="d3622-103">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="d3622-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d3622-104">Þetta efni lýsir því hvernig á að stofna lögaðila í Microsoft Dynamics 365 Commerce, sem verður að búa til og stilla áður en rásir eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d3622-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="d3622-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="d3622-105">Overview</span></span>

<span data-ttu-id="d3622-106">Lögaðili er fyrirtæki sem hefur skráð ögfest lagalega uppbyggingu.</span><span class="sxs-lookup"><span data-stu-id="d3622-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="d3622-107">Lögaðila er hægt að færa inn í samninga og eru þeir krafnir um að útbúa yfirlit sem segir til um frammistöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="d3622-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="d3622-108">Fyrirtæki er lögaðila.</span><span class="sxs-lookup"><span data-stu-id="d3622-108">A company is a type of legal entity.</span></span> <span data-ttu-id="d3622-109">Eins og stendur eru fyrirtæki aðeins ein tegund af lögaðila sem þú getur búið til, og sérhver lögaðili tengist auðkenni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="d3622-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="d3622-110">Þessi tenging er til staðar þar sem sum virk svæði í forritinu nota fyrirtækjakenni eða *DataAreaId* í gagnalíkönum sínum.</span><span class="sxs-lookup"><span data-stu-id="d3622-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="d3622-111">Í þessum virku svæðum eru fyrirtæki notuð sem mörk fyrir öryggi gagna.</span><span class="sxs-lookup"><span data-stu-id="d3622-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="d3622-112">Notendur geta nálgast gögn aðeins fyrir fyrirtæki sem eru skráðir inn í.</span><span class="sxs-lookup"><span data-stu-id="d3622-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="d3622-113">Þegar þú stofnar rás verður þú að tilgreina hvaða lögaðila þessi rás tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="d3622-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="d3622-114">Stofna nýjan lögaðila</span><span class="sxs-lookup"><span data-stu-id="d3622-114">Create a new legal entity</span></span>

<span data-ttu-id="d3622-115">Til að stofna nýjan lögaðila í Dynamics 365 Commerce  skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d3622-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d3622-116">Í yfirlitsglugganum ferðu í **Einingar \> Uppsetning höfuðstöðva \> Lögaðilar**.</span><span class="sxs-lookup"><span data-stu-id="d3622-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="d3622-117">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d3622-117">On the action pane, select **New**.</span></span> <span data-ttu-id="d3622-118">Glugginn **Nýr lögaðili** birtist til hægri.</span><span class="sxs-lookup"><span data-stu-id="d3622-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="d3622-119">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d3622-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="d3622-120">Í reitinn **Fyrirtæki** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d3622-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="d3622-121">Í reitinn **Land/svæði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d3622-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="d3622-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d3622-122">Select **OK**.</span></span> 

   ![Stofnun lögaðila](media/legal-entities.png)

1. <span data-ttu-id="d3622-124">Í kaflanum **Almennt** gefurðu upp eftirfarandi almennar upplýsingar um lögaðilann:</span><span class="sxs-lookup"><span data-stu-id="d3622-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="d3622-125">Færa skal inn leitarheiti, ef krafist er leitarheitis.</span><span class="sxs-lookup"><span data-stu-id="d3622-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="d3622-126">Leitarheiti er annað nafn sem hægt er að nota til að leita að þessum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="d3622-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="d3622-127">Veljið hvort þessi lögaðili er notaður sem samstæðufyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="d3622-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="d3622-128">Veljið hvort þessi lögaðili er notaður sem losunarfyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="d3622-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="d3622-129">Veldu **sjálfgefið tungumál** fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="d3622-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="d3622-130">Veljið **tímabelti** fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="d3622-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="d3622-131">Í hlutanum **Aðsetur** velurðu **Breyta** til að færa inn upplýsingar um aðsetur, til dæmis götunafn og götunúmer, póstnúmer og borg.</span><span class="sxs-lookup"><span data-stu-id="d3622-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="d3622-132">Í hlutanum **Tengslaupplýsingar** skal færa inn upplýsingar um aðferðir samskipta, svo sem tölvupósta, vefslóðir og símanúmer.</span><span class="sxs-lookup"><span data-stu-id="d3622-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="d3622-133">Í hlutanum **Lögboðin skýrslugerð** skal færa inn skráningarnúmerin sem eru notuð fyrir lögboðna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d3622-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="d3622-134">Í hlutanum **Skráningarnúmer** skaltu slá inn allar upplýsingar sem lögaðilinn krefst.</span><span class="sxs-lookup"><span data-stu-id="d3622-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="d3622-135">Í hlutanum **Bankareikningsupplýsingar** skal slá inn bankareikninga og leiðarnúmer fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="d3622-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="d3622-136">Í hlutanum **Erlend viðskipti og vörustjórnun** skaltu færa sendingarupplýsingar inn fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="d3622-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="d3622-137">Í hlutanum **Númeraröð** er hægt að skoða númeraraðirnar sem tengjast lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="d3622-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="d3622-138">Til að byrja með verður þetta tómt.</span><span class="sxs-lookup"><span data-stu-id="d3622-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="d3622-139">Í hlutanum **Yfirlitsmynd** skaltu skoða eða breyta merki og yfirlitsmynd sem tengjast lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="d3622-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="d3622-140">Í hlutanum **Skattskráning** skal færa inn skráningarnúmerin sem eru notuð til að senda skýrslu til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="d3622-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="d3622-141">Í hlutanum **Skattur 1099** skal færa inn 1099 upplýsingar fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="d3622-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="d3622-142">Í hlutanum **Skattaupplýsingar** færirðu inn skattaupplýsingar fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="d3622-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="d3622-143">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d3622-143">Select **Save**.</span></span>

<span data-ttu-id="d3622-144">Eftirfarandi mynd sýnir upplýsingar um dæmi um lögaðila.</span><span class="sxs-lookup"><span data-stu-id="d3622-144">The following image shows details of an example legal entity.</span></span>

![Almennur hluti lögaðila](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="d3622-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d3622-146">Additional resources</span></span>

[<span data-ttu-id="d3622-147">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="d3622-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d3622-148">Skipuleggja fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="d3622-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d3622-149">Stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="d3622-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="d3622-150">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="d3622-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d3622-151">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="d3622-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
