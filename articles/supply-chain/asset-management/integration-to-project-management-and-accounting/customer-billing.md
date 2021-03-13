---
title: Reikningur vegna viðhalds á eignum viðskiptavinar
description: Þetta efnisatriði útskýrir hvernig á að stofna, vinna úr og rukka fyrir viðhaldsvinnu sem gerð er á eignum sem viðskiptavinir eiga.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131842"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="82030-103">Reikningur vegna viðhalds á eignum viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="82030-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82030-104">Eiginleikinn *Innheimta verkbeiðni* gerir kleift að stofna, vinna úr og rukka fyrir viðhaldsvinnu sem gerð er á eignum sem viðskiptavinir eiga.</span><span class="sxs-lookup"><span data-stu-id="82030-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="82030-105">Þessi eiginleiki gerir notendum kleift að framkvæma eftirfarandi verkefni:</span><span class="sxs-lookup"><span data-stu-id="82030-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="82030-106">Tengja viðskiptavini við eignirnar sem þeir eiga.</span><span class="sxs-lookup"><span data-stu-id="82030-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="82030-107">Velja viðskiptavin og skoða eignirnar sem viðskiptavinur á þegar verkbeiðni er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="82030-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="82030-108">Setja upp yfirverk fyrir hvern viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="82030-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="82030-109">Skrá vinnustundir, vörur, kostnað og gjöld á móti verkbeiðni og stofna síðan reikningstillögu fyrir viðskiptavininn síðar.</span><span class="sxs-lookup"><span data-stu-id="82030-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="82030-110">Að auki býður eiginleikinn upp á eftirfarandi virkni:</span><span class="sxs-lookup"><span data-stu-id="82030-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="82030-111">Verksamningurinn úr yfirverki viðskiptavinar er sjálfkrafa afritaður í viðeigandi verkbeiðni verks.</span><span class="sxs-lookup"><span data-stu-id="82030-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="82030-112">Eignastýring getur nú notað verkfærslugerðina *þóknun* á bæði spár verkbeiðnir og færslubækur verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="82030-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="82030-113">Kveikja á reikningseiginleika viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="82030-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="82030-114">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="82030-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="82030-115">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="82030-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="82030-116">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="82030-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="82030-117">**Eining:** *Verkefnastjórnun og bókhald*</span><span class="sxs-lookup"><span data-stu-id="82030-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="82030-118">**Heiti eiginleika:** *Innheimta verkbeiðni*</span><span class="sxs-lookup"><span data-stu-id="82030-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="82030-119">Dæmi</span><span class="sxs-lookup"><span data-stu-id="82030-119">Example scenario</span></span>

