---
title: Skilgreina forskoðunarumhverfi viðskipta
description: Þetta efni útskýrir hvernig á að stilla forsýningarumhverfi Microsoft Dynamics 365 Commerce eftir að það er úthlutað.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906140"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="bb24b-103">Skilgreina forskoðunarumhverfi viðskipta</span><span class="sxs-lookup"><span data-stu-id="bb24b-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bb24b-104">Þetta efni útskýrir hvernig á að stilla forsýningarumhverfi Microsoft Dynamics 365 Commerce eftir að það er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="bb24b-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="bb24b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="bb24b-105">Overview</span></span>

<span data-ttu-id="bb24b-106">Ljúktu verklagsreglunum í þessu efni aðeins eftir að forskoðunarumhverfi Commerce hefur verið útvegað.</span><span class="sxs-lookup"><span data-stu-id="bb24b-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="bb24b-107">Fyrir upplýsingar um hvernig skuli úthluta þér forskoðunarumhverfi Commerce skal sjá [Veita forskoðunarumhverfi Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="bb24b-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="bb24b-108">Eftir að forskoðunarumhverfi Commerce hefur verið úthlutað á öllum sviðum verður að ljúka eftirúthlutunarstillingarþrepunum áður en þú getur byrjað að meta umhverfið.</span><span class="sxs-lookup"><span data-stu-id="bb24b-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="bb24b-109">Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, og Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="bb24b-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="bb24b-110">Áður en byrjað er</span><span class="sxs-lookup"><span data-stu-id="bb24b-110">Before you start</span></span>

1. <span data-ttu-id="bb24b-111">Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="bb24b-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="bb24b-112">Farðu í verkefnið.</span><span class="sxs-lookup"><span data-stu-id="bb24b-112">Go to your project.</span></span>
1. <span data-ttu-id="bb24b-113">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="bb24b-114">Veldu umhverfið á listanum.</span><span class="sxs-lookup"><span data-stu-id="bb24b-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="bb24b-115">Í upplýsingum um umhverfið til hægri skaltu velja **Nánari upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="bb24b-116">Veldu **Skrá inn** til að opna valmynd og veldu síðan **Skrá inn í umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="bb24b-117">Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="bb24b-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="bb24b-118">Stilla sölustað í LCS</span><span class="sxs-lookup"><span data-stu-id="bb24b-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="bb24b-119">Tengdu starfsmann við kenni þitt</span><span class="sxs-lookup"><span data-stu-id="bb24b-119">Associate a worker with your identity</span></span>

<span data-ttu-id="bb24b-120">Fylgdu þessum skrefum til að tengja starfsmann við kenni þitt í LCS.</span><span class="sxs-lookup"><span data-stu-id="bb24b-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="bb24b-121">Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail \> Starfsmenn \> Starfskraftar**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="bb24b-122">Í listanum skal finna og velja eftirfarandi skrá: **000713 - Andrew Colette**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="bb24b-123">Í aðgerðarúðunni skal velja **Retail**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="bb24b-124">Veldu **Tengja fyrirliggjandi kenni**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="bb24b-125">Í reitinn **Netfang** til hægri við **Leita með tölvupósti** skaltu slá inn netfangið þitt.</span><span class="sxs-lookup"><span data-stu-id="bb24b-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="bb24b-126">Velja **Leita**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-126">Select **Search**.</span></span>
1. <span data-ttu-id="bb24b-127">Veldu skrána með nafninu þínu.</span><span class="sxs-lookup"><span data-stu-id="bb24b-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="bb24b-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-128">Select **OK**.</span></span>
1. <span data-ttu-id="bb24b-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="bb24b-130">Virkja sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="bb24b-130">Activate Cloud POS</span></span>

