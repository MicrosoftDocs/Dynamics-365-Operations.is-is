---
title: Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)
description: Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4cd3960594ab37ca867792c655cfd28dc332fa9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684764"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="14de5-103">Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="14de5-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14de5-104">Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="14de5-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="14de5-105">Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="14de5-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="14de5-106">Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".</span><span class="sxs-lookup"><span data-stu-id="14de5-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="14de5-107">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="14de5-107">Create a new format configuration</span></span>
1. <span data-ttu-id="14de5-108">Fara í **Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="14de5-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="14de5-109">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="14de5-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="14de5-110">Veljið **Greiðslur (einfaldað líkan)** í trénu.</span><span class="sxs-lookup"><span data-stu-id="14de5-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="14de5-111">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14de5-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="14de5-112">Ef þú sérð ekki **Stofna skilgreiningu** verður þú að virkja hönnunarsnið á síðunni **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="14de5-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="14de5-113">Í svæðinu **Nýtt** skal færa inn **Snið byggir á gagnalíkani PaymentModel**,</span><span class="sxs-lookup"><span data-stu-id="14de5-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="14de5-114">Í svæðinu **Heiti** skal slá inn **BACS (UK skáldað)**.</span><span class="sxs-lookup"><span data-stu-id="14de5-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="14de5-115">Í svæðinu **Lýsing** skal færa inn **BACS greiðslusnið lánardrottins (UK skáldað)**.</span><span class="sxs-lookup"><span data-stu-id="14de5-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="14de5-116">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="14de5-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="14de5-117">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="14de5-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="14de5-118">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="14de5-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="14de5-119">Hægt er að skilgreina ákveðið snið rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="14de5-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="14de5-120">Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="14de5-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="14de5-121">Í svæðinu **Skilgreining gagnalíkans** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="14de5-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="14de5-122">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-122">Click **Create configuration**.</span></span> <span data-ttu-id="14de5-123">Ný Skilgreining hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="14de5-123">A new configuration has been created.</span></span> <span data-ttu-id="14de5-124">Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="14de5-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="14de5-125">Hannið snið fyrir rafrænt skjal</span><span class="sxs-lookup"><span data-stu-id="14de5-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="14de5-126">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="14de5-126">Click **Designer**.</span></span>
2. <span data-ttu-id="14de5-127">Smellið á **Bæta við rót** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14de5-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="14de5-128">Veljið **Common\File** í trénu.</span><span class="sxs-lookup"><span data-stu-id="14de5-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="14de5-129">Í svæðið **Heiti** skal færa inn **Xml**.</span><span class="sxs-lookup"><span data-stu-id="14de5-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="14de5-130">Í svæðið **Kóðun** skal færa inn **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="14de5-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="14de5-131">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-131">Click **OK**.</span></span>
7. <span data-ttu-id="14de5-132">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="14de5-132">Click **Add**.</span></span>
8. <span data-ttu-id="14de5-133">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="14de5-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="14de5-134">Í svæðið **Heiti** skal færa inn **Skilaboð**.</span><span class="sxs-lookup"><span data-stu-id="14de5-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="14de5-135">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-135">Click **OK**.</span></span>
11. <span data-ttu-id="14de5-136">Í trénu skal velja **Xml\Message**.</span><span class="sxs-lookup"><span data-stu-id="14de5-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="14de5-137">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="14de5-138">Í svæðinu **Heiti** skal færa inn **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="14de5-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="14de5-139">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-139">Click **OK**.</span></span>
15. <span data-ttu-id="14de5-140">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="14de5-141">Í svæðið Heiti skal færa inn **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="14de5-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="14de5-142">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-142">Click **OK**.</span></span>
18. <span data-ttu-id="14de5-143">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="14de5-144">Í svæðið **Heiti** skal færa inn **Greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="14de5-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="14de5-145">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-145">Click **OK**.</span></span>
21. <span data-ttu-id="14de5-146">Í trénu skal velja **Xml\Message\Payments**.</span><span class="sxs-lookup"><span data-stu-id="14de5-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="14de5-147">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="14de5-148">Í svæðið **Heiti** skal færa inn **Vara**.</span><span class="sxs-lookup"><span data-stu-id="14de5-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="14de5-149">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-149">Click **OK**.</span></span>
25. <span data-ttu-id="14de5-150">Í trénu skal velja **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="14de5-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="14de5-151">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="14de5-151">Click **Add**.</span></span>
27. <span data-ttu-id="14de5-152">Í trénu skal velja **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="14de5-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="14de5-153">Í svæðið Heiti skal færa inn **Auðkenni**.</span><span class="sxs-lookup"><span data-stu-id="14de5-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="14de5-154">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-154">Click **OK**.</span></span>
30. <span data-ttu-id="14de5-155">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="14de5-155">Click **Add**.</span></span>
31. <span data-ttu-id="14de5-156">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="14de5-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="14de5-157">Í svæðið Heiti skal færa inn **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="14de5-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="14de5-158">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-158">Click **OK**.</span></span>
34. <span data-ttu-id="14de5-159">Í trénu skal velja **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="14de5-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="14de5-160">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="14de5-161">Í svæðið Heiti skal færa inn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="14de5-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="14de5-162">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-162">Click **OK**.</span></span>
38. <span data-ttu-id="14de5-163">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="14de5-164">Í svæðið **Heiti** skal færa inn **Banki**.</span><span class="sxs-lookup"><span data-stu-id="14de5-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="14de5-165">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-165">Click **OK**.</span></span>
41. <span data-ttu-id="14de5-166">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank**.</span><span class="sxs-lookup"><span data-stu-id="14de5-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="14de5-167">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="14de5-168">Í svæðið **Heiti** skal færa inn **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="14de5-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="14de5-169">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-169">Click **OK**.</span></span>
45. <span data-ttu-id="14de5-170">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="14de5-171">Í svæðið **Heiti** skal færa inn **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="14de5-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="14de5-172">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-172">Click **OK**.</span></span>
48. <span data-ttu-id="14de5-173">Í trénu skal velja **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="14de5-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="14de5-174">Smellið á **Afrit**.</span><span class="sxs-lookup"><span data-stu-id="14de5-174">Click **Copy**.</span></span>
50. <span data-ttu-id="14de5-175">Í trénu skal velja **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="14de5-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="14de5-176">Smellið á **Líma**.</span><span class="sxs-lookup"><span data-stu-id="14de5-176">Click **Paste**.</span></span>
52. <span data-ttu-id="14de5-177">Í svæðið **Heiti** skal færa inn **Greiðandi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="14de5-178">Í trénu skal velja **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="14de5-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="14de5-179">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="14de5-180">Í svæðið **Heiti** skal færa inn **Gjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="14de5-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="14de5-181">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-181">Click **OK**.</span></span>
57. <span data-ttu-id="14de5-182">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="14de5-183">Í svæðið **Heiti** skal færa inn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="14de5-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="14de5-184">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-184">Click **OK**.</span></span>
60. <span data-ttu-id="14de5-185">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="14de5-186">Í svæðið Heiti skal færa inn **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="14de5-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="14de5-187">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-187">Click **OK**.</span></span>
63. <span data-ttu-id="14de5-188">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="14de5-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="14de5-189">Í svæðið Heiti skal færa inn **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="14de5-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="14de5-190">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="14de5-191">Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="14de5-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="14de5-192">Í trénu skal velja **Xml\Message\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="14de5-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="14de5-193">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14de5-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="14de5-194">Í trénu skal velja **Text\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="14de5-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="14de5-195">Í svæðið **Snið** skal færa inn **áááá-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="14de5-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="14de5-196">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-196">Click **OK**.</span></span>
6. <span data-ttu-id="14de5-197">Í trénu skal velja **Xml\Message\Payments\Item\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="14de5-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="14de5-198">Smellið á **Bæta við DateTime**.</span><span class="sxs-lookup"><span data-stu-id="14de5-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="14de5-199">Í svæðið **Snið** skal færa inn **áááá-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="14de5-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="14de5-200">Í svæðisgerðinni **DateTime** skal velja **Dagsetning**.</span><span class="sxs-lookup"><span data-stu-id="14de5-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="14de5-201">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-201">Click **OK**.</span></span>
11. <span data-ttu-id="14de5-202">Í trénu skal velja **Xml\Message\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="14de5-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="14de5-203">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14de5-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="14de5-204">Í trénu skal velja **Text/String**.</span><span class="sxs-lookup"><span data-stu-id="14de5-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="14de5-205">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-205">Click **OK**.</span></span>
15. <span data-ttu-id="14de5-206">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Name**.</span><span class="sxs-lookup"><span data-stu-id="14de5-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="14de5-207">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-207">Click **Add String**.</span></span>
17. <span data-ttu-id="14de5-208">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-208">Click **OK**.</span></span>
18. <span data-ttu-id="14de5-209">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="14de5-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="14de5-210">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-210">Click **Add String**.</span></span>
20. <span data-ttu-id="14de5-211">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-211">Click **OK**.</span></span>
21. <span data-ttu-id="14de5-212">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="14de5-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="14de5-213">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-213">Click **Add String**.</span></span>
23. <span data-ttu-id="14de5-214">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-214">Click **OK**.</span></span>
24. <span data-ttu-id="14de5-215">Í trénu skal velja **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="14de5-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="14de5-216">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-216">Click **Add String**.</span></span>
26. <span data-ttu-id="14de5-217">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-217">Click **OK**.</span></span>
27. <span data-ttu-id="14de5-218">Í trénu skal velja **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="14de5-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="14de5-219">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-219">Click **Add String**.</span></span>
29. <span data-ttu-id="14de5-220">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-220">Click **OK**.</span></span>
30. <span data-ttu-id="14de5-221">Í trénu skal velja **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="14de5-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="14de5-222">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-222">Click **Add String**.</span></span>
32. <span data-ttu-id="14de5-223">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-223">Click **OK**.</span></span>
33. <span data-ttu-id="14de5-224">Í trénu skal velja **Xml\Message\Payments\Item\Currency**.</span><span class="sxs-lookup"><span data-stu-id="14de5-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="14de5-225">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-225">Click **Add String**.</span></span>
35. <span data-ttu-id="14de5-226">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-226">Click **OK**.</span></span>
36. <span data-ttu-id="14de5-227">Í trénu skal velja **Xml\Message\Payments\Item\Description**.</span><span class="sxs-lookup"><span data-stu-id="14de5-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="14de5-228">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-228">Click **Add String**.</span></span>
38. <span data-ttu-id="14de5-229">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-229">Click **OK**.</span></span>
39. <span data-ttu-id="14de5-230">Í trénu skal velja **Xml\Message\Payments\Item\Amount**.</span><span class="sxs-lookup"><span data-stu-id="14de5-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="14de5-231">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="14de5-231">Click **Add String**.</span></span>
41. <span data-ttu-id="14de5-232">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="14de5-232">Click **OK**.</span></span>
42. <span data-ttu-id="14de5-233">Smellið á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="14de5-233">Click **Save**.</span></span>
43. <span data-ttu-id="14de5-234">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14de5-234">Close the page.</span></span>

