---
title: Setja upp smásölurás
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937535"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="e29e4-103">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="e29e4-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e29e4-104">Í þessu efnisatriði er lýst hvernig eigi að stofna nýja smásölurás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e29e4-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e29e4-105">Dynamics 365 Commerce styður margar smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="e29e4-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="e29e4-106">Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir).</span><span class="sxs-lookup"><span data-stu-id="e29e4-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="e29e4-107">Hvert smásöluverslunarrás getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="e29e4-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="e29e4-108">Setja verður upp allar þessar einingar áður en hægt er að stofna smásöluverslunarrás.</span><span class="sxs-lookup"><span data-stu-id="e29e4-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="e29e4-109">Áður en smásölurás er búin til skaltu ganga úr skugga um að þú fylgir [forsendur rásar](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="e29e4-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="e29e4-110">Stofna og stilla nýja smásölurás</span><span class="sxs-lookup"><span data-stu-id="e29e4-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="e29e4-111">Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Verslanir \> Allar smásöluverslanir**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="e29e4-112">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e29e4-113">Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.</span><span class="sxs-lookup"><span data-stu-id="e29e4-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="e29e4-114">Í svæðinu **Verslunarnúmer** skal gefa upp einkvæmt verslunarnúmer.</span><span class="sxs-lookup"><span data-stu-id="e29e4-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="e29e4-115">Talan getur verið bók- eða tölustafir og að hámarki 10 stafir.</span><span class="sxs-lookup"><span data-stu-id="e29e4-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="e29e4-116">Í fellivallistanum **Lögaðili** skal slá inn viðeigandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="e29e4-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="e29e4-117">Í fellivallistanum **Vöruhús** slærðu inn viðeigandi vöruhús.</span><span class="sxs-lookup"><span data-stu-id="e29e4-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="e29e4-118">Í reitnum **Tímabelti verslunar** velurðu viðeigandi tímabelti.</span><span class="sxs-lookup"><span data-stu-id="e29e4-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="e29e4-119">Í fellilistanum **VSK-flokkur** velurðu viðeigandi VSK-flokk fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="e29e4-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="e29e4-120">Í reitnum **Gjaldmiðill** velurðu viðeigandi gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="e29e4-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="e29e4-121">Í reitnum **Heimilisfangabók viðskiptavina** gefurðu upp gilda aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="e29e4-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="e29e4-122">Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="e29e4-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="e29e4-123">Í reitnum **Virkniregla** velurðu virknireglu ef við á.</span><span class="sxs-lookup"><span data-stu-id="e29e4-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="e29e4-124">Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="e29e4-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="e29e4-125">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="e29e4-126">Eftirfarandi mynd sýnir stofnun nýrrar smásölurásar.</span><span class="sxs-lookup"><span data-stu-id="e29e4-126">The following image shows the creation of a new retail channel.</span></span>

![Ný smásölurás](media/channel-setup-retail-1.png)

<span data-ttu-id="e29e4-128">Eftirfarandi mynd sýnir dæmi um smásölurás.</span><span class="sxs-lookup"><span data-stu-id="e29e4-128">The following image shows an example retail channel.</span></span>

![Dæmi um smásölurás](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="e29e4-130">Aðrar stillingar</span><span class="sxs-lookup"><span data-stu-id="e29e4-130">Other settings</span></span>

<span data-ttu-id="e29e4-131">Það eru fjölmargar aðrar valkvæðar stillingar sem hægt er að stilla í hlutunum **Yfirlýsing/lokun** og **Ýmislegt**, miðað við þarfir smásöluverslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="e29e4-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="e29e4-132">Að auki, sjá [Skjáupplýsingar fyrir sölustað (POS)](pos-screen-layouts.md) til að fá upplýsingar um uppsetningu á sjálfgefinni skjáuppsetningu í hlutanum **Skjáskipulag** og [Stilla og setja upp Retail vélbúnaðarstöð](retail-hardware-station-configuration-installation.md) fyrir uppsetningarupplýsingar um hlutann **Vélbúnaðarstöðvar**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="e29e4-133">Eftirfarandi mynd sýnir dæmi um uppsetningarstillingu smásölurásar.</span><span class="sxs-lookup"><span data-stu-id="e29e4-133">The following image shows an example retail channel setup configuration.</span></span>

![Dæmi um stillingu smásölurásar](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="e29e4-135">Viðbótaruppsetning grunnrásar</span><span class="sxs-lookup"><span data-stu-id="e29e4-135">Additional channel set up</span></span>

<span data-ttu-id="e29e4-136">Það eru fleiri hlutir sem þarf að setja upp fyrir rás sem er að finna í aðgerðaglugganum undir kaflanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="e29e4-137">Viðbótarupplýsingar sem krafist er fyrir uppsetningu netrásar fela í sér uppsetningu á greiðslumáta, skilgreiningu reiðufjár, afhendingaraðferðum, tekju-/útgjaldalykli, hlutum, úthlutun uppfyllingarflokks og öryggishólfa.</span><span class="sxs-lookup"><span data-stu-id="e29e4-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="e29e4-138">Eftirfarandi mynd sýnir ýmsa viðbótaruppsetningarvalkosti smásölurásar á flipanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Setja upp rás](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="e29e4-140">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="e29e4-140">Set up payment methods</span></span>

<span data-ttu-id="e29e4-141">Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.</span><span class="sxs-lookup"><span data-stu-id="e29e4-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="e29e4-142">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="e29e4-143">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e29e4-144">Í yfirlitsglugganum velurðu óskaðan greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="e29e4-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="e29e4-145">Í kaflanum **Almennt** skaltu gefa upp **Heiti aðgerðar** og stilla allar aðrar stillingar sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="e29e4-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="e29e4-146">Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="e29e4-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="e29e4-147">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="e29e4-148">Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.</span><span class="sxs-lookup"><span data-stu-id="e29e4-148">The following image shows an example of a cash payment method.</span></span>

![Dæmi um greiðslumáta](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="e29e4-150">Setja upp skilgreiningar reiðufjár</span><span class="sxs-lookup"><span data-stu-id="e29e4-150">Set up cash declaration</span></span>

1. <span data-ttu-id="e29e4-151">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Skilgreining reiðufjár**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="e29e4-152">Í aðgerðaglugganum velurðu **Nýtt** og síðan stofnarður öll gildi **myntar** og **seðla** sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="e29e4-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="e29e4-153">Eftirfarandi mynd sýnir dæmi um skilgreingingu reiðufjár.</span><span class="sxs-lookup"><span data-stu-id="e29e4-153">The following image shows an example of a cash declaration.</span></span>

![Uppsetning á skilgreiningu reiðufjár](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="e29e4-155">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="e29e4-155">Set up modes of delivery</span></span>

<span data-ttu-id="e29e4-156">Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í Aðgerðarglugganum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="e29e4-157">Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="e29e4-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="e29e4-158">Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="e29e4-159">Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.</span><span class="sxs-lookup"><span data-stu-id="e29e4-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="e29e4-160">Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni.</span><span class="sxs-lookup"><span data-stu-id="e29e4-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="e29e4-161">Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.</span><span class="sxs-lookup"><span data-stu-id="e29e4-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="e29e4-162">Eftirfarandi mynd sýnir dæmi um afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="e29e4-162">The following image shows an example of a mode of delivery.</span></span>

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="e29e4-164">Setja upp tekju-/útgjaldalykil</span><span class="sxs-lookup"><span data-stu-id="e29e4-164">Set up income/expense account</span></span>

<span data-ttu-id="e29e4-165">Til að setja upp tekju-/útgjaldalykil skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="e29e4-166">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Tekju-/útgjaldalykil**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="e29e4-167">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e29e4-168">Undir **Heiti** slærðu inn nafn.</span><span class="sxs-lookup"><span data-stu-id="e29e4-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="e29e4-169">Undir **Leitarheiti** slærðu inn leitarheiti.</span><span class="sxs-lookup"><span data-stu-id="e29e4-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="e29e4-170">Undir **Lykilgerð** færirðu inn lykilgerð.</span><span class="sxs-lookup"><span data-stu-id="e29e4-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="e29e4-171">Sláðu inn texta fyrir **Skilaboðalínu 1**, **Skilaboðalínu 2**, **Seðiltexta 1** og **Seðiltexta 2** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="e29e4-172">Undir **Bókun** slærðu inn upplýsingar um bókun.</span><span class="sxs-lookup"><span data-stu-id="e29e4-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="e29e4-173">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="e29e4-174">Eftirfarandi mynd sýnir dæmi um tekju-/útgjaldalykil.</span><span class="sxs-lookup"><span data-stu-id="e29e4-174">The following image shows an example of an income/expense account.</span></span>

![Setja upp tekju-/útgjaldalykla](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="e29e4-176">Setja upp hluta</span><span class="sxs-lookup"><span data-stu-id="e29e4-176">Set up sections</span></span>

<span data-ttu-id="e29e4-177">Til að setja upp hluta skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="e29e4-178">Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Hlutar**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="e29e4-179">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e29e4-180">Undir **Hlutanúmer** slærðu inn hlutanúmer.</span><span class="sxs-lookup"><span data-stu-id="e29e4-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="e29e4-181">Undir **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="e29e4-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="e29e4-182">Undir **Hlutastærð** slærðu inn hlutastærð.</span><span class="sxs-lookup"><span data-stu-id="e29e4-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="e29e4-183">Stilla viðbótarstillingar fyrir **Almennt** og **Söluupplýsingar** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="e29e4-184">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="e29e4-185">Setja upp úthlutun uppfyllingarflokks</span><span class="sxs-lookup"><span data-stu-id="e29e4-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="e29e4-186">Til að setja upp úthlutun uppfyllingarflokks skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="e29e4-187">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Úthlutun uppfyllingarflokks**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="e29e4-188">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e29e4-189">Í fellilistanum **Uppfyllingarhópur** velurðu uppfyllingarhóp.</span><span class="sxs-lookup"><span data-stu-id="e29e4-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="e29e4-190">Í fellilistanum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="e29e4-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="e29e4-191">Í aðgerðaglugganum velurðu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="e29e4-192">Eftirfarandi mynd sýnir dæmi um uppstillingu úthlutunar uppfyllingarflokks.</span><span class="sxs-lookup"><span data-stu-id="e29e4-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Setja upp úthlutanir uppfyllingarflokks](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="e29e4-194">Setja upp öryggishólf</span><span class="sxs-lookup"><span data-stu-id="e29e4-194">Set up safes</span></span>

<span data-ttu-id="e29e4-195">Til að setja upp öryggishólf skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e29e4-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="e29e4-196">Í aðgerðaglugganum velurðu flipann **Setja upp** og smellir á **Öryggishólf**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="e29e4-197">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e29e4-198">Sláðu inn heiti fyrir öryggishólfið.</span><span class="sxs-lookup"><span data-stu-id="e29e4-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="e29e4-199">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="e29e4-200">Tryggja einkvæm færslukenni</span><span class="sxs-lookup"><span data-stu-id="e29e4-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="e29e4-201">Frá og með Commerce-útgáfu 10.0.18 verða færslukenni fyrri sölustaðinn í samfelldri röð og innihalda eftirfarandi hluta:</span><span class="sxs-lookup"><span data-stu-id="e29e4-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="e29e4-202">Fastur hluti, sem er samsetning verslunarkennis og kennis afgreiðslustöðvar.</span><span class="sxs-lookup"><span data-stu-id="e29e4-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="e29e4-203">Samfelldur hluti, sem er númeraröð.</span><span class="sxs-lookup"><span data-stu-id="e29e4-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="e29e4-204">Nánar tiltekið er sniðið *{store}-{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="e29e4-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="e29e4-205">Þar sem hægt er að mynda færslukenni með og án nettengingar hafa komið upp tilvik þar sem sama færslukennið hefur verið búið til oftar en einu sinni.</span><span class="sxs-lookup"><span data-stu-id="e29e4-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="e29e4-206">Mikil handvirk lagfæring gagna felst í að fjarlægja tvítekin færslukenni.</span><span class="sxs-lookup"><span data-stu-id="e29e4-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="e29e4-207">Með Commerce-útgáfu 10.0.19 hefur snið færslukennis verið uppfært til að fjarlægja samfellda hlutann og í staðinn notað 13 stafa tölu sem búin er til með því að reikna tímann í millisekúndum frá árinu 1970.</span><span class="sxs-lookup"><span data-stu-id="e29e4-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="e29e4-208">Með þessari breytingu er nýja snið færslukennisins orðið *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="e29e4-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="e29e4-209">Með þessari uppfærslu verður færslukennið í ósamfelldri röð og tryggir að færslukennin verði alltaf einkvæm.</span><span class="sxs-lookup"><span data-stu-id="e29e4-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="e29e4-210">Færslukenni eru eingöngu ætluð til nota í innra kerfinu og þurfa því ekki að vera í samfelldri röð.</span><span class="sxs-lookup"><span data-stu-id="e29e4-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="e29e4-211">Mörg lönd gera hins vegar kröfu um að kenni innhreyfingarskjala séu í samfelldri röð.</span><span class="sxs-lookup"><span data-stu-id="e29e4-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="e29e4-212">Nýja eiginleikann fyrir snið færslukennis er hægt að virkja á vinnusvæðinu **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="e29e4-213">Til að virkja notkun nýrra færsluauðkenna skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="e29e4-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="e29e4-214">Í Commerce Headquarters skal fara í **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="e29e4-215">Síið fyrir eininguna „smásala og viðskipti“.</span><span class="sxs-lookup"><span data-stu-id="e29e4-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="e29e4-216">Leitið að eiginleikaheitinu **Virkja nýtt færslukenni til að forðast tvítekin færslukenni**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="e29e4-217">Veljið eiginleikann og veljið svo **Virkja núna** á hægra svæðinu.</span><span class="sxs-lookup"><span data-stu-id="e29e4-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="e29e4-218">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="e29e4-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="e29e4-219">Keyrið vinnslurnar **1070 Stilling rásar** og **1170 Verkskráning sölustaðar** til að samstilla virkjaðan eiginleika við verslanirnar.</span><span class="sxs-lookup"><span data-stu-id="e29e4-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="e29e4-220">Þegar breytingarnar hafa verið sendar í verslanirnar þarf að loka og opna aftur afgreiðslukössum verslunar til að nota nýtt snið færslukennis.</span><span class="sxs-lookup"><span data-stu-id="e29e4-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="e29e4-221">Þegar nýr eiginleiki fyrir snið færslukennis hefur verið gerður virkur verður ekki hægt að slökkva á þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="e29e4-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="e29e4-222">Hafðu samband við Commerce Support ef hún þarf að vera óvirk.</span><span class="sxs-lookup"><span data-stu-id="e29e4-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e29e4-223">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e29e4-223">Additional resources</span></span>

[<span data-ttu-id="e29e4-224">Yfirlit rása</span><span class="sxs-lookup"><span data-stu-id="e29e4-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e29e4-225">Skilyrði fyrir uppsetningu rásar</span><span class="sxs-lookup"><span data-stu-id="e29e4-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="e29e4-226">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="e29e4-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="e29e4-227">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="e29e4-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