<span data-ttu-id="82030-120">Til að fá upplýsingar um hvernig þessi eiginleiki virkar skal fylgja eftirfarandi aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="82030-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="82030-121">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp.</span><span class="sxs-lookup"><span data-stu-id="82030-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="82030-122">Nauðsynlegt er að velja **USMF**-lögaðila áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="82030-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="82030-123">Einnig er hægt að nota þessar aðstæður sem leiðsögn um notkun á eiginleikanum þegar unnið er í framleiðslukerfi.</span><span class="sxs-lookup"><span data-stu-id="82030-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="82030-124">Í slíku tilfelli þarf hinsvegar að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.</span><span class="sxs-lookup"><span data-stu-id="82030-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="82030-125">Skref 1: Stofna nýjan verksamning fyrir viðskiptavininn</span><span class="sxs-lookup"><span data-stu-id="82030-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="82030-126">Opnaðu **Verkefnastjórnun og bókhald \> Verk \> Verksamningar**.</span><span class="sxs-lookup"><span data-stu-id="82030-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="82030-127">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="82030-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="82030-128">Sláið inn eftirfarandi gildi í svarglugganum **Nýr verksamningur**:</span><span class="sxs-lookup"><span data-stu-id="82030-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="82030-129">**Heiti:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="82030-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="82030-130">**Gerð fjármögnunar:** *Viðskiptavinur*</span><span class="sxs-lookup"><span data-stu-id="82030-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="82030-131">**Uppruni fjármögnunar:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="82030-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="82030-132">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="82030-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="82030-133">Skref 2: Búa til nýtt yfirverk fyrir viðskiptavininn</span><span class="sxs-lookup"><span data-stu-id="82030-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="82030-134">Yfirverkið sem er stofnað hér verður notað þegar verkbeiðnir fyrir viðskiptavininn eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="82030-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="82030-135">Opnaðu **Verkefnastjórnun og bókhald \> Verk \> Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="82030-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="82030-136">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="82030-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="82030-137">Sláið inn eftirfarandi gildi í svarglugganum **Nýtt verkefni**:</span><span class="sxs-lookup"><span data-stu-id="82030-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="82030-138">**Gerð verks:** *Tími og efni*</span><span class="sxs-lookup"><span data-stu-id="82030-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="82030-139">**Heiti verks:** *Pelican Wholesales work orders*</span><span class="sxs-lookup"><span data-stu-id="82030-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="82030-140">**Verkflokkur:** *TM*</span><span class="sxs-lookup"><span data-stu-id="82030-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="82030-141">**Verksamningskenni:** *Pelican-Sales* (samningurinn sem var stofnaður fyrr)</span><span class="sxs-lookup"><span data-stu-id="82030-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="82030-142">**Upphafsdagsetning:** Veldu daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="82030-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="82030-143">Velja **Stofna verk**.</span><span class="sxs-lookup"><span data-stu-id="82030-143">Select **Create project**.</span></span>
1. <span data-ttu-id="82030-144">Nýja verkið er opnað.</span><span class="sxs-lookup"><span data-stu-id="82030-144">The new project is opened.</span></span> <span data-ttu-id="82030-145">Skráið niður gildið **Verkkenni**.</span><span class="sxs-lookup"><span data-stu-id="82030-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="82030-146">Nauðsynlegt er að færa það inn síðar.</span><span class="sxs-lookup"><span data-stu-id="82030-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="82030-147">Skref 3: stofna nýja gerð verkbeiðni í Eignastýring</span><span class="sxs-lookup"><span data-stu-id="82030-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="82030-148">Farið í **Eignastýring \> Uppsetning \> Verkbeiðni \> Gerðir verkbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="82030-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="82030-149">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="82030-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="82030-150">Nýrri færslu er bætt við listann.</span><span class="sxs-lookup"><span data-stu-id="82030-150">A new record is added to the list.</span></span> <span data-ttu-id="82030-151">Stillið eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="82030-151">Set the following values for it:</span></span>

    - <span data-ttu-id="82030-152">**Gerð verkbeiðni:** *Þjónusta*</span><span class="sxs-lookup"><span data-stu-id="82030-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="82030-153">**Heiti:** *Verkbeiðnir þjónustu*</span><span class="sxs-lookup"><span data-stu-id="82030-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="82030-154">**Líftímastaða verkbeiðni:** *Venjuleg*</span><span class="sxs-lookup"><span data-stu-id="82030-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="82030-155">Skref 4: Tengja viðskiptavinalykil við yfirverk</span><span class="sxs-lookup"><span data-stu-id="82030-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="82030-156">Nú verður að tengja viðskiptavinalykilinn við yfirverkið í verkuppsetningu eignastýringar.</span><span class="sxs-lookup"><span data-stu-id="82030-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="82030-157">Farið í **Eignastýring \> Uppsetning \> Verkbeiðnir \> Uppsetning verks**.</span><span class="sxs-lookup"><span data-stu-id="82030-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="82030-158">Í flipanum **Yfirverk** skal velja **Bæta við** til að bæta við línu.</span><span class="sxs-lookup"><span data-stu-id="82030-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="82030-159">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="82030-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82030-160">**Viðskiptavinalykill:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="82030-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="82030-161">**Kenni verks:** Færið inn verkkennið sem skrifað var niður hér á undan.</span><span class="sxs-lookup"><span data-stu-id="82030-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="82030-162">Skref 5: Tengið verkflokkinn og gerðina við verk verkbeiðninnar</span><span class="sxs-lookup"><span data-stu-id="82030-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="82030-163">Þú ættir enn að vera á síðunni **Uppsetning verks** (**Eignastýring \> Uppsetning \> Verkbeiðnir \> Uppsetning verks**).</span><span class="sxs-lookup"><span data-stu-id="82030-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="82030-164">Í flipanum **Verkflokkur** skal velja **Bæta við** til að bæta við línu.</span><span class="sxs-lookup"><span data-stu-id="82030-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="82030-165">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="82030-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82030-166">**Gerð verkbeiðni:** *Þjónusta* (verkbeiðnigerðin sem stofnuð var hér á undan)</span><span class="sxs-lookup"><span data-stu-id="82030-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="82030-167">**Verkflokkur:** *TM*</span><span class="sxs-lookup"><span data-stu-id="82030-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="82030-168">Verksamningur fyrir verk verkbeiðni er alltaf fenginn frá yfirverkinu.</span><span class="sxs-lookup"><span data-stu-id="82030-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="82030-169">Skref 6: Tengja eign við kenni viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="82030-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="82030-170">Opnið **Eignastýring \> Eignir \> Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="82030-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="82030-171">Í reitinn **Sía** skal slá inn *VE-102* og velja að sía eftir **Eign**.</span><span class="sxs-lookup"><span data-stu-id="82030-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="82030-172">Veljið eignina til að opna stillingar hennar.</span><span class="sxs-lookup"><span data-stu-id="82030-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="82030-173">Í flipanum **Viðskiptavinur** skal stilla **Viðskiptavinareikningur** reitinn á *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="82030-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="82030-174">Reiturinn **Heiti** uppfærist sjálfkrafa í *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="82030-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="82030-175">Skref 7: Stofna nýja verkbeiðni fyrir eignina</span><span class="sxs-lookup"><span data-stu-id="82030-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="82030-176">Opnið **Eignastýring \> Verkbeiðnir \> Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="82030-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="82030-177">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="82030-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="82030-178">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til verkbeiðni**:</span><span class="sxs-lookup"><span data-stu-id="82030-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="82030-179">**Gerð verkbeiðni:** *Þjónusta*</span><span class="sxs-lookup"><span data-stu-id="82030-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="82030-180">**Lýsing:** *Viðgerð á vöruflutningabíl*</span><span class="sxs-lookup"><span data-stu-id="82030-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="82030-181">**Viðskiptavinalykill:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="82030-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="82030-182">**Eign:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="82030-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="82030-183">Uppfletting sýnir aðeins eignir sem eru tengdar við valinn viðskiptavinalykil.</span><span class="sxs-lookup"><span data-stu-id="82030-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="82030-184">**Gerð viðhaldsverks:** *Viðgerð*</span><span class="sxs-lookup"><span data-stu-id="82030-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="82030-185">**Starfsgrein:** *Bifvélavirki*</span><span class="sxs-lookup"><span data-stu-id="82030-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="82030-186">**Þjónustustig:** *4*</span><span class="sxs-lookup"><span data-stu-id="82030-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="82030-187">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="82030-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="82030-188">Skref 8: Yfirfara verkbeiðni og hefja vinnu á henni</span><span class="sxs-lookup"><span data-stu-id="82030-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="82030-189">Í þessum hluta verður unnið í verkbeiðninni sem stofnuð var í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="82030-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="82030-190">Fylgið eftirfarandi skrefum til að staðfesta að foreldrahlutverkið sé *Pelican wholesales verkbeiðni*:</span><span class="sxs-lookup"><span data-stu-id="82030-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="82030-191">Í hlutanum **Viðhaldsverk verkbeiðni** skal velja línu.</span><span class="sxs-lookup"><span data-stu-id="82030-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="82030-192">Í flýtiflipanum **Upplýsingar um línu** skal skoða gildið **Verkkenni**.</span><span class="sxs-lookup"><span data-stu-id="82030-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="82030-193">Það ætti að vera númer tengt með bandstriki á forminu *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="82030-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="82030-194">Gildið er tengill.</span><span class="sxs-lookup"><span data-stu-id="82030-194">This value is a link.</span></span>
    1. <span data-ttu-id="82030-195">Veljið tengil verkkennis til að opna síðu þar sem hægt er að skoða yfirverkið og verkheiti.</span><span class="sxs-lookup"><span data-stu-id="82030-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="82030-196">Á aðgerðasvæðinu, í flipanum **Verkbeiðni**, í flokknum **Líftímastaða**, skal velja **Uppfæra stöðu verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="82030-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="82030-197">Í svarglugganum **Uppfæra stöðu verkbeiðni**, í dálkinum **Velja**, skal velja gátreitinn fyrir línuna þar sem reiturinn **Líftímastaða** er stilltur á *Í vinnslu*.</span><span class="sxs-lookup"><span data-stu-id="82030-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="82030-198">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="82030-198">Select **OK**.</span></span>
