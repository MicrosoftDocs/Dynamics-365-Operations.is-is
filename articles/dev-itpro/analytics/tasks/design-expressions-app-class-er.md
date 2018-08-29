--- 
title: "Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka"
description: "Þessi handbók veitir upplýsingar um hvernig á að endurnýta núverandi forritaskrár í grunnstillingu rafrænnar skýrslugerðar (ER) með því að kalla á nauðsynlegar aðferðir við forritaflokka í segðum rafrænnar skýrslugerðar."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="d6a01-103">Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka</span><span class="sxs-lookup"><span data-stu-id="d6a01-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6a01-104">Þessi handbók veitir upplýsingar um hvernig á að endurnýta núverandi forritaskrár í grunnstillingu rafrænnar skýrslugerðar (ER) með því að kalla á nauðsynlegar aðferðir við forritaflokka í segðum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="d6a01-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="d6a01-105">Hægt er að skilgreina gildi frumbreyta fyrir köllunarflokka á keyrslutíma: Til dæmis byggt á upplýsingum í þáttunarskjalinu til að tryggja réttmæti þess.</span><span class="sxs-lookup"><span data-stu-id="d6a01-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="d6a01-106">Í þessum leiðbeiningum mun notandi stofna þær grunnstillingar rafrænnar skýrslugerðar sem krafist er fyrir sýnifyrirtækið Litware, Inc. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="d6a01-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="d6a01-107">Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er.</span><span class="sxs-lookup"><span data-stu-id="d6a01-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="d6a01-108">Þú verður líka að hlaða niður og vista eftirfarandi skrá staðbundið: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="d6a01-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="d6a01-109">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð Stofna skilgreiningaveitu og merkja hana sem virka.“</span><span class="sxs-lookup"><span data-stu-id="d6a01-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="d6a01-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d6a01-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d6a01-111">Sannprófið að grunnstillingarveita fyrir sýnifyrirtækið Litware, Inc. sé tiltæk og merkt sem virk.</span><span class="sxs-lookup"><span data-stu-id="d6a01-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="d6a01-112">Ef þessi skilgreiningarveita sést ekki, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="d6a01-113">Gerum ráð fyrir að þú sért að hanna aðferð til að þátta bankayfirlit á innleið fyrir uppfærslu á umsóknargögnum.</span><span class="sxs-lookup"><span data-stu-id="d6a01-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="d6a01-114">Þú færð bankayfirlit á innleið sem TXT skrár sem innihalda IBAN kóða.</span><span class="sxs-lookup"><span data-stu-id="d6a01-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="d6a01-115">Sem hluti af innflutningsferli bankareikningsins þarftu að staðfesta réttmæti þessara IBAN kóða með því að nota rökfræði sem er nú þegar í boði í Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d6a01-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="d6a01-116">Flytja inn nýja grunnstillingu líkans í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="d6a01-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="d6a01-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d6a01-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6a01-118">Velja skal Microsoft reitinn.</span><span class="sxs-lookup"><span data-stu-id="d6a01-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="d6a01-119">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="d6a01-119">Click Repositories.</span></span>
3. <span data-ttu-id="d6a01-120">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="d6a01-120">Click Show filters.</span></span>
4. <span data-ttu-id="d6a01-121">Bæta við síureit „Gerð heitis“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="d6a01-122">Í svæðinu heiti skal færa inn gildið „tilföng“, velja síuna „inniheldur“ og smella svo á nota.</span><span class="sxs-lookup"><span data-stu-id="d6a01-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="d6a01-123">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="d6a01-123">Click Open.</span></span>
6. <span data-ttu-id="d6a01-124">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="d6a01-125">Ef innflutningshnappurinn á flýtiflipa Versions er ekki virkur hefur útgáfa 1 af stillingum „Greiðslulíkan“ rafrænnar skýrslugerðar þegar verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="d6a01-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="d6a01-126">Þú mátt sleppa þeim skrefum sem eftir eru í þessu undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="d6a01-127">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="d6a01-127">Click Import.</span></span>
8. <span data-ttu-id="d6a01-128">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="d6a01-128">Click Yes.</span></span>
9. <span data-ttu-id="d6a01-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-129">Close the page.</span></span>
10. <span data-ttu-id="d6a01-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="d6a01-131">Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="d6a01-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="d6a01-132">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="d6a01-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d6a01-133">Bæta við nýju sniði fyrir rafræna skýrslugerð til að þátta bankayfirlit á innleið á TXT-sniði.</span><span class="sxs-lookup"><span data-stu-id="d6a01-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="d6a01-134">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="d6a01-135">Smellt er á Stofna skilgreiningu til að opna svarglugga.</span><span class="sxs-lookup"><span data-stu-id="d6a01-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="d6a01-136">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="d6a01-137">Í reitnum Heiti skal færa inn „Innflutningssnið bankayfirlits (dæmi)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="d6a01-138">Innflutningssnið bankayfirlits (dæmi)</span><span class="sxs-lookup"><span data-stu-id="d6a01-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="d6a01-139">Velja Já í svæði Styður gagnainnflutning.</span><span class="sxs-lookup"><span data-stu-id="d6a01-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="d6a01-140">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d6a01-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="d6a01-141">Veljið grunnstillingu rafrænnar skýrslugerðar - snið</span><span class="sxs-lookup"><span data-stu-id="d6a01-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="d6a01-142">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="d6a01-142">Click Designer.</span></span>
    * <span data-ttu-id="d6a01-143">Uppsetta sniðið stendur fyrir væntanlega uppbyggingu ytri skráar á TXT-sniði.</span><span class="sxs-lookup"><span data-stu-id="d6a01-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="d6a01-144">Smelltu á Bæta við rót til að opna svargluggann.</span><span class="sxs-lookup"><span data-stu-id="d6a01-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="d6a01-145">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="d6a01-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="d6a01-146">Í reitnum Heiti skal færa inn ‚rót'.</span><span class="sxs-lookup"><span data-stu-id="d6a01-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="d6a01-147">Rót</span><span class="sxs-lookup"><span data-stu-id="d6a01-147">Root</span></span>  
