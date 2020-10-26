---
title: Ljúka grunnuppsetningu útgefins afurðarsniðmáts
description: Þetta efni sýnir hvernig á að ljúka lágmarksuppsetningu sem er krafist áður en hægt er að nota afurðarsniðmát í uppskriftarútgáfum.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986408"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="5d137-103">Ljúka grunnuppsetningu útgefins afurðarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="5d137-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d137-104">Þetta efni sýnir hvernig á að ljúka lágmarksuppsetningu sem er krafist áður en hægt er að nota afurðarsniðmát í uppskriftarútgáfum.</span><span class="sxs-lookup"><span data-stu-id="5d137-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="5d137-105">Þetta er þriðja ferli af átta sem útskýrir hvernig á að byggja upp samsetningar fyrir víddaskilgreining.</span><span class="sxs-lookup"><span data-stu-id="5d137-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="5d137-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="5d137-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5d137-107">Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="5d137-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="5d137-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5d137-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d137-109">Veljið afurðarsniðmátið sem hefur verið losað í öðru ferli.</span><span class="sxs-lookup"><span data-stu-id="5d137-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="5d137-110">afurðarsniðmát er stofnuð með skilgreiningartækni sem byggist á víddum.</span><span class="sxs-lookup"><span data-stu-id="5d137-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="5d137-111">Í aðgerðasvæðinu velurðu **Afurð.**</span><span class="sxs-lookup"><span data-stu-id="5d137-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="5d137-112">Veldu **Víddaflokkar** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5d137-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="5d137-113">Í reitnum **Geymsluvíddarflokkur** velurðu fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5d137-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5d137-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5d137-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d137-115">Geymsluvíddaflokkinn ákvarðar hvaða geymsluvíddir eru notaðar fyrir vöru í færslu.</span><span class="sxs-lookup"><span data-stu-id="5d137-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="5d137-116">Veldu **Stað** fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="5d137-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="5d137-117">Í reitnum **Rakningarvíddarflokkur** velurðu fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5d137-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5d137-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5d137-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d137-119">Rakningarvíddarflokkur ákvarðar hvaða rakningarvíddir eru notaðar fyrir vöru í færslu.</span><span class="sxs-lookup"><span data-stu-id="5d137-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="5d137-120">Veldu **Ekkert** fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="5d137-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="5d137-121">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d137-121">Click **OK**.</span></span>
10. <span data-ttu-id="5d137-122">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="5d137-122">Click **Edit**.</span></span>
11. <span data-ttu-id="5d137-123">Í reitnum **Vörulíkanaflokkur** velurðu fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5d137-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="5d137-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5d137-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d137-125">Vörulíkanaflokkar innihalda stillingar sem ákvarða hvernig vörum er stýrt og þær meðhöndlaðar á inn- og úthreyfingum.</span><span class="sxs-lookup"><span data-stu-id="5d137-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="5d137-126">Þeir ákvarða einnig hvernig vörunotkun er reiknuð út.</span><span class="sxs-lookup"><span data-stu-id="5d137-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="5d137-127">Veldu **FIFO** fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="5d137-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="5d137-128">Stækkaðu hlutann **Stjórnun kostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="5d137-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="5d137-129">Í reitnum **Vöruflokkur** velurðu fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5d137-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5d137-130">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5d137-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="5d137-131">Vöruflokkar eru notaðir til að stjórna birgðum með því að skipta birgðavörum í hópa.</span><span class="sxs-lookup"><span data-stu-id="5d137-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="5d137-132">Veldu **CarAudio** fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="5d137-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="5d137-133">Í aðgerðarúðunni velurðu **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="5d137-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="5d137-134">Veldu **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="5d137-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="5d137-135">Veljið valkost í reitnum **Sjálfgefin gerð pöntunar**.</span><span class="sxs-lookup"><span data-stu-id="5d137-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="5d137-136">Veldu **Framleiðslu** til að tilgreina að sjálfgefinn kostur framboðs fyrir þessa afurðarsniðmát er að framleiða þær.</span><span class="sxs-lookup"><span data-stu-id="5d137-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="5d137-137">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5d137-137">Select **Save**.</span></span>
20. <span data-ttu-id="5d137-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5d137-138">Close the page.</span></span>
21. <span data-ttu-id="5d137-139">Lokið skjámyndinni **Upplýsingar um losaða afurð**.</span><span class="sxs-lookup"><span data-stu-id="5d137-139">Close the **Released product details** form.</span></span>

