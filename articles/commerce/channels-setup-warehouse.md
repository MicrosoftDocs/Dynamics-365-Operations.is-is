---
title: Setja upp vöruhús
description: Þetta efnisatriði lýsir því hvernig á að setja upp vöruhús sem á að nota með nýrri rás í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477635"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="25c91-103">Uppsetning vöruhúss</span><span class="sxs-lookup"><span data-stu-id="25c91-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="25c91-104">Þetta efnisatriði lýsir því hvernig á að setja upp vöruhús sem á að nota með nýrri rás í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="25c91-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="25c91-105">Hver Commerce-rás þarf að vera með stillt vöruhús tengt.</span><span class="sxs-lookup"><span data-stu-id="25c91-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="25c91-106">Eftirfarandi ferli veita lágmarksstillingu sem þarf til að setja upp vöruhús fyrir Commerce-rás.</span><span class="sxs-lookup"><span data-stu-id="25c91-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="25c91-107">Nánari upplýsingar um skipulag vöruhúsa er að finna í [Yfirlit vöruhúsastjórnunar](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="25c91-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="25c91-108">Stilla svæði vöruhúss</span><span class="sxs-lookup"><span data-stu-id="25c91-108">Configure a warehouse site</span></span>

<span data-ttu-id="25c91-109">Áður en vöruhús er sett upp þarftu að stilla vöruhússíðu.</span><span class="sxs-lookup"><span data-stu-id="25c91-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="25c91-110">Fylgdu þessum skrefum til að stilla vöruhús.</span><span class="sxs-lookup"><span data-stu-id="25c91-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="25c91-111">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Svæði**.</span><span class="sxs-lookup"><span data-stu-id="25c91-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="25c91-112">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25c91-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="25c91-113">Í reitinn **Svæði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25c91-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="25c91-114">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25c91-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="25c91-115">Í kaflanum **Almennt** stillirðu viðeigandi **Tímabelti**.</span><span class="sxs-lookup"><span data-stu-id="25c91-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="25c91-116">Í hlutanum **Aðsetur** færirðu inn heimilisfang.</span><span class="sxs-lookup"><span data-stu-id="25c91-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="25c91-117">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="25c91-118">Eftirfarandi mynd sýnir dæmi um vöruhússvæði.</span><span class="sxs-lookup"><span data-stu-id="25c91-118">The following image shows an example warehouse site.</span></span>

