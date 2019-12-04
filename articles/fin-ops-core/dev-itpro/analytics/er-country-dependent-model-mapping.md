---
title: Stilla landssamhengisháðar varpanir ER-líkans
description: Þetta efni útskýrir hvernig þú getur sett upp ER-líkanavarpanir svo þær séu háðar samhengi lands/landsvæðis lögaðilans sem stjórnar notkun þeirra.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 6c4b18a3cf2ba313756d5f761ef1beb2c3015516
ms.sourcegitcommit: 56add4c49c35c65a75fa2ca5234927e7f7cd66ef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2781146"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a><span data-ttu-id="b4fd3-103">Stilla landssamhengisháðar varpanir ER-líkans</span><span class="sxs-lookup"><span data-stu-id="b4fd3-103">Configure country context dependent ER model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b4fd3-104">Þú getur stillt líkanavarpanir rafrænnar skýrslugerðar (ER) þannig að þau innleiða almennt ER gagnalíkan en eru sértæk fyrir Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-104">You can configure Electronic reporting (ER) model mappings so that they implement a generic ER data model but are specific to Dynamics 365 Finance.</span></span> <span data-ttu-id="b4fd3-105">Þetta efnisatriði útskýrir hvernig á að hanna margar ER-líkanavarpanir fyrir ER-gagnalíkan til að stjórna því hvernig þær eru notaðar af samsvarandi ER-sniðum sem eru keyrð úr fyrirtækjum sem hafa mismunandi lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-105">This topic explains how to design multiple ER model mappings for an ER data model to control how they are used by corresponding ER formats that are run from companies that have different country/region contexts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b4fd3-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="b4fd3-106">Prerequisites</span></span>

<span data-ttu-id="b4fd3-107">Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:</span><span class="sxs-lookup"><span data-stu-id="b4fd3-107">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="b4fd3-108">Aðgangur að Finance fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="b4fd3-108">Access to Finance for one of the following roles:</span></span>
    - <span data-ttu-id="b4fd3-109">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="b4fd3-110">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b4fd3-111">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="b4fd3-111">System administrator</span></span>

- <span data-ttu-id="b4fd3-112">Aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="b4fd3-112">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>
    - <span data-ttu-id="b4fd3-113">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="b4fd3-114">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b4fd3-115">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="b4fd3-115">System administrator</span></span>

<span data-ttu-id="b4fd3-116">Sum skref í þessu efni þurfa að framkvæma ER snið.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-116">Some steps in this topic require execution of an ER format.</span></span> <span data-ttu-id="b4fd3-117">Í sumum tilvikum verður framkvæmd á ER-sniði fyrir áhrifum af lands-/svæðissamhengi fyrirtækisins sem þú ert skráð (ur) inn á.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-117">In some cases, execution of an ER format is affected by the country/region context of the company that you're currently signed in to.</span></span> <span data-ttu-id="b4fd3-118">Þú getur keyrt ER snið í núverandi RCS tilviki ef fyrirtækið sem hefur tilskilið lands-/svæðissamhengi er fáanlegt í RCS.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-118">You can run an ER format in the current RCS instance if the company that has the required country/region context is available in RCS.</span></span> <span data-ttu-id="b4fd3-119">Annars verður þú að hlaða upp lokinni útgáfu af stillingum á ER-líkanavörpunum og ER-sniðum sem nota ER-gagnalíkanið í tilviki þínu af Finance og keyra síðan ER sniðið í því tilviki af Finance.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-119">Otherwise, you must upload a completed version of the ER model mapping and ER format configurations that use the ER data model to your Finance instance, and then run the ER format in that Finance instance.</span></span> <span data-ttu-id="b4fd3-120">Nánari upplýsingar um hvernig á að flytja inn stillingar sem eru í RCS í tilvik af Finance er að finna í [Flytja inn stillingar úr RCS](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-120">For information about how to import configurations that reside in RCS into a Finance instance, see [Import configurations from RCS](rcs-download-configurations.md).</span></span>

## <a name="single-model-mapping-case"></a><span data-ttu-id="b4fd3-121">Stakt dæmi um líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="b4fd3-121">Single model mapping case</span></span>

<span data-ttu-id="b4fd3-122">Fylgdu skrefunum í [Viðauki 1](#appendix1) af þessu efni til að hanna nauðsynlega ER íhluti.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-122">Follow the steps in [Appendix 1](#appendix1) of this topic to design the required ER components.</span></span> <span data-ttu-id="b4fd3-123">Núna ertu með stillingu líkanavörpunar **Vörpun (almennt)** sem inniheldur líkanavörpun fyrir skilgreininguna **Inngangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-123">You now have the **Mapping (General)** model mapping configuration that contains the model mapping for the **Entry point 1** definition.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="b4fd3-125">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-125">Run the configured format</span></span>

1.  <span data-ttu-id="b4fd3-126">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-126">On the **Configurations page**, on the **Versions** FastTab, select **Run**.</span></span>
2.  <span data-ttu-id="b4fd3-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-127">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-128">Taktu eftir að vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-128">Notice that the web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="b4fd3-129">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og aðeins stök líkanavörpun er nú fáanleg fyrir grunnlíkanið sem inniheldur vörpun fyrir þessa skilgreiningu notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt)** í skilgreiningunni **Vörpun (almennt)** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-129">Because this format was configured to use the **Entry point 1** definition, and only a single model mapping is currently available for the base model that contains a mapping for this definition, the executed ER format used the **Mapping (General)** model mapping of the **Mapping (General)** configuration as a data source.</span></span> <span data-ttu-id="b4fd3-130">Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-130">Therefore, the downloaded file contains the **Generic functionality 1** text.</span></span>

## <a name="multiple-shared-model-mappings-case"></a><span data-ttu-id="b4fd3-131">Margvísleg samnýting á vörpunardæmi líkana</span><span class="sxs-lookup"><span data-stu-id="b4fd3-131">Multiple shared model mappings case</span></span>

<span data-ttu-id="b4fd3-132">Fylgdu skrefunum í [Viðauki 2](#appendix2) af þessu efni til að hanna nauðsynlega ER íhluti.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-132">Follow the steps in [Appendix 2](#appendix2) of this topic to design the required ER components.</span></span> <span data-ttu-id="b4fd3-133">Núna ertu með stillingar líkanavörpunar **Vörpun (almennt)** og **Vörpun (almennt) sérsnið** sem inniheldur hvor fyrir sig líkanavörpun fyrir skilgreininguna **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-133">You now have **Mapping (General)** and **Mapping (General) custom** model mapping configurations, each of which contains the model mapping for the **Entry point 1** definition.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="b4fd3-135">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-135">Run the configured format</span></span>

1.  <span data-ttu-id="b4fd3-136">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-136">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="b4fd3-137">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-137">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="b4fd3-138">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-138">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-139">Taktu eftir að framkvæmd á völdu ER sniði tókst ekki.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-139">Notice that execution of the selected ER format is unsuccessful.</span></span> <span data-ttu-id="b4fd3-140">Villuboð upplýsa þig um að fleiri en ein gerð vörpunar er til fyrir líkanið **Líkan til að læra varpanir** og skilgreininguna **Aðgangsstaður 1** á stillingum líkanavarpana **Kortlagning (almennt)** og **Kortlagning (almenn) sérsniðin**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-140">An error message informs you that more than one model mapping exists for the **Model to learn mappings** model and the **Entry point 1** definition in the **Mapping (General)** and **Mapping (General) custom** model mapping configurations.</span></span> <span data-ttu-id="b4fd3-141">Skilaboðin mæla einnig með að þú veljir eina af þessum stillingum sem sjálfgefna stillingu.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-141">The message also recommends that you select one of those configurations as the default configuration.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a><span data-ttu-id="b4fd3-143">Skilgreindu sjálfgefna líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="b4fd3-143">Define a default mapping configuration</span></span>

<span data-ttu-id="b4fd3-144">Fylgdu þessum skrefum til að skilgreina stillingu líkanavörpunar **Kortlagning (almenn) sérsniðin** sem sjálfgefna stillingu, svo að hægt sé að nota varpanir hennar sem gagnagjafa fyrir ER-sniðið **Snið til að læra vörpun**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-144">Follow these steps to define the **Mapping (General) custom** model mapping configuration as the default configuration, so that its mappings can be used as data sources for the **Format to learn mappings** ER format.</span></span>

1.  <span data-ttu-id="b4fd3-145">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt) sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-145">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="b4fd3-146">Veldu eftir þörfum **Breyta** til að gera þessa síðu tilbúna til að breyta.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-146">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="b4fd3-147">Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-147">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="b4fd3-148">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-148">Select **Save**.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="b4fd3-150">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-150">Run the configured format</span></span>

