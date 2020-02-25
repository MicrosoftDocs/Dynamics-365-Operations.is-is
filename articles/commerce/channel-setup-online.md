---
title: Setja upp netrás
description: Þetta efni lýsir því hvernig á að stofna nýja netrás í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002428"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="c6ebf-103">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="c6ebf-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c6ebf-104">Þetta efni lýsir því hvernig á að stofna nýja netrás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6ebf-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c6ebf-105">Overview</span></span>

<span data-ttu-id="c6ebf-106">Dynamics 365 Commerce styður margar smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="c6ebf-107">Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir).</span><span class="sxs-lookup"><span data-stu-id="c6ebf-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="c6ebf-108">Netverslun gefur viðskiptavinum val um að kaupa afurðir úr netverslun smásala til viðbótar við smásöluverslanir þeirra.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="c6ebf-109">Til að stofna netverslun í Commerce verðurðu fyrst að búa til netrás.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="c6ebf-110">Áður en ný netrás er stofnuð skaltu ganga úr skugga um að þú hafir lokið við [Skilyrði fyrir rásauppsetningu](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="c6ebf-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="c6ebf-111">Stofna og stilla nýja netrás</span><span class="sxs-lookup"><span data-stu-id="c6ebf-111">Create and configure a new online channel</span></span>

<span data-ttu-id="c6ebf-112">Til að stofna og stilla nýja netrás fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="c6ebf-113">Í yfirlitsglugganum ferðu í **Einingar \> Rásir \> Netverslanir**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="c6ebf-114">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c6ebf-115">Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="c6ebf-116">Í fellivalmyndinni **Lögaðili** skal slá inn viðeigandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="c6ebf-117">Í fellivalmyndinni **Vöruhús** slærðu inn viðeigandi vöruhús.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="c6ebf-118">Í reitnum **Tímabelti verslunar** velurðu viðeigandi tímabelti.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="c6ebf-119">Í reitnum **Gjaldmiðill** velurðu viðeigandi gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="c6ebf-120">Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="c6ebf-121">Í reitnum **Heimilisfangabók viðskiptavina** gefurðu upp gilda aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="c6ebf-122">Í reitnum **Virkniregla** velurðu virknireglu ef við á.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="c6ebf-123">Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="c6ebf-124">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="c6ebf-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c6ebf-125">Eftirfarandi mynd sýnir stofnun nýrrar netrásar.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-125">The following image shows the creation of a new online channel.</span></span>

![Ný netrás](media/channel-setup-online-1.png)

<span data-ttu-id="c6ebf-127">Eftirfarandi mynd sýnir dæmi um netrás.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-127">The following image shows an example online channel.</span></span>

![Dæmi um netrás](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="c6ebf-129">Setja upp tungumál</span><span class="sxs-lookup"><span data-stu-id="c6ebf-129">Set up languages</span></span>

<span data-ttu-id="c6ebf-130">Ef netverslunarsíðan mun styðja mörg tungumál skaltu stækka hlutann **Tungumál** og bæta við fleiri tungumálum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="c6ebf-131">Setja upp greiðslulykil</span><span class="sxs-lookup"><span data-stu-id="c6ebf-131">Set up payment account</span></span>

<span data-ttu-id="c6ebf-132">Í hlutanum **Greiðslulykill** er hægt að bæta við greiðsluaðila þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="c6ebf-133">Nánari upplýsingar um að setja upp Adyen greiðslutengi, sjá [Dynamics 365 greiðslutengi fyrir Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="c6ebf-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="c6ebf-134">Viðbótaruppsetning grunnrásar</span><span class="sxs-lookup"><span data-stu-id="c6ebf-134">Additional channel set up</span></span>

<span data-ttu-id="c6ebf-135">Viðbótarupplýsingar sem krafist er fyrir uppsetningu netrásar fela í sér uppsetningu á greiðslumáta, afhendingaraðferðum og úthlutanir uppfyllingarflokks.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="c6ebf-136">Eftirfarandi mynd sýnir uppsetningarkostina **Afhendingarmáta**, **Greiðslumáta** og **Úthlutanir uppfyllingarflokks** á flipanum **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Viðbótar uppsetningaraðgerðir netrásar](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="c6ebf-138">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="c6ebf-138">Set up payment methods</span></span>

<span data-ttu-id="c6ebf-139">Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="c6ebf-140">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="c6ebf-141">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c6ebf-142">Í yfirlitsglugganum velurðu óskaðan greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="c6ebf-143">Í kaflanum **Almennt** skaltu gefa upp **Heiti aðgerðar** og stilla allar aðrar stillingar sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="c6ebf-144">Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="c6ebf-145">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="c6ebf-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c6ebf-146">Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-146">The following image shows an example of a cash payment method.</span></span>

![Dæmi um greiðslumáta](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="c6ebf-148">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="c6ebf-148">Set up modes of delivery</span></span>

<span data-ttu-id="c6ebf-149">Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="c6ebf-150">Fylgdu þessum skrefum til að breyta eða bæta við afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="c6ebf-151">Í yfirlitsglugganum ferðu í **Einingar \> Birgðastjórnun \> Afhendingmáti**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="c6ebf-152">Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="c6ebf-153">Í kaflanum **Smásölurásir** velurðu **Bæta við línu** til að bæta við rásinni.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="c6ebf-154">Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="c6ebf-155">Eftirfarandi mynd sýnir dæmi um afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-155">The following image shows an example of a mode of delivery.</span></span>

![Setja upp afhendingarmáta](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="c6ebf-157">Setja upp úthlutun uppfyllingarflokks</span><span class="sxs-lookup"><span data-stu-id="c6ebf-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="c6ebf-158">Til að setja upp úthlutun uppfyllingarflokks skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="c6ebf-159">Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Úthlutun uppfyllingarflokks**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="c6ebf-160">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c6ebf-161">Í fellilistanum **Uppfyllingarhópur** velurðu uppfyllingarhóp.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="c6ebf-162">Í fellilistanum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="c6ebf-163">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="c6ebf-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c6ebf-164">Eftirfarandi mynd sýnir dæmi um uppstillingu úthlutunar uppfyllingarflokks.</span><span class="sxs-lookup"><span data-stu-id="c6ebf-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Setja upp úthlutun uppfyllingarflokks](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="c6ebf-166">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c6ebf-166">Additional resources</span></span>

[<span data-ttu-id="c6ebf-167">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="c6ebf-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c6ebf-168">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="c6ebf-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c6ebf-169">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="c6ebf-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="c6ebf-170">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="c6ebf-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="c6ebf-171">Dynamics 365-greiðslutengill fyrir Adyen</span><span class="sxs-lookup"><span data-stu-id="c6ebf-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
