---
title: Stilla Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa92a581a96de6bed26b4a0c6601ebd9d5088347
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993426"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="87ab4-103">Stilla Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="87ab4-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87ab4-104">Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.</span><span class="sxs-lookup"><span data-stu-id="87ab4-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="87ab4-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="87ab4-105">Overview</span></span>

<span data-ttu-id="87ab4-106">Ljúktu aðeins við aðgerðirnar í þessu efnisatriði eftir að forskoðunarumhverfi fyrir Commerce hefur verið úthlutað.</span><span class="sxs-lookup"><span data-stu-id="87ab4-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="87ab4-107">Frekari upplýsingar um hvernig á að úthluta matsumhverfinu í Commerce er að finna í [Úthlutun Commerce-matsumhverfis](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="87ab4-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="87ab4-108">Eftir að Commerce-umhverfismatinu hefur verið úthlutað í heild sinni, þarf að ljúka nokkrum grunnstillingarskrefum eftir úthlutun áður en hægt er að leggja mat á umhverfið.</span><span class="sxs-lookup"><span data-stu-id="87ab4-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="87ab4-109">Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="87ab4-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="87ab4-110">Áður en byrjað er</span><span class="sxs-lookup"><span data-stu-id="87ab4-110">Before you start</span></span>

1. <span data-ttu-id="87ab4-111">Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="87ab4-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="87ab4-112">Farðu í verkefnið.</span><span class="sxs-lookup"><span data-stu-id="87ab4-112">Go to your project.</span></span>
1. <span data-ttu-id="87ab4-113">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="87ab4-114">Veldu umhverfið á listanum.</span><span class="sxs-lookup"><span data-stu-id="87ab4-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="87ab4-115">Í upplýsingum um umhverfið hægra megin skal velja **Skrá inn í umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="87ab4-116">Þér verður beint á Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="87ab4-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="87ab4-117">Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="87ab4-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="87ab4-118">Við úthlutun verkþátta eftir á í Commerce Headquarters skal ganga úr skugga um að **USRT** lögaðilinn sé alltaf valinn.</span><span class="sxs-lookup"><span data-stu-id="87ab4-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="87ab4-119">Grunnstilling sölustaðar</span><span class="sxs-lookup"><span data-stu-id="87ab4-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="87ab4-120">Tengdu starfsmann við kenni þitt</span><span class="sxs-lookup"><span data-stu-id="87ab4-120">Associate a worker with your identity</span></span>

<span data-ttu-id="87ab4-121">Til að tengja starfsmann við kennimerkið þitt skal fylgja þessum skrefum í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="87ab4-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="87ab4-122">Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Starfsmenn \> Starfskraftar**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="87ab4-123">Í listanum skal finna og velja eftirfarandi skrá: **000713 - Andrew Colette**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="87ab4-124">Á aðgerðasvæðinu skal velja **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="87ab4-125">Veldu **Tengja fyrirliggjandi kenni**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="87ab4-126">Í reitinn **Netfang** til hægri við **Leita með tölvupósti** skaltu slá inn netfangið þitt.</span><span class="sxs-lookup"><span data-stu-id="87ab4-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="87ab4-127">Velja **Leita**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-127">Select **Search**.</span></span>
1. <span data-ttu-id="87ab4-128">Veldu skrána með nafninu þínu.</span><span class="sxs-lookup"><span data-stu-id="87ab4-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="87ab4-129">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-129">Select **OK**.</span></span>
1. <span data-ttu-id="87ab4-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="87ab4-131">Virkja sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="87ab4-131">Activate Cloud POS</span></span>

