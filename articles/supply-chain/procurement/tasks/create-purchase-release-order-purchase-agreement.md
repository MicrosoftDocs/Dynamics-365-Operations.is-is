---
title: Stofna úttektarpöntun innkaupa úr innkaupasamningi
description: Þessi ferli sýnir hvernig á að nota innkaupasamning þegar innkaupapöntun er stofnuð.
author: mkirknel
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da161c9066c822f8c09e5eda90994e8b03af4681
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916861"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="0a982-103">Stofna úttektarpöntun innkaupa úr innkaupasamningi</span><span class="sxs-lookup"><span data-stu-id="0a982-103">Create a purchase release order from a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a982-104">Þessi ferli sýnir hvernig á að nota innkaupasamning þegar innkaupapöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0a982-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="0a982-105">Innkaupasamnings verður að nota þegar innkaupapöntun er stofnuð þar almennir skilmálar sem á að afrita í haus innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="0a982-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="0a982-106">Þetta verk myndi venjulega framkvæmt af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="0a982-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="0a982-107">Nauðsynleg frumforsenda þessari handbók, þú verður að hafa gildan innkaupasamning með í ráðstöfun afurðarmagns fyrir lánardrottinn og vörur.</span><span class="sxs-lookup"><span data-stu-id="0a982-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="0a982-108">Hægt er að nota sömu aðferð ef þú ert með  innkaupasamning með aðrar gerðir af ráðstafanir.</span><span class="sxs-lookup"><span data-stu-id="0a982-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="0a982-109">Hægt er að keyra þessari handbók sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="0a982-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="0a982-110">Ef verið er að nota USMF er hægt að keyra "Stofna innkaupasamning" leiðarvísi fyrst til að setja upp nauðsynlegt frumskilyrði fyrir þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="0a982-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="0a982-111">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="0a982-111">Create a purchase order</span></span>
1. <span data-ttu-id="0a982-112">Í **skoðunarrúðunni** ferðu í **Vinnusvæði> Undirbúningur innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="0a982-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="0a982-113">Smelltu á **Ný innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="0a982-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="0a982-114">Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0a982-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a982-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0a982-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0a982-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0a982-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0a982-117">Útvíkkaðu flýtiflipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="0a982-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="0a982-118">Í reitnum **Innkaupasamningur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0a982-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="0a982-119">Allar tiltækar samninga lánardrottins eru taldar upp hér.</span><span class="sxs-lookup"><span data-stu-id="0a982-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="0a982-120">Finna gildan samning sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="0a982-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="0a982-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0a982-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0a982-122">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="0a982-122">Click **Yes**.</span></span>
10. <span data-ttu-id="0a982-123">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a982-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="0a982-124">Bæta við línu</span><span class="sxs-lookup"><span data-stu-id="0a982-124">Add a line</span></span>
1. <span data-ttu-id="0a982-125">Í reitnum **Vörunúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0a982-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="0a982-126">Ef tilteknar víddir staðsetningar eða birgða eru á ráðstöfun verður þú að færa inn sama gildi í innkaupapöntunarlínu til að geta notað samningnum.</span><span class="sxs-lookup"><span data-stu-id="0a982-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="0a982-127">Í reitnum **Svæði** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0a982-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="0a982-128">Svæðið er hugsanlega útfyllt þegar með sjálfgefnu gildi úr pöntuninni, eða frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="0a982-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="0a982-129">Ef svo er er hægt að sleppa þessu þrepi.</span><span class="sxs-lookup"><span data-stu-id="0a982-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="0a982-130">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0a982-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0a982-131">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0a982-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0a982-132">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="0a982-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="0a982-133">Villuleita að verð er afritað úr ráðstöfun.</span><span class="sxs-lookup"><span data-stu-id="0a982-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="0a982-134">Fletta upp á ráðstöfun</span><span class="sxs-lookup"><span data-stu-id="0a982-134">Look up the commitment</span></span>
1. <span data-ttu-id="0a982-135">Smelltu á **Uppfæra línu**.</span><span class="sxs-lookup"><span data-stu-id="0a982-135">Click **Update line**.</span></span>
2. <span data-ttu-id="0a982-136">Smelltu á **Meðfylgjandi**.</span><span class="sxs-lookup"><span data-stu-id="0a982-136">Click **Attached**.</span></span> <span data-ttu-id="0a982-137">Hér er hægt að fá upplýsingar fyrir innkaupasamning.</span><span class="sxs-lookup"><span data-stu-id="0a982-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="0a982-138">Til dæmis er hægt að sjá verð og hvort verð og afsláttur er fastur, sem þýðir að ef þú breytir verði eða afslætti á innkaupapöntun í annað gildi en á ráðstöfun, mun kerfið fjarlægja tengil svo innkaupapöntunarlínan uppfyllir ekki á ráðstöfun.</span><span class="sxs-lookup"><span data-stu-id="0a982-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="0a982-139">Er einnig hægt að sjá hvort valkosturinn Hámark er notað er valinn, sem þýðir að magn á ráðstöfun má ekki fara fram úr með samlagningu allra innkaupa sem uppfylla ráðstöfun.</span><span class="sxs-lookup"><span data-stu-id="0a982-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="0a982-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0a982-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="0a982-141">Fletta upp á innkaupasamningur</span><span class="sxs-lookup"><span data-stu-id="0a982-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="0a982-142">Á **aðgerðasvæðinu** er smellt á **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="0a982-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="0a982-143">Smelltu á **Innkaupasamningur**.</span><span class="sxs-lookup"><span data-stu-id="0a982-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="0a982-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0a982-144">Close the page.</span></span>
4. <span data-ttu-id="0a982-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0a982-145">Close the page.</span></span>

