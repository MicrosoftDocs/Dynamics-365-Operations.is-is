---
title: Hlaða upp skilgreiningu í Lifecycle Services
description: Í þessu efnisatriði er útskýrt hvernig á að stofna nýja skilgreiningu rafrænnar skýrslugerðar og hlaða hana upp í Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270560"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="f947b-103">Hlaða upp skilgreiningu í Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f947b-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f947b-104">Þetta efnisatriði útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað [Skilgreiningarsnið fyrir rafræna skýrslugerð (ER)](../general-electronic-reporting.md#Configuration) og hlaðið því upp í [Eignasafn á verkefnastigi](../../lifecycle-services/asset-library.md) í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f947b-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f947b-105">Verið er að [úrelda](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) notkun LCS sem gagnageymslu fyrir skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f947b-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="f947b-106">Frekari upplýsingar er að finna í [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="f947b-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="f947b-107">Í þessu dæmi stofnarðu skilgreiningu og hleður henni upp í LCS fyrir sýnifyrirtæki sem kallast Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="f947b-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="f947b-108">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í [Stofna skilgreiningarveitendur og merkja þá sem virka](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f947b-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="f947b-109">Aðgangur að LCS er einnig nauðsynlegur.</span><span class="sxs-lookup"><span data-stu-id="f947b-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="f947b-110">Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="f947b-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="f947b-111">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="f947b-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="f947b-112">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f947b-112">System administrator</span></span>

2. <span data-ttu-id="f947b-113">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="f947b-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f947b-114">Veljið **Litware, Inc.** og merkið það sem **Virkt**.</span><span class="sxs-lookup"><span data-stu-id="f947b-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="f947b-115">Velja **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f947b-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="f947b-116">Ganga skal úr skugga um að núverandi Dynamics 365 Finance notandi sé aðili að LCS-verki sem inniheldur [Eignasafnið](../../lifecycle-services/asset-library.md#asset-library-support) sem er notað til að flytja inn skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="f947b-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="f947b-117">Ekki er hægt að opna LCS-verk úr rafrænni gagnageymslu sem stendur fyrir annað lén en lénið sem er notað í Finance.</span><span class="sxs-lookup"><span data-stu-id="f947b-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="f947b-118">Ef það er reynt verður tæmandi listi yfir LCS-verk sýndur og ekki er hægt að flytja inn skilgreiningar rafrænnar skýrslugerðar úr verkstigi eignasafns í LCS.</span><span class="sxs-lookup"><span data-stu-id="f947b-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="f947b-119">Til að fá aðgang að eignasöfnum verks úr geymslu sem er notuð til að flytja inn skilgreining rafrænnar skýrslugerðar skal skrá sig inn í Finance með því að nota skilríki notanda sem tilheyrir leigjandanum (léninu) sem gildandi Finance tilviki hefur verið úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="f947b-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="f947b-120">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="f947b-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="f947b-121">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f947b-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f947b-122">Í **Skilgreiningar** skal velja **Stofna skilgreiningu** til að opna fellilistagluggann.</span><span class="sxs-lookup"><span data-stu-id="f947b-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f947b-123">Í þessu dæmi muntu stofna skilgreiningu sem inniheldur dæmi um gagnalíkan fyrir rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="f947b-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="f947b-124">Skilgreining gagnalíkans verður hlaðið upp í LCS síðar.</span><span class="sxs-lookup"><span data-stu-id="f947b-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="f947b-125">Í svæðið **Heiti** skal færa inn **Dæmi um skilgreining líkans**.</span><span class="sxs-lookup"><span data-stu-id="f947b-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="f947b-126">Í svæðið **Lýsing** skal færa **Dæmi um líkanaskilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="f947b-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="f947b-127">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="f947b-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="f947b-128">Veljið **Hönnuður líkana**.</span><span class="sxs-lookup"><span data-stu-id="f947b-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="f947b-129">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f947b-129">Select **New**.</span></span>
8. <span data-ttu-id="f947b-130">Í reitinn **Heiti** skal færa inn **Aðgangsstaður**.</span><span class="sxs-lookup"><span data-stu-id="f947b-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="f947b-131">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f947b-131">Select **Add**.</span></span>
10. <span data-ttu-id="f947b-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f947b-132">Select **Save**.</span></span>
11. <span data-ttu-id="f947b-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f947b-133">Close the page.</span></span>
12. <span data-ttu-id="f947b-134">Veljið **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="f947b-134">Select **Change status**.</span></span>
13. <span data-ttu-id="f947b-135">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="f947b-135">Select **Complete**.</span></span>
14. <span data-ttu-id="f947b-136">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f947b-136">Select **OK**.</span></span>
15. <span data-ttu-id="f947b-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f947b-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="f947b-138">Skrá nýtt gagnasafn</span><span class="sxs-lookup"><span data-stu-id="f947b-138">Register a new repository</span></span>

1. <span data-ttu-id="f947b-139">Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="f947b-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="f947b-140">Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="f947b-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="f947b-141">Í **Litware, Inc.** reitnum, skal velja **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="f947b-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="f947b-142">Nú getur þú opnað lista yfir gagnasöfn fyrir skilgreiningarveitur fyrir Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f947b-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="f947b-143">Veljið **Bæta við** til að opna fellilistagluggann.</span><span class="sxs-lookup"><span data-stu-id="f947b-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f947b-144">Nú er hægt að bæta við nýrri gagnageymslu.</span><span class="sxs-lookup"><span data-stu-id="f947b-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="f947b-145">Í reitnum **færa inn gagnasafn fyrir skilgreiningar** skal velja **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f947b-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="f947b-146">Veljið **Stofna geymslu**.</span><span class="sxs-lookup"><span data-stu-id="f947b-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="f947b-147">Færa inn eða veljið gildi í svæðinu **Verk**.</span><span class="sxs-lookup"><span data-stu-id="f947b-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="f947b-148">Í þessu dæmi skal velja viðeigandi LCS-verk.</span><span class="sxs-lookup"><span data-stu-id="f947b-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="f947b-149">Þú verður að hafa [aðgang](#accessconditions) að verkinu.</span><span class="sxs-lookup"><span data-stu-id="f947b-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="f947b-150">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f947b-150">Select **OK**.</span></span>

    <span data-ttu-id="f947b-151">Ljúka við nýja færslu í gagnasafni.</span><span class="sxs-lookup"><span data-stu-id="f947b-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="f947b-152">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f947b-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="f947b-153">Í þessu dæmi skal velja **LCS-færslu** gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="f947b-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="f947b-154">Athugið að skráð geymsla er merkt af núverandi veitu.</span><span class="sxs-lookup"><span data-stu-id="f947b-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="f947b-155">Með öðrum orðum er aðeins hægt að setja upp skilgreiningar sem eru í eigu viðkomandi veitu í þessa geymslu og hlaða þeim upp í valið LCS-verk.</span><span class="sxs-lookup"><span data-stu-id="f947b-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="f947b-156">Veljið **Opna**.</span><span class="sxs-lookup"><span data-stu-id="f947b-156">Select **Open**.</span></span>

    <span data-ttu-id="f947b-157">Þú opnar gagnasafn til að skoða lista yfir skilgreiningar Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f947b-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="f947b-158">Ef valið verk hefur ekki enn verið notað fyrir samnýtingu á skilgreiningum rafrænnar skýrslugerðar er listinn auður.</span><span class="sxs-lookup"><span data-stu-id="f947b-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="f947b-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f947b-159">Close the page.</span></span>
12. <span data-ttu-id="f947b-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f947b-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="f947b-161">Hlaða skilgreiningu upp í LCS</span><span class="sxs-lookup"><span data-stu-id="f947b-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="f947b-162">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="f947b-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f947b-163">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Dæmi um skilgreiningu líkans**.</span><span class="sxs-lookup"><span data-stu-id="f947b-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="f947b-164">Þú verður að velja stofnaða skilgreiningu sem þegar hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="f947b-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="f947b-165">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f947b-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f947b-166">Í þessu dæmi skal velja útgáfu þessarar skilgreiningar sem hefur stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="f947b-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="f947b-167">Veljið **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="f947b-167">Select **Change status**.</span></span>
5. <span data-ttu-id="f947b-168">Veldu **Deila**.</span><span class="sxs-lookup"><span data-stu-id="f947b-168">Select **Share**.</span></span>

    <span data-ttu-id="f947b-169">Stöðu skilgreiningar er breytt úr **Lokið** í **Samnýtt** þegar skilgreiningin er birt í LCS.</span><span class="sxs-lookup"><span data-stu-id="f947b-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="f947b-170">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f947b-170">Select **OK**.</span></span>
7. <span data-ttu-id="f947b-171">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f947b-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f947b-172">Í þessu dæmi skal velja skilgreiningarútgáfu sem hefur stöðuna **Samnýtt**.</span><span class="sxs-lookup"><span data-stu-id="f947b-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="f947b-173">Athugið að staða valda útgáfu hefur breyst úr **Lokið** í **Samnýttar**.</span><span class="sxs-lookup"><span data-stu-id="f947b-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="f947b-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f947b-174">Close the page.</span></span>
9. <span data-ttu-id="f947b-175">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="f947b-175">Select **Repositories**.</span></span>

    <span data-ttu-id="f947b-176">Nú getur þú opnað lista yfir gagnasöfn fyrir skilgreiningarveitur fyrir Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f947b-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="f947b-177">Veljið **Opna**.</span><span class="sxs-lookup"><span data-stu-id="f947b-177">Select **Open**.</span></span>

    <span data-ttu-id="f947b-178">Veldu **LCS**-gagnasafnið í þessu dæmi og opnaðu það.</span><span class="sxs-lookup"><span data-stu-id="f947b-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="f947b-179">Athugið að valin skilgreining er sýnd sem eign valins LCS verks.</span><span class="sxs-lookup"><span data-stu-id="f947b-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="f947b-180">Opnaðu LCS með því að fara á <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="f947b-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="f947b-181">Opna verk sem var notað áður fyrir geymsluskráningu.</span><span class="sxs-lookup"><span data-stu-id="f947b-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="f947b-182">Opnið eignasafnið fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="f947b-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="f947b-183">Veljið eignagerðin **GER-skilgreining**.</span><span class="sxs-lookup"><span data-stu-id="f947b-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="f947b-184">Skilgreining rafrænnar skýrslugerðar sem var hlaðið upp ætti að vera á listanum.</span><span class="sxs-lookup"><span data-stu-id="f947b-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="f947b-185">Athugaðu að upphalaðri LCS skilgreiningu er hægt að flytja inn í annað tilvik ef veiturnar hafa aðgang að þessu LCS verki.</span><span class="sxs-lookup"><span data-stu-id="f947b-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
