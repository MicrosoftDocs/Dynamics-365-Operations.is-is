---
title: Hanna skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum
description: Í þessu efni er útskýrt hvernig á að hanna skilgreiningar sem mynda rafræn skjöl á Excel- og Word-sniði sem innihalda innfelldar myndir.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944558"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c0e34-103">Hanna skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum</span><span class="sxs-lookup"><span data-stu-id="c0e34-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0e34-104">Til að ljúka þessum skrefum í ferlinu skal fyrst ljúka við ferlið „Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka.“</span><span class="sxs-lookup"><span data-stu-id="c0e34-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="c0e34-105">Ferlið útskýrir hvernig á að hanna grunnstillingar fyrir rafræna skýrslugerð til að mynda ívafnar myndir í Microsoft Excel eða Word skjali sem inniheldur ívafnar myndir.</span><span class="sxs-lookup"><span data-stu-id="c0e34-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c0e34-106">Í þessu ferli mun notandi stofna nauðsynlega grunnstillingu rafrænnar skýrslugerðar fyrir sýnifyrirtæki, Litware, Inc. Hægt er að ljúka þessum skrefum með USMF-gagnamengi.</span><span class="sxs-lookup"><span data-stu-id="c0e34-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c0e34-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="c0e34-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c0e34-108">Áður en hafist er handa skal sækja og vista eftirfarandi skrár:</span><span class="sxs-lookup"><span data-stu-id="c0e34-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="c0e34-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="c0e34-109">Description</span></span>                                          | <span data-ttu-id="c0e34-110">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="c0e34-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="c0e34-111">Skilgreining á gagnalíkani í ER</span><span class="sxs-lookup"><span data-stu-id="c0e34-111">ER data model configuration</span></span>                          | [<span data-ttu-id="c0e34-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="c0e34-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="c0e34-113">ER Sníða skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="c0e34-113">ER format configuration</span></span>                              | [<span data-ttu-id="c0e34-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="c0e34-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="c0e34-115">Mynd af merki fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="c0e34-115">Company logo image</span></span>                                   | [<span data-ttu-id="c0e34-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="c0e34-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="c0e34-117">Mynd af undirskrift</span><span class="sxs-lookup"><span data-stu-id="c0e34-117">Signature image</span></span>                                      | [<span data-ttu-id="c0e34-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="c0e34-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="c0e34-119">Önnur mynd af undirskrift</span><span class="sxs-lookup"><span data-stu-id="c0e34-119">Alternative signature image</span></span>                          | [<span data-ttu-id="c0e34-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="c0e34-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="c0e34-121">Microsoft Word-sniðmát fyrir prentun greiðsluávísana</span><span class="sxs-lookup"><span data-stu-id="c0e34-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="c0e34-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="c0e34-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="c0e34-123">Staðfesta forkröfur</span><span class="sxs-lookup"><span data-stu-id="c0e34-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c0e34-124">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="c0e34-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c0e34-125">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="c0e34-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c0e34-126">Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="c0e34-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="c0e34-127">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c0e34-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c0e34-128">Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="c0e34-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c0e34-129">Í stað þess að búa til nýtt líkan er hægt að hlaða upp líkanstillingarskránn rafrænnar skýrslugerðar (Model for cheques.xml) sem var vituð áður.</span><span class="sxs-lookup"><span data-stu-id="c0e34-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c0e34-130">Þessi skrá inniheldur sýnigögn gagnalíkans fyrir greiðslu ávísana og vörpun gagnalíkans í gagnalíka Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="c0e34-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c0e34-131">Á Útgáfur flýtiflipa skal smella á Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0e34-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c0e34-132">Smellt er á Hlaða úr XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="c0e34-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c0e34-133">Smellið á Fletta og veljið Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c0e34-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c0e34-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-134">Click OK.</span></span>  
 6. <span data-ttu-id="c0e34-135">Hlaðið líka verður notað sem gagnaveita fyrir upplýsingar til að búa til skjöl sem innihalda myndir í Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="c0e34-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c0e34-136">Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="c0e34-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c0e34-137">Í stað þess að búa til nýtt snið er hægt að hlaða upp líkanastillingaskrá rafrænnar skýrslugerðar (Cheques printing format.xml) sem var vistuð áður.</span><span class="sxs-lookup"><span data-stu-id="c0e34-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c0e34-138">Þessi skrá inniheldur sýniútlit sniðsins til að prenta ávísanir með forstillingarsniði og vörpun þessa sniðs í „Model for cheques” gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="c0e34-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="c0e34-139">Smellt er á Skipta út.</span><span class="sxs-lookup"><span data-stu-id="c0e34-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="c0e34-140">Smellt er á Hlaða úr XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="c0e34-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c0e34-141">Flettið og veljið Ávísanir prentsnið format.xml skrá.</span><span class="sxs-lookup"><span data-stu-id="c0e34-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c0e34-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-142">Click OK.</span></span>  
 6. <span data-ttu-id="c0e34-143">Í trénu skal víkka út „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c0e34-144">Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c0e34-145">Hlaðið snið verður notað til að búa til skjöl sem innihalda myndir í Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="c0e34-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c0e34-146">Skilgreina færibreytur notanda rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c0e34-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c0e34-147">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="c0e34-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c0e34-148">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="c0e34-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="c0e34-149">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="c0e34-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c0e34-150">Kveikið á „Keyrsludrög” fánann til að hefja drög að útgáfu af völdu sniði í stað þess sem lokið er.</span><span class="sxs-lookup"><span data-stu-id="c0e34-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c0e34-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c0e34-152">Grunnstilla færibreytur reiðufjár- og bankastjórnunar</span><span class="sxs-lookup"><span data-stu-id="c0e34-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c0e34-153">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="c0e34-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c0e34-154">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c0e34-155">Í aðgerðasvæðinu er smellt á setja upp.</span><span class="sxs-lookup"><span data-stu-id="c0e34-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c0e34-156">Smella skal á athuga.</span><span class="sxs-lookup"><span data-stu-id="c0e34-156">Click Check.</span></span>  
 5. <span data-ttu-id="c0e34-157">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="c0e34-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c0e34-158">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-158">Click Edit.</span></span>  
 7. <span data-ttu-id="c0e34-159">Velja Já í reitnum Lógó fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c0e34-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c0e34-160">Prenta merki fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c0e34-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="c0e34-161">Smellt er á breyta.</span><span class="sxs-lookup"><span data-stu-id="c0e34-161">Click Change.</span></span>  
 10. <span data-ttu-id="c0e34-162">Smellið á Fletta og veljið skrána sem var sótt áður Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="c0e34-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c0e34-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-163">Click Save.</span></span>  
 12. <span data-ttu-id="c0e34-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0e34-164">Close the page.</span></span>  
 13. <span data-ttu-id="c0e34-165">Víkkið út hlutann Undirskrift.</span><span class="sxs-lookup"><span data-stu-id="c0e34-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c0e34-166">Velja skal Já í svæðinu Prenta fyrstu undirskrift.</span><span class="sxs-lookup"><span data-stu-id="c0e34-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c0e34-167">Smellt er á breyta.</span><span class="sxs-lookup"><span data-stu-id="c0e34-167">Click Change.</span></span>  
 16. <span data-ttu-id="c0e34-168">Smellið á Fletta og veljið skrána sem var sótt áður Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="c0e34-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c0e34-169">Útvíkka hluta Eintaka.</span><span class="sxs-lookup"><span data-stu-id="c0e34-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c0e34-170">Í reitnum Vatnsmerki skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="c0e34-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c0e34-171">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="c0e34-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c0e34-172">Veljið Veldu stillingarnar „Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c0e34-173">Nú verður snið rafrænnar skýrslugerðar notað fyrir prentun ávísana.</span><span class="sxs-lookup"><span data-stu-id="c0e34-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c0e34-174">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="c0e34-174">Click Attach.</span></span>  
 23. <span data-ttu-id="c0e34-175">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-175">Click New.</span></span>  
 24. <span data-ttu-id="c0e34-176">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="c0e34-176">Click File.</span></span>  
 25. <span data-ttu-id="c0e34-177">Smellið á Fletta og veljið skrána sem var sótt áður Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="c0e34-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c0e34-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0e34-178">Close the page.</span></span>  
 27. <span data-ttu-id="c0e34-179">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0e34-179">Close the page.</span></span>  
 28. <span data-ttu-id="c0e34-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0e34-180">Close the page.</span></span>  
 29. <span data-ttu-id="c0e34-181">Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="c0e34-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c0e34-182">Velja skal Já í Leyfa stofnun fyrirframkvittana fyrir óvirka bankareikninga: reitinn.</span><span class="sxs-lookup"><span data-stu-id="c0e34-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c0e34-183">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c0e34-183">Click Save.</span></span>  
 32. <span data-ttu-id="c0e34-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0e34-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
