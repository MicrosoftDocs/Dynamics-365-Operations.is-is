---
title: Stofna lögaðila
description: Þetta efnisatriði lýsir því hvernig á að stofna lögaðila í Microsoft Dynamics 365 Commerce, sem þarf að búa til og skilgreina áður en rásir eru stofnaðar.
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
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478213"
---
# <a name="create-legal-entities"></a><span data-ttu-id="668c3-103">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="668c3-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="668c3-104">Þetta efnisatriði lýsir því hvernig á að stofna lögaðila í Microsoft Dynamics 365 Commerce, sem þarf að búa til og skilgreina áður en rásir eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="668c3-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="668c3-105">Lögaðili er fyrirtæki sem hefur skráð ögfest lagalega uppbyggingu.</span><span class="sxs-lookup"><span data-stu-id="668c3-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="668c3-106">Lögaðila er hægt að færa inn í samninga og eru þeir krafnir um að útbúa yfirlit sem segir til um frammistöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="668c3-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="668c3-107">Fyrirtæki er lögaðila.</span><span class="sxs-lookup"><span data-stu-id="668c3-107">A company is a type of legal entity.</span></span> <span data-ttu-id="668c3-108">Eins og stendur eru fyrirtæki aðeins ein tegund af lögaðila sem þú getur búið til, og sérhver lögaðili tengist auðkenni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="668c3-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="668c3-109">Þessi tenging er til staðar þar sem sum virk svæði í forritinu nota fyrirtækjakenni eða *DataAreaId* í gagnalíkönum sínum.</span><span class="sxs-lookup"><span data-stu-id="668c3-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="668c3-110">Í þessum virku svæðum eru fyrirtæki notuð sem mörk fyrir öryggi gagna.</span><span class="sxs-lookup"><span data-stu-id="668c3-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="668c3-111">Notendur geta nálgast gögn aðeins fyrir fyrirtæki sem eru skráðir inn í.</span><span class="sxs-lookup"><span data-stu-id="668c3-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="668c3-112">Þegar þú stofnar rás verður þú að tilgreina hvaða lögaðila þessi rás tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="668c3-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="668c3-113">Stofna nýjan lögaðila</span><span class="sxs-lookup"><span data-stu-id="668c3-113">Create a new legal entity</span></span>

<span data-ttu-id="668c3-114">Til að stofna nýjan lögaðila í Dynamics 365 Commerce  skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="668c3-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="668c3-115">Í yfirlitsglugganum ferðu í **Einingar \> Uppsetning höfuðstöðva \> Lögaðilar**.</span><span class="sxs-lookup"><span data-stu-id="668c3-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="668c3-116">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="668c3-116">On the action pane, select **New**.</span></span> <span data-ttu-id="668c3-117">Glugginn **Nýr lögaðili** birtist til hægri.</span><span class="sxs-lookup"><span data-stu-id="668c3-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="668c3-118">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="668c3-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="668c3-119">Í reitinn **Fyrirtæki** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="668c3-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="668c3-120">Í reitinn **Land/svæði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="668c3-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="668c3-121">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="668c3-121">Select **OK**.</span></span> 

   ![Stofnun lögaðila](media/legal-entities.png)

1. <span data-ttu-id="668c3-123">Í kaflanum **Almennt** gefurðu upp eftirfarandi almennar upplýsingar um lögaðilann:</span><span class="sxs-lookup"><span data-stu-id="668c3-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="668c3-124">Færa skal inn leitarheiti, ef krafist er leitarheitis.</span><span class="sxs-lookup"><span data-stu-id="668c3-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="668c3-125">Leitarheiti er annað nafn sem hægt er að nota til að leita að þessum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="668c3-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="668c3-126">Veljið hvort þessi lögaðili er notaður sem samstæðufyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="668c3-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="668c3-127">Veljið hvort þessi lögaðili er notaður sem losunarfyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="668c3-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="668c3-128">Veldu **sjálfgefið tungumál** fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="668c3-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="668c3-129">Veljið **tímabelti** fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="668c3-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="668c3-130">Í hlutanum **Aðsetur** velurðu **Breyta** til að færa inn upplýsingar um aðsetur, til dæmis götunafn og götunúmer, póstnúmer og borg.</span><span class="sxs-lookup"><span data-stu-id="668c3-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="668c3-131">Í hlutanum **Tengslaupplýsingar** skal færa inn upplýsingar um aðferðir samskipta, svo sem tölvupósta, vefslóðir og símanúmer.</span><span class="sxs-lookup"><span data-stu-id="668c3-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="668c3-132">Í hlutanum **Lögboðin skýrslugerð** skal færa inn skráningarnúmerin sem eru notuð fyrir lögboðna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="668c3-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="668c3-133">Í hlutanum **Skráningarnúmer** skaltu slá inn allar upplýsingar sem lögaðilinn krefst.</span><span class="sxs-lookup"><span data-stu-id="668c3-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="668c3-134">Í hlutanum **Bankareikningsupplýsingar** skal slá inn bankareikninga og leiðarnúmer fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="668c3-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="668c3-135">Í hlutanum **Erlend viðskipti og vörustjórnun** skaltu færa sendingarupplýsingar inn fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="668c3-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="668c3-136">Í hlutanum **Númeraröð** er hægt að skoða númeraraðirnar sem tengjast lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="668c3-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="668c3-137">Til að byrja með verður þetta tómt.</span><span class="sxs-lookup"><span data-stu-id="668c3-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="668c3-138">Í hlutanum **Yfirlitsmynd** skaltu skoða eða breyta merki og yfirlitsmynd sem tengjast lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="668c3-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="668c3-139">Í hlutanum **Skattskráning** skal færa inn skráningarnúmerin sem eru notuð til að senda skýrslu til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="668c3-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="668c3-140">Í hlutanum **Skattur 1099** skal færa inn 1099 upplýsingar fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="668c3-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="668c3-141">Í hlutanum **Skattaupplýsingar** færirðu inn skattaupplýsingar fyrir lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="668c3-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="668c3-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="668c3-142">Select **Save**.</span></span>

<span data-ttu-id="668c3-143">Eftirfarandi mynd sýnir upplýsingar um dæmi um lögaðila.</span><span class="sxs-lookup"><span data-stu-id="668c3-143">The following image shows details of an example legal entity.</span></span>

![Almennur hluti lögaðila](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="668c3-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="668c3-145">Additional resources</span></span>

[<span data-ttu-id="668c3-146">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="668c3-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="668c3-147">Skipuleggja fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="668c3-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="668c3-148">Stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="668c3-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="668c3-149">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="668c3-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="668c3-150">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="668c3-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
