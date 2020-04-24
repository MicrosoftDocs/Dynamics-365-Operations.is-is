---
title: Setja upp farmflytjendur
description: Þetta efni sýnir hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201595"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="fe109-103">Setja upp farmflytjendur</span><span class="sxs-lookup"><span data-stu-id="fe109-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe109-104">Þetta efni sýnir hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta.</span><span class="sxs-lookup"><span data-stu-id="fe109-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="fe109-105">Samræmingaraðili við flutninga getur þá úthluta farmflytjanda á hleðslu á inn eða útleið.</span><span class="sxs-lookup"><span data-stu-id="fe109-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="fe109-106">Stofna nýtt farmflytjandi</span><span class="sxs-lookup"><span data-stu-id="fe109-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="fe109-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Uppsetning > Flutningsaðilar > Farmflytjendur**.</span><span class="sxs-lookup"><span data-stu-id="fe109-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="fe109-108">Veldu **Nýtt** í aðgerðarrúðunni.</span><span class="sxs-lookup"><span data-stu-id="fe109-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="fe109-109">Í reitnum **Farmflytjandi** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="fe109-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fe109-111">Í reitnum **Stilling** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="fe109-112">Fyllið inn almennar upplýsingar um farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="fe109-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="fe109-113">Víxla útvíkkun á liðnum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="fe109-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="fe109-114">Kanna eða afhaka gátreitinn **Virkja farmflytjanda**.</span><span class="sxs-lookup"><span data-stu-id="fe109-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="fe109-115">Í reitnum **Lánardrottnalykill** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="fe109-116">Veljið lánardrottnalykil sem á að úthluta farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="fe109-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="fe109-117">Í reitnum **Gerð flutningstilboðs** velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="fe109-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="fe109-118">Veljið **Handvirkt** til að nota Tilboðssíðu flutninga eða velja **EDI** til að uppfæra tilboð með því að nota Rafræna gagnamillifærslu (EDI).</span><span class="sxs-lookup"><span data-stu-id="fe109-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="fe109-119">Merkja eða afmerkja gátreitinn **Virkja mat á farmflytjanda**.</span><span class="sxs-lookup"><span data-stu-id="fe109-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="fe109-120">Stofna nauðsynlega þjónustuna fyrir farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="fe109-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="fe109-121">Víxlaðu útvíkkun á liðnum **Þjónusta**.</span><span class="sxs-lookup"><span data-stu-id="fe109-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="fe109-122">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="fe109-122">Select **New**.</span></span>
3. <span data-ttu-id="fe109-123">Í reitinn **Flutningsþjónusta** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="fe109-124">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fe109-125">Í reitnum **Flutningsaðferð** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="fe109-126">Setja upp aðsetur fyrir flutningsaðila (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="fe109-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="fe109-127">Víxlaðu útvíkkun á liðnum **Heimilisföng**.</span><span class="sxs-lookup"><span data-stu-id="fe109-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="fe109-128">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="fe109-128">Select **New**.</span></span>
3. <span data-ttu-id="fe109-129">Í reitinn **Nafn eða lýsing** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="fe109-130">Í reitnum **Land/landsvæði** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="fe109-131">Í reitnum **Póstnúmer** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="fe109-132">Í reitinn **Gata** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="fe109-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fe109-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="fe109-134">Setja upp taxtaforstilling fyrir farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="fe109-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="fe109-135">Víxlaðu útvíkkun á liðnum **Taxtaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="fe109-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="fe109-136">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="fe109-136">Select **New**.</span></span>
3. <span data-ttu-id="fe109-137">Í reitinn **Taxtaforstilling** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="fe109-138">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fe109-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fe109-139">Í reitnum **Svæði** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="fe109-140">Í reitnum **Vöruhús** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="fe109-141">Í reitnum **Taxtavél** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="fe109-142">Veljið taxtavél sem er í samræmi við samning sem á að hafa með farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="fe109-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="fe109-143">Í reitnum **Taxtasniðmát** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="fe109-144">Í reitnum **Flutningstímavél** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fe109-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="fe109-145">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="fe109-145">Select **Save**.</span></span>