<span data-ttu-id="87ab4-132">Til að virkja sölukerfi í skýinu skal fylgja þessum skrefum í LCS.</span><span class="sxs-lookup"><span data-stu-id="87ab4-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="87ab4-133">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="87ab4-134">Veldu umhverfið á listanum.</span><span class="sxs-lookup"><span data-stu-id="87ab4-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="87ab4-135">Í upplýsingum um umhverfið hægra megin skal velja **Skrá sig inn í sölukerfi í skýinu**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="87ab4-136">Veljið **Næst** til að opna svargluggann **Áður en þú hefst handa**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="87ab4-137">Skiljið **Vefslóð þjóns** eftir eins og hann er.</span><span class="sxs-lookup"><span data-stu-id="87ab4-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="87ab4-138">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-138">Select **Next**.</span></span>
1. <span data-ttu-id="87ab4-139">Skráðu þig inn með Microsoft Azure Active Directory (Azure AD)-reikningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="87ab4-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="87ab4-140">Undir **Heiti verslunar** skal velja **San Francisco** og síðan velja **Næst**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="87ab4-141">Undir **Skráning og tæki** velurðu **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="87ab4-142">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-142">Select **Activate**.</span></span> <span data-ttu-id="87ab4-143">Þú ert skráð/ur út og færð/ur á POS-innskráningarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="87ab4-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="87ab4-144">Þú getur nú skráð þig inn á Cloud POS-reynsluna með kenni rekstraraðila **000713** og lykilorði **123**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="87ab4-145">Settu upp vefsvæðið í Commerce</span><span class="sxs-lookup"><span data-stu-id="87ab4-145">Set up your site in Commerce</span></span>

<span data-ttu-id="87ab4-146">Til að hefja uppsetningu á matssvæðinu þínu í Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="87ab4-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="87ab4-147">Skráðu þig inn á vefsmið með því að nota slóðina sem þú skráðir þegar þú ræstir e-Commerce á meðan úthlutun stóð (sjá [Frumstilla rafræn viðskipti](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="87ab4-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="87ab4-148">Veldu svæðið **Fabrikam** til að opna uppsetningarglugga svæðisins.</span><span class="sxs-lookup"><span data-stu-id="87ab4-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="87ab4-149">Veldu lénið sem þú slóst inn þegar þú frumstilltir e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="87ab4-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="87ab4-150">Veldu **Fabrikam útvíkkuð netverslun** sem sjálfgefna rás.</span><span class="sxs-lookup"><span data-stu-id="87ab4-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="87ab4-151">(Gakktu úr skugga um að þú veljir **framlengda** netverslun.)</span><span class="sxs-lookup"><span data-stu-id="87ab4-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="87ab4-152">Veldu **en-us** sem sjálfgefið tungumál.</span><span class="sxs-lookup"><span data-stu-id="87ab4-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="87ab4-153">Hafðu gildið í reitnum **Slóð** eins og það er.</span><span class="sxs-lookup"><span data-stu-id="87ab4-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="87ab4-154">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-154">Select **OK**.</span></span> <span data-ttu-id="87ab4-155">Listinn yfir síður svæðisins birtist.</span><span class="sxs-lookup"><span data-stu-id="87ab4-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="87ab4-156">Virkja vinnslur</span><span class="sxs-lookup"><span data-stu-id="87ab4-156">Enable jobs</span></span>

<span data-ttu-id="87ab4-157">Til að virkja vinnslur í Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="87ab4-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="87ab4-158">Skráðu þig inn í umhverfið (HQ).</span><span class="sxs-lookup"><span data-stu-id="87ab4-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="87ab4-159">Notaðu valmyndina til vinstri til að fara í **Retail og Commerce \> Fyrirspurnir og skýrslur \> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="87ab4-160">Hinum skrefum þessa ferlis verður að vera lokið fyrir sérhverja af eftirfarandi vinnslum:</span><span class="sxs-lookup"><span data-stu-id="87ab4-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="87ab4-161">Vinna úr tilkynningartölvupósti smásölupöntunar</span><span class="sxs-lookup"><span data-stu-id="87ab4-161">Process retail order email notification</span></span>
    * <span data-ttu-id="87ab4-162">Tiltækar afurðir</span><span class="sxs-lookup"><span data-stu-id="87ab4-162">Product availability</span></span>
    * <span data-ttu-id="87ab4-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="87ab4-163">P-0001</span></span>
    * <span data-ttu-id="87ab4-164">Samstilla pantanavinnslu</span><span class="sxs-lookup"><span data-stu-id="87ab4-164">Synchronize orders job</span></span>

