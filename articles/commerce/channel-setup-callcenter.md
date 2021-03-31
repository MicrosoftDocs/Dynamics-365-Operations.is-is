---
title: Setja upp rás símavers
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja rás símavers í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 878774c8e5485211525e7e7b63973173f6874b26
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218370"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="8172a-103">Uppsetning símaversrásar</span><span class="sxs-lookup"><span data-stu-id="8172a-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8172a-104">Í þessu efnisatriði er lýst hvernig eigi að stofna nýja rás símavers í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8172a-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8172a-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="8172a-105">Overview</span></span>


<span data-ttu-id="8172a-106">Í Dynamics 365 Commerce er símaver tegund Commerce-rásar sem hægt er að skilgreina í forritinu.</span><span class="sxs-lookup"><span data-stu-id="8172a-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="8172a-107">Að skilgreina rás fyrir símaþjónustueiningar þínar gerir kerfinu kleift að binda tiltekin gögn og sjálfgildi pöntunarvinnslu við sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="8172a-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="8172a-108">Þó fyrirtæki geti skilgreint margar símaversrásir í Commerce, er mikilvægt að hafa í huga að stakur notandi getur aðeins verið tengd einni símaversrás.</span><span class="sxs-lookup"><span data-stu-id="8172a-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="8172a-109">Áður en ný rás símavers er stofnuð skaltu ganga úr skugga um að þú hafir lokið við [Skilyrði fyrir rásauppsetningu](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="8172a-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="8172a-110">Stofna og stilla nýja rás símavers</span><span class="sxs-lookup"><span data-stu-id="8172a-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="8172a-111">Til að stofna og stilla nýja rás símavers fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8172a-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="8172a-112">Í yfirlitssvæðinu ferðu í **Retail og Commerce \> Rásir \> Símaver \> Öll símaver**.</span><span class="sxs-lookup"><span data-stu-id="8172a-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="8172a-113">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8172a-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8172a-114">Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.</span><span class="sxs-lookup"><span data-stu-id="8172a-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="8172a-115">Veldu viðeigandi **Lögaðila** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="8172a-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="8172a-116">Veldu viðeigandi staðsetningu **vöruhúss** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="8172a-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="8172a-117">Þessi staðsetning verður notuð sem sjálfgildi í sölupöntunum sem voru stofnaðar fyrir þessa símaversrás, nema önnur sjálfgildi hafi verið skilgreind á viðskiptavinar- eða vörustigi.</span><span class="sxs-lookup"><span data-stu-id="8172a-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="8172a-118">Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="8172a-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="8172a-119">Þessi gögn eru notuð til að aðstoða við sjálfval þegar nýjar viðskiptavinafærslur eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="8172a-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="8172a-120">Þegar búið er til pantanir í símaverum er ekki ráðlegt að búa til pantanir fyrir sjálfgefna viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="8172a-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="8172a-121">Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="8172a-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="8172a-122">Þegar pantanir símavers eru búnar til og unnar er tilkynningasniðið notað til að kalla fram sjálfvirkar tilkynningar um tölvupóst til viðskiptavina með upplýsingar um stöðu pöntunar.</span><span class="sxs-lookup"><span data-stu-id="8172a-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="8172a-123">Gefa upp upplýsingakóða **verðhnekkingar**.</span><span class="sxs-lookup"><span data-stu-id="8172a-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="8172a-124">Þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.</span><span class="sxs-lookup"><span data-stu-id="8172a-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="8172a-125">Þessi upplýsingakóði veitir sett af ástæðukóða sem notandinn verður beðinn um að velja úr þegar hann notar verðhækkunaraðgerðina í pöntun símavers.</span><span class="sxs-lookup"><span data-stu-id="8172a-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="8172a-126">Gefðu upp upplýsingakóðann **Biðkóði**.</span><span class="sxs-lookup"><span data-stu-id="8172a-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="8172a-127">Þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.</span><span class="sxs-lookup"><span data-stu-id="8172a-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="8172a-128">Þessi upplýsingakóði veitir sett af valkvæðum ástæðukóðum sem notandinn verður beðinn um að velja úr þegar hann setur pöntun í bið.</span><span class="sxs-lookup"><span data-stu-id="8172a-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="8172a-129">Gefðu upp upplýsingakóðann **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="8172a-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="8172a-130">Þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.</span><span class="sxs-lookup"><span data-stu-id="8172a-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="8172a-131">Þessi upplýsingakóði veitir þann fjölda ástæðukóða sem notandinn getur valið um þegar hann notar pöntunarlánatækni í símaþjónustuver til að veita viðskiptavinum ýmsar endurgreiðslur af þjónustuástæðum.</span><span class="sxs-lookup"><span data-stu-id="8172a-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="8172a-132">Valfrjálst: setja upp fjárhagsvíddir á flýtiflipanum **Fjárhagsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="8172a-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="8172a-133">Málin sem hér eru færð inn munu sjálfkrafa vera í öllum sölupöntunum sem búnar eru til í þessari stöðvarstöð.</span><span class="sxs-lookup"><span data-stu-id="8172a-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="8172a-134">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8172a-134">Click **Save**.</span></span>

