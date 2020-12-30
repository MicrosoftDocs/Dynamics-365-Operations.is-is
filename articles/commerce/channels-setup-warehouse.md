---
title: Setja upp vöruhús
description: Þetta efni lýsir því hvernig á að setja upp vöruhús til að nota með nýrri rás í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413151"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="172cd-103">Uppsetning vöruhúss</span><span class="sxs-lookup"><span data-stu-id="172cd-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="172cd-104">Þetta efni lýsir því hvernig á að setja upp vöruhús til að nota með nýrri rás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="172cd-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="172cd-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="172cd-105">Overview</span></span>

<span data-ttu-id="172cd-106">Hver Commerce-rás þarf að vera með stillt vöruhús tengt.</span><span class="sxs-lookup"><span data-stu-id="172cd-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="172cd-107">Eftirfarandi ferli veita lágmarksstillingu sem þarf til að setja upp vöruhús fyrir Commerce-rás.</span><span class="sxs-lookup"><span data-stu-id="172cd-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="172cd-108">Nánari upplýsingar um skipulag vöruhúsa er að finna í [Yfirlit vöruhúsastjórnunar](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="172cd-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="172cd-109">Stilla svæði vöruhúss</span><span class="sxs-lookup"><span data-stu-id="172cd-109">Configure a warehouse site</span></span>

<span data-ttu-id="172cd-110">Áður en vöruhús er sett upp þarftu að stilla vöruhússíðu.</span><span class="sxs-lookup"><span data-stu-id="172cd-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="172cd-111">Fylgdu þessum skrefum til að stilla vöruhús.</span><span class="sxs-lookup"><span data-stu-id="172cd-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="172cd-112">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Svæði**.</span><span class="sxs-lookup"><span data-stu-id="172cd-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="172cd-113">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="172cd-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="172cd-114">Í reitinn **Svæði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="172cd-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="172cd-115">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="172cd-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="172cd-116">Í kaflanum **Almennt** stillirðu viðeigandi **Tímabelti**.</span><span class="sxs-lookup"><span data-stu-id="172cd-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="172cd-117">Í hlutanum **Aðsetur** færirðu inn heimilisfang.</span><span class="sxs-lookup"><span data-stu-id="172cd-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="172cd-118">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="172cd-119">Eftirfarandi mynd sýnir dæmi um vöruhússvæði.</span><span class="sxs-lookup"><span data-stu-id="172cd-119">The following image shows an example warehouse site.</span></span>

![Dæmi um vöruhússvæði](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="172cd-121">Setja upp vöruhús</span><span class="sxs-lookup"><span data-stu-id="172cd-121">Set up a warehouse</span></span>

<span data-ttu-id="172cd-122">Til að setja upp vöruhús skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="172cd-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="172cd-123">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="172cd-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="172cd-124">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="172cd-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="172cd-125">Í reitnum **Vöruhús** slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="172cd-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="172cd-126">Ef þetta er 1:1 vörpun í verslun skaltu íhuga að nota heiti verslunarinnar eða nafn svæðisbundinnar dreifingarmiðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="172cd-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="172cd-127">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="172cd-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="172cd-128">Í fellivalmyndinni **Vefsvæði** velurðu vörugeymslusíðuna sem áður var búin til.</span><span class="sxs-lookup"><span data-stu-id="172cd-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="172cd-129">Í reitnum **Tegund** velurðu **Sjálfgildi**.</span><span class="sxs-lookup"><span data-stu-id="172cd-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="172cd-130">Ef þú vilt stilla **Biðgeymsluvöruhús** þarftu fyrst að fylgja þessum skrefum til að búa til viðbótar vöruhús þar sem **Gerð** er stillt á **Biðgeymslu**.</span><span class="sxs-lookup"><span data-stu-id="172cd-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="172cd-131">Ef þú vilt stilla **Flutningsvöruhús** þarftu fyrst að fylgja þessum skrefum til að búa til viðbótar vöruhús þar sem **Gerð** er stillt á **Flutning**.</span><span class="sxs-lookup"><span data-stu-id="172cd-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="172cd-132">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="172cd-133">Setja upp birgðaganga</span><span class="sxs-lookup"><span data-stu-id="172cd-133">Set up inventory aisles</span></span>

<span data-ttu-id="172cd-134">Til að setja upp birgðaganga skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="172cd-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="172cd-135">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Uppsetning staðetningar \> Birgðagangar**.</span><span class="sxs-lookup"><span data-stu-id="172cd-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="172cd-136">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="172cd-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="172cd-137">Í fellivalmyndinni **Vöruhús** velurðu vöruhúsið sem áður var búið til.</span><span class="sxs-lookup"><span data-stu-id="172cd-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="172cd-138">Í reitnum **Gangur** skaltu slá inn nafn (til dæmis „Sjálfg“).</span><span class="sxs-lookup"><span data-stu-id="172cd-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="172cd-139">Í reitnum **Heiti** skaltu slá inn nafn (til dæmis „Sjálfgefinn gangur“).</span><span class="sxs-lookup"><span data-stu-id="172cd-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="172cd-140">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="172cd-141">Setja upp birgðastaðsetningar vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="172cd-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="172cd-142">Fylgdu þessum skrefum til að setja upp birgðastaðsetningar vöruhúss fyrir staðlaðar, skemmdar og skilaðar birgðir.</span><span class="sxs-lookup"><span data-stu-id="172cd-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="172cd-143">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="172cd-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="172cd-144">Veldu vöruhúsið sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="172cd-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="172cd-145">Í aðgerðaglugganum velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="172cd-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="172cd-146">Í aðgerðaglugganum velurðu **Vöruhús** og síðan velurðu **Bigðastaðsetning**.</span><span class="sxs-lookup"><span data-stu-id="172cd-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="172cd-147">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="172cd-147">On the action pane, select **New**.</span></span> <span data-ttu-id="172cd-148">Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="172cd-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="172cd-149">Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.</span><span class="sxs-lookup"><span data-stu-id="172cd-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="172cd-150">Stilltu **Handvirk uppfærsla** á **Já**</span><span class="sxs-lookup"><span data-stu-id="172cd-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="172cd-151">Í reitinn **Staðsetning** færirðu heiti vöruhússins inn.</span><span class="sxs-lookup"><span data-stu-id="172cd-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="172cd-152">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="172cd-153">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="172cd-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="172cd-154">Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="172cd-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="172cd-155">Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.</span><span class="sxs-lookup"><span data-stu-id="172cd-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="172cd-156">Stilltu **Handvirk uppfærsla** á **Já**</span><span class="sxs-lookup"><span data-stu-id="172cd-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="172cd-157">Í reitinn **Staðsetning** slærðu inn „Skemmdir“.</span><span class="sxs-lookup"><span data-stu-id="172cd-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="172cd-158">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="172cd-159">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="172cd-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="172cd-160">Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="172cd-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="172cd-161">Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.</span><span class="sxs-lookup"><span data-stu-id="172cd-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="172cd-162">Stilltu **Handvirk uppfærsla** á **Já**</span><span class="sxs-lookup"><span data-stu-id="172cd-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="172cd-163">Í reitinn **Staðsetning** slærðu inn „Skil“.</span><span class="sxs-lookup"><span data-stu-id="172cd-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="172cd-164">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="172cd-165">Eftirfarandi mynd sýnir uppsetning birgðastaðsetningar vöruhúss í San Francisco.</span><span class="sxs-lookup"><span data-stu-id="172cd-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Dæmi um uppsetningu birgðastaðsetningar](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="172cd-167">Lokin uppsetning vöruhúss</span><span class="sxs-lookup"><span data-stu-id="172cd-167">Complete warehouse setup</span></span>

<span data-ttu-id="172cd-168">Fylgið eftirfarandi skrefum til að ljúka uppsetningu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="172cd-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="172cd-169">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="172cd-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="172cd-170">Veldu vöruhúsið sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="172cd-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="172cd-171">Í aðgerðaglugganum velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="172cd-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="172cd-172">Undir **Birgða- og vöruhúsakerfi**:</span><span class="sxs-lookup"><span data-stu-id="172cd-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="172cd-173">Setja **Sjálfgefin staðsetning innhreyfinga** í sjálfgefna staðinn búinn til hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="172cd-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="172cd-174">Veldu **Sjálfgefin staðsetning úthreyfinga** í sjálfgefna staðinn búinn til hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="172cd-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="172cd-175">Undir hlutann **Heimilisföng** slærðu inn heimilisfang vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="172cd-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="172cd-176">Undir hlutanum **Retail**:</span><span class="sxs-lookup"><span data-stu-id="172cd-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="172cd-177">Í reitinn **Sjálfgefin skilastaðsetning** slærðu inn skilastaðsetningu sem áður var búin til.</span><span class="sxs-lookup"><span data-stu-id="172cd-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="172cd-178">Stilltu **Verslun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="172cd-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="172cd-179">Stilltu **þyngd** á **1,00**.</span><span class="sxs-lookup"><span data-stu-id="172cd-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="172cd-180">Í reitinn **Geymsluvídd** slærðu inn sjálfgefna staðsetningu sem áður var búin til.</span><span class="sxs-lookup"><span data-stu-id="172cd-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="172cd-181">Undir hlutanum **Vöruhús** stillirðu **Efnislega neikvæð birgðastaða** að **Já**.</span><span class="sxs-lookup"><span data-stu-id="172cd-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="172cd-182">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="172cd-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="172cd-183">Eftirfarandi mynd sýnir upplýsingar um stillt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="172cd-183">The following image shows details for a configured warehouse.</span></span>

![Dæmi stillt vöruhús](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="172cd-185">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="172cd-185">Additional resources</span></span>

[<span data-ttu-id="172cd-186">Yfirlit yfir vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="172cd-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="172cd-187">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="172cd-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="172cd-188">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="172cd-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="172cd-189">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="172cd-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="172cd-190">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="172cd-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="172cd-191">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="172cd-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





