---
title: Yfirfara skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum
description: Í þessu efnisatriði er útskýrt hvernig á að hanna skilgreiningar skýrslugerðar til að mynda rafræn skjöl sem innihalda innfelldar myndir. (Hluti 1 – Setja upp færibreytur).
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de815b363daa9135b50a2f5c9c4ac19e87b6b7ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751583"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="b987c-104">Yfirfara skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum</span><span class="sxs-lookup"><span data-stu-id="b987c-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b987c-105">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 1: Setja upp færibreytur)“.</span><span class="sxs-lookup"><span data-stu-id="b987c-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="b987c-106">Ferlið sýnir hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl sem innihalda ívafnar myndir í Microsoft Excel og Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b987c-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="b987c-107">Í þessu dæmi muntu yfirfara grunnstillingu Rafræn skýrslugerð fyrir dæmi um fyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b987c-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="b987c-108">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="b987c-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="b987c-109">Skrefin er hægt að klára með því að nota USMF gagnasafnið.</span><span class="sxs-lookup"><span data-stu-id="b987c-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="b987c-110">Yfirfara innflutt gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="b987c-110">Review the imported data model</span></span>
1. <span data-ttu-id="b987c-111">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="b987c-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b987c-112">Í trénu skal velja „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="b987c-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="b987c-113">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b987c-113">Click Designer.</span></span>
    * <span data-ttu-id="b987c-114">Þetta líkan er sett upp til að standa fyrir færslur lánardrottins frá viðskiptasjónarmiði og vörpun þessa líkans til gagnaveitu forritsins.</span><span class="sxs-lookup"><span data-stu-id="b987c-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="b987c-115">Yfirfara líkanið með Rafræn skýrslugerð Rekstrar hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b987c-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="b987c-116">Athugið að eigindir líkaneininga sem eru birtar: skipan, nafn, lýsing, tegund gagna, osfrv.</span><span class="sxs-lookup"><span data-stu-id="b987c-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="b987c-117">Stækkið „Rót“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="b987c-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="b987c-118">Í trénu skal velja „rót\ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="b987c-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="b987c-119">Í trénu skal víkka út „rót\ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="b987c-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="b987c-120">Í trénu skal víkka út „rót\ávísanir\eigindir“.</span><span class="sxs-lookup"><span data-stu-id="b987c-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="b987c-121">Í trénu skal víkka út „rót\greiðandi“.</span><span class="sxs-lookup"><span data-stu-id="b987c-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="b987c-122">Í trénu skal velja „rót\erprufukeyrsla“.</span><span class="sxs-lookup"><span data-stu-id="b987c-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="b987c-123">Í trénu skal velja „rót\útlit“.</span><span class="sxs-lookup"><span data-stu-id="b987c-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="b987c-124">Útlitseiningar líkansins standa fyrir upplýsingar um útlitsform prentun ávísunar fyrir valinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="b987c-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="b987c-125">Það inniheldur líka tvo hnúta frá tegund gagna Hólfs til að geyma myndir.</span><span class="sxs-lookup"><span data-stu-id="b987c-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="b987c-126">Í trénu skal víkka út „rót\útlit“.</span><span class="sxs-lookup"><span data-stu-id="b987c-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="b987c-127">Í trénu skal velja „rót\útlit\fyrirtæki lógó“.</span><span class="sxs-lookup"><span data-stu-id="b987c-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="b987c-128">Í trénu skal víkka út „rót\útlit\fyrirtæki lógó“.</span><span class="sxs-lookup"><span data-stu-id="b987c-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="b987c-129">Í trénu skal velja „rót\útlit\fyrirtæki lógó\mynd“.</span><span class="sxs-lookup"><span data-stu-id="b987c-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="b987c-130">Í trénu skal velja „rót\útlit\fyrirtæki lógó\erprentað“.</span><span class="sxs-lookup"><span data-stu-id="b987c-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="b987c-131">Í trénu skal velja „rót\útlit\undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="b987c-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="b987c-132">Í trénu skal víkka út „rót\útlit\undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="b987c-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="b987c-133">Í trénu skal velja „rót\útlit\undirskrift\mynd“.</span><span class="sxs-lookup"><span data-stu-id="b987c-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="b987c-134">Í trénu skal velja „rót\útlit\undirskrift\erprentað“.</span><span class="sxs-lookup"><span data-stu-id="b987c-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="b987c-135">Athugið að tvær gagnalíkanseiningar eru bundnar reitum taflanna sem innihalda myndir af lógó fyrirtækisins og undirskrift frá viðurkenndum aðila á tvöföldu formi.</span><span class="sxs-lookup"><span data-stu-id="b987c-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="b987c-136">Í trénu skal víkka út „rót\útlit\vatnsmerki“.</span><span class="sxs-lookup"><span data-stu-id="b987c-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="b987c-137">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b987c-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="b987c-138">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b987c-138">Click Designer.</span></span>
