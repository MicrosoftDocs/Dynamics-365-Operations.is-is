---
title: Nota kennslu fyrir Regression Suite Automation Tool
description: Þetta efni sýnir hvernig á að nota Regression Suite Automation Tool (RSAT). Það lýsir ýmsum eiginleikum og gefur dæmi sem nota ítarlegar forskriftir.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070821"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="ea70c-104">Notaðu kennsluefni fyrir Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="ea70c-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ea70c-105">Notaðu verkfæri þín í internetvafranum til að sækja og vista þessa síðu á pdf-sniði.</span><span class="sxs-lookup"><span data-stu-id="ea70c-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="ea70c-106">Þetta kennsluefni fer í gegnum nokkra ítarlega eiginleika Regression Suite Automation Tool (RSAT), inniheldur sýniúthlutun og lýsir stefnu og lykilatriðum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="ea70c-107">Eiginleikar RSAT/verkskráningar</span><span class="sxs-lookup"><span data-stu-id="ea70c-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="ea70c-108">Villuleita reitargildi</span><span class="sxs-lookup"><span data-stu-id="ea70c-108">Validate a field value</span></span>

<span data-ttu-id="ea70c-109">Nánari upplýsingar um þennan eiginleika er að finna í [Stofna nýja verkskráningu sem hefur staðfestingaraðgerð](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="ea70c-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="ea70c-110">Vistuð breyta</span><span class="sxs-lookup"><span data-stu-id="ea70c-110">Saved variable</span></span>

<span data-ttu-id="ea70c-111">Nánari upplýsingar um þennan eiginleika er að finna í [Breyta núverandi verkskráningu til að búa til vistað breytu](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="ea70c-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="ea70c-112">Afleitt prófunardæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-112">Derived test case</span></span>

1. <span data-ttu-id="ea70c-113">Opnaðu Regression Suite Automation Tool (RSAT) og veldu bæði prófunardæmin sem þú stofnaðir í kennsluefninu [Setja upp Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="ea70c-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="ea70c-114">Veldu **Nýtt \> Stofna afleitt prófunardæmi**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-114">Select **New \> Create derived test case**.</span></span>

    ![Stofna afleidda prófunardæmisskipun í valmyndinni Nýtt](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="ea70c-116">Þú færð skilaboð sem kveða á um að stofnað verði prófunardæmi fyrir hvert valið prófunardæmi í núverandi prófunarpakka og að hvert afleidd prófunardæmi muni hafa eigið afrit af Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="ea70c-117">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea70c-118">Þegar þú keyrir afleidd prófunardæmi notar það verkskráningu yfirprófunardæmis og eigið afrit af Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="ea70c-119">Þannig geturðu keyrt sama prófið með mismunandi færibreytum, án þess að þurfa að viðhalda fleiri en einni verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="ea70c-120">Afleitt prófunardæmi þarf ekki að vera hluti af sama prófunarpakka og yfirprófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Skilaboðagluggi](./media/use_rsa_tool_02.png)

    <span data-ttu-id="ea70c-122">Tvö afleidd prófunardæmi eru stofnuð og hakreiturinn **Afleidd?** er valinn fyrir þau.</span><span class="sxs-lookup"><span data-stu-id="ea70c-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Afleidd prófunardæmi stofnuð](./media/use_rsa_tool_03.png)

    <span data-ttu-id="ea70c-124">Afleidd prófunardæmi eru sjálfvirkt stofnuð í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ea70c-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="ea70c-125">Það er undiratriði í prófunardæminu **Stofna nýja afurð** og er merkt með sérstöku lykilorði: **RSAT: DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="ea70c-126">Þessum prófunardæmum er einnig sjálfkrafa bætt við prófunaráætlunina í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ea70c-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Lykilorðið RSAT: DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="ea70c-128">Ef afleidd prófunardæmi sem eru af einhverjum ástæðum stofnuð eru ekki í réttri röð, skaltu fara í Azure DevOps og endurraða prófdæmunum í prófunarpakkanum, þannig að RSAT geti keyrt þau í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="ea70c-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="ea70c-129">Veldu aðeins afleidd prófunardæmi og veldu síðan **Breyta** til að opna samsvarandi Excel-færibreytuskrár.</span><span class="sxs-lookup"><span data-stu-id="ea70c-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="ea70c-130">Breyttu þessum Excel-færibreytuskrám á sama hátt og þú breyttir yfirskránum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="ea70c-131">Með öðrum orðum skaltu ganga úr skugga um að afurðakennið sé stillt þannig að það sé sjálfkrafa myndað.</span><span class="sxs-lookup"><span data-stu-id="ea70c-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="ea70c-132">Passaðu einnig að vistuð breyta sé afrituð í viðeigandi reiti.</span><span class="sxs-lookup"><span data-stu-id="ea70c-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="ea70c-133">Á flipanum **Almennt** í báðum Excel-færibreytuskránum skaltu uppfæra gildi reitsins **Fyrirtæki** í **USSI**, þannig að afleidd prófunardæmi verði keyrð gegn öðrum lögaðila en yfirprófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="ea70c-134">Til að keyra prófdæmin gegn ákveðnum notanda (eða hlutverki sem tengist ákveðnum notanda) getur þú uppfært gildi reitsins **Prófa notanda**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="ea70c-135">Veldu **Keyra** og sannreyndu að afurðin sé stofnuð bæði í USMF-lögaðilanum og USSI-lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="ea70c-136">Sannprófa tilkynningar</span><span class="sxs-lookup"><span data-stu-id="ea70c-136">Validate notifications</span></span>

<span data-ttu-id="ea70c-137">Þennan eiginleika er hægt að nota til að staðfesta hvort aðgerð hafi átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="ea70c-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="ea70c-138">Til dæmis, þegar framleiðslupöntun er stofnuð, áætluð og síðan hafin sýnir forritið skilaboðin „Production - Start“ til að tilkynna þér að framleiðslupöntun hafi verið hafin.</span><span class="sxs-lookup"><span data-stu-id="ea70c-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Framleiðsla – Ræsa tilkynningu](./media/use_rsa_tool_05.png)

<span data-ttu-id="ea70c-140">Þú getur valið þessi skilaboð í gegnum RSAT með því að slá inn skilaboðartexta á flipann **MessageValidation** í Excel-færibreytuskránni fyrir viðeigandi skráningu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Flipinn Sannprófun skilaboða](./media/use_rsa_tool_06.png)

<span data-ttu-id="ea70c-142">Þegar prófunardæmið hefur verið keyrt eru skilaboðin í Excel-færibreytuskránni borin saman við skilaboðin sem birtast.</span><span class="sxs-lookup"><span data-stu-id="ea70c-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="ea70c-143">Ef skilaboðin stemma ekki mun prófunardæmið ekki takast.</span><span class="sxs-lookup"><span data-stu-id="ea70c-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="ea70c-144">Þú getur slegið inn fleiri en eina skilaboð á flipann **MessageValidation** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="ea70c-145">Skilaboðin geta einnig verið villuboð eða viðvörunarboð í stað upplýsingaboða.</span><span class="sxs-lookup"><span data-stu-id="ea70c-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="ea70c-146">Staðfesta gildi með því að nota virkja</span><span class="sxs-lookup"><span data-stu-id="ea70c-146">Validate values by using operators</span></span>

<span data-ttu-id="ea70c-147">Í fyrri útgáfum af RSAT var aðeins hægt að sannprófa gildi ef eftirlitsgildi jafngild áætluðu gildi.</span><span class="sxs-lookup"><span data-stu-id="ea70c-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="ea70c-148">Hinn nýi eiginleiki gerir þér kleift að staðfesta að breyta sé ekki jafnt og, sé minna en eða meira en tilgreint gildi.</span><span class="sxs-lookup"><span data-stu-id="ea70c-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="ea70c-149">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="ea70c-150">Í Excel-færibreytuskránni birtist nýi reiturinn **Virki**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea70c-151">Ef þú hefur verið að nota eldri útgáfu af RSAT verður þú að búa til nýjar Excel-færibreytuskrár.</span><span class="sxs-lookup"><span data-stu-id="ea70c-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Reiturinn Virki](./media/use_rsa_tool_07.png)

<span data-ttu-id="ea70c-153">Eftirfarandi dæmi sýnir hvernig hægt er að nota þennan eiginleika til að sannreyna hvort lagerbirgðir séu meiri en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="ea70c-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="ea70c-154">Í kynningargögnum í fyrirtækinu **USMF** skaltu stofna verkskráningu sem er með eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="ea70c-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="ea70c-155">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="ea70c-156">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="ea70c-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea70c-157">Til dæmis sía gildið í reitnum **1000** fyrir reitinn **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="ea70c-158">Veldu **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="ea70c-159">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="ea70c-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea70c-160">Til dæmis, sía á gildinu **1** fyrir reitinn **Vefsvæði**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="ea70c-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="ea70c-162">Sannprófaðu að gildi reitsins **Samtals magn til ráðstöfunar** sé **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="ea70c-163">Vistaðu verkskráninguna í BPM-safnið í LCS og samstilltu það við Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ea70c-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="ea70c-164">Bættu prófunardæminu við prófunaráætlunina og settu prófunardæmið í RSAT.</span><span class="sxs-lookup"><span data-stu-id="ea70c-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="ea70c-165">Opnaðu Excel-færibreytuskrána.</span><span class="sxs-lookup"><span data-stu-id="ea70c-165">Open the Excel parameter file.</span></span> <span data-ttu-id="ea70c-166">Á flipanum **InventOnhandItem** muntu sjá hlutann **Staðfesta InventOnhandItem** sem inniheldur reitinn **Virki**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Reiturinn Virki](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="ea70c-168">Til að sannreyna hvort birgðir á lager verði alltaf meiri en 0 skaltu breyta gildi reitsins **Gildi** úr **411** í **0** og gildi reitsins **Virki** úr samasemmerki (**=**) í meiraenmerki (**\>**).</span><span class="sxs-lookup"><span data-stu-id="ea70c-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Gildum reitanna Gildi og Virki breytt](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="ea70c-170">Vistaðu og lokaðu Excel-færibreytskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="ea70c-171">Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ea70c-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="ea70c-172">Nú, ef gildi reitsins **Samtals magn til ráðstöfunar** fyrir tilgreint atriði í birgðum er meira en 0 (núll), prófanir munu standast, óháð raunverulegu gildi lagerbirgða.</span><span class="sxs-lookup"><span data-stu-id="ea70c-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="ea70c-173">Kladdar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="ea70c-173">Generator logs</span></span>

<span data-ttu-id="ea70c-174">Þessi eiginleiki býr til möppu sem inniheldur kladdana í prófunardæmunum sem hafa verið keyrð.</span><span class="sxs-lookup"><span data-stu-id="ea70c-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="ea70c-175">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="ea70c-176">Þegar prófunardæmin hafa verið keyrð geturðu fundið kladdaskrárnar undir **C:\\Notendur\\\<Notendanafn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Mappan GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="ea70c-178">Ef það voru til staðar prófunardæmi áður en þú breyttir gildinu í .config-skránni verða kladdar ekki myndaðir fyrir þessi prófdæmi fyrr en þú myndar nýjar prófunarkeyrsluskrár.</span><span class="sxs-lookup"><span data-stu-id="ea70c-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Skipunin Mynda textakeyrsluskrár í valmyndinni Nýtt](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="ea70c-180">Skyndimynd</span><span class="sxs-lookup"><span data-stu-id="ea70c-180">Snapshot</span></span>

<span data-ttu-id="ea70c-181">Þessi eiginleiki tekur skjámyndir af þeim skrefum sem voru gerð meðan á verkskráningu stóð.</span><span class="sxs-lookup"><span data-stu-id="ea70c-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="ea70c-182">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="ea70c-183">Undir **C:\\Notendur\\\<Notendanafn\>\\AppData\\Roaming\\regressionTool\\playback**, sérstakri möppu er stofnuð fyrir hvert prófunardæmi sem er keyrt.</span><span class="sxs-lookup"><span data-stu-id="ea70c-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Mappan Skyndimynd fyrir prófunardæmi](./media/use_rsa_tool_12.png)

