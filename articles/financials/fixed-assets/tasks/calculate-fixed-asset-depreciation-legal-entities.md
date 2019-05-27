---
title: Reikna afskriftir eigna milli lögaðila
description: Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2575354af322827972ffa650e9c732170c5a6eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566544"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="7ba24-103">Reikna afskriftir eigna milli lögaðila</span><span class="sxs-lookup"><span data-stu-id="7ba24-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ba24-104">Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi.</span><span class="sxs-lookup"><span data-stu-id="7ba24-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="7ba24-105">Þessi aðferð sýnir hvernig skal setja upp og keyra ferlið fyrir marga lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7ba24-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="7ba24-106">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7ba24-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="7ba24-107">Setja upp færslubókakeyrslu afskrifta á milli fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="7ba24-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="7ba24-108">Fara í Eignir > Uppsetning > Færibreytur eigna.</span><span class="sxs-lookup"><span data-stu-id="7ba24-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="7ba24-109">Útvíkka eignatillagnahlutann.</span><span class="sxs-lookup"><span data-stu-id="7ba24-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="7ba24-110">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7ba24-110">Click Add.</span></span>
4. <span data-ttu-id="7ba24-111">Sláið inn eða veldu gildi í reitnum bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="7ba24-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="7ba24-112">Sláið inn eða veljið gildi í reitnum heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="7ba24-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="7ba24-113">Endurtaka uppsetning færslubókar á síðunni Færibreytur eigna fyrir hverjum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7ba24-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="7ba24-114">Afskriftarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="7ba24-114">Depreciation run</span></span>
1. <span data-ttu-id="7ba24-115">Fara í Eignir > Færslubókarfærslur > Stofna afskriftartillögu.</span><span class="sxs-lookup"><span data-stu-id="7ba24-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="7ba24-116">Sláið inn eða veldu gildi í reitnum bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="7ba24-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="7ba24-117">Færslubókarnafnið mun verða sjálfgefið úr Færibreytum eigna.</span><span class="sxs-lookup"><span data-stu-id="7ba24-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="7ba24-118">Því er hægt að breyta hér fyrir núgildandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7ba24-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="7ba24-119">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="7ba24-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="7ba24-120">Veljið lögaðilana sem á að hafa með í afskriftarkeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="7ba24-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="7ba24-121">Aðeins lögaðilar með uppsettar færslubækur fyrir Eignatillögur á síðunni Færibreytur eigna verða sýndir á listanum.</span><span class="sxs-lookup"><span data-stu-id="7ba24-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="7ba24-122">Veljið Já í reitnum bóka færslubækur.</span><span class="sxs-lookup"><span data-stu-id="7ba24-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="7ba24-123">Síureitir ná yfir allar eignir, hópa og bækur fyrir lögaðila sem valdir eru fyrir þessa afskriftakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="7ba24-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="7ba24-124">Runuvinnsluvalkosturinn er virkjaður að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="7ba24-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="7ba24-125">Þegar þessi valkostur er virkjaður, mun stofnun og bókun færslubókar afskrifta keyrast í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="7ba24-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="7ba24-126">Smella skal Stofna færslubók.</span><span class="sxs-lookup"><span data-stu-id="7ba24-126">Click Create journal.</span></span>
6. <span data-ttu-id="7ba24-127">Fara í Eignir >°Færslubókarfærslur°> Eignabók.</span><span class="sxs-lookup"><span data-stu-id="7ba24-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

