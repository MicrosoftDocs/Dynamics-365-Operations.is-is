---
title: Búa til skýrslur á Office-sniði með innfelldum myndum
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki „Kerfisstjóra“ eða „Þróunaraðila rafrænnar skýrslulausnar“ getur hannað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl í MS office sniði (Excel og Word) sem innihalda ívafnar myndir.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684380"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="3a546-103">Búa til skýrslur á Office-sniði með innfelldum myndum</span><span class="sxs-lookup"><span data-stu-id="3a546-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3a546-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki „Kerfisstjóra“ eða „Þróunaraðila rafrænnar skýrslulausnar“ getur hannað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl í MS office sniði (Excel og Word) sem innihalda ívafnar myndir.</span><span class="sxs-lookup"><span data-stu-id="3a546-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="3a546-105">Í þessu dæmi muntu nota stofnaða Rafræn skýrslugerð skilgreiningar fyrir sýni fyrirtæki, „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="3a546-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="3a546-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Rafræn skýrslugerð í MS Office sniði með ívafnar myndir (Hluti 2: Endurskoða grunnstillingar)“.</span><span class="sxs-lookup"><span data-stu-id="3a546-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="3a546-107">Hægt er að framkvæma þessi skref í „USMF“ fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="3a546-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="3a546-108">Keyra snið með upphaflegu vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="3a546-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="3a546-109">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="3a546-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="3a546-110">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="3a546-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="3a546-111">Í aðgerðasvæðinu er smellt á setja upp.</span><span class="sxs-lookup"><span data-stu-id="3a546-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="3a546-112">Smella skal á athuga.</span><span class="sxs-lookup"><span data-stu-id="3a546-112">Click Check.</span></span>
5. <span data-ttu-id="3a546-113">Smella á Prenta athugun.</span><span class="sxs-lookup"><span data-stu-id="3a546-113">Click Print test.</span></span>
    * <span data-ttu-id="3a546-114">Keyra sniðið til prufu.</span><span class="sxs-lookup"><span data-stu-id="3a546-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="3a546-115">Veljið Já í reitnum Snið fyrir framseljanlega ávísun</span><span class="sxs-lookup"><span data-stu-id="3a546-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="3a546-116">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3a546-116">Click OK.</span></span>
    * <span data-ttu-id="3a546-117">Endurskoða stofnað úttak.</span><span class="sxs-lookup"><span data-stu-id="3a546-117">Review the created output.</span></span> <span data-ttu-id="3a546-118">Lógó fyrirtækisins er í skýrslunni ásamt undirskrift frá viðurkenndum aðila.</span><span class="sxs-lookup"><span data-stu-id="3a546-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="3a546-119">Myndin af undirskriftinni er tekin úr reit frá „Hólf“ gagnategund úr útlitskrá ávísunar sem tengist völdum bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="3a546-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="3a546-120">Útvíkka hluta Eintaka.</span><span class="sxs-lookup"><span data-stu-id="3a546-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="3a546-121">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="3a546-121">Click Edit.</span></span>
10. <span data-ttu-id="3a546-122">Í reitnum vatnsmerki, skal færa inn „Prenta vatnsmerki sem ógilt“.</span><span class="sxs-lookup"><span data-stu-id="3a546-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="3a546-123">Breyta stillingu vatnsmerkjasniðsins þannig að það sýni vatnsmerkjatextann í mynduðu skjali í Excel lagaðri einingu.</span><span class="sxs-lookup"><span data-stu-id="3a546-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="3a546-124">Smella á Prenta athugun.</span><span class="sxs-lookup"><span data-stu-id="3a546-124">Click Print test.</span></span>
12. <span data-ttu-id="3a546-125">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3a546-125">Click OK.</span></span>
    * <span data-ttu-id="3a546-126">Endurskoða stofnað úttak.</span><span class="sxs-lookup"><span data-stu-id="3a546-126">Review the created output.</span></span> <span data-ttu-id="3a546-127">Vatnsmerkið er sýnt í stofnuðu skýrslunni í samræmi við valmöguleikann.</span><span class="sxs-lookup"><span data-stu-id="3a546-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="3a546-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-128">Close the page.</span></span>
