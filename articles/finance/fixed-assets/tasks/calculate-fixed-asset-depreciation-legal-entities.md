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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b09bbe4d0143aa521ca0a4cf67e86b7165b0f4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968955"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="383bd-103">Reikna afskriftir eigna milli lögaðila</span><span class="sxs-lookup"><span data-stu-id="383bd-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="383bd-104">Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi.</span><span class="sxs-lookup"><span data-stu-id="383bd-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="383bd-105">Þessi aðferð sýnir hvernig skal setja upp og keyra ferlið fyrir marga lögaðila.</span><span class="sxs-lookup"><span data-stu-id="383bd-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="383bd-106">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="383bd-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="383bd-107">Setja upp færslubókakeyrslu afskrifta á milli fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="383bd-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="383bd-108">Fara í Eignir > Uppsetning > Færibreytur eigna.</span><span class="sxs-lookup"><span data-stu-id="383bd-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="383bd-109">Útvíkka eignatillagnahlutann.</span><span class="sxs-lookup"><span data-stu-id="383bd-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="383bd-110">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="383bd-110">Click Add.</span></span>
4. <span data-ttu-id="383bd-111">Sláið inn eða veldu gildi í reitnum bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="383bd-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="383bd-112">Sláið inn eða veljið gildi í reitnum heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="383bd-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="383bd-113">Endurtaka uppsetning færslubókar á síðunni Færibreytur eigna fyrir hverjum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="383bd-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="383bd-114">Afskriftarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="383bd-114">Depreciation run</span></span>
1. <span data-ttu-id="383bd-115">Fara í Eignir > Færslubókarfærslur > Stofna afskriftartillögu.</span><span class="sxs-lookup"><span data-stu-id="383bd-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="383bd-116">Sláið inn eða veldu gildi í reitnum bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="383bd-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="383bd-117">Færslubókarnafnið mun verða sjálfgefið úr Færibreytum eigna.</span><span class="sxs-lookup"><span data-stu-id="383bd-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="383bd-118">Því er hægt að breyta hér fyrir núgildandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="383bd-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="383bd-119">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="383bd-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="383bd-120">Veljið lögaðilana sem á að hafa með í afskriftarkeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="383bd-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="383bd-121">Aðeins lögaðilar með uppsettar færslubækur fyrir Eignatillögur á síðunni Færibreytur eigna verða sýndir á listanum.</span><span class="sxs-lookup"><span data-stu-id="383bd-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="383bd-122">Veljið Já í reitnum bóka færslubækur.</span><span class="sxs-lookup"><span data-stu-id="383bd-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="383bd-123">Síureitir ná yfir allar eignir, hópa og bækur fyrir lögaðila sem valdir eru fyrir þessa afskriftakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="383bd-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="383bd-124">Runuvinnsluvalkosturinn er virkjaður að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="383bd-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="383bd-125">Þegar þessi valkostur er virkjaður, mun stofnun og bókun færslubókar afskrifta keyrast í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="383bd-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="383bd-126">Smella skal Stofna færslubók.</span><span class="sxs-lookup"><span data-stu-id="383bd-126">Click Create journal.</span></span>
6. <span data-ttu-id="383bd-127">Fara í Eignir >°Færslubókarfærslur°> Eignabók.</span><span class="sxs-lookup"><span data-stu-id="383bd-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

