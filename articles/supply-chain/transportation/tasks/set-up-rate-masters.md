---
title: Setja upp sniðmát fyrir taxta
description: Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808991"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="045dc-103">Setja upp sniðmát fyrir taxta</span><span class="sxs-lookup"><span data-stu-id="045dc-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="045dc-104">Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="045dc-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="045dc-105">stjórnandi vörustjórnunar setur yfirleitt upp taxtasniðmát, allt eftir samningum sem voru undirritað með í flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="045dc-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="045dc-106">Í þessu tilfelli verður að setja upp taxtasniðmát fyrir flutningsaðila í lofti.</span><span class="sxs-lookup"><span data-stu-id="045dc-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="045dc-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="045dc-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="045dc-108">Setja upp sniðmát hlés</span><span class="sxs-lookup"><span data-stu-id="045dc-108">Set up break master</span></span>

1. <span data-ttu-id="045dc-109">Fara í **Flutningsstjórnun > Uppsetning >Einkunn > Sniðmát hlés**.</span><span class="sxs-lookup"><span data-stu-id="045dc-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="045dc-110">Sniðmát hlés eru notuð til að skilgreina uppbyggingu verðlagningar og rofstaði hennar.</span><span class="sxs-lookup"><span data-stu-id="045dc-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="045dc-111">Uppbygging verðlagningar notar lagskipt verðlagningu sem byggir á efnislegum víddum.</span><span class="sxs-lookup"><span data-stu-id="045dc-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="045dc-112">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="045dc-112">Select **New**.</span></span>
1. <span data-ttu-id="045dc-113">Í reitinn **Sniðmát hlés** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="045dc-114">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="045dc-115">Veljið gagnagerðina í reitnum **Gagnagerð**.</span><span class="sxs-lookup"><span data-stu-id="045dc-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="045dc-116">Í svæðinu **Samanburður** skal færa inn tegund samanburðar sem beðið er um (með virknitáknum).</span><span class="sxs-lookup"><span data-stu-id="045dc-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="045dc-117">Í reitinn **Skipta einingu** skal færa inn skiptieiningu.</span><span class="sxs-lookup"><span data-stu-id="045dc-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="045dc-118">Í hlutanum **Upplýsingar** skal stofna eins mörg hlé og þörf er á vegna verðlagsuppbyggingar.</span><span class="sxs-lookup"><span data-stu-id="045dc-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="045dc-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="045dc-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="045dc-120">Setja upp taxtasniðmát</span><span class="sxs-lookup"><span data-stu-id="045dc-120">Set up rate master</span></span>

1. <span data-ttu-id="045dc-121">Fara í **Flutningsstjórnun > Uppsetning >Einkunn > Taxtasniðmát**.</span><span class="sxs-lookup"><span data-stu-id="045dc-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="045dc-122">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="045dc-122">Select **New**.</span></span>
1. <span data-ttu-id="045dc-123">Í reitinn **Taxtasniðmát** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="045dc-124">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="045dc-125">Í reitnum **Lýsigagnakenni fyrir taxta** skal velja á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="045dc-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="045dc-126">Lýsigagnakenni fyrir taxta ákvarða gögn sem þarf fyrir taxtasniðmátið, þar sem það skilgreinir lýsigögn sem flutningsstjórnunarvél býst við með þessu taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="045dc-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="045dc-127">Í þessu dæmi skal velja valkostinn P2P.</span><span class="sxs-lookup"><span data-stu-id="045dc-127">For this example, select the P2P option.</span></span> <span data-ttu-id="045dc-128">Þetta er þegar skilgreint í sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="045dc-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="045dc-129">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="045dc-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="045dc-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="045dc-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="045dc-131">Setja upp taxtagrunn</span><span class="sxs-lookup"><span data-stu-id="045dc-131">Set up rate base</span></span>

