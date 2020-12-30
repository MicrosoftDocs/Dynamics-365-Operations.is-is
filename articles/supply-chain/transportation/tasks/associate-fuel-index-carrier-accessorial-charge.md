---
title: Tengja eldsneytisvísi flutningsaðila sem aukagjald
description: Þessar leiðbeiningar sýnir hvernig stofna á aukaúthlutunina, aukalegt gjald flutningsaðila, aukalega sniðmát fyrir eldsneytisálag og tengja eldsneytisvísi flutningsaðila við flutningsaðila.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91d49c2ccdc274632e3acf94b836e19dc6cdaa8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430708"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="dd0a1-103">Tengja eldsneytisvísi flutningsaðila sem aukagjald</span><span class="sxs-lookup"><span data-stu-id="dd0a1-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd0a1-104">Þessar leiðbeiningar sýnir hvernig stofna á aukaúthlutunina, aukalegt gjald flutningsaðila, aukalega sniðmát fyrir eldsneytisálag og tengja eldsneytisvísi flutningsaðila við flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="dd0a1-105">Það Þarf að vera uppsettur eldsneytisvísi flutningsaðila áður en þessari leiðbeiningar er keyrð.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="dd0a1-106">Hægt er að nota leiðbeiningarnar "Setja upp eldsneytisvísi flutningsaðila" til að gera þetta.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="dd0a1-107">Þessi uppsetningarverk eru yfirleitt gert með stjórnanda í Vörustjórnun.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="dd0a1-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="dd0a1-109">Stofna aukalegt sniðmát</span><span class="sxs-lookup"><span data-stu-id="dd0a1-109">Create an accessorial master</span></span>
1. <span data-ttu-id="dd0a1-110">Fara í flutningsstjórnun > Uppsetning > Einkunn > Aukalegt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="dd0a1-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-111">Click New.</span></span>
3. <span data-ttu-id="dd0a1-112">Í reitinn Aukalegt sniðmát skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="dd0a1-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dd0a1-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="dd0a1-115">Stofna aukagjöld flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="dd0a1-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="dd0a1-116">Fara í flutningsstjórnun > Uppsetning >Einkunn > Aukagjöld flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="dd0a1-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-117">Click New.</span></span>
3. <span data-ttu-id="dd0a1-118">Færa inn gildi í reitnum aukalegt kenni flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="dd0a1-119">Í reitnum Farmflytjandi skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dd0a1-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dd0a1-121">Í þessu dæmi skal velja Flutningsaðila með vörubíla.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="dd0a1-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="dd0a1-123">Í reitnum Flutningsþjónusta skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="dd0a1-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dd0a1-125">Í reitnum Aukalegt sniðmát skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dd0a1-126">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dd0a1-127">Í þessu dæmi skal velja nýstofnuð aukalega sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="dd0a1-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="dd0a1-129">Stofna aukalega úthlutun</span><span class="sxs-lookup"><span data-stu-id="dd0a1-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="dd0a1-130">Smellt er á úthlutanir aukaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="dd0a1-131">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-131">Click New.</span></span>
3. <span data-ttu-id="dd0a1-132">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dd0a1-133">Víxla útvíkkun á liðnum skilyrði.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="dd0a1-134">Í skilyrðunum er Hægt er að velja að nota alltaf eldsneytisálag eða í þessu dæmi velja að það á einungis við innan ákveðið svæði.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="dd0a1-135">Í reitinn Póstnúmer frá skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="dd0a1-136">Í reitinn Póstnúmer til skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="dd0a1-137">Víxla útvíkkun á liðnum útreikningur.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="dd0a1-138">Í hlutanum útreikning er hægt að tilgreina hvernig á að reikna út eldsneytisálag.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="dd0a1-139">Þessi útreikningur fer eftir aukalegu einunguna sem þú valdir sem grunn fyrir útreikninga.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="dd0a1-140">Veljið í svæðinu aukagjalds skal velja 'Eldsneytisálag'.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="dd0a1-141">Veljið 'Vegalengd' í svæðinu aukaleg eining.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="dd0a1-142">Í reitnum Svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="dd0a1-143">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dd0a1-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="dd0a1-145">Uppfæra taxtaforstillingu flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="dd0a1-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="dd0a1-146">Farið í flutningsstjórnun > Uppsetning > Flutningsaðilar > Farmflytjendur.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="dd0a1-147">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dd0a1-148">Víxla útvíkkun á liðnum taxtaforstillingar.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="dd0a1-149">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-149">Click Edit.</span></span>
5. <span data-ttu-id="dd0a1-150">Í reitnum Eldsneytisvísir flutningsaðila skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dd0a1-151">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="dd0a1-152">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd0a1-152">Click Save.</span></span>

