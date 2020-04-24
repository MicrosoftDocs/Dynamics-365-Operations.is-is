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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a64817f140d8a2302b3b2c2d1e55de103a5bb36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209698"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="98a35-103">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="98a35-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98a35-104">Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.</span><span class="sxs-lookup"><span data-stu-id="98a35-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="98a35-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="98a35-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="98a35-106">Setja upp Áætlunarflokk innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="98a35-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="98a35-107">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="98a35-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="98a35-108">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="98a35-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="98a35-109">Til dæmis, sía svæðið Heiti með virði '10'.</span><span class="sxs-lookup"><span data-stu-id="98a35-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="98a35-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="98a35-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="98a35-111">Smellið á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="98a35-111">Click **Delete**.</span></span> <span data-ttu-id="98a35-112">Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="98a35-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="98a35-113">Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.</span><span class="sxs-lookup"><span data-stu-id="98a35-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="98a35-114">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="98a35-114">Click **Yes**.</span></span>
6. <span data-ttu-id="98a35-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="98a35-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="98a35-116">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="98a35-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="98a35-117">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Vinnusvæði > Aðaláætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="98a35-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="98a35-118">Smelltu á **Aðaláætlanagerð innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="98a35-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="98a35-119">Í reitnum **Fjárhagsáætlunarflokkur innan samstæðu** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="98a35-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="98a35-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="98a35-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="98a35-121">Veldu áætlunarflokk innan samstæðu 10.</span><span class="sxs-lookup"><span data-stu-id="98a35-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="98a35-122">Í reitnum **Fjöldi áætlaðra ítrekana innan samstæðu** skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="98a35-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="98a35-123">Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi.</span><span class="sxs-lookup"><span data-stu-id="98a35-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="98a35-124">Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum.</span><span class="sxs-lookup"><span data-stu-id="98a35-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="98a35-125">Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF).</span><span class="sxs-lookup"><span data-stu-id="98a35-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="98a35-126">Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="98a35-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="98a35-127">Í reitnum **Fyrsta ítrekun** skal velja „Endurgerð“.</span><span class="sxs-lookup"><span data-stu-id="98a35-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="98a35-128">Í reitnum **Síðari ítrekanir** skal velja „Endurgerð“.</span><span class="sxs-lookup"><span data-stu-id="98a35-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="98a35-129">Í reitinn **Fjöldi þráða** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="98a35-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="98a35-130">Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="98a35-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="98a35-131">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="98a35-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="98a35-132">Skoða niðurstaða áætlunar.</span><span class="sxs-lookup"><span data-stu-id="98a35-132">View the result of the plan</span></span>
1. <span data-ttu-id="98a35-133">Í reitnum **Áætlun** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="98a35-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="98a35-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="98a35-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="98a35-135">Smelltu á tengil StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="98a35-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="98a35-136">Þú þarft að vera í fyrirtæki USMF.</span><span class="sxs-lookup"><span data-stu-id="98a35-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="98a35-137">Smelltu á **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="98a35-137">Click **Planned orders**.</span></span>

