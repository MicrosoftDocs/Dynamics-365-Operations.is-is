---
title: Stilla landssamhengisháðar varpanir ER-líkans
description: Þetta efni útskýrir hvernig þú getur sett upp ER-líkanavarpanir svo þær séu háðar samhengi lands/landsvæðis lögaðilans sem stjórnar notkun þeirra.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 48d2e3c81d038cc55f6f100f3081561506946199
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562287"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="6bac1-103">Stilla landssamhengisháðar varpanir ER-líkans</span><span class="sxs-lookup"><span data-stu-id="6bac1-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6bac1-104">Þú getur stillt líkanavarpanir rafrænnar skýrslugerðar (ER) þannig að þau innleiða almennt ER gagnalíkan en eru sértæk fyrir Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6bac1-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="6bac1-105">Þetta efnisatriði útskýrir hvernig á að hanna margar ER-líkanavarpanir fyrir ER-gagnalíkan til að stjórna því hvernig þær eru notaðar af samsvarandi ER-sniðum sem eru keyrð úr fyrirtækjum sem hafa mismunandi lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6bac1-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="6bac1-106">Prerequisites</span></span>

<span data-ttu-id="6bac1-107">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="6bac1-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="6bac1-108">Aðgangur að Finance fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="6bac1-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="6bac1-109">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="6bac1-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="6bac1-110">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6bac1-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6bac1-111">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="6bac1-111">System administrator</span></span>

- <span data-ttu-id="6bac1-112">Aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="6bac1-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="6bac1-113">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="6bac1-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="6bac1-114">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6bac1-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6bac1-115">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="6bac1-115">System administrator</span></span>

<span data-ttu-id="6bac1-116">Sum skref í þessu efni þurfa að framkvæma ER snið.</span><span class="sxs-lookup"><span data-stu-id="6bac1-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="6bac1-117">Í sumum tilvikum verður framkvæmd á ER-sniði fyrir áhrifum af lands-/svæðissamhengi fyrirtækisins sem þú ert skráð (ur) inn á.</span><span class="sxs-lookup"><span data-stu-id="6bac1-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="6bac1-118">Þú getur keyrt ER snið í núverandi RCS tilviki ef fyrirtækið sem hefur tilskilið lands-/svæðissamhengi er fáanlegt í RCS.</span><span class="sxs-lookup"><span data-stu-id="6bac1-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="6bac1-119">Annars verður þú að hlaða upp lokinni útgáfu af stillingum á ER-líkanavörpunum og ER-sniðum sem nota ER-gagnalíkanið í tilviki þínu af Finance og keyra síðan ER sniðið í því tilviki af Finance.</span><span class="sxs-lookup"><span data-stu-id="6bac1-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="6bac1-120">Nánari upplýsingar um hvernig á að flytja inn stillingar sem eru í RCS í tilvik af Finance er að finna í [Flytja inn stillingar úr RCS](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="6bac1-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="6bac1-121">Stakt dæmi um líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="6bac1-121">Single model mapping case</span></span>

<span data-ttu-id="6bac1-122">Fylgdu skrefunum í [Viðauki 1](#appendix1) af þessu efni til að hanna nauðsynlega ER íhluti.</span><span class="sxs-lookup"><span data-stu-id="6bac1-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="6bac1-123">Núna ertu með stillingu líkanavörpunar **Vörpun (almennt)** sem inniheldur líkanavörpun fyrir skilgreininguna **Inngangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="6bac1-125">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="6bac1-125">Run the configured format</span></span>

1.  <span data-ttu-id="6bac1-126">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="6bac1-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-127">Select **OK**.</span></span>

<span data-ttu-id="6bac1-128">Taktu eftir að vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6bac1-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="6bac1-129">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og aðeins stök líkanavörpun er nú fáanleg fyrir grunnlíkanið sem inniheldur vörpun fyrir þessa skilgreiningu notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt)** í skilgreiningunni **Vörpun (almennt)** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6bac1-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="6bac1-130">Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="6bac1-131">Margvísleg samnýting á vörpunardæmi líkana</span><span class="sxs-lookup"><span data-stu-id="6bac1-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="6bac1-132">Fylgdu skrefunum í [Viðauki 2](#appendix2) af þessu efni til að hanna nauðsynlega ER íhluti.</span><span class="sxs-lookup"><span data-stu-id="6bac1-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="6bac1-133">Núna ertu með stillingar líkanavörpunar **Vörpun (almennt)** og **Vörpun (almennt) sérsnið** sem inniheldur hvor fyrir sig líkanavörpun fyrir skilgreininguna **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="6bac1-135">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="6bac1-135">Run the configured format</span></span>

1.  <span data-ttu-id="6bac1-136">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="6bac1-137">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="6bac1-138">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-138">Select **OK**.</span></span>

<span data-ttu-id="6bac1-139">Taktu eftir að framkvæmd á völdu ER sniði tókst ekki.</span><span class="sxs-lookup"><span data-stu-id="6bac1-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="6bac1-140">Villuboð upplýsa þig um að fleiri en ein gerð vörpunar er til fyrir líkanið **Líkan til að læra varpanir** og skilgreininguna **Aðgangsstaður 1** á stillingum líkanavarpana **Kortlagning (almennt)** og **Kortlagning (almenn) sérsniðin**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="6bac1-141">Skilaboðin mæla einnig með að þú veljir eina af þessum stillingum sem sjálfgefna stillingu.</span><span class="sxs-lookup"><span data-stu-id="6bac1-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="6bac1-143">Skilgreindu sjálfgefna líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="6bac1-143">Define a default mapping configuration</span></span>

<span data-ttu-id="6bac1-144">Fylgdu þessum skrefum til að skilgreina stillingu líkanavörpunar **Kortlagning (almenn) sérsniðin** sem sjálfgefna stillingu, svo að hægt sé að nota varpanir hennar sem gagnagjafa fyrir ER-sniðið **Snið til að læra vörpun**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="6bac1-145">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt) sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="6bac1-146">Veldu eftir þörfum **Breyta** til að gera þessa síðu tilbúna til að breyta.</span><span class="sxs-lookup"><span data-stu-id="6bac1-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="6bac1-147">Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="6bac1-148">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-148">Select **Save**.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="6bac1-150">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="6bac1-150">Run the configured format</span></span>

