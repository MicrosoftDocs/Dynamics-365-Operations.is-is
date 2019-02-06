--- 
title: "Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: is-is
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="4dca9-103">Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="4dca9-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dca9-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="4dca9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="4dca9-105">Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="4dca9-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="4dca9-106">Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".</span><span class="sxs-lookup"><span data-stu-id="4dca9-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="4dca9-107">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="4dca9-107">Create a new format configuration</span></span>
1. <span data-ttu-id="4dca9-108">Fara í **Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="4dca9-109">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="4dca9-110">Veljið **Greiðslur (einfaldað líkan)** í trénu.</span><span class="sxs-lookup"><span data-stu-id="4dca9-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="4dca9-111">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4dca9-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="4dca9-112">Ef þú sérð ekki **Stofna skilgreiningu** verður þú að virkja hönnunarsnið á síðunni **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="4dca9-113">Í svæðinu **Nýtt** skal færa inn **Snið byggir á gagnalíkani PaymentModel**,</span><span class="sxs-lookup"><span data-stu-id="4dca9-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="4dca9-114">Í svæðinu **Heiti** skal slá inn **BACS (UK skáldað)**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="4dca9-115">Í svæðinu **Lýsing** skal færa inn **BACS greiðslusnið lánardrottins (UK skáldað)**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="4dca9-116">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="4dca9-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="4dca9-117">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="4dca9-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="4dca9-118">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="4dca9-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="4dca9-119">Hægt er að skilgreina ákveðið snið rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="4dca9-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="4dca9-120">Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="4dca9-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="4dca9-121">Í svæðinu **Skilgreining gagnalíkans** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="4dca9-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="4dca9-122">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-122">Click **Create configuration**.</span></span> <span data-ttu-id="4dca9-123">Ný Skilgreining hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4dca9-123">A new configuration has been created.</span></span> <span data-ttu-id="4dca9-124">Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="4dca9-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="4dca9-125">Ef þú sérð ekki **Stofna skilgreiningu** verður þú að virkja hönnunarsnið á síðunni **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="4dca9-126">Hannið snið fyrir rafrænt skjal</span><span class="sxs-lookup"><span data-stu-id="4dca9-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="4dca9-127">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-127">Click **Designer**.</span></span>
2. <span data-ttu-id="4dca9-128">Smellið á **Bæta við rót** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4dca9-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="4dca9-129">Veljið **Common\File** í trénu.</span><span class="sxs-lookup"><span data-stu-id="4dca9-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="4dca9-130">Í svæðið **Heiti** skal færa inn **Xml**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="4dca9-131">Í svæðið **Kóðun** skal færa inn **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="4dca9-132">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-132">Click **OK**.</span></span>
7. <span data-ttu-id="4dca9-133">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-133">Click **Add**.</span></span>
8. <span data-ttu-id="4dca9-134">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="4dca9-135">Í svæðið **Heiti** skal færa inn **Skilaboð**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="4dca9-136">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-136">Click **OK**.</span></span>
11. <span data-ttu-id="4dca9-137">Í trénu skal velja **Xml\Message**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="4dca9-138">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="4dca9-139">Í svæðinu **Heiti** skal færa inn **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="4dca9-140">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-140">Click **OK**.</span></span>
15. <span data-ttu-id="4dca9-141">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="4dca9-142">Í svæðið Heiti skal færa inn **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="4dca9-143">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-143">Click **OK**.</span></span>
18. <span data-ttu-id="4dca9-144">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="4dca9-145">Í svæðið **Heiti** skal færa inn **Greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="4dca9-146">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-146">Click **OK**.</span></span>
21. <span data-ttu-id="4dca9-147">Í trénu skal velja **Xml\Message\Payments**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="4dca9-148">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="4dca9-149">Í svæðið **Heiti** skal færa inn **Vara**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="4dca9-150">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-150">Click **OK**.</span></span>
25. <span data-ttu-id="4dca9-151">Í trénu skal velja **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="4dca9-152">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-152">Click **Add**.</span></span>
27. <span data-ttu-id="4dca9-153">Í trénu skal velja **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="4dca9-154">Í svæðið Heiti skal færa inn **Auðkenni**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="4dca9-155">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-155">Click **OK**.</span></span>
30. <span data-ttu-id="4dca9-156">Smellið á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-156">Click **Add**.</span></span>
31. <span data-ttu-id="4dca9-157">Í trénu skal velja **XML/Element**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="4dca9-158">Í svæðið Heiti skal færa inn **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="4dca9-159">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-159">Click **OK**.</span></span>
34. <span data-ttu-id="4dca9-160">Í trénu skal velja **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="4dca9-161">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="4dca9-162">Í svæðið Heiti skal færa inn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="4dca9-163">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-163">Click **OK**.</span></span>
38. <span data-ttu-id="4dca9-164">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="4dca9-165">Í svæðið **Heiti** skal færa inn **Banki**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="4dca9-166">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-166">Click **OK**.</span></span>
41. <span data-ttu-id="4dca9-167">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="4dca9-168">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="4dca9-169">Í svæðið **Heiti** skal færa inn **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="4dca9-170">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-170">Click **OK**.</span></span>
45. <span data-ttu-id="4dca9-171">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="4dca9-172">Í svæðið **Heiti** skal færa inn **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="4dca9-173">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-173">Click **OK**.</span></span>
48. <span data-ttu-id="4dca9-174">Í trénu skal velja **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="4dca9-175">Smellið á **Afrit**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-175">Click **Copy**.</span></span>
50. <span data-ttu-id="4dca9-176">Í trénu skal velja **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="4dca9-177">Smellið á **Líma**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-177">Click **Paste**.</span></span>
52. <span data-ttu-id="4dca9-178">Í svæðið **Heiti** skal færa inn **Greiðandi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="4dca9-179">Í trénu skal velja **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="4dca9-180">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="4dca9-181">Í svæðið **Heiti** skal færa inn **Gjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="4dca9-182">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-182">Click **OK**.</span></span>
57. <span data-ttu-id="4dca9-183">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="4dca9-184">Í svæðið **Heiti** skal færa inn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="4dca9-185">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-185">Click **OK**.</span></span>
60. <span data-ttu-id="4dca9-186">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="4dca9-187">Í svæðið Heiti skal færa inn **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="4dca9-188">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-188">Click **OK**.</span></span>
63. <span data-ttu-id="4dca9-189">Smellið á **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="4dca9-190">Í svæðið Heiti skal færa inn **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="4dca9-191">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="4dca9-192">Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="4dca9-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="4dca9-193">Í trénu skal velja **Xml\Message\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="4dca9-194">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4dca9-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="4dca9-195">Í trénu skal velja **Text\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="4dca9-196">Í svæðið **Snið** skal færa inn **áááá-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="4dca9-197">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-197">Click **OK**.</span></span>
6. <span data-ttu-id="4dca9-198">Í trénu skal velja **Xml\Message\Payments\Item\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="4dca9-199">Smellið á **Bæta við DateTime**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="4dca9-200">Í svæðið **Snið** skal færa inn **áááá-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="4dca9-201">Í svæðisgerðinni **DateTime** skal velja **Dagsetning**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="4dca9-202">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-202">Click **OK**.</span></span>
11. <span data-ttu-id="4dca9-203">Í trénu skal velja **Xml\Message\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="4dca9-204">Smellið á **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4dca9-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="4dca9-205">Í trénu skal velja **Text/String**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="4dca9-206">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-206">Click **OK**.</span></span>
15. <span data-ttu-id="4dca9-207">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Name**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="4dca9-208">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-208">Click **Add String**.</span></span>
17. <span data-ttu-id="4dca9-209">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-209">Click **OK**.</span></span>
18. <span data-ttu-id="4dca9-210">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="4dca9-211">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-211">Click **Add String**.</span></span>
20. <span data-ttu-id="4dca9-212">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-212">Click **OK**.</span></span>
21. <span data-ttu-id="4dca9-213">Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="4dca9-214">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-214">Click **Add String**.</span></span>
23. <span data-ttu-id="4dca9-215">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-215">Click **OK**.</span></span>
24. <span data-ttu-id="4dca9-216">Í trénu skal velja **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="4dca9-217">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-217">Click **Add String**.</span></span>
26. <span data-ttu-id="4dca9-218">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-218">Click **OK**.</span></span>
27. <span data-ttu-id="4dca9-219">Í trénu skal velja **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="4dca9-220">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-220">Click **Add String**.</span></span>
29. <span data-ttu-id="4dca9-221">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-221">Click **OK**.</span></span>
30. <span data-ttu-id="4dca9-222">Í trénu skal velja **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="4dca9-223">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-223">Click **Add String**.</span></span>
32. <span data-ttu-id="4dca9-224">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-224">Click **OK**.</span></span>
33. <span data-ttu-id="4dca9-225">Í trénu skal velja **Xml\Message\Payments\Item\Currency**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="4dca9-226">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-226">Click **Add String**.</span></span>
35. <span data-ttu-id="4dca9-227">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-227">Click **OK**.</span></span>
36. <span data-ttu-id="4dca9-228">Í trénu skal velja **Xml\Message\Payments\Item\Description**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="4dca9-229">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-229">Click **Add String**.</span></span>
38. <span data-ttu-id="4dca9-230">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-230">Click **OK**.</span></span>
39. <span data-ttu-id="4dca9-231">Í trénu skal velja **Xml\Message\Payments\Item\Amount**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="4dca9-232">Smellið á **Bæta við streng**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-232">Click **Add String**.</span></span>
41. <span data-ttu-id="4dca9-233">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-233">Click **OK**.</span></span>
42. <span data-ttu-id="4dca9-234">Smellið á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="4dca9-234">Click **Save**.</span></span>
43. <span data-ttu-id="4dca9-235">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4dca9-235">Close the page.</span></span>


