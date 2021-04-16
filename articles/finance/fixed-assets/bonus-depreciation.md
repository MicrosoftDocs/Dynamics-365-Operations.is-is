---
title: Viðbótarafskriftir
description: Þessi grein veitir yfirlit yfir virknina viðbótarafskriftir.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f811b913f751a860c21fc120b15bac406281d7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827027"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="6f16d-103">Viðbótarafskriftir</span><span class="sxs-lookup"><span data-stu-id="6f16d-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f16d-104">Þessi grein veitir yfirlit yfir virknina viðbótarafskriftir.</span><span class="sxs-lookup"><span data-stu-id="6f16d-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="6f16d-105">Fyrir viðbótarafskriftir er hægt að taka aukalegar afskriftarupphæðir á fyrsta ári sem eign er í þjónustu og afskrifuð .</span><span class="sxs-lookup"><span data-stu-id="6f16d-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="6f16d-106">Viðbótarafskriftir verður að taka á undan öðrum afskriftaútreikningum.</span><span class="sxs-lookup"><span data-stu-id="6f16d-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="6f16d-107">Þess vegna er best að nota viðbótarafskriftir með bækur þar sem Bóka á fjárhag virkni er óvirkur.</span><span class="sxs-lookup"><span data-stu-id="6f16d-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="6f16d-108">Hægt er að nota **Eyða færslum sem eru ekki bókaðar í fjárhag** valkost til að eyða sögulegum færslum fyrir bókum sem ekki bóka í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="6f16d-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="6f16d-109">Svo er hægt að hýsa viðbótarafskriftir síðar í líftíma eignar með því að eyða afskriftarfærslum sem voru áður bókaðar.</span><span class="sxs-lookup"><span data-stu-id="6f16d-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="6f16d-110">Hægt er að reikna út viðbótarafskriftir með því að nota tillöguferli og hægt er að stofna handvirkar færslur viðbótarafskrifta.</span><span class="sxs-lookup"><span data-stu-id="6f16d-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="6f16d-111">Ekki er hægt að stofna viðbótarafsrkiftir ef afskriftarfærslur eða -breytingar eru þegar til fyrir viðkomandi eignabók.</span><span class="sxs-lookup"><span data-stu-id="6f16d-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="6f16d-112">Þegar tillöguferli er notað til að reikna viðbótarafskriftir eru allar tiltækar viðbótarfærslur hafðar með í útreikningi á grunninum.</span><span class="sxs-lookup"><span data-stu-id="6f16d-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="6f16d-113">Útreikningurinn inniheldur einnig allar fyrri viðbótarafskriftir sem voru færðar inn handvirkt fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="6f16d-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="6f16d-114">Þegar gera á fleiri en eina afskrift fyrir eign er tekið tillit til forgangs.</span><span class="sxs-lookup"><span data-stu-id="6f16d-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="6f16d-115">Hver viðbót dregur úr grunni fyrir næstu viðbót.</span><span class="sxs-lookup"><span data-stu-id="6f16d-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="6f16d-116">Ekki er tekið tillit til hrakvirðis í eignagrundvelli fyrir útreikning viðbótarafskriftar og afskriftarhefð á ekki við fyrir viðbótarafskriftir.</span><span class="sxs-lookup"><span data-stu-id="6f16d-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="6f16d-117">Eins og er falla ákveðnar eignir undir eignir í Kafla 179 í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="6f16d-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="6f16d-118">Með því að nota frádrátt Kafla 179 er hægt að endurheimta allt eða hluta af kostnaði við tiltekna eignir, upp að mörkum.</span><span class="sxs-lookup"><span data-stu-id="6f16d-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="6f16d-119">Hægt er að endurheimta kostnað með því að draga hann frá á árinu þegar þú setur eign í þjónustu.</span><span class="sxs-lookup"><span data-stu-id="6f16d-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="6f16d-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6f16d-120">Example</span></span>
<span data-ttu-id="6f16d-121">Eftirfarandi viðbótaruppskriftir eru tengdar eignabók:</span><span class="sxs-lookup"><span data-stu-id="6f16d-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="6f16d-122">**Kafli 179**: $1.000,00, Forgangur 1</span><span class="sxs-lookup"><span data-stu-id="6f16d-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="6f16d-123">**Liberty Zone**: 30%, Forgangur 2</span><span class="sxs-lookup"><span data-stu-id="6f16d-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="6f16d-124">Stofnkostnaðurinn er 5.000,00.</span><span class="sxs-lookup"><span data-stu-id="6f16d-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="6f16d-125">Þegar viðbótarafskrift er reiknaður er fyrsta upphæð viðbótaruppskriftar 1.000,00 fyrir Kafla 179 afskrift.</span><span class="sxs-lookup"><span data-stu-id="6f16d-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="6f16d-126">Upphæð næstu viðbótarafskriftar, fyrir afskrift Liberty Zone, er reiknuð á eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6f16d-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="6f16d-127">Kaupverð - $1.000 (afskrift Kafla 179) x 30% = 1.200</span><span class="sxs-lookup"><span data-stu-id="6f16d-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="6f16d-128">Ef upphæð viðbótarafskriftar er hærri en eftirstandandi kaupverð er upphæð viðbótarafskrifta annað hvort niðurstaða útreikningur viðbótarafskrifta eða eftirstandandi kaupverð, hvort heldur sem er lægri.</span><span class="sxs-lookup"><span data-stu-id="6f16d-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="6f16d-129">Ef eftirstandandi kaupverð er 0 eða minna verða viðbótarafskriftafærslur ekki myndaðar.</span><span class="sxs-lookup"><span data-stu-id="6f16d-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="6f16d-130">Þegar viðbótarafskrift er reiknuð með tillöguferlinu er viðbótarafskriftarfærsla stofnuð fyrir allar viðeigandi skrár viðbótarafskrifta sem tengjast eignabók.</span><span class="sxs-lookup"><span data-stu-id="6f16d-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="6f16d-131">Hægt er að stofna ótakmarkaðan fjölda af viðbótarafskriftafærslum.</span><span class="sxs-lookup"><span data-stu-id="6f16d-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="6f16d-132">Eftir að þessum færslum hefur verið úthlutað á eignaflokka eru þær notaðar í eignabók.</span><span class="sxs-lookup"><span data-stu-id="6f16d-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="6f16d-133">Viðbótarafskriftir eru færðar inn sem prósenta eða föst upphæð.</span><span class="sxs-lookup"><span data-stu-id="6f16d-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="6f16d-134">Þegar þú bókar afskriftartillögur eru bókaðar viðbótarafskriftafærslur í bókina sem aðskildar færslur úr afskriftarfærslum.</span><span class="sxs-lookup"><span data-stu-id="6f16d-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]