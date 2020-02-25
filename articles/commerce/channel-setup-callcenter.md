---
title: Setja upp rás símavers
description: Þetta efni lýsir því hvernig á að stofna nýja símaversrás í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002451"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="aa4c2-103">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="aa4c2-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aa4c2-104">Þetta efni lýsir því hvernig á að stofna nýja símaversrás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aa4c2-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="aa4c2-105">Overview</span></span>

<span data-ttu-id="aa4c2-106">Í Dynamics 365 Commerce er símaver tegund smásölurásar sem hægt er að skilgreina í forritinu.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="aa4c2-107">Að skilgreina rás fyrir símaþjónustueiningar þínar gerir kerfinu kleift að binda tiltekin gögn og sjálfgildi pöntunarvinnslu við sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="aa4c2-108">Fyrirtæki getur skilgreint margar rásir símavers í Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="aa4c2-109">Áður en ný rás símavers er stofnuð skaltu ganga úr skugga um að þú hafir lokið við [Skilyrði fyrir rásauppsetningu](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="aa4c2-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="aa4c2-110">Stofna og stilla nýja rás símavers</span><span class="sxs-lookup"><span data-stu-id="aa4c2-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="aa4c2-111">Til að stofna og stilla nýja rás símavers fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="aa4c2-112">Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Símaver \> Öll símaver**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="aa4c2-113">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa4c2-114">Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="aa4c2-115">Veldu viðeigandi **Lögaðila** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="aa4c2-116">Veldu viðeigandi staðsetningu **vöruhúss** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="aa4c2-117">Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="aa4c2-118">Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="aa4c2-119">Gefa upp upplýsingakóða **verðhnekkingar**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="aa4c2-120">Athugaðu að þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="aa4c2-121">Gefðu upp upplýsingakóðann **Biðkóði**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="aa4c2-122">Athugaðu að þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="aa4c2-123">Gefðu upp upplýsingakóðann **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="aa4c2-124">Athugaðu að þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="aa4c2-125">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-125">Select **Save**.</span></span>

<span data-ttu-id="aa4c2-126">Eftirfarandi mynd sýnir stofnun nýrrar símaversrásar.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-126">The following image shows the creation of a new call center channel.</span></span>

![Ný rás símavers](media/channel-setup-callcenter-1.png)

<span data-ttu-id="aa4c2-128">Eftirfarandi mynd sýnir dæmi um símaversrás.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-128">The following image shows an example call center channel.</span></span>

![Dæmi um rás símavers](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="aa4c2-130">Viðbótaruppsetning grunnrásar</span><span class="sxs-lookup"><span data-stu-id="aa4c2-130">Additional channel setup</span></span>

<span data-ttu-id="aa4c2-131">Viðbótarupplýsingar sem krafist er fyrir uppsetningu símaversrásar fela í sér uppsetningu á greiðslumáta og afhendingaraðferðum.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="aa4c2-132">Eftirfarandi mynd sýnir uppsetningarkostina **Afhendingarmáta** og **Greiðslumáta** á flipanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Viðbótar uppsetningaraðgerðir símaversrásar](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="aa4c2-134">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="aa4c2-134">Set up payment methods</span></span>

<span data-ttu-id="aa4c2-135">Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="aa4c2-136">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="aa4c2-137">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aa4c2-138">Í yfirlitsglugganum velurðu óskaðan greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="aa4c2-139">Í kaflanum **Almennt** skaltu gefa upp **Heiti aðgerðar** og stilla allar aðrar stillingar sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="aa4c2-140">Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="aa4c2-141">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="aa4c2-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aa4c2-142">Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-142">The following image shows an example of a cash payment method.</span></span>

![Dæmi um greiðslumáta](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="aa4c2-144">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="aa4c2-144">Set up modes of delivery</span></span>

<span data-ttu-id="aa4c2-145">Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="aa4c2-146">Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="aa4c2-147">Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="aa4c2-148">Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="aa4c2-149">Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="aa4c2-150">Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="aa4c2-151">Eftirfarandi mynd sýnir dæmi um afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="aa4c2-151">The following image shows an example of a mode of delivery.</span></span>

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="aa4c2-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="aa4c2-153">Additional resources</span></span>

[<span data-ttu-id="aa4c2-154">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="aa4c2-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="aa4c2-155">Söluvirkni símavers</span><span class="sxs-lookup"><span data-stu-id="aa4c2-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="aa4c2-156">Uppsetning valkosta pantanavinnslu símavers</span><span class="sxs-lookup"><span data-stu-id="aa4c2-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="aa4c2-157">Vörulistar símavers</span><span class="sxs-lookup"><span data-stu-id="aa4c2-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="aa4c2-158">Setja upp og vinna með svikaviðvaranir</span><span class="sxs-lookup"><span data-stu-id="aa4c2-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="aa4c2-159">Setja upp samfelldniáætlanir fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="aa4c2-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