<span data-ttu-id="ea70c-185">Í sérhverri af þessum möppum er hægt að finna skyndimyndir af þeim skrefum sem voru gerð meðan prófunardæmin voru keyrð.</span><span class="sxs-lookup"><span data-stu-id="ea70c-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Skyndimyndaskrár](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="ea70c-187">Verkefni</span><span class="sxs-lookup"><span data-stu-id="ea70c-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="ea70c-188">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="ea70c-188">Scenario</span></span>

1. <span data-ttu-id="ea70c-189">Vöruhönnuður stofnar nýja útgefna vöru.</span><span class="sxs-lookup"><span data-stu-id="ea70c-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="ea70c-190">Framleiðslustjóri setur framleiðslufyrirmæli af stað til að koma birgðastigi í tvær einingar.</span><span class="sxs-lookup"><span data-stu-id="ea70c-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="ea70c-191">Framleiðsla byrjar og endar framleiðslupöntunina og staðfestir að magnið í lagerbirgðum sé tvær einingar.</span><span class="sxs-lookup"><span data-stu-id="ea70c-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="ea70c-192">Söluhópurinn fær pöntun um fjögur stykki af nýrri afurð.</span><span class="sxs-lookup"><span data-stu-id="ea70c-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="ea70c-193">Þess vegna uppfærir söluhópurinn nettóþarfirnar í gegnum kviku áætlunina.</span><span class="sxs-lookup"><span data-stu-id="ea70c-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="ea70c-194">Þar sem engin viðbótargeta er til staðar er sjálfgefin pöntunarregla stillt á „kaupa í stað þess að búa til“.</span><span class="sxs-lookup"><span data-stu-id="ea70c-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="ea70c-195">Þess vegna er innkaupatillaga stofnuð.</span><span class="sxs-lookup"><span data-stu-id="ea70c-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="ea70c-196">Kaupandi bætir við lánardrottni, staðfestir áætlaða innkaupapöntun og staðfestir síðan innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="ea70c-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="ea70c-197">Þegar vörurnar sem voru keyptar koma í verslunina leitar verslunarrekandinn að viðkomandi innkaupapöntun og tekur á móti vörunum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="ea70c-198">Þar sem pöntuninni hefur nú verið lokið er hægt að taka vörurnar til og pakka á móti sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="ea70c-199">Fjármál birta innkaupareikning og sölureikning.</span><span class="sxs-lookup"><span data-stu-id="ea70c-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="ea70c-200">Eftirfarandi mynd sýnir flæðið fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="ea70c-200">The following illustration shows the flow for this scenario.</span></span>

