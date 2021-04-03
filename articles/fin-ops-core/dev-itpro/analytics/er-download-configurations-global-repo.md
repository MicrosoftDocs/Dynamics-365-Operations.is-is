---
title: Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu
description: Í þessu efnisatriði er útskýrt hvernig á að sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c4f083163db72569d91825819a904319a0fe3123
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561903"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="6507b-103">Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu</span><span class="sxs-lookup"><span data-stu-id="6507b-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6507b-104">Í þessu efnisatriði er útskýrt hvernig á að sækja [Skilgreiningar rafrænnar skýrslugerðar](general-electronic-reporting.md#Configuration) úr altækri geymslu skilgreiningarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="6507b-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="6507b-105">Frekari upplýsingar er að finna í [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Skilgreiningarþjónusta](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="6507b-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="6507b-106">Opna gagnageymslur skilgreininga</span><span class="sxs-lookup"><span data-stu-id="6507b-106">Open configurations repository</span></span>

1. <span data-ttu-id="6507b-107">Skráðu þig inn í Dynamics 365 Finance-forritið með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="6507b-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="6507b-108">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="6507b-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="6507b-109">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6507b-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6507b-110">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="6507b-110">System administrator</span></span>

2. <span data-ttu-id="6507b-111">Fara í **Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="6507b-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="6507b-112">Í **veitandi skilgreininga** hlutanum, veljið gluggareitinn **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="6507b-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="6507b-113">Í reitnum **Microsoft** skal velja **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="6507b-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Vinnusvæði rafrænnar skýrslugerðar](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="6507b-115">Á síðunni **Gagnageymslur skilgreininga**, í hnitanetinu, skal velja fyrirliggjandi gagnageymslu af gerðinni **LCS**.</span><span class="sxs-lookup"><span data-stu-id="6507b-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="6507b-116">Ef þessi gagnasafn birtist ekki í hnitanetinu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="6507b-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="6507b-117">Smellið á **Bæta við** til að bæta við nýrri gagnageymslu.</span><span class="sxs-lookup"><span data-stu-id="6507b-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="6507b-118">Veljið **Altæk** sem gagngeymslugerð og veljið síðan **Búa til gagnageymslu**.</span><span class="sxs-lookup"><span data-stu-id="6507b-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="6507b-119">Ef beðið er um það skal fylgja heimildarleiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="6507b-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="6507b-120">Sláið inn heiti og lýsingu fyrir gagnageymsluna og veljið síðan **Í lagi** til að staðfesta nýju gagnageymslufærsluna.</span><span class="sxs-lookup"><span data-stu-id="6507b-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="6507b-121">Í hnitanetinu skal velja nýja gagnageymslu af gerðinni **Altæk**.</span><span class="sxs-lookup"><span data-stu-id="6507b-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="6507b-122">Smellið á **Opna** til að skoða lista yfir skilgreiningar rafrænnar skýrslugerðar fyrir valda gagnageymslu.</span><span class="sxs-lookup"><span data-stu-id="6507b-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Gagnageymslusíða skilgreininga](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="6507b-124">Flytja inn eina skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="6507b-124">Import a single configuration</span></span>

1. <span data-ttu-id="6507b-125">Á síðunni **Gagnageymslur skilgreininga**, í grunnstillingatrénu, skal velja skilgreiningu rafrænnar skýrslugerðar sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6507b-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="6507b-126">Á flýtiflipanum **Útgáfur** skal velja nauðsynlega útgáfu skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="6507b-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="6507b-127">Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.</span><span class="sxs-lookup"><span data-stu-id="6507b-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6507b-128">Hnappurinn **Flytja inn** er ekki tiltækur fyrir útgáfur skilgreininga rafrænnar skýrslugerðar sem þegar eru til staðar í núverandi fjármálatilviki.</span><span class="sxs-lookup"><span data-stu-id="6507b-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Síðan Skilgreiningagagnasafn](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="6507b-130">Flytja inn síaðar skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="6507b-130">Import filtered configurations</span></span>

1. <span data-ttu-id="6507b-131">Á síðunni **Gagnageymslur skilgreininga**, í grunnstillingatrénu, skal stækka flýtiflipann **Sía**.</span><span class="sxs-lookup"><span data-stu-id="6507b-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="6507b-132">Í hnitanetinu **Merki** skal bæta við öllum nauðsynlegum merkjum.</span><span class="sxs-lookup"><span data-stu-id="6507b-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="6507b-133">Í reitnum **Land/svæði sem við á** skal velja viðeigandi lands-/svæðiskóði og síðan velja **Nota síu**.</span><span class="sxs-lookup"><span data-stu-id="6507b-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6507b-134">Flýtiflipinn **Skilgreiningar** sýnir allar skilgreiningar sem uppfylla tilgreind skilyrði vals.</span><span class="sxs-lookup"><span data-stu-id="6507b-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="6507b-135">Í flýtiflipanum **Skilgreiningar** skal velja **Flytja inn** til að sækja síaðar skilgreiningar úr altæku geymslunni í núverandi tilvik.</span><span class="sxs-lookup"><span data-stu-id="6507b-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="6507b-136">Í flýtiflipanum **Skilgreiningar** skal velja **Endurstilla síu** til að hreinsa tilgreind skilyrði vals.</span><span class="sxs-lookup"><span data-stu-id="6507b-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Síðan Skilgreiningagagnasafn](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="6507b-138">Það fer eftir stillingum rafrænnar skýrslugerðar hvernig skilgreiningar eru villuleitaðar eftir að þær eru fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="6507b-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="6507b-139">Notandi gæti verið látinn vita um vandamál ósamræmi sem fundust.</span><span class="sxs-lookup"><span data-stu-id="6507b-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="6507b-140">Áður en hægt er að nota innflutta útgáfu skilgreingar þarf að leysa úr vandamálunum.</span><span class="sxs-lookup"><span data-stu-id="6507b-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="6507b-141">Frekari upplýsingar er að finna í lista yfir tengd tilföng í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="6507b-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="6507b-142">Hægt er að stilla skilgreiningar rafrænnar skýrslugerðar sem háðar öðrum skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="6507b-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="6507b-143">Þess vegna, ásamt valdri skilgreiningu, verða aðrar skilgreiningar hugsanlega fluttar inn sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="6507b-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="6507b-144">Meira um tengsl skilgreininga er að finna í [Skilgreina hversu mikil áhrif skilgreiningar rafrænnar skýrslugerðar hafa á aðra hluta](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="6507b-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6507b-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6507b-145">Additional resources</span></span>

[<span data-ttu-id="6507b-146">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="6507b-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]