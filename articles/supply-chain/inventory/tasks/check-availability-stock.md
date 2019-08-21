---
title: Athuga framboð birgðaframboð
description: Þetta ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b78b2e4ec3179450d635857353846c9bcb23eed
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795173"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="6fb19-103">Athuga framboð birgðaframboð</span><span class="sxs-lookup"><span data-stu-id="6fb19-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6fb19-104">Þetta ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="6fb19-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="6fb19-105">Það sýnir líka hvernig á að fá upplýsingar um framboð tengdar vöru.</span><span class="sxs-lookup"><span data-stu-id="6fb19-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="6fb19-106">Lagerbirgðir sem eru efnislegar birgðir eru tiltækar birgðir á lager – sem hefur verið keypt, móttekin og skráð.</span><span class="sxs-lookup"><span data-stu-id="6fb19-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="6fb19-107">Lagerbirgðir inniheldur tiltækar birgðir á lager, en einnig birgðirnar sem hefur verið pöntuð er vænst en hefur enn ekki verið móttekin og skráð.</span><span class="sxs-lookup"><span data-stu-id="6fb19-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="6fb19-108">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="6fb19-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="6fb19-109">Ef verið er að nota USMF má nota dæmagildin sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="6fb19-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="6fb19-110">Þessi verkefnum myndu venjulega vera framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="6fb19-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="6fb19-111">Kanna birgðir á lager fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="6fb19-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="6fb19-112">Fara í birgðastjórnun > Fyrirspurnir og skýrslur > Birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="6fb19-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="6fb19-113">Velurðu línu vörunúmers.</span><span class="sxs-lookup"><span data-stu-id="6fb19-113">Select the Item number row.</span></span>
    * <span data-ttu-id="6fb19-114">Til að spyrjast fyrir um birgðir á lager eftir vörunúmeri, veljið línuna þar sem Taflan er stillt á birgðum á lager og reitur er stillt á vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="6fb19-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="6fb19-115">Í svæðinu skilyrði, Veldu vöru sem þú vilt telja.</span><span class="sxs-lookup"><span data-stu-id="6fb19-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="6fb19-116">Ef verið er að nota sýnigögn USMF-fyrirtækis er hægt að velja 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="6fb19-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="6fb19-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6fb19-117">Click OK.</span></span>
5. <span data-ttu-id="6fb19-118">Smellt er á Víddir.</span><span class="sxs-lookup"><span data-stu-id="6fb19-118">Click Dimensions.</span></span>
    * <span data-ttu-id="6fb19-119">Flipinn Víddir leyfir að velja hversu miklar upplýsingar til að sjá um birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="6fb19-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="6fb19-120">Ef þarf gögn sem tengjast frátekningu, verður að birta birgðavíddir á vörum sem nota ferli ítarlegrar vöruhúsa (WHS).</span><span class="sxs-lookup"><span data-stu-id="6fb19-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="6fb19-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6fb19-121">Click OK.</span></span>
7. <span data-ttu-id="6fb19-122">Á Aðgerðasvæðinu skal smellt á Tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="6fb19-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="6fb19-123">Ef það sést ekki, gæti þurft að smella á hnappinn Ellipsis (...) til að sjá valkostir frekari aðgerða.</span><span class="sxs-lookup"><span data-stu-id="6fb19-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="6fb19-124">Smellt er á birgðayfirlitið.</span><span class="sxs-lookup"><span data-stu-id="6fb19-124">Click Supply overview.</span></span>
    * <span data-ttu-id="6fb19-125">yfirlitsflipann Framboð veitir birgðaupplýsingar fyrir tiltekna vöru, eins og magn á lager, afhendingartíma og lánardrottnaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="6fb19-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="6fb19-126">Víkkið út hlutann Á lager.</span><span class="sxs-lookup"><span data-stu-id="6fb19-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="6fb19-127">Stækka hlutann Lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="6fb19-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="6fb19-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6fb19-128">Close the page.</span></span>
12. <span data-ttu-id="6fb19-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6fb19-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="6fb19-130">Athuga Efnislegar lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="6fb19-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="6fb19-131">Fara í vöruhúsakerfi > Fyrirspurnir og skýrslur > Efnislegar birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="6fb19-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="6fb19-132">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6fb19-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6fb19-133">Hægt er að nota svæðin Svæðis og Vöruhúss til að sía listann yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="6fb19-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="6fb19-134">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="6fb19-134">Refresh the page.</span></span>
4. <span data-ttu-id="6fb19-135">Smellt er á Sýna víddir.</span><span class="sxs-lookup"><span data-stu-id="6fb19-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="6fb19-136">Birtingarflipinn Víddir gerir kleift að velja hversu miklar upplýsingar til að sjá um birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="6fb19-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="6fb19-137">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6fb19-137">Click OK.</span></span>
6. <span data-ttu-id="6fb19-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6fb19-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="6fb19-139">Athuga Birgðir eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="6fb19-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="6fb19-140">Fara í vöruhúsakerfi > Fyrirspurnir og skýrslur > Á lager eftir staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="6fb19-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="6fb19-141">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6fb19-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="6fb19-142">Ef verið er að nota USMF sýnigögn fyrirtæki er hægt að nota '51'.</span><span class="sxs-lookup"><span data-stu-id="6fb19-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="6fb19-143">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="6fb19-143">Refresh the page.</span></span>
4. <span data-ttu-id="6fb19-144">Smellt er á Sýna víddir.</span><span class="sxs-lookup"><span data-stu-id="6fb19-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="6fb19-145">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6fb19-145">Click OK.</span></span>
6. <span data-ttu-id="6fb19-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6fb19-146">Close the page.</span></span>

