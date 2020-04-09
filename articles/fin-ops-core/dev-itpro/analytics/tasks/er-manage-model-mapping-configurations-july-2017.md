---
title: Stjórna vörum líkana rafrænar skýrslugerðar í mismunandi skilgreiningar rafrænnar skýrslugerðar
description: Eftirfarandi skref útskýra hvernig notanda sem úthlutað hefur verið hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stjórnað líkansvörpun fyrir Rafræna skýrslugerð (ER) úr öðrum grunnstillingum Rafræn skýrslugerð.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: b8ff3b419caafec626497c65ea18ca24ca95cb5d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143054"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="48767-103">Stjórna vörum líkana rafrænar skýrslugerðar í mismunandi skilgreiningar rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="48767-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48767-104">Eftirfarandi skref útskýra hvernig notanda sem úthlutað hefur verið hlutverk Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stjórnað líkansvörpun fyrir Rafræna skýrslugerð (ER) úr öðrum grunnstillingum Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="48767-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="48767-105">Í þessum verkefnaleiðbeiningum skal stofna nauðsynlega grunnstillingu Rafræn skýrslugerð fyrir sýnifyrirtæki, Litware, Inc. Til að ljúka þessum verkefnaleiðbeiningum, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningum „Stofna grunnstillingarveitu í Rafræna skýrslugerð” og merkja hana sem virka.</span><span class="sxs-lookup"><span data-stu-id="48767-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="48767-106">Þar sem grunnstillingar Rafræn skýrslugerð er deilt á meðal fyrirtækja, geturðu lokið við þessar verkefnaleiðbeiningar með því að nota fyrirtækjagagnasafn að eigin vali.</span><span class="sxs-lookup"><span data-stu-id="48767-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="48767-107">Virkni fyrir þessar verkefnaleiðbeiningar eru tiltækar ef þú hefur hlaðið inn einni af eftirfarandi bráðabótum: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 fyrir Dynamics AX 7.0 útgáfuna eða https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 fyrir Dynamics 365 for Operations útfgáfuna.</span><span class="sxs-lookup"><span data-stu-id="48767-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="48767-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="48767-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="48767-109">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="48767-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="48767-110">Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í verkefnaleiðbeiningar „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="48767-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="48767-111">Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="48767-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="48767-112">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="48767-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="48767-113">Bæta við nýrri grunnstillingu líkans.</span><span class="sxs-lookup"><span data-stu-id="48767-113">Add a new model configuration.</span></span> <span data-ttu-id="48767-114">Heitið verður að vera einkvæmt í tré grunnstillingarinnar.</span><span class="sxs-lookup"><span data-stu-id="48767-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="48767-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="48767-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="48767-116">Í svæðið Heiti, Færðu inn „Sýnigagnalíkan“.</span><span class="sxs-lookup"><span data-stu-id="48767-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="48767-117">Sýnigagnalíkan</span><span class="sxs-lookup"><span data-stu-id="48767-117">Sample data model</span></span>  
4. <span data-ttu-id="48767-118">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="48767-118">Click Create configuration.</span></span>
5. <span data-ttu-id="48767-119">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="48767-119">Click Designer.</span></span>
6. <span data-ttu-id="48767-120">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="48767-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="48767-121">Í reitnum Heiti skal færa inn ‚rót'.</span><span class="sxs-lookup"><span data-stu-id="48767-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="48767-122">Rót</span><span class="sxs-lookup"><span data-stu-id="48767-122">Root</span></span>  
8. <span data-ttu-id="48767-123">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="48767-123">Click Add.</span></span>
9. <span data-ttu-id="48767-124">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="48767-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="48767-125">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="48767-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="48767-126">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="48767-126">Company</span></span>  
11. <span data-ttu-id="48767-127">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="48767-127">Click Add.</span></span>
12. <span data-ttu-id="48767-128">Í reitinn Lýsing skal færa inn textann, Lýsing á lögaðila eða fyrirtæki sem notandi er skráður inn á við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="48767-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="48767-129">Lýsing á lögaðila eða fyrirtæki sem notandi er skráður inn á við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="48767-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="48767-130">Smelltu á Rótartilvísun</span><span class="sxs-lookup"><span data-stu-id="48767-130">Click Root reference.</span></span>
14. <span data-ttu-id="48767-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-131">Click OK.</span></span>
15. <span data-ttu-id="48767-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="48767-132">Click Save.</span></span>
16. <span data-ttu-id="48767-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-133">Close the page.</span></span>
17. <span data-ttu-id="48767-134">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="48767-134">Click Change status.</span></span>
18. <span data-ttu-id="48767-135">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="48767-135">Click Complete.</span></span>
19. <span data-ttu-id="48767-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="48767-137">Bæta við nýrri grunnstillingu líkan vörpun í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="48767-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="48767-138">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="48767-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="48767-139">Í svæði Nýtt skal slá inn „Vörpun líkans byggð á gagnalíkani Sýnigagnalíkani“.</span><span class="sxs-lookup"><span data-stu-id="48767-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="48767-140">Í svæðið Heiti, færðu inn „Sýnivörpun“.</span><span class="sxs-lookup"><span data-stu-id="48767-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="48767-141">Sýnivörpun</span><span class="sxs-lookup"><span data-stu-id="48767-141">Sample mapping</span></span>  
4. <span data-ttu-id="48767-142">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="48767-142">Click Create configuration.</span></span>
5. <span data-ttu-id="48767-143">Stækka hlutann Skilyrði</span><span class="sxs-lookup"><span data-stu-id="48767-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="48767-144">Athugið að skilyrðaflokkur Framkvæmdir hefur verið bætt sjálfkrafa við.</span><span class="sxs-lookup"><span data-stu-id="48767-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="48767-145">Flokkurinn inniheldur skilyrðahlutana sem taka til yfireiningar grunnstillingar gagnalíkansins og er merkt sem Framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="48767-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="48767-146">Þetta þýðir að þetta sýnidæmi um grunnstillingar vörpun líkansvörpunar er talið samsvara því að setja gagnalíkanið í framkvæmd, Sýnigagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="48767-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="48767-147">Þar af leiðandi mun þessi hluti neyða Rafræn skýrslugerð til að hlaða niður grunnstillingum líkansvörpunarinnar, Sýnivörpun frá geymslu Rafræn skýrslugerð þegar grunnstillingar líkans, Sýnigagnalíkan, er hlaðið niður.</span><span class="sxs-lookup"><span data-stu-id="48767-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="48767-148">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="48767-148">Click Designer.</span></span>
    * <span data-ttu-id="48767-149">Athugið að grunnstillingar líkansvörpunar sem þegar hafa verið stofnaðar, innihalda nýja og auða vörpun með sama heiti og grunnstillingin sem þegar hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="48767-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="48767-150">Verið meðvituð um það að þegar valin yfireining grunnstillingar líkans inniheldur líkansvarpanir, munu þær verða afritaðar í nýjar grunnstillingar líkansvörpunar.</span><span class="sxs-lookup"><span data-stu-id="48767-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="48767-151">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="48767-151">Click Designer.</span></span>
