---
title: Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar
description: Í þessu efnisatriði er útskýrt hvernig á að flytja inn uppfærðar útgáfur af Skilgreiningum rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
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
ms.openlocfilehash: 0c65315c4fa6a42b4bbb0d008b58f8df9cc0ea3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561879"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="5c1fe-103">Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c1fe-104">[Geymslur](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar eru notaðar til að samnýta [Skilgreiningar rafrænnar skýrslugerðar](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="5c1fe-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="5c1fe-105">Hægt er að [flytja inn](download-electronic-reporting-configuration-lcs.md) skilgreiningar rafrænnar skýrslugerðar úr öðrum geymslum og yfir í tilvikið þitt af Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="5c1fe-106">Þegar skilgreiningar rafrænnar skýrslugerðar eru fluttar inn, geta [skilgreiningarveitur](general-electronic-reporting.md#Provider) gefið út nýjar [útgáfur](general-electronic-reporting.md#component-versioning) af geymslum þannig að hægt sé að deila þeim.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="5c1fe-107">Í þessu efnisatriði er útskýrt hvernig á að flytja inn uppfærðar útgáfur af Skilgreiningum rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="5c1fe-108">Frekari upplýsingar er að finna í [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Skilgreiningarþjónusta](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="5c1fe-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="5c1fe-109">Yfirfara tiltækar uppfærðar útgáfur</span><span class="sxs-lookup"><span data-stu-id="5c1fe-109">Review the available updated versions</span></span>

1. <span data-ttu-id="5c1fe-110">Skráði ykkur inn í Fjármál með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="5c1fe-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="5c1fe-111">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="5c1fe-112">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5c1fe-113">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="5c1fe-113">System administrator</span></span>

2. <span data-ttu-id="5c1fe-114">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="5c1fe-115">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Flytja inn uppfærslur fyrir skilgreiningarútgáfur**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Skilgreiningasíða staðfæringar](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="5c1fe-117">Í svarglugganum **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar**, í reitnum **Keyrsluháttur** skal velja **Sýna aðeins uppfærslur sem eru í boði**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="5c1fe-118">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-118">Then select **OK**.</span></span> 

    ![Reitur keyrsluháttar stilltur á Sýna aðeins uppfærslur sem eru í boði](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="5c1fe-120">Farið yfir skilaboðin sem berast.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-120">Review the messages that you receive.</span></span> <span data-ttu-id="5c1fe-121">Þessi skilaboð veita eftirfarandi upplýsingar um skilgreiningar rafrænnar skýrslugerðar í núverandi Fjármálatilviki og hvernig það er í samanburði við efnið í altæku geymslunni:</span><span class="sxs-lookup"><span data-stu-id="5c1fe-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="5c1fe-122">Heildarfjöldi skilgreininga rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="5c1fe-123">Skilgreiningar rafrænnar skýrslugerðar sem eru ekki til staðar í altæku geymslunni</span><span class="sxs-lookup"><span data-stu-id="5c1fe-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="5c1fe-124">Skilgreiningar rafrænnar skýrslugerðar þar sem nýjasta útgáfan er þegar í boði í núverandi Fjármálatilviki (Til að skoða heildarlistann yfir þessar skilgreiningar rafrænnar skýrslugerðar skal velja tengilinn **Upplýsingar um skilaboð**.)</span><span class="sxs-lookup"><span data-stu-id="5c1fe-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![„Nýjustu útgáfur eftirfarandi skilgreininga hafa þegar verið fluttar inn“ skilaboðin og upplýsingar um skilaboð](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="5c1fe-126">Skilgreiningar rafrænnar skýrslugerðar þar sem nýjasta útgáfan er í boði í altæku geymslunni og hægt er að flytja inn í núverandi Fjármálatilvik (Til að skoða heildarlistann yfir þessar skilgreiningar rafrænnar skýrslugerðar skal velja tengilinn **Upplýsingar um skilaboð**.)</span><span class="sxs-lookup"><span data-stu-id="5c1fe-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![„Uppfærslur í boði“ skilaboð og upplýsingar um skilaboð](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="5c1fe-128">Flytja inn uppfærðar útgáfur í boði</span><span class="sxs-lookup"><span data-stu-id="5c1fe-128">Import available updated versions</span></span>

1. <span data-ttu-id="5c1fe-129">Skráði ykkur inn í Fjármál með því að nota eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="5c1fe-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="5c1fe-130">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="5c1fe-131">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="5c1fe-132">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="5c1fe-132">System administrator</span></span>

2. <span data-ttu-id="5c1fe-133">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="5c1fe-134">Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Flytja inn uppfærslur fyrir skilgreiningarútgáfur**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="5c1fe-135">Í svarglugganum **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar**, í reitnum **Keyrsluháttur**, skal velja **Flytja inn nýjustu uppfærslurnar** til að flytja inn nýjustu útgáfur skilgreininga rafrænnar skýrslugerðar úr altæku geymslunni og yfir í núverandi Fjármálatilvik.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="5c1fe-136">Til að áætla runuvinnslu fyrir innflutninginn, í flýtiflipanum **Keyra í bakgrunni**, skal stilla valkostinn **Runuvinnsla** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="5c1fe-137">Ef ætlunin er að endurtaka innflutninginn reglulega skal skilgreina nauðsynlega endurtekningu.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Reitur keyrsluháttar stilltur á Flytja inn nýjustu uppfærslur](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="5c1fe-139">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-139">Select **OK**.</span></span>
7. <span data-ttu-id="5c1fe-140">Til að fá upplýsingar um það hvaða skilgreiningarútgáfur hafa verið fluttar inn skal fylgja einu af þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="5c1fe-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="5c1fe-141">Ef verið er að keyra innflutninginn gagnvirkt í stað þess að nota runuvinnslu, skal yfirfara skilaboðin sem eru móttekin.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Skilaboð sem berast við gagnvirka innflutningskeyrslu](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="5c1fe-143">Fylgdu þessum skrefum ef þú keyrir innflutninginn í runustillingu:</span><span class="sxs-lookup"><span data-stu-id="5c1fe-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="5c1fe-144">Farið í **Almennt** \> **Fyrirspurnir** \> **Runuvinnslur** \> **Mínar runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="5c1fe-145">Finnið og veljið verkið **Flytja inn uppfærslur fyrir skilgreiningarútgáfur rafrænnar skýrslugerðar** og síðan, á aðgerðasvæðinu, í flipanum **Runuvinnsla**, skal velja **Runuvinnsluferill** til að skoða verkferilinn.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="5c1fe-146">Á síðunni **Runuvinnsluferill** skal velja **Kladdi**.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="5c1fe-147">Því næst, í skilaboðunum sem birtast, skal velja tengilinn **Upplýsingar um skilaboð** til að skoða verkkladdann.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Verkkladdi](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="5c1fe-149">Ekki er mælt með því að áætla endurtekna runuvinnsla til að flytja inn uppfærðar útgáfur af skilgreiningum rafrænnar skýrslugerðar beint úr altæku geymslunni og yfir í vinnsluumhverfi, því að innfluttar útgáfur verður hægt að nota um leið.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="5c1fe-150">Þess í stað skal nota þessa nálgun til að setja upp útgáfur af skilgreiningum rafrænnar skýrslugerðar í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="5c1fe-151">Hægt er að meta þær í sandkassaumhverfinu áður en þær eru virkjaðar í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="5c1fe-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c1fe-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5c1fe-152">Additional resources</span></span>

- [<span data-ttu-id="5c1fe-153">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="5c1fe-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="5c1fe-154">Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu</span><span class="sxs-lookup"><span data-stu-id="5c1fe-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]