<span data-ttu-id="bb24b-131">Fylgdu þessum skrefum til að virkja Cloud POS í LCS.</span><span class="sxs-lookup"><span data-stu-id="bb24b-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="bb24b-132">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="bb24b-133">Veldu umhverfið á listanum.</span><span class="sxs-lookup"><span data-stu-id="bb24b-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="bb24b-134">Í upplýsingum um umhverfið til hægri skaltu velja **Nánari upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="bb24b-135">Veldu **Skrá inn** til að opna valmynd og veldu síðan **Skrá inn á sölustað í skýi** til að opna sölustaðinn (POS).</span><span class="sxs-lookup"><span data-stu-id="bb24b-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="bb24b-136">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-136">Select **Next**.</span></span>
1. <span data-ttu-id="bb24b-137">Skráðu þig inn með Microsoft Azure Active Directory (Azure AD)-reikningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="bb24b-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="bb24b-138">Undir **Verslunarheiti** velurðu **San Fransiskó**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="bb24b-139">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-139">Select **Next**.</span></span>
1. <span data-ttu-id="bb24b-140">Undir **Skráning og tæki** velurðu **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="bb24b-141">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-141">Select **Activate**.</span></span> <span data-ttu-id="bb24b-142">Þú ert skráð/ur út og færð/ur á POS-innskráningarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="bb24b-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="bb24b-143">Þú getur nú skráð þig inn á Cloud POS-reynsluna með kenni rekstraraðila **000713** og lykilorði **123**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="bb24b-144">Settu upp vefsvæðið í Commerce</span><span class="sxs-lookup"><span data-stu-id="bb24b-144">Set up your site in Commerce</span></span>

<span data-ttu-id="bb24b-145">Fylgdu þessum skrefum til að byrja að setja upp forskoðunarsíðuna í Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb24b-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bb24b-146">Skráðu þig inn á stjórnunartól vefsvæðisins með því að nota slóðina sem þú skrifaðir niður þegar þú frumstilltir e-Commerce við úthlutun (sjá [Frumstilla e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="bb24b-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="bb24b-147">Veldu svæðið **Fabrikam** til að opna uppsetningarglugga svæðisins.</span><span class="sxs-lookup"><span data-stu-id="bb24b-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="bb24b-148">Veldu lénið sem þú slóst inn þegar þú frumstilltir e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb24b-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="bb24b-149">Veldu **Fabrikam útvíkkuð netverslun** sem sjálfgefna rás.</span><span class="sxs-lookup"><span data-stu-id="bb24b-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="bb24b-150">(Gakktu úr skugga um að þú veljir **framlengda** netverslun.)</span><span class="sxs-lookup"><span data-stu-id="bb24b-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="bb24b-151">Veldu **en-us** sem sjálfgefið tungumál.</span><span class="sxs-lookup"><span data-stu-id="bb24b-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="bb24b-152">Hafðu gildið í reitnum **Slóð** eins og það er.</span><span class="sxs-lookup"><span data-stu-id="bb24b-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="bb24b-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-153">Select **OK**.</span></span> <span data-ttu-id="bb24b-154">Listinn yfir síður svæðisins birtist.</span><span class="sxs-lookup"><span data-stu-id="bb24b-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="bb24b-155">Virkja störf í Retail</span><span class="sxs-lookup"><span data-stu-id="bb24b-155">Enable jobs in Retail</span></span>

<span data-ttu-id="bb24b-156">Til að virkja vinnslur í Retail skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="bb24b-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="bb24b-157">Skráðu þig inn í umhverfið (HQ).</span><span class="sxs-lookup"><span data-stu-id="bb24b-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="bb24b-158">Notaðu valmyndina til vinstri til að fara í **Retail \> Fyrirspurnir og skýrslur \> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="bb24b-159">Hinum skrefum þessa ferlis verður að vera lokið fyrir sérhverja af eftirfarandi vinnslum:</span><span class="sxs-lookup"><span data-stu-id="bb24b-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="bb24b-160">Vinna úr tilkynningartölvupósti smásölupöntunar</span><span class="sxs-lookup"><span data-stu-id="bb24b-160">Process retail order email notification</span></span>
    * <span data-ttu-id="bb24b-161">Tiltækar afurðir</span><span class="sxs-lookup"><span data-stu-id="bb24b-161">Product availability</span></span>
    * <span data-ttu-id="bb24b-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="bb24b-162">P-0001</span></span>
    * <span data-ttu-id="bb24b-163">Samstilla pantanavinnslu</span><span class="sxs-lookup"><span data-stu-id="bb24b-163">Synchronize orders job</span></span>