14. <span data-ttu-id="3a546-129">Í Aðgerðarrúðunni er smellt á Stjórna greiðslum.</span><span class="sxs-lookup"><span data-stu-id="3a546-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="3a546-130">Smellið á Ávísanir.</span><span class="sxs-lookup"><span data-stu-id="3a546-130">Click Checks.</span></span>
16. <span data-ttu-id="3a546-131">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="3a546-131">Click Show filters.</span></span>
17. <span data-ttu-id="3a546-132">Notið eftirfarandi síur: færðu inn síugildi "381","385","389" á reitnum "heiti ávísunarnúmer" með því að nota síuvirknitáknið „er eitt af".</span><span class="sxs-lookup"><span data-stu-id="3a546-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="3a546-133">Í listanum er merkt við allar línur.</span><span class="sxs-lookup"><span data-stu-id="3a546-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="3a546-134">Smellið á Prenta afrit af ávísun</span><span class="sxs-lookup"><span data-stu-id="3a546-134">Click Print check copy.</span></span>
    * <span data-ttu-id="3a546-135">Keyrið sniðið til að endurprenta valdar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="3a546-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="3a546-136">Endurskoða stofnað úttak.</span><span class="sxs-lookup"><span data-stu-id="3a546-136">Review the created output.</span></span> <span data-ttu-id="3a546-137">Vldar ávísanirnar hafa verið endurprentaðar.</span><span class="sxs-lookup"><span data-stu-id="3a546-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="3a546-138">Lógó og merkimiðar fyrirtækisins eru ekki prentaðir út því þeir birtast á forprentaða forminu.</span><span class="sxs-lookup"><span data-stu-id="3a546-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="3a546-139">Breyta vörpun innflutts gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="3a546-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="3a546-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-140">Close the page.</span></span>
2. <span data-ttu-id="3a546-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-141">Close the page.</span></span>
3. <span data-ttu-id="3a546-142">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="3a546-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="3a546-143">Í trénu skal velja „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="3a546-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="3a546-144">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="3a546-144">Click Designer.</span></span>
6. <span data-ttu-id="3a546-145">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="3a546-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="3a546-146">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="3a546-146">Click Designer.</span></span>
    * <span data-ttu-id="3a546-147">Við munum breyta bindingu undirskriftarafurðar gagnalíkans til að ná í undirskriftarmyndina frá skjalinu sem hefur verið hengt við útlitsskrá ávísunarinnar sem er tengd við valinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="3a546-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="3a546-148">Slökkva á Sýna upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="3a546-148">Turn off Show details.</span></span>
9. <span data-ttu-id="3a546-149">Í trénu skal víkka út „Útlit“.</span><span class="sxs-lookup"><span data-stu-id="3a546-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="3a546-150">Í trénu skal víkka út „Útlit\Undirskrift“.</span><span class="sxs-lookup"><span data-stu-id="3a546-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="3a546-151">Í trénu skal velja „Útlit\Undirskrift\mynd = ávísanareikningur.„<Tengsl“.BankChequeLayout.Signature1Bmp“.</span><span class="sxs-lookup"><span data-stu-id="3a546-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="3a546-152">Í trénu skal víkka út „ávísanareikningur“.</span><span class="sxs-lookup"><span data-stu-id="3a546-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="3a546-153">Í trénu skal víkka út „ávísanareikningur\<Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="3a546-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="3a546-154">Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout“.</span><span class="sxs-lookup"><span data-stu-id="3a546-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="3a546-155">Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout\<Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="3a546-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="3a546-156">Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout\<Tengsl\<Skjöl“.</span><span class="sxs-lookup"><span data-stu-id="3a546-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="3a546-157">Í trénu skal víkka út „ávísanareikningur\<Tengsl\BankChequeLayout\<Tengsl\<Skjöl\getFileContentAsContainer()“.</span><span class="sxs-lookup"><span data-stu-id="3a546-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="3a546-158">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="3a546-158">Click Bind.</span></span>
19. <span data-ttu-id="3a546-159">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3a546-159">Click Save.</span></span>
20. <span data-ttu-id="3a546-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-160">Close the page.</span></span>
21. <span data-ttu-id="3a546-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-161">Close the page.</span></span>
22. <span data-ttu-id="3a546-162">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-162">Close the page.</span></span>
23. <span data-ttu-id="3a546-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="3a546-164">Keyra snið með því að nota leiðrétta vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="3a546-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="3a546-165">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="3a546-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="3a546-166">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="3a546-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3a546-167">Til dæmis, sía svæðið bankareikningur með gildið 'USMF OPER'.</span><span class="sxs-lookup"><span data-stu-id="3a546-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="3a546-168">Í aðgerðasvæðinu er smellt á setja upp.</span><span class="sxs-lookup"><span data-stu-id="3a546-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="3a546-169">Smella skal á athuga.</span><span class="sxs-lookup"><span data-stu-id="3a546-169">Click Check.</span></span>
5. <span data-ttu-id="3a546-170">Smella á Prenta athugun.</span><span class="sxs-lookup"><span data-stu-id="3a546-170">Click Print test.</span></span>
6. <span data-ttu-id="3a546-171">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3a546-171">Click OK.</span></span>
    * <span data-ttu-id="3a546-172">Endurskoða stofnað úttak.</span><span class="sxs-lookup"><span data-stu-id="3a546-172">Review the created output.</span></span> <span data-ttu-id="3a546-173">Myndin frá viðhengi Skjalastjórnunar birtist sem undirskrift frá viðurkenndum aðila.</span><span class="sxs-lookup"><span data-stu-id="3a546-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="3a546-174">Nota MS Word skjal sem sniðmát í innflutta sniðinu</span><span class="sxs-lookup"><span data-stu-id="3a546-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="3a546-175">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-175">Close the page.</span></span>