<span data-ttu-id="8172a-135">Eftirfarandi mynd sýnir stofnun nýrrar símaversrásar.</span><span class="sxs-lookup"><span data-stu-id="8172a-135">The following image shows the creation of a new call center channel.</span></span>

![Ný rás símavers](media/channel-setup-callcenter-1.png)

<span data-ttu-id="8172a-137">Eftirfarandi mynd sýnir dæmi um símaversrás.</span><span class="sxs-lookup"><span data-stu-id="8172a-137">The following image shows an example call center channel.</span></span>

![Dæmi um rás símavers](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="8172a-139">Viðbótaruppsetning grunnrásar</span><span class="sxs-lookup"><span data-stu-id="8172a-139">Additional channel setup</span></span>

<span data-ttu-id="8172a-140">Viðbótarupplýsingar sem krafist er fyrir uppsetningu símaversrásar fela í sér uppsetningu á greiðslumáta og afhendingaraðferðum.</span><span class="sxs-lookup"><span data-stu-id="8172a-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="8172a-141">Eftirfarandi mynd sýnir uppsetningarkostina **Afhendingarmáta** og **Greiðslumáta** á flipanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="8172a-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Viðbótar uppsetningaraðgerðir símaversrásar](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="8172a-143">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="8172a-143">Set up payment methods</span></span>

<span data-ttu-id="8172a-144">Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.</span><span class="sxs-lookup"><span data-stu-id="8172a-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="8172a-145">Notendur verða að velja úr fyrirfram skilgreindum greiðsluaðferðum til að tengja þær við símaversrásina.</span><span class="sxs-lookup"><span data-stu-id="8172a-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="8172a-146">Áður en þú setur upp greiðslumáta símaþjónustunnar skaltu fyrst setja upp greiðslumáta þína í **Verslun og verslun \> Uppsetning rásar \> Greiðslumátar \> Greiðslumátar**.</span><span class="sxs-lookup"><span data-stu-id="8172a-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="8172a-147">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.</span><span class="sxs-lookup"><span data-stu-id="8172a-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="8172a-148">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8172a-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8172a-149">Veldu greiðslumáta úr fyrirfram skilgreindum greiðslum í boði á leiðsögubrautinni.</span><span class="sxs-lookup"><span data-stu-id="8172a-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="8172a-150">Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="8172a-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="8172a-151">Að því er varðar kreditkort, gjafakort eða vildarkort þarf viðbótar uppsetningu með því að velja virknina **Uppsetning korta**.</span><span class="sxs-lookup"><span data-stu-id="8172a-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="8172a-152">Stilla rétt bókun reikninga fyrir greiðslugerðina í hlutanum **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="8172a-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="8172a-153">Í aðgerðasvæðinu smellirðu á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8172a-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="8172a-154">Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.</span><span class="sxs-lookup"><span data-stu-id="8172a-154">The following image shows an example of a cash payment method.</span></span>

![Dæmi um greiðslumáta](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="8172a-156">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="8172a-156">Set up modes of delivery</span></span>

<span data-ttu-id="8172a-157">Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.</span><span class="sxs-lookup"><span data-stu-id="8172a-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="8172a-158">Fylgdu þessum skrefum til að breyta eða bæta við afhendingaraðferð sem á að tengjast símaþjónustuverinu.</span><span class="sxs-lookup"><span data-stu-id="8172a-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="8172a-159">Veldu af sendingarformi símaþjónustuvera **Hafa umsjón með afhendingaraðferðum**</span><span class="sxs-lookup"><span data-stu-id="8172a-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="8172a-160">Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.</span><span class="sxs-lookup"><span data-stu-id="8172a-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="8172a-161">Í kaflanum **Smásölurásir** smellirðu á **Bæta við línu** til að bæta við símaversrás.</span><span class="sxs-lookup"><span data-stu-id="8172a-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="8172a-162">Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.</span><span class="sxs-lookup"><span data-stu-id="8172a-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="8172a-163">Gakktu úr skugga um að afhendingarstíllinn hafi verið stilltur með gögnum á flýtiflipunum **Vörur** og **Heimilisföng**.</span><span class="sxs-lookup"><span data-stu-id="8172a-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="8172a-164">Ef engar vörur eða afhendingarföng eru gild fyrir afhendingaraðferðina, þá mun það velja villur við pöntunarfærslu.</span><span class="sxs-lookup"><span data-stu-id="8172a-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="8172a-165">Þegar breytingar hafa verið gerðar á símaversstillingum afhendingarstillinga verður að keyra vinnsluna **Afhendingarmátar vinnslu** að keyra starf til að sprengja breytileika.</span><span class="sxs-lookup"><span data-stu-id="8172a-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="8172a-166">Þetta starf er að finna með því að fara á **Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Afhendingarmátar vinnslu**.</span><span class="sxs-lookup"><span data-stu-id="8172a-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="8172a-167">Eftirfarandi mynd sýnir dæmi um afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="8172a-167">The following image shows an example of a mode of delivery.</span></span>

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="8172a-169">Setja upp rásarnotendur</span><span class="sxs-lookup"><span data-stu-id="8172a-169">Set up channel users</span></span>

<span data-ttu-id="8172a-170">Til að búa til sölupöntun sem er tengd við símaþjónustuver rás frá höfuðstöðvum viðskiptanna verður notandinn sem býr til sölupöntunina að vera tengdur við símaþjónustuver rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="8172a-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="8172a-171">Notandinn getur ekki tengt handvirkt sölupöntun sem búin var til í Commerce Headquarters í símaversrás.</span><span class="sxs-lookup"><span data-stu-id="8172a-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="8172a-172">Hlekkurinn er kerfisbundinn og byggist á notanda og tengslum notandans við símaversrásina.</span><span class="sxs-lookup"><span data-stu-id="8172a-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="8172a-173">Notandi getur aðeins verið tengdur við eina símaversrás.</span><span class="sxs-lookup"><span data-stu-id="8172a-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="8172a-174">Í aðgerðaglugganum velurðu flipann **Rás** og velur síðan **Notendur rásar**.</span><span class="sxs-lookup"><span data-stu-id="8172a-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="8172a-175">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8172a-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8172a-176">Veldu núverandi **Notandakenni** úr fellivalmyndinni til að tengja þennan notanda við símaversrásina</span><span class="sxs-lookup"><span data-stu-id="8172a-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="8172a-177">Þegar uppsetningu rásarnotanda er lokið og notandinn stofnar nýja sölupöntun í Commerce Headquarters verður sölupöntunin tengd við tengda rás símaþjónustuvers hans.</span><span class="sxs-lookup"><span data-stu-id="8172a-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="8172a-178">Allar stillingar fyrir þessa rás verður beitt kerfisbundið á sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="8172a-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="8172a-179">Notandi getur staðfest hvaða símaþjónustuver rás sölupöntunin er tengd með því að skoða tilvísun rásarheitisins á sölupöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="8172a-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="8172a-180">Setja upp verðflokka</span><span class="sxs-lookup"><span data-stu-id="8172a-180">Set up price groups</span></span>

<span data-ttu-id="8172a-181">Verðhópar eru valfrjálsir, en ef þeir eru notaðir geta þeir stjórnað því hvaða söluverð verður boðið viðskiptavinum sem setja pantanir í símaversrásina.</span><span class="sxs-lookup"><span data-stu-id="8172a-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="8172a-182">Ef verðflokkur hefur ekki verið stilltur fyrir viðskiptavininn, eða ef ekki er beitt vöruflokkahópum á sölupöntunina (með því að nota reitinn **Kenni upprunakóða** á pöntunarhausum símaþjónustunnar), þá er verðflokkur rásarinnar notaður til að finna verð á hlutum.</span><span class="sxs-lookup"><span data-stu-id="8172a-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="8172a-183">Ef verðlagshópur er ekki að finna á stöðvunarstöðinni, er sjálfgefið yfirverð vöru notuð.</span><span class="sxs-lookup"><span data-stu-id="8172a-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="8172a-184">Til að setja upp verðflokk, gerðu eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="8172a-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="8172a-185">Í aðgerðaglugganum smellirðu á flipann **Rás** og velur síðan **Verðflokkar**.</span><span class="sxs-lookup"><span data-stu-id="8172a-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="8172a-186">Í aðgerðasvæðinu er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8172a-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="8172a-187">Veldu **Smásöluverðshóp** úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="8172a-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8172a-188">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8172a-188">Additional resources</span></span>

[<span data-ttu-id="8172a-189">Skilyrði fyrir uppsetningu rásar</span><span class="sxs-lookup"><span data-stu-id="8172a-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="8172a-190">Söluvirkni símavers</span><span class="sxs-lookup"><span data-stu-id="8172a-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="8172a-191">Uppsetning valkosta pantanavinnslu símavers</span><span class="sxs-lookup"><span data-stu-id="8172a-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="8172a-192">Vörulistar símavers</span><span class="sxs-lookup"><span data-stu-id="8172a-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="8172a-193">Setja upp og vinna með svikaviðvaranir</span><span class="sxs-lookup"><span data-stu-id="8172a-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="8172a-194">Setja upp samfelldniáætlanir fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="8172a-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]