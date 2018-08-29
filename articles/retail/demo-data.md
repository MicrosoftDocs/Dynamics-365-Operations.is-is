---
title: "Skjáútlit sýnigagna í Retail Modern POS (MPOS) og Cloud POS"
description: "Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás sem er innifalið í sýnigagnasafninu fyrir sölustað (POS) upplifunina í Microsoft Dynamics 365 for Retail."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41930e89a7cae5cdb84e728da47de3bc5de312ca
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="demo-data-screen-layouts-in-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="8a1b6-103">Skjáútlit sýnigagna í Retail Modern POS (MPOS) og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="8a1b6-103">Demo data screen layouts in Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a1b6-104">Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás sem er innifalið í sýnigagnasafninu fyrir sölustað (POS) upplifunina í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="8a1b6-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="8a1b6-105">Overview</span></span>

<span data-ttu-id="8a1b6-106">Sýnishorn af útliti skjás sem fylgja með sýnigögnum Retail bjóða upp á efni sem er fínstillt fyrir ýmsa smásöluhluta, hlutverk verslunarstarfsmanns og tæki.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="8a1b6-107">Ein gerð útlits getur innihaldið nokkrar útlitsstærðir og samsetningar hnappahnita til að tryggja dekkun þar sem verslunarstarfsmenn fara á milli búnaðar og stöðva.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="8a1b6-108">Í þessu efnisatriði er lögð áhersla á muninn á þessum útlitsgerðum, aðgerðunum sem þær bjóða upp á og heildarupplifunin sem þær skila.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![Útlit sýnigagna á milli tækja](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="8a1b6-110">Grunnskipulag kennis skjáútlits</span><span class="sxs-lookup"><span data-stu-id="8a1b6-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="8a1b6-111">Til að finna útlitsgerðir skjás í Retail skal fara í **Smásala**  > **Uppsetningu rásar** > **Uppsetning POS** > **POS** > **Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![Síða skjáútlits í Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="8a1b6-113">Kenni skjáútlits getur haft allt að 10 stafi.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="8a1b6-114">Kennið er strengur sem samanstendur af þremur upplýsingahlutum, í þessari röð:</span><span class="sxs-lookup"><span data-stu-id="8a1b6-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="8a1b6-115">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="8a1b6-115">Company</span></span>
2. <span data-ttu-id="8a1b6-116">Útlitsgerð</span><span class="sxs-lookup"><span data-stu-id="8a1b6-116">Layout version</span></span>
3. <span data-ttu-id="8a1b6-117">Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="8a1b6-118">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="8a1b6-118">Company</span></span>

| <span data-ttu-id="8a1b6-119">Stafur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-119">Letter</span></span> | <span data-ttu-id="8a1b6-120">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="8a1b6-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="8a1b6-121">A</span><span class="sxs-lookup"><span data-stu-id="8a1b6-121">A</span></span>      | <span data-ttu-id="8a1b6-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="8a1b6-122">Adventure Works</span></span> |
| <span data-ttu-id="8a1b6-123">F</span><span class="sxs-lookup"><span data-stu-id="8a1b6-123">F</span></span>      | <span data-ttu-id="8a1b6-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8a1b6-124">Fabrikam</span></span>        |
| <span data-ttu-id="8a1b6-125">F</span><span class="sxs-lookup"><span data-stu-id="8a1b6-125">C</span></span>      | <span data-ttu-id="8a1b6-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="8a1b6-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="8a1b6-127">Útlitsgerð</span><span class="sxs-lookup"><span data-stu-id="8a1b6-127">Layout version</span></span>

| <span data-ttu-id="8a1b6-128">Útgáfunúmer</span><span class="sxs-lookup"><span data-stu-id="8a1b6-128">Version number</span></span> | <span data-ttu-id="8a1b6-129">lýsing</span><span class="sxs-lookup"><span data-stu-id="8a1b6-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1b6-130">3</span><span class="sxs-lookup"><span data-stu-id="8a1b6-130">3</span></span>              | <span data-ttu-id="8a1b6-131">Grunnútgáfan sem styður margar skjástærðir fyrir mismunandi tæki og myndhlutföll</span><span class="sxs-lookup"><span data-stu-id="8a1b6-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="8a1b6-132">3.1</span><span class="sxs-lookup"><span data-stu-id="8a1b6-132">3.1</span></span>            | <span data-ttu-id="8a1b6-133">Grunngerðin sem hefur viðbótarstuðning fyrir **Vörur sem mælt er með** gluggann.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="8a1b6-134">Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-134">Persona</span></span>

| <span data-ttu-id="8a1b6-135">Skammstöfun</span><span class="sxs-lookup"><span data-stu-id="8a1b6-135">Abbreviation</span></span> | <span data-ttu-id="8a1b6-136">Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-136">Persona</span></span>       | <span data-ttu-id="8a1b6-137">Innihald</span><span class="sxs-lookup"><span data-stu-id="8a1b6-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="8a1b6-138">CSH</span><span class="sxs-lookup"><span data-stu-id="8a1b6-138">CSH</span></span>          | <span data-ttu-id="8a1b6-139">Gjaldkeri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-139">Cashier</span></span>       | <span data-ttu-id="8a1b6-140">Gjaldkeraútlit felur í sér öll viðskiptatengd starfsemi, svo sem viðskiptavina pantanir, skil, afslætti, ógildingu og gjafakort.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="8a1b6-141">Þessar útlitsgerðir innihalda einnig dagleg verkefni fyrir birgðastjórnun, svo sem verðathuganir, uppflettingu í birgðum og birgðatalningar.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="8a1b6-142">Einnig er boðið upp á grunnstjórnun vakta varðandi byrjunarupphæðir, frestun vakta og tímaklukku.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="8a1b6-143">MGR</span><span class="sxs-lookup"><span data-stu-id="8a1b6-143">MGR</span></span>          | <span data-ttu-id="8a1b6-144">Verslunarstjóri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-144">Store Manager</span></span> | <span data-ttu-id="8a1b6-145">Útlit fyrir verslunarstjóra innihalda öll viðskiptatengda starfsemi sem er að finna í gjaldkeraútlitinu, en einnig fela í sér skattahnekkingar.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="8a1b6-146">Þessar útlitsgerðir innihalda einnig dagleg verkefni sem tengjast birgðastjórnun, svo sem verðathuganir, uppfletting í birgðum og birgðatalningu.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="8a1b6-147">Í boði er vaktastjórnun til að hefja, fresta og ljúka vöktum.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="8a1b6-148">Að auki innihalda útlitsgerðirnar skúffuvalmöguleika fyrir færslur, brottnám, talningu skiptimyntar og peningaflutninga í öryggishólf og banka.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="8a1b6-149">Að lokum veita þessar útlitsgerðir aðgang árangursskýrslum og gera mögulegt að prenta út X og Z skýrslur.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="8a1b6-150">STK</span><span class="sxs-lookup"><span data-stu-id="8a1b6-150">STK</span></span>          | <span data-ttu-id="8a1b6-151">Afgreiðslustarfsmaður birgða</span><span class="sxs-lookup"><span data-stu-id="8a1b6-151">Stock Clerk</span></span>   | <span data-ttu-id="8a1b6-152">Útlitsgerðir fyrir Afgreiðslustarfsmaður birgða eru fínstilltar fyrir birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="8a1b6-153">Þær fela í sér aðgang að daglegum verkefnum verðathugunar, uppflettingu í birgðum, tiltekt og móttöku, birgðatalningu og sundurhlutun setts.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="8a1b6-154">Þessar útlitsgerðir veita einnig grunnaðgerðir fyrir vaktir varðandi tímaklukku og frestun vakta.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="8a1b6-155">Þrátt fyrir að þessar útlitsgerðir séu aðallega ætlaðar fyrir aðgerðir í bakvinnslu, hafa afgreiðslustarfsmenn birgða aðgang að sömu aðgerðum og gjaldkerar á færsluskjáum.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="8a1b6-156">Dæmi útlit</span><span class="sxs-lookup"><span data-stu-id="8a1b6-156">Example layout</span></span>

<span data-ttu-id="8a1b6-157">Hér er dæmi um kenni skjáútlits fyrir Fabrikam fyrirtækið, útlitsútgáfu 3, og Verslunarstjóri einstaklingur:</span><span class="sxs-lookup"><span data-stu-id="8a1b6-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="8a1b6-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="8a1b6-158">F3MGR</span></span>

<span data-ttu-id="8a1b6-159">Eftirfarandi skýringarmynd sýnir dæmi um Velkomin(n) skjáinn sem birtist Fabrikam verslunarstjóranum.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Velkomin(n) skjár fyrir Fabrikam verslunarstjórann](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="8a1b6-161">Útlitsstærðir</span><span class="sxs-lookup"><span data-stu-id="8a1b6-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="8a1b6-162">Fullt útlit á móti þjöppuðu útliti</span><span class="sxs-lookup"><span data-stu-id="8a1b6-162">Full vs. compact layouts</span></span>

<span data-ttu-id="8a1b6-163">Útlit skjás getur einnig innihaldið skilgreiningar fyrir bæði heilt tæki og þjappað tæki.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="8a1b6-164">Þar af leiðandi getur notanda verið úthlutað á eina tegund skjáútlits sem mun virka í mismunandi stærðar- og skjámyndaþáttum innan verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="8a1b6-165">**Modern POS - Fullt** – Fullt útlit hentar yfirleitt best fyrir stærri skjái eins og tölvuskjái eða spjaldtölvur.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="8a1b6-166">Notendur geta valið viðmótseiningar sem útlitið inniheldur, tilgreint stærð og staðsetningu þessara eininga og stillt nákvæma eiginleika þeirra.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="8a1b6-167">Full útlit styðja bæði þversniðis- og langsniðsskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="8a1b6-168">**Modern POS - Þjappað** – Þjappað útlit hentar yfirleitt best fyrir síma eða litlar spjaldtölvur.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="8a1b6-169">Hönnunarmöguleikar takmarkast við smækkuð tæki.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="8a1b6-170">Notendur geta skilgreint dálka og reiti fyrir móttöku- og samtölusvæði.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="8a1b6-171">Skjáupplausnir sem boðið er upp á</span><span class="sxs-lookup"><span data-stu-id="8a1b6-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="8a1b6-172">Eftirfarandi tafla sýnir þær útlitsstærðir sem eru í boði fyrir hefðbundnar skjáupplausnir.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="8a1b6-173">Útlitsgerð</span><span class="sxs-lookup"><span data-stu-id="8a1b6-173">Layout type</span></span> | <span data-ttu-id="8a1b6-174">Upplausn</span><span class="sxs-lookup"><span data-stu-id="8a1b6-174">Resolution</span></span> | <span data-ttu-id="8a1b6-175">Myndhlutfall</span><span class="sxs-lookup"><span data-stu-id="8a1b6-175">Aspect ratio</span></span> | <span data-ttu-id="8a1b6-176">Markskjár</span><span class="sxs-lookup"><span data-stu-id="8a1b6-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="8a1b6-177">Þjappa\*</span><span class="sxs-lookup"><span data-stu-id="8a1b6-177">Compact\*</span></span>   | <span data-ttu-id="8a1b6-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="8a1b6-178">480 × 853</span></span>  | <span data-ttu-id="8a1b6-179">16:9</span><span class="sxs-lookup"><span data-stu-id="8a1b6-179">16:9</span></span>         | <span data-ttu-id="8a1b6-180">Símar</span><span class="sxs-lookup"><span data-stu-id="8a1b6-180">Phones</span></span>                  |
| <span data-ttu-id="8a1b6-181">Fullt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-181">Full</span></span>        | <span data-ttu-id="8a1b6-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="8a1b6-182">1024 × 768</span></span> | <span data-ttu-id="8a1b6-183">4:3</span><span class="sxs-lookup"><span data-stu-id="8a1b6-183">4:3</span></span>          | <span data-ttu-id="8a1b6-184">Spjaldtölvur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-184">Tablets</span></span>                 |
| <span data-ttu-id="8a1b6-185">Fullt\*</span><span class="sxs-lookup"><span data-stu-id="8a1b6-185">Full\*</span></span>      | <span data-ttu-id="8a1b6-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="8a1b6-186">1280 × 720</span></span> | <span data-ttu-id="8a1b6-187">16:9</span><span class="sxs-lookup"><span data-stu-id="8a1b6-187">16:9</span></span>         | <span data-ttu-id="8a1b6-188">Spjaldtölvur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-188">Tablets</span></span>                 |
| <span data-ttu-id="8a1b6-189">Fullt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-189">Full</span></span>        | <span data-ttu-id="8a1b6-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="8a1b6-190">1366 × 768</span></span> | <span data-ttu-id="8a1b6-191">16:9</span><span class="sxs-lookup"><span data-stu-id="8a1b6-191">16:9</span></span>         | <span data-ttu-id="8a1b6-192">Spjaldtölvur, stærri skjáir</span><span class="sxs-lookup"><span data-stu-id="8a1b6-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="8a1b6-193">Fullt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-193">Full</span></span>        | <span data-ttu-id="8a1b6-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="8a1b6-194">1440 × 960</span></span> | <span data-ttu-id="8a1b6-195">3:2</span><span class="sxs-lookup"><span data-stu-id="8a1b6-195">3:2</span></span>          | <span data-ttu-id="8a1b6-196">Spjaldtölvur, stærri skjáir</span><span class="sxs-lookup"><span data-stu-id="8a1b6-196">Tablets, larger screens</span></span> |

<span data-ttu-id="8a1b6-197">\* Þessir viðbótar útlitsstærðir eru aðeins tiltækar í Adventure Works og Fabrikam útliti.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="8a1b6-198">POS velur sjálfkrafa útlitsstærðir, byggt á nærtækustu stærð sem er tiltæk fyrir skjáupplausn núverandi skjámyndar forrits.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="8a1b6-199">Til að finna skjákenni útlits og upplausn útlits sem eru í notkun núna, skal opna Retail Modern POS (MPOS) eða Retail Cloud POS (CPOS) **Stillingar** síðuna og leita í **Lotuupplýsingar** hlutanum.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="8a1b6-200">Þú getur einnig séð raunupplausn glugga fyrir forrit eða vafraramma sem verið er að nota núna.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="8a1b6-201">Eftir að þú hefur fengið þessar upplýsingar er hægt að finna uppsprettu útlitsefnis í Retail með því að fara á **Uppsetning rásar** > **Uppsetning POS** > **POS** > **Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![Útlit skjáa og útlitsupplausnir/stærðir í Retail og POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="8a1b6-203">Fyrirtæki og vörumerki</span><span class="sxs-lookup"><span data-stu-id="8a1b6-203">Companies and brands</span></span>

<span data-ttu-id="8a1b6-204">Sérhver ímyndað fyrirtæki er beint að mismunandi smásöluhluta og inniheldur vörulista sem eru stillt fyrir markað fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="8a1b6-205">Hvert fyrirtæki hefur einstakt vörumerkjaútlit sem fylgir vörum þess.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="8a1b6-206">Vörumerkjaþættir innihalda áherslulit, dökkt eða létt þema og meðfylgjandi myndir sem veita raunhæfa upplifun.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="8a1b6-207">Fyrirtækjahluti og sjónræn einkenni</span><span class="sxs-lookup"><span data-stu-id="8a1b6-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="8a1b6-208">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="8a1b6-208">Company</span></span>         | <span data-ttu-id="8a1b6-209">Staður</span><span class="sxs-lookup"><span data-stu-id="8a1b6-209">Location</span></span> | <span data-ttu-id="8a1b6-210">Hluti</span><span class="sxs-lookup"><span data-stu-id="8a1b6-210">Segment</span></span>        | <span data-ttu-id="8a1b6-211">Áhersla</span><span class="sxs-lookup"><span data-stu-id="8a1b6-211">Accent</span></span> | <span data-ttu-id="8a1b6-212">Þema</span><span class="sxs-lookup"><span data-stu-id="8a1b6-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="8a1b6-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="8a1b6-213">Adventure Works</span></span> | <span data-ttu-id="8a1b6-214">Seattle</span><span class="sxs-lookup"><span data-stu-id="8a1b6-214">Seattle</span></span>  | <span data-ttu-id="8a1b6-215">Íþróttavörur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-215">Sporting Goods</span></span> | <span data-ttu-id="8a1b6-216">Blátt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-216">Blue</span></span>   | <span data-ttu-id="8a1b6-217">Dökkt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-217">Dark</span></span>  |
| <span data-ttu-id="8a1b6-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8a1b6-218">Fabrikam</span></span>        | <span data-ttu-id="8a1b6-219">Houston</span><span class="sxs-lookup"><span data-stu-id="8a1b6-219">Houston</span></span>  | <span data-ttu-id="8a1b6-220">Tíska</span><span class="sxs-lookup"><span data-stu-id="8a1b6-220">Fashion</span></span>        | <span data-ttu-id="8a1b6-221">Grænt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-221">Green</span></span>  | <span data-ttu-id="8a1b6-222">Ljóst</span><span class="sxs-lookup"><span data-stu-id="8a1b6-222">Light</span></span> |
| <span data-ttu-id="8a1b6-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="8a1b6-223">Contoso</span></span>         | <span data-ttu-id="8a1b6-224">Boston</span><span class="sxs-lookup"><span data-stu-id="8a1b6-224">Boston</span></span>   | <span data-ttu-id="8a1b6-225">Raftæki</span><span class="sxs-lookup"><span data-stu-id="8a1b6-225">Electronics</span></span>    | <span data-ttu-id="8a1b6-226">Rautt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-226">Red</span></span>    | <span data-ttu-id="8a1b6-227">Dökkt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="8a1b6-228">Adventure Works og Fabrikam eru tvö flaggskip vörumerki.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="8a1b6-229">Contoso er í boði, en ekki hefur verið gert ráð fyrir öllum útlitsgerðum.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="8a1b6-230">Eftirfarandi myndir sýna dæmi um velkomin(n) síðu og viðskiptasíðu fyrir sýnifyrirtækin þrjú.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="8a1b6-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="8a1b6-231">Adventure Works</span></span>

![Sýnigögn velkomin(n) síðu fyrir Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Sýnigögn viðskiptasíðu fyrir Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="8a1b6-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8a1b6-234">Fabrikam</span></span>

![Sýnigögn velkomin(n) síðu fyrir Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Sýnigögn viðskiptasíðu fyrir Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="8a1b6-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="8a1b6-237">Contoso</span></span>

![Sýnigögn útlits fyrir Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="8a1b6-239">Notandaskráning í fylki</span><span class="sxs-lookup"><span data-stu-id="8a1b6-239">User sign in matrix</span></span>

<span data-ttu-id="8a1b6-240">Náð hefur verið í notendur fyrir mismunandi skjáútlit.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="8a1b6-241">Með því að nota eftirfarandi töflu, ættir þú að fá aðgang að öllum skjáunum.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="8a1b6-242">Skráðu þig inn með því að nota viðeigandi stjórnandakenni.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="8a1b6-243">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="8a1b6-243">Company</span></span>         | <span data-ttu-id="8a1b6-244">Útlitskenni afgreiðsluskjás</span><span class="sxs-lookup"><span data-stu-id="8a1b6-244">Screen layout ID</span></span> | <span data-ttu-id="8a1b6-245">Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="8a1b6-245">Persona</span></span>          | <span data-ttu-id="8a1b6-246">Stjórnandakenni</span><span class="sxs-lookup"><span data-stu-id="8a1b6-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="8a1b6-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="8a1b6-247">Adventure Works</span></span> | <span data-ttu-id="8a1b6-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="8a1b6-248">A3MGR</span></span>            | <span data-ttu-id="8a1b6-249">Verslunarstjóri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-249">Store Manager</span></span>    | <span data-ttu-id="8a1b6-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="8a1b6-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="8a1b6-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="8a1b6-251">Adventure Works</span></span> | <span data-ttu-id="8a1b6-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="8a1b6-252">A3CSH</span></span>            | <span data-ttu-id="8a1b6-253">Gjaldkeri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-253">Cashier</span></span>          | <span data-ttu-id="8a1b6-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="8a1b6-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="8a1b6-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="8a1b6-255">Adventure Works</span></span> | <span data-ttu-id="8a1b6-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="8a1b6-256">A3STK</span></span>            | <span data-ttu-id="8a1b6-257">Afgreiðslustarfsmaður birgða</span><span class="sxs-lookup"><span data-stu-id="8a1b6-257">Stock Clerk</span></span>      | <span data-ttu-id="8a1b6-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="8a1b6-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="8a1b6-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8a1b6-259">Fabrikam</span></span>        | <span data-ttu-id="8a1b6-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="8a1b6-260">F3MGR</span></span>            | <span data-ttu-id="8a1b6-261">Verslunarstjóri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-261">Store Manager</span></span>    | <span data-ttu-id="8a1b6-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="8a1b6-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="8a1b6-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8a1b6-263">Fabrikam</span></span>        | <span data-ttu-id="8a1b6-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="8a1b6-264">F3CSH</span></span>            | <span data-ttu-id="8a1b6-265">Gjaldkeri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-265">Cashier</span></span>          | <span data-ttu-id="8a1b6-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="8a1b6-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="8a1b6-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="8a1b6-267">Fabrikam</span></span>        | <span data-ttu-id="8a1b6-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="8a1b6-268">F3STK</span></span>            | <span data-ttu-id="8a1b6-269">Afgreiðslustarfsmaður birgða</span><span class="sxs-lookup"><span data-stu-id="8a1b6-269">Stock Clerk</span></span>      | <span data-ttu-id="8a1b6-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="8a1b6-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="8a1b6-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="8a1b6-271">Contoso</span></span>         | <span data-ttu-id="8a1b6-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="8a1b6-272">C3MGR</span></span>            | <span data-ttu-id="8a1b6-273">Verslunarstjóri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-273">Store Manager</span></span>    | <span data-ttu-id="8a1b6-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="8a1b6-274">000100, 000111</span></span>         |
| <span data-ttu-id="8a1b6-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="8a1b6-275">Contoso</span></span>         | <span data-ttu-id="8a1b6-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="8a1b6-276">C3CSH</span></span>            | <span data-ttu-id="8a1b6-277">Gjaldkeri</span><span class="sxs-lookup"><span data-stu-id="8a1b6-277">Cashier</span></span>          | <span data-ttu-id="8a1b6-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="8a1b6-278">000110, 000120</span></span>         |
| <span data-ttu-id="8a1b6-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="8a1b6-279">Contoso</span></span>         | <span data-ttu-id="8a1b6-280">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-280">Not applicable</span></span>   | <span data-ttu-id="8a1b6-281">Afgreiðslustarfsmaður birgða</span><span class="sxs-lookup"><span data-stu-id="8a1b6-281">Stock Clerk</span></span>      | <span data-ttu-id="8a1b6-282">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="8a1b6-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="8a1b6-283">Til að ná sem bestum árangri skaltu virkja afgreiðslukassa á viðkomandi verslunarsvæði og setja fyrirtækið í félagið einstaklingsins sem þú ætlar að nota þegar þú skráir þig inn.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="8a1b6-284">Þannig hjálpar þú að tryggja að sjónrænt útlit og vörumerkjamyndir samræmist upplifuninni.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="8a1b6-285">Til dæmis, ef þú hefur áhuga á að sjá Fabrikam útlit fyrir gjaldkeri, þá ættir þú að virkja afgreiðslukassa í Houston versluninni.</span><span class="sxs-lookup"><span data-stu-id="8a1b6-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

