---
title: "Búa til nýtt vöruhúsaútlit"
description: "Þessi verklýsing sýnir hvernig á að setja upp upplýsingar um staðsetningar í vöruhúsi."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: is-is
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="c0957-103">Búa til nýtt vöruhúsaútlit</span><span class="sxs-lookup"><span data-stu-id="c0957-103">Create a new warehouse layout</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0957-104">Þessi verklýsing sýnir hvernig á að setja upp upplýsingar um staðsetningar í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="c0957-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="c0957-105">Þetta á aðeins við vöruhús sem eru stofnaðar með "grunn vöruhús" í kerfinu birgðastjórnun, ekki á við vöruhús sem er stofnað í vöruhúsakerfinu.</span><span class="sxs-lookup"><span data-stu-id="c0957-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="c0957-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="c0957-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="c0957-107">Stilla sjálfgefna afkastagetu staðsetningar</span><span class="sxs-lookup"><span data-stu-id="c0957-107">Set the default location capacity</span></span>
1. <span data-ttu-id="c0957-108">Fara í Birgðastjórnun > Uppsetning > Birgðir og færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="c0957-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="c0957-109">Smellt er á the Staðsetning flipa.</span><span class="sxs-lookup"><span data-stu-id="c0957-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="c0957-110">Í reitinn stöðluð breidd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="c0957-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="c0957-111">Í reitinn stöðluð dýpt skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="c0957-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="c0957-112">Í reitinn stöðluð hæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="c0957-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="c0957-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c0957-113">Click Save.</span></span>
7. <span data-ttu-id="c0957-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0957-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="c0957-115">Skilgreina heiti staðsetningarsniðið</span><span class="sxs-lookup"><span data-stu-id="c0957-115">Define the location name format</span></span>
1. <span data-ttu-id="c0957-116">Fara í Birgðastjórnun > Uppsetning > Birgðasundurliðun > Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="c0957-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="c0957-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c0957-117">Click New.</span></span>
3. <span data-ttu-id="c0957-118">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c0957-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="c0957-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c0957-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c0957-120">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c0957-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c0957-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c0957-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c0957-122">Víxla útvíkkun á liðnum heiti staðsetninga.</span><span class="sxs-lookup"><span data-stu-id="c0957-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="c0957-123">Valkostirnir í þessum hluta er að skilgreina sjálfgefið snið fyrir heiti staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="c0957-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="c0957-124">Í dæminu okkar mælt verður að innihalda gangnúmers, rekkanúmer og hillunúmer.</span><span class="sxs-lookup"><span data-stu-id="c0957-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="c0957-125">Stilltu valkostur hafa gang með á Já.</span><span class="sxs-lookup"><span data-stu-id="c0957-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="c0957-126">Stilltu valkostur hafa rekka með á Já.</span><span class="sxs-lookup"><span data-stu-id="c0957-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="c0957-127">Færa inn gildi í svæðinu Snið fyrir rekka.</span><span class="sxs-lookup"><span data-stu-id="c0957-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="c0957-128">Til dæmis: -##</span><span class="sxs-lookup"><span data-stu-id="c0957-128">For example: -##</span></span>  
11. <span data-ttu-id="c0957-129">Stilltu valkostur hafa hillu með á Já.</span><span class="sxs-lookup"><span data-stu-id="c0957-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="c0957-130">Færa inn gildi í svæðinu Snið fyrir í hillu.</span><span class="sxs-lookup"><span data-stu-id="c0957-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="c0957-131">Til dæmis: -##</span><span class="sxs-lookup"><span data-stu-id="c0957-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="c0957-132">Skilgreina Staðsetningar vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="c0957-132">Define warehouse locations</span></span>
1. <span data-ttu-id="c0957-133">Í aðgerðasvæðinu er smellt á vöruhús.</span><span class="sxs-lookup"><span data-stu-id="c0957-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="c0957-134">Smellt er á Leiðsagnarforrit Staðsetninga.</span><span class="sxs-lookup"><span data-stu-id="c0957-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="c0957-135">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-135">Click Next.</span></span>
4. <span data-ttu-id="c0957-136">Afveljið valkostinn úthlið</span><span class="sxs-lookup"><span data-stu-id="c0957-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="c0957-137">Af-velja valkostinn fjöldastaðsetningar</span><span class="sxs-lookup"><span data-stu-id="c0957-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="c0957-138">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-138">Click Next.</span></span>
7. <span data-ttu-id="c0957-139">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-139">Click Next.</span></span>
8. <span data-ttu-id="c0957-140">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-140">Click Next.</span></span>
9. <span data-ttu-id="c0957-141">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-141">Click Next.</span></span>
10. <span data-ttu-id="c0957-142">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-142">Click Next.</span></span>
11. <span data-ttu-id="c0957-143">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-143">Click Next.</span></span>
12. <span data-ttu-id="c0957-144">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-144">Click Next.</span></span>
    * <span data-ttu-id="c0957-145">Athugaðu að við efnislegar víddir sem sýna á þessari síðu eru þær sem var stillt í upphafi þessa ferlis.</span><span class="sxs-lookup"><span data-stu-id="c0957-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="c0957-146">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="c0957-146">Click Next.</span></span>
14. <span data-ttu-id="c0957-147">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="c0957-147">Click Finish.</span></span>
15. <span data-ttu-id="c0957-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0957-148">Close the page.</span></span>
16. <span data-ttu-id="c0957-149">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="c0957-149">Refresh the page.</span></span>