![Flæði fyrir kynningaraðstæður](./media/use_rsa_tool_14.png)

<span data-ttu-id="ea70c-202">Eftirfarandi mynd sýnir viðskiptaferlin fyrir þessar aðstæður í RSAT.</span><span class="sxs-lookup"><span data-stu-id="ea70c-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Viðskiptaferli fyrir kynningaraðstæður](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="ea70c-204">Stjórnunarstefna – Lykilnám</span><span class="sxs-lookup"><span data-stu-id="ea70c-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="ea70c-205">Gögn</span><span class="sxs-lookup"><span data-stu-id="ea70c-205">Data</span></span>

- <span data-ttu-id="ea70c-206">Passaðu að þú hafir dæmigert gagnamagn (afrit af framleiðslu-/gullgrunnstillingargögnum auk yfirfærðra gagna).</span><span class="sxs-lookup"><span data-stu-id="ea70c-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="ea70c-207">Þegar þú myndar ný gögn í gegnum verkskráningu skaltu stofna prófunarheiti sem munu ekki rekast á við fyrirliggjandi heiti (t.d. nota forskeyti eins og **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="ea70c-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="ea70c-208">Notaðu endurheimt Azure Point-In-Time til að endurkeyra prófanir í umhverfi sem ekki eru í 1. lagi.</span><span class="sxs-lookup"><span data-stu-id="ea70c-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="ea70c-209">Þó að þú getir notað Excel-aðgerðirnar **RANDOM** og **NOW** til að mynda einkvæma samsetningu er framlagið tiltölulega hátt.</span><span class="sxs-lookup"><span data-stu-id="ea70c-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="ea70c-210">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="ea70c-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="ea70c-211">Verkskráning</span><span class="sxs-lookup"><span data-stu-id="ea70c-211">Task recorder</span></span>

