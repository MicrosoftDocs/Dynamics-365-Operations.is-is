--- 
title: "Reikna afskriftir eigna milli lögaðila"
description: "Þessi aðferð sýnir hvernig skal setja upp og keyra afskriftarferlið fyrir marga lögaðila."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77df61bd85d3c296e44d3a2cfb0fce8b16eaaf9f
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="cac8b-103">Reikna afskriftir eigna milli lögaðila</span><span class="sxs-lookup"><span data-stu-id="cac8b-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cac8b-104">Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi.</span><span class="sxs-lookup"><span data-stu-id="cac8b-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="cac8b-105">Þessi aðferð sýnir hvernig skal setja upp og keyra ferlið fyrir marga lögaðila.</span><span class="sxs-lookup"><span data-stu-id="cac8b-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="cac8b-106">Það notar hlutverk Bókhaldara.</span><span class="sxs-lookup"><span data-stu-id="cac8b-106">It uses the accountant role.</span></span>  

<span data-ttu-id="cac8b-107">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="cac8b-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="cac8b-108">Skref (16) Undirverkefni: Setja upp færslubókakeyrslu afskrifta á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="cac8b-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="cac8b-109">Í fyrsta lagi verður þú að setja upp færslubækurnar sem nota í keyrslu afskrifta milli fyrirtækja hjá sérhverjum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="cac8b-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="cac8b-110">Fara í Eignir > Uppsetning > Færibreytur eigna.</span><span class="sxs-lookup"><span data-stu-id="cac8b-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="cac8b-111">Útvíkka eignatillagnahlutann.</span><span class="sxs-lookup"><span data-stu-id="cac8b-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="cac8b-112">Búðu til skrá með færslubókarheitinu sem á að nota fyrir hvert bókunarlag í lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="cac8b-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="cac8b-113">Ef bækur bóka ekki í fjárhag, ætti að velja bókunarlagið Engin með tengdu færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="cac8b-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="cac8b-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="cac8b-114">Click Add.</span></span> 
4. <span data-ttu-id="cac8b-115">Sláið inn eða veldu gildi í reitnum bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="cac8b-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="cac8b-116">Sláið inn eða veljið gildi í reitnum heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="cac8b-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="cac8b-117">Endurtaka uppsetning færslubókar á síðunni Færibreytur eigna fyrir hverjum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="cac8b-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="cac8b-118">Undirverkefni: Reikna út afskriftir</span><span class="sxs-lookup"><span data-stu-id="cac8b-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="cac8b-119">Notaðu síðuna Stofna afskriftartillögu til að hefja afskriftakeyrslu þína á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="cac8b-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="cac8b-120">Fara í Eignir > Færslubókarfærslur > Stofna afskriftartillögu.</span><span class="sxs-lookup"><span data-stu-id="cac8b-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="cac8b-121">Sláið inn eða veldu gildi í reitnum bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="cac8b-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="cac8b-122">Færslubókarnafnið mun verða sjálfgefið úr Færibreytum eigna.</span><span class="sxs-lookup"><span data-stu-id="cac8b-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="cac8b-123">Því er hægt að breyta hér fyrir núgildandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="cac8b-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="cac8b-124">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="cac8b-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="cac8b-125">Veljið lögaðilana sem á að hafa með í afskriftarkeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="cac8b-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="cac8b-126">Aðeins lögaðilar með uppsettar færslubækur fyrir Eignatillögur á síðunni Færibreytur eigna verða sýndir á listanum.</span><span class="sxs-lookup"><span data-stu-id="cac8b-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="cac8b-127">Þegar Bóka færslubækur valkosturinn er virkjaður, mun hann sjálfkrafa bóka færslubækur afskriftar þegar þær eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="cac8b-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="cac8b-128">Þegar hann er ekki valinn, verða færslubækur búnar til en ekki bókaðar, svo þú getir skoðað upplýsingarnar fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="cac8b-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="cac8b-129">Veljið Já í reitnum bóka færslubækur.</span><span class="sxs-lookup"><span data-stu-id="cac8b-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="cac8b-130">Síureitir ná yfir allar eignir, hópa og bækur fyrir lögaðila sem valdir eru fyrir þessa afskriftakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="cac8b-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="cac8b-131">Runuvinnsluvalkosturinn er virkjaður að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="cac8b-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="cac8b-132">Þegar þessi valkostur er virkjaður, mun stofnun og bókun færslubókar afskrifta keyrast í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="cac8b-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="cac8b-133">Smella skal Stofna færslubók.</span><span class="sxs-lookup"><span data-stu-id="cac8b-133">Click Create journal.</span></span> 
10. <span data-ttu-id="cac8b-134">Þú verður að skoða færslubækur afskrifta sem eru búnar til í viðkomandi lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="cac8b-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="cac8b-135">Fara í Eignir >°Færslubókarfærslur°> Eignabók.</span><span class="sxs-lookup"><span data-stu-id="cac8b-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

