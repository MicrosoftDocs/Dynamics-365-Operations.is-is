---
title: Flytja inn skilgreiningu úr Lifecycle Services
description: Í þessu efni er útskýrt hvernig á að flytja inn nýja útgáfu af skilgreiningu rafrænnar skýrslugerðar úr Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 674d0dc02b4a53e455a15a06fdb7f24ca3036ba3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752365"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="ff2ab-103">Flytja inn skilgreiningu úr Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ff2ab-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff2ab-104">Þetta efnisatriði útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur flutt inn nýja útgáfu af [Skilgreiningarsnið fyrir rafræna skýrslugerð (ER)](../general-electronic-reporting.md#Configuration) úr [Eignasafn á verkefnastigi](../../lifecycle-services/asset-library.md) í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ff2ab-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="ff2ab-105">Í þessu dæmi velurðu þá útgáfu af skilgreiningu fyrir Rafræna skýrslugerð sem þér hugnast, og flytur hana inn fyrir sýnifyrirtæki sem kallast Litware, Inc. Þessum skrefum má ljúka í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="ff2ab-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í [Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ff2ab-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="ff2ab-107">Aðgangur að LCS er einnig nauðsynlegur.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="ff2ab-108">Skráðu þig inn í forritið með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="ff2ab-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="ff2ab-109">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="ff2ab-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="ff2ab-110">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="ff2ab-110">System administrator</span></span>

2. <span data-ttu-id="ff2ab-111">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="ff2ab-112">Velja **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="ff2ab-113">Ganga skal úr skugga um að núverandi Dynamics 365 Finance notandi sé aðili að LCS-verki sem inniheldur eignasafnið sem notandinn vill fá [aðgang](../../lifecycle-services/asset-library.md#asset-library-support) að til að flytja inn skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="ff2ab-114">Ekki er hægt að opna LCS-verk úr rafrænni gagnageymslu sem stendur fyrir annað lén en lénið sem er notað í Finance.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="ff2ab-115">Ef það er reynt verður tæmandi listi yfir LCS-verk sýndur og ekki er hægt að flytja inn skilgreiningar rafrænnar skýrslugerðar úr verkstigi eignasafns í LCS.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="ff2ab-116">Til að fá aðgang að eignasöfnum verks úr geymslu sem er notuð til að flytja inn skilgreining rafrænnar skýrslugerðar skal skrá sig inn í Finance með því að nota skilríki notanda sem tilheyrir leigjandanum (léninu) sem gildandi Finance tilviki hefur verið úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="ff2ab-117">Eyða samnýttri útgáfu skilgreiningar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="ff2ab-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="ff2ab-118">Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Dæmi um skilgreiningu líkans**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="ff2ab-119">Fyrsta útgáfa af stillingum sýnigagnalíkansins var stofnuð og birt í LCS þegar lokið var við skrefin í [Hlaða skilgreiningu upp í Lifecycle Services fyrir rafræna skýrslugerð](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ff2ab-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="ff2ab-120">Í þessu ferli muntu eyða þeirri útgáfu á skilgreiningu rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="ff2ab-121">Þú munt síðan flytja inn þá útgáfu úr LCS síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="ff2ab-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ff2ab-123">Í þessu dæmi skal velja útgáfu þessarar skilgreiningar sem hefur stöðuna **Samnýtt**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="ff2ab-124">Þessi staða tilgreinir að skilgreiningin sé nú birt í LCS.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="ff2ab-125">Veljið **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-125">Select **Change status**.</span></span>
4. <span data-ttu-id="ff2ab-126">Veldu **Hætta**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="ff2ab-127">Með því að breyta stöðu valinnar útgáfu úr **Samnýtt** í **Hætt** er hægt að eyða einingunni.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="ff2ab-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-128">Select **OK**.</span></span>
6. <span data-ttu-id="ff2ab-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ff2ab-130">Í þessu dæmi skal velja útgáfu skilgreiningarinnar sem hefur stöðuna **Hætt**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="ff2ab-131">Veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-131">Select **Delete**.</span></span>
8. <span data-ttu-id="ff2ab-132">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-132">Select **Yes**.</span></span>

    <span data-ttu-id="ff2ab-133">Athugið að einu drögin að útgáfu 2 af hinni völdu skilgreiningu gagnalíkans eru nú tiltæk.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="ff2ab-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="ff2ab-135">Flytja inn samnýttu útgáfu skilgreiningar gagnalíkans úr LCS</span><span class="sxs-lookup"><span data-stu-id="ff2ab-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="ff2ab-136">Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="ff2ab-137">Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="ff2ab-138">Í **Litware, Inc.** reitnum, skal velja **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="ff2ab-139">Nú getur þú opnað lista yfir gagnasöfn fyrir skilgreiningarveitur fyrir Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="ff2ab-140">Veljið **Opna**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-140">Select **Open**.</span></span>

    <span data-ttu-id="ff2ab-141">Veldu **LCS**-gagnasafnið í þessu dæmi og opnaðu það.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="ff2ab-142">Þú verður að vera með [aðgang](#accessconditions) að LCS-verkinu og eignasafninu sem er opnað með því að velja ER-gagnageymsluna.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="ff2ab-143">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="ff2ab-144">Í þessu dæmi skal velja fyrstu útgáfu af **Dæmi um líkanaskilgreiningu** á útgáfulistanum.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="ff2ab-145">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-145">Select **Import**.</span></span>
7. <span data-ttu-id="ff2ab-146">Veldu **Já** til að staðfesta innflutning valda útgáfu úr LCS.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="ff2ab-147">Upplýsingaskilaboð staðfesta að valin útgáfa hafi verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="ff2ab-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-148">Close the page.</span></span>
9. <span data-ttu-id="ff2ab-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-149">Close the page.</span></span>
10. <span data-ttu-id="ff2ab-150">Velja **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="ff2ab-151">Veljið **Dæmi um skilgreiningu líkans** í trénu.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="ff2ab-152">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ff2ab-153">Í þessu dæmi skal velja útgáfu þessarar skilgreiningar sem hefur stöðuna **Samnýtt**.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="ff2ab-154">Athugið að samnýtt útgáfa 1 hinnar völdu skilgreiningar gagnalíkans er nú tiltæk.</span><span class="sxs-lookup"><span data-stu-id="ff2ab-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]