![Dæmi um vöruhússvæði](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="25c91-120">Setja upp vöruhús</span><span class="sxs-lookup"><span data-stu-id="25c91-120">Set up a warehouse</span></span>

<span data-ttu-id="25c91-121">Til að setja upp vöruhús skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="25c91-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="25c91-122">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="25c91-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="25c91-123">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25c91-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="25c91-124">Í reitnum **Vöruhús** slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25c91-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="25c91-125">Ef þetta er 1:1 vörpun í verslun skaltu íhuga að nota heiti verslunarinnar eða nafn svæðisbundinnar dreifingarmiðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="25c91-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="25c91-126">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="25c91-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="25c91-127">Í fellivalmyndinni **Vefsvæði** velurðu vörugeymslusíðuna sem áður var búin til.</span><span class="sxs-lookup"><span data-stu-id="25c91-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="25c91-128">Í reitnum **Tegund** velurðu **Sjálfgildi**.</span><span class="sxs-lookup"><span data-stu-id="25c91-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="25c91-129">Ef þú vilt stilla **Biðgeymsluvöruhús** þarftu fyrst að fylgja þessum skrefum til að búa til viðbótar vöruhús þar sem **Gerð** er stillt á **Biðgeymslu**.</span><span class="sxs-lookup"><span data-stu-id="25c91-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="25c91-130">Ef þú vilt stilla **Flutningsvöruhús** þarftu fyrst að fylgja þessum skrefum til að búa til viðbótar vöruhús þar sem **Gerð** er stillt á **Flutning**.</span><span class="sxs-lookup"><span data-stu-id="25c91-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="25c91-131">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="25c91-132">Setja upp birgðaganga</span><span class="sxs-lookup"><span data-stu-id="25c91-132">Set up inventory aisles</span></span>

<span data-ttu-id="25c91-133">Til að setja upp birgðaganga skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="25c91-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="25c91-134">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Uppsetning staðetningar \> Birgðagangar**.</span><span class="sxs-lookup"><span data-stu-id="25c91-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="25c91-135">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25c91-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="25c91-136">Í fellivalmyndinni **Vöruhús** velurðu vöruhúsið sem áður var búið til.</span><span class="sxs-lookup"><span data-stu-id="25c91-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="25c91-137">Í reitnum **Gangur** skaltu slá inn nafn (til dæmis „Sjálfg“).</span><span class="sxs-lookup"><span data-stu-id="25c91-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="25c91-138">Í reitnum **Heiti** skaltu slá inn nafn (til dæmis „Sjálfgefinn gangur“).</span><span class="sxs-lookup"><span data-stu-id="25c91-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="25c91-139">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="25c91-140">Setja upp birgðastaðsetningar vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="25c91-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="25c91-141">Fylgdu þessum skrefum til að setja upp birgðastaðsetningar vöruhúss fyrir staðlaðar, skemmdar og skilaðar birgðir.</span><span class="sxs-lookup"><span data-stu-id="25c91-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="25c91-142">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="25c91-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="25c91-143">Veldu vöruhúsið sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="25c91-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="25c91-144">Í aðgerðaglugganum velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="25c91-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="25c91-145">Í aðgerðaglugganum velurðu **Vöruhús** og síðan velurðu **Bigðastaðsetning**.</span><span class="sxs-lookup"><span data-stu-id="25c91-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="25c91-146">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25c91-146">On the action pane, select **New**.</span></span> <span data-ttu-id="25c91-147">Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="25c91-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="25c91-148">Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.</span><span class="sxs-lookup"><span data-stu-id="25c91-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="25c91-149">Stilltu **Handvirk uppfærsla** á **Já**</span><span class="sxs-lookup"><span data-stu-id="25c91-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="25c91-150">Í reitinn **Staðsetning** færirðu heiti vöruhússins inn.</span><span class="sxs-lookup"><span data-stu-id="25c91-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="25c91-151">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="25c91-152">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25c91-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="25c91-153">Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="25c91-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="25c91-154">Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.</span><span class="sxs-lookup"><span data-stu-id="25c91-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="25c91-155">Stilltu **Handvirk uppfærsla** á **Já**</span><span class="sxs-lookup"><span data-stu-id="25c91-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="25c91-156">Í reitinn **Staðsetning** slærðu inn „Skemmdir“.</span><span class="sxs-lookup"><span data-stu-id="25c91-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="25c91-157">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="25c91-158">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="25c91-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="25c91-159">Fellilistinn **Vöruhús** ætti að vera sjálfgefinn í nýja vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="25c91-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="25c91-160">Í reitinn **Gangur** slærðu inn heiti gangsins sem þú tilgreindir áður.</span><span class="sxs-lookup"><span data-stu-id="25c91-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="25c91-161">Stilltu **Handvirk uppfærsla** á **Já**</span><span class="sxs-lookup"><span data-stu-id="25c91-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="25c91-162">Í reitinn **Staðsetning** slærðu inn „Skil“.</span><span class="sxs-lookup"><span data-stu-id="25c91-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="25c91-163">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="25c91-164">Eftirfarandi mynd sýnir uppsetning birgðastaðsetningar vöruhúss í San Francisco.</span><span class="sxs-lookup"><span data-stu-id="25c91-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Dæmi um uppsetningu birgðastaðsetningar](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="25c91-166">Lokin uppsetning vöruhúss</span><span class="sxs-lookup"><span data-stu-id="25c91-166">Complete warehouse setup</span></span>

<span data-ttu-id="25c91-167">Fylgið eftirfarandi skrefum til að ljúka uppsetningu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="25c91-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="25c91-168">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="25c91-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="25c91-169">Veldu vöruhúsið sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="25c91-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="25c91-170">Í aðgerðaglugganum velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="25c91-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="25c91-171">Undir **Birgða- og vöruhúsakerfi**:</span><span class="sxs-lookup"><span data-stu-id="25c91-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="25c91-172">Setja **Sjálfgefin staðsetning innhreyfinga** í sjálfgefna staðinn búinn til hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="25c91-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="25c91-173">Veldu **Sjálfgefin staðsetning úthreyfinga** í sjálfgefna staðinn búinn til hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="25c91-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="25c91-174">Undir hlutann **Heimilisföng** slærðu inn heimilisfang vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="25c91-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="25c91-175">Undir hlutanum **Retail**:</span><span class="sxs-lookup"><span data-stu-id="25c91-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="25c91-176">Í reitinn **Sjálfgefin skilastaðsetning** slærðu inn skilastaðsetningu sem áður var búin til.</span><span class="sxs-lookup"><span data-stu-id="25c91-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="25c91-177">Stilltu **Verslun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="25c91-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="25c91-178">Stilltu **þyngd** á **1,00**.</span><span class="sxs-lookup"><span data-stu-id="25c91-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="25c91-179">Í reitinn **Geymsluvídd** slærðu inn sjálfgefna staðsetningu sem áður var búin til.</span><span class="sxs-lookup"><span data-stu-id="25c91-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="25c91-180">Undir hlutanum **Vöruhús** stillirðu **Efnislega neikvæð birgðastaða** að **Já**.</span><span class="sxs-lookup"><span data-stu-id="25c91-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="25c91-181">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="25c91-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="25c91-182">Eftirfarandi mynd sýnir upplýsingar um stillt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="25c91-182">The following image shows details for a configured warehouse.</span></span>

![Dæmi stillt vöruhús](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="25c91-184">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="25c91-184">Additional resources</span></span>

[<span data-ttu-id="25c91-185">Yfirlit yfir vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="25c91-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="25c91-186">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="25c91-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="25c91-187">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="25c91-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="25c91-188">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="25c91-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="25c91-189">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="25c91-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="25c91-190">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="25c91-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
