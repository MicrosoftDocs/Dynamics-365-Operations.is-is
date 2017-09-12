--- 
title: "Ljúka grunnuppsetningu útgefins afurðarsniðmáts"
description: "Þessi verklýsing sýnir hvernig á að ljúka lágmarksuppsetningu sem er krafist áður en hægt er að nota afurðarsniðmát í uppskriftarútgáfum."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c42476ca3ffee41e303457150ef15da0f5af8a8f
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="559f1-103">Ljúka grunnuppsetningu útgefins afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="559f1-103">Complete basic setup of a released product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="559f1-104">Þessi verklýsing sýnir hvernig á að ljúka lágmarksuppsetningu sem er krafist áður en hægt er að nota afurðarsniðmát í uppskriftarútgáfum.</span><span class="sxs-lookup"><span data-stu-id="559f1-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="559f1-105">Þetta er þriðja ferli af átta sem útskýrir hvernig á að byggja upp samsetningar fyrir víddaskilgreining.</span><span class="sxs-lookup"><span data-stu-id="559f1-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="559f1-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="559f1-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="559f1-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="559f1-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="559f1-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="559f1-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="559f1-109">Veljið afurðarsniðmátið sem hefur verið losað í öðru ferli.</span><span class="sxs-lookup"><span data-stu-id="559f1-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="559f1-110">afurðarsniðmát er stofnuð með skilgreiningartækni sem byggist á víddum.</span><span class="sxs-lookup"><span data-stu-id="559f1-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="559f1-111">Í aðgerðasvæðinu er smellt á Afurð.</span><span class="sxs-lookup"><span data-stu-id="559f1-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="559f1-112">Smellt er á Víddaflokkar til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="559f1-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="559f1-113">Í reitnum Geymsluvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="559f1-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="559f1-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="559f1-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="559f1-115">Geymsluvíddaflokkinn ákvarðar hvaða geymsluvíddir eru notaðar fyrir vöru í færslu.</span><span class="sxs-lookup"><span data-stu-id="559f1-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="559f1-116">Veljið stað fyrir þessa færslu.</span><span class="sxs-lookup"><span data-stu-id="559f1-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="559f1-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="559f1-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="559f1-118">Í reitnum Rakningarvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="559f1-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="559f1-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="559f1-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="559f1-120">Rakningarvíddarflokkur ákvarðar hvaða rakningarvíddir eru notaðar fyrir vöru í færslu.</span><span class="sxs-lookup"><span data-stu-id="559f1-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="559f1-121">Velja Ekkert fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="559f1-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="559f1-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="559f1-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="559f1-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="559f1-123">Click OK.</span></span>
12. <span data-ttu-id="559f1-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="559f1-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="559f1-125">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="559f1-125">Click Edit.</span></span>
    * <span data-ttu-id="559f1-126">Opnið skjámyndinni „Upplýsingar um losaða afurð“ til að halda áfram uppsetningarverkinu.</span><span class="sxs-lookup"><span data-stu-id="559f1-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="559f1-127">Í reitnum Vörulíkanaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="559f1-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="559f1-128">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="559f1-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="559f1-129">Vörulíkanaflokkar innihalda stillingar sem ákvarða hvernig vörum er stýrt og þær meðhöndlaðar á inn- og úthreyfingum.</span><span class="sxs-lookup"><span data-stu-id="559f1-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="559f1-130">Þeir ákvarða einnig hvernig vörunotkun er reiknuð út.</span><span class="sxs-lookup"><span data-stu-id="559f1-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="559f1-131">Veljið FIFO fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="559f1-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="559f1-132">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="559f1-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="559f1-133">Stækka eða fella saman hlutann Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="559f1-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="559f1-134">Í reitnum Vöruflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="559f1-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="559f1-135">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="559f1-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="559f1-136">Vöruflokkar eru notaðir til að stjórna birgðum með því að skipta birgðavörum í hópa.</span><span class="sxs-lookup"><span data-stu-id="559f1-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="559f1-137">Veljið CarAudio fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="559f1-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="559f1-138">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="559f1-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="559f1-139">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="559f1-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="559f1-140">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="559f1-140">Click Default order settings.</span></span>
23. <span data-ttu-id="559f1-141">Veljið valkost í svæðinu sjálfgefin gerð pöntunar.</span><span class="sxs-lookup"><span data-stu-id="559f1-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="559f1-142">Velja Framleiðslu til að tilgreina að sjálfgefinn kostur framboðs fyrir þessa afurðarsniðmát er að framleiða þær.</span><span class="sxs-lookup"><span data-stu-id="559f1-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="559f1-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="559f1-143">Close the page.</span></span>
25. <span data-ttu-id="559f1-144">Lokið skjámyndinni „Upplýsingar um losaða afurð“.</span><span class="sxs-lookup"><span data-stu-id="559f1-144">Close the Released product details form.</span></span>


