---
title: Stofna nýtt verk
description: Þetta efnisatriði gefur upplýsingar um hvernig á að búa til nýtt verk.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760573"
---
# <a name="create-a-new-project"></a><span data-ttu-id="157c4-103">Stofna nýtt verk</span><span class="sxs-lookup"><span data-stu-id="157c4-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="157c4-104">Ljúkið eftirfarandi skrefum til að stofna nýtt verk.</span><span class="sxs-lookup"><span data-stu-id="157c4-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="157c4-105">Á **Verkefnastjórnun** skal velja **Nýtt verk** og færa eftirfarandi gildi inn:</span><span class="sxs-lookup"><span data-stu-id="157c4-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="157c4-106">**Gerð verks:** Tími og efni</span><span class="sxs-lookup"><span data-stu-id="157c4-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="157c4-107">**Verkheiti:** XYZ Uppfærsla þrep 2</span><span class="sxs-lookup"><span data-stu-id="157c4-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="157c4-108">**Verkflokkur:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="157c4-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="157c4-109">**Auðkenni verksamnings:** 00000002</span><span class="sxs-lookup"><span data-stu-id="157c4-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="157c4-110">Velja **Stofna verk**.</span><span class="sxs-lookup"><span data-stu-id="157c4-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="157c4-111">Úthluta tilfangi á verk</span><span class="sxs-lookup"><span data-stu-id="157c4-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="157c4-112">Á síðunni **Starfskraftar** í listanum **Starfskraftar**, skal velja skrá starfskrafts sem hefur áður verið sett upp hæfni fyrir og opna starfskrafts.</span><span class="sxs-lookup"><span data-stu-id="157c4-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="157c4-113">Á Aðgerðarrúðunni, á flipanum **Verk** í flokkinum **Uppsetning** veljið **Úthluta verkum**.</span><span class="sxs-lookup"><span data-stu-id="157c4-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="157c4-114">Á **Úthlutanir tilfanga fyrir villuleit í verki** síðunni á **Verk** flipanum í **Bæta verki við valin verk** reitnum skal sía eftir **XYZ Uppfærsla þrep 2** verki.</span><span class="sxs-lookup"><span data-stu-id="157c4-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="157c4-115">Í rúðunni **Eftirstandandi verk**, veljið verk og smellið síðan á örvarhnappur til að bæta því við í **Valin verk** rúðunni.</span><span class="sxs-lookup"><span data-stu-id="157c4-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="157c4-116">Einnig er hægt að úthluta tegundum fyrir tilföng eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="157c4-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="157c4-117">Gerð tegundar er annað hvort **Kostnaður** eða **Tekjur**.</span><span class="sxs-lookup"><span data-stu-id="157c4-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="157c4-118">Gerð tegundar er ákvörðuð af fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="157c4-118">The category type is determined by your organization.</span></span> <span data-ttu-id="157c4-119">Ef engin tegund er fyrir tilfönginmun Finance fletta upp sjálfgefinni tegund á verð á klukkustund fyrir kostnað og tekjur.</span><span class="sxs-lookup"><span data-stu-id="157c4-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="157c4-120">Setja upp verk tilfanga og einkenni verks</span><span class="sxs-lookup"><span data-stu-id="157c4-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="157c4-121">Verkefnastjóri getur notað aðgerðir verktilfanga til að stofna hlutverk sem krafist er fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="157c4-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="157c4-122">Hægt er að nota hlutverk þegar staðfest tilföng eru enn óþekkt við frátekt tilfanga.</span><span class="sxs-lookup"><span data-stu-id="157c4-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="157c4-123">Hægt er að taka hlutverk tímabundið frá sem áætluð tilföng, svo hægt sé að halda áfram verkáætlun.</span><span class="sxs-lookup"><span data-stu-id="157c4-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="157c4-124">[![Dæmi um hlutverk](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="157c4-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="157c4-125">**Aðstæður:** Contoso var ráðinn til að ljúka við Tíma- og efnisverk sem hefur samþykkta skipulagsskrá verks.</span><span class="sxs-lookup"><span data-stu-id="157c4-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="157c4-126">Undirverkefnastjóri er enn að ljúka við umfang verksins.</span><span class="sxs-lookup"><span data-stu-id="157c4-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="157c4-127">Tilfangastjórnandi er sem stendur að auðkenna tiltekin tilföng sem eru frátekin til að vinna í hinu nýja verki.</span><span class="sxs-lookup"><span data-stu-id="157c4-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="157c4-128">Vegna mikilvægis verkefnisins bað kostunaraðili verksins um Yfirverkefnastjóri í einu hlutverki.</span><span class="sxs-lookup"><span data-stu-id="157c4-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="157c4-129">Stjórnandi tilfanga verður að fá nýtt tilfang og skilgreinir hlutverkið í kerfinu ef undirverkefnastjóri krefst tilfangaupplýsingar meðan á verkáætlun stendur.</span><span class="sxs-lookup"><span data-stu-id="157c4-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="157c4-130">Eftirfarandi skref sýna hvernig stjórnandi tilfanga getur sett upp hlutverkið Yfirverkefnastjóri og tengt eiginleika tilfanga við það.</span><span class="sxs-lookup"><span data-stu-id="157c4-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="157c4-131">Síðar er hægt að nota hlutverkið til að leita að lausum tilföngum sem samsvara áskildri hæfni tilfangsins.</span><span class="sxs-lookup"><span data-stu-id="157c4-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="157c4-132">'A **Uppsetning hlutverka** síðunni skal velja **Nýtt** og færa eftirfarandi gildi inn:</span><span class="sxs-lookup"><span data-stu-id="157c4-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="157c4-133">**Kenni hlutverks:** Yfirverkefnastjóri</span><span class="sxs-lookup"><span data-stu-id="157c4-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="157c4-134">**Lýsing:** Yfirverkefnastjóri</span><span class="sxs-lookup"><span data-stu-id="157c4-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="157c4-135">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="157c4-135">Select **Create**.</span></span>
3. <span data-ttu-id="157c4-136">Velja skal hlutverkið **Yfirverkefnastjóri** og veljið svo **Skilgreina einkenni**.</span><span class="sxs-lookup"><span data-stu-id="157c4-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="157c4-137">Í reitnum **Gerð einkenna** skal velja **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="157c4-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="157c4-138">Í reitnum **Tiltæk einkenni** skal færa inn færnina sem verið er að leita að.</span><span class="sxs-lookup"><span data-stu-id="157c4-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="157c4-139">Í reitnum **Gerð einkenna** skal velja **Réttindi**.</span><span class="sxs-lookup"><span data-stu-id="157c4-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="157c4-140">Í reitnum **Tiltæk einkenni** skal færa inn tegund réttinda sem verið er að leita að.</span><span class="sxs-lookup"><span data-stu-id="157c4-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="157c4-141">Úthlutið verktilföngum á verk</span><span class="sxs-lookup"><span data-stu-id="157c4-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="157c4-142">Á **Öll verk** síðunni skal velja verkið **XYZ Uppfærsla þrep 2**.</span><span class="sxs-lookup"><span data-stu-id="157c4-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="157c4-143">Á flipanum **Verkhópur og áætlun** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="157c4-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="157c4-144">Á svæðinu **Hlutverk**, veljið **Meðlimur**.</span><span class="sxs-lookup"><span data-stu-id="157c4-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="157c4-145">Veljið **Bóka úr dagatali**.</span><span class="sxs-lookup"><span data-stu-id="157c4-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="157c4-146">Á síðunni **Forði til ráðstöfunar** er valið **Skoða stillingar**.</span><span class="sxs-lookup"><span data-stu-id="157c4-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="157c4-147">Á síðunni **Breyta stillingum yfirlits** skal færa inn eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="157c4-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="157c4-148">**Snið fyrir dagsetningabil:** Dagur</span><span class="sxs-lookup"><span data-stu-id="157c4-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="157c4-149">**Birta lýsingar á framboði:** Já</span><span class="sxs-lookup"><span data-stu-id="157c4-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="157c4-150">**Sýna eftirstöðvar afkastagetu:** Já</span><span class="sxs-lookup"><span data-stu-id="157c4-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="157c4-151">Í lista yfir tilföng, velja tilfang.</span><span class="sxs-lookup"><span data-stu-id="157c4-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="157c4-152">Veljið **Bundin bókun** og **Full afkastageta**.</span><span class="sxs-lookup"><span data-stu-id="157c4-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="157c4-153">Tengja tilfang við sjálfgefið hlutverk</span><span class="sxs-lookup"><span data-stu-id="157c4-153">Assign a resource to a default role</span></span>

