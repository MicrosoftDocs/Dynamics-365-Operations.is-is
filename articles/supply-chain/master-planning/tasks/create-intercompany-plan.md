---
title: Búa til áætlun innan samstæðu
description: Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "333738"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="009fe-103">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="009fe-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="009fe-104">Þessi verklýsing sýnir hvernig á að stofna innansamstæðu áætlun.</span><span class="sxs-lookup"><span data-stu-id="009fe-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="009fe-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="009fe-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="009fe-106">Setja upp Áætlunarflokk innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="009fe-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="009fe-107">Fara í Áætlunarflokkar innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="009fe-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="009fe-108">Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="009fe-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="009fe-109">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="009fe-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="009fe-110">Til dæmis, sía svæðið Heiti með virði '10'.</span><span class="sxs-lookup"><span data-stu-id="009fe-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="009fe-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="009fe-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="009fe-112">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="009fe-112">Click Delete.</span></span>
    * <span data-ttu-id="009fe-113">Þetta skref er nauðsynlegt til að stytta áætlunarkeyrslu innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="009fe-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="009fe-114">Áætlanagerð innan samstæðu mun keyra aðaláætlanagerð í öllum fyrirtækjum í áætlunarflokki, frá lægstu röðunarröðinni.</span><span class="sxs-lookup"><span data-stu-id="009fe-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="009fe-115">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="009fe-115">Click Yes.</span></span>
6. <span data-ttu-id="009fe-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="009fe-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="009fe-117">Búa til áætlun innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="009fe-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="009fe-118">Smelltu á samstæðuáætlun</span><span class="sxs-lookup"><span data-stu-id="009fe-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="009fe-119">Þetta er á vinnusvæði aðaláætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="009fe-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="009fe-120">Í reitnum Áætlunarflokkur innan samstæðu áætlunskal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="009fe-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="009fe-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="009fe-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="009fe-122">Veldu áætlunarflokk innan samstæðu 10.</span><span class="sxs-lookup"><span data-stu-id="009fe-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="009fe-123">Í reitnum Fjöldi ítrekana fyrir samstæðuáætlun skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="009fe-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="009fe-124">Áætlunarflokkur innan samstæðu 10 er með tvo meðlimi.</span><span class="sxs-lookup"><span data-stu-id="009fe-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="009fe-125">Til að dreifa seinkanir frá upprunafyrirtæki (USMF) til fyrirtækis viðskiptavinar (DEMF), þarf að keyra innan samstæðu í báðum fyrirtækjunum tvisvar sinnum.</span><span class="sxs-lookup"><span data-stu-id="009fe-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="009fe-126">Fyrsta ítrekun mun dreifa eftirspurninni og auðkenna seinkanir í upprunafyrirtækinu (USMF).</span><span class="sxs-lookup"><span data-stu-id="009fe-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="009fe-127">Önnur ítrekun mun dreifa seinkanir úr USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="009fe-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="009fe-128">Veljið valkost í svæðinu fyrsta ítrekun.</span><span class="sxs-lookup"><span data-stu-id="009fe-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="009fe-129">Í reitnum fyrsta ítrekun skal velja "Endurnýjun".</span><span class="sxs-lookup"><span data-stu-id="009fe-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="009fe-130">Í reitnum síðari ítrekanir skal velja "Endurnýjun".</span><span class="sxs-lookup"><span data-stu-id="009fe-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="009fe-131">Í svæðinu Fjölda þráða skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="009fe-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="009fe-132">Þetta táknar fjölda samhliða þráða sem er nota við áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="009fe-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="009fe-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="009fe-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="009fe-134">Skoða niðurstaða áætlunar.</span><span class="sxs-lookup"><span data-stu-id="009fe-134">View the result of the plan</span></span>
1. <span data-ttu-id="009fe-135">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="009fe-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="009fe-136">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="009fe-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="009fe-137">Smelltu á tengil StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="009fe-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="009fe-138">Þú þarft að vera í fyrirtæki USMF.</span><span class="sxs-lookup"><span data-stu-id="009fe-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="009fe-139">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="009fe-139">Click Planned orders.</span></span>

