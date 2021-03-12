---
title: Stofna aðalsniðmát
description: Stofna afurðarsniðmát fyrir forskilgreind afbrigði.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 612f83f2df0ca3e66aa38defa27ec34315b4b2ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001725"
---
# <a name="create-a-product-master"></a><span data-ttu-id="f6003-103">Stofna aðalsniðmát</span><span class="sxs-lookup"><span data-stu-id="f6003-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6003-104">Stofna afurðarsniðmát fyrir forskilgreind afbrigði.</span><span class="sxs-lookup"><span data-stu-id="f6003-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="f6003-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f6003-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f6003-106">Þetta ferli er ætluð fyrir vöruhönnuð.</span><span class="sxs-lookup"><span data-stu-id="f6003-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="f6003-107">Stofna nýtt afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="f6003-107">Create a new product master</span></span>
1. <span data-ttu-id="f6003-108">Farðu í **Skoðunarrúðu > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="f6003-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="f6003-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f6003-109">Click **New**.</span></span>
3. <span data-ttu-id="f6003-110">Í reitnum **Afurðarnúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f6003-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="f6003-111">Hvert númer verður að vera einkvæmt.</span><span class="sxs-lookup"><span data-stu-id="f6003-111">The number must be unique.</span></span> <span data-ttu-id="f6003-112">Hægt er að setja inn númeraröð fyrir reitinn **Afurðarnúmer**.</span><span class="sxs-lookup"><span data-stu-id="f6003-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="f6003-113">Í þessu tilfelli þarf notandinn ekki að færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f6003-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="f6003-114">Í reitinn **Afurðarheiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f6003-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="f6003-115">Færa inn lýsandi afurðarheiti .</span><span class="sxs-lookup"><span data-stu-id="f6003-115">Enter a descriptive product name.</span></span> <span data-ttu-id="f6003-116">Gildið er sjálfgefið í leitarnafn, en hægt er að breyta því af notanda.</span><span class="sxs-lookup"><span data-stu-id="f6003-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="f6003-117">Í reitnum **Afurðavíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f6003-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f6003-118">Afurðavíddaflokkurinn ákvarðar hvaða 4 afurðarvíddir er hægt að nota til að stofna afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="f6003-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="f6003-119">Þetta dæmi notar flokk með lit og stærð.</span><span class="sxs-lookup"><span data-stu-id="f6003-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="f6003-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f6003-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f6003-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f6003-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="f6003-122">Sjálfgefin **Afbrigðistækni** er Forskilgreint afbrigði.</span><span class="sxs-lookup"><span data-stu-id="f6003-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="f6003-123">Þetta verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="f6003-123">This will be used for this example.</span></span>
8. <span data-ttu-id="f6003-124">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6003-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="f6003-125">Velja afurðavíddaflokka</span><span class="sxs-lookup"><span data-stu-id="f6003-125">Select product dimension groups</span></span>
1. <span data-ttu-id="f6003-126">Í reitnum **Litaflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f6003-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f6003-127">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f6003-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f6003-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f6003-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f6003-129">Í reitnum **Stærðarflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f6003-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f6003-130">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f6003-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f6003-131">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f6003-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="f6003-132">Bæta við Víddaflokkar</span><span class="sxs-lookup"><span data-stu-id="f6003-132">Add dimension groups</span></span>
1. <span data-ttu-id="f6003-133">Í **Aðgerðasvæði** er smellt á **Afurð**.</span><span class="sxs-lookup"><span data-stu-id="f6003-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="f6003-134">Smelltu á **Víddaflokkar** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f6003-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="f6003-135">Í reitnum **Geymsluvíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f6003-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f6003-136">Geymsluvíddir stjórna því hvernig vörur eru geymdar og teknar út af lager.</span><span class="sxs-lookup"><span data-stu-id="f6003-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="f6003-137">Til dæmis getur geymsluvídd innihaldið Svæði og vöruhús</span><span class="sxs-lookup"><span data-stu-id="f6003-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="f6003-138">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f6003-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f6003-139">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f6003-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f6003-140">Í reitnum **Rakningarvíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f6003-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="f6003-141">Rakningarvíddarflokkur ákvarðar hvaða víddaflokkar er hægt að bæta við afurð.</span><span class="sxs-lookup"><span data-stu-id="f6003-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="f6003-142">Til dæmis má nota rununúmer og raðnúmer til að rekja birgðavörur.</span><span class="sxs-lookup"><span data-stu-id="f6003-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="f6003-143">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f6003-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f6003-144">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f6003-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f6003-145">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6003-145">Click **OK**.</span></span>
10. <span data-ttu-id="f6003-146">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f6003-146">Click **Save**.</span></span>
11. <span data-ttu-id="f6003-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f6003-147">Close the page.</span></span>

