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
ms.openlocfilehash: 654685a382ca5f3f462ad8a9c506b51b52c3758c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811650"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="4938f-104">Notaðu kennsluefni fyrir Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="4938f-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4938f-105">Notaðu verkfæri þín í internetvafranum til að sækja og vista þessa síðu á pdf-sniði.</span><span class="sxs-lookup"><span data-stu-id="4938f-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="4938f-106">Þetta kennsluefni fer í gegnum nokkra ítarlega eiginleika Regression Suite Automation Tool (RSAT), inniheldur sýniúthlutun og lýsir stefnu og lykilatriðum.</span><span class="sxs-lookup"><span data-stu-id="4938f-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="4938f-107">Eiginleikar RSAT/verkskráningar</span><span class="sxs-lookup"><span data-stu-id="4938f-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="4938f-108">Villuleita reitargildi</span><span class="sxs-lookup"><span data-stu-id="4938f-108">Validate a field value</span></span>

<span data-ttu-id="4938f-109">Nánari upplýsingar um þennan eiginleika er að finna í [Stofna nýja verkskráningu sem hefur staðfestingaraðgerð](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="4938f-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="4938f-110">Vistuð breyta</span><span class="sxs-lookup"><span data-stu-id="4938f-110">Saved variable</span></span>

<span data-ttu-id="4938f-111">Nánari upplýsingar um þennan eiginleika er að finna í [Breyta núverandi verkskráningu til að búa til vistað breytu](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="4938f-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="4938f-112">Afleitt prófunardæmi</span><span class="sxs-lookup"><span data-stu-id="4938f-112">Derived test case</span></span>

1. <span data-ttu-id="4938f-113">Opnaðu Regression Suite Automation Tool (RSAT) og veldu bæði prófunardæmin sem þú stofnaðir í kennsluefninu [Setja upp Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="4938f-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="4938f-114">Veldu **Nýtt \> Stofna afleitt prófunardæmi**.</span><span class="sxs-lookup"><span data-stu-id="4938f-114">Select **New \> Create derived test case**.</span></span>

    ![Stofna afleidda prófunardæmisskipun í valmyndinni Nýtt](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="4938f-116">Þú færð skilaboð sem kveða á um að stofnað verði prófunardæmi fyrir hvert valið prófunardæmi í núverandi prófunarpakka og að hvert afleidd prófunardæmi muni hafa eigið afrit af Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="4938f-117">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4938f-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4938f-118">Þegar þú keyrir afleidd prófunardæmi notar það verkskráningu yfirprófunardæmis og eigið afrit af Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="4938f-119">Þannig geturðu keyrt sama prófið með mismunandi færibreytum, án þess að þurfa að viðhalda fleiri en einni verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="4938f-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="4938f-120">Afleitt prófunardæmi þarf ekki að vera hluti af sama prófunarpakka og yfirprófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="4938f-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Skilaboðagluggi](./media/use_rsa_tool_02.png)

    <span data-ttu-id="4938f-122">Tvö afleidd prófunardæmi eru stofnuð og hakreiturinn **Afleidd?** er valinn fyrir þau.</span><span class="sxs-lookup"><span data-stu-id="4938f-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Afleidd prófunardæmi stofnuð](./media/use_rsa_tool_03.png)

    <span data-ttu-id="4938f-124">Afleidd prófunardæmi eru sjálfvirkt stofnuð í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="4938f-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="4938f-125">Það er undiratriði í prófunardæminu **Stofna nýja afurð** og er merkt með sérstöku lykilorði: **RSAT: DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="4938f-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="4938f-126">Þessum prófunardæmum er einnig sjálfkrafa bætt við prófunaráætlunina í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="4938f-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Lykilorðið RSAT: DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="4938f-128">Ef afleidd prófunardæmi sem eru af einhverjum ástæðum stofnuð eru ekki í réttri röð, skaltu fara í Azure DevOps og endurraða prófdæmunum í prófunarpakkanum, þannig að RSAT geti keyrt þau í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="4938f-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="4938f-129">Veldu aðeins afleidd prófunardæmi og veldu síðan **Breyta** til að opna samsvarandi Excel-færibreytuskrár.</span><span class="sxs-lookup"><span data-stu-id="4938f-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="4938f-130">Breyttu þessum Excel-færibreytuskrám á sama hátt og þú breyttir yfirskránum.</span><span class="sxs-lookup"><span data-stu-id="4938f-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="4938f-131">Með öðrum orðum skaltu ganga úr skugga um að afurðakennið sé stillt þannig að það sé sjálfkrafa myndað.</span><span class="sxs-lookup"><span data-stu-id="4938f-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="4938f-132">Passaðu einnig að vistuð breyta sé afrituð í viðeigandi reiti.</span><span class="sxs-lookup"><span data-stu-id="4938f-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="4938f-133">Á flipanum **Almennt** í báðum Excel-færibreytuskránum skaltu uppfæra gildi reitsins **Fyrirtæki** í **USSI**, þannig að afleidd prófunardæmi verði keyrð gegn öðrum lögaðila en yfirprófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="4938f-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="4938f-134">Til að keyra prófdæmin gegn ákveðnum notanda (eða hlutverki sem tengist ákveðnum notanda) getur þú uppfært gildi reitsins **Prófa notanda**.</span><span class="sxs-lookup"><span data-stu-id="4938f-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="4938f-135">Veldu **Keyra** og sannreyndu að afurðin sé stofnuð bæði í USMF-lögaðilanum og USSI-lögaðilanum.</span><span class="sxs-lookup"><span data-stu-id="4938f-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="4938f-136">Sannprófa tilkynningar</span><span class="sxs-lookup"><span data-stu-id="4938f-136">Validate notifications</span></span>

<span data-ttu-id="4938f-137">Þennan eiginleika er hægt að nota til að staðfesta hvort aðgerð hafi átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="4938f-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="4938f-138">Til dæmis, þegar framleiðslupöntun er stofnuð, áætluð og síðan hafin sýnir forritið skilaboðin „Production - Start“ til að tilkynna þér að framleiðslupöntun hafi verið hafin.</span><span class="sxs-lookup"><span data-stu-id="4938f-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Framleiðsla – Ræsa tilkynningu](./media/use_rsa_tool_05.png)

<span data-ttu-id="4938f-140">Þú getur valið þessi skilaboð í gegnum RSAT með því að slá inn skilaboðartexta á flipann **MessageValidation** í Excel-færibreytuskránni fyrir viðeigandi skráningu.</span><span class="sxs-lookup"><span data-stu-id="4938f-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Flipinn Sannprófun skilaboða](./media/use_rsa_tool_06.png)

<span data-ttu-id="4938f-142">Þegar prófunardæmið hefur verið keyrt eru skilaboðin í Excel-færibreytuskránni borin saman við skilaboðin sem birtast.</span><span class="sxs-lookup"><span data-stu-id="4938f-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="4938f-143">Ef skilaboðin stemma ekki mun prófunardæmið ekki takast.</span><span class="sxs-lookup"><span data-stu-id="4938f-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="4938f-144">Þú getur slegið inn fleiri en eina skilaboð á flipann **MessageValidation** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="4938f-145">Skilaboðin geta einnig verið villuboð eða viðvörunarboð í stað upplýsingaboða.</span><span class="sxs-lookup"><span data-stu-id="4938f-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="4938f-146">Staðfesta gildi með því að nota virkja</span><span class="sxs-lookup"><span data-stu-id="4938f-146">Validate values by using operators</span></span>

<span data-ttu-id="4938f-147">Í fyrri útgáfum af RSAT var aðeins hægt að sannprófa gildi ef eftirlitsgildi jafngild áætluðu gildi.</span><span class="sxs-lookup"><span data-stu-id="4938f-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="4938f-148">Hinn nýi eiginleiki gerir þér kleift að staðfesta að breyta sé ekki jafnt og, sé minna en eða meira en tilgreint gildi.</span><span class="sxs-lookup"><span data-stu-id="4938f-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="4938f-149">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="4938f-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="4938f-150">Í Excel-færibreytuskránni birtist nýi reiturinn **Virki**.</span><span class="sxs-lookup"><span data-stu-id="4938f-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4938f-151">Ef þú hefur verið að nota eldri útgáfu af RSAT verður þú að búa til nýjar Excel-færibreytuskrár.</span><span class="sxs-lookup"><span data-stu-id="4938f-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Reiturinn Virki](./media/use_rsa_tool_07.png)

<span data-ttu-id="4938f-153">Eftirfarandi dæmi sýnir hvernig hægt er að nota þennan eiginleika til að sannreyna hvort lagerbirgðir séu meiri en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="4938f-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="4938f-154">Í kynningargögnum í fyrirtækinu **USMF** skaltu stofna verkskráningu sem er með eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="4938f-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="4938f-155">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="4938f-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="4938f-156">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="4938f-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4938f-157">Til dæmis sía gildið í reitnum **1000** fyrir reitinn **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="4938f-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="4938f-158">Veldu **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="4938f-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="4938f-159">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="4938f-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4938f-160">Til dæmis, sía á gildinu **1** fyrir reitinn **Vefsvæði**.</span><span class="sxs-lookup"><span data-stu-id="4938f-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="4938f-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="4938f-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="4938f-162">Sannprófaðu að gildi reitsins **Samtals magn til ráðstöfunar** sé **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="4938f-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="4938f-163">Vistaðu verkskráninguna í BPM-safnið í LCS og samstilltu það við Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="4938f-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="4938f-164">Bættu prófunardæminu við prófunaráætlunina og settu prófunardæmið í RSAT.</span><span class="sxs-lookup"><span data-stu-id="4938f-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="4938f-165">Opnaðu Excel-færibreytuskrána.</span><span class="sxs-lookup"><span data-stu-id="4938f-165">Open the Excel parameter file.</span></span> <span data-ttu-id="4938f-166">Á flipanum **InventOnhandItem** muntu sjá hlutann **Staðfesta InventOnhandItem** sem inniheldur reitinn **Virki**.</span><span class="sxs-lookup"><span data-stu-id="4938f-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Reiturinn Virki](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="4938f-168">Til að sannreyna hvort birgðir á lager verði alltaf meiri en 0 skaltu breyta gildi reitsins **Gildi** úr **411** í **0** og gildi reitsins **Virki** úr samasemmerki (**=**) í meiraenmerki (**\>**).</span><span class="sxs-lookup"><span data-stu-id="4938f-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Gildum reitanna Gildi og Virki breytt](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="4938f-170">Vistaðu og lokaðu Excel-færibreytskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="4938f-171">Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="4938f-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="4938f-172">Nú, ef gildi reitsins **Samtals magn til ráðstöfunar** fyrir tilgreint atriði í birgðum er meira en 0 (núll), prófanir munu standast, óháð raunverulegu gildi lagerbirgða.</span><span class="sxs-lookup"><span data-stu-id="4938f-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="4938f-173">Kladdar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="4938f-173">Generator logs</span></span>

<span data-ttu-id="4938f-174">Þessi eiginleiki býr til möppu sem inniheldur kladdana í prófunardæmunum sem hafa verið keyrð.</span><span class="sxs-lookup"><span data-stu-id="4938f-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="4938f-175">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="4938f-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="4938f-176">Þegar prófunardæmin hafa verið keyrð geturðu fundið kladdaskrárnar undir **C:\\Notendur\\\<Notendanafn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="4938f-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Mappan GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="4938f-178">Ef það voru til staðar prófunardæmi áður en þú breyttir gildinu í .config-skránni verða kladdar ekki myndaðir fyrir þessi prófdæmi fyrr en þú myndar nýjar prófunarkeyrsluskrár.</span><span class="sxs-lookup"><span data-stu-id="4938f-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Skipunin Mynda textakeyrsluskrár í valmyndinni Nýtt](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="4938f-180">Skyndimynd</span><span class="sxs-lookup"><span data-stu-id="4938f-180">Snapshot</span></span>

<span data-ttu-id="4938f-181">Þessi eiginleiki tekur skjámyndir af þeim skrefum sem voru gerð meðan á verkskráningu stóð.</span><span class="sxs-lookup"><span data-stu-id="4938f-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="4938f-182">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="4938f-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="4938f-183">Undir **C:\\Notendur\\\<Notendanafn\>\\AppData\\Roaming\\regressionTool\\playback**, sérstakri möppu er stofnuð fyrir hvert prófunardæmi sem er keyrt.</span><span class="sxs-lookup"><span data-stu-id="4938f-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Mappan Skyndimynd fyrir prófunardæmi](./media/use_rsa_tool_12.png)

<span data-ttu-id="4938f-185">Í sérhverri af þessum möppum er hægt að finna skyndimyndir af þeim skrefum sem voru gerð meðan prófunardæmin voru keyrð.</span><span class="sxs-lookup"><span data-stu-id="4938f-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Skyndimyndaskrár](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="4938f-187">Verkefni</span><span class="sxs-lookup"><span data-stu-id="4938f-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="4938f-188">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="4938f-188">Scenario</span></span>

1. <span data-ttu-id="4938f-189">Vöruhönnuður stofnar nýja útgefna vöru.</span><span class="sxs-lookup"><span data-stu-id="4938f-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="4938f-190">Framleiðslustjóri setur framleiðslufyrirmæli af stað til að koma birgðastigi í tvær einingar.</span><span class="sxs-lookup"><span data-stu-id="4938f-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="4938f-191">Framleiðsla byrjar og endar framleiðslupöntunina og staðfestir að magnið í lagerbirgðum sé tvær einingar.</span><span class="sxs-lookup"><span data-stu-id="4938f-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="4938f-192">Söluhópurinn fær pöntun um fjögur stykki af nýrri afurð.</span><span class="sxs-lookup"><span data-stu-id="4938f-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="4938f-193">Þess vegna uppfærir söluhópurinn nettóþarfirnar í gegnum kviku áætlunina.</span><span class="sxs-lookup"><span data-stu-id="4938f-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="4938f-194">Þar sem engin viðbótargeta er til staðar er sjálfgefin pöntunarregla stillt á „kaupa í stað þess að búa til“.</span><span class="sxs-lookup"><span data-stu-id="4938f-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="4938f-195">Þess vegna er innkaupatillaga stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4938f-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="4938f-196">Kaupandi bætir við lánardrottni, staðfestir áætlaða innkaupapöntun og staðfestir síðan innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="4938f-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="4938f-197">Þegar vörurnar sem voru keyptar koma í verslunina leitar verslunarrekandinn að viðkomandi innkaupapöntun og tekur á móti vörunum.</span><span class="sxs-lookup"><span data-stu-id="4938f-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="4938f-198">Þar sem pöntuninni hefur nú verið lokið er hægt að taka vörurnar til og pakka á móti sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="4938f-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="4938f-199">Fjármál birta innkaupareikning og sölureikning.</span><span class="sxs-lookup"><span data-stu-id="4938f-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="4938f-200">Eftirfarandi mynd sýnir flæðið fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="4938f-200">The following illustration shows the flow for this scenario.</span></span>

![Flæði fyrir kynningaraðstæður](./media/use_rsa_tool_14.png)

<span data-ttu-id="4938f-202">Eftirfarandi mynd sýnir viðskiptaferlin fyrir þessar aðstæður í RSAT.</span><span class="sxs-lookup"><span data-stu-id="4938f-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Viðskiptaferli fyrir kynningaraðstæður](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="4938f-204">Stjórnunarstefna – Lykilnám</span><span class="sxs-lookup"><span data-stu-id="4938f-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="4938f-205">Gögn</span><span class="sxs-lookup"><span data-stu-id="4938f-205">Data</span></span>

- <span data-ttu-id="4938f-206">Passaðu að þú hafir dæmigert gagnamagn (afrit af framleiðslu-/gullgrunnstillingargögnum auk yfirfærðra gagna).</span><span class="sxs-lookup"><span data-stu-id="4938f-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="4938f-207">Þegar þú myndar ný gögn í gegnum verkskráningu skaltu stofna prófunarheiti sem munu ekki rekast á við fyrirliggjandi heiti (t.d. nota forskeyti eins og **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="4938f-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="4938f-208">Notaðu endurheimt Azure Point-In-Time til að endurkeyra prófanir í umhverfi sem ekki eru í 1. lagi.</span><span class="sxs-lookup"><span data-stu-id="4938f-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="4938f-209">Þó að þú getir notað Excel-aðgerðirnar **RANDOM** og **NOW** til að mynda einkvæma samsetningu er framlagið tiltölulega hátt.</span><span class="sxs-lookup"><span data-stu-id="4938f-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="4938f-210">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="4938f-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="4938f-211">Verkskráning</span><span class="sxs-lookup"><span data-stu-id="4938f-211">Task recorder</span></span>

- <span data-ttu-id="4938f-212">Skilgreindu aðstæður áður en þú hefur skráningu.</span><span class="sxs-lookup"><span data-stu-id="4938f-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="4938f-213">Vel stýrt verk er með fyrirframskilgreindar prófunaraðstæður.</span><span class="sxs-lookup"><span data-stu-id="4938f-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="4938f-214">Til að byggja upp prófunardæmi skaltu íhuga hversu fyrirsjáanleg niðurstaða þessara prófunaraðstæðna er.</span><span class="sxs-lookup"><span data-stu-id="4938f-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="4938f-215">Skiptu skráningum ef þær eru gerðar með mismunandi hlutverkum eða ef það er biðtími eða utanaðkomandi viðburður á undan næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="4938f-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="4938f-216">Forðastu að velja gildi í listum.</span><span class="sxs-lookup"><span data-stu-id="4938f-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="4938f-217">Notaðu þess í stað textasnið, til dæmis **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="4938f-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="4938f-218">Þegar þú velur í lista er staðsetning gildis í listanum skráð, ekki gildið sjálft.</span><span class="sxs-lookup"><span data-stu-id="4938f-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="4938f-219">Ef hlutum er bætt við listann getur staðsetning gildisins breyst.</span><span class="sxs-lookup"><span data-stu-id="4938f-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="4938f-220">Þess vegna mun skráningin nota aðra færibreytu og afgangurinn af aðstæðunum gæti orðið fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="4938f-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="4938f-221">Hugsaðu um hegðun fjölnotenda.</span><span class="sxs-lookup"><span data-stu-id="4938f-221">Think about multi-user behavior.</span></span> <span data-ttu-id="4938f-222">Til dæmis skaltu ekki gera ráð fyrir að nýstofnuð sölupöntun þín verði alltaf sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="4938f-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="4938f-223">Notaðu þess í stað alltaf síuna til að finna réttu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="4938f-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="4938f-224">Notaðu virknina Afrita í verkskráningum til að vista heiti nýstofnaðrar afurðar þannig að hægt sé að nota það í keðjuðum prófunardæmum.</span><span class="sxs-lookup"><span data-stu-id="4938f-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="4938f-225">Notaðu virknina Sannprófa í verkskráningunni til að stilla gátstaði sem staðfesta að skref hafi verið keyrð rétt.</span><span class="sxs-lookup"><span data-stu-id="4938f-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="4938f-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="4938f-226">RSAT</span></span>

- <span data-ttu-id="4938f-227">Til að keyra prófið í öðru fyrirtæki geturðu breytt fyrirtækinu á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="4938f-228">Passaðu að stillingar og gögn séu tiltæk í nýja valda fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="4938f-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="4938f-229">Þú getur breytt prófnotanda á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="4938f-230">Tilgreindu netfang notandans mun keyra prófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="4938f-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="4938f-231">Þannig er hægt að keyra prófunardæmið með því að nota öryggisheimildir tiltekins notanda.</span><span class="sxs-lookup"><span data-stu-id="4938f-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="4938f-232">Til að bíða áður en prófunin hefst geturðu skilgreint hlé á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="4938f-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="4938f-233">Þetta hlé má nota í runuvinnslu (til dæmis ef keyra þarf verkflæði áður en hægt er að framkvæma næsta skref.)</span><span class="sxs-lookup"><span data-stu-id="4938f-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="4938f-234">Ítarlegri forskriftir</span><span class="sxs-lookup"><span data-stu-id="4938f-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="4938f-235">Skipunarlína</span><span class="sxs-lookup"><span data-stu-id="4938f-235">Command line</span></span>

<span data-ttu-id="4938f-236">Hægt er að kalla RSAT úr glugganum **Skipanakvaðning**.</span><span class="sxs-lookup"><span data-stu-id="4938f-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="4938f-237">Staðfestu að umhverfisbreytan **TestRoot** sé stillt á RSAT-uppsetningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="4938f-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="4938f-238">(Í Microsoft Windows skaltu opna **Stjórnborð**, velja **Kerfi og öryggi \> Kerfi \> Ítarlegir kerfisstillingar** og velja síðan **Umhverfisbreytur** .)</span><span class="sxs-lookup"><span data-stu-id="4938f-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="4938f-239">Opnaðu gluggann **Skipanakvaðning** sem stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="4938f-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="4938f-240">Keyrðu verkfærið úr skráarsafni uppsetningar.</span><span class="sxs-lookup"><span data-stu-id="4938f-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="4938f-241">Listi yfir alla skipanir.</span><span class="sxs-lookup"><span data-stu-id="4938f-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="4938f-242">Windows PowerShell-dæmi</span><span class="sxs-lookup"><span data-stu-id="4938f-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="4938f-243">Keyrðu prófunardæmi í lykkju</span><span class="sxs-lookup"><span data-stu-id="4938f-243">Run a test case in a loop</span></span>

<span data-ttu-id="4938f-244">Þú ert með prófunarforskrift sem stofnar nýjan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="4938f-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="4938f-245">Með forskriftum er hægt að keyra þetta prófunardæmi í lykkju með slembiröðun á eftirfarandi gögnum áður en hver ítrekun er keyrð:</span><span class="sxs-lookup"><span data-stu-id="4938f-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="4938f-246">Kenni viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="4938f-246">Customer ID</span></span>
- <span data-ttu-id="4938f-247">Nafn viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="4938f-247">Customer name</span></span>
- <span data-ttu-id="4938f-248">Aðsetur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="4938f-248">Customer address</span></span>

<span data-ttu-id="4938f-249">Kenni viðskiptavinar verður á sniðinu *ATCUS\<númer\>*, þar sem \<númer\> er gildi á milli **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="4938f-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="4938f-250">Eftirfarandi dæmi notar eina breytu, **byrja**, til að skilgreina fyrsta númerið sem er notað.</span><span class="sxs-lookup"><span data-stu-id="4938f-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="4938f-251">Er notuð önnur færibreyta, **nr**, til að skilgreina fjölda viðskiptavina sem verður að stofna.</span><span class="sxs-lookup"><span data-stu-id="4938f-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="4938f-252">Fyrir hverja ítrekun er færibreytunum í Excel-færibreytuskránni breytt með því að nota virknina UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="4938f-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="4938f-253">Síðan er RSAT-skipanalínan kölluð í virkninni RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="4938f-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="4938f-254">Opnaðu Microsoft Windows PowerShell Integrated Scripting Environment (ISE) í stjórnandaham og límdu eftirfarandi kóða inn í gluggann sem heitir **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="4938f-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="4938f-255">Keyrðu handrit sem fer eftir gögnum í Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4938f-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="4938f-256">Eftirfarandi dæmi notar Open Data Protocol (OData)-kall til að finna pöntunarstöðu innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="4938f-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="4938f-257">Ef staðan er ekki **innheimt**, getur þú til dæmis kallað í RSAT-prófunardæmi sem bókar reikninginn.</span><span class="sxs-lookup"><span data-stu-id="4938f-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