<span data-ttu-id="157c4-154">Til að aðstoða verkefnastjóra eða tilfangastjórnendur, er hægt að kafa frekar niður á tilföng sem má tengja við verk.</span><span class="sxs-lookup"><span data-stu-id="157c4-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="157c4-155">Hægt er að tengja sjálfgefið hlutverk við fyrirliggjandi tilfang eða nýlega áunnið tilfang.</span><span class="sxs-lookup"><span data-stu-id="157c4-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="157c4-156">Til dæmis þegar Daniel var ráðinn hafði hann reynslu og hæfni til að fylla hlutverk viðskiptagreinis.</span><span class="sxs-lookup"><span data-stu-id="157c4-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="157c4-157">Stjórnandi tilfanga úthlutaði þessu hlutverki sem sjálfgefin hlutverk Daniels í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="157c4-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="157c4-158">Þess vegna bætti stjórnandi tilfanga Daniel við hóp viðskiptagreina sem eru tiltækir til að vinna verk.</span><span class="sxs-lookup"><span data-stu-id="157c4-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="157c4-159">Meðan á frátekningu tilfanga stendur geta verkefnisstjórar síað hlutverkatilföng sem eru tiltæk til að vinna að verkum.</span><span class="sxs-lookup"><span data-stu-id="157c4-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="157c4-160">Þeir geta notað þessar upplýsingar sem eitt skilyrði þegar þeir framkvæma ákvarðanagreiningu um mörg skilyrði við uppfyllingar tilfanga.</span><span class="sxs-lookup"><span data-stu-id="157c4-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="157c4-161">Þeir get líka bætt öðrum eiginleika tilfanga við síuna til að leita að tilföngum sem hafa tiltekna hæfni, menntun og reynslu fyrir tiltekið verk.</span><span class="sxs-lookup"><span data-stu-id="157c4-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="157c4-162">**Dæmi:** Samþykkt verk er hafið og hlutverk Yfirverkefnastjóra var frátekið sem áætluð tilföng í verkáætlunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="157c4-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="157c4-163">Stjórnandi tilfanga hefur nú fengið tilfang til að uppfylla hlutverkið Yfirverkefnastjóri.</span><span class="sxs-lookup"><span data-stu-id="157c4-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="157c4-164">Í síðunni **Tilföng**, veljið **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="157c4-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="157c4-165">Á síðunni **Tilfangahlutverk** síðunni skal velja **Nýt** og færa eftirfarandi gildi inn:</span><span class="sxs-lookup"><span data-stu-id="157c4-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="157c4-166">**Gildistími:** Færið inn núgildandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="157c4-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="157c4-167">**Lok gildistíma:** Færið inn **Aldrei**.</span><span class="sxs-lookup"><span data-stu-id="157c4-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="157c4-168">**Hlutverk:** Sláið inn **Yfirverkefnastjóri**.</span><span class="sxs-lookup"><span data-stu-id="157c4-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="157c4-169">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="157c4-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="157c4-170">Á flipanum **Hæfni**, bæta við **ProjectMgmt** hæfni og **PMP** réttindum.</span><span class="sxs-lookup"><span data-stu-id="157c4-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
