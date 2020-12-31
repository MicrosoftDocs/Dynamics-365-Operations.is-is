---
title: Rafræn skýrslugerð Uppfærðu snið með því að taka upp nýja grunnútgáfu sniðs
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur viðhaldið skilgreiningarsnið fyrir rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17fe6d772040c73959685920743225c128421951
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684261"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="29c85-103">Rafræn skýrslugerð Uppfærðu snið með því að taka upp nýja grunnútgáfu sniðs</span><span class="sxs-lookup"><span data-stu-id="29c85-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29c85-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur viðhaldið skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="29c85-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="29c85-105">Þetta ferli útskýrir hvernig sérsniðin útgáfu sniðs er hægt að mynda á grundvelli snið móttekið frá veitandi skilgreiningar (CP).</span><span class="sxs-lookup"><span data-stu-id="29c85-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="29c85-106">Það útskýrir einnig hvernig eigi að taka upp nýja grunnútgáfu af því sniði.</span><span class="sxs-lookup"><span data-stu-id="29c85-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="29c85-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlunum „Stofna skilgreiningarveitu og merkja hana sem virka” og „Nota stofnuð snið til að mynda rafræn skjöl fyrir greiðslur”.</span><span class="sxs-lookup"><span data-stu-id="29c85-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="29c85-108">Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="29c85-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="29c85-109">Veljið skilgreiningu sniðs fyrir sérsnið</span><span class="sxs-lookup"><span data-stu-id="29c85-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="29c85-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="29c85-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="29c85-111">Í þessu dæmi mun sýnifyrirtækið Litware, Inc. (https://www.litware.com) vinna sem skilgreiningarveita sem styður skilgreiningarsnið fyrir rafrænar greiðslur fyrir tiltekið land.</span><span class="sxs-lookup"><span data-stu-id="29c85-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="29c85-112">Sýnifyrirtæki Proseware, Inc. (http://www.proseware.com) mun vinna sem neytandi skilgreiningarsniðs sem Litware, Inc. útvegaði.</span><span class="sxs-lookup"><span data-stu-id="29c85-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="29c85-113">Proseware, Inc. motar snið í sumum svæðum þess lands.</span><span class="sxs-lookup"><span data-stu-id="29c85-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="29c85-114">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="29c85-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="29c85-115">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="29c85-115">Click Show filters.</span></span>
4. <span data-ttu-id="29c85-116">Notið eftirfarandi síur: færðu inn síugildi „UK sérsniðið upphugsað” á svæði „Heiti" með því að nota síuvirknitáknið „byrjar á”.</span><span class="sxs-lookup"><span data-stu-id="29c85-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="29c85-117">Valið skilgreiningarsnið (UK sérsniðið upphugsað) BACS, er í eigu Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="29c85-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="29c85-118">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="29c85-118">Click Show filters.</span></span>
6. <span data-ttu-id="29c85-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="29c85-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="29c85-120">Útgáfa sniðs með stöðuna Lokið mun verða notað af Proseware, Inc. fyrir sérstillingu.</span><span class="sxs-lookup"><span data-stu-id="29c85-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="29c85-121">Stofna nýja skilgreiningu fyrir sérsniðið snið rafrænna skjala</span><span class="sxs-lookup"><span data-stu-id="29c85-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="29c85-122">Proseware, Inc. hefur móttekið útgáfa 1.1 fyrir skilgreiningar BACS (UK upphugsað) sem inniheldur upphaflegt snið til að mynda rafræn greiðsluskjöl úr Litware, Inc. í samræmi við þjónustuáskrift þeirra.</span><span class="sxs-lookup"><span data-stu-id="29c85-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="29c85-123">Proseware, Inc. vill byrja að nota þetta sem staðal fyrir þeirra land en nokkur sérstillingar er krafist til að styðja sérstakar svæðisbundið kröfur.</span><span class="sxs-lookup"><span data-stu-id="29c85-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="29c85-124">Proseware, Inc. villl einnig halda getunni til að uppfæra sérsniðnir snið um leið og ný útgáfu þess (með breytingum til að styðja við landsbundnar þarfir) kemur út hjá Litware, Inc. og það vill framkvæma þessa uppfærslu með sem minnstum tilkostnaði.</span><span class="sxs-lookup"><span data-stu-id="29c85-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="29c85-125">Til að gera þetta þarf Proseware, Inc. að stofna skilgreiningu með því að nota Litware, Inc. skilgreininguna BACS (UK upphugsað) sem grunn.</span><span class="sxs-lookup"><span data-stu-id="29c85-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="29c85-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29c85-126">Close the page.</span></span>
2. <span data-ttu-id="29c85-127">Veljið Proseware, Inc. til að gera hana að virkri veitu.</span><span class="sxs-lookup"><span data-stu-id="29c85-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="29c85-128">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="29c85-128">Click Set active.</span></span>
4. <span data-ttu-id="29c85-129">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="29c85-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="29c85-130">Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="29c85-131">Í trénu, veljið 'Payments (einfaldað líkan)\BACS (UK upphugsað)'.</span><span class="sxs-lookup"><span data-stu-id="29c85-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="29c85-132">Velja skilgreiningu BACS (Bretland upphugsað) úr Litware, Inc. Proseware, Inc. mun nota útgáfu 1.1 sem grunn fyrir sérsniðnu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="29c85-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="29c85-133">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="29c85-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="29c85-134">Þetta gerir mögulegt að stofna nýja skilgreiningu fyrir sérsniðna greiðslusnið.</span><span class="sxs-lookup"><span data-stu-id="29c85-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="29c85-135">Í svæðinu Nýtt, veljið 'Leiða af nafni: BACS (UK upphugsað), Litware, Inc'.</span><span class="sxs-lookup"><span data-stu-id="29c85-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="29c85-136">Veljið valkost afleiddur til að staðfesta notkun BACS (UK upphugsað) sem grunn til að stofna sérsniðna útgáfu.</span><span class="sxs-lookup"><span data-stu-id="29c85-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="29c85-137">Í reitinn Heiti skal slá inn 'BACS (UK upphugsað sérsniðið)'.</span><span class="sxs-lookup"><span data-stu-id="29c85-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="29c85-138">Færið inn 'BACS greiðsla lánardrottins (UK sérsniðið upphugsað)' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="29c85-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="29c85-139">Virkt skilgreiningarveitu (Proseware, Inc) er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="29c85-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="29c85-140">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="29c85-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="29c85-141">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="29c85-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="29c85-142">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="29c85-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="29c85-143">Sérsníða snið fyrir rafrænt skjal</span><span class="sxs-lookup"><span data-stu-id="29c85-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="29c85-144">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="29c85-144">Click Designer.</span></span>
2. <span data-ttu-id="29c85-145">Smellt er á Víkka/draga saman.</span><span class="sxs-lookup"><span data-stu-id="29c85-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="29c85-146">Smellt er á Víkka/draga saman.</span><span class="sxs-lookup"><span data-stu-id="29c85-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="29c85-147">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="29c85-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="29c85-148">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="29c85-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="29c85-149">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="29c85-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="29c85-150">Í svæðið Heiti, færðu inn ‚IBAN-númer'.</span><span class="sxs-lookup"><span data-stu-id="29c85-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="29c85-151">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="29c85-151">Click OK.</span></span>
9. <span data-ttu-id="29c85-152">Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="29c85-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="29c85-153">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="29c85-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="29c85-154">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="29c85-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="29c85-155">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="29c85-155">Click OK.</span></span>
13. <span data-ttu-id="29c85-156">Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="29c85-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="29c85-157">Í reitinn hámarkslengd skal slá inn 60.</span><span class="sxs-lookup"><span data-stu-id="29c85-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="29c85-158">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="29c85-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="29c85-159">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="29c85-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="29c85-160">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="29c85-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="29c85-161">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="29c85-162">Útvíkka 'model\Payments\Creditor\Account', í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="29c85-163">Í tré skal velja 'model\Payments\Creditor\Account\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="29c85-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="29c85-164">Í tré skal velja 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\IBAN\String'.</span><span class="sxs-lookup"><span data-stu-id="29c85-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="29c85-165">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="29c85-165">Click Bind.</span></span>
23. <span data-ttu-id="29c85-166">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="29c85-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="29c85-167">Villuleita sérsniðna snið</span><span class="sxs-lookup"><span data-stu-id="29c85-167">Validate the customized format</span></span>
1. <span data-ttu-id="29c85-168">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="29c85-168">Click Validate.</span></span>

    <span data-ttu-id="29c85-169">Villuleita sérsniðna útlit sniðs og breytingar gagnakortalagning til að tryggja að allar bindingar eru í lagi.</span><span class="sxs-lookup"><span data-stu-id="29c85-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="29c85-170">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29c85-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="29c85-171">Breyta stöðu núgildandi útgáfa grunnstillingar sérstillts sniðs</span><span class="sxs-lookup"><span data-stu-id="29c85-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="29c85-172">Breyta stöðu hannaðs skilgreiningarsniðs - úr DRÖG í LOKIÐ til að gera hann tiltækan fyrir myndun greiðsluskjals.</span><span class="sxs-lookup"><span data-stu-id="29c85-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="29c85-173">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="29c85-173">Click Change status.</span></span>

    <span data-ttu-id="29c85-174">Athugið að núverandi útgáfa valinnar skilgreiningar er í stöðunni DRÖG.</span><span class="sxs-lookup"><span data-stu-id="29c85-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="29c85-175">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="29c85-175">Click Complete.</span></span>
3. <span data-ttu-id="29c85-176">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="29c85-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="29c85-177">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="29c85-177">Click OK.</span></span>
5. <span data-ttu-id="29c85-178">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="29c85-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="29c85-179">Athugið að stofnuð skilgreining er vistuð sem lokin útgáfa 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="29c85-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="29c85-180">Þetta þýðir að það er útgáfa 1 sérsniðna BACS (UK sérsniðið upphugsað) snið, sem er byggð á sniði útgáfu 1 BACS (Bretland upphugsað), sem er byggð á 1 útgáfa gagnalíkans Greiðslna (einfaldaður líkan).</span><span class="sxs-lookup"><span data-stu-id="29c85-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="29c85-181">Prófa Sérsniðnar snið til að mynda greiðsluskrár</span><span class="sxs-lookup"><span data-stu-id="29c85-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="29c85-182">Ljúkið skrefunum í ferlinu „Nota stofnuð snið til að mynda rafræn skjöl fyrir greiðslur” í samhliða lotu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="29c85-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="29c85-183">Velja BACS snið (Bretland sérsniðið upphugsað) í færibreytum rafrænnar greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="29c85-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="29c85-184">Gangið úr skugga um að stofnaða greiðsluskráin inniheldur nýlega kynnta XML-hnútnum sem setur fram iban-kóða í samræmi við svæðisbundið þarfir.</span><span class="sxs-lookup"><span data-stu-id="29c85-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="29c85-185">Uppfæra fyrirliggjandi landsbunda skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="29c85-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="29c85-186">Litware, Inc. þarf að uppfæra skilgreiningu BACS (UK upphugsað) og aðlaga nýjar svæðisbundnar kröfur fyrir stjórnun á sniði rafræna skjalið.</span><span class="sxs-lookup"><span data-stu-id="29c85-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="29c85-187">Síðar, þetta mun vera innan nýja útgáfu þessarar skilgreiningar sem verður í boði fyrir áskrifendur þjónustu, þar á meðal Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="29c85-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="29c85-188">Í raunverulegum vinnslum sem tengjast þjónustuveitum, er hægt að flytja inn hverja nýja útgáfa af BACS (UK upphugsað) úr geymslu Litware, Inc. með Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="29c85-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="29c85-189">Í þessu ferli verður líkt eftir þessu með því að uppfæra BACS (UK upphugsað) fyrir hönd þjónustuveitanda.</span><span class="sxs-lookup"><span data-stu-id="29c85-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="29c85-190">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29c85-190">Close the page.</span></span>
2. <span data-ttu-id="29c85-191">Velja Litware, Inc. veitu.</span><span class="sxs-lookup"><span data-stu-id="29c85-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="29c85-192">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="29c85-192">Click Set active.</span></span>
4. <span data-ttu-id="29c85-193">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="29c85-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="29c85-194">Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="29c85-195">Í trénu, veljið 'Payments (einfaldað líkan)\BACS (UK upphugsað)'.</span><span class="sxs-lookup"><span data-stu-id="29c85-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="29c85-196">Útgáfudrögin í eigu Litware, Inc. veita BACS (UK upphugsað) eru valin til að koma með breytingar til að styðja við nýjar svæðisbundnar kröfur.</span><span class="sxs-lookup"><span data-stu-id="29c85-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="29c85-197">Staðfæra grunnsnið rafræna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="29c85-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="29c85-198">Gefum okkur til staðar séu nýjar svæðisbundnar þarfir sem Litware, Inc. þarf að styðja:</span><span class="sxs-lookup"><span data-stu-id="29c85-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="29c85-199">Gildi fyrir SWIFT-kóða banka lánveitanda í hverri greiðslufærslu.</span><span class="sxs-lookup"><span data-stu-id="29c85-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="29c85-200">Takmörkun uppá 100 stafi fyrir lengd textans fyrir nafn lánardrottins í myndunarskránni.</span><span class="sxs-lookup"><span data-stu-id="29c85-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="29c85-201">Nýjar landsbundnar kröfur</span><span class="sxs-lookup"><span data-stu-id="29c85-201">New country-specific requirements</span></span>  
- <span data-ttu-id="29c85-202">Velja útgáfu sem eru drög fyrir skilgreiningu sem óskað er til að kynna til leiks breytingar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="29c85-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="29c85-203">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="29c85-203">Click Designer.</span></span>
2. <span data-ttu-id="29c85-204">Smellt er á Víkka/draga saman.</span><span class="sxs-lookup"><span data-stu-id="29c85-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="29c85-205">Smellt er á Víkka/draga saman.</span><span class="sxs-lookup"><span data-stu-id="29c85-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="29c85-206">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="29c85-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="29c85-207">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="29c85-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="29c85-208">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="29c85-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="29c85-209">Í svæðið Heiti, færðu inn ‚SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="29c85-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="29c85-210">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="29c85-210">Click OK.</span></span>
9. <span data-ttu-id="29c85-211">Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="29c85-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="29c85-212">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="29c85-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="29c85-213">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="29c85-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="29c85-214">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="29c85-214">Click OK.</span></span>
13. <span data-ttu-id="29c85-215">Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="29c85-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="29c85-216">Í reitinn hámarkslengd skal slá inn 100.</span><span class="sxs-lookup"><span data-stu-id="29c85-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="29c85-217">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="29c85-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="29c85-218">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="29c85-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="29c85-219">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="29c85-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="29c85-220">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="29c85-221">Útvíkka 'model\Payments\Creditor\Agent', í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="29c85-222">Í tré skal velja 'model\Payments\Creditor\Agent\SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="29c85-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="29c85-223">Í tré skal velja 'Xml\Message\Payments\Item = model.Payments\Vendor\Bank\SWIFT\String'.</span><span class="sxs-lookup"><span data-stu-id="29c85-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="29c85-224">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="29c85-224">Click Bind.</span></span>
23. <span data-ttu-id="29c85-225">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="29c85-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="29c85-226">Sannprófa staðbundinn snið</span><span class="sxs-lookup"><span data-stu-id="29c85-226">Validate the localized format</span></span>
1. <span data-ttu-id="29c85-227">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="29c85-227">Click Validate.</span></span>
2. <span data-ttu-id="29c85-228">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29c85-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="29c85-229">Breyta stöðu á gildandi útgáfu af grunnskilgreiningarsniði</span><span class="sxs-lookup"><span data-stu-id="29c85-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="29c85-230">Breyta stöðu uppfærðs grunns skilgreiningarsniðs - úr DRÖG í LOKIÐ til að gera hann tiltækan fyrir myndun greiðsluskjals og uppfærslur á skilgreiningarsniðum sem fengin eru úr því.</span><span class="sxs-lookup"><span data-stu-id="29c85-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="29c85-231">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="29c85-231">Click Change status.</span></span>

    <span data-ttu-id="29c85-232">Athugið að núverandi útgáfa valinnar skilgreiningar er í stöðunni DRÖG.</span><span class="sxs-lookup"><span data-stu-id="29c85-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="29c85-233">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="29c85-233">Click Complete.</span></span>
3. <span data-ttu-id="29c85-234">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="29c85-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="29c85-235">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="29c85-235">Click OK.</span></span>
5. <span data-ttu-id="29c85-236">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="29c85-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="29c85-237">Breyta Grunnútgáfa fyrir sérsniðna skilgreiningarsnið</span><span class="sxs-lookup"><span data-stu-id="29c85-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="29c85-238">Proseware, Inc. er upplýst um að ný útgáfu 1,2 af skilgreiningar BACS (UK upphugsað) er tiltækt til að mynda rafræn greiðsluskjöl í samræmi við til nýlega tilkynntar landsbundnar þarfir.</span><span class="sxs-lookup"><span data-stu-id="29c85-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="29c85-239">Proseware, Inc. vill byrja að nota það sem staðal fyrir landið.</span><span class="sxs-lookup"><span data-stu-id="29c85-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="29c85-240">Til að svo megi verða þarf Proseware, Inc. að breyta grunnskilgreiningarútgáfa fyrir sérsniðna skilgreiningu BACS (UK upphugsað sérsniðið).</span><span class="sxs-lookup"><span data-stu-id="29c85-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="29c85-241">Í stað útgáfu 1,1 af BACS (UK upphugsað) skal nota nýjú útgáfuna 1,2.</span><span class="sxs-lookup"><span data-stu-id="29c85-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="29c85-242">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="29c85-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="29c85-243">Veldu Proseware, Inc. veitandi til að merkja það sem virkt.</span><span class="sxs-lookup"><span data-stu-id="29c85-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="29c85-244">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="29c85-244">Click Set active.</span></span>
4. <span data-ttu-id="29c85-245">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="29c85-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="29c85-246">Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="29c85-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="29c85-247">Í trénu, víkka út "greiðslur" (einfaldað líkan)/BACS (UK upphugsað)</span><span class="sxs-lookup"><span data-stu-id="29c85-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="29c85-248">Í trénu skal velja 'greiðslur (einfaldað líkan)\BACS (UK upphugsað)\BACS (UK upphugsað sérsniðið)'.</span><span class="sxs-lookup"><span data-stu-id="29c85-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="29c85-249">Velja skilgreiningu (Bretland sérsniðið upphugsað) BACS, sem er í eigu Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="29c85-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="29c85-250">Nota útgáfu sem eru drög fyrir skilgreiningu sem valin er til að kynna til leiks breytingar sem þarf.</span><span class="sxs-lookup"><span data-stu-id="29c85-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="29c85-251">Smellt er á Endurreikna grunn.</span><span class="sxs-lookup"><span data-stu-id="29c85-251">Click Rebase.</span></span>

    <span data-ttu-id="29c85-252">Veljið nýja útgáfu 1,2 fyrir grunnskilgreiningu til að nota sem nýjan grunn til að uppfæra skilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="29c85-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="29c85-253">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="29c85-253">Click OK.</span></span>

    <span data-ttu-id="29c85-254">Athugið að sumar árekstra hafa fundust milli samruna sérsniðnu útgáfunnar og nýja grunnútgáfa sem standa fyrir sumar breytingar sem ekki er hægt að sameina sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="29c85-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="29c85-255">Leysa úr Árekstrar við endurreikning grunns</span><span class="sxs-lookup"><span data-stu-id="29c85-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="29c85-256">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="29c85-256">Click Designer.</span></span>
    
    <span data-ttu-id="29c85-257">Athugið að breytingar á mörkum á textalengd á heiti lánardrottins var ekki hægt að leysa sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="29c85-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="29c85-258">Þess birtist það í lista yfir árekstra.</span><span class="sxs-lookup"><span data-stu-id="29c85-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="29c85-259">Fyrir hverja árekstur af gerðinni Uppfærsla eru eftirtaldir valkostir tiltækir:- Nota í fyrra grunngildi (hnappinn yfir hnitanetinu) til að færa í gildi fyrri grunnútgáfa (0 í okkar tilfelli).</span><span class="sxs-lookup"><span data-stu-id="29c85-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="29c85-260">- Nota grunngildi (hnappinn yfir hnitanetinu) til að færa í nýtt gildi grunnútgáfu (100 í okkar tilfelli).</span><span class="sxs-lookup"><span data-stu-id="29c85-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="29c85-261">- Halda þínu eigin gildi (sérstillt) (60 í okkar tilfelli).</span><span class="sxs-lookup"><span data-stu-id="29c85-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="29c85-262">Smellið á Nota grunngildi til að nota landsbundin mörk uppá 100 stafi fyrir textalengd á heiti lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="29c85-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="29c85-263">Athugaðu að Proseware, Inc. og Litware, Inc. hafa sérsniðnar og staðbundnar útgáfur af þessu sniði og nota IBAN og swift-kóða með tengdar íhluti sem sjálfkrafa eru sameinaðir í stjórnunarsniðið.</span><span class="sxs-lookup"><span data-stu-id="29c85-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="29c85-264">Smellt er á Nota grunngildi</span><span class="sxs-lookup"><span data-stu-id="29c85-264">Click Apply base value.</span></span>

    <span data-ttu-id="29c85-265">Smellið á Nota grunngildi til að nota landsbundin mörk uppá 100 stafi fyrir heiti lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="29c85-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="29c85-266">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="29c85-266">Click Save.</span></span>

    <span data-ttu-id="29c85-267">Að Vista snið fjarlægir árekstra sem leyst hefur verið úr af listanum yfir árekstra.</span><span class="sxs-lookup"><span data-stu-id="29c85-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="29c85-268">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29c85-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="29c85-269">Breyta stöðu á nýju útgáfu af sérsniðnu skilgreiningarsniði</span><span class="sxs-lookup"><span data-stu-id="29c85-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="29c85-270">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="29c85-270">Click Change status.</span></span>

    <span data-ttu-id="29c85-271">Breyta stöðu uppfærða, sérsniðna skilgreiningarsniðs úr Drög í Lokið.</span><span class="sxs-lookup"><span data-stu-id="29c85-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="29c85-272">Þetta gerir skilgreiningu sniðs tiltækt fyrir myndun greiðsluskjala.</span><span class="sxs-lookup"><span data-stu-id="29c85-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="29c85-273">Athugið að núverandi útgáfa valinnar skilgreiningar er í stöðunni DRÖG.</span><span class="sxs-lookup"><span data-stu-id="29c85-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="29c85-274">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="29c85-274">Click Complete.</span></span>
3. <span data-ttu-id="29c85-275">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="29c85-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="29c85-276">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="29c85-276">Click OK.</span></span>

    <span data-ttu-id="29c85-277">Athugið að hin stofnaða skilgreining er vistuð sem lokin útgáfa 1.2.2. Útgáfa 2 af grunnsniði BACS (UK sérsniðið upphugsað) snið, sem er byggð á sniði útgáfu 2 BACS (Bretland upphugsað), sem er byggð á 1 útgáfu gagnalíkans Greiðslna (einfaldaður líkan).</span><span class="sxs-lookup"><span data-stu-id="29c85-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="29c85-278">Prófa Sérsniðnar snið til að mynda greiðsluskrár</span><span class="sxs-lookup"><span data-stu-id="29c85-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="29c85-279">Ljúkið skrefunum í ferlinu „Nota stofnuð snið til að mynda rafræn skjöl fyrir greiðslur” í samhliða lotu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="29c85-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="29c85-280">Velja hið stofnaða „BACS snið (Bretland sérsniðið upphugsað)” í færibreytum rafrænnar greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="29c85-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="29c85-281">Gangið úr skugga um að stofnaða greiðsluskráin innihaldi, nýlega kynnta af Proseware Inc., XML-hnúta sem setur fram IBAN-kóða í samræmi við svæðisbundið þarfir.</span><span class="sxs-lookup"><span data-stu-id="29c85-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="29c85-282">Skráin ætti einnig að innihalda, nýlega kynnta af Litware, Inc., XML-hnúta sem setur fram SWIFT-kóða í samræmi við svæðisbundið þarfir.</span><span class="sxs-lookup"><span data-stu-id="29c85-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