1. <span data-ttu-id="82030-199">Í svarglugganum **Líftímastaða: InProgress** skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="82030-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="82030-200">Skref 9: Bóka vinnustundirnar sem fóru í verkbeiðnina og stofna nýja reikningstillögu</span><span class="sxs-lookup"><span data-stu-id="82030-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="82030-201">Í þessum hluta verður haldið áfram að vinna í verkbeiðninni sem unnin var í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="82030-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="82030-202">Á aðgerðasvæðinu, í flipanum **Verkbeiðni**, í flokknum **Verk**, skal velja **Færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="82030-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="82030-203">Síðan **Færslubækur verkbeiðni** birtist.</span><span class="sxs-lookup"><span data-stu-id="82030-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="82030-204">Hér er hægt að skrá tímann sem var eytt í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="82030-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="82030-205">Í flýtiflipanum **Vinnustundir** skal velja **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="82030-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="82030-206">Stillið reitinn **Klukkustundir** á *4* á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="82030-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="82030-207">Á aðgerðasvæðinu skal velja **Bóka færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="82030-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="82030-208">Lokið síðunni **Færslubækur verkbeiðni** til að fara aftur í verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="82030-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="82030-209">Á aðgerðasvæðinu, í flipanum **Reikningsfærsla**, skal velja **Ný reikningstillaga**.</span><span class="sxs-lookup"><span data-stu-id="82030-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="82030-210">Í svarglugganum **Stofna reikningstillögu**, í hlutanum **Verkfærslur**, skal velja gátreitinn **Velja** fyrir hverja línu sem á að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="82030-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="82030-211">Veljið **Í lagi** til að loka svarglugganum og skoða nýju reikningstillöguna.</span><span class="sxs-lookup"><span data-stu-id="82030-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
