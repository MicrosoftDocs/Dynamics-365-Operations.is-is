--- 
title: "Rafræn skýrslugerð Varpa efnisþætti ef stofnað snið einingar gagnalíkans (nóvember 2016)"
description: "Eftirfarandi ferli sýnir hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili Rafræn skýrslugerð getur varpað gagnalíkanaeiningar í íhluti af stofnaðri grunnstillingu Rafræn skýrslugerð, sem skilgreinir snið rafrænt skjal fyrir viðskiptalén greiðslna."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a24ef0e091379f14a163a6385be988143a1ec608
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="34fd8-103">Rafræn skýrslugerð Varpa efnisþætti ef stofnað snið einingar gagnalíkans (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="34fd8-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34fd8-104">Eftirfarandi ferli sýnir hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili Rafræn skýrslugerð getur varpað gagnalíkanaeiningar í íhluti af stofnaðri grunnstillingu Rafræn skýrslugerð, sem skilgreinir snið rafrænt skjal fyrir viðskiptalén greiðslna.</span><span class="sxs-lookup"><span data-stu-id="34fd8-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="34fd8-105">Þetta snið verður notað síðar til að stofna rafræn skjöl fyrir úrvinnsla á greiðslum.</span><span class="sxs-lookup"><span data-stu-id="34fd8-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="34fd8-106">Í þessu dæmi muntu stofna grunnstilling sniðs fyrir sýnifyrirtækið, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="34fd8-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="34fd8-107">Þessi skref er hægt að framkvæma í hvaða fyrirtæki þar sem grunnstillingar rafrænnar skýrslugerðar eru samnýttar í öllum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="34fd8-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="34fd8-108">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Stofna grunnstillingu sniðs“.</span><span class="sxs-lookup"><span data-stu-id="34fd8-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="34fd8-109">Velja grunnstillingu sniðs</span><span class="sxs-lookup"><span data-stu-id="34fd8-109">Select a format configuration</span></span>
1. <span data-ttu-id="34fd8-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="34fd8-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="34fd8-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="34fd8-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="34fd8-112">Stækkið „Greiðslur (EINFÖLDUN líkan)“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="34fd8-113">Í trénu, veljið 'Payments (einfaldað líkan)\BACS (UK upphugsað)'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="34fd8-114">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="34fd8-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="34fd8-115">Varpa íhluti sniðs í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="34fd8-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="34fd8-116">Smellt er á Víkka/draga saman.</span><span class="sxs-lookup"><span data-stu-id="34fd8-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="34fd8-117">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="34fd8-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="34fd8-118">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="34fd8-119">Í trénu skal velja 'Xml\Message\ProcessingDate\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="34fd8-120">Í trénu skal velja 'model\ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="34fd8-121">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-121">Click Bind.</span></span>
7. <span data-ttu-id="34fd8-122">Í trénu skal velja 'Xml\Message\MessageId\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="34fd8-123">Í trénu skal velja 'model\MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="34fd8-124">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-124">Click Bind.</span></span>
10. <span data-ttu-id="34fd8-125">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="34fd8-126">Í trénu skal velja 'Xml\Message\Payments\Item\Amount\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="34fd8-127">Í trénu skal velja 'model\Payments\InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="34fd8-128">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-128">Click Bind.</span></span>
14. <span data-ttu-id="34fd8-129">Í trénu skal velja 'Xml\Message\Payments\Item\TransDate\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="34fd8-130">Í trénu skal velja 'model\Payments\TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="34fd8-131">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-131">Click Bind.</span></span>
17. <span data-ttu-id="34fd8-132">Í trénu skal velja 'Xml\Message\Payments\Item\Description\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="34fd8-133">Veljið 'model\Payments\Description', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="34fd8-134">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-134">Click Bind.</span></span>
20. <span data-ttu-id="34fd8-135">Í trénu skal velja 'Xml\Message\Payments\Item\Currency\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="34fd8-136">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="34fd8-137">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-137">Click Bind.</span></span>
23. <span data-ttu-id="34fd8-138">Í trénu skal velja 'Xml\Message\Payments\Item\Id'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="34fd8-139">Í trénu skal velja 'model\Payments\End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="34fd8-140">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-140">Click Bind.</span></span>
26. <span data-ttu-id="34fd8-141">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="34fd8-142">Útvíkka 'model\Payments\Creditor\Account', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="34fd8-143">Útvíkka 'model\Payments\Creditor\Agent', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="34fd8-144">Í tré skal velja 'Xml\Message\Payments\Item\Vendor\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="34fd8-145">Veljið 'model\Payments\Creditor\Name', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="34fd8-146">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-146">Click Bind.</span></span>
32. <span data-ttu-id="34fd8-147">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="34fd8-148">Í trénu skal velja 'model\Payments\Creditor\Agent\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="34fd8-149">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-149">Click Bind.</span></span>
35. <span data-ttu-id="34fd8-150">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="34fd8-151">Veljið 'model\Payments\Creditor\Account\Number', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="34fd8-152">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-152">Click Bind.</span></span>
38. <span data-ttu-id="34fd8-153">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="34fd8-154">Útvíkka 'model\Payments\Debtor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="34fd8-155">Útvíkka 'model\Payments\Debtor\Account', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="34fd8-156">Útvíkka 'model\Payments\Debtor\Agent', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="34fd8-157">Veljið 'model\Payments\Debtor\Name', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="34fd8-158">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-158">Click Bind.</span></span>
44. <span data-ttu-id="34fd8-159">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="34fd8-160">Í trénu skal velja 'model\Payments\Debtor\Agent\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="34fd8-161">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-161">Click Bind.</span></span>
47. <span data-ttu-id="34fd8-162">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="34fd8-163">Veljið 'model\Payments\Debtor\Account\Number', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="34fd8-164">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-164">Click Bind.</span></span>
50. <span data-ttu-id="34fd8-165">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="34fd8-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="34fd8-166">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="34fd8-167">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="34fd8-167">Click Bind.</span></span>
53. <span data-ttu-id="34fd8-168">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="34fd8-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="34fd8-169">Sannprófa vörpun sniðs</span><span class="sxs-lookup"><span data-stu-id="34fd8-169">Validate format mapping</span></span>
1. <span data-ttu-id="34fd8-170">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="34fd8-170">Click Validate.</span></span>
    * <span data-ttu-id="34fd8-171">Sannprófa nýja vörpun til að tryggja að allar bindingar séu í lagi.</span><span class="sxs-lookup"><span data-stu-id="34fd8-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="34fd8-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="34fd8-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="34fd8-173">Breyta stöðu á gildandi útgáfu af skilgreiningarsniði</span><span class="sxs-lookup"><span data-stu-id="34fd8-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="34fd8-174">Í næsta skref verður breytt stöðu grunnstillingarsniðs úr Drög í Lokið til að gera það tiltækan fyrir myndun greiðsluskjala.</span><span class="sxs-lookup"><span data-stu-id="34fd8-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="34fd8-175">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="34fd8-175">Click Change status.</span></span>
2. <span data-ttu-id="34fd8-176">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="34fd8-176">Click Complete.</span></span>
3. <span data-ttu-id="34fd8-177">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="34fd8-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="34fd8-178">Til dæmis „Útgáfa 1“.</span><span class="sxs-lookup"><span data-stu-id="34fd8-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="34fd8-179">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="34fd8-179">Click OK.</span></span>
5. <span data-ttu-id="34fd8-180">Velja skal lokna útgáfa af núgildandi grunnstilling.</span><span class="sxs-lookup"><span data-stu-id="34fd8-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="34fd8-181">Athugið að sniðið er vistað sem lokin útgáfa 1.1. útgáfa 1 af sniðinu, sem er byggð á útgáfu 1 af gagnalíkaninu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="34fd8-182">Tilgreina gildisdagsetning fyrir lokið útgáfa sniðs</span><span class="sxs-lookup"><span data-stu-id="34fd8-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="34fd8-183">Hægt er að skilgreina hverja sniðsútgáfa sem tiltæk fyrir notkun frá tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="34fd8-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="34fd8-184">Þegar fleiri en ein útgáfa sniðs er virk á tilteknum degi, verður síðasta snið (á grundvelli útgáfunúmers) valið fyrir notkun.</span><span class="sxs-lookup"><span data-stu-id="34fd8-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="34fd8-185">Dagsetningargildi lotu er notað til að velja rétta útgáfu.</span><span class="sxs-lookup"><span data-stu-id="34fd8-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="34fd8-186">Takmarka aðgang að stofnuðu sniði frá fyrirtækjum</span><span class="sxs-lookup"><span data-stu-id="34fd8-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="34fd8-187">Víkka út hlutann ISO lands-/svæðiskóða.</span><span class="sxs-lookup"><span data-stu-id="34fd8-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="34fd8-188">Hvert aðgangur sniðs má takmarka með því að  auðkenna tiltekna lönd/svæði þar sem snið á við.</span><span class="sxs-lookup"><span data-stu-id="34fd8-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="34fd8-189">Þegar listi yfir lönd/svæði fyrir tiltekið snið er tómt er hægt að nota þetta snið fyrir öll fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="34fd8-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="34fd8-190">Þegar sumar ISO lands/svæðiskóða eru færðar inn á lista yfir lönd/svæði, er hægt að nota sniðið eingöngu í fyrirtæki sem hafa aðalaðsetur með landskóðinn af þeim lista.</span><span class="sxs-lookup"><span data-stu-id="34fd8-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  


