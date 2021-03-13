---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3 - stofna snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar í úttaki rafrænnar skýrslugerðar. (Hluti 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092617"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="64821-104">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3 - stofna snið)</span><span class="sxs-lookup"><span data-stu-id="64821-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64821-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="64821-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="64821-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="64821-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="64821-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 2: framlengja gagnalíkans”.</span><span class="sxs-lookup"><span data-stu-id="64821-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="64821-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="64821-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="64821-109">Stofna snið til að vinna reikninga</span><span class="sxs-lookup"><span data-stu-id="64821-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="64821-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="64821-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="64821-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="64821-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="64821-112">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="64821-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="64821-113">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="64821-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="64821-114">Þú munt stofna snið til að stofna rafræn skilaboð með upplýsingar um allar skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.</span><span class="sxs-lookup"><span data-stu-id="64821-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="64821-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="64821-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="64821-116">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani líkan reikningur viðskiptavinar (sérstillt)“.</span><span class="sxs-lookup"><span data-stu-id="64821-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="64821-117">Í svæðið Heiti skal færa inn 'dæmi um skilaboð Rafrænn reikningur'.</span><span class="sxs-lookup"><span data-stu-id="64821-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="64821-118">Dæmi um skilaboð Rafræns reiknings</span><span class="sxs-lookup"><span data-stu-id="64821-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="64821-119">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="64821-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="64821-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="64821-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="64821-121">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="64821-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="64821-122">Breyta sniði til að fylla út viðhengi í myndun skilaboða í MIME-sniði</span><span class="sxs-lookup"><span data-stu-id="64821-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="64821-123">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="64821-123">Click Designer.</span></span>
2. <span data-ttu-id="64821-124">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64821-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="64821-125">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="64821-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="64821-126">Í reitnum Heiti skal færa inn ‚reikningur'.</span><span class="sxs-lookup"><span data-stu-id="64821-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="64821-127">Reikningur</span><span class="sxs-lookup"><span data-stu-id="64821-127">Invoice</span></span>  
5. <span data-ttu-id="64821-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-128">Click OK.</span></span>
6. <span data-ttu-id="64821-129">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64821-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="64821-130">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="64821-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="64821-131">Í svæðið Heiti, færðu inn 'SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="64821-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="64821-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="64821-132">SalesOrder</span></span>  
9. <span data-ttu-id="64821-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-133">Click OK.</span></span>
10. <span data-ttu-id="64821-134">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="64821-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="64821-135">Í svæðið Heiti, færðu inn 'InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="64821-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="64821-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="64821-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="64821-137">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-137">Click OK.</span></span>
13. <span data-ttu-id="64821-138">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="64821-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="64821-139">Í svæðið Heiti, færðu inn 'InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="64821-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="64821-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="64821-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="64821-141">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-141">Click OK.</span></span>
16. <span data-ttu-id="64821-142">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64821-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="64821-143">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="64821-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="64821-144">Í svæðið Heiti, færðu inn 'EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="64821-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="64821-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="64821-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="64821-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-146">Click OK.</span></span>
20. <span data-ttu-id="64821-147">Í trénu skal velja 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="64821-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="64821-148">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="64821-148">Click Add Element.</span></span>
22. <span data-ttu-id="64821-149">Í svæðið Heiti, færðu inn 'skjal'.</span><span class="sxs-lookup"><span data-stu-id="64821-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="64821-150">Skjal</span><span class="sxs-lookup"><span data-stu-id="64821-150">Document</span></span>  
23. <span data-ttu-id="64821-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-151">Click OK.</span></span>
24. <span data-ttu-id="64821-152">Í trénu skal velja 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="64821-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="64821-153">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64821-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="64821-154">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="64821-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="64821-155">Í svæðið Heiti, færðu inn 'FileName'.</span><span class="sxs-lookup"><span data-stu-id="64821-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="64821-156">Skráarheiti</span><span class="sxs-lookup"><span data-stu-id="64821-156">FileName</span></span>  
28. <span data-ttu-id="64821-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-157">Click OK.</span></span>
29. <span data-ttu-id="64821-158">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64821-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="64821-159">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="64821-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="64821-160">Í svæðið Heiti, færðu inn 'FileContent'.</span><span class="sxs-lookup"><span data-stu-id="64821-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="64821-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="64821-161">FileContent</span></span>  
32. <span data-ttu-id="64821-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-162">Click OK.</span></span>
33. <span data-ttu-id="64821-163">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent'.</span><span class="sxs-lookup"><span data-stu-id="64821-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="64821-164">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="64821-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="64821-165">Í trénu skal velja 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="64821-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="64821-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64821-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="64821-167">Varpa sniðsíhlutum í gagnalíkan sem gagnaveitu</span><span class="sxs-lookup"><span data-stu-id="64821-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="64821-168">Í trénu skal velja 'Invoice\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="64821-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="64821-169">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="64821-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="64821-170">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="64821-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="64821-171">Í trénu skal velja 'model\Sales order number(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="64821-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="64821-172">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64821-172">Click Bind.</span></span>
6. <span data-ttu-id="64821-173">Í trénu skal velja 'Invoice\InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="64821-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="64821-174">Í trénu skal víkka út 'model\Base invoice(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="64821-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="64821-175">Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span><span class="sxs-lookup"><span data-stu-id="64821-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="64821-176">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64821-176">Click Bind.</span></span>
10. <span data-ttu-id="64821-177">Í trénu skal velja 'Invoice\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="64821-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="64821-178">Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="64821-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="64821-179">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64821-179">Click Bind.</span></span>
13. <span data-ttu-id="64821-180">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="64821-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="64821-181">Í trénu skal velja 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="64821-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="64821-182">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="64821-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="64821-183">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64821-183">Click Bind.</span></span>
17. <span data-ttu-id="64821-184">Í trénu skal velja 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="64821-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="64821-185">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileName'.</span><span class="sxs-lookup"><span data-stu-id="64821-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="64821-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64821-186">Click Bind.</span></span>
20. <span data-ttu-id="64821-187">Í trénu skal velja 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="64821-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="64821-188">Í trénu skal velja 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="64821-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="64821-189">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64821-189">Click Bind.</span></span>
23. <span data-ttu-id="64821-190">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="64821-190">Click Save.</span></span>
24. <span data-ttu-id="64821-191">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64821-191">Close the page.</span></span>

