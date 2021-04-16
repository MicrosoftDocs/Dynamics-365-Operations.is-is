---
title: Kennsla í Regression Suite Automation Tool
description: Þetta efni sýnir hvernig á að nota Regression Suite Automation Tool (RSAT). Það lýsir ýmsum eiginleikum og gefur dæmi sem nota ítarlegar forskriftir.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 5a9f19168093f24a7f152b2b5b23b3728ca80222
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745166"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="cffc3-104">Kennsla í Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="cffc3-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="cffc3-105">Notaðu verkfæri þín í internetvafranum til að sækja og vista þessa síðu á pdf-sniði.</span><span class="sxs-lookup"><span data-stu-id="cffc3-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="cffc3-106">Þetta kennsluefni fer í gegnum nokkra ítarlega eiginleika Regression Suite Automation Tool (RSAT), inniheldur sýniúthlutun og lýsir stefnu og lykilatriðum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="cffc3-107">Athyglisverðir eiginleikar RSAT og verkskráning</span><span class="sxs-lookup"><span data-stu-id="cffc3-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="cffc3-108">Villuleita reitargildi</span><span class="sxs-lookup"><span data-stu-id="cffc3-108">Validate a field value</span></span>

<span data-ttu-id="cffc3-109">RSAT gerir þér kleift að setja staðfestingarskref í prófatilvikið þitt til að staðfesta vænt gildi.</span><span class="sxs-lookup"><span data-stu-id="cffc3-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="cffc3-110">Upplýsingar um þennan eiginleika er að finna í greininni [Staðfesta væntanleg gildi](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="cffc3-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="cffc3-111">Eftirfarandi dæmi sýnir hvernig hægt er að nota þennan eiginleika til að sannreyna hvort lagerbirgðir séu meiri en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="cffc3-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="cffc3-112">Í kynningargögnum í fyrirtækinu **USMF** skaltu stofna verkskráningu sem er með eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="cffc3-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="cffc3-113">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="cffc3-114">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="cffc3-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cffc3-115">Til dæmis sía gildið í reitnum **1000** fyrir reitinn **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="cffc3-116">Veldu **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="cffc3-117">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="cffc3-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cffc3-118">Til dæmis, sía á gildinu **1** fyrir reitinn **Vefsvæði**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="cffc3-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="cffc3-120">Sannprófaðu að gildi reitsins **Samtals magn til ráðstöfunar** sé **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="cffc3-121">Vistið verkskráningu sem **skráningu þróunaraðila** og hengið hana við prófunardæmið í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="cffc3-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="cffc3-122">Bættu prófunardæminu við prófunaráætlunina og settu prófunardæmið í RSAT.</span><span class="sxs-lookup"><span data-stu-id="cffc3-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="cffc3-123">Opnið Excel-færibreytuskrána og farið í flipann **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="cffc3-124">Til að sannprófa hvort lagerbirgðir muni alltaf verða meiri en **0** skal fara í skrefið **Sannprófa samtals til ráðstöfunar** og breyta gildi þeirra úr **411** í **0**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="cffc3-125">Breytið gildinu í reitnum **Virknitákn** úr samasemmerki (**=**) í stærra en merki (**\>**).</span><span class="sxs-lookup"><span data-stu-id="cffc3-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="cffc3-126">Vistaðu og lokaðu Excel-færibreytskránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="cffc3-127">Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="cffc3-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="cffc3-128">Nú, ef gildi reitsins **Samtals magn til ráðstöfunar** fyrir tilgreint atriði í birgðum er meira en 0 (núll), prófanir munu standast, óháð raunverulegu gildi lagerbirgða.</span><span class="sxs-lookup"><span data-stu-id="cffc3-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="cffc3-129">Vistaðar breytur og keðjupróf</span><span class="sxs-lookup"><span data-stu-id="cffc3-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="cffc3-130">Eitt af lykileiginleikunum í RSAT er keðja prófunardæma, það er að segja, geta prófunar til að gefa breytur til annarra prófana.</span><span class="sxs-lookup"><span data-stu-id="cffc3-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="cffc3-131">Nánari upplýsingar er að finna í greininni [Afrita breytur í keðjuprófatilfelli](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="cffc3-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="cffc3-132">Afleitt prófunardæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-132">Derived test case</span></span>

<span data-ttu-id="cffc3-133">RSAT gerir þér kleift að nota sömu verkefnaskráningu með mörgum prófatilvikum, sem gerir verki kleift að keyra með mismunandi gagnaskipan.</span><span class="sxs-lookup"><span data-stu-id="cffc3-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="cffc3-134">Sjá greinina [Afleidd prófunartilvik](rsat-derived-test-cases.md) fyrir meiri upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="cffc3-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="cffc3-135">Staðfesta tilkynningar og skilaboð</span><span class="sxs-lookup"><span data-stu-id="cffc3-135">Validate notifications and messages</span></span>

<span data-ttu-id="cffc3-136">Þennan eiginleika er hægt að nota til að staðfesta hvort aðgerð hafi átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="cffc3-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="cffc3-137">Til dæmis, þegar framleiðslupöntun er stofnuð, áætluð og síðan hafin sýnir forritið skilaboðin „Production - Start“ til að tilkynna þér að framleiðslupöntun hafi verið hafin.</span><span class="sxs-lookup"><span data-stu-id="cffc3-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Framleiðsla – Ræsa tilkynningu](./media/use_rsa_tool_05.png)