1. <span data-ttu-id="bb24b-164">Notaðu hraðsíuna til að leita að vinnslunni eftir heiti.</span><span class="sxs-lookup"><span data-stu-id="bb24b-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="bb24b-165">Ef staða vinnslunnar er **Halda eftir** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="bb24b-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="bb24b-166">Veldu skrána.</span><span class="sxs-lookup"><span data-stu-id="bb24b-166">Select the record.</span></span>
    1. <span data-ttu-id="bb24b-167">Í aðgerðaglugganum á flipanum **Runuvinnsla** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="bb24b-168">Veldu **Bíður** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="bb24b-169">Keyra fulla samstillingu gagna í Retail</span><span class="sxs-lookup"><span data-stu-id="bb24b-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="bb24b-170">Fylgdu þessum skrefum til að keyra fulla samstillingu gagna í Retail.</span><span class="sxs-lookup"><span data-stu-id="bb24b-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="bb24b-171">Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail \> Uppsetning höfuðstöðva \> Retail Verkraðari \> Rásagagnagrunnur**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="bb24b-172">Á listanum til vinstri er rásin **Sjálfgefið** valin.</span><span class="sxs-lookup"><span data-stu-id="bb24b-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="bb24b-173">Veldu hina rásina sem er tiltæk.</span><span class="sxs-lookup"><span data-stu-id="bb24b-173">Select the other available channel.</span></span> <span data-ttu-id="bb24b-174">Þessi rás heitir **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="bb24b-175">Í aðgerðaglugganum velurðu **Samstilling allra gagna**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="bb24b-176">Skráðu **9999** sem dreifingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="bb24b-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="bb24b-177">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-177">Select **OK**.</span></span>
1. <span data-ttu-id="bb24b-178">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb24b-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="bb24b-179">Prófaðu kreditkortaupplýsingar til að gera prufukaup</span><span class="sxs-lookup"><span data-stu-id="bb24b-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="bb24b-180">Til að framkvæma prófunarviðskipti á vefnum geturðu notað eftirfarandi prufukreditkortaupplýsingar:</span><span class="sxs-lookup"><span data-stu-id="bb24b-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="bb24b-181">**Kortanúmer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="bb24b-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="bb24b-182">**Gildistími:** 10/20</span><span class="sxs-lookup"><span data-stu-id="bb24b-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="bb24b-183">**Sannprófunargildi korts (CVV)-kóði:** 737</span><span class="sxs-lookup"><span data-stu-id="bb24b-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb24b-184">Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bb24b-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb24b-185">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="bb24b-185">Next steps</span></span>

<span data-ttu-id="bb24b-186">Eftir að úthlutunar- og stillingarskrefunum er lokið ertu tilbúin/n til að meta forskoðunarumhverfið þitt.</span><span class="sxs-lookup"><span data-stu-id="bb24b-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="bb24b-187">Notaðu slóðina á stjórnunartólinu Commerce til að fara í höfundarupplifunina.</span><span class="sxs-lookup"><span data-stu-id="bb24b-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="bb24b-188">Notaðu slóðina á Commerce-svæðinu til að fara í svæðisreynslu smásöluviðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="bb24b-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="bb24b-189">Til að stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce skal sjá [Stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="bb24b-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb24b-190">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bb24b-190">Additional resources</span></span>

[<span data-ttu-id="bb24b-191">Yfirlit yfir forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="bb24b-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="bb24b-192">Úthluta forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="bb24b-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="bb24b-193">Stilltu valfrjálsa eiginleika fyrir forsýningarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="bb24b-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="bb24b-194">Algengar spurningar um forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="bb24b-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="bb24b-195">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="bb24b-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="bb24b-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="bb24b-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="bb24b-197">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="bb24b-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="bb24b-198">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="bb24b-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="bb24b-199">Hjálpartilföng fyrir Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="bb24b-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
