---
title: Hanna skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum
description: Skrefin í þessu efni veita upplýsingar um hvernig á að hanna stillingar fyrir rafræna skýrslugerð (ER) sem búa til rafræn skjöl á Microsoft Office sniði (Excel og Word) sem innihalda innbyggðar myndir.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "358095"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c7390-103">Hanna skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum</span><span class="sxs-lookup"><span data-stu-id="c7390-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7390-104">Til að ljúka þessum skrefum í ferlinu skal fyrst ljúka við ferlið „Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka.“</span><span class="sxs-lookup"><span data-stu-id="c7390-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="c7390-105">Ferlið útskýrir hvernig á að hanna grunnstillingar fyrir rafræna skýrslugerð til að mynda ívafnar myndir í Microsoft Excel og Microsoft Word skjölum.</span><span class="sxs-lookup"><span data-stu-id="c7390-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c7390-106">Í þessu ferli mun notandi stofna nauðsynlega grunnstillingu rafrænnar skýrslugerðar fyrir sýnifyrirtæki, Litware, Inc. Hægt er að ljúka þessum skrefum með USMF-gagnamengi.</span><span class="sxs-lookup"><span data-stu-id="c7390-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c7390-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="c7390-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c7390-108">Áður en hafist er hand skal hlaða niður og vista skrárnar sem tilteknar eru í hjálparefninu [Innfelling mynda og forma í viðskiptaskjöl sem mynduð er með rafrænu skýrslugerðaverkfæri](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="c7390-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="c7390-109">Skrárnar eru: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="c7390-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="c7390-110">Staðfesta forkröfur</span><span class="sxs-lookup"><span data-stu-id="c7390-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c7390-111">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="c7390-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c7390-112">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="c7390-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c7390-113">Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka.“</span><span class="sxs-lookup"><span data-stu-id="c7390-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="c7390-114">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c7390-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c7390-115">Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="c7390-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c7390-116">Í stað þess að búa til nýtt líkan er hægt að hlaða upp líkanstillingarskránn rafrænnar skýrslugerðar (Model for cheques.xml) sem var vituð áður.</span><span class="sxs-lookup"><span data-stu-id="c7390-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c7390-117">Þessi skrá inniheldur sýnigögn gagnalíkans fyrir greiðslu ávísana og vörpun gagnalíkans í gagnalíka Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="c7390-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c7390-118">Á Útgáfur flýtiflipa skal smella á Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7390-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c7390-119">Smellt er á Hlaða úr XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="c7390-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c7390-120">Smellið á Fletta og veljið Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c7390-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c7390-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c7390-121">Click OK.</span></span>  
 6. <span data-ttu-id="c7390-122">Hlaðið líka verður notað sem gagnaveita fyrir upplýsingar til að búa til skjöl sem innihalda myndir í Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="c7390-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c7390-123">Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="c7390-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c7390-124">Í stað þess að búa til nýtt snið er hægt að hlaða upp líkanastillingaskrá rafrænnar skýrslugerðar (Cheques printing format.xml) sem var vistuð áður.</span><span class="sxs-lookup"><span data-stu-id="c7390-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c7390-125">Þessi skrá inniheldur sýniútlit sniðsins til að prenta ávísanir með forstillingarsniði og vörpun þessa sniðs í ‘Model for cheques’ gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="c7390-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="c7390-126">Smellt er á Skipta út.</span><span class="sxs-lookup"><span data-stu-id="c7390-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="c7390-127">Smellt er á Hlaða úr XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="c7390-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c7390-128">Flettið og veljið Ávísanir prentsnið format.xml skrá.</span><span class="sxs-lookup"><span data-stu-id="c7390-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c7390-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c7390-129">Click OK.</span></span>  
 6. <span data-ttu-id="c7390-130">Í trénu skal víkka út „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="c7390-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c7390-131">Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="c7390-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c7390-132">Hlaðið snið verður notað til að búa til skjöl sem innihalda myndir í Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="c7390-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c7390-133">Skilgreina færibreytur notanda rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c7390-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c7390-134">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="c7390-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c7390-135">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="c7390-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="c7390-136">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="c7390-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c7390-137">Kveikið á ‚Kerysludrög' fánann til að hefja drög að útgáfu af völdu sniði í stað þess sem lokið er.</span><span class="sxs-lookup"><span data-stu-id="c7390-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c7390-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c7390-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c7390-139">Grunnstilla færibreytur reiðufjár- og bankastjórnunar</span><span class="sxs-lookup"><span data-stu-id="c7390-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c7390-140">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="c7390-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c7390-141">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="c7390-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c7390-142">Í aðgerðasvæðinu er smellt á setja upp.</span><span class="sxs-lookup"><span data-stu-id="c7390-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c7390-143">Smella skal á athuga.</span><span class="sxs-lookup"><span data-stu-id="c7390-143">Click Check.</span></span>  
 5. <span data-ttu-id="c7390-144">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="c7390-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c7390-145">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="c7390-145">Click Edit.</span></span>  
 7. <span data-ttu-id="c7390-146">Velja Já í reitnum Lógó fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c7390-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c7390-147">Prenta merki fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c7390-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="c7390-148">Smellt er á breyta.</span><span class="sxs-lookup"><span data-stu-id="c7390-148">Click Change.</span></span>  
 10. <span data-ttu-id="c7390-149">Smellið á Fletta og veljið skrána sem var sótt áður Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="c7390-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c7390-150">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c7390-150">Click Save.</span></span>  
 12. <span data-ttu-id="c7390-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c7390-151">Close the page.</span></span>  
 13. <span data-ttu-id="c7390-152">Víkkið út hlutann Undirskrift.</span><span class="sxs-lookup"><span data-stu-id="c7390-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c7390-153">Velja skal Já í svæðinu Prenta fyrstu undirskrift.</span><span class="sxs-lookup"><span data-stu-id="c7390-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c7390-154">Smellt er á breyta.</span><span class="sxs-lookup"><span data-stu-id="c7390-154">Click Change.</span></span>  
 16. <span data-ttu-id="c7390-155">Smellið á Fletta og veljið skrána sem var sótt áður Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="c7390-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c7390-156">Útvíkka hluta Eintaka.</span><span class="sxs-lookup"><span data-stu-id="c7390-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c7390-157">Í reitnum Vatnsmerki skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="c7390-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c7390-158">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="c7390-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c7390-159">Veljið Veldu stillingarnar „Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="c7390-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c7390-160">Nú verður snið rafrænnar skýrslugerðar notað fyrir prentun ávísana.</span><span class="sxs-lookup"><span data-stu-id="c7390-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c7390-161">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="c7390-161">Click Attach.</span></span>  
 23. <span data-ttu-id="c7390-162">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c7390-162">Click New.</span></span>  
 24. <span data-ttu-id="c7390-163">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="c7390-163">Click File.</span></span>  
 25. <span data-ttu-id="c7390-164">Smellið á Fletta og veljið skrána sem var sótt áður Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="c7390-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c7390-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c7390-165">Close the page.</span></span>  
 27. <span data-ttu-id="c7390-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c7390-166">Close the page.</span></span>  
 28. <span data-ttu-id="c7390-167">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c7390-167">Close the page.</span></span>  
 29. <span data-ttu-id="c7390-168">Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="c7390-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c7390-169">Velja skal Já í Leyfa stofnun fyrirframkvittana fyrir óvirka bankareikninga: reitinn.</span><span class="sxs-lookup"><span data-stu-id="c7390-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c7390-170">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c7390-170">Click Save.</span></span>  
 32. <span data-ttu-id="c7390-171">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c7390-171">Close the page.</span></span>  