5. <span data-ttu-id="d6a01-148">Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="d6a01-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="d6a01-149">Valkosturinn „Ný lína - Windows (CR LF)“ hefur verið valinn í reitnum „sérstafir“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="d6a01-150">Byggt á þessari stillingu telst sérhver lína í þáttunarskrá aðskilin færsla.</span><span class="sxs-lookup"><span data-stu-id="d6a01-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="d6a01-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-151">Click OK.</span></span>
7. <span data-ttu-id="d6a01-152">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d6a01-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="d6a01-153">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="d6a01-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="d6a01-154">Í svæðið Heiti skal slá inn „Raðir“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="d6a01-155">Línur</span><span class="sxs-lookup"><span data-stu-id="d6a01-155">Rows</span></span>  
10. <span data-ttu-id="d6a01-156">Veljið „Einn margir“ í svæðinu Margfeldi.</span><span class="sxs-lookup"><span data-stu-id="d6a01-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="d6a01-157">Valkosturinn „Einn margir“ hefur verið valinn í svæðinu „Margfeldi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="d6a01-158">Byggt á þessari stillingu er gert ráð fyrir að minnsta kosti ein lína verði kynnt í þáttunarskránni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="d6a01-159">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-159">Click OK.</span></span>
12. <span data-ttu-id="d6a01-160">Í trénu skal velja „Rót\Raðir“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="d6a01-161">Smellið á „Bæta við röð“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="d6a01-162">Í svæðið Heiti skal slá inn „Svæði“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="d6a01-163">Svæði</span><span class="sxs-lookup"><span data-stu-id="d6a01-163">Fields</span></span>  
15. <span data-ttu-id="d6a01-164">Veljið „Akkúrat einn“ í svæðinu Margfeldi.</span><span class="sxs-lookup"><span data-stu-id="d6a01-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="d6a01-165">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-165">Click OK.</span></span>
17. <span data-ttu-id="d6a01-166">Í trénu skal velja „Rót\Raðir\Reitir“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="d6a01-167">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d6a01-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="d6a01-168">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="d6a01-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="d6a01-169">Í svæðið Heiti, færðu inn ‚IBAN-númer'.</span><span class="sxs-lookup"><span data-stu-id="d6a01-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="d6a01-170">IBAN-númer</span><span class="sxs-lookup"><span data-stu-id="d6a01-170">IBAN</span></span>  
21. <span data-ttu-id="d6a01-171">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-171">Click OK.</span></span>
    * <span data-ttu-id="d6a01-172">Það hefur verið stillt á að hver lína í þáttunarskrá innihaldi eina IBAN kóðann.</span><span class="sxs-lookup"><span data-stu-id="d6a01-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="d6a01-173">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="d6a01-174">Veljið grunnstillingu rafrænnar skýrslugerðar - vörpun í gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="d6a01-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="d6a01-175">Smellt er á Varpa sniði á líkan.</span><span class="sxs-lookup"><span data-stu-id="d6a01-175">Click Map format to model.</span></span>
