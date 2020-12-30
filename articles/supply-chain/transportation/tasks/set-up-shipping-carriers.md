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
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430703"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="733c1-103">Setja upp farmflytjendur</span><span class="sxs-lookup"><span data-stu-id="733c1-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="733c1-104">Þetta efni sýnir hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta.</span><span class="sxs-lookup"><span data-stu-id="733c1-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="733c1-105">Samræmingaraðili við flutninga getur þá úthluta farmflytjanda á hleðslu á inn eða útleið.</span><span class="sxs-lookup"><span data-stu-id="733c1-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="733c1-106">Stofna nýtt farmflytjandi</span><span class="sxs-lookup"><span data-stu-id="733c1-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="733c1-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Uppsetning > Flutningsaðilar > Farmflytjendur**.</span><span class="sxs-lookup"><span data-stu-id="733c1-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="733c1-108">Veljið **Nýtt** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="733c1-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="733c1-109">Í reitnum **Farmflytjandi** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="733c1-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="733c1-111">Í reitnum **Stilling** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="733c1-112">Fyllið inn almennar upplýsingar um farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="733c1-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="733c1-113">Víxla útvíkkun á liðnum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="733c1-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="733c1-114">Kanna eða afhaka gátreitinn **Virkja farmflytjanda**.</span><span class="sxs-lookup"><span data-stu-id="733c1-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="733c1-115">Í reitnum **Lánardrottnalykill** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="733c1-116">Veljið lánardrottnalykil sem á að úthluta farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="733c1-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="733c1-117">Í reitnum **Gerð flutningstilboðs** velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="733c1-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="733c1-118">Veljið **Handvirkt** til að nota Tilboðssíðu flutninga eða velja **EDI** til að uppfæra tilboð með því að nota Rafræna gagnamillifærslu (EDI).</span><span class="sxs-lookup"><span data-stu-id="733c1-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="733c1-119">Merkja eða afmerkja gátreitinn **Virkja mat á farmflytjanda**.</span><span class="sxs-lookup"><span data-stu-id="733c1-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="733c1-120">Stofna nauðsynlega þjónustuna fyrir farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="733c1-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="733c1-121">Víxlaðu útvíkkun á liðnum **Þjónusta**.</span><span class="sxs-lookup"><span data-stu-id="733c1-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="733c1-122">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="733c1-122">Select **New**.</span></span>
3. <span data-ttu-id="733c1-123">Í reitinn **Flutningsþjónusta** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="733c1-124">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="733c1-125">Í reitnum **Flutningsaðferð** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="733c1-126">Setja upp aðsetur fyrir flutningsaðila (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="733c1-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="733c1-127">Víxlaðu útvíkkun á liðnum **Heimilisföng**.</span><span class="sxs-lookup"><span data-stu-id="733c1-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="733c1-128">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="733c1-128">Select **New**.</span></span>
3. <span data-ttu-id="733c1-129">Í reitinn **Nafn eða lýsing** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="733c1-130">Í reitnum **Land/landsvæði** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="733c1-131">Í reitnum **Póstnúmer** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="733c1-132">Í reitinn **Gata** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="733c1-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="733c1-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="733c1-134">Setja upp taxtaforstilling fyrir farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="733c1-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="733c1-135">Víxlaðu útvíkkun á liðnum **Taxtaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="733c1-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="733c1-136">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="733c1-136">Select **New**.</span></span>
3. <span data-ttu-id="733c1-137">Í reitinn **Taxtaforstilling** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="733c1-138">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="733c1-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="733c1-139">Í reitnum **Svæði** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="733c1-140">Í reitnum **Vöruhús** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="733c1-141">Í reitnum **Taxtavél** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="733c1-142">Veljið taxtavél sem er í samræmi við samning sem á að hafa með farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="733c1-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="733c1-143">Í reitnum **Taxtasniðmát** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="733c1-144">Í reitnum **Flutningstímavél** velurðu valkost úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="733c1-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="733c1-145">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="733c1-145">Select **Save**.</span></span>

