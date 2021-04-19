---
title: Skilgreina Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795860"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="3aecb-103">Skilgreina Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="3aecb-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3aecb-104">Þetta efnisatriði útskýrir hvernig á að grunnstilla Microsoft Dynamics 365 Commerce matsumhverfi eftir úthlutun þess.</span><span class="sxs-lookup"><span data-stu-id="3aecb-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="3aecb-105">Ljúktu aðeins við aðgerðirnar í þessu efnisatriði eftir að forskoðunarumhverfi fyrir Commerce hefur verið úthlutað.</span><span class="sxs-lookup"><span data-stu-id="3aecb-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="3aecb-106">Frekari upplýsingar um hvernig á að úthluta matsumhverfinu í Commerce er að finna í [Úthlutun Commerce-matsumhverfis](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="3aecb-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="3aecb-107">Eftir að Commerce-umhverfismatinu hefur verið úthlutað í heild sinni, þarf að ljúka nokkrum grunnstillingarskrefum eftir úthlutun áður en hægt er að leggja mat á umhverfið.</span><span class="sxs-lookup"><span data-stu-id="3aecb-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="3aecb-108">Til að klára þessi skref verður þú að nota Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3aecb-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="3aecb-109">Áður en byrjað er</span><span class="sxs-lookup"><span data-stu-id="3aecb-109">Before you start</span></span>

