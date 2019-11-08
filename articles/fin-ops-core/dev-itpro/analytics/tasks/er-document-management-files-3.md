---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3 - stofna snið)
description: Eftirfarandi skref útskýra hvernig notandi með hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stillg snið rafrænnar skýrslugerðar til að nota skjalastjórnunarskrár í rafrænum skýrslum.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 618fabc96bdfeb0c2b577aa686702d9f1257ed70
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550718"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="feafc-103">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3 - stofna snið)</span><span class="sxs-lookup"><span data-stu-id="feafc-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="feafc-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="feafc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="feafc-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="feafc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="feafc-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 2: framlengja gagnalíkans” ferli.</span><span class="sxs-lookup"><span data-stu-id="feafc-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="feafc-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="feafc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="feafc-108">Stofna snið til að vinna reikninga</span><span class="sxs-lookup"><span data-stu-id="feafc-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="feafc-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="feafc-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="feafc-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="feafc-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="feafc-111">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="feafc-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="feafc-112">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="feafc-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="feafc-113">Þú munt stofna snið til að stofna rafræn skilaboð með upplýsingar um allar skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.</span><span class="sxs-lookup"><span data-stu-id="feafc-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="feafc-114">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="feafc-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="feafc-115">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani líkan reikningur viðskiptavinar (sérstillt)“.</span><span class="sxs-lookup"><span data-stu-id="feafc-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="feafc-116">Í svæðið Heiti skal færa inn 'dæmi um skilaboð Rafrænn reikningur'.</span><span class="sxs-lookup"><span data-stu-id="feafc-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="feafc-117">Dæmi um skilaboð Rafræns reiknings</span><span class="sxs-lookup"><span data-stu-id="feafc-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="feafc-118">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="feafc-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="feafc-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="feafc-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="feafc-120">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="feafc-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="feafc-121">Breyta sniði til að fylla út viðhengi í myndun skilaboða í MIME-sniði</span><span class="sxs-lookup"><span data-stu-id="feafc-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="feafc-122">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="feafc-122">Click Designer.</span></span>
2. <span data-ttu-id="feafc-123">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="feafc-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="feafc-124">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="feafc-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="feafc-125">Í reitnum Heiti skal færa inn ‚reikningur'.</span><span class="sxs-lookup"><span data-stu-id="feafc-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="feafc-126">Reikningur</span><span class="sxs-lookup"><span data-stu-id="feafc-126">Invoice</span></span>  
5. <span data-ttu-id="feafc-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-127">Click OK.</span></span>
6. <span data-ttu-id="feafc-128">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="feafc-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="feafc-129">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="feafc-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="feafc-130">Í svæðið Heiti, færðu inn 'SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="feafc-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="feafc-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="feafc-131">SalesOrder</span></span>  
9. <span data-ttu-id="feafc-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-132">Click OK.</span></span>
10. <span data-ttu-id="feafc-133">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="feafc-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="feafc-134">Í svæðið Heiti, færðu inn 'InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="feafc-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="feafc-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="feafc-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="feafc-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-136">Click OK.</span></span>
13. <span data-ttu-id="feafc-137">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="feafc-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="feafc-138">Í svæðið Heiti, færðu inn 'InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="feafc-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="feafc-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="feafc-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="feafc-140">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-140">Click OK.</span></span>
16. <span data-ttu-id="feafc-141">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="feafc-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="feafc-142">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="feafc-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="feafc-143">Í svæðið Heiti, færðu inn 'EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="feafc-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="feafc-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="feafc-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="feafc-145">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-145">Click OK.</span></span>
20. <span data-ttu-id="feafc-146">Í trénu skal velja 'Invoice\EnclosedDocs'.</span><span class="sxs-lookup"><span data-stu-id="feafc-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="feafc-147">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="feafc-147">Click Add Element.</span></span>
22. <span data-ttu-id="feafc-148">Í svæðið Heiti, færðu inn 'skjal'.</span><span class="sxs-lookup"><span data-stu-id="feafc-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="feafc-149">Skjal</span><span class="sxs-lookup"><span data-stu-id="feafc-149">Document</span></span>  
23. <span data-ttu-id="feafc-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-150">Click OK.</span></span>
24. <span data-ttu-id="feafc-151">Í trénu skal velja 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="feafc-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="feafc-152">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="feafc-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="feafc-153">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="feafc-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="feafc-154">Í svæðið Heiti, færðu inn 'FileName'.</span><span class="sxs-lookup"><span data-stu-id="feafc-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="feafc-155">Skráarheiti</span><span class="sxs-lookup"><span data-stu-id="feafc-155">FileName</span></span>  
28. <span data-ttu-id="feafc-156">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-156">Click OK.</span></span>
29. <span data-ttu-id="feafc-157">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="feafc-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="feafc-158">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="feafc-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="feafc-159">Í svæðið Heiti, færðu inn 'FileContent'.</span><span class="sxs-lookup"><span data-stu-id="feafc-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="feafc-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="feafc-160">FileContent</span></span>  
32. <span data-ttu-id="feafc-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-161">Click OK.</span></span>
33. <span data-ttu-id="feafc-162">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent'.</span><span class="sxs-lookup"><span data-stu-id="feafc-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="feafc-163">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="feafc-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="feafc-164">Í trénu skal velja 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="feafc-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="feafc-165">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="feafc-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="feafc-166">Varpa sniðsíhlutum í gagnalíkan sem gagnaveitu</span><span class="sxs-lookup"><span data-stu-id="feafc-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="feafc-167">Í trénu skal velja 'Invoice\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="feafc-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="feafc-168">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="feafc-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="feafc-169">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="feafc-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="feafc-170">Í trénu skal velja 'model\Sales order number(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="feafc-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="feafc-171">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="feafc-171">Click Bind.</span></span>
6. <span data-ttu-id="feafc-172">Í trénu skal velja 'Invoice\InvoiceNumber'.</span><span class="sxs-lookup"><span data-stu-id="feafc-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="feafc-173">Í trénu skal víkka út 'model\Base invoice(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="feafc-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="feafc-174">Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span><span class="sxs-lookup"><span data-stu-id="feafc-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="feafc-175">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="feafc-175">Click Bind.</span></span>
10. <span data-ttu-id="feafc-176">Í trénu skal velja 'Invoice\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="feafc-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="feafc-177">Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="feafc-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="feafc-178">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="feafc-178">Click Bind.</span></span>
13. <span data-ttu-id="feafc-179">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="feafc-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="feafc-180">Í trénu skal velja 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="feafc-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="feafc-181">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="feafc-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="feafc-182">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="feafc-182">Click Bind.</span></span>
17. <span data-ttu-id="feafc-183">Í trénu skal velja 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="feafc-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="feafc-184">Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileName'.</span><span class="sxs-lookup"><span data-stu-id="feafc-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="feafc-185">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="feafc-185">Click Bind.</span></span>
20. <span data-ttu-id="feafc-186">Í trénu skal velja 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="feafc-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="feafc-187">Í trénu skal velja 'Invoice\EnclosedDocs\Document'.</span><span class="sxs-lookup"><span data-stu-id="feafc-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="feafc-188">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="feafc-188">Click Bind.</span></span>
23. <span data-ttu-id="feafc-189">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="feafc-189">Click Save.</span></span>
24. <span data-ttu-id="feafc-190">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="feafc-190">Close the page.</span></span>

