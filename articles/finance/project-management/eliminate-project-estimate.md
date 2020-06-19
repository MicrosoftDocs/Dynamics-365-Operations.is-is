---
title: Útiloka verkmat
description: Í þessu efnisatriði er að finna upplýsingar um losun verkáætlunar eftir að henni er lokið.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410230"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="21791-103">Útiloka verkmat</span><span class="sxs-lookup"><span data-stu-id="21791-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21791-104">Verkáætlanir bjóða upp á fjárhagsyfirlit fyrir vinnu sem er áætluð og tímasett fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="21791-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="21791-105">Til að vinna með mat fyrir stigveldi verks, verður að  hengja verkið við matsverk.</span><span class="sxs-lookup"><span data-stu-id="21791-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="21791-106">Matsverk er alltaf byggt á núverandi verki, en þó geta mörg verk átt við eitt matsverk.</span><span class="sxs-lookup"><span data-stu-id="21791-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="21791-107">Aðeins er hægt að hengja föst verð og fjárfestingaverkefni við matsverk og þau verk verða að tilheyra sama verkflokknum sem matsverkið.</span><span class="sxs-lookup"><span data-stu-id="21791-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="21791-108">Til að eyða matsverki verður að ljúka því.</span><span class="sxs-lookup"><span data-stu-id="21791-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="21791-109">Eftirfarandi skref útskýra hvernig á að eyða mati.</span><span class="sxs-lookup"><span data-stu-id="21791-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="21791-110">Opnið **Verkefnastjórnun og bókhald** > **Öll verk** og opnið verkið.</span><span class="sxs-lookup"><span data-stu-id="21791-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="21791-111">Í flipanum **Stjórna** skal velja **Mat** og á síðunni **Mat** skal velja **Losa**.</span><span class="sxs-lookup"><span data-stu-id="21791-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="21791-112">Á síðunni **Losa mat** í flipanum **Almennt** skal stilla eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="21791-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="21791-113">**Tímabilskóði**: Veljið tímabilskóða til að velja viðeigandi matsverk.</span><span class="sxs-lookup"><span data-stu-id="21791-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="21791-114">**Dagsetning mats**: Veljið réttu matsdagsetninguna fyrir losun.</span><span class="sxs-lookup"><span data-stu-id="21791-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="21791-115">**Eyða með VÍV-viðvörun**: Virkið þennan valkost til að bjóða upp á tilkynningu þegar mat sem tengist verki í vinnslu verður losað.</span><span class="sxs-lookup"><span data-stu-id="21791-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="21791-116">Ef þessi valkostur er ekki virkjaður getur losunin ekki haldið áfram ef einhverjar ómetnar færslur eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="21791-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="21791-117">Þessi valkostur er aðeins í boði þegar losun er notuð í matsverki.</span><span class="sxs-lookup"><span data-stu-id="21791-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="21791-118">Hann er ekki í boði ef notaðar eru reglubundnar bókanir.</span><span class="sxs-lookup"><span data-stu-id="21791-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="21791-119">Þessi stilling virkar með stillingum í flipanum **Mat** á síðunni **Færibreytur verks**, í reitahópnum **Leyfa losun þegar ómetnar færslur eru til**.</span><span class="sxs-lookup"><span data-stu-id="21791-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="21791-120">**Setja stig á Lokið**: Virkið þennan valkost til að stilla stig matsverks á **Lokið** eftir að losunin er sett af stað.</span><span class="sxs-lookup"><span data-stu-id="21791-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="21791-121">**Prenta matslista**: Veljið upplýsingar sem eiga að fylgja með þegar matslistinn er prentaður.</span><span class="sxs-lookup"><span data-stu-id="21791-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="21791-122">**Sýna athugasemdakladda**: Virkið þennan valkost til að birta athugasemdakladdann.</span><span class="sxs-lookup"><span data-stu-id="21791-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="21791-123">**Bókunardagsetning**: Veljið fjárhagsbókunardagsetningu fyrir matið.</span><span class="sxs-lookup"><span data-stu-id="21791-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="21791-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="21791-124">Select **OK**.</span></span>
5. <span data-ttu-id="21791-125">Þegar losunarferlinu er lokið verður losaða matsverkið sýnt með neikvæðu gildi.</span><span class="sxs-lookup"><span data-stu-id="21791-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="21791-126">Ef ætlunin var ekki að losa mat er hægt að velja losaða matið og velja **Bakfæra losun**.</span><span class="sxs-lookup"><span data-stu-id="21791-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
