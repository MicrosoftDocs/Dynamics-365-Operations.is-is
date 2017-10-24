--- 
title: "Flytja inn skilgreiningu úr Lifecycle Services fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="aa556-103">Flytja inn skilgreiningu úr Lifecycle Services fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="aa556-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa556-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af skilgreiningarsnið fyrir rafræna skýrslugerð (ER) úr Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="aa556-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="aa556-105">Í þessu dæmi velurðu þá útgáfu af skilgreiningu fyrir Rafræna skýrslugerð sem þér hugnast, og flytur hana inn fyrir sýnifyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="aa556-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="aa556-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Hlaða upp Hlaða upp skilgreiningu Rafræn skýrslugerð í Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="aa556-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="aa556-107">Aðgangur að LCS er einnig nauðsynlegur til að ljúka þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="aa556-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="aa556-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="aa556-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="aa556-109">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="aa556-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="aa556-110">Eyða samnýttu útgáfu skilgreiningar gagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="aa556-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="aa556-111">Veljið 'dæmi um skilgreiningu líkans', í trénu.</span><span class="sxs-lookup"><span data-stu-id="aa556-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="aa556-112">Fyrsta útgáfa af dæmi um skilgreiningu gagnalíkans hefur verið stofnuð og birt í LVS á meðan á ferlinu "hlaða upp skilgreiningu Rafræn skýrslugerð í Lifecycle Services" stóð.</span><span class="sxs-lookup"><span data-stu-id="aa556-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="aa556-113">Í þessu ferli verður að eyða þessi útgáfa skilgreiningar Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="aa556-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="aa556-114">Þessi útgáfa af dæmi um skilgreiningu gagnalíkans verður flutt inn síðar úr LCS.</span><span class="sxs-lookup"><span data-stu-id="aa556-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="aa556-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa556-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa556-116">Veljið útgáfu þessarar skilgreiningar sem er í stöðunni "samnýtt".</span><span class="sxs-lookup"><span data-stu-id="aa556-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="aa556-117">Þessi staða tilgreinir að skilgreiningin sé nú birt í LCS.</span><span class="sxs-lookup"><span data-stu-id="aa556-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="aa556-118">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="aa556-118">Click Change status.</span></span>
4. <span data-ttu-id="aa556-119">Smellið á hætta notkun.</span><span class="sxs-lookup"><span data-stu-id="aa556-119">Click Discontinue.</span></span>
    * <span data-ttu-id="aa556-120">Breyta stöðu valda útgáfu úr 'Samnýttum' til 'hætt í notkun" til að gera tiltækt fyrir eyðingu.</span><span class="sxs-lookup"><span data-stu-id="aa556-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="aa556-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="aa556-121">Click OK.</span></span>
6. <span data-ttu-id="aa556-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa556-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa556-123">Veljið útgáfu þessarar skilgreiningar sem hefur stöðuna "hætt í notkun".</span><span class="sxs-lookup"><span data-stu-id="aa556-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="aa556-124">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="aa556-124">Click Delete.</span></span>
8. <span data-ttu-id="aa556-125">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="aa556-125">Click Yes.</span></span>
    * <span data-ttu-id="aa556-126">Athugið að eina drög að útgáfu 2 hinnar völdu skilgreiningar gagnalíkans er tiltækt.</span><span class="sxs-lookup"><span data-stu-id="aa556-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="aa556-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="aa556-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="aa556-128">Flytja inn samnýttu útgáfu skilgreiningar gagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="aa556-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="aa556-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="aa556-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="aa556-130">Opna lista yfir geymslur fyrir „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="aa556-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="aa556-131">veitandi skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="aa556-131">configuration provider.</span></span>  
2. <span data-ttu-id="aa556-132">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="aa556-132">Click Repositories.</span></span>
3. <span data-ttu-id="aa556-133">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="aa556-133">Click Open.</span></span>
    * <span data-ttu-id="aa556-134">Velja lcs-gagnasafn og opna hana.</span><span class="sxs-lookup"><span data-stu-id="aa556-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="aa556-135">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="aa556-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="aa556-136">Veljið fyrsta útgáfa "dæmi um skilgreiningu líkans" í útgáfulistanum.</span><span class="sxs-lookup"><span data-stu-id="aa556-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="aa556-137">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="aa556-137">Click Import.</span></span>
6. <span data-ttu-id="aa556-138">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="aa556-138">Click Yes.</span></span>
    * <span data-ttu-id="aa556-139">Staðfesta innflutning valda útgáfu úr LCS.</span><span class="sxs-lookup"><span data-stu-id="aa556-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="aa556-140">Athugið að upplýsingaskilaboð (ofan skjámyndin) staðfestir að tókst að flytja inn valda útgáfu.</span><span class="sxs-lookup"><span data-stu-id="aa556-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="aa556-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="aa556-141">Close the page.</span></span>
8. <span data-ttu-id="aa556-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="aa556-142">Close the page.</span></span>
9. <span data-ttu-id="aa556-143">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="aa556-143">Click Configurations.</span></span>
10. <span data-ttu-id="aa556-144">Veljið 'dæmi um skilgreiningu líkans', í trénu.</span><span class="sxs-lookup"><span data-stu-id="aa556-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="aa556-145">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa556-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa556-146">Veljið útgáfu þessarar skilgreiningar sem hefur stöðuna "samnýtt".</span><span class="sxs-lookup"><span data-stu-id="aa556-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="aa556-147">Athugið að samnýtt útgáfu 1 hinnar völdu skilgreiningar gagnalíkans er tiltækt nú líka.</span><span class="sxs-lookup"><span data-stu-id="aa556-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


