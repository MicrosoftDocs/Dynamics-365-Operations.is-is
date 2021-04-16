---
title: Staðgreiðsluskattsskýrsla fyrir Egyptaland
description: Þetta efnisatriði útskýrir hvernig á að skilgreina og mynda staðgreiðsluskattsskýrslu fyrir Egyptaland.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839793"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="c273f-103">Staðgreiðsluskattsskýrsla fyrir Egyptaland (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="c273f-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="c273f-104">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c273f-104">Overview</span></span>
<span data-ttu-id="c273f-105">Þetta efnisatriði útskýrir hvernig á að setja upp og mynda staðgreiðsluskattskýrslu og eyðublöð staðgreiðsluskattskýrslu 41 og 11 fyrir lögaðila í Egyptalandi</span><span class="sxs-lookup"><span data-stu-id="c273f-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="c273f-106">Allar egypskar einingar verða að undirbúa eyðublað 41, sem tekur saman alla skatta sem eru varðveittir frá staðbundnum birgjum og þjónustuveitum.</span><span class="sxs-lookup"><span data-stu-id="c273f-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="c273f-107">Til viðbótar við eyðublað 41 verður eyðublað 11 að vera myndað til að gefa upplýsingar um alla varðveitta skatta frá erlendum aðilum.</span><span class="sxs-lookup"><span data-stu-id="c273f-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="c273f-108">Skýrslan **Staðgreiðsluskattsskýrsla** í Dynamics 365 Finance inniheldur eftirfarandi skýrslur:</span><span class="sxs-lookup"><span data-stu-id="c273f-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="c273f-109">Framtalseyðublað nr.</span><span class="sxs-lookup"><span data-stu-id="c273f-109">Declaration form No.</span></span> <span data-ttu-id="c273f-110">41</span><span class="sxs-lookup"><span data-stu-id="c273f-110">41</span></span>
- <span data-ttu-id="c273f-111">Framtalseyðublað nr.</span><span class="sxs-lookup"><span data-stu-id="c273f-111">Declaration form No.</span></span> <span data-ttu-id="c273f-112">11</span><span class="sxs-lookup"><span data-stu-id="c273f-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="c273f-113">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="c273f-113">Prerequisites</span></span>
<span data-ttu-id="c273f-114">Aðalaðsetur lögaðilans verður að vera í Egyptalandi.</span><span class="sxs-lookup"><span data-stu-id="c273f-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="c273f-115">Á vinnusvæðinu **Eiginleikastjórnun** þarf að virkja eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="c273f-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="c273f-116">**Altækur staðgreiðsluskattur**</span><span class="sxs-lookup"><span data-stu-id="c273f-116">**Global withholding tax**</span></span>