- <span data-ttu-id="ea70c-212">Skilgreindu aðstæður áður en þú hefur skráningu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="ea70c-213">Vel stýrt verk er með fyrirframskilgreindar prófunaraðstæður.</span><span class="sxs-lookup"><span data-stu-id="ea70c-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="ea70c-214">Til að byggja upp prófunardæmi skaltu íhuga hversu fyrirsjáanleg niðurstaða þessara prófunaraðstæðna er.</span><span class="sxs-lookup"><span data-stu-id="ea70c-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="ea70c-215">Skiptu skráningum ef þær eru gerðar með mismunandi hlutverkum eða ef það er biðtími eða utanaðkomandi viðburður á undan næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="ea70c-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="ea70c-216">Forðastu að velja gildi í listum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="ea70c-217">Notaðu þess í stað textasnið, til dæmis **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="ea70c-218">Þegar þú velur í lista er staðsetning gildis í listanum skráð, ekki gildið sjálft.</span><span class="sxs-lookup"><span data-stu-id="ea70c-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="ea70c-219">Ef hlutum er bætt við listann getur staðsetning gildisins breyst.</span><span class="sxs-lookup"><span data-stu-id="ea70c-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="ea70c-220">Þess vegna mun skráningin nota aðra færibreytu og afgangurinn af aðstæðunum gæti orðið fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="ea70c-221">Hugsaðu um hegðun fjölnotenda.</span><span class="sxs-lookup"><span data-stu-id="ea70c-221">Think about multi-user behavior.</span></span> <span data-ttu-id="ea70c-222">Til dæmis skaltu ekki gera ráð fyrir að nýstofnuð sölupöntun þín verði alltaf sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="ea70c-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="ea70c-223">Notaðu þess í stað alltaf síuna til að finna réttu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="ea70c-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="ea70c-224">Notaðu virknina Afrita í verkskráningum til að vista heiti nýstofnaðrar afurðar þannig að hægt sé að nota það í keðjuðum prófunardæmum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="ea70c-225">Notaðu virknina Sannprófa í verkskráningunni til að stilla gátstaði sem staðfesta að skref hafi verið keyrð rétt.</span><span class="sxs-lookup"><span data-stu-id="ea70c-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="ea70c-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="ea70c-226">RSAT</span></span>

