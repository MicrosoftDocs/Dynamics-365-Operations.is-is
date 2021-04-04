---
title: Sjálfvirk prófun með rafrænni skýrslugerð
description: Þetta efni útskýrir hvernig hægt er að nota grunnlínueiginleika ramma rafrænnar skýrslugerðar (ER) til að gera sjálfvirka prófun á virkni.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 503d4ca562df5c60ee7c475ac146dffbe0edc0c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569046"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="a414f-103">Sjálfvirk prófun með rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a414f-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a414f-104">Þetta efni útskýrir hvernig hægt er að nota ramma rafrænnar skýrslugerðar (ER) til að gera sjálfvirka prófun á sumri virkni.</span><span class="sxs-lookup"><span data-stu-id="a414f-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="a414f-105">Dæmið í þessu efni sýnir hvernig á að gera sjálfvirka prófun á greiðsluvinnslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="a414f-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="a414f-106">Forritið notar ER ramma til að búa til greiðsluskrár og samsvarandi skjöl meðan á greiðsluvinnslu lánardrottins stendur.</span><span class="sxs-lookup"><span data-stu-id="a414f-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="a414f-107">ER-ramminn samanstendur af íhlutum gagnalíkans, líkanavörpunum og sniðs sem styðja greiðslu vinnslu fyrir mismunandi gerðir greiðslu og myndun skjala á mismunandi sniðum.</span><span class="sxs-lookup"><span data-stu-id="a414f-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="a414f-108">Hægt er að sækja þessa þætti úr Microsoft Dynamics Lifecycle Services (LCS) og flytja þá inn í tilvikið.</span><span class="sxs-lookup"><span data-stu-id="a414f-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="a414f-109">Þú getur einnig sérsniðið hvern íhlut Microsoft og notað hann sem grundvöll eigin sérsniðins íhluta.</span><span class="sxs-lookup"><span data-stu-id="a414f-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="a414f-110">Með því að búa til sérsniðna útgáfu geturðu gert breytingar sem styðja tilteknar kröfur.</span><span class="sxs-lookup"><span data-stu-id="a414f-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="a414f-111">Til dæmis geturðu stillt ER-gagnalíkan og ER-líkanavörpun til að fá aðgang að forritsgögnum sem tengjast tilteknum viðskiptavini, eða þú getur breytt ER-sniði til að breyta útliti á myndun skjala.</span><span class="sxs-lookup"><span data-stu-id="a414f-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="a414f-112">Þú getur notað sérsniðin ER-snið til að vinna greiðsluskrár sem mynda lánardrottnagreiðslur og einnig til að vinna eftirlitsskýrslur.</span><span class="sxs-lookup"><span data-stu-id="a414f-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="a414f-113">Sögugeymnin er studd í ER þáttum.</span><span class="sxs-lookup"><span data-stu-id="a414f-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="a414f-114">Þess vegna getur Microsoft veitt uppfærðar útgáfur af ER-lausnum fyrir greiðsluvinnslu lánardrottins og þú getur sjálfkrafa sameinað uppfærða útgáfu með sérsniðnum þætti með því að endurreikna hana.</span><span class="sxs-lookup"><span data-stu-id="a414f-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="a414f-115">Hins vegar verður þú að prófa endurreiknaða útgáfu til að tryggja að hún virki eins og þú átt von á.</span><span class="sxs-lookup"><span data-stu-id="a414f-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="a414f-116">ER-gagnalíkön og ER-líkanavarpanir eru algengar fyrir mörg ER-snið sem eru notuð til að vinna greiðslur af ólíkum gerðum og til að búa til lands-/svæðissértæk greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="a414f-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="a414f-117">Þess vegna er afar æskilegt að gera notandasamþykki sjálfvirkt og samþættingarprófun þannig að það sé sjálfkrafa gert í mörgum fyrirtækjum en taki tillit til lands-/svæðissamhengi hvers markfyrirtækis, noti mismunandi gagnasöfn og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="a414f-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="a414f-118">Nánari upplýsingar um hvernig á að stofna sérsniðna útgáfu af sniði sem er byggt á sniðinu sem þú fékkst frá skilgreiningarveitunni eru að finna í [ER Uppfæra snið með því að nota nýja grunnútgáfu af viðkomandi sniði](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="a414f-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="a414f-119">Lykilhugtök</span><span class="sxs-lookup"><span data-stu-id="a414f-119">Key concepts</span></span>

<span data-ttu-id="a414f-120">Virkir kraftnotendur geta samið notandasamþykki og samþættingarprófun án þess að þurfa að skrifa frumkóða.</span><span class="sxs-lookup"><span data-stu-id="a414f-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="a414f-121">Notaðu ER-grunnlínueiginleikann til að bera mynduð skjöl saman við aðaleintök.</span><span class="sxs-lookup"><span data-stu-id="a414f-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="a414f-122">Nánari upplýsingar er að sjá í [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="a414f-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="a414f-123">Notaðu verkskráningu til að ská prófunardæmi og innifela gunnlínumat.</span><span class="sxs-lookup"><span data-stu-id="a414f-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="a414f-124">Nánari upplýsingar er að finna [Tilföng verkskráningar](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="a414f-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="a414f-125">Flokkaðu prófunardæmi fyrir nauðsynlegar prófunaraðstæður.</span><span class="sxs-lookup"><span data-stu-id="a414f-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="a414f-126">Nánari upplýsingar er að finna í [Stofna og gera sjálfvirkt staðfestingarpróf notanda](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="a414f-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="a414f-127">Notaðu Viðskiptaferlavinnslu (BPM) í LCS til að búa til söfn fyrir samþykktarprófanir fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="a414f-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="a414f-128">Notaðu BPM-prófunarsöfn til að búa til prufuáætlun og prófunarpakka í Microsoft Azure DevOps Services (Azure DevOps).</span><span class="sxs-lookup"><span data-stu-id="a414f-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="a414f-129">Virkir kraftnotendur geta keyrt prófanir fyrir notandasamþykki og samþættingu.</span><span class="sxs-lookup"><span data-stu-id="a414f-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="a414f-130">Notaðu Regression Suite Automation Tool (RSAT) til að keyra prófunardæmi í æskilegum prófunarpakka.</span><span class="sxs-lookup"><span data-stu-id="a414f-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="a414f-131">Tilkynntu niðurstöður prófana til Azure DevOps og notaðu þessa þjónustu til að kanna þessar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="a414f-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a414f-132">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="a414f-132">Prerequisites</span></span>

<span data-ttu-id="a414f-133">Áður en hægt er að ljúka þessum verkum í efninu verður að ljúka við eftirfarandi forsendur:</span><span class="sxs-lookup"><span data-stu-id="a414f-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="a414f-134">Nota grannfræði sem styður prófunarsjálfvirkni.</span><span class="sxs-lookup"><span data-stu-id="a414f-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="a414f-135">Þú verður að hafa aðgang að tilviki í þessari grannfræði fyrir hlutverkið **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="a414f-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="a414f-136">Þessi grannfræði verður að innihalda kynningargögn sem verða notuð í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="a414f-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="a414f-137">Nánari upplýsingar er að finna [Setja upp og nota umhverfi sem styður samfellda smíði og sjálfvirkni prófunar](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="a414f-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="a414f-138">Til að keyra notandasamþykki og samþættingarprófanir sjálfkrafa verður þú að setja upp RSAT í grannfræðinni sem þú notar og skilgreina það á viðeigandi hátt.</span><span class="sxs-lookup"><span data-stu-id="a414f-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="a414f-139">Upplýsingar um hvernig á að setja upp og skilgreina RSAT og skilgreina það til að vinna með Finance and Operations forritum og Azure DevOps er að finna í [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="a414f-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="a414f-140">Gefðu gaum að forsendum fyrir notkun tækisins.</span><span class="sxs-lookup"><span data-stu-id="a414f-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="a414f-141">Eftirfarandi skýringarmynd sýnir dæmi um stillingar á RSAT.</span><span class="sxs-lookup"><span data-stu-id="a414f-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="a414f-142">Blái ferhyrningurinn nær utan um breytur sem tilgreina aðgang að Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a414f-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="a414f-143">Græni ferhyrningurinn nær utan um breytur sem tilgreina aðgang að tilvikinu.</span><span class="sxs-lookup"><span data-stu-id="a414f-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="a414f-144">![RSAT-stillingar](media/GER-Configure.png "Skjámynd af svarglugganum RSAT-stillingar")</span><span class="sxs-lookup"><span data-stu-id="a414f-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="a414f-145">Til að skipuleggja prófunardæmi í pakka til að tryggja rétta framkvæmdaröð, svo að hægt sé að safna klöddum um framkvæmd prófana til frekari skýrslugerðar og rannsókna, verðurðu að hafa aðgang að Azure DevOps úr notaðri grannfræði.</span><span class="sxs-lookup"><span data-stu-id="a414f-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="a414f-146">Til að ljúka dæminu í þessu efni mælum við með því að þú sækir [ER-notkun fyrir RSAT-prófanir](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="a414f-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="a414f-147">Þessi zip-skrá inniheldur eftirfarandi verkleiðbeiningar:</span><span class="sxs-lookup"><span data-stu-id="a414f-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="a414f-148">Efni</span><span class="sxs-lookup"><span data-stu-id="a414f-148">Content</span></span>                                           | <span data-ttu-id="a414f-149">Skrárheiti og staðsetning</span><span class="sxs-lookup"><span data-stu-id="a414f-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="a414f-150">Verkskráningardæmi til að undirbúa gögn til prófunar</span><span class="sxs-lookup"><span data-stu-id="a414f-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="a414f-151">Undirbúa\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="a414f-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="a414f-152">Verkskráningardæmi til að vinna lánardrottinsgreiðslu</span><span class="sxs-lookup"><span data-stu-id="a414f-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="a414f-153">Meðhöndla\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="a414f-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="a414f-154">Undirbúa viðskiptaskuldaeininguna til að vinna lánardrottinsgreiðslur</span><span class="sxs-lookup"><span data-stu-id="a414f-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="a414f-155">Skráðu þig inn á tilvikið.</span><span class="sxs-lookup"><span data-stu-id="a414f-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="a414f-156">Sækja eftirfarandi ER-skilgreiningar úr LCS.</span><span class="sxs-lookup"><span data-stu-id="a414f-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="a414f-157">Leiðbeiningar er að finna í [ER Flytja inn skilgreiningu úr Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="a414f-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="a414f-158">**Greiðslulíkan** ER greiðslulíkan</span><span class="sxs-lookup"><span data-stu-id="a414f-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="a414f-159">**Vörpun greiðslulíkans 1611** ER skilgreining vörpunar greiðslulíkans</span><span class="sxs-lookup"><span data-stu-id="a414f-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="a414f-160">**BACS (UK)** ER sniðmátsskilgreining</span><span class="sxs-lookup"><span data-stu-id="a414f-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="a414f-161">![Skilgreiningar rafrænnar skýrslugerðar](media/GER-Configurations.png "Skjámynd af stillingasíðunni í rafrænum skýrslum")</span><span class="sxs-lookup"><span data-stu-id="a414f-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="a414f-162">Veldu **GBSI** sýnigagnafyrirtæki, sem er með lands-/svæðissamhengi í Bretlandi.</span><span class="sxs-lookup"><span data-stu-id="a414f-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="a414f-163">Skilgreina færibreytur viðskiptaskulda:</span><span class="sxs-lookup"><span data-stu-id="a414f-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="a414f-164">Farðu í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluhætti**.</span><span class="sxs-lookup"><span data-stu-id="a414f-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="a414f-165">Veldu greiðsluháttinn **Rafrænt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="a414f-166">Skilgreindu valinn greiðsluhátt þannig að hann noti ER-sniðið **BACS (UK)** sem þú sóttir áður fyrir greiðslu lánardrottins:</span><span class="sxs-lookup"><span data-stu-id="a414f-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="a414f-167">Á flýtiflipanum **Skráarsnið** stillirðu valkostinn **Almennt rafrænt útflutningssnið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a414f-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="a414f-168">Í reitnum **Skilgreining útflutningssniðs** velurðu **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="a414f-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="a414f-169">![Síðan Greiðsluhættir](media/GER-APParameters.png "Skjámynd af síðunni Greiðslumátar")</span><span class="sxs-lookup"><span data-stu-id="a414f-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="a414f-170">Ef þú ert með afleidda útgáfu af þessu ER-sniði sem var stofnuð til að styðja sérstillingar geturðu valið þessa skilgreiningu í greiðsluhættinum **Rafrænt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="a414f-171">Búðu til dæmi um lánardrottinsgreiðslu:</span><span class="sxs-lookup"><span data-stu-id="a414f-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="a414f-172">Farðu í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="a414f-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="a414f-173">Gakktu úr skugga um að þú hafir ekki bókað greiðslubókina.</span><span class="sxs-lookup"><span data-stu-id="a414f-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="a414f-174">![Síðan Heiti greiðslubókar](media/GER-APJournal.png "Skjámynd af síðunni Greiðslubók")</span><span class="sxs-lookup"><span data-stu-id="a414f-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="a414f-175">Veldu **Línur** og sláðu inn línu sem er með eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a414f-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="a414f-176">Svæði</span><span class="sxs-lookup"><span data-stu-id="a414f-176">Field</span></span>               | <span data-ttu-id="a414f-177">Dæmi um gildi</span><span class="sxs-lookup"><span data-stu-id="a414f-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="a414f-178">Nafn lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a414f-178">Vendor name</span></span>         | <span data-ttu-id="a414f-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="a414f-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="a414f-180">Debet</span><span class="sxs-lookup"><span data-stu-id="a414f-180">Debit</span></span>               | <span data-ttu-id="a414f-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a414f-181">1,000.00</span></span>        |
        | <span data-ttu-id="a414f-182">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="a414f-182">Currency</span></span>            | <span data-ttu-id="a414f-183">GBP</span><span class="sxs-lookup"><span data-stu-id="a414f-183">GBP</span></span>             |
        | <span data-ttu-id="a414f-184">Gerð mótlykils</span><span class="sxs-lookup"><span data-stu-id="a414f-184">Offset account type</span></span> | <span data-ttu-id="a414f-185">Banki</span><span class="sxs-lookup"><span data-stu-id="a414f-185">Bank</span></span>            |
        | <span data-ttu-id="a414f-186">Mótlykill</span><span class="sxs-lookup"><span data-stu-id="a414f-186">Offset account</span></span>      | <span data-ttu-id="a414f-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="a414f-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="a414f-188">Greiðsluháttur</span><span class="sxs-lookup"><span data-stu-id="a414f-188">Method of payment</span></span>   | <span data-ttu-id="a414f-189">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="a414f-189">Electronic</span></span>      |

    <span data-ttu-id="a414f-190">![Síðan Greiðslur lánardrottna](media/GER-APJournalLines.png "Skjámynd af síðunni Greiðslur lánardrottna")</span><span class="sxs-lookup"><span data-stu-id="a414f-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="a414f-191">Undirbúa ER-ramma til að prófa greiðsluvinnslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a414f-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="a414f-192">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="a414f-192">Configure ER parameters</span></span>

1. <span data-ttu-id="a414f-193">Farðu í **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="a414f-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="a414f-194">Á flipanum **Viðhengi**, í reitnum **Grunnlína** velurðu **Skrá** sem þá skjalategund sem rammi skjalastjórnunarkerfis (DM) notar til að halda skjölum sem tengjast grunnlínueiginleikanum sem DM-viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="a414f-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="a414f-195">![Síða rafrænna skýrslufæribreyta](media/GER-ERParameters.png "Skjámynd af síðunni Færibreytur rafrænna skýrslna")</span><span class="sxs-lookup"><span data-stu-id="a414f-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="a414f-196">Myndaðu grunnlínuafrit af skjölum sem tengjast lánardrottni</span><span class="sxs-lookup"><span data-stu-id="a414f-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="a414f-197">Farðu í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="a414f-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="a414f-198">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="a414f-198">Select **Lines**.</span></span>
3. <span data-ttu-id="a414f-199">Veldu **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="a414f-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="a414f-200">Veldu greiðsluháttinn **Rafrænt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="a414f-201">Veldu bankareikninginn **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="a414f-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="a414f-202">Stilltu valkostinn **Prenta eftirlitsskýrslu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a414f-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="a414f-203">Sæktu myndað úttak sem zip-skrá.</span><span class="sxs-lookup"><span data-stu-id="a414f-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="a414f-204">Opnaðu skrána sem var sótt.</span><span class="sxs-lookup"><span data-stu-id="a414f-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="a414f-205">Dragðu út eftirfarandi skrár úr skránni sem var sótt:</span><span class="sxs-lookup"><span data-stu-id="a414f-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="a414f-206">**Skrá** greiðsluskrá í textaformi</span><span class="sxs-lookup"><span data-stu-id="a414f-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="a414f-207">**ERVendOutPaymControlReport** eftirlitsskýrsluskrá á XLSX-sniði</span><span class="sxs-lookup"><span data-stu-id="a414f-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="a414f-208">![Útdregnar skrár](media/GER-APJournalProcessed.png "Skjámynd af útdregnum skráarheitum í Windows Explorer")</span><span class="sxs-lookup"><span data-stu-id="a414f-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="a414f-209">Kveiktu á grunnlínueiginleikum ER</span><span class="sxs-lookup"><span data-stu-id="a414f-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="a414f-210">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="a414f-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a414f-211">í aðgerðarúðunni, á flipanum **Skilgreiningar** skaltu velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="a414f-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="a414f-212">Stilltu valkostinn **Keyra í kembistillingum** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a414f-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="a414f-213">Með því að kveikja á breytunni **Keyra í kembistillingum** þvingarðu ramma ER til að framkvæma eftirfarandi aðgerðir eftir framkvæmd á ER-sniði sem býr til skjöl á útleið:</span><span class="sxs-lookup"><span data-stu-id="a414f-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="a414f-214">Ákvarðaðu hvort grunnlína hafi verið skilgreind fyrir einhverja íhluti af framkvæmdu ER-sniði.</span><span class="sxs-lookup"><span data-stu-id="a414f-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="a414f-215">Ákvarðaðu hvort hver skiglreind grunnlína gildi við núverandi aðstæður (fyrirtækjakóði innskráðs fyrirtækis, skráarheiti og heiti skráarframlengingar myndaðs úttaks og svo framvegis).</span><span class="sxs-lookup"><span data-stu-id="a414f-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="a414f-216">Framkvæmdu eftirfarandi aðgerðir fyrir hverja viðeigandi grunnlínu:</span><span class="sxs-lookup"><span data-stu-id="a414f-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="a414f-217">Berðu úttakið sem myndast við framkvæmd ER-sniðs saman við samsvarandi grunnlínu.</span><span class="sxs-lookup"><span data-stu-id="a414f-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="a414f-218">Geymdu samanburðarniðurstöðurnar í ER kembingarkladda skilgreininga.</span><span class="sxs-lookup"><span data-stu-id="a414f-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="a414f-219">Skilgreina ER-grunnlínur fyrir greiðsluvinnslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a414f-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="a414f-220">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="a414f-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a414f-221">Veldu **Grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="a414f-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="a414f-222">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-222">Select **New**.</span></span>
4. <span data-ttu-id="a414f-223">Í reitnum **Tilvísun** velurðu sniðið **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="a414f-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="a414f-224">Veldu **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="a414f-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="a414f-225">Bættu við nýrri gunnlínu fyrir greiðsluskrá lánardrottins:</span><span class="sxs-lookup"><span data-stu-id="a414f-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="a414f-226">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-226">Select **New**.</span></span>
    2. <span data-ttu-id="a414f-227">Í reitnum **Gerð** velurðu DM-skjalagerðina **Skrá** sem þú skilgreindir í ER-breytum til að geyma grunnlínugervingar.</span><span class="sxs-lookup"><span data-stu-id="a414f-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="a414f-228">Flettu til að velja staðbundið vistuðu greiðsluskrána **Skrá** í textasniðinu.</span><span class="sxs-lookup"><span data-stu-id="a414f-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="a414f-229">Í reitnum **Lýsing** slærðu inn **TXT-greiðsluskrá**.</span><span class="sxs-lookup"><span data-stu-id="a414f-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="a414f-230">Bættu við nýrri grunnlínu fyrir eftirlitsskýrsluna fyrir lánardrottinsgreiðsluna:</span><span class="sxs-lookup"><span data-stu-id="a414f-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="a414f-231">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-231">Select **New**.</span></span>
    2. <span data-ttu-id="a414f-232">Í reitnum **Gerð** velurðu DM-skjalagerðina **Skrá** sem þú skilgreindir í ER-breytum til að geyma grunnlínugervingar.</span><span class="sxs-lookup"><span data-stu-id="a414f-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="a414f-233">Flettu til að velja staðbundið vistuðu eftirlitsskýrsluna **ERVendOutPaymControlReport** á XLSX-sniði.</span><span class="sxs-lookup"><span data-stu-id="a414f-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="a414f-234">Í reitnum **Lýsing** slærðu inn **XLSX-eftirlitsskýrsla greiðslu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="a414f-235">![Grunnlínur fyrir skrá lánardrottinsgreiðslu og eftirlitsskýrslu](media/GER-BaselineAttachments.png "Skjámynd af stillingasíðunni með greiðslu XLSX stjórnunarskýrslu valinn")</span><span class="sxs-lookup"><span data-stu-id="a414f-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="a414f-236">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a414f-236">Close the page.</span></span>
9. <span data-ttu-id="a414f-237">Á flýtiflipanum **Grunnlínur** velurðu **Nýtt** til að skilgreina grunnlínu fyrir greiðsluskrá:</span><span class="sxs-lookup"><span data-stu-id="a414f-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="a414f-238">Nefndu línuna **Grunnlínustillingu fyrir greiðsluskrá**.</span><span class="sxs-lookup"><span data-stu-id="a414f-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="a414f-239">Í reitnum **Heiti skráaríhlutar** velurðu **skrá** til að beita þessari grunnlínu við úttak ER-sniðsins sem myndar greiðsluskrána í textasniðinu BACS (UK).</span><span class="sxs-lookup"><span data-stu-id="a414f-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="a414f-240">Í reitnum **Fyrirtæki** velurðu **GBSI** til að beita þessari grunnlínu þegar ER-sniðið **BACS (UK)** er keyrt í GBSI-fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a414f-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="a414f-241">Í reitnum **Skráarheiti síu** slærðu inn **\*.TXT** til að beita þessari grunnlínu aðeins á úttök af sniðíhlutnum **skrá** sem hafa skráarendinguna **.txt**.</span><span class="sxs-lookup"><span data-stu-id="a414f-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="a414f-242">Í reitnum **Grunngildi** velurðu **TXT-greiðsluskrá** þannig að þessi grunnlína sé notuð til samanburðar við myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="a414f-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="a414f-243">Veldu **Nýtt** til að skilgreina grunnlínu fyrir eftirlitsskýrsluna:</span><span class="sxs-lookup"><span data-stu-id="a414f-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="a414f-244">Nefndu línuna **Grunnlínustillingu fyrir eftirlitsskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="a414f-245">Í reitnum **Heiti skráaríhlutar** velurðu **ERVendOutPaymControlReport** til að beita þessari grunnlínu við úttak ER-sniðsins sem myndar eftirlitsskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="a414f-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="a414f-246">Í reitnum **Fyrirtæki** velurðu **GBSI** til að beita þessari grunnlínu þegar ER-sniðið **BACS (UK)** er keyrt í GBSI-fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a414f-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="a414f-247">Í reitnum **Skráarheiti síu** slærðu inn **\*.XLSX** til að beita þessari grunnlínu aðeins á úttök af sniðíhlutnum **ERVendOutPaymControlReport** sem hafa skráarendinguna **.xlsx**.</span><span class="sxs-lookup"><span data-stu-id="a414f-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="a414f-248">Í reitnum **Grunngildi** velurðu **Efitrlitsskýrsla XLSX-greiðslu** þannig að þessi grunnlína sé notuð til samanburðar við myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="a414f-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="a414f-249">![Grunnlínur flýtiflipa á stillingasíðunni](media/GER-BaselineRules.png "Skjámynd af flýtiflipanum Grunnlínum á stillingasíðunni")</span><span class="sxs-lookup"><span data-stu-id="a414f-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="a414f-250">Skráðu prófanir til að sannreyna greiðsluvinnslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a414f-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="a414f-251">Sem virkur kraftnotandi geturðu skráð eigin skref til að prófa greiðsluvinnslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="a414f-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="a414f-252">Við mælum með að þú spilir (og breytir, eftir því sem við á) verkskráninguna **Undirbúa\\Recording.xml** sem þú sóttir áður.</span><span class="sxs-lookup"><span data-stu-id="a414f-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="a414f-253">Þessi skráning er notuð til að stilla öll prófunargögn í rétta stöðu.</span><span class="sxs-lookup"><span data-stu-id="a414f-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="a414f-254">Þetta skref er nauðsynlegt vegna þess að hægt er að gera prófunina mörgum sinnum og hver prófun verður að nota gögn sem eru í sömu stöðu.</span><span class="sxs-lookup"><span data-stu-id="a414f-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="a414f-255">Endurstilla notandastillingar</span><span class="sxs-lookup"><span data-stu-id="a414f-255">Reset user settings</span></span>

1. <span data-ttu-id="a414f-256">Opnaðu sjálfgefið yfirlit.</span><span class="sxs-lookup"><span data-stu-id="a414f-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="a414f-257">Veldu hnappinn **Stillingar** (gírtáknið).</span><span class="sxs-lookup"><span data-stu-id="a414f-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="a414f-258">Veldu **Notendastillingar**.</span><span class="sxs-lookup"><span data-stu-id="a414f-258">Select **User options**.</span></span>
4. <span data-ttu-id="a414f-259">Veldu **Notkunargögn**.</span><span class="sxs-lookup"><span data-stu-id="a414f-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="a414f-260">Veldu **Endurstilla**.</span><span class="sxs-lookup"><span data-stu-id="a414f-260">Select **Reset**.</span></span>
6. <span data-ttu-id="a414f-261">Veldu **Já** til að staðfesta að þú viljir endurstilla notkunargögn.</span><span class="sxs-lookup"><span data-stu-id="a414f-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="a414f-262">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a414f-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="a414f-263">Skráðu skrefin til að undirbúa gögn til prófunar</span><span class="sxs-lookup"><span data-stu-id="a414f-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="a414f-264">Veldu hnappinn **Stillingar** (gírtáknið).</span><span class="sxs-lookup"><span data-stu-id="a414f-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="a414f-265">Veldu **Verkskráningu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="a414f-266">Veldu **Spila skráningu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="a414f-267">Veldu **Opna í þessari tölvu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="a414f-268">Veldu **Skoða** og veldu staðbundið vistuðu skrána **Undirbúa\\Recording.xml**.</span><span class="sxs-lookup"><span data-stu-id="a414f-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="a414f-269">Velja **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="a414f-269">Select **Start**.</span></span>
7. <span data-ttu-id="a414f-270">Haltu áfram að velja **Spila næsta skref í bið** þar til að öll skrefin í upptökunni hafa verið spiluð.</span><span class="sxs-lookup"><span data-stu-id="a414f-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="a414f-271">Þessi verkskráning framkvæmir eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="a414f-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="a414f-272">Stilltu stöðu unninnar greiðslulínu á **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="a414f-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="a414f-273">![Verkskráningarskref 3 til 4](media/GER-Recording1Review1.png "Skjámynd af verkskráningarskrefum 3 til 4")</span><span class="sxs-lookup"><span data-stu-id="a414f-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="a414f-274">Kveiktu á ER-notandabreytunni **Keyra í kembistillingum**.</span><span class="sxs-lookup"><span data-stu-id="a414f-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="a414f-275">![Verkskráningarskref 9 til 10](media/GER-Recording1Review2.png "Skjámynd af verkskráningarskrefum 9 til 10")</span><span class="sxs-lookup"><span data-stu-id="a414f-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="a414f-276">Hreinsaðu ER-kembikladdann sem inniheldur niðurstöður samanburðar á mynduðum skrám í grunnlínur.</span><span class="sxs-lookup"><span data-stu-id="a414f-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="a414f-277">![Verkskráningarskref 13 til 15](media/GER-Recording1Review3.png "Skjámynd af verkskráningarskrefum 13 til 15")</span><span class="sxs-lookup"><span data-stu-id="a414f-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="a414f-278">Skráðu skrefin til að prófa greiðsluvinnslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a414f-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="a414f-279">Við mælum með að þú spilir (og breytir, eftir því sem við á) verkskráninguna **Vinna\\Recording.xml** sem þú sóttir áður.</span><span class="sxs-lookup"><span data-stu-id="a414f-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="a414f-280">Þessi upptaka er notuð til að vinna lánardrottnagreiðslur og staðfesta samanburðarniðurstöður af mynduðum skjölum við samsvarandi grunnlínur.</span><span class="sxs-lookup"><span data-stu-id="a414f-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="a414f-281">Veldu hnappinn **Stillingar** (gírtáknið).</span><span class="sxs-lookup"><span data-stu-id="a414f-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="a414f-282">Veldu **Verkskráningu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="a414f-283">Veldu **Spila skráningu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="a414f-284">Veldu **Opna í þessari tölvu**.</span><span class="sxs-lookup"><span data-stu-id="a414f-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="a414f-285">Veldu **Skoða** og veldu staðbundið vistuðu skrána **Vinna\\Recording.xml**.</span><span class="sxs-lookup"><span data-stu-id="a414f-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="a414f-286">Velja **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="a414f-286">Select **Start**.</span></span>
7. <span data-ttu-id="a414f-287">Haltu áfram að velja **Spila næsta skref í bið** þar til að öll skrefin í upptökunni hafa verið spiluð.</span><span class="sxs-lookup"><span data-stu-id="a414f-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="a414f-288">Þessi verkskráning framkvæmir eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="a414f-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="a414f-289">Ræstu vinnslu lánardrottnagreiðslna.</span><span class="sxs-lookup"><span data-stu-id="a414f-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="a414f-290">Veldu réttar keyrslutímabreytur og kveiktu á myndun eftirlitsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="a414f-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="a414f-291">![Verkskráningarskref 3 til 8](media/GER-Recording2Review1.png "Skjámynd af verkskráningarskrefum 3 til 8")</span><span class="sxs-lookup"><span data-stu-id="a414f-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="a414f-292">Farðu í ER-kembikladdann til að skrá samanburðarniðurstöður á mynduðu úttaki við samsvarandi grunnlínur.</span><span class="sxs-lookup"><span data-stu-id="a414f-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="a414f-293">Í ER-kembikladdanum birtast niðurstöður samanburðarins í reitnum **Myndaður texti**.</span><span class="sxs-lookup"><span data-stu-id="a414f-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="a414f-294">Reitirnir **Sniðsþáttur** og **Sniðsslóð sem olli kladdafærslu** vísa til skráarþáttarins sem myndað úttak hefur verið borið saman við grunnlínuna fyrir.</span><span class="sxs-lookup"><span data-stu-id="a414f-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="a414f-295">![Færslur í keyrslukladdasíðu rafrænnar skýrslugerðar](media/GER-ERDebugLog.png "Skjáskot af færslum í keyrslukladdasíðu rafrænnar skýrslugerðar")</span><span class="sxs-lookup"><span data-stu-id="a414f-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="a414f-296">Samanburður á núverandi úttaki við grunnlínu er skráður með því að nota verskráningarkostinn **Staðfesta** og velja  **Núverandi gildi**.</span><span class="sxs-lookup"><span data-stu-id="a414f-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="a414f-297">![Notaðu villuleikarkostinn til samanburðar við núverandi gildi](media/GER-TRRecordValidation.png "Skjáskot af notkun villuleikarkosts til samanburðar við núverandi gildi")</span><span class="sxs-lookup"><span data-stu-id="a414f-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="a414f-298">Eftirfarandi skýringarmynd sýnir hvernig skráð staðfestingarskref líta út í verkskráningunni.</span><span class="sxs-lookup"><span data-stu-id="a414f-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="a414f-299">![Verkskráningarskref 13 og 15](media/GER-Recording2Review2.png "Skjámynd af verkskráningarskrefum 13 og 15")</span><span class="sxs-lookup"><span data-stu-id="a414f-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="a414f-300">Bættu skráðum prófunum við Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="a414f-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="a414f-301">Opnaðu Azure DevOps umhverfið.</span><span class="sxs-lookup"><span data-stu-id="a414f-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="a414f-302">Veldu verkið sem þú skilgreindir í RSAT-breytunum þegar þú [skilgreindir tólið](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a414f-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="a414f-303">Veldu prófunaráætlunina sem þú skilgreindir í RSAT-breytunum þegar þú [skilgreindir tólið](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a414f-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="a414f-304">Stofnaðu nýtt prófunarmál fyrir valda prófunaráætlun:</span><span class="sxs-lookup"><span data-stu-id="a414f-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="a414f-305">Nefndu prófdæmið **Undirbúa gögn til að prófa vinnslu á rafrænum greiðslum lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="a414f-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="a414f-306">Hengdu við skrána **Recording.xml** úr möppunni **Undirbúa** sem þú sóttir áður.</span><span class="sxs-lookup"><span data-stu-id="a414f-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="a414f-307">Stofnaðu nýtt prófunarmál fyrir valda prófunaráætlun:</span><span class="sxs-lookup"><span data-stu-id="a414f-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="a414f-308">Nefndu prófunardæmið **Prófvinnsla á lánardrottnagreiðslum með því að nota ER-sniðið BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="a414f-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="a414f-309">Hengdu við skrána **Recording.xml** úr möppunni **Vinna** sem þú sóttir áður.</span><span class="sxs-lookup"><span data-stu-id="a414f-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="a414f-310">![Ný prófunarmál fyrir valda prófunaráætlun:](media/GER-RSAT-DevOps-Tests-Passed.png "Skjáskot af nýjum prófunarmálum fyrir valda prófunaráætlun:")</span><span class="sxs-lookup"><span data-stu-id="a414f-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="a414f-311">Gættu þess að framkvæmdaröðin sé rétt á þeim prófunum sem var bætt við.</span><span class="sxs-lookup"><span data-stu-id="a414f-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="a414f-312">Undirbúa RSAT til að keyra skráðar prófanir</span><span class="sxs-lookup"><span data-stu-id="a414f-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="a414f-313">Hladdu prófunum úr Azure DevOps í RSAT</span><span class="sxs-lookup"><span data-stu-id="a414f-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="a414f-314">Opnaðu staðbundna RSAT-forritið í núverandi grannfræði.</span><span class="sxs-lookup"><span data-stu-id="a414f-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="a414f-315">Veldu **Hlaða** til að hlaða prófunum sem eru eins og stendur í Azure DevOps inn í RSAT.</span><span class="sxs-lookup"><span data-stu-id="a414f-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="a414f-316">![Próf hlaðin í RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Skjámynd af prófunum hlaðin í RSAT")</span><span class="sxs-lookup"><span data-stu-id="a414f-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="a414f-317">Stofna sjálfvirkni- og færibreytuskrár</span><span class="sxs-lookup"><span data-stu-id="a414f-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="a414f-318">Í RSAT skaltu velja þær prófanir sem þú hlóðst úr Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a414f-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="a414f-319">Veldu **Nýtt** til að stofna RSAT sjálfvirkni- og færibreytuskrár.</span><span class="sxs-lookup"><span data-stu-id="a414f-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="a414f-320">![RSAT-sjálfvirkni- og færibreytuskrár stofnaðar í RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Skjáskot af RSAT-sjálfvirkni- og færibreytuskrár stofnaðar í RSAT")</span><span class="sxs-lookup"><span data-stu-id="a414f-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="a414f-321">Breyta færibreytuskrám</span><span class="sxs-lookup"><span data-stu-id="a414f-321">Modify the parameters files</span></span>

1. <span data-ttu-id="a414f-322">Í RSAT velurðu prófdæmið **Undirbúa gögn til að prófa vinnslu á rafrænum greiðslum lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="a414f-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="a414f-323">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a414f-323">Select **Edit**.</span></span>
3. <span data-ttu-id="a414f-324">Í vinnubók sem er opnuð í Microsoft Excel, á vinnublaðinu **Almennt**, skaltu breyta fyrirtækjakóðanum í **GBSI**, vegna þess að þetta fyrirtæki verður notað fyrir prófunarframkvæmd.</span><span class="sxs-lookup"><span data-stu-id="a414f-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="a414f-325">Í RSAT velurðu prófunardæmið **Prófvinnsla á lánardrottnagreiðslum með því að nota ER-sniðið BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="a414f-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="a414f-326">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a414f-326">Select **Edit**.</span></span>
6. <span data-ttu-id="a414f-327">Í Excel-vinnubókinni sem er opnuð, í vinnublaðinu **Almennt**, skaltu breyta fyrirtækjakóðanum í **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="a414f-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="a414f-328">Á vinnublaðinu **ERFormatMappingRunLogTable** skaltu athuga að reitirnir A:3 og C:3 innihalda textann í reitunum í ER-kembikladdatöflunni sem er notuð til að staðfesta niðurstöður samanburðar við úttak grunnlínunnar.</span><span class="sxs-lookup"><span data-stu-id="a414f-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="a414f-329">Þessir textar verða notaðir til að meta ER-kembikladdaskrár sem eru búnar til við framkvæmd prófunar.</span><span class="sxs-lookup"><span data-stu-id="a414f-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="a414f-330">![ERFormatMappingRunLogTable vinnublað](media/GER-RSAT-RSAT-ExcelParameters.png "Skjámynd af ERFormatMappingRunLogTable vinnublaðinu")</span><span class="sxs-lookup"><span data-stu-id="a414f-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="a414f-331">Keyrðu prófanirnar og greindu niðurstöðurnar</span><span class="sxs-lookup"><span data-stu-id="a414f-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="a414f-332">Keyrðu prófanirnar í RSAT</span><span class="sxs-lookup"><span data-stu-id="a414f-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="a414f-333">Í RSAT veldurðu hlaðnar prófanir.</span><span class="sxs-lookup"><span data-stu-id="a414f-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="a414f-334">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="a414f-334">Select **Run**.</span></span>

<span data-ttu-id="a414f-335">Athugaðu að prófunardæmin eru sjálfkrafa keyrð í forritinu með því að nota vafra.</span><span class="sxs-lookup"><span data-stu-id="a414f-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="a414f-336">Greindu niðurstöður prófunarframkvæmdar</span><span class="sxs-lookup"><span data-stu-id="a414f-336">Analyze the results of test execution</span></span>

<span data-ttu-id="a414f-337">Niðurstöður prófunarinnar eru geymdar í RSAT.</span><span class="sxs-lookup"><span data-stu-id="a414f-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="a414f-338">Athugaðu að báðar prófanirnar stóðust.</span><span class="sxs-lookup"><span data-stu-id="a414f-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="a414f-339">![Próf sem stóðust í RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Skjámynd af prófunum sem stóðust í RSAT")</span><span class="sxs-lookup"><span data-stu-id="a414f-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="a414f-340">Athugaðu að niðurstöður prófunar eru einnig sendar til Azure DevOps svo að þú getir gert frekari greiningu.</span><span class="sxs-lookup"><span data-stu-id="a414f-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="a414f-341">![Niðurstöður prófunar í Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Skjámynd af niðurstöðum prófsframkvæmda í Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="a414f-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="a414f-342">Hermdu eftir aðstæðum þar sem prófanir mistakast</span><span class="sxs-lookup"><span data-stu-id="a414f-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="a414f-343">Þessi prófunarpakki verður að misheppnast þegar að minnsta kosti eitt af mynduðum úttökum stemmir ekki við samsvarandi grunnlínu.</span><span class="sxs-lookup"><span data-stu-id="a414f-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="a414f-344">Til að ná þessum aðstæðum geturðu notað afleidda útgáfu þína af sniðinu **BACS (UK)** sem mun mynda greiðsluskrá sem hefur mismunandi efni en samsvarandi grunnlínu.</span><span class="sxs-lookup"><span data-stu-id="a414f-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="a414f-345">Til að líkja eftir þessum aðstæðum geturðu notað sama sniðið af **BACS (UK)** en breytt greiðsluupphæðinni á unninni greiðslulínu.</span><span class="sxs-lookup"><span data-stu-id="a414f-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="a414f-346">Opnaðu forritið og farðu í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="a414f-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="a414f-347">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="a414f-347">Select **Lines**.</span></span>
3. <span data-ttu-id="a414f-348">Veldu greiðslulínuna og veldu síðan **Greiðslustaða \> Enginn**.</span><span class="sxs-lookup"><span data-stu-id="a414f-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="a414f-349">Í reitnum **Debet** skaltu breyta gildinu úr **1.000,00** í **2.000,00**.</span><span class="sxs-lookup"><span data-stu-id="a414f-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="a414f-350">Veldu **Vista** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="a414f-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="a414f-351">Keyrðu prófanirnar í RSAT</span><span class="sxs-lookup"><span data-stu-id="a414f-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="a414f-352">Í RSAT veldurðu hlaðnar prófanir.</span><span class="sxs-lookup"><span data-stu-id="a414f-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="a414f-353">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="a414f-353">Select **Run**.</span></span>

<span data-ttu-id="a414f-354">Athugaðu að prófunardæmin eru sjálfkrafa keyrð í forritinu með því að nota vafra.</span><span class="sxs-lookup"><span data-stu-id="a414f-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="a414f-355">Greindu niðurstöður prófunarframkvæmdar</span><span class="sxs-lookup"><span data-stu-id="a414f-355">Analyze the results of test execution</span></span>

<span data-ttu-id="a414f-356">Niðurstöður prófunarinnar eru geymdar í RSAT.</span><span class="sxs-lookup"><span data-stu-id="a414f-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="a414f-357">Athugaðu að annað próf bilaði meðan á seinni framkvæmdinni stóð.</span><span class="sxs-lookup"><span data-stu-id="a414f-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="a414f-358">![Fallniðurstöður prófa í RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Skjámynd af fallniðurstöðum prófana í RSAT")</span><span class="sxs-lookup"><span data-stu-id="a414f-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="a414f-359">Athugaðu að niðurstöður prófunar eru einnig sendar til Azure DevOps svo að þú getir gert frekari greiningu.</span><span class="sxs-lookup"><span data-stu-id="a414f-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="a414f-360">![Fallniðurstöður prófa í Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Skjámynd af fallniðurstöðum prófana í Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="a414f-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="a414f-361">Þú getur fengið aðgang að stöðu hverrar prófunar.</span><span class="sxs-lookup"><span data-stu-id="a414f-361">You can access the status of each test.</span></span> <span data-ttu-id="a414f-362">Þú getur einnig nálgast framkvæmdakladdann þannig að þú greinir ástæður fyrir bilun.</span><span class="sxs-lookup"><span data-stu-id="a414f-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="a414f-363">Á eftirfarandi skýringarmynd sýnir framkvæmdakladdinn að bilun hafi átt sér stað út af muninum á innihaldi milli myndaðrar greiðsluskrár og grunnlínu hennar.</span><span class="sxs-lookup"><span data-stu-id="a414f-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="a414f-364">![Framkvæmdaskrá til að greina bilun í Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Skjámynd af framkvæmdaskránni til að greina bilun í Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="a414f-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="a414f-365">Eins og þú hefur séð, er þess vegna hægt að meta virkni ER-sniðs sjálfkrafa með því að nota RSAT sem prófunarvettvang og með því að nota prófunardæmi sem byggjast á verkskráningu og nota ER-grunnlínueiginleika.</span><span class="sxs-lookup"><span data-stu-id="a414f-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a414f-366">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a414f-366">Additional resources</span></span>

- [<span data-ttu-id="a414f-367">Tilföng verkskráningar</span><span class="sxs-lookup"><span data-stu-id="a414f-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="a414f-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="a414f-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="a414f-369">Stofna samþykkisprófun notanda og gera hana sjálfvirka</span><span class="sxs-lookup"><span data-stu-id="a414f-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="a414f-370">Beita og nota umhverfi sem styðja samfellda smíði og sjálfvirkni prófana</span><span class="sxs-lookup"><span data-stu-id="a414f-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="a414f-371">Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi</span><span class="sxs-lookup"><span data-stu-id="a414f-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="a414f-372">Rafræn skýrslugerð Uppfærðu snið með því að taka upp nýja grunnútgáfu sniðs</span><span class="sxs-lookup"><span data-stu-id="a414f-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="a414f-373">Rafræn skýrslugerð Flytja inn skilgreiningu úr Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a414f-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]