8. <span data-ttu-id="48767-152">Í trénu skal velja „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="48767-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="48767-153">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="48767-153">Click Add root.</span></span>
10. <span data-ttu-id="48767-154">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="48767-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="48767-155">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="48767-155">Company</span></span>  
11. <span data-ttu-id="48767-156">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="48767-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="48767-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="48767-157">CompanyInfo</span></span>  
12. <span data-ttu-id="48767-158">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-158">Click OK.</span></span>
13. <span data-ttu-id="48767-159">Útvíkka, í trénu „Fyrirtæki“.</span><span class="sxs-lookup"><span data-stu-id="48767-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="48767-160">Í trénu skal víkka út „Fyrirtæki\finna()“.</span><span class="sxs-lookup"><span data-stu-id="48767-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="48767-161">Í trénu skal velja „Fyrirtæki\finna()\Nafn“.</span><span class="sxs-lookup"><span data-stu-id="48767-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="48767-162">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="48767-162">Click Bind.</span></span>
17. <span data-ttu-id="48767-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="48767-163">Click Save.</span></span>
18. <span data-ttu-id="48767-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-164">Close the page.</span></span>
19. <span data-ttu-id="48767-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-165">Close the page.</span></span>
20. <span data-ttu-id="48767-166">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="48767-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="48767-167">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="48767-167">Click User parameters.</span></span>
22. <span data-ttu-id="48767-168">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="48767-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="48767-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-169">Click OK.</span></span>
24. <span data-ttu-id="48767-170">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="48767-170">Click Edit.</span></span>
25. <span data-ttu-id="48767-171">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="48767-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="48767-172">Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="48767-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="48767-173">Veljið „Sýnigagnalíkan“, í trénu.</span><span class="sxs-lookup"><span data-stu-id="48767-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="48767-174">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="48767-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="48767-175">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani Sýnigagnalíkan“.</span><span class="sxs-lookup"><span data-stu-id="48767-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="48767-176">Í svæðið Heiti, færðu inn „Sýnisnið“.</span><span class="sxs-lookup"><span data-stu-id="48767-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="48767-177">Sýnisnið</span><span class="sxs-lookup"><span data-stu-id="48767-177">Sample format</span></span>  
5. <span data-ttu-id="48767-178">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="48767-178">Click Create configuration.</span></span>
6. <span data-ttu-id="48767-179">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="48767-179">Click Designer.</span></span>
7. <span data-ttu-id="48767-180">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="48767-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="48767-181">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="48767-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="48767-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-182">Click OK.</span></span>
10. <span data-ttu-id="48767-183">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="48767-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="48767-184">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="48767-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="48767-185">Í trénu skal velja „líkan\Fyrirtæki“.</span><span class="sxs-lookup"><span data-stu-id="48767-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="48767-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="48767-186">Click Bind.</span></span>
14. <span data-ttu-id="48767-187">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="48767-187">Click Save.</span></span>
15. <span data-ttu-id="48767-188">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-188">Close the page.</span></span>
    * <span data-ttu-id="48767-189">Keyrið drög að útgáfu sniðsins sem þegar hefur verið stofnað til prufu.</span><span class="sxs-lookup"><span data-stu-id="48767-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="48767-190">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="48767-190">Click Run.</span></span>
    * <span data-ttu-id="48767-191">Á Útgáfur flýtiflipa, smellið á Keyra.</span><span class="sxs-lookup"><span data-stu-id="48767-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="48767-192">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-192">Click OK.</span></span>
    * <span data-ttu-id="48767-193">Yfirfara úttakið sem inniheldur heiti fyrirtækisins sem notandinn, sem er að keyra þessa grunnstillingu sniðs, er skráður inn á.</span><span class="sxs-lookup"><span data-stu-id="48767-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="48767-194">Athugið að áður stofnuð grunnstilling líkansvörpunar er notað af þessari grunnstillingu sniðs vegna þess að það er aðeins ein grunnstilling tiltæk sem inniheldur þær líkansvarpanir sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="48767-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="48767-195">Bæta við annarri grunnstillingu fyrir líkan vörpun í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="48767-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="48767-196">Veljið „Sýnigagnalíkan“, í trénu.</span><span class="sxs-lookup"><span data-stu-id="48767-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="48767-197">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="48767-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="48767-198">Í svæði Nýtt skal slá inn „Vörpun líkans byggð á gagnalíkani Sýnigagnalíkani“.</span><span class="sxs-lookup"><span data-stu-id="48767-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="48767-199">Í svæðið Heiti, færðu inn „Sýnivörpun (valkostur)“.</span><span class="sxs-lookup"><span data-stu-id="48767-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="48767-200">Sýnivörpun (valkostur)</span><span class="sxs-lookup"><span data-stu-id="48767-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="48767-201">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="48767-201">Click Create configuration.</span></span>
