---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3 - stofna snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar í úttaki rafrænnar skýrslugerðar. (Hluti 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755011"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="b550d-104">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3 - stofna snið)</span><span class="sxs-lookup"><span data-stu-id="b550d-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b550d-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="b550d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b550d-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="b550d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="b550d-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 2: framlengja gagnalíkans”.</span><span class="sxs-lookup"><span data-stu-id="b550d-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="b550d-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="b550d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="b550d-109">Stofna snið til að vinna reikninga</span><span class="sxs-lookup"><span data-stu-id="b550d-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="b550d-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b550d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b550d-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b550d-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b550d-112">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="b550d-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="b550d-113">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="b550d-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="b550d-114">Þú munt stofna snið til að stofna rafræn skilaboð með upplýsingar um allar skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.</span><span class="sxs-lookup"><span data-stu-id="b550d-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="b550d-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="b550d-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="b550d-116">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani líkan reikningur viðskiptavinar (sérstillt)“.</span><span class="sxs-lookup"><span data-stu-id="b550d-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="b550d-117">Í svæðið Heiti skal færa inn 'dæmi um skilaboð Rafrænn reikningur'.</span><span class="sxs-lookup"><span data-stu-id="b550d-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="b550d-118">Dæmi um skilaboð Rafræns reiknings</span><span class="sxs-lookup"><span data-stu-id="b550d-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="b550d-119">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="b550d-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="b550d-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="b550d-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="b550d-121">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b550d-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="b550d-122">Breyta sniði til að fylla út viðhengi í myndun skilaboða í MIME-sniði</span><span class="sxs-lookup"><span data-stu-id="b550d-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="b550d-123">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b550d-123">Click Designer.</span></span>
2. <span data-ttu-id="b550d-124">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b550d-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="b550d-125">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b550d-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="b550d-126">Í reitnum Heiti skal færa inn ‚reikningur'.</span><span class="sxs-lookup"><span data-stu-id="b550d-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="b550d-127">Reikningur</span><span class="sxs-lookup"><span data-stu-id="b550d-127">Invoice</span></span>  
5. <span data-ttu-id="b550d-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-128">Click OK.</span></span>
6. <span data-ttu-id="b550d-129">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b550d-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="b550d-130">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="b550d-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="b550d-131">Í svæðið Heiti, færðu inn 'SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="b550d-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="b550d-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="b550d-132">SalesOrder</span></span>  
9. <span data-ttu-id="b550d-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-133">Click OK.</span></span>
10. <span data-ttu-id="b550d-134">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b550d-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="b550d-135">Í svæðið Heiti, færðu inn 'InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="b550d-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="b550d-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="b550d-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="b550d-137">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-137">Click OK.</span></span>
13. <span data-ttu-id="b550d-138">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b550d-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="b550d-139">Í svæðið Heiti, færðu inn 'InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="b550d-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="b550d-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="b550d-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="b550d-141">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-141">Click OK.</span></span>
16. <span data-ttu-id="b550d-142">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b550d-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="b550d-143">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b550d-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="b550d-144">Í svæðið Heiti, færðu inn 'EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="b550d-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="b550d-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="b550d-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="b550d-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-146">Click OK.</span></span>
20. <span data-ttu-id="b550d-147">Í trénu skal velja 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="b550d-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="b550d-148">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="b550d-148">Click Add Element.</span></span>
22. <span data-ttu-id="b550d-149">Í svæðið Heiti, færðu inn 'skjal'.</span><span class="sxs-lookup"><span data-stu-id="b550d-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="b550d-150">Skjal</span><span class="sxs-lookup"><span data-stu-id="b550d-150">Document</span></span>  
23. <span data-ttu-id="b550d-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-151">Click OK.</span></span>
24. <span data-ttu-id="b550d-152">Í trénu skal velja 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="b550d-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="b550d-153">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b550d-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="b550d-154">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="b550d-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="b550d-155">Í svæðið Heiti, færðu inn 'FileName'.</span><span class="sxs-lookup"><span data-stu-id="b550d-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="b550d-156">Skráarheiti</span><span class="sxs-lookup"><span data-stu-id="b550d-156">FileName</span></span>  
28. <span data-ttu-id="b550d-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-157">Click OK.</span></span>
29. <span data-ttu-id="b550d-158">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b550d-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="b550d-159">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b550d-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="b550d-160">Í svæðið Heiti, færðu inn 'FileContent'.</span><span class="sxs-lookup"><span data-stu-id="b550d-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="b550d-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="b550d-161">FileContent</span></span>  
32. <span data-ttu-id="b550d-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-162">Click OK.</span></span>
33. <span data-ttu-id="b550d-163">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent'.</span><span class="sxs-lookup"><span data-stu-id="b550d-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="b550d-164">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b550d-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="b550d-165">Í trénu skal velja 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="b550d-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="b550d-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b550d-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="b550d-167">Varpa sniðsíhlutum í gagnalíkan sem gagnaveitu</span><span class="sxs-lookup"><span data-stu-id="b550d-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="b550d-168">Í trénu skal velja 'Invoice\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="b550d-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="b550d-169">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="b550d-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="b550d-170">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="b550d-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="b550d-171">Í trénu skal velja 'model\Sales order number(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="b550d-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="b550d-172">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b550d-172">Click Bind.</span></span>
6. <span data-ttu-id="b550d-173">Í trénu skal velja 'Invoice\InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="b550d-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="b550d-174">Í trénu skal víkka út 'model\Base invoice(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="b550d-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="b550d-175">Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span><span class="sxs-lookup"><span data-stu-id="b550d-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="b550d-176">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b550d-176">Click Bind.</span></span>
10. <span data-ttu-id="b550d-177">Í trénu skal velja 'Invoice\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="b550d-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="b550d-178">Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="b550d-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="b550d-179">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b550d-179">Click Bind.</span></span>
13. <span data-ttu-id="b550d-180">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="b550d-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="b550d-181">Í trénu skal velja 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="b550d-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="b550d-182">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="b550d-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="b550d-183">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b550d-183">Click Bind.</span></span>
17. <span data-ttu-id="b550d-184">Í trénu skal velja 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="b550d-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="b550d-185">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileName'.</span><span class="sxs-lookup"><span data-stu-id="b550d-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="b550d-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b550d-186">Click Bind.</span></span>
20. <span data-ttu-id="b550d-187">Í trénu skal velja 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="b550d-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="b550d-188">Í trénu skal velja 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="b550d-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="b550d-189">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b550d-189">Click Bind.</span></span>
23. <span data-ttu-id="b550d-190">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b550d-190">Click Save.</span></span>
24. <span data-ttu-id="b550d-191">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b550d-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]