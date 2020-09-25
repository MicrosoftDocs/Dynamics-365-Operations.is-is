---
title: Stofna verkhóp
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að stofna og stjórna verkefnishópum.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760574"
---
# <a name="create-a-project-team"></a><span data-ttu-id="14fcf-103">Stofna verkhóp</span><span class="sxs-lookup"><span data-stu-id="14fcf-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14fcf-104">Til að nota hlutverk sem voru áður sett upp í verkefni verður verkefnastjóri að tengja hlutverk við verkið.</span><span class="sxs-lookup"><span data-stu-id="14fcf-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="14fcf-105">Hægt er að tengja mörg hlutverk við verk.</span><span class="sxs-lookup"><span data-stu-id="14fcf-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="14fcf-106">Til að koma í veg fyrir misskilning eru þessi hlutverk sjálfkrafa merkt við frátekningu.</span><span class="sxs-lookup"><span data-stu-id="14fcf-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="14fcf-107">Til dæmis, ef verkefnastjóri krefst þriggja hugbúnaðarverkfræðinga eru þrjú hlutverk hugbúnaðarverkfræðinga sem eru merktir sem **hugbúnaðarverkfræðingur 1**, **hugbúnaðarverkfræðingur 2** og **hugbúnaðarverkfræðingur 3**, sjálfvirkt mynduð.</span><span class="sxs-lookup"><span data-stu-id="14fcf-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="14fcf-108">Ef einkenni hlutverks hafa áður verið stillt fyrir hlutverkið, eru þau notuð sem sía við leit tilfanga.</span><span class="sxs-lookup"><span data-stu-id="14fcf-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="14fcf-109">Hægt er að bæta frekari eiginleikum við sem þarf til að fínstilla leitina enn frekar.</span><span class="sxs-lookup"><span data-stu-id="14fcf-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="14fcf-110">Einnig er hægt að sérsníða skoðun á stillingum til að gefa betra yfirlit yfir tiltæk tilföng.</span><span class="sxs-lookup"><span data-stu-id="14fcf-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="14fcf-111">Það eru valkostir til að sýna tiltæki eftir klukkustund, daglega, vikulega, mánaðarlega, ársfjórðungslega og árlega.</span><span class="sxs-lookup"><span data-stu-id="14fcf-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="14fcf-112">Það er einnig valkostur að sýna tiltæka og eftirstandandi afkastagetu á tilföng.</span><span class="sxs-lookup"><span data-stu-id="14fcf-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="14fcf-113">Þessi valkostur er gagnlegur fyrir tímastjórnun þegar verið er að meta tiltækan tíma fyrir verkþætti eða tiltæk tilföng.</span><span class="sxs-lookup"><span data-stu-id="14fcf-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="14fcf-114">Verkefnastjórinn getur valið hlutverk á síðunni og, séu tiltæk tilföng sem hentar þörfinni, valið að taka frá tilfang til að fylla hlutverkið.</span><span class="sxs-lookup"><span data-stu-id="14fcf-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="14fcf-115">Athugið að ekki þarf að taka tilföng frá á þessum tíma meðan á áætlunarferli stendur.</span><span class="sxs-lookup"><span data-stu-id="14fcf-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="14fcf-116">Þegar Sundurliðun verkþátta (WBS) er stofnað er hægt að skipta út hlutverk með mönnuðum tilföngum fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="14fcf-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="14fcf-117">Ef hlutverkum er skipt út fyrir mönnuð tilföng í WBS, uppfærir uppsetning tilfanga sjálfkrafa skráningar og röðun í verkhópinn.</span><span class="sxs-lookup"><span data-stu-id="14fcf-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="14fcf-118">[![Verkhópur skráningar sem inniheldur bæði hlutverk og raunveruleg tilföng](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="14fcf-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="14fcf-119">Verkefnastjórinn hefur mismunandi valkosti fyrir bókun tilfanga fyrir verk, eins og **Eftirstöðvar afkastagetu**, **Full afkastageta**, **Hlutfall Afkastagetu**, og **Tilgreina klukkustundir**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="14fcf-120">Hætta má við þessa bókunarvalkosti hvenær sem er ef úthlutun tilfanga breytist.</span><span class="sxs-lookup"><span data-stu-id="14fcf-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="14fcf-121">Til eru tvær gerðir bókunar:</span><span class="sxs-lookup"><span data-stu-id="14fcf-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="14fcf-122">**Bundin bókun** – Frátekning tilfanga var samþykkt og staðfest að vinna í úttekt fyrir tilgreinda tímalengd.</span><span class="sxs-lookup"><span data-stu-id="14fcf-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="14fcf-123">**Óbundin bókun** – Frátekningar á tilföngum var með fyrirvara stillt á að vinna í úttekt fyrir tilgreinda tímalengd.</span><span class="sxs-lookup"><span data-stu-id="14fcf-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="14fcf-124">Notið eftirfarandi aðferðir til þess að stofna verkhóp.</span><span class="sxs-lookup"><span data-stu-id="14fcf-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="14fcf-125">Stofna verkhóp</span><span class="sxs-lookup"><span data-stu-id="14fcf-125">Create a project team</span></span>

1. <span data-ttu-id="14fcf-126">Á listasíðunni **Öll verk** veldu verk og velja svo **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="14fcf-127">Á flipanum **Verkhópur Og áætlun**, á svæðinu **Áætluð lokadagsetning**, færið inn áætlaða upphafsdagsetningu plús einn mánuður.</span><span class="sxs-lookup"><span data-stu-id="14fcf-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="14fcf-128">Til dæmis, ef áætluð upphafsdagsetning er 24. Júní, 2017 (24/06/2017), færa inn **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="14fcf-129">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-129">Select **Add**.</span></span>
4. <span data-ttu-id="14fcf-130">Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="14fcf-131">Veljið **Áskilin hæfni**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="14fcf-132">Á síðunni **Velja eiginleika**, eru þeir eiginleikar sem þú stilltir áður á hlutverk Yfirverkefnastjóra valdir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="14fcf-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="14fcf-133">Veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-133">Select **OK**.</span></span>
7. <span data-ttu-id="14fcf-134">Á síðunni **Bæta hlutverkum við verk**, í svæðinu **Fjöldi tilfanga** skal færa inn **1**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="14fcf-135">Í svæðinu **Tilföng** sýnir uppfletting öll tilföng sem hafa áskilda hæfni.</span><span class="sxs-lookup"><span data-stu-id="14fcf-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="14fcf-136">Velja **Daniel Goldschmidt**, og svo **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="14fcf-137">Á síðunni **Verk** síðunni er valið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="14fcf-138">Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk** veljið **Meðlimur**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="14fcf-139">Í svæðinu **Fjöldi tilfanga** skal slá inn **5**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="14fcf-140">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-140">Select **Create**.</span></span>
12. <span data-ttu-id="14fcf-141">Á síðunni **Verk** er valið **Uppfylla tilföng**.</span><span class="sxs-lookup"><span data-stu-id="14fcf-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="14fcf-142">Fylgjast með verkhópum</span><span class="sxs-lookup"><span data-stu-id="14fcf-142">Monitor project teams</span></span>
1. <span data-ttu-id="14fcf-143">Á síðunni **Öll verk** skal velja **Verkkenni** tengilinn fyrir verkið **XYZ uppfærsla þrep 2** project.</span><span class="sxs-lookup"><span data-stu-id="14fcf-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="14fcf-144">Á flýtiflipanum **Verkhópur og áætlun** sakl ganga úr skugga um að tilföng verks sem eru talin upp séu rétt.</span><span class="sxs-lookup"><span data-stu-id="14fcf-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