<span data-ttu-id="cffc3-139">Þú getur valið þessi skilaboð í gegnum RSAT með því að slá inn skilaboðartexta á flipann **MessageValidation** í Excel-færibreytuskránni fyrir viðeigandi skráningu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Flipinn Sannprófun skilaboða](./media/use_rsa_tool_06.png)

<span data-ttu-id="cffc3-141">Þegar prófunardæmið hefur verið keyrt eru skilaboðin í Excel-færibreytuskránni borin saman við skilaboðin sem birtast.</span><span class="sxs-lookup"><span data-stu-id="cffc3-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="cffc3-142">Ef skilaboðin stemma ekki mun prófunardæmið ekki takast.</span><span class="sxs-lookup"><span data-stu-id="cffc3-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="cffc3-143">Þú getur slegið inn fleiri en eina skilaboð á flipann **MessageValidation** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="cffc3-144">Skilaboðin geta einnig verið villuboð eða viðvörunarboð í stað upplýsingaboða.</span><span class="sxs-lookup"><span data-stu-id="cffc3-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="cffc3-145">Skyndimynd</span><span class="sxs-lookup"><span data-stu-id="cffc3-145">Snapshot</span></span>

<span data-ttu-id="cffc3-146">Þessi eiginleiki tekur skjámyndir af þeim skrefum sem voru gerð meðan á verkskráningu stóð.</span><span class="sxs-lookup"><span data-stu-id="cffc3-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="cffc3-147">Það er gagnlegt fyrir endurskoðun eða kembiforrit.</span><span class="sxs-lookup"><span data-stu-id="cffc3-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="cffc3-148">Til að nota þennan eiginleika, skaltu opna skrána **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** í RSAT-uppsetningarmöppunni (til dæmis, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og breyta gildinu í eftirfarandi einingu úr **rangt** í **rétt**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="cffc3-149">Þegar þú keyrir prófunartilvikið mun RSAT búa til myndatökur (myndir) af skrefunum í spilunarmöppunni á prófatilvikunum í vinnumiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="cffc3-150">Ef verið er að nota eldri útgáfu af RSAT eru myndirnar vistaðar í **C:\\Notendur\\\<Username\>\\AppData\\Roaming\\regressionTool\\spilun**, aðskilin mappa er búin til fyrir hvert prófunartilvik sem er keyrt.</span><span class="sxs-lookup"><span data-stu-id="cffc3-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="cffc3-151">Verkefni</span><span class="sxs-lookup"><span data-stu-id="cffc3-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="cffc3-152">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="cffc3-152">Scenario</span></span>

1. <span data-ttu-id="cffc3-153">Vöruhönnuður stofnar nýja útgefna vöru.</span><span class="sxs-lookup"><span data-stu-id="cffc3-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="cffc3-154">Framleiðslustjóri setur framleiðslufyrirmæli af stað til að koma birgðastigi í tvær einingar.</span><span class="sxs-lookup"><span data-stu-id="cffc3-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="cffc3-155">Framleiðsla byrjar og endar framleiðslupöntunina og staðfestir að magnið í lagerbirgðum sé tvær einingar.</span><span class="sxs-lookup"><span data-stu-id="cffc3-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="cffc3-156">Söluhópurinn fær pöntun um fjögur stykki af nýrri afurð.</span><span class="sxs-lookup"><span data-stu-id="cffc3-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="cffc3-157">Þess vegna uppfærir söluhópurinn nettóþarfirnar í gegnum kviku áætlunina.</span><span class="sxs-lookup"><span data-stu-id="cffc3-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="cffc3-158">Þar sem engin viðbótargeta er til staðar er sjálfgefin pöntunarregla stillt á „kaupa í stað þess að búa til“.</span><span class="sxs-lookup"><span data-stu-id="cffc3-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="cffc3-159">Þess vegna er innkaupatillaga stofnuð.</span><span class="sxs-lookup"><span data-stu-id="cffc3-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="cffc3-160">Kaupandi bætir við lánardrottni, staðfestir áætlaða innkaupapöntun og staðfestir síðan innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="cffc3-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="cffc3-161">Þegar vörurnar sem voru keyptar koma í verslunina leitar verslunarrekandinn að viðkomandi innkaupapöntun og tekur á móti vörunum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="cffc3-162">Þar sem pöntuninni hefur nú verið lokið er hægt að taka vörurnar til og pakka á móti sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="cffc3-163">Fjármál birta innkaupareikning og sölureikning.</span><span class="sxs-lookup"><span data-stu-id="cffc3-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="cffc3-164">Eftirfarandi mynd sýnir flæðið fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="cffc3-164">The following illustration shows the flow for this scenario.</span></span>

![Flæði fyrir kynningaraðstæður](./media/use_rsa_tool_14.png)

<span data-ttu-id="cffc3-166">Eftirfarandi mynd sýnir stigveldi viðskiptaferla fyrir þessa atburðarás í LCS Viðskiptaferlavinnslu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Viðskiptaferli fyrir kynningaraðstæður](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="cffc3-168">Stjórnunarstefna – Lykilnám</span><span class="sxs-lookup"><span data-stu-id="cffc3-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="cffc3-169">Gögn</span><span class="sxs-lookup"><span data-stu-id="cffc3-169">Data</span></span>

- <span data-ttu-id="cffc3-170">Passaðu að þú hafir dæmigert gagnamagn (afrit af framleiðslu-/gullgrunnstillingargögnum auk yfirfærðra gagna).</span><span class="sxs-lookup"><span data-stu-id="cffc3-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="cffc3-171">Þegar þú myndar ný gögn í gegnum verkskráningu skaltu stofna prófunarheiti sem munu ekki rekast á við fyrirliggjandi heiti (t.d. nota forskeyti eins og **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="cffc3-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="cffc3-172">Notaðu endurheimt Azure Point-In-Time til að endurkeyra prófanir í umhverfi sem ekki eru í 1. lagi.</span><span class="sxs-lookup"><span data-stu-id="cffc3-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="cffc3-173">Þó að þú getir notað Excel-aðgerðirnar **RANDOM** og **NOW** til að mynda einkvæma samsetningu er framlagið tiltölulega hátt.</span><span class="sxs-lookup"><span data-stu-id="cffc3-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="cffc3-174">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="cffc3-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="cffc3-175">Verkskráning</span><span class="sxs-lookup"><span data-stu-id="cffc3-175">Task recorder</span></span>

- <span data-ttu-id="cffc3-176">Skilgreindu aðstæður áður en þú hefur skráningu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="cffc3-177">Vel stýrt verk er með fyrirframskilgreindar prófunaraðstæður.</span><span class="sxs-lookup"><span data-stu-id="cffc3-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="cffc3-178">Til að byggja upp prófunardæmi skaltu íhuga hversu fyrirsjáanleg niðurstaða þessara prófunaraðstæðna er.</span><span class="sxs-lookup"><span data-stu-id="cffc3-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="cffc3-179">Skiptu skráningum ef þær eru gerðar með mismunandi hlutverkum eða ef það er biðtími eða utanaðkomandi viðburður á undan næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="cffc3-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="cffc3-180">Forðastu að velja gildi í listum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="cffc3-181">Notaðu þess í stað textasnið, til dæmis **FIFO**, **AudioRM** og **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="cffc3-182">Þegar þú velur í lista er staðsetning gildis í listanum skráð, ekki gildið sjálft.</span><span class="sxs-lookup"><span data-stu-id="cffc3-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="cffc3-183">Ef hlutum er bætt við listann getur staðsetning gildisins breyst.</span><span class="sxs-lookup"><span data-stu-id="cffc3-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="cffc3-184">Þess vegna mun skráningin nota aðra færibreytu og afgangurinn af aðstæðunum gæti orðið fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="cffc3-185">Hugsaðu um hegðun fjölnotenda.</span><span class="sxs-lookup"><span data-stu-id="cffc3-185">Think about multi-user behavior.</span></span> <span data-ttu-id="cffc3-186">Til dæmis skaltu ekki gera ráð fyrir að nýstofnuð sölupöntun þín verði alltaf sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="cffc3-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="cffc3-187">Notaðu þess í stað alltaf síuna til að finna réttu pöntunina.</span><span class="sxs-lookup"><span data-stu-id="cffc3-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="cffc3-188">Notaðu virknina Afrita í verkskráningum til að vista heiti nýstofnaðrar afurðar þannig að hægt sé að nota það í keðjuðum prófunardæmum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="cffc3-189">Notaðu virknina Sannprófa í verkskráningunni til að stilla gátstaði sem staðfesta að skref hafi verið keyrð rétt.</span><span class="sxs-lookup"><span data-stu-id="cffc3-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="cffc3-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="cffc3-190">RSAT</span></span>

- <span data-ttu-id="cffc3-191">Til að keyra prófið í öðru fyrirtæki geturðu breytt fyrirtækinu á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="cffc3-192">Passaðu að stillingar og gögn séu tiltæk í nýja valda fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="cffc3-193">Þú getur breytt prófnotanda á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="cffc3-194">Tilgreindu netfang notandans mun keyra prófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="cffc3-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="cffc3-195">Þannig er hægt að keyra prófunardæmið með því að nota öryggisheimildir tiltekins notanda.</span><span class="sxs-lookup"><span data-stu-id="cffc3-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="cffc3-196">Til að bíða áður en prófunin hefst geturðu skilgreint hlé á flipanum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="cffc3-197">Þetta hlé má nota í runuvinnslu (til dæmis ef keyra þarf verkflæði áður en hægt er að framkvæma næsta skref.)</span><span class="sxs-lookup"><span data-stu-id="cffc3-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="cffc3-198">Ítarlegri forskriftir</span><span class="sxs-lookup"><span data-stu-id="cffc3-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="cffc3-199">CLI</span><span class="sxs-lookup"><span data-stu-id="cffc3-199">CLI</span></span>

<span data-ttu-id="cffc3-200">Hægt er að kalla RSAT úr glugganum **Skipanakvaðning** eða **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="cffc3-201">Staðfestu að umhverfisbreytan **TestRoot** sé stillt á RSAT-uppsetningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="cffc3-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="cffc3-202">(Í Microsoft Windows skaltu opna **Stjórnborð**, velja **Kerfi og öryggi \> Kerfi \> Ítarlegir kerfisstillingar** og velja síðan **Umhverfisbreytur** .)</span><span class="sxs-lookup"><span data-stu-id="cffc3-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="cffc3-203">Opnaðu gluggann **Skipanakvaðning** eða **PowerShell** sem stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="cffc3-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="cffc3-204">Farðu í RSAT uppsetningarskrána.</span><span class="sxs-lookup"><span data-stu-id="cffc3-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="cffc3-205">Listi yfir alla skipanir.</span><span class="sxs-lookup"><span data-stu-id="cffc3-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="cffc3-206">?</span><span class="sxs-lookup"><span data-stu-id="cffc3-206">?</span></span>

<span data-ttu-id="cffc3-207">Sýnir hjálp um allar tiltækar skipanir og færibreytur þeirra.</span><span class="sxs-lookup"><span data-stu-id="cffc3-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="cffc3-208">?: Valkvæðar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-208">?: Optional parameters</span></span>

<span data-ttu-id="cffc3-209">`command`: Þar sem ``[command]`` er ein af skipununum sem tilgreindar eru hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="cffc3-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="cffc3-210">um</span><span class="sxs-lookup"><span data-stu-id="cffc3-210">about</span></span>

<span data-ttu-id="cffc3-211">Birtir núverandi útgáfu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="cffc3-212">cls</span><span class="sxs-lookup"><span data-stu-id="cffc3-212">cls</span></span>

<span data-ttu-id="cffc3-213">Hreinsar skjáinn.</span><span class="sxs-lookup"><span data-stu-id="cffc3-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="cffc3-214">sækja</span><span class="sxs-lookup"><span data-stu-id="cffc3-214">download</span></span>

<span data-ttu-id="cffc3-215">Sækir viðhengi fyrir tilgreint prófatilfelli í úttaksskrána.</span><span class="sxs-lookup"><span data-stu-id="cffc3-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="cffc3-216">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="cffc3-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="cffc3-217">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="cffc3-218">niðurhal: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-218">download: required parameters</span></span>

+ <span data-ttu-id="cffc3-219">`test_case_id`: Stendur fyrir kenni prófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="cffc3-220">`output_dir`: Stendur fyrir skráasafn úttaks.</span><span class="sxs-lookup"><span data-stu-id="cffc3-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="cffc3-221">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="cffc3-222">niðurhal: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="cffc3-223">breyta</span><span class="sxs-lookup"><span data-stu-id="cffc3-223">edit</span></span>

<span data-ttu-id="cffc3-224">Gerir þér kleift að opna færibreytuskrá í Excel-forritinu og breyta henni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="cffc3-225">breyta: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-225">edit: required parameters</span></span>

+ <span data-ttu-id="cffc3-226">`excel_file`: Verður að innihalda fulla slóð á fyrirliggjandi Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="cffc3-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="cffc3-227">breyta: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="cffc3-228">generate</span><span class="sxs-lookup"><span data-stu-id="cffc3-228">generate</span></span>

<span data-ttu-id="cffc3-229">Myndar prófaframkvæmdar- og færibreytuskrár fyrir tilgreint próftilfelli í úttaksskráasafninu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="cffc3-230">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="cffc3-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="cffc3-231">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="cffc3-232">mynda: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-232">generate: required parameters</span></span>

+ <span data-ttu-id="cffc3-233">`test_case_id`: Stendur fyrir kenni prófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="cffc3-234">`output_dir`: Stendur fyrir skráasafn úttaks.</span><span class="sxs-lookup"><span data-stu-id="cffc3-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="cffc3-235">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="cffc3-236">mynda: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="cffc3-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="cffc3-237">generatederived</span></span>

<span data-ttu-id="cffc3-238">Býr til nýtt prófatilvik, unnið úr gefnu prófatilviki.</span><span class="sxs-lookup"><span data-stu-id="cffc3-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="cffc3-239">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="cffc3-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="cffc3-240">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="cffc3-241">generatederived: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="cffc3-242">`parent_test_case_id`: Stendur fyrir kenni yfirprófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="cffc3-243">`test_plan_id`: Stendur fyrir kenni prófunaráætlunar.</span><span class="sxs-lookup"><span data-stu-id="cffc3-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="cffc3-244">`test_suite_id`: Stendur fyrir kenni prófunarpakka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="cffc3-245">generatederived: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="cffc3-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="cffc3-246">generatetestonly</span></span>

<span data-ttu-id="cffc3-247">Myndar aðeins prófunarframkvæmdarskrá fyrir tilgreint prófunartilfelli í úttaksskráasafninu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="cffc3-248">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="cffc3-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="cffc3-249">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="cffc3-250">generatetestonly: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="cffc3-251">`test_case_id`: Stendur fyrir kenni prófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="cffc3-252">`output_dir`: Stendur fyrir skráasafn úttaks.</span><span class="sxs-lookup"><span data-stu-id="cffc3-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="cffc3-253">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="cffc3-254">generatetestonly: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="cffc3-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="cffc3-255">generatetestsuite</span></span>

<span data-ttu-id="cffc3-256">Býr til öll prófunartilvik fyrir tilgreindan flokk í úttaksskráasafninu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="cffc3-257">Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="cffc3-258">Notaðu eitthvert gildi úr dálknum sem færibreytuna **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="cffc3-259">generatetestsuite: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="cffc3-260">`test_suite_name`: Stendur fyrir heiti prófunarpakka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="cffc3-261">`output_dir`: Stendur fyrir skráasafn úttaks.</span><span class="sxs-lookup"><span data-stu-id="cffc3-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="cffc3-262">Skráasafnið verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="cffc3-263">generatetestsuite: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="cffc3-264">help</span><span class="sxs-lookup"><span data-stu-id="cffc3-264">help</span></span>

<span data-ttu-id="cffc3-265">Eins og [?](#section)</span><span class="sxs-lookup"><span data-stu-id="cffc3-265">Identical to the [?](#section)</span></span> <span data-ttu-id="cffc3-266">skipun.</span><span class="sxs-lookup"><span data-stu-id="cffc3-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="cffc3-267">Listi</span><span class="sxs-lookup"><span data-stu-id="cffc3-267">list</span></span>

<span data-ttu-id="cffc3-268">Listar yfir öll tiltæk prófunartilvik.</span><span class="sxs-lookup"><span data-stu-id="cffc3-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="cffc3-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="cffc3-269">listtestplans</span></span>

<span data-ttu-id="cffc3-270">Listar yfir allar tiltækar prófunaráætlanir.</span><span class="sxs-lookup"><span data-stu-id="cffc3-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="cffc3-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="cffc3-271">listtestsuite</span></span>

<span data-ttu-id="cffc3-272">Listar yfir prófunartilvik fyrir tilgreindan prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="cffc3-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="cffc3-273">Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="cffc3-274">Notaðu eitthvert gildi úr fyrsta dálknum sem færibreytuna **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="cffc3-275">listtestsuite: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="cffc3-276">`suite_name`: Heiti æskilegs pakka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="cffc3-277">listtestsuite: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="cffc3-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="cffc3-278">listtestsuitenames</span></span>

<span data-ttu-id="cffc3-279">Listar yfir alla tiltæka prófunarflokka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="cffc3-280">playback</span><span class="sxs-lookup"><span data-stu-id="cffc3-280">playback</span></span>

<span data-ttu-id="cffc3-281">Spilar prófunartilvik með Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="cffc3-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="cffc3-282">playback: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-282">playback: required parameters</span></span>

+ <span data-ttu-id="cffc3-283">`excel_file`: Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="cffc3-284">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="cffc3-285">spilun: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="cffc3-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="cffc3-286">playbackbyid</span></span>

<span data-ttu-id="cffc3-287">Spilar mörg prófunartilvik í einu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="cffc3-288">Þú getur notað skipunina ``list`` til að fá öll tiltæk prófatilvik.</span><span class="sxs-lookup"><span data-stu-id="cffc3-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="cffc3-289">Notaðu eitthvert gildi úr fyrsta dálki sem færibreytuna **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="cffc3-290">playback: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="cffc3-291">`test_case_id1`: kenni fyrirliggjand prófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="cffc3-292">`test_case_id2`: kenni fyrirliggjand prófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="cffc3-293">`test_case_idN`: kenni fyrirliggjand prófunardæmis.</span><span class="sxs-lookup"><span data-stu-id="cffc3-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="cffc3-294">playbackbyid: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="cffc3-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="cffc3-295">playbackmany</span></span>

<span data-ttu-id="cffc3-296">Spilar mörg prófunartilvik í einu með Excel-skrám.</span><span class="sxs-lookup"><span data-stu-id="cffc3-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="cffc3-297">playbackmany: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="cffc3-298">`excel_file1`: Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="cffc3-299">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-299">File must exist.</span></span>
+ <span data-ttu-id="cffc3-300">`excel_file2`: Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="cffc3-301">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-301">File must exist.</span></span>
+ <span data-ttu-id="cffc3-302">`excel_fileN`: Full slóð að Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="cffc3-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="cffc3-303">Skrá verður að vera til.</span><span class="sxs-lookup"><span data-stu-id="cffc3-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="cffc3-304">playbackmany: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="cffc3-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="cffc3-305">playbacksuite</span></span>

<span data-ttu-id="cffc3-306">Spilar öll prófunartilvik úr tilgreinda prófunarflokknum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="cffc3-307">Þú getur notað skipunina ``listtestsuitenames`` til að fá alla tiltæka prófunaarflokka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="cffc3-308">Notaðu eitthvert gildi úr fyrsta dálknum sem færibreytuna **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="cffc3-309">playbacksuite: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="cffc3-310">`suite_name`: Heiti æskilegs pakka.</span><span class="sxs-lookup"><span data-stu-id="cffc3-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="cffc3-311">playbacksuite: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="cffc3-312">quit</span><span class="sxs-lookup"><span data-stu-id="cffc3-312">quit</span></span>

<span data-ttu-id="cffc3-313">Lokar forritinu.</span><span class="sxs-lookup"><span data-stu-id="cffc3-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="cffc3-314">upload</span><span class="sxs-lookup"><span data-stu-id="cffc3-314">upload</span></span>

<span data-ttu-id="cffc3-315">Hleður inn öllum skrám sem tilheyra tilgreindum prófunarflokk eða prófunartilvikum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="cffc3-316">upphal: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-316">upload: required parameters</span></span>

+ <span data-ttu-id="cffc3-317">`suite_name`: Allar skrár sem tilheyra tilgreindum prófunarpakka verður hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="cffc3-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="cffc3-318">`testcase_id`: Allar skrár sem tilheyra tilgreindu prófunardæmi verður hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="cffc3-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="cffc3-319">hlaða upp: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="cffc3-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="cffc3-320">uploadrecording</span></span>

<span data-ttu-id="cffc3-321">Hleður aðeins inn upptökuskránni sem tilheyrir tilgreindum prófunartilvikum.</span><span class="sxs-lookup"><span data-stu-id="cffc3-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="cffc3-322">uploadrecording: nauðsynlegar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cffc3-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="cffc3-323">`testcase_id`: Upptökuskrá sem tilheyrir tilgreindum prófunarpökkum verður hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="cffc3-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="cffc3-324">uploadrecording: dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="cffc3-325">usage</span><span class="sxs-lookup"><span data-stu-id="cffc3-325">usage</span></span>

<span data-ttu-id="cffc3-326">Sýnir tvær leiðir til að kalla á þetta forrit: önnur sem notar sjálfgefna stillingaskrá og önnur með stillingarskrá.</span><span class="sxs-lookup"><span data-stu-id="cffc3-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="cffc3-327">Windows PowerShell-dæmi</span><span class="sxs-lookup"><span data-stu-id="cffc3-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="cffc3-328">Keyrðu prófunardæmi í lykkju</span><span class="sxs-lookup"><span data-stu-id="cffc3-328">Run a test case in a loop</span></span>

<span data-ttu-id="cffc3-329">Þú ert með prófunarforskrift sem stofnar nýjan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="cffc3-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="cffc3-330">Með forskriftum er hægt að keyra þetta prófunardæmi í lykkju með slembiröðun á eftirfarandi gögnum áður en hver ítrekun er keyrð:</span><span class="sxs-lookup"><span data-stu-id="cffc3-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="cffc3-331">Kenni viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cffc3-331">Customer ID</span></span>
- <span data-ttu-id="cffc3-332">Nafn viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cffc3-332">Customer name</span></span>
- <span data-ttu-id="cffc3-333">Aðsetur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cffc3-333">Customer address</span></span>

<span data-ttu-id="cffc3-334">Viðskiptavinakennið verður á sniðinu *ATCUS\<number\>* þar sem \<number\> er gildi á milli **000000001** og **999999999**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="cffc3-335">Eftirfarandi dæmi notar eina breytu, **byrja**, til að skilgreina fyrsta númerið sem er notað.</span><span class="sxs-lookup"><span data-stu-id="cffc3-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="cffc3-336">Er notuð önnur færibreyta, **nr**, til að skilgreina fjölda viðskiptavina sem verður að stofna.</span><span class="sxs-lookup"><span data-stu-id="cffc3-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="cffc3-337">Fyrir hverja ítrekun er færibreytunum í Excel-færibreytuskránni breytt með því að nota virknina UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="cffc3-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="cffc3-338">Síðan er RSAT-skipanalínan kölluð í virkninni RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="cffc3-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="cffc3-339">Opnaðu Microsoft Windows PowerShell Integrated Scripting Environment (ISE) í stjórnandaham og límdu eftirfarandi kóða inn í gluggann sem heitir **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="cffc3-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="cffc3-340">Keyrðu handrit sem fer eftir gögnum í Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cffc3-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="cffc3-341">Eftirfarandi dæmi notar Open Data Protocol (OData)-kall til að finna pöntunarstöðu innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="cffc3-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="cffc3-342">Ef staðan er ekki **innheimt**, getur þú til dæmis kallað í RSAT-prófunardæmi sem bókar reikninginn.</span><span class="sxs-lookup"><span data-stu-id="cffc3-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]