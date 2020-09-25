---
title: Setja upp verktilföng.
description: Þetta efnisatriði gefur upplýsingar um uppsetningu eða beiðni verktilfanga.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760578"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="2c745-103">Setja upp verktilföng.</span><span class="sxs-lookup"><span data-stu-id="2c745-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c745-104">Þú þarft að setja upp dagatal og tengja það við starfsmann eða starfskraft.</span><span class="sxs-lookup"><span data-stu-id="2c745-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="2c745-105">Dagatalið er notað til að áætla verkið og vinnutíma þeirra tilfanga sem eru frátekin fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="2c745-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="2c745-106">Við uppsetningu dagatals geta verkefnisstjórar framkvæmt sléttun á tilföngum sem hluta af fínstillingu tilfanga.</span><span class="sxs-lookup"><span data-stu-id="2c745-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="2c745-107">Samkvæmt áætlun dagatals geta takmarkanir verið settar á tilföng.</span><span class="sxs-lookup"><span data-stu-id="2c745-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="2c745-108">Hægt er að setja upp dagatal sem á síðunni **Dagatöl**.</span><span class="sxs-lookup"><span data-stu-id="2c745-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="2c745-109">Þegar starfsmaður er settur upp sem tilföng verks er hægt að velja úr starfsmönnum sem vinna í fyrirtækinu þar sem verið er að setja upp tilföng.</span><span class="sxs-lookup"><span data-stu-id="2c745-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="2c745-110">Einnig er hægt að velja starfskraftur úr öðrum fyrirtækjum innan fyrirtækisins þíns.</span><span class="sxs-lookup"><span data-stu-id="2c745-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="2c745-111">Þessir starfskraftar eru þekktir sem samstæðutilföng.</span><span class="sxs-lookup"><span data-stu-id="2c745-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="2c745-112">Eftirfarandi ferli útskýra hvernig setja á upp starfsmanns sem tilföng verks innan fyrirtækisins og hvernig á að setja upp samstæðuverk tilfanga.</span><span class="sxs-lookup"><span data-stu-id="2c745-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="2c745-113">Setja upp starfmann sem verktilfang.</span><span class="sxs-lookup"><span data-stu-id="2c745-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="2c745-114">Á síðunni **Starfsmenn**, í listanum **Starfsfólk**, veljið starfsmann sem verið er að bæta við sem tilfang verks og opnið skrá starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="2c745-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="2c745-115">Á Aðgerðasvæðinu skal velja **Verk** &gt; **Uppsetning** &gt; **Verkuppsetning**.</span><span class="sxs-lookup"><span data-stu-id="2c745-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="2c745-116">Velja skal Dagatal og loka svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="2c745-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="2c745-117">Einnig er hægt að tilgreina sjálfgefið verk fyrir tilföng sem gerð áætlaðs verkefnis.</span><span class="sxs-lookup"><span data-stu-id="2c745-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="2c745-118">Hægt er að nota áætlaðar úthlutanir þegar tilfangastjórnandi eða verkstjóri veit hvaða verk tilfangið verður að vinna að fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="2c745-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="2c745-119">Einnig er hægt að byggja áætlaðar úthlutanir á beiðni kostunaraðila verks eða viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2c745-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="2c745-120">Til að úthluta verki fyrirfram: Á síðunni **Úthluta verkum**, á flipanum **Verk**, á listanum **Eftirstandandi verk** skal velja viðeigandi verk.</span><span class="sxs-lookup"><span data-stu-id="2c745-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="2c745-121">Setja upp samstæðutilföng</span><span class="sxs-lookup"><span data-stu-id="2c745-121">Set up an intercompany resource</span></span>

<span data-ttu-id="2c745-122">Þegar starfsmaður er settur upp sem samstæðutilföng verður að ljúka uppsetningunni í bæði útlánafyrirtækinu og lántökufyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="2c745-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="2c745-123">Í útlánafyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="2c745-123">In the lending company</span></span>