1.  <span data-ttu-id="6bac1-151">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="6bac1-152">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="6bac1-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-153">Select **OK**.</span></span>

<span data-ttu-id="6bac1-154">Taktu eftir að framkvæmd á völdu ER sniði tókst.</span><span class="sxs-lookup"><span data-stu-id="6bac1-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="6bac1-155">Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6bac1-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="6bac1-156">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (almennt) sérsnið** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt) afrit** í skilgreiningunni **Vörpun (almennt) sérsnið** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6bac1-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="6bac1-157">Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1 sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="6bac1-158">Ef þú skiptir um fyrirtæki sem þú ert skráð/ur inn í og keyrir þetta ER snið aftur, þá færðu sama innihaldið í myndinni, vegna þess að sjálfgefna uppsetning ER gerðanna inniheldur engar fyrirtækjaháðar hömlur.</span><span class="sxs-lookup"><span data-stu-id="6bac1-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="6bac1-159">Mörg blönduð vörpunardæmi líkana</span><span class="sxs-lookup"><span data-stu-id="6bac1-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="6bac1-160">Fylgdu skrefunum í [Viðauki 3](#appendix3) af þessu efni til að hanna nauðsynlega ER íhluti.</span><span class="sxs-lookup"><span data-stu-id="6bac1-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="6bac1-161">Núna ertu með stillingar **Vörpun (almennt)**, **Vörpun (almennt) sérsnið** og **Vörpun (FR) líkanavörpunar** sem innihalda líkanavörpun fyrir skilgreininguna **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="6bac1-162">Taktu eftir að útgáfa 1 af stillingu líkanavörpunar **Vörpun (FR)** er þannig stillt að hún á aðeins við um ER-snið í líkaninu **Líkan til að læra varpanir** sem eru keyrði í fjármálafyrirtækjum sem hafa franskt lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="6bac1-164">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="6bac1-164">Run the configured format</span></span>

1.  <span data-ttu-id="6bac1-165">Breyttu fyrirtækinu í **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="6bac1-166">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="6bac1-167">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="6bac1-168">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-168">Select **OK**.</span></span>

<span data-ttu-id="6bac1-169">Taktu eftir að framkvæmd á völdu ER sniði tókst.</span><span class="sxs-lookup"><span data-stu-id="6bac1-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="6bac1-170">Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6bac1-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="6bac1-171">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (almennt) sérsnið** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt) afrit** í skilgreiningunni **Vörpun (almennt) sérsnið** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6bac1-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="6bac1-172">Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1 sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="6bac1-173">Tilgreindu líkanastillingar sem eru sértækar fyrir Frakkland sem sjálfgefna stillingu</span><span class="sxs-lookup"><span data-stu-id="6bac1-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="6bac1-174">Fylgdu þessum skrefum til að skilgreina sérsniðna líkanavörpunarstillingu **Vörpun (FR)** sem sjálfgefna stillingu.</span><span class="sxs-lookup"><span data-stu-id="6bac1-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="6bac1-175">Athugaðu að vegna þess að þessi vörpun er sértæk fyrir Frakkland verður hún talin sjálfgefin vörpun milli allra stillinga líkanavarpana sem hafa landskóðann **FR** sem tilgreindur er í reitnum **ISO lands-/svæðiskóðar**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="6bac1-176">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (FR)**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="6bac1-177">Veldu eftir þörfum **Breyta** til að gera þessa síðu tilbúna til að breyta.</span><span class="sxs-lookup"><span data-stu-id="6bac1-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="6bac1-178">Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="6bac1-179">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-179">Select **Save**.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="6bac1-181">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="6bac1-181">Run the configured format</span></span>

1.  <span data-ttu-id="6bac1-182">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="6bac1-183">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="6bac1-184">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-184">Select **OK**.</span></span>

<span data-ttu-id="6bac1-185">Taktu eftir að framkvæmd á völdu ER sniði tókst.</span><span class="sxs-lookup"><span data-stu-id="6bac1-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="6bac1-186">Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="6bac1-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="6bac1-187">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (FR)** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (FR)** í skilgreiningunni **Vörpun (FR)** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6bac1-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="6bac1-188">Þess vegna inniheldur niðurflutt skrá textann **FR virkni 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="6bac1-189">Ef þú skiptir um fyrirtæki sem þú ert skráð/ur inn í og keyrir þetta ER snið aftur mun framleiðslan fara eftir samhengi lands-/svæðis valins fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="6bac1-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="6bac1-190">Önnur dæmi um líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="6bac1-190">Other model mapping cases</span></span>

