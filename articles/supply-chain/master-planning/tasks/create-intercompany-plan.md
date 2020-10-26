---
title: Búa til áætlun innan samstæðu
description: Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978274"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="84d24-103">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="84d24-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84d24-104">Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.</span><span class="sxs-lookup"><span data-stu-id="84d24-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="84d24-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="84d24-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="84d24-106">Setja upp Áætlunarflokk innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="84d24-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="84d24-107">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="84d24-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="84d24-108">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="84d24-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="84d24-109">Til dæmis, sía svæðið Heiti með virði '10'.</span><span class="sxs-lookup"><span data-stu-id="84d24-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="84d24-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="84d24-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="84d24-111">Smellið á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="84d24-111">Click **Delete**.</span></span> <span data-ttu-id="84d24-112">Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="84d24-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="84d24-113">Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.</span><span class="sxs-lookup"><span data-stu-id="84d24-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="84d24-114">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="84d24-114">Click **Yes**.</span></span>
6. <span data-ttu-id="84d24-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="84d24-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="84d24-116">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="84d24-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="84d24-117">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Vinnusvæði > Aðaláætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="84d24-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="84d24-118">Smelltu á **Aðaláætlanagerð innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="84d24-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="84d24-119">Í reitnum **Fjárhagsáætlunarflokkur innan samstæðu** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="84d24-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="84d24-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="84d24-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="84d24-121">Veldu áætlunarflokk innan samstæðu 10.</span><span class="sxs-lookup"><span data-stu-id="84d24-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="84d24-122">Í reitnum **Fjöldi áætlaðra ítrekana innan samstæðu** skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="84d24-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="84d24-123">Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi.</span><span class="sxs-lookup"><span data-stu-id="84d24-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="84d24-124">Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum.</span><span class="sxs-lookup"><span data-stu-id="84d24-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="84d24-125">Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF).</span><span class="sxs-lookup"><span data-stu-id="84d24-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="84d24-126">Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="84d24-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="84d24-127">Í reitnum **Fyrsta ítrekun** skal velja „Endurgerð“.</span><span class="sxs-lookup"><span data-stu-id="84d24-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="84d24-128">Í reitnum **Síðari ítrekanir** skal velja „Endurgerð“.</span><span class="sxs-lookup"><span data-stu-id="84d24-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="84d24-129">Í reitinn **Fjöldi þráða** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="84d24-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="84d24-130">Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="84d24-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="84d24-131">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="84d24-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="84d24-132">Skoða niðurstaða áætlunar.</span><span class="sxs-lookup"><span data-stu-id="84d24-132">View the result of the plan</span></span>
1. <span data-ttu-id="84d24-133">Í reitnum **Áætlun** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="84d24-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="84d24-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="84d24-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="84d24-135">Smelltu á tengil StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="84d24-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="84d24-136">Þú þarft að vera í fyrirtæki USMF.</span><span class="sxs-lookup"><span data-stu-id="84d24-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="84d24-137">Smelltu á **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="84d24-137">Click **Planned orders**.</span></span>