2. <span data-ttu-id="d6a01-176">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-176">Click New.</span></span>
3. <span data-ttu-id="d6a01-177">Í svæði Skilgreining skal slá inn „BankToCustomerDebitCreditNotificationInitiation“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="d6a01-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="d6a01-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="d6a01-179">„Leysa úr“ breytir skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d6a01-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="d6a01-180">Í reitnum Heiti skal færa inn „Vörpun í gagnalíkan“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="d6a01-181">Vörpun í gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="d6a01-181">Mapping to data model</span></span>  
6. <span data-ttu-id="d6a01-182">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-182">Click Save.</span></span>
7. <span data-ttu-id="d6a01-183">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="d6a01-183">Click Designer.</span></span>
8. <span data-ttu-id="d6a01-184">Í trénu skal velja „Dynamics 365 for Operations\Klasi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="d6a01-185">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="d6a01-185">Click Add root.</span></span>
    * <span data-ttu-id="d6a01-186">Bæta nýjum gagnagjafa við fyrirliggjandi forritsgrunn fyrir sannprófun IBAN-númera.</span><span class="sxs-lookup"><span data-stu-id="d6a01-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="d6a01-187">Í svæðið Heiti skal slá inn „check_codes“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="d6a01-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="d6a01-188">check_codes</span></span>  