1.  <span data-ttu-id="b4fd3-151">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-151">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="b4fd3-152">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-152">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="b4fd3-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-153">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-154">Taktu eftir að framkvæmd á völdu ER sniði tókst.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-154">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="b4fd3-155">Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-155">The web browser offers to download the text file that was generated by executed ER format.</span></span> <span data-ttu-id="b4fd3-156">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (almennt) sérsnið** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt) afrit** í skilgreiningunni **Vörpun (almennt) sérsnið** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-156">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="b4fd3-157">Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1 sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-157">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

> [!NOTE]
> <span data-ttu-id="b4fd3-158">Ef þú skiptir um fyrirtæki sem þú ert skráð/ur inn í og keyrir þetta ER snið aftur, þá færðu sama innihaldið í myndinni, vegna þess að sjálfgefna uppsetning ER gerðanna inniheldur engar fyrirtækjaháðar hömlur.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-158">If you change the company that you're currently signed in to and run this ER format again, you get the same content in the generated file, because the default ER model mapping configuration doesn't contain any company-dependent restrictions.</span></span>

## <a name="multiple-mixed-model-mappings-case"></a><span data-ttu-id="b4fd3-159">Mörg blönduð vörpunardæmi líkana</span><span class="sxs-lookup"><span data-stu-id="b4fd3-159">Multiple mixed model mappings case</span></span>

