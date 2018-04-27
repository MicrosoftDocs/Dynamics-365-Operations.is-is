--- 
title: "Breyta og keyra snið til að nota skjalastjórnunarskrár í sniðsúttökum"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b38f69fc169367aa56468b2c8f06b65fd1291c79
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="9aacc-103">Breyta og keyra snið til að nota skjalastjórnunarskrár í sniðsúttökum</span><span class="sxs-lookup"><span data-stu-id="9aacc-103">Modify and run format to use Document Management files in format outputs</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9aacc-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="9aacc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9aacc-105">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="9aacc-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9aacc-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4: keyra snið)” ferli.</span><span class="sxs-lookup"><span data-stu-id="9aacc-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="9aacc-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="9aacc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="9aacc-108">Breyta sniði til að fylla út viðhengi í myndun skilaboða í tvíundar sniði</span><span class="sxs-lookup"><span data-stu-id="9aacc-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="9aacc-109">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="9aacc-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9aacc-110">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="9aacc-111">Í trénu skal víkka út 'Customer invoice model\Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="9aacc-112">Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="9aacc-113">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="9aacc-113">Click Designer.</span></span>
    * <span data-ttu-id="9aacc-114">Þú munt fylla út skilaboð reiknings í myndandi úttaki sem XML-skrá með því að nota Unicode-dulritun.</span><span class="sxs-lookup"><span data-stu-id="9aacc-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="9aacc-115">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9aacc-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="9aacc-116">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="9aacc-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="9aacc-117">Í reitnum Heiti skal færa inn ‚Xml-skilaboð‘.</span><span class="sxs-lookup"><span data-stu-id="9aacc-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="9aacc-118">Xml skilaboð</span><span class="sxs-lookup"><span data-stu-id="9aacc-118">Xml message</span></span>  
9. <span data-ttu-id="9aacc-119">Í reitinn Kóðun skal slá inn „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="9aacc-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="9aacc-120">UTF-8</span></span>  
10. <span data-ttu-id="9aacc-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-121">Click OK.</span></span>
    * <span data-ttu-id="9aacc-122">Skilgreina myndun úttaks sem zip-skrá.</span><span class="sxs-lookup"><span data-stu-id="9aacc-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="9aacc-123">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9aacc-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="9aacc-124">Í trénu skal velja 'Common\Folder'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="9aacc-125">Í svæðið Heiti, færðu inn 'úttak zip-skrár'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="9aacc-126">Úttak Zip-skrár</span><span class="sxs-lookup"><span data-stu-id="9aacc-126">Zip output</span></span>  
14. <span data-ttu-id="9aacc-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-127">Click OK.</span></span>
15. <span data-ttu-id="9aacc-128">Í trénu skal velja „Úttak zip-skrár“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="9aacc-129">Bæta við viðhengjum við myndandi zip-skrá sem skrár með upphaflegu nöfn og viðauka.</span><span class="sxs-lookup"><span data-stu-id="9aacc-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="9aacc-130">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9aacc-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="9aacc-131">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="9aacc-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="9aacc-132">Í svæðið Heiti, færðu inn 'skrá í viðhengi'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="9aacc-133">Hengja við skrá</span><span class="sxs-lookup"><span data-stu-id="9aacc-133">Attached file</span></span>  
19. <span data-ttu-id="9aacc-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-134">Click OK.</span></span>
20. <span data-ttu-id="9aacc-135">Í trénu skal velja 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="9aacc-136">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9aacc-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="9aacc-137">Í trénu skal velja 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="9aacc-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="9aacc-139">Varpa nýjum einingum sniðs í gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="9aacc-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="9aacc-140">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="9aacc-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="9aacc-141">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="9aacc-142">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="9aacc-143">Í trénu skal velja 'Zip output\Attached file\Base64'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="9aacc-144">Í trénu skal velja 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="9aacc-145">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9aacc-145">Click Bind.</span></span>
7. <span data-ttu-id="9aacc-146">Í trénu skal velja 'Zip output\Attached file'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="9aacc-147">Smelltu á Breyta skrárheiti</span><span class="sxs-lookup"><span data-stu-id="9aacc-147">Click Edit filename.</span></span>
9. <span data-ttu-id="9aacc-148">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="9aacc-149">Í trénu, stækka 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="9aacc-150">Í trénu skal velja 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="9aacc-151">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9aacc-151">Click Add data source.</span></span>
13. <span data-ttu-id="9aacc-152">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="9aacc-152">Click Save.</span></span>
14. <span data-ttu-id="9aacc-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9aacc-153">Close the page.</span></span>
15. <span data-ttu-id="9aacc-154">Í trénu skal velja 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="9aacc-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="9aacc-155">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9aacc-155">Click Bind.</span></span>
17. <span data-ttu-id="9aacc-156">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-156">Click Save.</span></span>
18. <span data-ttu-id="9aacc-157">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9aacc-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="9aacc-158">Keyra viðkomandi skýrslu fyrir valinn reikning</span><span class="sxs-lookup"><span data-stu-id="9aacc-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="9aacc-159">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-159">Click Run.</span></span>
2. <span data-ttu-id="9aacc-160">Útvíkka Færslur til að taka () hluta.</span><span class="sxs-lookup"><span data-stu-id="9aacc-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="9aacc-161">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="9aacc-161">Click Filter.</span></span>
4. <span data-ttu-id="9aacc-162">Velja línu reikningabókar viðskiptavinar og reitinn sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="9aacc-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="9aacc-163">Í forsendusvæðinu, í forsendusvæðinu “sölupöntun”, skal færa inn pöntunarnúmer 000148.</span><span class="sxs-lookup"><span data-stu-id="9aacc-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="9aacc-164">000148</span><span class="sxs-lookup"><span data-stu-id="9aacc-164">000148</span></span>  
6. <span data-ttu-id="9aacc-165">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-165">Click OK.</span></span>
7. <span data-ttu-id="9aacc-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9aacc-166">Click OK.</span></span>
    * <span data-ttu-id="9aacc-167">Fara yfir myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="9aacc-167">Review the generated output.</span></span> <span data-ttu-id="9aacc-168">Athugið að auk skilaboð reiknings í xml-sniði, hefur eina skrá verið stofnuð fyrir hverja viðhengi.</span><span class="sxs-lookup"><span data-stu-id="9aacc-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="9aacc-169">Viðhegndar skrárnar eru fyllt út með úttaki zip-skrár með tvíundarsniði.</span><span class="sxs-lookup"><span data-stu-id="9aacc-169">The attachment files are populated with the zipped output in binary format.</span></span>  


