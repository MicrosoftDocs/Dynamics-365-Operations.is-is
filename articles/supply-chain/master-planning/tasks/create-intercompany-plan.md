---
title: Búa til áætlun innan samstæðu
description: Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867351"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="32565-103">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="32565-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32565-104">Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.</span><span class="sxs-lookup"><span data-stu-id="32565-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="32565-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="32565-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="32565-106">Setja upp Áætlunarflokk innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="32565-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="32565-107">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="32565-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="32565-108">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="32565-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="32565-109">Til dæmis, sía svæðið Heiti með virði '10'.</span><span class="sxs-lookup"><span data-stu-id="32565-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="32565-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="32565-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="32565-111">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="32565-111">Select **Delete**.</span></span> <span data-ttu-id="32565-112">Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="32565-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="32565-113">Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.</span><span class="sxs-lookup"><span data-stu-id="32565-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="32565-114">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="32565-114">Select **Yes**.</span></span>
6. <span data-ttu-id="32565-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="32565-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="32565-116">Stofna aðaláætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="32565-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="32565-117">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Aðaláætlanagerð > Vinnusvæði > Aðaláætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="32565-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="32565-118">Veljið **Aðaláætlanagerð innan samstæðu**.</span><span class="sxs-lookup"><span data-stu-id="32565-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="32565-119">Í reitnum **Áætlunarflokkur innan samstæðu** skal velja á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="32565-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="32565-120">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="32565-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="32565-121">Veldu áætlunarflokk innan samstæðu 10.</span><span class="sxs-lookup"><span data-stu-id="32565-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="32565-122">Í reitnum **Fjöldi áætlaðra ítrekana innan samstæðu** skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="32565-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="32565-123">Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi.</span><span class="sxs-lookup"><span data-stu-id="32565-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="32565-124">Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum.</span><span class="sxs-lookup"><span data-stu-id="32565-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="32565-125">Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF).</span><span class="sxs-lookup"><span data-stu-id="32565-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="32565-126">Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="32565-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="32565-127">Í reitnum **Fyrsta ítrekun** skal velja „Endurgerð“.</span><span class="sxs-lookup"><span data-stu-id="32565-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="32565-128">Í reitnum **Síðari ítrekanir** skal velja „Endurgerð“.</span><span class="sxs-lookup"><span data-stu-id="32565-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="32565-129">Í reitinn **Fjöldi þráða** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="32565-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="32565-130">Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="32565-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="32565-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="32565-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="32565-132">Skoða niðurstaða áætlunar.</span><span class="sxs-lookup"><span data-stu-id="32565-132">View the result of the plan</span></span>

1. <span data-ttu-id="32565-133">Í reitnum **Áætlun** velurðu fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="32565-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="32565-134">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="32565-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="32565-135">Veljið tengil StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="32565-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="32565-136">Þú þarft að vera í fyrirtæki USMF.</span><span class="sxs-lookup"><span data-stu-id="32565-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="32565-137">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="32565-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]