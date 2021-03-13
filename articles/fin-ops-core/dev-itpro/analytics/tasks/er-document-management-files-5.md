---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 5 - breyta og keyra snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar (viðhengi) í úttaki rafrænnar skýrslugerðar. (Hluti 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092489"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="c5f78-104">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 5 - breyta og keyra snið)</span><span class="sxs-lookup"><span data-stu-id="c5f78-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5f78-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="c5f78-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c5f78-106">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="c5f78-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c5f78-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4: keyra snið)”.</span><span class="sxs-lookup"><span data-stu-id="c5f78-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="c5f78-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="c5f78-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="c5f78-109">Breyta sniði til að fylla út viðhengi í myndun skilaboða í tvíundar sniði</span><span class="sxs-lookup"><span data-stu-id="c5f78-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="c5f78-110">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="c5f78-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c5f78-111">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="c5f78-112">Í trénu skal víkka út 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="c5f78-113">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="c5f78-114">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="c5f78-114">Click Designer.</span></span>
    * <span data-ttu-id="c5f78-115">Þú munt fylla út skilaboð reiknings í myndandi úttaki sem XML-skrá með því að nota Unicode-dulritun.</span><span class="sxs-lookup"><span data-stu-id="c5f78-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="c5f78-116">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c5f78-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="c5f78-117">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="c5f78-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="c5f78-118">Í reitnum Heiti skal færa inn ‚Xml-skilaboð‘.</span><span class="sxs-lookup"><span data-stu-id="c5f78-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="c5f78-119">Xml skilaboð</span><span class="sxs-lookup"><span data-stu-id="c5f78-119">Xml message</span></span>  
9. <span data-ttu-id="c5f78-120">Í reitinn Kóðun skal slá inn „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c5f78-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c5f78-121">UTF-8</span></span>  
10. <span data-ttu-id="c5f78-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-122">Click OK.</span></span>
    * <span data-ttu-id="c5f78-123">Skilgreina myndun úttaks sem zip-skrá.</span><span class="sxs-lookup"><span data-stu-id="c5f78-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="c5f78-124">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c5f78-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="c5f78-125">Í trénu skal velja 'Common\Folder'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="c5f78-126">Í svæðið Heiti, færðu inn 'úttak zip-skrár'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="c5f78-127">Úttak Zip-skrár</span><span class="sxs-lookup"><span data-stu-id="c5f78-127">Zip output</span></span>  
14. <span data-ttu-id="c5f78-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-128">Click OK.</span></span>
15. <span data-ttu-id="c5f78-129">Í trénu skal velja „Úttak zip-skrár“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="c5f78-130">Bæta við viðhengjum við myndandi zip-skrá sem skrár með upphaflegu nöfn og viðauka.</span><span class="sxs-lookup"><span data-stu-id="c5f78-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="c5f78-131">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c5f78-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c5f78-132">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="c5f78-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="c5f78-133">Í svæðið Heiti, færðu inn 'skrá í viðhengi'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="c5f78-134">Hengja við skrá</span><span class="sxs-lookup"><span data-stu-id="c5f78-134">Attached file</span></span>  
19. <span data-ttu-id="c5f78-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-135">Click OK.</span></span>
20. <span data-ttu-id="c5f78-136">Í trénu skal velja 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="c5f78-137">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c5f78-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="c5f78-138">Í trénu skal velja 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="c5f78-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="c5f78-140">Varpa nýjum einingum sniðs í gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="c5f78-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="c5f78-141">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="c5f78-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c5f78-142">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="c5f78-143">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="c5f78-144">Í trénu skal velja 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="c5f78-145">Í trénu skal velja 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="c5f78-146">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="c5f78-146">Click Bind.</span></span>
7. <span data-ttu-id="c5f78-147">Í trénu skal velja 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="c5f78-148">Smelltu á Breyta skrárheiti</span><span class="sxs-lookup"><span data-stu-id="c5f78-148">Click Edit filename.</span></span>
9. <span data-ttu-id="c5f78-149">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="c5f78-150">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="c5f78-151">Í trénu skal velja 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="c5f78-152">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="c5f78-152">Click Add data source.</span></span>
13. <span data-ttu-id="c5f78-153">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="c5f78-153">Click Save.</span></span>
14. <span data-ttu-id="c5f78-154">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c5f78-154">Close the page.</span></span>
15. <span data-ttu-id="c5f78-155">Í trénu skal velja 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="c5f78-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="c5f78-156">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="c5f78-156">Click Bind.</span></span>
17. <span data-ttu-id="c5f78-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-157">Click Save.</span></span>
18. <span data-ttu-id="c5f78-158">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c5f78-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="c5f78-159">Keyra viðkomandi skýrslu fyrir valinn reikning</span><span class="sxs-lookup"><span data-stu-id="c5f78-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="c5f78-160">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="c5f78-160">Click Run.</span></span>
2. <span data-ttu-id="c5f78-161">Útvíkka Færslur til að taka () hluta.</span><span class="sxs-lookup"><span data-stu-id="c5f78-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="c5f78-162">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="c5f78-162">Click Filter.</span></span>
4. <span data-ttu-id="c5f78-163">Velja línu reikningabókar viðskiptavinar og reitinn sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="c5f78-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="c5f78-164">Í forsendusvæðinu, í forsendusvæðinu „sölupöntun” skal færa inn pöntunarnúmer 000148.</span><span class="sxs-lookup"><span data-stu-id="c5f78-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="c5f78-165">000148</span><span class="sxs-lookup"><span data-stu-id="c5f78-165">000148</span></span>  
6. <span data-ttu-id="c5f78-166">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c5f78-166">Click OK.</span></span>
7. <span data-ttu-id="c5f78-167">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c5f78-167">Click OK.</span></span>
    * <span data-ttu-id="c5f78-168">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="c5f78-168">Review the generated output.</span></span> <span data-ttu-id="c5f78-169">Athugið að auk skilaboð reiknings í xml-sniði, hefur eina skrá verið stofnuð fyrir hverja viðhengi.</span><span class="sxs-lookup"><span data-stu-id="c5f78-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="c5f78-170">Viðhegndar skrárnar eru fyllt út með úttaki zip-skrár með tvíundarsniði.</span><span class="sxs-lookup"><span data-stu-id="c5f78-170">The attachment files are populated with the zipped output in binary format.</span></span>  