11. <span data-ttu-id="d6a01-189">Í reitinn klasi skal færa inn „ISO7064“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="d6a01-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="d6a01-190">ISO7064</span></span>  
12. <span data-ttu-id="d6a01-191">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-191">Click OK.</span></span>
13. <span data-ttu-id="d6a01-192">Í trénu skal víkka út „snið“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="d6a01-193">Í trénu skal víkka út „snið\Rót: Röð(Rót)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="d6a01-194">Í trénu skal velja „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="d6a01-195">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="d6a01-195">Click Bind.</span></span>
17. <span data-ttu-id="d6a01-196">Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="d6a01-197">Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)\Reitir: Röð 1..1 (Reitir)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="d6a01-198">Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)\Reitir: Röð 1..1 (Reitir)\IBAN: Strengur(IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="d6a01-199">Í trénu skal víkka út „Payments = format.Root.Rows“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="d6a01-200">Í trénu skal víkka út „Payments = format.Root.Rows\Reikningur lánveitanda(CreditorAccount)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="d6a01-201">Í trénu skal víkka út „Payments = format.Root.Rows\Reikningur lánveitanda(CreditorAccount)\Sannkennsl“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="d6a01-202">Í trénu skal velja „Payments = format.Root.Rows\Reikningur lánveitanda(CreditorAccount)\Sannkennsl\IBAN“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="d6a01-203">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="d6a01-203">Click Bind.</span></span>
25. <span data-ttu-id="d6a01-204">Smellt er á flipann Sannprófanir.</span><span class="sxs-lookup"><span data-stu-id="d6a01-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="d6a01-205">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-205">Click New.</span></span>
    * <span data-ttu-id="d6a01-206">Bættu við nýrri villuleitarreglu sem sýnir villu fyrir hvaða línu sem er í þáttunarskránni sem inniheldur ógildan IBAN kóða.</span><span class="sxs-lookup"><span data-stu-id="d6a01-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="d6a01-207">Breyta skilyrði.</span><span class="sxs-lookup"><span data-stu-id="d6a01-207">Click Edit condition.</span></span>
28. <span data-ttu-id="d6a01-208">Í trénu skal víkka út „check_codes“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="d6a01-209">Í trénu skal velja „check_codes\verifyMOD1271_36“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="d6a01-210">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="d6a01-210">Click Add data source.</span></span>
31. <span data-ttu-id="d6a01-211">Í Formúlureitinn skal slá inn „check_codes.verifyMOD1271_36('.</span><span class="sxs-lookup"><span data-stu-id="d6a01-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="d6a01-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="d6a01-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="d6a01-213">Í trénu skal víkka út „snið“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="d6a01-214">Í trénu skal víkka út „snið\Rót: Röð(Rót)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="d6a01-215">Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="d6a01-216">Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)\Reitir: Röð 1..1 (Reitir)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="d6a01-217">Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..\* (Raðir)\Reitir: Röð 1..1 (Reitir)\IBAN: Strengur(IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="d6a01-218">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="d6a01-218">Click Add data source.</span></span>
38. <span data-ttu-id="d6a01-219">Í Formúlureitinn skal slá inn „check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="d6a01-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="d6a01-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="d6a01-221">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-221">Click Save.</span></span>
40. <span data-ttu-id="d6a01-222">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-222">Close the page.</span></span>
    * <span data-ttu-id="d6a01-223">Villuleitarskilyrði hafa verið stillt til að skila FALSE fyrir hvaða ógildan IBAN kóða með því að kalla núverandi aðferð „verifyMOD1271_36“ umsóknarflokksins „ISO7064“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="d6a01-224">Athugaðu að gildi IBAN-kóðans er skilgreindt gagnvirkt á keyrslutíma sem frumbreyta köllunaraðferðarinnar, byggt á innihaldi TXT þáttunarskráarinnar.</span><span class="sxs-lookup"><span data-stu-id="d6a01-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="d6a01-225">Smellt er á Breyta skilaboðum.</span><span class="sxs-lookup"><span data-stu-id="d6a01-225">Click Edit message.</span></span>
42. <span data-ttu-id="d6a01-226">Í Formúlureitinn skal slá inn „CONCATENATE("Invalid IBAN code has been found: format.Root.Rows.Fields.IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="d6a01-227">CONCATENATE(„Ógildur IBAN-kóði fannst: “, format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="d6a01-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="d6a01-228">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-228">Click Save.</span></span>
44. <span data-ttu-id="d6a01-229">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-229">Close the page.</span></span>
45. <span data-ttu-id="d6a01-230">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-230">Click Save.</span></span>
46. <span data-ttu-id="d6a01-231">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d6a01-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="d6a01-232">Keyra vörpun sniðs</span><span class="sxs-lookup"><span data-stu-id="d6a01-232">Run the format mapping</span></span>
<span data-ttu-id="d6a01-233">Til að prófa, skal framkvæma vörpun sniðs með SampleIncomingMessage.txt-skránni sem þú sóttir.</span><span class="sxs-lookup"><span data-stu-id="d6a01-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="d6a01-234">Myndað úttak inniheldur gögn sem verða flutt inn úr valinni TXT-skrá og fyllt út í sérstillt gagnalíkan í rauninnflutningi.</span><span class="sxs-lookup"><span data-stu-id="d6a01-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="d6a01-235">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-235">Click Run.</span></span>
    * <span data-ttu-id="d6a01-236">Smellt er á Fletta og flett á skrána SampleIncomingMessage.txt sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="d6a01-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="d6a01-237">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d6a01-237">Click OK.</span></span>
    * <span data-ttu-id="d6a01-238">Farið yfir úttak í XML-sniði, sem stendur fyrir gögn sem hafa verið innflutt úr valinni skrá og tengd við gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="d6a01-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="d6a01-239">Athugaðu að aðeins 3 línur af innfluttri TXT-skrá voru unnar.</span><span class="sxs-lookup"><span data-stu-id="d6a01-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="d6a01-240">IBAN-númerið á línu 4 sem er ógilt var sleppt og villuskilaboð eru veitt í Infolog.</span><span class="sxs-lookup"><span data-stu-id="d6a01-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  


