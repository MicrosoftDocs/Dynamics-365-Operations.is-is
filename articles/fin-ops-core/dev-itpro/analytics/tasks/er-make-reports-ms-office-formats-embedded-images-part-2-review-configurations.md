---
title: Yfirfara skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum
description: 'Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 1: Setja upp færibreytur)“.'
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 8f81f0f86c255d048393047965c0aa29cbef09d0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143077"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="71df6-103">Yfirfara skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum</span><span class="sxs-lookup"><span data-stu-id="71df6-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71df6-104">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 1: Setja upp færibreytur)“.</span><span class="sxs-lookup"><span data-stu-id="71df6-104">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="71df6-105">Ferlið sýnir hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl sem innihalda ívafnar myndir í Microsoft Excel og Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="71df6-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="71df6-106">Í þessu dæmi muntu yfirfara grunnstillingu Rafræn skýrslugerð fyrir dæmi um fyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="71df6-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="71df6-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="71df6-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="71df6-108">Skrefin er hægt að klára með því að nota USMF gagnasafnið.</span><span class="sxs-lookup"><span data-stu-id="71df6-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="71df6-109">Yfirfara innflutt gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="71df6-109">Review the imported data model</span></span>
1. <span data-ttu-id="71df6-110">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="71df6-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="71df6-111">Í trénu skal velja „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="71df6-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="71df6-112">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="71df6-112">Click Designer.</span></span>
    * <span data-ttu-id="71df6-113">Þetta líkan er sett upp til að standa fyrir færslur lánardrottins frá viðskiptasjónarmiði og vörpun þessa líkans til gagnaveitu forritsins.</span><span class="sxs-lookup"><span data-stu-id="71df6-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="71df6-114">Yfirfara líkanið með Rafræn skýrslugerð Rekstrar hönnuður.</span><span class="sxs-lookup"><span data-stu-id="71df6-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="71df6-115">Athugið að eigindir líkaneininga sem eru birtar: skipan, nafn, lýsing, tegund gagna, osfrv.</span><span class="sxs-lookup"><span data-stu-id="71df6-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="71df6-116">Stækkið „Rót“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="71df6-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="71df6-117">Í trénu skal velja „rót\ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="71df6-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="71df6-118">Í trénu skal víkka út „rót\ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="71df6-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="71df6-119">Í trénu skal víkka út „rót\ávísanir\eigindir“.</span><span class="sxs-lookup"><span data-stu-id="71df6-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="71df6-120">Í trénu skal víkka út „rót\greiðandi“.</span><span class="sxs-lookup"><span data-stu-id="71df6-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="71df6-121">Í trénu skal velja „rót\erprufukeyrsla“.</span><span class="sxs-lookup"><span data-stu-id="71df6-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="71df6-122">Í trénu skal velja „rót\útlit“.</span><span class="sxs-lookup"><span data-stu-id="71df6-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="71df6-123">Útlitseiningar líkansins standa fyrir upplýsingar um útlitsform prentun ávísunar fyrir valinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="71df6-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="71df6-124">Það inniheldur líka tvo hnúta frá tegund gagna Hólfs til að geyma myndir.</span><span class="sxs-lookup"><span data-stu-id="71df6-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="71df6-125">Í trénu skal víkka út „rót\útlit“.</span><span class="sxs-lookup"><span data-stu-id="71df6-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="71df6-126">Í trénu skal velja „rót\útlit\fyrirtæki lógó“.</span><span class="sxs-lookup"><span data-stu-id="71df6-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="71df6-127">Í trénu skal víkka út „rót\útlit\fyrirtæki lógó“.</span><span class="sxs-lookup"><span data-stu-id="71df6-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="71df6-128">Í trénu skal velja „rót\útlit\fyrirtæki lógó\mynd“.</span><span class="sxs-lookup"><span data-stu-id="71df6-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="71df6-129">Í trénu skal velja „rót\útlit\fyrirtæki lógó\erprentað“.</span><span class="sxs-lookup"><span data-stu-id="71df6-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="71df6-130">Í trénu skal velja „rót\útlit\undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="71df6-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="71df6-131">Í trénu skal víkka út „rót\útlit\undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="71df6-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="71df6-132">Í trénu skal velja „rót\útlit\undirskrift\mynd“.</span><span class="sxs-lookup"><span data-stu-id="71df6-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="71df6-133">Í trénu skal velja „rót\útlit\undirskrift\erprentað“.</span><span class="sxs-lookup"><span data-stu-id="71df6-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="71df6-134">Athugið að tvær gagnalíkanseiningar eru bundnar reitum taflanna sem innihalda myndir af lógó fyrirtækisins og undirskrift frá viðurkenndum aðila á tvöföldu formi.</span><span class="sxs-lookup"><span data-stu-id="71df6-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="71df6-135">Í trénu skal víkka út „rót\útlit\vatnsmerki“.</span><span class="sxs-lookup"><span data-stu-id="71df6-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="71df6-136">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="71df6-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="71df6-137">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="71df6-137">Click Designer.</span></span>
