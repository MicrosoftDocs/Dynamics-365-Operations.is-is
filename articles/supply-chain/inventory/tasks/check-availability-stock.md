---
title: Athuga framboð birgðaframboð
description: Þetta ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3f6f601d2d48ede2c4db198ac5438aa32e056d
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829778"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="8ef93-103">Athuga framboð birgðaframboð</span><span class="sxs-lookup"><span data-stu-id="8ef93-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ef93-104">Þetta ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="8ef93-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="8ef93-105">Það sýnir líka hvernig á að fá upplýsingar um framboð tengdar vöru.</span><span class="sxs-lookup"><span data-stu-id="8ef93-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="8ef93-106">Lagerbirgðir sem eru efnislegar birgðir eru tiltækar birgðir á lager – sem hafa verið keyptar, mótteknar og skráðar.</span><span class="sxs-lookup"><span data-stu-id="8ef93-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="8ef93-107">Lagerbirgðir innihalda tiltækar birgðir á lager, en einnig birgðirnar sem hafa verið pantaðar og er vænst en hafa ekki enn verið mótteknar og skráðar.</span><span class="sxs-lookup"><span data-stu-id="8ef93-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="8ef93-108">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="8ef93-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8ef93-109">Ef verið er að nota USMF má nota dæmagildin sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="8ef93-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="8ef93-110">Þessi verkefnum myndu venjulega vera framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="8ef93-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="8ef93-111">Kanna birgðir á lager fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="8ef93-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="8ef93-112">Fara í **Skoðunarglugga > Kerfiseiningar > Birgðastjórnun > Fyrirspurnir og skýrslur > Birgðir á lager**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="8ef93-113">Velurðu **línu vörunúmers**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-113">Select the **Item number** row.</span></span> <span data-ttu-id="8ef93-114">Til að spyrjast fyrir um birgðir á lager eftir vörunúmeri, veljið línuna þar sem Taflan er stillt á **Birgðir á lager** og reitur er stilltur á **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="8ef93-115">Í reitnum **Skilyrði** velurðu vöruna sem þú vilt gera fyrirspurn um.</span><span class="sxs-lookup"><span data-stu-id="8ef93-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="8ef93-116">Ef verið er að nota sýnigögn USMF-fyrirtækis er hægt að velja 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="8ef93-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="8ef93-117">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-117">Click **OK**.</span></span>
5. <span data-ttu-id="8ef93-118">Í **Aðgerðasvæði** er smellt á **Víddir**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="8ef93-119">Flipinn **Víddir** leyfir að velja hversu miklar upplýsingar til að sjá um birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="8ef93-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="8ef93-120">Ef þarf gögn sem tengjast frátekningu, verður að birta birgðavíddir á vörum sem nota ferli ítarlegrar vöruhúsa (WMS).</span><span class="sxs-lookup"><span data-stu-id="8ef93-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="8ef93-121">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-121">Click **OK**.</span></span>
7. <span data-ttu-id="8ef93-122">Á **Aðgerðasvæðinu** skal smellt á **Tengdar upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="8ef93-123">Ef það sést ekki, gæti þurft að smella á hnappinn „Úrfellingarmerki“ (…) til að sjá fleiri valkosti aðgerðasvæðis.</span><span class="sxs-lookup"><span data-stu-id="8ef93-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="8ef93-124">Smelltu á **Birgðayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-124">Click **Supply overview**.</span></span> <span data-ttu-id="8ef93-125">Flipinn **Birgðayfirlit** veitir birgðaupplýsingar fyrir tiltekna vöru, eins og magn á lager, afhendingartíma og lánardrottnaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8ef93-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="8ef93-126">Víkkið út hlutann **Á lager**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="8ef93-127">Stækkaðu hlutann **Lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="8ef93-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ef93-128">Close the page.</span></span>
12. <span data-ttu-id="8ef93-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ef93-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="8ef93-130">Athuga Efnislegar lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="8ef93-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="8ef93-131">Fara í **Skoðunarglugga > Kerfiseiningar > Vöruhússtjórnun > Fyrirspurnir og skýrslur > Efnislegar lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="8ef93-132">Í reitnum **Vörunúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8ef93-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="8ef93-133">Hægt er að nota svæðin Svæðis og Vöruhúss til að sía listann yfir vörur.</span><span class="sxs-lookup"><span data-stu-id="8ef93-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="8ef93-134">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="8ef93-134">Refresh the page.</span></span>
4. <span data-ttu-id="8ef93-135">Í **Aðgerðasvæði** er smellt á **Sýna víddir**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="8ef93-136">Birtingarflipinn Víddir gerir kleift að velja hversu miklar upplýsingar til að sjá um birgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="8ef93-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="8ef93-137">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-137">Click **OK**.</span></span>
6. <span data-ttu-id="8ef93-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ef93-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="8ef93-139">Athuga Birgðir eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="8ef93-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="8ef93-140">Fara í **Skoðunarglugga > Kerfiseiningar > Vöruhússtjórnun > Fyrirspurnir og skýrslur > Á lager eftir staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="8ef93-141">Í reitinn **Vöruhús** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8ef93-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="8ef93-142">Ef verið er að nota USMF sýnigögn fyrirtæki er hægt að nota '51'.</span><span class="sxs-lookup"><span data-stu-id="8ef93-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="8ef93-143">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="8ef93-143">Refresh the page.</span></span>
4. <span data-ttu-id="8ef93-144">Smelltu á **Sýna víddir**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="8ef93-145">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ef93-145">Click **OK**.</span></span>
6. <span data-ttu-id="8ef93-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8ef93-146">Close the page.</span></span>