1. <span data-ttu-id="3aecb-110">Skráðu þig inn [LCS-gáttina](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="3aecb-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="3aecb-111">Farðu í verkefnið.</span><span class="sxs-lookup"><span data-stu-id="3aecb-111">Go to your project.</span></span>
1. <span data-ttu-id="3aecb-112">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3aecb-113">Veldu umhverfið á listanum.</span><span class="sxs-lookup"><span data-stu-id="3aecb-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="3aecb-114">Í upplýsingum um umhverfið hægra megin skal velja **Skrá inn í umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="3aecb-115">Þér verður beint á Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3aecb-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="3aecb-116">Gakktu úr skugga um að lögaðilinn **USRT** sé valinn efst í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="3aecb-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="3aecb-117">Við úthlutun verkþátta eftir á í Commerce Headquarters skal ganga úr skugga um að **USRT** lögaðilinn sé alltaf valinn.</span><span class="sxs-lookup"><span data-stu-id="3aecb-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="3aecb-118">Grunnstilling sölustaðar</span><span class="sxs-lookup"><span data-stu-id="3aecb-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="3aecb-119">Tengdu starfsmann við kenni þitt</span><span class="sxs-lookup"><span data-stu-id="3aecb-119">Associate a worker with your identity</span></span>

<span data-ttu-id="3aecb-120">Til að tengja starfsmann við kennimerkið þitt skal fylgja þessum skrefum í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3aecb-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="3aecb-121">Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Starfsmenn \> Starfskraftar**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="3aecb-122">Í listanum skal finna og velja eftirfarandi skrá: **000713 - Andrew Colette**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="3aecb-123">Á aðgerðasvæðinu skal velja **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="3aecb-124">Veldu **Tengja fyrirliggjandi kenni**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="3aecb-125">Í reitinn **Netfang** til hægri við **Leita með tölvupósti** skaltu slá inn netfangið þitt.</span><span class="sxs-lookup"><span data-stu-id="3aecb-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="3aecb-126">Velja **Leita**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-126">Select **Search**.</span></span>
1. <span data-ttu-id="3aecb-127">Veldu skrána með nafninu þínu.</span><span class="sxs-lookup"><span data-stu-id="3aecb-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="3aecb-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-128">Select **OK**.</span></span>
1. <span data-ttu-id="3aecb-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="3aecb-130">Virkja sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="3aecb-130">Activate Cloud POS</span></span>

<span data-ttu-id="3aecb-131">Til að virkja sölukerfi í skýinu skal fylgja þessum skrefum í LCS.</span><span class="sxs-lookup"><span data-stu-id="3aecb-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="3aecb-132">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3aecb-133">Veldu umhverfið á listanum.</span><span class="sxs-lookup"><span data-stu-id="3aecb-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="3aecb-134">Í upplýsingum um umhverfið hægra megin skal velja **Skrá sig inn í sölukerfi í skýinu**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="3aecb-135">Veljið **Næst** til að opna svargluggann **Áður en þú hefst handa**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="3aecb-136">Skiljið **Vefslóð þjóns** eftir eins og hann er.</span><span class="sxs-lookup"><span data-stu-id="3aecb-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="3aecb-137">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-137">Select **Next**.</span></span>
1. <span data-ttu-id="3aecb-138">Skráðu þig inn með Microsoft Azure Active Directory (Azure AD)-reikningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="3aecb-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="3aecb-139">Undir **Heiti verslunar** skal velja **San Francisco** og síðan velja **Næst**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="3aecb-140">Undir **Skráning og tæki** velurðu **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="3aecb-141">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-141">Select **Activate**.</span></span> <span data-ttu-id="3aecb-142">Þú ert skráð/ur út og færð/ur á POS-innskráningarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="3aecb-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="3aecb-143">Þú getur nú skráð þig inn á Cloud POS-reynsluna með kenni rekstraraðila **000713** og lykilorði **123**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="3aecb-144">Settu upp vefsvæðið í Commerce</span><span class="sxs-lookup"><span data-stu-id="3aecb-144">Set up your site in Commerce</span></span>

<span data-ttu-id="3aecb-145">Til að hefja uppsetningu á matssvæðinu þínu í Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3aecb-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3aecb-146">Skráðu þig inn á vefsmið með því að nota slóðina sem þú skráðir þegar þú ræstir e-Commerce á meðan úthlutun stóð (sjá [Frumstilla rafræn viðskipti](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="3aecb-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="3aecb-147">Veldu svæðið **Fabrikam** til að opna uppsetningarglugga svæðisins.</span><span class="sxs-lookup"><span data-stu-id="3aecb-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="3aecb-148">Veldu lénið sem þú slóst inn þegar þú frumstilltir e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="3aecb-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="3aecb-149">Veldu **Fabrikam útvíkkuð netverslun** sem sjálfgefna rás.</span><span class="sxs-lookup"><span data-stu-id="3aecb-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="3aecb-150">(Gakktu úr skugga um að þú veljir **framlengda** netverslun.)</span><span class="sxs-lookup"><span data-stu-id="3aecb-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="3aecb-151">Veldu **en-us** sem sjálfgefið tungumál.</span><span class="sxs-lookup"><span data-stu-id="3aecb-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="3aecb-152">Hafðu gildið í reitnum **Slóð** eins og það er.</span><span class="sxs-lookup"><span data-stu-id="3aecb-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="3aecb-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-153">Select **OK**.</span></span> <span data-ttu-id="3aecb-154">Listinn yfir síður svæðisins birtist.</span><span class="sxs-lookup"><span data-stu-id="3aecb-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="3aecb-155">Virkja vinnslur</span><span class="sxs-lookup"><span data-stu-id="3aecb-155">Enable jobs</span></span>

<span data-ttu-id="3aecb-156">Til að virkja vinnslur í Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3aecb-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3aecb-157">Skráðu þig inn í umhverfið (HQ).</span><span class="sxs-lookup"><span data-stu-id="3aecb-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="3aecb-158">Notaðu valmyndina til vinstri til að fara í **Retail og Commerce \> Fyrirspurnir og skýrslur \> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="3aecb-159">Hinum skrefum þessa ferlis verður að vera lokið fyrir sérhverja af eftirfarandi vinnslum:</span><span class="sxs-lookup"><span data-stu-id="3aecb-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="3aecb-160">Vinna úr tilkynningartölvupósti smásölupöntunar</span><span class="sxs-lookup"><span data-stu-id="3aecb-160">Process retail order email notification</span></span>
    * <span data-ttu-id="3aecb-161">Tiltækar afurðir</span><span class="sxs-lookup"><span data-stu-id="3aecb-161">Product availability</span></span>
    * <span data-ttu-id="3aecb-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="3aecb-162">P-0001</span></span>
    * <span data-ttu-id="3aecb-163">Samstilla pantanavinnslu</span><span class="sxs-lookup"><span data-stu-id="3aecb-163">Synchronize orders job</span></span>

1. <span data-ttu-id="3aecb-164">Notaðu hraðsíuna til að leita að vinnslunni eftir heiti.</span><span class="sxs-lookup"><span data-stu-id="3aecb-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="3aecb-165">Ef staða vinnslunnar er **Í gangi** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="3aecb-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="3aecb-166">Veldu skrána.</span><span class="sxs-lookup"><span data-stu-id="3aecb-166">Select the record.</span></span>
    1. <span data-ttu-id="3aecb-167">Í aðgerðaglugganum á flipanum **Runuvinnsla** velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="3aecb-168">Velja skal **Hætta við** og svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="3aecb-169">Einnig er hægt að stilla endurtekningartímabil á eina (1) mínútu fyrir eftirfarandi störf:</span><span class="sxs-lookup"><span data-stu-id="3aecb-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="3aecb-170">Vinna úr vinnslu vegna tilkynningar á smásölupöntun í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="3aecb-170">Process retail order email notification job</span></span>
* <span data-ttu-id="3aecb-171">P-0001 starf</span><span class="sxs-lookup"><span data-stu-id="3aecb-171">P-0001 job</span></span>
* <span data-ttu-id="3aecb-172">Samstilla pantanavinnslu</span><span class="sxs-lookup"><span data-stu-id="3aecb-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="3aecb-173">Keyra fulla samstillingu gagna</span><span class="sxs-lookup"><span data-stu-id="3aecb-173">Run full data synchronization</span></span>

<span data-ttu-id="3aecb-174">Til að keyra heildarsamstillingu gagna í Commerce skal fylgja þessum skrefum í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3aecb-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="3aecb-175">Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Viðskiptaverkraðari \> Gagnagrunnur rásar**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="3aecb-176">Veldu rásina sem kallast **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="3aecb-177">Í aðgerðaglugganum velurðu **Samstilling allra gagna**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="3aecb-178">Skráðu **9999** sem dreifingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="3aecb-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="3aecb-179">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-179">Select **OK**.</span></span>
1. <span data-ttu-id="3aecb-180">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3aecb-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="3aecb-181">Prófaðu kreditkortaupplýsingar til að gera prufukaup</span><span class="sxs-lookup"><span data-stu-id="3aecb-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="3aecb-182">Til að framkvæma prófunarviðskipti á vefnum geturðu notað eftirfarandi prufukreditkortaupplýsingar:</span><span class="sxs-lookup"><span data-stu-id="3aecb-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="3aecb-183">**Kortanúmer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="3aecb-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="3aecb-184">**Gildistími:** 10/20</span><span class="sxs-lookup"><span data-stu-id="3aecb-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="3aecb-185">**Sannprófunargildi korts (CVV)-kóði:** 737</span><span class="sxs-lookup"><span data-stu-id="3aecb-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3aecb-186">Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="3aecb-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3aecb-187">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="3aecb-187">Next steps</span></span>

<span data-ttu-id="3aecb-188">Þegar úthlutunar- og grunnstillingarskrefum er lokið er hægt að byrja að nota matsumhverfið.</span><span class="sxs-lookup"><span data-stu-id="3aecb-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="3aecb-189">Notið vefslóð Commerce-vefsmiðins til að fara í höfundarviðmótið.</span><span class="sxs-lookup"><span data-stu-id="3aecb-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="3aecb-190">Notið vefslóð Commerce-vefsvæðis til að fara á vefviðmót viðskiptavinar smásölu.</span><span class="sxs-lookup"><span data-stu-id="3aecb-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="3aecb-191">Til að grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið skal skoða [Grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="3aecb-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3aecb-192">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3aecb-192">Additional resources</span></span>

[<span data-ttu-id="3aecb-193">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="3aecb-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3aecb-194">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="3aecb-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="3aecb-195">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="3aecb-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3aecb-196">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="3aecb-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="3aecb-197">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="3aecb-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="3aecb-198">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="3aecb-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="3aecb-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="3aecb-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="3aecb-200">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="3aecb-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="3aecb-201">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="3aecb-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
