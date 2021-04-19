---
title: Setja upp smásölurás
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 713cbe68c151b6893519843611089941cabf0e70
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800592"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="7c270-103">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="7c270-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c270-104">Í þessu efnisatriði er lýst hvernig eigi að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c270-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7c270-105">Dynamics 365 Commerce styður margar smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="7c270-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="7c270-106">Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir).</span><span class="sxs-lookup"><span data-stu-id="7c270-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="7c270-107">Hvert smásöluverslunarrás getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="7c270-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="7c270-108">Setja verður upp allar þessar einingar áður en hægt er að stofna smásöluverslunarrás.</span><span class="sxs-lookup"><span data-stu-id="7c270-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="7c270-109">Áður en smásölurás er búin til skaltu ganga úr skugga um að þú fylgir [forsendur rásar](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="7c270-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="7c270-110">Stofna og stilla nýja smásölurás</span><span class="sxs-lookup"><span data-stu-id="7c270-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="7c270-111">Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Verslanir \> Allar smásöluverslanir**.</span><span class="sxs-lookup"><span data-stu-id="7c270-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="7c270-112">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7c270-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c270-113">Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.</span><span class="sxs-lookup"><span data-stu-id="7c270-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="7c270-114">Í svæðinu **Verslunarnúmer** skal gefa upp einkvæmt verslunarnúmer.</span><span class="sxs-lookup"><span data-stu-id="7c270-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="7c270-115">Talan getur verið bók- eða tölustafir og að hámarki 10 stafir.</span><span class="sxs-lookup"><span data-stu-id="7c270-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="7c270-116">Í fellivallistanum **Lögaðili** skal slá inn viðeigandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="7c270-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="7c270-117">Í fellivallistanum **Vöruhús** slærðu inn viðeigandi vöruhús.</span><span class="sxs-lookup"><span data-stu-id="7c270-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="7c270-118">Í reitnum **Tímabelti verslunar** velurðu viðeigandi tímabelti.</span><span class="sxs-lookup"><span data-stu-id="7c270-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="7c270-119">Í fellilistanum **VSK-flokkur** velurðu viðeigandi VSK-flokk fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="7c270-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="7c270-120">Í reitnum **Gjaldmiðill** velurðu viðeigandi gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="7c270-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="7c270-121">Í reitnum **Heimilisfangabók viðskiptavina** gefurðu upp gilda aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="7c270-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="7c270-122">Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="7c270-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="7c270-123">Í reitnum **Virkniregla** velurðu virknireglu ef við á.</span><span class="sxs-lookup"><span data-stu-id="7c270-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="7c270-124">Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="7c270-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="7c270-125">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="7c270-125">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7c270-126">Eftirfarandi mynd sýnir stofnun nýrrar smásölurásar.</span><span class="sxs-lookup"><span data-stu-id="7c270-126">The following image shows the creation of a new retail channel.</span></span>

![Ný smásölurás](media/channel-setup-retail-1.png)

<span data-ttu-id="7c270-128">Eftirfarandi mynd sýnir dæmi um smásölurás.</span><span class="sxs-lookup"><span data-stu-id="7c270-128">The following image shows an example retail channel.</span></span>

![Dæmi um smásölurás](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="7c270-130">Aðrar stillingar</span><span class="sxs-lookup"><span data-stu-id="7c270-130">Other settings</span></span>

<span data-ttu-id="7c270-131">Það eru fjölmargar aðrar valkvæðar stillingar sem hægt er að stilla í hlutunum **Yfirlýsing/lokun** og **Ýmislegt**, miðað við þarfir smásöluverslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="7c270-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="7c270-132">Að auki, sjá [Skjáupplýsingar fyrir sölustað (POS)](pos-screen-layouts.md) til að fá upplýsingar um uppsetningu á sjálfgefinni skjáuppsetningu í hlutanum **Skjáskipulag** og [Stilla og setja upp Retail vélbúnaðarstöð](retail-hardware-station-configuration-installation.md) fyrir uppsetningarupplýsingar um hlutann **Vélbúnaðarstöðvar**.</span><span class="sxs-lookup"><span data-stu-id="7c270-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="7c270-133">Eftirfarandi mynd sýnir dæmi um uppsetningarstillingu smásölurásar.</span><span class="sxs-lookup"><span data-stu-id="7c270-133">The following image shows an example retail channel setup configuration.</span></span>

![Dæmi um stillingu smásölurásar](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="7c270-135">Viðbótaruppsetning grunnrásar</span><span class="sxs-lookup"><span data-stu-id="7c270-135">Additional channel set up</span></span>

<span data-ttu-id="7c270-136">Það eru fleiri hlutir sem þarf að setja upp fyrir rás sem er að finna í **aðgerðaglugganum** undir kaflanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="7c270-136">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="7c270-137">Viðbótarupplýsingar sem krafist er fyrir uppsetningu netrásar fela í sér uppsetningu á greiðslumáta, skilgreiningu reiðufjár, afhendingaraðferðum, tekju-/útgjaldalykli, hlutum, úthlutun uppfyllingarflokks og öryggishólfa.</span><span class="sxs-lookup"><span data-stu-id="7c270-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="7c270-138">Eftirfarandi mynd sýnir ýmsa viðbótaruppsetningarvalkosti smásölurásar á flipanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="7c270-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Setja upp rás](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="7c270-140">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="7c270-140">Set up payment methods</span></span>

<span data-ttu-id="7c270-141">Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.</span><span class="sxs-lookup"><span data-stu-id="7c270-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="7c270-142">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.</span><span class="sxs-lookup"><span data-stu-id="7c270-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="7c270-143">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7c270-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c270-144">Í yfirlitsglugganum velurðu óskaðan greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="7c270-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="7c270-145">Í kaflanum **Almennt** skaltu gefa upp **Heiti aðgerðar** og stilla allar aðrar stillingar sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="7c270-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="7c270-146">Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="7c270-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="7c270-147">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="7c270-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7c270-148">Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.</span><span class="sxs-lookup"><span data-stu-id="7c270-148">The following image shows an example of a cash payment method.</span></span>

![Dæmi um greiðslumáta](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="7c270-150">Setja upp skilgreiningar reiðufjár</span><span class="sxs-lookup"><span data-stu-id="7c270-150">Set up cash declaration</span></span>

1. <span data-ttu-id="7c270-151">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Skilgreining reiðufjár**.</span><span class="sxs-lookup"><span data-stu-id="7c270-151">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="7c270-152">Í aðgerðaglugganum velurðu **Nýtt** og síðan stofnarður öll gildi **myntar** og **seðla** sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="7c270-152">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="7c270-153">Eftirfarandi mynd sýnir dæmi um skilgreingingu reiðufjár.</span><span class="sxs-lookup"><span data-stu-id="7c270-153">The following image shows an example of a cash declaration.</span></span>

![Uppsetning á skilgreiningu reiðufjár](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="7c270-155">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="7c270-155">Set up modes of delivery</span></span>

<span data-ttu-id="7c270-156">Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.</span><span class="sxs-lookup"><span data-stu-id="7c270-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="7c270-157">Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="7c270-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="7c270-158">Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.</span><span class="sxs-lookup"><span data-stu-id="7c270-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="7c270-159">Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.</span><span class="sxs-lookup"><span data-stu-id="7c270-159">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="7c270-160">Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni.</span><span class="sxs-lookup"><span data-stu-id="7c270-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="7c270-161">Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.</span><span class="sxs-lookup"><span data-stu-id="7c270-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="7c270-162">Eftirfarandi mynd sýnir dæmi um afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="7c270-162">The following image shows an example of a mode of delivery.</span></span>

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="7c270-164">Setja upp tekju-/útgjaldalykil</span><span class="sxs-lookup"><span data-stu-id="7c270-164">Set up income/expense account</span></span>

<span data-ttu-id="7c270-165">Til að setja upp tekju-/útgjaldalykil skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7c270-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="7c270-166">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Tekju-/útgjaldalykil**.</span><span class="sxs-lookup"><span data-stu-id="7c270-166">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="7c270-167">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7c270-167">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c270-168">Undir **Heiti** slærðu inn nafn.</span><span class="sxs-lookup"><span data-stu-id="7c270-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="7c270-169">Undir **Leitarheiti** slærðu inn leitarheiti.</span><span class="sxs-lookup"><span data-stu-id="7c270-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="7c270-170">Undir **Lykilgerð** færirðu inn lykilgerð.</span><span class="sxs-lookup"><span data-stu-id="7c270-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="7c270-171">Sláðu inn texta fyrir **Skilaboðalínu 1**, **Skilaboðalínu 2**, **Seðiltexta 1** og **Seðiltexta 2** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7c270-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="7c270-172">Undir **Bókun** slærðu inn upplýsingar um bókun.</span><span class="sxs-lookup"><span data-stu-id="7c270-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="7c270-173">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="7c270-173">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7c270-174">Eftirfarandi mynd sýnir dæmi um tekju-/útgjaldalykil.</span><span class="sxs-lookup"><span data-stu-id="7c270-174">The following image shows an example of an income/expense account.</span></span>

![Setja upp tekju-/útgjaldalykla](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="7c270-176">Setja upp hluta</span><span class="sxs-lookup"><span data-stu-id="7c270-176">Set up sections</span></span>

<span data-ttu-id="7c270-177">Til að setja upp hluta skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7c270-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="7c270-178">Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Hlutar**.</span><span class="sxs-lookup"><span data-stu-id="7c270-178">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="7c270-179">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7c270-179">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c270-180">Undir **Hlutanúmer** slærðu inn hlutanúmer.</span><span class="sxs-lookup"><span data-stu-id="7c270-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="7c270-181">Undir **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="7c270-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="7c270-182">Undir **Hlutastærð** slærðu inn hlutastærð.</span><span class="sxs-lookup"><span data-stu-id="7c270-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="7c270-183">Stilla viðbótarstillingar fyrir **Almennt** og **Söluupplýsingar** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="7c270-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="7c270-184">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="7c270-184">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="7c270-185">Setja upp úthlutun uppfyllingarflokks</span><span class="sxs-lookup"><span data-stu-id="7c270-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="7c270-186">Til að setja upp úthlutun uppfyllingarflokks skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7c270-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="7c270-187">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Úthlutun uppfyllingarflokks**.</span><span class="sxs-lookup"><span data-stu-id="7c270-187">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="7c270-188">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7c270-188">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c270-189">Í fellilistanum **Uppfyllingarhópur** velurðu uppfyllingarhóp.</span><span class="sxs-lookup"><span data-stu-id="7c270-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="7c270-190">Í fellilistanum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="7c270-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="7c270-191">Í aðgerðaglugganum velurðu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7c270-191">On the action pane, select **Save**</span></span>

<span data-ttu-id="7c270-192">Eftirfarandi mynd sýnir dæmi um uppstillingu úthlutunar uppfyllingarflokks.</span><span class="sxs-lookup"><span data-stu-id="7c270-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Setja upp úthlutanir uppfyllingarflokks](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="7c270-194">Setja upp öryggishólf</span><span class="sxs-lookup"><span data-stu-id="7c270-194">Set up safes</span></span>

<span data-ttu-id="7c270-195">Til að setja upp öryggishólf skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="7c270-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="7c270-196">Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Öryggishólf**.</span><span class="sxs-lookup"><span data-stu-id="7c270-196">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="7c270-197">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7c270-197">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c270-198">Sláðu inn heiti fyrir öryggishólfið.</span><span class="sxs-lookup"><span data-stu-id="7c270-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="7c270-199">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="7c270-199">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c270-200">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c270-200">Additional resources</span></span>

[<span data-ttu-id="7c270-201">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="7c270-201">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7c270-202">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="7c270-202">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7c270-203">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="7c270-203">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7c270-204">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="7c270-204">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
