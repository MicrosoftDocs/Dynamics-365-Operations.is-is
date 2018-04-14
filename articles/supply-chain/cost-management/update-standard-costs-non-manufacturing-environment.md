---
title: "Uppfærsla staðalkostnaðar í umhverfi sem tengist ekki framleiðslu"
description: "Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðslulausu umhverfi."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 432cdc516c74c4fff570366d0eab77323d3159bf
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="bebc1-103">Uppfærsla staðalkostnaðar í umhverfi sem tengist ekki framleiðslu</span><span class="sxs-lookup"><span data-stu-id="bebc1-103">Update standard costs in a non-manufacturing environment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bebc1-104">Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðslulausu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="bebc1-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="bebc1-105">Eftirfarandi leiðbeiningar gera ráð fyrir að notuð sé tveggja útgáfu nálgunin til að uppfæra staðlaðan kostnað.</span><span class="sxs-lookup"><span data-stu-id="bebc1-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="bebc1-106">Í þessari nálgun inniheldur ein kostnaðarútgáfa upphaflega skilgreindan staðlaðan kostnað fyrir fryst tímabil og seinni kostnaðarútgáfan inniheldur stigvaxandi uppfærslur.</span><span class="sxs-lookup"><span data-stu-id="bebc1-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="bebc1-107">Hver uppfærsla er færð inn sem kostnaðarfærsla innan seinni kostnaðarútgáfunnar og að lokum gerð virk.</span><span class="sxs-lookup"><span data-stu-id="bebc1-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="bebc1-108">Önnur lausn felst í einnar útgáfu nálgun með því að nota upphaflega skilgreindan staðlaðan kostnað.</span><span class="sxs-lookup"><span data-stu-id="bebc1-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="bebc1-109">Tveggja útgáfu nálgunin krefst þess að skilgreind sé önnur kostnaðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="bebc1-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="bebc1-110">Hér eru leiðbeiningar fyrir skilgreiningu þessarar kostnaðarútgáfu:</span><span class="sxs-lookup"><span data-stu-id="bebc1-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="bebc1-111">Notið kostnaðargerðina **Staðlaður kostnaður**.</span><span class="sxs-lookup"><span data-stu-id="bebc1-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="bebc1-112">Gefið kostnaðarútgáfunni lýsandi kenni sem skýrir innihaldið, til dæmis **2016-UPPFÆRSLUR**.</span><span class="sxs-lookup"><span data-stu-id="bebc1-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="bebc1-113">Tryggja þarf að kostnaðarfærslur séu teknar með.</span><span class="sxs-lookup"><span data-stu-id="bebc1-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="bebc1-114">Leyfið kostnaðarfærslur fyrir öll svæði.</span><span class="sxs-lookup"><span data-stu-id="bebc1-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="bebc1-115">Ef svæði er sérstaklega tilgreint er aðeins hægt að færa kostnaðarfærslur fyrir það svæði.</span><span class="sxs-lookup"><span data-stu-id="bebc1-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="bebc1-116">Tilgreinið varaúrræði sem **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="bebc1-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="bebc1-117">Varaúrræðisreglan á aðeins við kostnaðarútreikninga vegna framleiddra vara.</span><span class="sxs-lookup"><span data-stu-id="bebc1-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="bebc1-118">Þannig er farið að við að leiðrétta, aðlaga eða uppfæra staðlaðan kostnað nýrra vara:</span><span class="sxs-lookup"><span data-stu-id="bebc1-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="bebc1-119">Notið skjámyndina **Kostnaðarútgáfa** **Uppsetning**til að leyfa skráningu á kostnaðarfærslum inn í seinni kostnaðarútgáfuna.</span><span class="sxs-lookup"><span data-stu-id="bebc1-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="bebc1-120">Koma má í veg fyrir virkjun á kostnaði í bið, svo að virkjun verði leyfð eftir að kostnaður í bið hefur verið algerlega og nákvæmlega skilgreindur.</span><span class="sxs-lookup"><span data-stu-id="bebc1-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="bebc1-121">Einnig er hægt að færa inn dagsetningu í svæðinu **Frá dagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="bebc1-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="bebc1-122">Gott er að nota dagsetninguna þegar á að virkja stigvaxandi uppfærslur.</span><span class="sxs-lookup"><span data-stu-id="bebc1-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="bebc1-123">Sem annar valkostur, skiljið svæðið **Frá dagsetningu** eftir autt fyrir kostnaðarútgáfuna, og færið svo inn dagsetningu í svæðið **Frá dagsetningu** fyrir hverja kostnaðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="bebc1-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="bebc1-124">Nota skal síðuna **Vöruverð** til að færa inn uppfærslur sem kostnaðarfærslur vöru sem eru innan seinni kostnaðarútgáfunnar.</span><span class="sxs-lookup"><span data-stu-id="bebc1-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="bebc1-125">Notið skýrsluna **Vöruverð** til að sannprófa heilleika og réttmæti vörukostnaðarfærslanna innan seinni kostnaðarútgáfunnar.</span><span class="sxs-lookup"><span data-stu-id="bebc1-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="bebc1-126">Notið síðuna **Viðhald kostnaðarútgáfu** til að breyta lokunarflaggi til að heimila virkjun á biðkostnaðarfærslum í seinni kostnaðarútgáfunni.</span><span class="sxs-lookup"><span data-stu-id="bebc1-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="bebc1-127">Notið síðuna **Virkja verð** (sem er opnuð úr síðunni **Viðhald Kostnaðarútgáfu**) til að virkja allar biðkostnaðarfærslur í seinni kostnaðarútgáfunni.</span><span class="sxs-lookup"><span data-stu-id="bebc1-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="bebc1-128">Einnig er hægt að gera kostnaðarfærslur í bið fyrir stakar vörur virkar með því að smella á hnappinn **Virkja biðverð** á síðunni **Vöruverð**.</span><span class="sxs-lookup"><span data-stu-id="bebc1-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="bebc1-129">Notið skjámyndina **Uppsetning kostnaðarútgáfu** til þess að breyta lokunarflöggum í síðari kostnaðarútgáfunni og koma í veg fyrir frekara gagnaviðhald.</span><span class="sxs-lookup"><span data-stu-id="bebc1-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="bebc1-130">Lokunarreglurnar hindra færslu nýs kostnaðar í bið og virkjun kostnaðar í bið.</span><span class="sxs-lookup"><span data-stu-id="bebc1-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