1. <span data-ttu-id="87ab4-165">Notaðu hraðsíuna til að leita að vinnslunni eftir heiti.</span><span class="sxs-lookup"><span data-stu-id="87ab4-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="87ab4-166">Ef staða vinnslunnar er **Í gangi** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="87ab4-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="87ab4-167">Veldu skrána.</span><span class="sxs-lookup"><span data-stu-id="87ab4-167">Select the record.</span></span>
    1. <span data-ttu-id="87ab4-168">Í aðgerðaglugganum á flipanum **Runuvinnsla** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="87ab4-169">Velja skal **Hætta við** og svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="87ab4-170">Einnig er hægt að stilla endurtekningartímabil á eina (1) mínútu fyrir eftirfarandi störf:</span><span class="sxs-lookup"><span data-stu-id="87ab4-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="87ab4-171">Vinna úr vinnslu vegna tilkynningar á smásölupöntun í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="87ab4-171">Process retail order email notification job</span></span>
* <span data-ttu-id="87ab4-172">P-0001 starf</span><span class="sxs-lookup"><span data-stu-id="87ab4-172">P-0001 job</span></span>
* <span data-ttu-id="87ab4-173">Samstilla pantanavinnslu</span><span class="sxs-lookup"><span data-stu-id="87ab4-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="87ab4-174">Keyra fulla samstillingu gagna</span><span class="sxs-lookup"><span data-stu-id="87ab4-174">Run full data synchronization</span></span>

<span data-ttu-id="87ab4-175">Til að keyra heildarsamstillingu gagna í Commerce skal fylgja þessum skrefum í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="87ab4-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="87ab4-176">Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Viðskiptaverkraðari \> Gagnagrunnur rásar**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="87ab4-177">Veldu rásina sem kallast **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="87ab4-178">Í aðgerðaglugganum velurðu **Samstilling allra gagna**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="87ab4-179">Skráðu **9999** sem dreifingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="87ab4-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="87ab4-180">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-180">Select **OK**.</span></span>
1. <span data-ttu-id="87ab4-181">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="87ab4-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="87ab4-182">Prófaðu kreditkortaupplýsingar til að gera prufukaup</span><span class="sxs-lookup"><span data-stu-id="87ab4-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="87ab4-183">Til að framkvæma prófunarviðskipti á vefnum geturðu notað eftirfarandi prufukreditkortaupplýsingar:</span><span class="sxs-lookup"><span data-stu-id="87ab4-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="87ab4-184">**Kortanúmer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="87ab4-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="87ab4-185">**Gildistími:** 10/20</span><span class="sxs-lookup"><span data-stu-id="87ab4-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="87ab4-186">**Sannprófunargildi korts (CVV)-kóði:** 737</span><span class="sxs-lookup"><span data-stu-id="87ab4-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87ab4-187">Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="87ab4-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="87ab4-188">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="87ab4-188">Next steps</span></span>

<span data-ttu-id="87ab4-189">Þegar úthlutunar- og grunnstillingarskrefum er lokið er hægt að byrja að nota matsumhverfið.</span><span class="sxs-lookup"><span data-stu-id="87ab4-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="87ab4-190">Notið vefslóð Commerce-vefsmiðins til að fara í höfundarviðmótið.</span><span class="sxs-lookup"><span data-stu-id="87ab4-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="87ab4-191">Notið vefslóð Commerce-vefsvæðis til að fara á vefviðmót viðskiptavinar smásölu.</span><span class="sxs-lookup"><span data-stu-id="87ab4-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="87ab4-192">Til að grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið skal skoða [Grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="87ab4-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87ab4-193">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="87ab4-193">Additional resources</span></span>

[<span data-ttu-id="87ab4-194">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="87ab4-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="87ab4-195">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="87ab4-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="87ab4-196">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="87ab4-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="87ab4-197">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="87ab4-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="87ab4-198">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="87ab4-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="87ab4-199">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="87ab4-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="87ab4-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="87ab4-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="87ab4-201">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="87ab4-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="87ab4-202">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="87ab4-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