6. <span data-ttu-id="48767-202">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="48767-202">Click Designer.</span></span>
7. <span data-ttu-id="48767-203">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="48767-203">Click Designer.</span></span>
8. <span data-ttu-id="48767-204">Í trénu skal velja „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="48767-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="48767-205">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="48767-205">Click Add root.</span></span>
10. <span data-ttu-id="48767-206">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="48767-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="48767-207">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="48767-207">Company</span></span>  
11. <span data-ttu-id="48767-208">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="48767-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="48767-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="48767-209">CompanyInfo</span></span>  
12. <span data-ttu-id="48767-210">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-210">Click OK.</span></span>
13. <span data-ttu-id="48767-211">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="48767-211">Click Edit.</span></span>
14. <span data-ttu-id="48767-212">Veljið 'String\CONCATENATE', í trénu.</span><span class="sxs-lookup"><span data-stu-id="48767-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="48767-213">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="48767-213">Click Add function.</span></span>
16. <span data-ttu-id="48767-214">Útvíkka, í trénu „Fyrirtæki“.</span><span class="sxs-lookup"><span data-stu-id="48767-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="48767-215">Í trénu skal víkka út „Fyrirtæki\finna()“.</span><span class="sxs-lookup"><span data-stu-id="48767-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="48767-216">Í trénu skal velja „Fyrirtæki\finna()\Nafn“.</span><span class="sxs-lookup"><span data-stu-id="48767-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="48767-217">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="48767-217">Click Add data source.</span></span>
20. <span data-ttu-id="48767-218">Í reitinn Formúla skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="48767-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="48767-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="48767-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="48767-220">Í trénu skal velja „Fyrirtæki\finna()\Fyrirtæki(DataArea)“.</span><span class="sxs-lookup"><span data-stu-id="48767-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="48767-221">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="48767-221">Click Add data source.</span></span>
23. <span data-ttu-id="48767-222">Í reitinn Formúla skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="48767-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="48767-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="48767-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="48767-224">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="48767-224">Click Save.</span></span>
25. <span data-ttu-id="48767-225">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-225">Close the page.</span></span>
26. <span data-ttu-id="48767-226">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="48767-226">Click Save.</span></span>
27. <span data-ttu-id="48767-227">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-227">Close the page.</span></span>
28. <span data-ttu-id="48767-228">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48767-228">Close the page.</span></span>
29. <span data-ttu-id="48767-229">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="48767-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="48767-230">Nota fyrirliggjandi grunnstillingu fyrir líkan vörpun í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="48767-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="48767-231">Veljið „Sýnigagnalíkan/Sýnisnið“, í trénu.</span><span class="sxs-lookup"><span data-stu-id="48767-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="48767-232">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="48767-232">Click Run.</span></span>
    * <span data-ttu-id="48767-233">Athugið að valin útgáfudrög að grunnstillingum sniðs Rafræn skýrslugerð er ekki hægt að framkvæma vegna þess að það eru fleiri en ein grunnstilling líkansvörpunar tiltæk fyrir hið óskilgreinda gagnalíkan sem hefur verið valið sem gagnaveita fyrir snið Rafræn skýrslugerð sem verið er að keyra.</span><span class="sxs-lookup"><span data-stu-id="48767-233">Note that the selected draft version of the ER format configuration can't be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="48767-234">Næst muntu skilgreina aðra grunnstillingu fyrir líkansvörpun, sem þá sem líkansvarpanir verða notaðar sem gagnaveitur fyrir, fyrir keyrslu sniðs Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="48767-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="48767-235">Veljið „Sýnigagnalíkan/Sýnivörpun (valkostur)“, í trénu.</span><span class="sxs-lookup"><span data-stu-id="48767-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="48767-236">Veljið Já í „Sjálfgefið fyrir líkanavörpun“.</span><span class="sxs-lookup"><span data-stu-id="48767-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="48767-237">Veljið „Sýnigagnalíkan/Sýnisnið“, í trénu.</span><span class="sxs-lookup"><span data-stu-id="48767-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="48767-238">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="48767-238">Click Run.</span></span>
7. <span data-ttu-id="48767-239">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="48767-239">Click OK.</span></span>
    * <span data-ttu-id="48767-240">Athugið að sjálfgefin grunnstilling líkansvörpunar er notuð af þessari grunnstillingu sniðs til að búa til rafræn skjöl (úttakið sem þegar hefur verið stofnað inniheldur fyrirtækjakóðann).</span><span class="sxs-lookup"><span data-stu-id="48767-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