23. <span data-ttu-id="b987c-139">Í trénu skal víkka út „valdarávísanir“.</span><span class="sxs-lookup"><span data-stu-id="b987c-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="b987c-140">Í trénu skal víkka út „Útlit“.</span><span class="sxs-lookup"><span data-stu-id="b987c-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="b987c-141">Í trénu skal víkka út „útlit\fyrirtækjalógó“.</span><span class="sxs-lookup"><span data-stu-id="b987c-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="b987c-142">Í trénu skal víkka út „Útlit\Undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="b987c-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="b987c-143">Í trénu skal víkka út „útlit\vatnsmerki“.</span><span class="sxs-lookup"><span data-stu-id="b987c-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="b987c-144">Kveikið á „Sýna upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="b987c-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="b987c-145">Athugið að gagnalíkanseiningar ávísananna eru bundnar TmpChequePrintout töflunni sem, við keyrslu, mun innihalda skrár fyrir ávísanir sem notandi hefur valið fyrir prentun.</span><span class="sxs-lookup"><span data-stu-id="b987c-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="b987c-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-146">Close the page.</span></span>
30. <span data-ttu-id="b987c-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-147">Close the page.</span></span>
31. <span data-ttu-id="b987c-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="b987c-149">Yfirfara innflutt snið</span><span class="sxs-lookup"><span data-stu-id="b987c-149">Review the imported format</span></span>
1. <span data-ttu-id="b987c-150">Í trénu skal víkka út „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="b987c-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="b987c-151">Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="b987c-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="b987c-152">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b987c-152">Click Designer.</span></span>
4. <span data-ttu-id="b987c-153">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="b987c-153">Click Attachments.</span></span>
5. <span data-ttu-id="b987c-154">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="b987c-154">Click Open.</span></span>
    * <span data-ttu-id="b987c-155">Opna viðhengt sniðmát skýrslu í Excel.</span><span class="sxs-lookup"><span data-stu-id="b987c-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="b987c-156">Yfirfara viðhengt Ecxel-sniðmát skýrslunnar sem verður notuð til að prenta ávísanirnar.</span><span class="sxs-lookup"><span data-stu-id="b987c-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="b987c-157">Sniðmátið inniheldur tvær ávísanir fyrir hverja síðu og er hannað til að prenta ávísanir til forprentaðs forms.</span><span class="sxs-lookup"><span data-stu-id="b987c-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="b987c-158">Athugið að tvær auðar myndir eru ívafðar.</span><span class="sxs-lookup"><span data-stu-id="b987c-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="b987c-159">Þessar auðu myndir eru fyrir lógó fyrirtækisins og undirskrift þess aðila sem heimilar greiðslu.</span><span class="sxs-lookup"><span data-stu-id="b987c-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="b987c-160">Staðfesta að myndirnar heita CompLogo og SignatureImage í Excel.</span><span class="sxs-lookup"><span data-stu-id="b987c-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="b987c-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-161">Close the page.</span></span>
7. <span data-ttu-id="b987c-162">Stækkið „skýrsla“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="b987c-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="b987c-163">Í trénu skal víkka út „Skýrsla\ChequeLines“.</span><span class="sxs-lookup"><span data-stu-id="b987c-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="b987c-164">Í trénu skal velja 'Report\ChequeLines\CompLogo'.</span><span class="sxs-lookup"><span data-stu-id="b987c-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="b987c-165">Kveikið á „Sýna upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="b987c-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="b987c-166">Athugið að reitaeining „CompLogo“ sniðsins stendur fyrir Excel afurðina sem er notuð til að útfylla myndina af lógó fyrirtækisins í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="b987c-167">Þetta sniðseining er bundin við myndgagnalíkanseininguna sem, við keyrslu, inniheldur mynd af lógó fyrirtækisins í tvöföldu formi.</span><span class="sxs-lookup"><span data-stu-id="b987c-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="b987c-168">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="b987c-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="b987c-169">Smella á virkja Breytingar.</span><span class="sxs-lookup"><span data-stu-id="b987c-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="b987c-170">Athugið að hægt er að búa til hólfeiningar sniðsins „CompLogo“ þannig að það er ekki lengur virkt.</span><span class="sxs-lookup"><span data-stu-id="b987c-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="b987c-171">Þannig mun Excel myndeiningin sem þessu tengist fela lógó fyrirtækisins í skýrslunni sem búin er til.</span><span class="sxs-lookup"><span data-stu-id="b987c-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="b987c-172">Ef segðin sem er virk skilar af sér SATT og skilgreind bindingin birtir enga mynd, mun Excel myndeiningin sem þessu tengist sýna mynd sem hefur verið vistuð í Excel sniðinu.</span><span class="sxs-lookup"><span data-stu-id="b987c-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="b987c-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-173">Close the page.</span></span>
14. <span data-ttu-id="b987c-174">Stækkið „merkimiða: Hólf“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="b987c-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="b987c-175">Sumir merkimiðar sem birtast í forprentuðu ávísanaforminu verða með í skýrslunni þegar hún er stofnuð til prófunar.</span><span class="sxs-lookup"><span data-stu-id="b987c-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="b987c-176">Þessir merkimiðar verða samt sem áður ekki prentaðir þegar raunprentun fer fram, vegna þess að forprentaða formið inniheldur þá nú þegar.</span><span class="sxs-lookup"><span data-stu-id="b987c-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="b987c-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b987c-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]