23. <span data-ttu-id="71df6-138">Í trénu skal víkka út „valdarávísanir“.</span><span class="sxs-lookup"><span data-stu-id="71df6-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="71df6-139">Í trénu skal víkka út „Útlit“.</span><span class="sxs-lookup"><span data-stu-id="71df6-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="71df6-140">Í trénu skal víkka út „útlit\fyrirtækjalógó“.</span><span class="sxs-lookup"><span data-stu-id="71df6-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="71df6-141">Í trénu skal víkka út „Útlit\Undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="71df6-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="71df6-142">Í trénu skal víkka út „útlit\vatnsmerki“.</span><span class="sxs-lookup"><span data-stu-id="71df6-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="71df6-143">Kveikið á „Sýna upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="71df6-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="71df6-144">Athugið að gagnalíkanseiningar ávísananna eru bundnar TmpChequePrintout töflunni sem, við keyrslu, mun innihalda skrár fyrir ávísanir sem notandi hefur valið fyrir prentun.</span><span class="sxs-lookup"><span data-stu-id="71df6-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="71df6-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-145">Close the page.</span></span>
30. <span data-ttu-id="71df6-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-146">Close the page.</span></span>
31. <span data-ttu-id="71df6-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="71df6-148">Yfirfara innflutt snið</span><span class="sxs-lookup"><span data-stu-id="71df6-148">Review the imported format</span></span>
1. <span data-ttu-id="71df6-149">Í trénu skal víkka út „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="71df6-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="71df6-150">Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="71df6-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="71df6-151">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="71df6-151">Click Designer.</span></span>
4. <span data-ttu-id="71df6-152">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="71df6-152">Click Attachments.</span></span>
5. <span data-ttu-id="71df6-153">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="71df6-153">Click Open.</span></span>
    * <span data-ttu-id="71df6-154">Opna viðhengt sniðmát skýrslu í Excel.</span><span class="sxs-lookup"><span data-stu-id="71df6-154">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="71df6-155">Yfirfara viðhengt Ecxel-sniðmát skýrslunnar sem verður notuð til að prenta ávísanirnar.</span><span class="sxs-lookup"><span data-stu-id="71df6-155">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="71df6-156">Sniðmátið inniheldur tvær ávísanir fyrir hverja síðu og er hannað til að prenta ávísanir til forprentaðs forms.</span><span class="sxs-lookup"><span data-stu-id="71df6-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="71df6-157">Athugið að tvær auðar myndir eru ívafðar.</span><span class="sxs-lookup"><span data-stu-id="71df6-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="71df6-158">Þessar auðu myndir eru fyrir lógó fyrirtækisins og undirskrift þess aðila sem heimilar greiðslu.</span><span class="sxs-lookup"><span data-stu-id="71df6-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="71df6-159">Staðfesta að myndirnar heita CompLogo og SignatureImage í Excel.</span><span class="sxs-lookup"><span data-stu-id="71df6-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="71df6-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-160">Close the page.</span></span>
7. <span data-ttu-id="71df6-161">Stækkið „skýrsla“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="71df6-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="71df6-162">Í trénu skal víkka út „Skýrsla\ChequeLines“.</span><span class="sxs-lookup"><span data-stu-id="71df6-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="71df6-163">Í trénu skal velja 'Report\ChequeLines\CompLogo'.</span><span class="sxs-lookup"><span data-stu-id="71df6-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="71df6-164">Kveikið á „Sýna upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="71df6-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="71df6-165">Athugið að reitaeining „CompLogo“ sniðsins stendur fyrir Excel afurðina sem er notuð til að útfylla myndina af lógó fyrirtækisins í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-165">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="71df6-166">Þetta sniðseining er bundin við myndgagnalíkanseininguna sem, við keyrslu, inniheldur mynd af lógó fyrirtækisins í tvöföldu formi.</span><span class="sxs-lookup"><span data-stu-id="71df6-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="71df6-167">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="71df6-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="71df6-168">Smella á virkja Breytingar.</span><span class="sxs-lookup"><span data-stu-id="71df6-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="71df6-169">Athugið að hægt er að búa til hólfeiningar sniðsins „CompLogo“ þannig að það er ekki lengur virkt.</span><span class="sxs-lookup"><span data-stu-id="71df6-169">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="71df6-170">Þannig mun Excel myndeiningin sem þessu tengist fela lógó fyrirtækisins í skýrslunni sem búin er til.</span><span class="sxs-lookup"><span data-stu-id="71df6-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="71df6-171">Ef segðin sem er virk skilar af sér SATT og skilgreind bindingin birtir enga mynd, mun Excel myndeiningin sem þessu tengist sýna mynd sem hefur verið vistuð í Excel sniðinu.</span><span class="sxs-lookup"><span data-stu-id="71df6-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="71df6-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-172">Close the page.</span></span>
14. <span data-ttu-id="71df6-173">Stækkið „merkimiða: Hólf“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="71df6-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="71df6-174">Sumir merkimiðar sem birtast í forprentuðu ávísanaforminu verða með í skýrslunni þegar hún er stofnuð til prófunar.</span><span class="sxs-lookup"><span data-stu-id="71df6-174">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="71df6-175">Þessir merkimiðar verða samt sem áður ekki prentaðir þegar raunprentun fer fram, vegna þess að forprentaða formið inniheldur þá nú þegar.</span><span class="sxs-lookup"><span data-stu-id="71df6-175">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="71df6-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71df6-176">Close the page.</span></span>

