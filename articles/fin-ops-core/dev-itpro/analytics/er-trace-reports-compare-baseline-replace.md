---
title: Endurbætur á rakningu á niðurstöðum myndaðra rafrænna skýrslna og samanburður þeirra við grunnlínugildi
description: Þetta umræðuefni veitir upplýsingar um hvernig ER-grunnlínueiginleiki hefur verið endurbættur í Microsoft Dynamics 365 for Finance and Operations útgáfu 10.0.3 (júní, 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 45c0e3b569ca733ae3b70187633d2e84db5ecd87
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771167"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="44681-103">Endurbætur á rakningu á niðurstöðum myndaðra rafrænna skýrslna og samanburður þeirra við grunnlínugildi</span><span class="sxs-lookup"><span data-stu-id="44681-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="44681-104">Í þessu efni er fjallað um fyrsta sett endurbóta sem hafa verið gerðar á grunnlínueiginleika á ramma rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="44681-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="44681-105">Þessar endurbætur eru fáanlegar í Microsoft Dynamics 365 for Finance and Operations útgáfu 10.0.3 (júní, 2019) og nýrri.</span><span class="sxs-lookup"><span data-stu-id="44681-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="44681-106">Gera skilgreiningu á reglum grunnlína sjálfvirka</span><span class="sxs-lookup"><span data-stu-id="44681-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="44681-107">Efnisatriðið [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md) útskýrir hvernig á að skilgreina ER-ramma til að safna upplýsingum um framkvæmd ER-sniðs og meta niðurstöður þeirra framkvæmda.</span><span class="sxs-lookup"><span data-stu-id="44681-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="44681-108">Dæmið í þessu efni sýnir skrefin sem verður að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="44681-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="44681-109">Hér eru sum af skrefunum:</span><span class="sxs-lookup"><span data-stu-id="44681-109">Here are some of the steps:</span></span>

- <span data-ttu-id="44681-110">Keyrðu ER-snið til að mynda skrá á útleið og geyma hana staðbundið.</span><span class="sxs-lookup"><span data-stu-id="44681-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="44681-111">Bættu staðbundnu skránni við sem viðhengi grunnlínunnar sem var bætt við fyrir ER-snið.</span><span class="sxs-lookup"><span data-stu-id="44681-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="44681-112">Skilgreina reglu grunnlínu fyrir viðbætta grunnlínu.</span><span class="sxs-lookup"><span data-stu-id="44681-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="44681-113">Þessi skilgreining inniheldur eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="44681-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="44681-114">Tilgreina þátt ER-sniðs sem er notað til að mynda skrá á útleið.</span><span class="sxs-lookup"><span data-stu-id="44681-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="44681-115">Veldu viðhengið sem vísar til myndaðrar skrár á útleið.</span><span class="sxs-lookup"><span data-stu-id="44681-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="44681-116">Þessi skref verður að gera handvirkt, jafnvel þótt nýja ER-getan geri kleift að þau séu sjálfvirk.</span><span class="sxs-lookup"><span data-stu-id="44681-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="44681-117">Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="44681-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="44681-118">Dæmi: Gera skilgreiningu á reglum grunnlína sjálfvirka</span><span class="sxs-lookup"><span data-stu-id="44681-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="44681-119">Til að ljúka skrefunum í þessu dæmi verður fyrst að ljúka skrefunum í dæminu í efnisatriðinu [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md), upp í gegnum kaflann „Bæta við nýrri grunnlínu fyrir uppsett ER-snið“.</span><span class="sxs-lookup"><span data-stu-id="44681-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="44681-120">Skoðaðu viðbótargrunnlínu</span><span class="sxs-lookup"><span data-stu-id="44681-120">Review added baseline</span></span>

1. <span data-ttu-id="44681-121">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="44681-122">Veldu **Grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="44681-123">Hnappurinn **Grunnlínur** á aðgerðarrúðunni er aðeins í boði þegar kveikt er á ER-notandafæribreytunni **Keyra í kembistillingum** fyrir núverandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="44681-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="44681-124">Grunnlínugildinu hefur verið bætt við fyrir valið snið **Snið til að læra ER-grunnlínur** en reglum grunnlína hefur ekki enn verið bætt við fyrir þessa grunnlínu.</span><span class="sxs-lookup"><span data-stu-id="44681-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="44681-125">![Síðan Grunnlínusnið rafrænnar skýrslugerðar](media/GER-BaselineSample-AddBaseline2.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")</span><span class="sxs-lookup"><span data-stu-id="44681-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="44681-126">Gera nýja grunnlínureglu</span><span class="sxs-lookup"><span data-stu-id="44681-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="44681-127">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="44681-128">Í trénu stækkarðu **Líkan til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="44681-129">Í trénu skaltu velja **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="44681-130">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="44681-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="44681-131">Í reitnum **Skrá kenni** slærðu inn **1**.</span><span class="sxs-lookup"><span data-stu-id="44681-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="44681-132">Stilltu valkostinn **Gera grunnslínukrár** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="44681-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="44681-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44681-133">Select **OK**.</span></span>
8. <span data-ttu-id="44681-134">Veldu **Grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-134">Select **Baselines**.</span></span>

    <span data-ttu-id="44681-135">![Síðan Grunnlínusnið rafrænnar skýrslugerðar](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")</span><span class="sxs-lookup"><span data-stu-id="44681-135">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="44681-136">Mynduð skrá á útleið hefur verið sjálfvirkt tengd við grunnlínu framkvæmds ER-sniðs.</span><span class="sxs-lookup"><span data-stu-id="44681-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="44681-137">Grunnlínureglunni hefur verið sjálfkrafa bætt við þessa grunnlínu og inniheldur einnig tilvísun í viðhengda skrá.</span><span class="sxs-lookup"><span data-stu-id="44681-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="44681-138">Í reitinn **Heiti** skal færa inn **Grunnlína 1**.</span><span class="sxs-lookup"><span data-stu-id="44681-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="44681-139">Í reitinn **Sía skráarheiti** slærðu inn **.xml**.</span><span class="sxs-lookup"><span data-stu-id="44681-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="44681-140">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="44681-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="44681-141">Keyrðu sniðið</span><span class="sxs-lookup"><span data-stu-id="44681-141">Run the format</span></span>

<span data-ttu-id="44681-142">Núna ertu tilbúin/n til að klára eftirstandandi skref í dæminu í efnisatriðinu [Rekja myndaðar skýrsluniðurstöður og beru þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md), byrjaðu á hlutanum „Keyra uppsett ER-snið og endurskoða kladdann til að greina niðurstöðurnar“.</span><span class="sxs-lookup"><span data-stu-id="44681-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="44681-143">Þegar þú eyðir sjálfvirkt viðbættri reglu grunnlínu á flipann **Grunnlínur** er tilvísuðu viðhengi ekki sjálfkrafa eytt.</span><span class="sxs-lookup"><span data-stu-id="44681-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="44681-144">Skilgreina grunnlínuna þannig að hún hunsar stöðugt að breyta hlutum ER-úttaks</span><span class="sxs-lookup"><span data-stu-id="44681-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="44681-145">Þegar ER-snið hefur verið sett upp til að innihalda upplýsingar sem er breytt þegar sniðið er keyrt, verður sniðið að vera nauðsynlegt til að nota ER-grunnlínueiginleikann til að bera niðurstöðurnar saman við grunnlínugildin.</span><span class="sxs-lookup"><span data-stu-id="44681-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="44681-146">Til dæmis geta upplýsingarnar verið vinnsludagsetning og tími eða einstakt auðkenni myndaðs skjals í mismunandi sniðum (altækt einkvæmt auðkenni \[GUID\], og svo framvegis).</span><span class="sxs-lookup"><span data-stu-id="44681-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="44681-147">Nýja ER-getan gerir þér kleift að skilgreina reglu grunnlínu þannig að hún hunsi breytanlega þætti í ER-sniði þegar sniðið er keyrt með það að markmiði að bera grunnlínugildin saman við niðurstöður á útfærslu sniðsins.</span><span class="sxs-lookup"><span data-stu-id="44681-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="44681-148">Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="44681-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="44681-149">Dæmi: Skilgreina grunnlínuna þannig að hún hunsar stöðugt að breyta hlutum ER-úttaks</span><span class="sxs-lookup"><span data-stu-id="44681-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="44681-150">Til að ljúka skrefunum í þessu dæmi verður fyrst að ljúka skrefunum í dæminu í efnisatriðinu [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="44681-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="44681-151">Breyta skilgreindu ER-sniði</span><span class="sxs-lookup"><span data-stu-id="44681-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="44681-152">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="44681-153">Í trénu stækkarðu **Líkan til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="44681-154">Í trénu skaltu velja **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="44681-155">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="44681-155">Select **Designer**.</span></span>
5. <span data-ttu-id="44681-156">Í trénu velurðu **Úttak\\Skrá**.</span><span class="sxs-lookup"><span data-stu-id="44681-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="44681-157">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="44681-157">Select **Add**.</span></span>
7. <span data-ttu-id="44681-158">Í fellilistanum í trénu velurðu **XML\\Eigind**.</span><span class="sxs-lookup"><span data-stu-id="44681-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="44681-159">Í reitinn **Heiti** slærðu inn **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="44681-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="44681-160">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44681-160">Select **OK**.</span></span>
10. <span data-ttu-id="44681-161">Á flipann **Vörpun** í trénu velurðu **Úttak\\Skjal\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="44681-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="44681-162">Veljið **Breyta formúlu**.</span><span class="sxs-lookup"><span data-stu-id="44681-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="44681-163">Í reitnum **Formúla** skráirðu eftirfarandi segð: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="44681-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="44681-164">Veldu **Vista** og síðan **Prófa**.</span><span class="sxs-lookup"><span data-stu-id="44681-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="44681-165">Veldu **Prófa** aftur til að endurprófa skilgreinda segð.</span><span class="sxs-lookup"><span data-stu-id="44681-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="44681-166">![Síðan Formúluhönnuður](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Skjámynd af síðunni Formúluhönnuður")</span><span class="sxs-lookup"><span data-stu-id="44681-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="44681-167">Flipinn **Prófa niðurstöðu** sýnir að skilgreind segð skilar mismunandi dagsetningu og tíma í hvert skipti sem það er kallað.</span><span class="sxs-lookup"><span data-stu-id="44681-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="44681-168">Lokaðu síðunni **Formúluhönnuður** og veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="44681-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="44681-169">![Síða sniðshönnuðar](media/GER-BaselineSample-FormatMappingDesign2.PNG "Skjámynd af síðunni Sniðmátahönnuður")</span><span class="sxs-lookup"><span data-stu-id="44681-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="44681-170">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="44681-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="44681-171">Fjarlægðu núverandi grunnlínureglu</span><span class="sxs-lookup"><span data-stu-id="44681-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="44681-172">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="44681-173">Veldu **Grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="44681-174">Í lista yfir grunnlínur skaltu velja grunnlínuna sem er skilgreint fyrir sniðið **Snið til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="44681-175">Á flýtiflipanum **Grunnlínur** velurðu **Eyða** til að fjarlægja grunnlínuregluna sem þú hefur stillt áður.</span><span class="sxs-lookup"><span data-stu-id="44681-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="44681-176">![Síðan Grunnlínusnið rafrænnar skýrslugerðar](media/GER-BaselineSample-AddBaseline3.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")</span><span class="sxs-lookup"><span data-stu-id="44681-176">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="44681-177">Skilgreindu skipti fyrir bindingu á hönnuðu ER-sniði</span><span class="sxs-lookup"><span data-stu-id="44681-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="44681-178">Á síðunni **Skilgreiningar**, á flýtiflipanum **Endurnýjanir** velurðu **Velja íhluti**.</span><span class="sxs-lookup"><span data-stu-id="44681-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="44681-179">Í íhlutatré sniðmáta víkkarðu út **Úttak**, síðan **Úttak\\Skjal** og velur síðan hakreitinn fyrir **Úttak\\Skjal\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="44681-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="44681-180">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44681-180">Select **OK**.</span></span>

<span data-ttu-id="44681-181">![Síðan Grunnlínusnið rafrænnar skýrslugerðar](media/GER-BaselineSample-AddBaseline4.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")</span><span class="sxs-lookup"><span data-stu-id="44681-181">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="44681-182">Íhluta valins ER-sniðs hefur verið bætt við lista yfir íhluti á flýtiflipanum **Endurnýjanir**.</span><span class="sxs-lookup"><span data-stu-id="44681-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="44681-183">Þegar ER-grunnsniðið er keyrt í kembiham mun bindingu sniðsins fyrir hvern íhluta verða skipt út fyrir bindinguna sem er sýnd í dálkinum **Binding**.</span><span class="sxs-lookup"><span data-stu-id="44681-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="44681-184">Til að breyta sjálfgefinni bindingu fyrir íhluti sem er skráður á flýtiflipanum **Endurnýjanir** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="44681-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="44681-185">Gera nýja grunnlínureglu</span><span class="sxs-lookup"><span data-stu-id="44681-185">Make a new baseline rule</span></span>

<span data-ttu-id="44681-186">Fylgdu leiðbeiningunum í „Dæmi: Gera skilgreiningu grunnlínureglna sjálfvirka“ sem er fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="44681-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="44681-187">Tilkynning varar við því að skrá á útleið hafi verið mynduð með því að nota grunnlínustillingar og að þvinguð endurnýjun á bindingum sniðs hafi átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="44681-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="44681-188">![Síðan Tilkynning um stillingar](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Skjámynd af tilkynningu á síðunni Skilgreiningar")</span><span class="sxs-lookup"><span data-stu-id="44681-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="44681-189">Hindraðu viðvaranir um að endurnýjun á bindingum sniðs</span><span class="sxs-lookup"><span data-stu-id="44681-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="44681-190">Með því að stilla sérstakar ER-breytur er hægt að bæla tilkynningar sem vara við endurnýjun á sniðmátsbindingum.</span><span class="sxs-lookup"><span data-stu-id="44681-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="44681-191">Þessi bæling getur verið gagnleg þegar sniðmátsbindingar eru endurnýjaðar í eftirlitslausum ham með því að nota Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="44681-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="44681-192">Í þessu tilviki getur viðvörunin talist bilun á prófunartilfellinu sem er í gangi.</span><span class="sxs-lookup"><span data-stu-id="44681-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="44681-193">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **Skilgreiningar**, velurðu **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="44681-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="44681-194">Stilltu valkostinn **Hindra grunnlínuviðvaranir** á **Já** og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44681-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="44681-195">Yfirfara myndaða grunnlínuskrá</span><span class="sxs-lookup"><span data-stu-id="44681-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="44681-196">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="44681-197">Veldu **Grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="44681-198">Veldu **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="44681-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="44681-199">Mynduð skrá inniheldur texta vinnsludagsetningar og tíma (**„#“**) úr bindingu sem var stillt í viðbættri reglu grunnlínu, ekki úr bindingu sniðsins.</span><span class="sxs-lookup"><span data-stu-id="44681-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="44681-200">Lokaðu síðunni **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="44681-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="44681-201">Keyrðu uppsett ER-snið og endurskoðaðu skrána til að greina niðurstöðurnar</span><span class="sxs-lookup"><span data-stu-id="44681-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="44681-202">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="44681-203">Í trénu stækkarðu **Líkan til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="44681-204">Í trénu skaltu velja **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.</span><span class="sxs-lookup"><span data-stu-id="44681-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="44681-205">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="44681-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="44681-206">Í reitnum **Skrá kenni** ritarðu **1**.</span><span class="sxs-lookup"><span data-stu-id="44681-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="44681-207">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44681-207">Select **OK**.</span></span>
7. <span data-ttu-id="44681-208">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Kembingarkladdar skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="44681-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="44681-209">Framkvæmdakladdinn inniheldur upplýsingar um niðurstöður samanburðar á myndaðri skrá við skilgreinda grunnlínu.</span><span class="sxs-lookup"><span data-stu-id="44681-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="44681-210">Kladdinn gefur til kynna að mynduð skrá og grunnlínan séu eins, jafnvel þó að framkvæmt snið innihaldi bindingu til að færa inn síbreytileg dags.- og tímagildi í skrána á útleið.</span><span class="sxs-lookup"><span data-stu-id="44681-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="44681-211">Þó að skrá á útleið hafi verið mynduð með því að nota grunnlínustillingar sem þvinga endurnýjun á bindingu sniðsins, færðu engar viðvaranir um endurnýjunina.</span><span class="sxs-lookup"><span data-stu-id="44681-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="44681-212">Skipta um grunnlínustillingar á milli umhverfa</span><span class="sxs-lookup"><span data-stu-id="44681-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="44681-213">Flytja út grunnlínustillingar</span><span class="sxs-lookup"><span data-stu-id="44681-213">Export baseline settings</span></span>

<span data-ttu-id="44681-214">Nýja ER-getan gerir þér kleift að flytja út grunnlínustillingar fyrir valið ER-snið úr núverandi umhverfi og geyma þær sem XML-skrár.</span><span class="sxs-lookup"><span data-stu-id="44681-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="44681-215">Til að flytja út grunnstillingar skaltu á síðunni **Grunnlínusnið rafrænnar skýrslugerðar** velja **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="44681-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="44681-216">Flytja inn grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="44681-216">Import baseline settings</span></span>

<span data-ttu-id="44681-217">Útfluttar grunnlínustillingar má flytja inn í mismunandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="44681-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="44681-218">Fyrst verður að flytja umhverfið inn sem ER-snið.</span><span class="sxs-lookup"><span data-stu-id="44681-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="44681-219">Síðan geturðu flutt grunnlínustillingar.</span><span class="sxs-lookup"><span data-stu-id="44681-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="44681-220">Til að flytja inn grunnlínustillingar úr staðbundið vistaðri XML-skrá skaltu á síðunni **Grunnlínur rafrænnar skýrslugerðar** velja **Flytja inn** og síðan **Skoða** til að velja XML-skrána.</span><span class="sxs-lookup"><span data-stu-id="44681-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="44681-221">![Svarglugginn Flytja inn grunnstillingar](media/GER-BaselineSample-ImportBaseline1.PNG "Skjámynd af svarglugganum Innflutningur á grunnlínustillingum")</span><span class="sxs-lookup"><span data-stu-id="44681-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="44681-222">Til að flytja inn grunnlínustillingar úr XML-skrá sem er geymd á Microsoft SharePoint-þjóni, byggð á núverandi skjalastjórnunarstillingum og völdum skjalategundum, skaltu á síðunni **Grunnlínur rafræns skýrslugerðarsniðs** velja **Flytja inn úr uppruna**.</span><span class="sxs-lookup"><span data-stu-id="44681-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="44681-223">Veldu síðan gerð skjalsins og XML-skrána.</span><span class="sxs-lookup"><span data-stu-id="44681-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="44681-224">Tilskilin skjalagerð til að fá aðgang að SharePoint-möppunni verður að vera skilgreind fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="44681-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="44681-225">![Flytja inn úr svarglugga uppruna](media/GER-BaselineSample-ImportBaseline2.PNG "Skjámynd af svarglugganum Innflutningur úr uppruna")</span><span class="sxs-lookup"><span data-stu-id="44681-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="44681-226">Þú getur notað verkskráningu til að skrá skrefin til að velja nauðsynlega skjalagerð og skráarheiti í svarglugganum **Flytja inn úr uppruna**.</span><span class="sxs-lookup"><span data-stu-id="44681-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="44681-227">Þannig geturðu haldið nauðsynlegum grunnlínustillingum á SharePoint-þjóninum og flutt þær síðan sjálfvirkt inn með því að spila verkskráninguna þegar þú keyrir sjálfvirk próf með því að nota Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="44681-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44681-228">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="44681-228">Additional resources</span></span>

- [<span data-ttu-id="44681-229">Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi</span><span class="sxs-lookup"><span data-stu-id="44681-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="44681-230">Tilföng verkskráningar</span><span class="sxs-lookup"><span data-stu-id="44681-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)
