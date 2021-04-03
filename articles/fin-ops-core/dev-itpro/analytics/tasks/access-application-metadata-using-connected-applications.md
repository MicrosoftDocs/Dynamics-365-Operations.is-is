---
title: Aðgangur að lýsigögnum forrits með tengdum forritum
description: Skrefin í þessu efnisatriði útskýra hvernig notandi Regulatory Configuration Service getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með notkun á lýsigögnunum.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0a769bdc86d36f8c5373c0301ed55f26757b405
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562905"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="1b541-103">Aðgangur að lýsigögnum forrits með tengdum forritum</span><span class="sxs-lookup"><span data-stu-id="1b541-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b541-104">Eftirfarandi skref útskýra hvernig notandi Regulatory Configuration Service í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með því að nota lýsigögnin í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b541-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="1b541-105">Lýsigögn hugbúnaðar verða skoðuð á netinu með því að nota RCS -tengda forritið.</span><span class="sxs-lookup"><span data-stu-id="1b541-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="1b541-106">Dæmi um líkanavörpun rafrænnar skýrslugerðar verður skilgreint til að fá aðgang að utanríkisviðskiptafærslum.</span><span class="sxs-lookup"><span data-stu-id="1b541-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="1b541-107">Til að ljúka þessum skrefum verður í RCS fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1b541-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="1b541-108">Ef þú hefur ekki lokið við skrefin í efninu [Fáðu aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar](access-application-metadata-er-configuration.md), skaltu fara í [Síðu með dæmum um rafræna skýrslugerð](https://go.microsoft.com/fwlink/?linkid=862266) til að sækja og vista eftirfarandi skilgreiningar rafrænnar skýrslugerðar: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, og ljúka síðan við skrefin í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="1b541-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1b541-109">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="1b541-109">Prerequisites</span></span>
1. <span data-ttu-id="1b541-110">Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="1b541-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="1b541-111">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="1b541-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1b541-112">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1b541-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="1b541-113">Sækja umbeðnar ER-skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="1b541-113">Get required ER configurations</span></span>
1. <span data-ttu-id="1b541-114">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="1b541-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="1b541-115">Ef þú hefur þegar lokið við skrefin í ferlinu [Fá aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar](access-application-metadata-er-configuration.md) hefurðu nú þegar allar nauðsynlegar skilgreiningar rafrænnar skýrslugerðar (skilgreiningar lýsigagna utanríkisviðskipta, líkans og vörpunar) í gildandi RCS-tilviki.</span><span class="sxs-lookup"><span data-stu-id="1b541-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="1b541-116">Þú getur sleppt öllum eftirstandandi skrefum í þessu undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="1b541-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="1b541-117">Smelltu á **Skipta út**.</span><span class="sxs-lookup"><span data-stu-id="1b541-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="1b541-118">Smelltu á **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="1b541-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="1b541-119">Smelltu á **Skoða** og veldu skrána **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="1b541-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="1b541-120">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b541-120">Click **OK**.</span></span> 
7. <span data-ttu-id="1b541-121">Smelltu á **Skipta út**.</span><span class="sxs-lookup"><span data-stu-id="1b541-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="1b541-122">Smelltu á **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="1b541-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="1b541-123">Smelltu á **Skoða** og veldu skrána **Foreign trade model.xml**.</span><span class="sxs-lookup"><span data-stu-id="1b541-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="1b541-124">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b541-124">Click **OK**.</span></span> 
11. <span data-ttu-id="1b541-125">Smelltu á **Skipta út**.</span><span class="sxs-lookup"><span data-stu-id="1b541-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="1b541-126">Smelltu á **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="1b541-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="1b541-127">Smelltu á **Skoða** og veldu skrána **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="1b541-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="1b541-128">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b541-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="1b541-129">Skráðu tengdan hugbúnað</span><span class="sxs-lookup"><span data-stu-id="1b541-129">Register a connected application</span></span>
1. <span data-ttu-id="1b541-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-130">Close the page.</span></span> 
2. <span data-ttu-id="1b541-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-131">Close the page.</span></span> 
3. <span data-ttu-id="1b541-132">Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="1b541-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="1b541-133">Smelltu á **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="1b541-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="1b541-134">Gakktu úr skugga um að skilgreint forrit sé byggt á Azure og aðgengilegt fyrir núverandi notanda RCS.</span><span class="sxs-lookup"><span data-stu-id="1b541-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="1b541-135">Þess er einnig krafist að núverandi RCS-notandi hafi aðgang að völdu forriti og hafi verið skráður sem notandi þessa forrits sem sér um að veita réttindi til að fá aðgang að lýsigögnum forritsins.</span><span class="sxs-lookup"><span data-stu-id="1b541-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="1b541-136">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="1b541-136">Click **New**.</span></span> 
7. <span data-ttu-id="1b541-137">Í reitinn **Heiti** slærðu inn „MyConnectedApp“.</span><span class="sxs-lookup"><span data-stu-id="1b541-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="1b541-138">Í reitinn **Forrit** slærðu inn „https:// mycompany.operations.dynamics.com“.</span><span class="sxs-lookup"><span data-stu-id="1b541-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="1b541-139">Í reitinn **Leigjandi** „slærðu inn mycompany.onmicrosoft.com“.</span><span class="sxs-lookup"><span data-stu-id="1b541-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="1b541-140">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="1b541-140">Click **Save**.</span></span> 
11. <span data-ttu-id="1b541-141">Þegar þú skoðar tengingu við skilgreint forrit skaltu á síðunni **Tengja við ytra forrit** smella á tengilinn **Smellta hér til að tengja við valið ytra forrit**.</span><span class="sxs-lookup"><span data-stu-id="1b541-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="1b541-142">Smelltu á **Athuga tengingu**.</span><span class="sxs-lookup"><span data-stu-id="1b541-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="1b541-143">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="1b541-143">Click **Close**.</span></span> 
14. <span data-ttu-id="1b541-144">Þegar tengingarvottun hefur tekist verða upplýsingar um útgáfu og leigjendur uppfærðar fyrir skilgreind forrit í núverandi hnitaneti.</span><span class="sxs-lookup"><span data-stu-id="1b541-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="1b541-145">Yfirfara fyrirliggjandi skilgreiningu fyrir líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="1b541-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="1b541-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-146">Close the page.</span></span> 
2. <span data-ttu-id="1b541-147">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="1b541-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="1b541-148">Í trénu útvíkkarðu **Líkan utanríkisverslunar**.</span><span class="sxs-lookup"><span data-stu-id="1b541-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="1b541-149">Í trénu skaltu velja **Líkan utanríkisviðskipta\Vörpun utanríkisviðskipta**.</span><span class="sxs-lookup"><span data-stu-id="1b541-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="1b541-150">Stækkaðu hlutann **Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="1b541-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1b541-151">Eins og er vísar þessi vörpun í skilgreiningu lýsigagna.</span><span class="sxs-lookup"><span data-stu-id="1b541-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="1b541-152">Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan verið er að setja þessa líkanavörpun upp.</span><span class="sxs-lookup"><span data-stu-id="1b541-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="1b541-153">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="1b541-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="1b541-154">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="1b541-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="1b541-155">Í trénu velurðu **Dynamics 365 for Operations\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="1b541-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="1b541-156">Smelltu á **Bæta rót við**.</span><span class="sxs-lookup"><span data-stu-id="1b541-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="1b541-157">Sláið inn eða veldu gildi í reitnum **Tafla**.</span><span class="sxs-lookup"><span data-stu-id="1b541-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1b541-158">Eins og er vísar þessi vörpun í skilgreiningu lýsigagna.</span><span class="sxs-lookup"><span data-stu-id="1b541-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="1b541-159">Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan verið er að setja þessa líkanavörpun upp.</span><span class="sxs-lookup"><span data-stu-id="1b541-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="1b541-160">Smelltu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="1b541-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="1b541-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-161">Close the page.</span></span> 
13. <span data-ttu-id="1b541-162">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="1b541-163">Úthluta tengdu forriti á líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="1b541-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="1b541-164">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="1b541-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="1b541-165">Veldu forritið **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="1b541-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1b541-166">Eins og er, vísar þessi vörpun í lýsigögn valins tengds forrits.</span><span class="sxs-lookup"><span data-stu-id="1b541-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="1b541-167">Þegar sama vöpun vísar í lýsigagnaskilgreiningu um leið og tengt forrit verða lýsigögn tengds forrits notuð.</span><span class="sxs-lookup"><span data-stu-id="1b541-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="1b541-168">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="1b541-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="1b541-169">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="1b541-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="1b541-170">Í trénu velurðu **Dynamics 365 for Operations\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="1b541-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="1b541-171">Smelltu á **Bæta rót við**.</span><span class="sxs-lookup"><span data-stu-id="1b541-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="1b541-172">Sláið inn eða veldu gildi í reitnum **Tafla**.</span><span class="sxs-lookup"><span data-stu-id="1b541-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1b541-173">Fleiri en tvær forritstöflur voru boðnar núna þar sem þessi vörpun notar öll lýsigögn tengds forrits sem hefur verið úthlutað fyrir það.</span><span class="sxs-lookup"><span data-stu-id="1b541-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="1b541-174">Smelltu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="1b541-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="1b541-175">Smelltu á **Villuleita**.</span><span class="sxs-lookup"><span data-stu-id="1b541-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1b541-176">Okkur tókst að binda þætti gagnalíkans við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits úr tengdu forriti sem hefue verið úthlutað fyrir þessa vörpun.</span><span class="sxs-lookup"><span data-stu-id="1b541-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="1b541-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-177">Close the page.</span></span> 
11. <span data-ttu-id="1b541-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b541-178">Close the page.</span></span> 

<span data-ttu-id="1b541-179">Þegar þú þarft að meta þessa líkanavörpun með því að nota lýsigögn annarrar útgáfu forrits skaltu skrá annað tengt forrit, úthluta því á þessara líkanavörpun og sannprófa það gegn nýjum lýsigögnum.</span><span class="sxs-lookup"><span data-stu-id="1b541-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]