1. <span data-ttu-id="2c745-124">Í Finance skal staðfesta að útlánafyrirtækið sé valið, og ljúka síðan ferlinu hér að framan, „Setja upp starfsmann sem tilfang verks“.</span><span class="sxs-lookup"><span data-stu-id="2c745-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="2c745-125">Á síðunni **Samstæðulyklar** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="2c745-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="2c745-126">Í svæðinu **Kenni lögaðila** skal velja útlánafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="2c745-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="2c745-127">Fyllið út eftirstandandi svæði eftir þörfum og velja svo **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2c745-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="2c745-128">Á síðunni **Innanhússverð** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="2c745-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="2c745-129">Í **Lögaðili sem fær lánað** reitnum skal velja viðkomandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="2c745-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="2c745-130">Til að lána lántökufyrirtækinu aðeins þau tilföng sem voru stofnuð í upphafi þessa hluta í svæðinu **Tilföng** skal velja nafn tilfanganna sem voru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="2c745-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="2c745-131">Til að gera öll tilföng í fyrirtækinu tiltæk lántökufyrirtæki skal skilja svæðið **Tilföng** eftir autt.</span><span class="sxs-lookup"><span data-stu-id="2c745-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="2c745-132">Á **Verkefnastjórnun og bókhaldsfæribreytur** síðunni, á flipanum **Samstæða** Skal stilla **Virkja samstæðuröðun tilfanga og tímablöð** valkostinn á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2c745-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="2c745-133">Í lántökufyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="2c745-133">In the borrowing company</span></span>

- <span data-ttu-id="2c745-134">Á **Tilfangalisti** síðunni skal færa inn heiti tilfangs sem þú stofnaðir í útlánafyrirtækinu til að staðfesta að heitið sé innifalið í tilfangalistalántökufyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="2c745-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="2c745-135">Biðja um verktilföng</span><span class="sxs-lookup"><span data-stu-id="2c745-135">Request project resources</span></span>
<span data-ttu-id="2c745-136">Virknin fyrir röðun verktilfanga styður aðeins stjórnendur tilfanga til að dreifa mönnuðum tilföngum á úttektir eða verk.</span><span class="sxs-lookup"><span data-stu-id="2c745-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="2c745-137">Til að virkja þennan eiginleika skal ljúka eftirfarandi verkum eða að staðfesta að þeim sé lokið:</span><span class="sxs-lookup"><span data-stu-id="2c745-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="2c745-138">Setja upp númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="2c745-138">Set up number sequences.</span></span>
- <span data-ttu-id="2c745-139">Setja upp verkflæði fyrir verkefnastjórnun og bókhald</span><span class="sxs-lookup"><span data-stu-id="2c745-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="2c745-140">Virkja verkflæði tilfangabeiðni.</span><span class="sxs-lookup"><span data-stu-id="2c745-140">Enable resource request workflows.</span></span>

<span data-ttu-id="2c745-141">Eftir að fyrri verkefnum hefur verið lokið er hægt að ljúka eftirfarandi verkefnum eftir þörfum:</span><span class="sxs-lookup"><span data-stu-id="2c745-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="2c745-142">Stofna beiðni tilfanga úr óbundið mönnuðum tilföngum.</span><span class="sxs-lookup"><span data-stu-id="2c745-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="2c745-143">Fylgjast með tilfangabeiðnum.</span><span class="sxs-lookup"><span data-stu-id="2c745-143">Monitor resource requests.</span></span>
- <span data-ttu-id="2c745-144">Uppfylla tilfangabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="2c745-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="2c745-145">Biðja um mönnuð tilföng úr WBS.</span><span class="sxs-lookup"><span data-stu-id="2c745-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="2c745-146">Bóka tilföng á verk án þess að þurfa að biðja um mönnuð tilföng.</span><span class="sxs-lookup"><span data-stu-id="2c745-146">Book resources to a project without having a request for a staffed resource.</span></span>