<span data-ttu-id="6bac1-191">Eins og þú hefur séð virkar val á líkanavörpun til framkvæmdar á ER sniði á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6bac1-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="6bac1-192">Skilgreining á líkanavörpun sem ER snið notar er tilgreind (**Aðgangsstaður 1** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="6bac1-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="6bac1-193">Hægt er að nota allar vörpunarstillingar sem innihalda vörpun sem hefur tilgreinda skilgreiningu og fullnægja samhengishömlum landa/svæða sem eru uppsettar til að keyra ER snið (**Vörpun (almennt)**, **Vörpun (almenn) sérsniðin** og **Vörpun (FR)** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="6bac1-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="6bac1-194">Sérhver sjálfgefin vörpun líkana sem hefur takmarkanir á landi/svæðum hefur forgangsröðun fyrir val (**Vörpun (FR)** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="6bac1-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="6bac1-195">Sérhver sjálfgefin vörpun líkana sem hefur ekki takmarkanir á landi/svæðum hefur næsthæstu forgangsröðun fyrir val (**Vörpun (almennt) sérsnið** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="6bac1-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="6bac1-196">Sérhver líkanakortlagning sem hefur takmarkanir á landi/svæðum hefur meiri forgang við val en vörpun líkana sem eru ekki með samhengi takmarkana á landi/svæðum.</span><span class="sxs-lookup"><span data-stu-id="6bac1-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="6bac1-197">Eftirfarandi tafla veitir upplýsingar um niðurstöður val á líkanavörpun fyrir öll möguleg tilvik fyrir líkanavarpanastillingar:</span><span class="sxs-lookup"><span data-stu-id="6bac1-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="6bac1-198">Dálkur 1 gefur til kynna hvort fyrsta vörpun líkansins sem hefur ekki takmarkanir á samhengi landa/svæða (til dæmis samnýtta líkanið **Vörpun (almennt)**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="6bac1-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="6bac1-199">Dálkur 2 gefur til kynna hvort önnur vörpun líkansins sem hefur ekki takmarkanir á samhengi landa/svæða (til dæmis samnýtta líkanið **Vörpun (almennt) sérsnið**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="6bac1-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="6bac1-200">Dálkur 3 gefur til kynna hvort fyrsta vörpun líkansins sem hefur takmarkanir á samhengi landa/svæða A (til dæmis Frakklands-sértæka líkanið **Vörpun (FR)**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="6bac1-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="6bac1-201">Dálkur 4 gefur til kynna hvort önnur vörpun líkansins sem hefur takmarkanir á samhengi landa/svæða A (til dæmis Frakklands-sértæka líkanið Vörpun (FR)) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="6bac1-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="6bac1-202">Dálkur 5 sýnir niðurstöðu úr vali á líkanavörpun fyrir framkvæmd á ER sniði undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi A.</span><span class="sxs-lookup"><span data-stu-id="6bac1-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="6bac1-203">Dálkur 6 sýnir niðurstöðu úr vali á líkanavörpun fyrir framkvæmd á ER sniði undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi B.</span><span class="sxs-lookup"><span data-stu-id="6bac1-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="6bac1-204">Í töflunni bendir plúsmerki (+) til að til sé stilling líkanavörpunar í núverandi tilviki Microsoft Azure þjónustu sem er notuð til að keyra ER snið (annaðhvort Finance eða RCS).</span><span class="sxs-lookup"><span data-stu-id="6bac1-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="6bac1-205">Tilvik</span><span class="sxs-lookup"><span data-stu-id="6bac1-205">Case</span></span> | <span data-ttu-id="6bac1-206">Líkanavörpun 1 án samhengis lands/svæðis (MM1)</span><span class="sxs-lookup"><span data-stu-id="6bac1-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="6bac1-207">Líkanavörpun 2 án samhengis lands/svæðis (MM2)</span><span class="sxs-lookup"><span data-stu-id="6bac1-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="6bac1-208">Líkanavörpun 1 með samhengi lands/svæðis A (MM1A)</span><span class="sxs-lookup"><span data-stu-id="6bac1-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="6bac1-209">Líkanavörpun 2 með samhengi lands/svæðis A (MM2A)</span><span class="sxs-lookup"><span data-stu-id="6bac1-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="6bac1-210">Keyra undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi A</span><span class="sxs-lookup"><span data-stu-id="6bac1-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="6bac1-211">Keyra undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi B</span><span class="sxs-lookup"><span data-stu-id="6bac1-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="6bac1-212">1</span><span class="sxs-lookup"><span data-stu-id="6bac1-212">1</span></span>   |     <span data-ttu-id="6bac1-213">2</span><span class="sxs-lookup"><span data-stu-id="6bac1-213">2</span></span>   |    <span data-ttu-id="6bac1-214">3</span><span class="sxs-lookup"><span data-stu-id="6bac1-214">3</span></span>    |    <span data-ttu-id="6bac1-215">4</span><span class="sxs-lookup"><span data-stu-id="6bac1-215">4</span></span>    |           <span data-ttu-id="6bac1-216">5</span><span class="sxs-lookup"><span data-stu-id="6bac1-216">5</span></span>               |            <span data-ttu-id="6bac1-217">6</span><span class="sxs-lookup"><span data-stu-id="6bac1-217">6</span></span>               |
|     <span data-ttu-id="6bac1-218">1</span><span class="sxs-lookup"><span data-stu-id="6bac1-218">1</span></span>   |         |         |         |         | <span data-ttu-id="6bac1-219">Villa (vantar vörpun)</span><span class="sxs-lookup"><span data-stu-id="6bac1-219">Error (missing mapping)</span></span>   | <span data-ttu-id="6bac1-220">Villa (vantar vörpun)</span><span class="sxs-lookup"><span data-stu-id="6bac1-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="6bac1-221">2</span><span class="sxs-lookup"><span data-stu-id="6bac1-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="6bac1-222">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-222">MM1</span></span>                       | <span data-ttu-id="6bac1-223">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-223">MM1</span></span>                        |
|     <span data-ttu-id="6bac1-224">3</span><span class="sxs-lookup"><span data-stu-id="6bac1-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="6bac1-225">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="6bac1-225">Error (multiple mappings)</span></span> | <span data-ttu-id="6bac1-226">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="6bac1-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="6bac1-227">4</span><span class="sxs-lookup"><span data-stu-id="6bac1-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="6bac1-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-228">MM1A</span></span>                      | <span data-ttu-id="6bac1-229">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-229">MM1</span></span>                        |
|     <span data-ttu-id="6bac1-230">5</span><span class="sxs-lookup"><span data-stu-id="6bac1-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="6bac1-231">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="6bac1-231">Error (multiple mappings)</span></span> | <span data-ttu-id="6bac1-232">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-232">MM1</span></span>                        |
|     <span data-ttu-id="6bac1-233">6</span><span class="sxs-lookup"><span data-stu-id="6bac1-233">6</span></span>   |     +   | <span data-ttu-id="6bac1-234">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-234">default</span></span> |    +    |    +    | <span data-ttu-id="6bac1-235">MM2</span><span class="sxs-lookup"><span data-stu-id="6bac1-235">MM2</span></span>                       | <span data-ttu-id="6bac1-236">MM2</span><span class="sxs-lookup"><span data-stu-id="6bac1-236">MM2</span></span>                        |
|     <span data-ttu-id="6bac1-237">7</span><span class="sxs-lookup"><span data-stu-id="6bac1-237">7</span></span>   |     +   |         | <span data-ttu-id="6bac1-238">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-238">default</span></span> |         | <span data-ttu-id="6bac1-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-239">MM1A</span></span>                      | <span data-ttu-id="6bac1-240">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-240">MM1</span></span>                        |
|     <span data-ttu-id="6bac1-241">8</span><span class="sxs-lookup"><span data-stu-id="6bac1-241">8</span></span>   |     +   |         | <span data-ttu-id="6bac1-242">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-242">default</span></span> |    +    | <span data-ttu-id="6bac1-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-243">MM1A</span></span>                      | <span data-ttu-id="6bac1-244">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-244">MM1</span></span>                        |
|     <span data-ttu-id="6bac1-245">9</span><span class="sxs-lookup"><span data-stu-id="6bac1-245">9</span></span>   |     +   |         | <span data-ttu-id="6bac1-246">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-246">default</span></span> | <span data-ttu-id="6bac1-247">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-247">default</span></span> | <span data-ttu-id="6bac1-248">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="6bac1-248">Error (multiple mappings)</span></span> | <span data-ttu-id="6bac1-249">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-249">MM1</span></span>                        |
|    <span data-ttu-id="6bac1-250">10</span><span class="sxs-lookup"><span data-stu-id="6bac1-250">10</span></span>   | <span data-ttu-id="6bac1-251">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-251">default</span></span> |         |         |         | <span data-ttu-id="6bac1-252">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-252">MM1</span></span>                       | <span data-ttu-id="6bac1-253">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-253">MM1</span></span>                        |
|    <span data-ttu-id="6bac1-254">11</span><span class="sxs-lookup"><span data-stu-id="6bac1-254">11</span></span>   | <span data-ttu-id="6bac1-255">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-255">default</span></span> |    +    |         |         | <span data-ttu-id="6bac1-256">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-256">MM1</span></span>                       | <span data-ttu-id="6bac1-257">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-257">MM1</span></span>                        |
|    <span data-ttu-id="6bac1-258">12</span><span class="sxs-lookup"><span data-stu-id="6bac1-258">12</span></span>   | <span data-ttu-id="6bac1-259">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-259">default</span></span> |         |    +    |         | <span data-ttu-id="6bac1-260">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-260">MM1</span></span>                       | <span data-ttu-id="6bac1-261">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-261">MM1</span></span>                        |
|    <span data-ttu-id="6bac1-262">13</span><span class="sxs-lookup"><span data-stu-id="6bac1-262">13</span></span>   | <span data-ttu-id="6bac1-263">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-263">default</span></span> | <span data-ttu-id="6bac1-264">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-264">default</span></span> |         |         | <span data-ttu-id="6bac1-265">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="6bac1-265">Error (multiple mappings)</span></span> | <span data-ttu-id="6bac1-266">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="6bac1-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="6bac1-267">14</span><span class="sxs-lookup"><span data-stu-id="6bac1-267">14</span></span>   | <span data-ttu-id="6bac1-268">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-268">default</span></span> |         | <span data-ttu-id="6bac1-269">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-269">default</span></span> |         | <span data-ttu-id="6bac1-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-270">MM1A</span></span>                      | <span data-ttu-id="6bac1-271">MM1</span><span class="sxs-lookup"><span data-stu-id="6bac1-271">MM1</span></span>                        |
|    <span data-ttu-id="6bac1-272">15</span><span class="sxs-lookup"><span data-stu-id="6bac1-272">15</span></span>   | <span data-ttu-id="6bac1-273">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-273">default</span></span> |         | <span data-ttu-id="6bac1-274">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-274">default</span></span> | <span data-ttu-id="6bac1-275">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-275">default</span></span> | <span data-ttu-id="6bac1-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-276">MM1A</span></span>                      | <span data-ttu-id="6bac1-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="6bac1-277">MM2A</span></span>                       |
|    <span data-ttu-id="6bac1-278">16</span><span class="sxs-lookup"><span data-stu-id="6bac1-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="6bac1-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-279">MM1A</span></span>                      | <span data-ttu-id="6bac1-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="6bac1-280">MM2A</span></span>                       |
|    <span data-ttu-id="6bac1-281">17</span><span class="sxs-lookup"><span data-stu-id="6bac1-281">17</span></span>   |         |         | <span data-ttu-id="6bac1-282">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-282">default</span></span> | <span data-ttu-id="6bac1-283">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="6bac1-283">default</span></span> | <span data-ttu-id="6bac1-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="6bac1-284">MM1A</span></span>                      | <span data-ttu-id="6bac1-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="6bac1-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="6bac1-286">Lærðu hvaða vörpun var notuð við framkvæmd ER sniðs</span><span class="sxs-lookup"><span data-stu-id="6bac1-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="6bac1-287">Skilgreina færibreytur notanda rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6bac1-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="6bac1-288">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **CONFIGURATIONS**, velurðu **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="6bac1-289">Stilltu valkostinn **Keyra í kembistillingum** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="6bac1-290">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="6bac1-291">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="6bac1-291">Run the configured format</span></span>

1.  <span data-ttu-id="6bac1-292">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="6bac1-293">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="6bac1-294">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="6bac1-295">Skoðaðu villuleitarskrá ER</span><span class="sxs-lookup"><span data-stu-id="6bac1-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="6bac1-296">Farðu í **Einingar \> Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Kembingarkladdar skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="6bac1-297">Veldu hnappinn **Endurhlaða þessa síðu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-297">Select the **Reload this page** button.</span></span>

![Síðan ER-keyrsluskrár](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="6bac1-299">Taktu eftir að nýrri skrá hefur verið bætt við ER kembiforrit fyrir keyrð ER snið.</span><span class="sxs-lookup"><span data-stu-id="6bac1-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="6bac1-300">Þar sem reiturinn **Stig** í þessari skrár er stilltur á **Upplýsingar** er skráin upplýsandi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="6bac1-301">Þar sem reiturinn Sniðsíhlutur er stilltur á **Vörpunarstilling** upplýsir skráin þig um líkanavörpun sem var notuð við framkvæmd á ER-sniðinu **Snið til að læra vörpun** (valið í reitnum **Stillingarheiti**).</span><span class="sxs-lookup"><span data-stu-id="6bac1-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="6bac1-302">Innihald reitsins **Myndaður texti** upplýsir þig um að vörpunarhlutinn **Vörpun (FR)** sem er staðsett í stillingunni **Vörpun (FR)** hefur verið notaður til að keyra þessa skýrslu.</span><span class="sxs-lookup"><span data-stu-id="6bac1-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix-1"></a><a name="appendix1"></a> <span data-ttu-id="6bac1-303">Viðauki 1</span><span class="sxs-lookup"><span data-stu-id="6bac1-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="6bac1-304">Stilltu sýnishorn gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="6bac1-304">Configure a sample data model</span></span>

<span data-ttu-id="6bac1-305">Skráðu þig inn á RCS tilvikið.</span><span class="sxs-lookup"><span data-stu-id="6bac1-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="6bac1-306">Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Til að ljúka þessum skrefum verður fyrst í RCS að ljúka skrefum ferlisins [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="6bac1-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="6bac1-307">Stofna nýjan skilgreiningu ER-gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="6bac1-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="6bac1-308">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="6bac1-309">Veldu reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="6bac1-310">Á síðunni **Skilgreiningar** skal velja **Stofna stillingu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="6bac1-311">Í fellilistanum, í reitnum **Heiti**, slærðu inn **Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="6bac1-312">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="6bac1-313">Veldu flýtiflipann **Stillingarhlutar**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="6bac1-314">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="6bac1-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="6bac1-315">Þessi útgáfa inniheldur íhluta gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="6bac1-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="6bac1-316">Hanna sýnishorn gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="6bac1-316">Design a sample data model</span></span>

1.  <span data-ttu-id="6bac1-317">Á síðunni **Síðan skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="6bac1-318">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-318">Select **New**.</span></span>
3.  <span data-ttu-id="6bac1-319">Í fellilistanum, í reitnum **Heiti** slærðu inn **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="6bac1-320">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-320">Select **Add**.</span></span>
5.  <span data-ttu-id="6bac1-321">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-321">Select **New**.</span></span>
6.  <span data-ttu-id="6bac1-322">Í fellilistanum, í reitnum **Heiti**, slærðu inn **Lýsing á virkni**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="6bac1-323">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-323">Select **Add**.</span></span>
8.  <span data-ttu-id="6bac1-324">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-324">Select **New**.</span></span>
9.  <span data-ttu-id="6bac1-325">Í fellilistanum, í reitahópnum **Nýr hnútur**, velurðu **Líkanshnútur**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="6bac1-326">Í reitinn **Heiti** slærðu inn **Aðgangsstaður 2**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="6bac1-327">Veldu **Inngangsstaður 2**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="6bac1-328">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-328">Select **Add**.</span></span>
13. <span data-ttu-id="6bac1-329">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-329">Select **New**.</span></span>
14. <span data-ttu-id="6bac1-330">Í fellilistanum, í reitnum **Heiti**, slærðu inn **Lýsing á virkni**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="6bac1-331">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-331">Select **Add**.</span></span>

    ![Hönnuðarsíðan ER-gagnavörpun](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="6bac1-333">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-333">Select **Save**.</span></span>
17. <span data-ttu-id="6bac1-334">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="6bac1-335">Ljúka við breyttu útgáfuna af líkanastillingu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6bac1-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="6bac1-336">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="6bac1-337">Breyta stöðu hönnuðar líkanastillingar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að hanna nauðsynlegar varpanir og snið líkansins.</span><span class="sxs-lookup"><span data-stu-id="6bac1-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="6bac1-338">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="6bac1-339">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-339">Select **OK**.</span></span>

<span data-ttu-id="6bac1-340">Athugið að skilgreiningin sem þú stofnaðir er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="6bac1-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="6bac1-341">Stilltu sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="6bac1-342">Stofna grunnstillingu ER-líkansvörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="6bac1-343">Á síðunni **Skilgreiningar** skal velja **Stofna stillingu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="6bac1-344">Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Líkanavörpun byggð á gagnalíkaninu Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="6bac1-345">Í reitinn **Heiti** slærðu inn **Vörpun (almennt)**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="6bac1-346">Í reitnum **Skilgreining gagnalíkans** velurðu **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="6bac1-347">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-347">Select **Create configuration**.</span></span>

<span data-ttu-id="6bac1-348">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="6bac1-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="6bac1-349">Þessi útgáfa inniheldur íhluta líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="6bac1-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="6bac1-350">Hanna sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="6bac1-351">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="6bac1-352">Taktu eftir því að kortlagning líkansins á stefnugerðinni **Til líkans** hefur sjálfkrafa verið bætt við þennan íhlut fyrir skilgreininguna **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="6bac1-353">Veldu **Hönnuður** til að byrja að breyta viðbættri líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6bac1-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="6bac1-354">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="6bac1-355">Í reitinn **Formúla** skal færa inn **„Almenn virkni 1“**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="6bac1-356">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-356">Select **Save**.</span></span>
6.  <span data-ttu-id="6bac1-357">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-357">Close the **Formula designer** page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="6bac1-359">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-359">Select **Save**.</span></span>
8.  <span data-ttu-id="6bac1-360">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="6bac1-361">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-361">Select **New**.</span></span>
10. <span data-ttu-id="6bac1-362">Í reitnum **Skilgreining** velurðu **Aðgangsstaður 2**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="6bac1-363">Í reitinn **Heiti** slærðu inn **Vörpun (almennt) 2**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="6bac1-364">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-364">Select **Designer**.</span></span>
13. <span data-ttu-id="6bac1-365">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="6bac1-366">Í reitinn **Formúla** skal færa inn **„Almenn virkni 2“**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="6bac1-367">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-367">Select **Save**.</span></span>
16. <span data-ttu-id="6bac1-368">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-368">Close the **Formula designer** page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="6bac1-370">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-370">Select **Save**.</span></span>
18. <span data-ttu-id="6bac1-371">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-371">Close the **Model mapping designer** page.</span></span>

    ![Síðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="6bac1-373">Lokið síðunni **Líkanavarpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="6bac1-374">Ljúka við breyttu útgáfuna af stillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="6bac1-375">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="6bac1-376">Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="6bac1-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="6bac1-377">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="6bac1-378">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-378">Select **OK**.</span></span>

<span data-ttu-id="6bac1-379">Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="6bac1-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="6bac1-380">Stilla sýnissnið</span><span class="sxs-lookup"><span data-stu-id="6bac1-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="6bac1-381">Stofna skilgreiningu ER-sniðs</span><span class="sxs-lookup"><span data-stu-id="6bac1-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="6bac1-382">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="6bac1-383">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="6bac1-384">Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Sniðmát byggt á gagnalíkaninu Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="6bac1-385">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="6bac1-386">Í reitnum **Skilgreining gagnalíkans** velurðu **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="6bac1-387">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-387">Select **Create configuration**.</span></span>

<span data-ttu-id="6bac1-388">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="6bac1-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="6bac1-389">Þessi útgáfa inniheldur íhluta sniðsins.</span><span class="sxs-lookup"><span data-stu-id="6bac1-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="6bac1-390">Hanna sýnissnið</span><span class="sxs-lookup"><span data-stu-id="6bac1-390">Design a sample format</span></span>

1.  <span data-ttu-id="6bac1-391">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="6bac1-392">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="6bac1-393">Í hópnum **Texti** velurðu liðinn **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="6bac1-394">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="6bac1-395">Binda sniðsþætti í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="6bac1-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="6bac1-396">Á síðunni **Sniðahönnuður**, á flipanum **Vörpun**, stækkarðu gagnagjafa líkansins.</span><span class="sxs-lookup"><span data-stu-id="6bac1-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="6bac1-397">Veldu reitinn **Lýsing á virkni**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="6bac1-398">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-398">Select **Bind**.</span></span>

    ![Síða ER-sniðshönnuðar](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="6bac1-400">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-400">Select **Save**.</span></span>
5.  <span data-ttu-id="6bac1-401">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-401">Close the page.</span></span>

## <a name="appendix-2"></a><a name="appendix2"></a> <span data-ttu-id="6bac1-402">Viðauki 2</span><span class="sxs-lookup"><span data-stu-id="6bac1-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="6bac1-403">Stilla vörpun sýnislíkans fyrir almenna sérstillingu</span><span class="sxs-lookup"><span data-stu-id="6bac1-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="6bac1-404">Þú gætir viljað sérsníða líkanavörpun sem stillingarveita (samstarfsaðili) gaf þér og notað síðan sérsniðna útgáfu sem gagnagjafa fyrir ER sniðin þín.</span><span class="sxs-lookup"><span data-stu-id="6bac1-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="6bac1-405">Í þessu tilfelli verður þú að stofna sérsniðna vörpunarstillingu ER-líkans til að gera nauðsynlegar breytingar á fyrirliggjandi vörpun.</span><span class="sxs-lookup"><span data-stu-id="6bac1-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="6bac1-406">Aðferðirnar í þessum viðbæti nota líkanavörpunina **Vörpun (almennt)** sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="6bac1-407">Stofna grunnstillingu ER-líkansvörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="6bac1-408">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt)**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="6bac1-409">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="6bac1-410">Í fellivalmyndinni í reitahópnum **Nýtt**, velurðu **Leiða af nafni: Vörpun (Almennt), Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="6bac1-411">Í reitinn **Heiti** slærðu inn **Vörpun (almennt) sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="6bac1-412">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-412">Select **Create configuration**.</span></span>

<span data-ttu-id="6bac1-413">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="6bac1-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="6bac1-414">Hanna sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="6bac1-415">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="6bac1-416">Taktu eftir því að líkanavarpanir grunnstillingarinnar eru sjálfkrafa afritaðar í þessa stillingu.</span><span class="sxs-lookup"><span data-stu-id="6bac1-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="6bac1-417">Veldu vörpunina **Vörpun (almennt) afrit**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="6bac1-418">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="6bac1-419">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="6bac1-420">Í reitinn **Formúla** skal færa inn **„Almenn virkni 1 sérsnið“**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="6bac1-421">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-421">Select **Save**.</span></span>
7.  <span data-ttu-id="6bac1-422">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-422">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="6bac1-424">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-424">Select **Save**.</span></span>
9.  <span data-ttu-id="6bac1-425">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-425">Close the page.</span></span>
10. <span data-ttu-id="6bac1-426">Veldu vörpunina **Vörpun 2 (almennt) afrit**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="6bac1-427">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-427">Select **Designer**.</span></span>
12. <span data-ttu-id="6bac1-428">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="6bac1-429">Í reitinn **Formúla** skal færa inn **„Almenn virkni 2 sérsnið“**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="6bac1-430">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-430">Select **Save**.</span></span>
15. <span data-ttu-id="6bac1-431">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-431">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="6bac1-433">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-433">Select **Save**.</span></span>
17. <span data-ttu-id="6bac1-434">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-434">Close the page.</span></span>

    ![Síðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="6bac1-436">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="6bac1-437">Ljúka við breyttu útgáfuna af stillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="6bac1-438">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="6bac1-439">Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="6bac1-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="6bac1-440">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="6bac1-441">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-441">Select **OK**.</span></span>

<span data-ttu-id="6bac1-442">Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="6bac1-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix-3"></a><a name="appendix3"></a> <span data-ttu-id="6bac1-443">Viðauki 3</span><span class="sxs-lookup"><span data-stu-id="6bac1-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="6bac1-444">Stilla vörpun sýnislíkans fyrir lands-/landsvæðissértæka sérstillingu</span><span class="sxs-lookup"><span data-stu-id="6bac1-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="6bac1-445">Fyrir sum ER snið geta verið lands-/svæðissértækar kröfur um undirbúning gagna.</span><span class="sxs-lookup"><span data-stu-id="6bac1-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="6bac1-446">Í þessu tilfelli getur þú stjórnað sérstakri vörpun ER-líkana og einangrað framkvæmd þessara lands-/svæðisbundnu krafna frá almennri framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="6bac1-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="6bac1-447">Ferlin í þessum viðauka nota ER-sniðið **Snið til að læra varpanir** og franskar sértækar kröfur sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="6bac1-448">Stofna grunnstillingu ER-líkansvörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="6bac1-449">Í fyrsta lagi skaltu búa til nýja stillingu ER-líkanavörpunar til að innleiða lands-/svæðisbundnar kröfur.</span><span class="sxs-lookup"><span data-stu-id="6bac1-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="6bac1-450">Notaðu sérsniðna stillingu ER-líkanavörpunar sem grunn.</span><span class="sxs-lookup"><span data-stu-id="6bac1-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="6bac1-451">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt) sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="6bac1-452">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="6bac1-453">Í fellivalmyndinni í reitahópnum **Nýtt**, velurðu **Leiða af nafni: Vörpun (Almennt) sérsnið, Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="6bac1-454">Í reitinn **Heiti** slærðu inn **Vörpun (FR)**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="6bac1-455">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-455">Select **Create configuration**.</span></span>

<span data-ttu-id="6bac1-456">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="6bac1-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="6bac1-457">Hanna sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="6bac1-458">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="6bac1-459">Taktu eftir því að líkanavarpanir grunnstillingarinnar eru sjálfkrafa afritaðar í þessa stillingu.</span><span class="sxs-lookup"><span data-stu-id="6bac1-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="6bac1-460">Veldu vörpunina **Vörpun (almennt) afrit afrit**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="6bac1-461">Endurnefndu hana **Vörpun (FR)**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="6bac1-462">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="6bac1-463">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="6bac1-464">Í reitinn **Formúla** skal færa inn **„FR-virkni 1“**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="6bac1-465">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-465">Select **Save**.</span></span>
8.  <span data-ttu-id="6bac1-466">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-466">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="6bac1-468">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-468">Select **Save**.</span></span>
10. <span data-ttu-id="6bac1-469">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-469">Close the page.</span></span>
11. <span data-ttu-id="6bac1-470">Veldu vörpunina **Vörpun 2 (almennt) afrit afrit**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="6bac1-471">Endurnefndu hana **Vörpun 2 (FR)**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="6bac1-472">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-472">Select **Designer**.</span></span>
14. <span data-ttu-id="6bac1-473">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="6bac1-474">Í reitinn **Formúla** skal færa inn **„FR-virkni 2“**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="6bac1-475">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-475">Select **Save**.</span></span>
17. <span data-ttu-id="6bac1-476">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-476">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="6bac1-478">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-478">Select **Save**.</span></span>
19. <span data-ttu-id="6bac1-479">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-479">Close the page.</span></span>

    ![Síðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="6bac1-481">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6bac1-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="6bac1-482">Tilgreindu lands-/svæðisbundnar samhengistakmarkanir fyrir notkun</span><span class="sxs-lookup"><span data-stu-id="6bac1-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="6bac1-483">Á síðunni **Skilgreiningar**, á flýtiflipanum **ISO lands-/svæðiskóðar** velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="6bac1-484">Í reitnum **ISO** er valið **FR**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="6bac1-485">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-485">Select **Save**.</span></span>

<span data-ttu-id="6bac1-486">Athugaðu að þú verður að skrá þig inn á tiltekið fyrirtæki í Finance til að keyra ER-snið.</span><span class="sxs-lookup"><span data-stu-id="6bac1-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="6bac1-487">Þess vegna getur þetta fyrirtæki talist aðili sem stjórnar bæði framkvæmd ER-sniða og vali á réttri vörpun ER-líkans af ER-grunngagnalíkani.</span><span class="sxs-lookup"><span data-stu-id="6bac1-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="6bac1-488">Með því að bæta við landskóðanum **FR** tilgreinirðu að vörpun líkansins er tiltæk til vals með ER sniði grunngagnalíkansins aðeins þegar það snið er keyrt undir stjórn fyrirtækis sem hefur franskt lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="6bac1-489">Þú getur bætt við mörgum lands-/svæðiskóðum fyrir staka útgáfu af stillingum á ER-líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6bac1-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="6bac1-490">Þannig er hægt að nota líkanavarpanir sem búa í þeirri stillingu líkanavörpunar fyrir ER-snið sem er keyrt undir stjórn fyrirtækja sem hafa annað lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="6bac1-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="6bac1-491">Athugaðu að listinn yfir lands-/svæðisnúmer er tilgreindur fyrir hverja útgáfu af stillingum ER-líkanavörpunar og getur verið breytilegur frá einnu útgáfu til annarrar.</span><span class="sxs-lookup"><span data-stu-id="6bac1-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="6bac1-492">Ljúka við breyttu útgáfuna af stillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="6bac1-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="6bac1-493">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="6bac1-494">Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="6bac1-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="6bac1-495">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="6bac1-496">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-496">Select **OK**.</span></span>

<span data-ttu-id="6bac1-497">Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="6bac1-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bac1-498">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6bac1-498">Additional resources</span></span>

[<span data-ttu-id="6bac1-499">Yfirlit yfir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="6bac1-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="6bac1-500">Stjórna vörpunarlíkani rafrænnar skýrslugerðar í aðskilinni skilgreiningu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6bac1-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="6bac1-501">Nota lands-/svæðistengt samhengi</span><span class="sxs-lookup"><span data-stu-id="6bac1-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="6bac1-502">Algengar spurningar</span><span class="sxs-lookup"><span data-stu-id="6bac1-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="6bac1-503">Ég stillti tvær sameiginlegar stillingar ER-líkanavörpunar í RCS og merkti eina þeirra sem sjálfgefna stillingu líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="6bac1-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="6bac1-504">Mér tókst að keyra ER-snið sem var búið til fyrir sömu grunngerð ER-gagnalíkanastillingar, til að prófa líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="6bac1-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="6bac1-505">Síðan flutti ég inn alla ER-lausnina (ER-gagnalíkan, tvær stillingar ER-líkanavarpana og stillingar á ER-sniði) í Finance.</span><span class="sxs-lookup"><span data-stu-id="6bac1-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="6bac1-506">Af hverju fæ ég villuboð þegar ég reyni að keyra sama ER-snið í Finance?</span><span class="sxs-lookup"><span data-stu-id="6bac1-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="6bac1-507">Sjálfgefin stilling líkanavörpunar er umhverfissértæk.</span><span class="sxs-lookup"><span data-stu-id="6bac1-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="6bac1-508">Hún er stillt í RCS en er ekki flutt til Finance.</span><span class="sxs-lookup"><span data-stu-id="6bac1-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="6bac1-509">Til að keyra þetta ER-snið verður þú að merkja eina af stillingum ER-líkanavörpunar sem sjálfgefna stillingu líkanavörpunar í Finance líka.</span><span class="sxs-lookup"><span data-stu-id="6bac1-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="6bac1-510">Ég stillti eina líkanavörpun sem samnýtta líkanavörpun og kláraði drög að útgáfu hennar.</span><span class="sxs-lookup"><span data-stu-id="6bac1-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="6bac1-511">Síðan bætti ég við nýrri gerð stillingar líkanavörpunar fyrir sama gagnalíkan og stillti það sem fransk-sértækt.</span><span class="sxs-lookup"><span data-stu-id="6bac1-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="6bac1-512">Hvers vegna er sameiginleg líkanavörpun valin þegar ég keyri ER-snið, jafnvel þó að þetta ER-snið noti réttar rótarskilgreiningar og framkvæmd er gerð undir stjórn fyrirtækisins sem hefur franskt lands-/svæðissamhengi?</span><span class="sxs-lookup"><span data-stu-id="6bac1-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="6bac1-513">Gakktu úr skugga um að samnýtta stilling líkanavörpunar sé ekki merkt sem sjálfgefin stilling líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="6bac1-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="6bac1-514">Annars mun það hafa meiri forgang við val á vörpun.</span><span class="sxs-lookup"><span data-stu-id="6bac1-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="6bac1-515">Gakktu einnig úr skugga um að stillt sé á franskar sértækar stillingar líkanavörpunar þegar vörpun er valin við framkvæmd ER sniðs.</span><span class="sxs-lookup"><span data-stu-id="6bac1-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="6bac1-516">Stillingar á ER-líkanavörpun er aðeins tiltæk til vals ef að minnsta kosti eitt af eftirfarandi skilyrðum er uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="6bac1-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="6bac1-517">Að minnsta kosti ein útgáfa af stilligum ER-líkanavörpunar hefur annaðhvort stöðuna **Lokið** eða **Deilt**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="6bac1-518">Í þessu tilfelli verður útgáfan sem er með hæsta útgáfunúmerið notuð við framkvæmd ER sniðs.</span><span class="sxs-lookup"><span data-stu-id="6bac1-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="6bac1-519">Kveikt er á valkostinum **Keyra drög** fyrir stillingu ER-líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="6bac1-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="6bac1-520">Í þessu tilfelli verður útgáfan sem er með stöðuna **Drög** notuð við framkvæmd ER sniðs.</span><span class="sxs-lookup"><span data-stu-id="6bac1-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="6bac1-521">Valkosturinn **Keyra drög** verður í boði á síðunni **Stillingar** fyrir sérhverja stillingu ER-líkanavörpunar þegar kveikt er á ER-færibreytu notanda **Keyra stillingu**.</span><span class="sxs-lookup"><span data-stu-id="6bac1-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]