1. <span data-ttu-id="045dc-132">Veljið **Taxtagrunnur**.</span><span class="sxs-lookup"><span data-stu-id="045dc-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="045dc-133">Taxtagrunn ákvarðar gengi farmflytjanda og hægt er að nota til að setja upp uppbyggingu taxta þar sem það byggir upp taxta á rofstöðum sem skilgreint í aðalgögnum skila.</span><span class="sxs-lookup"><span data-stu-id="045dc-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="045dc-134">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="045dc-134">Select **New**.</span></span>
3. <span data-ttu-id="045dc-135">Í reitnum **Taxtagrunnur** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="045dc-136">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="045dc-137">Í reitnum **Sniðmát hlés** skal velja á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="045dc-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="045dc-138">Sniðmát hlés eru notuð til að skilgreina uppbyggingu verðlagningar og rofstaði hennar.</span><span class="sxs-lookup"><span data-stu-id="045dc-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="045dc-139">Uppbygging verðlagningar notar lagskipt verðlagningu sem byggir á efnislegum víddum.</span><span class="sxs-lookup"><span data-stu-id="045dc-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="045dc-140">Í þessu dæmi notarðu þyngd.</span><span class="sxs-lookup"><span data-stu-id="045dc-140">For this example, use weight.</span></span> <span data-ttu-id="045dc-141">Þetta er þegar skilgreint í sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="045dc-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="045dc-142">Í listanum skal velja tengilinn í auðkenndu línunni.</span><span class="sxs-lookup"><span data-stu-id="045dc-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="045dc-143">Útvíkka hlutann **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="045dc-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="045dc-144">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="045dc-144">Select **New**.</span></span>
10. <span data-ttu-id="045dc-145">Í reitnum **Póstnúmer affermingar** frá skal slá inn ‚30301‘.</span><span class="sxs-lookup"><span data-stu-id="045dc-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="045dc-146">Í reitnum **Póstnúmer affermingar** til skal slá inn ‚30318‘.</span><span class="sxs-lookup"><span data-stu-id="045dc-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="045dc-147">Í reitnum **Landsvæði affermingar** skal slá inn ‚USA‘.</span><span class="sxs-lookup"><span data-stu-id="045dc-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="045dc-148">Í reitnum **<1,00** pund ritið '100'.</span><span class="sxs-lookup"><span data-stu-id="045dc-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="045dc-149">Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 1 pund.</span><span class="sxs-lookup"><span data-stu-id="045dc-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="045dc-150">Í reitnum **<5,00 pund** ritið '300'.</span><span class="sxs-lookup"><span data-stu-id="045dc-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="045dc-151">Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 5 pund.</span><span class="sxs-lookup"><span data-stu-id="045dc-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="045dc-152">Í reitnum **<20,00** pund ritið '500'.</span><span class="sxs-lookup"><span data-stu-id="045dc-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="045dc-153">Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 20 pund.</span><span class="sxs-lookup"><span data-stu-id="045dc-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="045dc-154">Í reitnum **<100,00** pund ritið ‚1.000'.</span><span class="sxs-lookup"><span data-stu-id="045dc-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="045dc-155">Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minna en 100 pund.</span><span class="sxs-lookup"><span data-stu-id="045dc-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="045dc-156">Í reitnum **<1.000,00** pund ritið '3000'.</span><span class="sxs-lookup"><span data-stu-id="045dc-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="045dc-157">Setja inn taxtann fyrir hvert pund ef heildarþyngd hleðslu er minni en 1.000 pund.</span><span class="sxs-lookup"><span data-stu-id="045dc-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="045dc-158">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="045dc-158">Select **Save**.</span></span>
19. <span data-ttu-id="045dc-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="045dc-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="045dc-160">Úthluta taxtagrunn</span><span class="sxs-lookup"><span data-stu-id="045dc-160">Assign rate base</span></span>

1. <span data-ttu-id="045dc-161">Víkka eða draga saman hlutann **Úthlutanir taxtagrunns**.</span><span class="sxs-lookup"><span data-stu-id="045dc-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="045dc-162">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="045dc-162">Select **New**.</span></span>
    * <span data-ttu-id="045dc-163">Hægt er að hafa nokkrar úthlutanir taxtagrunns fyrir hverja taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="045dc-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="045dc-164">Þetta gerir mögulegt að stofna nokkra mismunandi verðpunkta fyrir hvern farmflytjanda eftir áfangastaði, þjónustu eða mismunandi taxtagrunnum.</span><span class="sxs-lookup"><span data-stu-id="045dc-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="045dc-165">Í þessu ferli verður aðeins að stofna eina úthlutun taxtagrunns.</span><span class="sxs-lookup"><span data-stu-id="045dc-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="045dc-166">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="045dc-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="045dc-167">Í reitnum **Taxtagrunnur** skal velja á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="045dc-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="045dc-168">Í listanum skal velja tengilinn í auðkenndu línunni.</span><span class="sxs-lookup"><span data-stu-id="045dc-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="045dc-169">Í reitnum **Þjónusta** skal velja á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="045dc-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="045dc-170">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="045dc-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="045dc-171">Í listanum skal velja tengilinn í auðkenndu línunni.</span><span class="sxs-lookup"><span data-stu-id="045dc-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="045dc-172">Í Svæðið **Póstnúmer** þar sem sótt er, skal færa inn '98052'.</span><span class="sxs-lookup"><span data-stu-id="045dc-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="045dc-173">Tilgreina hvaða póstnúmer þessa úthlutun taxtagrunns á að gilda frá.</span><span class="sxs-lookup"><span data-stu-id="045dc-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="045dc-174">Í reitnum **Landsvæði** þar sem sótt er, skal slá inn ‚USA‘.</span><span class="sxs-lookup"><span data-stu-id="045dc-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="045dc-175">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="045dc-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]