<span data-ttu-id="b4fd3-160">Fylgdu skrefunum í [Viðauki 3](#appendix3) af þessu efni til að hanna nauðsynlega ER íhluti.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-160">Follow the steps in [Appendix 3](#appendix3) of this topic to design the required ER components.</span></span> <span data-ttu-id="b4fd3-161">Núna ertu með stillingar **Vörpun (almennt)**, **Vörpun (almennt) sérsnið** og **Vörpun (FR) líkanavörpunar** sem innihalda líkanavörpun fyrir skilgreininguna **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-161">You now have **Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR) model mapping** configurations that contain the model mapping for the **Entry point 1** definition.</span></span>

<span data-ttu-id="b4fd3-162">Taktu eftir að útgáfa 1 af stillingu líkanavörpunar **Vörpun (FR)** er þannig stillt að hún á aðeins við um ER-snið í líkaninu **Líkan til að læra varpanir** sem eru keyrði í fjármálafyrirtækjum sem hafa franskt lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-162">Notice that version 1 of the **Mapping (FR)** model mapping configuration is configured so that it applies only to ER formats of the **Model to learn mappings** model that are run in Finance companies that have French country/region context.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="b4fd3-164">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-164">Run the configured format</span></span>

1.  <span data-ttu-id="b4fd3-165">Breyttu fyrirtækinu í **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-165">Change the company to **FRSI**.</span></span>
2.  <span data-ttu-id="b4fd3-166">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-166">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
3.  <span data-ttu-id="b4fd3-167">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-167">On the **Versions** FastTab, select **Run**.</span></span>
4.  <span data-ttu-id="b4fd3-168">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-168">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-169">Taktu eftir að framkvæmd á völdu ER sniði tókst.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-169">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="b4fd3-170">Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-170">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="b4fd3-171">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (almennt) sérsnið** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (almennt) afrit** í skilgreiningunni **Vörpun (almennt) sérsnið** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-171">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (General) custom** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (General) copy** model mapping of the **Mapping (General) custom** configuration as a data source.</span></span> <span data-ttu-id="b4fd3-172">Þess vegna inniheldur niðurflutt skrá textann **Almenn virkni 1 sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-172">Therefore, the downloaded file contains the **Generic functionality 1 custom** text.</span></span>

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a><span data-ttu-id="b4fd3-173">Tilgreindu líkanastillingar sem eru sértækar fyrir Frakkland sem sjálfgefna stillingu</span><span class="sxs-lookup"><span data-stu-id="b4fd3-173">Define the France-specific mapping configuration as the default configuration</span></span>

<span data-ttu-id="b4fd3-174">Fylgdu þessum skrefum til að skilgreina sérsniðna líkanavörpunarstillingu **Vörpun (FR)** sem sjálfgefna stillingu.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-174">Follow these steps to define the custom **Mapping (FR)** model mapping configuration as the default configuration.</span></span> <span data-ttu-id="b4fd3-175">Athugaðu að vegna þess að þessi vörpun er sértæk fyrir Frakkland verður hún talin sjálfgefin vörpun milli allra stillinga líkanavarpana sem hafa landskóðann **FR** sem tilgreindur er í reitnum **ISO lands-/svæðiskóðar**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-175">Note that, because this mapping is specific to France, it will be considered the default mapping between all model mapping configurations that have the **FR** country code specified in the **ISO country/region codes** field.</span></span>

1.  <span data-ttu-id="b4fd3-176">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (FR)**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-176">On the **Configurations** page, in the configurations tree, select **Mapping (FR)**.</span></span>
2.  <span data-ttu-id="b4fd3-177">Veldu eftir þörfum **Breyta** til að gera þessa síðu tilbúna til að breyta.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-177">As required, select **Edit** to make the current page ready for editing.</span></span>
3.  <span data-ttu-id="b4fd3-178">Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-178">Set the **Default for model mapping** option to **Yes**.</span></span>
4.  <span data-ttu-id="b4fd3-179">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-179">Select **Save**.</span></span>

![Skilgreiningarsíða í ER](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a><span data-ttu-id="b4fd3-181">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-181">Run the configured format</span></span>

1.  <span data-ttu-id="b4fd3-182">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-182">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="b4fd3-183">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-183">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="b4fd3-184">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-184">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-185">Taktu eftir að framkvæmd á völdu ER sniði tókst.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-185">Notice that execution of the selected ER format succeeds.</span></span> <span data-ttu-id="b4fd3-186">Vafrinn býður upp á að hlaða niður textaskránni sem mynduð var með framkvæmdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-186">The web browser offers to download the text file that was generated by the executed ER format.</span></span> <span data-ttu-id="b4fd3-187">Þar sem þetta snið var stillt til að nota skilgreininguna **Aðgangsstaður 1** og stilling líkanavörpunar **Vörpun (FR)** var valin sem sjálfgefin stilling notaði keyrða ER-sniðið líkanavörpunina **Vörpun (FR)** í skilgreiningunni **Vörpun (FR)** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-187">Because this format was configured to use the **Entry point 1** definition, and the **Mapping (FR)** model mapping configuration was selected as the default configuration, the executed ER format used the **Mapping (FR)** model mapping of the **Mapping (FR)** configuration as a data source.</span></span> <span data-ttu-id="b4fd3-188">Þess vegna inniheldur niðurflutt skrá textann **FR virkni 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-188">Therefore, the downloaded file contains the **FR functionality 1** text.</span></span>

> [!NOTE]
> <span data-ttu-id="b4fd3-189">Ef þú skiptir um fyrirtæki sem þú ert skráð/ur inn í og keyrir þetta ER snið aftur mun framleiðslan fara eftir samhengi lands-/svæðis valins fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-189">If you change the company that you're currently signed in to and run this ER format again, the output will depend on the country/region context of the selected company.</span></span>

## <a name="other-model-mapping-cases"></a><span data-ttu-id="b4fd3-190">Önnur dæmi um líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="b4fd3-190">Other model mapping cases</span></span>

<span data-ttu-id="b4fd3-191">Eins og þú hefur séð virkar val á líkanavörpun til framkvæmdar á ER sniði á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="b4fd3-191">As you've seen, the selection of a model mapping for the execution of an ER format works in the following way:</span></span>

- <span data-ttu-id="b4fd3-192">Skilgreining á líkanavörpun sem ER snið notar er tilgreind (**Aðgangsstaður 1** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-192">The model mapping definition that an ER format uses is specified (**Entry point 1** in the examples in this topic).</span></span>
- <span data-ttu-id="b4fd3-193">Hægt er að nota allar vörpunarstillingar sem innihalda vörpun sem hefur tilgreinda skilgreiningu og fullnægja samhengishömlum landa/svæða sem eru uppsettar til að keyra ER snið (**Vörpun (almennt)**, **Vörpun (almenn) sérsniðin** og **Vörpun (FR)** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-193">All mapping configurations that contain a mapping that has the specified definition, and that satisfy any country/region context restrictions that are configured, can potentially be used to run the ER format (**Mapping (General)**, **Mapping (General) custom**, and **Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="b4fd3-194">Sérhver sjálfgefin vörpun líkana sem hefur takmarkanir á landi/svæðum hefur forgangsröðun fyrir val (**Vörpun (FR)** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-194">Any default model mapping that has country/region context restrictions has the highest priority for selection (**Mapping (FR)** in the examples in this topic).</span></span>
- <span data-ttu-id="b4fd3-195">Sérhver sjálfgefin vörpun líkana sem hefur ekki takmarkanir á landi/svæðum hefur næsthæstu forgangsröðun fyrir val (**Vörpun (almennt) sérsnið** í dæmunum í þessu efni).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-195">Any default model mapping that doesn't have country/region context restrictions has the next higher priority for selection  (**Mapping (General) custom** in the examples in this topic).</span></span>
- <span data-ttu-id="b4fd3-196">Sérhver líkanakortlagning sem hefur takmarkanir á landi/svæðum hefur meiri forgang við val en vörpun líkana sem eru ekki með samhengi takmarkana á landi/svæðum.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-196">Any model mapping that has country/region context restrictions has higher priority for selection than a model mapping that doesn't have country/region context restrictions.</span></span>

<span data-ttu-id="b4fd3-197">Eftirfarandi tafla veitir upplýsingar um niðurstöður val á líkanavörpun fyrir öll möguleg tilvik fyrir líkanavarpanastillingar:</span><span class="sxs-lookup"><span data-stu-id="b4fd3-197">The following table provides information about the results of model mapping selection for all possible cases for model mapping settings:</span></span>

- <span data-ttu-id="b4fd3-198">Dálkur 1 gefur til kynna hvort fyrsta vörpun líkansins sem hefur ekki takmarkanir á samhengi landa/svæða (til dæmis samnýtta líkanið **Vörpun (almennt)**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-198">Column 1 indicates whether the first model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="b4fd3-199">Dálkur 2 gefur til kynna hvort önnur vörpun líkansins sem hefur ekki takmarkanir á samhengi landa/svæða (til dæmis samnýtta líkanið **Vörpun (almennt) sérsnið**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-199">Column 2 indicates whether the second model mapping that doesn't have country/region context restrictions (for example, the shared **Mapping (General) custom** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="b4fd3-200">Dálkur 3 gefur til kynna hvort fyrsta vörpun líkansins sem hefur takmarkanir á samhengi landa/svæða A (til dæmis Frakklands-sértæka líkanið **Vörpun (FR)**) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-200">Column 3 indicates whether the first model mapping that has country/region A context restrictions (for example, the France-specific **Mapping (FR)** mapping) is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="b4fd3-201">Dálkur 4 gefur til kynna hvort önnur vörpun líkansins sem hefur takmarkanir á samhengi landa/svæða A (til dæmis Frakklands-sértæka líkanið Vörpun (FR)) er kynnt og, ef það er, hvort valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-201">Column 4 indicates whether the second model mapping that has country/region A context restrictions is presented and, if it is, whether the **Default for model mapping** option is set to **Yes** for it.</span></span>
- <span data-ttu-id="b4fd3-202">Dálkur 5 sýnir niðurstöðu úr vali á líkanavörpun fyrir framkvæmd á ER sniði undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi A.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-202">Column 5 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region A context.</span></span>
- <span data-ttu-id="b4fd3-203">Dálkur 6 sýnir niðurstöðu úr vali á líkanavörpun fyrir framkvæmd á ER sniði undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi B.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-203">Column 6 presents the result of a model mapping selection for execution of an ER format under the control of a company that has country/region B context.</span></span>

<span data-ttu-id="b4fd3-204">Í töflunni bendir plúsmerki (+) til að til sé stilling líkanavörpunar í núverandi tilviki Microsoft Azure þjónustu sem er notuð til að keyra ER snið (annaðhvort Finance eða RCS).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-204">In the table, a plus sign (+) indicates the presence of a model mapping configuration in the current instance of the Microsoft Azure service that is used to run an ER format (either Finance or RCS).</span></span>

| <span data-ttu-id="b4fd3-205">Tilvik</span><span class="sxs-lookup"><span data-stu-id="b4fd3-205">Case</span></span> | <span data-ttu-id="b4fd3-206">Líkanavörpun 1 án samhengis lands/svæðis (MM1)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-206">Model mapping 1 without country/region context (MM1)</span></span> | <span data-ttu-id="b4fd3-207">Líkanavörpun 2 án samhengis lands/svæðis (MM2)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-207">Model mapping 2 without country/region context (MM2)</span></span> | <span data-ttu-id="b4fd3-208">Líkanavörpun 1 með samhengi lands/svæðis A (MM1A)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-208">Model mapping 1 with country/region A context (MM1A)</span></span> | <span data-ttu-id="b4fd3-209">Líkanavörpun 2 með samhengi lands/svæðis A (MM2A)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-209">Model mapping 2 with country/region A context (MM2A)</span></span> | <span data-ttu-id="b4fd3-210">Keyra undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-210">Run under control of a company that has country/region A context</span></span> | <span data-ttu-id="b4fd3-211">Keyra undir stjórn fyrirtækis sem hefur lands-/svæðissamhengi B</span><span class="sxs-lookup"><span data-stu-id="b4fd3-211">Run under the control of a company that has country/region B context</span></span> |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     <span data-ttu-id="b4fd3-212">1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-212">1</span></span>   |     <span data-ttu-id="b4fd3-213">2</span><span class="sxs-lookup"><span data-stu-id="b4fd3-213">2</span></span>   |    <span data-ttu-id="b4fd3-214">3</span><span class="sxs-lookup"><span data-stu-id="b4fd3-214">3</span></span>    |    <span data-ttu-id="b4fd3-215">4</span><span class="sxs-lookup"><span data-stu-id="b4fd3-215">4</span></span>    |           <span data-ttu-id="b4fd3-216">5</span><span class="sxs-lookup"><span data-stu-id="b4fd3-216">5</span></span>               |            <span data-ttu-id="b4fd3-217">6</span><span class="sxs-lookup"><span data-stu-id="b4fd3-217">6</span></span>               |
|     <span data-ttu-id="b4fd3-218">1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-218">1</span></span>   |         |         |         |         | <span data-ttu-id="b4fd3-219">Villa (vantar vörpun)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-219">Error (missing mapping)</span></span>   | <span data-ttu-id="b4fd3-220">Villa (vantar vörpun)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-220">Error (missing mapping)</span></span>    |
|     <span data-ttu-id="b4fd3-221">2</span><span class="sxs-lookup"><span data-stu-id="b4fd3-221">2</span></span>   |     +   |         |         |         | <span data-ttu-id="b4fd3-222">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-222">MM1</span></span>                       | <span data-ttu-id="b4fd3-223">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-223">MM1</span></span>                        |
|     <span data-ttu-id="b4fd3-224">3</span><span class="sxs-lookup"><span data-stu-id="b4fd3-224">3</span></span>   |     +   |     +   |         |         | <span data-ttu-id="b4fd3-225">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-225">Error (multiple mappings)</span></span> | <span data-ttu-id="b4fd3-226">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-226">Error (multiple mappings)</span></span>  |
|     <span data-ttu-id="b4fd3-227">4</span><span class="sxs-lookup"><span data-stu-id="b4fd3-227">4</span></span>   |     +   |         |    +    |         | <span data-ttu-id="b4fd3-228">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-228">MM1A</span></span>                      | <span data-ttu-id="b4fd3-229">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-229">MM1</span></span>                        |
|     <span data-ttu-id="b4fd3-230">5</span><span class="sxs-lookup"><span data-stu-id="b4fd3-230">5</span></span>   |     +   |         |    +    |    +    | <span data-ttu-id="b4fd3-231">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-231">Error (multiple mappings)</span></span> | <span data-ttu-id="b4fd3-232">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-232">MM1</span></span>                        |
|     <span data-ttu-id="b4fd3-233">6</span><span class="sxs-lookup"><span data-stu-id="b4fd3-233">6</span></span>   |     +   | <span data-ttu-id="b4fd3-234">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-234">default</span></span> |    +    |    +    | <span data-ttu-id="b4fd3-235">MM2</span><span class="sxs-lookup"><span data-stu-id="b4fd3-235">MM2</span></span>                       | <span data-ttu-id="b4fd3-236">MM2</span><span class="sxs-lookup"><span data-stu-id="b4fd3-236">MM2</span></span>                        |
|     <span data-ttu-id="b4fd3-237">7</span><span class="sxs-lookup"><span data-stu-id="b4fd3-237">7</span></span>   |     +   |         | <span data-ttu-id="b4fd3-238">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-238">default</span></span> |         | <span data-ttu-id="b4fd3-239">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-239">MM1A</span></span>                      | <span data-ttu-id="b4fd3-240">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-240">MM1</span></span>                        |
|     <span data-ttu-id="b4fd3-241">8</span><span class="sxs-lookup"><span data-stu-id="b4fd3-241">8</span></span>   |     +   |         | <span data-ttu-id="b4fd3-242">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-242">default</span></span> |    +    | <span data-ttu-id="b4fd3-243">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-243">MM1A</span></span>                      | <span data-ttu-id="b4fd3-244">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-244">MM1</span></span>                        |
|     <span data-ttu-id="b4fd3-245">9</span><span class="sxs-lookup"><span data-stu-id="b4fd3-245">9</span></span>   |     +   |         | <span data-ttu-id="b4fd3-246">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-246">default</span></span> | <span data-ttu-id="b4fd3-247">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-247">default</span></span> | <span data-ttu-id="b4fd3-248">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-248">Error (multiple mappings)</span></span> | <span data-ttu-id="b4fd3-249">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-249">MM1</span></span>                        |
|    <span data-ttu-id="b4fd3-250">10</span><span class="sxs-lookup"><span data-stu-id="b4fd3-250">10</span></span>   | <span data-ttu-id="b4fd3-251">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-251">default</span></span> |         |         |         | <span data-ttu-id="b4fd3-252">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-252">MM1</span></span>                       | <span data-ttu-id="b4fd3-253">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-253">MM1</span></span>                        |
|    <span data-ttu-id="b4fd3-254">11</span><span class="sxs-lookup"><span data-stu-id="b4fd3-254">11</span></span>   | <span data-ttu-id="b4fd3-255">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-255">default</span></span> |    +    |         |         | <span data-ttu-id="b4fd3-256">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-256">MM1</span></span>                       | <span data-ttu-id="b4fd3-257">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-257">MM1</span></span>                        |
|    <span data-ttu-id="b4fd3-258">12</span><span class="sxs-lookup"><span data-stu-id="b4fd3-258">12</span></span>   | <span data-ttu-id="b4fd3-259">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-259">default</span></span> |         |    +    |         | <span data-ttu-id="b4fd3-260">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-260">MM1</span></span>                       | <span data-ttu-id="b4fd3-261">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-261">MM1</span></span>                        |
|    <span data-ttu-id="b4fd3-262">13</span><span class="sxs-lookup"><span data-stu-id="b4fd3-262">13</span></span>   | <span data-ttu-id="b4fd3-263">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-263">default</span></span> | <span data-ttu-id="b4fd3-264">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-264">default</span></span> |         |         | <span data-ttu-id="b4fd3-265">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-265">Error (multiple mappings)</span></span> | <span data-ttu-id="b4fd3-266">Villa (margar varpanir)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-266">Error (multiple mappings)</span></span>  |
|    <span data-ttu-id="b4fd3-267">14</span><span class="sxs-lookup"><span data-stu-id="b4fd3-267">14</span></span>   | <span data-ttu-id="b4fd3-268">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-268">default</span></span> |         | <span data-ttu-id="b4fd3-269">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-269">default</span></span> |         | <span data-ttu-id="b4fd3-270">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-270">MM1A</span></span>                      | <span data-ttu-id="b4fd3-271">MM1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-271">MM1</span></span>                        |
|    <span data-ttu-id="b4fd3-272">15</span><span class="sxs-lookup"><span data-stu-id="b4fd3-272">15</span></span>   | <span data-ttu-id="b4fd3-273">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-273">default</span></span> |         | <span data-ttu-id="b4fd3-274">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-274">default</span></span> | <span data-ttu-id="b4fd3-275">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-275">default</span></span> | <span data-ttu-id="b4fd3-276">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-276">MM1A</span></span>                      | <span data-ttu-id="b4fd3-277">MM2A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-277">MM2A</span></span>                       |
|    <span data-ttu-id="b4fd3-278">16</span><span class="sxs-lookup"><span data-stu-id="b4fd3-278">16</span></span>   |         |         |    +    |    +    | <span data-ttu-id="b4fd3-279">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-279">MM1A</span></span>                      | <span data-ttu-id="b4fd3-280">MM2A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-280">MM2A</span></span>                       |
|    <span data-ttu-id="b4fd3-281">17</span><span class="sxs-lookup"><span data-stu-id="b4fd3-281">17</span></span>   |         |         | <span data-ttu-id="b4fd3-282">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-282">default</span></span> | <span data-ttu-id="b4fd3-283">sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-283">default</span></span> | <span data-ttu-id="b4fd3-284">MM1A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-284">MM1A</span></span>                      | <span data-ttu-id="b4fd3-285">MM2A</span><span class="sxs-lookup"><span data-stu-id="b4fd3-285">MM2A</span></span>                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a><span data-ttu-id="b4fd3-286">Lærðu hvaða vörpun var notuð við framkvæmd ER sniðs</span><span class="sxs-lookup"><span data-stu-id="b4fd3-286">Learn what mapping was used in the execution of an ER format</span></span>

### <a name="configure-er-user-parameters"></a><span data-ttu-id="b4fd3-287">Skilgreina færibreytur notanda rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-287">Configure ER user parameters</span></span>

1.  <span data-ttu-id="b4fd3-288">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **CONFIGURATIONS**, velurðu **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-288">On the **Configurations** page, on the Action Pane, on the **CONFIGURATIONS** tab, select **User parameters**.</span></span>
2.  <span data-ttu-id="b4fd3-289">Stilltu valkostinn **Keyra í kembistillingum** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-289">Set the **Run in debug mode** option to **Yes**.</span></span>
4.  <span data-ttu-id="b4fd3-290">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-290">Select **Ok**.</span></span>

### <a name="run-the-configured-format"></a><span data-ttu-id="b4fd3-291">Keyra skilgreinint snið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-291">Run the configured format</span></span>

1.  <span data-ttu-id="b4fd3-292">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Snið til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-292">On the **Configurations** page, in the configurations tree, select **Format to learn mappings**.</span></span>
2.  <span data-ttu-id="b4fd3-293">Á flýtiflipanum **Útgáfur** velurðu **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-293">On the **Versions** FastTab, select **Run**.</span></span>
3.  <span data-ttu-id="b4fd3-294">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-294">Select **Ok**.</span></span>

### <a name="review-the-er-debug-log"></a><span data-ttu-id="b4fd3-295">Skoðaðu villuleitarskrá ER</span><span class="sxs-lookup"><span data-stu-id="b4fd3-295">Review the ER debug log</span></span>

1.  <span data-ttu-id="b4fd3-296">Farðu í **Einingar \> Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Kembingarkladdar skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-296">In the navigation pane, go to **Modules \> Organization administration \> Electronic reporting \> Configuration debug log**.</span></span>
2.  <span data-ttu-id="b4fd3-297">Veldu hnappinn **Endurhlaða þessa síðu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-297">Select the **Reload this page** button.</span></span>

![Síðan ER-keyrsluskrár](./media/RCS-Context-specific-mapping-DebugLog.PNG)

<span data-ttu-id="b4fd3-299">Taktu eftir að nýrri skrá hefur verið bætt við ER kembiforrit fyrir keyrð ER snið.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-299">Notice that a new record has been added to the ER debug log for the executed ER format.</span></span> <span data-ttu-id="b4fd3-300">Þar sem reiturinn **Stig** í þessari skrár er stilltur á **Upplýsingar** er skráin upplýsandi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-300">Because the **Level** field of this record is set to **Info**, the record is informational.</span></span> <span data-ttu-id="b4fd3-301">Þar sem reiturinn Sniðsíhlutur er stilltur á **Vörpunarstilling** upplýsir skráin þig um líkanavörpun sem var notuð við framkvæmd á ER-sniðinu **Snið til að læra vörpun** (valið í reitnum **Stillingarheiti**).</span><span class="sxs-lookup"><span data-stu-id="b4fd3-301">Because the Format component field is set to **Mapping configuration**, the record informs you about a model mapping that was used during execution of the **Format to learn mappings** ER format (selected in the **Configuration name** field).</span></span> <span data-ttu-id="b4fd3-302">Innihald reitsins **Myndaður texti** upplýsir þig um að vörpunarhlutinn **Vörpun (FR)** sem er staðsett í stillingunni **Vörpun (FR)** hefur verið notaður til að keyra þessa skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-302">The content of the **Generated text** field informs you that the **Mapping (FR)** mapping component that resides in the **Mapping (FR)** configuration has been used to run this report.</span></span>

## <a name="appendix1"></a> <span data-ttu-id="b4fd3-303">Viðauki 1</span><span class="sxs-lookup"><span data-stu-id="b4fd3-303">Appendix 1</span></span>

### <a name="configure-a-sample-data-model"></a><span data-ttu-id="b4fd3-304">Stilltu sýnishorn gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="b4fd3-304">Configure a sample data model</span></span>

<span data-ttu-id="b4fd3-305">Skráðu þig inn á RCS tilvikið.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-305">Sign in to your RCS instance.</span></span>

<span data-ttu-id="b4fd3-306">Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Til að ljúka þessum skrefum verður fyrst í RCS að ljúka skrefum ferlisins [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="b4fd3-306">In this example, you will create a configuration for sample company, Litware, Inc. To complete these steps, you must first complete, in RCS, the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

#### <a name="create-an-er-data-model-configuration"></a><span data-ttu-id="b4fd3-307">Stofna nýjan skilgreiningu ER-gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="b4fd3-307">Create an ER data model configuration</span></span>

1.  <span data-ttu-id="b4fd3-308">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-308">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="b4fd3-309">Veldu reitinn **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-309">Select the **Reporting configurations** tile.</span></span>
3.  <span data-ttu-id="b4fd3-310">Á síðunni **Skilgreiningar** skal velja **Stofna stillingu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-310">On the **Configurations** page, select **Create configuration**.</span></span>
4.  <span data-ttu-id="b4fd3-311">Í fellilistanum, í reitnum **Heiti**, slærðu inn **Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-311">In the drop-down dialog box, in the **Name** field, enter **Model to learn mappings**.</span></span>
5.  <span data-ttu-id="b4fd3-312">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-312">Select **Create configuration**.</span></span>
6.  <span data-ttu-id="b4fd3-313">Veldu flýtiflipann **Stillingarhlutar**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-313">Select the **Configuration components** FastTab.</span></span>

<span data-ttu-id="b4fd3-314">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-314">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="b4fd3-315">Þessi útgáfa inniheldur íhluta gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-315">This version contains the data model component.</span></span>

#### <a name="design-a-sample-data-model"></a><span data-ttu-id="b4fd3-316">Hanna sýnishorn gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="b4fd3-316">Design a sample data model</span></span>

1.  <span data-ttu-id="b4fd3-317">Á síðunni **Síðan skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-317">On the **Configurations page**, select **Designer**.</span></span>
2.  <span data-ttu-id="b4fd3-318">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-318">Select **New**.</span></span>
3.  <span data-ttu-id="b4fd3-319">Í fellilistanum, í reitnum **Heiti** slærðu inn **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-319">In the drop-down dialog box, in the **Name** field, enter **Entry point 1**.</span></span>
4.  <span data-ttu-id="b4fd3-320">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-320">Select **Add**.</span></span>
5.  <span data-ttu-id="b4fd3-321">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-321">Select **New**.</span></span>
6.  <span data-ttu-id="b4fd3-322">Í fellilistanum, í reitnum **Heiti**, slærðu inn **Lýsing á virkni**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-322">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
7.  <span data-ttu-id="b4fd3-323">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-323">Select **Add**.</span></span>
8.  <span data-ttu-id="b4fd3-324">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-324">Select **New**.</span></span>
9.  <span data-ttu-id="b4fd3-325">Í fellilistanum, í reitahópnum **Nýr hnútur**, velurðu **Líkanshnútur**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-325">In the drop-down dialog box, in the **New node** field group, select **Model root**.</span></span>
10. <span data-ttu-id="b4fd3-326">Í reitinn **Heiti** slærðu inn **Aðgangsstaður 2**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-326">In the **Name** field, enter **Entry point 2**.</span></span>
11. <span data-ttu-id="b4fd3-327">Veldu **Inngangsstaður 2**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-327">Select **Entry point 2**.</span></span>
12. <span data-ttu-id="b4fd3-328">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-328">Select **Add**.</span></span>
13. <span data-ttu-id="b4fd3-329">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-329">Select **New**.</span></span>
14. <span data-ttu-id="b4fd3-330">Í fellilistanum, í reitnum **Heiti**, slærðu inn **Lýsing á virkni**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-330">In the drop-down dialog box, in the **Name** field, enter **Functionality description**.</span></span>
15. <span data-ttu-id="b4fd3-331">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-331">Select **Add**.</span></span>

    ![Hönnuðarsíðan ER-gagnavörpun](./media/RCS-Context-specific-mapping-Model.PNG)

16. <span data-ttu-id="b4fd3-333">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-333">Select **Save**.</span></span>
17. <span data-ttu-id="b4fd3-334">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-334">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-configuration"></a><span data-ttu-id="b4fd3-335">Ljúka við breyttu útgáfuna af líkanastillingu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-335">Complete the modified version of the model configuration</span></span>

1.  <span data-ttu-id="b4fd3-336">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-336">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="b4fd3-337">Breyta stöðu hönnuðar líkanastillingar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að hanna nauðsynlegar varpanir og snið líkansins.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-337">Change the status of designed model configuration from **Draft** to **Completed**, so that it can be used to design the required model mappings and formats.</span></span>

2.  <span data-ttu-id="b4fd3-338">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-338">Select **Complete**.</span></span>
3.  <span data-ttu-id="b4fd3-339">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-339">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-340">Athugið að skilgreiningin sem þú stofnaðir er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-340">Notice that the configuration that you created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-model-mapping"></a><span data-ttu-id="b4fd3-341">Stilltu sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-341">Configure a sample model mapping</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="b4fd3-342">Stofna grunnstillingu ER-líkansvörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-342">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="b4fd3-343">Á síðunni **Skilgreiningar** skal velja **Stofna stillingu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-343">On the **Configurations** page, select **Create configuration**.</span></span>
2.  <span data-ttu-id="b4fd3-344">Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Líkanavörpun byggð á gagnalíkaninu Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-344">In the drop-down dialog box, in the **New** field group, select **Model mapping based on data model Model to learn mappings**.</span></span>
3.  <span data-ttu-id="b4fd3-345">Í reitinn **Heiti** slærðu inn **Vörpun (almennt)**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-345">In the **Name** field, enter **Mapping (General)**.</span></span>
4.  <span data-ttu-id="b4fd3-346">Í reitnum **Skilgreining gagnalíkans** velurðu **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-346">In the **Data model definition** field, select **Entry point 1**.</span></span>
5.  <span data-ttu-id="b4fd3-347">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-347">Select **Create configuration**.</span></span>

<span data-ttu-id="b4fd3-348">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-348">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="b4fd3-349">Þessi útgáfa inniheldur íhluta líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-349">This version contains the model mapping component.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="b4fd3-350">Hanna sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-350">Design a sample model mapping</span></span>

1.  <span data-ttu-id="b4fd3-351">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-351">On the **Configurations** page, select **Designer**.</span></span>

    <span data-ttu-id="b4fd3-352">Taktu eftir því að kortlagning líkansins á stefnugerðinni **Til líkans** hefur sjálfkrafa verið bætt við þennan íhlut fyrir skilgreininguna **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-352">Notice that the model mapping of the **To model** direction type has been automatically added to this component for the **Entry point 1** definition.</span></span>
    
2.  <span data-ttu-id="b4fd3-353">Veldu **Hönnuður** til að byrja að breyta viðbættri líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-353">Select **Designer** to start editing the added model mapping.</span></span>
3.  <span data-ttu-id="b4fd3-354">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-354">In the **Data model** section, select **Edit**.</span></span>
4.  <span data-ttu-id="b4fd3-355">Í reitinn **Formúla** skal færa inn **„Almenn virkni 1“**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-355">In the **Formula** field, enter **"Generic functionality 1"**.</span></span>
5.  <span data-ttu-id="b4fd3-356">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-356">Select **Save**.</span></span>
6.  <span data-ttu-id="b4fd3-357">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-357">Close the **Formula designer** page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  <span data-ttu-id="b4fd3-359">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-359">Select **Save**.</span></span>
8.  <span data-ttu-id="b4fd3-360">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-360">Close the **Model mapping designer** page.</span></span>
9.  <span data-ttu-id="b4fd3-361">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-361">Select **New**.</span></span>
10. <span data-ttu-id="b4fd3-362">Í reitnum **Skilgreining** velurðu **Aðgangsstaður 2**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-362">In the **Definition** field, select **Entry point 2**.</span></span>
11. <span data-ttu-id="b4fd3-363">Í reitinn **Heiti** slærðu inn **Vörpun (almennt) 2**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-363">In the **Name** field, enter **Mapping (General) 2**.</span></span>
12. <span data-ttu-id="b4fd3-364">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-364">Select **Designer**.</span></span>
13. <span data-ttu-id="b4fd3-365">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-365">In the **Data model** section, select **Edit**.</span></span>
14. <span data-ttu-id="b4fd3-366">Í reitinn **Formúla** skal færa inn **„Almenn virkni 2“**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-366">In the **Formula** field, enter **"Generic functionality 2"**.</span></span>
15. <span data-ttu-id="b4fd3-367">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-367">Select **Save**.</span></span>
16. <span data-ttu-id="b4fd3-368">Lokaðu síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-368">Close the **Formula designer** page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. <span data-ttu-id="b4fd3-370">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-370">Select **Save**.</span></span>
18. <span data-ttu-id="b4fd3-371">Lokið síðunni **Hönnuður líkanavörpunar**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-371">Close the **Model mapping designer** page.</span></span>

    ![Síðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. <span data-ttu-id="b4fd3-373">Lokið síðunni **Líkanavarpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-373">Close the **Model mappings** page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="b4fd3-374">Ljúka við breyttu útgáfuna af stillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-374">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="b4fd3-375">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-375">On the **Configurations page**, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="b4fd3-376">Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-376">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="b4fd3-377">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-377">Select **Complete**.</span></span>
3.  <span data-ttu-id="b4fd3-378">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-378">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-379">Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-379">Notice that the configuration that is created is saved as completed version 1.</span></span>

### <a name="configure-a-sample-format"></a><span data-ttu-id="b4fd3-380">Stilla sýnissnið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-380">Configure a sample format</span></span>

#### <a name="create-an-er-format-configuration"></a><span data-ttu-id="b4fd3-381">Stofna skilgreiningu ER-sniðs</span><span class="sxs-lookup"><span data-stu-id="b4fd3-381">Create an ER format configuration</span></span>

1.  <span data-ttu-id="b4fd3-382">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-382">On the **Configurations** page, in the configurations tree, select **Model to learn mappings**.</span></span>
2.  <span data-ttu-id="b4fd3-383">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-383">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="b4fd3-384">Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Sniðmát byggt á gagnalíkaninu Líkan til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-384">In the drop-down dialog box, in the **New** field group, select **Format based on data model Model to learn mappings**.</span></span>
4.  <span data-ttu-id="b4fd3-385">Í reitnum **Heiti** slærðu inn **Sniðmát til að læra varpanir**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-385">In the **Name** field, enter **Format to learn mappings**.</span></span>
5.  <span data-ttu-id="b4fd3-386">Í reitnum **Skilgreining gagnalíkans** velurðu **Aðgangsstaður 1**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-386">In the **Data model definition** field, select **Entry point 1**.</span></span>
6.  <span data-ttu-id="b4fd3-387">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-387">Select **Create configuration**.</span></span>

<span data-ttu-id="b4fd3-388">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-388">Notice that draft version 1 of this ER configuration is ready for editing.</span></span> <span data-ttu-id="b4fd3-389">Þessi útgáfa inniheldur íhluta sniðsins.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-389">This version contains the format component.</span></span>

#### <a name="design-a-sample-format"></a><span data-ttu-id="b4fd3-390">Hanna sýnissnið</span><span class="sxs-lookup"><span data-stu-id="b4fd3-390">Design a sample format</span></span>

1.  <span data-ttu-id="b4fd3-391">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-391">On the **Configurations** page, select **Designer**.</span></span>
2.  <span data-ttu-id="b4fd3-392">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-392">Select **Add root**.</span></span>
3.  <span data-ttu-id="b4fd3-393">Í hópnum **Texti** velurðu liðinn **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-393">In the **Text** group, select the **String** item.</span></span>
4.  <span data-ttu-id="b4fd3-394">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-394">Select **OK**.</span></span>

#### <a name="bind-format-elements-to-a-data-source"></a><span data-ttu-id="b4fd3-395">Binda sniðsþætti í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="b4fd3-395">Bind format elements to a data source</span></span>

1.  <span data-ttu-id="b4fd3-396">Á síðunni **Sniðahönnuður**, á flipanum **Vörpun**, stækkarðu gagnagjafa líkansins.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-396">On the **Format designer** page, on the **Mapping** tab, expand the model data source.</span></span>
2.  <span data-ttu-id="b4fd3-397">Veldu reitinn **Lýsing á virkni**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-397">Select the **Functionality description** field.</span></span>
3.  <span data-ttu-id="b4fd3-398">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-398">Select **Bind**.</span></span>

    ![Síða ER-sniðshönnuðar](./media/RCS-Context-specific-mapping-Format.PNG)

4.  <span data-ttu-id="b4fd3-400">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-400">Select **Save**.</span></span>
5.  <span data-ttu-id="b4fd3-401">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-401">Close the page.</span></span>

## <a name="appendix2"></a> <span data-ttu-id="b4fd3-402">Viðauki 2</span><span class="sxs-lookup"><span data-stu-id="b4fd3-402">Appendix 2</span></span>

### <a name="configure-a-sample-model-mapping-for-general-customization"></a><span data-ttu-id="b4fd3-403">Stilla vörpun sýnislíkans fyrir almenna sérstillingu</span><span class="sxs-lookup"><span data-stu-id="b4fd3-403">Configure a sample model mapping for general customization</span></span>

<span data-ttu-id="b4fd3-404">Þú gætir viljað sérsníða líkanavörpun sem stillingarveita (samstarfsaðili) gaf þér og notað síðan sérsniðna útgáfu sem gagnagjafa fyrir ER sniðin þín.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-404">You might want to customize a model mapping that a configuration provider (partner) provided to you, and then use the customized version as a data source for your ER formats.</span></span> <span data-ttu-id="b4fd3-405">Í þessu tilfelli verður þú að stofna sérsniðna vörpunarstillingu ER-líkans til að gera nauðsynlegar breytingar á fyrirliggjandi vörpun.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-405">In this case, you must create a custom ER model mapping configuration to make the required changes in existing model mappings.</span></span> <span data-ttu-id="b4fd3-406">Aðferðirnar í þessum viðbæti nota líkanavörpunina **Vörpun (almennt)** sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-406">The procedures in this appendix use the **Mapping (General)** model mapping as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="b4fd3-407">Stofna grunnstillingu ER-líkansvörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-407">Create an ER model mapping configuration</span></span>

1.  <span data-ttu-id="b4fd3-408">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt)**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-408">On the **Configurations** page, in the configurations tree, select **Mapping (General)**.</span></span>
2.  <span data-ttu-id="b4fd3-409">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-409">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="b4fd3-410">Í fellivalmyndinni í reitahópnum **Nýtt**, velurðu **Leiða af nafni: Vörpun (Almennt), Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-410">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General), Litware, Inc.**.</span></span>
4.  <span data-ttu-id="b4fd3-411">Í reitinn **Heiti** slærðu inn **Vörpun (almennt) sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-411">In the **Name** field, enter **Mapping (General) custom**.</span></span>
5.  <span data-ttu-id="b4fd3-412">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-412">Select **Create configuration**.</span></span>

<span data-ttu-id="b4fd3-413">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-413">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="b4fd3-414">Hanna sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-414">Design a sample model mapping</span></span>

1.  <span data-ttu-id="b4fd3-415">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-415">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="b4fd3-416">Taktu eftir því að líkanavarpanir grunnstillingarinnar eru sjálfkrafa afritaðar í þessa stillingu.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-416">Notice that the model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="b4fd3-417">Veldu vörpunina **Vörpun (almennt) afrit**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-417">Select the **Mapping (General) Copy** mapping.</span></span>
3.  <span data-ttu-id="b4fd3-418">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-418">Select **Designer**.</span></span>
4.  <span data-ttu-id="b4fd3-419">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-419">In the **Data model** section, select **Edit**.</span></span>
5.  <span data-ttu-id="b4fd3-420">Í reitinn **Formúla** skal færa inn **„Almenn virkni 1 sérsnið“**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-420">In the **Formula** field, enter **"Generic functionality 1 custom"**.</span></span>
6.  <span data-ttu-id="b4fd3-421">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-421">Select **Save**.</span></span>
7.  <span data-ttu-id="b4fd3-422">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-422">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  <span data-ttu-id="b4fd3-424">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-424">Select **Save**.</span></span>
9.  <span data-ttu-id="b4fd3-425">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-425">Close the page.</span></span>
10. <span data-ttu-id="b4fd3-426">Veldu vörpunina **Vörpun 2 (almennt) afrit**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-426">Select the **Mapping (General) 2 Copy** mapping.</span></span>
11. <span data-ttu-id="b4fd3-427">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-427">Select **Designer**.</span></span>
12. <span data-ttu-id="b4fd3-428">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-428">In the **Data model** section, select **Edit**.</span></span>
13. <span data-ttu-id="b4fd3-429">Í reitinn **Formúla** skal færa inn **„Almenn virkni 2 sérsnið“**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-429">In the **Formula** field, enter **"Generic functionality 2 custom"**.</span></span>
14. <span data-ttu-id="b4fd3-430">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-430">Select **Save**.</span></span>
15. <span data-ttu-id="b4fd3-431">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-431">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. <span data-ttu-id="b4fd3-433">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-433">Select **Save**.</span></span>
17. <span data-ttu-id="b4fd3-434">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-434">Close the page.</span></span>

    ![Síðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. <span data-ttu-id="b4fd3-436">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-436">Close the page.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="b4fd3-437">Ljúka við breyttu útgáfuna af stillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-437">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="b4fd3-438">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-438">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="b4fd3-439">Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-439">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="b4fd3-440">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-440">Select **Complete**.</span></span>
3.  <span data-ttu-id="b4fd3-441">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-441">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-442">Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-442">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="appendix3"></a> <span data-ttu-id="b4fd3-443">Viðauki 3</span><span class="sxs-lookup"><span data-stu-id="b4fd3-443">Appendix 3</span></span>

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a><span data-ttu-id="b4fd3-444">Stilla vörpun sýnislíkans fyrir lands-/landsvæðissértæka sérstillingu</span><span class="sxs-lookup"><span data-stu-id="b4fd3-444">Configure a sample model mapping for country/region-specific customization</span></span>

<span data-ttu-id="b4fd3-445">Fyrir sum ER snið geta verið lands-/svæðissértækar kröfur um undirbúning gagna.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-445">For some ER formats, there might be country/region-specific requirements for data preparation.</span></span> <span data-ttu-id="b4fd3-446">Í þessu tilfelli getur þú stjórnað sérstakri vörpun ER-líkana og einangrað framkvæmd þessara lands-/svæðisbundnu krafna frá almennri framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-446">In this case, you can manage a separate ER model mapping configuration and isolate the implementation of these country/region-specific requirements from the general implementation.</span></span> <span data-ttu-id="b4fd3-447">Ferlin í þessum viðauka nota ER-sniðið **Snið til að læra varpanir** og franskar sértækar kröfur sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-447">The procedures in this appendix use the **Format to learn mappings** ER format and French-specific requirements as an example.</span></span>

#### <a name="create-an-er-model-mapping-configuration"></a><span data-ttu-id="b4fd3-448">Stofna grunnstillingu ER-líkansvörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-448">Create an ER model mapping configuration</span></span>

<span data-ttu-id="b4fd3-449">Í fyrsta lagi skaltu búa til nýja stillingu ER-líkanavörpunar til að innleiða lands-/svæðisbundnar kröfur.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-449">First, create a new ER model mapping configuration to implement the country/region-specific requirements.</span></span> <span data-ttu-id="b4fd3-450">Notaðu sérsniðna stillingu ER-líkanavörpunar sem grunn.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-450">Use your custom ER model mapping configuration as a base.</span></span>

1.  <span data-ttu-id="b4fd3-451">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Vörpun (almennt) sérsnið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-451">On the **Configurations** page, in the configurations tree, select **Mapping (General) custom**.</span></span>
2.  <span data-ttu-id="b4fd3-452">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-452">Select **Create configuration**.</span></span>
3.  <span data-ttu-id="b4fd3-453">Í fellivalmyndinni í reitahópnum **Nýtt**, velurðu **Leiða af nafni: Vörpun (Almennt) sérsnið, Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-453">In the drop-down dialog box, in the **New** field group, select **Derive from Name: Mapping (General) custom, Litware, Inc**.</span></span>
4.  <span data-ttu-id="b4fd3-454">Í reitinn **Heiti** slærðu inn **Vörpun (FR)**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-454">In the **Name** field, enter **Mapping (FR)**.</span></span>
5.  <span data-ttu-id="b4fd3-455">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-455">Select **Create configuration**.</span></span>

<span data-ttu-id="b4fd3-456">Taktu eftir að drög að útgáfu 1 af þessari ER stillingu eru tilbúin til breytinga.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-456">Notice that draft version 1 of this ER configuration is ready for editing.</span></span>

#### <a name="design-a-sample-model-mapping"></a><span data-ttu-id="b4fd3-457">Hanna sýnishorn líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-457">Design a sample model mapping</span></span>

1.  <span data-ttu-id="b4fd3-458">Á síðunni **Skilgreiningar** skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-458">On the **Configurations** page, select **Designer**.</span></span>

    > <span data-ttu-id="b4fd3-459">Taktu eftir því að líkanavarpanir grunnstillingarinnar eru sjálfkrafa afritaðar í þessa stillingu.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-459">Notice that model mappings of the base configuration have been automatically copied to this configuration.</span></span>

2.  <span data-ttu-id="b4fd3-460">Veldu vörpunina **Vörpun (almennt) afrit afrit**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-460">Select the **Mapping (General) Copy Copy** mapping.</span></span>
3.  <span data-ttu-id="b4fd3-461">Endurnefndu hana **Vörpun (FR)**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-461">Rename it **Mapping (FR)**.</span></span>
4.  <span data-ttu-id="b4fd3-462">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-462">Select **Designer**.</span></span>
5.  <span data-ttu-id="b4fd3-463">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-463">In the **Data model** section, select **Edit**.</span></span>
6.  <span data-ttu-id="b4fd3-464">Í reitinn **Formúla** skal færa inn **„FR-virkni 1“**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-464">In the **Formula** field, enter **"FR functionality 1"**.</span></span>
7.  <span data-ttu-id="b4fd3-465">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-465">Select **Save**.</span></span>
8.  <span data-ttu-id="b4fd3-466">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-466">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  <span data-ttu-id="b4fd3-468">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-468">Select **Save**.</span></span>
10. <span data-ttu-id="b4fd3-469">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-469">Close the page.</span></span>
11. <span data-ttu-id="b4fd3-470">Veldu vörpunina **Vörpun 2 (almennt) afrit afrit**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-470">Select the **Mapping (General) 2 Copy Copy** mapping.</span></span>
12. <span data-ttu-id="b4fd3-471">Endurnefndu hana **Vörpun 2 (FR)**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-471">Rename it **Mapping (FR) 2**.</span></span>
13. <span data-ttu-id="b4fd3-472">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-472">Select **Designer**.</span></span>
14. <span data-ttu-id="b4fd3-473">Í hlutanum **Gagnalíkan** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-473">In the **Data model** section, select **Edit**.</span></span>
15. <span data-ttu-id="b4fd3-474">Í reitinn **Formúla** skal færa inn **„FR-virkni 2“**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-474">In the **Formula** field, enter **"FR functionality 2"**.</span></span>
16. <span data-ttu-id="b4fd3-475">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-475">Select **Save**.</span></span>
17. <span data-ttu-id="b4fd3-476">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-476">Close the page.</span></span>

    ![Hönnuðarsíðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. <span data-ttu-id="b4fd3-478">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-478">Select **Save**.</span></span>
19. <span data-ttu-id="b4fd3-479">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-479">Close the page.</span></span>

    ![Síðan ER-líkanavörpun](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. <span data-ttu-id="b4fd3-481">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-481">Close the page.</span></span>

#### <a name="specify-countryregion-context-restrictions-for-use"></a><span data-ttu-id="b4fd3-482">Tilgreindu lands-/svæðisbundnar samhengistakmarkanir fyrir notkun</span><span class="sxs-lookup"><span data-stu-id="b4fd3-482">Specify country/region context restrictions for use</span></span>

1.  <span data-ttu-id="b4fd3-483">Á síðunni **Skilgreiningar**, á flýtiflipanum **ISO lands-/svæðiskóðar** velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-483">On the **Configurations** page, on the **ISO Country/region codes** FastTab, select **New**.</span></span>
2.  <span data-ttu-id="b4fd3-484">Í reitnum **ISO** er valið **FR**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-484">In the **ISO** field, select **FR**.</span></span>
3.  <span data-ttu-id="b4fd3-485">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-485">Select **Save**.</span></span>

<span data-ttu-id="b4fd3-486">Athugaðu að þú verður að skrá þig inn á tiltekið fyrirtæki í Finance til að keyra ER-snið.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-486">Note that you must sign in to a specific company in Finance to run an ER format.</span></span> <span data-ttu-id="b4fd3-487">Þess vegna getur þetta fyrirtæki talist aðili sem stjórnar bæði framkvæmd ER-sniða og vali á réttri vörpun ER-líkans af ER-grunngagnalíkani.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-487">Therefore, this company can be considered a party that controls both ER format execution and selection of the correct ER model mapping of the base ER data model.</span></span> <span data-ttu-id="b4fd3-488">Með því að bæta við landskóðanum **FR** tilgreinirðu að vörpun líkansins er tiltæk til vals með ER sniði grunngagnalíkansins aðeins þegar það snið er keyrt undir stjórn fyrirtækis sem hefur franskt lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-488">By adding the **FR** country code, you specify that this model mapping is available for selection by an ER format of the base data model only when that format is run under the control of a company that has French country/region context.</span></span>

<span data-ttu-id="b4fd3-489">Þú getur bætt við mörgum lands-/svæðiskóðum fyrir staka útgáfu af stillingum á ER-líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-489">You can add multiple country/region codes for a single version of an ER model mapping configuration.</span></span> <span data-ttu-id="b4fd3-490">Þannig er hægt að nota líkanavarpanir sem búa í þeirri stillingu líkanavörpunar fyrir ER-snið sem er keyrt undir stjórn fyrirtækja sem hafa annað lands-/svæðissamhengi.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-490">In this way, model mappings that reside in that model mapping configuration can be used for an ER format that is run under the control of companies that have a different country/region context.</span></span>

<span data-ttu-id="b4fd3-491">Athugaðu að listinn yfir lands-/svæðisnúmer er tilgreindur fyrir hverja útgáfu af stillingum ER-líkanavörpunar og getur verið breytilegur frá einnu útgáfu til annarrar.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-491">Note that the list of country/region codes is specified for each version of an ER model mapping configuration and can vary from version to version.</span></span>

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a><span data-ttu-id="b4fd3-492">Ljúka við breyttu útgáfuna af stillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-492">Complete the modified version of the model mapping configuration</span></span>

1.  <span data-ttu-id="b4fd3-493">Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-493">On the **Configurations** page, on the **Versions** FastTab, select **Change status**.</span></span>

    > <span data-ttu-id="b4fd3-494">Breyta stöðu hönnuðar stillingar líkanavörpunar úr **Drög** í **Lokið** svo að hægt sé að nota hana til að í ER-sniðmátum.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-494">Change the status of designed model mapping configuration from **Draft** to **Completed**, so that it can be used by ER formats.</span></span>

2.  <span data-ttu-id="b4fd3-495">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-495">Select **Complete**.</span></span>
3.  <span data-ttu-id="b4fd3-496">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-496">Select **OK**.</span></span>

<span data-ttu-id="b4fd3-497">Athugið að skilgreiningin sem var stofnað er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-497">Notice that the configuration that is created is saved as completed version 1.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4fd3-498">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-498">Additional resources</span></span>

[<span data-ttu-id="b4fd3-499">Yfirlit yfir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="b4fd3-499">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b4fd3-500">Stjórna vörpunarlíkani rafrænnar skýrslugerðar í aðskilinni skilgreiningu rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-500">Manage ER model mapping in separate ER configurations</span></span>](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[<span data-ttu-id="b4fd3-501">Nota lands-/svæðistengt samhengi</span><span class="sxs-lookup"><span data-stu-id="b4fd3-501">Apply country/region context</span></span>](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="b4fd3-502">Algengar spurningar</span><span class="sxs-lookup"><span data-stu-id="b4fd3-502">Frequently asked questions</span></span>

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a><span data-ttu-id="b4fd3-503">Ég stillti tvær sameiginlegar stillingar ER-líkanavörpunar í RCS og merkti eina þeirra sem sjálfgefna stillingu líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-503">I configured two shared ER model mapping configurations in RCS and marked one of them as the default model mapping configuration.</span></span> <span data-ttu-id="b4fd3-504">Mér tókst að keyra ER-snið sem var búið til fyrir sömu grunngerð ER-gagnalíkanastillingar, til að prófa líkanavörpun.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-504">I successfully ran an ER format that was created for the same base ER data model configuration, to test model mappings.</span></span> <span data-ttu-id="b4fd3-505">Síðan flutti ég inn alla ER-lausnina (ER-gagnalíkan, tvær stillingar ER-líkanavarpana og stillingar á ER-sniði) í Finance.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-505">I then imported the whole ER solution (ER data model, two ER model mapping configurations, and ER format configuration) into Finance.</span></span> <span data-ttu-id="b4fd3-506">Af hverju fæ ég villuboð þegar ég reyni að keyra sama ER-snið í Finance?</span><span class="sxs-lookup"><span data-stu-id="b4fd3-506">Why do I receive an error message when I try to run the same ER format in Finance?</span></span>
<span data-ttu-id="b4fd3-507">Sjálfgefin stilling líkanavörpunar er umhverfissértæk.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-507">The default model mapping setting is environment-specific.</span></span> <span data-ttu-id="b4fd3-508">Hún er stillt í RCS en er ekki flutt til Finance.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-508">It's configured in RCS but isn't exported to Finance.</span></span> <span data-ttu-id="b4fd3-509">Til að keyra þetta ER-snið verður þú að merkja eina af stillingum ER-líkanavörpunar sem sjálfgefna stillingu líkanavörpunar í Finance líka.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-509">To successfully run this ER format, you must mark one of ER model mapping configurations as the default model mapping configuration in Finance too.</span></span>

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a><span data-ttu-id="b4fd3-510">Ég stillti eina líkanavörpun sem samnýtta líkanavörpun og kláraði drög að útgáfu hennar.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-510">I configured one model mapping as a shared model mapping and completed the draft version of it.</span></span> <span data-ttu-id="b4fd3-511">Síðan bætti ég við nýrri gerð stillingar líkanavörpunar fyrir sama gagnalíkan og stillti það sem fransk-sértækt.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-511">I then added a new model mapping configuration for same data model and configured it as French-specific.</span></span> <span data-ttu-id="b4fd3-512">Hvers vegna er sameiginleg líkanavörpun valin þegar ég keyri ER-snið, jafnvel þó að þetta ER-snið noti réttar rótarskilgreiningar og framkvæmd er gerð undir stjórn fyrirtækisins sem hefur franskt lands-/svæðissamhengi?</span><span class="sxs-lookup"><span data-stu-id="b4fd3-512">Why is the shared model mapping selected when I run an ER format, even though this ER format uses the correct root definition and execution is done under the control of the company that has French country/region context?</span></span>
<span data-ttu-id="b4fd3-513">Gakktu úr skugga um að samnýtta stilling líkanavörpunar sé ekki merkt sem sjálfgefin stilling líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-513">Make sure that the shared model mapping configuration isn't marked as the default model mapping configuration.</span></span> <span data-ttu-id="b4fd3-514">Annars mun það hafa meiri forgang við val á vörpun.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-514">Otherwise, it will have higher priority during mapping selection.</span></span> <span data-ttu-id="b4fd3-515">Gakktu einnig úr skugga um að stillt sé á franskar sértækar stillingar líkanavörpunar þegar vörpun er valin við framkvæmd ER sniðs.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-515">Also make sure that the French-specific model mapping configuration is considered when a mapping is selected during ER format execution.</span></span> <span data-ttu-id="b4fd3-516">Stillingar á ER-líkanavörpun er aðeins tiltæk til vals ef að minnsta kosti eitt af eftirfarandi skilyrðum er uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="b4fd3-516">An ER model mapping configuration is available for selection only if at least one of the following conditions is met:</span></span>
- <span data-ttu-id="b4fd3-517">Að minnsta kosti ein útgáfa af stilligum ER-líkanavörpunar hefur annaðhvort stöðuna **Lokið** eða **Deilt**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-517">At least one version of the ER model mapping configuration has either **Completed** or **Shared** status.</span></span> <span data-ttu-id="b4fd3-518">Í þessu tilfelli verður útgáfan sem er með hæsta útgáfunúmerið notuð við framkvæmd ER sniðs.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-518">In this case, the version that has the highest version number will be used for ER format execution.</span></span>
- <span data-ttu-id="b4fd3-519">Kveikt er á valkostinum **Keyra drög** fyrir stillingu ER-líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-519">The **Run draft** option for the ER model mapping configuration is turned on.</span></span> <span data-ttu-id="b4fd3-520">Í þessu tilfelli verður útgáfan sem er með stöðuna **Drög** notuð við framkvæmd ER sniðs.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-520">In this case, the version that has **Draft** status will be used for ER format execution.</span></span>
> <span data-ttu-id="b4fd3-521">Valkosturinn **Keyra drög** verður í boði á síðunni **Stillingar** fyrir sérhverja stillingu ER-líkanavörpunar þegar kveikt er á ER-færibreytu notanda **Keyra stillingu**.</span><span class="sxs-lookup"><span data-stu-id="b4fd3-521">The **Run draft** option becomes available on the **Configurations** page for each ER model mapping configuration when the **Run setting** ER user parameter is turned on.</span></span>