2. <span data-ttu-id="3a546-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-176">Close the page.</span></span>
3. <span data-ttu-id="3a546-177">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="3a546-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="3a546-178">Í trénu skal víkka út „Líkan fyrir ávísanir“.</span><span class="sxs-lookup"><span data-stu-id="3a546-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="3a546-179">Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.</span><span class="sxs-lookup"><span data-stu-id="3a546-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="3a546-180">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="3a546-180">Click Designer.</span></span>
7. <span data-ttu-id="3a546-181">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="3a546-181">Click Attachments.</span></span>
8. <span data-ttu-id="3a546-182">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="3a546-182">Click Delete.</span></span>
9. <span data-ttu-id="3a546-183">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="3a546-183">Click Yes.</span></span>
10. <span data-ttu-id="3a546-184">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3a546-184">Click New.</span></span>
11. <span data-ttu-id="3a546-185">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="3a546-185">Click File.</span></span>
    * <span data-ttu-id="3a546-186">Smellið á Fletta og veljið fyrirfram sótt „Cheque template Word.docx“ skjal.</span><span class="sxs-lookup"><span data-stu-id="3a546-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="3a546-187">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-187">Close the page.</span></span>
13. <span data-ttu-id="3a546-188">Sláið inn eða veldu gildi í reitnum sniðmát.</span><span class="sxs-lookup"><span data-stu-id="3a546-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="3a546-189">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3a546-189">Click Save.</span></span>
15. <span data-ttu-id="3a546-190">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-190">Close the page.</span></span>
16. <span data-ttu-id="3a546-191">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="3a546-191">Click Edit.</span></span>
17. <span data-ttu-id="3a546-192">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="3a546-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="3a546-193">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3a546-193">Close the page.</span></span>
19. <span data-ttu-id="3a546-194">Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="3a546-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="3a546-195">Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.</span><span class="sxs-lookup"><span data-stu-id="3a546-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="3a546-196">Smella skal á athuga.</span><span class="sxs-lookup"><span data-stu-id="3a546-196">Click Check.</span></span>
22. <span data-ttu-id="3a546-197">Smella á Prenta athugun.</span><span class="sxs-lookup"><span data-stu-id="3a546-197">Click Print test.</span></span>
23. <span data-ttu-id="3a546-198">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3a546-198">Click OK.</span></span>
    * <span data-ttu-id="3a546-199">Endurskoða stofnað úttak.</span><span class="sxs-lookup"><span data-stu-id="3a546-199">Review the created output.</span></span> <span data-ttu-id="3a546-200">Úttakið hefur verið búið til sem MS Word skjal með ívafnar myndir þar sem lógó fyrirtækisins birtist, undirskrift frá viðurkenndum aðila og valinn texti vatnsmerkisins.</span><span class="sxs-lookup"><span data-stu-id="3a546-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

