---
title: Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla kaup á netinu, sækja í verslun (BOPIS) í Microsoft Dynamics 365 Commerce matsumhverfi eftir að það hefur verið úthlutað.
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 219504da62fd4637ed01f9acbab32f873cef81b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795956"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="ce2b5-103">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ce2b5-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce2b5-104">Þetta efnisatriði útskýrir hvernig á að grunnstilla kaup á netinu, sækja í verslun (BOPIS) í Microsoft Dynamics 365 Commerce matsumhverfi eftir að umhverfinu hefur verið úthlutað.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="ce2b5-105">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="ce2b5-105">Prerequisite</span></span>

<span data-ttu-id="ce2b5-106">Ljúktu aðeins við aðgerðirnar í þessu efnisatriði eftir að matsumhverfi fyrir Commerce hefur verið úthlutað og grunnstillt.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="ce2b5-107">Frekari upplýsingar um hvernig á að úthluta og grunnstilla umhverfi þitt, sjá [Útvegun á Dynamics 365 Commerce matsumhverfi](provisioning-guide.md) og [Grunnstilla Dynamics 365 Commerce matsumhverfi](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="ce2b5-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="ce2b5-108">Eftir að Commerce umhverfið þitt hefur verið úthlutað og grunnstillt frá upphafi til enda geturðu notað þetta efnisatriði til að gera BOPIS atburðarás virka.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="ce2b5-109">Stilla sölustað</span><span class="sxs-lookup"><span data-stu-id="ce2b5-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="ce2b5-110">Grunnstilla Modern sölustað</span><span class="sxs-lookup"><span data-stu-id="ce2b5-110">Configure Modern POS</span></span>

<span data-ttu-id="ce2b5-111">BOPIS atburðarásir sem fela í sér kreditkortagreiðslu krefjast vélbúnaðarstöðvar.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="ce2b5-112">Vélbúnaðarstöð innbyggð í Modern sölustað fyrir Windows og Android biðlara.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="ce2b5-113">Ef þú notar sölukerfi í skýinu eða Modern sölustað fyrir iOS, verður biðlari sölustaðarins (POS) að vera paraður við samnýtta vélbúnaðarstöð.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="ce2b5-114">Þetta efnisatriði útskýrir hvernig á að stilla BOPIS fyrir Windows og Android biðlara.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="ce2b5-115">Frekari upplýsingar um hvernig á að setja upp vélbúnaðarstöðvar, sjá [Grunnstilling og uppsetning á vélbúnaðarstöð fyrir Retail](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="ce2b5-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="ce2b5-116">Opnaðu **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning sölustaðar \> Afgreiðslukassar**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="ce2b5-117">Veldu skráningu **SANFRAN-5** og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="ce2b5-118">Breyttu gildi reitsins **Forstilling vélbúnaðar** úr **HW002** í **HW001**, og smelltu síðan á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="ce2b5-119">Til að samstilla breytingarnar, opnaðu **Smásala og viðskipti \> Upplýsingatækni smásölu og viðskipta \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="ce2b5-120">Veldu dreifingaráætlun **1090** og veldu síðan **Keyra núna** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="ce2b5-121">Veldu **Já** og síðan **Í lagi** til að hefja samstillingu gagna.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="ce2b5-122">Setja upp Modern POS</span><span class="sxs-lookup"><span data-stu-id="ce2b5-122">Install Modern POS</span></span>

1. <span data-ttu-id="ce2b5-123">Opnaðu **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning sölustaðar \> Tæki**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="ce2b5-124">Veljið tæki **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="ce2b5-125">Veldu **Hlaða niður** á aðgerðarsvæðinu og veldu því næst **Skilgreiningarskrá**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="ce2b5-126">Veldu **Hlaða niður** og veldu því næst **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="ce2b5-127">Þegar niðurhal á **ModernPOSSetup.exe** skránni er lokið skaltu velja **Opna skrá**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Opna skrá](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="ce2b5-129">Veldu **Áfram** til að fara í gegnum uppsetningarferlið.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="ce2b5-130">Þegar uppsetningunni er lokið skaltu velja **Loka**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="ce2b5-131">Virkja Modern POS</span><span class="sxs-lookup"><span data-stu-id="ce2b5-131">Activate Modern POS</span></span>

1. <span data-ttu-id="ce2b5-132">Smelltu á **Upphafshnappinn** og sláðu inn **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="ce2b5-133">Veldu **Retail Modern POS** forritið til að ræsa virkjunina.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="ce2b5-134">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-134">Select **Next**.</span></span> <span data-ttu-id="ce2b5-135">Reitirnir **Vefslóð þjóns**, **Auðkenni tækis** og **Skráningarnúmer** ættu að vera forstilltir með því að nota upplýsingar úr skilgreiningarskránni sem þú hlóðst niður í fyrri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="ce2b5-136">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-136">Select **Activate**.</span></span>
5. <span data-ttu-id="ce2b5-137">Svargluggi sannvottunar opnast.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-137">An authentication dialog box appears.</span></span> <span data-ttu-id="ce2b5-138">Veldu reikninginn sem notar netfangið sem áður var tengt starfsmanni **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce2b5-139">Ef þú hefur ekki enn tengt starfsmann auðkennið þitt, þá mun virkjun ekki ná árangri.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="ce2b5-140">Í þessu tilfelli skaltu fylgja leiðbeiningunum undir hlutanum „Tengja starfsmann við auðkenni þitt“ í efnisatriðinu [Grunnstilla Dynamics 365 Commerce matsumhverfi](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="ce2b5-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="ce2b5-141">Þegar þú ert beðin/n um að láta fyrirtæki þitt stjórna tækinu skaltu velja **Aðeins þetta forrit**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="ce2b5-142">Þegar virkjun er lokið skaltu velja **Hefjast handa**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="ce2b5-143">Virkja BOPIS í Modern sölustað</span><span class="sxs-lookup"><span data-stu-id="ce2b5-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="ce2b5-144">Skráðu þig inn á Modern sölustað með því að nota **000713** sem kenni stjórnanda og **123** sem aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="ce2b5-145">Þegar sýnikennslumyndbandið er spilað skaltu velja gátreitina tvo neðst í vinstra horninu í svarglugganum og loka síðan svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="ce2b5-146">Ef þér er ekki beðið um að loka vaktinni, flettu til hægri á **Ávarpssíðunni** og smelltu á **Loka vakt**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="ce2b5-147">Þegar þú hefur skráð þig inn skaltu smella á **Framkvæma aðgerð utan skúffu** við kvaðningu.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="ce2b5-148">Flettu til hægri á **Ávarpssíðunni** og smelltu á aðgerðina **Velja vélbúnaðarstöð**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="ce2b5-149">Smelltu á **Stjórna** og stilltu valkostinn **Nota vélbúnaðarstöð** á **Kveikt** og smelltu síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="ce2b5-150">Skrá út af Sölustað og síðan skrá aftur inn.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="ce2b5-151">Eftir að þú hefur skráð þig inn skaltu velja **Opna nýja vakt** og velja síðan **Skúffu**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="ce2b5-152">Ljúktu við BOPIS-atburðarás</span><span class="sxs-lookup"><span data-stu-id="ce2b5-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="ce2b5-153">Búðu til pöntun í netverslun til að sækja í verslun</span><span class="sxs-lookup"><span data-stu-id="ce2b5-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="ce2b5-154">Farðu á slóðina sem þú tilgreindir í skrefinu [Frumstilla rafræn viðskipti](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) við grunnstillingu umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="ce2b5-155">Veldu hlut og veldu **Setja í körfu**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="ce2b5-156">Veldu innkaupapokasíðuna og smelltu á **Sækja þetta** fyrir pöntunarlínuna sem þú varst að bæta við.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="ce2b5-157">Í svargluggann **Velja verslun** slærðu inn **San Francisco** og smelltu síðan á **Leitarhnappinn**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="ce2b5-158">Finndu verslunina í San Francisco á niðurstöðulistanum og veldu **Sækja hér**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="ce2b5-159">Smelltu á **Skrá út sem gestur** á innkaupapokasíðunni.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ce2b5-160">Til að halda áfram og ljúka kaupum verður þú að samþykkja yfirlýsinguna um kökur.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="ce2b5-161">Þessi tilkynning birtist sem borði efst á síðunni þar sem gengið er frá kaupum.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="ce2b5-162">Færðu inn eftirfarandi upplýsingar fyrir greiðslumáta kreditkorta:</span><span class="sxs-lookup"><span data-stu-id="ce2b5-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="ce2b5-163">**Nafn korthafa:** Sláðu inn hvaða nafn sem er.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="ce2b5-164">**Kortanúmer:** Sláðu inn **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="ce2b5-165">**Gildistími:** Sláðu inn **10/20**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="ce2b5-166">**CVV-númer:** Sláðu inn **737**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ce2b5-167">Ekki skal undir neinum kringumstæðum reyna að nota raunverulegar kreditkortaupplýsingar á prófunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="ce2b5-168">Haltu áfram að ljúka kaupum með því að slá inn upplýsingar um heimilisfang greiðanda og smelltu síðan á **Vista og halda áfram**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="ce2b5-169">Smelltu á **Ljúka kaupum** þegar allt er til reiðu að leggja fram pöntunina.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="ce2b5-170">Samstilltu pantanir á netinu við skrifstofuna</span><span class="sxs-lookup"><span data-stu-id="ce2b5-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="ce2b5-171">Frekari upplýsingar um hvernig á að samstilla pantanir á netinu er að finna í [Bókun á netsölu og -greiðslum](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="ce2b5-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="ce2b5-172">Sækja pöntun í verslunina</span><span class="sxs-lookup"><span data-stu-id="ce2b5-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="ce2b5-173">Skráðu þig inn POS</span><span class="sxs-lookup"><span data-stu-id="ce2b5-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="ce2b5-174">Á **Upphafsskjánum** smellirðu á **Uppfylling pöntunar**</span><span class="sxs-lookup"><span data-stu-id="ce2b5-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="ce2b5-175">Veldu línuna úr pöntuninni sem var gerð á netinu á listanum yfir vörurnar sem á að sækja.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="ce2b5-176">Meðan pöntunarlínan er valin skaltu velja **Sækja**.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="ce2b5-177">Vörunni á línunni er bætt á færsluskjáinn og **$0,00** birtist sem upphæðin til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="ce2b5-178">Veldu upphæðina til greiðslu **$0,00** eða veldu hvaða greiðslumáta sem er til að ljúka við færsluna.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ce2b5-179">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="ce2b5-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="ce2b5-180">Netpantanir sem eru sóttar í sölustaðinn eru ekki með núlljafnaða upphæð til greiðslu</span><span class="sxs-lookup"><span data-stu-id="ce2b5-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="ce2b5-181">Þegar valið er að sækja vöru í verslun, ef upphæð til greiðslu er ekki 0 (núll), skal ganga úr skugga um að Modern sölustaður sé notaður og vélbúnaðarstöðin sé virk.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="ce2b5-182">Þegar sölukerfi í skýinu eða Modern sölustaður fyrir iOS er notað, skal ganga úr skugga um að samnýtta vélbúnaðarstöðin sé virk.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="ce2b5-183">Einhver tegund af virkri vélbúnaðarstöð er nauðsynleg til að sækja greiðslur sem gerðar voru á netinu.</span><span class="sxs-lookup"><span data-stu-id="ce2b5-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="ce2b5-184">Almenn vandamál varðandi greiðslutöku</span><span class="sxs-lookup"><span data-stu-id="ce2b5-184">General issues with payment capture</span></span>

<span data-ttu-id="ce2b5-185">Hvað öll almenn vandamál varðar, ættir þú fyrst að skoða tilvikaannála Modern sölustaðarins eða upplýsingaþjónustunnar á netinu (IIS).</span><span class="sxs-lookup"><span data-stu-id="ce2b5-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="ce2b5-186">Þú getur fundið þessar skrár undir eftirfarandi hnútum í tilvikaannál Windows:</span><span class="sxs-lookup"><span data-stu-id="ce2b5-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="ce2b5-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Modern sölustaður</span><span class="sxs-lookup"><span data-stu-id="ce2b5-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="ce2b5-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-vélbúnaðarstöð</span><span class="sxs-lookup"><span data-stu-id="ce2b5-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce2b5-189">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ce2b5-189">Additional resources</span></span>

[<span data-ttu-id="ce2b5-190">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="ce2b5-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ce2b5-191">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ce2b5-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="ce2b5-192">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ce2b5-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ce2b5-193">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ce2b5-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ce2b5-194">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="ce2b5-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ce2b5-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ce2b5-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ce2b5-196">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="ce2b5-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ce2b5-197">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="ce2b5-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="ce2b5-198">Adyen-greiðslutengill</span><span class="sxs-lookup"><span data-stu-id="ce2b5-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="ce2b5-199">Vista netgreiðslumáta með Adyen-tengli</span><span class="sxs-lookup"><span data-stu-id="ce2b5-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="ce2b5-200">Greiðsluyfirlit Omni-rásar</span><span class="sxs-lookup"><span data-stu-id="ce2b5-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]