- <span data-ttu-id="ea70c-227">Til að keyra prófið í öðru fyrirtæki geturðu breytt fyrirtækinu á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ea70c-228">Passaðu að stillingar og gögn séu tiltæk í nýja valda fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="ea70c-229">Þú getur breytt prófnotanda á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ea70c-230">Tilgreindu netfang notandans mun keyra prófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="ea70c-231">Þannig er hægt að keyra prófunardæmið með því að nota öryggisheimildir tiltekins notanda.</span><span class="sxs-lookup"><span data-stu-id="ea70c-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="ea70c-232">Til að bíða áður en prófunin hefst geturðu skilgreint hlé á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ea70c-233">Þetta hlé má nota í runuvinnslu (til dæmis ef keyra þarf verkflæði áður en hægt er að framkvæma næsta skref.)</span><span class="sxs-lookup"><span data-stu-id="ea70c-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="ea70c-234">Ítarlegri forskriftir</span><span class="sxs-lookup"><span data-stu-id="ea70c-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="ea70c-235">CLI</span><span class="sxs-lookup"><span data-stu-id="ea70c-235">CLI</span></span>

<span data-ttu-id="ea70c-236">Hægt er að kalla RSAT úr glugganum **Skipanakvaðning** eða **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="ea70c-237">Staðfestu að umhverfisbreytan **TestRoot** sé stillt á RSAT-uppsetningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="ea70c-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="ea70c-238">(Í Microsoft Windows skaltu opna **Stjórnborð**, velja **Kerfi og öryggi \> Kerfi \> Ítarlegir kerfisstillingar** og velja síðan **Umhverfisbreytur** .)</span><span class="sxs-lookup"><span data-stu-id="ea70c-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="ea70c-239">Opnaðu gluggann **Skipanakvaðning** eða **PowerShell** sem stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="ea70c-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="ea70c-240">Farðu í RSAT uppsetningarskrána.</span><span class="sxs-lookup"><span data-stu-id="ea70c-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="ea70c-241">Listi yfir alla skipanir.</span><span class="sxs-lookup"><span data-stu-id="ea70c-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="ea70c-242">?</span><span class="sxs-lookup"><span data-stu-id="ea70c-242">?</span></span> 
<span data-ttu-id="ea70c-243">Sýnir hjálp um allar tiltækar skipanir og færibreytur þeirra.</span><span class="sxs-lookup"><span data-stu-id="ea70c-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="ea70c-244">Valfrjálsar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="ea70c-245">Hvar ``[command]`` er ein skipan sem tilgreind er hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="ea70c-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="ea70c-246">um</span><span class="sxs-lookup"><span data-stu-id="ea70c-246">about</span></span>
<span data-ttu-id="ea70c-247">Birtir núverandi útgáfu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="ea70c-248">cls</span><span class="sxs-lookup"><span data-stu-id="ea70c-248">cls</span></span>
<span data-ttu-id="ea70c-249">Hreinsar skjáinn.</span><span class="sxs-lookup"><span data-stu-id="ea70c-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="ea70c-250">sækja</span><span class="sxs-lookup"><span data-stu-id="ea70c-250">download</span></span>
<span data-ttu-id="ea70c-251">Sækir viðhengi fyrir tilgreint prófatilfelli í úttaksskrána.</span><span class="sxs-lookup"><span data-stu-id="ea70c-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="ea70c-252">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="ea70c-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea70c-253">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-254">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-254">Required parameters</span></span>
<span data-ttu-id="ea70c-255">**``test_case_id``** táknar kenni próftilfellis.</span><span class="sxs-lookup"><span data-stu-id="ea70c-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ea70c-256">**``output_dir``** táknar úttaksskráarsafnið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea70c-257">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-258">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="ea70c-259">breyta</span><span class="sxs-lookup"><span data-stu-id="ea70c-259">edit</span></span>
<span data-ttu-id="ea70c-260">Gerir þér kleift að opna færibreytuskrá í Excel-forritinu og breyta henni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-261">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-261">Required parameters</span></span>
<span data-ttu-id="ea70c-262">**``excel_file``** Verður að innihalda fulla slóð að núverandi Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="ea70c-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-263">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="ea70c-264">generate</span><span class="sxs-lookup"><span data-stu-id="ea70c-264">generate</span></span>
<span data-ttu-id="ea70c-265">Myndar prófaframkvæmdar- og færibreytuskrár fyrir tilgreint próftilfelli í úttaksskráasafninu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="ea70c-266">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="ea70c-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea70c-267">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-268">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-268">Required parameters</span></span>
<span data-ttu-id="ea70c-269">**``test_case_id``** táknar kenni próftilfellis.</span><span class="sxs-lookup"><span data-stu-id="ea70c-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ea70c-270">**``output_dir``** táknar úttaksskráarsafnið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea70c-271">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-272">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="ea70c-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="ea70c-273">generatederived</span></span>
<span data-ttu-id="ea70c-274">Býr til nýtt prófatilvik, unnið úr gefnu prófatilviki.</span><span class="sxs-lookup"><span data-stu-id="ea70c-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="ea70c-275">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="ea70c-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea70c-276">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-277">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-277">Required parameters</span></span>
<span data-ttu-id="ea70c-278">**``parent_test_case_id``** táknar kenni yfirpróftilfellis.</span><span class="sxs-lookup"><span data-stu-id="ea70c-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="ea70c-279">**``test_plan_id``** táknar kenni prófáætlunar.</span><span class="sxs-lookup"><span data-stu-id="ea70c-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="ea70c-280">**``test_suite_id``** táknar kenni prófunarflokks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-281">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="ea70c-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="ea70c-282">generatetestonly</span></span>
<span data-ttu-id="ea70c-283">Myndar aðeins prófunarframkvæmdarskrá fyrir tilgreint prófunartilfelli í úttaksskráasafninu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="ea70c-284">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="ea70c-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea70c-285">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-286">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-286">Required parameters</span></span>
<span data-ttu-id="ea70c-287">**``test_case_id``** táknar kenni próftilfellis.</span><span class="sxs-lookup"><span data-stu-id="ea70c-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ea70c-288">**``output_dir``** táknar úttaksskráarsafnið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea70c-289">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-290">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="ea70c-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="ea70c-291">generatetestsuite</span></span>
<span data-ttu-id="ea70c-292">Býr til öll prófunartilvik fyrir tilgreindan flokk í úttaksskráasafninu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="ea70c-293">Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka.</span><span class="sxs-lookup"><span data-stu-id="ea70c-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="ea70c-294">Notaðu eitthvert gildi úr dálknum sem færibreytuna **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-295">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-295">Required parameters</span></span>
<span data-ttu-id="ea70c-296">**``test_suite_name``** táknar heiti prófunarflokks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="ea70c-297">**``output_dir``** táknar úttaksskráarsafnið.</span><span class="sxs-lookup"><span data-stu-id="ea70c-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea70c-298">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-299">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="ea70c-300">help</span><span class="sxs-lookup"><span data-stu-id="ea70c-300">help</span></span>
<span data-ttu-id="ea70c-301">Eins og [?](####?)</span><span class="sxs-lookup"><span data-stu-id="ea70c-301">Identical to the [?](####?)</span></span> <span data-ttu-id="ea70c-302">command</span><span class="sxs-lookup"><span data-stu-id="ea70c-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="ea70c-303">Listi</span><span class="sxs-lookup"><span data-stu-id="ea70c-303">list</span></span>
<span data-ttu-id="ea70c-304">Listar yfir öll tiltæk prófunartilvik.</span><span class="sxs-lookup"><span data-stu-id="ea70c-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="ea70c-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="ea70c-305">listtestplans</span></span>
<span data-ttu-id="ea70c-306">Listar yfir allar tiltækar prófunaráætlanir.</span><span class="sxs-lookup"><span data-stu-id="ea70c-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="ea70c-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="ea70c-307">listtestsuite</span></span>
<span data-ttu-id="ea70c-308">Listar yfir prófunartilvik fyrir tilgreindan prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="ea70c-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="ea70c-309">Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka.</span><span class="sxs-lookup"><span data-stu-id="ea70c-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ea70c-310">Notaðu eitthvert gildi úr fyrsta dálknum sem færibreytuna **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-311">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-311">Required parameters</span></span>
<span data-ttu-id="ea70c-312">**``suite_name``** Heiti viðkomandi flokks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-313">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="ea70c-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="ea70c-314">listtestsuitenames</span></span>
<span data-ttu-id="ea70c-315">Listar yfir alla tiltæka prófunarflokka.</span><span class="sxs-lookup"><span data-stu-id="ea70c-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="ea70c-316">playback</span><span class="sxs-lookup"><span data-stu-id="ea70c-316">playback</span></span>
<span data-ttu-id="ea70c-317">Spilar prófunartilvik með Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="ea70c-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-318">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-318">Required parameters</span></span>
<span data-ttu-id="ea70c-319">**``excel_file``** Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="ea70c-320">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="ea70c-321">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="ea70c-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="ea70c-322">playbackbyid</span></span>
<span data-ttu-id="ea70c-323">Spilar mörg prófunartilvik í einu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="ea70c-324">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="ea70c-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea70c-325">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-326">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-326">Required parameters</span></span>
<span data-ttu-id="ea70c-327">**``test_case_id1``** Auðkenni núverandi prófunartilviks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="ea70c-328">**``test_case_id2``** Auðkenni núverandi prófunartilviks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="ea70c-329">**``test_case_idN``** Auðkenni núverandi prófunartilviks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="ea70c-330">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="ea70c-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="ea70c-331">playbackmany</span></span>
<span data-ttu-id="ea70c-332">Spilar mörg prófunartilvik í einu með Excel-skrám.</span><span class="sxs-lookup"><span data-stu-id="ea70c-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-333">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-333">Required parameters</span></span>
<span data-ttu-id="ea70c-334">**``excel_file1``** Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="ea70c-335">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-335">File must exist.</span></span>  
<span data-ttu-id="ea70c-336">**``excel_file2``** Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="ea70c-337">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-337">File must exist.</span></span>  
<span data-ttu-id="ea70c-338">**``excel_fileN``** Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="ea70c-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="ea70c-339">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="ea70c-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="ea70c-340">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="ea70c-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="ea70c-341">playbacksuite</span></span>
<span data-ttu-id="ea70c-342">Spilar öll prófunartilvik úr tilgreinda prófunarflokknum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="ea70c-343">Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka.</span><span class="sxs-lookup"><span data-stu-id="ea70c-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ea70c-344">Notaðu eitthvert gildi úr fyrsta dálknum sem færibreytuna **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-345">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-345">Required parameters</span></span>
<span data-ttu-id="ea70c-346">**``suite_name``** Heiti viðkomandi flokks.</span><span class="sxs-lookup"><span data-stu-id="ea70c-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-347">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="ea70c-348">quit</span><span class="sxs-lookup"><span data-stu-id="ea70c-348">quit</span></span>
<span data-ttu-id="ea70c-349">Lokar forritinu.</span><span class="sxs-lookup"><span data-stu-id="ea70c-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="ea70c-350">upload</span><span class="sxs-lookup"><span data-stu-id="ea70c-350">upload</span></span>
<span data-ttu-id="ea70c-351">Hleður inn öllum skrám sem tilheyra tilgreindum prófunarflokk eða prófunartilvikum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="ea70c-352">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-352">Required parameters</span></span>
<span data-ttu-id="ea70c-353">**``suite_name``** Öllum skrám sem tilheyra tilgreindum prófunarflokki verður hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="ea70c-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="ea70c-354">**``testcase_id``** Öllum skrám sem tilheyra tilgreindum prófunartilvikum verður hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="ea70c-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-355">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="ea70c-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="ea70c-356">uploadrecording</span></span>
<span data-ttu-id="ea70c-357">Hleður aðeins inn upptökuskránni sem tilheyrir tilgreindum prófunartilvikum.</span><span class="sxs-lookup"><span data-stu-id="ea70c-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="ea70c-358">Áskildar færibreytur</span><span class="sxs-lookup"><span data-stu-id="ea70c-358">Required parameters</span></span>
<span data-ttu-id="ea70c-359">**``testcase_id``** Upptökuskrá sem tilheyrir tilgreindum prófunartilvikum verður hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="ea70c-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea70c-360">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="ea70c-361">usage</span><span class="sxs-lookup"><span data-stu-id="ea70c-361">usage</span></span>
<span data-ttu-id="ea70c-362">Sýnir tvær leiðir til að kalla á þetta forrit: önnur sem notar sjálfgefna stillingaskrá og önnur með stillingarskrá.</span><span class="sxs-lookup"><span data-stu-id="ea70c-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="ea70c-363">Windows PowerShell-dæmi</span><span class="sxs-lookup"><span data-stu-id="ea70c-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="ea70c-364">Keyrðu prófunardæmi í lykkju</span><span class="sxs-lookup"><span data-stu-id="ea70c-364">Run a test case in a loop</span></span>

<span data-ttu-id="ea70c-365">Þú ert með prófunarforskrift sem stofnar nýjan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="ea70c-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="ea70c-366">Með forskriftum er hægt að keyra þetta prófunardæmi í lykkju með slembiröðun á eftirfarandi gögnum áður en hver ítrekun er keyrð:</span><span class="sxs-lookup"><span data-stu-id="ea70c-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="ea70c-367">Kenni viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="ea70c-367">Customer ID</span></span>
- <span data-ttu-id="ea70c-368">Nafn viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="ea70c-368">Customer name</span></span>
- <span data-ttu-id="ea70c-369">Aðsetur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="ea70c-369">Customer address</span></span>

<span data-ttu-id="ea70c-370">Kenni viðskiptavinar verður á sniðinu *ATCUS\<númer\>*, þar sem \<númer\> er gildi á milli **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="ea70c-371">Eftirfarandi dæmi notar eina breytu, **byrja**, til að skilgreina fyrsta númerið sem er notað.</span><span class="sxs-lookup"><span data-stu-id="ea70c-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="ea70c-372">Er notuð önnur færibreyta, **nr**, til að skilgreina fjölda viðskiptavina sem verður að stofna.</span><span class="sxs-lookup"><span data-stu-id="ea70c-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="ea70c-373">Fyrir hverja ítrekun er færibreytunum í Excel-færibreytuskránni breytt með því að nota virknina UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="ea70c-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="ea70c-374">Síðan er RSAT-skipanalínan kölluð í virkninni RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="ea70c-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="ea70c-375">Opnaðu Microsoft Windows PowerShell Integrated Scripting Environment (ISE) í stjórnandaham og límdu eftirfarandi kóða inn í gluggann sem heitir **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="ea70c-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="ea70c-376">Keyrðu handrit sem fer eftir gögnum í Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ea70c-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="ea70c-377">Eftirfarandi dæmi notar Open Data Protocol (OData)-kall til að finna pöntunarstöðu innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="ea70c-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="ea70c-378">Ef staðan er ekki **innheimt**, getur þú til dæmis kallað í RSAT-prófunardæmi sem bókar reikninginn.</span><span class="sxs-lookup"><span data-stu-id="ea70c-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