<span data-ttu-id="c273f-117">Nánari upplýsingar um hvernig á að virkja eiginleika er að finna í [Yfirlit eiginleikastjórnunar.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c273f-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="c273f-118">Farið í **Skattur** > **Uppsetning** > **Færibreytur** > **Færibreytur fjárhags** og í flipanum **Staðgreiðsluskattur** skal stilla **Virkja altækan staðgreiðsluskatt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c273f-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="c273f-119">Á vinnusvæðinu **Rafræn skýrslugerð** skal flytja inn eftirfarandi snið rafrænnar skýrslugerðar úr gagnageymslunni:</span><span class="sxs-lookup"><span data-stu-id="c273f-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="c273f-120">Staðgreiðsluskattsskýrsla Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="c273f-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="c273f-121">Sniðið hér að ofan er byggt á **Skattskýrslulíkaninu** og notar **Líkanavörpun skattskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="c273f-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="c273f-122">Þessi aukalega skilgreining er sjálfkrafa flutt inn.</span><span class="sxs-lookup"><span data-stu-id="c273f-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="c273f-123">Frekari upplýsingar um hvernig á að flytja inn skilgreiningar rafrænnar skýrslugerðar er að finna í [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="c273f-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="c273f-124">Hlaða niður skilgreiningum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c273f-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="c273f-125">Innleiðing framtalseyðublaða staðgreiðsluskatts fyrir Egyptaland byggir á skilgreiningum rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="c273f-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="c273f-126">Frekari upplýsingar um möguleika og hugmyndir á bak við stillanlega skýrslugerð er að finna í [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c273f-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="c273f-127">Fyrir umhverfi framleiðslu og samþykkisprófun notanda skal fylgja leiðbeiningum í efnisatriðinu [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="c273f-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="c273f-128">Til að búa til staðgreiðsluskattsskýrslur í egypskum lögaðila þarf að hlaða upp eftirfarandi skilgreiningum:</span><span class="sxs-lookup"><span data-stu-id="c273f-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="c273f-129">Tax declaration model.version.82.xml eða nýrri útgáfu</span><span class="sxs-lookup"><span data-stu-id="c273f-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="c273f-130">Tax declaration model mapping.version.82.133.xml eða nýrri útgáfu</span><span class="sxs-lookup"><span data-stu-id="c273f-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="c273f-131">WHT Declaration Excel (EG).version.82.21 eða nýrri útgáfu</span><span class="sxs-lookup"><span data-stu-id="c273f-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="c273f-132">Þegar búið er að hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services (LCS) eða altæku geymslunni skal ljúka eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="c273f-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="c273f-133">Farið á vinnusvæðið **Rafræn skýrslugerð** og veljið reitinn **Skýrsluskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="c273f-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="c273f-134">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út > Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="c273f-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="c273f-135">Hlaðið upp öllum skránum í þeirri röð sem þær eru birtar í fyrri upptalningum.</span><span class="sxs-lookup"><span data-stu-id="c273f-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="c273f-136">Þegar öllum skilgreiningunum hefur verið hlaðið upp ætti skilgreiningatréð að vera til staðar í Finance.</span><span class="sxs-lookup"><span data-stu-id="c273f-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="c273f-137">Setja upp færibreytur tiltekins forrits</span><span class="sxs-lookup"><span data-stu-id="c273f-137">Set up application-specific parameters</span></span>

<span data-ttu-id="c273f-138">Valkostur færibreyta tiltekins forrits gerir notendum kleift að setja á skilyrði um hvernig á að flokka og reikna skattfærslurnar í hverri línu myndaðrar skýrslu eftir því hver skilgreiningin á **vöruflokki staðgreiðsluskatts** er eða önnur skilyrði sem gefin eru upp í skilgreiningu uppflettingarinnar.</span><span class="sxs-lookup"><span data-stu-id="c273f-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="c273f-139">Eyðublað staðgreiðsluskatts nr 41 inniheldur ákveðinn dálk þar sem staðgreiðsluskattsfærslan verður að vera flokkuð í samræmi við flokkun skattyfirvala sem heitir **Gerð afsláttarkóða**.</span><span class="sxs-lookup"><span data-stu-id="c273f-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="c273f-140">Í stað þess að taka þessar nýju flokkanir sem ný innsláttargögn þegar færslurnar eru bókaðar munu flokkanirnar verða ákvarðaðar samkvæmt mismunandi uppflettingum sem kynntar eru í **Skilgreiningar** > **Setja upp færibreytur tiltekins forrits** > **Uppsetning** til að uppfylla kröfur staðgreiðsluskýrslna fyrir Egyptaland.</span><span class="sxs-lookup"><span data-stu-id="c273f-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="c273f-141">Eftirfarandi skilgreining er notuð til að flokka færslurnar í skýrslu staðgreiðslueyðublaðs 41:</span><span class="sxs-lookup"><span data-stu-id="c273f-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="c273f-142">**DiscountTaxTypeLookup**-> dálkur nr 18</span><span class="sxs-lookup"><span data-stu-id="c273f-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="c273f-143">Ljúkið eftirfarandi skrefum til að setja upp mismunandi uppflettingar sem notaðar eru til að mynda staðgreiðsluskattsskýrslu og tengdar skýrslur bóka.</span><span class="sxs-lookup"><span data-stu-id="c273f-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="c273f-144">Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar** > **Uppsetning** til að setja upp reglurnar til að gera grein fyrir hvernig færslur eru flokkaðar í staðgreiðsluskattsskýrslum.</span><span class="sxs-lookup"><span data-stu-id="c273f-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="c273f-145">Veljið núverandi útgáfu og í flýtiflipanum **Uppflettingar** skal velja heiti uppflettingar.</span><span class="sxs-lookup"><span data-stu-id="c273f-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="c273f-146">Til dæmis **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="c273f-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="c273f-147">Þessi uppfletting auðkennir lista yfir afsláttargerðir sem skattyfirvöld krefjast.</span><span class="sxs-lookup"><span data-stu-id="c273f-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="c273f-148">Í flýtiflipanum **Skilyrði** skal velja **Bæta við** og í nýju línunni í dálknum **Niðurstaða uppflettingar** skal velja tengda línu sem stendur fyrir flokkunina í **Dálki 18**.</span><span class="sxs-lookup"><span data-stu-id="c273f-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="c273f-149">Í dálknum **Vöruflokkur staðgreiðsluskatts** skal velja viðeigandi kóða sem er notaður til að auðkenna flokkunina.</span><span class="sxs-lookup"><span data-stu-id="c273f-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="c273f-150">Til dæmis **Leyfður afsláttur**.</span><span class="sxs-lookup"><span data-stu-id="c273f-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="c273f-151">Endurtakið skref 3 og 4 fyrir tiltækar uppflettingar.</span><span class="sxs-lookup"><span data-stu-id="c273f-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="c273f-152">Veljið aftur **Bæta við** til að taka með síðustu færslulínuna og í dálknum **Niðurstaða uppflettingar** skal velja **Á ekki við**.</span><span class="sxs-lookup"><span data-stu-id="c273f-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="c273f-153">Í dálkunum sem eftir eru skal velja **Ekki autt**.</span><span class="sxs-lookup"><span data-stu-id="c273f-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="c273f-154">Setja upp færibreytur fyrir Fjárhag</span><span class="sxs-lookup"><span data-stu-id="c273f-154">Set up General ledger parameters</span></span>

<span data-ttu-id="c273f-155">Til að mynda skýrslur VSK-framtalseyðublaðs í Microsoft Excel skal skilgreina snið rafrænnar skýrslugerðar á síðunni **Færibreytur fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="c273f-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="c273f-156">Farið í **Skattur** > **Uppsetning** > **Færibreytur fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="c273f-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="c273f-157">Í flipanum **Staðgreiðsluskattur**, í reitnum **Vörpun skýrslusniðs fyrir staðgreiðsluskatt**, skal velja **Staðgreiðsluskattsskýrsla Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="c273f-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="c273f-158">Ef reiturinn er skilinn eftir auður verður stöðluð VSK-skýrsla búin til á SSRS-sniði.</span><span class="sxs-lookup"><span data-stu-id="c273f-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Framtalseyðublað](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="c273f-160">Mynda eyðublöð staðgreiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="c273f-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="c273f-161">Ferlið við að undirbúa og senda inn eyðublað staðgreiðsluskýrslu fyrir tiltekið tímabil er byggt á staðgreiðsluskattsfærslum sem bókaðar eru við uppgjörs- og bókunarvinnu skattgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="c273f-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="c273f-162">Frekari upplýsingar um altækan staðgreiðsluskatt er að finna í [Altækur staðgreiðsluskattur](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c273f-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="c273f-163">Ljúkið eftirfarandi skrefum til að mynda skattskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="c273f-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="c273f-164">Farið í **Skattur** > **Skattframtöl** > **Staðgreiðsluskattur** > \**Greiðsla staðgreiðsluskatts*.</span><span class="sxs-lookup"><span data-stu-id="c273f-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="c273f-165">Veljið jöfnunartímabilið og veljið síðan upphafsdagsetningu fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="c273f-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="c273f-166">Færið inn færsludagsetningu og veljið svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c273f-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="c273f-167">Í svarglugganum sem opnast skal velja eina eða fleiri gerðir eyðublaðs \*\*Eyðublað nr. 41 \*\*, **Eyðublað nr. 11**, eða **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="c273f-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="c273f-168">Ef **Ekkert** er valið mun stöðluð skýrsla vera búin til.</span><span class="sxs-lookup"><span data-stu-id="c273f-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="c273f-169">Veljið tungumálið.</span><span class="sxs-lookup"><span data-stu-id="c273f-169">Select the language.</span></span> <span data-ttu-id="c273f-170">Allar skýrslur eru þýddar á **en-us** og **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="c273f-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="c273f-171">Færið inn útibú og heiti bankans þar sem skattgreiðslan verður innt af hendi.</span><span class="sxs-lookup"><span data-stu-id="c273f-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="c273f-172">Veljið tegund viðskipta og sláið svo inn ávísun og skjalanúmer.</span><span class="sxs-lookup"><span data-stu-id="c273f-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="c273f-173">Færið inn einingagerðina.</span><span class="sxs-lookup"><span data-stu-id="c273f-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="c273f-174">Færið inn heiti einstaklingsins sem skráður er fyrir því að úthluta eyðublaðinu og veljið **Í lagi** til að staðfesta myndun skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="c273f-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
